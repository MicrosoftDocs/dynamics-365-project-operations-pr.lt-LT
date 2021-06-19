---
title: Grafiko API naudojimas norint atlikti operacijas su grafiko objektais
description: Šioje temoje pateikiama informacija ir pavyzdžiai, kaip naudoti grafiko API.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4a032dc7bcbdf23fce3c3b2ca63c51d473bd8e26
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116807"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="ebba6-103">Grafiko API naudojimas norint atlikti operacijas su grafiko objektais</span><span class="sxs-lookup"><span data-stu-id="ebba6-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="ebba6-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="ebba6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="ebba6-105">Kai kurios arba visos šioje temoje paminėtos funkcijos pasiekiamos kaip peržiūros versijos leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="ebba6-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="ebba6-106">Turinys ir funkcijos gali keistis.</span><span class="sxs-lookup"><span data-stu-id="ebba6-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="ebba6-107">Grafiko objektai</span><span class="sxs-lookup"><span data-stu-id="ebba6-107">Scheduling entities</span></span>

<span data-ttu-id="ebba6-108">Grafiko API suteikia galimybę atlikti kūrimo, naujinimo ir naikinimo operacijas naudojant **grafiko objektus**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="ebba6-109">Šie objektai valdomi naudojant „Project for the Web“ planavimo variklį.</span><span class="sxs-lookup"><span data-stu-id="ebba6-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="ebba6-110">Ankstesniuose „Dynamics 365 Project Operations“ leidimuose operacijų kūrimas, naujinimas ir naikinimas naudojant **planavimo objektus** buvo apribotas.</span><span class="sxs-lookup"><span data-stu-id="ebba6-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="ebba6-111">Toliau esančioje lentelėje pateikiamas visas **planavimo objektų** sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ebba6-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="ebba6-112">Objekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-112">Entity name</span></span>  | <span data-ttu-id="ebba6-113">Loginis objekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="ebba6-114">Project</span><span class="sxs-lookup"><span data-stu-id="ebba6-114">Project</span></span> | <span data-ttu-id="ebba6-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ebba6-115">msdyn_project</span></span> |
| <span data-ttu-id="ebba6-116">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="ebba6-116">Project Task</span></span>  | <span data-ttu-id="ebba6-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="ebba6-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="ebba6-118">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="ebba6-118">Project Task Dependency</span></span>  | <span data-ttu-id="ebba6-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="ebba6-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="ebba6-120">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-120">Resource Assignment</span></span> | <span data-ttu-id="ebba6-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="ebba6-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="ebba6-122">Projekto talpykla</span><span class="sxs-lookup"><span data-stu-id="ebba6-122">Project Bucket</span></span>  | <span data-ttu-id="ebba6-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="ebba6-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="ebba6-124">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="ebba6-124">Project Team Member</span></span> | <span data-ttu-id="ebba6-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="ebba6-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="ebba6-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="ebba6-126">OperationSet</span></span>

<span data-ttu-id="ebba6-127">OperationSet yra darbo vieneto modelis, kurį galima naudoti, kai operacijoje reikia apdoroti keletą grafikui poveikį darančių užklausų.</span><span class="sxs-lookup"><span data-stu-id="ebba6-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="ebba6-128">Grafiko API</span><span class="sxs-lookup"><span data-stu-id="ebba6-128">Schedule APIs</span></span>

<span data-ttu-id="ebba6-129">Toliau pateikiamas dabartinių grafiko API sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ebba6-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="ebba6-130">**msdyn_CreateProjectV1**: šį API galima naudoti norint sukurti projektą.</span><span class="sxs-lookup"><span data-stu-id="ebba6-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="ebba6-131">Projektas ir numatytoji projekto talpykla sukuriami nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="ebba6-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="ebba6-132">**msdyn_CreateTeamMemberV1**:šį API galima naudoti norint sukurti projekto komandos narį.</span><span class="sxs-lookup"><span data-stu-id="ebba6-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="ebba6-133">Komandos nario įrašas sukuriamas nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="ebba6-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="ebba6-134">**msdyn_CreateOperationSetV1**: šį API galima naudoti norint suplanuoti keletą užklausų, kurias reikia atlikti operacijoje.</span><span class="sxs-lookup"><span data-stu-id="ebba6-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="ebba6-135">**msdyn_PSSCreateV1**: šį API galima naudoti norint sukurti objektą.</span><span class="sxs-lookup"><span data-stu-id="ebba6-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="ebba6-136">Objektu gali būti bet kuris iš planavimo objektų, palaikančių kūrimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="ebba6-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="ebba6-137">**msdyn_PSSUpdateV1**: šį API galima naudoti norint atnaujinti objektą.</span><span class="sxs-lookup"><span data-stu-id="ebba6-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="ebba6-138">Objektu gali būti bet kuris iš planavimo objektų, palaikančių naujinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="ebba6-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="ebba6-139">**msdyn_PSSDeleteV1**: šį API galima naudoti norint panaikinti objektą.</span><span class="sxs-lookup"><span data-stu-id="ebba6-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="ebba6-140">Objektu gali būti bet kuris iš planavimo objektų, palaikančių naikinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="ebba6-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="ebba6-141">**msdyn_ExecuteOperationSetV1**: šis API naudojamas norint vykdyti visas nurodyto operacijų rinkinio operacijas.</span><span class="sxs-lookup"><span data-stu-id="ebba6-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="ebba6-142">Grafiko API naudojimas kartu su OperationSet</span><span class="sxs-lookup"><span data-stu-id="ebba6-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="ebba6-143">Kadangi įrašai, naudojant **CreateProjectV1** ir **CreateTeamMemberV1**, sukuriami nedelsiant, šių API negalima naudoti tiesiai **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="ebba6-144">Tačiau API galite naudoti norėdami sukurti reikiamus įrašus, **OperationSet**, tada šiuos iš anksto sukurtus įrašus panaudoti **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="ebba6-145">Palaikomos operacijos</span><span class="sxs-lookup"><span data-stu-id="ebba6-145">Supported operations</span></span>

