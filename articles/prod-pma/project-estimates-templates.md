---
title: Projekto įvertinimų sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurie naudojami norint sinchronizuoti projekto valandų įvertinimus ir projekto išlaidų įvertinimus tiesiogiai iš „Microsoft Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.
author: Yowelle
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
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 336de474c859d30d1ec07ae34bf0c3d578faeef1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080964"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="c0c22-103">Projekto įvertinimų sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“</span><span class="sxs-lookup"><span data-stu-id="c0c22-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c0c22-104">Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurie naudojami norint sinchronizuoti projekto valandų įvertinimus ir projekto išlaidų įvertinimus tiesiogiai iš „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="c0c22-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="c0c22-105">Projekto užduočių integravimas, išlaidų operacijų kategorijos, valandų įvertinimas, išlaidų įvertinimas ir funkcijų blokavimas prieinami 8.0 versijoje.</span><span class="sxs-lookup"><span data-stu-id="c0c22-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="c0c22-106">Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.</span><span class="sxs-lookup"><span data-stu-id="c0c22-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="c0c22-107">Duomenų srautas iš „Project Service Automation“ į „Finance“</span><span class="sxs-lookup"><span data-stu-id="c0c22-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="c0c22-108">Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="c0c22-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="c0c22-109">Integravimo šablonai, kuriuos galima naudoti su duomenų integravimo funkcija, įjungia duomenų srautą apie projekto valandų įvertinimus ir projekto išlaidų įvertinimus iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c0c22-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c0c22-110">Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c0c22-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="c0c22-111">[![„Project Service Automation“ ir „Finance“ integravimo duomenų srautas](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="c0c22-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="c0c22-112">Projekto valandų įvertinimai</span><span class="sxs-lookup"><span data-stu-id="c0c22-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="c0c22-113">Šablonas ir užduotys</span><span class="sxs-lookup"><span data-stu-id="c0c22-113">Template and tasks</span></span>

