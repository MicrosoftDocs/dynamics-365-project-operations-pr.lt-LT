---
title: Pasirinktinių laukų ir objektų kūrimas
description: Šioje temoje paaiškinama, kaip kurti parinkčių rinkinius ir objektus naudojant asmeninį sprendimą Power Apps platformoje.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/26/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: fb160bfd-e037-4a21-a968-3ff2e6e16481
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 7ee30e3bb6b8034ef226e2e9181195685355011f
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753761"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="77cd6-103">Pasirinktinių laukų ir objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="77cd6-103">Create custom fields and entities</span></span> 

<span data-ttu-id="77cd6-104">Atlikite toliau nurodytus veiksmus bet kuriuo metu, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą „Power Apps“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="77cd6-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="77cd6-105">Šioje temoje nurodytas procedūras reikia atlikti naudojant „Project Service Automation“ (PSA) internetinę sąsają.</span><span class="sxs-lookup"><span data-stu-id="77cd6-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="77cd6-106">Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą.</span><span class="sxs-lookup"><span data-stu-id="77cd6-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="77cd6-107">Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="77cd6-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="77cd6-108">Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.</span><span class="sxs-lookup"><span data-stu-id="77cd6-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>


## <a name="create-a-custom-solution-for-pricing-dimensions"></a><span data-ttu-id="77cd6-109">Pasirinktinio sprendimo kainodaros dimensijoms kūrimas</span><span class="sxs-lookup"><span data-stu-id="77cd6-109">Create a custom solution for pricing dimensions</span></span>
1. <span data-ttu-id="77cd6-110">Naudodami PSA spustelėkite **Parametrai** > **Sprendimai**, tada spustelėkite **Naujas** ir sukurkite naują sprendimą.</span><span class="sxs-lookup"><span data-stu-id="77cd6-110">In PSA, click **Settings** > **Solutions**, and then click **New** to create a new solution.</span></span> 
2. <span data-ttu-id="77cd6-111">Pavadinkite sprendimą (**\<organizacijos pavadinimas > kainodaros dimensijos**), įveskite likusią reikiamą informaciją, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-111">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then click **Save**.</span></span>

> ![Pasirinktinio sprendimo kainodaros dimensijoms kūrimas](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="77cd6-113">Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime</span><span class="sxs-lookup"><span data-stu-id="77cd6-113">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="77cd6-114">Kainodaros dimensija gali būti parinkčių rinkinys arba objektas.</span><span class="sxs-lookup"><span data-stu-id="77cd6-114">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="77cd6-115">Abu turi būti sukurti jūsų kainodaros sprendime.</span><span class="sxs-lookup"><span data-stu-id="77cd6-115">Both must be created in your pricing solution.</span></span> <span data-ttu-id="77cd6-116">Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.</span><span class="sxs-lookup"><span data-stu-id="77cd6-116">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="77cd6-117">Objekto dimensijos</span><span class="sxs-lookup"><span data-stu-id="77cd6-117">Entity-based dimensions</span></span>

1. <span data-ttu-id="77cd6-118">(PSA) spustelėkite **„Parametrai“** > **„Sprendimai“**, tada dukart spustelėkite **\<organizacijos pavadinimas > kainų dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-118">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="77cd6-119">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-119">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="77cd6-120">Spustelėkite **Naujas**, kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-120">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="77cd6-121">Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-121">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standartinio pavadinimo objekto apibrėžtis](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="77cd6-123">Parinkčių rinkinio matmenys</span><span class="sxs-lookup"><span data-stu-id="77cd6-123">Option set-based dimensions</span></span> 
<span data-ttu-id="77cd6-124">Galite sukurti du parinkčių rinkinio matmenis.</span><span class="sxs-lookup"><span data-stu-id="77cd6-124">You can create two option set-based dimensions.</span></span> <span data-ttu-id="77cd6-125">Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje**, o pasinaudodami lauku **Išteklių darbo valandos**, su vertėmis **Įprastos** ir **Viršvalandžiai**, pritaikykite antkainį darbui pasibaigus.</span><span class="sxs-lookup"><span data-stu-id="77cd6-125">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="77cd6-126">Apsilankę PSA spustelėkite **Parametrai** > **Sprendimai**, tada dukart spustelėkite **\<organizacijos pavadinimas > kainų dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-126">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="77cd6-127">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-127">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="77cd6-128">Spustelėkite **Naujas**, kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-128">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="77cd6-129">Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo vieta“</span><span class="sxs-lookup"><span data-stu-id="77cd6-129">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="77cd6-130">Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo valandos“</span><span class="sxs-lookup"><span data-stu-id="77cd6-130">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="77cd6-131">Objekto dimensijų duomenų kūrimas</span><span class="sxs-lookup"><span data-stu-id="77cd6-131">Create data for entity-based dimensions</span></span>

<span data-ttu-id="77cd6-132">Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą.</span><span class="sxs-lookup"><span data-stu-id="77cd6-132">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="77cd6-133">Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-133">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="77cd6-134">Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.</span><span class="sxs-lookup"><span data-stu-id="77cd6-134">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="77cd6-135">Apsilankę PSA spustelėkite **Išplėstinė ieška**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-135">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="77cd6-136">Pasirinkite objektą **Standartinis pavadinimas**, tada spustelėkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-136">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="77cd6-137">Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.</span><span class="sxs-lookup"><span data-stu-id="77cd6-137">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="77cd6-138">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-138">Click **New**.</span></span> <span data-ttu-id="77cd6-139">Lauke **Pavadinimas** įveskite „Sistemų inžinierius“, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-139">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="77cd6-140">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="77cd6-140">Close the form.</span></span> 
4. <span data-ttu-id="77cd6-141">Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="77cd6-141">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="77cd6-142">Standartinio pavadinimo objekto duomenų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="77cd6-142">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)

