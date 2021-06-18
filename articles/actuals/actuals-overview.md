---
title: Faktiniai duomenys
description: Šioje temoje pateikiama informacija apie tai, kaip dirbti su faktiniais duomenimis programoje „Microsoft Dynamics 365 Project Operations“.
author: rumant
ms.date: 04/01/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 78c7a9486d0338adfd7770447f21d17509e654f7
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996621"
---
# <a name="actuals"></a><span data-ttu-id="21c63-103">Faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="21c63-103">Actuals</span></span> 

<span data-ttu-id="21c63-104">_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_</span><span class="sxs-lookup"><span data-stu-id="21c63-104">_**Applies to:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="21c63-105">Faktinių duomenų srityje pateikiama projekto peržiūrėta ir patvirtinta finansinė bei grafiko eiga.</span><span class="sxs-lookup"><span data-stu-id="21c63-105">Actuals represent the reviewed and approved financial and schedule progress on a project.</span></span> <span data-ttu-id="21c63-106">Jie kuriami patvirtinus laiką, išlaidas, medžiagos naudojimo įrašus, žurnalų įrašus ir sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="21c63-106">They are created as a result of approval of time, expense, material usage entries, and journal entries and invoices.</span></span>

## <a name="journal-lines-and-time-submission"></a><span data-ttu-id="21c63-107">Žurnalo eilutės ir laiko pateikimas</span><span class="sxs-lookup"><span data-stu-id="21c63-107">Journal lines and time submission</span></span>

