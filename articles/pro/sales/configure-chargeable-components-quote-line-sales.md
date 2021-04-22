---
title: Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie apmokestinamų ir neapmokestinamų komponentų nustatymą projektais pagrįsto pasiūlymo eilutėje.
author: rumant
manager: Annbe
ms.date: 03/30/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1a9e1851bd8c5a4070df2774c945d1f3eabaaa8a
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858303"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a><span data-ttu-id="e272e-103">Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="e272e-103">Configure the chargeable components of a quote line</span></span> 

<span data-ttu-id="e272e-104">_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="e272e-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="e272e-105">Projektais pagrįsto pasiūlymo eilutėje pateikiama *įtrauktų* ir *apmokestinamų* sąvoka.</span><span class="sxs-lookup"><span data-stu-id="e272e-105">A project-based quote line has the concept of *included* components and *chargeable* components.</span></span>

<span data-ttu-id="e272e-106">Įtrauktiems komponentams taikomos toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="e272e-106">Included components are subject to:</span></span>

  - <span data-ttu-id="e272e-107">Sąskaitų išrašymo būdo ir klientų išskaidymas</span><span class="sxs-lookup"><span data-stu-id="e272e-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="e272e-108">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="e272e-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="e272e-109">Sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįsto pasiūlymo eilutėje</span><span class="sxs-lookup"><span data-stu-id="e272e-109">Invoice frequency settings defined on the project-based quote line</span></span>

<span data-ttu-id="e272e-110">Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas naudojant lauką **Atsiskaitymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="e272e-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="e272e-111">Laukas **Atsiskaitymo tipas** yra parinkčių rinkinys, leidžiantis toliau nurodytas reikšmes pasiūlymo eilutės kontekste.</span><span class="sxs-lookup"><span data-stu-id="e272e-111">The **Billing Type** field is an option-set that allows the following values in the context of a quote line:</span></span>

  - <span data-ttu-id="e272e-112">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-112">Chargeable</span></span>
  - <span data-ttu-id="e272e-113">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-113">Non-chargeable</span></span>

<span data-ttu-id="e272e-114">Apmokestinamus komponentus galima apibrėžti užduotyse, vaidmenyse ir operacijų kategorijose.</span><span class="sxs-lookup"><span data-stu-id="e272e-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="e272e-115">Pasiūlymo eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms.</span><span class="sxs-lookup"><span data-stu-id="e272e-115">Chargeability is defined on the tasks for a quote line and applies to all transaction classes included on that line.</span></span> <span data-ttu-id="e272e-116">Jei laukas **Įtraukti užduotis** yra tuščias arba nustatytas į parinktį **Visas projektas**, skirtukas **Apmokestinamos užduotys** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="e272e-116">If the **Include Tasks** field is set to **Entire project** or left blank, the **Chargeable Tasks** tab isn't available.</span></span>

<span data-ttu-id="e272e-117">Pasiūlymo eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei.</span><span class="sxs-lookup"><span data-stu-id="e272e-117">Chargeability is defined on roles for a quote line and only applies to the **Time** transaction class.</span></span> <span data-ttu-id="e272e-118">Jei projekto pasiūlymo eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="e272e-118">If the field, **Include Time** is set to **No** on a project quote line, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="e272e-119">Pasiūlymo eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei.</span><span class="sxs-lookup"><span data-stu-id="e272e-119">Chargeability is defined on transaction categories for a  quote line and only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="e272e-120">Jei projekto pasiūlymo eilutės laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="e272e-120">If the field, **Include Expenses** is set to **No** on a project quote line, the **Chargeable Categories** tab isn't available.</span></span>

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="e272e-121">Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="e272e-121">Update a project task to be chargeable or non-chargeable</span></span>

<span data-ttu-id="e272e-122">Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečios projektais pagrįsto pasiūlymo eilutės kontekste, todėl galima nustatyti toliau nurodytą sąranką.</span><span class="sxs-lookup"><span data-stu-id="e272e-122">A project task can be chargeable or non-chargeable in the context of a specific project-based quote line, which makes the following setup possible.</span></span>

