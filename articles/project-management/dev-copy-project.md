---
title: Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą
description: Šioje temoje pateikta informacija apie tai, kaip kurti projektų šablonus naudojant pasirinktinį veiksmą Kopijuoti projektą.
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590908"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ palaiko galimybę nukopijuoti projektą ir atšaukti bet kokius priskyrimus, kad būtų naudojami bendrieji ištekliai, atspindintys vaidmenį. Naudodami šią funkciją klientai gali kurti pagrindinių projektų šablonus.

Pasirinkus **Kopijuoti projektą**, tikslinio projekto būsena atnaujinama. Naudokite **būsenos tipą**, kad nustatytumėte, kada kopijavimo veiksmas yra baigtas. Pasirinkus **Kopijuoti projektą** taip pat projekto pradžios data atnaujinama į dabartinę pradžios datą, jei tikslinio projekto objekte neaptikta tikslinė data.

## <a name="copy-project-custom-action"></a>Pasirinktinis veiksmas Kopijuoti projektą

### <a name="name"></a>Pavadinimą 

msdyn\_ CopyProjectV3

### <a name="input-parameters"></a>Įvesties parametrai

Yra trys įvesties parametrai.

- **ReplaceNamedResources** arba **ClearTeamsAndAssignments** – nustatykite tik vieną iš parinkčių. Nenustatykite abiejų.

    - **\{"ReplaceNamedResources":true\}** – numatytasis "Project Operations" veikimo būdas. Visi pavadinti ištekliai pakeičiami bendraisiais ištekliais.
    - **\{"ClearTeamsAndAssignments":true\}** – numatytasis "Project for the Web" veikimo būdas. Visos užduotys ir komandos nariai pašalinami.

- **SourceProject** – šaltinio projekto, iš kurio kopijuojama, objekto nuoroda. Šis parametras negali būti neapibrėžtas.
- **Tikslas** – tikslinio projekto, į kurį norite kopijuoti, objekto nuoroda. Šis parametras negali būti neapibrėžtas.

Šioje lentelėje pateikiama trijų parametrų santrauka.

| Parametras                | Tipas             | Vertė                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | Bulio logikos          | **Teisinga** arba **klaidinga** |
| ClearTeamsAndAssignments | Bulio logikos          | **Teisinga** arba **klaidinga** |
| SourceProject            | Objekto nuoroda | Šaltinio projektas    |
| Vertimas                   | Objekto nuoroda | Tikslinis projektas    |

Daugiau numatytųjų veiksmų ypatybių ieškokite [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions).

### <a name="validations"></a>Tikrinimą

Atliekami šie patvirtinimai.

1. Null tikrina ir nuskaito šaltinio ir tikslinius projektus, kad patvirtintų abiejų projektų buvimą organizacijoje.
2. Sistema patvirtina, kad tikslinis projektas galioja kopijavimui, patikrinusi šias sąlygas:

    - Projekte nėra ankstesnės veiklos (įskaitant skirtuko **Užduotys** pasirinkimą) ir projektas kuriamas naujai.
    - Nėra ankstesnės kopijos, šiame projekte nebuvo pareikalauta importuoti, o projekto būsena **nepavyko**.

3. Operacija neiškviečiama naudojant HTTP.

## <a name="specify-fields-to-copy"></a>Kopijuotinų laukų nurodymas

Kai veiksmas iškviečiamas, funkcija **Kopijuoti projektą** ieškos projekto rodinyje **Kopijuoti projekto stulpelius** ir nustatys, kuriuos laukus kopijuoti, kai projektas kopijuojamas.

### <a name="example"></a>Pavyzdžiui

Toliau pateiktame pavyzdyje parodyta, kaip iškviesti pasirinktinį veiksmą **CopyProjectV3** su **parametrų rinkiniu RemoveNamedResources**.

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
