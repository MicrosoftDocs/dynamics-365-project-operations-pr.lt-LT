---
title: Projekto išlaidų kategorijų sinchronizavimas tarp „Finance and Operations“ ir „Project Service Automation“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurios naudojami norint sinchronizuoti projekto išlaidų kategorijas tarp „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080975"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="e70da-103">Projekto išlaidų kategorijų sinchronizavimas tarp „Finance and Operations“ ir „Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="e70da-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e70da-104">Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurios naudojami norint sinchronizuoti projekto išlaidų kategorijas tarp „Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="e70da-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Dynamics 365 Finance and Dynamics 365 Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="e70da-105">Projekto užduočių integravimas, išlaidų operacijų kategorijos, valandų įvertinimas, išlaidų įvertinimas ir funkcijų blokavimas prieinami 8.0 versijoje.</span><span class="sxs-lookup"><span data-stu-id="e70da-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in version 8.0.</span></span>
> - <span data-ttu-id="e70da-106">Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.</span><span class="sxs-lookup"><span data-stu-id="e70da-106">Actuals integration is available in version 8.0.1 or later.</span></span>
> - <span data-ttu-id="e70da-107">Jei naudojate „Enterprise Edition“ 7.3.0, įdiegę KB 4132657 ir KB 4132660, galėsite naudoti šablonus projektų užduotims, išlaidų operacijų kategorijoms, valandų įvertinimui, išlaidų įvertinimui ir faktiniams duomenims integruoti bei funkcijų blokavimui konfigūruoti.</span><span class="sxs-lookup"><span data-stu-id="e70da-107">If you're using Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="e70da-108">Jei reikia iš naujo nustatyti apskaitos paskirstymą, rekomenduojame įdiegti ir KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="e70da-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance"></a><span data-ttu-id="e70da-109">Duomenų srautas iš „Project Service Automation“ ir „Finance“</span><span class="sxs-lookup"><span data-stu-id="e70da-109">Data flow for Project Service Automation and Finance</span></span>

<span data-ttu-id="e70da-110">Naudojant „Project Service Automation“ ir „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose.</span><span class="sxs-lookup"><span data-stu-id="e70da-110">The Project Service Automation and Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="e70da-111">Integravimo šablonai, kuriuos galima naudoti su duomenų integravimo funkcija, įjungia duomenų srautą apie projekto išlaidų operacijų kategorijas tarp „Project Service Automation“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Project Service Automation.</span></span>

<span data-ttu-id="e70da-112">Jei projekto išlaidų kategorijos valdomos „Finance“, integravimo srautas pirmiausia vyksta iš „Finance“ į „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="e70da-112">If the project expense categories are mastered in Finance, the integration flow is first from Finance to Project Service Automation.</span></span> <span data-ttu-id="e70da-113">Projekto išlaidų kategorijų integravimo ID atnaujinami sinchronizuojant iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e70da-114">Jei projekto išlaidų kategorijos valdomos „Project Service Automation“, integravimo srautas pirmiausia vyksta iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance.</span></span> <span data-ttu-id="e70da-115">Prieš sinchronizuojant iš „Project Service Automation“ projektų kategorijos jau turi būti sukonfigūruotos „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-115">The project categories must already be configured in Finance before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="e70da-116">Tada sinchronizuokite iš „Finance“ atgal į „Project Service Automation“, o tada – vėl iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-116">Then synchronize from Finance back to Project Service Automation, and then from Project Service Automation to Finance again.</span></span> <span data-ttu-id="e70da-117">Tokiu būdu padėsite užtikrinti, kad kategorijos būtų susietos ir kad nebūtų sukurta jokių dublikatų.</span><span class="sxs-lookup"><span data-stu-id="e70da-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="e70da-118">Paprastai, projekto išlaidų kategorijos valdomos „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-118">Typically, the project expense categories are mastered in Finance.</span></span> <span data-ttu-id="e70da-119">Tačiau, jei jų nėra arba jei išlaidų kategorijos jau buvo sukurtos „Project Service Automation“, pirmiausia turite sinchronizuoti naudodami projekto išlaidų operacijų kategorijų (PSA į „Fin and Ops“) šabloną.</span><span class="sxs-lookup"><span data-stu-id="e70da-119">However, if they aren't, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="e70da-120">Tada sinchronizuokite naudodami projekto išlaidų operacijų kategorijų („Fin and Ops“ į PSA) šabloną.</span><span class="sxs-lookup"><span data-stu-id="e70da-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="e70da-121">Tada turėtumėte dar kartą sinchronizuoti iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-121">You should then run the synchronization from Project Service Automation to Finance one more time.</span></span>
>
> <span data-ttu-id="e70da-122">Jei pirmą kartą sinchronizuojate iš „Project Service Automation“, prieš paleisdami sinchronizavimą turite atitikti tolesnius „Finance“ reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="e70da-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance before the synchronization is run:</span></span>
>
> - <span data-ttu-id="e70da-123">„Project Service Automation“ turi būti bendrai naudojama kategorija, kuri atitinka projekto kategoriją, ir ji turi būti įjungta tiek **Projektas** , tiek **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="e70da-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="e70da-124">Kiekvienas „Finance“ juridinis subjektas, su kuriuo turi būti integruota, turi turėti tolesnes kategorijas.</span><span class="sxs-lookup"><span data-stu-id="e70da-124">For each Finance legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="e70da-125">**Projekto kategorija** yra.</span><span class="sxs-lookup"><span data-stu-id="e70da-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="e70da-126">**Naudoti išlaidose** įjungta.</span><span class="sxs-lookup"><span data-stu-id="e70da-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="e70da-127">**Aktyvu žurnale** įgalinta.</span><span class="sxs-lookup"><span data-stu-id="e70da-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="e70da-128">**Operacijos tipas** nustatytas kaip **Išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="e70da-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="e70da-129">Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="e70da-130">[![„Project Service Automation“ ir „Finance“ integravimo duomenų srautas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="e70da-130">[![Data flow for Project Service Automation integration with Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a><span data-ttu-id="e70da-131">Projekto išlaidų kategorijos sinchronizavimas iš „Finance“ į „Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="e70da-131">Project expense category synchronization from Finance to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="e70da-132">Šablonas ir užduotis</span><span class="sxs-lookup"><span data-stu-id="e70da-132">Template and task</span></span>

