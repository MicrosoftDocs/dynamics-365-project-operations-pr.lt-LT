---
title: Kas nauja arba pakeista „Project Service Automation“ V3 32 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 32 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
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
ms.openlocfilehash: 11bf451ef4f24e2301ffde4f86a556a8a4fe30b0
ms.sourcegitcommit: 886102894244887d72e5a6213071e8d8a52c9d48
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/01/2021
ms.locfileid: "6129676"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a><span data-ttu-id="dea82-103">Kas nauja arba pakeista „Project Service Automation“ V3 32 atnaujintame leidime</span><span class="sxs-lookup"><span data-stu-id="dea82-103">What's new or changed in Project Service Automation Update Release 32, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="dea82-104">Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą.</span><span class="sxs-lookup"><span data-stu-id="dea82-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="dea82-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="dea82-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="dea82-106">Ji suderinama su „Dynamics 365 9.x“.</span><span class="sxs-lookup"><span data-stu-id="dea82-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="dea82-107">Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą.</span><span class="sxs-lookup"><span data-stu-id="dea82-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="dea82-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="dea82-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="dea82-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 32 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="dea82-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 32.</span></span> <span data-ttu-id="dea82-110">Šios versijos komponavimo numeris yra V3.10.53.108; ji visuotinai pasiekiama naudojant 2021 m. birželio mėn. savarankišką naujinimą.</span><span class="sxs-lookup"><span data-stu-id="dea82-110">This version has a build number of V3.10.53.108 and is generally available through a self-update in June 2021.</span></span>

## <a name="update-release-32"></a><span data-ttu-id="dea82-111">32 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="dea82-111">Update Release 32</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="dea82-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="dea82-112">Bug fixes</span></span>

#### <a name="general"></a><span data-ttu-id="dea82-113">Bendroji informacija</span><span class="sxs-lookup"><span data-stu-id="dea82-113">General</span></span>

- <span data-ttu-id="dea82-114">Kai nepavyksta atlikti didelio atnaujinimo, siekiant užtikrinti, kad bendrinami objektai vis dar būtų pasiekiami, turėtų būti užblokuojami tik pagrindiniai programos įvesties taškai.</span><span class="sxs-lookup"><span data-stu-id="dea82-114">When a major upgrade fails, only the main application entry points should be blocked, to ensure that shared entities are still accessible.</span></span>

#### <a name="time-and-expense"></a><span data-ttu-id="dea82-115">Laikas ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="dea82-115">Time and Expense</span></span>

<span data-ttu-id="dea82-116">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="dea82-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="dea82-117">**TimeEntriesImportFromResourceAssignment** neišlaiko išteklių priskyrimo dalies pradžios ir pabaigos laikų.</span><span class="sxs-lookup"><span data-stu-id="dea82-117">**TimeEntriesImportFromResourceAssignment** doesn't maintain the start and end times of the resource assignment contour slice.</span></span>
- <span data-ttu-id="dea82-118">Kai pasirenkate **Atidaryti įrašą** tinklelyje **Laiko įrašas**, gali būti, kad jums nebus galima pasirinkti kitų formų.</span><span class="sxs-lookup"><span data-stu-id="dea82-118">When you select **Open Entry** on the **Time Entry** grid, you might be prevented from selecting other forms.</span></span>
- <span data-ttu-id="dea82-119">Kai importuojate priskyrimus į laiko įrašus, kliento kodo užklausa gali sugeneruoti ilgą URL, kuris užklausos neįvykdo.</span><span class="sxs-lookup"><span data-stu-id="dea82-119">While you import assignments to time entries, the client code query could generate a long URL that fails the query.</span></span>
- <span data-ttu-id="dea82-120">Tinklelyje **Laiko įrašas** iš langelio panaikinus reikšmę, tinklelyje įvesties vietos neliks.</span><span class="sxs-lookup"><span data-stu-id="dea82-120">In the **Time Entry** grid, after a value is deleted from a cell, the focus doesn't remain in the grid.</span></span>
- <span data-ttu-id="dea82-121">Mygtukas **Atmesti** buvo pašalintas iš modernių patvirtinimų rodinio **Patvirtinimų apdorojimas**.</span><span class="sxs-lookup"><span data-stu-id="dea82-121">The **Reject** button has been removed from the **Processing approvals** view for modern approvals.</span></span>
- <span data-ttu-id="dea82-122">Laiko įvesties masinio patvirtinimo stabilumą ir efektyvumą paveikė aklavietė ir netinkamai apdorojami tinkinimai, susiję su objektu **Laiko įvedimo**.</span><span class="sxs-lookup"><span data-stu-id="dea82-122">The stability and performance of time entry bulk approval are affected by deadlocks and a failure to appropriately handle customizations that are related to the **Time Entry** entity.</span></span>

