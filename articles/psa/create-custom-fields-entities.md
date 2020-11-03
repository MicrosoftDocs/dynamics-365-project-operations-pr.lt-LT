---
title: Pasirinktinių laukų ir objektų kūrimas
description: Šioje temoje paaiškinama, kaip kurti parinkčių rinkinius ir objektus naudojant asmeninį sprendimą Power Apps platformoje.
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
ms.openlocfilehash: 442ff9cf2206bec307cea7ff30b9266502d8f77b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080905"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="b20c2-103">Pasirinktinių laukų ir objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="b20c2-103">Create custom fields and entities</span></span> 

<span data-ttu-id="b20c2-104">Atlikite toliau nurodytus veiksmus bet kuriuo metu, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą „Power Apps“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="b20c2-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="b20c2-105">Šioje temoje nurodytas procedūras reikia atlikti naudojant „Project Service Automation“ (PSA) internetinę sąsają.</span><span class="sxs-lookup"><span data-stu-id="b20c2-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b20c2-106">Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą.</span><span class="sxs-lookup"><span data-stu-id="b20c2-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="b20c2-107">Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="b20c2-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="b20c2-108">Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.</span><span class="sxs-lookup"><span data-stu-id="b20c2-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="b20c2-109">Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime</span><span class="sxs-lookup"><span data-stu-id="b20c2-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="b20c2-110">Kainodaros dimensija gali būti parinkčių rinkinys arba objektas.</span><span class="sxs-lookup"><span data-stu-id="b20c2-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="b20c2-111">Abu turi būti sukurti jūsų kainodaros sprendime.</span><span class="sxs-lookup"><span data-stu-id="b20c2-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="b20c2-112">Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.</span><span class="sxs-lookup"><span data-stu-id="b20c2-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="b20c2-113">Objekto dimensijos</span><span class="sxs-lookup"><span data-stu-id="b20c2-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="b20c2-114">PSA pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-114">In PSA, click **Settings** > **Solutions** , and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="b20c2-115">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="b20c2-116">Spustelėkite **Naujas** , kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="b20c2-117">Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standartinio pavadinimo objekto apibrėžtis](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="b20c2-119">Parinkčių rinkinio matmenys</span><span class="sxs-lookup"><span data-stu-id="b20c2-119">Option set-based dimensions</span></span> 
<span data-ttu-id="b20c2-120">Galite sukurti du parinkčių rinkinio matmenis.</span><span class="sxs-lookup"><span data-stu-id="b20c2-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="b20c2-121">Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje** , o pasinaudodami lauku **Išteklių darbo valandos** , su vertėmis **Įprastos** ir **Viršvalandžiai** , pritaikykite antkainį darbui pasibaigus.</span><span class="sxs-lookup"><span data-stu-id="b20c2-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="b20c2-122">PSA pasirinkite **Parametrai** > **Sprendimai** , o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-122">In PSA, click **Settings** > **Solutions** , and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="b20c2-123">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="b20c2-124">Spustelėkite **Naujas** , kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="b20c2-125">Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo vieta“</span><span class="sxs-lookup"><span data-stu-id="b20c2-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="b20c2-126">Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo valandos“</span><span class="sxs-lookup"><span data-stu-id="b20c2-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="b20c2-127">Objekto dimensijų duomenų kūrimas</span><span class="sxs-lookup"><span data-stu-id="b20c2-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="b20c2-128">Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą.</span><span class="sxs-lookup"><span data-stu-id="b20c2-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="b20c2-129">Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="b20c2-130">Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.</span><span class="sxs-lookup"><span data-stu-id="b20c2-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="b20c2-131">Apsilankę PSA spustelėkite **Išplėstinė ieška**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="b20c2-132">Pasirinkite objektą **Standartinis pavadinimas** , tada spustelėkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="b20c2-133">Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.</span><span class="sxs-lookup"><span data-stu-id="b20c2-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="b20c2-134">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-134">Click **New**.</span></span> <span data-ttu-id="b20c2-135">Lauke **Pavadinimas** įveskite „Sistemų inžinierius“, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="b20c2-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="b20c2-136">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="b20c2-136">Close the form.</span></span> 
4. <span data-ttu-id="b20c2-137">Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="b20c2-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="b20c2-138">Standartinio pavadinimo objekto duomenų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="b20c2-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)


