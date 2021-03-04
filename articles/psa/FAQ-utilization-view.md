---
title: Peržiūrėti apmokestinamą išteklių naudojimą
description: Šioje temoje pateikiama informacija apie išteklių naudojimo rodinį.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4516c562e7eaf35c5fef638183967eef5a033b11
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146403"
---
# <a name="view-chargeable-utilization-for-resources"></a><span data-ttu-id="5720a-103">Peržiūrėti apmokestinamą išteklių naudojimą</span><span class="sxs-lookup"><span data-stu-id="5720a-103">View chargeable utilization for resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]
 
<span data-ttu-id="5720a-104">Puslapyje **„Project Service“ išteklių naudojimas** **Naudojimo rodinys** rodo kiekvieno rezervuojamo ištekliaus apmokestinamą naudojimą.</span><span class="sxs-lookup"><span data-stu-id="5720a-104">The **Utilization View** on the **Project Service Resource Utilization** page shows the chargeable utilization for each bookable resource.</span></span> <span data-ttu-id="5720a-105">Kadangi rodinys grindžiamas Grafiko lenta, pamatysite, kad yra daug tokių pačių funkcijų.</span><span class="sxs-lookup"><span data-stu-id="5720a-105">Because the view is based on the schedule board, you’ll find many of the same functions.</span></span>

> ![Naudingumo rodinio ekrano nuotrauka](media/FAQ-utilization-1.png)
 

<span data-ttu-id="5720a-107">Apmokestinamo naudojimo skaičiavimas atliekamas taip:</span><span class="sxs-lookup"><span data-stu-id="5720a-107">The chargeable utilization calculation works as follows:</span></span>

   <span data-ttu-id="5720a-108">Apmokestinamas naudojimas = (Apmokestinamos faktinės valandos) / (Išteklių pajėgumas).</span><span class="sxs-lookup"><span data-stu-id="5720a-108">Chargeable utilization = (Chargeable actual hours) / (resource capacity)</span></span>

<span data-ttu-id="5720a-109">Langeliuose pateikiamas suskaičiuotas apmokestinamas naudojimas per pasirinktą laikotarpį (dienas, savaites ar mėnesius).</span><span class="sxs-lookup"><span data-stu-id="5720a-109">The cells represent the calculated chargeable utilization for the selected period (days, weeks, or months).</span></span>

<span data-ttu-id="5720a-110">Spalvos kiekviename langelyje reiškia apmokestinamą išteklio naudojimą, palyginti su tiksliniu apmokestinamu naudojimu.</span><span class="sxs-lookup"><span data-stu-id="5720a-110">The colors in each cell show the chargeable utilization for a resource as compared to their target chargeable utilization.</span></span> 

<span data-ttu-id="5720a-111">Gali būti nustatytas tikslinis numatytojo ištekliaus vaidmens arba atskiro ištekliaus naudojimas.</span><span class="sxs-lookup"><span data-stu-id="5720a-111">The target utilization can be set on the resource’s default role or on the individual resource itself.</span></span> <span data-ttu-id="5720a-112">Skaičiuojant pirma atsižvelgiama į atskirą išteklių kaip į tikslą, tada į numatytąjį ištekliaus vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="5720a-112">The calculation looks at the individual for the target first, and then to the resource’s default role.</span></span>

## <a name="set-target-on-a-resource"></a><span data-ttu-id="5720a-113">Išteklių tikslo nustatymas</span><span class="sxs-lookup"><span data-stu-id="5720a-113">Set target on a resource</span></span>

1. <span data-ttu-id="5720a-114">Eikite į **Ištekliai** \> **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="5720a-114">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="5720a-115">Pasirinkite išteklius, norėdami atidaryti įrašą.</span><span class="sxs-lookup"><span data-stu-id="5720a-115">Select a resource to open the record.</span></span> 
3. <span data-ttu-id="5720a-116">Skirtuke **Project Service** galite nustatyti ištekliaus tikslinį naudojimą.</span><span class="sxs-lookup"><span data-stu-id="5720a-116">On the **Project Service** tab, you can set the resource’s target utilization.</span></span>

> ![Skirtuko „Project Service“ naudojimo, siekiant nustatyti tikslinį naudojimą, ekrano nuotrauka](media/FAQ-utilization-2.png)
 
## <a name="set-target-utilization-on-a-role"></a><span data-ttu-id="5720a-118">Tikslinio naudojimo nustatymas vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="5720a-118">Set target utilization on a role</span></span>

