---
title: Faktinių duomenų apžvalga
description: Šioje temoje pateikta informacija apie projekto faktinius duomenis.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: c4a3424bed704243dfb5524fa541c3fcc0899e57
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5285628"
---
# <a name="actuals-overview"></a><span data-ttu-id="97635-103">Faktinių duomenų apžvalga</span><span class="sxs-lookup"><span data-stu-id="97635-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="97635-104">Faktiniai duomenys yra projekto užbaigto darbo kiekis.</span><span class="sxs-lookup"><span data-stu-id="97635-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="97635-105">Projekto faktinius duomenis galima atsekti jų pirminiuose dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="97635-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="97635-106">Šie pirminiai dokumentai apima laiko, išlaidų ir žurnalo įrašus, taip pat sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="97635-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kaip dokumentų faktinius duomenis galima atsekti pirminiuose dokumentuose](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="97635-108">Laiko įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="97635-108">Submitting a time entry</span></span>

<span data-ttu-id="97635-109">Naudojant PSA, kai laiko įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="97635-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="97635-110">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="97635-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="97635-111">Kai laiko įrašas pateikiamas projektui, susietam su nustatytos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="97635-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="97635-112">Numatytųjų kainų įvedimo logika yra žurnalo eilutėje</span><span class="sxs-lookup"><span data-stu-id="97635-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="97635-113">Visos laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="97635-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="97635-114">Šiuose laukuose nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="97635-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="97635-115">Dėl laukų, turinčių įtakos numatytosioms kainoms, pvz., **Vaidmuo** ir **Org vienetas**, pagal numatytuosius nustatymus įvedama atitinkama kaina į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="97635-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="97635-116">Jei į laiko įrašą įtrauksite pasirinktinį lauką ir norite, kad lauko reikšmė būtų dauginama į faktinius duomenis, sukurkite lauką faktinių duomenų objekto lauke ir naudokite lauko susiejimo funkciją, kad nukopijuotumėte lauką iš laiko įrašo į faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="97635-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="97635-117">Išlaidų įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="97635-117">Submitting an expense entry</span></span>

<span data-ttu-id="97635-118">Naudojant PSA, kai išlaidų įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="97635-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="97635-119">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="97635-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="97635-120">Kai išlaidų įrašas pateikiamas projektui, susietam su fiksuotos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="97635-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="97635-121">Išlaidų numatytųjų kainų įvedimo logika grindžiama išlaidų kategorija, kuri pasirenkama **Išlaidų įvedimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="97635-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="97635-122">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="97635-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="97635-123">Tačiau pačioje kainoje suma, kurią vartotojas įvedė, pagal nutylėjimą yra tiesiogiai nukreipiama atitinkamų išlaidų žurnalų kaštų ir pardavimų eilutėse.</span><span class="sxs-lookup"><span data-stu-id="97635-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="97635-124">Dabartinėje PSA versijoje kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.</span><span class="sxs-lookup"><span data-stu-id="97635-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="97635-125">Įrašų žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="97635-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="97635-126">PSA programoje įrašų žurnalai leidžia įrašyti išlaidas arba pajamas medžiagos, mokesčio, laiko, išlaidų arba mokesčių operacijų klasėse.</span><span class="sxs-lookup"><span data-stu-id="97635-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="97635-127">Žurnale yra antraštė, eilutės ir **Patvirtinti** veiksmas.</span><span class="sxs-lookup"><span data-stu-id="97635-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="97635-128">Štai keletas scenarijų, kai galite naudoti žurnalą:</span><span class="sxs-lookup"><span data-stu-id="97635-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="97635-129">Turite įrašyti medžiagos projekto faktines išlaidas ir pardavimą.</span><span class="sxs-lookup"><span data-stu-id="97635-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="97635-130">Transakcijų faktinius duomenis turite perkelti iš kitos sistemos į PSA.</span><span class="sxs-lookup"><span data-stu-id="97635-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="97635-131">Reikia įrašyti išlaidas, patirtas kitoje sistemoje, pvz., pirkimų arba subrangos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="97635-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="97635-132">Faktinių duomenų kūrimas naudojant įrašų žurnalus turėtų būti atliekamas tik vartotojo, kuris supranta, kaip faktiniai duomenys paveikia apskaitą.</span><span class="sxs-lookup"><span data-stu-id="97635-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="97635-133">Taip yra todėl, kad programa nepatvirtina žurnalo eilutės tipo arba susijusių kainų, kurios įvedamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="97635-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="97635-134">Dėl šio žurnalo tipo svarbos atsargiai pasirinkite asmenis, kuriems suteikiama prieiga kurti įrašų žurnalus.</span><span class="sxs-lookup"><span data-stu-id="97635-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="97635-135">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="97635-135">Recording actuals based on project events</span></span>

