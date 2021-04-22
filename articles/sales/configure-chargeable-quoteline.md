---
title: Projektu pagrįsto pasiūlymo eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikiama informacija apie įtrauktus, apmokestinamus ir neapmokestinamus komponentus projektu pagrįsto pasiūlymo eilutėse.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5484c37181bc8a26a6dfe67807093cc83e53e703
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278743"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a><span data-ttu-id="cd997-103">Projektu pagrįsto pasiūlymo eilutės apmokestinamų komponentų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cd997-103">Configure the chargeable components of a project-based quote line</span></span>

<span data-ttu-id="cd997-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="cd997-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cd997-105">Projektu pagrįsto pasiūlymo eilutėje gali būti įtrauktų komponentų ir apmokestinamų komponentų.</span><span class="sxs-lookup"><span data-stu-id="cd997-105">A project-based quote line can have included components and chargeable components.</span></span>

<span data-ttu-id="cd997-106">Įtrauktiems komponentams taikomas atsiskaitymo metodas, išskaidymai klientams, limitai, kurių negalima viršyti, ir sąskaitų faktūrų dažnio parametrai, apibrėžti projektu pagrįsto pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd997-106">Included components are subject to the billing method, customer splits, not-to-exceed limits, and invoice frequency settings defined on the project-based quote line.</span></span>
<span data-ttu-id="cd997-107">Antrinis įtrauktų komponentų rinkinys gali būti pažymėtas kaip apmokestinamas, naudojant lauką **Atsiskaitymo tipas**.</span><span class="sxs-lookup"><span data-stu-id="cd997-107">A subset of the included components can be marked as chargeable by using **Billing Type**.</span></span> <span data-ttu-id="cd997-108">Pasiūlymo eilutės kontekste, lauke **Atsiskaitymo tipas**, galite pasirinkti vieną iš toliau nurodytų parinkčių:</span><span class="sxs-lookup"><span data-stu-id="cd997-108">You can select one of the following options in the **Billing Type** field in the context of a quote line:</span></span>

   - <span data-ttu-id="cd997-109">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-109">Chargeable</span></span>
   - <span data-ttu-id="cd997-110">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-110">Non-chargeable</span></span>

<span data-ttu-id="cd997-111">Apmokestinamus komponentus galima apibrėžti naudojant vaidmenis ir operacijų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="cd997-111">Chargeable components can be defined on roles and transaction categories.</span></span>

<span data-ttu-id="cd997-112">Apmokestinimas, apibrėžtas naudojant projekto pasiūlymo eilutės vaidmenis, taikomas tik operacijos klasei **Laikas**.</span><span class="sxs-lookup"><span data-stu-id="cd997-112">Chargeability that is defined on roles for a project quote line only applies to the **Time** transaction class.</span></span> <span data-ttu-id="cd997-113">Jei projekto pasiūlymo eilutėje **Įtraukti laiką** = **Ne**, tai skirtukas **Apmokestinami vaidmenys** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="cd997-113">If a project quote line has **Include Time** = **No**, the **Chargeable Roles** tab isn't available.</span></span>

