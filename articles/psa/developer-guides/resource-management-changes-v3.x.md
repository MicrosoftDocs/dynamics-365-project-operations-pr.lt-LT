---
title: Išteklių valdymo pakeitimai (Project Service Automation 3.x)
description: Šioje temoje pateikiama informacija apie pakeitimus išteklių valdymo srityje.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148653"
---
# <a name="resource-management-changes-project-service-automation-3x"></a><span data-ttu-id="0fee8-103">Išteklių valdymo pakeitimai (Project Service Automation 3.x)</span><span class="sxs-lookup"><span data-stu-id="0fee8-103">Resource management changes (Project Service Automation 3.x)</span></span>

[!include [banner](../../includes/psa-now-project-operations.md)]

<span data-ttu-id="0fee8-104">Šios temos skyriuose pateikiama informacija apie pakeitimus, kurie atlikti Dynamics 365 Project Service Automation 3.x versijos išteklių valdymo srityje.</span><span class="sxs-lookup"><span data-stu-id="0fee8-104">The sections of this topic provide information about the changes that have been made to the Resource management area of Dynamics 365 Project Service Automation version 3.x.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="0fee8-105">Projekto įvertinimai</span><span class="sxs-lookup"><span data-stu-id="0fee8-105">Project estimates</span></span>

<span data-ttu-id="0fee8-106">Projekto įvertinimai pagrįsti ne objektu **msdyn\_projecttask** (**Projekto užduotis**), o objektu **msdyn\_resourceassignment** (**Išteklių priskyrimas**).</span><span class="sxs-lookup"><span data-stu-id="0fee8-106">Instead of being based on the **msdyn\_projecttask** entity (**Project Task**), project estimates are based on the **msdyn\_resourceassignment** entity (**Resource Assignment**).</span></span> <span data-ttu-id="0fee8-107">Išteklių priskyrimai užduočių planavimui ir įkainiams tapo „tiesos šaltiniu“.</span><span class="sxs-lookup"><span data-stu-id="0fee8-107">Resource assignments have become the "source of truth" for task scheduling and pricing.</span></span>

## <a name="line-tasks"></a><span data-ttu-id="0fee8-108">Eilutės užduotys</span><span class="sxs-lookup"><span data-stu-id="0fee8-108">Line tasks</span></span>

<span data-ttu-id="0fee8-109">PSA 3.x versijoje eilutės užduotys yra pasenusios (nebenaudojamos).</span><span class="sxs-lookup"><span data-stu-id="0fee8-109">In PSA 3.x, line tasks are obsolete (deprecated).</span></span> <span data-ttu-id="0fee8-110">Dabar priskyrimai nurodo visą užduotį, o ne eilutės užduotis.</span><span class="sxs-lookup"><span data-stu-id="0fee8-110">Assignments now point to the whole task instead of the line tasks.</span></span>

<span data-ttu-id="0fee8-111">Toliau pateiktame pavyzdyje parodoma, kaip užduotis, pavadinimu „Bandomoji užduotis“, priskiriama komandos nariams A ir B ankstesnė PSA versijose ir PSA 3.x versijoje.</span><span class="sxs-lookup"><span data-stu-id="0fee8-111">The following example shows how a task that is named "Test task" is assigned to team members A and B in earlier versions of PSA and in PSA 3.x.</span></span>

- <span data-ttu-id="0fee8-112">**Prieš PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="0fee8-112">**Before PSA 3.x:**</span></span>

    - <span data-ttu-id="0fee8-113">Bandomoji užduotis</span><span class="sxs-lookup"><span data-stu-id="0fee8-113">Test task</span></span>

        - <span data-ttu-id="0fee8-114">Bandomoji užduotis – 1 eilutės užduotis</span><span class="sxs-lookup"><span data-stu-id="0fee8-114">Test task – Line task 1</span></span>

            - <span data-ttu-id="0fee8-115">Priskyrimas A</span><span class="sxs-lookup"><span data-stu-id="0fee8-115">Assignment to A</span></span>

        - <span data-ttu-id="0fee8-116">Bandomoji užduotis – 2 eilutės užduotis</span><span class="sxs-lookup"><span data-stu-id="0fee8-116">Test task – Line task 2</span></span>

            - <span data-ttu-id="0fee8-117">Priskyrimas B</span><span class="sxs-lookup"><span data-stu-id="0fee8-117">Assignment to B</span></span>

