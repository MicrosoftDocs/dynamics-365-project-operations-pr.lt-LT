---
title: Grafiko API naudojimas norint atlikti operacijas su grafiko objektais
description: Šioje temoje pateikiama informacija ir pavyzdžiai, kaip naudoti grafiko API.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868139"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a><span data-ttu-id="ab422-103">Grafiko API naudojimas norint atlikti operacijas su grafiko objektais</span><span class="sxs-lookup"><span data-stu-id="ab422-103">Use Schedule APIs to perform operations with Scheduling entities</span></span>

<span data-ttu-id="ab422-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="ab422-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT] 
> <span data-ttu-id="ab422-105">Kai kurios arba visos šioje temoje paminėtos funkcijos pasiekiamos kaip peržiūros versijos leidimo dalis.</span><span class="sxs-lookup"><span data-stu-id="ab422-105">Some or all of the functionality noted in this topic is available as part of a preview release.</span></span> <span data-ttu-id="ab422-106">Turinys ir funkcijos gali keistis.</span><span class="sxs-lookup"><span data-stu-id="ab422-106">The content and the functionality are subject to change.</span></span> 

## <a name="scheduling-entities"></a><span data-ttu-id="ab422-107">Grafiko objektai</span><span class="sxs-lookup"><span data-stu-id="ab422-107">Scheduling entities</span></span>

<span data-ttu-id="ab422-108">Grafiko API suteikia galimybę atlikti kūrimo, naujinimo ir naikinimo operacijas naudojant **grafiko objektus**.</span><span class="sxs-lookup"><span data-stu-id="ab422-108">Schedule APIs provide the ability to perform create, update, and delete operations with **Scheduling entities**.</span></span> <span data-ttu-id="ab422-109">Šie objektai valdomi naudojant „Project for the Web“ planavimo variklį.</span><span class="sxs-lookup"><span data-stu-id="ab422-109">These entities are managed through the Scheduling engine in Project for the web.</span></span> <span data-ttu-id="ab422-110">Ankstesniuose „Dynamics 365 Project Operations“ leidimuose operacijų kūrimas, naujinimas ir naikinimas naudojant **planavimo objektus** buvo apribotas.</span><span class="sxs-lookup"><span data-stu-id="ab422-110">Create, update, and delete operations with **Scheduling entities** were restricted in earlier Dynamics 365 Project Operations releases.</span></span>

<span data-ttu-id="ab422-111">Toliau esančioje lentelėje pateikiamas visas **planavimo objektų** sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ab422-111">The following table provides a full list of the **Scheduling entities**.</span></span>

| <span data-ttu-id="ab422-112">Objekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ab422-112">Entity name</span></span>  | <span data-ttu-id="ab422-113">Loginis objekto pavadinimas</span><span class="sxs-lookup"><span data-stu-id="ab422-113">Entity logical name</span></span> |
| --- | --- |
| <span data-ttu-id="ab422-114">Project</span><span class="sxs-lookup"><span data-stu-id="ab422-114">Project</span></span> | <span data-ttu-id="ab422-115">msdyn_project</span><span class="sxs-lookup"><span data-stu-id="ab422-115">msdyn_project</span></span> |
| <span data-ttu-id="ab422-116">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="ab422-116">Project Task</span></span>  | <span data-ttu-id="ab422-117">msdyn_projecttask</span><span class="sxs-lookup"><span data-stu-id="ab422-117">msdyn_projecttask</span></span>  |
| <span data-ttu-id="ab422-118">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="ab422-118">Project Task Dependency</span></span>  | <span data-ttu-id="ab422-119">msdyn_projecttaskdependency</span><span class="sxs-lookup"><span data-stu-id="ab422-119">msdyn_projecttaskdependency</span></span>  |
| <span data-ttu-id="ab422-120">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="ab422-120">Resource Assignment</span></span> | <span data-ttu-id="ab422-121">msdyn_resourceassignment</span><span class="sxs-lookup"><span data-stu-id="ab422-121">msdyn_resourceassignment</span></span> |
| <span data-ttu-id="ab422-122">Projekto talpykla</span><span class="sxs-lookup"><span data-stu-id="ab422-122">Project Bucket</span></span>  | <span data-ttu-id="ab422-123">msdyn_projectbucket</span><span class="sxs-lookup"><span data-stu-id="ab422-123">msdyn_projectbucket</span></span> |
| <span data-ttu-id="ab422-124">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="ab422-124">Project Team Member</span></span> | <span data-ttu-id="ab422-125">msdyn_projectteam</span><span class="sxs-lookup"><span data-stu-id="ab422-125">msdyn_projectteam</span></span> |