<span data-ttu-id="e272e-123">Jei projekto pasiūlymo eilutėje yra **Laikas** ir užduotis **T1**, užduotis susieta su pasiūlymo eilute kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="e272e-123">If a project-based quote line includes **Time** and the task **T1**, the task is associated to the quote line as chargeable.</span></span> <span data-ttu-id="e272e-124">Jei antroje išlaidas eilutėje yra **Išlaidos**, **T1** užduotį galite susieti išlaidas eilutėje kaip neapmokestinamą.</span><span class="sxs-lookup"><span data-stu-id="e272e-124">If there is a second quote line that includes **Expenses**, you can associate the **T1** task on the quote line as non-chargeable.</span></span> <span data-ttu-id="e272e-125">Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos užduotyje įrašytos išlaidos – neapmokestinamos.</span><span class="sxs-lookup"><span data-stu-id="e272e-125">The result is that all time recorded on the task is chargeable and all expenses recorded on the task are non-chargeable.</span></span>

<span data-ttu-id="e272e-126">Užduoties sąskaitų išrašymo tipą galima sukonfigūruoti projektu pagrįstos pasiūlymo eilutės skirtuke **Apmokestinamosios užduotys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Pasiūlymo eilučių užduotys**.</span><span class="sxs-lookup"><span data-stu-id="e272e-126">A task's billing type can be configured on the **Chargeable Tasks** tab of a project-based quote line by updating the **Billing Type** field on the **Quote Line Tasks** subgrid.</span></span> <span data-ttu-id="e272e-127">Arba galite atnaujinti projekto užduoties atsiskaitymo tipą lauke **Atsiskaitymo tipas**, esantį projekto, kuriame pasiūlymo eilutės rodomos kaip susietos su užduotimi, atsiskaitymo už užduotis sąrankos papildomame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="e272e-127">Alternatively, you can update the billing type for a project task in the **Billing Type** field on the subgrid on the task billing setup of a project that shows the quote lines associated to a task.</span></span>

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="e272e-128">Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="e272e-128">Update a role to be chargeable or non-chargeable</span></span>

<span data-ttu-id="e272e-129">Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečios projektais pagrįsto pasiūlymo eilutės kontekste.</span><span class="sxs-lookup"><span data-stu-id="e272e-129">A role can be chargeable or non-chargeable in the context of a specific project-based quote line.</span></span>

<span data-ttu-id="e272e-130">Vaidmens sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamieji vaidmenys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamieji vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="e272e-130">A role's billing type can be configured on the **Chargeable Roles** tab of a quote line by updating the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="e272e-131">Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="e272e-131">Update a transaction category to be chargeable or non-chargeable</span></span>

<span data-ttu-id="e272e-132">Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="e272e-132">A transaction category can be chargeable or non-chargeable on a specific quote line.</span></span>

<span data-ttu-id="e272e-133">Operacijos sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamosios kategorijos**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="e272e-133">A transaction's billing type can be configured on the **Chargeable Categories** tab of a quote line by updating the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="e272e-134">Apmokestinamumo sprendimas</span><span class="sxs-lookup"><span data-stu-id="e272e-134">Resolve chargeability</span></span>
<span data-ttu-id="e272e-135">Įvertinimas arba faktiniai sukurti laikui duomenys bus apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="e272e-135">An estimate or actual created for time will only be considered chargeable if:</span></span>

   - <span data-ttu-id="e272e-136">Į pasiūlymo eilutę įtraukta reikšmė **Laikas**.</span><span class="sxs-lookup"><span data-stu-id="e272e-136">**Time** is included on the quote line.</span></span>
   - <span data-ttu-id="e272e-137">Pasiūlymo eilutėje **Vaidmuo** yra sukonfigūruotas kaip apmokestinamas.</span><span class="sxs-lookup"><span data-stu-id="e272e-137">**Role** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="e272e-138">Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="e272e-138">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span> 

<span data-ttu-id="e272e-139">Jei šie trys punktai atitinkami, **užduotis** taip pat sukonfigūruojama kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="e272e-139">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="e272e-140">Įvertinimas arba faktiniai sukurti išlaidoms duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="e272e-140">An estimate or actual created for expense is only considered chargeable if:</span></span> 

   - <span data-ttu-id="e272e-141">Į pasiūlymo eilutę įtraukta reikšmė **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="e272e-141">**Expense** is included on the quote line.</span></span>
   - <span data-ttu-id="e272e-142">Pasiūlymo eilutėje **Operacijos kategorija** yra sukonfigūruota kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="e272e-142">**Transaction category** is configured as chargeable on the quote line.</span></span>
   - <span data-ttu-id="e272e-143">Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="e272e-143">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="e272e-144">Jei šie trys punktai atitinkami, **užduotis** taip pat sukonfigūruojama kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="e272e-144">If these three things are true, the **Task** is also configured as chargeable.</span></span> 

