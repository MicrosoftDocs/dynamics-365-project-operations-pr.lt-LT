---
title: Projekto eiga ir sąnaudos
description: Šioje temoje pateikta informacija apie tai, kaip sekti projekto eigą ir sąnaudas.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753754"
---
# <a name="project-progress-and-cost-consumption"></a><span data-ttu-id="5de31-103">Projekto eiga ir sąnaudos</span><span class="sxs-lookup"><span data-stu-id="5de31-103">Project progress and cost consumption</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5de31-104">Poreikis sekti eigą atsižvelgiant į grafiką, priklauso nuo pramonės šakos.</span><span class="sxs-lookup"><span data-stu-id="5de31-104">The need to track progress against a schedule varies by industry.</span></span> <span data-ttu-id="5de31-105">Kai kurie pramonės šakų atstovai seka projektą stambiu planu, o kitų pramonės šakų atstovai seka eigą bendru planu.</span><span class="sxs-lookup"><span data-stu-id="5de31-105">Some industries track at a granular level, whereas other industries track at a higher level.</span></span> <span data-ttu-id="5de31-106">Šioje temoje nurodyta, kaip planuoti norint atitikti jūsų organizacijos reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="5de31-106">This topic shows how to schedule in order to meet your organization's requirements.</span></span>

## <a name="effort-tracking-view"></a><span data-ttu-id="5de31-107">Pastangų sekimo rodinys</span><span class="sxs-lookup"><span data-stu-id="5de31-107">Effort tracking view</span></span>

<span data-ttu-id="5de31-108">Rodinyje **Pastangų sekimas** sekama užduočių eiga grafike.</span><span class="sxs-lookup"><span data-stu-id="5de31-108">The **Effort tracking** view tracks the progress of tasks in the schedule.</span></span> <span data-ttu-id="5de31-109">Jame faktinės pastangų valandos, iki šiol sugaištos atliekant užduotį, lyginamos su suplanuotomis užduoties pastangų valandomis.</span><span class="sxs-lookup"><span data-stu-id="5de31-109">It compares the actual effort hours that have been spent on a task to the planned effort hours for that task.</span></span> <span data-ttu-id="5de31-110">Norėdami apskaičiuoti sekimo metriką, PSA naudoja šias formules:</span><span class="sxs-lookup"><span data-stu-id="5de31-110">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="5de31-111">Eiga procentais = iki šios datos naudotos faktinės pastangos ÷ planuojamų užduoties pastangų</span><span class="sxs-lookup"><span data-stu-id="5de31-111">Progress percentage = Actual effort spent to date ÷ Planned effort for the task</span></span> 
- <span data-ttu-id="5de31-112">Įvertinimas užbaigti (ETC) = planuojamos pastangos – iki šios datos naudotos faktinės pastangos</span><span class="sxs-lookup"><span data-stu-id="5de31-112">Estimate to complete (ETC) = Planned effort – Actual effort spent to date</span></span> 
- <span data-ttu-id="5de31-113">Įvertinimas pabaigoje (EAC) = likusios pastangos – iki šios datos naudotos faktinės pastangos</span><span class="sxs-lookup"><span data-stu-id="5de31-113">Estimate at complete (EAC) = Remaining effort + Actual effort spent to date</span></span> 
- <span data-ttu-id="5de31-114">Numatomos pastangos nuokrypis = planuojamos pastangos – EAC</span><span class="sxs-lookup"><span data-stu-id="5de31-114">Projected effort variance = Planned effort – EAC</span></span>

