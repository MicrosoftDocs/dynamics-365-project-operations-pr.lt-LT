---
title: „Project Service Automation“ apžvalga
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“ integravimo sprendimą.
author: ruhercul
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5ca459b99881b612e4656be112c8a2e420b4196e
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005891"
---
# <a name="project-service-automation-overview"></a><span data-ttu-id="38e3b-103">„Project Service Automation“ apžvalga</span><span class="sxs-lookup"><span data-stu-id="38e3b-103">Project Service Automation overview</span></span>

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="38e3b-104">Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“ egzemplioriuose per „Common Data Service“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-104">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Dynamics 365 Finance and Dynamics 365 Project Service Automation via Common Data Service.</span></span> <span data-ttu-id="38e3b-105">Integravimo šablonai, kuriuos galima naudoti su duomenų integravimo funkcija, leidžia vykdyti projektų, projektų sutarčių, projektų sutarčių eilučių, projektų sutarčių eilučių etapų, projektų užduočių, išlaidų operacijų kategorijų, valandų įvertinimo ir išlaidų įvertinimo srautą iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-105">The integration templates that are available with the Data integration feature enable the flow of projects, project contracts, project contract lines, project contract line milestones, project tasks, expense transaction categories, hour estimates, and expense estimates from Project Service Automation to Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="38e3b-106">Jei naudojate 7.3.0 versiją, turite įdiegti KB 4074835.</span><span class="sxs-lookup"><span data-stu-id="38e3b-106">If you're using version 7.3.0, you must install KB 4074835.</span></span> <span data-ttu-id="38e3b-107">Tada galėsite integruoti fiksuotos kainos projektus.</span><span class="sxs-lookup"><span data-stu-id="38e3b-107">You will then be able to integrate fixed price projects.</span></span>
> - <span data-ttu-id="38e3b-108">Jei naudojate 7.3.0 versiją ir norite įtraukti mokesčių operacijas iš „Project Service Automation“, turite įdiegti KB 4345320, kad įtrauktumėte šiuos mokesčius į projekto sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="38e3b-108">If you're using version 7.3.0, and you are bringing fee transactions over from Project Service Automation, you must install KB 4345320 in order to include those fees in the project invoice.</span></span>
> - <span data-ttu-id="38e3b-109">Jei naudojate 8.0 versiją, galėsite naudoti projekto užduočių integravimą, išlaidų operacijų kategorijas, valandų įvertinimą, išlaidų įvertinimą ir funkcijų blokavimą.</span><span class="sxs-lookup"><span data-stu-id="38e3b-109">If you're using version 8.0, you will be able to use project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking.</span></span>
> - <span data-ttu-id="38e3b-110">Jei naudojate 8.0.1 arba naujesnę versiją, galėsite sinchronizuoti faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="38e3b-110">If you're using version 8.0.1 or later, you will be able to synchronize actuals.</span></span>

<span data-ttu-id="38e3b-111">Kad galėtumėte integruoti „Project Service Automation“ ir „Finance“, turite sukonfigūruoti „Project Service Automation“ integravimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="38e3b-111">Before you can integrate Project Service Automation Finance, you must configure the Project Service Automation integration parameters.</span></span> <span data-ttu-id="38e3b-112">Daugiau informacijos žr. skyriuje [„Project Service Automation“ integravimo parametrai](PSA-parameters.md).</span><span class="sxs-lookup"><span data-stu-id="38e3b-112">For more information, see [Project Service Automation integration parameters](PSA-parameters.md).</span></span>

<span data-ttu-id="38e3b-113">Šis integravimo sprendimas leidžia tiesiogiai sinchronizuoti toliau pateikiamais atvejais.</span><span class="sxs-lookup"><span data-stu-id="38e3b-113">This integration solution enables direct synchronization in the following scenarios:</span></span>

- <span data-ttu-id="38e3b-114">Saugokite projektų sutartis „Project Service Automation“ ir sinchronizuokite jas tiesiogiai iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-114">Maintain project contracts in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="38e3b-115">Kurkite projektus, naudodami „Project Service Automation“, ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-115">Create projects in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="38e3b-116">Saugokite projektų sutarčių eilutes „Project Service Automation“ ir sinchronizuokite jas tiesiogiai iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-116">Maintain project contract lines in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="38e3b-117">Saugokite projektų sutarčių eilučių etapus „Project Service Automation“ ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-117">Maintain project contract line milestones in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="38e3b-118">Saugokite projektų užduotis „Project Service Automation“ ir sinchronizuokite jas tiesiogiai iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-118">Maintain project tasks in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="38e3b-119">Saugokite išlaidų operacijų kategorijas „Finance“ ir sinchronizuokite jas tiesiogiai iš „Finance“ į „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-119">Maintain expense transaction categories in Finance, and synchronize them directly from Finance to Project Service Automation.</span></span>
- <span data-ttu-id="38e3b-120">Kurkite projektų valandų įvertinimus, naudodami „Project Service Automation“, ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-120">Create project hour estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="38e3b-121">Kurkite projektų išlaidų įvertinimus, naudodami „Project Service Automation“, ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-121">Create project expense estimates in Project Service Automation, and synchronize them directly from Project Service Automation to Finance.</span></span>
- <span data-ttu-id="38e3b-122">Kurkite projektų laiko, išlaidų ir mokesčių faktinius duomenis, naudodami „Project Service Automation“, ir kurkite projektų operacijas „Project Service Automation“ integravimo žurnale, kad jas būtų galima užregistruoti naudojant „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-122">Create project time, expense, and fee actuals in Project Service Automation, and create project transactions in the Project Service Automation integration journal so that they can be posted in Finance.</span></span>