- <span data-ttu-id="0fee8-118">**PSA 3.x:**</span><span class="sxs-lookup"><span data-stu-id="0fee8-118">**PSA 3.x:**</span></span>

    - <span data-ttu-id="0fee8-119">Bandomoji užduotis</span><span class="sxs-lookup"><span data-stu-id="0fee8-119">Test task</span></span>

        - <span data-ttu-id="0fee8-120">Priskyrimas A</span><span class="sxs-lookup"><span data-stu-id="0fee8-120">Assignment to A</span></span>
        - <span data-ttu-id="0fee8-121">Priskyrimas B</span><span class="sxs-lookup"><span data-stu-id="0fee8-121">Assignment to B</span></span>

## <a name="unassigned-assignment"></a><span data-ttu-id="0fee8-122">Nepriskirti priskyrimai</span><span class="sxs-lookup"><span data-stu-id="0fee8-122">Unassigned assignment</span></span>

<span data-ttu-id="0fee8-123">PSA 3.x nepriskirtas priskyrimas yra priskyrimas, kuris priskirtas **NULL** komandos nariui ir **NULL** ištekliams.</span><span class="sxs-lookup"><span data-stu-id="0fee8-123">In PSA 3.x, an unassigned assignment is an assignment that is assigned to a **NULL** team member and a **NULL** resource.</span></span> <span data-ttu-id="0fee8-124">Nepriskirti priskyrimai įvyksta keliais atvejais:</span><span class="sxs-lookup"><span data-stu-id="0fee8-124">Unassigned assignments can occur in a couple of scenarios:</span></span>

- <span data-ttu-id="0fee8-125">Jei užduotis sukurta, tačiau dar nepriskirta jokiam komandos nariui, visada sukuriamas nepriskirtas priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="0fee8-125">If a task has been created, but it hasn't yet been assigned to any team member, an unassigned assignment is always created.</span></span> 
- <span data-ttu-id="0fee8-126">Jei visi užduočiai priskirtieji asmenys yra pašalinami, šiai užduočiai iš naujo sukuriamas nepriskirtas priskyrimas.</span><span class="sxs-lookup"><span data-stu-id="0fee8-126">If all assignees on a task are removed, an unassigned assignment is re-created for that task.</span></span>

## <a name="scheduling-fields-on-the-project-task-entity"></a><span data-ttu-id="0fee8-127">Projekto užduoties objekto planavimo laukai</span><span class="sxs-lookup"><span data-stu-id="0fee8-127">Scheduling fields on the Project Task entity</span></span>

<span data-ttu-id="0fee8-128">Laukai objekte **msdyn\_projecttask** nebenaudojami arba perkelti į objektą **msdyn\_resourceassignment**, arba dabar jie yra nurodomi iš objekto **msdyn\_projectteam** (**Projekto komandos narys**).</span><span class="sxs-lookup"><span data-stu-id="0fee8-128">The fields on the **msdyn\_projecttask** entity have been deprecated or moved to the **msdyn\_resourceassignment** entity, or they are now referenced from the **msdyn\_projectteam** entity (**Project Team Member**).</span></span>

| <span data-ttu-id="0fee8-129">Nebenaudojamas laukas, esantis msdyn\_projecttask (Projekto užduotis)</span><span class="sxs-lookup"><span data-stu-id="0fee8-129">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="0fee8-130">Naujas laukas, esantis msdyn\_resourceassignment (Išteklių priskyrimas)</span><span class="sxs-lookup"><span data-stu-id="0fee8-130">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> | <span data-ttu-id="0fee8-131">Komentaras</span><span class="sxs-lookup"><span data-stu-id="0fee8-131">Comment</span></span> |
|---|---|---|
| <span data-ttu-id="0fee8-132">msdyn\_assignedresources</span><span class="sxs-lookup"><span data-stu-id="0fee8-132">msdyn\_assignedresources</span></span> | <span data-ttu-id="0fee8-133">Joks</span><span class="sxs-lookup"><span data-stu-id="0fee8-133">None</span></span> | |
| <span data-ttu-id="0fee8-134">msdyn\_assignedteammembers</span><span class="sxs-lookup"><span data-stu-id="0fee8-134">msdyn\_assignedteammembers</span></span> | <span data-ttu-id="0fee8-135">Joks</span><span class="sxs-lookup"><span data-stu-id="0fee8-135">None</span></span> | |
| <span data-ttu-id="0fee8-136">msdyn\_numberofresources</span><span class="sxs-lookup"><span data-stu-id="0fee8-136">msdyn\_numberofresources</span></span> | <span data-ttu-id="0fee8-137">Joks</span><span class="sxs-lookup"><span data-stu-id="0fee8-137">None</span></span> | |
| <span data-ttu-id="0fee8-138">msdyn\_scheduledhours</span><span class="sxs-lookup"><span data-stu-id="0fee8-138">msdyn\_scheduledhours</span></span> | <span data-ttu-id="0fee8-139">Joks</span><span class="sxs-lookup"><span data-stu-id="0fee8-139">None</span></span> | |
| <span data-ttu-id="0fee8-140">msdyn\_effortcontour</span><span class="sxs-lookup"><span data-stu-id="0fee8-140">msdyn\_effortcontour</span></span> | <span data-ttu-id="0fee8-141">msdyn\_plannedwork</span><span class="sxs-lookup"><span data-stu-id="0fee8-141">msdyn\_plannedwork</span></span> | <span data-ttu-id="0fee8-142">„JavaScript Object Notation“ (JSON) duomenų struktūros saugomos lauke, formatas pakeistas.</span><span class="sxs-lookup"><span data-stu-id="0fee8-142">The format of the JavaScript Object Notation (JSON) data structure that is stored in the field has been changed.</span></span> |

