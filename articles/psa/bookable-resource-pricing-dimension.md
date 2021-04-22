---
title: Rezervuojamų išteklių naudojimas kaip kainodaros dimensijos
description: Šioje temoje pateikiama informacijos apie rezervuojamų išteklių naudojimą kaip kainodaros dimensijos.
author: Rumant
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
ms.openlocfilehash: d3f5ed7da5972cec5b22524bdcb3dc34a83eee28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290954"
---
# <a name="use-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="f7860-103">Rezervuojamų išteklių naudojimas kaip kainodaros dimensijos</span><span class="sxs-lookup"><span data-stu-id="f7860-103">Use bookable resource as a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f7860-104">Šioje temoje pateikiama informacijos apie rezervuojamų išteklių naudojimą kaip kainodaros dimensijos.</span><span class="sxs-lookup"><span data-stu-id="f7860-104">This topic provides information about using a bookable resource as a pricing dimension.</span></span> <span data-ttu-id="f7860-105">Prieš pradėdami, jei dar nesukūrėte kainodaros dimensijos sprendimo, turėsite sukurti naują sprendimą.</span><span class="sxs-lookup"><span data-stu-id="f7860-105">Before you begin, if you have not already created a pricing dimension solution, you will need to create a new one.</span></span> <span data-ttu-id="f7860-106">Jei jau turite kainodaros dimensijos sprendimą, galite atlikti šio sprendimo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="f7860-106">If you already have a pricing dimension solution, then you can make your changes in that solution.</span></span> <span data-ttu-id="f7860-107">Jei savo organizacijai nesukūrėte naujo kainodaros dimensijos sprendimo, atlikite procedūras, nurodytas temoje [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities.md).</span><span class="sxs-lookup"><span data-stu-id="f7860-107">If you have not created a new pricing dimension solution for your organization, complete the procedures in the [Create custom fields and entities](create-custom-fields-entities.md) topic.</span></span>

## <a name="add-bookable-resource-to-forms-and-views"></a><span data-ttu-id="f7860-108">Rezervuojamų išteklių įtraukimas į formas ir rodinius</span><span class="sxs-lookup"><span data-stu-id="f7860-108">Add bookable resource to forms and views</span></span>
<span data-ttu-id="f7860-109">Norint, kad laukai būtų rodomi kainodaros dimensijos sprendimo UI, reikia peržiūrėti visų pagrindinių „Project Service“ objektų formas ir rodinius ir į juos įtraukti šiuos laukus.</span><span class="sxs-lookup"><span data-stu-id="f7860-109">To make the fields visible in the UI in the pricing dimension solution, you will need to walk through all of the forms and views of the key Project Service entities and add these fields to the forms and views of those entities.</span></span>
<span data-ttu-id="f7860-110">Tolesnėje lentelėje pateikiamas išsamus parengtų naudoti formų ir rodinių, išvardytų pagal objektus, sąrašas, kurį reikės atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="f7860-110">The following table is a comprehensive list of the out-of-the box forms and views, listed by entity, that will need to be updated.</span></span> <span data-ttu-id="f7860-111">Jei šių objektų tinkinimuose yra papildomų rodinių arba formų, įtraukite šiuos naujus laukus ir į juos.</span><span class="sxs-lookup"><span data-stu-id="f7860-111">If there are any additional views or forms in your customizations on these entities, add the new fields to those as well.</span></span>
<span data-ttu-id="f7860-112">Atidarykite kainodaros dimensijos sprendimo langą Sprendimų naršyklė ir spustelėkite **Publikuoti visus tinkinimus**.</span><span class="sxs-lookup"><span data-stu-id="f7860-112">Open Solution Explorer for the pricing dimension solution and then click **Publish All Customizations**.</span></span>


