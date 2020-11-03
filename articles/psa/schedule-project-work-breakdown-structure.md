---
title: Projekto planavimas su darbo paskirstymo struktūra
description: Projekto planavimas su darbo paskirstymo struktūra „Project Service“
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d77d9f8427f06015d4f4cb9438d7f59ac840b061
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081018"
---
# <a name="schedule-a-project-with-a-work-breakdown-structure-project-service"></a><span data-ttu-id="0a803-103">Projekto planavimas su darbo paskirstymo struktūra („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="0a803-103">Schedule a project with a work breakdown structure (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="0a803-104">Projekto grafikas nurodo, kokius darbus reikės atlikti, kurie ištekliai darbą atliks ir laiko ribas, per kurias darbą reikės atlikti.</span><span class="sxs-lookup"><span data-stu-id="0a803-104">A project schedule communicates what work needs to be performed, which resources will perform the work, and the timeframe in which that work needs to be completed.</span></span> <span data-ttu-id="0a803-105">Projekto grafikas atspindi visą darbą, susijusį su projekto atlikimu laiku.</span><span class="sxs-lookup"><span data-stu-id="0a803-105">The project schedule reflects all the work associated with delivering the project on time.</span></span> <span data-ttu-id="0a803-106">Vienas iš pirmųjų projekto inicijavimo etapo veiksmų yra projekto grafiko sudarymas.</span><span class="sxs-lookup"><span data-stu-id="0a803-106">One of the first steps in the initiation phase of the project is to come up with a project schedule.</span></span> <span data-ttu-id="0a803-107">Norint sudaryti projekto grafiką, reikia sukurti darbo paskirstymo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="0a803-107">To establish a project schedule, you need to create a work breakdown structure.</span></span>  
  
 <span data-ttu-id="0a803-108">Sukurkite projekto struktūrą su darbo paskirstymo struktūra, kuri jums padės:</span><span class="sxs-lookup"><span data-stu-id="0a803-108">Create a project structure with a work breakdown structure, which helps you:</span></span>  
  
- <span data-ttu-id="0a803-109">suskirstyti darbą į įvykdomas užduotis;</span><span class="sxs-lookup"><span data-stu-id="0a803-109">Break down work into manageable tasks</span></span>  
  
- <span data-ttu-id="0a803-110">įvertinti, kiek laiko reikės užduočiai atlikti;</span><span class="sxs-lookup"><span data-stu-id="0a803-110">Estimate the time required to complete a task</span></span>  
  
- <span data-ttu-id="0a803-111">nustatyti užduočių priklausomybes ir užduočių trukmę;</span><span class="sxs-lookup"><span data-stu-id="0a803-111">Set task dependencies and task duration</span></span>  
  
- <span data-ttu-id="0a803-112">apibrėžti kiekvienai užduočiai atlikti reikalingus vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="0a803-112">Determine the roles required to complete each task</span></span>  
  
  <span data-ttu-id="0a803-113">Projekto grafikas darbo paskirstymo struktūroje yra panašus į projekto grafiką interaktyviojoje Ganto diagramoje.</span><span class="sxs-lookup"><span data-stu-id="0a803-113">The project schedule in the work breakdown structure has a familiar look and feel, complete with an interactive Gantt chart.</span></span>  
  
## <a name="create-a-work-breakdown-structure-for-a-project"></a><span data-ttu-id="0a803-114">Projekto darbo paskirstymo struktūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="0a803-114">Create a work breakdown structure for a project</span></span>  
 <span data-ttu-id="0a803-115">Sukurkite darbo paskirstymo struktūrą, vaizduojančią projekto užduočių seką.</span><span class="sxs-lookup"><span data-stu-id="0a803-115">Create a work breakdown structure to represent the sequence of tasks in a project.</span></span> <span data-ttu-id="0a803-116">Darbo paskirstymo struktūra apima užduotis, kiekvienos užduoties reikalavimus ir įplaukų bei savikainos informaciją.</span><span class="sxs-lookup"><span data-stu-id="0a803-116">The work breakdown structure includes tasks, requirements for each task, and revenue and cost information.</span></span> <span data-ttu-id="0a803-117">Į darbo paskirstymo struktūrą galite įtraukti:</span><span class="sxs-lookup"><span data-stu-id="0a803-117">In your work breakdown structure, you can add:</span></span>  
  