| <span data-ttu-id="ebba6-146">Grafiko objektas</span><span class="sxs-lookup"><span data-stu-id="ebba6-146">Scheduling entity</span></span> | <span data-ttu-id="ebba6-147">Kūrimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-147">Create</span></span> | <span data-ttu-id="ebba6-148">Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-148">Update</span></span> | <span data-ttu-id="ebba6-149">Delete</span><span class="sxs-lookup"><span data-stu-id="ebba6-149">Delete</span></span> | <span data-ttu-id="ebba6-150">Svarbi informacija</span><span class="sxs-lookup"><span data-stu-id="ebba6-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="ebba6-151">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="ebba6-151">Project task</span></span> | <span data-ttu-id="ebba6-152">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-152">Yes</span></span> | <span data-ttu-id="ebba6-153">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-153">Yes</span></span> | <span data-ttu-id="ebba6-154">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-154">Yes</span></span> | <span data-ttu-id="ebba6-155">Nėra</span><span class="sxs-lookup"><span data-stu-id="ebba6-155">None</span></span> |
| <span data-ttu-id="ebba6-156">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="ebba6-156">Project task dependency</span></span> | <span data-ttu-id="ebba6-157">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-157">Yes</span></span> | <span data-ttu-id="ebba6-158">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-158">Yes</span></span> | | <span data-ttu-id="ebba6-159">Projekto užduoties priklausomybės įrašai neatnaujinami.</span><span class="sxs-lookup"><span data-stu-id="ebba6-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="ebba6-160">Vietoj to, seną įrašą galima panaikinti ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="ebba6-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ebba6-161">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-161">Resource assignment</span></span> | <span data-ttu-id="ebba6-162">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-162">Yes</span></span> | <span data-ttu-id="ebba6-163">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-163">Yes</span></span> | | <span data-ttu-id="ebba6-164">Nepalaikomos operacijos, kurioms naudojami šie laukai: **BookableResourceID**, **Pastangos**, **EffortCompleted**, **EffortRemaining** ir **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="ebba6-165">Išteklių priskyrimo įrašai neatnaujinami.</span><span class="sxs-lookup"><span data-stu-id="ebba6-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="ebba6-166">Vietoj to, seną įrašą galima panaikinti ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="ebba6-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ebba6-167">Projekto talpykla</span><span class="sxs-lookup"><span data-stu-id="ebba6-167">Project bucket</span></span> | <span data-ttu-id="ebba6-168">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ebba6-168">N/A</span></span> | <span data-ttu-id="ebba6-169">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ebba6-169">N/A</span></span> | <span data-ttu-id="ebba6-170">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ebba6-170">N/A</span></span> | <span data-ttu-id="ebba6-171">Numatytoji talpykla sukuriama naudojant **CreateProjectV1** API.</span><span class="sxs-lookup"><span data-stu-id="ebba6-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="ebba6-172">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="ebba6-172">Project team member</span></span> | <span data-ttu-id="ebba6-173">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-173">Yes</span></span> | <span data-ttu-id="ebba6-174">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-174">Yes</span></span> | <span data-ttu-id="ebba6-175">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-175">Yes</span></span> | <span data-ttu-id="ebba6-176">Kūrimo operacijai naudokite **CreateTeamMemberV1** API.</span><span class="sxs-lookup"><span data-stu-id="ebba6-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="ebba6-177">Project</span><span class="sxs-lookup"><span data-stu-id="ebba6-177">Project</span></span> | <span data-ttu-id="ebba6-178">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-178">Yes</span></span> | <span data-ttu-id="ebba6-179">Taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-179">Yes</span></span> | <span data-ttu-id="ebba6-180">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ebba6-180">N/A</span></span> | <span data-ttu-id="ebba6-181">Nepalaikomos operacijos, kurioms naudojami šie laukai: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Pastangos**, **EffortCompleted**, **EffortRemaining**, **Eiga**, **Pabaiga**, **TaskEarliestStart** ir **Duration**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="ebba6-182">Šias API galima iškviesti naudojant objektus, kuriuose įtraukti pasirinktini laukai.</span><span class="sxs-lookup"><span data-stu-id="ebba6-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="ebba6-183">ID ypatybė yra pasirinktinė.</span><span class="sxs-lookup"><span data-stu-id="ebba6-183">The ID property is optional.</span></span> <span data-ttu-id="ebba6-184">Jei ji pateikta, sistema bando ypatybę panaudoti ir, jei to padaryti negalima, pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="ebba6-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="ebba6-185">Jei ypatybė nepateikta, sistema ją sugeneruos.</span><span class="sxs-lookup"><span data-stu-id="ebba6-185">If it isn't provided, the system will generate it.</span></span>

## <a name="restricted-fields"></a><span data-ttu-id="ebba6-186">Apriboti laukai</span><span class="sxs-lookup"><span data-stu-id="ebba6-186">Restricted fields</span></span>

<span data-ttu-id="ebba6-187">Toliau pateikiamose lentelėse apibrėžiami laukai, kurių negalima **Kurti** ir **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-187">The following tables define the fields that are restricted from **Create** and **Edit.**</span></span>

### <a name="project-task"></a><span data-ttu-id="ebba6-188">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="ebba6-188">Project task</span></span>

