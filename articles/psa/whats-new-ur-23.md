---
title: Kas nauja arba pakeista „Project Service Automation“ V3 23 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 23 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 08/25/2020
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
ms.openlocfilehash: 87f89828aeff22d9b473539e294d5cf04d46a203
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150048"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="98d2a-103">„Project Service Automation“ V3 23 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="98d2a-103">Project Service Automation Update Release 23, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="98d2a-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="98d2a-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="98d2a-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="98d2a-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="98d2a-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="98d2a-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="98d2a-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="98d2a-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="98d2a-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="98d2a-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="98d2a-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 23 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="98d2a-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="98d2a-110">Ši versija turi naują komponavimo versijos numerį V 3.10.34.30 ir ją galima pasiekti per 2020 m. rugpjūčio mėn. automatinį naujinimą.</span><span class="sxs-lookup"><span data-stu-id="98d2a-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="98d2a-111">23 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="98d2a-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="98d2a-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="98d2a-112">Bug fixes</span></span>

<span data-ttu-id="98d2a-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="98d2a-113">**Time and Expense**</span></span>

<span data-ttu-id="98d2a-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="98d2a-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="98d2a-115">Tvarkykite kraštutinį atvejį **Projekto komandos nario ištrynimo** lauke, norėdami pateikti prasmingą išimtį.</span><span class="sxs-lookup"><span data-stu-id="98d2a-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="98d2a-116">Importavimo rezultatų priskyrimas tuščiame pašalinimo ekrane.</span><span class="sxs-lookup"><span data-stu-id="98d2a-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="98d2a-117">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="98d2a-117">**Resource Management**</span></span>

<span data-ttu-id="98d2a-118">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="98d2a-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="98d2a-119">**Ištekliaus panaudojimo tinklelio ištekliaus kortelė** rodo neteisingus duomenis, kai laiko mastelis yra didesnis nei penkios dienos.</span><span class="sxs-lookup"><span data-stu-id="98d2a-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="98d2a-120">Kai klientai sukuria rezervuojamą išteklių, priedas negali automatiškai su pertraukomis pridėti ištekliaus prie „Microsoft Office 365“ grupės.</span><span class="sxs-lookup"><span data-stu-id="98d2a-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="98d2a-121">**Susitaikymo** rodinys neteisingai pateikia rankinį kontūrą **savaitės** arba **mėnesio** rodinyje.</span><span class="sxs-lookup"><span data-stu-id="98d2a-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="98d2a-122">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="98d2a-122">**Project Management**</span></span>

<span data-ttu-id="98d2a-123">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="98d2a-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="98d2a-124">Pernelyg didelis **RetrieveMultiple for usersettings** objektų skaičius blogina projektų patvirtinimo ir kitų operacijų atlikimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="98d2a-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="98d2a-125">**Užduočių planavimo** tinklelio ištekliaus peržiūra yra ribojama iki penkių komandos narių iš projekto komandos.</span><span class="sxs-lookup"><span data-stu-id="98d2a-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="98d2a-126">**Užduočių planavimo** tinklelio ištekliaus peržiūra nefiltruoja neaktyvių išteklių.</span><span class="sxs-lookup"><span data-stu-id="98d2a-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="98d2a-127">Rankinis režimas neveikia kaip numatyta projekto planavimo darbo paskirstymo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="98d2a-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="98d2a-128">**Užduočių planavimo** tinklelis rodo **neaktyvias transakcijų kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="98d2a-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="98d2a-129">**Išteklių priskyrimo** tinklelis apvalina neteisingai, kai užduotis turi kelis priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="98d2a-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="98d2a-130">Reikšmių apvalinimas skiriasi tarp suplanuotų išlaidų ir tikrosios vienos užduoties kainos.</span><span class="sxs-lookup"><span data-stu-id="98d2a-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="98d2a-131">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="98d2a-131">**Sales**</span></span>

<span data-ttu-id="98d2a-132">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="98d2a-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="98d2a-133">Dukart paspaudus **Sukelti visas transakcijų kategorijas**, sukuriamos kelios eilutės.</span><span class="sxs-lookup"><span data-stu-id="98d2a-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