## <a name="data-synchronization"></a><span data-ttu-id="38e3b-123">Duomenų sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="38e3b-123">Data synchronization</span></span>

<span data-ttu-id="38e3b-124">Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami vykdant integravimą tarp „Project Service Automation“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="38e3b-124">The following illustration shows how data is synchronized as part of the integration between Project Service Automation and Finance.</span></span>

> [!NOTE]
> <span data-ttu-id="38e3b-125">Šiuo metu pasiekiami ne visi šablonai.</span><span class="sxs-lookup"><span data-stu-id="38e3b-125">Not all templates are currently available.</span></span> <span data-ttu-id="38e3b-126">Šablonai bus išleisti juos užbaigus.</span><span class="sxs-lookup"><span data-stu-id="38e3b-126">Templates will be released as they are completed.</span></span>

<span data-ttu-id="38e3b-127">[![„Project Service Automation“ ir „Finance“ integravimas](./media/PSA-integration.png)](./media/PSA-integration.png)</span><span class="sxs-lookup"><span data-stu-id="38e3b-127">[![Project Service Automation integration with Finance](./media/PSA-integration.png)](./media/PSA-integration.png)</span></span>

## <a name="system-requirements-for-finance"></a><span data-ttu-id="38e3b-128">„Finance“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="38e3b-128">System requirements for Finance</span></span>

<span data-ttu-id="38e3b-129">Norėdami naudoti „Project Service Automation“ į „Finance“ integravimo sprendimą, turite įdiegti „Enterprise edition“ 7.3 su 12 arba naujesnės versijos platforma.</span><span class="sxs-lookup"><span data-stu-id="38e3b-129">To use the Project Service Automation to Finance integration solution, you must install Enterprise edition 7.3 with Platform update 12 or later.</span></span>

## <a name="system-requirements-for-project-service-automation"></a><span data-ttu-id="38e3b-130">„Project Service Automation“ sistemos reikalavimai</span><span class="sxs-lookup"><span data-stu-id="38e3b-130">System requirements for Project Service Automation</span></span>

<span data-ttu-id="38e3b-131">Norėdami naudoti „Project Service Automation“ į „Finance“ integravimo sprendimą, turite įdiegti toliau pateikiamus komponentus.</span><span class="sxs-lookup"><span data-stu-id="38e3b-131">To use the Project Service Automation to Finance integration solution, you must install the following components:</span></span>

- <span data-ttu-id="38e3b-132">„Dynamics 365 Project Service Automation“ 9.0.0.0 arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="38e3b-132">Dynamics 365 Project Service Automation version 9.0.0.0 or later</span></span>
- <span data-ttu-id="38e3b-133">„Dynamics 365 Sales“ skirtas galimų klientų pavertimo pinigais sprendimas, 1.14.0.0 (v14) arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="38e3b-133">Prospect to cash solution for Dynamics 365 Sales, version 1.14.0.0 (v14) or later</span></span>
- <span data-ttu-id="38e3b-134">„Dynamics 365 Project Service Automation“ skirtas „Project Service Automation“ į „Finance“ sprendimas, 1.0.0.0 arba naujesnė versija</span><span class="sxs-lookup"><span data-stu-id="38e3b-134">Project Service Automation to Finance solution for Dynamics 365 Project Service Automation version 1.0.0.0 or later</span></span>

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a><span data-ttu-id="38e3b-135">„Project Service Automation“ į „Finance“ integravimo sprendimo diegimas „Project Service Automation“ egzemplioriuje</span><span class="sxs-lookup"><span data-stu-id="38e3b-135">Install the Project Service Automation to Finance integration solution in your Project Service Automation instance</span></span>

<span data-ttu-id="38e3b-136">Atsisiųskite „Project Service Automation“ į „Finance“ integravimo sprendimą iš [„Microsoft“ atsisiuntimo centro](https://www.microsoft.com/download/details.aspx?id=57016) ir vykdykite į sprendimą įtrauktas instrukcijas.</span><span class="sxs-lookup"><span data-stu-id="38e3b-136">Download the Project Service Automation to Finance integration solution from [Microsoft Download Center](https://www.microsoft.com/download/details.aspx?id=57016), and follow the instructions that are included with the solution.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]