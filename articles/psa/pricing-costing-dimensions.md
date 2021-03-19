---
title: Kainodaros ir įkainojimo dimensijų pagrindinis puslapis
description: Šioje temoje pateikta kainodaros dimensijų apžvalga.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 137fee27dd2302d47ae12faccde1682cff43db93
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5284143"
---
# <a name="pricing-and-costing-dimensions-home-page"></a><span data-ttu-id="e5782-103">Kainodaros ir įkainojimo dimensijų pagrindinis puslapis</span><span class="sxs-lookup"><span data-stu-id="e5782-103">Pricing and costing dimensions home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e5782-104">Dimensijos, naudojamos darbo kainodarai ir savikainai nustatyti projektų vykdymo organizacijose, yra veikiamos šių atributų:</span><span class="sxs-lookup"><span data-stu-id="e5782-104">The dimensions used to set labor pricing and costing in project-based organizations are influenced by the following attributes:</span></span>

- <span data-ttu-id="e5782-105">Darbuotojai, kurie dirba pagal jų patirtį, vaidmenį ir lokaciją</span><span class="sxs-lookup"><span data-stu-id="e5782-105">People doing work similar to their experience, role, or geography</span></span>
- <span data-ttu-id="e5782-106">Atliekamas darbas pagal jo sudėtingumą arba dienos metą</span><span class="sxs-lookup"><span data-stu-id="e5782-106">Work to be performed similar to its complexity or time of day</span></span>

<span data-ttu-id="e5782-107">Atsižvelgiant į įprastą šių darbo atributų ir žmonių, reikalingų atlikti darbui, pobūdį, išskiriami du „Project Service Automation“ kainodaros dimensijų reikšmių tipai:</span><span class="sxs-lookup"><span data-stu-id="e5782-107">Given the typical nature of these attrubutes of the work and the people required to perform the work, there are two types of pricing dimension values available in Project Service Automation:</span></span> 

- <span data-ttu-id="e5782-108">**Parinkčių rinkiniai** – atributai, kurie yra fiksuoti reikšmių rinkinių išvardijimai.</span><span class="sxs-lookup"><span data-stu-id="e5782-108">**Option sets** - Attributes that are fixed enumerations for a set of values.</span></span>
- <span data-ttu-id="e5782-109">**Objektų reikšmės** – atributai, galintys turėti įvairų reikšmių rinkinį, kuris yra ribotas, bet ilgainiui gali kisti.</span><span class="sxs-lookup"><span data-stu-id="e5782-109">**Entity-based values** - Attributes that can have a varied set of values that are finite but can change over time.</span></span>

## <a name="pricing-dimensions"></a><span data-ttu-id="e5782-110">Kainodaros dimensijos</span><span class="sxs-lookup"><span data-stu-id="e5782-110">Pricing dimensions</span></span>

<span data-ttu-id="e5782-111">PSA pateikiamas su numatytuoju kainodaros dimensijų rinkiniu.</span><span class="sxs-lookup"><span data-stu-id="e5782-111">PSA ships with a default set of pricing dimensions.</span></span> <span data-ttu-id="e5782-112">Jas galite peržiūrėti apsilankę **„Project Service“** > **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="e5782-112">You can view these by going to **Project Service** > **Parameters**.</span></span> <span data-ttu-id="e5782-113">Parametrų įraše, esančiame skirtuke **Suma pagrįstos kainodaros dimensijos**, patvirtinkite, kad vaidmuo **msdyn_resourcecategory** ir išteklių organizacinio vieneto **msdyn_organizationalunit** laukai **Taikoma pardavimui** ir **Taikoma savikainai** nustatyti į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e5782-113">In the parameter record, on the **Amount-based pricing dimensions** tab, verify that the role, **msdyn_resourcecategory** and resourcing organizational unit, **msdyn_organizationalunit** have the fields **Applicable to sales** and **Applicable to cost** set to **Yes**.</span></span> <span data-ttu-id="e5782-114">Taip galėsite nustatyti kiekvieno vaidmens ir organizacinio vieneto derinio kainą ir savikainą.</span><span class="sxs-lookup"><span data-stu-id="e5782-114">This will allow you to set up the price and cost for each role and organizational unit combination.</span></span>

