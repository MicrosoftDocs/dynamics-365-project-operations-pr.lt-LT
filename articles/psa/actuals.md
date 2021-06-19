---
title: Faktinių duomenų apžvalga
description: Šioje temoje pateikta informacija apie projekto faktinius duomenis.
author: rumant
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
ms.openlocfilehash: 73f1b14bbb4cc53111a1b3a93756a86db04475ab
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6014666"
---
# <a name="actuals-overview"></a><span data-ttu-id="a2e5c-103">Faktinių duomenų apžvalga</span><span class="sxs-lookup"><span data-stu-id="a2e5c-103">Actuals overview</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a2e5c-104">Faktiniai duomenys yra projekto užbaigto darbo kiekis.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-104">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="a2e5c-105">Projekto faktinius duomenis galima atsekti jų pirminiuose dokumentuose.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-105">Project actuals can be traced back to their source documents.</span></span> <span data-ttu-id="a2e5c-106">Šie pirminiai dokumentai apima laiko, išlaidų ir žurnalo įrašus, taip pat sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-106">Those source documents include time, expense, and journal entries, and also invoices.</span></span>

![Kaip dokumentų faktinius duomenis galima atsekti pirminiuose dokumentuose](media/basic-guide-18.png)

## <a name="submitting-a-time-entry"></a><span data-ttu-id="a2e5c-108">Laiko įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-108">Submitting a time entry</span></span>

<span data-ttu-id="a2e5c-109">Naudojant PSA, kai laiko įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-109">In PSA, when a time entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a2e5c-110">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-110">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a2e5c-111">Kai laiko įrašas pateikiamas projektui, susietam su nustatytos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-111">When a time entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span> 

<span data-ttu-id="a2e5c-112">Numatytųjų kainų įvedimo logika yra žurnalo eilutėje</span><span class="sxs-lookup"><span data-stu-id="a2e5c-112">Logic for entering default prices resides on the journal line.</span></span> <span data-ttu-id="a2e5c-113">Visos laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-113">All the field values from a time entry are copied to the journal line.</span></span> <span data-ttu-id="a2e5c-114">Šiuose laukuose nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-114">These fields include the date of the transaction, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span> 

<span data-ttu-id="a2e5c-115">Dėl laukų, turinčių įtakos numatytosioms kainoms, pvz., **Vaidmuo** ir **Org vienetas**, pagal numatytuosius nustatymus įvedama atitinkama kaina į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-115">The fields that affect default prices, such as **Role** and **Org Unit**, cause an appropriate price to be entered by default on the journal line.</span></span> <span data-ttu-id="a2e5c-116">Jei į laiko įrašą įtrauksite pasirinktinį lauką ir norite, kad lauko reikšmė būtų dauginama į faktinius duomenis, sukurkite lauką faktinių duomenų objekto lauke ir naudokite lauko susiejimo funkciją, kad nukopijuotumėte lauką iš laiko įrašo į faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-116">If you add a custom field on the time entry, and you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="submitting-an-expense-entry"></a><span data-ttu-id="a2e5c-117">Išlaidų įrašo pateikimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-117">Submitting an expense entry</span></span>

<span data-ttu-id="a2e5c-118">Naudojant PSA, kai išlaidų įrašas pateikiamas projektui, susietam su laiko ir medžiagų sutarties eilute, sukuriamos dvi žurnalo eilutės.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-118">In PSA, when an expense entry is submitted for a project that is mapped to a time-and-materials contract line, two journal lines are created.</span></span> <span data-ttu-id="a2e5c-119">Viena eilutė skirta išlaidoms, o kita eilutė skirta neįvardintiems pardavimams.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-119">One line is for cost, and the other line is for unbilled sales.</span></span> <span data-ttu-id="a2e5c-120">Kai išlaidų įrašas pateikiamas projektui, susietam su fiksuotos kainos sutarties eilute, sukuriama žurnalo eilutė tik išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-120">When an expense entry is submitted for a project that is mapped to a fixed-price contract line, a journal line is created only for cost.</span></span>

<span data-ttu-id="a2e5c-121">Išlaidų numatytųjų kainų įvedimo logika grindžiama išlaidų kategorija, kuri pasirenkama **Išlaidų įvedimas** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-121">Logic for entering default prices for expenses is based on the expense category that is selected on the **Expense entry** page.</span></span> <span data-ttu-id="a2e5c-122">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-122">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="a2e5c-123">Tačiau pačioje kainoje suma, kurią vartotojas įvedė, pagal nutylėjimą yra tiesiogiai nukreipiama atitinkamų išlaidų žurnalų kaštų ir pardavimų eilutėse.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-123">However, for the price itself, the amount that the user entered is set directly on the related expense journal lines for cost and sales by default.</span></span>