-   <span data-ttu-id="0a803-118">užduočių seką pagal hierarchiją;</span><span class="sxs-lookup"><span data-stu-id="0a803-118">The sequence of tasks in a hierarchy</span></span>  
  
-   <span data-ttu-id="0a803-119">kitas užduotis, jei jų yra, kurias būtina atlikti, kad būtų galima pradėti vykdyti užduotį;</span><span class="sxs-lookup"><span data-stu-id="0a803-119">Other tasks, if any, that must be completed before a task can be started</span></span>  
  
-   <span data-ttu-id="0a803-120">užduoties pradžios datą, pabaigos datą ir trukmę;</span><span class="sxs-lookup"><span data-stu-id="0a803-120">The starting date, ending date, and duration of a task</span></span>  
  
-   <span data-ttu-id="0a803-121">užduočiai atlikti reikalingų valandų skaičių;</span><span class="sxs-lookup"><span data-stu-id="0a803-121">The number of hours required for a task</span></span>  
  
-   <span data-ttu-id="0a803-122">visus reikalingus darbuotojų įgūdžius ir išsilavinimą;</span><span class="sxs-lookup"><span data-stu-id="0a803-122">Any required worker skills and education</span></span>  
  
-   <span data-ttu-id="0a803-123">užduočiai priskirtus darbuotojus;</span><span class="sxs-lookup"><span data-stu-id="0a803-123">The workers who are assigned to a task</span></span>  
  
-   <span data-ttu-id="0a803-124">prognozuojamas įplaukas ir savikainą.</span><span class="sxs-lookup"><span data-stu-id="0a803-124">Estimated revenue and costs</span></span>  
  
## <a name="task-types"></a><span data-ttu-id="0a803-125">Užduočių tipai</span><span class="sxs-lookup"><span data-stu-id="0a803-125">Task types</span></span>  
<span data-ttu-id="0a803-126">Kuriant darbo paskirstymo struktūrą, naudojamos šių tipų užduotys:</span><span class="sxs-lookup"><span data-stu-id="0a803-126">You’ll use the following types of tasks when creating your work breakdown structure:</span></span>  