<span data-ttu-id="e70da-133">Norėdami pasiekti šabloną, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai** , tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.</span><span class="sxs-lookup"><span data-stu-id="e70da-133">To access the template, in the Microsoft Power Apps admin center, select **Projects** , and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="e70da-134">Toliau pateikiamas šablonas ir pagrindinė užduotis naudojami norint sinchronizuoti projekto išlaidų kategorijas iš „Finance“ į „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="e70da-134">The following template and underlying task are used to synchronize project expense categories from Finance to Project Service Automation:</span></span>

- <span data-ttu-id="e70da-135">**Šablono pavadinimas pasirinkus duomenų integravimą:** projekto išlaidų operacijų kategorijos („Fin and Ops“ į PSA)</span><span class="sxs-lookup"><span data-stu-id="e70da-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="e70da-136">**Užduoties pavadinimas projekte:** kategorijų sinchronizavimas į PSA</span><span class="sxs-lookup"><span data-stu-id="e70da-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="e70da-137">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="e70da-137">Entity set</span></span>

| <span data-ttu-id="e70da-138">Finansai</span><span class="sxs-lookup"><span data-stu-id="e70da-138">Finance</span></span>                           | <span data-ttu-id="e70da-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e70da-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="e70da-140">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="e70da-140">Integration entity for categories</span></span> | <span data-ttu-id="e70da-141">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="e70da-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="e70da-142">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="e70da-142">Entity flow</span></span>

<span data-ttu-id="e70da-143">Projekto išlaidų kategorijos valdomos naudojant „Finance, o sinchronizuojamos su „Project Service Automation“ kaip operacijų kategorijos.</span><span class="sxs-lookup"><span data-stu-id="e70da-143">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="e70da-144">„Power Query“</span><span class="sxs-lookup"><span data-stu-id="e70da-144">Power Query</span></span>

<span data-ttu-id="e70da-145">Kai sinchronizuojate į „Project Service Automation“, turite naudoti „ Microsoft Power Query for Excel“, kad nustatytumėte atsiskaitymo tipą transakcijos kategorijoje.</span><span class="sxs-lookup"><span data-stu-id="e70da-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="e70da-146">Projekto išlaidų operacijų kategorijų („Fin and Ops“ į PSA) šablonas pateikia numatytąjį stulpelį ir susiejimą.</span><span class="sxs-lookup"><span data-stu-id="e70da-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="e70da-147">Kurdami savo šabloną, turite įtraukti sąlygos stulpelį į „Power Query“.</span><span class="sxs-lookup"><span data-stu-id="e70da-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="e70da-148">Atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="e70da-148">Follow these steps.</span></span>

