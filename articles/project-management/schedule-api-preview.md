---
title: Grafiko API naudojimas norint atlikti operacijas su grafiko objektais
description: Šioje temoje pateikiama informacija ir pavyzdžiai, kaip naudoti grafiko API.
author: sigitac
manager: Annbe
ms.date: 04/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e03f4e6c49a835206b23cade3fabe3fd26693441
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950814"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="6ad49-103">Grafiko API naudojimas norint atlikti operacijas su grafiko objektais</span><span class="sxs-lookup"><span data-stu-id="6ad49-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="6ad49-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="6ad49-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="6ad49-105">Kai kurios arba visos šioje temoje paminėtos funkcijos pasiekiamos kaip peržiūros versijos leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="6ad49-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="6ad49-106">Turinys ir funkcijos gali keistis.</span><span class="sxs-lookup"><span data-stu-id="6ad49-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="6ad49-107">Grafiko objektai</span><span class="sxs-lookup"><span data-stu-id="6ad49-107">Scheduling entities</span></span>

<span data-ttu-id="6ad49-108">Grafiko API suteikia galimybę atlikti kūrimo, naujinimo ir naikinimo operacijas naudojant **grafiko objektus**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="6ad49-109">Šie objektai valdomi naudojant „Project for the Web“ planavimo variklį.</span><span class="sxs-lookup"><span data-stu-id="6ad49-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="6ad49-110">Ankstesniuose „Dynamics 365 Project Operations“ leidimuose operacijų kūrimas, naujinimas ir naikinimas naudojant **planavimo objektus** buvo apribotas.</span><span class="sxs-lookup"><span data-stu-id="6ad49-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="6ad49-111">Toliau esančioje lentelėje pateikiamas visas **planavimo objektų** sąrašas.</span><span class="sxs-lookup"><span data-stu-id="6ad49-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="6ad49-112">Objekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-112">Entity name</span></span>  | <span data-ttu-id="6ad49-113">Loginis objekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="6ad49-114">Project</span><span class="sxs-lookup"><span data-stu-id="6ad49-114">Project</span></span> | <span data-ttu-id="6ad49-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="6ad49-115">msdyn_project</span></span> |
| <span data-ttu-id="6ad49-116">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="6ad49-116">Project Task</span></span>  | <span data-ttu-id="6ad49-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="6ad49-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="6ad49-118">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="6ad49-118">Project Task Dependency</span></span>  | <span data-ttu-id="6ad49-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="6ad49-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="6ad49-120">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-120">Resource Assignment</span></span> | <span data-ttu-id="6ad49-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="6ad49-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="6ad49-122">Projekto talpykla</span><span class="sxs-lookup"><span data-stu-id="6ad49-122">Project Bucket</span></span>  | <span data-ttu-id="6ad49-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="6ad49-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="6ad49-124">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="6ad49-124">Project Team Member</span></span> | <span data-ttu-id="6ad49-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="6ad49-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="6ad49-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="6ad49-126">OperationSet</span></span>

<span data-ttu-id="6ad49-127">OperationSet yra darbo vieneto modelis, kurį galima naudoti, kai operacijoje reikia apdoroti keletą grafikui poveikį darančių užklausų.</span><span class="sxs-lookup"><span data-stu-id="6ad49-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="6ad49-128">Grafiko API</span><span class="sxs-lookup"><span data-stu-id="6ad49-128">Schedule APIs</span></span>

<span data-ttu-id="6ad49-129">Toliau pateikiamas dabartinių grafiko API sąrašas.</span><span class="sxs-lookup"><span data-stu-id="6ad49-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="6ad49-130">**msdyn_CreateProjectV1**: šį API galima naudoti norint sukurti projektą.</span><span class="sxs-lookup"><span data-stu-id="6ad49-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="6ad49-131">Projektas ir numatytoji projekto talpykla sukuriami nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="6ad49-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="6ad49-132">**msdyn_CreateTeamMemberV1**:šį API galima naudoti norint sukurti projekto komandos narį.</span><span class="sxs-lookup"><span data-stu-id="6ad49-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="6ad49-133">Komandos nario įrašas sukuriamas nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="6ad49-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="6ad49-134">**msdyn_CreateOperationSetV1**: šį API galima naudoti norint suplanuoti keletą užklausų, kurias reikia atlikti operacijoje.</span><span class="sxs-lookup"><span data-stu-id="6ad49-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="6ad49-135">**msdyn_PSSCreateV1**: šį API galima naudoti norint sukurti objektą.</span><span class="sxs-lookup"><span data-stu-id="6ad49-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="6ad49-136">Objektu gali būti bet kuris iš planavimo objektų, palaikančių kūrimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="6ad49-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="6ad49-137">**msdyn_PSSUpdateV1**: šį API galima naudoti norint atnaujinti objektą.</span><span class="sxs-lookup"><span data-stu-id="6ad49-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="6ad49-138">Objektu gali būti bet kuris iš planavimo objektų, palaikančių naujinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="6ad49-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="6ad49-139">**msdyn_PSSDeleteV1**: šį API galima naudoti norint panaikinti objektą.</span><span class="sxs-lookup"><span data-stu-id="6ad49-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="6ad49-140">Objektu gali būti bet kuris iš planavimo objektų, palaikančių naikinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="6ad49-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="6ad49-141">**msdyn_ExecuteOperationSetV1**: šis API naudojamas norint vykdyti visas nurodyto operacijų rinkinio operacijas.</span><span class="sxs-lookup"><span data-stu-id="6ad49-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="6ad49-142">Grafiko API naudojimas kartu su OperationSet</span><span class="sxs-lookup"><span data-stu-id="6ad49-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="6ad49-143">Kadangi įrašai, naudojant **CreateProjectV1** ir **CreateTeamMemberV1**, sukuriami nedelsiant, šių API negalima naudoti tiesiai **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="6ad49-144">Tačiau API galite naudoti norėdami sukurti reikiamus įrašus, **OperationSet**, tada šiuos iš anksto sukurtus įrašus panaudoti **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="6ad49-145">Palaikomos operacijos</span><span class="sxs-lookup"><span data-stu-id="6ad49-145">Supported operations</span></span>