|   <span data-ttu-id="f7860-113">Objektas</span><span class="sxs-lookup"><span data-stu-id="f7860-113">Entity</span></span>        | <span data-ttu-id="f7860-114">Formos</span><span class="sxs-lookup"><span data-stu-id="f7860-114">Forms</span></span>   |<span data-ttu-id="f7860-115">Rodiniai</span><span class="sxs-lookup"><span data-stu-id="f7860-115">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="f7860-116">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="f7860-116">Role Price</span></span>|<span data-ttu-id="f7860-117">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-117">• Information</span></span> |<span data-ttu-id="f7860-118">• Aktyviųjų išteklių kategorijų kainos</span><span class="sxs-lookup"><span data-stu-id="f7860-118">• Active Resource Category Prices</span></span><br> <span data-ttu-id="f7860-119">• Išteklių kategorijos kainos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-119">• Resource Category Price Associated View</span></span>|
|  <span data-ttu-id="f7860-120">Vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="f7860-120">Role Price Markup</span></span>|<span data-ttu-id="f7860-121">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-121">• Information</span></span>|<span data-ttu-id="f7860-122">• Aktyviojo vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="f7860-122">• Active Role Price Markup</span></span><br><span data-ttu-id="f7860-123">• Vaidmens kainos antkainio susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-123">• Role Price Markup Associated View</span></span>|
|  <span data-ttu-id="f7860-124">Pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-124">Quote line detail</span></span>|<span data-ttu-id="f7860-125">• Projekto informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-125">• Project Information</span></span><br><span data-ttu-id="f7860-126">• Spartusis projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7860-126">• Project Quick Create</span></span>|<span data-ttu-id="f7860-127">• Aktyviojo pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-127">• Active Quote Line Detail</span></span><br><span data-ttu-id="f7860-128">• Jungtinių pasiūlymo eilučių informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-128">• Combined Quote Line Details</span></span><br><span data-ttu-id="f7860-129">• Pasiūlymo eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-129">• Quote Line Detail associated view</span></span>|
|  <span data-ttu-id="f7860-130">• Projekto sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-130">Project Contract line detail</span></span>|<span data-ttu-id="f7860-131">• Projekto informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-131">• Project Information</span></span><br><span data-ttu-id="f7860-132">• Spartusis projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7860-132">• Project Quick Create</span></span>|<span data-ttu-id="f7860-133">• Jungtinių sutarties eilučių informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-133">• Combined Contract line Details</span></span><br><span data-ttu-id="f7860-134">• Aktyvios sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-134">• Active Contract Line Details</span></span><br><span data-ttu-id="f7860-135">• Sutarties eilutės išsamios informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-135">• Contract Line Detail associated view</span></span>|
|  <span data-ttu-id="f7860-136">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="f7860-136">Project Task</span></span>|<span data-ttu-id="f7860-137">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-137">• Information</span></span><br><span data-ttu-id="f7860-138">• Nauja forma</span><span class="sxs-lookup"><span data-stu-id="f7860-138">• New Form</span></span>||
|  <span data-ttu-id="f7860-139">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="f7860-139">Project Team Member</span></span>|<span data-ttu-id="f7860-140">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-140">• Information</span></span><br><span data-ttu-id="f7860-141">• Nauja forma</span><span class="sxs-lookup"><span data-stu-id="f7860-141">• New Form</span></span>|<span data-ttu-id="f7860-142">• Aktyvieji projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="f7860-142">• Active Project Team Members</span></span><br><span data-ttu-id="f7860-143">• Projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="f7860-143">• Project Team Members</span></span><br><span data-ttu-id="f7860-144">• Projekto komandos narių susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-144">• Project Team members associated View</span></span>|
|  <span data-ttu-id="f7860-145">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="f7860-145">Time Entry</span></span>|<span data-ttu-id="f7860-146">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-146">• Information</span></span><br><span data-ttu-id="f7860-147">• Laiko įrašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7860-147">• Create Time Entry</span></span>|<span data-ttu-id="f7860-148">• Mano laiko įrašai pagal datą</span><span class="sxs-lookup"><span data-stu-id="f7860-148">• My Time Entries By Date</span></span><br><span data-ttu-id="f7860-149">• Mano laiko įrašai šią savaitę</span><span class="sxs-lookup"><span data-stu-id="f7860-149">• My time Entries for this week</span></span><br><span data-ttu-id="f7860-150">• Laiko įrašai, skirti patvirtinti</span><span class="sxs-lookup"><span data-stu-id="f7860-150">• Time entries for approval</span></span>|
|  <span data-ttu-id="f7860-151">Žurnalo eilutė</span><span class="sxs-lookup"><span data-stu-id="f7860-151">Journal Line</span></span>|<span data-ttu-id="f7860-152">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-152">• Information</span></span><br><span data-ttu-id="f7860-153">• Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7860-153">• Quick create</span></span>|<span data-ttu-id="f7860-154">• Aktyviojo žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="f7860-154">• Active journal lines</span></span><br><span data-ttu-id="f7860-155">• Žurnalo eilučių susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-155">• Journal Line associated view</span></span>|
|  <span data-ttu-id="f7860-156">Sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-156">Invoice Line Detail</span></span>|<span data-ttu-id="f7860-157">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-157">• Information</span></span><br><span data-ttu-id="f7860-158">• Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7860-158">• Quick create</span></span>|<span data-ttu-id="f7860-159">• Aktyvioji sąskaitos faktūros eilutės išsami informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-159">• Active Invoice Line Details</span></span><br><span data-ttu-id="f7860-160">• Apmokestinamos sąskaitų faktūrų operacijos</span><span class="sxs-lookup"><span data-stu-id="f7860-160">• Chargeable Invoice Transactions</span></span><br><span data-ttu-id="f7860-161">• Nemokamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="f7860-161">• Complimentary Invoice Transactions</span></span><br><span data-ttu-id="f7860-162">• Sąskaitos faktūros eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-162">• Invoice Line Detail associated view</span></span><br><span data-ttu-id="f7860-163">• Neapmokestinamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="f7860-163">• Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="f7860-164">Faktinis</span><span class="sxs-lookup"><span data-stu-id="f7860-164">Actual</span></span>|<span data-ttu-id="f7860-165">• Informacija</span><span class="sxs-lookup"><span data-stu-id="f7860-165">• Information</span></span><br><span data-ttu-id="f7860-166">• Aktyvieji faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="f7860-166">• Active Actuals</span></span>|<span data-ttu-id="f7860-167">• Faktinis susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="f7860-167">• Actual Associated view</span></span>|