| | | 
|---------------------------------------|-----------------------------------------------------------------| 
| <span data-ttu-id="0a803-127">**Projekto šakninis mazgas**</span><span class="sxs-lookup"><span data-stu-id="0a803-127">**Project root node**</span></span> | <span data-ttu-id="0a803-128">Tai projekto aukščiausio lygio suvestinė užduotis.</span><span class="sxs-lookup"><span data-stu-id="0a803-128">The top-level summary task for the project.</span></span> <span data-ttu-id="0a803-129">Joje yra kuriamos visos kitos projekto užduotys.</span><span class="sxs-lookup"><span data-stu-id="0a803-129">All other project tasks are created under it.</span></span> <span data-ttu-id="0a803-130">Šakninei užduočiai suteikiamas projekto pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="0a803-130">The name of the root task is the project name.</span></span> <span data-ttu-id="0a803-131">Šakninio mazgo pastangos, datos ir trukmė yra pagrįstos žemiau jos esančios hierarchijos reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="0a803-131">The effort, dates, and duration of the root node are based on the values on the hierarchy below it.</span></span> <span data-ttu-id="0a803-132">Negalite nei redaguoti šakninio mazgo ypatybių, nei panaikinti paties šakninio mazgo.</span><span class="sxs-lookup"><span data-stu-id="0a803-132">You can’t edit root node properties or delete the root node.</span></span> | 
| <span data-ttu-id="0a803-133">**Suvestinės arba konteinerio užduotys**</span><span class="sxs-lookup"><span data-stu-id="0a803-133">**Summary or container tasks**</span></span> | <span data-ttu-id="0a803-134">Suvestinė užduotis yra užduotis, turinti papildomų užduočių.</span><span class="sxs-lookup"><span data-stu-id="0a803-134">A summary task is a task that has sub-tasks under it.</span></span> <span data-ttu-id="0a803-135">Pati suvestinė užduotis neturi jokių darbo pastangų nei savikainos.</span><span class="sxs-lookup"><span data-stu-id="0a803-135">A summary task doesn’t have any work effort or cost of its own.</span></span> <span data-ttu-id="0a803-136">Jos darbo pastangos ir savikaina yra jos papildomų užduočių apibendrinamoji reikšmė.</span><span class="sxs-lookup"><span data-stu-id="0a803-136">Its work effort and cost are a rollup of its sub-tasks.</span></span> <span data-ttu-id="0a803-137">Galite keisti suvestinės užduoties pavadinimą, bet negalite keisti pastangų, datų ar trukmės, nes jos apskaičiuojamos automatiškai.</span><span class="sxs-lookup"><span data-stu-id="0a803-137">You can change the name of a summary task, but you can’t change the effort, dates, or duration, because those are automatically calculated.</span></span> <span data-ttu-id="0a803-138">Panaikinus suvestinę užduotį, panaikinama pati užduotis ir visos jos papildomos užduotys.</span><span class="sxs-lookup"><span data-stu-id="0a803-138">Deleting a summary task deletes the task and all of its sub-tasks.</span></span>|  
| <span data-ttu-id="0a803-139">**Lapo mazgo užduotys**</span><span class="sxs-lookup"><span data-stu-id="0a803-139">**Leaf node tasks**</span></span> | <span data-ttu-id="0a803-140">Lapo mazgo užduotis vaizduoja patį smulkiausią projekto darbą.</span><span class="sxs-lookup"><span data-stu-id="0a803-140">A leaf node task represents the most detailed work on the project.</span></span> <span data-ttu-id="0a803-141">Ji rodo prognozuojamas pastangas, planuojamą išteklių skaičių, planuojamas pradžios bei pabaigos datas ir trukmę.</span><span class="sxs-lookup"><span data-stu-id="0a803-141">It has an estimated effort, a planned number of resources, planned start and end dates, and a duration.</span></span>|

  
## <a name="task-hierarchy"></a><span data-ttu-id="0a803-142">Užduoties hierarchija</span><span class="sxs-lookup"><span data-stu-id="0a803-142">Task hierarchy</span></span>  
 <span data-ttu-id="0a803-143">Kuriant užduoties hierarchiją, naudojamos šios parinktys:</span><span class="sxs-lookup"><span data-stu-id="0a803-143">You have the following options when creating a task hierarchy:</span></span>  
  
- <span data-ttu-id="0a803-144">**Įtraukti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="0a803-144">**Add task**.</span></span>   <span data-ttu-id="0a803-145">Užduotį galite įtraukti pasirinktoje užduoties hierarchijos vietoje.</span><span class="sxs-lookup"><span data-stu-id="0a803-145">You can add a task at a position you choose in the task hierarchy.</span></span> <span data-ttu-id="0a803-146">Jei vietos nepasirinksite, nauja užduotis bus įtraukta į pabaigą.</span><span class="sxs-lookup"><span data-stu-id="0a803-146">If you don’t select a position, your new task appears at the end.</span></span>  
  
- <span data-ttu-id="0a803-147">**Užduoties įtrauka**.</span><span class="sxs-lookup"><span data-stu-id="0a803-147">**Indent task**.</span></span>   <span data-ttu-id="0a803-148">Pritaikius užduoties įtrauką, užduotis tampa antrine užduotimi tos užduoties, kuri yra virš jos.</span><span class="sxs-lookup"><span data-stu-id="0a803-148">Indent a task to make it a child of the task directly above it.</span></span>  
  
- <span data-ttu-id="0a803-149">**Atvirkštinė užduoties įtrauka**.</span><span class="sxs-lookup"><span data-stu-id="0a803-149">**Outdent task**.</span></span>   <span data-ttu-id="0a803-150">Pasirinkite atvirkštinę įtrauką, jei nebenorite, kad ši užduotis būtų papildoma pirminės užduoties užduotimi.</span><span class="sxs-lookup"><span data-stu-id="0a803-150">Outdent a task to make it so it’s no longer a sub-task of its original parent task.</span></span>  
  