| <span data-ttu-id="ebba6-189">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ebba6-189">**Logical name**</span></span>                       | <span data-ttu-id="ebba6-190">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-190">**Can create**</span></span> | <span data-ttu-id="ebba6-191">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-191">**Can edit**</span></span>     |
|----------------------------------------|----------------|------------------|
| <span data-ttu-id="ebba6-192">msdyn_actualcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-192">msdyn_actualcost</span></span>                       | <span data-ttu-id="ebba6-193">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-193">no</span></span>             | <span data-ttu-id="ebba6-194">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-194">no</span></span>               |
| <span data-ttu-id="ebba6-195">msdyn_actualcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-195">msdyn_actualcost_base</span></span>                  | <span data-ttu-id="ebba6-196">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-196">no</span></span>             | <span data-ttu-id="ebba6-197">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-197">no</span></span>               |
| <span data-ttu-id="ebba6-198">msdyn_actualend</span><span class="sxs-lookup"><span data-stu-id="ebba6-198">msdyn_actualend</span></span>                        | <span data-ttu-id="ebba6-199">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-199">no</span></span>             | <span data-ttu-id="ebba6-200">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-200">no</span></span>               |
| <span data-ttu-id="ebba6-201">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="ebba6-201">msdyn_actualsales</span></span>                      | <span data-ttu-id="ebba6-202">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-202">no</span></span>             | <span data-ttu-id="ebba6-203">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-203">no</span></span>               |
| <span data-ttu-id="ebba6-204">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-204">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="ebba6-205">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-205">no</span></span>             | <span data-ttu-id="ebba6-206">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-206">no</span></span>               |
| <span data-ttu-id="ebba6-207">msdyn_actualstart</span><span class="sxs-lookup"><span data-stu-id="ebba6-207">msdyn_actualstart</span></span>                      | <span data-ttu-id="ebba6-208">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-208">no</span></span>             | <span data-ttu-id="ebba6-209">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-209">no</span></span>               |
| <span data-ttu-id="ebba6-210">msdyn_costatcompleteestimate</span><span class="sxs-lookup"><span data-stu-id="ebba6-210">msdyn_costatcompleteestimate</span></span>           | <span data-ttu-id="ebba6-211">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-211">no</span></span>             | <span data-ttu-id="ebba6-212">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-212">no</span></span>               |
| <span data-ttu-id="ebba6-213">msdyn_costatcompleteestimate_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-213">msdyn_costatcompleteestimate_base</span></span>      | <span data-ttu-id="ebba6-214">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-214">no</span></span>             | <span data-ttu-id="ebba6-215">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-215">no</span></span>               |
| <span data-ttu-id="ebba6-216">msdyn_costconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="ebba6-216">msdyn_costconsumptionpercentage</span></span>        | <span data-ttu-id="ebba6-217">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-217">no</span></span>             | <span data-ttu-id="ebba6-218">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-218">no</span></span>               |
| <span data-ttu-id="ebba6-219">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ebba6-219">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="ebba6-220">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-220">no</span></span>             | <span data-ttu-id="ebba6-221">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-221">no</span></span>               |
| <span data-ttu-id="ebba6-222">msdyn_effortestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ebba6-222">msdyn_effortestimateatcomplete</span></span>         | <span data-ttu-id="ebba6-223">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-223">no</span></span>             | <span data-ttu-id="ebba6-224">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-224">no</span></span>               |
| <span data-ttu-id="ebba6-225">msdyn_iscritical</span><span class="sxs-lookup"><span data-stu-id="ebba6-225">msdyn_iscritical</span></span>                       | <span data-ttu-id="ebba6-226">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-226">no</span></span>             | <span data-ttu-id="ebba6-227">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-227">no</span></span>               |
| <span data-ttu-id="ebba6-228">msdyn_iscriticalname</span><span class="sxs-lookup"><span data-stu-id="ebba6-228">msdyn_iscriticalname</span></span>                   | <span data-ttu-id="ebba6-229">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-229">no</span></span>             | <span data-ttu-id="ebba6-230">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-230">no</span></span>               |
| <span data-ttu-id="ebba6-231">msdyn_ismanual</span><span class="sxs-lookup"><span data-stu-id="ebba6-231">msdyn_ismanual</span></span>                         | <span data-ttu-id="ebba6-232">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-232">no</span></span>             | <span data-ttu-id="ebba6-233">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-233">no</span></span>               |
| <span data-ttu-id="ebba6-234">msdyn_ismanualname</span><span class="sxs-lookup"><span data-stu-id="ebba6-234">msdyn_ismanualname</span></span>                     | <span data-ttu-id="ebba6-235">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-235">no</span></span>             | <span data-ttu-id="ebba6-236">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-236">no</span></span>               |
| <span data-ttu-id="ebba6-237">msdyn_ismilestone</span><span class="sxs-lookup"><span data-stu-id="ebba6-237">msdyn_ismilestone</span></span>                      | <span data-ttu-id="ebba6-238">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-238">no</span></span>             | <span data-ttu-id="ebba6-239">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-239">no</span></span>               |
| <span data-ttu-id="ebba6-240">msdyn_ismilestonename</span><span class="sxs-lookup"><span data-stu-id="ebba6-240">msdyn_ismilestonename</span></span>                  | <span data-ttu-id="ebba6-241">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-241">no</span></span>             | <span data-ttu-id="ebba6-242">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-242">no</span></span>               |
| <span data-ttu-id="ebba6-243">msdyn_LinkStatus</span><span class="sxs-lookup"><span data-stu-id="ebba6-243">msdyn_LinkStatus</span></span>                       | <span data-ttu-id="ebba6-244">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-244">no</span></span>             | <span data-ttu-id="ebba6-245">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-245">no</span></span>               |
| <span data-ttu-id="ebba6-246">msdyn_linkstatusname</span><span class="sxs-lookup"><span data-stu-id="ebba6-246">msdyn_linkstatusname</span></span>                   | <span data-ttu-id="ebba6-247">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-247">no</span></span>             | <span data-ttu-id="ebba6-248">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-248">no</span></span>               |
| <span data-ttu-id="ebba6-249">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="ebba6-249">msdyn_msprojectclientid</span></span>                | <span data-ttu-id="ebba6-250">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-250">no</span></span>             | <span data-ttu-id="ebba6-251">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-251">no</span></span>               |
| <span data-ttu-id="ebba6-252">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-252">msdyn_plannedcost</span></span>                      | <span data-ttu-id="ebba6-253">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-253">no</span></span>             | <span data-ttu-id="ebba6-254">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-254">no</span></span>               |
| <span data-ttu-id="ebba6-255">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-255">msdyn_plannedcost_base</span></span>                 | <span data-ttu-id="ebba6-256">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-256">no</span></span>             | <span data-ttu-id="ebba6-257">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-257">no</span></span>               |
| <span data-ttu-id="ebba6-258">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ebba6-258">msdyn_plannedsales</span></span>                     | <span data-ttu-id="ebba6-259">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-259">no</span></span>             | <span data-ttu-id="ebba6-260">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-260">no</span></span>               |
| <span data-ttu-id="ebba6-261">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-261">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="ebba6-262">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-262">no</span></span>             | <span data-ttu-id="ebba6-263">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-263">no</span></span>               |
| <span data-ttu-id="ebba6-264">msdyn_pluginprocessingdata</span><span class="sxs-lookup"><span data-stu-id="ebba6-264">msdyn_pluginprocessingdata</span></span>             | <span data-ttu-id="ebba6-265">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-265">no</span></span>             | <span data-ttu-id="ebba6-266">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-266">no</span></span>               |
| <span data-ttu-id="ebba6-267">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="ebba6-267">msdyn_progress</span></span>                         | <span data-ttu-id="ebba6-268">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-268">no</span></span>             | <span data-ttu-id="ebba6-269">ne (taip, jei P4W)</span><span class="sxs-lookup"><span data-stu-id="ebba6-269">no (yes for P4W)</span></span> |
| <span data-ttu-id="ebba6-270">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-270">msdyn_remainingcost</span></span>                    | <span data-ttu-id="ebba6-271">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-271">no</span></span>             | <span data-ttu-id="ebba6-272">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-272">no</span></span>               |
| <span data-ttu-id="ebba6-273">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-273">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="ebba6-274">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-274">no</span></span>             | <span data-ttu-id="ebba6-275">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-275">no</span></span>               |
| <span data-ttu-id="ebba6-276">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ebba6-276">msdyn_remainingsales</span></span>                   | <span data-ttu-id="ebba6-277">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-277">no</span></span>             | <span data-ttu-id="ebba6-278">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-278">no</span></span>               |
| <span data-ttu-id="ebba6-279">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-279">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="ebba6-280">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-280">no</span></span>             | <span data-ttu-id="ebba6-281">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-281">no</span></span>               |
| <span data-ttu-id="ebba6-282">msdyn_requestedhours</span><span class="sxs-lookup"><span data-stu-id="ebba6-282">msdyn_requestedhours</span></span>                   | <span data-ttu-id="ebba6-283">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-283">no</span></span>             | <span data-ttu-id="ebba6-284">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-284">no</span></span>               |
| <span data-ttu-id="ebba6-285">msdyn_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="ebba6-285">msdyn_resourcecategory</span></span>                 | <span data-ttu-id="ebba6-286">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-286">no</span></span>             | <span data-ttu-id="ebba6-287">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-287">no</span></span>               |
| <span data-ttu-id="ebba6-288">msdyn_resourcecategoryname</span><span class="sxs-lookup"><span data-stu-id="ebba6-288">msdyn_resourcecategoryname</span></span>             | <span data-ttu-id="ebba6-289">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-289">no</span></span>             | <span data-ttu-id="ebba6-290">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-290">no</span></span>               |
| <span data-ttu-id="ebba6-291">msdyn_resourceorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="ebba6-291">msdyn_resourceorganizationalunitid</span></span>     | <span data-ttu-id="ebba6-292">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-292">no</span></span>             | <span data-ttu-id="ebba6-293">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-293">no</span></span>               |
| <span data-ttu-id="ebba6-294">msdyn_resourceorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="ebba6-294">msdyn_resourceorganizationalunitidname</span></span> | <span data-ttu-id="ebba6-295">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-295">no</span></span>             | <span data-ttu-id="ebba6-296">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-296">no</span></span>               |
| <span data-ttu-id="ebba6-297">msdyn_salesconsumptionpercentage</span><span class="sxs-lookup"><span data-stu-id="ebba6-297">msdyn_salesconsumptionpercentage</span></span>       | <span data-ttu-id="ebba6-298">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-298">no</span></span>             | <span data-ttu-id="ebba6-299">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-299">no</span></span>               |
| <span data-ttu-id="ebba6-300">msdyn_salesestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ebba6-300">msdyn_salesestimateatcomplete</span></span>          | <span data-ttu-id="ebba6-301">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-301">no</span></span>             | <span data-ttu-id="ebba6-302">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-302">no</span></span>               |
| <span data-ttu-id="ebba6-303">msdyn_salesestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-303">msdyn_salesestimateatcomplete_base</span></span>     | <span data-ttu-id="ebba6-304">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-304">no</span></span>             | <span data-ttu-id="ebba6-305">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-305">no</span></span>               |
| <span data-ttu-id="ebba6-306">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="ebba6-306">msdyn_salesvariance</span></span>                    | <span data-ttu-id="ebba6-307">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-307">no</span></span>             | <span data-ttu-id="ebba6-308">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-308">no</span></span>               |
| <span data-ttu-id="ebba6-309">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-309">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="ebba6-310">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-310">no</span></span>             | <span data-ttu-id="ebba6-311">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-311">no</span></span>               |
| <span data-ttu-id="ebba6-312">msdyn_scheduleddurationminutes</span><span class="sxs-lookup"><span data-stu-id="ebba6-312">msdyn_scheduleddurationminutes</span></span>         | <span data-ttu-id="ebba6-313">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-313">no</span></span>             | <span data-ttu-id="ebba6-314">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-314">no</span></span>               |
| <span data-ttu-id="ebba6-315">msdyn_scheduledend</span><span class="sxs-lookup"><span data-stu-id="ebba6-315">msdyn_scheduledend</span></span>                     | <span data-ttu-id="ebba6-316">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-316">no</span></span>             | <span data-ttu-id="ebba6-317">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-317">no</span></span>               |
| <span data-ttu-id="ebba6-318">msdyn_scheduledstart</span><span class="sxs-lookup"><span data-stu-id="ebba6-318">msdyn_scheduledstart</span></span>                   | <span data-ttu-id="ebba6-319">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-319">no</span></span>             | <span data-ttu-id="ebba6-320">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-320">no</span></span>               |
| <span data-ttu-id="ebba6-321">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="ebba6-321">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="ebba6-322">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-322">no</span></span>             | <span data-ttu-id="ebba6-323">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-323">no</span></span>               |
| <span data-ttu-id="ebba6-324">msdyn_skipupdateestimateline</span><span class="sxs-lookup"><span data-stu-id="ebba6-324">msdyn_skipupdateestimateline</span></span>           | <span data-ttu-id="ebba6-325">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-325">no</span></span>             | <span data-ttu-id="ebba6-326">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-326">no</span></span>               |
| <span data-ttu-id="ebba6-327">msdyn_skipupdateestimatelinename</span><span class="sxs-lookup"><span data-stu-id="ebba6-327">msdyn_skipupdateestimatelinename</span></span>       | <span data-ttu-id="ebba6-328">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-328">no</span></span>             | <span data-ttu-id="ebba6-329">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-329">no</span></span>               |
| <span data-ttu-id="ebba6-330">msdyn_summary</span><span class="sxs-lookup"><span data-stu-id="ebba6-330">msdyn_summary</span></span>                          | <span data-ttu-id="ebba6-331">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-331">no</span></span>             | <span data-ttu-id="ebba6-332">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-332">no</span></span>               |
| <span data-ttu-id="ebba6-333">msdyn_varianceofcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-333">msdyn_varianceofcost</span></span>                   | <span data-ttu-id="ebba6-334">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-334">no</span></span>             | <span data-ttu-id="ebba6-335">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-335">no</span></span>               |
| <span data-ttu-id="ebba6-336">msdyn_varianceofcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-336">msdyn_varianceofcost_base</span></span>              | <span data-ttu-id="ebba6-337">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-337">no</span></span>             | <span data-ttu-id="ebba6-338">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-338">no</span></span>               |