## <a name="set-up-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="f7860-168">Rezervuojamų išteklių nustatymas kaip kainodaros dimensijos</span><span class="sxs-lookup"><span data-stu-id="f7860-168">Set up bookable resource as a pricing dimension</span></span>

1. <span data-ttu-id="f7860-169">Žiniatinklio sąsajoje eikite į **Project Service** > **Parametrai** > **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f7860-169">In the web interface, go to **Project Service** > **Settings** > **Parameters**.</span></span> <span data-ttu-id="f7860-170">Puslapio **Parametrai** skirtuke **Kiekiu pagrįstos kainodaros dimensijos** atkreipkite dėmesį, kad tinklelyje rodomi kainodaros dimensijų objekto įrašai.</span><span class="sxs-lookup"><span data-stu-id="f7860-170">On the **Parameter** page, on the **Amount-Based Pricing Dimensions** tab, notice that the grid on the tab shows the records in the pricing dimensions entity.</span></span> 
2. <span data-ttu-id="f7860-171">Įtraukite **Rezervuojamą išteklių** į šį kainodaros dimensijų sąrašą kaip **msdyn_bookableresource**.</span><span class="sxs-lookup"><span data-stu-id="f7860-171">Add **Bookable Resource** to this list of pricing dimensions as **msdyn_bookableresource**.</span></span> 
3. <span data-ttu-id="f7860-172">Nurodykite kontekstą, kuriame rezervuojamas išteklius veiks kaip kainodaros dimensija, ir nustatykite reikšmes **Taikoma savikainai** ir **Taikoma pardavimui**.</span><span class="sxs-lookup"><span data-stu-id="f7860-172">Indicate the context in which the bookable resource works as a pricing dimension and set the **Applicable to cost** and **Applicable to sales** values.</span></span>
4. <span data-ttu-id="f7860-173">Lauke **Dimensijos tipas** pažymėkite **Pagrįsta kiekiu**.</span><span class="sxs-lookup"><span data-stu-id="f7860-173">In the **Dimension Type** field, select **Amount-based**.</span></span> 
5. <span data-ttu-id="f7860-174">Pasirinkite rezervuojamo ištekliaus savikainos ir pardavimo prioritetą.</span><span class="sxs-lookup"><span data-stu-id="f7860-174">Select the cost and sales priority for the bookable resource.</span></span> <span data-ttu-id="f7860-175">Paprastai, kai rezervuojamas išteklius įtraukiamas kaip kainodaros dimensija, jam suteikiamas didžiausias prioritetas, todėl nustatoma parinktis **1** (arba **0**, atsižvelgiant į tai, kaip skaičiuojate prioritetą), kad būtų užtikrintas toks veikimas.</span><span class="sxs-lookup"><span data-stu-id="f7860-175">Typically, when included as a pricing dimension, a bookable resource has the highest priority so setting this to **1** (or **0** depending on how you count the priority) would ensure that behavior.</span></span>