<span data-ttu-id="a2e5c-124">Dabartinėje PSA versijoje kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-124">In the current version of PSA, category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="using-entry-journals-to-record-costs"></a><span data-ttu-id="a2e5c-125">Įrašų žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="a2e5c-125">Using Entry journals to record costs</span></span>

<span data-ttu-id="a2e5c-126">PSA programoje įrašų žurnalai leidžia įrašyti išlaidas arba pajamas medžiagos, mokesčio, laiko, išlaidų arba mokesčių operacijų klasėse.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-126">In PSA, Entry journals let you record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="a2e5c-127">Žurnale yra antraštė, eilutės ir **Patvirtinti** veiksmas.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-127">A journal has a header, lines, and a **Confirm** action.</span></span> <span data-ttu-id="a2e5c-128">Štai keletas scenarijų, kai galite naudoti žurnalą:</span><span class="sxs-lookup"><span data-stu-id="a2e5c-128">Here are some scenarios where you might use a journal:</span></span>

- <span data-ttu-id="a2e5c-129">Turite įrašyti medžiagos projekto faktines išlaidas ir pardavimą.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-129">You must record material actual costs and sales on a project.</span></span>
- <span data-ttu-id="a2e5c-130">Transakcijų faktinius duomenis turite perkelti iš kitos sistemos į PSA.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-130">You must move transaction actuals from another system to PSA.</span></span>
- <span data-ttu-id="a2e5c-131">Reikia įrašyti išlaidas, patirtas kitoje sistemoje, pvz., pirkimų arba subrangos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-131">You must record costs that occurred in another system, such as procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a2e5c-132">Faktinių duomenų kūrimas naudojant įrašų žurnalus turėtų būti atliekamas tik vartotojo, kuris supranta, kaip faktiniai duomenys paveikia apskaitą.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-132">Using Entry journals to create actuals should be done only by a user who is fully aware of the accounting impact the Actuals have on the project.</span></span> <span data-ttu-id="a2e5c-133">Taip yra todėl, kad programa nepatvirtina žurnalo eilutės tipo arba susijusių kainų, kurios įvedamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-133">This is because the application does not validate the journal line type, or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="a2e5c-134">Dėl šio žurnalo tipo svarbos atsargiai pasirinkite asmenis, kuriems suteikiama prieiga kurti įrašų žurnalus.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-134">Because of the impact of this journal type, exercise adequate caution in who is given access to create Entry journals.</span></span>     


## <a name="recording-actuals-based-on-project-events"></a><span data-ttu-id="a2e5c-135">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="a2e5c-135">Recording actuals based on project events</span></span>

<span data-ttu-id="a2e5c-136">PSA registruoja projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-136">PSA records the financial transactions that occur during a project.</span></span> <span data-ttu-id="a2e5c-137">Šios operacijos įrašomos kaip **faktiniai duomenys**.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-137">These transactions are recorded as **actuals**.</span></span> <span data-ttu-id="a2e5c-138">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-138">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