| <span data-ttu-id="6ad49-146">Grafiko objektas</span><span class="sxs-lookup"><span data-stu-id="6ad49-146">Scheduling entity</span></span> | <span data-ttu-id="6ad49-147">Kūrimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-147">Create</span></span> | <span data-ttu-id="6ad49-148">Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-148">Update</span></span> | <span data-ttu-id="6ad49-149">Delete</span><span class="sxs-lookup"><span data-stu-id="6ad49-149">Delete</span></span> | <span data-ttu-id="6ad49-150">Svarbi informacija</span><span class="sxs-lookup"><span data-stu-id="6ad49-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="6ad49-151">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="6ad49-151">Project task</span></span> | <span data-ttu-id="6ad49-152">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-152">Yes</span></span> | <span data-ttu-id="6ad49-153">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-153">Yes</span></span> | <span data-ttu-id="6ad49-154">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-154">Yes</span></span> | <span data-ttu-id="6ad49-155">Nėra</span><span class="sxs-lookup"><span data-stu-id="6ad49-155">None</span></span> |
| <span data-ttu-id="6ad49-156">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="6ad49-156">Project task dependency</span></span> | <span data-ttu-id="6ad49-157">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-157">Yes</span></span> | <span data-ttu-id="6ad49-158">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-158">Yes</span></span> | | <span data-ttu-id="6ad49-159">Projekto užduoties priklausomybės įrašai neatnaujinami.</span><span class="sxs-lookup"><span data-stu-id="6ad49-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="6ad49-160">Vietoj to, seną įrašą galima panaikinti ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="6ad49-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="6ad49-161">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-161">Resource assignment</span></span> | <span data-ttu-id="6ad49-162">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-162">Yes</span></span> | <span data-ttu-id="6ad49-163">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-163">Yes</span></span> | | <span data-ttu-id="6ad49-164">Nepalaikomos operacijos, kurioms naudojami šie laukai: **BookableResourceID**, **Pastangos**, **EffortCompleted**, **EffortRemaining** ir **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="6ad49-165">Išteklių priskyrimo įrašai neatnaujinami.</span><span class="sxs-lookup"><span data-stu-id="6ad49-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="6ad49-166">Vietoj to, seną įrašą galima panaikinti ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="6ad49-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="6ad49-167">Projekto talpykla</span><span class="sxs-lookup"><span data-stu-id="6ad49-167">Project bucket</span></span> | <span data-ttu-id="6ad49-168">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="6ad49-168">N/A</span></span> | <span data-ttu-id="6ad49-169">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="6ad49-169">N/A</span></span> | <span data-ttu-id="6ad49-170">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="6ad49-170">N/A</span></span> | <span data-ttu-id="6ad49-171">Numatytoji talpykla sukuriama naudojant **CreateProjectV1** API.</span><span class="sxs-lookup"><span data-stu-id="6ad49-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="6ad49-172">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="6ad49-172">Project team member</span></span> | <span data-ttu-id="6ad49-173">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-173">Yes</span></span> | <span data-ttu-id="6ad49-174">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-174">Yes</span></span> | <span data-ttu-id="6ad49-175">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-175">Yes</span></span> | <span data-ttu-id="6ad49-176">Kūrimo operacijai naudokite **CreateTeamMemberV1** API.</span><span class="sxs-lookup"><span data-stu-id="6ad49-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="6ad49-177">Project</span><span class="sxs-lookup"><span data-stu-id="6ad49-177">Project</span></span> | <span data-ttu-id="6ad49-178">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-178">Yes</span></span> | <span data-ttu-id="6ad49-179">Taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-179">Yes</span></span> | <span data-ttu-id="6ad49-180">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="6ad49-180">N/A</span></span> | <span data-ttu-id="6ad49-181">Nepalaikomos operacijos, kurioms naudojami šie laukai: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Pastangos**, **EffortCompleted**, **EffortRemaining**, **Eiga**, **Pabaiga**, **TaskEarliestStart** ir **Duration**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="6ad49-182">Šias API galima iškviesti naudojant objektus, kuriuose įtraukti pasirinktini laukai.</span><span class="sxs-lookup"><span data-stu-id="6ad49-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="6ad49-183">ID ypatybė yra pasirinktinė.</span><span class="sxs-lookup"><span data-stu-id="6ad49-183">The ID property is optional.</span></span> <span data-ttu-id="6ad49-184">Jei ji pateikta, sistema bando ypatybę panaudoti ir, jei to padaryti negalima, pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="6ad49-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="6ad49-185">Jei ypatybė nepateikta, sistema ją sugeneruos.</span><span class="sxs-lookup"><span data-stu-id="6ad49-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="6ad49-186">Apriboti laukai</span><span class="sxs-lookup"><span data-stu-id="6ad49-186">Restricted fields</span></span>

<span data-ttu-id="6ad49-187">Toliau pateikiamose lentelėse apibrėžiami laukai, kurių negalima **Kurti** ir **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="6ad49-188">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="6ad49-188">Project task</span></span>

