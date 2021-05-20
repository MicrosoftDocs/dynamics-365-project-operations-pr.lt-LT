---
title: Kas nauja arba pakeista „Project Service Automation“ V3 19 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 19 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949149"
---
# <a name="project-service-automation-update-release-19-v3"></a><span data-ttu-id="663f3-103">„Project Service Automation“ V3 19 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="663f3-103">Project Service Automation Update Release 19, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="663f3-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="663f3-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="663f3-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="663f3-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="663f3-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="663f3-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="663f3-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="663f3-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="663f3-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="663f3-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="663f3-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 19 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="663f3-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 19.</span></span> <span data-ttu-id="663f3-110">Šios versijos komponavimo versijos numeris yra V3.10.30.41 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="663f3-110">This version has a build number of V3.10.30.41 and is generally available through a self-update in May 2020.</span></span>

## <a name="update-release-19"></a><span data-ttu-id="663f3-111">19 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="663f3-111">Update Release 19</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="663f3-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="663f3-112">Bug fixes</span></span>

<span data-ttu-id="663f3-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="663f3-113">**Time and Expense**</span></span>

<span data-ttu-id="663f3-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="663f3-114">The following issues have been fixed:</span></span> 

- <span data-ttu-id="663f3-115">Klaidos, gaunamos importuojant laiko įrašus, rodomos netinkamai.</span><span class="sxs-lookup"><span data-stu-id="663f3-115">Errors derived from time entry imports are not surfaced correctly.</span></span>
- <span data-ttu-id="663f3-116">Laiko įrašo tinklelis nepalaiko lauko veikimo **Tik data**.</span><span class="sxs-lookup"><span data-stu-id="663f3-116">Time Entry Grid does not support **Date Only** field behavior.</span></span>
- <span data-ttu-id="663f3-117">Projekto ištekliai negali sukurti išlaidų su projektu.</span><span class="sxs-lookup"><span data-stu-id="663f3-117">Project Resources are unable to create an expense with a project.</span></span>

<span data-ttu-id="663f3-118">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="663f3-118">**Project Management**</span></span>

<span data-ttu-id="663f3-119">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="663f3-119">The following issues have been fixed:</span></span> 

-  <span data-ttu-id="663f3-120">Dėl tretinės užduoties pastangų įvertinimo pabaigoje (EAC) skaičiavimai yra klaidingi.</span><span class="sxs-lookup"><span data-stu-id="663f3-120">Grandchild task causes an incorrect effort estimate during the Completion (EAC) Calculation.</span></span>

<span data-ttu-id="663f3-121">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="663f3-121">**Sales**</span></span>

<span data-ttu-id="663f3-122">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="663f3-122">The following issues have been fixed:</span></span> 

- <span data-ttu-id="663f3-123">Veiksmas **Perskaičiuoti** neveikia su išlaidų sutarties eilutės išsamia informacija arba pasiūlymo eilutės išsamia informacija.</span><span class="sxs-lookup"><span data-stu-id="663f3-123">The **Recalculate** action does not work with expense contract line details or quote line details.</span></span>
- <span data-ttu-id="663f3-124">Išlaidų įvertinimuose trūksta parinkties **Naujinti kainas**.</span><span class="sxs-lookup"><span data-stu-id="663f3-124">**Update Prices** is missing for expense estimates.</span></span>
-  <span data-ttu-id="663f3-125">Klientai negali pasirinkti pasirinktinių sutarties būsenos tipų puslapyje **Projekto sutartis**.</span><span class="sxs-lookup"><span data-stu-id="663f3-125">Customers are unable to select custom contract status reasons from the **Project Contract** page.</span></span>
- <span data-ttu-id="663f3-126">Klientai kurdami pasirinktinį kainoraštį pagal pasiūlymą susiduria su suprastėjusiu veikimu.</span><span class="sxs-lookup"><span data-stu-id="663f3-126">Customers experience degraded performance when creating a custom price list from a quote.</span></span>
- <span data-ttu-id="663f3-127">Klientai susiduria su **vienetų** numatytųjų reikšmių nenuoseklumu puslapiuose **Pasiūlymo eilutės išsami informacija** ir **Sutarties eilutės išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="663f3-127">Customers experience inconsistency with **unit** defaults on **Quote Line Details** and **Contract Line Details** pages.</span></span>
- <span data-ttu-id="663f3-128">Į apmokestinamą sutarties eilutę įtraukus neapmokestinamų operacijų kategorijos elementus, nebus paisomas operacijos kategorijos atsiskaitymo tipas **Neapmokestinama**.</span><span class="sxs-lookup"><span data-stu-id="663f3-128">Adding non-chargeable transaction category items to a chargeable contract line will not respect the **Non-chargeable** billing type of the transaction category.</span></span>
- <span data-ttu-id="663f3-129">Klientai negali naudoti naujai įtrauktų vaidmenų ir kategorijos anksčiau sudarytoms sutartims.</span><span class="sxs-lookup"><span data-stu-id="663f3-129">Customers can't use the newly added roles and category on previously created contracts.</span></span>
- <span data-ttu-id="663f3-130">Klientai susiduria su suprastėjusiu veikimu, kai šaltinio kode „PreValidateProjectTeamMemberUpdate.cs” vykdomas nereikalingas grąžinimas</span><span class="sxs-lookup"><span data-stu-id="663f3-130">Customers experience degraded performance Unnecessary retrieve in PreValidateProjectTeamMemberUpdate.cs</span></span>
- <span data-ttu-id="663f3-131">Vaidmenys, nustatyti kaip neapmokestinami sąraše **Išteklių kategorijos**, projekto sutarties eilutėje turėtų būti įtraukti į skirtuką **Apmokestinami vaidmenys** kaip **Neapmokestinami**.</span><span class="sxs-lookup"><span data-stu-id="663f3-131">Roles set up as non-chargeable in the **Resource Categories** list should be added to the **Chargeable Roles** tab as **Non0chargeable** on the contract line for a project.</span></span>
- <span data-ttu-id="663f3-132">Kurdami projektą klientai gali susiduria su prastesniu veikimu, nes **GetBookableResourceIdFromUser** grąžina visus rezervuojamų išteklių stulpelius, o ne tik pirminį ID.</span><span class="sxs-lookup"><span data-stu-id="663f3-132">Customers may experience degraded performance when creating a project because **GetBookableResourceIdFromUser** retrieves all columns of bookable resources instead of just the primary ID.</span></span>
- <span data-ttu-id="663f3-133">Objektas **TransactionType** neturi išankstinio tikrinimo naujinimo priedo, kad vartotojai negalėtų įvesti **vienetų** ir **UnitGroups**, netinkančių operacijos tipams.</span><span class="sxs-lookup"><span data-stu-id="663f3-133">**TransactionType** entity missing the pre-validation update plug-in to prevent users from entering **Units** and **UnitGroups** that are not valid for transaction types.</span></span>
- <span data-ttu-id="663f3-134">Veiksmas **Šalinti** neveikia importuojant laiko įrašą.</span><span class="sxs-lookup"><span data-stu-id="663f3-134">The **Remove** step does not work for time entry import.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]