- <span data-ttu-id="0a803-151">**Perkelti aukštyn arba perkelti žemyn**.</span><span class="sxs-lookup"><span data-stu-id="0a803-151">**Move up and Move down**.</span></span>   <span data-ttu-id="0a803-152">Pirminių užduočių hierarchijoje perkelkite užduotis aukštyn arba žemyn.</span><span class="sxs-lookup"><span data-stu-id="0a803-152">Move tasks up and down in the hierarchy of its parent task.</span></span> <span data-ttu-id="0a803-153">Užduoties perkėlimas aukštyn arba žemyn niekaip nepaveikia jos pastangų, savikainos, datų ar trukmės.</span><span class="sxs-lookup"><span data-stu-id="0a803-153">Moving a task up or down has no effect on its effort, cost, dates, or duration.</span></span>  
  
## <a name="task-attributes"></a><span data-ttu-id="0a803-154">Užduoties atributai</span><span class="sxs-lookup"><span data-stu-id="0a803-154">Task attributes</span></span>  
 <span data-ttu-id="0a803-155">Užduoties pavadinimas aprašo darbą, kurį reikia atlikti.</span><span class="sxs-lookup"><span data-stu-id="0a803-155">A task’s name describes the work that needs to be completed.</span></span> <span data-ttu-id="0a803-156">Įvairūs užduoties atributai naudojami aprašant užduoties grafiką ir reikalingų darbuotojų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="0a803-156">You use various task attributes to describe the schedule and staffing requirements for the task.</span></span>  
  
### <a name="schedule-attributes"></a><span data-ttu-id="0a803-157">Grafiko atributai</span><span class="sxs-lookup"><span data-stu-id="0a803-157">Schedule attributes</span></span>

 - <span data-ttu-id="0a803-158">Priskiriant reikšmes laukuose **Pastangų valandos** , **Išteklių skaičius** , **Pradžios data** , **Pabaigos data** ir **Trukmė** , apibrėžiamas užduoties grafikas.</span><span class="sxs-lookup"><span data-stu-id="0a803-158">Assign values to **Effort hours** , **Number of resources** , **Start date** , **End date** , and **Duration** to determine the schedule for the task.</span></span> 
 - <span data-ttu-id="0a803-159">**Pastangos** yra prognozuojamas valandų skaičius, reikalingas užduočiai atlikti.</span><span class="sxs-lookup"><span data-stu-id="0a803-159">**Effort** is an estimate of the hours it takes to complete the task.</span></span>
 - <span data-ttu-id="0a803-160">**Išteklių skaičius** yra prognozuojami ištekliai, projekto vadovo skiriami užduočiai, siekiant sudaryti geriausią galimą grafiką.</span><span class="sxs-lookup"><span data-stu-id="0a803-160">**Number of resources** is an estimate that the project manager puts in the task to help come up with the best possible schedule.</span></span> 
 - <span data-ttu-id="0a803-161">**Trukmė** (dienomis) rodo užduočiai atlikti reikalingų darbo dienų skaičių.</span><span class="sxs-lookup"><span data-stu-id="0a803-161">**Duration** (in days) indicates the number of work days it will take to complete the task.</span></span>  
  
### <a name="staffing-attributes"></a><span data-ttu-id="0a803-162">Darbuotojų atributai</span><span class="sxs-lookup"><span data-stu-id="0a803-162">Staffing attributes</span></span>

 - <span data-ttu-id="0a803-163">**Vaidmuo** , **Išteklių organizacinis vienetas** , **Išteklių skaičius** ir **Ištekliai** aprašo užduoties darbuotojų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="0a803-163">**Role** , **Resource organizational unit** , **Number of resources** , and **Resources** describe the staffing requirements for the task.</span></span> 
 - <span data-ttu-id="0a803-164">**Vaidmuo** aprašo užduočiai atlikti reikalingų išteklių tipą.</span><span class="sxs-lookup"><span data-stu-id="0a803-164">**Role** describes the type of resource needed to perform the task.</span></span> 
 - <span data-ttu-id="0a803-165">**Išteklių organizacinis vienetas** nurodo organizacinį vienetą, iš kurio šiai užduočiai turi būti skiriami ištekliai; šis atributas paveikia užduoties savikainą ir pardavimo sąmatą, kadangi į jį atsižvelgiama nustatant ištekliaus vieneto pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="0a803-165">**Resource organizational unit** indicates the organizational unit from which resources should be staffed for that task; this also impacts the cost and sales estimate of the task, since this is accounted for when determining the unit sales price for the resource.</span></span> 
 - <span data-ttu-id="0a803-166">**Ištekliai** – tai bendrojo ištekliaus pavadinimas arba įvardyto ištekliaus, kai toks surandamas, pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="0a803-166">**Resources** holds a generic resource or a named resource when one is found.</span></span>  
  
