---
title: Kas naujo „Project Service Automation“ 16 atnaujintame leidime, V3
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 16 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: business-applications
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 3.x
ms.assetid: b890a7b6-1664-4812-8732-fed77653cc05
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 0f4c206fd5b7a36d940e966b28c2437525812a98
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753692"
---
# <a name="project-service-automation-v3-update-release-16"></a><span data-ttu-id="2c194-103">„Project Service Automation“ V3, 16 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="2c194-103">Project Service Automation V3, Update Release 16</span></span>
<span data-ttu-id="2c194-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="2c194-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2c194-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="2c194-105">This release includes some important improvements to quality, performance, and usability.</span></span>

<span data-ttu-id="2c194-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="2c194-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2c194-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="2c194-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="2c194-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas ir naujinimas](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span><span class="sxs-lookup"><span data-stu-id="2c194-108">For more information, see [Install, Update a Preferred Solution](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).</span></span> <span data-ttu-id="2c194-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 16 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="2c194-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 16.</span></span> <span data-ttu-id="2c194-110">Ši versija turi naują komponavimo versijos numerį V3.10.6.34 ir ją galima pasiekti per 2020 m. sausio mėn. automatinį naujinimą</span><span class="sxs-lookup"><span data-stu-id="2c194-110">This version has a build number of V3.10.6.34 and is generally available through a self-update in January 2020</span></span>

## <a name="update-release-16"></a><span data-ttu-id="2c194-111">16 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="2c194-111">Update Release 16</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2c194-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="2c194-112">Bug fixes</span></span>

-   <span data-ttu-id="2c194-113">Laikas ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="2c194-113">Time and Expense</span></span>

    -   <span data-ttu-id="2c194-114">Ištaisyta: vartotojai, norintys pateikti panaikintus laiko ir išlaidų įrašus patvirtinimui, dabar gaus susijusius klaidų pranešimus.</span><span class="sxs-lookup"><span data-stu-id="2c194-114">Fixed: Users attempting to submit deleted time and expense entries for approvals will now receive relevant error messages.</span></span>

-   <span data-ttu-id="2c194-115">Projektų valdymas</span><span class="sxs-lookup"><span data-stu-id="2c194-115">Project Management</span></span>

    -   <span data-ttu-id="2c194-116">Ištaisyta: į išteklių paskirstymo vienetus, apibrėžtus komandos nariams šablonuose, atsižvelgiama, kai šablonai taikomi naujam projektui.</span><span class="sxs-lookup"><span data-stu-id="2c194-116">Fixed: The resourcing units defined for team members in templates are respected with the templates are applied to a new project.</span></span>

    -   <span data-ttu-id="2c194-117">Ištaisyta: pagerintas įrašo nuosavybės pakartotinio priskyrimo tvarkymas.</span><span class="sxs-lookup"><span data-stu-id="2c194-117">Fixed: Improved handling of the re-assignment of record ownership.</span></span>

    -   <span data-ttu-id="2c194-118">Ištaisyta: projektų, kurie yra kopijuojami, nebus galima nukopijuoti, kol nebaigtas kopijavimo procesas.</span><span class="sxs-lookup"><span data-stu-id="2c194-118">Fixed: Projects that are in the process of being copied will not be permitted to copied until all copy operations are complete.</span></span>

-   <span data-ttu-id="2c194-119">Išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="2c194-119">Resource Management</span></span>

    -   <span data-ttu-id="2c194-120">Ištaisyta: naudojant funkciją „Išplėsti rezervavimus“ dabar trumpi periodai tvarkomi tinkamai ir išplėstiniuose rezervavimuose nebekuriamos nulinės valandos.</span><span class="sxs-lookup"><span data-stu-id="2c194-120">Fixed: Extend bookings now handles short durations correctly and no longer creates zero hours for extended bookings.</span></span>

    -   <span data-ttu-id="2c194-121">Ištaisyta: suderinimo rodinys dabar pateikiamas, kai projekto laiko juosta yra +5:30 GMT, o vartojo laiko juosta yra kita.</span><span class="sxs-lookup"><span data-stu-id="2c194-121">Fixed: The reconciliation view now renders when the project time zone is +5:30 GMT and the user’s time aone is different.</span></span>

-   <span data-ttu-id="2c194-122">Sales</span><span class="sxs-lookup"><span data-stu-id="2c194-122">Sales</span></span>

    -   <span data-ttu-id="2c194-123">Ištaisyta: kai projektas, susietas su sutarties eilute, buvo pašalinamas ir susiejamas naujas projektas, naujo projekto faktiniai įrašai nebuvo iš naujo įvertinti pagal apmokėjimo ir kainodaros taisykles, apibrėžtas sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="2c194-123">Fixed: When a project mapped to a contract line is removed and a new project is mapped, the actual records on the new project were not getting re-evaluated based on the billing and pricing rules defined on the contract line.</span></span> <span data-ttu-id="2c194-124">Ši klaida ištaisyta šiame leidime.</span><span class="sxs-lookup"><span data-stu-id="2c194-124">This has been fixed in this release.</span></span> <span data-ttu-id="2c194-125">Kainodaros ir faktiniai įrašai naujai susietame projekte bus anuliuoti ir iš naujo tinkamai sukurti pagal sutarties eilutės kainodaros ir apmokėjimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="2c194-125">Pricing and actual records on the newly mapped project will get reversed and re-created correctly based on the pricing and billing rules of the contract line.</span></span> <span data-ttu-id="2c194-126">Nesusieto projekto faktiniai įrašai taip pat bus iš naujo įvertinti ir dėl to perkurti.</span><span class="sxs-lookup"><span data-stu-id="2c194-126">The actual records of the un-mapped project will also get re-evaluated and re-created as a consequence.</span></span>

    -   <span data-ttu-id="2c194-127">Ištaisyta: įtrauktas papildomas tikrinimas į sąmatos eilutės lauką **Suma** siekiant užtikrinti, kad neliktų nulinių reikšmių.</span><span class="sxs-lookup"><span data-stu-id="2c194-127">Fixed: Additional validation has been added to an estimate line’s **Amount** field to ensure that null values are not persisted.</span></span>

    -   <span data-ttu-id="2c194-128">Ištaisyta: į projekto pagrindinę formą įtrauktas atnaujinimo mygtukas, kad, kai atnaujinami projekto faktiniai duomenys, vartotojas juos galėtų iš naujo sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="2c194-128">Fixed: When actuals have been updated on a project, a refresh button has been added to the project main form to allow users to re-sync the actuals.</span></span>

    -   <span data-ttu-id="2c194-129">Ištaisyta: kai vartotojai 2.X versiją atnaujina į 3X versiją, projektai su NULINE reikšme pavadinime bus leidžiami.</span><span class="sxs-lookup"><span data-stu-id="2c194-129">Fixed: When users upgrade from 2.X to 3.X, projects with a NULL value for project name will be permitted.</span></span>