<span data-ttu-id="5de31-115">PSA rodoma pastangų nuokrypio projekcija užduočiai.</span><span class="sxs-lookup"><span data-stu-id="5de31-115">PSA shows a projection of the effort variance on the task.</span></span> <span data-ttu-id="5de31-116">Jei EAC yra daugiau nei planuojamų pastangų, užduotis prognozuojama užtrukti ilgiau nei buvo planuota iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="5de31-116">If the EAC is more than the planned effort, the task is projected to take more time than was originally planned.</span></span> <span data-ttu-id="5de31-117">Todėl pagal grafiką ją vėluojama atlikti.</span><span class="sxs-lookup"><span data-stu-id="5de31-117">Therefore, it's behind schedule.</span></span> <span data-ttu-id="5de31-118">Jei EAC yra mažiau nei planuojamų pastangų, užduotis prognozuojama užtrukti trumpiau nei buvo planuota iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="5de31-118">If the EAC is less than the planned effort, the task is projected to take less time than was originally planned.</span></span> <span data-ttu-id="5de31-119">Todėl ji įgyvendinama greičiau nei nurodyta grafike.</span><span class="sxs-lookup"><span data-stu-id="5de31-119">Therefore, it's ahead of schedule.</span></span>

## <a name="re-projecting-effort"></a><span data-ttu-id="5de31-120">Projekto pakartotinė prognozė</span><span class="sxs-lookup"><span data-stu-id="5de31-120">Re-projecting effort</span></span>

<span data-ttu-id="5de31-121">Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas.</span><span class="sxs-lookup"><span data-stu-id="5de31-121">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="5de31-122">Projekto pakartotinės prognozės yra projekto vadovo, atsižvelgiant į dabartinę projekto būseną, įvertinimų suvokimas.</span><span class="sxs-lookup"><span data-stu-id="5de31-122">Project re-projections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="5de31-123">Tačiau nerekomenduojame projekto vadovams keisti pradinių skaičių, nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.</span><span class="sxs-lookup"><span data-stu-id="5de31-123">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="5de31-124">Yra du būdai, kaip projektų vadovas gali iš naujo sukurti užduotis pastangų prognozę:</span><span class="sxs-lookup"><span data-stu-id="5de31-124">There are two ways that a project manager can re-project effort on tasks:</span></span>

- <span data-ttu-id="5de31-125">Perrašyti numatytuosius ETC nustatymus su nauju užduoties likusių pastangų įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="5de31-125">Override the default ETC with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="5de31-126">Perrašyti numatytuosius eigos procentais nustatymus su nauju užduoties patikslintos eigos įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="5de31-126">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="5de31-127">Dėl kiekvieno iš šių metodų perskaičiuojamos užduoties ETC, EAC bei eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis.</span><span class="sxs-lookup"><span data-stu-id="5de31-127">Each of these approaches cause a recalculation of the task's ETC, EAC, and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="5de31-128">Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.</span><span class="sxs-lookup"><span data-stu-id="5de31-128">The EAC, ETC, and progress percentage on the summary tasks are also recalculated, and produce a new projection of effort variance.</span></span>

## <a name="re-projection-of-effort-on-summary-tasks"></a><span data-ttu-id="5de31-129">Pakartotinė pastangų suvestinėms užduotims prognozė</span><span class="sxs-lookup"><span data-stu-id="5de31-129">Re-projection of effort on summary tasks</span></span>

<span data-ttu-id="5de31-130">Pastangas suvestinėms užduotims ir konteinerio užduotims galima dar kartą prognozuoti.</span><span class="sxs-lookup"><span data-stu-id="5de31-130">Effort on summary tasks or container tasks can be re-projected.</span></span> <span data-ttu-id="5de31-131">Neatsižvelgiant į tai, ar vartotojas pakartotinai kurs suvestinių užduočių prognozę pagal likusiais pastangas ar eigą procentais, tokie skaičiavimo procesai pradedami vykdyti:</span><span class="sxs-lookup"><span data-stu-id="5de31-131">Regardless of whether the user re-projects by using the remaining effort or the progress percentage on the summary tasks, the following set of calculations begins:</span></span>