## <a name="task-dependencies"></a><span data-ttu-id="0a803-167">Užduoties priklausomybės</span><span class="sxs-lookup"><span data-stu-id="0a803-167">Task dependencies</span></span>  
 <span data-ttu-id="0a803-168">Darbo paskirstymo struktūroje galima sukurti ankstesnės užduoties ryšius su viena ar daugiau užduočių.</span><span class="sxs-lookup"><span data-stu-id="0a803-168">You can create predecessor relationships between one or more tasks in the work breakdown structure.</span></span> <span data-ttu-id="0a803-169">Užduotyse galima nustatyti vieną ar daugiau ankstesnės užduoties lauko reikšmių, nurodančių nuo jų priklausančias užduotis.</span><span class="sxs-lookup"><span data-stu-id="0a803-169">You can set one or more values for the predecessor field on tasks to indicate the tasks that it will be dependent on.</span></span> <span data-ttu-id="0a803-170">Užduočiai priskyrus ankstesnės užduoties reikšmę, užduotį pradėti galima tik atlikus visas ankstesnės užduoties užduotis.</span><span class="sxs-lookup"><span data-stu-id="0a803-170">When you assign a predecessor value to a task, the task can only start when all the predecessor tasks have completed.</span></span> <span data-ttu-id="0a803-171">Nustačius užduočiai šią priklausomybę, planuojama užduoties pradžios data bus perskaičiuota į vėliausią visų jos ankstesnių užduočių atlikimo pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="0a803-171">Setting this dependency on a task will result in the recalculation of the planned start date of the task as the latest end of all of its predecessors.</span></span> <span data-ttu-id="0a803-172">Ankstesnių užduočių poveikis grafikui neapsiriboja užduočiai apibrėžtu užduoties režimu.</span><span class="sxs-lookup"><span data-stu-id="0a803-172">Predecessor-related impacts on a schedule are not limited by the task mode defined on the task.</span></span>  
  
## <a name="task-mode"></a><span data-ttu-id="0a803-173">Užduoties režimas</span><span class="sxs-lookup"><span data-stu-id="0a803-173">Task mode</span></span>  
 <span data-ttu-id="0a803-174">Užduoties režimas yra vienas iš svarbių veiksnių, lemiančių lapo mazgo užduočių planavimą.</span><span class="sxs-lookup"><span data-stu-id="0a803-174">Task mode is one of the important factors that determine scheduling leaf node tasks.</span></span> <span data-ttu-id="0a803-175">Yra du galimi kiekvienos užduoties režimai: automatinio planavimo režimas ir rankinio planavimo režimas.</span><span class="sxs-lookup"><span data-stu-id="0a803-175">There are two task modes for every task: auto scheduling mode and manual scheduling mode.</span></span>  
  
-   <span data-ttu-id="0a803-176">**Automatinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="0a803-176">**Auto scheduling**.</span></span>   <span data-ttu-id="0a803-177">nustačius automatinio planavimo užduoties režimą, užduoties planavimo modulis, nustatydamas užduoties grafiką, planavimo taisykles taiko šiems užduoties atributams.</span><span class="sxs-lookup"><span data-stu-id="0a803-177">When you set the task mode to Automatically Scheduled, the task scheduling engine uses the scheduling rules on the following task attributes to determine the schedule for the task:</span></span>  
  
    -   <span data-ttu-id="0a803-178">Ankstesnės užduotys</span><span class="sxs-lookup"><span data-stu-id="0a803-178">Predecessors</span></span>  
  
    -   <span data-ttu-id="0a803-179">Pastangos</span><span class="sxs-lookup"><span data-stu-id="0a803-179">Effort</span></span>  
  
    -   <span data-ttu-id="0a803-180">Išteklių skaičius</span><span class="sxs-lookup"><span data-stu-id="0a803-180">Number of resources</span></span>  
  
    -   <span data-ttu-id="0a803-181">pradžios ir pabaigos datos;</span><span class="sxs-lookup"><span data-stu-id="0a803-181">Start and end dates</span></span>  
  