## <a name="operationset"></a><span data-ttu-id="ab422-126">OperationSet</span><span class="sxs-lookup"><span data-stu-id="ab422-126">OperationSet</span></span>

<span data-ttu-id="ab422-127">OperationSet yra darbo vieneto modelis, kurį galima naudoti, kai operacijoje reikia apdoroti keletą grafikui poveikį darančių užklausų.</span><span class="sxs-lookup"><span data-stu-id="ab422-127">OperationSet is a unit-of-work pattern that can be used when several schedule impacting requests must be processed within a transaction.</span></span>

## <a name="schedule-apis"></a><span data-ttu-id="ab422-128">Grafiko API</span><span class="sxs-lookup"><span data-stu-id="ab422-128">Schedule APIs</span></span>

<span data-ttu-id="ab422-129">Toliau pateikiamas dabartinių grafiko API sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ab422-129">The following is a list of current Schedule APIs.</span></span>

- <span data-ttu-id="ab422-130">**msdyn_CreateProjectV1**: šį API galima naudoti norint sukurti projektą.</span><span class="sxs-lookup"><span data-stu-id="ab422-130">**msdyn_CreateProjectV1**: This API can be used to create a project.</span></span> <span data-ttu-id="ab422-131">Projektas ir numatytoji projekto talpykla sukuriami nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="ab422-131">The project and default project bucket is created immediately.</span></span>
- <span data-ttu-id="ab422-132">**msdyn_CreateTeamMemberV1**:šį API galima naudoti norint sukurti projekto komandos narį.</span><span class="sxs-lookup"><span data-stu-id="ab422-132">**msdyn_CreateTeamMemberV1**: This API can be used to create a project team member.</span></span> <span data-ttu-id="ab422-133">Komandos nario įrašas sukuriamas nedelsiant.</span><span class="sxs-lookup"><span data-stu-id="ab422-133">The team member record is created immediately.</span></span>
- <span data-ttu-id="ab422-134">**msdyn_CreateOperationSetV1**: šį API galima naudoti norint suplanuoti keletą užklausų, kurias reikia atlikti operacijoje.</span><span class="sxs-lookup"><span data-stu-id="ab422-134">**msdyn_CreateOperationSetV1**: This API can be used to schedule several requests that must be performed within a transaction.</span></span>
- <span data-ttu-id="ab422-135">**msdyn_PSSCreateV1**: šį API galima naudoti norint sukurti objektą.</span><span class="sxs-lookup"><span data-stu-id="ab422-135">**msdyn_PSSCreateV1**: This API can be used to create an entity.</span></span> <span data-ttu-id="ab422-136">Objektu gali būti bet kuris iš planavimo objektų, palaikančių kūrimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="ab422-136">The entity can be any of the Scheduling entities that support the create operation.</span></span>
- <span data-ttu-id="ab422-137">**msdyn_PSSUpdateV1**: šį API galima naudoti norint atnaujinti objektą.</span><span class="sxs-lookup"><span data-stu-id="ab422-137">**msdyn_PSSUpdateV1**: This API can be used to update an entity.</span></span> <span data-ttu-id="ab422-138">Objektu gali būti bet kuris iš planavimo objektų, palaikančių naujinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="ab422-138">The entity can be any of the Scheduling entities that support the update operation.</span></span>
- <span data-ttu-id="ab422-139">**msdyn_PSSDeleteV1**: šį API galima naudoti norint panaikinti objektą.</span><span class="sxs-lookup"><span data-stu-id="ab422-139">**msdyn_PSSDeleteV1**: This API can be used to delete an entity.</span></span> <span data-ttu-id="ab422-140">Objektu gali būti bet kuris iš planavimo objektų, palaikančių naikinimo operaciją.</span><span class="sxs-lookup"><span data-stu-id="ab422-140">The entity can be any of the Scheduling entities that support the delete operation.</span></span>
- <span data-ttu-id="ab422-141">**msdyn_ExecuteOperationSetV1**: šis API naudojamas norint vykdyti visas nurodyto operacijų rinkinio operacijas.</span><span class="sxs-lookup"><span data-stu-id="ab422-141">**msdyn_ExecuteOperationSetV1**: This API is used to execute all of the operations within the given operation set.</span></span>

