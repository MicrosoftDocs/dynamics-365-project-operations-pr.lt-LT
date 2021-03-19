---
title: Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų
description: Šioje temoje pateikta informacija apie tai, kaip kurti pasirinktinių parinkčių rinkinius arba objektus.
author: rumant
manager: AnnBe
ms.date: 11/18/2020
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
ms.openlocfilehash: 089481cd3e7c0f8f1d1aa880d64cb79e8d677c2d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275638"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="55034-103">Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų</span><span class="sxs-lookup"><span data-stu-id="55034-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="55034-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="55034-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="55034-105">Atlikite toliau nurodytus veiksmus, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą, skirtą naudoti kaip kainodaros dimensija.</span><span class="sxs-lookup"><span data-stu-id="55034-105">Complete the following steps when you want to create a custom option set or entity for using it as a pricing dimension.</span></span> <span data-ttu-id="55034-106">Norėdami gauti daugiau informacijos, žr. [Kainodaros dimensijų apžvalga](pricing-dimensions-overview.md).</span><span class="sxs-lookup"><span data-stu-id="55034-106">For more information, see [Pricing dimensions overview](pricing-dimensions-overview.md).</span></span>  

> [!IMPORTANT]
> <span data-ttu-id="55034-107">Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą.</span><span class="sxs-lookup"><span data-stu-id="55034-107">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="55034-108">Ši svarbi geriausia praktika suteikia lankstumo ateityje, prireikus atnaujinti arba pašalinti pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="55034-108">This important best practice provides flexibility in the future to update or remove changes as needed.</span></span> <span data-ttu-id="55034-109">Tai padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.</span><span class="sxs-lookup"><span data-stu-id="55034-109">This will also help with re-use of your work and make it easier to port these changes to another instance After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="55034-110">Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime</span><span class="sxs-lookup"><span data-stu-id="55034-110">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="55034-111">Kainodaros dimensija gali būti parinkčių rinkinys arba objektas.</span><span class="sxs-lookup"><span data-stu-id="55034-111">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="55034-112">Abu turi būti sukurti jūsų kainodaros sprendime.</span><span class="sxs-lookup"><span data-stu-id="55034-112">Both must be created in your pricing solution.</span></span> <span data-ttu-id="55034-113">Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.</span><span class="sxs-lookup"><span data-stu-id="55034-113">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="55034-114">Objekto dimensijos</span><span class="sxs-lookup"><span data-stu-id="55034-114">Entity-based dimensions</span></span>
<span data-ttu-id="55034-115">Jei norite kurti objekto dimensijas, atlikite toliau nurodytus veiksmus:</span><span class="sxs-lookup"><span data-stu-id="55034-115">To create entity-based dimensions, follow these steps:</span></span>

1. <span data-ttu-id="55034-116">Eikite į **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="55034-116">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="55034-117">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="55034-117">In Solution Explorer, in the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="55034-118">Pasirinkite **Naujas**, kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="55034-118">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="55034-119">Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="55034-119">Enter the remaining required information, and then select **Save**.</span></span>

> ![Standartinio pavadinimo objekto apibrėžtis](media/Standard-Title-entity-definition.png)

### <a name="option-set-based-dimensions"></a><span data-ttu-id="55034-121">Parinkčių rinkinio matmenys</span><span class="sxs-lookup"><span data-stu-id="55034-121">Option set-based dimensions</span></span> 
<span data-ttu-id="55034-122">Galite sukurti du parinkčių rinkinio matmenis.</span><span class="sxs-lookup"><span data-stu-id="55034-122">You can create two option set-based dimensions.</span></span> 

- <span data-ttu-id="55034-123">Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje**.</span><span class="sxs-lookup"><span data-stu-id="55034-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work.</span></span> 
- <span data-ttu-id="55034-124">Pasinaudodami lauku **Išteklių darbo valandos**, su reikšmėmis **Įprastos** ir **Viršvalandžiai**, pritaikykite antkainį darbui pasibaigus.</span><span class="sxs-lookup"><span data-stu-id="55034-124">Use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when the work is complete.</span></span>

<span data-ttu-id="55034-125">Toliau esančiame grafiniame vaizde pateikiamas **išteklių darbo vietos** dimensijos rodinys.</span><span class="sxs-lookup"><span data-stu-id="55034-125">The following graphic provides a view of the **Resource Work Location** dimension.</span></span> 

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo vieta“](media/Option-set-PD-called-Resource-Work-Location.png)

<span data-ttu-id="55034-127">Toliau esančiame grafiniame vaizde pateikiamas **išteklių darbo valandų** dimensijos rodinys.</span><span class="sxs-lookup"><span data-stu-id="55034-127">The following graphic provides a view of the **Resource Work Hours** dimension.</span></span> 

> ![Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo valandos“](media/Option-set-PD-called-Resource-Work-Hours.png)

1. <span data-ttu-id="55034-129">Eikite į **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="55034-129">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="55034-130">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="55034-130">In Solution Explorer, in the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="55034-131">Pasirinkite **Naujas**, kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="55034-131">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="55034-132">Objekto dimensijų duomenų kūrimas</span><span class="sxs-lookup"><span data-stu-id="55034-132">Create data for entity-based dimensions</span></span>

<span data-ttu-id="55034-133">Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą.</span><span class="sxs-lookup"><span data-stu-id="55034-133">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="55034-134">Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="55034-134">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="55034-135">Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.</span><span class="sxs-lookup"><span data-stu-id="55034-135">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="55034-136">Pasirinkite **Išplėstinė ieška**.</span><span class="sxs-lookup"><span data-stu-id="55034-136">Select **Advanced Find**.</span></span>
2. <span data-ttu-id="55034-137">Pasirinkite objektą **Standartinis pavadinimas**, o tada pasirinkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="55034-137">Select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="55034-138">Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.</span><span class="sxs-lookup"><span data-stu-id="55034-138">All of the rows in the **Standard Title** entity will be shown.</span></span>
3. <span data-ttu-id="55034-139">Pasirinkite **Naujas** ir lauke **Pavadinimas** įveskite „Sistemos inžinierius“ ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="55034-139">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
4. <span data-ttu-id="55034-140">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="55034-140">Close the page.</span></span> 
5. <span data-ttu-id="55034-141">Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="55034-141">Repeat steps 1-3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![Standartinio pavadinimo objekto duomenų pavyzdžiai](media/ST-data.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]