| <span data-ttu-id="6ad49-189">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="6ad49-189">**Logical name**</span></span>                       | <span data-ttu-id="6ad49-190">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-190">**Can create**</span></span> | <span data-ttu-id="6ad49-191">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="6ad49-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="6ad49-193">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-193">no</span></span>             | <span data-ttu-id="6ad49-194">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-194">no</span></span>               |
| <span data-ttu-id="6ad49-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="6ad49-196">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-196">no</span></span>             | <span data-ttu-id="6ad49-197">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-197">no</span></span>               |
| <span data-ttu-id="6ad49-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="6ad49-198">msdyn_actualend</span></span>                        | <span data-ttu-id="6ad49-199">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-199">no</span></span>             | <span data-ttu-id="6ad49-200">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-200">no</span></span>               |
| <span data-ttu-id="6ad49-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="6ad49-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="6ad49-202">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-202">no</span></span>             | <span data-ttu-id="6ad49-203">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-203">no</span></span>               |
| <span data-ttu-id="6ad49-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="6ad49-205">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-205">no</span></span>             | <span data-ttu-id="6ad49-206">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-206">no</span></span>               |
| <span data-ttu-id="6ad49-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="6ad49-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="6ad49-208">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-208">no</span></span>             | <span data-ttu-id="6ad49-209">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-209">no</span></span>               |
| <span data-ttu-id="6ad49-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="6ad49-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="6ad49-211">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-211">no</span></span>             | <span data-ttu-id="6ad49-212">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-212">no</span></span>               |
| <span data-ttu-id="6ad49-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="6ad49-214">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-214">no</span></span>             | <span data-ttu-id="6ad49-215">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-215">no</span></span>               |
| <span data-ttu-id="6ad49-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="6ad49-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="6ad49-217">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-217">no</span></span>             | <span data-ttu-id="6ad49-218">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-218">no</span></span>               |
| <span data-ttu-id="6ad49-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6ad49-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="6ad49-220">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-220">no</span></span>             | <span data-ttu-id="6ad49-221">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-221">no</span></span>               |
| <span data-ttu-id="6ad49-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6ad49-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="6ad49-223">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-223">no</span></span>             | <span data-ttu-id="6ad49-224">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-224">no</span></span>               |
| <span data-ttu-id="6ad49-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="6ad49-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="6ad49-226">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-226">no</span></span>             | <span data-ttu-id="6ad49-227">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-227">no</span></span>               |
| <span data-ttu-id="6ad49-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="6ad49-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="6ad49-229">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-229">no</span></span>             | <span data-ttu-id="6ad49-230">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-230">no</span></span>               |
| <span data-ttu-id="6ad49-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="6ad49-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="6ad49-232">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-232">no</span></span>             | <span data-ttu-id="6ad49-233">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-233">no</span></span>               |
| <span data-ttu-id="6ad49-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="6ad49-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="6ad49-235">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-235">no</span></span>             | <span data-ttu-id="6ad49-236">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-236">no</span></span>               |
| <span data-ttu-id="6ad49-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="6ad49-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="6ad49-238">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-238">no</span></span>             | <span data-ttu-id="6ad49-239">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-239">no</span></span>               |
| <span data-ttu-id="6ad49-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="6ad49-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="6ad49-241">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-241">no</span></span>             | <span data-ttu-id="6ad49-242">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-242">no</span></span>               |
| <span data-ttu-id="6ad49-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="6ad49-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="6ad49-244">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-244">no</span></span>             | <span data-ttu-id="6ad49-245">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-245">no</span></span>               |
| <span data-ttu-id="6ad49-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="6ad49-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="6ad49-247">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-247">no</span></span>             | <span data-ttu-id="6ad49-248">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-248">no</span></span>               |
| <span data-ttu-id="6ad49-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="6ad49-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="6ad49-250">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-250">no</span></span>             | <span data-ttu-id="6ad49-251">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-251">no</span></span>               |
| <span data-ttu-id="6ad49-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="6ad49-253">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-253">no</span></span>             | <span data-ttu-id="6ad49-254">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-254">no</span></span>               |
| <span data-ttu-id="6ad49-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="6ad49-256">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-256">no</span></span>             | <span data-ttu-id="6ad49-257">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-257">no</span></span>               |
| <span data-ttu-id="6ad49-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6ad49-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="6ad49-259">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-259">no</span></span>             | <span data-ttu-id="6ad49-260">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-260">no</span></span>               |
| <span data-ttu-id="6ad49-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="6ad49-262">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-262">no</span></span>             | <span data-ttu-id="6ad49-263">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-263">no</span></span>               |
| <span data-ttu-id="6ad49-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="6ad49-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="6ad49-265">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-265">no</span></span>             | <span data-ttu-id="6ad49-266">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-266">no</span></span>               |
| <span data-ttu-id="6ad49-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="6ad49-267">msdyn_progress</span></span>                         | <span data-ttu-id="6ad49-268">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-268">no</span></span>             | <span data-ttu-id="6ad49-269">ne (taip, jei P4W)</span><span class="sxs-lookup"><span data-stu-id="6ad49-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="6ad49-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="6ad49-271">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-271">no</span></span>             | <span data-ttu-id="6ad49-272">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-272">no</span></span>               |
| <span data-ttu-id="6ad49-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="6ad49-274">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-274">no</span></span>             | <span data-ttu-id="6ad49-275">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-275">no</span></span>               |
| <span data-ttu-id="6ad49-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="6ad49-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="6ad49-277">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-277">no</span></span>             | <span data-ttu-id="6ad49-278">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-278">no</span></span>               |
| <span data-ttu-id="6ad49-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="6ad49-280">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-280">no</span></span>             | <span data-ttu-id="6ad49-281">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-281">no</span></span>               |
| <span data-ttu-id="6ad49-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="6ad49-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="6ad49-283">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-283">no</span></span>             | <span data-ttu-id="6ad49-284">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-284">no</span></span>               |
| <span data-ttu-id="6ad49-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="6ad49-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="6ad49-286">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-286">no</span></span>             | <span data-ttu-id="6ad49-287">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-287">no</span></span>               |
| <span data-ttu-id="6ad49-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="6ad49-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="6ad49-289">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-289">no</span></span>             | <span data-ttu-id="6ad49-290">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-290">no</span></span>               |
| <span data-ttu-id="6ad49-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="6ad49-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="6ad49-292">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-292">no</span></span>             | <span data-ttu-id="6ad49-293">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-293">no</span></span>               |
| <span data-ttu-id="6ad49-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="6ad49-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="6ad49-295">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-295">no</span></span>             | <span data-ttu-id="6ad49-296">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-296">no</span></span>               |
| <span data-ttu-id="6ad49-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="6ad49-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="6ad49-298">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-298">no</span></span>             | <span data-ttu-id="6ad49-299">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-299">no</span></span>               |
| <span data-ttu-id="6ad49-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6ad49-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="6ad49-301">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-301">no</span></span>             | <span data-ttu-id="6ad49-302">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-302">no</span></span>               |
| <span data-ttu-id="6ad49-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="6ad49-304">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-304">no</span></span>             | <span data-ttu-id="6ad49-305">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-305">no</span></span>               |
| <span data-ttu-id="6ad49-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="6ad49-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="6ad49-307">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-307">no</span></span>             | <span data-ttu-id="6ad49-308">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-308">no</span></span>               |
| <span data-ttu-id="6ad49-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="6ad49-310">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-310">no</span></span>             | <span data-ttu-id="6ad49-311">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-311">no</span></span>               |
| <span data-ttu-id="6ad49-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="6ad49-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="6ad49-313">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-313">no</span></span>             | <span data-ttu-id="6ad49-314">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-314">no</span></span>               |
| <span data-ttu-id="6ad49-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="6ad49-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="6ad49-316">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-316">no</span></span>             | <span data-ttu-id="6ad49-317">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-317">no</span></span>               |
| <span data-ttu-id="6ad49-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="6ad49-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="6ad49-319">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-319">no</span></span>             | <span data-ttu-id="6ad49-320">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-320">no</span></span>               |
| <span data-ttu-id="6ad49-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="6ad49-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="6ad49-322">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-322">no</span></span>             | <span data-ttu-id="6ad49-323">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-323">no</span></span>               |
| <span data-ttu-id="6ad49-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="6ad49-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="6ad49-325">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-325">no</span></span>             | <span data-ttu-id="6ad49-326">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-326">no</span></span>               |
| <span data-ttu-id="6ad49-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="6ad49-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="6ad49-328">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-328">no</span></span>             | <span data-ttu-id="6ad49-329">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-329">no</span></span>               |
| <span data-ttu-id="6ad49-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="6ad49-330">msdyn_summary</span></span>                          | <span data-ttu-id="6ad49-331">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-331">no</span></span>             | <span data-ttu-id="6ad49-332">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-332">no</span></span>               |
| <span data-ttu-id="6ad49-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="6ad49-334">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-334">no</span></span>             | <span data-ttu-id="6ad49-335">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-335">no</span></span>               |
| <span data-ttu-id="6ad49-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="6ad49-337">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-337">no</span></span>             | <span data-ttu-id="6ad49-338">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="6ad49-339">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="6ad49-339">Project task dependency</span></span>