## <a name="using-schedule-apis-with-operationset"></a><span data-ttu-id="ab422-142">Grafiko API naudojimas kartu su OperationSet</span><span class="sxs-lookup"><span data-stu-id="ab422-142">Using Schedule APIs with OperationSet</span></span>

<span data-ttu-id="ab422-143">Kadangi įrašai, naudojant **CreateProjectV1** ir **CreateTeamMemberV1**, sukuriami nedelsiant, šių API negalima naudoti tiesiai **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ab422-143">Because records with both **CreateProjectV1** and **CreateTeamMemberV1** are created immediately, these APIs can't be used in the **OperationSet** directly.</span></span> <span data-ttu-id="ab422-144">Tačiau API galite naudoti norėdami sukurti reikiamus įrašus, **OperationSet**, tada šiuos iš anksto sukurtus įrašus panaudoti **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ab422-144">However, you can use the API to create needed records, create an **OperationSet**, and then use these pre-created records in the **OperationSet**.</span></span>

## <a name="supported-operations"></a><span data-ttu-id="ab422-145">Palaikomos operacijos</span><span class="sxs-lookup"><span data-stu-id="ab422-145">Supported operations</span></span>

| <span data-ttu-id="ab422-146">Grafiko objektas</span><span class="sxs-lookup"><span data-stu-id="ab422-146">Scheduling entity</span></span> | <span data-ttu-id="ab422-147">Kūrimas</span><span class="sxs-lookup"><span data-stu-id="ab422-147">Create</span></span> | <span data-ttu-id="ab422-148">Atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="ab422-148">Update</span></span> | <span data-ttu-id="ab422-149">Delete</span><span class="sxs-lookup"><span data-stu-id="ab422-149">Delete</span></span> | <span data-ttu-id="ab422-150">Svarbi informacija</span><span class="sxs-lookup"><span data-stu-id="ab422-150">Important considerations</span></span> |
| --- | --- | --- | --- | --- |
<span data-ttu-id="ab422-151">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="ab422-151">Project task</span></span> | <span data-ttu-id="ab422-152">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-152">Yes</span></span> | <span data-ttu-id="ab422-153">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-153">Yes</span></span> | <span data-ttu-id="ab422-154">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-154">Yes</span></span> | <span data-ttu-id="ab422-155">Nėra</span><span class="sxs-lookup"><span data-stu-id="ab422-155">None</span></span> |
| <span data-ttu-id="ab422-156">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="ab422-156">Project task dependency</span></span> | <span data-ttu-id="ab422-157">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-157">Yes</span></span> | <span data-ttu-id="ab422-158">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-158">Yes</span></span> | | <span data-ttu-id="ab422-159">Projekto užduoties priklausomybės įrašai neatnaujinami.</span><span class="sxs-lookup"><span data-stu-id="ab422-159">Project task dependency records aren't updated.</span></span> <span data-ttu-id="ab422-160">Vietoj to, seną įrašą galima panaikinti ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="ab422-160">Instead, an old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ab422-161">Išteklių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="ab422-161">Resource assignment</span></span> | <span data-ttu-id="ab422-162">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-162">Yes</span></span> | <span data-ttu-id="ab422-163">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-163">Yes</span></span> | | <span data-ttu-id="ab422-164">Nepalaikomos operacijos, kurioms naudojami šie laukai: **BookableResourceID**, **Pastangos**, **EffortCompleted**, **EffortRemaining** ir **PlannedWork**.</span><span class="sxs-lookup"><span data-stu-id="ab422-164">Operations with the following fields aren't supported: **BookableResourceID**, **Effort**, **EffortCompleted**, **EffortRemaining**, and **PlannedWork**.</span></span> <span data-ttu-id="ab422-165">Išteklių priskyrimo įrašai neatnaujinami.</span><span class="sxs-lookup"><span data-stu-id="ab422-165">Resource assignment records aren't updated.</span></span> <span data-ttu-id="ab422-166">Vietoj to, seną įrašą galima panaikinti ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="ab422-166">Instead, the old record can be deleted and a new record can be created.</span></span> |
| <span data-ttu-id="ab422-167">Projekto talpykla</span><span class="sxs-lookup"><span data-stu-id="ab422-167">Project bucket</span></span> | <span data-ttu-id="ab422-168">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ab422-168">N/A</span></span> | <span data-ttu-id="ab422-169">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ab422-169">N/A</span></span> | <span data-ttu-id="ab422-170">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ab422-170">N/A</span></span> | <span data-ttu-id="ab422-171">Numatytoji talpykla sukuriama naudojant **CreateProjectV1** API.</span><span class="sxs-lookup"><span data-stu-id="ab422-171">The default bucket is created using the **CreateProjectV1** API.</span></span> |
| <span data-ttu-id="ab422-172">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="ab422-172">Project team member</span></span> | <span data-ttu-id="ab422-173">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-173">Yes</span></span> | <span data-ttu-id="ab422-174">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-174">Yes</span></span> | <span data-ttu-id="ab422-175">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-175">Yes</span></span> | <span data-ttu-id="ab422-176">Kūrimo operacijai naudokite **CreateTeamMemberV1** API.</span><span class="sxs-lookup"><span data-stu-id="ab422-176">For the create operation, use the **CreateTeamMemberV1** API.</span></span> |
| <span data-ttu-id="ab422-177">Project</span><span class="sxs-lookup"><span data-stu-id="ab422-177">Project</span></span> | <span data-ttu-id="ab422-178">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-178">Yes</span></span> | <span data-ttu-id="ab422-179">Taip</span><span class="sxs-lookup"><span data-stu-id="ab422-179">Yes</span></span> | <span data-ttu-id="ab422-180">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ab422-180">N/A</span></span> | <span data-ttu-id="ab422-181">Nepalaikomos operacijos, kurioms naudojami šie laukai: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Pastangos**, **EffortCompleted**, **EffortRemaining**, **Eiga**, **Pabaiga**, **TaskEarliestStart** ir **Duration**.</span><span class="sxs-lookup"><span data-stu-id="ab422-181">Operations with the following fields aren't supported: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Effort**, **EffortCompleted**, **EffortRemaining**, **Progress**, **Finish**, **TaskEarliestStart**, and **Duration**.</span></span> |

