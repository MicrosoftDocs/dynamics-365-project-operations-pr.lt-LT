---
title: Kainodaros ir įkainojimo dimensijų pagrindinis puslapis
description: Šioje temoje pateikta kainodaros dimensijų apžvalga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 425d7bb8-9015-4f67-b9c9-cf3602e9afe8
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 2379d0d2e038f28a1a8df87a851e9bf7db7fe33f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753677"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="6141a-103">Kainodaros ir įkainojimo dimensijų pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="6141a-103">Pricing and costing dimensions home page</span></span>

<span data-ttu-id="6141a-104">Dimensijos, naudojamos žmogiškųjų išteklių kainodarai ir savikainai nustatyti, skirstomos į dvi kategorijas:</span><span class="sxs-lookup"><span data-stu-id="6141a-104">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="6141a-105">Žmonės</span><span class="sxs-lookup"><span data-stu-id="6141a-105">People</span></span>
- <span data-ttu-id="6141a-106">Suplanuotas darbas</span><span class="sxs-lookup"><span data-stu-id="6141a-106">Planned work</span></span>

<span data-ttu-id="6141a-107">Dėl to egzistuoja dviejų tipų kainodaros dimensijų reikšmės programoje „Project Service Automation“ (PSA):</span><span class="sxs-lookup"><span data-stu-id="6141a-107">Because of this, there are two types of pricing dimension values available in Project Service Automation (PSA):</span></span> 

- <span data-ttu-id="6141a-108">**Parinkčių rinkiniai** – dimensijos, kurios yra reikšmių rinkiniams skirti fiksuoti išvardijimai.</span><span class="sxs-lookup"><span data-stu-id="6141a-108">**Option sets** - Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="6141a-109">**Objektu pagrįstos reikšmės** – dimensijos, kurios gali būti kintančiu reikšmių rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="6141a-109">**Entity-based values** - Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="6141a-110">Kainodaros dimensijos</span><span class="sxs-lookup"><span data-stu-id="6141a-110">Pricing dimensions</span></span>

<span data-ttu-id="6141a-111">PSA pateikiamas su numatytuoju kainodaros dimensijų rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="6141a-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="6141a-112">Jas galite peržiūrėti apsilankę **„Project Service“** > **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6141a-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="6141a-113">Parametrų įraše, esančiame skirtuke **Suma pagrįstos kainodaros dimensijos**, patvirtinkite, kad vaidmuo **msdyn_resourcecategory** ir išteklių organizacinio vieneto **msdyn_organizationalunit** laukai **Taikoma pardavimui** ir **Taikoma savikainai** nustatyti į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="6141a-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="6141a-114">Taip galėsite nustatyti kiekvieno vaidmens ir organizacinio vieneto derinio kainą ir savikainą.</span><span class="sxs-lookup"><span data-stu-id="6141a-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![„Project Service“ parametrų ekrano kopija su pažymėtu lauku „Taikoma pardavimui“](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="6141a-116">Jei naudojote visiškai parengtus vaidmens ir organizacinio vieneto laukus kaip kainodaros dimensijas prieš 3 PSA versiją, jokių pastebimų pakeitimų nebus.</span><span class="sxs-lookup"><span data-stu-id="6141a-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="6141a-117">Galite toliau naudoti „Project Service“ kaip įprasta.</span><span class="sxs-lookup"><span data-stu-id="6141a-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="6141a-118">Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas.</span><span class="sxs-lookup"><span data-stu-id="6141a-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="6141a-119">Daugiau informacijos rasite toliau pateikiamose temose, tačiau atkreipkite dėmesį, kad procedūras reikia atlikti toliau išvardyta tvarka:</span><span class="sxs-lookup"><span data-stu-id="6141a-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="6141a-120">Sukurti pritaikytus laukus ir objektus</span><span class="sxs-lookup"><span data-stu-id="6141a-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="6141a-121">Pridėti pritaikytus laukus prie kainos sąrankos ir operacijos objektų</span><span class="sxs-lookup"><span data-stu-id="6141a-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="6141a-122">Nustatyti pritaikytus laukus kaip kainodaros dimensijas</span><span class="sxs-lookup"><span data-stu-id="6141a-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="6141a-123">Atnaujinti priedo atributus, kad įtrauktumėte naujas kainodaros dimensijas</span><span class="sxs-lookup"><span data-stu-id="6141a-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="6141a-124">Žmogiškųjų išteklių laiko kainodara</span><span class="sxs-lookup"><span data-stu-id="6141a-124">Pricing human resource time</span></span>
<span data-ttu-id="6141a-125">Kaip organizacijos nustato kainą žmogiškųjų išteklių laikui dažnai yra svarbus strateginis aspektas, turintis tiesioginės įtakos organizacijos pelningumui.</span><span class="sxs-lookup"><span data-stu-id="6141a-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="6141a-126">Dirbkite su finansų komandomis ir praktikos vadovais, kai jūsų organizacija yra pasirengusi nustatyti, kaip ji nori nustatyti sąskaitų ir savikainos tarifus, skirtus žmogiškųjų išteklių laikui.</span><span class="sxs-lookup"><span data-stu-id="6141a-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="6141a-127">Vienas iš kitų kainodaros aspektų yra ar reikia pakartotinai naudoti laukus arba objektus, kurie šiuo metu nėra kainodaros dimensijos, tačiau taikomi kaip jūsų organizacijos kainodaros dimensija.</span><span class="sxs-lookup"><span data-stu-id="6141a-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="6141a-128">Laukai, kaip **Operacijos kategorija** (**msdyn_transactioncategory**) ir **Rezervuojami ištekliai** (**bookableresource**), yra potencialių dimensijų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="6141a-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="6141a-129">Taip pat turėtumėte įvertinti, ar jūsų kainodaros dimensija turi būti lentelė ar parinkčių rinkinys.</span><span class="sxs-lookup"><span data-stu-id="6141a-129">You should also consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="6141a-130">Jei numatote dimensijos reikšmių pakitimus, kurie viršys 10 ar 12, ir jums reikia papildomų atributų šioms reikšmėms, galite sukurti objektą, o ne parinkčių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="6141a-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="6141a-131">Parinkčių rinkinio tvarkymui, pavyzdžiui, įtraukiant ar šalinant reikšmes, būtinas administratorius arba kūrėjas, o įtraukti naujų eilučių į lentelę gali daugelis vartotojų.</span><span class="sxs-lookup"><span data-stu-id="6141a-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="6141a-132">Toliau pateiktame pavyzdyje pateikiami sąskaitų tarifai, nustatyti pagal vaidmenį ir išteklių organizacijos vienetą, kuriam priklauso išteklius.</span><span class="sxs-lookup"><span data-stu-id="6141a-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="6141a-133">Savikainos tarifai paprastai nustatomi pagal darbuotojo atlyginimų juostą ir organizacijos vienetą, kuriam jie priklauso.</span><span class="sxs-lookup"><span data-stu-id="6141a-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="6141a-134">Šiame pavyzdyje sąskaitų ir savikainos tarifų lentelės atrodo taip:</span><span class="sxs-lookup"><span data-stu-id="6141a-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="6141a-135">**Pavyzdiniai sąskaitų tarifai**</span><span class="sxs-lookup"><span data-stu-id="6141a-135">**Sample bill rates**</span></span>