## <a name="schedule-contour"></a><span data-ttu-id="0fee8-143">Grafiko kontūras</span><span class="sxs-lookup"><span data-stu-id="0fee8-143">Schedule contour</span></span>

<span data-ttu-id="0fee8-144">Grafiko kontūras saugomas kiekvieno objekto **Išteklių priskyrimas** (**msdyn\_resourceassignment**) lauke **Suplanuotas darbas** (**msdyn\_plannedwork**).</span><span class="sxs-lookup"><span data-stu-id="0fee8-144">The schedule contour is stored in the **Planned Work** field (**msdyn\_plannedwork**) of each **Resource Assignment** entity (**msdyn\_resourceassignment**).</span></span>

### <a name="structure"></a><span data-ttu-id="0fee8-145">Struktūra</span><span class="sxs-lookup"><span data-stu-id="0fee8-145">Structure</span></span>

<span data-ttu-id="0fee8-146">Naują grafiko kontūro struktūrą sudaro lankstūs laiko segmentai, kurie apibrėžti kiekvienai grafiko dienai.</span><span class="sxs-lookup"><span data-stu-id="0fee8-146">The new structure of the schedule contour consists of flexible time slices that are defined for each day of the schedule.</span></span> <span data-ttu-id="0fee8-147">Kiekvienas laiko segmentas turi šias ypatybes:</span><span class="sxs-lookup"><span data-stu-id="0fee8-147">Each time slice has the following properties:</span></span>

- <span data-ttu-id="0fee8-148">**Pradžia** – dienos darbo valandų pradžia pagal projekto kalendorių.</span><span class="sxs-lookup"><span data-stu-id="0fee8-148">**Start** – The start of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="0fee8-149">**Pabaiga** – dienos darbo valandų pabaiga pagal projekto kalendorių.</span><span class="sxs-lookup"><span data-stu-id="0fee8-149">**End** – The end of the working hours for the day, according to the project calendar.</span></span>
- <span data-ttu-id="0fee8-150">**Valandos** – valandų, priskirtų dienai, skaičius.</span><span class="sxs-lookup"><span data-stu-id="0fee8-150">**Hours** – The number of hours that are assigned on the day.</span></span>

<span data-ttu-id="0fee8-151">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="0fee8-151">**Example**</span></span>

<span data-ttu-id="0fee8-152">Šiame pavyzdyje pateikiamas projekto kalendorius, kuriame darbo diena tęsiasi nuo 9 val. iki 17 val. pagal UTC-8 laiko juostą.</span><span class="sxs-lookup"><span data-stu-id="0fee8-152">This example uses a project calendar where the workday is from 9 AM to 5 PM in the UTC-8 time zone.</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a><span data-ttu-id="0fee8-153">Automatinis planavimas ir rankinis planavimas</span><span class="sxs-lookup"><span data-stu-id="0fee8-153">Auto-scheduling and manual scheduling</span></span>

<span data-ttu-id="0fee8-154">Jei užduotis yra suplanuota automatiškai, valandos yra iš anksto įkeltos, o užduoties trukmę galima sutrumpinti.</span><span class="sxs-lookup"><span data-stu-id="0fee8-154">If a task is auto-scheduled, the hours are front-loaded, and the task duration might be reduced.</span></span>

<span data-ttu-id="0fee8-155">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="0fee8-155">**Example**</span></span>

<span data-ttu-id="0fee8-156">Ši užduotis automatiškai suplanuota 18 valandų trims dienoms (2018 m. gruodžio 3 d.–2018 m. gruodžio 5 d.).</span><span class="sxs-lookup"><span data-stu-id="0fee8-156">The following task is auto-scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