| <span data-ttu-id="6ad49-340">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="6ad49-340">**Logical name**</span></span>              | <span data-ttu-id="6ad49-341">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-341">**Can create**</span></span> | <span data-ttu-id="6ad49-342">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="6ad49-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="6ad49-343">msdyn_linktype</span></span>                | <span data-ttu-id="6ad49-344">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-344">no</span></span>             | <span data-ttu-id="6ad49-345">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-345">no</span></span>           |
| <span data-ttu-id="6ad49-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="6ad49-346">msdyn_linktypename</span></span>            | <span data-ttu-id="6ad49-347">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-347">no</span></span>             | <span data-ttu-id="6ad49-348">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-348">no</span></span>           |
| <span data-ttu-id="6ad49-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="6ad49-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="6ad49-350">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-350">yes</span></span>            | <span data-ttu-id="6ad49-351">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-351">no</span></span>           |
| <span data-ttu-id="6ad49-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="6ad49-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="6ad49-353">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-353">yes</span></span>            | <span data-ttu-id="6ad49-354">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-354">no</span></span>           |
| <span data-ttu-id="6ad49-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="6ad49-355">msdyn_project</span></span>                 | <span data-ttu-id="6ad49-356">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-356">yes</span></span>            | <span data-ttu-id="6ad49-357">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-357">no</span></span>           |
| <span data-ttu-id="6ad49-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="6ad49-358">msdyn_projectname</span></span>             | <span data-ttu-id="6ad49-359">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-359">yes</span></span>            | <span data-ttu-id="6ad49-360">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-360">no</span></span>           |
| <span data-ttu-id="6ad49-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="6ad49-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="6ad49-362">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-362">yes</span></span>            | <span data-ttu-id="6ad49-363">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-363">no</span></span>           |
| <span data-ttu-id="6ad49-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="6ad49-364">msdyn_successortask</span></span>           | <span data-ttu-id="6ad49-365">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-365">yes</span></span>            | <span data-ttu-id="6ad49-366">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-366">no</span></span>           |
| <span data-ttu-id="6ad49-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="6ad49-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="6ad49-368">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-368">yes</span></span>            | <span data-ttu-id="6ad49-369">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="6ad49-370">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-370">Resource assignment</span></span>