### <a name="project-task-dependency"></a><span data-ttu-id="ebba6-339">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="ebba6-339">Project task dependency</span></span>

| <span data-ttu-id="ebba6-340">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ebba6-340">**Logical name**</span></span>              | <span data-ttu-id="ebba6-341">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-341">**Can create**</span></span> | <span data-ttu-id="ebba6-342">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-342">**Can edit**</span></span> |
|-------------------------------|----------------|--------------|
| <span data-ttu-id="ebba6-343">msdyn_linktype</span><span class="sxs-lookup"><span data-stu-id="ebba6-343">msdyn_linktype</span></span>                | <span data-ttu-id="ebba6-344">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-344">no</span></span>             | <span data-ttu-id="ebba6-345">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-345">no</span></span>           |
| <span data-ttu-id="ebba6-346">msdyn_linktypename</span><span class="sxs-lookup"><span data-stu-id="ebba6-346">msdyn_linktypename</span></span>            | <span data-ttu-id="ebba6-347">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-347">no</span></span>             | <span data-ttu-id="ebba6-348">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-348">no</span></span>           |
| <span data-ttu-id="ebba6-349">msdyn_predecessortask</span><span class="sxs-lookup"><span data-stu-id="ebba6-349">msdyn_predecessortask</span></span>         | <span data-ttu-id="ebba6-350">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-350">yes</span></span>            | <span data-ttu-id="ebba6-351">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-351">no</span></span>           |
| <span data-ttu-id="ebba6-352">msdyn_predecessortaskname</span><span class="sxs-lookup"><span data-stu-id="ebba6-352">msdyn_predecessortaskname</span></span>     | <span data-ttu-id="ebba6-353">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-353">yes</span></span>            | <span data-ttu-id="ebba6-354">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-354">no</span></span>           |
| <span data-ttu-id="ebba6-355">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ebba6-355">msdyn_project</span></span>                 | <span data-ttu-id="ebba6-356">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-356">yes</span></span>            | <span data-ttu-id="ebba6-357">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-357">no</span></span>           |
| <span data-ttu-id="ebba6-358">msdyn_projectname</span><span class="sxs-lookup"><span data-stu-id="ebba6-358">msdyn_projectname</span></span>             | <span data-ttu-id="ebba6-359">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-359">yes</span></span>            | <span data-ttu-id="ebba6-360">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-360">no</span></span>           |
| <span data-ttu-id="ebba6-361">msdyn_projecttaskdependencyid</span><span class="sxs-lookup"><span data-stu-id="ebba6-361">msdyn_projecttaskdependencyid</span></span> | <span data-ttu-id="ebba6-362">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-362">yes</span></span>            | <span data-ttu-id="ebba6-363">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-363">no</span></span>           |
| <span data-ttu-id="ebba6-364">msdyn_successortask</span><span class="sxs-lookup"><span data-stu-id="ebba6-364">msdyn_successortask</span></span>           | <span data-ttu-id="ebba6-365">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-365">yes</span></span>            | <span data-ttu-id="ebba6-366">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-366">no</span></span>           |
| <span data-ttu-id="ebba6-367">msdyn_successortaskname</span><span class="sxs-lookup"><span data-stu-id="ebba6-367">msdyn_successortaskname</span></span>       | <span data-ttu-id="ebba6-368">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-368">yes</span></span>            | <span data-ttu-id="ebba6-369">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-369">no</span></span>           |

### <a name="resource-assignment"></a><span data-ttu-id="ebba6-370">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-370">Resource assignment</span></span>

