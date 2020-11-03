---
title: Projekto eiga ir savikainos naudojimas
description: Šioje temoje pateikta informacija apie projekto eigos ir sąnaudų sekimą.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
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
ms.openlocfilehash: 3b60f72b371a76a59216b0b528d8e63513b06e0d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080997"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="e16dd-103">Projekto eiga ir savikainos naudojimas</span><span class="sxs-lookup"><span data-stu-id="e16dd-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e16dd-104">Poreikis sekti eigą atsižvelgiant į grafiką, priklauso nuo pramonės šakos.</span><span class="sxs-lookup"><span data-stu-id="e16dd-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="e16dd-105">Kai kurie pramonės šakų atstovai seka projektą stambiu planu, o kitų pramonės šakų atstovai seka eigą bendru planu.</span><span class="sxs-lookup"><span data-stu-id="e16dd-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="e16dd-106">Šioje temoje nurodyta, kaip planuoti norint atitikti jūsų organizacijos reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="e16dd-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="e16dd-107">Pastangų sekimo rodinys</span><span class="sxs-lookup"><span data-stu-id="e16dd-107">Effort tracking view</span></span>

<span data-ttu-id="e16dd-108">Rodinyje **Pastangų sekimas** sekama užduočių eiga grafike.</span><span class="sxs-lookup"><span data-stu-id="e16dd-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="e16dd-109">Jame faktinės pastangų valandos, sugaištos atliekant užduotį, lyginamos su suplanuotomis užduoties pastangų valandomis.</span><span class="sxs-lookup"><span data-stu-id="e16dd-109">It compares the actual effort hours spent on a task to the task's planned effort hours.</span></span> <span data-ttu-id="e16dd-110">Siekiant apskaičiuoti sekimo metrikas, „Project Service Automation“ naudoja šias formules:</span><span class="sxs-lookup"><span data-stu-id="e16dd-110">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="e16dd-111">Iš pradžių užduoties kūrime: suplanuota kaina bus nustatyta į numatomą savikainą.</span><span class="sxs-lookup"><span data-stu-id="e16dd-111">Initially on the task creation: Planned cost will be set to the Estimated cost at complete.</span></span> <span data-ttu-id="e16dd-112">Kai faktiniai duomenys įrašomi į užduotį, sekantis veiksmas bus stebėjimo rodinio apskaičiavimas pastangai</span><span class="sxs-lookup"><span data-stu-id="e16dd-112">Once Actuals are recorded on the task, the following will be calculation on the Tracking view for Effort</span></span>

- <span data-ttu-id="e16dd-113">Progreso procentas = faktinė pastanga iki šios datos ÷ įvertinimas pabaigoje (EAC)</span><span class="sxs-lookup"><span data-stu-id="e16dd-113">Progress percentage = Actual effort spent to date ÷ Estimate at complete (EAC)</span></span> 
- <span data-ttu-id="e16dd-114">Įvertinimas pabaigoje (ETC) = įvertinimas pabaigoje (EAC) – faktinė pastanga iki šios datos</span><span class="sxs-lookup"><span data-stu-id="e16dd-114">Estimate to complete (ETC) = Estimate at complete (EAC)  – Actual effort spent to date</span></span> 
- <span data-ttu-id="e16dd-115">EAC = likusi pastanga + faktinė pastanga iki šios datos</span><span class="sxs-lookup"><span data-stu-id="e16dd-115">EAC = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="e16dd-116">Numatomos pastangos nuokrypis = planuojamos pastangos – EAC</span><span class="sxs-lookup"><span data-stu-id="e16dd-116">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="e16dd-117">„Project Service Automation“ rodo pastangos nuokrypio užduotyje projekciją.</span><span class="sxs-lookup"><span data-stu-id="e16dd-117">Project Service Automation shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="e16dd-118">Jei EAC yra daugiau nei planuojamų pastangų, užduotis prognozuojama užtrukti ilgiau nei buvo planuota iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="e16dd-118">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="e16dd-119">Todėl pagal grafiką ją vėluojama atlikti.</span><span class="sxs-lookup"><span data-stu-id="e16dd-119">Therefore, it's behind schedule.</span></span> <span data-ttu-id="e16dd-120">Jei EAC yra mažiau nei planuojamų pastangų, užduotis prognozuojama užtrukti trumpiau nei buvo planuota iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="e16dd-120">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="e16dd-121">Todėl ji įgyvendinama greičiau nei nurodyta grafike.</span><span class="sxs-lookup"><span data-stu-id="e16dd-121">Therefore, it's ahead of schedule.</span></span>

## <a name="reprojecting-effort"></a><span data-ttu-id="e16dd-122">Pastangų pakartotinė prognozė</span><span class="sxs-lookup"><span data-stu-id="e16dd-122">Reprojecting effort</span></span>