<span data-ttu-id="0fee8-157">Jei užduotis suplanuota rankiniu būdu, valandos vienodai paskirstomos visoms datoms.</span><span class="sxs-lookup"><span data-stu-id="0fee8-157">If a task is manually scheduled, the hours are evenly distributed to all the dates.</span></span>

<span data-ttu-id="0fee8-158">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="0fee8-158">**Example**</span></span>

<span data-ttu-id="0fee8-159">Ši užduotis rankiniu būdu suplanuota 18 valandų trims dienoms (2018 m. gruodžio 3 d.–2018 m. gruodžio 5 d.).</span><span class="sxs-lookup"><span data-stu-id="0fee8-159">The following task is manually scheduled for 18 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a><span data-ttu-id="0fee8-160">Priskyrimo vienetas</span><span class="sxs-lookup"><span data-stu-id="0fee8-160">Assignment unit</span></span>

<span data-ttu-id="0fee8-161">Priskyrimo vienetas nebenaudojamas PSA 3.x versijoje.</span><span class="sxs-lookup"><span data-stu-id="0fee8-161">The assignment unit has been deprecated in PSA 3.x.</span></span> <span data-ttu-id="0fee8-162">Užduoties vienos dienos pastangų valandos vienodai padalintos visiems priskirtiems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="0fee8-162">The task effort hours are now equally divided, per day, among all the assigned resources.</span></span>

<span data-ttu-id="0fee8-163">**Pavyzdys**</span><span class="sxs-lookup"><span data-stu-id="0fee8-163">**Example**</span></span>

<span data-ttu-id="0fee8-164">Šiame pavyzdyje užduotis priskirta dviem ištekliams ir automatiškai suplanuota 36 valandoms trims dienoms (2018 m. gruodžio 3 d.–2018 m. gruodžio 5 d.).</span><span class="sxs-lookup"><span data-stu-id="0fee8-164">In this example, the task is is assigned to two resources and is auto-scheduled for 36 hours over three days (December 3, 2018, to December 5, 2018).</span></span>

- <span data-ttu-id="0fee8-165">1 priskyrimas:</span><span class="sxs-lookup"><span data-stu-id="0fee8-165">Assignment 1:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- <span data-ttu-id="0fee8-166">2 priskyrimas:</span><span class="sxs-lookup"><span data-stu-id="0fee8-166">Assignment 2:</span></span>

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a><span data-ttu-id="0fee8-167">Kainodaros dimensijos</span><span class="sxs-lookup"><span data-stu-id="0fee8-167">Pricing dimensions</span></span>

<span data-ttu-id="0fee8-168">PSA 3.x versijoje konkrečių išteklių kainodaros dimensijos laukai (pavyzdžiui, **Vaidmuo** ir **Organizacinis vienetas**) pašalinti iš objekto **msdyn\_projecttask**.</span><span class="sxs-lookup"><span data-stu-id="0fee8-168">In PSA 3.x, resource-specific pricing dimension fields (such as **Role** and **Organizational Unit**) have been removed from the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="0fee8-169">Šiuos laukus dabar galima gauti iš išteklių priskyrimo (**msdyn\_resourceassignment**) atitinkamo projekto komandos nario (**msdyn\_projectteam**), kai sugeneruojami projekto įvertinimai.</span><span class="sxs-lookup"><span data-stu-id="0fee8-169">These fields can now be retrieved from the corresponding project team member (**msdyn\_projectteam**) of the resource assignment (**msdyn\_resourceassignment**) when project estimates are generated.</span></span> <span data-ttu-id="0fee8-170">Naujas laukas **msdyn\_organizationalunit** įtrauktas į objektą **msdyn\_projectteam**.</span><span class="sxs-lookup"><span data-stu-id="0fee8-170">A new field, **msdyn\_organizationalunit**, has been added to the **msdyn\_projectteam** entity.</span></span>

| <span data-ttu-id="0fee8-171">Nebenaudojamas laukas, esantis msdyn\_projecttask (Projekto užduotis)</span><span class="sxs-lookup"><span data-stu-id="0fee8-171">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="0fee8-172">Laukas iš msdyn\_projectteam (Projekto komandos narys), kuris naudojamas vietoje</span><span class="sxs-lookup"><span data-stu-id="0fee8-172">Field from msdyn\_projectteam (Project Team Member) that is used instead</span></span> |
|---|---|
| <span data-ttu-id="0fee8-173">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="0fee8-173">msdyn\_resourcecategory</span></span> | <span data-ttu-id="0fee8-174">msdyn\_resourcecategory</span><span class="sxs-lookup"><span data-stu-id="0fee8-174">msdyn\_resourcecategory</span></span> |
| <span data-ttu-id="0fee8-175">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="0fee8-175">msdyn\_organizationalunit</span></span> | <span data-ttu-id="0fee8-176">msdyn\_organizationalunit</span><span class="sxs-lookup"><span data-stu-id="0fee8-176">msdyn\_organizationalunit</span></span> |

