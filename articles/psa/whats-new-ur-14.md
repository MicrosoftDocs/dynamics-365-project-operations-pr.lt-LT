---
title: Kas nauja arba pakeista „Project Service Automation“ V3 14 atnaujintame leidime
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 14 atnaujintame leidime V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 8754f8eace50f1fa5743c5611d94f8c86693ebc9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006881"
---
# <a name="project-service-automation-update-release-14-v3"></a><span data-ttu-id="37654-103">„Project Service Automation“ V3 14 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="37654-103">Project Service Automation Update Release 14, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="37654-104">Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą.</span><span class="sxs-lookup"><span data-stu-id="37654-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="37654-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="37654-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="37654-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="37654-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="37654-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="37654-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="37654-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="37654-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="37654-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 14 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="37654-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 14.</span></span> <span data-ttu-id="37654-110">Ši versija turi naują komponavimo versijos numerį V3.10.4.21 ir ją galima gauti pagal toliau pateiktą grafiką:</span><span class="sxs-lookup"><span data-stu-id="37654-110">This version has a build number of V3.10.4.21 and is available on the following schedule:</span></span>

- <span data-ttu-id="37654-111">**Bendras prieinamumas (automatinis naujinimas):** 2020 m. sausio mėn.</span><span class="sxs-lookup"><span data-stu-id="37654-111">**General availability (self-update):** January 2020</span></span>
- <span data-ttu-id="37654-112">**Automatinis naujinimas:** 2020 m. vasario mėn.</span><span class="sxs-lookup"><span data-stu-id="37654-112">**Auto-update:** February 2020</span></span>

## <a name="update-release-14"></a><span data-ttu-id="37654-113">14 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="37654-113">Update Release 14</span></span>

### <a name="enhancements"></a><span data-ttu-id="37654-114">Patobulinimai</span><span class="sxs-lookup"><span data-stu-id="37654-114">Enhancements</span></span>

- <span data-ttu-id="37654-115">Sales</span><span class="sxs-lookup"><span data-stu-id="37654-115">Sales</span></span>

     - <span data-ttu-id="37654-116">Pasirinktinės lauko reikšmės iš **Pasiūlymo eilutės išsami informacija** kopijuojamos į **Projekto sutarties eilutės išsami informacija**, kai pasiūlymas atnaujinamas į **Uždarytas kaip laimėjęs**.</span><span class="sxs-lookup"><span data-stu-id="37654-116">Custom field values from **Quote Line Details** are copied to **Project Contract Line Details** when a quote is updated to **Closed as won**.</span></span>
     - <span data-ttu-id="37654-117">Patvirtinti projektai gali būti **Uždaryti kaip pralaimėję**.</span><span class="sxs-lookup"><span data-stu-id="37654-117">Confirmed projects can be **Closed as lost**.</span></span>

- <span data-ttu-id="37654-118">Išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="37654-118">Resource Management</span></span>

     - <span data-ttu-id="37654-119">Išplečiant rezervacijas vartotojai matys patvirtinimo dialogo langelį, kuris paragins apibendrinti rezervavimo rezultatus ir pateikti saitą į Išlaikyti rezervavimus.</span><span class="sxs-lookup"><span data-stu-id="37654-119">When extending bookings, users will be prompted with a confirmation dialog box to summarize booking results and provide a link to Maintain Bookings.</span></span>


### <a name="bug-fixes"></a><span data-ttu-id="37654-120">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="37654-120">Bug fixes</span></span>

- <span data-ttu-id="37654-121">Laikas ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="37654-121">Time and Expense</span></span>

     - <span data-ttu-id="37654-122">Pataisyta: pagerinta vartotojo patirtis, kai jis nepasirinko jokių taisytinų įrašų.</span><span class="sxs-lookup"><span data-stu-id="37654-122">Fixed: Improved the user experience when the user has not selected any entries to be corrected.</span></span>

- <span data-ttu-id="37654-123">Išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="37654-123">Resource Management</span></span>

     - <span data-ttu-id="37654-124">Sutaisyta: ištekliaus rezervavimas kelis kartus užpildo rezervuojamo ištekliaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="37654-124">Fixed: Booking a resource multiple times overflows the name of the bookable resource.</span></span>

- <span data-ttu-id="37654-125">Sales</span><span class="sxs-lookup"><span data-stu-id="37654-125">Sales</span></span>

     - <span data-ttu-id="37654-126">Sutaisyta: bendra pardavimo kaina nėra apskaičiuojama, kol vartotojas neįveda išlaidų savikainos, apskaičiuotos projektui.</span><span class="sxs-lookup"><span data-stu-id="37654-126">Fixed: The total sales price is not calculated until the user also inputs a cost price for expense estimates on a project.</span></span>
     - <span data-ttu-id="37654-127">Sutaisyta: uždaryti pasiūlymo kaip **Laimėjęs** nepavyksta, jei susijusio projekto būsena nėra **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="37654-127">Fixed: Closing a quote as **Won** fails if the associated project contract is not in a **Draft** state.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]