- <span data-ttu-id="5de31-132">Užduoties EAC, ETC bei eiga procentais apskaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="5de31-132">The EAC, ETC, and progress percentage on the task are calculated.</span></span>
- <span data-ttu-id="5de31-133">Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis užduoties EAC.</span><span class="sxs-lookup"><span data-stu-id="5de31-133">The new EAC is distributed down to the child tasks in the same proportion as the original EAC was on the task.</span></span>
- <span data-ttu-id="5de31-134">Naujas kiekvienos individualios užduoties iki lapo mazgo užduočių EAC apskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="5de31-134">The new EAC on each of the individualt tasks down to the leaf node tasks is calculated.</span></span> 
- <span data-ttu-id="5de31-135">Paveiktų antrinių užduočių iki lapų mazgų ETC ir eiga procentais perskaičiuojami pagal EAC reikšmę.</span><span class="sxs-lookup"><span data-stu-id="5de31-135">The affected child tasks down to the leaf nodes have their ETC and progress percentage recalculated based on the EAC value.</span></span> <span data-ttu-id="5de31-136">Taip sukuriama nauja pastangų užduočiai nuokrypio prognozė.</span><span class="sxs-lookup"><span data-stu-id="5de31-136">This results in a new projection for the effort variance of the task.</span></span> 
- <span data-ttu-id="5de31-137">Suvestinių užduočių iki šaknies mazgo EAC perskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="5de31-137">The EACs of the summary tasks all the way to the root node are recalculated.</span></span>

### <a name="cost-tracking-view"></a><span data-ttu-id="5de31-138">Savikainos sekimo rodinys</span><span class="sxs-lookup"><span data-stu-id="5de31-138">Cost tracking view</span></span> 

<span data-ttu-id="5de31-139">Rodinyje **Savikainos sekimas** lyginama faktinė savikaina užduočiai atlikti su planuojama užduoties savikaina.</span><span class="sxs-lookup"><span data-stu-id="5de31-139">The **Cost tracking** view compares the actual cost that was spent on a task to the planned cost on a task.</span></span> 

> [!NOTE]
> <span data-ttu-id="5de31-140">Šiame rodinyje rodomos tik darbo savikainos ir nėra įtraukiamos savikainos iš išlaidų įvertinimų.</span><span class="sxs-lookup"><span data-stu-id="5de31-140">This view shows only labor costs and doesn’t include costs from the expense estimates.</span></span> 

<span data-ttu-id="5de31-141">Norėdami apskaičiuoti sekimo metriką, PSA naudoja šias formules:</span><span class="sxs-lookup"><span data-stu-id="5de31-141">PSA uses the following formulas to calculate the tracking metrics:</span></span>

- <span data-ttu-id="5de31-142">Sąnaudų procentinė dalis = iki šios datos naudota faktinė savikaina ÷ planuojama užduoties savikaina</span><span class="sxs-lookup"><span data-stu-id="5de31-142">Percentage of cost consumed = Actual cost spent to date ÷ Planned cost for the task</span></span>
- <span data-ttu-id="5de31-143">Savikaina užbaigti (CTC) = planuojama savikaina – iki šios datos naudota savikaina</span><span class="sxs-lookup"><span data-stu-id="5de31-143">Cost to complete (CTC) = Planned cost – Actual cost spent to date</span></span>
- <span data-ttu-id="5de31-144">EAC = CTC + iki šios datos naudota faktinė savikaina</span><span class="sxs-lookup"><span data-stu-id="5de31-144">EAC = CTC + Actual cost spent to date</span></span>
- <span data-ttu-id="5de31-145">Prognozuojamas savikainos nuokrypis = planuojama savikaina – EAC</span><span class="sxs-lookup"><span data-stu-id="5de31-145">Projected cost variance = Planned cost – EAC</span></span>

<span data-ttu-id="5de31-146">Rodoma savikainos nuokrypio užduočiai prognozė.</span><span class="sxs-lookup"><span data-stu-id="5de31-146">A projection of the cost variance is shown on the task.</span></span> <span data-ttu-id="5de31-147">Jei EAC yra daugiau nei planuojama savikaina, užduotis prognozuojama kainuosianti daugiau nei buvo planuota iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="5de31-147">If the EAC is more than the planned cost, the task is projected to cost more than was originally planned.</span></span> <span data-ttu-id="5de31-148">Todėl biudžetas viršijamas.</span><span class="sxs-lookup"><span data-stu-id="5de31-148">Therefore, it's trending over budget.</span></span> <span data-ttu-id="5de31-149">Jei EAC yra mažiau nei planuojama savikaina, užduotis prognozuojama kainuosianti daugiau nei buvo planuota iš pradžių.</span><span class="sxs-lookup"><span data-stu-id="5de31-149">If the EAC is less than the planned cost, the task is projected to cost less than was originally planned.</span></span> <span data-ttu-id="5de31-150">Todėl biudžetas nėra viršijamas.</span><span class="sxs-lookup"><span data-stu-id="5de31-150">Therefore, it's trending under budget.</span></span>