-   <span data-ttu-id="0a803-182">**Planavimo taisyklės**.</span><span class="sxs-lookup"><span data-stu-id="0a803-182">**Scheduling rules**.</span></span>   <span data-ttu-id="0a803-183">Lapo mazgo užduoties, neturinčios ankstesnių užduočių, pradžios data pagal numatytąją reikšmę yra projekto grafiko pradžios data.</span><span class="sxs-lookup"><span data-stu-id="0a803-183">The start date of a leaf node task that does not have predecessors defaults to the project’s scheduling start date.</span></span> <span data-ttu-id="0a803-184">Lapo mazgo užduoties trukmė visada apskaičiuojama kaip darbo dienų skaičius nuo jos pradžios datos iki pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="0a803-184">The duration of a leaf node task is always calculated as the number of working days between its start and end dates.</span></span> <span data-ttu-id="0a803-185">Planuojant užduotį automatiškai, planavimo modulis taiko šias taisykles:</span><span class="sxs-lookup"><span data-stu-id="0a803-185">When a task is automatically scheduled, the scheduling engine follows the rules below:</span></span>  
  
    -   <span data-ttu-id="0a803-186">užduoties pradžios ir pabaigos datos, suplanuotos projekto planavimo kalendoriuje, visada turi būti darbo dienos;</span><span class="sxs-lookup"><span data-stu-id="0a803-186">Start and end dates of a task must always be working days according to the project’s scheduling calendar</span></span>  
  
    -   <span data-ttu-id="0a803-187">užduoties, kuri turi ankstesnių užduočių, pradžios data pagal numatytąją reikšmę yra vėliausia jos ankstesnių užduočių atlikimo pabaigos data;</span><span class="sxs-lookup"><span data-stu-id="0a803-187">The start date of a task that has predecessors defaults to the latest end date of its predecessors</span></span>  
  
    -   <span data-ttu-id="0a803-188">pastangos = darbuotojų skaičius \* trukmė \* valandomis per įprastą darbo dieną projekto kalendoriuje.</span><span class="sxs-lookup"><span data-stu-id="0a803-188">Effort = Number of people \* Duration \* hours in a standard work day of the project calendar</span></span>  
  
-   <span data-ttu-id="0a803-189">**Neautomatinis planavimas**.</span><span class="sxs-lookup"><span data-stu-id="0a803-189">**Manual scheduling**.</span></span>   <span data-ttu-id="0a803-190">Kai kuriais atvejais galite norėti nukrypti nuo šių taisyklių.</span><span class="sxs-lookup"><span data-stu-id="0a803-190">In some cases, you might want to deviate from these rules.</span></span> <span data-ttu-id="0a803-191">Tokiais atvejais galite nustatyti, kad užduoties režimas užduočiai būtų planuojamas rankomis.</span><span class="sxs-lookup"><span data-stu-id="0a803-191">In these cases, you can set the task mode for the task to be manually scheduled.</span></span> <span data-ttu-id="0a803-192">Taip planavimo modulis sustabdomas ir nebeskaičiuoja kitų planavimo atributų reikšmių.</span><span class="sxs-lookup"><span data-stu-id="0a803-192">This stops the scheduling engine from calculating the values for other scheduling attributes.</span></span> <span data-ttu-id="0a803-193">Užduotyse nustačius ankstesnes užduotis, tai visada paveikia priklausančios užduoties pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="0a803-193">Setting predecessors on tasks always impacts the dependent task’s start date.</span></span>  
  
## <a name="create-a-work-breakdown-structure"></a><span data-ttu-id="0a803-194">Darbo paskirstymo struktūros kūrimas</span><span class="sxs-lookup"><span data-stu-id="0a803-194">Create a work breakdown structure</span></span>  
  