| <span data-ttu-id="6141a-136">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="6141a-136">Role</span></span>        | <span data-ttu-id="6141a-137">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="6141a-137">Org Unit</span></span>    |<span data-ttu-id="6141a-138">Vienetas</span><span class="sxs-lookup"><span data-stu-id="6141a-138">Unit</span></span>      |<span data-ttu-id="6141a-139">Kaina</span><span class="sxs-lookup"><span data-stu-id="6141a-139">Price</span></span>      |<span data-ttu-id="6141a-140">Valiuta</span><span class="sxs-lookup"><span data-stu-id="6141a-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="6141a-141">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="6141a-141">Developer</span></span>   | <span data-ttu-id="6141a-142">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="6141a-142">Contoso US</span></span>  |<span data-ttu-id="6141a-143">Hour</span><span class="sxs-lookup"><span data-stu-id="6141a-143">Hour</span></span> | <span data-ttu-id="6141a-144">200</span><span class="sxs-lookup"><span data-stu-id="6141a-144">200</span></span>|<span data-ttu-id="6141a-145">USD</span><span class="sxs-lookup"><span data-stu-id="6141a-145">USD</span></span>     |
| <span data-ttu-id="6141a-146">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="6141a-146">Developer</span></span>   | <span data-ttu-id="6141a-147">„Danys India“</span><span class="sxs-lookup"><span data-stu-id="6141a-147">Contoso India</span></span> |<span data-ttu-id="6141a-148">Hour</span><span class="sxs-lookup"><span data-stu-id="6141a-148">Hour</span></span>|   <span data-ttu-id="6141a-149">112</span><span class="sxs-lookup"><span data-stu-id="6141a-149">112</span></span>|<span data-ttu-id="6141a-150">USD</span><span class="sxs-lookup"><span data-stu-id="6141a-150">USD</span></span>     |


<span data-ttu-id="6141a-151">**Pavyzdiniai savikainos tarifai**</span><span class="sxs-lookup"><span data-stu-id="6141a-151">**Sample cost rates**</span></span>

| <span data-ttu-id="6141a-152">Atlyginimų juosta</span><span class="sxs-lookup"><span data-stu-id="6141a-152">Salary Band</span></span>     | <span data-ttu-id="6141a-153">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="6141a-153">Org Unit</span></span>    |<span data-ttu-id="6141a-154">Vienetas</span><span class="sxs-lookup"><span data-stu-id="6141a-154">Unit</span></span>      |<span data-ttu-id="6141a-155">Kaina</span><span class="sxs-lookup"><span data-stu-id="6141a-155">Price</span></span>      |<span data-ttu-id="6141a-156">Valiuta</span><span class="sxs-lookup"><span data-stu-id="6141a-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="6141a-157">„My company_Band1“</span><span class="sxs-lookup"><span data-stu-id="6141a-157">My company_Band1</span></span> | <span data-ttu-id="6141a-158">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="6141a-158">Contoso US</span></span>  |<span data-ttu-id="6141a-159">Hour</span><span class="sxs-lookup"><span data-stu-id="6141a-159">Hour</span></span> | <span data-ttu-id="6141a-160">145</span><span class="sxs-lookup"><span data-stu-id="6141a-160">145</span></span>|<span data-ttu-id="6141a-161">USD</span><span class="sxs-lookup"><span data-stu-id="6141a-161">USD</span></span>     |
| <span data-ttu-id="6141a-162">„My company_Band2“</span><span class="sxs-lookup"><span data-stu-id="6141a-162">My company_Band2</span></span> | <span data-ttu-id="6141a-163">„Danys India“</span><span class="sxs-lookup"><span data-stu-id="6141a-163">Contoso India</span></span> |<span data-ttu-id="6141a-164">Hour</span><span class="sxs-lookup"><span data-stu-id="6141a-164">Hour</span></span>|   <span data-ttu-id="6141a-165">67</span><span class="sxs-lookup"><span data-stu-id="6141a-165">67</span></span>|<span data-ttu-id="6141a-166">USD</span><span class="sxs-lookup"><span data-stu-id="6141a-166">USD</span></span>     |