![„Project Service“ parametrų ekrano kopija su pažymėtu lauku „Taikoma pardavimui“](media/PS-OOB-parameters.png)

> [!IMPORTANT]
> <span data-ttu-id="e5782-116">Jei naudojote visiškai parengtus vaidmens ir organizacinio vieneto laukus kaip kainodaros dimensijas prieš 3 PSA versiją, jokių pastebimų pakeitimų nebus.</span><span class="sxs-lookup"><span data-stu-id="e5782-116">If you have been the using out-of-the box fields of role and organizational unit as pricing dimensions prior to version 3 of PSA, there will not be any observable change.</span></span> <span data-ttu-id="e5782-117">Galite toliau naudoti „Project Service“ kaip įprasta.</span><span class="sxs-lookup"><span data-stu-id="e5782-117">You can continue to use Project Service as usual.</span></span> 

<span data-ttu-id="e5782-118">Jei jums reikia nustatyti išteklių kainą arba savikainą naudojant papildomus atributus, galite sukurti pritaikytus laukus, objektus ir dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e5782-118">If you need to price or cost for your resources using additional attributes, you can create customized fields, entities, and dimensions.</span></span> <span data-ttu-id="e5782-119">Daugiau informacijos rasite toliau pateikiamose temose, tačiau atkreipkite dėmesį, kad procedūras reikia atlikti toliau išvardyta tvarka:</span><span class="sxs-lookup"><span data-stu-id="e5782-119">For more information, see the following topics, however note that you must complete the procedures in the order listed below:</span></span>

- [<span data-ttu-id="e5782-120">Sukurti pritaikytus laukus ir objektus</span><span class="sxs-lookup"><span data-stu-id="e5782-120">Create custom fields and entities</span></span>](create-custom-fields-entities.md)
- [<span data-ttu-id="e5782-121">Pridėti pritaikytus laukus prie kainos sąrankos ir operacijos objektų</span><span class="sxs-lookup"><span data-stu-id="e5782-121">Add custom fields to price setup and transactional entities</span></span>](field-references.md)
- [<span data-ttu-id="e5782-122">Pasirinktinių laukų kaip kainodaros dimensijų nustatymas </span><span class="sxs-lookup"><span data-stu-id="e5782-122">Set up custom fields as pricing dimensions</span></span>](set-up-pricing-dimensions.md)
- [<span data-ttu-id="e5782-123">Atnaujinti priedo atributus, kad įtrauktumėte naujas kainodaros dimensijas</span><span class="sxs-lookup"><span data-stu-id="e5782-123">Update plug-in attributes to include new pricing dimensions</span></span>](update-plug-in-attributes.md)

## <a name="pricing-human-resource-time"></a><span data-ttu-id="e5782-124">Žmogiškųjų išteklių laiko kainodara</span><span class="sxs-lookup"><span data-stu-id="e5782-124">Pricing human resource time</span></span>
<span data-ttu-id="e5782-125">Kaip organizacijos nustato kainą žmogiškųjų išteklių laikui dažnai yra svarbus strateginis aspektas, turintis tiesioginės įtakos organizacijos pelningumui.</span><span class="sxs-lookup"><span data-stu-id="e5782-125">How an organization prices human resource time is often an important strategic consideration that directly affects the organization's profitability.</span></span> <span data-ttu-id="e5782-126">Dirbkite su finansų komandomis ir praktikos vadovais, kai jūsų organizacija yra pasirengusi nustatyti, kaip ji nori nustatyti sąskaitų ir savikainos tarifus, skirtus žmogiškųjų išteklių laikui.</span><span class="sxs-lookup"><span data-stu-id="e5782-126">Work with the finance teams and practice heads when your organization is ready to identify how it wants to set up bill and cost rates for human resource time.</span></span>