<span data-ttu-id="97635-136">PSA registruoja projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="97635-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="97635-137">Šios operacijos įrašomos kaip **faktiniai duomenys**.</span><span class="sxs-lookup"><span data-stu-id="97635-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="97635-138">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="97635-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="97635-139">**Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="97635-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="97635-140">Įvykis</span><span class="sxs-lookup"><span data-stu-id="97635-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="97635-141">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="97635-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="97635-142">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="97635-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="97635-143">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="97635-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="97635-144">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="97635-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="97635-145">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="97635-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="97635-146">Faktinės</span><span class="sxs-lookup"><span data-stu-id="97635-146">Actuals</span></span></th>
<th><span data-ttu-id="97635-147">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-147">Transaction currency</span></span></th>
<th><span data-ttu-id="97635-148">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="97635-148">Fixed price</span></span></th>
<th><span data-ttu-id="97635-149">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="97635-150">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="97635-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="97635-151">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="97635-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-152">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="97635-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="97635-153">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="97635-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97635-154">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="97635-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="97635-155">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-155">Cost actual</span></span></td>
<td><span data-ttu-id="97635-156">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-157">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-158">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="97635-159">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-160">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-161">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="97635-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="97635-162">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97635-163">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="97635-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="97635-164">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-164">Cost actual</span></span></td>
<td><span data-ttu-id="97635-165">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-166">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-167">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-168">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-169">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-170">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="97635-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="97635-171">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-172">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="97635-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="97635-173">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97635-174">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="97635-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="97635-175">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="97635-176">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-177">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="97635-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-178">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-179">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-180">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-181">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="97635-181">Billed sales</span></span></td>
<td><span data-ttu-id="97635-182">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97635-183">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="97635-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="97635-184">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="97635-185">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-187">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-188">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-189">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-190">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="97635-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="97635-191">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-192">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="97635-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="97635-193">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97635-194">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="97635-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="97635-195">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="97635-196">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="97635-197">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="97635-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="97635-198">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="97635-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="97635-199">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-200">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-201">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-202">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="97635-202">Billed sales</span></span></td>
<td><span data-ttu-id="97635-203">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97635-204">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="97635-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="97635-205">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="97635-206">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-207">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="97635-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="97635-208">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-209">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="97635-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="97635-210">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="97635-211">**Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="97635-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="97635-212">Įvykis</span><span class="sxs-lookup"><span data-stu-id="97635-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="97635-213">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="97635-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="97635-214">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="97635-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="97635-215">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="97635-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="97635-216">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="97635-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="97635-217">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="97635-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="97635-218">Faktinės</span><span class="sxs-lookup"><span data-stu-id="97635-218">Actuals</span></span></th>
<th><span data-ttu-id="97635-219">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-219">Transaction currency</span></span></th>
<th><span data-ttu-id="97635-220">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="97635-220">Fixed price</span></span></th>
<th><span data-ttu-id="97635-221">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="97635-222">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="97635-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="97635-223">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="97635-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-224">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="97635-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="97635-225">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="97635-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="97635-226">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="97635-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="97635-227">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-227">Cost actual</span></span></td>
<td><span data-ttu-id="97635-228">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="97635-229">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="97635-230">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="97635-231">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="97635-232">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-233">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="97635-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="97635-234">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-235">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="97635-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="97635-236">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-237">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="97635-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="97635-238">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="97635-239">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="97635-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="97635-240">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-240">Cost actual</span></span></td>
<td><span data-ttu-id="97635-241">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-242">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-243">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-244">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-245">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="97635-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-246">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="97635-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="97635-247">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-248">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="97635-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="97635-249">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="97635-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-250">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="97635-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="97635-251">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-252">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="97635-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="97635-253">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97635-254">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="97635-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="97635-255">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="97635-256">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-257">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="97635-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-258">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-259">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="97635-260">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-261">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="97635-261">Billed sales</span></span></td>
<td><span data-ttu-id="97635-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97635-263">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="97635-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="97635-264">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="97635-265">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-266">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-267">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-268">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="97635-269">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-270">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="97635-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="97635-271">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-272">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="97635-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="97635-273">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="97635-274">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="97635-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="97635-275">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="97635-276">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="97635-277">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="97635-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="97635-278">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="97635-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="97635-279">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-280">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="97635-281">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="97635-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-282">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="97635-282">Billed sales</span></span></td>
<td><span data-ttu-id="97635-283">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="97635-284">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="97635-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="97635-285">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="97635-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="97635-286">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-287">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="97635-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="97635-288">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="97635-289">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="97635-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="97635-290">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="97635-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]