| <span data-ttu-id="6ad49-371">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="6ad49-371">**Logical name**</span></span>             | <span data-ttu-id="6ad49-372">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-372">**Can create**</span></span> | <span data-ttu-id="6ad49-373">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="6ad49-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="6ad49-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="6ad49-375">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-375">yes</span></span>            | <span data-ttu-id="6ad49-376">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-376">no</span></span>           |
| <span data-ttu-id="6ad49-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="6ad49-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="6ad49-378">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-378">yes</span></span>            | <span data-ttu-id="6ad49-379">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-379">no</span></span>           |
| <span data-ttu-id="6ad49-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="6ad49-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="6ad49-381">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-381">no</span></span>             | <span data-ttu-id="6ad49-382">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-382">no</span></span>           |
| <span data-ttu-id="6ad49-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="6ad49-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="6ad49-384">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-384">no</span></span>             | <span data-ttu-id="6ad49-385">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-385">no</span></span>           |
| <span data-ttu-id="6ad49-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="6ad49-386">msdyn_committype</span></span>             | <span data-ttu-id="6ad49-387">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-387">no</span></span>             | <span data-ttu-id="6ad49-388">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-388">no</span></span>           |
| <span data-ttu-id="6ad49-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="6ad49-389">msdyn_committypename</span></span>         | <span data-ttu-id="6ad49-390">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-390">no</span></span>             | <span data-ttu-id="6ad49-391">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-391">no</span></span>           |
| <span data-ttu-id="6ad49-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6ad49-392">msdyn_effort</span></span>                 | <span data-ttu-id="6ad49-393">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-393">no</span></span>             | <span data-ttu-id="6ad49-394">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-394">no</span></span>           |
| <span data-ttu-id="6ad49-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6ad49-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="6ad49-396">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-396">no</span></span>             | <span data-ttu-id="6ad49-397">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-397">no</span></span>           |
| <span data-ttu-id="6ad49-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6ad49-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="6ad49-399">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-399">no</span></span>             | <span data-ttu-id="6ad49-400">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-400">no</span></span>           |
| <span data-ttu-id="6ad49-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6ad49-401">msdyn_finish</span></span>                 | <span data-ttu-id="6ad49-402">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-402">no</span></span>             | <span data-ttu-id="6ad49-403">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-403">no</span></span>           |
| <span data-ttu-id="6ad49-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="6ad49-405">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-405">no</span></span>             | <span data-ttu-id="6ad49-406">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-406">no</span></span>           |
| <span data-ttu-id="6ad49-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="6ad49-408">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-408">no</span></span>             | <span data-ttu-id="6ad49-409">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-409">no</span></span>           |
| <span data-ttu-id="6ad49-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="6ad49-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="6ad49-411">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-411">no</span></span>             | <span data-ttu-id="6ad49-412">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-412">no</span></span>           |
| <span data-ttu-id="6ad49-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6ad49-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="6ad49-414">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-414">no</span></span>             | <span data-ttu-id="6ad49-415">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-415">no</span></span>           |
| <span data-ttu-id="6ad49-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="6ad49-417">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-417">no</span></span>             | <span data-ttu-id="6ad49-418">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-418">no</span></span>           |
| <span data-ttu-id="6ad49-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="6ad49-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="6ad49-420">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-420">no</span></span>             | <span data-ttu-id="6ad49-421">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-421">no</span></span>           |
| <span data-ttu-id="6ad49-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="6ad49-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="6ad49-423">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-423">no</span></span>             | <span data-ttu-id="6ad49-424">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-424">no</span></span>           |
| <span data-ttu-id="6ad49-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="6ad49-425">msdyn_projectid</span></span>              | <span data-ttu-id="6ad49-426">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-426">yes</span></span>            | <span data-ttu-id="6ad49-427">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-427">no</span></span>           |
| <span data-ttu-id="6ad49-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="6ad49-428">msdyn_projectidname</span></span>          | <span data-ttu-id="6ad49-429">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-429">no</span></span>             | <span data-ttu-id="6ad49-430">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-430">no</span></span>           |
| <span data-ttu-id="6ad49-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="6ad49-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="6ad49-432">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-432">no</span></span>             | <span data-ttu-id="6ad49-433">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-433">no</span></span>           |
| <span data-ttu-id="6ad49-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="6ad49-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="6ad49-435">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-435">no</span></span>             | <span data-ttu-id="6ad49-436">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-436">no</span></span>           |
| <span data-ttu-id="6ad49-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="6ad49-437">msdyn_start</span></span>                  | <span data-ttu-id="6ad49-438">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-438">no</span></span>             | <span data-ttu-id="6ad49-439">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-439">no</span></span>           |
| <span data-ttu-id="6ad49-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="6ad49-440">msdyn_taskid</span></span>                 | <span data-ttu-id="6ad49-441">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-441">no</span></span>             | <span data-ttu-id="6ad49-442">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-442">no</span></span>           |
| <span data-ttu-id="6ad49-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="6ad49-443">msdyn_taskidname</span></span>             | <span data-ttu-id="6ad49-444">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-444">no</span></span>             | <span data-ttu-id="6ad49-445">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-445">no</span></span>           |
| <span data-ttu-id="6ad49-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="6ad49-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="6ad49-447">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-447">no</span></span>             | <span data-ttu-id="6ad49-448">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="6ad49-449">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="6ad49-449">Project team member</span></span>

