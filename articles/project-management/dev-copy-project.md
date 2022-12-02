---
title: Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą
description: Šiame straipsnyje pateikta informacija apie tai, kaip kurti projektų šablonus naudojant pasirinktinį veiksmą Kopijuoti projektą.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 47c1023bbc4c21e3571bffbf3670bf0f7854f81d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923842"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ palaiko galimybę nukopijuoti projektą ir atšaukti bet kokius priskyrimus, kad būtų naudojami bendrieji ištekliai, atspindintys vaidmenį. Naudodami šią funkciją klientai gali kurti pagrindinių projektų šablonus.

Pasirinkus **Kopijuoti projektą**, tikslinio projekto būsena atnaujinama. Naudokite **būsenos tipą**, kad nustatytumėte, kada kopijavimo veiksmas yra baigtas. Pasirinkus **Kopijuoti projektą** taip pat projekto pradžios data atnaujinama į dabartinę pradžios datą, jei tikslinio projekto objekte neaptikta tikslinė data.

## <a name="copy-project-custom-action"></a>Pasirinktinis veiksmas Kopijuoti projektą

### <a name="name"></a>Pavadinimą 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>Įvesties parametrai

Yra trys įvesties parametrai.

- **ReplaceNamedResources** arba **ClearTeamsAndAssignments** – nustatykite tik vieną iš šių parinkčių. Nenustatykite abiejų.

    - **\{"ReplaceNamedResources":true\}** – numatytasis „Project Operations“ veikimo būdas. Visi įvardytieji ištekliai pakeičiami bendraisiais ištekliais.
    - **\{"ClearTeamsAndAssignments":true\}** – numatytasis žiniatinklio „Project for the Web“ veikimo būdas. Visi priskyrimai ir komandos nariai pašalinami.

- **SourceProject** – šaltinio projekto, iš kurio reikia kopijuoti, objekto nuoroda. Šis parametras negali būti nulinis.
- **Target** – tikslinio projekto, į kurį reikia kopijuoti, objekto nuoroda. Šis parametras negali būti nulinis.

Toliau pateiktoje lentelėje pateikta šių trijų parametrų suvestinė.

| Parametras                | Tipas             | Vertė                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Bulio logikos          | **Teisinga** arba **Klaidinga** |
| ClearTeamsAndAssignments | Bulio logikos          | **Teisinga** arba **Klaidinga** |
| SourceProject            | Objekto nuoroda | Šaltinio projektas    |
| Target                   | Objekto nuoroda | Tikslinis projektas    |

Daugiau informacijos apie veiksmus žr. [Žiniatinklio API veiksmai](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Tikrinimai

Atliekami toliau nurodyti tikrinimai.

1. Naudojant nulines reikšmes tikrinami ir nuskaitomi šaltinio ir tikslinis projektai, kad būtų patvirtintas abiejų projektų egzistavimą organizacijoje.
2. Sistema tikrina, ar tikslinis projektas tinkamas kopijuoti, patikrindama šias sąlygas:

    - Su projektu neatliekamos ankstesnės veiklos (įskaitant skirtuko **Užduotys** parinkimą) ir projektas yra naujai sukurtas.
    - Nėra ankstesnės kopijos, neprašoma šio projekto importuoti, projekto būsena nėra **Nepavyko**.

3. Operacija neiškviečiama naudojant HTTP.

## <a name="specify-fields-to-copy"></a>Kopijuotinų laukų nurodymas

Kai veiksmas iškviečiamas, funkcija **Kopijuoti projektą** ieškos projekto rodinyje **Kopijuoti projekto stulpelius** ir nustatys, kuriuos laukus kopijuoti, kai projektas kopijuojamas.

### <a name="example"></a>Pavyzdžiui

Toliau pateiktame pavyzdyje parodyta, kaip iškviesti pasirinktinį veiksmą **CopyProjectV3** naudojant parametrų rinkinį **removeNamedResources**.

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
