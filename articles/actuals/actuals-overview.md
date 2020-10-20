---
title: Faktinių duomenų pagrindinis puslapis
description: Šioje temoje pateikta informacija, kaip dirbti su faktiniais duomenimis programoje „Microsoft Dynamics 365 Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 75ad336a995aba3505325466433a5c5e2bb3e776
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907328"
---
# <a name="actuals"></a><span data-ttu-id="f5bce-103">Faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="f5bce-103">Actuals</span></span>

<span data-ttu-id="f5bce-104">_**Taikoma:** „Project Operations“, skirtai išteklių / ne atsargomis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="f5bce-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f5bce-105">Faktiniai duomenys yra projekto užbaigto darbo kiekis.</span><span class="sxs-lookup"><span data-stu-id="f5bce-105">Actuals are the amount of work that has been completed on a project.</span></span> <span data-ttu-id="f5bce-106">Jie sukuriami pagal laiko ir išlaidų įrašų, žurnalo įrašų ir sąskaitų faktūrų rezultatus.</span><span class="sxs-lookup"><span data-stu-id="f5bce-106">They are created as a result of time and expense entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="f5bce-107">Žurnalo eilutės ir laiko pateikimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-107">Journal lines and time submission</span></span>

<span data-ttu-id="f5bce-108">Daugiau informacijos apie laiko įrašą žr. [Laiko įrašo apžvalga](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f5bce-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f5bce-109">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="f5bce-109">Time and materials</span></span>

<span data-ttu-id="f5bce-110">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="f5bce-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f5bce-111">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-111">Fixed price</span></span>

<span data-ttu-id="f5bce-112">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f5bce-113">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="f5bce-113">Default pricing</span></span>

<span data-ttu-id="f5bce-114">Numatytųjų kainų kūrimo logika yra žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f5bce-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="f5bce-115">Laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="f5bce-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="f5bce-116">Šiose reikšmėse nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="f5bce-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="f5bce-117">Laukai, turintys įtakos numatytąjai kainodarai, pvz., **Vaidmuo** ir **Organizacinis vienetas**, naudojami atitinkamai žurnalo eilutės kainai nustatyti.</span><span class="sxs-lookup"><span data-stu-id="f5bce-117">The fields that affect default pricing, such as **Role** and **Org Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="f5bce-118">Į laiko įrašą galite įtraukti pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="f5bce-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="f5bce-119">Jei norite, kad lauko reikšmė būtų perkelta į faktinius duomenis, sukurkite lauką faktinių duomenų objekte ir naudokite lauko susiejimus norėdami kopijuoti lauką iš laiko įrašo į faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="f5bce-119">If you want the field value to be propagated to actuals, create the field on the Actuals entity, and use field mappings to copy the field from the time entry to the actual.</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="f5bce-120">Žurnalo eilutės ir pagrindinių išlaidų pateikimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-120">Journal lines and basic expense submission</span></span>

<span data-ttu-id="f5bce-121">Daugiau informacijos apie išlaidų įrašą žr. [Išlaidų apžvalga](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="f5bce-121">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="f5bce-122">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="f5bce-122">Time and materials</span></span>

<span data-ttu-id="f5bce-123">Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="f5bce-123">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="f5bce-124">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-124">Fixed price</span></span>

<span data-ttu-id="f5bce-125">Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-125">When a basic expense entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="f5bce-126">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="f5bce-126">Default pricing</span></span>

<span data-ttu-id="f5bce-127">Numatytųjų išlaidų kainų įvedimo logika priklauso nuo išlaidų kategorijos.</span><span class="sxs-lookup"><span data-stu-id="f5bce-127">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="f5bce-128">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami, kad nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="f5bce-128">The transaction date, the contract line that the project is mapped to, and the currency are all used to determine the appropriate price list.</span></span> <span data-ttu-id="f5bce-129">Tačiau, pagal numatytuosius nustatymus, pačiai kainai įvedama suma yra nustatoma tiesiogiai ant susijusių išlaidų žurnalo eilučių, skirtų savikainai ir pardavimams.</span><span class="sxs-lookup"><span data-stu-id="f5bce-129">However, by default, the amount that is entered for the price itself is set directly on the related expense journal lines for cost and sales.</span></span>

<span data-ttu-id="f5bce-130">Kategorija paremti numatytųjų vieneto kainų įrašai išlaidų įrašuose negalimi.</span><span class="sxs-lookup"><span data-stu-id="f5bce-130">Category-based entry of per-unit default prices on expense entries isn't available.</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="f5bce-131">Įrašų žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="f5bce-131">Use entry journals to record costs</span></span>

<span data-ttu-id="f5bce-132">Galite naudoti įrašų žurnalus, kad įrašytumėte savikainą ar pajamas medžiagos, mokesčio, laiko, išlaidų ar mokesčių operacijų klasėms.</span><span class="sxs-lookup"><span data-stu-id="f5bce-132">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="f5bce-133">Žurnalus galima naudoti šiems tikslams:</span><span class="sxs-lookup"><span data-stu-id="f5bce-133">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="f5bce-134">Įrašyti faktines projekto medžiagų ir pardavimų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-134">Record the actual cost of materials and sales on a project.</span></span>
- <span data-ttu-id="f5bce-135">Perkelti operacijų faktinius duomenis iš kitos sistemos į „Microsoft Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="f5bce-135">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="f5bce-136">Įrašyti išlaidas, atsiradusias kitoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="f5bce-136">Record costs that occurred in another system.</span></span> <span data-ttu-id="f5bce-137">Šios išlaidos gali apimti viešuosius pirkimus arba subrangos išlaidas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-137">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="f5bce-138">Programa nepatvirtina žurnalo eilutės tipo arba susijusios kainos, įvestos žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f5bce-138">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="f5bce-139">Todėl tik vartotojas, gerai žinantis kokį apskaitos poveikį faktiniai duomenys turi projektui, gali naudoti įrašų žurnalus faktiniams duomenis kurti.</span><span class="sxs-lookup"><span data-stu-id="f5bce-139">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="f5bce-140">Dėl šio žurnalo tipo poveikio reikia atidžiai pasirinkti, kas turi prieigą prie įrašų žurnalų kūrimo.</span><span class="sxs-lookup"><span data-stu-id="f5bce-140">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>
## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="f5bce-141">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="f5bce-141">Record actuals based on project events</span></span>

<span data-ttu-id="f5bce-142">„Project Operations“ įrašo projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-142">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="f5bce-143">Šios operacijos įrašomos kaip faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="f5bce-143">These transactions are recorded as actuals.</span></span> <span data-ttu-id="f5bce-144">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-144">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="f5bce-145">Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="f5bce-145">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f5bce-146">Įvykis</span><span class="sxs-lookup"><span data-stu-id="f5bce-146">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f5bce-147">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="f5bce-147">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f5bce-148">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="f5bce-148">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f5bce-149">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="f5bce-149">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f5bce-150">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="f5bce-150">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f5bce-151">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-151">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f5bce-152">Faktinės</span><span class="sxs-lookup"><span data-stu-id="f5bce-152">Actuals</span></span></th>
<th><span data-ttu-id="f5bce-153">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-153">Transaction currency</span></span></th>
<th><span data-ttu-id="f5bce-154">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-154">Fixed price</span></span></th>
<th><span data-ttu-id="f5bce-155">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-155">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f5bce-156">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-156">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f5bce-157">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="f5bce-157">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-158">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-158">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f5bce-159">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="f5bce-159">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5bce-160">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="f5bce-160">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5bce-161">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-161">Cost actual</span></span></td>
<td><span data-ttu-id="f5bce-162">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-162">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-163">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-163">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-164">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-164">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="f5bce-165">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-165">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-166">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-166">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-167">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="f5bce-167">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f5bce-168">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-168">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5bce-169">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="f5bce-169">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5bce-170">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-170">Cost actual</span></span></td>
<td><span data-ttu-id="f5bce-171">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-171">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-172">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-172">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-173">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-173">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-174">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-174">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-175">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-175">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-176">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="f5bce-176">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5bce-177">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-177">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-178">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="f5bce-178">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5bce-179">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-179">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5bce-180">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="f5bce-180">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5bce-181">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-181">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5bce-182">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-182">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-183">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="f5bce-183">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-184">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-184">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-185">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-185">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-186">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-186">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-187">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-187">Billed sales</span></span></td>
<td><span data-ttu-id="f5bce-188">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-188">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5bce-189">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="f5bce-189">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5bce-190">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-190">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5bce-191">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-191">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-192">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-192">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-193">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-193">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-194">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-194">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-195">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-195">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-196">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="f5bce-196">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5bce-197">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-197">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-198">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="f5bce-198">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5bce-199">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-199">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5bce-200">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="f5bce-200">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5bce-201">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-201">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5bce-202">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-202">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f5bce-203">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="f5bce-203">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f5bce-204">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="f5bce-204">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f5bce-205">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-205">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-206">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-206">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-207">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-207">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-208">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-208">Billed sales</span></span></td>
<td><span data-ttu-id="f5bce-209">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-209">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5bce-210">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="f5bce-210">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5bce-211">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-211">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5bce-212">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-212">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-213">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="f5bce-213">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f5bce-214">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-214">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-215">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="f5bce-215">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5bce-216">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-216">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="f5bce-217">Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="f5bce-217">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="f5bce-218">Įvykis</span><span class="sxs-lookup"><span data-stu-id="f5bce-218">Event</span></span></th>
<th colspan="4"><span data-ttu-id="f5bce-219">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="f5bce-219">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="f5bce-220">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="f5bce-220">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="f5bce-221">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="f5bce-221">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="f5bce-222">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="f5bce-222">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="f5bce-223">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-223">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="f5bce-224">Faktinės</span><span class="sxs-lookup"><span data-stu-id="f5bce-224">Actuals</span></span></th>
<th><span data-ttu-id="f5bce-225">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-225">Transaction currency</span></span></th>
<th><span data-ttu-id="f5bce-226">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-226">Fixed price</span></span></th>
<th><span data-ttu-id="f5bce-227">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-227">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="f5bce-228">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-228">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="f5bce-229">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="f5bce-229">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-230">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="f5bce-230">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="f5bce-231">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="f5bce-231">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="f5bce-232">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="f5bce-232">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5bce-233">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-233">Cost actual</span></span></td>
<td><span data-ttu-id="f5bce-234">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-234">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f5bce-235">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-235">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f5bce-236">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-236">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="f5bce-237">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-237">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="f5bce-238">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-238">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-239">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="f5bce-239">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="f5bce-240">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-240">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-241">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-241">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f5bce-242">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-242">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-243">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-243">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f5bce-244">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-244">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="f5bce-245">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="f5bce-245">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="f5bce-246">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-246">Cost actual</span></span></td>
<td><span data-ttu-id="f5bce-247">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-247">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-248">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-248">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-249">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-249">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-250">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-250">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-251">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="f5bce-251">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-252">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="f5bce-252">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="f5bce-253">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-253">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-254">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-254">Interorganizational sales</span></span></td>
<td><span data-ttu-id="f5bce-255">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="f5bce-255">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-256">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="f5bce-256">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5bce-257">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-257">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-258">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="f5bce-258">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5bce-259">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-259">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5bce-260">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="f5bce-260">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5bce-261">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-261">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5bce-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-262">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-263">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="f5bce-263">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-264">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-264">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-265">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-265">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="f5bce-266">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-266">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-267">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-267">Billed sales</span></span></td>
<td><span data-ttu-id="f5bce-268">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-268">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5bce-269">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="f5bce-269">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="f5bce-270">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-270">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="f5bce-271">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-271">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-272">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-272">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-273">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-273">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-274">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-274">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="f5bce-275">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-275">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-276">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="f5bce-276">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="f5bce-277">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-277">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-278">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="f5bce-278">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5bce-279">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-279">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="f5bce-280">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="f5bce-280">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5bce-281">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-281">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5bce-282">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-282">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="f5bce-283">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="f5bce-283">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="f5bce-284">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="f5bce-284">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="f5bce-285">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-285">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-286">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-286">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="f5bce-287">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="f5bce-287">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-288">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-288">Billed sales</span></span></td>
<td><span data-ttu-id="f5bce-289">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-289">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="f5bce-290">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="f5bce-290">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="f5bce-291">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="f5bce-291">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="f5bce-292">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-292">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-293">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="f5bce-293">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="f5bce-294">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-294">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="f5bce-295">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="f5bce-295">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="f5bce-296">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="f5bce-296">Project contract currency</span></span></td>
</tr>
</tbody>
</table>