<span data-ttu-id="a2e5c-139">**Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="a2e5c-139">**The resource belongs to same organizational unit as the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a2e5c-140">Įvykis</span><span class="sxs-lookup"><span data-stu-id="a2e5c-140">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a2e5c-141">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-141">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a2e5c-142">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="a2e5c-142">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a2e5c-143">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-143">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a2e5c-144">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-144">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a2e5c-145">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="a2e5c-145">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a2e5c-146">Faktinės</span><span class="sxs-lookup"><span data-stu-id="a2e5c-146">Actuals</span></span></th>
<th><span data-ttu-id="a2e5c-147">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-147">Transaction currency</span></span></th>
<th><span data-ttu-id="a2e5c-148">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="a2e5c-148">Fixed price</span></span></th>
<th><span data-ttu-id="a2e5c-149">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-149">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a2e5c-150">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-150">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a2e5c-151">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="a2e5c-151">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-152">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-152">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a2e5c-153">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="a2e5c-153">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a2e5c-154">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-154">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a2e5c-155">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-155">Cost actual</span></span></td>
<td><span data-ttu-id="a2e5c-156">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-156">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-157">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-157">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-158">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-158">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="a2e5c-159">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-159">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-160">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-160">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-161">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="a2e5c-161">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a2e5c-162">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-162">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a2e5c-163">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-163">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a2e5c-164">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-164">Cost actual</span></span></td>
<td><span data-ttu-id="a2e5c-165">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-165">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-166">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-166">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-167">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-167">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-168">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-168">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-169">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-169">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-170">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="a2e5c-170">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a2e5c-171">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-171">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-172">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-172">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a2e5c-173">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-173">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a2e5c-174">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-174">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a2e5c-175">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-175">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a2e5c-176">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-176">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-177">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-177">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-178">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-178">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-179">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-179">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-180">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-180">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-181">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-181">Billed sales</span></span></td>
<td><span data-ttu-id="a2e5c-182">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-182">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a2e5c-183">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-183">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a2e5c-184">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-184">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a2e5c-185">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-185">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-186">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-187">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-187">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-188">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-188">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-189">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-189">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-190">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="a2e5c-190">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a2e5c-191">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-191">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-192">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-192">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a2e5c-193">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-193">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a2e5c-194">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-194">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a2e5c-195">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-195">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a2e5c-196">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-196">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a2e5c-197">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-197">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a2e5c-198">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="a2e5c-198">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a2e5c-199">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-199">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-200">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-200">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-201">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-201">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-202">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-202">Billed sales</span></span></td>
<td><span data-ttu-id="a2e5c-203">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-203">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a2e5c-204">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-204">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a2e5c-205">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-205">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a2e5c-206">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-206">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-207">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="a2e5c-207">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a2e5c-208">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-208">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-209">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-209">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a2e5c-210">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-210">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="a2e5c-211">**Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas**</span><span class="sxs-lookup"><span data-stu-id="a2e5c-211">**The resource belongs to an organizational unit that differs from the project's contracting unit**</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="a2e5c-212">Įvykis</span><span class="sxs-lookup"><span data-stu-id="a2e5c-212">Event</span></span></th>
<th colspan="4"><span data-ttu-id="a2e5c-213">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-213">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="a2e5c-214">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="a2e5c-214">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="a2e5c-215">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-215">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="a2e5c-216">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-216">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="a2e5c-217">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="a2e5c-217">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="a2e5c-218">Faktinės</span><span class="sxs-lookup"><span data-stu-id="a2e5c-218">Actuals</span></span></th>
<th><span data-ttu-id="a2e5c-219">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-219">Transaction currency</span></span></th>
<th><span data-ttu-id="a2e5c-220">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="a2e5c-220">Fixed price</span></span></th>
<th><span data-ttu-id="a2e5c-221">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-221">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="a2e5c-222">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-222">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="a2e5c-223">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="a2e5c-223">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-224">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-224">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="a2e5c-225">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="a2e5c-225">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="a2e5c-226">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-226">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a2e5c-227">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-227">Cost actual</span></span></td>
<td><span data-ttu-id="a2e5c-228">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-228">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a2e5c-229">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-229">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a2e5c-230">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-230">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="a2e5c-231">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-231">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="a2e5c-232">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-232">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-233">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="a2e5c-233">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="a2e5c-234">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-235">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="a2e5c-235">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a2e5c-236">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-236">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-237">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-237">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a2e5c-238">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-238">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="a2e5c-239">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-239">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="a2e5c-240">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-240">Cost actual</span></span></td>
<td><span data-ttu-id="a2e5c-241">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-241">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-242">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-242">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-243">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-243">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-244">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-244">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-245">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="a2e5c-245">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-246">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="a2e5c-246">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="a2e5c-247">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-247">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-248">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-248">Interorganizational sales</span></span></td>
<td><span data-ttu-id="a2e5c-249">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="a2e5c-249">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-250">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="a2e5c-250">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a2e5c-251">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-251">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-252">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-252">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a2e5c-253">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-253">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a2e5c-254">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-254">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a2e5c-255">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-255">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a2e5c-256">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-256">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-257">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-257">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-258">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-258">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-259">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-259">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="a2e5c-260">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-260">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-261">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-261">Billed sales</span></span></td>
<td><span data-ttu-id="a2e5c-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-262">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a2e5c-263">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-263">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="a2e5c-264">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-264">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="a2e5c-265">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-265">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-266">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-266">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-267">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-267">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-268">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-268">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="a2e5c-269">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-269">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-270">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="a2e5c-270">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="a2e5c-271">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-271">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-272">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-272">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="a2e5c-273">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-273">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="a2e5c-274">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-274">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a2e5c-275">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-275">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a2e5c-276">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-276">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="a2e5c-277">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-277">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="a2e5c-278">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="a2e5c-278">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="a2e5c-279">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-279">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-280">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-280">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="a2e5c-281">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="a2e5c-281">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-282">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-282">Billed sales</span></span></td>
<td><span data-ttu-id="a2e5c-283">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-283">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="a2e5c-284">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-284">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="a2e5c-285">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="a2e5c-285">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="a2e5c-286">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-286">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-287">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="a2e5c-287">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="a2e5c-288">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-288">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="a2e5c-289">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="a2e5c-289">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="a2e5c-290">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="a2e5c-290">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]