| <span data-ttu-id="ebba6-371">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ebba6-371">**Logical name**</span></span>             | <span data-ttu-id="ebba6-372">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-372">**Can create**</span></span> | <span data-ttu-id="ebba6-373">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-373">**Can edit**</span></span> |
|------------------------------|----------------|--------------|
| <span data-ttu-id="ebba6-374">msdyn_bookableresourceid</span><span class="sxs-lookup"><span data-stu-id="ebba6-374">msdyn_bookableresourceid</span></span>     | <span data-ttu-id="ebba6-375">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-375">yes</span></span>            | <span data-ttu-id="ebba6-376">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-376">no</span></span>           |
| <span data-ttu-id="ebba6-377">msdyn_bookableresourceidname</span><span class="sxs-lookup"><span data-stu-id="ebba6-377">msdyn_bookableresourceidname</span></span> | <span data-ttu-id="ebba6-378">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-378">yes</span></span>            | <span data-ttu-id="ebba6-379">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-379">no</span></span>           |
| <span data-ttu-id="ebba6-380">msdyn_bookingstatusid</span><span class="sxs-lookup"><span data-stu-id="ebba6-380">msdyn_bookingstatusid</span></span>        | <span data-ttu-id="ebba6-381">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-381">no</span></span>             | <span data-ttu-id="ebba6-382">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-382">no</span></span>           |
| <span data-ttu-id="ebba6-383">msdyn_bookingstatusidname</span><span class="sxs-lookup"><span data-stu-id="ebba6-383">msdyn_bookingstatusidname</span></span>    | <span data-ttu-id="ebba6-384">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-384">no</span></span>             | <span data-ttu-id="ebba6-385">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-385">no</span></span>           |
| <span data-ttu-id="ebba6-386">msdyn_committype</span><span class="sxs-lookup"><span data-stu-id="ebba6-386">msdyn_committype</span></span>             | <span data-ttu-id="ebba6-387">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-387">no</span></span>             | <span data-ttu-id="ebba6-388">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-388">no</span></span>           |
| <span data-ttu-id="ebba6-389">msdyn_committypename</span><span class="sxs-lookup"><span data-stu-id="ebba6-389">msdyn_committypename</span></span>         | <span data-ttu-id="ebba6-390">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-390">no</span></span>             | <span data-ttu-id="ebba6-391">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-391">no</span></span>           |
| <span data-ttu-id="ebba6-392">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ebba6-392">msdyn_effort</span></span>                 | <span data-ttu-id="ebba6-393">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-393">no</span></span>             | <span data-ttu-id="ebba6-394">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-394">no</span></span>           |
| <span data-ttu-id="ebba6-395">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ebba6-395">msdyn_effortcompleted</span></span>        | <span data-ttu-id="ebba6-396">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-396">no</span></span>             | <span data-ttu-id="ebba6-397">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-397">no</span></span>           |
| <span data-ttu-id="ebba6-398">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ebba6-398">msdyn_effortremaining</span></span>        | <span data-ttu-id="ebba6-399">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-399">no</span></span>             | <span data-ttu-id="ebba6-400">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-400">no</span></span>           |
| <span data-ttu-id="ebba6-401">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ebba6-401">msdyn_finish</span></span>                 | <span data-ttu-id="ebba6-402">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-402">no</span></span>             | <span data-ttu-id="ebba6-403">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-403">no</span></span>           |
| <span data-ttu-id="ebba6-404">msdyn_plannedcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-404">msdyn_plannedcost</span></span>            | <span data-ttu-id="ebba6-405">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-405">no</span></span>             | <span data-ttu-id="ebba6-406">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-406">no</span></span>           |
| <span data-ttu-id="ebba6-407">msdyn_plannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-407">msdyn_plannedcost_base</span></span>       | <span data-ttu-id="ebba6-408">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-408">no</span></span>             | <span data-ttu-id="ebba6-409">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-409">no</span></span>           |
| <span data-ttu-id="ebba6-410">msdyn_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="ebba6-410">msdyn_plannedcostcontour</span></span>     | <span data-ttu-id="ebba6-411">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-411">no</span></span>             | <span data-ttu-id="ebba6-412">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-412">no</span></span>           |
| <span data-ttu-id="ebba6-413">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ebba6-413">msdyn_plannedsales</span></span>           | <span data-ttu-id="ebba6-414">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-414">no</span></span>             | <span data-ttu-id="ebba6-415">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-415">no</span></span>           |
| <span data-ttu-id="ebba6-416">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-416">msdyn_plannedsales_base</span></span>      | <span data-ttu-id="ebba6-417">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-417">no</span></span>             | <span data-ttu-id="ebba6-418">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-418">no</span></span>           |
| <span data-ttu-id="ebba6-419">msdyn_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="ebba6-419">msdyn_plannedsalescontour</span></span>    | <span data-ttu-id="ebba6-420">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-420">no</span></span>             | <span data-ttu-id="ebba6-421">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-421">no</span></span>           |
| <span data-ttu-id="ebba6-422">msdyn_plannedwork</span><span class="sxs-lookup"><span data-stu-id="ebba6-422">msdyn_plannedwork</span></span>            | <span data-ttu-id="ebba6-423">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-423">no</span></span>             | <span data-ttu-id="ebba6-424">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-424">no</span></span>           |
| <span data-ttu-id="ebba6-425">msdyn_projectid</span><span class="sxs-lookup"><span data-stu-id="ebba6-425">msdyn_projectid</span></span>              | <span data-ttu-id="ebba6-426">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-426">yes</span></span>            | <span data-ttu-id="ebba6-427">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-427">no</span></span>           |
| <span data-ttu-id="ebba6-428">msdyn_projectidname</span><span class="sxs-lookup"><span data-stu-id="ebba6-428">msdyn_projectidname</span></span>          | <span data-ttu-id="ebba6-429">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-429">no</span></span>             | <span data-ttu-id="ebba6-430">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-430">no</span></span>           |
| <span data-ttu-id="ebba6-431">msdyn_projectteamid</span><span class="sxs-lookup"><span data-stu-id="ebba6-431">msdyn_projectteamid</span></span>          | <span data-ttu-id="ebba6-432">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-432">no</span></span>             | <span data-ttu-id="ebba6-433">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-433">no</span></span>           |
| <span data-ttu-id="ebba6-434">msdyn_projectteamidname</span><span class="sxs-lookup"><span data-stu-id="ebba6-434">msdyn_projectteamidname</span></span>      | <span data-ttu-id="ebba6-435">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-435">no</span></span>             | <span data-ttu-id="ebba6-436">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-436">no</span></span>           |
| <span data-ttu-id="ebba6-437">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="ebba6-437">msdyn_start</span></span>                  | <span data-ttu-id="ebba6-438">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-438">no</span></span>             | <span data-ttu-id="ebba6-439">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-439">no</span></span>           |
| <span data-ttu-id="ebba6-440">msdyn_taskid</span><span class="sxs-lookup"><span data-stu-id="ebba6-440">msdyn_taskid</span></span>                 | <span data-ttu-id="ebba6-441">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-441">no</span></span>             | <span data-ttu-id="ebba6-442">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-442">no</span></span>           |
| <span data-ttu-id="ebba6-443">msdyn_taskidname</span><span class="sxs-lookup"><span data-stu-id="ebba6-443">msdyn_taskidname</span></span>             | <span data-ttu-id="ebba6-444">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-444">no</span></span>             | <span data-ttu-id="ebba6-445">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-445">no</span></span>           |
| <span data-ttu-id="ebba6-446">msdyn_userresourceid</span><span class="sxs-lookup"><span data-stu-id="ebba6-446">msdyn_userresourceid</span></span>         | <span data-ttu-id="ebba6-447">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-447">no</span></span>             | <span data-ttu-id="ebba6-448">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-448">no</span></span>           |

### <a name="project-team-member"></a><span data-ttu-id="ebba6-449">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="ebba6-449">Project team member</span></span>

| <span data-ttu-id="ebba6-450">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ebba6-450">**Logical name**</span></span>                                 | <span data-ttu-id="ebba6-451">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-451">**Can create**</span></span> | <span data-ttu-id="ebba6-452">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-452">**Can edit**</span></span> |
|--------------------------------------------------|----------------|--------------|
| <span data-ttu-id="ebba6-453">msdyn_calendarid</span><span class="sxs-lookup"><span data-stu-id="ebba6-453">msdyn_calendarid</span></span>                                 | <span data-ttu-id="ebba6-454">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-454">no</span></span>             | <span data-ttu-id="ebba6-455">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-455">no</span></span>           |
| <span data-ttu-id="ebba6-456">msdyn_creategenericteammemberwithrequirementname</span><span class="sxs-lookup"><span data-stu-id="ebba6-456">msdyn_creategenericteammemberwithrequirementname</span></span> | <span data-ttu-id="ebba6-457">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-457">no</span></span>             | <span data-ttu-id="ebba6-458">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-458">no</span></span>           |
| <span data-ttu-id="ebba6-459">msdyn_deletestatus</span><span class="sxs-lookup"><span data-stu-id="ebba6-459">msdyn_deletestatus</span></span>                               | <span data-ttu-id="ebba6-460">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-460">no</span></span>             | <span data-ttu-id="ebba6-461">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-461">no</span></span>           |
| <span data-ttu-id="ebba6-462">msdyn_deletestatusname</span><span class="sxs-lookup"><span data-stu-id="ebba6-462">msdyn_deletestatusname</span></span>                           | <span data-ttu-id="ebba6-463">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-463">no</span></span>             | <span data-ttu-id="ebba6-464">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-464">no</span></span>           |
| <span data-ttu-id="ebba6-465">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ebba6-465">msdyn_effort</span></span>                                     | <span data-ttu-id="ebba6-466">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-466">no</span></span>             | <span data-ttu-id="ebba6-467">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-467">no</span></span>           |
| <span data-ttu-id="ebba6-468">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ebba6-468">msdyn_effortcompleted</span></span>                            | <span data-ttu-id="ebba6-469">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-469">no</span></span>             | <span data-ttu-id="ebba6-470">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-470">no</span></span>           |
| <span data-ttu-id="ebba6-471">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ebba6-471">msdyn_effortremaining</span></span>                            | <span data-ttu-id="ebba6-472">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-472">no</span></span>             | <span data-ttu-id="ebba6-473">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-473">no</span></span>           |
| <span data-ttu-id="ebba6-474">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ebba6-474">msdyn_finish</span></span>                                     | <span data-ttu-id="ebba6-475">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-475">no</span></span>             | <span data-ttu-id="ebba6-476">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-476">no</span></span>           |
| <span data-ttu-id="ebba6-477">msdyn_hardbookedhours</span><span class="sxs-lookup"><span data-stu-id="ebba6-477">msdyn_hardbookedhours</span></span>                            | <span data-ttu-id="ebba6-478">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-478">no</span></span>             | <span data-ttu-id="ebba6-479">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-479">no</span></span>           |
| <span data-ttu-id="ebba6-480">msdyn_hours</span><span class="sxs-lookup"><span data-stu-id="ebba6-480">msdyn_hours</span></span>                                      | <span data-ttu-id="ebba6-481">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-481">no</span></span>             | <span data-ttu-id="ebba6-482">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-482">no</span></span>           |
| <span data-ttu-id="ebba6-483">msdyn_markedfordeletiontimer</span><span class="sxs-lookup"><span data-stu-id="ebba6-483">msdyn_markedfordeletiontimer</span></span>                     | <span data-ttu-id="ebba6-484">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-484">no</span></span>             | <span data-ttu-id="ebba6-485">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-485">no</span></span>           |
| <span data-ttu-id="ebba6-486">msdyn_markedfordeletiontimestamp</span><span class="sxs-lookup"><span data-stu-id="ebba6-486">msdyn_markedfordeletiontimestamp</span></span>                 | <span data-ttu-id="ebba6-487">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-487">no</span></span>             | <span data-ttu-id="ebba6-488">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-488">no</span></span>           |
| <span data-ttu-id="ebba6-489">msdyn_msprojectclientid</span><span class="sxs-lookup"><span data-stu-id="ebba6-489">msdyn_msprojectclientid</span></span>                          | <span data-ttu-id="ebba6-490">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-490">no</span></span>             | <span data-ttu-id="ebba6-491">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-491">no</span></span>           |
| <span data-ttu-id="ebba6-492">msdyn_percentage</span><span class="sxs-lookup"><span data-stu-id="ebba6-492">msdyn_percentage</span></span>                                 | <span data-ttu-id="ebba6-493">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-493">no</span></span>             | <span data-ttu-id="ebba6-494">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-494">no</span></span>           |
| <span data-ttu-id="ebba6-495">msdyn_requiredhours</span><span class="sxs-lookup"><span data-stu-id="ebba6-495">msdyn_requiredhours</span></span>                              | <span data-ttu-id="ebba6-496">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-496">no</span></span>             | <span data-ttu-id="ebba6-497">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-497">no</span></span>           |
| <span data-ttu-id="ebba6-498">msdyn_softbookedhours</span><span class="sxs-lookup"><span data-stu-id="ebba6-498">msdyn_softbookedhours</span></span>                            | <span data-ttu-id="ebba6-499">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-499">no</span></span>             | <span data-ttu-id="ebba6-500">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-500">no</span></span>           |
| <span data-ttu-id="ebba6-501">msdyn_start</span><span class="sxs-lookup"><span data-stu-id="ebba6-501">msdyn_start</span></span>                                      | <span data-ttu-id="ebba6-502">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-502">no</span></span>             | <span data-ttu-id="ebba6-503">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-503">no</span></span>           |

