---
title: Sąskaitos faktūros grafikų kūrimas projektu pagrįstoje sutarties eilutėje – „Lite“ versija
description: Šioje temoje pateikta informacija apie sąskaitų faktūrų grafikų ir etapų kūrimą.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4706a2a711efa7d176030deaa33b65bca28d8498
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273388"
---
# <a name="create-invoice-schedules-on-a-project-based-contract-line---lite"></a><span data-ttu-id="869da-103">Sąskaitos faktūros grafikų kūrimas projektu pagrįstoje sutarties eilutėje – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="869da-103">Create invoice schedules on a project-based contract line - lite</span></span>

<span data-ttu-id="869da-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="869da-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="869da-105">Projektu pagrįstoje sutarties eilutėje galite pridėti sąskaitos faktūros grafiką.</span><span class="sxs-lookup"><span data-stu-id="869da-105">You can attach an invoice schedule on a project-based contract line.</span></span> <span data-ttu-id="869da-106">Sąskaitas faktūras išrašyti galima tik tada, kai laimėtas projekto sutarties kūrimo konkursas.</span><span class="sxs-lookup"><span data-stu-id="869da-106">Invoicing is only allowed after the contract is won to create a Project contract.</span></span> <span data-ttu-id="869da-107">Sąskaitų faktūrų grafikas leidžia automatiškai kurti projektu pagrįstos sutarties eilutės sąskaitų faktūrų juodraščius.</span><span class="sxs-lookup"><span data-stu-id="869da-107">Invoice schedules allow draft invoices for a project-based contract line to be created automatically.</span></span> <span data-ttu-id="869da-108">Jei ketinate visada sąskaitas faktūras išrašyti neautomatiniu būdu, galite praleisti sąskaitų faktūrų grafikų kūrimo projektu pagrįstoje sutarties eilutėje ar įprastoje sutarties eilutėje etapą.</span><span class="sxs-lookup"><span data-stu-id="869da-108">If you plan to always create invoices manually, you can skip creating invoice schedules on a project-based contract line or a contract line.</span></span>

## <a name="create-a-time-and-material-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="869da-109">Laiko ir medžiagų sąskaitų faktūrų grafiko kūrimas projektu pagrįstai sutarties eilutei</span><span class="sxs-lookup"><span data-stu-id="869da-109">Create a time and material invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="869da-110">Kai projektu pagrįstos sutarties eilutės atsiskaitymo būdas yra laikas ir medžiaga, galite kurti data pagrįstą sąskaitos faktūros grafiką.</span><span class="sxs-lookup"><span data-stu-id="869da-110">When a project-based contract line has a time and material billing method, you can create a date-based invoice schedule.</span></span> <span data-ttu-id="869da-111">Norėdami automatiškai sugeneruoti data pagrįstą sąskaitos faktūros grafiką, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="869da-111">To automatically generate a date-based invoice schedule, complete the following steps.</span></span>

1. <span data-ttu-id="869da-112">Nueikite į **Parametrai** > **Sąskaitų faktūrų dažnis**, kad nustatytumėte sąskaitų faktūrų dažnį.</span><span class="sxs-lookup"><span data-stu-id="869da-112">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="869da-113">Atidarykite projekto sutartį ir skirtuke **Suvestinė** nustatykite pageidaujamą pristatymo datą.</span><span class="sxs-lookup"><span data-stu-id="869da-113">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="869da-114">Atidarykite laiko ir medžiagų sutarties eilutę, kuriai norite sukurti data pagrįstą sąskaitų faktūrų grafiką.</span><span class="sxs-lookup"><span data-stu-id="869da-114">Open the time and material contract line that you want to create a date-based invoice schedule for.</span></span> 
4. <span data-ttu-id="869da-115">Skirtuke **Sąskaitų faktūrų grafikas** pažymėkite sąskaitų išrašymo pradžios datą ir sąskaitų faktūrų dažnį.</span><span class="sxs-lookup"><span data-stu-id="869da-115">On the **Invoice Schedule** tab, select a billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="869da-116">Papildomame tinklelyje pasirinkite **Generuoti sąskaitų faktūrų grafiką**.</span><span class="sxs-lookup"><span data-stu-id="869da-116">On the subgrid, select **Generate Invoice Schedule**.</span></span>

    <span data-ttu-id="869da-117">Sistema sąskaitų faktūrų grafiką sukuria su tolesne laukų informacija.</span><span class="sxs-lookup"><span data-stu-id="869da-117">The system generates the invoice schedule with the following field information:</span></span>

    - <span data-ttu-id="869da-118">**Sąskaitos faktūros vykdymo data** nustatoma kaip data, parenkama pagal sąskaitų faktūrų dažnį.</span><span class="sxs-lookup"><span data-stu-id="869da-118">**Invoice Run Date** is set to the date based on the invoice frequency.</span></span>
    - <span data-ttu-id="869da-119">**Operacijos galutinė data** nustatoma kaip diena prieš **sąskaitos faktūros vykdymo datą**.</span><span class="sxs-lookup"><span data-stu-id="869da-119">**Transaction Cut-off Date** is set to the day before the **Invoice Run Date**.</span></span>
    - <span data-ttu-id="869da-120">**Vykdymo būsena** automatiškai nustatoma į **Nevykdoma**.</span><span class="sxs-lookup"><span data-stu-id="869da-120">**Run Status** is automatically set to **Not Run**.</span></span> <span data-ttu-id="869da-121">Kai automatinio sąskaitos faktūros kūrimo užduotis paleidžiama tam tikrai **sąskaitos faktūros vykdymo datai**, ji atnaujins šį lauką į **Vykdymas sėkmingas** arba **Vykdymas nepavyko**.</span><span class="sxs-lookup"><span data-stu-id="869da-121">When the automatic invoice creation job runs for a certain **Invoice Run Date**, this field is updated to **Run Successful** or **Run Failed**.</span></span>

