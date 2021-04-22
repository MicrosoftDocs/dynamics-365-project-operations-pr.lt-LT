---
title: Projekto rezervavimo kūrimas i iš Grafiko lentos
description: Šioje temoje pateikiama informacija apie tai, kaip kurti projekto rezervavimą iš grafiko lentos.
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
ms.openlocfilehash: 5d815210ee78f3c728c0722e03bab2f790c953ee
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286123"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a><span data-ttu-id="18ad4-103">Projekto rezervavimo kūrimas i iš Grafiko lentos</span><span class="sxs-lookup"><span data-stu-id="18ad4-103">Create a project booking from the Schedule board</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="18ad4-104">Išteklius projektui galite rezervuoti projekto skirtuke **„Komanda“** iš karto arba iš bendrojo komandos nario priskyrimo sugeneruodami išteklių reikalavimą ir tada jį įvykdydami su projekto komandos nariu.</span><span class="sxs-lookup"><span data-stu-id="18ad4-104">You can book a resource onto a project directly from the **Team** tab of the project or by generating a resource requirement from a generic team member assignment and then fulfilling the generated requirement with a project team member.</span></span>

<span data-ttu-id="18ad4-105">Taip pat išteklius projektui galite rezervuoti tiesiai iš Grafiko lentos.</span><span class="sxs-lookup"><span data-stu-id="18ad4-105">You can also book a resource onto a project directly from the Schedule board.</span></span> <span data-ttu-id="18ad4-106">Yra trys būdai tai padaryti:</span><span class="sxs-lookup"><span data-stu-id="18ad4-106">There are three ways to do this:</span></span>

- <span data-ttu-id="18ad4-107">**„Rezervavimas iš sugeneruoto ištekliaus reikalavimo“:** sukūrę bendrąjį išteklių ir priskyrę užduotis projekte galite sugeneruoti išteklių reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="18ad4-107">**Book from a generated resource requirement:** You can generate a resource requirement after you create a generic resource and assign tasks within a project.</span></span>

- <span data-ttu-id="18ad4-108">**„Rezervavimas iš pagrindinio reikalavimo“:** pagrindiniai reikalavimai rodomi Grafiko lentoje, skirtuke **„Projektas“**.</span><span class="sxs-lookup"><span data-stu-id="18ad4-108">**Book from the primary requirement:** The primary requirements show up on the Schedule board on the **Project** tab.</span></span> 

- <span data-ttu-id="18ad4-109">**„Rezervavimas iš naujo ištekliaus reikalavimo“:** galite iš naujo sukurti išteklių reikalavimą ir susieti jį su projektu.</span><span class="sxs-lookup"><span data-stu-id="18ad4-109">**Book from a new resource requirement:** You can create a resource requirement from scratch and associate it with a project.</span></span> <span data-ttu-id="18ad4-110">Grafiko lentoje išteklių reikalavimai rodomi skirtuke **„Atidaryti reikalavimus“**.</span><span class="sxs-lookup"><span data-stu-id="18ad4-110">On the Schedule board, the resource requirement shows up on the **Open Requirements** tab.</span></span>

## <a name="book-from-a-generated-resource-requirement"></a><span data-ttu-id="18ad4-111">Rezervavimas iš sugeneruoto išteklių reikalavimo</span><span class="sxs-lookup"><span data-stu-id="18ad4-111">Book from a generated resource requirement</span></span>

<span data-ttu-id="18ad4-112">Galite sukurti bendrąjį išteklių ir projekte jam priskirti vieną ar kelias užduotis.</span><span class="sxs-lookup"><span data-stu-id="18ad4-112">You can create a generic resource and assign it one or more tasks within a project.</span></span> <span data-ttu-id="18ad4-113">Tada galite generuoti išteklių reikalavimą iš bendrojo komandos nario.</span><span class="sxs-lookup"><span data-stu-id="18ad4-113">Then you can generate a resource requirement from the generic team member.</span></span> 