| <span data-ttu-id="6ad49-450">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="6ad49-450">**Logical name**</span></span>                                 | <span data-ttu-id="6ad49-451">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-451">**Can create**</span></span> | <span data-ttu-id="6ad49-452">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="6ad49-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="6ad49-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="6ad49-454">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-454">no</span></span>             | <span data-ttu-id="6ad49-455">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-455">no</span></span>           |
| <span data-ttu-id="6ad49-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="6ad49-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="6ad49-457">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-457">no</span></span>             | <span data-ttu-id="6ad49-458">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-458">no</span></span>           |
| <span data-ttu-id="6ad49-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="6ad49-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="6ad49-460">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-460">no</span></span>             | <span data-ttu-id="6ad49-461">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-461">no</span></span>           |
| <span data-ttu-id="6ad49-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="6ad49-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="6ad49-463">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-463">no</span></span>             | <span data-ttu-id="6ad49-464">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-464">no</span></span>           |
| <span data-ttu-id="6ad49-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6ad49-465">msdyn_effort</span></span>                                     | <span data-ttu-id="6ad49-466">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-466">no</span></span>             | <span data-ttu-id="6ad49-467">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-467">no</span></span>           |
| <span data-ttu-id="6ad49-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6ad49-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="6ad49-469">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-469">no</span></span>             | <span data-ttu-id="6ad49-470">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-470">no</span></span>           |
| <span data-ttu-id="6ad49-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6ad49-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="6ad49-472">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-472">no</span></span>             | <span data-ttu-id="6ad49-473">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-473">no</span></span>           |
| <span data-ttu-id="6ad49-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6ad49-474">msdyn_finish</span></span>                                     | <span data-ttu-id="6ad49-475">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-475">no</span></span>             | <span data-ttu-id="6ad49-476">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-476">no</span></span>           |
| <span data-ttu-id="6ad49-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="6ad49-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="6ad49-478">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-478">no</span></span>             | <span data-ttu-id="6ad49-479">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-479">no</span></span>           |
| <span data-ttu-id="6ad49-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="6ad49-480">msdyn_hours</span></span>                                      | <span data-ttu-id="6ad49-481">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-481">no</span></span>             | <span data-ttu-id="6ad49-482">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-482">no</span></span>           |
| <span data-ttu-id="6ad49-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="6ad49-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="6ad49-484">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-484">no</span></span>             | <span data-ttu-id="6ad49-485">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-485">no</span></span>           |
| <span data-ttu-id="6ad49-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="6ad49-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="6ad49-487">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-487">no</span></span>             | <span data-ttu-id="6ad49-488">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-488">no</span></span>           |
| <span data-ttu-id="6ad49-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="6ad49-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="6ad49-490">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-490">no</span></span>             | <span data-ttu-id="6ad49-491">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-491">no</span></span>           |
| <span data-ttu-id="6ad49-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="6ad49-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="6ad49-493">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-493">no</span></span>             | <span data-ttu-id="6ad49-494">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-494">no</span></span>           |
| <span data-ttu-id="6ad49-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="6ad49-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="6ad49-496">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-496">no</span></span>             | <span data-ttu-id="6ad49-497">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-497">no</span></span>           |
| <span data-ttu-id="6ad49-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="6ad49-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="6ad49-499">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-499">no</span></span>             | <span data-ttu-id="6ad49-500">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-500">no</span></span>           |
| <span data-ttu-id="6ad49-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="6ad49-501">msdyn_start</span></span>                                      | <span data-ttu-id="6ad49-502">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-502">no</span></span>             | <span data-ttu-id="6ad49-503">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="6ad49-504">Project</span><span class="sxs-lookup"><span data-stu-id="6ad49-504">Project</span></span>