#### <a name="project-planning"></a><span data-ttu-id="dea82-123">Projekto planavimas</span><span class="sxs-lookup"><span data-stu-id="dea82-123">Project Planning</span></span>

- <span data-ttu-id="dea82-124">Nulinė nuorodos išimtis sugeneruojama atnaujinus projektą, kuris lauke **Sutartį sudarantis vienetas** turi nulinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dea82-124">A null reference exception is generated when you update a project that has a null value in the **Contracting Unit** field.</span></span>
- <span data-ttu-id="dea82-125">**Atnaujinti projekto sumas** neteisingai skaičiuojamos likusios projekto išlaidos ir likęs pardavimas.</span><span class="sxs-lookup"><span data-stu-id="dea82-125">**Refresh Project Totals** incorrectly calculates the remaining cost and remaining sales on a project.</span></span>
- <span data-ttu-id="dea82-126">Dėl nereikalingo kainodaros skaičiavimo paveikiamas našumas, susijęs su išteklių priskyrimo kontūrų naujinimais.</span><span class="sxs-lookup"><span data-stu-id="dea82-126">Redundant pricing calculations affect performance that is related to updates on resource assignment contours.</span></span>

#### <a name="resource-management"></a><span data-ttu-id="dea82-127">Išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="dea82-127">Resource Management</span></span>

<span data-ttu-id="dea82-128">Toliau nurodyta problema buvo išspręsta.</span><span class="sxs-lookup"><span data-stu-id="dea82-128">The following issue has been fixed:</span></span>

- <span data-ttu-id="dea82-129">Kai rezervuotino išteklių kalendoriaus pajėgumas yra didesnis nei 1, „Project Service Automation“ netinkamai atpažįsta pajėgumą kaip 0 (nulinis).</span><span class="sxs-lookup"><span data-stu-id="dea82-129">When a bookable resource's calendar capacity is more than 1, Project Service Automation incorrectly recognizes the capacity as 0 (zero).</span></span> <span data-ttu-id="dea82-130">Todėl grafiko rodinyje sukeliamas begalinis ciklas.</span><span class="sxs-lookup"><span data-stu-id="dea82-130">Therefore, an infinite loop occurs in the schedule view.</span></span>

#### <a name="sales"></a><span data-ttu-id="dea82-131">Pardavimas</span><span class="sxs-lookup"><span data-stu-id="dea82-131">Sales</span></span>

<span data-ttu-id="dea82-132">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="dea82-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="dea82-133">Kai sukuriama žurnalo eilutė, kurios operacijos tipas yra pasirinktinis, įvyksta tokia nulinės nuorodos išimtis: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span><span class="sxs-lookup"><span data-stu-id="dea82-133">When a journal line is created that has a custom transaction type, the following null reference exception occurs: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.</span></span>
- <span data-ttu-id="dea82-134">Prieš kopijuodami pasiūlymą į apmokestinamus naujai nukopijuoto pasiūlymo vaidmenis ir kategorijas negalima įtraukti išjungtų vaidmenų ir kategorijų.</span><span class="sxs-lookup"><span data-stu-id="dea82-134">Roles and categories that are inactivated before a quotation is copied should not be added to chargeable roles and categories of the newly copied quotation.</span></span>
- <span data-ttu-id="dea82-135">Dokumento data ir apskaitos data nesulygiuojamos su pradžios data, pateikiama sąskaitos faktūros eilutės išsamioje informacijoje, kuri sukuriama tiesiogiai juodraščio sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="dea82-135">The document date and accounting date aren't aligned with the start date that is provided on an invoice line detail that is created directly on a draft invoice.</span></span>
- <span data-ttu-id="dea82-136">Nulinės nuorodos išimtys generuojamos scenarijuose, susijusiuose su vaidmenų ir kategorijų išjungimu prieš kopijuojant pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="dea82-136">Null reference exceptions are generated in scenarios that are related to inactivation of roles and categories before a quotation is copied.</span></span>
- <span data-ttu-id="dea82-137">Puslapyje **Projektai** veiksmas **Atnaujinti kainas** nenaujina išlaidų įvertinimų ir medžiagų įvertinimų.</span><span class="sxs-lookup"><span data-stu-id="dea82-137">The **Update Prices** action on the **Projects** page doesn't update expense estimates and material estimates.</span></span>
