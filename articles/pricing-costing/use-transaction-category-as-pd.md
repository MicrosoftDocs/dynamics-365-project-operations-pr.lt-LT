---
title: Operacijos kategorijos kaip kainodaros dimensijos naudojimas
description: Šioje temoje pateikiama informacijos, kaip operacijos kategorijos lauką naudoti kaip kainodaros dimensiją.
author: rumant
manager: tfehr
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bace11455d34fdda95e08be1a7cc37850a0cf589
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4514006"
---
# <a name="use-transaction-category-as-a-pricing-dimension"></a><span data-ttu-id="62160-103">Operacijos kategorijos kaip kainodaros dimensijos naudojimas</span><span class="sxs-lookup"><span data-stu-id="62160-103">Use Transaction Category as a pricing dimension</span></span>


<span data-ttu-id="62160-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="62160-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="62160-105">Šioje temoje paaiškinta, kaip naudoti lauką **Operacijos kategorija** kaip kainodaros dimensiją.</span><span class="sxs-lookup"><span data-stu-id="62160-105">This topic explains how to use the **Transaction Category** field as a pricing dimension.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="62160-106">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="62160-106">Prerequisites</span></span>
<span data-ttu-id="62160-107">Kad galėtumėte atlikti šioje temoje nurodytus veiksmus, turite turėti naują savo organizacijos kainodaros dimensijos sprendimą.</span><span class="sxs-lookup"><span data-stu-id="62160-107">Before you complete the procedures in this topic, you must have a new pricing dimension solution for your organization.</span></span> <span data-ttu-id="62160-108">Jei dar jo nesukūrėte, žr. [Pasirinktinių laukų ir objektų kaip kainodaros dimensijų kūrimas](create-custom-fields-entities-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="62160-108">If you haven't already created one, see [Create custom fields and entities as pricing dimensions](create-custom-fields-entities-pricing-dimensions.md).</span></span>

## <a name="add-the-transaction-category-field-to-forms-and-views"></a><span data-ttu-id="62160-109">Operacijos kategorijos lauko įtraukimas į formas ir rodinius</span><span class="sxs-lookup"><span data-stu-id="62160-109">Add the Transaction Category field to forms and views</span></span>
<span data-ttu-id="62160-110">Jei norite, kad laukas **Operacijos kategorija** būtų rodomas kainodaros dimensijos sprendime, reikia pridėti lauką prie visų formų ir rodinių kaip objektą.</span><span class="sxs-lookup"><span data-stu-id="62160-110">To make the **Transaction Category** field visible in the pricing dimension solution, you need to add the field to all the forms and views as an entity.</span></span>

<span data-ttu-id="62160-111">Toliau esančioje lentelėje pateiktos visos paruoštos naudoti formos ir rodiniai pagal objektą.</span><span class="sxs-lookup"><span data-stu-id="62160-111">The following table lists all of the out-of-the box forms and views, by entity.</span></span> <span data-ttu-id="62160-112">Taip pat turėsite pridėti naują lauką prie bet kokių papildomų formų ar rodinių, esančių jūsų tinkintuose objektuose.</span><span class="sxs-lookup"><span data-stu-id="62160-112">You will also need to add the new field to any additional forms or views in your customized entities.</span></span>

|  <span data-ttu-id="62160-113">Entity</span><span class="sxs-lookup"><span data-stu-id="62160-113">Entity</span></span>        | <span data-ttu-id="62160-114">Formos</span><span class="sxs-lookup"><span data-stu-id="62160-114">Forms</span></span>     |<span data-ttu-id="62160-115">Peržiūros</span><span class="sxs-lookup"><span data-stu-id="62160-115">Views</span></span>        |
| ------------------------------|---------------------------------|----------------------------------|
|  <span data-ttu-id="62160-116">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="62160-116">Role Price</span></span>| <span data-ttu-id="62160-117">Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-117">Information</span></span> |<span data-ttu-id="62160-118">- Aktyvių išteklių kategorijų kainos</span><span class="sxs-lookup"><span data-stu-id="62160-118">- Active Resource Category Prices</span></span><br> <span data-ttu-id="62160-119">- Išteklių kategorijos kainos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-119">- Resource Category Price Associated</span></span> |
|  <span data-ttu-id="62160-120">Vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="62160-120">Role Price Markup</span></span>| <span data-ttu-id="62160-121">Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-121">Information</span></span>|<span data-ttu-id="62160-122">- Aktyvaus vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="62160-122">- Active Role Price Markup</span></span><br><span data-ttu-id="62160-123">- Vaidmens kainos antkainio susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-123">- Role Price Markup Associated</span></span> |
|  <span data-ttu-id="62160-124">Pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="62160-124">Quote Line Detail</span></span>|<span data-ttu-id="62160-125">- Projekto informacija</span><span class="sxs-lookup"><span data-stu-id="62160-125">- Project Information</span></span><br><span data-ttu-id="62160-126">- Spartusis projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="62160-126">- Project Quick Create</span></span>| <span data-ttu-id="62160-127">- Aktyvaus pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="62160-127">- Active Quote Line Detail</span></span><br><span data-ttu-id="62160-128">- Jungtinių pasiūlymo eilučių informacija</span><span class="sxs-lookup"><span data-stu-id="62160-128">- Combined Quote Line Details</span></span><br><span data-ttu-id="62160-129">- Pasiūlymo eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-129">- Quote Line Detail Associated</span></span> |
|  <span data-ttu-id="62160-130">Projekto sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="62160-130">Project Contract Line Detail</span></span>|<span data-ttu-id="62160-131">- Projekto informacija</span><span class="sxs-lookup"><span data-stu-id="62160-131">- Project Information</span></span><br><span data-ttu-id="62160-132">- Spartusis projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="62160-132">- Project Quick Create</span></span>|<span data-ttu-id="62160-133">- Jungtinių sutarties eilučių informacija</span><span class="sxs-lookup"><span data-stu-id="62160-133">- Combined Contract Line Details</span></span><br><span data-ttu-id="62160-134">- Aktyvios sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="62160-134">- Active Contract Line Details</span></span><br><span data-ttu-id="62160-135">- Sutarties eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-135">- Contract Line Detail Associated</span></span> |
|  <span data-ttu-id="62160-136">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="62160-136">Project Task</span></span>|<span data-ttu-id="62160-137">- Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-137">- Information</span></span><br><span data-ttu-id="62160-138">- Nauja forma</span><span class="sxs-lookup"><span data-stu-id="62160-138">- New Form</span></span>| &nbsp; |
|  <span data-ttu-id="62160-139">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="62160-139">Project Team Member</span></span>|<span data-ttu-id="62160-140">- Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-140">- Information</span></span><br><span data-ttu-id="62160-141">- Nauja forma</span><span class="sxs-lookup"><span data-stu-id="62160-141">- New Form</span></span>|<span data-ttu-id="62160-142">- Aktyvūs projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="62160-142">- Active Project Team Members</span></span><br><span data-ttu-id="62160-143">- Projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="62160-143">- Project Team Members</span></span><br><span data-ttu-id="62160-144">- Projekto komandos narių susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-144">- Project Team Members Associated</span></span> |
|  <span data-ttu-id="62160-145">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="62160-145">Time Entry</span></span>|<span data-ttu-id="62160-146">- Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-146">- Information</span></span><br><span data-ttu-id="62160-147">- Kurti laiko įrašą</span><span class="sxs-lookup"><span data-stu-id="62160-147">- Create Time Entry</span></span>|<span data-ttu-id="62160-148">- Mano laiko įrašai pagal datą</span><span class="sxs-lookup"><span data-stu-id="62160-148">- My Time Entries By Date</span></span><br><span data-ttu-id="62160-149">- Mano laiko įrašai šią savaitę</span><span class="sxs-lookup"><span data-stu-id="62160-149">- My Time Entries for this Week</span></span><br><span data-ttu-id="62160-150">- Laiko įrašai, skirti patvirtinti</span><span class="sxs-lookup"><span data-stu-id="62160-150">- Time entries for Approval</span></span>|
|  <span data-ttu-id="62160-151">Žurnalo eilutė</span><span class="sxs-lookup"><span data-stu-id="62160-151">Journal Line</span></span>|<span data-ttu-id="62160-152">- Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-152">- Information</span></span><br><span data-ttu-id="62160-153">- Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="62160-153">- Quick Create</span></span>|<span data-ttu-id="62160-154">- Aktyvaus žurnalo eilutės</span><span class="sxs-lookup"><span data-stu-id="62160-154">- Active Journal Lines</span></span><br><span data-ttu-id="62160-155">- Žurnalo eilučių susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-155">- Journal Line Associated</span></span>|
|  <span data-ttu-id="62160-156">Sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="62160-156">Invoice Line Detail</span></span>|<span data-ttu-id="62160-157">- Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-157">- Information</span></span><br><span data-ttu-id="62160-158">- Spartusis kūrimas</span><span class="sxs-lookup"><span data-stu-id="62160-158">- Quick Create</span></span>|<span data-ttu-id="62160-159">- Aktyvios sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="62160-159">- Active Invoice Line Details</span></span><br><span data-ttu-id="62160-160">- Apmokestinamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="62160-160">- Chargeable Invoice Transactions</span></span><br><span data-ttu-id="62160-161">- Nemokamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="62160-161">- Complimentary Invoice Transactions</span></span><br><span data-ttu-id="62160-162">- Sąskaitos faktūros eilutės informacijos susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-162">- Invoice Line Detail Associated</span></span> <br><span data-ttu-id="62160-163">- Neapmokestinamos sąskaitos faktūros operacijos</span><span class="sxs-lookup"><span data-stu-id="62160-163">- Non-Chargeable Invoice Transactions</span></span>|
|  <span data-ttu-id="62160-164">Faktinis</span><span class="sxs-lookup"><span data-stu-id="62160-164">Actual</span></span>|<span data-ttu-id="62160-165">- Informacija</span><span class="sxs-lookup"><span data-stu-id="62160-165">- Information</span></span><br><span data-ttu-id="62160-166">- Aktyvūs faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="62160-166">- Active Actuals</span></span>| <span data-ttu-id="62160-167">Faktinis susietasis rodinys</span><span class="sxs-lookup"><span data-stu-id="62160-167">Actual Associated</span></span> |

## <a name="set-up-the-transaction-category-field-as-a-pricing-dimension"></a><span data-ttu-id="62160-168">Operacijos kategorijos lauko kaip kainodaros dimensijos nustatymas</span><span class="sxs-lookup"><span data-stu-id="62160-168">Set up the Transaction Category field as a pricing dimension</span></span>

1. <span data-ttu-id="62160-169">Eikite į **Parametrai** > **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="62160-169">Go to **Settings** > **Parameters**.</span></span> 
2. <span data-ttu-id="62160-170">Puslapio **Parametrai** skirtuke **Suma pagrįstos kainodaros dimensijos** įsitikinkite, kad tinklelyje rodomi objekto **Kainodaros dimensijos** įrašai.</span><span class="sxs-lookup"><span data-stu-id="62160-170">On the **Parameters** page, on the **Amount-Based Pricing Dimensions** tab, verify that the grid shows the records in the **Pricing Dimensions** entity.</span></span>
3. <span data-ttu-id="62160-171">Prie šio sąrašo pridėkite **Operacijos kategorija** ir nustatykite laukus **Taikoma savikainai** ir **Taikoma pardavimui** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="62160-171">Add **Transaction Category** to this list and set the **Applicable to Cost** and **Applicable to Sale** fields to **Yes**.</span></span>
4. <span data-ttu-id="62160-172">Lauke **Dimensijos tipas** pasirinkite **Pagrįsta suma**, tada pasirinkite lauko **Operacijos kategorija** prioritetą, nes jis susijęs su savikaina ir pardavimu.</span><span class="sxs-lookup"><span data-stu-id="62160-172">In the **Dimension Type** field, select **Amount-based**, and then select the priority for **Transaction Category** as it relates to cost and sales.</span></span>