---
title: Sprendimo pasirinktinėms kainodaros dimensijoms kūrimas
description: Šioje temoje pateikta informacijos, kaip kurti sprendimus, skirtus pasirinktinėms kainodaros dimensijoms.
author: Rumant
manager: tfehr
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3e3f688b0147974ef252a0ee00be20c4669d7165
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278428"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="6efa6-103">Sprendimo pasirinktinėms kainodaros dimensijoms kūrimas</span><span class="sxs-lookup"><span data-stu-id="6efa6-103">Create a solution for custom pricing dimensions</span></span>

 <span data-ttu-id="6efa6-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="6efa6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span> 

>[!IMPORTANT]
><span data-ttu-id="6efa6-105">Visi pasirinktinės kainodaros dimensijos pokyčiai turi būti atskirame sprendime.</span><span class="sxs-lookup"><span data-stu-id="6efa6-105">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="6efa6-106">Ši svarbi geriausios praktikos procedūra suteikia galimybę lanksčiai atnaujinti arba pašalinti pakeitimus, padeda pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitus egzempliorius.</span><span class="sxs-lookup"><span data-stu-id="6efa6-106">This important best practice allows the flexibility to update or remove changes as needed, helps with re-use of your work, and makes it easier to port changes to other instances.</span></span> <span data-ttu-id="6efa6-107">Atlikę reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima naudoti pakartotinai.</span><span class="sxs-lookup"><span data-stu-id="6efa6-107">After you make the required changes, export this solution as a **Managed** solution, and then import into other instances for reuse.</span></span>

## <a name="create-a-solution-for-custom-pricing-dimensions"></a><span data-ttu-id="6efa6-108">Sprendimo pasirinktinėms kainodaros dimensijoms kūrimas</span><span class="sxs-lookup"><span data-stu-id="6efa6-108">Create a solution for custom pricing dimensions</span></span>