1.  <span data-ttu-id="18ad4-114">Grafiko lentoje šie ištekliai bus matomi skirtuke **„Atidaryti reikalavimus“**. Jei turite daug atidarytų reikalavimų, jums gali tekti panaudoti stulpelio filtrus, esančius tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="18ad4-114">On the Schedule board, this resource will show up on the **Open Requirements** tab. You might need to use column filters on the grid if you have many open requirements.</span></span> 

    <span data-ttu-id="18ad4-115">![Reikalavimų skirtuko atidarymas grafiko lentoje](media/FAQ-Project-Booking-Schedule-Board-1.png "Rezervavimo ir užduočių lentelės ekrano nuotrauka")</span><span class="sxs-lookup"><span data-stu-id="18ad4-115">![Open Requirements tab on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-1.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="18ad4-116">Pasirinkite reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="18ad4-116">Select the requirement.</span></span> <span data-ttu-id="18ad4-117">Skirtukas **„Rasti pasiekiamumą“** matomas pasirinktos eilutės viršuje.</span><span class="sxs-lookup"><span data-stu-id="18ad4-117">The **Find Availability** tab will appear at the top of the selected row.</span></span>
 
3. <span data-ttu-id="18ad4-118">Pasirinkus skirtuką paleidžiamas Grafiko lentos pagalbinės planavimo priemonės režimas ir atrenkami galimi ištekliai, atitinkantys ištekliaus reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="18ad4-118">When you select the tab, the Schedule Assistant mode of the Schedule board opens and then filters the available resources that meet the resource requirement.</span></span> <span data-ttu-id="18ad4-119">Tada jau galite rezervuoti išteklius.</span><span class="sxs-lookup"><span data-stu-id="18ad4-119">After that, you can book a resource.</span></span>

4. <span data-ttu-id="18ad4-120">Taip pat galite nuvilkti pasirinktą eilutę iš Grafiko lentos apačios į išteklių langelį, esantį tinklelio viršuje.</span><span class="sxs-lookup"><span data-stu-id="18ad4-120">You can also drag and drop the selected row from the bottom of the Schedule board to a resource cell in the grid above.</span></span> <span data-ttu-id="18ad4-121">Jį paleidus dešinėje atidaromas skydas **„Kurti išteklių rezervavimą“**.</span><span class="sxs-lookup"><span data-stu-id="18ad4-121">When you drop it, it opens the **Create Resource Booking** panel on the right.</span></span>

    <span data-ttu-id="18ad4-122">Pasirinkus **„Rezervuoti“** rezervuojami ištekliai projekto komandai.</span><span class="sxs-lookup"><span data-stu-id="18ad4-122">Selecting **Book** books the resource onto the project team.</span></span>

![Kurti išteklių rezervavimo sritį](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a><span data-ttu-id="18ad4-124">Rezervavimas iš pirminio reikalavimo</span><span class="sxs-lookup"><span data-stu-id="18ad4-124">Book from the Primary Requirement</span></span>

<span data-ttu-id="18ad4-125">Sukūrus projektą „Project Service“ programoje, automatiškai sukuriamas išteklių reikalavimas, vadinamas pirminiu reikalavimu.</span><span class="sxs-lookup"><span data-stu-id="18ad4-125">Creating a project in Project Service automatically creates a resource requirement called the Primary Requirement.</span></span> <span data-ttu-id="18ad4-126">Šis reikalavimas yra tuščias ir naudojamas norint greitai rezervuoti išteklius Grafiko lentoje, išvengiant reikalavimo generavimo arba jo kūrimo iš naujo.</span><span class="sxs-lookup"><span data-stu-id="18ad4-126">This is an empty requirement that is used to quickly book a resource with the Schedule board without generating a requirement or creating one from scratch.</span></span> <span data-ttu-id="18ad4-127">Kadangi reikalavimas yra tuščias, turėsite nurodyti datas, paskirstymo metodą ir valandas, jei tai yra taikoma.</span><span class="sxs-lookup"><span data-stu-id="18ad4-127">Because the requirement is empty, you’ll need to specify dates as well as the allocation method and hours, if applicable.</span></span> 

1. <span data-ttu-id="18ad4-128">Norėdami rezervuoti išteklius iš pagrindinio reikalavimo Grafiko lentoje, pasirinkite skirtuką **„Projektas“**. Jei turite daug projektų, gali tekti stulpelyje **„Projektas“** panaudoti stulpelio filtrą.</span><span class="sxs-lookup"><span data-stu-id="18ad4-128">To book a resource with the Primary Requirement, on the Schedule board, select the **Project** tab. You might need to use the column filter on the **Project** column if you have many projects.</span></span>

   <span data-ttu-id="18ad4-129">![Stulpelio filtrai grafiko lentoje](media/FAQ-Project-Booking-Schedule-Board-2.png "Rezervavimo ir užduočių lentelės ekrano nuotrauka")</span><span class="sxs-lookup"><span data-stu-id="18ad4-129">![Column filters on the Schedule board](media/FAQ-Project-Booking-Schedule-Board-2.png "Screenshot of bookings and assignments table")</span></span>

2. <span data-ttu-id="18ad4-130">Pasirinkite reikalavimą, kurio pavadinimo laukelyje įrašytas projekto pavadinimas, o trukmė – 0.</span><span class="sxs-lookup"><span data-stu-id="18ad4-130">Select the requirement that only has the project name as its name and has a duration of zero (0).</span></span>

3. <span data-ttu-id="18ad4-131">Pasirinkite skirtuką **„Rasti pasiekiamumą“**, atsirandantį eilutėje.</span><span class="sxs-lookup"><span data-stu-id="18ad4-131">Select the **Find Availability** tab that appears on the row.</span></span> <span data-ttu-id="18ad4-132">Atlikus šį veiksmą Grafiko lentoje įjungiamas pagalbinės planavimo priemonės režimas ir parodomi galimi ištekliai, kuriuos galima rezervuoti projektui.</span><span class="sxs-lookup"><span data-stu-id="18ad4-132">This puts the Schedule board in Schedule Assistant mode and shows the available resources that can be booked onto the project.</span></span>

4. <span data-ttu-id="18ad4-133">Kadangi **„Pagrindinis reikalavimas“** yra tuščias reikalavimas, o jo trukmė – 0, rinkdamiesi ir rezervuodami išteklius srityje **„Kurti išteklių rezervavimą”** turėsite nustatyti trukmę.</span><span class="sxs-lookup"><span data-stu-id="18ad4-133">Because a **Primary Requirement** is an empty requirement with zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when selecting and booking a resource.</span></span>

5. <span data-ttu-id="18ad4-134">Taip pat Grafiko lentos apačioje galite pasirinkti **„Pagrindinis projekto reikalavimas“** bei jį nuvilkti ant išteklių, kad juos rezervuotumėte.</span><span class="sxs-lookup"><span data-stu-id="18ad4-134">You can also select the **Project Primary Requirement** at the bottom of the Schedule board and drag and drop it on a resource to book it.</span></span>
 
    <span data-ttu-id="18ad4-135">Kadangi **„Pagrindinis reikalavimas“** yra tuščias reikalavimas, o jo trukmė – 0, rinkdamiesi ir rezervuodami išteklius srityje **„Kurti išteklių rezervavimą”** turėsite nustatyti trukmę.</span><span class="sxs-lookup"><span data-stu-id="18ad4-135">Because the **Primary Requirement** is an empty requirement that has zero (0) duration, you’ll need to set the duration on the **Create Resource Booking** panel when you select and book a resource.</span></span>
 
    <span data-ttu-id="18ad4-136">Rezervuodami išteklius Grafiko lentoje per **„Pagrindinis reikalavimas“**, išteklius prie projekto komandos pridedate be jokių užduočių.</span><span class="sxs-lookup"><span data-stu-id="18ad4-136">When you book a resource through the **Primary Requirement** on the Schedule board, you add it to the project team without any assignments.</span></span>
 
## <a name="book-from-a-new-resource-requirement"></a><span data-ttu-id="18ad4-137">Rezervavimas iš naujo išteklių reikalavimo</span><span class="sxs-lookup"><span data-stu-id="18ad4-137">Book from a new resource requirement</span></span>
<span data-ttu-id="18ad4-138">Atlikite šiuos veiksmus norėdami rezervuoti iš naujo išteklių reikalavimo.</span><span class="sxs-lookup"><span data-stu-id="18ad4-138">Complete the following steps to book from a new resource requirement.</span></span> 

1. <span data-ttu-id="18ad4-139">Norėdami sukurti naują išteklių reikalavimą, eikite į **„Išteklių reikalavimai”** ir pasirinkite **„Naujas”**.</span><span class="sxs-lookup"><span data-stu-id="18ad4-139">Go to **Resource Requirements**, and then select **New** to create a new resource requirement.</span></span>

2. <span data-ttu-id="18ad4-140">Skirtuke **„Projektas“** pažymėkite projektą, kurį reikia susieti su reikalavimu.</span><span class="sxs-lookup"><span data-stu-id="18ad4-140">On the **Project** tab, select a project to associate the requirement to the project.</span></span>
 
    <span data-ttu-id="18ad4-141">Šis naujai sukurtas reikalavimas Grafiko lentoje rodomas kaip **„Atidaryti reikalavimą“**, kurį galite įvykdyti.</span><span class="sxs-lookup"><span data-stu-id="18ad4-141">On the Schedule board, this new requirement shows as an **Open Requirement** that you can fulfill.</span></span>

3. <span data-ttu-id="18ad4-142">Rezervuokite išteklius, kad jie būtų įtraukti į projekto komandą.</span><span class="sxs-lookup"><span data-stu-id="18ad4-142">Book the resource to add it to the project team.</span></span>

4. <span data-ttu-id="18ad4-143">Kai ištekliai jau rezervuoti, reikia rankiniu būdu priskirti užduotis.</span><span class="sxs-lookup"><span data-stu-id="18ad4-143">Now that the resource is booked, you must assign tasks manually.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]