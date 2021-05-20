---
title: Kas nauja arba pakeista „Project Service Automation“ V3 22 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 22 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 07/28/2020
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
ms.openlocfilehash: 8863d321ad88d761d0fcbd82ca26562a69468f2f
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949014"
---
# <a name="project-service-automation-update-release-22-v3"></a><span data-ttu-id="47a67-103">„Project Service Automation“ V3 22 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="47a67-103">Project Service Automation Update Release 22, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="47a67-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="47a67-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="47a67-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="47a67-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="47a67-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="47a67-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="47a67-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="47a67-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="47a67-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="47a67-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="47a67-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 22 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="47a67-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 22.</span></span> <span data-ttu-id="47a67-110">Šios versijos komponavimo versijos numeris yra V 3.10.33.48 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. birželio mėn.</span><span class="sxs-lookup"><span data-stu-id="47a67-110">This version has a build number of V 3.10.33.48 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-22"></a><span data-ttu-id="47a67-111">22 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="47a67-111">Update Release 22</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="47a67-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="47a67-112">Bug fixes</span></span>



<span data-ttu-id="47a67-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="47a67-113">**Time and Expense**</span></span>

<span data-ttu-id="47a67-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="47a67-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="47a67-115">**Laiko įrašai** po importavimo nėra automatiškai įtraukiami į laiko įrašų grafiką.</span><span class="sxs-lookup"><span data-stu-id="47a67-115">**Time entries** are not automatically added in the Time entries schedule after import.</span></span>
- <span data-ttu-id="47a67-116">**Laiko įrašo** tinklelio datos parinkiklis neatpažįsta vartotojo regioninių parametrų.</span><span class="sxs-lookup"><span data-stu-id="47a67-116">The **Time Entry** grid date picker does not recognize a user's regional settings.</span></span>

<span data-ttu-id="47a67-117">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="47a67-117">**Resource Management**</span></span>

<span data-ttu-id="47a67-118">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="47a67-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="47a67-119">Veikiant rankiniam režimui, pakeitimai į **Išteklių priskyrimo** kontūrus nepripažįstami, kai generuojami **Išteklių reikalavimai**.</span><span class="sxs-lookup"><span data-stu-id="47a67-119">In manual mode, changes to **Resource Assignment** contours are not recognized when generating **Resource Requirements**.</span></span>
- <span data-ttu-id="47a67-120">**Išteklių užklausos** nepalaiko pasirinktinių užklausų būsenų.</span><span class="sxs-lookup"><span data-stu-id="47a67-120">**Resource Requests** do not support custom request statuses.</span></span>

<span data-ttu-id="47a67-121">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="47a67-121">**Project Management**</span></span>

<span data-ttu-id="47a67-122">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="47a67-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="47a67-123">Du kartus spustelėjus „EstimateGridControl“, olandiško formato skaičiai nebus tinkamai išanalizuoti.</span><span class="sxs-lookup"><span data-stu-id="47a67-123">Using double-click on EstimateGridControl will not correctly parse Dutch format numbers.</span></span>
- <span data-ttu-id="47a67-124">Priskirtos valandos nėra tinkamai atnaujinamos, kai priskyrimai pakeičiami naudojant „Microsoft Project“ stalinio kompiuterio papildinį.</span><span class="sxs-lookup"><span data-stu-id="47a67-124">Assigned hours do not update correctly when assignments are changed using the Microsoft Project desktop client add-in.</span></span>
- <span data-ttu-id="47a67-125">Projektų stebėjimo ir įvertinimo tinkleliuose rodomas neteisingas pardavimo valiutos kodas, kai sutarties valiuta skiriasi nuo kliento valiutos ir organizacija sukonfigūruota taip, kad būtų rodomi valiutos kodai, o ne valiutos simboliai.</span><span class="sxs-lookup"><span data-stu-id="47a67-125">Project Tracking and Estimates grids display incorrect sales currency code when contract currency is different than customer currency and organization is configured to display currency codes instead of currency symbols.</span></span>
- <span data-ttu-id="47a67-126">Prie komandos nario pabaigos datos bus pridėta viena diena, jei darbo valandų grafikas yra 24 valandos per dieną.</span><span class="sxs-lookup"><span data-stu-id="47a67-126">A Team member's finish date will add one day if the work hour schedule is 24-hours per day.</span></span>
- <span data-ttu-id="47a67-127">Projekto grafike įtraukus operacijų kategoriją į užduotį, automatinis įrašymas nėra aktyvuojamas.</span><span class="sxs-lookup"><span data-stu-id="47a67-127">On the Project Schedule, adding a Transaction Category to a task does not trigger auto save.</span></span>
- <span data-ttu-id="47a67-128">Į projekto šabloną įtraukiant komandos narį, parodoma ši klaida: „Išteklių reikalavimų negalima susieti su projekto šablonais“.</span><span class="sxs-lookup"><span data-stu-id="47a67-128">The following error is displayed when adding a team member to the Project Template: "Resource requirements cannot be associated with project templates".</span></span> 
- <span data-ttu-id="47a67-129">Juostelės taisyklės scenarijus „msdyn.Approval.CanApproveOrReject“ parodo skirtojo laiko klaidą.</span><span class="sxs-lookup"><span data-stu-id="47a67-129">Ribbon rule script "msdyn.Approval.CanApproveOrReject" displays a timeout error.</span></span>

<span data-ttu-id="47a67-130">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="47a67-130">**Sales**</span></span>

<span data-ttu-id="47a67-131">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="47a67-131">The following issues have been fixed:</span></span>

- <span data-ttu-id="47a67-132">Tikrinimo klaidos pranešimas nerodomas, kai formos / objekto „Naujo pasiūlymo projektų kainoraštis“ kainoraščio peržvalgoje pasirenkamas savikainos kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="47a67-132">Validation error message not displayed when a Cost Price List is selected in Price List lookup on 'New Quote Project Price List' form/entity.</span></span>
- <span data-ttu-id="47a67-133">Uždarius pasiūlymą kaip laimėtą, nėra pereinama į sukurtą sutartį, jei prie pasiūlymo pridėtas BPF yra galutiniame etape.</span><span class="sxs-lookup"><span data-stu-id="47a67-133">Closing the quote as won does not navigate to the created contract if a BPF attached to the quote is in the final stage.</span></span>
- <span data-ttu-id="47a67-134">Atšaukiant **Pardavimą, už kurį neišrašyta sąskaita** susiejama su originalia savikaina, kai laiko įrašas atšaukiamas.</span><span class="sxs-lookup"><span data-stu-id="47a67-134">Reversing **Unbilled Sales** is linked to original cost when a time entry is recalled.</span></span>
- <span data-ttu-id="47a67-135">Paspaudus mygtuką **Patvirtinti**, sąskaitos faktūros būsena nepakeičiama į **Patvirtinta**, nebent sąskaita faktūra yra atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="47a67-135">After selecting the **Confirm** button, the invoice status doesn't change to **Confirmed** unless the invoice is refreshed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]