### <a name="project"></a><span data-ttu-id="ebba6-504">Project</span><span class="sxs-lookup"><span data-stu-id="ebba6-504">Project</span></span>

| <span data-ttu-id="ebba6-505">**Loginis pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ebba6-505">**Logical name**</span></span>                       | <span data-ttu-id="ebba6-506">**Gali kurti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-506">**Can create**</span></span> | <span data-ttu-id="ebba6-507">**Gali redaguoti**</span><span class="sxs-lookup"><span data-stu-id="ebba6-507">**Can edit**</span></span> |
|----------------------------------------|----------------|--------------|
| <span data-ttu-id="ebba6-508">msdyn_actualexpensecost</span><span class="sxs-lookup"><span data-stu-id="ebba6-508">msdyn_actualexpensecost</span></span>                | <span data-ttu-id="ebba6-509">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-509">no</span></span>             | <span data-ttu-id="ebba6-510">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-510">no</span></span>           |
| <span data-ttu-id="ebba6-511">msdyn_actualexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-511">msdyn_actualexpensecost_base</span></span>           | <span data-ttu-id="ebba6-512">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-512">no</span></span>             | <span data-ttu-id="ebba6-513">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-513">no</span></span>           |
| <span data-ttu-id="ebba6-514">msdyn_actuallaborcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-514">msdyn_actuallaborcost</span></span>                  | <span data-ttu-id="ebba6-515">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-515">no</span></span>             | <span data-ttu-id="ebba6-516">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-516">no</span></span>           |
| <span data-ttu-id="ebba6-517">msdyn_actuallaborcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-517">msdyn_actuallaborcost_base</span></span>             | <span data-ttu-id="ebba6-518">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-518">no</span></span>             | <span data-ttu-id="ebba6-519">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-519">no</span></span>           |
| <span data-ttu-id="ebba6-520">msdyn_actualsales</span><span class="sxs-lookup"><span data-stu-id="ebba6-520">msdyn_actualsales</span></span>                      | <span data-ttu-id="ebba6-521">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-521">no</span></span>             | <span data-ttu-id="ebba6-522">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-522">no</span></span>           |
| <span data-ttu-id="ebba6-523">msdyn_actualsales_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-523">msdyn_actualsales_base</span></span>                 | <span data-ttu-id="ebba6-524">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-524">no</span></span>             | <span data-ttu-id="ebba6-525">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-525">no</span></span>           |
| <span data-ttu-id="ebba6-526">msdyn_contractlineproject</span><span class="sxs-lookup"><span data-stu-id="ebba6-526">msdyn_contractlineproject</span></span>              | <span data-ttu-id="ebba6-527">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-527">yes</span></span>            | <span data-ttu-id="ebba6-528">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-528">no</span></span>           |
| <span data-ttu-id="ebba6-529">msdyn_contractorganizationalunitid</span><span class="sxs-lookup"><span data-stu-id="ebba6-529">msdyn_contractorganizationalunitid</span></span>     | <span data-ttu-id="ebba6-530">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-530">yes</span></span>            | <span data-ttu-id="ebba6-531">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-531">no</span></span>           |
| <span data-ttu-id="ebba6-532">msdyn_contractorganizationalunitidname</span><span class="sxs-lookup"><span data-stu-id="ebba6-532">msdyn_contractorganizationalunitidname</span></span> | <span data-ttu-id="ebba6-533">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-533">yes</span></span>            | <span data-ttu-id="ebba6-534">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-534">no</span></span>           |
| <span data-ttu-id="ebba6-535">msdyn_costconsumption</span><span class="sxs-lookup"><span data-stu-id="ebba6-535">msdyn_costconsumption</span></span>                  | <span data-ttu-id="ebba6-536">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-536">no</span></span>             | <span data-ttu-id="ebba6-537">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-537">no</span></span>           |
| <span data-ttu-id="ebba6-538">msdyn_costestimateatcomplete</span><span class="sxs-lookup"><span data-stu-id="ebba6-538">msdyn_costestimateatcomplete</span></span>           | <span data-ttu-id="ebba6-539">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-539">no</span></span>             | <span data-ttu-id="ebba6-540">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-540">no</span></span>           |
| <span data-ttu-id="ebba6-541">msdyn_costestimateatcomplete_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-541">msdyn_costestimateatcomplete_base</span></span>      | <span data-ttu-id="ebba6-542">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-542">no</span></span>             | <span data-ttu-id="ebba6-543">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-543">no</span></span>           |
| <span data-ttu-id="ebba6-544">msdyn_costvariance</span><span class="sxs-lookup"><span data-stu-id="ebba6-544">msdyn_costvariance</span></span>                     | <span data-ttu-id="ebba6-545">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-545">no</span></span>             | <span data-ttu-id="ebba6-546">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-546">no</span></span>           |
| <span data-ttu-id="ebba6-547">msdyn_costvariance_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-547">msdyn_costvariance_base</span></span>                | <span data-ttu-id="ebba6-548">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-548">no</span></span>             | <span data-ttu-id="ebba6-549">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-549">no</span></span>           |
| <span data-ttu-id="ebba6-550">msdyn_duration</span><span class="sxs-lookup"><span data-stu-id="ebba6-550">msdyn_duration</span></span>                         | <span data-ttu-id="ebba6-551">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-551">no</span></span>             | <span data-ttu-id="ebba6-552">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-552">no</span></span>           |
| <span data-ttu-id="ebba6-553">msdyn_effort</span><span class="sxs-lookup"><span data-stu-id="ebba6-553">msdyn_effort</span></span>                           | <span data-ttu-id="ebba6-554">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-554">no</span></span>             | <span data-ttu-id="ebba6-555">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-555">no</span></span>           |
| <span data-ttu-id="ebba6-556">msdyn_effortcompleted</span><span class="sxs-lookup"><span data-stu-id="ebba6-556">msdyn_effortcompleted</span></span>                  | <span data-ttu-id="ebba6-557">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-557">no</span></span>             | <span data-ttu-id="ebba6-558">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-558">no</span></span>           |
| <span data-ttu-id="ebba6-559">msdyn_effortestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="ebba6-559">msdyn_effortestimateatcompleteeac</span></span>      | <span data-ttu-id="ebba6-560">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-560">no</span></span>             | <span data-ttu-id="ebba6-561">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-561">no</span></span>           |
| <span data-ttu-id="ebba6-562">msdyn_effortremaining</span><span class="sxs-lookup"><span data-stu-id="ebba6-562">msdyn_effortremaining</span></span>                  | <span data-ttu-id="ebba6-563">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-563">no</span></span>             | <span data-ttu-id="ebba6-564">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-564">no</span></span>           |
| <span data-ttu-id="ebba6-565">msdyn_finish</span><span class="sxs-lookup"><span data-stu-id="ebba6-565">msdyn_finish</span></span>                           | <span data-ttu-id="ebba6-566">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-566">yes</span></span>            | <span data-ttu-id="ebba6-567">taip</span><span class="sxs-lookup"><span data-stu-id="ebba6-567">yes</span></span>          |
| <span data-ttu-id="ebba6-568">msdyn_globalrevisiontoken</span><span class="sxs-lookup"><span data-stu-id="ebba6-568">msdyn_globalrevisiontoken</span></span>              | <span data-ttu-id="ebba6-569">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-569">no</span></span>             | <span data-ttu-id="ebba6-570">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-570">no</span></span>           |
| <span data-ttu-id="ebba6-571">msdyn_islinkedtomsprojectclient</span><span class="sxs-lookup"><span data-stu-id="ebba6-571">msdyn_islinkedtomsprojectclient</span></span>        | <span data-ttu-id="ebba6-572">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-572">no</span></span>             | <span data-ttu-id="ebba6-573">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-573">no</span></span>           |
| <span data-ttu-id="ebba6-574">msdyn_islinkedtomsprojectclientname</span><span class="sxs-lookup"><span data-stu-id="ebba6-574">msdyn_islinkedtomsprojectclientname</span></span>    | <span data-ttu-id="ebba6-575">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-575">no</span></span>             | <span data-ttu-id="ebba6-576">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-576">no</span></span>           |
| <span data-ttu-id="ebba6-577">msdyn_linkeddocumenturl</span><span class="sxs-lookup"><span data-stu-id="ebba6-577">msdyn_linkeddocumenturl</span></span>                | <span data-ttu-id="ebba6-578">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-578">no</span></span>             | <span data-ttu-id="ebba6-579">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-579">no</span></span>           |
| <span data-ttu-id="ebba6-580">msdyn_msprojectdocument</span><span class="sxs-lookup"><span data-stu-id="ebba6-580">msdyn_msprojectdocument</span></span>                | <span data-ttu-id="ebba6-581">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-581">no</span></span>             | <span data-ttu-id="ebba6-582">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-582">no</span></span>           |
| <span data-ttu-id="ebba6-583">msdyn_msprojectdocumentname</span><span class="sxs-lookup"><span data-stu-id="ebba6-583">msdyn_msprojectdocumentname</span></span>            | <span data-ttu-id="ebba6-584">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-584">no</span></span>             | <span data-ttu-id="ebba6-585">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-585">no</span></span>           |
| <span data-ttu-id="ebba6-586">msdyn_plannedexpensecost</span><span class="sxs-lookup"><span data-stu-id="ebba6-586">msdyn_plannedexpensecost</span></span>               | <span data-ttu-id="ebba6-587">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-587">no</span></span>             | <span data-ttu-id="ebba6-588">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-588">no</span></span>           |
| <span data-ttu-id="ebba6-589">msdyn_plannedexpensecost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-589">msdyn_plannedexpensecost_base</span></span>          | <span data-ttu-id="ebba6-590">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-590">no</span></span>             | <span data-ttu-id="ebba6-591">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-591">no</span></span>           |
| <span data-ttu-id="ebba6-592">msdyn_plannedlaborcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-592">msdyn_plannedlaborcost</span></span>                 | <span data-ttu-id="ebba6-593">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-593">no</span></span>             | <span data-ttu-id="ebba6-594">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-594">no</span></span>           |
| <span data-ttu-id="ebba6-595">msdyn_plannedlaborcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-595">msdyn_plannedlaborcost_base</span></span>            | <span data-ttu-id="ebba6-596">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-596">no</span></span>             | <span data-ttu-id="ebba6-597">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-597">no</span></span>           |
| <span data-ttu-id="ebba6-598">msdyn_plannedsales</span><span class="sxs-lookup"><span data-stu-id="ebba6-598">msdyn_plannedsales</span></span>                     | <span data-ttu-id="ebba6-599">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-599">no</span></span>             | <span data-ttu-id="ebba6-600">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-600">no</span></span>           |
| <span data-ttu-id="ebba6-601">msdyn_plannedsales_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-601">msdyn_plannedsales_base</span></span>                | <span data-ttu-id="ebba6-602">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-602">no</span></span>             | <span data-ttu-id="ebba6-603">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-603">no</span></span>           |
| <span data-ttu-id="ebba6-604">msdyn_progress</span><span class="sxs-lookup"><span data-stu-id="ebba6-604">msdyn_progress</span></span>                         | <span data-ttu-id="ebba6-605">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-605">no</span></span>             | <span data-ttu-id="ebba6-606">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-606">no</span></span>           |
| <span data-ttu-id="ebba6-607">msdyn_remainingcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-607">msdyn_remainingcost</span></span>                    | <span data-ttu-id="ebba6-608">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-608">no</span></span>             | <span data-ttu-id="ebba6-609">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-609">no</span></span>           |
| <span data-ttu-id="ebba6-610">msdyn_remainingcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-610">msdyn_remainingcost_base</span></span>               | <span data-ttu-id="ebba6-611">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-611">no</span></span>             | <span data-ttu-id="ebba6-612">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-612">no</span></span>           |
| <span data-ttu-id="ebba6-613">msdyn_remainingsales</span><span class="sxs-lookup"><span data-stu-id="ebba6-613">msdyn_remainingsales</span></span>                   | <span data-ttu-id="ebba6-614">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-614">no</span></span>             | <span data-ttu-id="ebba6-615">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-615">no</span></span>           |
| <span data-ttu-id="ebba6-616">msdyn_remainingsales_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-616">msdyn_remainingsales_base</span></span>              | <span data-ttu-id="ebba6-617">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-617">no</span></span>             | <span data-ttu-id="ebba6-618">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-618">no</span></span>           |
| <span data-ttu-id="ebba6-619">msdyn_replaylogheader</span><span class="sxs-lookup"><span data-stu-id="ebba6-619">msdyn_replaylogheader</span></span>                  | <span data-ttu-id="ebba6-620">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-620">no</span></span>             | <span data-ttu-id="ebba6-621">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-621">no</span></span>           |
| <span data-ttu-id="ebba6-622">msdyn_salesconsumption</span><span class="sxs-lookup"><span data-stu-id="ebba6-622">msdyn_salesconsumption</span></span>                 | <span data-ttu-id="ebba6-623">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-623">no</span></span>             | <span data-ttu-id="ebba6-624">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-624">no</span></span>           |
| <span data-ttu-id="ebba6-625">msdyn_salesestimateatcompleteeac</span><span class="sxs-lookup"><span data-stu-id="ebba6-625">msdyn_salesestimateatcompleteeac</span></span>       | <span data-ttu-id="ebba6-626">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-626">no</span></span>             | <span data-ttu-id="ebba6-627">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-627">no</span></span>           |
| <span data-ttu-id="ebba6-628">msdyn_salesestimateatcompleteeac_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-628">msdyn_salesestimateatcompleteeac_base</span></span>  | <span data-ttu-id="ebba6-629">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-629">no</span></span>             | <span data-ttu-id="ebba6-630">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-630">no</span></span>           |
| <span data-ttu-id="ebba6-631">msdyn_salesvariance</span><span class="sxs-lookup"><span data-stu-id="ebba6-631">msdyn_salesvariance</span></span>                    | <span data-ttu-id="ebba6-632">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-632">no</span></span>             | <span data-ttu-id="ebba6-633">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-633">no</span></span>           |
| <span data-ttu-id="ebba6-634">msdyn_salesvariance_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-634">msdyn_salesvariance_base</span></span>               | <span data-ttu-id="ebba6-635">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-635">no</span></span>             | <span data-ttu-id="ebba6-636">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-636">no</span></span>           |
| <span data-ttu-id="ebba6-637">msdyn_scheduleperformance</span><span class="sxs-lookup"><span data-stu-id="ebba6-637">msdyn_scheduleperformance</span></span>              | <span data-ttu-id="ebba6-638">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-638">no</span></span>             | <span data-ttu-id="ebba6-639">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-639">no</span></span>           |
| <span data-ttu-id="ebba6-640">msdyn_scheduleperformancename</span><span class="sxs-lookup"><span data-stu-id="ebba6-640">msdyn_scheduleperformancename</span></span>          | <span data-ttu-id="ebba6-641">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-641">no</span></span>             | <span data-ttu-id="ebba6-642">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-642">no</span></span>           |
| <span data-ttu-id="ebba6-643">msdyn_schedulevariance</span><span class="sxs-lookup"><span data-stu-id="ebba6-643">msdyn_schedulevariance</span></span>                 | <span data-ttu-id="ebba6-644">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-644">no</span></span>             | <span data-ttu-id="ebba6-645">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-645">no</span></span>           |
| <span data-ttu-id="ebba6-646">msdyn_taskearlieststart</span><span class="sxs-lookup"><span data-stu-id="ebba6-646">msdyn_taskearlieststart</span></span>                | <span data-ttu-id="ebba6-647">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-647">no</span></span>             | <span data-ttu-id="ebba6-648">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-648">no</span></span>           |
| <span data-ttu-id="ebba6-649">msdyn_teamsize</span><span class="sxs-lookup"><span data-stu-id="ebba6-649">msdyn_teamsize</span></span>                         | <span data-ttu-id="ebba6-650">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-650">no</span></span>             | <span data-ttu-id="ebba6-651">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-651">no</span></span>           |
| <span data-ttu-id="ebba6-652">msdyn_teamsize_date</span><span class="sxs-lookup"><span data-stu-id="ebba6-652">msdyn_teamsize_date</span></span>                    | <span data-ttu-id="ebba6-653">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-653">no</span></span>             | <span data-ttu-id="ebba6-654">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-654">no</span></span>           |
| <span data-ttu-id="ebba6-655">msdyn_teamsize_state</span><span class="sxs-lookup"><span data-stu-id="ebba6-655">msdyn_teamsize_state</span></span>                   | <span data-ttu-id="ebba6-656">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-656">no</span></span>             | <span data-ttu-id="ebba6-657">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-657">no</span></span>           |
| <span data-ttu-id="ebba6-658">msdyn_totalactualcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-658">msdyn_totalactualcost</span></span>                  | <span data-ttu-id="ebba6-659">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-659">no</span></span>             | <span data-ttu-id="ebba6-660">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-660">no</span></span>           |
| <span data-ttu-id="ebba6-661">msdyn_totalactualcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-661">msdyn_totalactualcost_base</span></span>             | <span data-ttu-id="ebba6-662">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-662">no</span></span>             | <span data-ttu-id="ebba6-663">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-663">no</span></span>           |
| <span data-ttu-id="ebba6-664">msdyn_totalplannedcost</span><span class="sxs-lookup"><span data-stu-id="ebba6-664">msdyn_totalplannedcost</span></span>                 | <span data-ttu-id="ebba6-665">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-665">no</span></span>             | <span data-ttu-id="ebba6-666">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-666">no</span></span>           |
| <span data-ttu-id="ebba6-667">msdyn_totalplannedcost_base</span><span class="sxs-lookup"><span data-stu-id="ebba6-667">msdyn_totalplannedcost_base</span></span>            | <span data-ttu-id="ebba6-668">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-668">no</span></span>             | <span data-ttu-id="ebba6-669">ne</span><span class="sxs-lookup"><span data-stu-id="ebba6-669">no</span></span>           |


