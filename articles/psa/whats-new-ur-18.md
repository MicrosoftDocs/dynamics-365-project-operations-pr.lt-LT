---
title: Kas nauja arba pakeista „Project Service Automation“ V3 18 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 18 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: d6e0bb669513185ca266858ea9b8a89ed6dd4408
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147213"
---
# <a name="project-service-automation-update-release-18-v3"></a><span data-ttu-id="58880-103">„Project Service Automation“ V3 18 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="58880-103">Project Service Automation Update Release 18, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="58880-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="58880-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="58880-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="58880-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="58880-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="58880-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="58880-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="58880-107">To update to this release, visit the Admin Center for Dynamics 365 online, solutions page to install the update.</span></span> <span data-ttu-id="58880-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="58880-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="58880-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 18 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="58880-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 18.</span></span> <span data-ttu-id="58880-110">Šios versijos komponavimo versijos numeris yra V3.10.8.12 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. balandžio mėn.</span><span class="sxs-lookup"><span data-stu-id="58880-110">This version has a build number of V3.10.8.12 and is generally available through a self-update in April 2020.</span></span>

## <a name="update-release-18"></a><span data-ttu-id="58880-111">18 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="58880-111">Update Release 18</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="58880-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="58880-112">Bug fixes</span></span>

<span data-ttu-id="58880-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="58880-113">**Time and Expense**</span></span>

- <span data-ttu-id="58880-114">Išspręsta: srautai **Atšaukti**, **Pateikti užklausą** ir **Atšaukti patvirtinimą** pateikia išimtis su neaiškiais klaidos pranešimais.</span><span class="sxs-lookup"><span data-stu-id="58880-114">Fixed: **Recall**, **Request**, and **Cancel Approval** flows throw exceptions with unclear error messages.</span></span>
- <span data-ttu-id="58880-115">Išspręsta: kai išlaidoms nepavyksta **Atšaukti patvirtinimą**, nepateikiama reikiama išimties klaida.</span><span class="sxs-lookup"><span data-stu-id="58880-115">Fixed: When **Cancel Approval** fails for an expense, a relevant exception error is not thrown.</span></span>
- <span data-ttu-id="58880-116">Išspręsta: tinklelyje Laiko įrašas neteisingai tvarkomos ne darbo dienos Australijoje po vasaros laiko įvedimo (DST) spalio mėn.</span><span class="sxs-lookup"><span data-stu-id="58880-116">Fixed: The Time Entry grid incorrectly handles non-working days in Australia after the daylight savings time (DST) switch in October.</span></span>
- <span data-ttu-id="58880-117">Išspręsta: dėl netinkamos numatytojo vykdymo logikos negalima pateikti išlaidų.</span><span class="sxs-lookup"><span data-stu-id="58880-117">Fixed: Incorrect defaulting logic prevents submission of expenses.</span></span>
- <span data-ttu-id="58880-118">Išspręsta: kai laiko įrašo patvirtinimas yra nesėkmingas, jis tebėra būsenoje **Laukiama**.</span><span class="sxs-lookup"><span data-stu-id="58880-118">Fixed: When time entry approval fails, the approval remains in a state of **Pending**.</span></span>
- <span data-ttu-id="58880-119">Išspręsta: SQL masinių patvirtinimų klaidos (aklavietė / pasibaigė skirtasis laikas).</span><span class="sxs-lookup"><span data-stu-id="58880-119">Fixed: SQL Errors on bulk approvals (deadlock/timeout).</span></span>
- <span data-ttu-id="58880-120">Išspręsta: patvirtinant laiko įrašus vartotojo patirtyje atsiranda reikšmingų našumo problemų, kai naujinami komandos nariai.</span><span class="sxs-lookup"><span data-stu-id="58880-120">Fixed: Significant performance issues in the user experience caused by updating team members while approving time entries.</span></span>

<span data-ttu-id="58880-121">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="58880-121">**Project Management**</span></span>

- <span data-ttu-id="58880-122">Išspręsta: laiko juostos pranešimas perkeltas iš rodinio **Suderinimas** į pagrindinę formą **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="58880-122">Fixed: Time zone notification moved from the **Reconciliation** view to the **Project** main form.</span></span>
- <span data-ttu-id="58880-123">Išspręsta: kalendoriaus šablonas netinkamai vykdomas, kai atidaroma nauja projekto forma.</span><span class="sxs-lookup"><span data-stu-id="58880-123">Fixed: Calendar template is not correctly defaulting when a new project form opens.</span></span>
- <span data-ttu-id="58880-124">Išspręsta: „Chromium“ pagrindu sukurtose naršyklėse vartotojai negali lengvai pažymėti naikinti ankstesnių užduočių.</span><span class="sxs-lookup"><span data-stu-id="58880-124">Fixed: For chromium-based browsers, users are unable to easily select predecessor tasks to delete.</span></span>
- <span data-ttu-id="58880-125">Išspręsta: kuriant arba kopijuojant **projektą iš tuščio šablono** iškviečiami nesusiję priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="58880-125">Fixed: Creating or copying **Project from Empty template** fetches unrelated assignments.</span></span>
- <span data-ttu-id="58880-126">Išspręsta: tam tikrais kraštutiniais atvejais sukūrus naują priskyrimą iš užduočių tinklelio, sukuriami įrašų dublikatai.</span><span class="sxs-lookup"><span data-stu-id="58880-126">Fixed: In specific edge cases, creating a new assignment from the task grid results in duplicate records being created.</span></span>
- <span data-ttu-id="58880-127">Išspręsta: neautomatiniu režimu vartotojai negali atnaujinti užduoties pradžios datos, kad ši būtų vėlesnė nei dabartinė įrašyta data.</span><span class="sxs-lookup"><span data-stu-id="58880-127">Fixed: In manual mode, users are unable to update task start dates to be later than the current date saved.</span></span>

<span data-ttu-id="58880-128">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="58880-128">**Resource Management**</span></span>

- <span data-ttu-id="58880-129">Išspręsta: išplėtus rezervavimus rodinio **Suderinimas** tarpinės sumos eilutėje neteisingai apskaičiuojamas rezervavimų nuokrypis.</span><span class="sxs-lookup"><span data-stu-id="58880-129">Fixed: **Reconciliation** view subtotal row incorrectly calculates bookings variance after extending bookings.</span></span>
- <span data-ttu-id="58880-130">Išspręsta: rodinyje **Suderinimas** netinkamai rodomi išteklių priskyrimai, kai rezervuotinų išteklių kalendorius neatitinka projekto kalendoriaus.</span><span class="sxs-lookup"><span data-stu-id="58880-130">Fixed: **Reconciliation** view incorrectly displays resource assignments when the bookable resource has a calendar that does not match the project calendar.</span></span>

<span data-ttu-id="58880-131">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="58880-131">**Sales**</span></span>

- <span data-ttu-id="58880-132">Išspręsta: kai laiko įrašai patvirtinami iš naujo (**Patvirtinti > Atšaukti >** patvirtinti dar kartą), sukuriamas įrašo duplikatas su neapmokestinama faktine reikšme.</span><span class="sxs-lookup"><span data-stu-id="58880-132">Fixed: When time entries are re-approved (**Approve > Cancel >** approve again), a duplicate non-chargeable actual is created.</span></span>
