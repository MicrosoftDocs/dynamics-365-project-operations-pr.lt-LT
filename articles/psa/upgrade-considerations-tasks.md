---
title: Darbo paskirstymo struktūros atnaujinimo aptarimas
description: Šioje temoje pateikta informacija, kaip atnaujinti darbo paskirstymo struktūrą pereinant iš „Project Service Automation“ 2.x versijos į 3.x versiją.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/18/2019
ms.topic: article
author: ruhercul
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
ms.openlocfilehash: d31ca60b267063e9cadf544468ece501353950fa
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951354"
---
# <a name="upgrade-considerations-for-the-work-breakdown-structure"></a><span data-ttu-id="225c8-103">Darbo paskirstymo struktūros atnaujinimo aptarimas</span><span class="sxs-lookup"><span data-stu-id="225c8-103">Upgrade considerations for the work breakdown structure</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="225c8-104">Šioje temoje pateikta informacija, kaip atnaujinti darbo paskirstymo struktūrą pereinant iš „Project Service Automation“ 2.x versijos į 3.x versiją.</span><span class="sxs-lookup"><span data-stu-id="225c8-104">This topic provides information about upgrading the work breakdown structure from Project Service Automation 2.x to 3.x.</span></span> <span data-ttu-id="225c8-105">Šioje temoje apibūdinta tinkama „Project Service Automation“ (PSA) projekto būsena, kurios reikia norint sėkmingai atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="225c8-105">This topic defines the healthy state of a project in Project Service Automation (PSA) that is required for a successful upgrade.</span></span> <span data-ttu-id="225c8-106">Taip pat pateikiama informacija apie įprastas blokavimo sąlygas, dėl kurių nepavyks atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="225c8-106">There is also information about the common blocking conditions that will cause upgrade to fail.</span></span> <span data-ttu-id="225c8-107">Daugiau informacijos apie projekto užduočių nustatymą ir jų funkcijas projekto grafike žr [Projekto grafikai](project-creating.md).</span><span class="sxs-lookup"><span data-stu-id="225c8-107">For more information about defining project tasks and their functions within a project schedule, see [Project schedules](project-creating.md).</span></span>

## <a name="key-entities"></a><span data-ttu-id="225c8-108">Pagrindiniai objektai</span><span class="sxs-lookup"><span data-stu-id="225c8-108">Key entities</span></span>
<span data-ttu-id="225c8-109">Tiksliai darbo paskirstymo struktūrai, į kurią jau įkelta išteklių, reikia toliau nurodytų objektų:</span><span class="sxs-lookup"><span data-stu-id="225c8-109">For an accurate work breakdown structure that is already loaded with resources, the following entities are required:</span></span>

- [<span data-ttu-id="225c8-110">Projektas</span><span class="sxs-lookup"><span data-stu-id="225c8-110">Project</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project)
- [<span data-ttu-id="225c8-111">Projekto komanda</span><span class="sxs-lookup"><span data-stu-id="225c8-111">Project Team</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam)
- [<span data-ttu-id="225c8-112">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="225c8-112">Project Task</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask)
- [<span data-ttu-id="225c8-113">Išteklių priskyrimai</span><span class="sxs-lookup"><span data-stu-id="225c8-113">Resource Assignments</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment)
- [<span data-ttu-id="225c8-114">Projekto užduoties priklausomybė</span><span class="sxs-lookup"><span data-stu-id="225c8-114">Project Task Dependency</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency)
- [<span data-ttu-id="225c8-115">Rezervuojami ištekliai</span><span class="sxs-lookup"><span data-stu-id="225c8-115">Bookable Resources</span></span>](/dynamics365/customerengagement/on-premises/developer/entities/bookableresource)

<span data-ttu-id="225c8-116">Jei norite nustatyti darbo paskirstymo struktūrą, į kurią įkelti ištekliai, turite atlikti šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="225c8-116">To define a resource loaded work breakdown structure, you must complete the following steps:</span></span>

