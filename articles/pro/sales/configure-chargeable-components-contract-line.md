---
title: Projektu pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie tai, kaip įtraukti apmokestinamus komponentus į sutarties eilutes naudojant „Project Operations“.
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b29c912828aa4af2d2d9cb47869012087cb834b4
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003731"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a><span data-ttu-id="24918-103">Projektu pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="24918-103">Configure chargeable components of a project-based contract line</span></span>

<span data-ttu-id="24918-104">_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="24918-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="24918-105">Į projektais pagrįstą sutarties eilutę *įtraukti* komponentai ir *apmokestinami* komponentai.</span><span class="sxs-lookup"><span data-stu-id="24918-105">A project-based contract line has *included* components and *chargeable* components.</span></span>

<span data-ttu-id="24918-106">Įtrauktiems komponentams taikomos toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="24918-106">Included components are components that are subject to:</span></span>

  - <span data-ttu-id="24918-107">Sąskaitų išrašymo būdo ir klientų išskaidymas</span><span class="sxs-lookup"><span data-stu-id="24918-107">Billing method and customer splits</span></span>
  - <span data-ttu-id="24918-108">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="24918-108">Not-to-exceed limits</span></span> 
  - <span data-ttu-id="24918-109">Sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįstoje sutarties eilutėje</span><span class="sxs-lookup"><span data-stu-id="24918-109">Invoice frequency settings defined on the project-based contract line</span></span>

<span data-ttu-id="24918-110">Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas naudojant lauką **Atsiskaitymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="24918-110">A subset of the included components can be marked as chargeable using the **Billing Type** field.</span></span> <span data-ttu-id="24918-111">Laukas **Atsiskaitymo tipas** yra parinkčių rinkinys, leidžiantis toliau nurodytas reikšmes sutarties eilutės kontekste.</span><span class="sxs-lookup"><span data-stu-id="24918-111">The **Billing Type** field is an option-set that allows the following values in the context of a contract line:</span></span>

  - <span data-ttu-id="24918-112">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-112">Chargeable</span></span>
  - <span data-ttu-id="24918-113">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-113">Non-chargeable</span></span>

<span data-ttu-id="24918-114">Apmokestinamus komponentus galima apibrėžti užduotyse, vaidmenyse ir operacijų kategorijose.</span><span class="sxs-lookup"><span data-stu-id="24918-114">Chargeable components can be defined on tasks, roles, and transaction categories.</span></span>

<span data-ttu-id="24918-115">Projekto sutarties eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms.</span><span class="sxs-lookup"><span data-stu-id="24918-115">Chargeability is defined on tasks for a project contract line and applies to all transaction classes included on the line.</span></span> <span data-ttu-id="24918-116">Jei sutarties eilutės laukas **Įtraukti užduotis** yra tuščias arba nustatytas kaip **Visas projektas**, skirtukas **Apmokestinamos užduotys** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="24918-116">If the **Include Tasks** field on a contract line is blank or set to **Entire project**, the **Chargeable tasks** tab will not be available.</span></span>

<span data-ttu-id="24918-117">Projekto sutarties eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei.</span><span class="sxs-lookup"><span data-stu-id="24918-117">Chargeability defined on roles for a project contract line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="24918-118">Jei sutarties eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="24918-118">If the **Include Time** field on a contract line is set to **No**, the **Chargeable roles** tab will not be available.</span></span>

<span data-ttu-id="24918-119">Projekto sutarties eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei.</span><span class="sxs-lookup"><span data-stu-id="24918-119">Chargeability defined on transaction categories for a project contract line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="24918-120">Jei laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="24918-120">If the **Include Expenses** field is set to **No**, the **Chargeable Categories** tab will not be available.</span></span>

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a><span data-ttu-id="24918-121">Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="24918-121">Update a project task as chargeable or non-chargeable</span></span>

<span data-ttu-id="24918-122">Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje, todėl galima nustatyti toliau nurodytą sąranką.</span><span class="sxs-lookup"><span data-stu-id="24918-122">A project task can be chargeable or non-chargeable on a specific contract line, which makes the following setup possible:</span></span>