<span data-ttu-id="cd997-114">Apmokestinimas, apibrėžtas naudojant projekto pasiūlymo eilutės operacijų kategorijas, taikomas tik operacijos klasei **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="cd997-114">Chargeability that is defined on transaction categories for a project quote line only applies to the **Expense** transaction class.</span></span> <span data-ttu-id="cd997-115">Jei projekto pasiūlymo eilutėje **Įtraukti išlaidas** = **Ne**, tai skirtukas **Apmokestinamos kategorijos** nebus pateiktas.</span><span class="sxs-lookup"><span data-stu-id="cd997-115">If a project quote line has **Include Expenses** = **No**, the **Chargeable Categories** tab isn't available.</span></span>

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="cd997-116">Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="cd997-116">Update a role to be chargeable or non-chargeable</span></span>
<span data-ttu-id="cd997-117">Projekto pasiūlymo eilutėje vaidmuo gali būti apmokestinamas arba neapmokestinamas.</span><span class="sxs-lookup"><span data-stu-id="cd997-117">A role can be chargeable or non-chargeable on a project-based quote line.</span></span> <span data-ttu-id="cd997-118">Atsiskaitymo tipą pagal vaidmenį galima sukonfigūruoti projektu pagrįsto pasiūlymo eilutės skirtuke **Apmokestinami vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="cd997-118">The billing type on a role can be configured on the **Chargeable Roles** tab of a project-based quote line.</span></span> <span data-ttu-id="cd997-119">Norėdami tai atlikti, atnaujinkite **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinami vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="cd997-119">To do this, update **Billing Type** on the **Chargeable Roles** subgrid.</span></span> 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a><span data-ttu-id="cd997-120">Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą</span><span class="sxs-lookup"><span data-stu-id="cd997-120">Update a transaction category to be chargeable or non-chargeable</span></span>
<span data-ttu-id="cd997-121">Projekto pasiūlymo eilutėje operacijos kategorija gali būti apmokestinama arba neapmokestinama.</span><span class="sxs-lookup"><span data-stu-id="cd997-121">A transaction category can be chargeable or non-chargeable on a project-based quote line.</span></span> <span data-ttu-id="cd997-122">Atsiskaitymo tipą pagal operaciją galima sukonfigūruoti projektu pagrįsto pasiūlymo eilutės skirtuke **Apmokestinamos kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="cd997-122">The billing type on a transaction can be configured on the **Chargeable Categories** tab of a project-based quote line.</span></span> <span data-ttu-id="cd997-123">Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="cd997-123">To do this, update the **Billing Type** field on the **Chargeable Categories** subgrid.</span></span> 

## <a name="resolve-chargeability"></a><span data-ttu-id="cd997-124">Apmokestinamumo sprendimas</span><span class="sxs-lookup"><span data-stu-id="cd997-124">Resolve chargeability</span></span>

<span data-ttu-id="cd997-125">Numatomi arba faktiniai duomenys, sukurti pagal laiką, yra apmokestinami tik tuo atveju, jei laikas įtrauktas į pasiūlymo eilutę ir jei vaidmuo sukonfigūruotas kaip apmokestinamas.</span><span class="sxs-lookup"><span data-stu-id="cd997-125">An estimate or actual created for time will only be considered chargeable if the time is included on the quote line and if the role is configured as chargeable.</span></span>
<span data-ttu-id="cd997-126">Numatomi arba faktiniai duomenys, sukurti pagal išlaidas, yra apmokestinami tik tuo atveju, jei išlaidos įtrauktos į pasiūlymo eilutę ir jei operacijos kategorija pasiūlymo eilutėje sukonfigūruota kaip apmokestinama.</span><span class="sxs-lookup"><span data-stu-id="cd997-126">An estimate or actual created for an expense will only be considered chargeable if the expense is included on the quote line and if the transaction category is configured as chargeable on the quote line.</span></span> <span data-ttu-id="cd997-127">Toliau esančioje lentelėje parodytos numatytosios apmokestinimo reikšmės pagal faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="cd997-127">The following table shows how chargeability defaults on each actual.</span></span> <span data-ttu-id="cd997-128">Numatytosios reikšmės pagrįstos įtrauktais komponentais ir atsiskaitymo tipu, nustatytu pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cd997-128">The defaults are based on the included components and the billing type that is set up on the quote line.</span></span>