1. <span data-ttu-id="225c8-117">Kurti naują projektą</span><span class="sxs-lookup"><span data-stu-id="225c8-117">Create a new project.</span></span> <span data-ttu-id="225c8-118">Daugiau informacijos apie tai, kaip sukurti naują projektą, žr. [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span><span class="sxs-lookup"><span data-stu-id="225c8-118">For more information about how to create a new project, see [msdyn_project](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_project).</span></span>
2. <span data-ttu-id="225c8-119">Sukurkite vieną ar kelias užduotis.</span><span class="sxs-lookup"><span data-stu-id="225c8-119">Create one or more tasks.</span></span> <span data-ttu-id="225c8-120">Daugiau informacijos apie tai, kaip sukurti užduotį, žr. [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span><span class="sxs-lookup"><span data-stu-id="225c8-120">For more information about how to create a task, see [msdyn_projecttask](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttask).</span></span>
3. <span data-ttu-id="225c8-121">Nustatykite užduočių priklausomybes.</span><span class="sxs-lookup"><span data-stu-id="225c8-121">Define the task dependencies.</span></span> <span data-ttu-id="225c8-122">Daugiau informacijos žr. [Projekto užduoties priklausomybė](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span><span class="sxs-lookup"><span data-stu-id="225c8-122">For more information, see [Project Task Dependency](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projecttaskdependency).</span></span>
4. <span data-ttu-id="225c8-123">Priskirkite projekto komandos narius prie projekto.</span><span class="sxs-lookup"><span data-stu-id="225c8-123">Assign project team members to the project.</span></span> <span data-ttu-id="225c8-124">Daugiau informacijos žr. [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span><span class="sxs-lookup"><span data-stu-id="225c8-124">For more information, see [msdyn_projectteam](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_projectteam).</span></span>
5. <span data-ttu-id="225c8-125">Priskirkite projekto komandos narius užduotims.</span><span class="sxs-lookup"><span data-stu-id="225c8-125">Assign project team members to the tasks.</span></span> <span data-ttu-id="225c8-126">Daugiau informacijos žr. [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span><span class="sxs-lookup"><span data-stu-id="225c8-126">For more information, see [msdyn_resourceassignment](/dynamics365/customerengagement/on-premises/developer/entities/msdyn_resourceassignment).</span></span>

## <a name="project-team-relationships"></a><span data-ttu-id="225c8-127">Projekto komandos ryšiai</span><span class="sxs-lookup"><span data-stu-id="225c8-127">Project team relationships</span></span>

<span data-ttu-id="225c8-128">Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:</span><span class="sxs-lookup"><span data-stu-id="225c8-128">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>
- <span data-ttu-id="225c8-129">Visi projekto komandos nariai turi būti susieti su rezervuojamu ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="225c8-129">All project team members must be associated with a bookable resource.</span></span>
- <span data-ttu-id="225c8-130">Visi projekto komandos nariai turi būti susieti su tuo pačiu projektu.</span><span class="sxs-lookup"><span data-stu-id="225c8-130">All project team members must be associated with the same project.</span></span> 

## <a name="project-task-relationships"></a><span data-ttu-id="225c8-131">Projekto užduočių ryšiai</span><span class="sxs-lookup"><span data-stu-id="225c8-131">Project task relationships</span></span>
<span data-ttu-id="225c8-132">Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:</span><span class="sxs-lookup"><span data-stu-id="225c8-132">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="225c8-133">Bet kokios susijusios užduotys turi būti susietos su tuo pačiu projektu.</span><span class="sxs-lookup"><span data-stu-id="225c8-133">Any related tasks must be associated with the same project.</span></span>
- <span data-ttu-id="225c8-134">Kiekviena eilutės užduotis turi turėti pirminę užduotį.</span><span class="sxs-lookup"><span data-stu-id="225c8-134">Every line task must have a parent task.</span></span>
- <span data-ttu-id="225c8-135">Kiekviena užduotis turi turėti pirminį projektą.</span><span class="sxs-lookup"><span data-stu-id="225c8-135">Every task must have a parent project.</span></span>

### <a name="valid-conditions"></a><span data-ttu-id="225c8-136">Galiojimo sąlygos</span><span class="sxs-lookup"><span data-stu-id="225c8-136">Valid conditions</span></span>

- <span data-ttu-id="225c8-137">Visų užduočių trukmė turi būti didesnė arba lygi (>=) vienai valandai ir mažesnė nei 1 800 000 minučių (1 250 dienų).\*</span><span class="sxs-lookup"><span data-stu-id="225c8-137">All task durations must be greater than or equal to (>=) one hour and less than 1,800,000 minutes (1,250 days).\*</span></span>
- <span data-ttu-id="225c8-138">Visų užduočių pradžios data turi būti ne ankstesnė nei 2000/01/01.\*</span><span class="sxs-lookup"><span data-stu-id="225c8-138">All tasks must have a start date no earlier than 2000/01/01.\*</span></span>
- <span data-ttu-id="225c8-139">Visų užduočių pradžios data turi būti ne vėliau kaip 17 metų nuo dabartinės dienos.\*</span><span class="sxs-lookup"><span data-stu-id="225c8-139">All tasks must have a start date no later than 17 years from the present day.\*</span></span>
- <span data-ttu-id="225c8-140">Visų užduočių pradžios data turi būti ankstesnė nei pabaigos data arba jai lygi.</span><span class="sxs-lookup"><span data-stu-id="225c8-140">All tasks must have a start date earlier or equal to their finish date.</span></span>
- <span data-ttu-id="225c8-141">Visų klasifikacijų operacijų tipai (išlaidos, medžiagos, mokestis ir laikas) turi turėti **Numatytojo vieneto** ir **Vienetų grupės** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="225c8-141">All transaction types on classifications (Expense, Material, Tax, and Time) must have values for **Default Unit** and **Unit Group**.</span></span>
- <span data-ttu-id="225c8-142">Reikia vengti datos formatų su raidėmis.</span><span class="sxs-lookup"><span data-stu-id="225c8-142">Date formats with letters should be avoided.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="225c8-143">Potencialūs sumažinimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="225c8-143">Potential mitigation steps</span></span>
- <span data-ttu-id="225c8-144">Naudodami išplėstinę iešką galite identifikuoti projekto užduotis, kurios neturi projekto ID.</span><span class="sxs-lookup"><span data-stu-id="225c8-144">Use Advanced Find to identify Project tasks that do not contain a Project ID.</span></span>
- <span data-ttu-id="225c8-145">Naudodami išplėstinę iešką galite identifikuoti projekto užduotis, kurių suplanuota trukmė yra ilgesnė nei >1 800 000.</span><span class="sxs-lookup"><span data-stu-id="225c8-145">Use Advanced Find to identify Project tasks where the scheduled duration is greater than > 1,800,000.</span></span>
- <span data-ttu-id="225c8-146">Prieš keisdami duomenis, turite išanalizuoti visus tinkinimus, susijusius su objektu, dėl kurio gali suprastėti duomenų būsena.</span><span class="sxs-lookup"><span data-stu-id="225c8-146">Prior to making any data changes, you should investigate any customizations associated with the entity that may have led to getting the data into a bad state.</span></span> <span data-ttu-id="225c8-147">Šie tinkinimai turėtų būti išanalizuoti prieš pradedant bet kokius su duomenimis susijusius naujinimus.</span><span class="sxs-lookup"><span data-stu-id="225c8-147">These customizations should be addressed before proceeding with any data-related updates.</span></span>
- <span data-ttu-id="225c8-148">Jei identifikuotos užduotys yra pavienės, apsvarstykite šių užduočių panaikinimą, jei jų nereikia, arba ar jas reikia susieti su tinkamu pirminiu projektu.</span><span class="sxs-lookup"><span data-stu-id="225c8-148">For the identified tasks that have been orphaned, consider deleting these tasks if they are not needed or if they should be associated with the correct parent project.</span></span>
- <span data-ttu-id="225c8-149">Jei užduočių trukmė yra ilgesnė nei 1250 dienos, apsvarstykite įtraukti kelias užduotis, kad būtų atspindėta bendra trukmė, jei įmanoma.</span><span class="sxs-lookup"><span data-stu-id="225c8-149">For any tasks where the duration is greater than 1,250 days, consider adding multiple tasks to represent the total duration, if feasible.</span></span>

> [!NOTE]
> <span data-ttu-id="225c8-150">Elementai, pažymėti žvaigždute (\*), turi apribojimus, nes ryšių su klientais valdymas (CRM) palaiko tik 7 320 pasikartojimų išplėtimus.</span><span class="sxs-lookup"><span data-stu-id="225c8-150">Items noted with an asterisk (\*) have limits that are due to the fact that customer relationship management (CRM) supports only 7,320 recurrence expansions.</span></span> <span data-ttu-id="225c8-151">Negalima viršyti šio apribojimo.</span><span class="sxs-lookup"><span data-stu-id="225c8-151">You must stay below this limit.</span></span>

## <a name="resource-assignment-relationships"></a><span data-ttu-id="225c8-152">Išteklių priskyrimo ryšiai</span><span class="sxs-lookup"><span data-stu-id="225c8-152">Resource Assignment relationships</span></span>
<span data-ttu-id="225c8-153">Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:</span><span class="sxs-lookup"><span data-stu-id="225c8-153">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="225c8-154">Visi išteklių priskyrimai darbo paskirstymo struktūroje turi būti susiję su tuo pačiu projektu.</span><span class="sxs-lookup"><span data-stu-id="225c8-154">All Resource Assignments in a work breakdown structure must be related to the same project.</span></span>
- <span data-ttu-id="225c8-155">Visi išteklių priskyrimai darbo paskirstymo struktūroje turi būti susieti su projekto komandos nariais tame pačiame projekte.</span><span class="sxs-lookup"><span data-stu-id="225c8-155">All Resource Assignments in a work breakdown structure must be associated to project team members in the same project.</span></span>

### <a name="potential-mitigation-steps"></a><span data-ttu-id="225c8-156">Potencialūs sumažinimo veiksmai</span><span class="sxs-lookup"><span data-stu-id="225c8-156">Potential mitigation steps</span></span>
- <span data-ttu-id="225c8-157">Identifikuokite visas užduotis, kurios nepatenkina pirmiau aprašytų sąlygų.</span><span class="sxs-lookup"><span data-stu-id="225c8-157">Identify all tasks that fall outside the conditions described above.</span></span>  
- <span data-ttu-id="225c8-158">Reikia panaikinti visus išteklių priskyrimus, kurie nebegalioja.</span><span class="sxs-lookup"><span data-stu-id="225c8-158">Any Resource Assignments that are no longer valid should be deleted.</span></span>

## <a name="project-task-dependency-relationships"></a><span data-ttu-id="225c8-159">Projekto užduoties priklausomybės ryšiai</span><span class="sxs-lookup"><span data-stu-id="225c8-159">Project task dependency relationships</span></span>
<span data-ttu-id="225c8-160">Norint užtikrinti sėkmingą atnaujinimą, reikia tinkamai išlaikyti šiuos ryšius:</span><span class="sxs-lookup"><span data-stu-id="225c8-160">To ensure a successful upgrade, the following relationships must be correctly maintained:</span></span>

- <span data-ttu-id="225c8-161">Visos projekto užduočių priklausomybės turi būti susijusios su tuo pačiu projektu.</span><span class="sxs-lookup"><span data-stu-id="225c8-161">All project task dependencies must be related to the same project.</span></span>
- <span data-ttu-id="225c8-162">Užduotyje ta pati priklausomybė negali būti nurodyta daugiau nei vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="225c8-162">A task can't have the same dependency referenced more than once.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]