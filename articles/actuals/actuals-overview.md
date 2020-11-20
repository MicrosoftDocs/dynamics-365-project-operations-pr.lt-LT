---
title: Faktiniai duomenys
description: Šioje temoje pateikta informacija, kaip dirbti su faktiniais duomenimis programoje „Microsoft Dynamics 365 Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 13c429763fa805fae5324e4dcf1bf7669e842281
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126320"
---
# <a name="actuals"></a><span data-ttu-id="3c064-103">Faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="3c064-103">Actuals</span></span> 

<span data-ttu-id="3c064-104">_**Taikoma:** „Project Operations“, skirtai išteklių / ne atsargomis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="3c064-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3c064-105">Faktiniai duomenys yra projekto užbaigto darbo kiekis.</span><span class="sxs-lookup"><span data-stu-id="3c064-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="3c064-106">Jie sukuriami pagal laiko ir išlaidų įrašų, žurnalo įrašų ir sąskaitų faktūrų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="3c064-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="3c064-107">Žurnalo eilutės ir laiko pateikimas</span><span class="sxs-lookup"><span data-stu-id="3c064-107">Journal lines and time submission</span></span>

<span data-ttu-id="3c064-108">Daugiau informacijos apie laiko įrašą žr. [Laiko įrašo apžvalga](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3c064-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3c064-109">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="3c064-109">Time and materials</span></span>

<span data-ttu-id="3c064-110">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="3c064-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3c064-111">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="3c064-111">Fixed price</span></span>

<span data-ttu-id="3c064-112">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="3c064-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3c064-113">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="3c064-113">Default pricing</span></span>

<span data-ttu-id="3c064-114">Numatytųjų kainų kūrimo logika yra žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3c064-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="3c064-115">Laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="3c064-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="3c064-116">Šiose reikšmėse nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="3c064-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="3c064-117">Laukai, turintys įtakos numatytąjai kainodarai, pvz., **Vaidmuo** ir **Organizacinis vienetas**, naudojami atitinkamai žurnalo eilutės kainai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="3c064-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="3c064-118">Į laiko įrašą galite įtraukti pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="3c064-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="3c064-119">Jei norite, kad lauko reikšmė būtų perkelta į faktinius duomenis, sukurkite lauką faktinių duomenų objekte ir naudokite lauko susiejimus norėdami kopijuoti lauką iš laiko įrašo į faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="3c064-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="3c064-120">Žurnalo eilutės ir pagrindinių išlaidų pateikimas</span><span class="sxs-lookup"><span data-stu-id="3c064-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="3c064-121">Daugiau informacijos apie išlaidų įrašą žr. [Išlaidų apžvalga](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="3c064-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="3c064-122">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="3c064-122">Time and materials</span></span>

<span data-ttu-id="3c064-123">Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="3c064-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="3c064-124">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="3c064-124">Fixed price</span></span>

<span data-ttu-id="3c064-125">Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="3c064-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="3c064-126">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="3c064-126">Default pricing</span></span>

<span data-ttu-id="3c064-127">Numatytųjų išlaidų kainų įvedimo logika priklauso nuo išlaidų kategorijos.</span><span class="sxs-lookup"><span data-stu-id="3c064-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="3c064-128">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="3c064-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="3c064-129">Tačiau, pagal numatytuosius nustatymus, pačiai kainai įvedama suma yra nustatoma tiesiogiai ant susijusių išlaidų žurnalo eilučių, skirtų savikainai ir pardavimams.</span><span class="sxs-lookup"><span data-stu-id="3c064-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="3c064-130">Kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.</span><span class="sxs-lookup"><span data-stu-id="3c064-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="3c064-131">Įrašų žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="3c064-131">Use entry journals to record costs</span></span>

<span data-ttu-id="3c064-132">Galite naudoti įrašų žurnalus, kad įrašytumėte savikainą ar pajamas medžiagos, mokesčio, laiko, išlaidų ar mokesčių operacijų klasėms.</span><span class="sxs-lookup"><span data-stu-id="3c064-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="3c064-133">Žurnalus galima naudoti šiems tikslams:</span><span class="sxs-lookup"><span data-stu-id="3c064-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="3c064-134">Įrašyti faktines projekto medžiagų ir pardavimų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="3c064-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="3c064-135">Perkelti operacijų faktinius duomenis iš kitos sistemos į „Microsoft Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="3c064-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="3c064-136">Įrašyti išlaidas, atsiradusias kitoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="3c064-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="3c064-137">Šios išlaidos gali apimti viešuosius pirkimus arba subrangos išlaidas.</span><span class="sxs-lookup"><span data-stu-id="3c064-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3c064-138">Programa nepatvirtina žurnalo eilutės tipo arba susijusios kainos, įvestos žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3c064-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="3c064-139">Todėl tik vartotojas, gerai žinantis kokį apskaitos poveikį faktiniai duomenys turi projektui, gali naudoti įrašų žurnalus faktiniams duomenis kurti.</span><span class="sxs-lookup"><span data-stu-id="3c064-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="3c064-140">Dėl šio žurnalo tipo poveikio reikia atidžiai pasirinkti, kas turi prieigą prie įrašų žurnalų kūrimo.</span><span class="sxs-lookup"><span data-stu-id="3c064-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="3c064-141">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="3c064-141">Record actuals based on project events</span></span>

<span data-ttu-id="3c064-142">„Project Operations“ įrašo projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="3c064-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="3c064-143">Šios operacijos įrašomos kaip faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="3c064-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="3c064-144">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="3c064-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="3c064-145">Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="3c064-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3c064-146">Įvykis</span><span class="sxs-lookup"><span data-stu-id="3c064-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3c064-147">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="3c064-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3c064-148">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="3c064-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3c064-149">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="3c064-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3c064-150">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="3c064-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3c064-151">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="3c064-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3c064-152">Faktinės</span><span class="sxs-lookup"><span data-stu-id="3c064-152">Actuals</span></span></th>
<th><span data-ttu-id="3c064-153">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-153">Transaction currency</span></span></th>
<th><span data-ttu-id="3c064-154">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="3c064-154">Fixed price</span></span></th>
<th><span data-ttu-id="3c064-155">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c064-156">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="3c064-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3c064-157">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="3c064-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-158">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="3c064-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3c064-159">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="3c064-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c064-160">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="3c064-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c064-161">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-161">Cost actual</span></span></td>
<td><span data-ttu-id="3c064-162">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-163">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-164">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="3c064-165">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-166">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-167">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="3c064-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3c064-168">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c064-169">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="3c064-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c064-170">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-170">Cost actual</span></span></td>
<td><span data-ttu-id="3c064-171">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-172">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-173">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-174">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-175">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-176">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="3c064-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c064-177">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-178">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="3c064-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c064-179">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c064-180">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="3c064-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c064-181">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c064-182">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-183">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="3c064-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-184">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-185">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-187">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="3c064-187">Billed sales</span></span></td>
<td><span data-ttu-id="3c064-188">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c064-189">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="3c064-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c064-190">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c064-191">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-192">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-193">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-194">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-195">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-196">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="3c064-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c064-197">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-198">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="3c064-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c064-199">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c064-200">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="3c064-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c064-201">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c064-202">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3c064-203">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="3c064-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3c064-204">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="3c064-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3c064-205">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-206">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-207">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-208">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="3c064-208">Billed sales</span></span></td>
<td><span data-ttu-id="3c064-209">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c064-210">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="3c064-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c064-211">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c064-212">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-213">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="3c064-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3c064-214">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-215">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="3c064-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c064-216">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="3c064-217">Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="3c064-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="3c064-218">Įvykis</span><span class="sxs-lookup"><span data-stu-id="3c064-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="3c064-219">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="3c064-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="3c064-220">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="3c064-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="3c064-221">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="3c064-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="3c064-222">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="3c064-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="3c064-223">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="3c064-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="3c064-224">Faktinės</span><span class="sxs-lookup"><span data-stu-id="3c064-224">Actuals</span></span></th>
<th><span data-ttu-id="3c064-225">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-225">Transaction currency</span></span></th>
<th><span data-ttu-id="3c064-226">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="3c064-226">Fixed price</span></span></th>
<th><span data-ttu-id="3c064-227">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="3c064-228">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="3c064-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="3c064-229">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="3c064-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-230">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="3c064-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="3c064-231">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="3c064-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="3c064-232">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="3c064-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c064-233">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-233">Cost actual</span></span></td>
<td><span data-ttu-id="3c064-234">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3c064-235">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3c064-236">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="3c064-237">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="3c064-238">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-239">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="3c064-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="3c064-240">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-241">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="3c064-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3c064-242">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-243">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="3c064-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3c064-244">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="3c064-245">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="3c064-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="3c064-246">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-246">Cost actual</span></span></td>
<td><span data-ttu-id="3c064-247">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-248">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-249">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-250">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-251">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="3c064-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-252">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="3c064-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="3c064-253">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-254">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="3c064-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="3c064-255">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="3c064-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-256">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="3c064-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c064-257">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-258">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="3c064-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c064-259">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c064-260">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="3c064-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c064-261">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c064-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-263">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="3c064-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-264">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-265">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="3c064-266">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-267">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="3c064-267">Billed sales</span></span></td>
<td><span data-ttu-id="3c064-268">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c064-269">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="3c064-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="3c064-270">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="3c064-271">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-272">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-273">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-274">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="3c064-275">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-276">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="3c064-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="3c064-277">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-278">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="3c064-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c064-279">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="3c064-280">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="3c064-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c064-281">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c064-282">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="3c064-283">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="3c064-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="3c064-284">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="3c064-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="3c064-285">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-286">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="3c064-287">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="3c064-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-288">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="3c064-288">Billed sales</span></span></td>
<td><span data-ttu-id="3c064-289">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="3c064-290">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="3c064-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="3c064-291">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="3c064-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="3c064-292">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-293">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="3c064-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="3c064-294">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="3c064-295">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="3c064-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="3c064-296">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="3c064-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
