---
title: Sukurti pasirinktinius sprendimus kainodaros dimensijoms
description: Šioje temoje aiškinama, kaip sukurti pasirinktinį sprendimą kuriant pasirinktines kainodaros dimensijas.
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
ms.openlocfilehash: 3e437fce5b9f1fb330a713788e24100a4fe02948
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080845"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="adc16-103">Sukurti pasirinktinius sprendimus kainodaros dimensijoms</span><span class="sxs-lookup"><span data-stu-id="adc16-103">Create custom solutions for pricing dimensions</span></span>

> [!IMPORTANT]
> <span data-ttu-id="adc16-104">Visi pasirinktinės kainodaros dimensijos pokyčiai turi būti atskirame sprendime.</span><span class="sxs-lookup"><span data-stu-id="adc16-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="adc16-105">Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="adc16-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="adc16-106">Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus atvejus pakartotiniam kainodaros nustatymui.</span><span class="sxs-lookup"><span data-stu-id="adc16-106">After you make the required changes, export this solution as a **Managed solution** , and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="adc16-107">Pasirinkite **Nustatymai** > **Sprendimai** ir spauskite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="adc16-107">Select **Settings** > **Solutions** , and then select **New**.</span></span> 
2. <span data-ttu-id="adc16-108">Pavadinkite sprendimą **\<your organization name>kainodaros dimensijos** , įveskite likusią reikiamą informaciją, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="adc16-108">Name the solution, **\<your organization name> pricing dimensions** , enter the remaining required information, and then select **Save**.</span></span>

> ![Pasirinktinio sprendimo kainodaros dimensijoms kūrimas](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="adc16-110">Pridėkite visus reikalingus objektus ir susijusius komponentus į kainodaros dimensijos sprendimą</span><span class="sxs-lookup"><span data-stu-id="adc16-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="adc16-111">Į kainodaros sprendimą turėsite įtraukti toliau nurodytus „Project Service“ objektus.</span><span class="sxs-lookup"><span data-stu-id="adc16-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="adc16-112">Užbaikite šioje procedūroje nurodytus veiksmus, kad atliktumėte svarbius kainodaros sprendimo schemos pakeitimus ir, kad objektai sužinotų apie naujas kainodaros dimensijas.</span><span class="sxs-lookup"><span data-stu-id="adc16-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="adc16-113">Pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="adc16-113">Select **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="adc16-114">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Pridėti esamus** > **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="adc16-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="adc16-115">Dialogo lange **Sprendimo komponentas** pasirinkite toliau nurodytus objektus.</span><span class="sxs-lookup"><span data-stu-id="adc16-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="adc16-116">Faktinis</span><span class="sxs-lookup"><span data-stu-id="adc16-116">Actual</span></span>
- <span data-ttu-id="adc16-117">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="adc16-117">Bookable Resource</span></span>
- <span data-ttu-id="adc16-118">Įvertinimo eilutė</span><span class="sxs-lookup"><span data-stu-id="adc16-118">Estimate Line</span></span>
- <span data-ttu-id="adc16-119">Projekto užduotis</span><span class="sxs-lookup"><span data-stu-id="adc16-119">Project Task</span></span>
- <span data-ttu-id="adc16-120">Sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="adc16-120">Invoice Line Detail</span></span>
- <span data-ttu-id="adc16-121">Žurnalo eilutė</span><span class="sxs-lookup"><span data-stu-id="adc16-121">Journal Line</span></span>
- <span data-ttu-id="adc16-122">Projekto sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="adc16-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="adc16-123">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="adc16-123">Project Team Member</span></span>
- <span data-ttu-id="adc16-124">Pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="adc16-124">Quote Line Detail</span></span>
- <span data-ttu-id="adc16-125">Vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="adc16-125">Role Price Markup</span></span>
- <span data-ttu-id="adc16-126">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="adc16-126">Role Price</span></span> 
- <span data-ttu-id="adc16-127">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="adc16-127">Time Entry</span></span> 

> ![Esamų objektų įtraukimas į kainodaros dimensijų sprendimą](media/Existing-entities-to-PD-solution.png)

> ![Sprendimo komponentų pasirinkimas](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="adc16-130">Būtinai įtraukite visas kiekvieno pasirinkto objekto formas ir rodinius.</span><span class="sxs-lookup"><span data-stu-id="adc16-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="adc16-131">Paraginti įtraukti bet kokius priklausomus objektus iš pasirinktų objektų, spauskite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="adc16-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![Neįtraukite visų susijusių komponentų](media/Do-not-include-required.png)