<span data-ttu-id="21c63-108">Daugiau informacijos apie laiko įrašą žr. [Laiko įrašo apžvalga](../time/time-entry-overview.md).</span><span class="sxs-lookup"><span data-stu-id="21c63-108">For more information about time entry, see [Time entry overview](../time/time-entry-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="21c63-109">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="21c63-109">Time and materials</span></span>

<span data-ttu-id="21c63-110">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="21c63-110">When a time entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="21c63-111">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="21c63-111">Fixed price</span></span>

<span data-ttu-id="21c63-112">Kai teikiamas laiko įrašas susiejamas su projektu, kuris susietas su fiksuotos kainos sutarties eilute, sistema sukuria vieną žurnalo eilutę už sąnaudas.</span><span class="sxs-lookup"><span data-stu-id="21c63-112">When a time entry that is submitted is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="21c63-113">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="21c63-113">Default pricing</span></span>

<span data-ttu-id="21c63-114">Numatytųjų kainų kūrimo logika yra žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="21c63-114">The logic for creating default prices resides on the journal line.</span></span> <span data-ttu-id="21c63-115">Laiko įrašo lauko reikšmės kopijuojamos į žurnalo eilutę.</span><span class="sxs-lookup"><span data-stu-id="21c63-115">The field values from the time entry are copied to the journal line.</span></span> <span data-ttu-id="21c63-116">Šiose reikšmėse nurodoma operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta iš atitinkamo kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="21c63-116">These values include the transaction date, the contract line that the project is mapped to, and the currency result in the appropriate price list.</span></span>

<span data-ttu-id="21c63-117">Laukai, turintys įtakos numatytajai kainodarai, pvz., **Vaidmuo** ir **Išteklių paskirstymo vienetas**, naudojami norint nustatyti atitinkamą kainą žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="21c63-117">The fields that affect default pricing, such as **Role** and **Resourcing Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="21c63-118">Į laiko įrašą galite įtraukti pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="21c63-118">You can add a custom field on the time entry.</span></span> <span data-ttu-id="21c63-119">Jei norite, kad lauko reikšmė būtų užpildoma faktiniais duomenimis, sukurkite lauką lentelėse **Faktiniai duomenys** ir **Žurnalo eilutė**.</span><span class="sxs-lookup"><span data-stu-id="21c63-119">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="21c63-120">Naudokite pasirinktinį kodą ir užpildykite pasirinktą faktinių duomenų laiko įrašą per žurnalo eilutę naudodami operacijos kilmę.</span><span class="sxs-lookup"><span data-stu-id="21c63-120">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="21c63-121">Norėdami gauti daugiau informacijos apie operacijų kilmę ir ryšius, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="21c63-121">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-basic-expense-submission"></a><span data-ttu-id="21c63-122">Žurnalo eilutės ir pagrindinių išlaidų pateikimas</span><span class="sxs-lookup"><span data-stu-id="21c63-122">Journal lines and basic expense submission</span></span>

<span data-ttu-id="21c63-123">Daugiau informacijos apie išlaidų įrašą žr. [Išlaidų apžvalga](../expense/expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="21c63-123">For more information about expense entry, see [Expense overview](../expense/expense-overview.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="21c63-124">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="21c63-124">Time and materials</span></span>

<span data-ttu-id="21c63-125">Kai teikiamas pagrindinių išlaidų įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistema sukuria dvi žurnalo eilutes – vieną už sąnaudas, o kitą už pardavimą, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="21c63-125">When a basic expense entry that is submitted is linked to a project that is mapped to a time-and-materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="21c63-126">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="21c63-126">Fixed price</span></span>

<span data-ttu-id="21c63-127">Kai pateiktas pagrindinis išlaidų įrašas susiejamas su projektu, susietu su fiksuotos kainos sutarties eilute, sistemoje sukuriama viena žurnalo eilutė išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="21c63-127">When a submitted basic expense entry is linked to a project that's mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="21c63-128">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="21c63-128">Default pricing</span></span>

<span data-ttu-id="21c63-129">Numatytųjų išlaidų kainų įvedimo logika priklauso nuo išlaidų kategorijos.</span><span class="sxs-lookup"><span data-stu-id="21c63-129">The logic for entering default prices for expenses is based on the expense category.</span></span> <span data-ttu-id="21c63-130">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami norint nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="21c63-130">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="21c63-131">Laukai, turintys įtakos numatytajai kainodarai, pvz., **Operacijos kategorija** ir **Vienetas**, naudojami norint nustatyti atitinkamą kainą žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="21c63-131">The fields that affect default pricing, such as **Transaction Category** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="21c63-132">Tačiau tai pasitarnauja tik tada, kai kainodaros būdas kainoraštyje yra **Vieneto kaina**.</span><span class="sxs-lookup"><span data-stu-id="21c63-132">However, this only works when the pricing method in the price list is **Price per unit**.</span></span> <span data-ttu-id="21c63-133">Jei kainodaros būdas yra **Savikaina** arba **Antkainis prie savikainos**, kaina, įvedama sukūrus išlaidų įrašą, naudojama savikainai, o kaina pardavimo žurnalo eilutėje apskaičiuojama pagal kainodaros būdą.</span><span class="sxs-lookup"><span data-stu-id="21c63-133">If pricing method is **At cost** or **Markup over cost**, the price entered when the expense entry is created is used for cost and the price on the sales journal line is calculated based on the pricing method.</span></span> 

<span data-ttu-id="21c63-134">Išlaidų įrašo dalyje galite įtraukti pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="21c63-134">You can add a custom field on the expense entry.</span></span> <span data-ttu-id="21c63-135">Jei norite, kad lauko reikšmė būtų užpildoma faktiniais duomenimis, sukurkite lauką lentelėse **Faktiniai duomenys** ir **Žurnalo eilutė**.</span><span class="sxs-lookup"><span data-stu-id="21c63-135">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="21c63-136">Naudokite pasirinktinį kodą ir užpildykite pasirinktą faktinių duomenų laiko įrašą per žurnalo eilutę naudodami operacijos kilmę.</span><span class="sxs-lookup"><span data-stu-id="21c63-136">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="21c63-137">Norėdami gauti daugiau informacijos apie operacijų kilmę ir ryšius, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="21c63-137">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="journal-lines-and-material-usage-log-submission"></a><span data-ttu-id="21c63-138">Žurnalo eilutės ir medžiagos naudojimo žurnalo pateikimas</span><span class="sxs-lookup"><span data-stu-id="21c63-138">Journal lines and material usage log submission</span></span>

<span data-ttu-id="21c63-139">Daugiau informacijos apie išlaidų įrašą žr. [Medžiagos naudojimo žurnalas](../material/material-usage-log.md).</span><span class="sxs-lookup"><span data-stu-id="21c63-139">For more information about expense entry, see [Material Usage Log](../material/material-usage-log.md).</span></span>

### <a name="time-and-materials"></a><span data-ttu-id="21c63-140">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="21c63-140">Time and materials</span></span>

<span data-ttu-id="21c63-141">Kai pateiktas medžiagos naudojimo žurnalo įrašas susiejamas su projektu, kuris susietas su laiko ir medžiagos sutarties eilute, sistemoje sukuriamos dvi žurnalo eilutės – viena išlaidoms, o kita – pardavimui, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="21c63-141">When a submitted material usage log entry is linked to a project that is mapped to a time and materials contract line, the system creates two journal lines, one for cost and one for unbilled sales.</span></span>

### <a name="fixed-price"></a><span data-ttu-id="21c63-142">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="21c63-142">Fixed price</span></span>

<span data-ttu-id="21c63-143">Kai pateiktas medžiagos naudojimo žurnalo įrašas susiejamas su projektu, susietu su fiksuotos kainos sutarties eilute, sistemoje sukuriama viena žurnalo eilutė išlaidoms.</span><span class="sxs-lookup"><span data-stu-id="21c63-143">When a submitted material usage log entry is linked to a project that is mapped to a fixed-price contract line, the system creates one journal line for cost.</span></span>

### <a name="default-pricing"></a><span data-ttu-id="21c63-144">Numatytoji kainodara</span><span class="sxs-lookup"><span data-stu-id="21c63-144">Default pricing</span></span>

<span data-ttu-id="21c63-145">Medžiagos numatytųjų kainų įvedimo logika pagrįsta produkto ir vieneto deriniu.</span><span class="sxs-lookup"><span data-stu-id="21c63-145">The logic for entering default prices for material is based on the product and unit combination.</span></span> <span data-ttu-id="21c63-146">Operacijos data, sutarties eilutė, su kuria susietas projektas, ir valiuta kartu naudojami norint nustatyti atitinkamą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="21c63-146">The transaction date, the contract line that the project is mapped to, and the currency, are all used to determine the appropriate price list.</span></span> <span data-ttu-id="21c63-147">Laukai, turintys įtakos numatytajai kainodarai, pvz., **Produkto ID** ir **Vienetas**, naudojami norint nustatyti atitinkamą kainą žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="21c63-147">The fields that affect default pricing, such as **Product ID** and **Unit**, are used to determine the appropriate price on the journal line.</span></span> <span data-ttu-id="21c63-148">Tačiau tai pasitarnauja tik katalogo produktų atveju.</span><span class="sxs-lookup"><span data-stu-id="21c63-148">However, this only works for catalog products.</span></span> <span data-ttu-id="21c63-149">Įtraukiamųjų produktų atveju, kaina, įvesta sukūrus medžiagos naudojimo žurnalo įrašą, naudojama išlaidoms ir pardavimo kainai žurnalo eilutėse įvesti.</span><span class="sxs-lookup"><span data-stu-id="21c63-149">For write-in products, the price entered when the material usage log entry is created is used for cost and sales price on the journal lines.</span></span> 

<span data-ttu-id="21c63-150">Išlaidų įrašo dalyje **Medžiagos naudojimo žurnalas** galite įtraukti pasirinktinį lauką.</span><span class="sxs-lookup"><span data-stu-id="21c63-150">You can add a custom field on the **Material Usage Log** entry.</span></span> <span data-ttu-id="21c63-151">Jei norite, kad lauko reikšmė būtų užpildoma faktiniais duomenimis, sukurkite lauką lentelėse **Faktiniai duomenys** ir **Žurnalo eilutė**.</span><span class="sxs-lookup"><span data-stu-id="21c63-151">If you want the field value to be propagated to actuals, create the field in the **Actuals** and **Journal Line** tables.</span></span> <span data-ttu-id="21c63-152">Naudokite pasirinktinį kodą ir užpildykite pasirinktą faktinių duomenų laiko įrašą per žurnalo eilutę naudodami operacijos kilmę.</span><span class="sxs-lookup"><span data-stu-id="21c63-152">Use custom code to propagate the selected field value from Time Entry to Actuals through the journal line using transaction origins.</span></span> <span data-ttu-id="21c63-153">Norėdami gauti daugiau informacijos apie operacijų kilmę ir ryšius, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span><span class="sxs-lookup"><span data-stu-id="21c63-153">For more information about transaction origins and connections, see [Linking Actuals to original records](linkingactuals.md#example-how-transaction-origin-works-with-transaction-connection).</span></span>

## <a name="use-entry-journals-to-record-costs"></a><span data-ttu-id="21c63-154">Įrašų žurnalų naudojimas išlaidoms įrašyti</span><span class="sxs-lookup"><span data-stu-id="21c63-154">Use entry journals to record costs</span></span>

<span data-ttu-id="21c63-155">Galite naudoti įrašų žurnalus, kad įrašytumėte savikainą ar pajamas medžiagos, mokesčio, laiko, išlaidų ar mokesčių operacijų klasėms.</span><span class="sxs-lookup"><span data-stu-id="21c63-155">You can use entry journals to record the cost or revenue in the material, fee, time, expense, or tax transaction classes.</span></span> <span data-ttu-id="21c63-156">Žurnalus galima naudoti šiems tikslams:</span><span class="sxs-lookup"><span data-stu-id="21c63-156">Journals can be used for the following purposes:</span></span>

- <span data-ttu-id="21c63-157">Operacijų faktinius duomenis perkelkite iš kitos sistemos į „Microsoft Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="21c63-157">Move transaction actuals from another system to Microsoft Dynamics 365 Project Operations.</span></span>
- <span data-ttu-id="21c63-158">Įrašyti išlaidas, atsiradusias kitoje sistemoje.</span><span class="sxs-lookup"><span data-stu-id="21c63-158">Record costs that occurred in another system.</span></span> <span data-ttu-id="21c63-159">Šios išlaidos gali apimti viešuosius pirkimus arba subrangos išlaidas.</span><span class="sxs-lookup"><span data-stu-id="21c63-159">These costs can include procurement or subcontracting costs.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="21c63-160">Programa nepatvirtina žurnalo eilutės tipo arba susijusios kainos, įvestos žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="21c63-160">The application doesn't validate the journal line type or the related pricing that is entered on the journal line.</span></span> <span data-ttu-id="21c63-161">Todėl tik vartotojas, gerai žinantis kokį apskaitos poveikį faktiniai duomenys turi projektui, gali naudoti įrašų žurnalus faktiniams duomenis kurti.</span><span class="sxs-lookup"><span data-stu-id="21c63-161">Therefore, only a user who is fully aware of the accounting impact that actuals have on the project should use entry journals to create actuals.</span></span> <span data-ttu-id="21c63-162">Dėl šio žurnalo tipo poveikio reikia atidžiai pasirinkti, kas turi prieigą prie įrašų žurnalų kūrimo.</span><span class="sxs-lookup"><span data-stu-id="21c63-162">Because of the impact of this journal type, you should carefully choose who has access to create entry journals.</span></span>

## <a name="record-actuals-based-on-project-events"></a><span data-ttu-id="21c63-163">Faktinių duomenų įrašymas pagal projekto įvykius</span><span class="sxs-lookup"><span data-stu-id="21c63-163">Record actuals based on project events</span></span>

<span data-ttu-id="21c63-164">„Project Operations“ įrašo projekto metu vykdomas finansines operacijas.</span><span class="sxs-lookup"><span data-stu-id="21c63-164">Project Operations records the financial transactions that occur during a project.</span></span> <span data-ttu-id="21c63-165">Šios operacijos įrašomos kaip faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="21c63-165">These transactions are recorded as actuals.</span></span> <span data-ttu-id="21c63-166">Toliau pateikiamose lentelėse rodomi skirtingi faktinių duomenų tipai, kurie sukuriami, atsižvelgiant į tai, ar projektas yra laiko ir medžiagų, ar fiksuotos kainos projektas, yra paruošiamųjų darbų prieš parduodant etape, arba yra vidinis projektas.</span><span class="sxs-lookup"><span data-stu-id="21c63-166">The following tables show the different types of actuals that are created, depending on whether the project is a time-and-materials or fixed-price project, is in the presales stage, or is an internal project.</span></span>

### <a name="the-resource-belongs-to-same-organizational-unit-as-the-projects-contracting-unit"></a><span data-ttu-id="21c63-167">Ištekliai priklauso tam pačiam organizaciniam vienetui kaip ir projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="21c63-167">The resource belongs to same organizational unit as the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="21c63-168">Įvykis</span><span class="sxs-lookup"><span data-stu-id="21c63-168">Event</span></span></th>
<th colspan="4"><span data-ttu-id="21c63-169">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="21c63-169">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="21c63-170">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="21c63-170">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="21c63-171">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="21c63-171">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="21c63-172">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="21c63-172">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="21c63-173">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="21c63-173">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="21c63-174">Faktinės</span><span class="sxs-lookup"><span data-stu-id="21c63-174">Actuals</span></span></th>
<th><span data-ttu-id="21c63-175">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-175">Transaction currency</span></span></th>
<th><span data-ttu-id="21c63-176">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="21c63-176">Fixed price</span></span></th>
<th><span data-ttu-id="21c63-177">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-177">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="21c63-178">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="21c63-178">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="21c63-179">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="21c63-179">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-180">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="21c63-180">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="21c63-181">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="21c63-181">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21c63-182">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="21c63-182">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21c63-183">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-183">Cost actual</span></span></td>
<td><span data-ttu-id="21c63-184">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-184">Contracting unit currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-185">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-185">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-186">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-186">Contracting unit currency</span></span>
<td rowspan="2"><span data-ttu-id="21c63-187">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-187">Cost actual</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-188">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-188">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-189">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="21c63-189">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="21c63-190">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-190">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21c63-191">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="21c63-191">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21c63-192">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-192">Cost actual</span></span></td>
<td><span data-ttu-id="21c63-193">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-193">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-194">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-194">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-195">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-195">Contracting unit currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-196">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-196">Cost actual</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-197">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-197">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-198">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="21c63-198">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21c63-199">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-199">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-200">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="21c63-200">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21c63-201">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-201">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21c63-202">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="21c63-202">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21c63-203">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-203">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21c63-204">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-204">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-205">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="21c63-205">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-206">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-206">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-207">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-207">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-208">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-208">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-209">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="21c63-209">Billed sales</span></span></td>
<td><span data-ttu-id="21c63-210">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-210">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21c63-211">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="21c63-211">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21c63-212">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-212">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21c63-213">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-213">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-214">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-214">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-215">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-215">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-216">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-216">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-217">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-217">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-218">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="21c63-218">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21c63-219">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-219">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-220">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="21c63-220">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21c63-221">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-221">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21c63-222">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="21c63-222">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21c63-223">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-223">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21c63-224">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-224">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="21c63-225">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="21c63-225">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="21c63-226">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="21c63-226">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="21c63-227">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-227">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-228">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-228">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-229">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-229">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-230">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="21c63-230">Billed sales</span></span></td>
<td><span data-ttu-id="21c63-231">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-231">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21c63-232">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="21c63-232">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21c63-233">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-233">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21c63-234">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-234">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-235">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="21c63-235">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="21c63-236">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-236">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-237">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="21c63-237">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="21c63-238">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-238">Project contract currency</span></span></td>
</tr>
</tbody>
</table>

### <a name="the-resource-belongs-to-an-organizational-unit-that-differs-from-the-projects-contracting-unit"></a><span data-ttu-id="21c63-239">Ištekliai priklauso skirtingam organizaciniam vienetui nei projekto sutarties vienetas</span><span class="sxs-lookup"><span data-stu-id="21c63-239">The resource belongs to an organizational unit that differs from the project's contracting unit</span></span>

<table>
<thead>
<tr>
<th rowspan="3"><span data-ttu-id="21c63-240">Įvykis</span><span class="sxs-lookup"><span data-stu-id="21c63-240">Event</span></span></th>
<th colspan="4"><span data-ttu-id="21c63-241">Apmokėtinas arba parduotas projektas</span><span class="sxs-lookup"><span data-stu-id="21c63-241">Billable or sold project</span></span></th>
<th rowspan="3"><span data-ttu-id="21c63-242">Projektas paruošiamųjų darbų etape prieš parduodant</span><span class="sxs-lookup"><span data-stu-id="21c63-242">Project in the presales stage</span></span></th>
<th rowspan="3"><span data-ttu-id="21c63-243">Vidinis projektas</span><span class="sxs-lookup"><span data-stu-id="21c63-243">Internal project</span></span></th>
</tr>
<tr>
<th colspan="2"><span data-ttu-id="21c63-244">Laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="21c63-244">Time and materials</span></span></th>
<th colspan="2"><span data-ttu-id="21c63-245">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="21c63-245">Fixed price</span></span></th>
</tr>
<tr>
<th><span data-ttu-id="21c63-246">Faktinės</span><span class="sxs-lookup"><span data-stu-id="21c63-246">Actuals</span></span></th>
<th><span data-ttu-id="21c63-247">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-247">Transaction currency</span></span></th>
<th><span data-ttu-id="21c63-248">Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="21c63-248">Fixed price</span></span></th>
<th><span data-ttu-id="21c63-249">Operacijos valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-249">Transaction currency</span></span></th>
</tr>
</thead>
<tbody>
<tr>
<td><span data-ttu-id="21c63-250">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="21c63-250">A time entry is created.</span></span></td>
<td colspan="6"><span data-ttu-id="21c63-251">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="21c63-251">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-252">Sukurtas laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="21c63-252">A time entry is submitted.</span></span></td>
<td colspan="6"><span data-ttu-id="21c63-253">Nėra veiksmų faktinių duomenų objekte</span><span class="sxs-lookup"><span data-stu-id="21c63-253">No activity in the Actuals entity</span></span></td>
</tr>
<tr>
<td rowspan="4"><span data-ttu-id="21c63-254">Laikas yra patvirtintas, o patvirtinimo metu apmokamos valandos nesikeičia ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="21c63-254">Time is approved, and no change to or increase in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21c63-255">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-255">Cost actual</span></span></td>
<td><span data-ttu-id="21c63-256">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-256">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="21c63-257">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-257">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="21c63-258">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-258">Contracting unit currency</span></span></td>
<td rowspan="4"><span data-ttu-id="21c63-259">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-259">Cost actual</span></span></td>
<td rowspan="4"><span data-ttu-id="21c63-260">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-260">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-261">Neišrašyta pardavimo suma - Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="21c63-261">Unbilled sales actual – Chargeable</span></span></td>
<td><span data-ttu-id="21c63-262">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-262">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-263">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="21c63-263">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="21c63-264">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-264">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-265">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="21c63-265">Interorganizational sales</span></span></td>
<td><span data-ttu-id="21c63-266">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-266">Contracting unit currency</span></span></td>
</tr>
<tr>
<td rowspan="5"><span data-ttu-id="21c63-267">Laikas yra patvirtintas, o patvirtinimo metu sumažėja apmokestinamų valandų skaičius.</span><span class="sxs-lookup"><span data-stu-id="21c63-267">Time is approved, and a decrease in billable hours occurs during approval.</span></span></td>
<td><span data-ttu-id="21c63-268">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-268">Cost actual</span></span></td>
<td><span data-ttu-id="21c63-269">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-269">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-270">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-270">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-271">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-271">Contracting unit currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-272">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-272">Cost actual</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-273">Faktinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="21c63-273">Cost actual</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-274">Išteklių paskirstymo vieneto savikaina</span><span class="sxs-lookup"><span data-stu-id="21c63-274">Resourcing unit cost</span></span></td>
<td><span data-ttu-id="21c63-275">Išteklių vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-275">Resourcing unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-276">Tarp organizacijų vykdomas pardavimas</span><span class="sxs-lookup"><span data-stu-id="21c63-276">Interorganizational sales</span></span></td>
<td><span data-ttu-id="21c63-277">Sutarties vieneto valiuta</span><span class="sxs-lookup"><span data-stu-id="21c63-277">Contracting unit currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-278">Neišrašyta pardavimo suma - Apmokestinama už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="21c63-278">Unbilled sales actual – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21c63-279">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-279">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-280">Neišrašyta pardavimo suma - Neapmokestinama už skirtumą</span><span class="sxs-lookup"><span data-stu-id="21c63-280">Unbilled sales actual – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21c63-281">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-281">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21c63-282">Sąskaita faktūra patvirtinta, nesikeičia apmokestinamos valandos ir jų skaičius nedidėja.</span><span class="sxs-lookup"><span data-stu-id="21c63-282">An invoice is confirmed, and no change to or increase in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21c63-283">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-283">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21c63-284">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-284">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-285">Išrašytas pardavimas už etapą</span><span class="sxs-lookup"><span data-stu-id="21c63-285">Billed sales for milestone</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-286">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-286">Project contract currency</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-287">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-287">Not applicable</span></span></td>
<td rowspan="2"><span data-ttu-id="21c63-288">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-288">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-289">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="21c63-289">Billed sales</span></span></td>
<td><span data-ttu-id="21c63-290">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-290">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21c63-291">Sąskaita faktūra patvirtinta ir sumažėja apmokestinamų valandų.</span><span class="sxs-lookup"><span data-stu-id="21c63-291">An invoice is confirmed, and a decrease in billable hours occurs.</span></span></td>
<td><span data-ttu-id="21c63-292">Neišrašyto pardavimo atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-292">Unbilled sales reversal</span></span></td>
<td><span data-ttu-id="21c63-293">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-293">Project contract currency</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-294">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-294">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-295">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-295">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-296">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-296">Not applicable</span></span></td>
<td rowspan="3"><span data-ttu-id="21c63-297">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-297">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-298">Išrašytas pardavimas - Apmokestinamas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="21c63-298">Billed sales – Chargeable for the new quantity</span></span></td>
<td><span data-ttu-id="21c63-299">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-299">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-300">Išrašytas pardavimas - Neapmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="21c63-300">Billed sales – Non-chargeable for the difference</span></span></td>
<td><span data-ttu-id="21c63-301">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-301">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="2"><span data-ttu-id="21c63-302">Sąskaita faktūra ištaisyta siekiant padidinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="21c63-302">An invoice is corrected to increase the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21c63-303">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-303">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21c63-304">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-304">Project contract currency</span></span></td>
<td rowspan="5">
<ul>
<li><span data-ttu-id="21c63-305">Išrašyto pardavimo atšaukimas už etapą</span><span class="sxs-lookup"><span data-stu-id="21c63-305">Billed sales reversal for milestone</span></span></li>
<li><span data-ttu-id="21c63-306">Etapo būsenos pakeitimas iš <strong>Išrašyta sąskaita faktūra</strong> į  <strong>Paruošta sąskaitai faktūrai</strong></span><span class="sxs-lookup"><span data-stu-id="21c63-306">Change in milestone status from <strong>Invoiced</strong> to <strong>Ready for invoice</strong></span></span></li>
</ul>
</td>
<td rowspan="5"><span data-ttu-id="21c63-307">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-307">Project contract currency</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-308">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-308">Not applicable</span></span></td>
<td rowspan="5"><span data-ttu-id="21c63-309">Netaikoma</span><span class="sxs-lookup"><span data-stu-id="21c63-309">Not applicable</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-310">Išrašytas pardavimas</span><span class="sxs-lookup"><span data-stu-id="21c63-310">Billed sales</span></span></td>
<td><span data-ttu-id="21c63-311">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-311">Project contract currency</span></span></td>
</tr>
<tr>
<td rowspan="3"><span data-ttu-id="21c63-312">Sąskaita faktūra ištaisoma siekiant sumažinti mokėtiną kiekį.</span><span class="sxs-lookup"><span data-stu-id="21c63-312">An invoice is corrected to decrease the chargeable quantity.</span></span></td>
<td><span data-ttu-id="21c63-313">Neišrašytas pardavimas - Atšaukimas</span><span class="sxs-lookup"><span data-stu-id="21c63-313">Billed sales – Reversal</span></span></td>
<td><span data-ttu-id="21c63-314">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-314">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-315">Išrašytas pardavimas už naują kiekį</span><span class="sxs-lookup"><span data-stu-id="21c63-315">Billed sales for the new quantity</span></span></td>
<td><span data-ttu-id="21c63-316">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-316">Project contract currency</span></span></td>
</tr>
<tr>
<td><span data-ttu-id="21c63-317">Neišrašytas pardavimas - apmokestinamas už skirtumą</span><span class="sxs-lookup"><span data-stu-id="21c63-317">Unbilled sales – Chargeable for the difference</span></span></td>
<td><span data-ttu-id="21c63-318">Projekto sutarties valiuta.</span><span class="sxs-lookup"><span data-stu-id="21c63-318">Project contract currency</span></span></td>
</tr>
</tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
