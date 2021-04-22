---
title: Kas nauja arba pakeista „Project Service Automation“ V3 25 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 25 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: 30822ec64b31e110202a587dd941bdff60116712
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280453"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a><span data-ttu-id="14919-103">Kas nauja arba pakeista „Project Service Automation“ V3 25 atnaujintame leidime</span><span class="sxs-lookup"><span data-stu-id="14919-103">What's new or changed in Project Service Automation Update Release 25, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="14919-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="14919-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="14919-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="14919-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="14919-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="14919-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="14919-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="14919-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="14919-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="14919-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="14919-109">Šioje temoje išvardytos naujos ar pakeistos „Project Service Automation“ V3, atnaujinto 25 leidimo funkcijos ir taisymai. Šios komponavimo versijos numeris yra V 3.10.43.76 ir ji yra visuotinai pasiekiama 2020 m. spalio mėn. savaiminiame naujinime.</span><span class="sxs-lookup"><span data-stu-id="14919-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 25 This version has a build number of V 3.10.43.76 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-25"></a><span data-ttu-id="14919-110">25 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="14919-110">Update Release 25</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="14919-111">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="14919-111">Bug fixes</span></span>

<span data-ttu-id="14919-112">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="14919-112">**Time and Expense**</span></span>

<span data-ttu-id="14919-113">Toliau nurodyta problema buvo išspręsta.</span><span class="sxs-lookup"><span data-stu-id="14919-113">The following issue has been fixed:</span></span>

- <span data-ttu-id="14919-114">Laiko įrašo diagrama, kurioje rodomi papildomi duomenys, pagrįsti per dideliu nuskaitomu intervalu.</span><span class="sxs-lookup"><span data-stu-id="14919-114">Time entry chart showing additional data based on too large of an interval being retrieved.</span></span>

<span data-ttu-id="14919-115">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="14919-115">**Resource Management**</span></span>

<span data-ttu-id="14919-116">Toliau nurodyta problema buvo išspręsta.</span><span class="sxs-lookup"><span data-stu-id="14919-116">The following issue has been fixed:</span></span>

- <span data-ttu-id="14919-117">Pridėtas „Package Deployer” kodas, skirtas praleisti „Universal Resource Scheduling” pataisos importavimą, jei jau yra naujesnės versijos pataisa.</span><span class="sxs-lookup"><span data-stu-id="14919-117">Added package deployer code to skip the Universal Resource Scheduling patch import if a higher version patch already exists.</span></span>

<span data-ttu-id="14919-118">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="14919-118">**Project Management**</span></span>

<span data-ttu-id="14919-119">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="14919-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="14919-120">Ištaisyti apvalinimo ir valiutos kurso nesutapimai, lemiantys netinkamą planuojamą savikainą projekto sekimo tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="14919-120">Corrected rounding and exchange rate discrepancies resulting in incorrect planned cost in the project tracking grid.</span></span>
- <span data-ttu-id="14919-121">Palaikoma galimybė rodyti du ar daugiau reagavimo tinklelių formoje **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="14919-121">Support the ability to display two or more react grids on the **Project** form.</span></span>
- <span data-ttu-id="14919-122">Teikiamas tikrinimas, skirtas galimybei priskirti užduotį praėjus kalendoriaus pabaigos datai, dėl ko nepavykdavo priskirti išteklių.</span><span class="sxs-lookup"><span data-stu-id="14919-122">Provided validation to address the ability to assign a task past the calendar end date, which results in a failed resource assignment.</span></span>
- <span data-ttu-id="14919-123">Patobulintas klaidų tvarkymas sprendžiant klaidą „Null Reference Exception” generuojamą iš:</span><span class="sxs-lookup"><span data-stu-id="14919-123">Improved error handling to address Null Reference Exception generated from the following:</span></span>

    - <span data-ttu-id="14919-124">**PreValidateProjectTeamMemberCreate** priedo</span><span class="sxs-lookup"><span data-stu-id="14919-124">**PreValidateProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="14919-125">**PreValidateProjectTaskCreate**, kai projekto užduotis sukuriama nenaudojant susijusio projekto</span><span class="sxs-lookup"><span data-stu-id="14919-125">**PreValidateProjectTaskCreate** when a project task is created without an associated project</span></span>
    - <span data-ttu-id="14919-126">**PreProjectTeamMemberCreate** priedo</span><span class="sxs-lookup"><span data-stu-id="14919-126">**PreProjectTeamMemberCreate** plug-in</span></span>
    - <span data-ttu-id="14919-127">**PostProjectTeamMemberDelete** priedo</span><span class="sxs-lookup"><span data-stu-id="14919-127">**PostProjectTeamMemberDelete** plug-in</span></span>
    - <span data-ttu-id="14919-128">**PreValidateProjectTaskDelete** priedo</span><span class="sxs-lookup"><span data-stu-id="14919-128">**PreValidateProjectTaskDelete** plug-in</span></span>

<span data-ttu-id="14919-129">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="14919-129">**Sales**</span></span>

<span data-ttu-id="14919-130">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="14919-130">The following issues have been fixed:</span></span>

- <span data-ttu-id="14919-131">Patobulintas klaidų tvarkymas, sprendžiant klaidą „Null Reference Exceptions”, generuojamą iš **Projekto kopijavimas: įvertinamas HelperResource valdymas**.</span><span class="sxs-lookup"><span data-stu-id="14919-131">Improved error handling to address Null Reference Exceptions generated from **Copy Project: Estimates HelperResource Management**.</span></span>
- <span data-ttu-id="14919-132">Laukas **Neparengta išrašyti sąskaitos faktūros** dalyje **Laiko ir medžiagų atsiskaitymo nebaigtos užduotys** neišvalo atsiskaitymo būsenos.</span><span class="sxs-lookup"><span data-stu-id="14919-132">**Not ready to Invoice** on a **Time and Material Billing Backlog** doesn't clear the billing status.</span></span>
- <span data-ttu-id="14919-133">Ištaisytas netinkamai pažymėtas mygtukas **Kainos** skirtukuose **Vaidmens kaina** ir **Katalogo elementai**.</span><span class="sxs-lookup"><span data-stu-id="14919-133">Corrected mislabeled **Prices** buttons on the **Role Price** and **Catalog Items** tab.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]