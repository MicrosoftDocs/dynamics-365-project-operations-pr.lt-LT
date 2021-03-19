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
ms.openlocfilehash: c58745a46e84a40b90fbb3cbf89b10e293588fc3
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290548"
---
# <a name="create-custom-fields-and-entities"></a><span data-ttu-id="e2b66-103">Pasirinktinių laukų ir objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="e2b66-103">Create custom fields and entities</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="e2b66-104">Atlikite toliau nurodytus veiksmus bet kuriuo metu, kai norite sukurti pasirinktinį parinkčių rinkinį arba objektą „Power Apps“ platformoje.</span><span class="sxs-lookup"><span data-stu-id="e2b66-104">Complete the following steps any time that you want to create a custom option set or entity on the Power Apps platform.</span></span>  
<span data-ttu-id="e2b66-105">Šioje temoje nurodytas procedūras reikia atlikti naudojant „Project Service Automation“ (PSA) internetinę sąsają.</span><span class="sxs-lookup"><span data-stu-id="e2b66-105">The procedures in this topic should be completed using the web interface of Project Service Automation (PSA).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="e2b66-106">Rekomenduojame visus pasirinktinio kainodaros dimensijų pakeitimus atlikti naudojant atskirą sprendimą.</span><span class="sxs-lookup"><span data-stu-id="e2b66-106">We recommend that you make all custom pricing dimension changes in a separate solution.</span></span> <span data-ttu-id="e2b66-107">Ši svarbi geriausia praktika suteikia lankstumo ateityje siekiant tinkamai atnaujinti arba pašalinti pakeitimus ir padės pakartotinai panaudoti savo darbą, o pakeitimus bus galima lengviau perkelti į kitą egzempliorių.</span><span class="sxs-lookup"><span data-stu-id="e2b66-107">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="e2b66-108">Atlikę visus reikiamus pakeitimus, eksportuokite šį sprendimą kaip **valdomąjį sprendimą** ir importuokite jį į kitus egzempliorius, kad būtų galima pakartotinai naudoti kainodaros nustatymus.</span><span class="sxs-lookup"><span data-stu-id="e2b66-108">After you have made all of the required changes, export this solution as a **Managed solution** and import it into other instances to reuse your pricing setup.</span></span>

  
## <a name="create-custom-fields-and-option-sets-in-the-pricing-dimension-solution"></a><span data-ttu-id="e2b66-109">Pasirinktinių laukų ir parinkčių rinkinių kūrimas kainodaros dimensijos sprendime</span><span class="sxs-lookup"><span data-stu-id="e2b66-109">Create custom fields and option sets in the pricing dimension solution</span></span>

<span data-ttu-id="e2b66-110">Kainodaros dimensija gali būti parinkčių rinkinys arba objektas.</span><span class="sxs-lookup"><span data-stu-id="e2b66-110">A pricing dimension can be an option set or an entity.</span></span> <span data-ttu-id="e2b66-111">Abu turi būti sukurti jūsų kainodaros sprendime.</span><span class="sxs-lookup"><span data-stu-id="e2b66-111">Both must be created in your pricing solution.</span></span> <span data-ttu-id="e2b66-112">Šioje procedūroje nurodytuose veiksmuose paaiškinta, kaip kurti objekto dimensijas ir parinkčių rinkinio dimensijas.</span><span class="sxs-lookup"><span data-stu-id="e2b66-112">The steps in this procedure explain how to create entity-based dimensions and option set-based dimensions.</span></span>

### <a name="entity-based-dimensions"></a><span data-ttu-id="e2b66-113">Objekto dimensijos</span><span class="sxs-lookup"><span data-stu-id="e2b66-113">Entity-based dimensions</span></span>

1. <span data-ttu-id="e2b66-114">PSA pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-114">In PSA, click **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span>
2. <span data-ttu-id="e2b66-115">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Objektai**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-115">In Solution Explorer, on the left navigation pane, select **Entities**.</span></span>
3. <span data-ttu-id="e2b66-116">Spustelėkite **Naujas**, kad sukurtumėte naują objektą pavadinimu **Standartinis pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-116">Click **New** to create a new entity called **Standard Title**.</span></span> <span data-ttu-id="e2b66-117">Įveskite trūkstamą reikiamą informaciją ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-117">Enter the remaining required information, and then click **Save**.</span></span>

> ![Standartinio pavadinimo objekto apibrėžtis](media/Standard-Title-entity-definition.png)


### <a name="option-set-based-dimensions"></a><span data-ttu-id="e2b66-119">Parinkčių rinkinio matmenys</span><span class="sxs-lookup"><span data-stu-id="e2b66-119">Option set-based dimensions</span></span> 
<span data-ttu-id="e2b66-120">Galite sukurti du parinkčių rinkinio matmenis.</span><span class="sxs-lookup"><span data-stu-id="e2b66-120">You can create two option set-based dimensions.</span></span> <span data-ttu-id="e2b66-121">Pasinaudokite lauku **Išteklių darbo vieta** ir sekite darbą **namų** vietoje bei **darbo vietoje**, o pasinaudodami lauku **Išteklių darbo valandos**, su vertėmis **Įprastos** ir **Viršvalandžiai**, pritaikykite antkainį darbui pasibaigus.</span><span class="sxs-lookup"><span data-stu-id="e2b66-121">Use **Resource Work Location** to track the price of **Home** location work and **Onsite** work and use **Resource Work hours** with values **Regular** and **Overtime** to apply a markup when work is completed.</span></span>