<span data-ttu-id="24918-123">Jei projekto sutarties eilutėje yra nurodyti **Laikas** ir tam tikra užduotis, **T1** su ja susieta kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="24918-123">If a project-based contract line includes **Time** and a certain task, **T1** is associated to it as chargeable.</span></span> <span data-ttu-id="24918-124">Jei antroje sutarties eilutėje yra **Išlaidos**, T1 užduotį galite susieti sutarties eilutėje kaip neapmokestinamą.</span><span class="sxs-lookup"><span data-stu-id="24918-124">If there is a second contract line that includes **Expense**, you can associate the T1 task on the contract line as non-chargeable.</span></span> <span data-ttu-id="24918-125">Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos išlaidos – neapmokestinamos.</span><span class="sxs-lookup"><span data-stu-id="24918-125">The result is that all of the time recorded on the task is chargeable and all expenses are non-chargeable.</span></span>

<span data-ttu-id="24918-126">Užduoties sąskaitų išrašymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinamosios užduotys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį sutarties eilutės užduočių papildomame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="24918-126">A task's billing type can be configured on the **Chargeable Tasks** tab of the contract line by updating the **Billing Type** field on the contract line tasks subgrid.</span></span> <span data-ttu-id="24918-127">Arba galite atnaujinti lauką **Atsiskaitymo tipas**, esantį projekto, kuriame sutarties eilutės rodomos kaip susietos su užduotimi, atsiskaitymo už užduotis sąrankos papildomame tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="24918-127">Alternatively, you can update the **Billing Type** field on the subgrid of the task Billing setup of a project that shows the contract lines associated to a task.</span></span>

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a><span data-ttu-id="24918-128">Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="24918-128">Update a role as chargeable or non-chargeable</span></span>

<span data-ttu-id="24918-129">Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečioje sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="24918-129">A role can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="24918-130">Vaidmens atsiskaitymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinami vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="24918-130">A role's billing type can be configured on the **Chargeable Roles** tab of a contract line.</span></span> <span data-ttu-id="24918-131">Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamieji vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="24918-131">To do this, update the **Billing Type** field on the **Chargeable Roles** subgrid.</span></span>

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a><span data-ttu-id="24918-132">Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="24918-132">Update a transaction category as chargeable or non-chargeable</span></span>

<span data-ttu-id="24918-133">Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="24918-133">A transaction category can be chargeable or non-chargeable on a specific contract line.</span></span>

<span data-ttu-id="24918-134">Operacijos atsiskaitymo tipą galima sukonfigūruoti projektais pagrįstos sutarties eilutės skirtuke **Apmokestinamos kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="24918-134">A transaction's billing type can be configured on the **Chargeable Categories** tab of a project-based contract line.</span></span> <span data-ttu-id="24918-135">Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="24918-135">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span>

### <a name="resolve-chargeability"></a><span data-ttu-id="24918-136">Apmokestinamumo sprendimas</span><span class="sxs-lookup"><span data-stu-id="24918-136">Resolve chargeability</span></span>

<span data-ttu-id="24918-137">Įvertinimas arba faktiniai sukurti laikui duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="24918-137">An estimate or actual created for time is only considered chargeable if:</span></span>

   - <span data-ttu-id="24918-138">Į sutarties eilutę įtraukta reikšmė **Laikas**.</span><span class="sxs-lookup"><span data-stu-id="24918-138">**Time** is included on the contract line.</span></span>
   - <span data-ttu-id="24918-139">Sutarties eilutėje **Vaidmuo** yra sukonfigūruotas kaip apmokestinamas.</span><span class="sxs-lookup"><span data-stu-id="24918-139">**Role** is configured as chargeable on the contract line.</span></span>
   - <span data-ttu-id="24918-140">Sutarties eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**.</span><span class="sxs-lookup"><span data-stu-id="24918-140">**Included Tasks** is set to **Selected tasks** on the contract line.</span></span>
 
 <span data-ttu-id="24918-141">Jei šie trys punktai atitinkami, užduotis sukonfigūruojama kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="24918-141">If these three things are true, the task is configured as chargeable.</span></span> 

