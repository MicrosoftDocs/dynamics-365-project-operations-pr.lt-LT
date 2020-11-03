---
title: Kas nauja arba pakeista „Project Service Automation“ V3 15 atnaujintame leidime
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 15 atnaujintame leidime V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/27/2020
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
ms.openlocfilehash: 6112e4874025e528a2bb583cf215fd9eff681534
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080793"
---
# <a name="project-service-automation-update-release-15-v3"></a><span data-ttu-id="b4786-103">„Project Service Automation“ V3 15 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="b4786-103">Project Service Automation Update Release 15, V3</span></span>

<span data-ttu-id="b4786-104">Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą.</span><span class="sxs-lookup"><span data-stu-id="b4786-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="b4786-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="b4786-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="b4786-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="b4786-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="b4786-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="b4786-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="b4786-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="b4786-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="b4786-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 15 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="b4786-109">This topic lists the features and fixes that are new or changed for PSA V3, Update Release 15.</span></span> <span data-ttu-id="b4786-110">Ši versija turi naują komponavimo versijos numerį V3.10.5.28 ir ją galima pasiekti per 2020 m. sausio mėn. automatinį naujinimą.</span><span class="sxs-lookup"><span data-stu-id="b4786-110">This version has a build number of V3.10.5.28 and is generally available through a self-update in January 2020.</span></span>

## <a name="update-release-15"></a><span data-ttu-id="b4786-111">15 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="b4786-111">Update Release 15</span></span> 

### <a name="enhancements"></a><span data-ttu-id="b4786-112">Patobulinimai</span><span class="sxs-lookup"><span data-stu-id="b4786-112">Enhancements</span></span>

- <span data-ttu-id="b4786-113">Projektų valdymas</span><span class="sxs-lookup"><span data-stu-id="b4786-113">Project Management</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="b4786-114">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="b4786-114">Bug fixes</span></span>

- <span data-ttu-id="b4786-115">Laikas ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="b4786-115">Time and Expense</span></span>

  - <span data-ttu-id="b4786-116">Sutaisyta: pridėtas įkėlimo klaidos tvarkymas suderinimo rodinyje.</span><span class="sxs-lookup"><span data-stu-id="b4786-116">Fixed: Add on-load error handling in the reconciliation view.</span></span>
  - <span data-ttu-id="b4786-117">Sutaisyta: projekto išteklių priegloba: pervadinta **Suma** , siekiant sumažinti neaiškumą.</span><span class="sxs-lookup"><span data-stu-id="b4786-117">Fixed: Project Resource Hub: Rename **Amount** to reduce ambiguity.</span></span>
  - <span data-ttu-id="b4786-118">Sutaisyta: pakoreguotas rodinys **Kopijuoti laiko įrašo stulpelius** , kad būtų įtrauktas tipas.</span><span class="sxs-lookup"><span data-stu-id="b4786-118">Fixed: Adjust the view **Copy Time Entry Columns** to include the type.</span></span>
  - <span data-ttu-id="b4786-119">Sutaisyta: laiko įrašo trukmės redagavimas tinklelio rodinyje naudojant dešimtainius skaičius sukelia kai kurių skaičių nežinomas klaidas.</span><span class="sxs-lookup"><span data-stu-id="b4786-119">Fixed: Editing time entry duration in the grid view using decimal numbers results in unknown error for some numbers.</span></span>

- <span data-ttu-id="b4786-120">Projektų valdymas</span><span class="sxs-lookup"><span data-stu-id="b4786-120">Project Management</span></span>

  - <span data-ttu-id="b4786-121">Sutaisyta: išskleidžiamasis **Naudoti sekimo rodinyje** dabar išplečiamas pagal parinkčių plotį.</span><span class="sxs-lookup"><span data-stu-id="b4786-121">Fixed: The drop-down menu for **Use in Tracking View** now expands based on the width of the options.</span></span>
  - <span data-ttu-id="b4786-122">Sutaisyta: tvarkant projektus +13 laiko juostose, užduočių skaičiavimuose gali būti netikslių rezultatų.</span><span class="sxs-lookup"><span data-stu-id="b4786-122">Fixed: When managing projects in the +13 time zone, tasks calculations can display inaccurate results.</span></span>
  - <span data-ttu-id="b4786-123">Sutaisyta: **Komandos nario pabaigos laikas** pakoreguotas naudojant 24 val. kalendorių.</span><span class="sxs-lookup"><span data-stu-id="b4786-123">Fixed: **Team Member End Time** has been corrected when using a 24-hour calendar.</span></span>
  - <span data-ttu-id="b4786-124">Sutaisyta: iš naujo suaktyvintas **BPF** **msdyn_project** pagrindinėje formoje.</span><span class="sxs-lookup"><span data-stu-id="b4786-124">Fixed: Re-activated the **BPF** in **msdyn_project** main form.</span></span>
  - <span data-ttu-id="b4786-125">Sutaisyta: skaičiuojant priskyrimus daugiau neignoruojama viena diena.</span><span class="sxs-lookup"><span data-stu-id="b4786-125">Fixed: Assignments calculation no longer ignores one day.</span></span>
  - <span data-ttu-id="b4786-126">Sutaisyta: nauja pranešimų juosta pridėta prie projekto formos, kai laiko zona skiriasi nuo vartotojo ir projekto.</span><span class="sxs-lookup"><span data-stu-id="b4786-126">Fixed: A new notification banner has been added to the project form when the time zone differs between user and project.</span></span>

- <span data-ttu-id="b4786-127">Sales</span><span class="sxs-lookup"><span data-stu-id="b4786-127">Sales</span></span>

  - <span data-ttu-id="b4786-128">Sutaisyta: išlaidų skaičiavimo kategorijos apžvalgą galima naudoti norint filtruoti dublikatus.</span><span class="sxs-lookup"><span data-stu-id="b4786-128">Fixed: Expense estimate category lookup can be used to filter duplicates.</span></span>
  - <span data-ttu-id="b4786-129">Sutaisyta: kode **PluginDomain.ExecuteInTryCatchBlock(..)** daugiau neslepiama išimties kilmė.</span><span class="sxs-lookup"><span data-stu-id="b4786-129">Fixed: Code in **PluginDomain.ExecuteInTryCatchBlock(..)** no longer hides the origin of the exception.</span></span>
  - <span data-ttu-id="b4786-130">Sutaisyta: daugiau negaunamas klaidos pranešimas **Projekto apžvalgos** **Pasiūlymo eilutės** formoje, kai yra daugiau nei 1000 projektų.</span><span class="sxs-lookup"><span data-stu-id="b4786-130">Fixed: No longer get an error message in **Project lookup** in the **Quote Line** form when there are more than 1000 projects.</span></span>
  - <span data-ttu-id="b4786-131">Sutaisyta: **Skaičiavimų** tinklelyje, skirtame darbo įverčiams ir išlaidų sąmatoms, dabar rodomas teisingas valiutos simbolis.</span><span class="sxs-lookup"><span data-stu-id="b4786-131">Fixed: **Estimates** grid for labor estimates and expense estimates now displays the correct currency symbol.</span></span>
  - <span data-ttu-id="b4786-132">Sutaisyta: kai organizacija atnaujina PSA iš 14 atnaujinto leidimo į 15 atnaujintą leidimą, skirtukas **Grafikas** formoje **Projektas** daugiau nerodomas kaip tuščias.</span><span class="sxs-lookup"><span data-stu-id="b4786-132">Fixed: After an organization updates PSA from Update Release 14 to Update Release 15, the **Schedule** tab no longer appears as blank on the **Project** form.</span></span>
