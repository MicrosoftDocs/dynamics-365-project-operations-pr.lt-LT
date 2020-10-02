---
title: Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų
description: Šioje temoje pateikta informacija apie tai, kaip kurti pasirinktinių parinkčių rinkinius arba objektus.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2000f7e710267560fe2bd52b0e33024617d108ea
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898271"
---
# <a name="create-custom-fields-and-entities-as-pricing-dimensions"></a><span data-ttu-id="46941-103">Pasirinktinių laukų ir objektų kūrimas kaip kainodaros dimensijų</span><span class="sxs-lookup"><span data-stu-id="46941-103">Create custom fields and entities as pricing dimensions</span></span>

<span data-ttu-id="46941-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="46941-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="46941-105">Atlikite toliau nurodytus veiksmus bet kuriuo metu, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą.</span><span class="sxs-lookup"><span data-stu-id="46941-105">Complete the following steps any time that you want to create a custom option set or entity.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="46941-106">Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą.</span><span class="sxs-lookup"><span data-stu-id="46941-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="46941-107">Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="46941-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="46941-108">Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.</span><span class="sxs-lookup"><span data-stu-id="46941-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="46941-109">Pasirinktinio sprendimo kainodaros dimensijoms kūrimas</span><span class="sxs-lookup"><span data-stu-id="46941-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="46941-110">Eikite į **Parametrai** > **Sprendimai**, o tada pasirinkite **Naujas** ir sukurkite naują sprendimą.</span><span class="sxs-lookup"><span data-stu-id="46941-110">Go to **Settings** > **Solutions**, and then select **New** to create a new solution.</span></span> 
2. <span data-ttu-id="46941-111">Pavadinkite sprendimą **\<your organization name>kainodaros dimensijos**, įveskite likusią reikiamą informaciją, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="46941-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="46941-112">Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime</span><span class="sxs-lookup"><span data-stu-id="46941-112">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="46941-113">Kainodaros dimensija gali būti parinkčių rinkinys arba objektas.</span><span class="sxs-lookup"><span data-stu-id="46941-113">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="46941-114">Abu turi būti sukurti jūsų kainodaros sprendime.</span><span class="sxs-lookup"><span data-stu-id="46941-114">Both must be created in your pricing solution.</span></span> <span data-ttu-id="46941-115">Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.</span><span class="sxs-lookup"><span data-stu-id="46941-115">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="46941-116">Objekto dimensijos</span><span class="sxs-lookup"><span data-stu-id="46941-116">Entity-based dimensions</span></span>

1. <span data-ttu-id="46941-117">Eikite į **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="46941-117">Go to **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="46941-118">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="46941-118">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="46941-119">Pasirinkite **Naujas**, kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="46941-119">Select **New** to create a new entity called **Standard Title**.</span></span> 
4. <span data-ttu-id="46941-120">Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="46941-120">Enter the remaining required information, and then select **Save**.</span></span>


### <a name="option-set-based-dimensions"></a><span data-ttu-id="46941-121">Parinkčių rinkinio matmenys</span><span class="sxs-lookup"><span data-stu-id="46941-121">Option set-based dimensions</span></span> 
<span data-ttu-id="46941-122">Galite sukurti du parinkčių rinkinio matmenis.</span><span class="sxs-lookup"><span data-stu-id="46941-122">You can create two option set-based dimensions.</span></span> <span data-ttu-id="46941-123">Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje**, o pasinaudodami lauku **Išteklių darbo valandos**, su vertėmis **Įprastos** ir **Viršvalandžiai**, pritaikykite antkainį darbui pasibaigus.</span><span class="sxs-lookup"><span data-stu-id="46941-123">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="46941-124">Eikite į **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="46941-124">Go to **Settings** > **Solutions**, and double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="46941-125">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="46941-125">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="46941-126">Pasirinkite **Naujas**, kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="46941-126">Select **New** to create a new option set, enter the remaining required information, and then select **Save**.</span></span>

## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="46941-127">Objekto dimensijų duomenų kūrimas</span><span class="sxs-lookup"><span data-stu-id="46941-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="46941-128">Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą.</span><span class="sxs-lookup"><span data-stu-id="46941-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="46941-129">Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="46941-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="46941-130">Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.</span><span class="sxs-lookup"><span data-stu-id="46941-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="46941-131">Pažymėkite **Išplėstinė ieška**, pažymėkite objekto **standartinį pavadinimą** ir pasirinkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="46941-131">Select **Advanced Find**, select the entity **Standard Title**, and then select **Results**.</span></span> <span data-ttu-id="46941-132">Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.</span><span class="sxs-lookup"><span data-stu-id="46941-132">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="46941-133">Pasirinkite **Naujas** ir lauke **Pavadinimas** įveskite „Sistemos inžinierius“ ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="46941-133">Select **New**, and in the **Name** field, enter "Systems Engineer" and then select **Save**.</span></span>
3. <span data-ttu-id="46941-134">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="46941-134">Close the form.</span></span> 
4. <span data-ttu-id="46941-135">Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="46941-135">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="46941-136">Visų reikiamų objektų ir susijusių komponentų įtraukimas į kainodaros dimensijos sprendimą</span><span class="sxs-lookup"><span data-stu-id="46941-136">Add all required entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="46941-137">Į kainodaros sprendimą turėsite įtraukti toliau nurodytus objektus.</span><span class="sxs-lookup"><span data-stu-id="46941-137">You will need to add the following entities to your pricing solution.</span></span> <span data-ttu-id="46941-138">Atlikite šioje procedūroje nurodytus veiksmus, kad atliktumėte svarbių kainodaros sprendimo schemos pakeitimų ir objektai žinotų apie naujas kainodaros dimensijas.</span><span class="sxs-lookup"><span data-stu-id="46941-138">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="46941-139">Pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijas**.</span><span class="sxs-lookup"><span data-stu-id="46941-139">Select **Settings** > **Solutions**, and double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="46941-140">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Pridėti esamus** > **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="46941-140">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="46941-141">Dialogo lange **Sprendimo komponentas** pasirinkite toliau nurodytus objektus.</span><span class="sxs-lookup"><span data-stu-id="46941-141">In the **Solution Components** dialog box, select the following entities:</span></span>

  - <span data-ttu-id="46941-142">Faktinis</span><span class="sxs-lookup"><span data-stu-id="46941-142">Actual</span></span>
  - <span data-ttu-id="46941-143">Rezervuojami ištekliai</span><span class="sxs-lookup"><span data-stu-id="46941-143">Bookable Resource</span></span>
  - <span data-ttu-id="46941-144">Įvertinimo eilutė</span><span class="sxs-lookup"><span data-stu-id="46941-144">Estimate Line</span></span>
  - <span data-ttu-id="46941-145">Sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="46941-145">Invoice Line Detail</span></span>
  - <span data-ttu-id="46941-146">Žurnalo eilutė</span><span class="sxs-lookup"><span data-stu-id="46941-146">Journal Line</span></span>
  - <span data-ttu-id="46941-147">Projekto sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="46941-147">Project Contract Line Detail</span></span>
  - <span data-ttu-id="46941-148">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="46941-148">Project Team Member</span></span>
  - <span data-ttu-id="46941-149">Pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="46941-149">Quote Line Detail</span></span>
  - <span data-ttu-id="46941-150">Vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="46941-150">Role Price Markup</span></span>
  - <span data-ttu-id="46941-151">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="46941-151">Role Price</span></span> 
  - <span data-ttu-id="46941-152">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="46941-152">Time Entry</span></span> 


> [!NOTE]
> <span data-ttu-id="46941-153">Būtinai įtraukite visas kiekvieno pasirinkto objekto formas ir rodinius.</span><span class="sxs-lookup"><span data-stu-id="46941-153">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="46941-154">Paraginti įtraukti priklausomus objektus iš pirmiau pasirinktų objektų, spustelėkite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="46941-154">When prompted to include any dependent entities for the entities selected above, select **No**.</span></span>

