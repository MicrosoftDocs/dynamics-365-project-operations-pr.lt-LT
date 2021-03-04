---
title: Kas nauja arba pakeista „Project Service Automation“ V3 28 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 28 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/26/2021
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
ms.openlocfilehash: 2c50d6bdc033836e1259a2fd12b78015280d8093
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150633"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-28-v3"></a><span data-ttu-id="2b3ad-103">Kas nauja arba pakeista „Project Service Automation“ V3 28 atnaujintame leidime</span><span class="sxs-lookup"><span data-stu-id="2b3ad-103">What's new or changed in Project Service Automation Update Release 28, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="2b3ad-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="2b3ad-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="2b3ad-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="2b3ad-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="2b3ad-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="2b3ad-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="2b3ad-109">Šioje temoje išvardytos naujos ar pakeistos „Project Service Automation“ V3, atnaujinto 28 leidimo funkcijos ir taisymai. Šios komponavimo versijos numeris yra V3.10.46.32 ir ji yra visuotinai pasiekiama 2021 m. sausio mėn. savaiminiame naujinime.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 28 This version has a build number of V3.10.46.32 and is generally available through a self-update in January 2021.</span></span>

## <a name="update-release-28"></a><span data-ttu-id="2b3ad-110">28 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="2b3ad-110">Update Release 28</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="2b3ad-111">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="2b3ad-111">Bug fixes</span></span>

<span data-ttu-id="2b3ad-112">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="2b3ad-112">**Time and Expense**</span></span>

<span data-ttu-id="2b3ad-113">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="2b3ad-113">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b3ad-114">Vartotojai gali naudoti parinktį **Masinis redagavimas**, kad atnaujintų patvirtintus ir pateiktus laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-114">Users can use **Bulk Edit** to update time entries that have been approved and submitted.</span></span>

<span data-ttu-id="2b3ad-115">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="2b3ad-115">**Project Management**</span></span>

<span data-ttu-id="2b3ad-116">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="2b3ad-116">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b3ad-117">Tais atvejais, kai užduoties GUID interpretuojamas kaip skaičius, užduočių negalima atidaryti redaguoti naudojant parinktį **Redaguoti užduotį**, kuri yra puslapio **Darbo paskirstymo struktūra** juostoje.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-117">In cases where the task GUID is interpreted as a number, tasks can't be opened for edit using **Edit Task** in the ribbon on the **Work Breakdown Structure** page.</span></span>

<span data-ttu-id="2b3ad-118">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="2b3ad-118">**Sales**</span></span>

<span data-ttu-id="2b3ad-119">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="2b3ad-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="2b3ad-120">Iškvietus **GetEstimatesForProject** priedą generuojama nulinės nuorodos išimtis.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-120">A null reference exception is generated when the **GetEstimatesForProject** plug-in is invoked.</span></span>
- <span data-ttu-id="2b3ad-121">**Pažymėti kaip parengtą išrašyti sąskaitą faktūrą** etapo tinklelyje tik iš dalies atnaujina atributus, išskyrus atributą **InvoiceStatus**, kuris atnaujinamas.</span><span class="sxs-lookup"><span data-stu-id="2b3ad-121">**Mark ready to invoice** on the milestone grid only partially updates attributes, except for the **InvoiceStatus** attribute, which is updated.</span></span>