<span data-ttu-id="24918-142">Įvertinimas arba faktiniai sukurti išlaidoms duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="24918-142">An estimate or actual created for expense is only considered chargeable if:</span></span>

   - <span data-ttu-id="24918-143">Į sutarties eilutę įtraukta reikšmė **Išlaidos**</span><span class="sxs-lookup"><span data-stu-id="24918-143">**Expense** is included on the contract line</span></span>
   - <span data-ttu-id="24918-144">Sutarties eilutėje **Operacijos kategorija** yra sukonfigūruota kaip apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-144">**Transaction category** is configured as chargeable on the contract line</span></span>
   - <span data-ttu-id="24918-145">Sutarties eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinkta užduotis**</span><span class="sxs-lookup"><span data-stu-id="24918-145">**Included Tasks** is set to **Selected task** on the contract line</span></span>
  
 <span data-ttu-id="24918-146">Jei šie trys punktai atitinkami, **užduotis** sukonfigūruojama kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="24918-146">If these three things are true, the **Task** is configured as chargeable.</span></span> 

<span data-ttu-id="24918-147">Įvertinimas arba faktiniai sukurti medžiagai duomenys apmokestinami tik esant toliau nurodytoms sąlygoms.</span><span class="sxs-lookup"><span data-stu-id="24918-147">An estimate or actual created for material is only considered chargeable if:</span></span>

   - <span data-ttu-id="24918-148">Į sutarties eilutę įtraukta reikšmė **Medžiagos**</span><span class="sxs-lookup"><span data-stu-id="24918-148">**Materials** is included on the contract line</span></span>
   - <span data-ttu-id="24918-149">Sutarties eilutėje **Įtrauktos užduotys** yra nustatytos kaip **Pasirinktos užduotys**</span><span class="sxs-lookup"><span data-stu-id="24918-149">**Included Tasks** is set to **Selected tasks** on the contract line</span></span>

<span data-ttu-id="24918-150">Jei šie du punktai atitinkami, **užduotis** sukonfigūruojama kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="24918-150">If these two things are true, the **Task** is configured as chargeable.</span></span> 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-151">
                    <strong>Įtrauktas laikas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-151">
                    <strong>Includes Time</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="24918-152">
                    <strong>Įtrauktos išlaidos</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-152">
                    <strong>Includes Expense</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="24918-153">
                    <strong>Įtrauktos medžiagos</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-153">
                    <strong>Includes Materials</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p><span data-ttu-id="24918-154">
                    <strong>Įtrauktos užduotys</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-154">
                    <strong>Included Tasks</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-155">
                    <strong>Vaidmuo</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-155">
                    <strong>Role</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-156">
                    <strong>Kategorija.</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-156">
                    <strong>Category</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-157">
                    <strong>Užduotis</strong>
                    <strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-157">
                    <strong>Task</strong>
                    <strong></strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p><span data-ttu-id="24918-158">
                    <strong>Poveikis apmokestinimui</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-158">
                    <strong>Chargeability impact</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-159">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-159">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-160">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-160">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-161">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-161">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-162">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="24918-162">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-163">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-163">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-164">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-164">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-165">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-165">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-166">Atsiskaitymas pagal faktinį laiką: <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-166">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-167">Atsiskaitymas pagal faktines išlaidas: <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-167">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-168">Atsiskaitymas pagal faktines medžiagas: <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-168">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-169">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-169">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-170">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-170">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-171">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-171">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-172">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="24918-172">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-173">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-173">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-174">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-174">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-175">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-175">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-176">Atsiskaitymas pagal faktinį laiką: <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-176">Billing on a time actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-177">Atsiskaitymas pagal faktines išlaidas: <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-177">Billing type on expense actual: <strong>Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-178">Atsiskaitymas pagal faktines medžiagas: <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-178">Billing type on material actual: <strong>Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-179">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-179">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-180">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-180">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-181">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-181">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-182">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="24918-182">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-183">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-183">
                    <strong>Non - Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-184">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-184">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-185">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-185">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-186">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-186">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-187">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="24918-187">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="24918-188">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-188">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-189">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-189">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-190">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-190">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-191">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-191">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-192">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="24918-192">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-193">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-193">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-194">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-194">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-195">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-195">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-196">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-196">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-197">Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-197">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-198">Atsiskaitymas pagal faktines medžiagas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-198">Billing type on material actual: <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-199">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-199">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-200">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-200">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-201">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-201">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-202">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="24918-202">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-203">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-203">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-204">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-204">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-205">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-205">
                    <strong>Non- Chargeable</strong>
                </span></span></p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-206">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-206">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-207">Atsiskaitymas pagal faktines išlaidas: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-207">Billing type on expense actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-208">Atsiskaitymas pagal faktines medžiagas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-208">Billing type on material actual: <strong> Non-Chargeable</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-209">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-209">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-210">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-210">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-211">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-211">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-212">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="24918-212">Selected tasks only</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-213">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-213">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-214">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-214">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-215">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-215">Chargeable</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-216">Atsiskaitymas pagal faktinį laiką: <strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-216">Billing on a time actual: <strong>Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-217">Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-217">Billing type on expense actual: <strong> Non-Chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-218">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-218">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-219">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-219">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-220">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-220">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-221">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-221">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-222">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="24918-222">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-223">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-223">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-224">
                    <strong>Apmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-224">
                    <strong>Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-225">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-225">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-226">Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-226">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-227">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="24918-227">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="24918-228">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-228">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-229">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-229">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-230">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-230">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-231">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-231">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-232">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="24918-232">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-233">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-233">Can't be set</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-234">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-234">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-235">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-235">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-236">Atsiskaitymas pagal faktinį laiką: <strong>Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-236">Billing on a time actual: <strong>Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-237">Atsiskaitymas pagal faktines išlaidas: <strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-237">Billing type on expense actual: <strong> Non-chargeable</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-238">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-238">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-239">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-239">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="24918-240">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-240">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-241">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-241">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-242">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="24918-242">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-243">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-243">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-244">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-244">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-245">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-245">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-246">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="24918-246">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="24918-247">Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-247">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-248">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-248">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-249">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-249">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p><span data-ttu-id="24918-250">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-250">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="63" valign="top">
                <p>
