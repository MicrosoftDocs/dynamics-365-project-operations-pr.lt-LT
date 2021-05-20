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
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949824"
---
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="28ee2-103">Projektų šablonų kūrimas naudojant veiksmą Kopijuoti projektą</span><span class="sxs-lookup"><span data-stu-id="28ee2-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="28ee2-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="28ee2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="28ee2-105">„Dynamics 365 Project Operations“ palaiko galimybę nukopijuoti projektą ir atšaukti bet kokius priskyrimus, kad būtų naudojami bendrieji ištekliai, atspindintys vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="28ee2-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="28ee2-106">Naudodami šią funkciją klientai gali kurti pagrindinių projektų šablonus.</span><span class="sxs-lookup"><span data-stu-id="28ee2-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="28ee2-107">Pasirinkus **Kopijuoti projektą**, tikslinio projekto būsena atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="28ee2-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="28ee2-108">Naudokite **būsenos tipą**, kad nustatytumėte, kada kopijavimo veiksmas yra baigtas.</span><span class="sxs-lookup"><span data-stu-id="28ee2-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="28ee2-109">Pasirinkus **Kopijuoti projektą** taip pat projekto pradžios data atnaujinama į dabartinę pradžios datą, jei tikslinio projekto objekte neaptikta tikslinė data.</span><span class="sxs-lookup"><span data-stu-id="28ee2-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="28ee2-110">Pasirinktinis veiksmas Kopijuoti projektą</span><span class="sxs-lookup"><span data-stu-id="28ee2-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="28ee2-111">Pavadinimas / vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="28ee2-111">Name</span></span> 

<span data-ttu-id="28ee2-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="28ee2-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="28ee2-113">Įvesties parametrai</span><span class="sxs-lookup"><span data-stu-id="28ee2-113">Input parameters</span></span>
<span data-ttu-id="28ee2-114">Yra trys įvesties parametrai.</span><span class="sxs-lookup"><span data-stu-id="28ee2-114">There are three input parameters:</span></span>

| <span data-ttu-id="28ee2-115">Parametras</span><span class="sxs-lookup"><span data-stu-id="28ee2-115">Parameter</span></span>          | <span data-ttu-id="28ee2-116">Tipas</span><span class="sxs-lookup"><span data-stu-id="28ee2-116">Type</span></span>   | <span data-ttu-id="28ee2-117">Reikšmės</span><span class="sxs-lookup"><span data-stu-id="28ee2-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="28ee2-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="28ee2-118">ProjectCopyOption</span></span>  | <span data-ttu-id="28ee2-119">String</span><span class="sxs-lookup"><span data-stu-id="28ee2-119">String</span></span> | <span data-ttu-id="28ee2-120">**{"removeNamedResources":true}** arba **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="28ee2-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="28ee2-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="28ee2-121">SourceProject</span></span>      | <span data-ttu-id="28ee2-122">Objekto nuoroda</span><span class="sxs-lookup"><span data-stu-id="28ee2-122">Entity Reference</span></span> | <span data-ttu-id="28ee2-123">Šaltinio projektas</span><span class="sxs-lookup"><span data-stu-id="28ee2-123">Source Project</span></span> |
| <span data-ttu-id="28ee2-124">Tikslinis objektas</span><span class="sxs-lookup"><span data-stu-id="28ee2-124">Target</span></span>             | <span data-ttu-id="28ee2-125">Objekto nuoroda</span><span class="sxs-lookup"><span data-stu-id="28ee2-125">Entity Reference</span></span> | <span data-ttu-id="28ee2-126">Tikslinis projektas</span><span class="sxs-lookup"><span data-stu-id="28ee2-126">Target Project</span></span> |


- <span data-ttu-id="28ee2-127">**{"clearTeamsAndAssignments":true}**: numatytas „Project“, skirto žiniatinkliui, veikimas, bus pašalinti visi priskyrimai ir komandos nariai.</span><span class="sxs-lookup"><span data-stu-id="28ee2-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="28ee2-128">**{"removeNamedResources":true}**: numatytasis „Project Operations“ veikimas, priskyrimai bus atkurti į bendruosius išteklius.</span><span class="sxs-lookup"><span data-stu-id="28ee2-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="28ee2-129">Daugiau informacijos apie veiksmus žr. [Žiniatinklio API veiksmai](/powerapps/developer/common-data-service/webapi/use-web-api-actions).</span><span class="sxs-lookup"><span data-stu-id="28ee2-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="28ee2-130">Kopijuotinų laukų nurodymas</span><span class="sxs-lookup"><span data-stu-id="28ee2-130">Specify fields to copy</span></span> 
<span data-ttu-id="28ee2-131">Kai veiksmas iškviečiamas, funkcija **Kopijuoti projektą** ieškos projekto rodinyje **Kopijuoti projekto stulpelius** ir nustatys, kuriuos laukus kopijuoti, kai projektas kopijuojamas.</span><span class="sxs-lookup"><span data-stu-id="28ee2-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="28ee2-132">Pavyzdžiui</span><span class="sxs-lookup"><span data-stu-id="28ee2-132">Example</span></span>
<span data-ttu-id="28ee2-133">Toliau pateiktame pavyzdyje parodyta, kaip iškviesti pasirinktinį veiksmą **CopyProject** naudojant parametrų rinkinį **removeNamedResources**.</span><span class="sxs-lookup"><span data-stu-id="28ee2-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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


[!INCLUDE[footer-include](../includes/footer-banner.md)]