<span data-ttu-id="e16dd-123">Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas.</span><span class="sxs-lookup"><span data-stu-id="e16dd-123">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="e16dd-124">Projekto pakartotinės prognozės yra projekto vadovo numatyta sąmata, apskaičiuota pagal dabartinę projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="e16dd-124">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="e16dd-125">Tačiau nerekomenduojame projekto vadovams keisti pradinių skaičių, nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.</span><span class="sxs-lookup"><span data-stu-id="e16dd-125">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="e16dd-126">Projektų vadovas gali iš naujo sukurti užduoties pastangų prognozę dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="e16dd-126">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="e16dd-127">Perrašyti numatytuosius ETC nustatymus su nauju užduoties likusių pastangų įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="e16dd-127">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="e16dd-128">Perrašyti numatytuosius eigos procentais nustatymus su nauju užduoties patikslintos eigos įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="e16dd-128">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="e16dd-129">Dėl kiekvieno iš šių metodų perskaičiuojamos užduoties ETC, EAC bei eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis.</span><span class="sxs-lookup"><span data-stu-id="e16dd-129">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="e16dd-130">Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.</span><span class="sxs-lookup"><span data-stu-id="e16dd-130">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="reprojection-of-effort-on-summary-tasks"></a><span data-ttu-id="e16dd-131">Pakartotinė pastangų suvestinėms užduotims prognozė</span><span class="sxs-lookup"><span data-stu-id="e16dd-131">Reprojection of effort on summary tasks</span></span>

<span data-ttu-id="e16dd-132">Pastangas suvestinėms užduotims ar talpyklės užduotims galima dar kartą prognozuoti.</span><span class="sxs-lookup"><span data-stu-id="e16dd-132">Effort on summary tasks or container tasks can be reprojected.</span></span> <span data-ttu-id="e16dd-133">Neatsižvelgiant į tai, ar vartotojas pakartotinai kurs suvestinių užduočių prognozę pagal likusiais pastangas ar eigą procentais, pradedami vykdyti šie skaičiavimo procesai:</span><span class="sxs-lookup"><span data-stu-id="e16dd-133">Regardless of whether the user reprojects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="e16dd-134">Užduoties EAC, ETC bei eiga procentais apskaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="e16dd-134">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="e16dd-135">Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis užduoties EAC.</span><span class="sxs-lookup"><span data-stu-id="e16dd-135">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="e16dd-136">Apskaičiuojamas kiekvienos individualios užduoties iki lapo mazgo užduočių naujas EAC.</span><span class="sxs-lookup"><span data-stu-id="e16dd-136">The new EAC on each of the individual tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="e16dd-137">Paveiktų antrinių užduočių iki lapų mazgų ETC ir eiga procentais perskaičiuojami pagal EAC reikšmę.</span><span class="sxs-lookup"><span data-stu-id="e16dd-137">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="e16dd-138">Taip sukuriama nauja pastangų užduočiai nuokrypio prognozė.</span><span class="sxs-lookup"><span data-stu-id="e16dd-138">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="e16dd-139">Suvestinių užduočių iki šaknies mazgo EAC perskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="e16dd-139">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="e16dd-140">Savikainos sekimo rodinys</span><span class="sxs-lookup"><span data-stu-id="e16dd-140">Cost tracking view</span></span> 

<span data-ttu-id="e16dd-141">**Kainos sekimo** rodinys lygina faktinę kainą, kuri buvo išleista užduočiai, su suplanuota kaina.</span><span class="sxs-lookup"><span data-stu-id="e16dd-141">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost.</span></span> 

> [!NOTE]
> <span data-ttu-id="e16dd-142">Šiame rodinyje rodomos tik darbo savikainos ir nėra įtraukiamos savikainos iš išlaidų įvertinimų.</span><span class="sxs-lookup"><span data-stu-id="e16dd-142">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="e16dd-143">Siekiant apskaičiuoti sekimo metrikas, „Project Service Automation“ naudoja šias formules:</span><span class="sxs-lookup"><span data-stu-id="e16dd-143">Project Service Automation uses the following formulas to calculate the tracking metrics:</span></span>

