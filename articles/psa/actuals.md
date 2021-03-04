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
ms.openlocfilehash: 63ad6544f0ec0a893aebd8d81f3ee895e51c294e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146133"
---
# <a name="actuals-overview"></a><span data-ttu-id="b1c8f-103">Faktinių duomenų apžvalga</span><span class="sxs-lookup"><span data-stu-id="b1c8f-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b1c8f-104">Faktiniai duomenys yra projekto užbaigto darbo kiekis.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="b1c8f-105">Projekto faktinius duomenis galima atsekti jų pirminiuose dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="b1c8f-106">Šie pirminiai dokumentai apima laiko, išlaidų ir žurnalo įrašus, taip pat sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kaip dokumentų faktinius duomenis galima atsekti pirminiuose dokumentuose](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="b1c8f-108">Laiko įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-108">Submitting a time entry</span></span>

<span data-ttu-id="b1c8f-109">Naudojant PSA, kai laiko įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="b1c8f-110">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="b1c8f-111">Kai laiko įrašas pateikiamas projektui, susietam su nustatytos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="b1c8f-112">Numatytųjų kainų įvedimo logika yra žurnalo eilutėje</span><span class="sxs-lookup"><span data-stu-id="b1c8f-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="b1c8f-113">Visos laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="b1c8f-114">Šiuose laukuose nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="b1c8f-115">Dėl laukų, turinčių įtakos numatytosioms kainoms, pvz., **Vaidmuo** ir **Org vienetas**, pagal numatytuosius nustatymus įvedama atitinkama kaina į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="b1c8f-116">Jei į laiko įrašą įtrauksite pasirinktinį lauką ir norite, kad lauko reikšmė būtų dauginama į faktinius duomenis, sukurkite lauką faktinių duomenų objekto lauke ir naudokite lauko susiejimo funkciją, kad nukopijuotumėte lauką iš laiko įrašo į faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="b1c8f-117">Išlaidų įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-117">Submitting an expense entry</span></span>

<span data-ttu-id="b1c8f-118">Naudojant PSA, kai išlaidų įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="b1c8f-119">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="b1c8f-120">Kai išlaidų įrašas pateikiamas projektui, susietam su fiksuotos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="b1c8f-121">Išlaidų numatytųjų kainų įvedimo logika grindžiama išlaidų kategorija, kuri pasirenkama **Išlaidų įvedimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="b1c8f-122">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="b1c8f-123">Tačiau pačioje kainoje suma, kurią vartotojas įvedė, pagal nutylėjimą yra tiesiogiai nukreipiama atitinkamų išlaidų žurnalų kaštų ir pardavimų eilutėse.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="b1c8f-124">Dabartinėje PSA versijoje kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="b1c8f-125">Įrašų žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="b1c8f-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="b1c8f-126">PSA programoje įrašų žurnalai leidžia įrašyti išlaidas arba pajamas medžiagos, mokesčio, laiko, išlaidų arba mokesčių operacijų klasėse.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="b1c8f-127">Žurnale yra antraštė, eilutės ir **Patvirtinti** veiksmas.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="b1c8f-128">Štai keletas scenarijų, kai galite naudoti žurnalą:</span><span class="sxs-lookup"><span data-stu-id="b1c8f-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="b1c8f-129">Turite įrašyti medžiagos projekto faktines išlaidas ir pardavimą.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="b1c8f-130">Transakcijų faktinius duomenis turite perkelti iš kitos sistemos į PSA.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="b1c8f-131">Reikia įrašyti išlaidas, patirtas kitoje sistemoje, pvz., pirkimų arba subrangos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b1c8f-132">Faktinių duomenų kūrimas naudojant įrašų žurnalus turėtų būti atliekamas tik vartotojo, kuris supranta, kaip faktiniai duomenys paveikia apskaitą.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="b1c8f-133">Taip yra todėl, kad programa nepatvirtina žurnalo eilutės tipo arba susijusių kainų, kurios įvedamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="b1c8f-134">Dėl šio žurnalo tipo svarbos atsargiai pasirinkite asmenis, kuriems suteikiama prieiga kurti įrašų žurnalus.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="b1c8f-135">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="b1c8f-135">Recording actuals based on project events</span></span>

