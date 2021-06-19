---
title: Projekto išteklių planavimo efektyvumas
description: Šioje temoje pateikta informacija apie tai, kaip padidinti daugelio projektų išteklių planavimo efektyvumą.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 113023909f88cb4dd498190ef21b6955482b25dd
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010031"
---
# <a name="project-resource-scheduling-performance"></a><span data-ttu-id="04c2a-103">Projekto išteklių planavimo efektyvumas</span><span class="sxs-lookup"><span data-stu-id="04c2a-103">Project resource scheduling performance</span></span>

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


<span data-ttu-id="04c2a-104">Kai projektų skaičius pasiekia tūkstančius, gali atsirasti su išteklių planavimu susijusių efektyvumo problemų.</span><span class="sxs-lookup"><span data-stu-id="04c2a-104">Performance issues related to resource scheduling can occur when the number of projects reaches into the thousands.</span></span> <span data-ttu-id="04c2a-105">Norint padidinti išteklių planavimo efektyvumą yra funkcija, leidžianti naudotojams sutrumpinti laiką, kurio reikia norint paleisti išteklių pasiekiamumo formą.</span><span class="sxs-lookup"><span data-stu-id="04c2a-105">To improve resource scheduling performance, a feature is available that allows users to reduce the time that it takes to launch the resource availability form.</span></span> <span data-ttu-id="04c2a-106">Tiksliau kalbant, taip pašalinamas išteklių pajėgumo sumavimo sinchronizavimo procesas ir naudojama lentelė **ResProjectResource**, kad paspartėtų išteklių peržvalga.</span><span class="sxs-lookup"><span data-stu-id="04c2a-106">Specifically, this removes the resource capacity roll-up synchronization process and uses the **ResProjectResource** table to speed up the resource lookup.</span></span> <span data-ttu-id="04c2a-107">Atkreipkite dėmesį, kad lentelė **ResRollup** nebebus naudojama.</span><span class="sxs-lookup"><span data-stu-id="04c2a-107">Note that the **ResRollup** table will no longer be used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="04c2a-108">Jei yra priklausomybė nuo išteklių pajėgumų sumavimo sinchronizavimo proceso arba lentelės **ResProjectResource**, šios funkcijos nenaudokite.</span><span class="sxs-lookup"><span data-stu-id="04c2a-108">If there is a dependency on either the resource capacity roll-up synchronization process or the **ResProjectResource** table, do not use this feature.</span></span>

## <a name="enable-resource-scheduling-performance-enhancement"></a><span data-ttu-id="04c2a-109">Išteklių planavimo efektyvumo didinimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="04c2a-109">Enable resource scheduling performance enhancement</span></span>
<span data-ttu-id="04c2a-110">Norėdami įjungti išteklių planavimo efektyvumo didinimą atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="04c2a-110">To enable resource scheduling performance enhancement, complete the following steps.</span></span>

1. <span data-ttu-id="04c2a-111">Eikite į **Funkcijų valdymas** > **Visi** ir funkcijų sąraše raskite **Įjungti projektų išteklių planavimo efektyvumo didinimo funkciją**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-111">Go to **Feature management** > **All**, and in the feature list, locate **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="04c2a-112">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-112">Select **Enable now**.</span></span>

> [!NOTE]
> <span data-ttu-id="04c2a-113">Jei funkcijos nerandate sąraše, pasirinkite **Tikrinti, ar yra naujinimų** norėdami sąrašą atnaujinti.</span><span class="sxs-lookup"><span data-stu-id="04c2a-113">If you can't find the feature in the list, select **Check for updates** to refresh the list.</span></span>

3. <span data-ttu-id="04c2a-114">Atnaujinkite naršyklę, tada eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projektų ištekliai** > **Sinchronizuoti išteklių kalendorių pajėgumą visose įmonėse**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-114">Refresh your browser, and then go to **Project management and accounting** > **Periodic** > **Project resources** > **Synchronize resource calendars capacity across all companies**.</span></span>
4. <span data-ttu-id="04c2a-115">Nustatykite **Pašalinti esamus pajėgumų įrašus** į **Taip** norėdami pašalinti ankstesnius duomenis.</span><span class="sxs-lookup"><span data-stu-id="04c2a-115">Set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="04c2a-116">Jei norite generuoti papildančiuosius duomenis, nustatykite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-116">If you want generate incremental data, set it to **No**.</span></span>
5. <span data-ttu-id="04c2a-117">Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio duomenys turėtų būti generuojami.</span><span class="sxs-lookup"><span data-stu-id="04c2a-117">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="04c2a-118">Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datos nebūtina apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="04c2a-118">If you select a period code, a start and end date do not need to be defined.</span></span>
6. <span data-ttu-id="04c2a-119">Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="04c2a-119">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
7. <span data-ttu-id="04c2a-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-120">Select **OK**.</span></span>

 > [!NOTE]
 > <span data-ttu-id="04c2a-121">Tada bendri duomenys bus paskirstyti lentelėje **ResCalendarCapacity** visoms jūsų aplinkos įmonėms, kad paketinę užduotį pakaktų paleisti tik viename juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="04c2a-121">This will distribute general data to the **ResCalendarCapacity** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="04c2a-122">Šios paketinės užduoties duomenys yra reikalingi norint apskaičiuoti išteklių pajėgumą susietame kalendoriuje.</span><span class="sxs-lookup"><span data-stu-id="04c2a-122">The data in this batch job is needed to calculate resource capacity through the associated calendar.</span></span>

