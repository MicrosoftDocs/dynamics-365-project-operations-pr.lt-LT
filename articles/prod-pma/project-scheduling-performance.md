---
title: Projekto išteklių planavimo efektyvumas
description: Šioje temoje pateikta informacija apie tai, kaip padidinti daugelio projektų išteklių planavimo efektyvumą.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: c3f219ce0635545976a6a4639233f166e18468af
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080819"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="a3e9c-103">Projekto išteklių planavimo efektyvumas</span><span class="sxs-lookup"><span data-stu-id="a3e9c-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="a3e9c-104">Kai projektų skaičius pasiekia tūkstančius, gali atsirasti su išteklių planavimu susijusių efektyvumo problemų.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="a3e9c-105">Norint padidinti išteklių planavimo efektyvumą yra funkcija, leidžianti naudotojams sutrumpinti laiką, kurio reikia norint paleisti išteklių pasiekiamumo formą.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="a3e9c-106">Tiksliau kalbant, taip pašalinamas išteklių pajėgumo sumavimo sinchronizavimo procesas ir naudojama lentelė **ResProjectResource** , kad paspartėtų išteklių peržvalga.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="a3e9c-107">Atkreipkite dėmesį, kad lentelė **ResRollup** nebebus naudojama.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="a3e9c-108">Jei yra priklausomybė nuo išteklių pajėgumų sumavimo sinchronizavimo proceso arba lentelės **ResProjectResource** , šios funkcijos nenaudokite.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a3e9c-109">Išteklių planavimo efektyvumo didinimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="a3e9c-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="a3e9c-110">Norėdami įjungti išteklių planavimo efektyvumo didinimą atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="a3e9c-111">Eikite į **Funkcijų valdymas** > **Visi** ir funkcijų sąraše raskite **Įjungti projektų išteklių planavimo efektyvumo didinimo funkciją**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-111">Go to **Feature management** > **All** , and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a3e9c-112">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="a3e9c-113">Jei funkcijos nerandate sąraše, pasirinkite **Tikrinti, ar yra naujinimų** norėdami sąrašą atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="a3e9c-114">Atnaujinkite naršyklę, tada eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projektų ištekliai** > **Sinchronizuoti išteklių kalendorių pajėgumą visose įmonėse**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="a3e9c-115">Nustatykite **Pašalinti esamus pajėgumų įrašus** į **Taip** norėdami pašalinti ankstesnius duomenis.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a3e9c-116">Jei norite generuoti papildančiuosius duomenis, nustatykite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="a3e9c-117">Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio duomenys turėtų būti generuojami.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a3e9c-118">Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datos nebūtina apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="a3e9c-119">Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="a3e9c-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="a3e9c-121">Tada bendri duomenys bus paskirstyti lentelėje **ResCalendarCapacity** visoms jūsų aplinkos įmonėms, kad paketinę užduotį pakaktų paleisti tik viename juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a3e9c-122">Šios paketinės užduoties duomenys yra reikalingi norint apskaičiuoti išteklių pajėgumą susietame kalendoriuje.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="a3e9c-123">Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projektų ištekliai** > **Užpildyti projektų išteklius visose įmonėse** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="a3e9c-124">Tai bendrų duomenų atnaujinimo scenarijus lentelėse **ResProjectResource** , **ResCalendarDateTimeRange** ir **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-124">This is the data upgrade script for general data in the **ResProjectResource** , **ResCalendarDateTimeRange** , and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="a3e9c-125">Lauko **PSAPRojSchedRole.RootActivity** reikšmės taip pat atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="a3e9c-126">Jei tai nevykdoma, gausite įspėjimą, kai bandysite vykdyti išteklių planavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="a3e9c-127">Išteklių planavimo efektyvumo didinimo išjungimas</span><span class="sxs-lookup"><span data-stu-id="a3e9c-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="a3e9c-128">Eikite į **Funkcijų valdymas** > **Visi** ir raskite **Įjungti projektų išteklių planavimo efektyvumo didinimo funkciją**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="a3e9c-129">Pasirinkite funkciją ir mygtuką **Išjungti**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="a3e9c-130">Atnaujinkite naršyklę.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-130">Refresh your browser.</span></span>
4. <span data-ttu-id="a3e9c-131">Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Pajėgumų sinchronizavimas** > **Sinchronizuoti išteklių pajėgumų sumavimą**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="a3e9c-132">Puslapyje **Pajėgumų sumavimo sinchronizavimas** nustatykite **Šalinti esamus pajėgumų įrašus** į **Taip** norėdami pašalinti ankstesnius duomenis.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="a3e9c-133">Jei norite generuoti papildančiuosius duomenis, nustatykite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="a3e9c-134">Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio duomenys turėtų būti generuojami.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="a3e9c-135">Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datos nebūtina apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="a3e9c-136">Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="a3e9c-137">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="a3e9c-138">Tada bendri duomenys bus paskirstyti lentelėje **ResRollup** visoms jūsų aplinkos įmonėms, kad paketinę užduotį pakaktų paleisti tik viename juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="a3e9c-139">Ši paketinė užduotis reikalinga visiems **Išteklių pasiekiamumo** rodiniams.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="a3e9c-140">Jei ši paketinė užduotis nevykdoma, **ResRollup** duomenys nebus sugeneruoti iš karto – tai gali užtrukti.</span><span class="sxs-lookup"><span data-stu-id="a3e9c-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>