<span data-ttu-id="e16dd-144">Kai užduotis sukuriama, suplanuota kaina yra lygi numatytai užbaigimo kainai.</span><span class="sxs-lookup"><span data-stu-id="e16dd-144">When a task is created, the planned cost is equal to the estimated cost at complete.</span></span> <span data-ttu-id="e16dd-145">Kai faktiniai duomenys įrašomi į užduotį, toliau apskaičiuojamas **Sekimo** rodinys kainai:</span><span class="sxs-lookup"><span data-stu-id="e16dd-145">After actuals are recorded on the task, the following is calculated on the **Tracking** view for cost:</span></span>

 - <span data-ttu-id="e16dd-146">Sąnaudų procentinė dalis = iki šios datos išleista faktinė kaina ÷ numatyta užduoties užbaigimo kaina</span><span class="sxs-lookup"><span data-stu-id="e16dd-146">Percentage of cost consumed = Actual cost spent to date ÷ Estimated cost at complete for the task</span></span>
 - <span data-ttu-id="e16dd-147">Kaina užbaigti (CTC) = numatyta užbaigimo kaina – iki šios datos išleista faktinė kaina</span><span class="sxs-lookup"><span data-stu-id="e16dd-147">Cost to complete (CTC) = Estimated cost at complete – Actual cost spent to date</span></span>
 - <span data-ttu-id="e16dd-148">Numatyta užbaigimo kaina = CTC + iki šios datos išleista faktinė kaina</span><span class="sxs-lookup"><span data-stu-id="e16dd-148">Estimated cost at complete = CTC + Actual cost spent to date</span></span>
 - <span data-ttu-id="e16dd-149">Numatytas kainų nuokrypis = suplanuota kaina – numatyta užbaigimo kaina</span><span class="sxs-lookup"><span data-stu-id="e16dd-149">Projected cost variance = Planned cost – Estimated cost at complete</span></span>

<span data-ttu-id="e16dd-150">Rodoma savikainos nuokrypio užduočiai prognozė.</span><span class="sxs-lookup"><span data-stu-id="e16dd-150">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="e16dd-151">Jei numatyta užbaigimo kaina yra didesnė nei suplanuota kaina, numatoma, kad užduotis kainuos daugiau nei buvo planuota iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="e16dd-151">If the estimated cost at complete is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="e16dd-152">Todėl biudžetas viršijamas.</span><span class="sxs-lookup"><span data-stu-id="e16dd-152">Therefore, it's trending over budget.</span></span> <span data-ttu-id="e16dd-153">Jei numatyta užbaigimo kaina yra mažesnė nei suplanuota kaina, numatoma, kad užduotis kainuos mažiau nei buvo planuota iš pradžių ir nesieks biudžeto. </span><span class="sxs-lookup"><span data-stu-id="e16dd-153">If the Estimated cost at complete is less than the planned cost, the task is projected to cost less than was originally planned and is trending under budget.</span></span>

## <a name="project-managers-reprojection-of-cost"></a><span data-ttu-id="e16dd-154">Projekto vadovo nauja išlaidų prognozė</span><span class="sxs-lookup"><span data-stu-id="e16dd-154">Project manager’s reprojection of cost</span></span>

<span data-ttu-id="e16dd-155">Kai pastanga yra numatoma iš naujo, CTC, numatoma užbaigimo kaina, sąnaudų procentinė dalis ir numatomas kainos nuokrypis yra perskaičiuojami pagal **Kainos sekimo** rodinį.</span><span class="sxs-lookup"><span data-stu-id="e16dd-155">When effort is reprojected, the CTC, Estimated cost at complete, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="e16dd-156">Projekto būsenos suvestinė</span><span class="sxs-lookup"><span data-stu-id="e16dd-156">Project status summary</span></span>

<span data-ttu-id="e16dd-157">Stebėjimo duomenys rodiniuose **Pastangų sekimas** ir **Savikainos sekimas** nurodo projekto šakninio mazgo, suvestinių užduočių ir lapų mazgo užduočių lygių eigą ir sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="e16dd-157">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="e16dd-158">Skyriuje **Būsena** , esančiame puslapyje **Projekto objektas** , rodoma projekto lygio būsenos suvestinė.</span><span class="sxs-lookup"><span data-stu-id="e16dd-158">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="e16dd-159">Būsenos suvestinės laukai</span><span class="sxs-lookup"><span data-stu-id="e16dd-159">Status summary fields</span></span>

<span data-ttu-id="e16dd-160">Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="e16dd-160">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="e16dd-161">Lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, kad nurodytų didėjančią riziką.</span><span class="sxs-lookup"><span data-stu-id="e16dd-161">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="e16dd-162">Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną.</span><span class="sxs-lookup"><span data-stu-id="e16dd-162">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="e16dd-163">Lauko **Būsena atnaujinta** negalima redaguoti, o reikšmė turi laiko žyma, kuri nurodo kada paskutinį kartą buvo atnaujinta būsena.</span><span class="sxs-lookup"><span data-stu-id="e16dd-163">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="e16dd-164">Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo datą.</span><span class="sxs-lookup"><span data-stu-id="e16dd-164">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="e16dd-165">Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite nustatyti šiuos laukus į **Prieš laiką**.</span><span class="sxs-lookup"><span data-stu-id="e16dd-165">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="e16dd-166">Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti juos į **Vėluoja**.</span><span class="sxs-lookup"><span data-stu-id="e16dd-166">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
