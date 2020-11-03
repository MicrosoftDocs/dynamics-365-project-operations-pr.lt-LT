---
title: Išteklių priskyrimas užduočiai
description: Šioje temoje pateikiama informacija apie tai, kaip priskirti išteklius užduotims.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 77f13d1e96b76dfea241fbf7a67d5676582f0235
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081025"
---
# <a name="assign-a-resource-to-a-task"></a><span data-ttu-id="e1bb2-103">Išteklių priskyrimas užduočiai</span><span class="sxs-lookup"><span data-stu-id="e1bb2-103">Assign a resource to a task</span></span>

<span data-ttu-id="e1bb2-104">Ištekliui priskirti užduotį programoje Microsoft Dynamics 365 Project Service Automation galima trimis būdais.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-104">There are three ways to assign a resource to a task in Microsoft Dynamics 365 Project Service Automation.</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="e1bb2-105">Rezervuokite išteklius kaip komandos narys, o tada priskirkite išteklių užduočiai</span><span class="sxs-lookup"><span data-stu-id="e1bb2-105">Book a resource as a team member, and then assign the resource to a task</span></span>

<span data-ttu-id="e1bb2-106">Galite pridėti išteklių prie projekto komandos, o tada projekto grafike juos priskirti užduotims.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-106">You can add a resource to the project team, and then assign the resource to tasks in the project schedule.</span></span>

1. <span data-ttu-id="e1bb2-107">Skirtuke **„Komandos narys“** pridėkite naują komandos narį, pasirinkdami **„Naujas“**.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-107">On the **Team Member** tab, add a new team member by selecting **New**.</span></span> 

2. <span data-ttu-id="e1bb2-108">Atidaroma sritis **„Spartusis komandos nario kūrimas“** , kuriame galima pasirinkti rezervuojamą išteklių pavadinimą ir nustatyti vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-108">The **Team Member Quick Create** panel opens, where you can select the bookable resource name and set a role.</span></span> 

    <span data-ttu-id="e1bb2-109">Pasirinkite vieną iš pateiktų išteklių rezervavimo paskirstymo metodų:</span><span class="sxs-lookup"><span data-stu-id="e1bb2-109">Select one of the following allocation methods for the resource’s booking:</span></span>

    - <span data-ttu-id="e1bb2-110">**Visas pajėgumo metodas**  – rezervuojamas visas išteklių pajėgumas tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-110">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e1bb2-111">**Pajėgumo procentinės dalies rezervavimo metodas**  – rezervuojama išteklių pajėgumo dalis procentais tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-111">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="e1bb2-112">**Tolygiai paskirstomų valandų metodas**  – ištekliai rezervuojami nurodytam valandų skaičiui, kiekvienai dienai skirtą laiką tolygiai paskirstant nuo nurodyto laikotarpio pradžios ir pabaigos.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-112">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing them evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="e1bb2-113">**Pirminės apkrovos metodas**  – ištekliai rezervuojami į išteklių naudojimo pradžios dieną keliant didžiausią dienos valandų skaičių tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-113">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>
    - <span data-ttu-id="e1bb2-114">**Joks**  – ištekliai pridedami prie komandos, tačiau rezervavimai, kurie sunaudoja išteklių pajėgumą, nesukuriami.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-114">**None** adds the resource to the team but doesn’t create any bookings that absorb their capacity.</span></span>

3. <span data-ttu-id="e1bb2-115">Užduoties tinklelyje **„Grafikas“** pasirinkite išteklių langelyje esančią piktogramą **„Ištekliai“** , o tada skirtuke **„Komandos nariai“** pasirinkite ką tik pridėtą komandos narį.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-115">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell, and then under **Team Members** , select the team member you just added.</span></span> 

> [!NOTE]
> <span data-ttu-id="e1bb2-116">Skirtukuose **„Komandos narys“** ir **„Derinimas“** matomos rezervuotos ir priskirtos išteklių valandos.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-116">On the **Team Member** and **Reconciliation** tabs, the resource shows booked and assigned hours.</span></span> <span data-ttu-id="e1bb2-117">Jų valandos turėtų būti vienodos, tačiau tai nėra privaloma, nes rezervavimas ir priskyrimai nėra tvirtai susieti.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-117">The hours should be the same, but it isn't required as bookings and assignments are not tightly coupled.</span></span> <span data-ttu-id="e1bb2-118">Skirtuke **„Derinimas“** galite rasti informaciją apie tai, kada jie skiriasi, pavyzdžiui, kada ištekliams priskiriate daugiau valandų nei rezervavote.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-118">The **Reconciliation** tab gives you details when they are different, such as when you assign a resource more hours than you have booked.</span></span> <span data-ttu-id="e1bb2-119">Tuomet, jeigu reikia, galite taisyti informaciją – prailginti išteklių rezervavimą arba pakeisti priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-119">If needed, you can correct the information by extending the resource's bookings or changing the assignment.</span></span>

## <a name="create-a-generic-team-member-through-task-assignment"></a><span data-ttu-id="e1bb2-120">Bendrojo komandos nario kūrimas priskiriant užduotį</span><span class="sxs-lookup"><span data-stu-id="e1bb2-120">Create a generic team member through task assignment</span></span>

<span data-ttu-id="e1bb2-121">Kai sukuriate bendrąjį komandos narį priskirdami jam užduotį, taip pat sukuriate vietos rezervavimo ženklą arba bendrąjį išteklių, kuriuo būtų nurodoma įvardyto ištekliaus, su kuriuo norite atlikti užduotis, charakteristika.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-121">When you create a generic team member through task assignment, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks.</span></span> <span data-ttu-id="e1bb2-122">Tada galite generuoti reikalavimą (arba pateikti užklausą naudojant reikalavimą), kuris yra naudojamas įvardytų išteklių paieškai ir rezervavimui atlikti.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-122">You then generate a requirement (or submit a request using the requirement) that is used to search for and book the named resource.</span></span>

