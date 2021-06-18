---
title: Kas nauja arba pakeista „Project Service Automation“ V3 13 atnaujintame leidime
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 13 atnaujintame leidime V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: c328821064065e19938406856d327f690f577e7a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000311"
---
# <a name="project-service-automation-update-release-13-v3"></a><span data-ttu-id="95017-103">„Project Service Automation“ V3 13 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="95017-103">Project Service Automation Update Release 13, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="95017-104">Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą.</span><span class="sxs-lookup"><span data-stu-id="95017-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="95017-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="95017-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="95017-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="95017-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="95017-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="95017-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="95017-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="95017-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="95017-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 13 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="95017-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 13.</span></span> <span data-ttu-id="95017-110">Ši versija turi naują komponavimo versijos numerį V3.10.3.18 ir ją galima gauti pagal toliau pateiktą grafiką:</span><span class="sxs-lookup"><span data-stu-id="95017-110">This version has a build number of V3.10.3.18 and is available on the following schedule:</span></span>

- <span data-ttu-id="95017-111">**Bendras prieinamumas (automatinis naujinimas):** 2019 m. lapkričio mėn.</span><span class="sxs-lookup"><span data-stu-id="95017-111">**General availability (self-update):** November 2019</span></span>
- <span data-ttu-id="95017-112">**Automatinis naujinimas:** 2019 m. gruodžio mėn.</span><span class="sxs-lookup"><span data-stu-id="95017-112">**Auto-update:** December 2019</span></span>


## <a name="update-release-13"></a><span data-ttu-id="95017-113">13 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="95017-113">Update Release 13</span></span> 

### <a name="bug-fixes"></a><span data-ttu-id="95017-114">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="95017-114">Bug fixes</span></span>

- <span data-ttu-id="95017-115">Laikas ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="95017-115">Time and Expense</span></span>

     - <span data-ttu-id="95017-116">Sutaisyta: ieškos funkcija puslapyje **Išlaidų patvirtinimas** neveikia, kai ieškoma išlaidų tikslu.</span><span class="sxs-lookup"><span data-stu-id="95017-116">Fixed: Search functionality on the **Expense approval** page does not work when searching by expense purpose.</span></span>

- <span data-ttu-id="95017-117">Išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="95017-117">Resource Management</span></span>

     - <span data-ttu-id="95017-118">Sutaisyta: skaičiai suderinime atnaujinti, kad būtų tinkamai pagrįsti.</span><span class="sxs-lookup"><span data-stu-id="95017-118">Fixed: Numbers in the reconciliation have been updated to be right justified.</span></span>
     - <span data-ttu-id="95017-119">Sutaisyta: įvardinti ištekliai negali būti priskirti užduotiems naudojant skirtuką **Grafikas**.</span><span class="sxs-lookup"><span data-stu-id="95017-119">Fixed: Named Resources can't be assigned to tasks through the **Schedule** tab.</span></span>

- <span data-ttu-id="95017-120">Projektų valdymas</span><span class="sxs-lookup"><span data-stu-id="95017-120">Project Management</span></span>

     - <span data-ttu-id="95017-121">Sutaisyta: neapibrėžtos nuorodos išimtis, kai priskiriamas komandos narys, kai **TransactionType** trūksta informacijos apie **Vienetas** ir **DefaultGroup**.</span><span class="sxs-lookup"><span data-stu-id="95017-121">Fixed: Null reference exception when assigning team member when the **TransactionType** is missing setup information for **Unit** and **DefaultGroup**.</span></span>

- <span data-ttu-id="95017-122">Sales</span><span class="sxs-lookup"><span data-stu-id="95017-122">Sales</span></span>

     - <span data-ttu-id="95017-123">Sutaisyta: dubliuoti operacijos tipo įrašai grąžina klaidą, kai sukuriami vaidmens kainos įrašai.</span><span class="sxs-lookup"><span data-stu-id="95017-123">Fixed: Duplicate transaction type records return an error when role price records are created.</span></span>
     - <span data-ttu-id="95017-124">Ištaisyta: papildomi mygtukai **Nauja galimybė**, **Pasiūlymas**, **Užsakymo eilutė** ir **Įtraukti produktą** yra matomi komandose, skirtose galimybėms, pasiūlymams, užsakymo produktams ir projektu pagrįstų eilučių papildomam tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="95017-124">Fixed: Extra buttons for **New Opportunity**, **Quote**, **Order Line**, and **Add Product** are visible in commands for Opportunities, Quotes, Order Products, and the project-based Lines subgrid.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]