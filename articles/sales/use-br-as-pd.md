---
title: Rezervuojamų išteklių kaip kainodaros dimensijos naudojimas
description: Šioje temoje pateikiama informacijos, kaip naudoti rezervuojamus išteklius kaip kainodaros dimensiją.
author: Rumant
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0c5cb85f7c43f7b2fd9c367d7f7ac9c3250e0a1
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643093"
---
# <a name="use-a-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="d10b3-103">Rezervuojamų išteklių kaip kainodaros dimensijos naudojimas</span><span class="sxs-lookup"><span data-stu-id="d10b3-103">Use a bookable resource as a pricing dimension</span></span>

 <span data-ttu-id="d10b3-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="d10b3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

<span data-ttu-id="d10b3-105">Šioje temoje pateikiama informacijos, kaip naudoti rezervuojamus išteklius kaip kainodaros dimensiją.</span><span class="sxs-lookup"><span data-stu-id="d10b3-105">This topic provides information about how to use a bookable resource as a pricing dimension.</span></span> <span data-ttu-id="d10b3-106">Jei jūsų kainodaros strategijoje nustatyta, kad kiekvienas rezervuojamas išteklius turi turėti konkrečią kainą ar įkainį, naudokite rezervuojamus išteklius kaip kainodaros dimensiją.</span><span class="sxs-lookup"><span data-stu-id="d10b3-106">If your pricing strategy is set up so that each bookable resource must have a specific price or cost rate, use a bookable resource as a pricing dimension.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d10b3-107">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="d10b3-107">Prerequisites</span></span>
<span data-ttu-id="d10b3-108">Kad galėtumėte atlikti šioje temoje nurodytus veiksmus, turite turėti naują savo organizacijos kainodaros dimensijos sprendimą.</span><span class="sxs-lookup"><span data-stu-id="d10b3-108">Before you complete the procedures in this topic, you must have a new pricing dimension solution for your organization.</span></span> <span data-ttu-id="d10b3-109">Jei dar jo nesukūrėte, žr. [Pasirinktinių laukų ir objektų kūrimas](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="d10b3-109">If you haven't already created one, see [Create custom fields and entities](../pricing-costing/create-custom-fields-entities-pricing-dimensions.md).</span></span>

## <a name="add-the-bookable-resource-field-to-forms-and-views"></a><span data-ttu-id="d10b3-110">Rezervuojamų išteklių lauko įtraukimas į formas ir rodinius</span><span class="sxs-lookup"><span data-stu-id="d10b3-110">Add the Bookable Resource field to forms and views</span></span>
<span data-ttu-id="d10b3-111">Jei norite, kad laukas **Rezervuojami ištekliai** būtų rodomas kainodaros dimensijos sprendime, reikia pridėti lauką prie visų formų ir rodinių kaip objektą.</span><span class="sxs-lookup"><span data-stu-id="d10b3-111">To make the **Bookable Resource** field visible in the pricing dimension solution, you need to add the field to all the forms and views as an entity.</span></span>

<span data-ttu-id="d10b3-112">Toliau esančioje lentelėje pateiktos visos paruoštos naudoti formos ir rodiniai pagal objektą.</span><span class="sxs-lookup"><span data-stu-id="d10b3-112">The following table lists all of the out-of-the box forms and views, by entity.</span></span> <span data-ttu-id="d10b3-113">Taip pat turėsite pridėti naują lauką prie bet kokių papildomų formų ar rodinių, esančių jūsų tinkintuose objektuose.</span><span class="sxs-lookup"><span data-stu-id="d10b3-113">You will also need to add the new field to any additional forms or views in your customized entities.</span></span>

|   <span data-ttu-id="d10b3-114">Entity</span><span class="sxs-lookup"><span data-stu-id="d10b3-114">Entity</span></span>        | <span data-ttu-id="d10b3-115">Formos</span><span class="sxs-lookup"><span data-stu-id="d10b3-115">Forms</span></span>   |<span data-ttu-id="d10b3-116">Peržiūros</span><span class="sxs-lookup"><span data-stu-id="d10b3-116">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="d10b3-117">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="d10b3-117">Role Price</span></span>| <span data-ttu-id="d10b3-118">Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-118">Information</span></span> | <span data-ttu-id="d10b3-119">- Aktyvių išteklių kategorijų kainos</span><span class="sxs-lookup"><span data-stu-id="d10b3-119">- Active Resource Category Prices</span></span><br> <span data-ttu-id="d10b3-120">- Išteklių kategorijos kainos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-120">- Resource Category Price Associated</span></span> |
|  <span data-ttu-id="d10b3-121">Vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="d10b3-121">Role Price Markup</span></span>| <span data-ttu-id="d10b3-122">Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-122">Information</span></span>| <span data-ttu-id="d10b3-123">- Aktyvaus vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="d10b3-123">- Active Role Price Markup</span></span><br><span data-ttu-id="d10b3-124">- Vaidmens kainos antkainio susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-124">- Role Price Markup Associated</span></span> |
|  <span data-ttu-id="d10b3-125">Pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-125">Quote line detail</span></span>| <span data-ttu-id="d10b3-126">- Projekto informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-126">- Project Information</span></span><br><span data-ttu-id="d10b3-127">- Spartusis projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="d10b3-127">- Project Quick Create</span></span>| <span data-ttu-id="d10b3-128">- Aktyvaus pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-128">- Active Quote Line Detail</span></span><br><span data-ttu-id="d10b3-129">- Jungtinių pasiūlymo eilučių informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-129">- Combined Quote Line Details</span></span><br><span data-ttu-id="d10b3-130">- Pasiūlymo eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-130">- Quote Line Detail Associated</span></span> |
|  <span data-ttu-id="d10b3-131">• Projekto sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-131">Project Contract line detail</span></span>| <span data-ttu-id="d10b3-132">- Projekto informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-132">- Project Information</span></span><br><span data-ttu-id="d10b3-133">- Spartusis projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="d10b3-133">- Project Quick Create</span></span>| <span data-ttu-id="d10b3-134">- Jungtinių sutarties eilučių informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-134">- Combined Contract Line Details</span></span><br><span data-ttu-id="d10b3-135">- Aktyvios sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-135">- Active Contract Line Details</span></span><br><span data-ttu-id="d10b3-136">- Sutarties eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-136">- Contract Line Detail Associated</span></span> |
|  <span data-ttu-id="d10b3-137">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="d10b3-137">Project Task</span></span>| <span data-ttu-id="d10b3-138">- Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-138">- Information</span></span><br><span data-ttu-id="d10b3-139">- Nauja forma</span><span class="sxs-lookup"><span data-stu-id="d10b3-139">- New Form</span></span>| &nbsp; |
|  <span data-ttu-id="d10b3-140">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="d10b3-140">Project Team Member</span></span>| <span data-ttu-id="d10b3-141">- Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-141">- Information</span></span><br><span data-ttu-id="d10b3-142">- Nauja forma</span><span class="sxs-lookup"><span data-stu-id="d10b3-142">- New Form</span></span>| <span data-ttu-id="d10b3-143">- Aktyvūs projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="d10b3-143">- Active Project Team Members</span></span><br><span data-ttu-id="d10b3-144">- Projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="d10b3-144">- Project Team Members</span></span><br><span data-ttu-id="d10b3-145">- Projekto komandos narių susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-145">- Project Team members Associated</span></span> |
|  <span data-ttu-id="d10b3-146">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="d10b3-146">Time Entry</span></span>| <span data-ttu-id="d10b3-147">- Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-147">- Information</span></span><br><span data-ttu-id="d10b3-148">- Kurti laiko įrašą</span><span class="sxs-lookup"><span data-stu-id="d10b3-148">- Create Time Entry</span></span>| <span data-ttu-id="d10b3-149">- Mano laiko įrašai pagal datą</span><span class="sxs-lookup"><span data-stu-id="d10b3-149">- My Time Entries By Date</span></span><br><span data-ttu-id="d10b3-150">- Mano laiko įrašai šią savaitę</span><span class="sxs-lookup"><span data-stu-id="d10b3-150">- My Time Entries for this Week</span></span><br><span data-ttu-id="d10b3-151">- Laiko įrašai, skirti patvirtinti</span><span class="sxs-lookup"><span data-stu-id="d10b3-151">- Time Entries for Approval</span></span>|
|  <span data-ttu-id="d10b3-152">Žurnalo eilutė</span><span class="sxs-lookup"><span data-stu-id="d10b3-152">Journal Line</span></span>| <span data-ttu-id="d10b3-153">- Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-153">- Information</span></span><br><span data-ttu-id="d10b3-154">- Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="d10b3-154">- Quick Create</span></span>| <span data-ttu-id="d10b3-155">- Aktyvaus žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="d10b3-155">- Active Journal Lines</span></span><br><span data-ttu-id="d10b3-156">- Žurnalo eilučių susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-156">- Journal Line Associated</span></span> |
|  <span data-ttu-id="d10b3-157">Sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-157">Invoice Line Detail</span></span>| <span data-ttu-id="d10b3-158">- Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-158">- Information</span></span><br><span data-ttu-id="d10b3-159">- Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="d10b3-159">- Quick Create</span></span>| <span data-ttu-id="d10b3-160">- Aktyvios sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-160">- Active Invoice Line Details</span></span><br><span data-ttu-id="d10b3-161">- Apmokestinamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="d10b3-161">- Chargeable Invoice Transactions</span></span><br><span data-ttu-id="d10b3-162">- Nemokamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="d10b3-162">- Complimentary Invoice Transactions</span></span><br><span data-ttu-id="d10b3-163">- Sąskaitos faktūros eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-163">- Invoice Line Detail Associated</span></span> <br><span data-ttu-id="d10b3-164">- Neapmokestinamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="d10b3-164">- Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="d10b3-165">Faktinis</span><span class="sxs-lookup"><span data-stu-id="d10b3-165">Actual</span></span>| <span data-ttu-id="d10b3-166">- Informacija</span><span class="sxs-lookup"><span data-stu-id="d10b3-166">- Information</span></span><br><span data-ttu-id="d10b3-167">- Aktyvūs faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="d10b3-167">- Active Actuals</span></span>| <span data-ttu-id="d10b3-168">Faktinis susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="d10b3-168">Actual Associated</span></span> |

## <a name="set-up-a-bookable-resource-as-a-pricing-dimension"></a><span data-ttu-id="d10b3-169">Rezervuojamų išteklių kaip kainodaros dimensijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="d10b3-169">Set up a bookable resource as a pricing dimension</span></span>
<span data-ttu-id="d10b3-170">Norėdami nustatyti rezervuojamus išteklius kaip kainodaros dimensiją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d10b3-170">To set up a bookable resource as a pricing dimension, follow these steps:</span></span>

1. <span data-ttu-id="d10b3-171">Eikite į **Parametrai** > **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-171">Go to **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="d10b3-172">Puslapio **Parametras** skirtuke **Suma pagrįstos kainodaros dimensijos** įsitikinkite, kad tinklelyje rodomi objekto **Kainodaros dimensijos** įrašai.</span><span class="sxs-lookup"><span data-stu-id="d10b3-172">On the **Parameter** page, on the **Amount-Based Pricing Dimensions** tab, verify that the grid shows the records in the **Pricing Dimensions** entity.</span></span> 
2. <span data-ttu-id="d10b3-173">Įtraukite **Rezervuojamą išteklių** į šį kainodaros dimensijų sąrašą kaip **msdyn_bookableresource**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-173">Add **Bookable Resource** to this list of pricing dimensions as **msdyn_bookableresource**.</span></span> 
3. <span data-ttu-id="d10b3-174">Dalyse **Taikoma savikainai** ir **Taikoma pardavimui** pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d10b3-174">In **Applicable to cost** and **Applicable to sales**, select a value.</span></span>
4. <span data-ttu-id="d10b3-175">Dalyje **Dimensijos tipas** pasirinkite **Pagrįsta suma**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-175">In **Dimension Type**, select **Amount-based**.</span></span> 
5. <span data-ttu-id="d10b3-176">Pasirinkite rezervuojamo ištekliaus savikainos ir pardavimo prioritetą.</span><span class="sxs-lookup"><span data-stu-id="d10b3-176">Select the cost and sales priority for the bookable resource.</span></span> <span data-ttu-id="d10b3-177">Paprastai rezervuojamiems ištekliams taikomas didžiausias prioritetas, kai jie įtraukiami kaip kainodaros dimensija.</span><span class="sxs-lookup"><span data-stu-id="d10b3-177">Typically, a bookable resource has the highest priority when included as a pricing dimension.</span></span> <span data-ttu-id="d10b3-178">Nustatykite prioriteto reikšmę **1** (arba **0**, atsižvelgiant į tai, kaip taikote prioritetus), kad užtikrintumėte šį veikimo principą.</span><span class="sxs-lookup"><span data-stu-id="d10b3-178">Set the priority to **1** (or **0** depending on how you count the priority) to ensure this behavior.</span></span>

## <a name="set-up-pricing-dimension-field-names"></a><span data-ttu-id="d10b3-179">Kainodaros dimensijų laukų pavadinimų nustatymas</span><span class="sxs-lookup"><span data-stu-id="d10b3-179">Set up pricing dimension field names</span></span>

<span data-ttu-id="d10b3-180">Kai lentelėje **Vaidmens kaina** kainodaros dimensijos lauko pavadinimas skiriasi nuo tos dimensijos lauko pavadinimo bet kuriame kitame objekte, kuriame naudojama numatytoji kaina, kainodaros dimensijos įraše būtina nurodyti, kad pavadinimai skiriasi.</span><span class="sxs-lookup"><span data-stu-id="d10b3-180">When the field name of a pricing dimension in the **Role Price** table is different from the field name in any of the other entities where the default price is used, the pricing dimension record must be notified of the different names.</span></span>  

<span data-ttu-id="d10b3-181">Objekto **Projekto komandos nariai** rezervuojamų išteklių lauko pavadinimas šiek tiek skiriasi nuo pavadinimo objekte **Vaidmens kaina**:</span><span class="sxs-lookup"><span data-stu-id="d10b3-181">For a bookable resource, the **Project Team Members** entity has a slightly different field name from what it is called on the **Role Price** entity:</span></span> 

 - <span data-ttu-id="d10b3-182">Objektas **Projekto komandos nariai** = **msdyn_bookableresourceid**</span><span class="sxs-lookup"><span data-stu-id="d10b3-182">**Project Team Members** entity = **msdyn_bookableresourceid**</span></span>
 - <span data-ttu-id="d10b3-183">Objektas **Vaidmens kaina** = **msdyn_bookableresource**</span><span class="sxs-lookup"><span data-stu-id="d10b3-183">**Role Price** entity = **msdyn_bookableresource**</span></span>

<span data-ttu-id="d10b3-184">Šį skirtumą būtina nurodyti **msydn_bookableresource** kainodaros dimensijos įraše.</span><span class="sxs-lookup"><span data-stu-id="d10b3-184">The pricing dimension record for **msydn_bookableresource** must be notified of this difference.</span></span>

1. <span data-ttu-id="d10b3-185">Dukart spustelėkite eilutę tinklelyje **Kainodaros dimensijos**, kad atidarytumėte dimensijos puslapį **msdyn_bookableresource**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-185">Double-click the row in the **Pricing Dimensions** grid to open the dimension page of **msdyn_bookableresource**.</span></span>
2. <span data-ttu-id="d10b3-186">Dimensijos puslapio skirtuke **Susiję** pasirinkite **Kainodaros dimensijų laukų pavadinimai**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-186">On dimension page, on the **Related** tab, select **Pricing Dimension Field Names**.</span></span>

  ![Skirtukas Kainodaros dimensijos laukų pavadinimai](media/PD-fieldname.png)

3. <span data-ttu-id="d10b3-188">Atsidariusiame susietajame rodinyje pasirinkite **Įtraukti naują kainodaros dimensijos lauko pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-188">In the associated view that opens, select **Add New Pricing Dimension Field Name**.</span></span>

  ![Naujų kainodaros dimensijų laukų pavadinimį įtraukimas](media/Add-NewPD-fieldname.png)

  <span data-ttu-id="d10b3-190">Bus atidarytas dimensijos **msdyn_bookableresource** puslapis **Naujas kainodaros dimensijos lauko pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-190">This opens the **New Pricing dimension field name** page for **msdyn_bookableresource**.</span></span> 

4. <span data-ttu-id="d10b3-191">Puslapyje **Naujų kainodaros dimensijų laukų pavadinimų forma** pridėkite **msdyn_projectteam** prie **Objekto loginis pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-191">On the **New Pricing Dimension Field Name** page, add **msdyn_projectteam** to **Entity Locigal Name**.</span></span>
5. <span data-ttu-id="d10b3-192">Pridėkite **msdyn_bookableresourceid** prie **Lauko pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="d10b3-192">Add  **msdyn_bookableresourceid** to **Field Name**.</span></span>

 ![Naujų kainodaros dimensijų laukų pavadinimų forma](media/PD-fieldname-Added.png)