1. <span data-ttu-id="e2b66-122">PSA pasirinkite **Parametrai** > **Sprendimai**, o tada dukart spustelėkite **\<your organization name> kainodaros dimensijos**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-122">In PSA, click **Settings** > **Solutions**, and then double-click  **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="e2b66-123">Sprendimų naršyklėje, kairiojoje naršymo srities pusėje, pasirinkite **Parinkčių rinkiniai**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-123">In Solution Explorer, on the left navigation pane, select  **Option Sets**.</span></span> 
3. <span data-ttu-id="e2b66-124">Spustelėkite **Naujas**, kad sukurtumėte naują parinkčių rinkinį, įveskite trūkstamą būtiną informaciją, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-124">Click **New** to create a new option set, enter the remaining required information, and then click **Save**.</span></span>

> ![<span data-ttu-id="e2b66-125">Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo vieta“</span><span class="sxs-lookup"><span data-stu-id="e2b66-125">Option set based pricing dimension called Resource Work Location</span></span> ](media/Option-set-PD-called-Resource-Work-Location.png)

> ![<span data-ttu-id="e2b66-126">Kainodaros dimensijos parinkčių rinkinys „Išteklių darbo valandos“</span><span class="sxs-lookup"><span data-stu-id="e2b66-126">Option set based pricing dimension called Resource Work Hours</span></span> ](media/Option-set-PD-called-Resource-Work-Hours.PNG)


## <a name="create-data-for-entity-based-dimensions"></a><span data-ttu-id="e2b66-127">Objekto dimensijų duomenų kūrimas</span><span class="sxs-lookup"><span data-stu-id="e2b66-127">Create data for entity-based dimensions</span></span>

<span data-ttu-id="e2b66-128">Objektų dimensijų duomenis galite kurti rankiniu būdu arba naudodami „Microsoft Excel“ importavimo ar aptarnavimo komandų iškvietimą.</span><span class="sxs-lookup"><span data-stu-id="e2b66-128">You can create data for entity-based dimensions manually, or by using Microsoft Excel import or service calls.</span></span> <span data-ttu-id="e2b66-129">Atlikite šioje procedūroje nurodytus veiksmus, kad du standartinius pavadinimus – **Sistemų inžinierius** ir **Vyresnysis sistemų inžinierius** – sukurtumėte pagal objekto dimensijos **standartinį pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-129">Use the steps in this procedure to create two standard titles, **Systems Engineer** and **Senior Systems Engineer** from the entity-based dimension, **Standard Title**.</span></span> <span data-ttu-id="e2b66-130">Jei duomenys, kuriuos norite sukurti, yra maži, kaip toliau pateiktame pavyzdyje, galite naudoti standartinę formą.</span><span class="sxs-lookup"><span data-stu-id="e2b66-130">If the data that you want to create is small, as in the following example, you can use a standard form.</span></span>

1. <span data-ttu-id="e2b66-131">Apsilankę PSA spustelėkite **Išplėstinė ieška**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-131">In PSA, click **Advanced Find**.</span></span> <span data-ttu-id="e2b66-132">Pasirinkite objektą **Standartinis pavadinimas**, tada spustelėkite **Rezultatai**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-132">Select the entity **Standard Title** and then click **Results**.</span></span> <span data-ttu-id="e2b66-133">Bus rodomos visos objekto **Standartinis pavadinimas** eilutės.</span><span class="sxs-lookup"><span data-stu-id="e2b66-133">All of the rows in the **Standard Title** entity will be shown.</span></span>
2. <span data-ttu-id="e2b66-134">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-134">Click **New**.</span></span> <span data-ttu-id="e2b66-135">Lauke **Pavadinimas** įveskite „Sistemų inžinierius“, tada spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="e2b66-135">In the **Name** field, enter "Systems Engineer" and then click **Save**.</span></span>
3. <span data-ttu-id="e2b66-136">Uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="e2b66-136">Close the form.</span></span> 
4. <span data-ttu-id="e2b66-137">Pakartokite 1–3 veiksmus, kad sukurtumėte kitą standartinį vyresniojo sistemų inžinieriaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e2b66-137">Repeat steps 1 - 3 to create another standard title for "Senior Systems Engineer".</span></span>

> ![<span data-ttu-id="e2b66-138">Standartinio pavadinimo objekto duomenų pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="e2b66-138">Sample Data for Standard Title entity</span></span> ](media/ST-data.png)




[!INCLUDE[footer-include](../includes/footer-banner.md)]