| <span data-ttu-id="6ad49-505">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="6ad49-505">**Logical name**</span></span>                       | <span data-ttu-id="6ad49-506">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-506">**Can create**</span></span> | <span data-ttu-id="6ad49-507">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="6ad49-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="6ad49-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="6ad49-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="6ad49-509">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-509">no</span></span>             | <span data-ttu-id="6ad49-510">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-510">no</span></span>           |
| <span data-ttu-id="6ad49-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="6ad49-512">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-512">no</span></span>             | <span data-ttu-id="6ad49-513">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-513">no</span></span>           |
| <span data-ttu-id="6ad49-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="6ad49-515">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-515">no</span></span>             | <span data-ttu-id="6ad49-516">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-516">no</span></span>           |
| <span data-ttu-id="6ad49-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="6ad49-518">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-518">no</span></span>             | <span data-ttu-id="6ad49-519">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-519">no</span></span>           |
| <span data-ttu-id="6ad49-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="6ad49-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="6ad49-521">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-521">no</span></span>             | <span data-ttu-id="6ad49-522">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-522">no</span></span>           |
| <span data-ttu-id="6ad49-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="6ad49-524">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-524">no</span></span>             | <span data-ttu-id="6ad49-525">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-525">no</span></span>           |
| <span data-ttu-id="6ad49-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="6ad49-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="6ad49-527">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-527">yes</span></span>            | <span data-ttu-id="6ad49-528">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-528">no</span></span>           |
| <span data-ttu-id="6ad49-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="6ad49-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="6ad49-530">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-530">yes</span></span>            | <span data-ttu-id="6ad49-531">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-531">no</span></span>           |
| <span data-ttu-id="6ad49-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="6ad49-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="6ad49-533">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-533">yes</span></span>            | <span data-ttu-id="6ad49-534">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-534">no</span></span>           |
| <span data-ttu-id="6ad49-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="6ad49-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="6ad49-536">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-536">no</span></span>             | <span data-ttu-id="6ad49-537">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-537">no</span></span>           |
| <span data-ttu-id="6ad49-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="6ad49-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="6ad49-539">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-539">no</span></span>             | <span data-ttu-id="6ad49-540">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-540">no</span></span>           |
| <span data-ttu-id="6ad49-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="6ad49-542">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-542">no</span></span>             | <span data-ttu-id="6ad49-543">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-543">no</span></span>           |
| <span data-ttu-id="6ad49-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="6ad49-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="6ad49-545">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-545">no</span></span>             | <span data-ttu-id="6ad49-546">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-546">no</span></span>           |
| <span data-ttu-id="6ad49-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="6ad49-548">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-548">no</span></span>             | <span data-ttu-id="6ad49-549">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-549">no</span></span>           |
| <span data-ttu-id="6ad49-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="6ad49-550">msdyn_duration</span></span>                         | <span data-ttu-id="6ad49-551">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-551">no</span></span>             | <span data-ttu-id="6ad49-552">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-552">no</span></span>           |
| <span data-ttu-id="6ad49-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="6ad49-553">msdyn_effort</span></span>                           | <span data-ttu-id="6ad49-554">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-554">no</span></span>             | <span data-ttu-id="6ad49-555">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-555">no</span></span>           |
| <span data-ttu-id="6ad49-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="6ad49-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="6ad49-557">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-557">no</span></span>             | <span data-ttu-id="6ad49-558">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-558">no</span></span>           |
| <span data-ttu-id="6ad49-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="6ad49-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="6ad49-560">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-560">no</span></span>             | <span data-ttu-id="6ad49-561">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-561">no</span></span>           |
| <span data-ttu-id="6ad49-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="6ad49-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="6ad49-563">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-563">no</span></span>             | <span data-ttu-id="6ad49-564">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-564">no</span></span>           |
| <span data-ttu-id="6ad49-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="6ad49-565">msdyn_finish</span></span>                           | <span data-ttu-id="6ad49-566">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-566">yes</span></span>            | <span data-ttu-id="6ad49-567">taip</span><span class="sxs-lookup"><span data-stu-id="6ad49-567">yes</span></span>          |
| <span data-ttu-id="6ad49-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="6ad49-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="6ad49-569">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-569">no</span></span>             | <span data-ttu-id="6ad49-570">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-570">no</span></span>           |
| <span data-ttu-id="6ad49-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="6ad49-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="6ad49-572">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-572">no</span></span>             | <span data-ttu-id="6ad49-573">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-573">no</span></span>           |
| <span data-ttu-id="6ad49-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="6ad49-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="6ad49-575">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-575">no</span></span>             | <span data-ttu-id="6ad49-576">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-576">no</span></span>           |
| <span data-ttu-id="6ad49-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="6ad49-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="6ad49-578">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-578">no</span></span>             | <span data-ttu-id="6ad49-579">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-579">no</span></span>           |
| <span data-ttu-id="6ad49-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="6ad49-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="6ad49-581">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-581">no</span></span>             | <span data-ttu-id="6ad49-582">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-582">no</span></span>           |
| <span data-ttu-id="6ad49-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="6ad49-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="6ad49-584">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-584">no</span></span>             | <span data-ttu-id="6ad49-585">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-585">no</span></span>           |
| <span data-ttu-id="6ad49-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="6ad49-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="6ad49-587">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-587">no</span></span>             | <span data-ttu-id="6ad49-588">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-588">no</span></span>           |
| <span data-ttu-id="6ad49-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="6ad49-590">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-590">no</span></span>             | <span data-ttu-id="6ad49-591">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-591">no</span></span>           |
| <span data-ttu-id="6ad49-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="6ad49-593">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-593">no</span></span>             | <span data-ttu-id="6ad49-594">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-594">no</span></span>           |
| <span data-ttu-id="6ad49-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="6ad49-596">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-596">no</span></span>             | <span data-ttu-id="6ad49-597">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-597">no</span></span>           |
| <span data-ttu-id="6ad49-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="6ad49-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="6ad49-599">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-599">no</span></span>             | <span data-ttu-id="6ad49-600">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-600">no</span></span>           |
| <span data-ttu-id="6ad49-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="6ad49-602">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-602">no</span></span>             | <span data-ttu-id="6ad49-603">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-603">no</span></span>           |
| <span data-ttu-id="6ad49-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="6ad49-604">msdyn_progress</span></span>                         | <span data-ttu-id="6ad49-605">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-605">no</span></span>             | <span data-ttu-id="6ad49-606">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-606">no</span></span>           |
| <span data-ttu-id="6ad49-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="6ad49-608">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-608">no</span></span>             | <span data-ttu-id="6ad49-609">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-609">no</span></span>           |
| <span data-ttu-id="6ad49-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="6ad49-611">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-611">no</span></span>             | <span data-ttu-id="6ad49-612">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-612">no</span></span>           |
| <span data-ttu-id="6ad49-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="6ad49-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="6ad49-614">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-614">no</span></span>             | <span data-ttu-id="6ad49-615">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-615">no</span></span>           |
| <span data-ttu-id="6ad49-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="6ad49-617">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-617">no</span></span>             | <span data-ttu-id="6ad49-618">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-618">no</span></span>           |
| <span data-ttu-id="6ad49-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="6ad49-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="6ad49-620">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-620">no</span></span>             | <span data-ttu-id="6ad49-621">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-621">no</span></span>           |
| <span data-ttu-id="6ad49-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="6ad49-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="6ad49-623">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-623">no</span></span>             | <span data-ttu-id="6ad49-624">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-624">no</span></span>           |
| <span data-ttu-id="6ad49-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="6ad49-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="6ad49-626">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-626">no</span></span>             | <span data-ttu-id="6ad49-627">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-627">no</span></span>           |
| <span data-ttu-id="6ad49-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="6ad49-629">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-629">no</span></span>             | <span data-ttu-id="6ad49-630">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-630">no</span></span>           |
| <span data-ttu-id="6ad49-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="6ad49-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="6ad49-632">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-632">no</span></span>             | <span data-ttu-id="6ad49-633">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-633">no</span></span>           |
| <span data-ttu-id="6ad49-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="6ad49-635">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-635">no</span></span>             | <span data-ttu-id="6ad49-636">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-636">no</span></span>           |
| <span data-ttu-id="6ad49-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="6ad49-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="6ad49-638">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-638">no</span></span>             | <span data-ttu-id="6ad49-639">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-639">no</span></span>           |
| <span data-ttu-id="6ad49-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="6ad49-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="6ad49-641">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-641">no</span></span>             | <span data-ttu-id="6ad49-642">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-642">no</span></span>           |
| <span data-ttu-id="6ad49-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="6ad49-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="6ad49-644">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-644">no</span></span>             | <span data-ttu-id="6ad49-645">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-645">no</span></span>           |
| <span data-ttu-id="6ad49-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="6ad49-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="6ad49-647">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-647">no</span></span>             | <span data-ttu-id="6ad49-648">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-648">no</span></span>           |
| <span data-ttu-id="6ad49-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="6ad49-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="6ad49-650">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-650">no</span></span>             | <span data-ttu-id="6ad49-651">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-651">no</span></span>           |
| <span data-ttu-id="6ad49-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="6ad49-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="6ad49-653">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-653">no</span></span>             | <span data-ttu-id="6ad49-654">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-654">no</span></span>           |
| <span data-ttu-id="6ad49-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="6ad49-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="6ad49-656">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-656">no</span></span>             | <span data-ttu-id="6ad49-657">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-657">no</span></span>           |
| <span data-ttu-id="6ad49-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="6ad49-659">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-659">no</span></span>             | <span data-ttu-id="6ad49-660">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-660">no</span></span>           |
| <span data-ttu-id="6ad49-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="6ad49-662">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-662">no</span></span>             | <span data-ttu-id="6ad49-663">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-663">no</span></span>           |
| <span data-ttu-id="6ad49-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="6ad49-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="6ad49-665">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-665">no</span></span>             | <span data-ttu-id="6ad49-666">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-666">no</span></span>           |
| <span data-ttu-id="6ad49-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="6ad49-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="6ad49-668">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-668">no</span></span>             | <span data-ttu-id="6ad49-669">ne</span><span class="sxs-lookup"><span data-stu-id="6ad49-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="6ad49-670">Apribojimai ir žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="6ad49-670">Limitations and known issues</span></span>
<span data-ttu-id="6ad49-671">Toliau pateikiamas apribojimų ir žinomų problemų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="6ad49-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="6ad49-672">Grafiko API gali naudoti tik **vartotojai, turintys „Microsoft Project“ licenciją.**</span><span class="sxs-lookup"><span data-stu-id="6ad49-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="6ad49-673">Jų negali toliau nurodyti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="6ad49-673">They can't be used by:</span></span>
    - <span data-ttu-id="6ad49-674">Programų vartotojai</span><span class="sxs-lookup"><span data-stu-id="6ad49-674">Application users</span></span>
    - <span data-ttu-id="6ad49-675">Sistemos vartotojai</span><span class="sxs-lookup"><span data-stu-id="6ad49-675">System users</span></span>
    - <span data-ttu-id="6ad49-676">Integravimo vartotojai</span><span class="sxs-lookup"><span data-stu-id="6ad49-676">Integration users</span></span>
    - <span data-ttu-id="6ad49-677">Kiti vartotojai, neturintys reikiamos licencijos</span><span class="sxs-lookup"><span data-stu-id="6ad49-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="6ad49-678">Kiekviename **OperationSet** gali būti ne daugiau kaip 100 operacijų.</span><span class="sxs-lookup"><span data-stu-id="6ad49-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="6ad49-679">Kiekvienas vartotojas gali turėti ne daugiau kaip 10 atvirų **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="6ad49-680">„Project Operations“ šiuo metu palaikoma ne daugiau kaip 500 projekto užduočių iš viso.</span><span class="sxs-lookup"><span data-stu-id="6ad49-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="6ad49-681">**OperationSet** trikties būsena ir trikties žurnalai šiuo metu negalimi.</span><span class="sxs-lookup"><span data-stu-id="6ad49-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="6ad49-682">Grafiko API yra viešosios priežiūros versijos.</span><span class="sxs-lookup"><span data-stu-id="6ad49-682">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="6ad49-683">„Microsoft“ nepalaiko šių API naudojimo gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="6ad49-683">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>