<span data-ttu-id="e5782-127">Vienas iš kitų kainodaros aspektų yra ar reikia pakartotinai naudoti laukus arba objektus, kurie šiuo metu nėra kainodaros dimensijos, tačiau taikomi kaip jūsų organizacijos kainodaros dimensija.</span><span class="sxs-lookup"><span data-stu-id="e5782-127">Other considerations for pricing include whether to re-use fields or entities that are not currently pricing dimensions but apply as a pricing dimension for your organization.</span></span> <span data-ttu-id="e5782-128">Laukai, kaip **Operacijos kategorija** (**msdyn_transactioncategory**) ir **Rezervuojami ištekliai** (**bookableresource**), yra potencialių dimensijų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="e5782-128">Fields like **Transaction Category** (**msdyn_transactioncategory**) and **Bookable Resource** (**bookableresource**) are examples of candidate dimensions.</span></span> 

<span data-ttu-id="e5782-129">Įvertinkite, ar jūsų kainodaros dimensija turi būti lentelė ar parinkčių rinkinys.</span><span class="sxs-lookup"><span data-stu-id="e5782-129">Consider whether your pricing dimension should be a table or an option set.</span></span> <span data-ttu-id="e5782-130">Jei numatote dimensijos reikšmių pakitimus, kurie viršys 10 ar 12, o jums reikia papildomų atributų šioms reikšmėms, sukurkite objektą, o ne parinkčių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="e5782-130">If you foresee changes to the values of a dimension which will exceed 10 or 12 and you need additional attributes on these values, create an entity rather than an option set.</span></span> <span data-ttu-id="e5782-131">Parinkčių rinkinio tvarkymui, pavyzdžiui, įtraukiant ar šalinant reikšmes, būtinas administratorius arba kūrėjas, o įtraukti naujas eilutes į lentelę gali dauguma verslo vartotojų.</span><span class="sxs-lookup"><span data-stu-id="e5782-131">Maintaining an option set, such as adding or removing values, requires an admin or developer whereas adding new rows to a table can be done by most business users.</span></span>

<span data-ttu-id="e5782-132">Toliau pateiktame pavyzdyje pateikiami sąskaitų tarifai, nustatyti pagal vaidmenį ir išteklių organizacijos vienetą, kuriam priklauso išteklius.</span><span class="sxs-lookup"><span data-stu-id="e5782-132">The following example shows bill rates that are set up based on the role and the resourcing org unit to which the resource belongs.</span></span> <span data-ttu-id="e5782-133">Savikainos tarifai paprastai nustatomi pagal darbuotojo atlyginimų juostą ir organizacijos vienetą, kuriam jie priklauso.</span><span class="sxs-lookup"><span data-stu-id="e5782-133">Cost rates are typically based on the salary band of the employee and the org unit that they belong to.</span></span> <span data-ttu-id="e5782-134">Šiame pavyzdyje sąskaitų ir savikainos tarifų lentelės atrodo taip:</span><span class="sxs-lookup"><span data-stu-id="e5782-134">In this example, the bill rate and cost rate tables will look like the following.</span></span>

<span data-ttu-id="e5782-135">**Pavyzdiniai sąskaitų tarifai**</span><span class="sxs-lookup"><span data-stu-id="e5782-135">**Sample bill rates**</span></span>

