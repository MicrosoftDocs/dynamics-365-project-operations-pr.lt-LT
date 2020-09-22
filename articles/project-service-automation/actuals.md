---
title: Faktinės
description: Šioje temoje pateikta informacija apie projekto faktinius duomenis.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 44c6e85f-5b21-4e24-999c-15a2f065d977
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8291e0eb8531e8e9690368675f333c44b6e92e48
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753758"
---
# <a name="actuals"></a><span data-ttu-id="12937-103">Faktinės</span><span class="sxs-lookup"><span data-stu-id="12937-103">Actuals</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="12937-104">Faktiniai duomenys yra projekto užbaigto darbo kiekis.</span><span class="sxs-lookup"><span data-stu-id="12937-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="12937-105">Projekto faktinis duomenis galima atsekti jų pirminiuose dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="12937-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="12937-106">Šie pirminiai dokumentai apima laiko, išlaidų ir žurnalo įrašus, taip pat sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="12937-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kaip dokumentų faktinius duomenis galima atsekti pirminiuose dokumentuose](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="12937-108">Laiko įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="12937-108">Submitting a time entry</span></span>

<span data-ttu-id="12937-109">Naudojant PSA, kai laiko įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="12937-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="12937-110">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="12937-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="12937-111">Kai laiko įrašas pateikiamas projektui, susietam su nustatytos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="12937-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="12937-112">Numatytųjų kainų įvedimo logika yra žurnalo eilutėje</span><span class="sxs-lookup"><span data-stu-id="12937-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="12937-113">Visos laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="12937-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="12937-114">Šiuose laukuose nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="12937-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="12937-115">Dėl laukų, turinčių įtakos numatytosioms kainoms, pvz., **Vaidmuo** ir **Org vienetas**, pagal numatytuosius nustatymus įvedama atitinkama kaina į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="12937-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="12937-116">Jei į laiko įrašą įtrauksite pasirinktinį lauką ir norite, kad lauko reikšmė būtų dauginama į faktinius duomenis, sukurkite lauką faktinių duomenų objekto lauke ir naudokite lauko susiejimo funkciją, kad nukopijuotumėte lauką iš laiko įrašo į faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="12937-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="12937-117">Išlaidų įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="12937-117">Submitting an expense entry</span></span>

<span data-ttu-id="12937-118">Naudojant PSA, kai išlaidų įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="12937-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="12937-119">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="12937-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="12937-120">Kai išlaidų įrašas pateikiamas projektui, susietam su fiksuotos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="12937-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="12937-121">Išlaidų numatytųjų kainų įvedimo logika grindžiama išlaidų kategorija, kuri pasirenkama **Išlaidų įvedimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="12937-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="12937-122">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="12937-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="12937-123">Tačiau pačioje kainoje suma, kurią vartotojas įvedė, pagal nutylėjimą yra tiesiogiai nukreipiama atitinkamų išlaidų žurnalų kaštų ir pardavimų eilutėse.</span><span class="sxs-lookup"><span data-stu-id="12937-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="12937-124">Dabartinėje PSA versijoje kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.</span><span class="sxs-lookup"><span data-stu-id="12937-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-journals-to-record-costs"></a><span data-ttu-id="12937-125">Žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="12937-125">Using journals to record costs</span></span>

<span data-ttu-id="12937-126">PSA programoje žurnalai leidžia įrašyti medžiagos, mokesčio, laiko, išlaidų arba mokesčių operacijų klasėse išlaidas arba pajamas.</span><span class="sxs-lookup"><span data-stu-id="12937-126">In PSA, journals let you record cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="12937-127">Žurnale yra antraštė, eilutės ir **Patvirtinti** veiksmas.</span><span class="sxs-lookup"><span data-stu-id="12937-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="12937-128">Štai keletas scenarijų, kai galite naudoti žurnalą:</span><span class="sxs-lookup"><span data-stu-id="12937-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="12937-129">Turite įrašyti medžiagos projekto faktines išlaidas ir pardavimą.</span><span class="sxs-lookup"><span data-stu-id="12937-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="12937-130">Transakcijų faktinius duomenis turite perkelti iš kitos sistemos į PSA.</span><span class="sxs-lookup"><span data-stu-id="12937-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="12937-131">Reikia įrašyti išlaidas, patirtas kitoje sistemoje, pvz., pirkimų arba subrangos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="12937-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="12937-132">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="12937-132">Recording actuals based on project events</span></span>