1. <span data-ttu-id="5720a-119">Eikite į **Ištekliai** \> **Išteklių planavimas**.</span><span class="sxs-lookup"><span data-stu-id="5720a-119">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="5720a-120">Pasirinkite išteklius ir atidarykite įrašą.</span><span class="sxs-lookup"><span data-stu-id="5720a-120">Select a role and open the record.</span></span> 
3. <span data-ttu-id="5720a-121">Nustatyti tikslinį vaidmens naudojimą.</span><span class="sxs-lookup"><span data-stu-id="5720a-121">Set the target utilization for the role.</span></span>

> ![Dalies „Išteklių vaidmenys“ naudojimo, siekiant nustatyti tikslinį naudojimą, ekrano nuotrauka](media/FAQ-utilization-3.png)
 
## <a name="calculate-chargeable-utilization-for-a-resource"></a><span data-ttu-id="5720a-123">Apmokestinamų išteklių naudojimo skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="5720a-123">Calculate chargeable utilization for a resource</span></span>

<span data-ttu-id="5720a-124">Norėdami apskaičiuoti apmokestinamą išteklių naudojimą, turite atlikti keletą nustatymų.</span><span class="sxs-lookup"><span data-stu-id="5720a-124">To calculate chargeable utilization for a resource, you will need to complete some pre-requisites.</span></span> 

### <a name="set-default-role-for-individual-resource"></a><span data-ttu-id="5720a-125">Nustatykite numatytąjį atskiro ištekliaus vaidmenį</span><span class="sxs-lookup"><span data-stu-id="5720a-125">Set default role for individual resource</span></span>

<span data-ttu-id="5720a-126">Pirmiausia, tikslinis naudojimas turi būti nustatytas atskiram ištekliui arba išteklių vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="5720a-126">First, the target utilization must be set on either the individual resource or on resource roles.</span></span> <span data-ttu-id="5720a-127">Jei naudojate išteklių vaidmenis kaip tikslus, kiekvienas atskiras išteklius privalo turėti numatytąjį vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="5720a-127">If you are using resource roles for targets, each individual resource must have a default role.</span></span> 

1. <span data-ttu-id="5720a-128">Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** \> **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="5720a-128">To set this, go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="5720a-129">Pažymėkite išteklių, atidarykite įrašą ir pažymėkite skirtuką **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="5720a-129">Select a resource, open the record, and then select the **Project Service** tab.</span></span> 
3. <span data-ttu-id="5720a-130">Tinklelyje **Išteklių vaidmuo** įsitikinkite, kad yra vienas išteklių vaidmuo, o **Numatytoji reikšmė** nustatyta į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="5720a-130">In the **Resource Role** grid, make sure there’s one role for the resource and **Is Default** is set to **Yes**.</span></span>
 
### <a name="change-billing-type-for-resource-role"></a><span data-ttu-id="5720a-131">Pasirinkite atsiskaitymo už šį išteklių vaidmenį tipą.</span><span class="sxs-lookup"><span data-stu-id="5720a-131">Change billing type for resource role</span></span>

<span data-ttu-id="5720a-132">Išteklių vaidmenys turi būti nustatyti į atsiskaitymo tipą **Apmokestinamas**.</span><span class="sxs-lookup"><span data-stu-id="5720a-132">The resource roles must be set to have a billing type of **Chargeable**.</span></span> 

1. <span data-ttu-id="5720a-133">Eikite į **Ištekliai** \> **Išteklių planavimas**.</span><span class="sxs-lookup"><span data-stu-id="5720a-133">Go to **Resources** \> **Resource Roles**.</span></span> 
2. <span data-ttu-id="5720a-134">Atidarykite įrašą, kurį norite atnaujinti, tada nustatykite numatytąjį atsiskaitymo tipą į **Apmokestinamas**.</span><span class="sxs-lookup"><span data-stu-id="5720a-134">Open the record you want to update, and then set the billing type default to **Chargeable**.</span></span>

### <a name="set-working-hours-for-resource-role"></a><span data-ttu-id="5720a-135">Išteklių vaidmenų darbo valandų nustatymas</span><span class="sxs-lookup"><span data-stu-id="5720a-135">Set working hours for resource role</span></span>
 
<span data-ttu-id="5720a-136">Turi būti nustatytos išteklių darbo valandos, siekiant suskaičiuoti pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="5720a-136">The resource must have working hours for the capacity calculation.</span></span> 