<span data-ttu-id="b1c8f-136">PSA registruoja projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="b1c8f-137">Šios operacijos įrašomos kaip **faktiniai duomenys**.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="b1c8f-138">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="b1c8f-139">**Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="b1c8f-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b1c8f-140">Įvykis</span><span class="sxs-lookup"><span data-stu-id="b1c8f-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b1c8f-141">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b1c8f-142">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="b1c8f-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b1c8f-143">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b1c8f-144">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b1c8f-145">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="b1c8f-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b1c8f-146">Faktinės</span><span class="sxs-lookup"><span data-stu-id="b1c8f-146">Actuals</span></span></th>
<th><span data-ttu-id="b1c8f-147">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-147">Transaction currency</span></span></th>
<th><span data-ttu-id="b1c8f-148">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="b1c8f-148">Fixed price</span></span></th>
<th><span data-ttu-id="b1c8f-149">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b1c8f-150">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b1c8f-151">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="b1c8f-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-152">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b1c8f-153">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="b1c8f-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1c8f-154">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b1c8f-155">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-155">Cost actual</span></span></td>
<td><span data-ttu-id="b1c8f-156">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-157">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-158">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="b1c8f-159">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-160">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-161">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b1c8f-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b1c8f-162">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1c8f-163">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b1c8f-164">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-164">Cost actual</span></span></td>
<td><span data-ttu-id="b1c8f-165">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-166">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-167">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-168">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-169">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-170">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="b1c8f-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b1c8f-171">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-172">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b1c8f-173">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1c8f-174">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b1c8f-175">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b1c8f-176">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-177">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-178">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-179">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-180">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-181">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-181">Billed sales</span></span></td>
<td><span data-ttu-id="b1c8f-182">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1c8f-183">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b1c8f-184">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b1c8f-185">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-187">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-188">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-189">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-190">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="b1c8f-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b1c8f-191">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-192">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b1c8f-193">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1c8f-194">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b1c8f-195">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b1c8f-196">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b1c8f-197">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b1c8f-198">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="b1c8f-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b1c8f-199">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-200">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-201">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-202">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-202">Billed sales</span></span></td>
<td><span data-ttu-id="b1c8f-203">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1c8f-204">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b1c8f-205">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b1c8f-206">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-207">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="b1c8f-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b1c8f-208">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-209">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b1c8f-210">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="b1c8f-211">**Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="b1c8f-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="b1c8f-212">Įvykis</span><span class="sxs-lookup"><span data-stu-id="b1c8f-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="b1c8f-213">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="b1c8f-214">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="b1c8f-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="b1c8f-215">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="b1c8f-216">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="b1c8f-217">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="b1c8f-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="b1c8f-218">Faktinės</span><span class="sxs-lookup"><span data-stu-id="b1c8f-218">Actuals</span></span></th>
<th><span data-ttu-id="b1c8f-219">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-219">Transaction currency</span></span></th>
<th><span data-ttu-id="b1c8f-220">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="b1c8f-220">Fixed price</span></span></th>
<th><span data-ttu-id="b1c8f-221">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="b1c8f-222">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="b1c8f-223">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="b1c8f-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-224">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="b1c8f-225">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="b1c8f-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="b1c8f-226">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b1c8f-227">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-227">Cost actual</span></span></td>
<td><span data-ttu-id="b1c8f-228">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b1c8f-229">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b1c8f-230">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="b1c8f-231">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="b1c8f-232">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-233">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b1c8f-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="b1c8f-234">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-235">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="b1c8f-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b1c8f-236">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-237">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b1c8f-238">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="b1c8f-239">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="b1c8f-240">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-240">Cost actual</span></span></td>
<td><span data-ttu-id="b1c8f-241">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-242">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-243">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-244">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-245">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="b1c8f-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-246">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="b1c8f-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="b1c8f-247">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-248">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="b1c8f-249">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="b1c8f-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-250">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="b1c8f-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b1c8f-251">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-252">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b1c8f-253">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1c8f-254">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b1c8f-255">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b1c8f-256">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-257">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-258">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-259">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="b1c8f-260">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-261">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-261">Billed sales</span></span></td>
<td><span data-ttu-id="b1c8f-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1c8f-263">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="b1c8f-264">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="b1c8f-265">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-266">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-267">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-268">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="b1c8f-269">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-270">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="b1c8f-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="b1c8f-271">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-272">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="b1c8f-273">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="b1c8f-274">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b1c8f-275">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b1c8f-276">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="b1c8f-277">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="b1c8f-278">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="b1c8f-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="b1c8f-279">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-280">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="b1c8f-281">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="b1c8f-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-282">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-282">Billed sales</span></span></td>
<td><span data-ttu-id="b1c8f-283">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="b1c8f-284">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="b1c8f-285">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="b1c8f-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="b1c8f-286">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-287">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="b1c8f-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="b1c8f-288">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="b1c8f-289">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="b1c8f-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="b1c8f-290">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="b1c8f-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