## <a name="create-a-fixed-price-invoice-schedule-for-a-project-based-contract-line"></a><span data-ttu-id="869da-122">Fiksuotos kainos sąskaitų faktūrų grafiko kūrimas projektu pagrįstai sutarties eilutei</span><span class="sxs-lookup"><span data-stu-id="869da-122">Create a fixed price invoice schedule for a project-based contract line</span></span>

<span data-ttu-id="869da-123">Kai projektu pagrįstai sutarties eilutei taikomas fiksuotos kainos atsiskaitymo metodas, galite sukurti etapinį sąskaitų faktūrų grafiką.</span><span class="sxs-lookup"><span data-stu-id="869da-123">When a project-based contract line has a fixed price billing method, you can create a milestone-based invoice schedule.</span></span> <span data-ttu-id="869da-124">Atlikite šiuos veiksmus, kad automatiškai būtų sukurtas etapinis sąskaitų faktūrų grafikas, pagal kurį nustatomas baigtinis etapų, tolygiai paskirstančių per kalendoriaus laikotarpį, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="869da-124">Complete the following steps to automatically generate a milestone-based invoice schedule for a fixed set of milestones that distribute equally for the calendar period.</span></span>

1. <span data-ttu-id="869da-125">Nueikite į **Parametrai** > **Sąskaitų faktūrų dažnis**, kad nustatytumėte sąskaitų faktūrų dažnį.</span><span class="sxs-lookup"><span data-stu-id="869da-125">Go to **Settings** > **Invoice Frequencies** to set up invoice frequency.</span></span>
2. <span data-ttu-id="869da-126">Atidarykite projekto sutartį ir skirtuke **Suvestinė** nustatykite pageidaujamą pristatymo datą.</span><span class="sxs-lookup"><span data-stu-id="869da-126">Open the project contract and on the **Summary** tab, set the requested delivery date.</span></span>
3. <span data-ttu-id="869da-127">Atidarykite fiksuotos kainos sutarties eilutę, kuriai reikia sukurti etapų grafiką.</span><span class="sxs-lookup"><span data-stu-id="869da-127">Open the fixed price contract line on which you need to create a milestone schedule.</span></span> 
4. <span data-ttu-id="869da-128">Skirtuke **Sąskaitų faktūrų grafikas (atsiskaitymo etapai)** pažymėkite sąskaitų išrašymo pradžios datą ir sąskaitų faktūrų dažnį.</span><span class="sxs-lookup"><span data-stu-id="869da-128">On the **Invoice Schedule (Billing Milestones)** tab, select the billing start date and the invoice frequency.</span></span> 
5. <span data-ttu-id="869da-129">Papildomame tinklelyje pasirinkite **Periodiški etapai**.</span><span class="sxs-lookup"><span data-stu-id="869da-129">On the subgrid, select **Generate Periodic Milestones**.</span></span>

    <span data-ttu-id="869da-130">Sistema sąskaitų faktūrų grafiką sukuria su tolesne etapų informacija.</span><span class="sxs-lookup"><span data-stu-id="869da-130">The system generates the invoice schedule with the following milestone information.</span></span>

    - <span data-ttu-id="869da-131">**Etapo pavadinimas** nustatomas kaip data, parenkama pagal sąskaitų faktūrų dažnį.</span><span class="sxs-lookup"><span data-stu-id="869da-131">**Milestone Name** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="869da-132">**Etapo data** nustatoma kaip data, parenkama pagal sąskaitų faktūrų dažnį.</span><span class="sxs-lookup"><span data-stu-id="869da-132">**Milestone Date** is set to the date that is dictated based on the invoice frequency.</span></span>
    - <span data-ttu-id="869da-133">**Etapo suma** apskaičiuojama sutarties sumą projektu pagrįstoje sutarties eilutėje padalijant iš etapų skaičiaus, kaip tai nurodo dažnis, sąskaitų išrašymo pradžia ir pageidaujamos pristatymo datos.</span><span class="sxs-lookup"><span data-stu-id="869da-133">**Milestone Amount** is calculated by dividing the contract amount on the project-based contract line by the number of milestones as dictated by the frequency, billing start, and requested delivery dates.</span></span>
    - <span data-ttu-id="869da-134">Jei sutarties eilutės lauke **Įvertinta mokesčių suma** yra reikšmė, šis laukas taip pat proporcingai paskirstomas kiekvienam etapui, kai generuojami periodiniai etapai.</span><span class="sxs-lookup"><span data-stu-id="869da-134">If the contract line has a value in the **Estimated Tax Amount** field, this field is also apportioned to each milestone equally when generating periodic milestones.</span></span>