<span data-ttu-id="24918-251">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-251">Yes</span></span> </p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-252">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="24918-252">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-253">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-253">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-254">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-254">Can't be set</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-255">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-255">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-256">Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-256">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-257">Atsiskaitymas pagal faktines išlaidas:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-257">Billing type on expense actual:<strong> Not available</strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-258">Atsiskaitymas pagal faktines medžiagas: Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-258">Billing type on material actual: Chargeable</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-259">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-259">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-260">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-260">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="24918-261">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-261">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-262">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="24918-262">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-263">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-263">Chargeable</span></span> </p>
            </td>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-264">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="24918-264">Chargeable</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-265">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-265">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-266">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="24918-266">Billing on a time actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="24918-267">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="24918-267">Billing type on expense actual: Chargeable</span></span> </p>
                <p>
<span data-ttu-id="24918-268">Atsiskaitymas pagal faktinę medžiagą: <strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-268">Billing type on material actual: <strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
<span data-ttu-id="24918-269">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-269">Yes</span></span> </p>
            </td>
            <td width="78" valign="top">
                <p>
<span data-ttu-id="24918-270">Taip</span><span class="sxs-lookup"><span data-stu-id="24918-270">Yes</span></span> </p>
            </td>
            <td width="63" valign="top">
                <p><span data-ttu-id="24918-271">
                    <strong>No</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-271">
                    <strong>No</strong>
                </span></span></p>
            </td>
            <td width="75" valign="top">
                <p>
<span data-ttu-id="24918-272">Visas projektas</span><span class="sxs-lookup"><span data-stu-id="24918-272">Entire Project</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="24918-273">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-273">
                    <strong>Non-Chargeable</strong>
                </span></span></p>
            </td>
            <td width="70" valign="top">
                <p><span data-ttu-id="24918-274">
                    <strong>Neapmokestinama</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-274">
                    <strong>Non-chargeable</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="24918-275">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="24918-275">Can't be set</span></span> </p>
            </td>
            <td width="350" valign="top">
                <p>
<span data-ttu-id="24918-276">Atsiskaitymas pagal faktinį laiką:<strong>Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-276">Billing on a time actual: <strong>Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-277">Atsiskaitymas pagal faktines išlaidas:<strong> Neapmokestinamas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-277">Billing type on expense actual:<strong> Non-chargeable </strong>
                </span></span></p>
                <p>
<span data-ttu-id="24918-278">Atsiskaitymas pagal faktinę medžiagą:<strong> Nėra</strong>
                </span><span class="sxs-lookup"><span data-stu-id="24918-278">Billing type on material actual:<strong> Not available</strong>
                </span></span></p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
