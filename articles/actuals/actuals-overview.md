---
title: Faktiniai duomenys
description: Šioje temoje pateikta informacija, kaip dirbti su faktiniais duomenimis programoje „Microsoft Dynamics 365 Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 93a945ffbe9c6dd998456b506b95e717ab8fbab7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080826"
---
# <a name="actuals"></a><span data-ttu-id="ed71f-103">Faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="ed71f-103">Actuals</span></span> 

<span data-ttu-id="ed71f-104">_**Taikoma:** „Project Operations“, skirtai išteklių / ne atsargomis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="ed71f-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ed71f-105">Faktiniai duomenys yra projekto užbaigto darbo kiekis.</span><span class="sxs-lookup"><span data-stu-id="ed71f-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="ed71f-106">Jie sukuriami pagal laiko ir išlaidų įrašų, žurnalo įrašų ir sąskaitų faktūrų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="ed71f-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="ed71f-107">Žurnalo eilutės ir laiko pateikimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-107">Journal lines and time submission</span></span>

<span data-ttu-id="ed71f-108">Daugiau informacijos apie laiko įrašą žr. [Laiko įrašo apžvalga](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed71f-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ed71f-109">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="ed71f-109">Time and materials</span></span>

<span data-ttu-id="ed71f-110">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="ed71f-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ed71f-111">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-111">Fixed price</span></span>

<span data-ttu-id="ed71f-112">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ed71f-113">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="ed71f-113">Default pricing</span></span>

<span data-ttu-id="ed71f-114">Numatytųjų kainų kūrimo logika yra žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ed71f-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="ed71f-115">Laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="ed71f-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="ed71f-116">Šiose reikšmėse nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="ed71f-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="ed71f-117">Laukai, turintys įtakos numatytąjai kainodarai, pvz., **Vaidmuo** ir **Organizacinis vienetas** , naudojami atitinkamai žurnalo eilutės kainai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="ed71f-117">The fields that affect default pricing, such as **Role** and **Org Unit** , are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="ed71f-118">Į laiko įrašą galite įtraukti pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="ed71f-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="ed71f-119">Jei norite, kad lauko reikšmė būtų perkelta į faktinius duomenis, sukurkite lauką faktinių duomenų objekte ir naudokite lauko susiejimus norėdami kopijuoti lauką iš laiko įrašo į faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="ed71f-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="ed71f-120">Žurnalo eilutės ir pagrindinių išlaidų pateikimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="ed71f-121">Daugiau informacijos apie išlaidų įrašą žr. [Išlaidų apžvalga](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="ed71f-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="ed71f-122">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="ed71f-122">Time and materials</span></span>

<span data-ttu-id="ed71f-123">Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="ed71f-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="ed71f-124">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-124">Fixed price</span></span>

<span data-ttu-id="ed71f-125">Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="ed71f-126">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="ed71f-126">Default pricing</span></span>

<span data-ttu-id="ed71f-127">Numatytųjų išlaidų kainų įvedimo logika priklauso nuo išlaidų kategorijos.</span><span class="sxs-lookup"><span data-stu-id="ed71f-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="ed71f-128">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="ed71f-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="ed71f-129">Tačiau, pagal numatytuosius nustatymus, pačiai kainai įvedama suma yra nustatoma tiesiogiai ant susijusių išlaidų žurnalo eilučių, skirtų savikainai ir pardavimams.</span><span class="sxs-lookup"><span data-stu-id="ed71f-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="ed71f-130">Kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.</span><span class="sxs-lookup"><span data-stu-id="ed71f-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="ed71f-131">Įrašų žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="ed71f-131">Use entry journals to record costs</span></span>

<span data-ttu-id="ed71f-132">Galite naudoti įrašų žurnalus, kad įrašytumėte savikainą ar pajamas medžiagos, mokesčio, laiko, išlaidų ar mokesčių operacijų klasėms.</span><span class="sxs-lookup"><span data-stu-id="ed71f-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="ed71f-133">Žurnalus galima naudoti šiems tikslams:</span><span class="sxs-lookup"><span data-stu-id="ed71f-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="ed71f-134">Įrašyti faktines projekto medžiagų ir pardavimų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="ed71f-135">Perkelti operacijų faktinius duomenis iš kitos sistemos į „Microsoft Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="ed71f-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="ed71f-136">Įrašyti išlaidas, atsiradusias kitoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="ed71f-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="ed71f-137">Šios išlaidos gali apimti viešuosius pirkimus arba subrangos išlaidas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ed71f-138">Programa nepatvirtina žurnalo eilutės tipo arba susijusios kainos, įvestos žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ed71f-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="ed71f-139">Todėl tik vartotojas, gerai žinantis kokį apskaitos poveikį faktiniai duomenys turi projektui, gali naudoti įrašų žurnalus faktiniams duomenis kurti.</span><span class="sxs-lookup"><span data-stu-id="ed71f-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="ed71f-140">Dėl šio žurnalo tipo poveikio reikia atidžiai pasirinkti, kas turi prieigą prie įrašų žurnalų kūrimo.</span><span class="sxs-lookup"><span data-stu-id="ed71f-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="ed71f-141">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="ed71f-141">Record actuals based on project events</span></span>

<span data-ttu-id="ed71f-142">„Project Operations“ įrašo projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="ed71f-143">Šios operacijos įrašomos kaip faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="ed71f-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="ed71f-144">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="ed71f-145">Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="ed71f-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ed71f-146">Įvykis</span><span class="sxs-lookup"><span data-stu-id="ed71f-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ed71f-147">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="ed71f-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ed71f-148">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="ed71f-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ed71f-149">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="ed71f-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ed71f-150">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="ed71f-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ed71f-151">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ed71f-152">Faktinės</span><span class="sxs-lookup"><span data-stu-id="ed71f-152">Actuals</span></span></th>
<th><span data-ttu-id="ed71f-153">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-153">Transaction currency</span></span></th>
<th><span data-ttu-id="ed71f-154">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-154">Fixed price</span></span></th>
<th><span data-ttu-id="ed71f-155">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ed71f-156">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ed71f-157">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="ed71f-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-158">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ed71f-159">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="ed71f-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ed71f-160">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="ed71f-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ed71f-161">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-161">Cost actual</span></span></td>
<td><span data-ttu-id="ed71f-162">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-163">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-164">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="ed71f-165">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-166">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-167">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="ed71f-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ed71f-168">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ed71f-169">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="ed71f-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ed71f-170">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-170">Cost actual</span></span></td>
<td><span data-ttu-id="ed71f-171">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-172">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-173">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-174">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-175">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-176">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="ed71f-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ed71f-177">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-178">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="ed71f-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ed71f-179">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ed71f-180">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="ed71f-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ed71f-181">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ed71f-182">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-183">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="ed71f-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-184">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-185">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-187">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-187">Billed sales</span></span></td>
<td><span data-ttu-id="ed71f-188">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ed71f-189">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="ed71f-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ed71f-190">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ed71f-191">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-192">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-193">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-194">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-195">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-196">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="ed71f-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ed71f-197">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-198">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="ed71f-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ed71f-199">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ed71f-200">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="ed71f-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ed71f-201">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ed71f-202">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ed71f-203">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="ed71f-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ed71f-204">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="ed71f-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ed71f-205">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-206">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-207">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-208">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-208">Billed sales</span></span></td>
<td><span data-ttu-id="ed71f-209">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ed71f-210">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="ed71f-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ed71f-211">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ed71f-212">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-213">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="ed71f-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ed71f-214">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-215">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="ed71f-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ed71f-216">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="ed71f-217">Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="ed71f-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="ed71f-218">Įvykis</span><span class="sxs-lookup"><span data-stu-id="ed71f-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="ed71f-219">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="ed71f-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="ed71f-220">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="ed71f-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="ed71f-221">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="ed71f-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="ed71f-222">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="ed71f-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="ed71f-223">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="ed71f-224">Faktinės</span><span class="sxs-lookup"><span data-stu-id="ed71f-224">Actuals</span></span></th>
<th><span data-ttu-id="ed71f-225">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-225">Transaction currency</span></span></th>
<th><span data-ttu-id="ed71f-226">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-226">Fixed price</span></span></th>
<th><span data-ttu-id="ed71f-227">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="ed71f-228">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="ed71f-229">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="ed71f-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-230">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="ed71f-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="ed71f-231">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="ed71f-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="ed71f-232">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="ed71f-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ed71f-233">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-233">Cost actual</span></span></td>
<td><span data-ttu-id="ed71f-234">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ed71f-235">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ed71f-236">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="ed71f-237">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="ed71f-238">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-239">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="ed71f-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="ed71f-240">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-241">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ed71f-242">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-243">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ed71f-244">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="ed71f-245">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="ed71f-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="ed71f-246">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-246">Cost actual</span></span></td>
<td><span data-ttu-id="ed71f-247">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-248">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-249">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-250">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-251">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="ed71f-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-252">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="ed71f-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="ed71f-253">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-254">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="ed71f-255">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="ed71f-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-256">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="ed71f-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ed71f-257">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-258">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="ed71f-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ed71f-259">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ed71f-260">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="ed71f-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ed71f-261">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ed71f-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-263">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="ed71f-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-264">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-265">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="ed71f-266">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-267">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-267">Billed sales</span></span></td>
<td><span data-ttu-id="ed71f-268">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ed71f-269">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="ed71f-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="ed71f-270">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="ed71f-271">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-272">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-273">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-274">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="ed71f-275">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-276">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="ed71f-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="ed71f-277">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-278">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="ed71f-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="ed71f-279">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="ed71f-280">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="ed71f-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ed71f-281">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ed71f-282">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="ed71f-283">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="ed71f-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="ed71f-284">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="ed71f-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="ed71f-285">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-286">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="ed71f-287">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="ed71f-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-288">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-288">Billed sales</span></span></td>
<td><span data-ttu-id="ed71f-289">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="ed71f-290">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="ed71f-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="ed71f-291">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="ed71f-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="ed71f-292">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-293">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="ed71f-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="ed71f-294">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="ed71f-295">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="ed71f-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="ed71f-296">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="ed71f-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