| <span data-ttu-id="e5782-136">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="e5782-136">Role</span></span>        | <span data-ttu-id="e5782-137">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="e5782-137">Org Unit</span></span>    |<span data-ttu-id="e5782-138">Vienetas</span><span class="sxs-lookup"><span data-stu-id="e5782-138">Unit</span></span>      |<span data-ttu-id="e5782-139">Kaina</span><span class="sxs-lookup"><span data-stu-id="e5782-139">Price</span></span>      |<span data-ttu-id="e5782-140">Valiuta</span><span class="sxs-lookup"><span data-stu-id="e5782-140">Currency</span></span>  |
| ------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e5782-141">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="e5782-141">Developer</span></span>   | <span data-ttu-id="e5782-142">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="e5782-142">Contoso US</span></span>  |<span data-ttu-id="e5782-143">Hour</span><span class="sxs-lookup"><span data-stu-id="e5782-143">Hour</span></span> | <span data-ttu-id="e5782-144">200</span><span class="sxs-lookup"><span data-stu-id="e5782-144">200</span></span>|<span data-ttu-id="e5782-145">USD</span><span class="sxs-lookup"><span data-stu-id="e5782-145">USD</span></span>     |
| <span data-ttu-id="e5782-146">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="e5782-146">Developer</span></span>   | <span data-ttu-id="e5782-147">„Danys India“</span><span class="sxs-lookup"><span data-stu-id="e5782-147">Contoso India</span></span> |<span data-ttu-id="e5782-148">Hour</span><span class="sxs-lookup"><span data-stu-id="e5782-148">Hour</span></span>|   <span data-ttu-id="e5782-149">112</span><span class="sxs-lookup"><span data-stu-id="e5782-149">112</span></span>|<span data-ttu-id="e5782-150">USD</span><span class="sxs-lookup"><span data-stu-id="e5782-150">USD</span></span>     |


<span data-ttu-id="e5782-151">**Pavyzdiniai savikainos tarifai**</span><span class="sxs-lookup"><span data-stu-id="e5782-151">**Sample cost rates**</span></span>

| <span data-ttu-id="e5782-152">Atlyginimų juosta</span><span class="sxs-lookup"><span data-stu-id="e5782-152">Salary Band</span></span>     | <span data-ttu-id="e5782-153">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="e5782-153">Org Unit</span></span>    |<span data-ttu-id="e5782-154">Vienetas</span><span class="sxs-lookup"><span data-stu-id="e5782-154">Unit</span></span>      |<span data-ttu-id="e5782-155">Kaina</span><span class="sxs-lookup"><span data-stu-id="e5782-155">Price</span></span>      |<span data-ttu-id="e5782-156">Valiuta</span><span class="sxs-lookup"><span data-stu-id="e5782-156">Currency</span></span>  |
| ----------------|-------------|----------|----------:|----------|
| <span data-ttu-id="e5782-157">„My company_Band1“</span><span class="sxs-lookup"><span data-stu-id="e5782-157">My company_Band1</span></span> | <span data-ttu-id="e5782-158">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="e5782-158">Contoso US</span></span>  |<span data-ttu-id="e5782-159">Hour</span><span class="sxs-lookup"><span data-stu-id="e5782-159">Hour</span></span> | <span data-ttu-id="e5782-160">145</span><span class="sxs-lookup"><span data-stu-id="e5782-160">145</span></span>|<span data-ttu-id="e5782-161">USD</span><span class="sxs-lookup"><span data-stu-id="e5782-161">USD</span></span>     |
| <span data-ttu-id="e5782-162">„My company_Band2“</span><span class="sxs-lookup"><span data-stu-id="e5782-162">My company_Band2</span></span> | <span data-ttu-id="e5782-163">„Danys India“</span><span class="sxs-lookup"><span data-stu-id="e5782-163">Contoso India</span></span> |<span data-ttu-id="e5782-164">Hour</span><span class="sxs-lookup"><span data-stu-id="e5782-164">Hour</span></span>|   <span data-ttu-id="e5782-165">67</span><span class="sxs-lookup"><span data-stu-id="e5782-165">67</span></span>|<span data-ttu-id="e5782-166">USD</span><span class="sxs-lookup"><span data-stu-id="e5782-166">USD</span></span>     |


[!INCLUDE[footer-include](../includes/footer-banner.md)]