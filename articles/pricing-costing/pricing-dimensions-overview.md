---
title: Kainodaros dimensijų apžvalga
description: Šioje temoje pateikiama informacija apie kainodaros dimensijas programoje „Dynamics 365 Project Operations“.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: ec2e350e0e4c28ea1c9540d70c83fdf0a75dc408
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128473"
---
# <a name="pricing-dimensions-overview"></a><span data-ttu-id="73f79-103">Kainodaros dimensijų apžvalga</span><span class="sxs-lookup"><span data-stu-id="73f79-103">Pricing dimensions overview</span></span>

<span data-ttu-id="73f79-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="73f79-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="73f79-105">Dimensijos, naudojamos žmogiškųjų išteklių kainodarai ir savikainai nustatyti, skirstomos į dvi kategorijas:</span><span class="sxs-lookup"><span data-stu-id="73f79-105">The dimensions that are used in human resources to set up pricing and costs fall into two categories:</span></span>

- <span data-ttu-id="73f79-106">Žmonės</span><span class="sxs-lookup"><span data-stu-id="73f79-106">People</span></span>
- <span data-ttu-id="73f79-107">Suplanuotas darbas</span><span class="sxs-lookup"><span data-stu-id="73f79-107">Planned work</span></span>

<span data-ttu-id="73f79-108">Dėl to egzistuoja dviejų tipų kainodaros dimensijų reikšmės:</span><span class="sxs-lookup"><span data-stu-id="73f79-108">Because of this, there are two types of pricing dimension values available:</span></span>

- <span data-ttu-id="73f79-109">**Parinkčių rinkiniai** – dimensijos, kurios yra reikšmių rinkiniams skirti fiksuoti išvardijimai.</span><span class="sxs-lookup"><span data-stu-id="73f79-109">**Option sets**: Dimensions that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="73f79-110">**Objektu pagrįstos reikšmės** – dimensijos, kurios gali būti kintančiu reikšmių rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="73f79-110">**Entity-based values**: Dimensions that can be a varied set of values.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="73f79-111">Kainodaros dimensijos</span><span class="sxs-lookup"><span data-stu-id="73f79-111">Pricing dimensions</span></span>

<span data-ttu-id="73f79-112">„Dynamics 365 Project Operations“ pateikiamas su numatytuoju kainodaros dimensijų rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="73f79-112">Dynamics 365 Project Operations ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="73f79-113">Kainodaros dimensijas galite peržiūrėti apsilankę **„Project Operations“** > **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="73f79-113">You can view these pricing dimensions by going to **Project Operations** > **Parameters**.</span></span> <span data-ttu-id="73f79-114">Parametrų įraše, esančiame skirtuke **Suma pagrįstos kainodaros dimensijos**, patvirtinkite, kad vaidmuo **msdyn_resourcecategory** ir išteklių organizacinio vieneto **msdyn_organizationalunit** laukai **Taikoma pardavimui** ir **Taikoma savikainai** nustatyti į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="73f79-114">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="73f79-115">Įgalinus šiuos laukus, galėsite nustatyti kiekvieno vaidmens ir organizacinio vieneto derinio kainą ir savikainą.</span><span class="sxs-lookup"><span data-stu-id="73f79-115">With these fields enabled, you can set up the price and cost for each role and organizational unit combination.</span></span>

<span data-ttu-id="73f79-116">Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas.</span><span class="sxs-lookup"><span data-stu-id="73f79-116">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span>

## <a name="pricing-human-resource-time"></a><span data-ttu-id="73f79-117">Žmogiškųjų išteklių laiko kainodara</span><span class="sxs-lookup"><span data-stu-id="73f79-117">Pricing human resource time</span></span>
<span data-ttu-id="73f79-118">Kaip organizacijos nustato kainą žmogiškųjų išteklių laikui dažnai yra svarbus strateginis aspektas, turintis tiesioginės įtakos organizacijos pelningumui.</span><span class="sxs-lookup"><span data-stu-id="73f79-118">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="73f79-119">Dirbkite su finansų komandomis ir praktikos vadovais, kai jūsų organizacija yra pasirengusi nustatyti, kaip ji nori nustatyti sąskaitų ir savikainos tarifus, skirtus žmogiškųjų išteklių laikui.</span><span class="sxs-lookup"><span data-stu-id="73f79-119">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="73f79-120">Vienas iš kitų kainodaros aspektų yra ar reikia pakartotinai naudoti laukus arba objektus, kurie šiuo metu nėra kainodaros dimensijos, tačiau taikomi kaip jūsų organizacijos kainodaros dimensija.</span><span class="sxs-lookup"><span data-stu-id="73f79-120">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="73f79-121">Laukai, kaip **Operacijos kategorija** (**msdyn_transactioncategory**) ir **Rezervuojami ištekliai** (**bookableresource**), yra potencialių dimensijų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="73f79-121">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="73f79-122">Įvertinkite, ar jūsų kainodaros dimensija turi būti lentelė ar parinkčių rinkinys.</span><span class="sxs-lookup"><span data-stu-id="73f79-122">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="73f79-123">Jei numatote dimensijos reikšmių pakitimus, kurie viršys 10 ar 12, ir jums reikia papildomų atributų šioms reikšmėms, galite sukurti objektą, o ne parinkčių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="73f79-123">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, you could create an entity rather than an option set.</span></span> <span data-ttu-id="73f79-124">Parinkčių rinkinio tvarkymui, pavyzdžiui, įtraukiant ar šalinant reikšmes, būtinas administratorius arba kūrėjas, o įtraukti naujų eilučių į lentelę gali daugelis vartotojų.</span><span class="sxs-lookup"><span data-stu-id="73f79-124">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most users.</span></span>

