---
title: Projekto užduočių sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“
description: Šioje temoje aprašomi šablonas ir pagrindinė užduotis, kurie naudojami norint sinchronizuoti projekto užduotis tiesiogiai iš „Microsoft Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: d7f32327-33c4-43ab-b799-786210e93277
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 66a255346727c7ee4fbbf2920d2ef437ded03308
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753760"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="76a49-103">Projekto užduočių sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="76a49-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="76a49-104">Šioje temoje aprašomi šablonas ir pagrindinė užduotis, kurie naudojami norint sinchronizuoti projekto užduotis tiesiogiai iš „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="76a49-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="76a49-105">Projekto užduočių integravimas, išlaidų operacijų kategorijos, valandų įvertinimas, išlaidų įvertinimas ir funkcijų blokavimas prieinami 8.0 versijoje.</span><span class="sxs-lookup"><span data-stu-id="76a49-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="76a49-106">Jei naudojate „Enterprise Edition“ 7.3.0, įdiegę KB 4132657 ir KB 4132660, galėsite naudoti šablonus projektų užduotims, išlaidų operacijų kategorijoms, valandų įvertinimui, išlaidų įvertinimui ir faktiniams duomenims integruoti bei funkcijų blokavimui konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="76a49-106">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="76a49-107">Jei reikia iš naujo nustatyti apskaitos paskirstymą, rekomenduojame įdiegti ir KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="76a49-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="76a49-108">Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.</span><span class="sxs-lookup"><span data-stu-id="76a49-108">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="76a49-109">Duomenų srautas iš „Project Service Automation“ į „Finance“</span><span class="sxs-lookup"><span data-stu-id="76a49-109">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="76a49-110">Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="76a49-110">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="76a49-111">Integravimo šablonas, kurį galima naudoti su duomenų integravimo funkcija, įjungia duomenų srautą apie projektų užduotis iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="76a49-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance.</span></span>

<span data-ttu-id="76a49-112">Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="76a49-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="76a49-113">[![„Project Service Automation“ ir „Finance“ integravimo duomenų srautas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="76a49-113">[![Data flow for Project Service Automation integration with Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="76a49-114">Šablonas ir užduotis</span><span class="sxs-lookup"><span data-stu-id="76a49-114">Template and task</span></span>

<span data-ttu-id="76a49-115">Norėdami pasiekti šabloną, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="76a49-115">To access the template, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="76a49-116">Toliau pateikiamas šablonas ir pagrindinė užduotis naudojami norint sinchronizuoti projekto užduotis iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="76a49-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="76a49-117">**Šablono pavadinimas pasirinkus duomenų integravimą:** projekto užduotys (PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="76a49-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="76a49-118">**Projekto užduoties pavadinimas:** projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="76a49-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="76a49-119">Prieš atliekant projekto užduočių sinchronizavimą, reikia sinchronizuoti projektų sutartis ir projektus.</span><span class="sxs-lookup"><span data-stu-id="76a49-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="76a49-120">Objektų rinkinys </span><span class="sxs-lookup"><span data-stu-id="76a49-120">Entity set</span></span>

| <span data-ttu-id="76a49-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="76a49-121">Project Service Automation</span></span> | <span data-ttu-id="76a49-122">„Finance“</span><span class="sxs-lookup"><span data-stu-id="76a49-122">Finance</span></span>                             |
|----------------------------|-------------------------------------|
| <span data-ttu-id="76a49-123">Projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="76a49-123">Project Tasks</span></span>              | <span data-ttu-id="76a49-124">Projekto užduoties integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="76a49-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="76a49-125">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="76a49-125">Entity flow</span></span>

<span data-ttu-id="76a49-126">Projektų užduotys valdomos naudojant „Project Service Automation“, o sinchronizuojamos su „Finance“ kaip projektų veiklos.</span><span class="sxs-lookup"><span data-stu-id="76a49-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="76a49-127">Būtinosios sąlygos ir susiejimo sąranka</span><span class="sxs-lookup"><span data-stu-id="76a49-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="76a49-128">Prieš atliekant projekto užduočių sinchronizavimą, reikia sinchronizuoti projektų sutartis ir projektus.</span><span class="sxs-lookup"><span data-stu-id="76a49-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="76a49-129">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="76a49-129">Power Query</span></span>

<span data-ttu-id="76a49-130">Norėdami filtruoti duomenis, jei patenkinama toliau pateikiama sąlyga, turite naudoti „Microsoft Power Query for Excel“.</span><span class="sxs-lookup"><span data-stu-id="76a49-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="76a49-131">Projekto užduotyje yra ištekliams būdingų įrašų.</span><span class="sxs-lookup"><span data-stu-id="76a49-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="76a49-132">Jei reikia naudoti „Power Query“, vadovaukitės toliau pateikiamais nurodymais.</span><span class="sxs-lookup"><span data-stu-id="76a49-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="76a49-133">Projektų užduočių (PSA į „Fin and Ops“) šablone yra numatytasis filtras, neįtraukiantis ištekliams būdingų įrašų į projekto užduotį, nustatydamas filtro **IsLineTask** reikšmę **Klaidinga**.</span><span class="sxs-lookup"><span data-stu-id="76a49-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="76a49-134">Kurdami savo šabloną, turite įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="76a49-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="76a49-135">Šablonų susiejimas pasirinkus Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="76a49-135">Template mapping in Data integration</span></span>

<span data-ttu-id="76a49-136">Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimų pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="76a49-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="76a49-137">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="76a49-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="76a49-138">[![Šablonų susiejimas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="76a49-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