1. <span data-ttu-id="e70da-149">Spustelėkite rodyklę, kad atidarytumėte projekto išlaidų kategorijų užduoties susiejimą projekto išlaidų operacijų kategorijų („Fin and Ops“ į PSA) šablone.</span><span class="sxs-lookup"><span data-stu-id="e70da-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="e70da-150">Spustelėkite saitą **Išankstinės užklausos ir filtravimas** , kad atidarytumėte „Power Query“.</span><span class="sxs-lookup"><span data-stu-id="e70da-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="e70da-151">Pažymėkite **Įtraukti sąlyginį stulpelį**.</span><span class="sxs-lookup"><span data-stu-id="e70da-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="e70da-152">Įveskite naujo stulpelio pavadinimą, pvz., **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="e70da-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="e70da-153">Įveskite šią sąlygą: **Jei CATEGORYID nėra lygi nuliui, tada 19235001, kitaip nulis**.</span><span class="sxs-lookup"><span data-stu-id="e70da-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="e70da-154">Stulpelyje spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="e70da-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="e70da-155">Įsitikinkite, kad susiejote šį naują stulpelį susiejimo puslapyje.</span><span class="sxs-lookup"><span data-stu-id="e70da-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="e70da-156">Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e70da-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="e70da-157">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Finance“ į „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="e70da-157">The mapping shows the field information that will be synchronized from Finance to Project Service Automation.</span></span>

<span data-ttu-id="e70da-158">[![Projekto išlaidų kategorijos ir „Project Service Automation“ šablonų susiejimas](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e70da-158">[![Project expense category to Project Service Automation template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a><span data-ttu-id="e70da-159">Projekto išlaidų kategorijos sinchronizavimas iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-159">Project expense category synchronization from Project Service Automation to Finance</span></span>

### <a name="template-and-task"></a><span data-ttu-id="e70da-160">Šablonas ir užduotis</span><span class="sxs-lookup"><span data-stu-id="e70da-160">Template and task</span></span>

<span data-ttu-id="e70da-161">Toliau pateikiamas šablonas ir pagrindinė užduotis naudojami norint sinchronizuoti projekto išlaidų kategorijas iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="e70da-162">**Šablono pavadinimas pasirinkus duomenų integravimą:** projekto išlaidų operacijų kategorijos (PSA į „Fin and Ops“)</span><span class="sxs-lookup"><span data-stu-id="e70da-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="e70da-163">**Užduoties pavadinimas projekte:** kategorijų sinchronizavimas į „Fin Ops“</span><span class="sxs-lookup"><span data-stu-id="e70da-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="e70da-164">Objektų rinkinys</span><span class="sxs-lookup"><span data-stu-id="e70da-164">Entity set</span></span>

| <span data-ttu-id="e70da-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="e70da-165">Project Service Automation</span></span> | <span data-ttu-id="e70da-166">Finansai</span><span class="sxs-lookup"><span data-stu-id="e70da-166">Finance</span></span>                           |
|----------------------------|-----------------------------------|
| <span data-ttu-id="e70da-167">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="e70da-167">Transaction categories</span></span>     | <span data-ttu-id="e70da-168">Kategorijų integravimo objektas</span><span class="sxs-lookup"><span data-stu-id="e70da-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="e70da-169">Objekto srautas</span><span class="sxs-lookup"><span data-stu-id="e70da-169">Entity flow</span></span>

<span data-ttu-id="e70da-170">Projekto išlaidų kategorijos valdomos naudojant „Finance, o sinchronizuojamos su „Project Service Automation“ kaip operacijų kategorijos.</span><span class="sxs-lookup"><span data-stu-id="e70da-170">Project expense categories are managed in Finance, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="e70da-171">Sinchronizavimas atgal į „Finance“ atnaujina projekto kategoriją „Finance“ suteikdamas integravimo ID iš „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="e70da-171">The synchronization back to Finance updates the project category in Finance with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="e70da-172">Šablonų susiejimas pasirinkus Duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="e70da-172">Template mapping in Data integration</span></span>

<span data-ttu-id="e70da-173">Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimo pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="e70da-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="e70da-174">Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.</span><span class="sxs-lookup"><span data-stu-id="e70da-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="e70da-175">[![„Project Service Automation“ ir „Finance“ šablonų susiejimas](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="e70da-175">[![Project Service Automation to Finance template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