1.  <span data-ttu-id="6efa6-109">Pasirinkite **Nustatymai** > **Sprendimai** ir spauskite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6efa6-109">Select **Settings** > **Solutions**, and then select **New**.</span></span>
2.  <span data-ttu-id="6efa6-110">Sukurkite sprendimo pavadinimą: *<your organization name> kainodaros dimensijos*.</span><span class="sxs-lookup"><span data-stu-id="6efa6-110">Name the solution, *<your organization name> pricing dimensions*.</span></span>
3. <span data-ttu-id="6efa6-111">Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6efa6-111">Enter the remaining required information, and then select **Save**.</span></span>

  ![Pasirinktinių kainodaros dimensijų sprendimo kūrimas](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="6efa6-113">Pridėkite visus reikalingus objektus ir susijusius komponentus į kainodaros dimensijos sprendimą</span><span class="sxs-lookup"><span data-stu-id="6efa6-113">Add all required entities and related components to the Pricing dimension solution</span></span>

<span data-ttu-id="6efa6-114">Pridėkite toliau nurodytus „Project Service“ objektus prie savo kainodaros sprendimo, kad atliktumėte svarbius schemos pakeitimus, susijusius su kainodaros sprendimu.</span><span class="sxs-lookup"><span data-stu-id="6efa6-114">Add the following Project Service entities to your pricing solution to make important schema changes in the pricing solution.</span></span> <span data-ttu-id="6efa6-115">Atlikus šią procedūrą, objektai atpažins naujas kainodaros dimensijas.</span><span class="sxs-lookup"><span data-stu-id="6efa6-115">After you have completed this procedure, the entities will recognize the new pricing dimensions.</span></span>

1.  <span data-ttu-id="6efa6-116">Pasirinkite **Parametrai** > **Sprendimai**, tada dukart spustelėkite **<*jūsų organizacijos pavadinimas*> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="6efa6-116">Select **Settings** > **Solutions**, and then double-click **<*your organization name*> pricing dimensions**.</span></span>
2.  <span data-ttu-id="6efa6-117">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Pridėti esamus** > **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="6efa6-117">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3.  <span data-ttu-id="6efa6-118">Dialogo lange **Sprendimo komponentas** pasirinkite toliau nurodytus objektus.</span><span class="sxs-lookup"><span data-stu-id="6efa6-118">In the **Solution Components** dialog box, select the following entities:</span></span>
 
   - <span data-ttu-id="6efa6-119">**Faktinis**</span><span class="sxs-lookup"><span data-stu-id="6efa6-119">**Actual**</span></span>
   - <span data-ttu-id="6efa6-120">**Rezervuojamas išteklius**</span><span class="sxs-lookup"><span data-stu-id="6efa6-120">**Bookable Resource**</span></span>
   - <span data-ttu-id="6efa6-121">**Įvertinimo eilutė**</span><span class="sxs-lookup"><span data-stu-id="6efa6-121">**Estimate Line**</span></span>
   - <span data-ttu-id="6efa6-122">**Projekto užduotis**</span><span class="sxs-lookup"><span data-stu-id="6efa6-122">**Project Task**</span></span>
   - <span data-ttu-id="6efa6-123">**Sąskaitos faktūros eilutės informacija**</span><span class="sxs-lookup"><span data-stu-id="6efa6-123">**Invoice Line Detail**</span></span>
   - <span data-ttu-id="6efa6-124">**Žurnalo eilutė**</span><span class="sxs-lookup"><span data-stu-id="6efa6-124">**Journal Line**</span></span>
   - <span data-ttu-id="6efa6-125">**Projekto sutarties eilutės informacija**</span><span class="sxs-lookup"><span data-stu-id="6efa6-125">**Project Contract Line Detail**</span></span>
   - <span data-ttu-id="6efa6-126">**Projekto komandos narys**</span><span class="sxs-lookup"><span data-stu-id="6efa6-126">**Project Team Member**</span></span>
   - <span data-ttu-id="6efa6-127">**Pasiūlymo eilutės informacija**</span><span class="sxs-lookup"><span data-stu-id="6efa6-127">**Quote Line Detail**</span></span>
   - <span data-ttu-id="6efa6-128">**Vaidmens kainos antkainis**</span><span class="sxs-lookup"><span data-stu-id="6efa6-128">**Role Price Markup**</span></span>
   - <span data-ttu-id="6efa6-129">**Vaidmens kaina**</span><span class="sxs-lookup"><span data-stu-id="6efa6-129">**Role Price**</span></span>
   - <span data-ttu-id="6efa6-130">**Laiko įrašas**</span><span class="sxs-lookup"><span data-stu-id="6efa6-130">**Time Entry**</span></span>
 
   ![Esamų objektų įtraukimas į pasirinktinių kainodaros dimensijų sprendimą](./media/Existing-entities-to-PD-solution.png)
 
 4. <span data-ttu-id="6efa6-132">Peržiūrėkite kiekvieno objekto pridedamus komponentus ir kiekvieno objekto galutinį objekto išteklių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="6efa6-132">For each entity, review the components being added and the final list of entity assets for each entity.</span></span> 

   >[!NOTE]
   > <span data-ttu-id="6efa6-133">Įtraukite visas kiekvieno pasirinkto objekto formas ir rodinius.</span><span class="sxs-lookup"><span data-stu-id="6efa6-133">Include all forms and views for each of the selected entities.</span></span>

  ![Pridėti objektai](./media/solution-component-selection.png)


5.  <span data-ttu-id="6efa6-135">Kai būsite paraginti įtraukti bet kokius pasirinktų objektų priklausomuosius objektus, pasirinkite **Ne, būtinųjų komponentų įtraukti nereikia.**</span><span class="sxs-lookup"><span data-stu-id="6efa6-135">When prompted to include any dependent entities for the selected entities, select **No, do not include required components.**</span></span>

    ![Priklausomųjų objektų įtraukimas](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]