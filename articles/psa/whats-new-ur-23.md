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
ms.openlocfilehash: 07f1a274914d7e641ddf2fd42f377dce1da7f815
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131128"
---
# <a name="project-service-automation-update-release-23-v3"></a><span data-ttu-id="9d3c2-103">„Project Service Automation“ V3 23 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="9d3c2-103">Project Service Automation Update Release 23, V3</span></span>

<span data-ttu-id="9d3c2-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9d3c2-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9d3c2-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9d3c2-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9d3c2-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9d3c2-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9d3c2-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 23 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 23.</span></span> <span data-ttu-id="9d3c2-110">Ši versija turi naują komponavimo versijos numerį V 3.10.34.30 ir ją galima pasiekti per 2020 m. rugpjūčio mėn. automatinį naujinimą.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-110">This version has a build number of V 3.10.34.30 and is generally available through a self-update in August 2020.</span></span>

## <a name="update-release-23"></a><span data-ttu-id="9d3c2-111">23 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="9d3c2-111">Update Release 23</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9d3c2-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="9d3c2-112">Bug fixes</span></span>

<span data-ttu-id="9d3c2-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="9d3c2-113">**Time and Expense**</span></span>

<span data-ttu-id="9d3c2-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="9d3c2-114">The following issues have been fixed:</span></span>
- <span data-ttu-id="9d3c2-115">Tvarkykite kraštutinį atvejį **Projekto komandos nario ištrynimo** lauke, norėdami pateikti prasmingą išimtį.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-115">Handle edge case in **Project Team Member Delete** to provide a meaningful exception.</span></span>
- <span data-ttu-id="9d3c2-116">Importavimo rezultatų priskyrimas tuščiame pašalinimo ekrane.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-116">Assignment import results in a blank remove screen.</span></span>

<span data-ttu-id="9d3c2-117">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="9d3c2-117">**Resource Management**</span></span>

<span data-ttu-id="9d3c2-118">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="9d3c2-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="9d3c2-119">**Ištekliaus panaudojimo tinklelio ištekliaus kortelė** rodo neteisingus duomenis, kai laiko mastelis yra didesnis nei penkios dienos.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-119">The **Resource utilization grid resource card** shows incorrect data when the time scale is more than five days.</span></span>
- <span data-ttu-id="9d3c2-120">Kai klientai sukuria rezervuojamą išteklių, priedas negali automatiškai su pertraukomis pridėti ištekliaus prie „Microsoft Office 365“ grupės.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-120">When customers create a bookable resource, the plug-in intermittently fails to automatically add the resource to a Microsoft Office 365 group.</span></span>
- <span data-ttu-id="9d3c2-121">**Susitaikymo** rodinys neteisingai pateikia rankinį kontūrą **savaitės** arba **mėnesio** rodinyje.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-121">**Reconciliation** view displays manual contours incorrectly in the **Week** or **Month** view.</span></span>

<span data-ttu-id="9d3c2-122">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="9d3c2-122">**Project Management**</span></span>

<span data-ttu-id="9d3c2-123">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="9d3c2-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="9d3c2-124">Pernelyg didelis **RetrieveMultiple for usersettings** objektų skaičius blogina projektų patvirtinimo ir kitų operacijų atlikimo rezultatus.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-124">An excessive number of **RetrieveMultiple for usersettings** entities are causing degraded performance for project approvals and other operations.</span></span>
- <span data-ttu-id="9d3c2-125">**Užduočių planavimo** tinklelio ištekliaus peržiūra yra ribojama iki penkių komandos narių iš projekto komandos.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-125">The **Task Planning** grid resource lookup is limited to only show up to five team members from the project team.</span></span> 
- <span data-ttu-id="9d3c2-126">**Užduočių planavimo** tinklelio ištekliaus peržiūra nefiltruoja neaktyvių išteklių.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-126">The **Task Planning** grid resource lookup does not filter inactive resources.</span></span>
- <span data-ttu-id="9d3c2-127">Rankinis režimas neveikia kaip numatyta projekto planavimo darbo paskirstymo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-127">Manual mode is not working as expected in the project planning work breakdown structure.</span></span>
- <span data-ttu-id="9d3c2-128">**Užduočių planavimo** tinklelis rodo **neaktyvias transakcijų kategorijas**.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-128">The **Task Planning** grid shows **Inactive Transaction Categories**.</span></span>
- <span data-ttu-id="9d3c2-129">**Išteklių priskyrimo** tinklelis apvalina neteisingai, kai užduotis turi kelis priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-129">The **Resource Assignment** grid rounds incorrectly when a task has multiple assignments.</span></span>
- <span data-ttu-id="9d3c2-130">Reikšmių apvalinimas skiriasi tarp suplanuotų išlaidų ir tikrosios vienos užduoties kainos.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-130">Rounding values are different between planned cost and actual cost for a single task.</span></span>

<span data-ttu-id="9d3c2-131">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="9d3c2-131">**Sales**</span></span>

<span data-ttu-id="9d3c2-132">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="9d3c2-132">The following issues have been fixed:</span></span>

- <span data-ttu-id="9d3c2-133">Dukart paspaudus **Sukelti visas transakcijų kategorijas**, sukuriamos kelios eilutės.</span><span class="sxs-lookup"><span data-stu-id="9d3c2-133">**Fetch All Transaction Categories** double-click creates multiple lines.</span></span>