<span data-ttu-id="869da-135">Atsiskaitymo etapai turi būti lygūs projektu pagrįstos sutarties eilutės vertei.</span><span class="sxs-lookup"><span data-stu-id="869da-135">Billing milestones should equal the contracted value of the project-based contract line.</span></span> <span data-ttu-id="869da-136">Jei jie nėra lygūs, įvyksta klaida.</span><span class="sxs-lookup"><span data-stu-id="869da-136">If they aren't equal, an error occurs.</span></span> <span data-ttu-id="869da-137">Šią klaidą galite ištaisyti užtikrindami, kad bendroji atsiskaitymo etapų suma būtų lygi eilutės sutarties vertei, kurdami, redaguodami arba naikindami etapus.</span><span class="sxs-lookup"><span data-stu-id="869da-137">You can fix that error by verifying that the billing milestones total the contracted value of the line by either creating, editing, or deleting milestones.</span></span> <span data-ttu-id="869da-138">Atlikę pakeitimus atnaujinkite puslapį.</span><span class="sxs-lookup"><span data-stu-id="869da-138">After the changes are made, refresh the page.</span></span>

### <a name="manually-create-milestones"></a><span data-ttu-id="869da-139">Etapų kūrimas rankiniu būdu</span><span class="sxs-lookup"><span data-stu-id="869da-139">Manually create milestones</span></span>

<span data-ttu-id="869da-140">Fiksuotos kainos etapus galima generuoti rankiniu būdu, kai jie nėra periodiškai išskaidomi.</span><span class="sxs-lookup"><span data-stu-id="869da-140">Fixed price milestones can be generated manually when they aren't periodically split.</span></span> <span data-ttu-id="869da-141">Norėdami sukurti etapą rankiniu būdu, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="869da-141">To create a milestone manually, complete the following steps.</span></span>

1. <span data-ttu-id="869da-142">Atidarykite fiksuotos kainos sutarties eilutę, kurioje norite sukurti etapą.</span><span class="sxs-lookup"><span data-stu-id="869da-142">Open the fixed price contract line on which you want to create a milestone.</span></span> 
2. <span data-ttu-id="869da-143">Skirtuko **Sąskaitų faktūrų grafikas** papildomame tinklelyje pasirinkite **+ Kurti naują sutarties eilutės etapą**.</span><span class="sxs-lookup"><span data-stu-id="869da-143">On the **Invoice Schedule** tab, on the subgrid, select **+ Create new Contract line milestone**.</span></span>
3. <span data-ttu-id="869da-144">Formoje **Etapo kūrimas** įveskite reikiamą informaciją pagal toliau pateiktą lentelę.</span><span class="sxs-lookup"><span data-stu-id="869da-144">On the **Milestone Creation** form, enter the required information based on the following table.</span></span> 