| <span data-ttu-id="cd997-129">Įtrauktas laikas</span><span class="sxs-lookup"><span data-stu-id="cd997-129">Includes time</span></span> | <span data-ttu-id="cd997-130">Įtrauktos išlaidos</span><span class="sxs-lookup"><span data-stu-id="cd997-130">Includes expense</span></span> | <span data-ttu-id="cd997-131">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="cd997-131">Role</span></span> | <span data-ttu-id="cd997-132">Kategorija.</span><span class="sxs-lookup"><span data-stu-id="cd997-132">Category</span></span> | <span data-ttu-id="cd997-133">Užduotis</span><span class="sxs-lookup"><span data-stu-id="cd997-133">Task</span></span> |
| --- | --- | --- | --- | --- |
| <span data-ttu-id="cd997-134">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-134">Yes</span></span> | <span data-ttu-id="cd997-135">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-135">Yes</span></span> | <span data-ttu-id="cd997-136">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-136">Chargeable</span></span> | <span data-ttu-id="cd997-137">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-137">Chargeable</span></span> | <span data-ttu-id="cd997-138">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-138">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="cd997-139">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-139">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="cd997-140">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-140">Yes</span></span> | <span data-ttu-id="cd997-141">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-141">Yes</span></span> | <span data-ttu-id="cd997-142">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-142">Non - Chargeable</span></span> | <span data-ttu-id="cd997-143">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-143">Chargeable</span></span> | <span data-ttu-id="cd997-144">Atsiskaitymas pagal faktinį laiką: Neapmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-144">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="cd997-145">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-145">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="cd997-146">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-146">Yes</span></span> | <span data-ttu-id="cd997-147">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-147">Yes</span></span> | <span data-ttu-id="cd997-148">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-148">Non-Chargeable</span></span> | <span data-ttu-id="cd997-149">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-149">Non-Chargeable</span></span> | <span data-ttu-id="cd997-150">Atsiskaitymas pagal faktinį laiką: Neapmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-150">Billing on a time actual: Non-Chargeable</span></span> </br><span data-ttu-id="cd997-151">Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-151">Billing type on an expense actual: Non-Chargeable</span></span> |
| <span data-ttu-id="cd997-152">No</span><span class="sxs-lookup"><span data-stu-id="cd997-152">No</span></span> | <span data-ttu-id="cd997-153">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-153">Yes</span></span> | <span data-ttu-id="cd997-154">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="cd997-154">Can't be set</span></span> | <span data-ttu-id="cd997-155">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-155">Chargeable</span></span> | <span data-ttu-id="cd997-156">Atsiskaitymas pagal faktinį laiką: Nėra</span><span class="sxs-lookup"><span data-stu-id="cd997-156">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="cd997-157">Atsiskaitymas pagal faktines išlaidas: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-157">Billing type on an expense actual: Chargeable</span></span> |
| <span data-ttu-id="cd997-158">No</span><span class="sxs-lookup"><span data-stu-id="cd997-158">No</span></span> | <span data-ttu-id="cd997-159">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-159">Yes</span></span> | <span data-ttu-id="cd997-160">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="cd997-160">Can't be set</span></span> | <span data-ttu-id="cd997-161">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-161">Non-Chargeable</span></span> | <span data-ttu-id="cd997-162">Atsiskaitymas pagal faktinį laiką: Nėra</span><span class="sxs-lookup"><span data-stu-id="cd997-162">Billing on a time actual: Not available</span></span> </br><span data-ttu-id="cd997-163">Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-163">Billing type on an expense actual: Non-chargeable</span></span> |
| <span data-ttu-id="cd997-164">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-164">Yes</span></span> | <span data-ttu-id="cd997-165">No</span><span class="sxs-lookup"><span data-stu-id="cd997-165">No</span></span> | <span data-ttu-id="cd997-166">Apmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-166">Chargeable</span></span> | <span data-ttu-id="cd997-167">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="cd997-167">Can't be set</span></span> | <span data-ttu-id="cd997-168">Atsiskaitymas pagal faktinį laiką: Apmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-168">Billing on a time actual: Chargeable</span></span> </br><span data-ttu-id="cd997-169">Atsiskaitymas pagal faktines išlaidas: Nėra</span><span class="sxs-lookup"><span data-stu-id="cd997-169">Billing type on an expense actual: Not available</span></span> |
| <span data-ttu-id="cd997-170">Taip</span><span class="sxs-lookup"><span data-stu-id="cd997-170">Yes</span></span> | <span data-ttu-id="cd997-171">No</span><span class="sxs-lookup"><span data-stu-id="cd997-171">No</span></span> | <span data-ttu-id="cd997-172">Neapmokestinama</span><span class="sxs-lookup"><span data-stu-id="cd997-172">Non-Chargeable</span></span> | <span data-ttu-id="cd997-173">Negalima nustatyti</span><span class="sxs-lookup"><span data-stu-id="cd997-173">Can't be set</span></span> | <span data-ttu-id="cd997-174">Atsiskaitymas pagal faktinį laiką: Neapmokestinamas</span><span class="sxs-lookup"><span data-stu-id="cd997-174">Billing on a time actual: Non-chargeable</span></span> </br> <span data-ttu-id="cd997-175">Atsiskaitymas pagal faktines išlaidas: Nėra</span><span class="sxs-lookup"><span data-stu-id="cd997-175">Billing type on an expense actual: Not available</span></span> |


[!INCLUDE[footer-include](../includes/footer-banner.md)]