<span data-ttu-id="ab422-182">Šias API galima iškviesti naudojant objektus, kuriuose įtraukti pasirinktini laukai.</span><span class="sxs-lookup"><span data-stu-id="ab422-182">These APIs can be called with entity objects that include custom fields.</span></span>

<span data-ttu-id="ab422-183">ID ypatybė yra pasirinktinė.</span><span class="sxs-lookup"><span data-stu-id="ab422-183">The ID property is optional.</span></span> <span data-ttu-id="ab422-184">Jei ji pateikta, sistema bando ypatybę panaudoti ir, jei to padaryti negalima, pateikia išimtį.</span><span class="sxs-lookup"><span data-stu-id="ab422-184">If it's provided, the system attempts to use it and throws an exception if it can't be used.</span></span> <span data-ttu-id="ab422-185">Jei ypatybė nepateikta, sistema ją sugeneruos.</span><span class="sxs-lookup"><span data-stu-id="ab422-185">If it isn't provided, the system will generate it.</span></span>

## <a name="limitations-and-known-issues"></a><span data-ttu-id="ab422-186">Apribojimai ir žinomos problemos</span><span class="sxs-lookup"><span data-stu-id="ab422-186">Limitations and known issues</span></span>
<span data-ttu-id="ab422-187">Toliau pateikiamas apribojimų ir žinomų problemų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="ab422-187">The following is a list of limitations and known issues:</span></span>