8. <span data-ttu-id="04c2a-123">Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projektų ištekliai** > **Užpildyti projektų išteklius visose įmonėse** ir pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-123">Go to **Project management and accounting** > **Periodic** > **Project resources** > **Populate project resources across all companies** and then select **OK**.</span></span> <span data-ttu-id="04c2a-124">Tai bendrų duomenų atnaujinimo scenarijus lentelėse **ResProjectResource**, **ResCalendarDateTimeRange** ir **ResEffectiveDateTimeRange**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-124">This is the data upgrade script for general data in the **ResProjectResource**, **ResCalendarDateTimeRange**, and **ResEffectiveDateTimeRange** tables.</span></span> <span data-ttu-id="04c2a-125">Lauko **PSAPRojSchedRole.RootActivity** reikšmės taip pat atnaujinamos.</span><span class="sxs-lookup"><span data-stu-id="04c2a-125">Values for the **PSAPRojSchedRole.RootActivity** field are also updated.</span></span> <span data-ttu-id="04c2a-126">Jei tai nevykdoma, gausite įspėjimą, kai bandysite vykdyti išteklių planavimo operacijas.</span><span class="sxs-lookup"><span data-stu-id="04c2a-126">If this is not run, you will receive a warning when you try to execute resource scheduling operations.</span></span>
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a><span data-ttu-id="04c2a-127">Išteklių planavimo efektyvumo didinimo išjungimas</span><span class="sxs-lookup"><span data-stu-id="04c2a-127">Turn off resource scheduling performance enhancement</span></span>

1. <span data-ttu-id="04c2a-128">Eikite į **Funkcijų valdymas** > **Visi** ir raskite **Įjungti projektų išteklių planavimo efektyvumo didinimo funkciją**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-128">Go to **Feature management** > **All**  and search for **Enable project resource scheduling performance enhancement feature**.</span></span>
2. <span data-ttu-id="04c2a-129">Pasirinkite funkciją ir mygtuką **Išjungti**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-129">Select the feature, and then select the **Disable** button.</span></span>
3. <span data-ttu-id="04c2a-130">Atnaujinkite naršyklę.</span><span class="sxs-lookup"><span data-stu-id="04c2a-130">Refresh your browser.</span></span>
4. <span data-ttu-id="04c2a-131">Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Pajėgumų sinchronizavimas** > **Sinchronizuoti išteklių pajėgumų sumavimą**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-131">Go to **Project management and accounting** > **Periodic** > **Capacity synchronization** > **Synchronize resource capacity roll-ups**.</span></span>
5. <span data-ttu-id="04c2a-132">Puslapyje **Pajėgumų sumavimo sinchronizavimas** nustatykite **Šalinti esamus pajėgumų įrašus** į **Taip** norėdami pašalinti ankstesnius duomenis.</span><span class="sxs-lookup"><span data-stu-id="04c2a-132">On the **Capacity roll-up synchronization** page, set **Remove existing capacity records** to **Yes** to remove previous data.</span></span> <span data-ttu-id="04c2a-133">Jei norite generuoti papildančiuosius duomenis, nustatykite **Ne**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-133">If you want to generate incremental data, set it to **No**.</span></span>
6. <span data-ttu-id="04c2a-134">Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio duomenys turėtų būti generuojami.</span><span class="sxs-lookup"><span data-stu-id="04c2a-134">In the **Period code** field, select the period in which data should be generated.</span></span> <span data-ttu-id="04c2a-135">Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datos nebūtina apibrėžti.</span><span class="sxs-lookup"><span data-stu-id="04c2a-135">If you select a period code, a start and end date do not need to be defined.</span></span>
7. <span data-ttu-id="04c2a-136">Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="04c2a-136">If you leave the **Period code** field blank, select specific start and end dates to generate data.</span></span>
8. <span data-ttu-id="04c2a-137">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="04c2a-137">Select **OK**.</span></span>

> [!NOTE]
> <span data-ttu-id="04c2a-138">Tada bendri duomenys bus paskirstyti lentelėje **ResRollup** visoms jūsų aplinkos įmonėms, kad paketinę užduotį pakaktų paleisti tik viename juridiniame subjekte.</span><span class="sxs-lookup"><span data-stu-id="04c2a-138">This will distribute general data to the **ResRollup** table across all companies in your environment, so the batch job only needs to be run in one legal entity.</span></span> <span data-ttu-id="04c2a-139">Ši paketinė užduotis reikalinga visiems **Išteklių pasiekiamumo** rodiniams.</span><span class="sxs-lookup"><span data-stu-id="04c2a-139">This batch job is needed for all **Resource Availability** views.</span></span> <span data-ttu-id="04c2a-140">Jei ši paketinė užduotis nevykdoma, **ResRollup** duomenys nebus sugeneruoti iš karto – tai gali užtrukti.</span><span class="sxs-lookup"><span data-stu-id="04c2a-140">If this batch job is not run, the **ResRollup** data will be generated on the fly, which can take time.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]