## <a name="limitations-and-known-issues"></a><span data-ttu-id="ebba6-670">Apribojimai ir žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="ebba6-670">Limitations and known issues</span></span>
<span data-ttu-id="ebba6-671">Toliau pateikiamas apribojimų ir žinomų problemų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ebba6-671">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="ebba6-672">Grafiko API gali naudoti tik **vartotojai, turintys „Microsoft Project“ licenciją.**</span><span class="sxs-lookup"><span data-stu-id="ebba6-672">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="ebba6-673">Jų negali toliau nurodyti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="ebba6-673">They can't be used by:</span></span>
    - <span data-ttu-id="ebba6-674">Programų vartotojai</span><span class="sxs-lookup"><span data-stu-id="ebba6-674">Application users</span></span>
    - <span data-ttu-id="ebba6-675">Sistemos vartotojai</span><span class="sxs-lookup"><span data-stu-id="ebba6-675">System users</span></span>
    - <span data-ttu-id="ebba6-676">Integravimo vartotojai</span><span class="sxs-lookup"><span data-stu-id="ebba6-676">Integration users</span></span>
    - <span data-ttu-id="ebba6-677">Kiti vartotojai, neturintys reikiamos licencijos</span><span class="sxs-lookup"><span data-stu-id="ebba6-677">Other users that don't have the required license</span></span>