## <a name="add-all-required-psa-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="77cd6-143">Visų reikiamų PSA objektų ir susijusių komponentų įtraukimas į kainodaros dimensijos sprendimą</span><span class="sxs-lookup"><span data-stu-id="77cd6-143">Add all required PSA entities and related components to the Pricing Dimension Solution</span></span>
<span data-ttu-id="77cd6-144">Į kainodaros sprendimą turėsite įtraukti toliau nurodytus „Project Service“ objektus.</span><span class="sxs-lookup"><span data-stu-id="77cd6-144">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="77cd6-145">Atlikite šioje procedūroje nurodytus veiksmus, kad atliktumėte svarbių kainodaros sprendimo schemos pakeitimų ir objektai žinotų apie naujas kainodaros dimensijas.</span><span class="sxs-lookup"><span data-stu-id="77cd6-145">Use the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="77cd6-146">(PSA) spustelėkite **„Parametrai“** > **„Sprendimai“**, tada dukart spustelėkite **\<organizacijos pavadinimas > kainų dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-146">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="77cd6-147">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Pridėti esamus** > **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-147">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="77cd6-148">Dialogo lange **Sprendimo komponentas** pasirinkite toliau nurodytus objektus.</span><span class="sxs-lookup"><span data-stu-id="77cd6-148">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="77cd6-149">Faktinis</span><span class="sxs-lookup"><span data-stu-id="77cd6-149">Actual</span></span>
- <span data-ttu-id="77cd6-150">Rezervuojami ištekliai</span><span class="sxs-lookup"><span data-stu-id="77cd6-150">Bookable Resource</span></span>
- <span data-ttu-id="77cd6-151">Įvertinimo eilutė</span><span class="sxs-lookup"><span data-stu-id="77cd6-151">Estimate Line</span></span>
- <span data-ttu-id="77cd6-152">Sąskaitos faktūros eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="77cd6-152">Invoice Line Detail</span></span>
- <span data-ttu-id="77cd6-153">Žurnalo eilutė</span><span class="sxs-lookup"><span data-stu-id="77cd6-153">Journal Line</span></span>
- <span data-ttu-id="77cd6-154">Projekto sutarties eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="77cd6-154">Project Contract Line Detail</span></span>
- <span data-ttu-id="77cd6-155">Projekto komandos narys</span><span class="sxs-lookup"><span data-stu-id="77cd6-155">Project Team Member</span></span>
- <span data-ttu-id="77cd6-156">Pasiūlymo eilutės informacija</span><span class="sxs-lookup"><span data-stu-id="77cd6-156">Quote Line Detail</span></span>
- <span data-ttu-id="77cd6-157">Vaidmens kainos antkainis</span><span class="sxs-lookup"><span data-stu-id="77cd6-157">Role Price Markup</span></span>
- <span data-ttu-id="77cd6-158">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="77cd6-158">Role Price</span></span> 
- <span data-ttu-id="77cd6-159">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="77cd6-159">Time Entry</span></span> 

> ![Esamų objektų įtraukimas į kainodaros dimensijų sprendimą](media/Existing-entities-to-PD-solution.png)

> ![Sprendimo komponentų pasirinkimas](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="77cd6-162">Būtinai įtraukite visas kiekvieno pasirinkto objekto formas ir rodinius.</span><span class="sxs-lookup"><span data-stu-id="77cd6-162">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="77cd6-163">Paraginti įtraukti priklausomus objektus iš pirmiau pasirinktų objektų, spustelėkite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="77cd6-163">When prompted to include any dependent entities for the entities selected above, click **No**.</span></span>

> ![Neįtraukite visų susijusių komponentų](media/Do-not-include-required.png)