<span data-ttu-id="12937-133">PSA registruoja projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="12937-133">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="12937-134">Šios operacijos įrašomos kaip **faktiniai duomenys**.</span><span class="sxs-lookup"><span data-stu-id="12937-134">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="12937-135">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="12937-135">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="12937-136">**Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="12937-136">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="12937-137">Įvykis</span><span class="sxs-lookup"><span data-stu-id="12937-137">Event</span></span></th>
<th colspan="4"><span data-ttu-id="12937-138">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="12937-138">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="12937-139">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="12937-139">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="12937-140">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="12937-140">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="12937-141">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="12937-141">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="12937-142">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="12937-142">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="12937-143">Faktinės</span><span class="sxs-lookup"><span data-stu-id="12937-143">Actuals</span></span></th>
<th><span data-ttu-id="12937-144">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-144">Transaction currency</span></span></th>
<th><span data-ttu-id="12937-145">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="12937-145">Fixed price</span></span></th>
<th><span data-ttu-id="12937-146">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-146">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="12937-147">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="12937-147">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="12937-148">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="12937-148">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-149">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="12937-149">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="12937-150">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="12937-150">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="12937-151">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="12937-151">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="12937-152">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-152">Cost actual</span></span></td>
<td><span data-ttu-id="12937-153">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-153">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-154">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-154">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-155">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-155">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="12937-156">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-156">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-157">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-157">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-158">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="12937-158">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="12937-159">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-159">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="12937-160">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="12937-160">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="12937-161">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-161">Cost actual</span></span></td>
<td><span data-ttu-id="12937-162">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-162">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-163">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-163">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-164">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-164">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-165">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-165">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-166">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-167">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="12937-167">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="12937-168">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-168">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-169">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="12937-169">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="12937-170">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-170">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="12937-171">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="12937-171">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="12937-172">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-172">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="12937-173">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-173">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-174">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="12937-174">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-175">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-175">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-176">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-176">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-177">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-177">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-178">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="12937-178">Billed sales</span></span></td>
<td><span data-ttu-id="12937-179">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="12937-180">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="12937-180">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="12937-181">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="12937-182">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-182">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-183">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-183">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-184">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-184">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-185">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-185">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-187">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="12937-187">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="12937-188">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-188">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-189">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="12937-189">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="12937-190">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="12937-191">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="12937-191">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="12937-192">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-192">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="12937-193">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-193">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="12937-194">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="12937-194">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="12937-195">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="12937-195">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="12937-196">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-196">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-197">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-197">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-198">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-198">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-199">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="12937-199">Billed sales</span></span></td>
<td><span data-ttu-id="12937-200">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-200">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="12937-201">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="12937-201">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="12937-202">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-202">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="12937-203">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-203">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-204">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="12937-204">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="12937-205">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-205">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-206">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="12937-206">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="12937-207">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-207">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="12937-208">**Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="12937-208">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="12937-209">Įvykis</span><span class="sxs-lookup"><span data-stu-id="12937-209">Event</span></span></th>
<th colspan="4"><span data-ttu-id="12937-210">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="12937-210">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="12937-211">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="12937-211">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="12937-212">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="12937-212">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="12937-213">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="12937-213">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="12937-214">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="12937-214">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="12937-215">Faktinės</span><span class="sxs-lookup"><span data-stu-id="12937-215">Actuals</span></span></th>
<th><span data-ttu-id="12937-216">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-216">Transaction currency</span></span></th>
<th><span data-ttu-id="12937-217">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="12937-217">Fixed price</span></span></th>
<th><span data-ttu-id="12937-218">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-218">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="12937-219">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="12937-219">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="12937-220">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="12937-220">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-221">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="12937-221">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="12937-222">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="12937-222">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="12937-223">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="12937-223">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="12937-224">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-224">Cost actual</span></span></td>
<td><span data-ttu-id="12937-225">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-225">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="12937-226">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-226">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="12937-227">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-227">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="12937-228">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-228">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="12937-229">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-229">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-230">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="12937-230">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="12937-231">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-231">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-232">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="12937-232">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="12937-233">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-233">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-234">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="12937-234">Interorganizational sales</span></span></td>
<td><span data-ttu-id="12937-235">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-235">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="12937-236">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="12937-236">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="12937-237">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-237">Cost actual</span></span></td>
<td><span data-ttu-id="12937-238">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-238">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-239">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-239">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-240">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-240">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-241">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-241">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-242">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="12937-242">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-243">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="12937-243">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="12937-244">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-244">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-245">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="12937-245">Interorganizational sales</span></span></td>
<td><span data-ttu-id="12937-246">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="12937-246">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-247">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="12937-247">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="12937-248">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-248">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-249">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="12937-249">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="12937-250">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-250">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="12937-251">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="12937-251">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="12937-252">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-252">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="12937-253">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-253">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-254">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="12937-254">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-255">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-255">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-256">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-256">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="12937-257">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-257">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-258">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="12937-258">Billed sales</span></span></td>
<td><span data-ttu-id="12937-259">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="12937-260">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="12937-260">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="12937-261">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="12937-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-262">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-263">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-263">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-264">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-264">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-265">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-265">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="12937-266">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-267">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="12937-267">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="12937-268">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-268">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-269">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="12937-269">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="12937-270">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-270">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="12937-271">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="12937-271">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="12937-272">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-272">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="12937-273">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-273">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="12937-274">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="12937-274">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="12937-275">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="12937-275">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="12937-276">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-276">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-277">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-277">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="12937-278">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="12937-278">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-279">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="12937-279">Billed sales</span></span></td>
<td><span data-ttu-id="12937-280">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-280">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="12937-281">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="12937-281">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="12937-282">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="12937-282">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="12937-283">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-283">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-284">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="12937-284">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="12937-285">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-285">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="12937-286">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="12937-286">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="12937-287">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="12937-287">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