<span data-ttu-id="e272e-145">Įvertinimas arba faktiniai sukurti medžiagai duomenys bus apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="e272e-145">An estimate or actual created for material will only be considered chargeable if:</span></span>

   - <span data-ttu-id="e272e-146">Į pasiūlymo eilutę įtraukta reikšmė **Medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="e272e-146">**Materials** is included on the quote line.</span></span>
   - <span data-ttu-id="e272e-147">Pasiūlymo eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="e272e-147">**Included Tasks** is set to **Selected tasks** on the quote line.</span></span>

<span data-ttu-id="e272e-148">Jei šie du punktai atitinkami, **užduotis** taip pat gali būti sukonfigūruota kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="e272e-148">If these two things are true, the **Task** should also be configured as chargeable.</span></span> 


<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-149">
                    <strong>Įtrauktas laikas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-149">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e272e-150">
                    <strong>Įtrauktos išlaidos</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-150">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e272e-151">
                    <strong>Įtrauktos medžiagos</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-151">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="e272e-152">
                    <strong>Įtrauktos užduotys</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-152">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-153">
                    <strong>Vaidmuo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-153">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-154">
                    <strong>Kategorija.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-154">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-155">
                    <strong>Užduotis</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-155">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="e272e-156">
                    <strong>Poveikis apmokestinimui</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-156">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-157">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-157">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-158">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-158">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-159">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-159">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-160">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="e272e-160">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-161">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-161">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-162">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-162">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-163">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-163">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-164">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-164">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-165">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-165">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-166">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-166">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-167">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-167">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-168">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-168">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-169">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-169">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-170">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="e272e-170">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-171">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-171">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-172">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-172">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-173">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-173">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-174">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-174">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-175">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-175">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-176">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-176">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-177">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-177">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-178">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-178">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-179">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-179">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-180">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="e272e-180">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-181">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-181">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-182">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-182">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-183">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-183">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-184">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-184">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-185">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-185">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-186">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-186">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-187">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-187">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-188">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-188">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-189">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-189">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-190">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="e272e-190">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-191">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-191">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-192">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-192">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-193">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-193">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-194">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-194">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-195">Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-195">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-196">Atsiskaitymas pagal faktines medžiagas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-196">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-197">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-197">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-198">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-198">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-199">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-199">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-200">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="e272e-200">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-201">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-201">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-202">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-202">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-203">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-203">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-204">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-204">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-205">Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-205">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-206">Atsiskaitymas pagal faktines medžiagas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-206">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-207">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-207">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-208">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-208">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-209">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-209">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-210">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="e272e-210">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-211">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-211">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-212">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-212">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-213">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-213">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-214">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-214">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-215">Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-215">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-216">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-216">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-217">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-217">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-218">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-218">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-219">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-219">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-220">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="e272e-220">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-221">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-221">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-222">
                    <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-222">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-223">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-223">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-224">Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-224">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-225">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-225">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-226">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-226">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-227">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-227">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-228">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-228">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-229">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-229">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-230">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="e272e-230">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-231">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-231">Cannot be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-232">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-232">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-233">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-233">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-234">Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-234">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-235">Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-235">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-236">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-236">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-237">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-237">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e272e-238">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-238">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-239">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-239">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-240">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="e272e-240">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-241">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-241">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-242">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-242">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-243">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-243">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-244">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-244">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-245">Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-245">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-246">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-246">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-247">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-247">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="e272e-248">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-248">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="e272e-249">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-249">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-250">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="e272e-250">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-251">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-251">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-252">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-252">Cannot be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-253">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-253">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-254">Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-254">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-255">Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-255">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-256">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-256">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-257">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-257">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-258">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-258">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e272e-259">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-259">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-260">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="e272e-260">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-261">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-261">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-262">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="e272e-262">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-263">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-263">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-264">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-264">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-265">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="e272e-265">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="e272e-266">Atsiskaitymas pagal faktinę medžiagą: <strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-266">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="e272e-267">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-267">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="e272e-268">Taip</span><span class="sxs-lookup"><span data-stu-id="e272e-268">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="e272e-269">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-269">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="e272e-270">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="e272e-270">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="e272e-271">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-271">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="e272e-272">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-272">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="e272e-273">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="e272e-273">Cannot be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="e272e-274">Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-274">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-275">Atsiskaitymas pagal faktines išlaidas:<strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-275">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="e272e-276">Atsiskaitymas pagal faktinę medžiagą:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="e272e-276">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