## <a name="project-managers-re-projection-of-cost"></a><span data-ttu-id="5de31-151">Projekto vadovo nauja išlaidų prognozė</span><span class="sxs-lookup"><span data-stu-id="5de31-151">Project manager’s re-projection of cost</span></span>

<span data-ttu-id="5de31-152">Kai pastangos yra iš naujo prognozuojamos, CTC, EAC, sąnaudų procentinė dalis ir prognozuojamas savikainos nuokrypis perskaičiuojami pagal rodinį **Savikainos sekimas**.</span><span class="sxs-lookup"><span data-stu-id="5de31-152">When effort is re-projected, the CTC, EAC, percentage of cost consumed, and projected cost variance are all recalculated in the **Cost tracking** view.</span></span>

## <a name="project-status-summary"></a><span data-ttu-id="5de31-153">Projekto būsenos suvestinė</span><span class="sxs-lookup"><span data-stu-id="5de31-153">Project status summary</span></span>

<span data-ttu-id="5de31-154">Stebėjimo duomenys rodiniuose **Pastangų sekimas** ir **Savikainos sekimas** nurodo projekto šakninio mazgo, suvestinių užduočių ir lapų mazgo užduočių lygių eigą ir sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="5de31-154">Tracking data in the **Effort tracking** and **Cost tracking** views shows the progress and cost consumption at the project root node, summary tasks, and leaf node tasks levels.</span></span> <span data-ttu-id="5de31-155">Skyriuje **Būsena**, esančiame puslapyje **Projekto objektas**, rodoma projekto lygio būsenos suvestinė.</span><span class="sxs-lookup"><span data-stu-id="5de31-155">The **Status** section on the **Project entity** page shows a summary of project-level status.</span></span>

## <a name="status-summary-fields"></a><span data-ttu-id="5de31-156">Būsenos suvestinės laukai</span><span class="sxs-lookup"><span data-stu-id="5de31-156">Status summary fields</span></span>

<span data-ttu-id="5de31-157">Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="5de31-157">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="5de31-158">Lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, kad nurodytų didėjančią riziką.</span><span class="sxs-lookup"><span data-stu-id="5de31-158">It uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> <span data-ttu-id="5de31-159">Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną.</span><span class="sxs-lookup"><span data-stu-id="5de31-159">The **Comments** field lets the project manager enter specific comments about the status.</span></span> <span data-ttu-id="5de31-160">Lauko **Būsena atnaujinta** negalima redaguoti, o reikšmė turi laiko žyma, kuri nurodo kada paskutinį kartą buvo atnaujinta būsena.</span><span class="sxs-lookup"><span data-stu-id="5de31-160">The **Status updated on** field is not editable and the value is a timestamp that indicates when the status was last updated.</span></span>

<span data-ttu-id="5de31-161">Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo datą.</span><span class="sxs-lookup"><span data-stu-id="5de31-161">The **Schedule performance** and **Cost performance** fields are set from the tracking date.</span></span> <span data-ttu-id="5de31-162">Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite nustatyti šiuos laukus į **Prieš laiką**.</span><span class="sxs-lookup"><span data-stu-id="5de31-162">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, you can set these fields to **Ahead**.</span></span> <span data-ttu-id="5de31-163">Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti juos į **Vėluoja**.</span><span class="sxs-lookup"><span data-stu-id="5de31-163">When the schedule and cost variance for the root node are negative, you can set them to **Behind**.</span></span>
