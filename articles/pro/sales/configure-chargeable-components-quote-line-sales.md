---
title: Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie apmokestinamų ir neapmokestinamų komponentų nustatymą projektais pagrįsto pasiūlymo eilutėje.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c933a3800aae72624dbcbe3f06df20e5981d74d4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003776"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="b0d09-103">Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="b0d09-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="b0d09-104">_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="b0d09-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b0d09-105">Projektais pagrįsto pasiūlymo eilutėje pateikiama *įtrauktų* ir *apmokestinamų* sąvoka.</span><span class="sxs-lookup"><span data-stu-id="b0d09-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="b0d09-106">Įtrauktiems komponentams taikomos toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="b0d09-106">Included components are subject to:</span></span>

  - <span data-ttu-id="b0d09-107">Sąskaitų išrašymo būdo ir klientų išskaidymas</span><span class="sxs-lookup"><span data-stu-id="b0d09-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="b0d09-108">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="b0d09-109">Sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįsto pasiūlymo eilutėje</span><span class="sxs-lookup"><span data-stu-id="b0d09-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="b0d09-110">Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas naudojant lauką **Atsiskaitymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="b0d09-111">Laukas **Atsiskaitymo tipas** yra parinkčių rinkinys, leidžiantis toliau nurodytas reikšmes pasiūlymo eilutės kontekste.</span><span class="sxs-lookup"><span data-stu-id="b0d09-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="b0d09-112">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-112">Chargeable</span></span>
  - <span data-ttu-id="b0d09-113">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-113">Non-chargeable</span></span>