## <a name="set-up-pricing-dimension-field-names"></a><span data-ttu-id="f7860-176">Kainodaros dimensijų laukų pavadinimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f7860-176">Set up pricing dimension field names</span></span>

<span data-ttu-id="f7860-177">Kai lentelėje **Vaidmens kaina** kainodaros dimensijos lauko pavadinimas skiriasi nuo tos dimensijos lauko pavadinimo bet kuriame kitame objekte, kuriame numatytosios kainos turi veikti, kainodaros dimensijos įraše būtina pranešti, kad pavadinimai skiriasi.</span><span class="sxs-lookup"><span data-stu-id="f7860-177">When the field name of a pricing dimension in the **Role Price** table is different from its field name in any of the other entities where price defaulting needs to work, the pricing dimension record must be made aware of the different names.</span></span>    
<span data-ttu-id="f7860-178">Rezervuojamo ištekliaus lauko pavadinimas (**msdyn_bookableresourceid**), esantis objekte **Projekto komandos nariai**, nežymiai skiriasi nuo jo pavadinimo objekte **vaidmens kaina** (**msdyn_bookableresource**).</span><span class="sxs-lookup"><span data-stu-id="f7860-178">For bookable resource, the **Project Team Members** entity has a slightly different field name (**msdyn_bookableresourceid**) from what it is called on the **Role price** entity (**msdyn_bookableresource**).</span></span> <span data-ttu-id="f7860-179">Apie tai būtina pranešti kainodaros dimensijos įraše **msdyn_bookableresource**.</span><span class="sxs-lookup"><span data-stu-id="f7860-179">The pricing dimension record for **msydn_bookableresource** must be made aware of this.</span></span> 
1. <span data-ttu-id="f7860-180">Norėdami tai atlikti, dukart spustelėkite tinklelyje **Kainodaros dimensijos** esančią eilutę ir kad atidarykite dimensijos **msdyn_bookableresource** puslapį.</span><span class="sxs-lookup"><span data-stu-id="f7860-180">To do this, double-click the row in the **Pricing Dimensions** grid to open the dimension page of **msdyn_bookableresource**.</span></span>
2. <span data-ttu-id="f7860-181">Dimensijos puslapio skirtuke **Susiję** spustelėkite **Kainodaros dimensijų laukų pavadinimai**.</span><span class="sxs-lookup"><span data-stu-id="f7860-181">On dimension page, on the **Related** tab, click **Pricing Dimension Field Names**.</span></span>

 ![Skirtukas Kainodaros dimensijos laukų pavadinimai](media/PD-fieldname.png)

4. <span data-ttu-id="f7860-183">Atsidariusiame susietajame rodinyje spustelėkite **Įtraukti naują kainodaros dimensijos lauko pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="f7860-183">On the associated view that opens, click **Add New Pricing Dimension Field Name**.</span></span>

 ![Naujų kainodaros dimensijų laukų pavadinimį įtraukimas](media/Add-NewPD-fieldname.png)


<span data-ttu-id="f7860-185">Bus atidarytas dimensijos **msdyn_bookableresource** puslapis **Naujas kainodaros dimensijos lauko pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="f7860-185">This opens the **New Pricing dimension field name** page for **msdyn_bookableresource**.</span></span> 

5. <span data-ttu-id="f7860-186">Į lauką **Objekto loginis pavadinimas** įtraukite **msdyn_projectteam**, o į lauką **Lauko pavadinimas** – **msdyn_bookableresourceid**.</span><span class="sxs-lookup"><span data-stu-id="f7860-186">Add **msdyn_projectteam** to the **Entity Locigal Name** field and **msdyn_bookableresourceid** to the **Field Name** field.</span></span> <span data-ttu-id="f7860-187">Išsaugokite įrašą.</span><span class="sxs-lookup"><span data-stu-id="f7860-187">Save the record.</span></span>

 ![Naujų kainodaros dimensijų laukų pavadinimų forma](media/PD-fieldname-Added.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]