<span data-ttu-id="73f79-125">Toliau pateiktame pavyzdyje pateikiami sąskaitų tarifai, nustatyti pagal vaidmenį ir išteklių organizacijos vienetą, kuriam priklauso išteklius.</span><span class="sxs-lookup"><span data-stu-id="73f79-125">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="73f79-126">Savikainos tarifai paprastai nustatomi pagal darbuotojo atlyginimų juostą ir organizacijos vienetą, kuriam jie priklauso.</span><span class="sxs-lookup"><span data-stu-id="73f79-126">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="73f79-127">Šiame pavyzdyje sąskaitų ir savikainos tarifų lentelės atrodo taip:</span><span class="sxs-lookup"><span data-stu-id="73f79-127">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="73f79-128">**Pavyzdiniai sąskaitų tarifai**</span><span class="sxs-lookup"><span data-stu-id="73f79-128">**Sample bill rates**</span></span>

| <span data-ttu-id="73f79-129">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="73f79-129">Role</span></span>        | <span data-ttu-id="73f79-130">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="73f79-130">Org Unit</span></span>    |<span data-ttu-id="73f79-131">Vienetas</span><span class="sxs-lookup"><span data-stu-id="73f79-131">Unit</span></span>      |<span data-ttu-id="73f79-132">Kaina</span><span class="sxs-lookup"><span data-stu-id="73f79-132">Price</span></span>      |<span data-ttu-id="73f79-133">Valiuta</span><span class="sxs-lookup"><span data-stu-id="73f79-133">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="73f79-134">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="73f79-134">Developer</span></span>   | <span data-ttu-id="73f79-135">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="73f79-135">Contoso US</span></span>  |<span data-ttu-id="73f79-136">Hour</span><span class="sxs-lookup"><span data-stu-id="73f79-136">Hour</span></span> | <span data-ttu-id="73f79-137">200</span><span class="sxs-lookup"><span data-stu-id="73f79-137">200</span></span>|<span data-ttu-id="73f79-138">USD</span><span class="sxs-lookup"><span data-stu-id="73f79-138">USD</span></span>     |
| <span data-ttu-id="73f79-139">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="73f79-139">Developer</span></span>   | <span data-ttu-id="73f79-140">„Danys India“</span><span class="sxs-lookup"><span data-stu-id="73f79-140">Contoso India</span></span> |<span data-ttu-id="73f79-141">Hour</span><span class="sxs-lookup"><span data-stu-id="73f79-141">Hour</span></span>|   <span data-ttu-id="73f79-142">112</span><span class="sxs-lookup"><span data-stu-id="73f79-142">112</span></span>|<span data-ttu-id="73f79-143">USD</span><span class="sxs-lookup"><span data-stu-id="73f79-143">USD</span></span>     |


<span data-ttu-id="73f79-144">**Pavyzdiniai savikainos tarifai**</span><span class="sxs-lookup"><span data-stu-id="73f79-144">**Sample cost rates**</span></span>

| <span data-ttu-id="73f79-145">Atlyginimų juosta</span><span class="sxs-lookup"><span data-stu-id="73f79-145">Salary Band</span></span>     | <span data-ttu-id="73f79-146">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="73f79-146">Org Unit</span></span>    |<span data-ttu-id="73f79-147">Vienetas</span><span class="sxs-lookup"><span data-stu-id="73f79-147">Unit</span></span>      |<span data-ttu-id="73f79-148">Kaina</span><span class="sxs-lookup"><span data-stu-id="73f79-148">Price</span></span>      |<span data-ttu-id="73f79-149">Valiuta</span><span class="sxs-lookup"><span data-stu-id="73f79-149">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="73f79-150">„My company_Band1“</span><span class="sxs-lookup"><span data-stu-id="73f79-150">My company_Band1</span></span> | <span data-ttu-id="73f79-151">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="73f79-151">Contoso US</span></span>  |<span data-ttu-id="73f79-152">Hour</span><span class="sxs-lookup"><span data-stu-id="73f79-152">Hour</span></span> | <span data-ttu-id="73f79-153">145</span><span class="sxs-lookup"><span data-stu-id="73f79-153">145</span></span>|<span data-ttu-id="73f79-154">USD</span><span class="sxs-lookup"><span data-stu-id="73f79-154">USD</span></span>     |
| <span data-ttu-id="73f79-155">„My company_Band2“</span><span class="sxs-lookup"><span data-stu-id="73f79-155">My company_Band2</span></span> | <span data-ttu-id="73f79-156">„Danys India“</span><span class="sxs-lookup"><span data-stu-id="73f79-156">Contoso India</span></span> |<span data-ttu-id="73f79-157">Hour</span><span class="sxs-lookup"><span data-stu-id="73f79-157">Hour</span></span>|   <span data-ttu-id="73f79-158">67</span><span class="sxs-lookup"><span data-stu-id="73f79-158">67</span></span>|<span data-ttu-id="73f79-159">USD</span><span class="sxs-lookup"><span data-stu-id="73f79-159">USD</span></span>     |