- <span data-ttu-id="ebba6-678">Kiekviename **OperationSet** gali būti ne daugiau kaip 100 operacijų.</span><span class="sxs-lookup"><span data-stu-id="ebba6-678">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="ebba6-679">Kiekvienas vartotojas gali turėti ne daugiau kaip 10 atvirų **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-679">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="ebba6-680">„Project Operations“ šiuo metu palaikoma ne daugiau kaip 500 projekto užduočių iš viso.</span><span class="sxs-lookup"><span data-stu-id="ebba6-680">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="ebba6-681">**OperationSet** trikties būsena ir trikties žurnalai šiuo metu negalimi.</span><span class="sxs-lookup"><span data-stu-id="ebba6-681">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- [<span data-ttu-id="ebba6-682">Projektų ir užduočių limitai bei ribos</span><span class="sxs-lookup"><span data-stu-id="ebba6-682">Limits and boundaries on projects and tasks</span></span>](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a><span data-ttu-id="ebba6-683">Klaidų apdorojimas</span><span class="sxs-lookup"><span data-stu-id="ebba6-683">Error handling</span></span>

   - <span data-ttu-id="ebba6-684">Norėdami peržiūrėti iš operacijų rinkinių sugeneruotas klaidas, eikite į **Parametrai** \> **Grafiko integravimas** \> **Operacijų rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-684">To review errors generated from the Operation Sets, go to **Settings** \> **Schedule Integration** \> **Operations Sets**.</span></span>
   - <span data-ttu-id="ebba6-685">Norėdami peržiūrėti iš projektų planavimo tarnybos sugeneruotas klaidas, eikite į **Parametrai** \> **Grafiko integravimas** \> **PSS klaidų žurnalai**.</span><span class="sxs-lookup"><span data-stu-id="ebba6-685">To review errors generated from the Project Scheduling Service, go to **Settings** \> **Schedule Integration** \> **PSS Error Logs**.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="ebba6-686">Scenarijaus pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ebba6-686">Sample scenario</span></span>

<span data-ttu-id="ebba6-687">Pagal šį scenarijų sukursite projektą, komandos narį, keturias užduotis ir du išteklių priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="ebba6-687">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="ebba6-688">Tada atnaujinsite vieną užduotį, atnaujinsite projektą, panaikinsite vieną užduotį, panaikinsite vieną išteklių priskyrimą ir sukursite užduoties priklausomybę.</span><span class="sxs-lookup"><span data-stu-id="ebba6-688">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

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

## <a name="additional-samples"></a><span data-ttu-id="ebba6-689">Papildomi pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="ebba6-689">Additional samples</span></span>

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
