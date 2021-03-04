---
title: Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą
description: Šioje temoje pateikta informacija apie tai, kaip kurti projektų šablonus naudojant pasirinktinį veiksmą Kopijuoti projektą.
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 87696b41db20e9ec70270c850d9acfe05df8cd84
ms.sourcegitcommit: d5004acb6f1c257b30063c873896fdea92191e3b
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 01/22/2021
ms.locfileid: "5045019"
---
# <a name="develop-project-templates-with-copy-project"></a>Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

„Dynamics 365 Project Operations“ palaiko galimybę nukopijuoti projektą ir atšaukti bet kokius priskyrimus, kad būtų naudojami bendrieji ištekliai, atspindintys vaidmenį. Naudodami šią funkciją klientai gali kurti pagrindinių projektų šablonus.

Pasirinkus **Kopijuoti projektą**, tikslinio projekto būsena atnaujinama. Naudokite **būsenos tipą**, kad nustatytumėte, kada kopijavimo veiksmas yra baigtas. Pasirinkus **Kopijuoti projektą** taip pat projekto pradžios data atnaujinama į dabartinę pradžios datą, jei tikslinio projekto objekte neaptikta tikslinė data.

## <a name="copy-project-custom-action"></a>Pasirinktinis veiksmas Kopijuoti projektą 

### <a name="name"></a>Pavadinimas / vardas, pavardė 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>Įvesties parametrai
Yra trys įvesties parametrai.

| Parametras          | Tipas   | Reikšmės                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** arba **{"clearTeamsAndAssignments":true}** |
| SourceProject      | Objekto nuoroda | Šaltinio projektas |
| Tikslinis objektas             | Objekto nuoroda | Tikslinis projektas |


- **{"clearTeamsAndAssignments":true}**: numatytas „Project“, skirto žiniatinkliui, veikimas, bus pašalinti visi priskyrimai ir komandos nariai.
- **{"removeNamedResources":true}**: numatytasis „Project Operations“ veikimas, priskyrimai bus atkurti į bendruosius išteklius.

Daugiau informacijos apie veiksmus žr. [Žiniatinklio API veiksmai](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions).

## <a name="specify-fields-to-copy"></a>Kopijuotinų laukų nurodymas 
Kai veiksmas iškviečiamas, funkcija **Kopijuoti projektą** ieškos projekto rodinyje **Kopijuoti projekto stulpelius** ir nustatys, kuriuos laukus kopijuoti, kai projektas kopijuojamas.


### <a name="example"></a>Pavyzdžiui
Toliau pateiktame pavyzdyje parodyta, kaip iškviesti pasirinktinį veiksmą **CopyProject** naudojant parametrų rinkinį **removeNamedResources**.
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```
