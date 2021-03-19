---
title: Kas nauja arba pakeista „Project Service Automation“ V3 29 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 29 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/22/2021
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
ms.openlocfilehash: 711255ab66f84fe46d0f16fa72e5a10fe0360394
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499681"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-29-v3"></a><span data-ttu-id="9ff37-103">Kas nauja arba pakeista „Project Service Automation“ V3 29 atnaujintame leidime</span><span class="sxs-lookup"><span data-stu-id="9ff37-103">What's new or changed in Project Service Automation Update Release 29, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="9ff37-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="9ff37-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="9ff37-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="9ff37-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="9ff37-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="9ff37-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="9ff37-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="9ff37-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="9ff37-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="9ff37-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="9ff37-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 29 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="9ff37-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 29.</span></span> <span data-ttu-id="9ff37-110">Šios versijos numeris yra V3.10.45.98 ir ji visuotinai pasiekiama įdiegiant savaiminį 2021 m. vasario mėn. naujinimą.</span><span class="sxs-lookup"><span data-stu-id="9ff37-110">This version has a build number of V3.10.45.98 and is generally available through a self-update in February 2021.</span></span>

## <a name="update-release-29"></a><span data-ttu-id="9ff37-111">29 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="9ff37-111">Update Release 29</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="9ff37-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="9ff37-112">Bug fixes</span></span>

<span data-ttu-id="9ff37-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="9ff37-113">**Time and Expense**</span></span>

<span data-ttu-id="9ff37-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="9ff37-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ff37-115">Vartotojams laiko įvedimo tinklelyje nemato darbo valandų, kai jie prisijungia ne darbo dienomis.</span><span class="sxs-lookup"><span data-stu-id="9ff37-115">Users can't see working hours logged on non-working days in the time entry grid.</span></span>
- <span data-ttu-id="9ff37-116">Patvirtintus išlaidų įrašus tinklelyje galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="9ff37-116">Approved expense entries can be edited on the grid.</span></span>

<span data-ttu-id="9ff37-117">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="9ff37-117">**Project Management**</span></span>

<span data-ttu-id="9ff37-118">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="9ff37-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ff37-119">Trūksta tikrinimo logikos, užtikrinančios, kad išteklių priskyrimo pastangų valandos negali būti neigiamos.</span><span class="sxs-lookup"><span data-stu-id="9ff37-119">Missing validation logic to ensure resource assignment effort hours can't be negative.</span></span>
- <span data-ttu-id="9ff37-120">Pasirinktinis veiksmas **AssignResourcesForTask** atnaujina visus laukus, o ne tik pakeistus laukus.</span><span class="sxs-lookup"><span data-stu-id="9ff37-120">The custom action, **AssignResourcesForTask** updates all fields instead of only changed fields.</span></span>
- <span data-ttu-id="9ff37-121">Kopijuojant projektą aplinkoje su priedais arba darbo eigomis, kurios yra užregistruotos įvykyje **CreateProject**, atributas **msdyn_bulkgenerationstatus** neatnaujinamas, jei **CopyWBSToProject** veiksmas nepavyks.</span><span class="sxs-lookup"><span data-stu-id="9ff37-121">When copying a project in an environment with plug-ins or workflows that are registered on the **CreateProject** event, the **msdyn_bulkgenerationstatus** attribute isn't updated if the **CopyWBSToProject** fails.</span></span>
- <span data-ttu-id="9ff37-122">Kai išplečiate projekto kalendorių, darbo dienos nerūšiuojamos didėjimo tvarka, todėl nepavyksta atnaujinti kai kurių projekto užduočių.</span><span class="sxs-lookup"><span data-stu-id="9ff37-122">When you expand the project calendar, the working days aren't sorted in ascending order causing some project task updates to fail.</span></span>
- <span data-ttu-id="9ff37-123">Keičiant esamo projekto projekto vadovą paleidžiama numatytoji organizacijos vieneto logika.</span><span class="sxs-lookup"><span data-stu-id="9ff37-123">Changing the Project Manager on an existing project triggers the organizational unit defaulting logic.</span></span>

<span data-ttu-id="9ff37-124">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="9ff37-124">**Sales**</span></span>

<span data-ttu-id="9ff37-125">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="9ff37-125">The following issues have been fixed:</span></span>

- <span data-ttu-id="9ff37-126">Puslapio **Sutartis** skirtuko **Sutaties efektyvumas** veiksmas nepavyksta inicijavimo metu, kai nėra sutarties eilučių.</span><span class="sxs-lookup"><span data-stu-id="9ff37-126">The **Contract Performance** tab on the **Contract** page fails silently during initialization when no contract lines are present.</span></span>