- <span data-ttu-id="ab422-188">Grafiko API gali naudoti tik **vartotojai, turintys „Microsoft Project“ licenciją.**</span><span class="sxs-lookup"><span data-stu-id="ab422-188">Schedule APIs can only be used by **Users with Microsoft Project License.**</span></span> <span data-ttu-id="ab422-189">Jų negali toliau nurodyti vartotojai.</span><span class="sxs-lookup"><span data-stu-id="ab422-189">They can't be used by:</span></span>
    - <span data-ttu-id="ab422-190">Programų vartotojai</span><span class="sxs-lookup"><span data-stu-id="ab422-190">Application users</span></span>
    - <span data-ttu-id="ab422-191">Sistemos vartotojai</span><span class="sxs-lookup"><span data-stu-id="ab422-191">System users</span></span>
    - <span data-ttu-id="ab422-192">Integravimo vartotojai</span><span class="sxs-lookup"><span data-stu-id="ab422-192">Integration users</span></span>
    - <span data-ttu-id="ab422-193">Kiti vartotojai, neturintys reikiamos licencijos</span><span class="sxs-lookup"><span data-stu-id="ab422-193">Other users that don't have the required license</span></span>
- <span data-ttu-id="ab422-194">Kiekviename **OperationSet** gali būti ne daugiau kaip 100 operacijų.</span><span class="sxs-lookup"><span data-stu-id="ab422-194">Each **OperationSet** can only have a maximum of 100 operations.</span></span>
- <span data-ttu-id="ab422-195">Kiekvienas vartotojas gali turėti ne daugiau kaip 10 atvirų **OperationSet**.</span><span class="sxs-lookup"><span data-stu-id="ab422-195">Each user can only have a maximum of 10 open **OperationSets**.</span></span>
- <span data-ttu-id="ab422-196">„Project Operations“ šiuo metu palaikoma ne daugiau kaip 500 projekto užduočių iš viso.</span><span class="sxs-lookup"><span data-stu-id="ab422-196">Project Operations currently supports a maximum of 500 total tasks on a project.</span></span>
- <span data-ttu-id="ab422-197">**OperationSet** trikties būsena ir trikties žurnalai šiuo metu negalimi.</span><span class="sxs-lookup"><span data-stu-id="ab422-197">**OperationSet** failure status and failure logs aren't currently available.</span></span>
- <span data-ttu-id="ab422-198">Grafiko API yra viešosios priežiūros versijos.</span><span class="sxs-lookup"><span data-stu-id="ab422-198">Schedule APIs are in Public preview.</span></span> <span data-ttu-id="ab422-199">„Microsoft“ nepalaiko šių API naudojimo gamybos aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ab422-199">Using these APIs in a Production environment isn't supported by Microsoft.</span></span>

## <a name="sample-scenario"></a><span data-ttu-id="ab422-200">Scenarijaus pavyzdys</span><span class="sxs-lookup"><span data-stu-id="ab422-200">Sample scenario</span></span>

<span data-ttu-id="ab422-201">Pagal šį scenarijų sukursite projektą, komandos narį, keturias užduotis ir du išteklių priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="ab422-201">In this scenario, you will create a project, a team member, four tasks, and two resource assignments.</span></span> <span data-ttu-id="ab422-202">Tada atnaujinsite vieną užduotį, atnaujinsite projektą, panaikinsite vieną užduotį, panaikinsite vieną išteklių priskyrimą ir sukursite užduoties priklausomybę.</span><span class="sxs-lookup"><span data-stu-id="ab422-202">Next, you will update one task, update the project, delete one task, delete one resource assignment, and create a task dependency.</span></span>

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a><span data-ttu-id="ab422-203">Papildomi pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="ab422-203">Additional samples</span></span>

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