## <a name="contours"></a><span data-ttu-id="0fee8-177">Kontūrai</span><span class="sxs-lookup"><span data-stu-id="0fee8-177">Contours</span></span>

<span data-ttu-id="0fee8-178">Kainodaros ir įvertinimo kontūro laukai, kurie nebenaudojami **msdyn\_projecttask** objekte.</span><span class="sxs-lookup"><span data-stu-id="0fee8-178">The pricing and estimation contour fields have been deprecated on the **msdyn\_projecttask** entity.</span></span> <span data-ttu-id="0fee8-179">Jie buvo perkelti į objektą **msdyn\_resourceassignment**.</span><span class="sxs-lookup"><span data-stu-id="0fee8-179">They have been moved to the **msdyn\_resourceassignment** entity.</span></span>

| <span data-ttu-id="0fee8-180">Nebenaudojamas laukas, esantis msdyn\_projecttask (Projekto užduotis)</span><span class="sxs-lookup"><span data-stu-id="0fee8-180">Deprecated field on msdyn\_projecttask (Project Task)</span></span> | <span data-ttu-id="0fee8-181">Naujas laukas, esantis msdyn\_resourceassignment (Išteklių priskyrimas)</span><span class="sxs-lookup"><span data-stu-id="0fee8-181">New field on msdyn\_resourceassignment (Resource Assignment)</span></span> |
|---|---|
| <span data-ttu-id="0fee8-182">msdyn\_costestimatecontour</span><span class="sxs-lookup"><span data-stu-id="0fee8-182">msdyn\_costestimatecontour</span></span> | <span data-ttu-id="0fee8-183">msdyn\_plannedcostcontour</span><span class="sxs-lookup"><span data-stu-id="0fee8-183">msdyn\_plannedcostcontour</span></span> |
| <span data-ttu-id="0fee8-184">msdyn\_salesestimatecontour</span><span class="sxs-lookup"><span data-stu-id="0fee8-184">msdyn\_salesestimatecontour</span></span> | <span data-ttu-id="0fee8-185">msdyn\_plannedsalescontour</span><span class="sxs-lookup"><span data-stu-id="0fee8-185">msdyn\_plannedsalescontour</span></span> |

<span data-ttu-id="0fee8-186">Toliau nurodyti laukai buvo įtraukti į objektą **msdyn\_resourceassignment**:</span><span class="sxs-lookup"><span data-stu-id="0fee8-186">The following fields have been added to the **msdyn\_resourceassignment** entity:</span></span>

* <span data-ttu-id="0fee8-187">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="0fee8-187">msdyn\_plannedcost</span></span>
* <span data-ttu-id="0fee8-188">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="0fee8-188">msdyn\_plannedsales</span></span>

<span data-ttu-id="0fee8-189">Toliau nurodyti suplanuotos, faktinės ir likusios savikainos ir pardavimo laukai objekte **msdyn\_projecttask** yra nepakitę:</span><span class="sxs-lookup"><span data-stu-id="0fee8-189">The following fields for planned, actual, and remaining cost and sales are unchanged on the **msdyn\_projecttask** entity:</span></span>

* <span data-ttu-id="0fee8-190">msdyn\_plannedcost</span><span class="sxs-lookup"><span data-stu-id="0fee8-190">msdyn\_plannedcost</span></span>
* <span data-ttu-id="0fee8-191">msdyn\_plannedsales</span><span class="sxs-lookup"><span data-stu-id="0fee8-191">msdyn\_plannedsales</span></span>
* <span data-ttu-id="0fee8-192">msdyn\_actualcost</span><span class="sxs-lookup"><span data-stu-id="0fee8-192">msdyn\_actualcost</span></span>
* <span data-ttu-id="0fee8-193">msdyn\_actualsales</span><span class="sxs-lookup"><span data-stu-id="0fee8-193">msdyn\_actualsales</span></span>
* <span data-ttu-id="0fee8-194">msdyn\_remainingcost</span><span class="sxs-lookup"><span data-stu-id="0fee8-194">msdyn\_remainingcost</span></span>
* <span data-ttu-id="0fee8-195">msdyn\_remainingsales</span><span class="sxs-lookup"><span data-stu-id="0fee8-195">msdyn\_remainingsales</span></span>