- [<span data-ttu-id="6ad49-684">Projektų ir užduočių limitai bei ribos</span><span class="sxs-lookup"><span data-stu-id="6ad49-684">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="6ad49-685">Klaidų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="6ad49-685">Error handling</span></span>

   - <span data-ttu-id="6ad49-686">Norėdami peržiūrėti iš operacijų rinkinių sugeneruotas klaidas, eikite į **Parametrai** \> **Grafiko integravimas** \> **Operacijų rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-686">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="6ad49-687">Norėdami peržiūrėti iš projektų planavimo tarnybos sugeneruotas klaidas, eikite į **Parametrai** \> **Grafiko integravimas** \> **PSS klaidų žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="6ad49-687">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="6ad49-688">Scenarijaus pavyzdys</span><span class="sxs-lookup"><span data-stu-id="6ad49-688">Sample scenario</span></span>

<span data-ttu-id="6ad49-689">Pagal šį scenarijų sukursite projektą, komandos narį, keturias užduotis ir du išteklių priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="6ad49-689">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="6ad49-690">Tada atnaujinsite vieną užduotį, atnaujinsite projektą, panaikinsite vieną užduotį, panaikinsite vieną išteklių priskyrimą ir sukursite užduoties priklausomybę.</span><span class="sxs-lookup"><span data-stu-id="6ad49-690">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="6ad49-691">Papildomi pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="6ad49-691">Additional samples</span></span>

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