<span data-ttu-id="b0d09-114">Apmokestinamus komponentus galima apibrėžti užduotyse, vaidmenyse ir operacijų kategorijose.</span><span class="sxs-lookup"><span data-stu-id="b0d09-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="b0d09-115">Pasiūlymo eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms.</span><span class="sxs-lookup"><span data-stu-id="b0d09-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="b0d09-116">Jei laukas **Įtraukti užduotis** yra tuščias arba nustatytas į parinktį **Visas projektas**, skirtukas **Apmokestinamos užduotys** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="b0d09-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="b0d09-117">Pasiūlymo eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei.</span><span class="sxs-lookup"><span data-stu-id="b0d09-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="b0d09-118">Jei projekto pasiūlymo eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="b0d09-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="b0d09-119">Pasiūlymo eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei.</span><span class="sxs-lookup"><span data-stu-id="b0d09-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="b0d09-120">Jei projekto pasiūlymo eilutės laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="b0d09-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0d09-121">Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="b0d09-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0d09-122">Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečios projektais pagrįsto pasiūlymo eilutės kontekste, todėl galima nustatyti toliau nurodytą sąranką.</span><span class="sxs-lookup"><span data-stu-id="b0d09-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="b0d09-123">Jei projekto pasiūlymo eilutėje yra **Laikas** ir užduotis **T1**, užduotis susieta su pasiūlymo eilute kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="b0d09-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="b0d09-124">Jei antroje išlaidas eilutėje yra **Išlaidos**, **T1** užduotį galite susieti išlaidas eilutėje kaip neapmokestinamą.</span><span class="sxs-lookup"><span data-stu-id="b0d09-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="b0d09-125">Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos užduotyje įrašytos išlaidos – neapmokestinamos.</span><span class="sxs-lookup"><span data-stu-id="b0d09-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="b0d09-126">Užduoties sąskaitų išrašymo tipą galima sukonfigūruoti projektu pagrįstos pasiūlymo eilutės skirtuke **Apmokestinamosios užduotys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Pasiūlymo eilučių užduotys**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="b0d09-127">Arba galite atnaujinti projekto užduoties atsiskaitymo tipą lauke **Atsiskaitymo tipas**, esantį projekto, kuriame pasiūlymo eilutės rodomos kaip susietos su užduotimi, atsiskaitymo už užduotis sąrankos papildomame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="b0d09-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0d09-128">Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="b0d09-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0d09-129">Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečios projektais pagrįsto pasiūlymo eilutės kontekste.</span><span class="sxs-lookup"><span data-stu-id="b0d09-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="b0d09-130">Vaidmens sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamieji vaidmenys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamieji vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="b0d09-131">Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="b0d09-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="b0d09-132">Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b0d09-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="b0d09-133">Operacijos sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamosios kategorijos**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="b0d09-134">Apmokestinamumo sprendimas</span><span class="sxs-lookup"><span data-stu-id="b0d09-134">Resolve chargeability</span></span>
<span data-ttu-id="b0d09-135">Įvertinimas arba faktiniai sukurti laikui duomenys bus apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="b0d09-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="b0d09-136">Į pasiūlymo eilutę įtraukta reikšmė **Laikas**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="b0d09-137">Pasiūlymo eilutėje **Vaidmuo** yra sukonfigūruotas kaip apmokestinamas.</span><span class="sxs-lookup"><span data-stu-id="b0d09-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="b0d09-138">Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="b0d09-139">Jei šie trys punktai atitinkami, **užduotis** taip pat sukonfigūruojama kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="b0d09-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="b0d09-140">Įvertinimas arba faktiniai sukurti išlaidoms duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="b0d09-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="b0d09-141">Į pasiūlymo eilutę įtraukta reikšmė **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="b0d09-142">Pasiūlymo eilutėje **Operacijos kategorija** yra sukonfigūruota kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="b0d09-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="b0d09-143">Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="b0d09-144">Jei šie trys punktai atitinkami, **užduotis** taip pat sukonfigūruojama kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="b0d09-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="b0d09-145">Įvertinimas arba faktiniai sukurti medžiagai duomenys bus apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="b0d09-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="b0d09-146">Į pasiūlymo eilutę įtraukta reikšmė **Medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="b0d09-147">Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="b0d09-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="b0d09-148">Jei šie du punktai atitinkami, **užduotis** taip pat gali būti sukonfigūruota kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="b0d09-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-149">
                    <strong>Įtrauktas laikas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0d09-150">
                    <strong>Įtrauktos išlaidos</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0d09-151">
                    <strong>Įtrauktos medžiagos</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="b0d09-152">
                    <strong>Įtrauktos užduotys</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-153">
                    <strong>Vaidmuo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-154">
                    <strong>Kategorija.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-155">
                    <strong>Užduotis</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="b0d09-156">
                    <strong>Poveikis apmokestinimui</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-157">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-158">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-159">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-160">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="b0d09-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-161">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-162">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-163">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-164">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-165">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-166">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-167">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-168">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-169">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-170">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="b0d09-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-171">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-172">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-173">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-174">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-175">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-176">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-177">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-178">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-179">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-180">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="b0d09-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-181">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-182">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-183">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-184">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-185">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-186">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-187">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-188">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-189">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-190">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="b0d09-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-191">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-192">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-193">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-194">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-195">Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-196">Atsiskaitymas pagal faktines medžiagas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-197">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-198">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-199">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-200">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="b0d09-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-201">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-202">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-203">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-204">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-205">Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-206">Atsiskaitymas pagal faktines medžiagas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-207">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-208">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-209">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-210">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="b0d09-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-211">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-212">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-213">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-214">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-215">Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-216">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-218">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-219">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-220">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="b0d09-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-221">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-222">
                    <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-223">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-224">Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-225">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-226">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-228">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-229">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-230">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="b0d09-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-231">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-232">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-233">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-234">Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-235">Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-236">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-237">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0d09-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-239">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-240">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="b0d09-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-241">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-242">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-243">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-244">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-245">Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-246">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-247">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="b0d09-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="b0d09-249">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-250">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="b0d09-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-251">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-252">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-253">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-254">Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-255">Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-256">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-257">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-258">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0d09-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-260">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="b0d09-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-261">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-262">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="b0d09-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-263">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-264">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-265">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="b0d09-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="b0d09-266">Atsiskaitymas pagal faktinę medžiagą: <strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="b0d09-267">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="b0d09-268">Taip</span><span class="sxs-lookup"><span data-stu-id="b0d09-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="b0d09-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="b0d09-270">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="b0d09-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="b0d09-271">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="b0d09-272">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="b0d09-273">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="b0d09-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="b0d09-274">Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-275">Atsiskaitymas pagal faktines išlaidas:<strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="b0d09-276">Atsiskaitymas pagal faktinę medžiagą:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b0d09-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