<span data-ttu-id="c0c22-114">Norėdami pasiekti galimus šablonus, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai** , tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="c0c22-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="c0c22-115">Toliau pateikiamas šablonas ir pagrindinės užduotys naudojami norint sinchronizuoti projekto valandų įvertinimus iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c0c22-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c0c22-116">**Šablono pavadinimas pasirinkus duomenų integravimą:** projekto valandų įvertinimai (PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="c0c22-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c0c22-117">**Projekto užduočių pavadinimas:**</span><span class="sxs-lookup"><span data-stu-id="c0c22-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c0c22-118">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="c0c22-118">Transaction relationships</span></span>
    - <span data-ttu-id="c0c22-119">Išlaidų sąmatos</span><span class="sxs-lookup"><span data-stu-id="c0c22-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="c0c22-120">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="c0c22-120">Entity set</span></span>

| <span data-ttu-id="c0c22-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c0c22-121">Project Service Automation</span></span> | <span data-ttu-id="c0c22-122">Finansai</span><span class="sxs-lookup"><span data-stu-id="c0c22-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="c0c22-123">Projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="c0c22-123">Project tasks</span></span>              | <span data-ttu-id="c0c22-124">Projekto valandų įvertinimų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="c0c22-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="c0c22-125">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="c0c22-125">Entity flow</span></span>

<span data-ttu-id="c0c22-126">Projekto valandų įvertinimai valdomi naudojant „Project Service Automation“, o sinchronizuojami su „Finance“ kaip projekto valandų prognozės.</span><span class="sxs-lookup"><span data-stu-id="c0c22-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c0c22-127">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="c0c22-127">Prerequisites</span></span>

<span data-ttu-id="c0c22-128">Prieš atliekant projekto valandų įvertinimų sinchronizavimą, reikia sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="c0c22-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c0c22-129">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="c0c22-129">Power Query</span></span>

<span data-ttu-id="c0c22-130">Projekto valandų įvertinimo šablone turite naudoti „Microsoft Power Query for Excel”, kad atliktumėte tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="c0c22-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="c0c22-131">Nustatykite numatytojo prognozės modelio ID, kuris bus naudojamas, kai integruojant bus kuriamos naujos valandų prognozės.</span><span class="sxs-lookup"><span data-stu-id="c0c22-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="c0c22-132">Filtruokite visus konkretiems ištekliams būdingus užduoties įrašus, kuriuos nepavyks integruoti į valandų prognozes.</span><span class="sxs-lookup"><span data-stu-id="c0c22-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="c0c22-133">Filtruokite tuščias operacijų kategorijos eilutes.</span><span class="sxs-lookup"><span data-stu-id="c0c22-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="c0c22-134">Jei nepavyks atlikti šios užduoties, valandų prognozės gali būti netikslios.</span><span class="sxs-lookup"><span data-stu-id="c0c22-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="c0c22-135">Numatytojo prognozės modelio ID nustatymas</span><span class="sxs-lookup"><span data-stu-id="c0c22-135">Set the default forecast model ID</span></span>

<span data-ttu-id="c0c22-136">Norėdami šablone atnaujinti numatytojo prognozės modelio ID, spustelėkite **struktūros** rodyklę ir atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="c0c22-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c0c22-137">Tada pasirinkite saitą **Išplėstinė užklausa ir filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="c0c22-138">Jei naudojate numatytąjį projekto valandų įvertinimų šabloną (PSA į „Fin and Ops“), sąraše **Taikomi veiksmai** pažymėkite **Įtraukta sąlyga**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="c0c22-139">Įraše **Funkcija** pakeiskite **O\_prognozė** prognozės modelio ID pavadinimu, kuris turi būti naudojamas su šiuo integravimu.</span><span class="sxs-lookup"><span data-stu-id="c0c22-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="c0c22-140">Numatytajame šablone naudojamas demonstracinių duomenų prognozės modelio ID.</span><span class="sxs-lookup"><span data-stu-id="c0c22-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="c0c22-141">Jei kuriate naują šabloną, turite įtraukti šį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="c0c22-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="c0c22-142">„Power Query” pasirinkite **Įtraukti sąlygos stulpelį** ir įveskite naujo stulpelio pavadinimą, pvz., **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-142">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="c0c22-143">Įveskite stulpelio sąlygą, kur, jei projekto užduotis apibrėžta, tada \<enter the forecast model ID\>; kitu atveju neapibrėžta reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c0c22-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="c0c22-144">Filtruokite konkretiems ištekliams būdingus įrašus</span><span class="sxs-lookup"><span data-stu-id="c0c22-144">Filter out resource-specific records</span></span>

<span data-ttu-id="c0c22-145">Projekto valandų įvertinimų (PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuriuo pašalinami visi konkretiems ištekliams būdingi įrašai.</span><span class="sxs-lookup"><span data-stu-id="c0c22-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="c0c22-146">Kurdami savo šabloną, turite įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="c0c22-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="c0c22-147">Pasirinkite saitą **Išplėstinė užklausa ir filtravimas** , jei norite filtruoti stulpelį **msdyn\_islinetask** , kad būtų įtraukti tik **Klaidingi** įrašai.</span><span class="sxs-lookup"><span data-stu-id="c0c22-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="c0c22-148">Filtruokite tuščias operacijų kategorijos eilutes</span><span class="sxs-lookup"><span data-stu-id="c0c22-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="c0c22-149">Reikia įtraukti filtrą, kad būtų pašalintos visos eilutės, kuriose yra tuščių operacijų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="c0c22-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="c0c22-150">Ši užduotis yra privaloma, neatsižvelgiant į tai, ar naudojate numatytąjį šabloną, ar kuriate savo.</span><span class="sxs-lookup"><span data-stu-id="c0c22-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="c0c22-151">Šiuo filtru iš „Project Service Automation” pašalinamos visos suvestinių eilutes, dėl kurių valandų prognozės programoje „Finance” gali būti netikslios.</span><span class="sxs-lookup"><span data-stu-id="c0c22-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="c0c22-152">Pasirinkite saitą **Išplėstinė užklausa ir filtravimas** , kad filtruotumėte neapibrėžtų reikšmių įrašus stulpelyje **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c0c22-153">Šablonų susiejimas pasirinkus Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="c0c22-153">Template mapping in Data integration</span></span>

<span data-ttu-id="c0c22-154">Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="c0c22-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="c0c22-155">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c0c22-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c0c22-156">[![Šablono užduoties susiejimas duomenų integravime](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0c22-156">[![Template task mapping in data integration](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="c0c22-157">Projekto išlaidų įvertinimai</span><span class="sxs-lookup"><span data-stu-id="c0c22-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="c0c22-158">Šablonas ir užduotys</span><span class="sxs-lookup"><span data-stu-id="c0c22-158">Template and tasks</span></span>

<span data-ttu-id="c0c22-159">Toliau pateikiamas šablonas ir pagrindinės užduotys naudojami norint sinchronizuoti projekto išlaidų įvertinimus iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c0c22-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="c0c22-160">**Šablono pavadinimas pasirinkus duomenų integravimą:** projekto išlaidų įvertinimai (PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="c0c22-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="c0c22-161">**Projekto užduočių pavadinimas:**</span><span class="sxs-lookup"><span data-stu-id="c0c22-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="c0c22-162">Operacijų ryšiai</span><span class="sxs-lookup"><span data-stu-id="c0c22-162">Transaction relationships</span></span> 
    - <span data-ttu-id="c0c22-163">Išlaidų sąmatos</span><span class="sxs-lookup"><span data-stu-id="c0c22-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="c0c22-164">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="c0c22-164">Entity set</span></span>

| <span data-ttu-id="c0c22-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="c0c22-165">Project Service Automation</span></span> | <span data-ttu-id="c0c22-166">Finansai</span><span class="sxs-lookup"><span data-stu-id="c0c22-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="c0c22-167">Operacijos ryšiai</span><span class="sxs-lookup"><span data-stu-id="c0c22-167">Transaction Connections</span></span>    | <span data-ttu-id="c0c22-168">Projekto operacijų ryšių integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="c0c22-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="c0c22-169">Įvertinimo eilutės</span><span class="sxs-lookup"><span data-stu-id="c0c22-169">Estimate Lines</span></span>             | <span data-ttu-id="c0c22-170">Projekto išlaidų įvertinimų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="c0c22-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="c0c22-171">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="c0c22-171">Entity flow</span></span>

<span data-ttu-id="c0c22-172">Projekto išlaidų įvertinimai valdomi naudojant „Project Service Automation“, o sinchronizuojami su „Finance“ kaip projekto išlaidų prognozės.</span><span class="sxs-lookup"><span data-stu-id="c0c22-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="c0c22-173">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="c0c22-173">Prerequisites</span></span>

<span data-ttu-id="c0c22-174">Prieš atliekant projekto išlaidų įvertinimų sinchronizavimą, reikia sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.</span><span class="sxs-lookup"><span data-stu-id="c0c22-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="c0c22-175">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="c0c22-175">Power Query</span></span>

<span data-ttu-id="c0c22-176">Projekto išlaidų įvertinimo šablone turite naudoti „Power Query”, kad atliktumėte tolesnes užduotis.</span><span class="sxs-lookup"><span data-stu-id="c0c22-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="c0c22-177">Filtruokite, kad įtrauktumėte tik išlaidų įvertinimų eilučių įrašus.</span><span class="sxs-lookup"><span data-stu-id="c0c22-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="c0c22-178">Nustatykite numatytojo prognozės modelio ID, kuris bus naudojamas, kai integruojant bus kuriamos naujos valandų prognozės.</span><span class="sxs-lookup"><span data-stu-id="c0c22-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="c0c22-179">Atsiskaitymo tipų keitimas.</span><span class="sxs-lookup"><span data-stu-id="c0c22-179">Transform the billing types.</span></span>
- <span data-ttu-id="c0c22-180">Operacijų tipų keitimas.</span><span class="sxs-lookup"><span data-stu-id="c0c22-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="c0c22-181">Filtruokite, kad įtrauktumėte tik išlaidų įvertinimų eilutes</span><span class="sxs-lookup"><span data-stu-id="c0c22-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="c0c22-182">Projekto išlaidų įvertinimų (PSA į „Fin and Ops“) šablone yra numatytasis filtras, kuriuo į integravimą įtraukiamos tik išlaidų eilutės.</span><span class="sxs-lookup"><span data-stu-id="c0c22-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="c0c22-183">Kurdami savo šabloną, turite įtraukti šį filtrą.</span><span class="sxs-lookup"><span data-stu-id="c0c22-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="c0c22-184">Pasirinkite užduotį **Operacijų ryšiai** , tada spustelėkite **struktūros** rodyklę, kad atidarytumėte susiejimą.</span><span class="sxs-lookup"><span data-stu-id="c0c22-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c0c22-185">Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="c0c22-186">Filtruokite stulpelį **msdyn\_transactiontype1** , kad jame būtų tik **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="c0c22-187">Numatytojo prognozės modelio ID nustatymas</span><span class="sxs-lookup"><span data-stu-id="c0c22-187">Set the default forecast model ID</span></span>

<span data-ttu-id="c0c22-188">Norėdami šablone atnaujinti numatytojo prognozės modelio ID, pasirinkite užduotį **Išlaidų įvertinimai** , tada spustelėkite **struktūros** rodyklę ir atidarykite susiejimą.</span><span class="sxs-lookup"><span data-stu-id="c0c22-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="c0c22-189">Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="c0c22-190">Jei naudojate numatytąjį projekto išlaidų įvertinimų šabloną (PSA į „Fin and Ops“), „Power Query” skyriuje **Taikomi veiksmai** pasirinkite pirmą **įtrauktą sąlygą**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="c0c22-191">Įraše **Funkcija** pakeiskite **O\_prognozė** prognozės modelio ID pavadinimu, kuris turi būti naudojamas su šiuo integravimu.</span><span class="sxs-lookup"><span data-stu-id="c0c22-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="c0c22-192">Numatytajame šablone naudojamas demonstracinių duomenų prognozės modelio ID.</span><span class="sxs-lookup"><span data-stu-id="c0c22-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="c0c22-193">Jei kuriate naują šabloną, turite įtraukti šį stulpelį.</span><span class="sxs-lookup"><span data-stu-id="c0c22-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="c0c22-194">„Power Query” pasirinkite **Įtraukti sąlygos stulpelį** ir įveskite naujo stulpelio pavadinimą, pvz., **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-194">In Power Query, select **Add Conditional Column** , and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="c0c22-195">Įveskite stulpelio sąlygą, kur, jei įvertinimo eilutės ID apibrėžta, tada \<enter the forecast model ID\>; kitu atveju neapibrėžta reikšmė.</span><span class="sxs-lookup"><span data-stu-id="c0c22-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="c0c22-196">Atsiskaitymo tipų keitimas</span><span class="sxs-lookup"><span data-stu-id="c0c22-196">Transform the billing types</span></span>

<span data-ttu-id="c0c22-197">Projekto išlaidų įvertinimų (PSA į „Fin and Ops“) šablone yra sąlygos stulpelis, kuris yra naudojamas atsiskaitymo tipams, gaunamiems iš „Project Service Automation” integravimo metu, keisti.</span><span class="sxs-lookup"><span data-stu-id="c0c22-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="c0c22-198">Kurdami savo šabloną, turite įtraukti šį sąlygos stulpelį.</span><span class="sxs-lookup"><span data-stu-id="c0c22-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="c0c22-199">Pasirinkite saitą **Išplėstinė užklausa ir filtravimas** , tada pasirinkite **Įtraukti sąlygos stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="c0c22-200">Įveskite naujo stulpelio pavadinimą, pvz., **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="c0c22-201">Tada įveskite tolesnę sąlygą.</span><span class="sxs-lookup"><span data-stu-id="c0c22-201">Then enter the following condition:</span></span>

<span data-ttu-id="c0c22-202">Jei **msdyn\_billingtype** lygu 192350000, tada **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="c0c22-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="c0c22-203">Taip pat jei **msdyn\_billingtype** lygu 192350001, tada **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="c0c22-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="c0c22-204">Taip pat jei **msdyn\_billingtype** lygu 192350002, tada **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="c0c22-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="c0c22-205">kitaip **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="c0c22-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="c0c22-206">Operacijų tipų keitimas</span><span class="sxs-lookup"><span data-stu-id="c0c22-206">Transform the transaction types</span></span>

<span data-ttu-id="c0c22-207">Projekto išlaidų įvertinimų (PSA į „Fin and Ops“) šablone yra sąlygos stulpelis, kuris yra naudojamas operacijų tipams, gaunamiems iš „Project Service Automation” integravimo metu, keisti.</span><span class="sxs-lookup"><span data-stu-id="c0c22-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="c0c22-208">Kurdami savo šabloną, turite įtraukti šį sąlygos stulpelį.</span><span class="sxs-lookup"><span data-stu-id="c0c22-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="c0c22-209">Pasirinkite saitą **Išplėstinė užklausa ir filtravimas** , tada pasirinkite **Įtraukti sąlygos stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="c0c22-210">Įveskite naujo stulpelio pavadinimą, pvz., **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="c0c22-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="c0c22-211">Tada įveskite tolesnę sąlygą.</span><span class="sxs-lookup"><span data-stu-id="c0c22-211">Then enter the following condition:</span></span>

<span data-ttu-id="c0c22-212">Jei **msdyn\_transactiontypecode** lygu 192350000, tada **Cost**</span><span class="sxs-lookup"><span data-stu-id="c0c22-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="c0c22-213">Taip pat jei **msdyn\_transactiontypecode** lygu 192350005, tada **Sales**</span><span class="sxs-lookup"><span data-stu-id="c0c22-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="c0c22-214">kitaip **null**</span><span class="sxs-lookup"><span data-stu-id="c0c22-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="c0c22-215">Šablonų susiejimas pasirinkus Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="c0c22-215">Template mapping in Data integration</span></span>

<span data-ttu-id="c0c22-216">Šiose iliustracijose pateikiami duomenų integravimo šablonų užduočių susiejimų pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="c0c22-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="c0c22-217">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="c0c22-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="c0c22-218">[![Išlaidų įvertinimo operacijų šablono susiejimas](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0c22-218">[![Template mapping of expense estimate transactions](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="c0c22-219">[![Išlaidų įvertinimo šablono susiejimas](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="c0c22-219">[![Template mapping of expense estimates](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