1. <span data-ttu-id="e1bb2-123">Užduoties tinklelyje **„Grafikas“** pasirinkite išteklių langelyje esančią piktogramą **„Ištekliai“**.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-123">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="e1bb2-124">Įveskite pavadinimą, kuris bus vietos rezervavimo ženklo išteklių pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-124">Type a name to serve as the placeholder resource’s name.</span></span> <span data-ttu-id="e1bb2-125">Pavyzdžiui, „Programos vadovas“.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-125">For example, Program Manager.</span></span>

3. <span data-ttu-id="e1bb2-126">Pasirinkite **„Kurti“** , o tada lauke **„Spartusis projekto komandos nario kūrimas“** nustatykite bendrųjų išteklių vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-126">Select **Create** , and in the **Quick Create Project Team Member** field, set the role for the generic resource.</span></span>

4. <span data-ttu-id="e1bb2-127">Užduoties **„Išteklių išrinkiklyje“** pasirinkę išteklius galite toliau priskirti užduotis šiems vietos rezervavimo ženklo ištekliams.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-127">You can continue to assign tasks to this placeholder resource by selecting the resource on the **Resource Selector** for the task.</span></span> <span data-ttu-id="e1bb2-128">Jie išvardyti skirtuke **„Komandos nariai“**.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-128">They’re listed under **Team Members**.</span></span>

5. <span data-ttu-id="e1bb2-129">Priskyrę bendruosius išteklius, skirtuke **„Komanda“** pasirinkite bendruosius išteklius, tada pasirinkite **„Generuoti reikalavimą“** ir sukurkite išteklių reikalavimą bendriesiems ištekliams.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-129">When you’re done assigning the generic resource, select the generic resource on the **Team** tab, and then select **Generate Requirement** to create a resource requirement for the generic resource.</span></span>

6. <span data-ttu-id="e1bb2-130">Bendriesiems ištekliams pasirinkite **„Rezervuoti“**.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-130">Select **Book** for the generic resource.</span></span> <span data-ttu-id="e1bb2-131">Tada, norėdami rasti tikrus išteklius, pasinaudokite Grafiko lenta.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-131">You can then use the Schedule board to find and book a real resource.</span></span> <span data-ttu-id="e1bb2-132">Taip pat galite išteklių vadovui pateikti reikalavimą, kad jis būtų įvykdytas.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-132">You can also submit the requirement for fulfillment by a resource manager.</span></span>

7. <span data-ttu-id="e1bb2-133">Kai bendrieji ištekliai pakeičiami įvardytais ištekliais, bendrieji ištekliai yra pašalinami iš komandos, o jiems paskirtos užduotys paskiriamos įvardytiems ištekliams, kuriais pakeičiami bendrųjų išteklių išteklių reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-133">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>

## <a name="assign-a-named-resource-from-the-list-of-all-bookable-resources"></a><span data-ttu-id="e1bb2-134">Įvardytų išteklių priskyrimas iš visų rezervuojamų išteklių sąrašo</span><span class="sxs-lookup"><span data-stu-id="e1bb2-134">Assign a named resource from the list of all bookable resources</span></span>

<span data-ttu-id="e1bb2-135">Jei norite ieškoti rezervuojamų išteklių ir juos priskirti užduočiai, galite pasinaudoti **„Išteklių išrinkiklio“** ieškos lauku.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-135">You can use the search box in the **Resource Selector** to search all bookable resources and assign them to a task.</span></span>

<span data-ttu-id="e1bb2-136">Tokiu būdu priskirti ištekliai įtraukiami į komandą neatliekant jokių rezervacijų.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-136">Resources assigned this way are added to the team without any bookings.</span></span> <span data-ttu-id="e1bb2-137">Taip pat galima įtraukti komandos narį ir vietoj paskirstymo metodo pažymėti „Nėra“.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-137">This is similar to adding a team member and selecting None as the allocation method.</span></span> <span data-ttu-id="e1bb2-138">Ištekliai yra rodomi skirtukuose **„Komanda“** ir **„Derinimas“** kaip ištekliai, turintys tik priskyrimus ir rezervavimo deficitus.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-138">The resource is displayed in the **Team** and **Reconciliation** tabs as resources with only assignments and a booking deficit.</span></span> <span data-ttu-id="e1bb2-139">Jei norite pasinaudoti jų prieinamumu, juos rezervuokite.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-139">Book them if you want to use their availability.</span></span>

1. <span data-ttu-id="e1bb2-140">Užduoties tinklelyje **„Grafikas“** pasirinkite išteklių langelyje esančią piktogramą **„Ištekliai“**.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-140">On the **Schedule** grid for a task, select the **Resource** icon in the resource cell.</span></span>

2. <span data-ttu-id="e1bb2-141">Pradėkite rašyti pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-141">Start typing a name.</span></span> <span data-ttu-id="e1bb2-142">Pavadinimo ieškos rezultatai pateikiami **„Išteklių išrinkiklis“** , parinktyje **„Kiti ištekliai“**.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-142">The search results for the name are displayed in the **Resource Selector** under **Other Resources**.</span></span>

3. <span data-ttu-id="e1bb2-143">Pažymėkite išteklių, kurį norite priskirti prie užduoties.</span><span class="sxs-lookup"><span data-stu-id="e1bb2-143">Select the resource that you want to assign to the task.</span></span>