1. <span data-ttu-id="5720a-137">Eikite į **Ištekliai** \> **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="5720a-137">Go to **Resources** \> **Resources**.</span></span> 
2. <span data-ttu-id="5720a-138">Pasirinkite išteklių, kad atidarytumėte įrašą, tada pasirinkite **Rodyti darbo valandas**.</span><span class="sxs-lookup"><span data-stu-id="5720a-138">Select a resource to open the record, and then select **Show Work Hours**.</span></span> 
3. <span data-ttu-id="5720a-139">Galite masiškai atnaujinti išteklių sąrašą, taikydami **Darbo valandų šablonas**, esantį rodinyje **Išteklių sąrašas**.</span><span class="sxs-lookup"><span data-stu-id="5720a-139">You can bulk-update the list of resources by applying a **Work Hour Template** from the **Resource List** view.</span></span>

## <a name="troubleshooting-chargeable-actual-hours"></a><span data-ttu-id="5720a-140">Apmokestinamų faktinių valandų trikčių šalinimas</span><span class="sxs-lookup"><span data-stu-id="5720a-140">Troubleshooting chargeable actual hours</span></span>

<span data-ttu-id="5720a-141">Apmokestinamos faktinės valandas gaunamos iš objekto **Faktiniai duomenys**.</span><span class="sxs-lookup"><span data-stu-id="5720a-141">The chargeable actual hours are sourced from the **Actuals** entity.</span></span> <span data-ttu-id="5720a-142">Faktiniai duomenys su atsiskaitymo tipu **Apmokestinamas** yra įtraukti į skaičiavimą, todėl privalote turėti projektus, kurių faktiniai duomenys yra apmokestinami.</span><span class="sxs-lookup"><span data-stu-id="5720a-142">Actuals with a billing type of **Chargeable** are included in the calculation and, for this reason, you must have projects where the actuals that are chargeable.</span></span>

<span data-ttu-id="5720a-143">Jei nematote apmokestinamo naudojimo, patikrinkite šiuos dalykus:</span><span class="sxs-lookup"><span data-stu-id="5720a-143">If you are not seeing chargeable utilization, here are some things you can check:</span></span>

- <span data-ttu-id="5720a-144">Apibrėžtas išteklio darbo valandų pajėgumas.</span><span class="sxs-lookup"><span data-stu-id="5720a-144">The resource has working hours defined for capacity.</span></span>
- <span data-ttu-id="5720a-145">Išteklius turi atskirai nustatytą naudojimo tikslą arba turi jam skirtą numatytąjį vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="5720a-145">The resource has either an individually defined utilization target or has a default role assigned to it.</span></span> <span data-ttu-id="5720a-146">Vaidmuo turi jam nustatytą naudojimo tikslą.</span><span class="sxs-lookup"><span data-stu-id="5720a-146">The role has a utilization target defined for it.</span></span>
- <span data-ttu-id="5720a-147">Faktiniai duomenys turi atsiskaitymo tipą **Apmokestinamas** laikotarpiui, kuriam tikitės naudojimo skaičiavimo.</span><span class="sxs-lookup"><span data-stu-id="5720a-147">Actuals have a billing type of **Chargeable** for the period you are expecting a utilization calculation for.</span></span> <span data-ttu-id="5720a-148">Jeigu matote faktinius duomenis su neapmokestinamu atsiskaitymo tipu, patikrinkite šias sąlygas:</span><span class="sxs-lookup"><span data-stu-id="5720a-148">Check the following if you are seeing actuals with billing types other than chargeable:</span></span>

  - <span data-ttu-id="5720a-149">Faktiniams duomenims naudojamas vaidmuo turi kitokį numatytąjį atsiskaitymo tipą nei apmokestinamas.</span><span class="sxs-lookup"><span data-stu-id="5720a-149">The role used on the actual has a default billing type of something other than chargeable.</span></span>
  - <span data-ttu-id="5720a-150">Projekto sutarties eilutės vaidmuo, kuriuo grindžiamas projektas, buvo nustatytas kaip neapmokestinamas.</span><span class="sxs-lookup"><span data-stu-id="5720a-150">The role on the project contract line backing the project has been set to non-chargeable.</span></span>
  - <span data-ttu-id="5720a-151">Projektas neturi susijusios sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="5720a-151">The project does not have an associated contract line.</span></span>