1.  <span data-ttu-id="0a803-195">Pasirinkite **Project Service > Projektai**.</span><span class="sxs-lookup"><span data-stu-id="0a803-195">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="0a803-196">Spustelėkite projektą, su kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="0a803-196">Click the project you want to work on.</span></span>  
  
3.  <span data-ttu-id="0a803-197">Juostoje ekrano viršuje pasirinkite žemyn nukreiptą rodyklę prie projekto pavadinimo, o tada spustelėkite Darbo paskirstymo struktūra.</span><span class="sxs-lookup"><span data-stu-id="0a803-197">In the bar across the top of the screen, select the down arrow next to the project name, and then click Work breakdown structure.</span></span>  
  
4.  <span data-ttu-id="0a803-198">Jei norite pridėti užduotį, spustelėkite **Įtraukti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="0a803-198">To add a task, click **Add Task**.</span></span> <span data-ttu-id="0a803-199">Užpildykite užduoties laukus, o tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="0a803-199">Fill in the fields for the task, and then click **Save**.</span></span>  
  
5.  <span data-ttu-id="0a803-200">Tęskite įtraukdami užduotis, kol užbaigsite darbo paskirstymo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="0a803-200">Continue adding tasks until your work breakdown structure is complete.</span></span> <span data-ttu-id="0a803-201">Kurdami darbo paskirstymo struktūrą, tvarkyti užduotis galite atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="0a803-201">While creating your work breakdown structure, you can do the following to organize your tasks:</span></span>  
  
    -   <span data-ttu-id="0a803-202">pasirinkite užduotį ir spustelėkite **Įtrauka** , jei užduotį norite perkelti žemiau kitos užduoties,„Atvirkštinė įtrauka, jei užduotį norite pakelti vienu lygiu;</span><span class="sxs-lookup"><span data-stu-id="0a803-202">Select a task and click **Indent** to move it under another task or click Outdent to move it out a level.</span></span>  
  
    -   <span data-ttu-id="0a803-203">pasirinkite užduotį ir spustelėkite **Perkelti aukštyn** arba **Perkelti žemyn** ; jei užduotį norite perkelti sąraše aukštyn arba žemyn;</span><span class="sxs-lookup"><span data-stu-id="0a803-203">Select a task and click **Move Up** or **Move Down** to move it up or down in the list.</span></span>  
  
    -   <span data-ttu-id="0a803-204">spustelėkite **Slėpti Ganto diagramą** , jei Ganto diagramą norite paslėpti, arba spustelėkite **Rodyti Ganto diagramą** , jei norite, kad Ganto diagrama vėl būtų rodoma;</span><span class="sxs-lookup"><span data-stu-id="0a803-204">Click **Hide Gantt** to hide the Gantt chart, and click **Show Gantt** to display it again.</span></span>  
  
    -   <span data-ttu-id="0a803-205">lauke **Laiko skalė** pasirinkite kitą Ganto diagramos laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="0a803-205">Select a different period of time for the Gantt chart in **Time Scale**.</span></span>  
  
6.  <span data-ttu-id="0a803-206">Norėdami projekto komandos nariams pridėti vaidmenis, kuriuos nurodėte darbo paskirstymo struktūroje, spustelėkite **Kurti projekto komandą**.</span><span class="sxs-lookup"><span data-stu-id="0a803-206">To add the roles you specified in your work breakdown structure to your project’s team members, click **Generate Project Team**.</span></span>  
  
7.  <span data-ttu-id="0a803-207">Atlikę pakeitimus, spustelėkite mygtuką **Įrašyti** , esantį ekrano apatiniame dešiniame kampe.</span><span class="sxs-lookup"><span data-stu-id="0a803-207">Click **Save** at the bottom right corner of the screen when you’re done making changes.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="0a803-208">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="0a803-208">See Also</span></span>  
 [<span data-ttu-id="0a803-209">Projekto vadovo vadovas</span><span class="sxs-lookup"><span data-stu-id="0a803-209">Project manager guide</span></span>](../psa/project-manager-guide.md)