| <span data-ttu-id="869da-145">Laukas</span><span class="sxs-lookup"><span data-stu-id="869da-145">Field</span></span> | <span data-ttu-id="869da-146">Vieta</span><span class="sxs-lookup"><span data-stu-id="869da-146">Location</span></span> | <span data-ttu-id="869da-147">Aprašo</span><span class="sxs-lookup"><span data-stu-id="869da-147">Description</span></span> | <span data-ttu-id="869da-148">Tolesnis poveikis</span><span class="sxs-lookup"><span data-stu-id="869da-148">Downstream impact</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="869da-149">Etapo pavadinimas</span><span class="sxs-lookup"><span data-stu-id="869da-149">Milestone Name</span></span> | <span data-ttu-id="869da-150">Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="869da-150">Quick Create</span></span> | <span data-ttu-id="869da-151">Etapo pavadinimo teksto laukas.</span><span class="sxs-lookup"><span data-stu-id="869da-151">Text field for the name of the milestone.</span></span> | <span data-ttu-id="869da-152">Šis laukas įtrauktas į projekto sutarties eilutės etapą ir sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="869da-152">This field is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="869da-153">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="869da-153">Project Task</span></span> | <span data-ttu-id="869da-154">Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="869da-154">Quick Create</span></span> | <span data-ttu-id="869da-155">Jei etapas yra susietas su projekto užduotimi, naudokite šią nuorodą ir įtraukite pasirinktinę logiką bei nustatykite etapo būseną pagal užduoties būseną.</span><span class="sxs-lookup"><span data-stu-id="869da-155">If the milestone is tied to a project task, use this reference to add custom logic and set the milestone status based on the task status.</span></span> | <span data-ttu-id="869da-156">Ši nuoroda vėliau užduočiai neturės jokios įtakos.</span><span class="sxs-lookup"><span data-stu-id="869da-156">There is no downstream impact of this reference to a task.</span></span> |
| <span data-ttu-id="869da-157">Etapo data</span><span class="sxs-lookup"><span data-stu-id="869da-157">Milestone Date</span></span> | <span data-ttu-id="869da-158">Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="869da-158">Quick Create</span></span> | <span data-ttu-id="869da-159">Data, kai automatinio sąskaitų faktūrų kūrimo procesas turėtų ieškoti šio etapo būsenos, kad jį svarstytų dėl sąskaitų faktūrų išrašymo.</span><span class="sxs-lookup"><span data-stu-id="869da-159">The date on which the automatic invoice creation process should look for the status of this milestone to consider it for invoicing.</span></span> | <span data-ttu-id="869da-160">Tai įtraukta į projekto sutarties eilutės etapą ir sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="869da-160">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="869da-161">Sąskaitos faktūros būsena</span><span class="sxs-lookup"><span data-stu-id="869da-161">Invoice Status</span></span> | <span data-ttu-id="869da-162">Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="869da-162">Quick Create</span></span> | <span data-ttu-id="869da-163">Sukūrus etapą, ši būsena visada nustatoma kaip **Neparengta išrašyti sąskaitos faktūros** arba **Nepradėta**.</span><span class="sxs-lookup"><span data-stu-id="869da-163">When the milestone is created, this status is always set to **Not ready for invoicing** or **Not started**.</span></span> | <span data-ttu-id="869da-164">Tai įtraukta į projekto sutarties eilutės etapą ir sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="869da-164">This is included on the project contract line milestone and the invoice.</span></span> |
| <span data-ttu-id="869da-165">Eilutės suma</span><span class="sxs-lookup"><span data-stu-id="869da-165">Line Amount</span></span> | <span data-ttu-id="869da-166">Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="869da-166">Quick Create</span></span> | <span data-ttu-id="869da-167">Etapo suma ar vertė, kuriai bus išrašyta klientui skirta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="869da-167">The amount or value of the milestone that will be invoiced to the customer.</span></span> | <span data-ttu-id="869da-168">Šis laukas įtrauktas į projekto sutarties eilutės etapą ir sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="869da-168">This field is included on the project contract line milestone and the invoice,</span></span> |
| <span data-ttu-id="869da-169">Mokesčiai</span><span class="sxs-lookup"><span data-stu-id="869da-169">Tax</span></span> | <span data-ttu-id="869da-170">Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="869da-170">Quick Create</span></span> | <span data-ttu-id="869da-171">Etapui taikoma mokesčių suma.</span><span class="sxs-lookup"><span data-stu-id="869da-171">The tax amount applied on the milestone.</span></span> | <span data-ttu-id="869da-172">Tai įtraukta į projekto sutarties eilutės etapą ir sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="869da-172">This is included on the project contract line milestone and the invoice.</span></span> |

4. <span data-ttu-id="869da-173">Pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="869da-173">Select **Save and Close**.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]