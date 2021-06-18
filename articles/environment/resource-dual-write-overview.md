---
title: „Project Operations“ dvigubo rašymo integravimas
description: Šioje temoje apžvelgiamas „Project Operations“ dvigubo rašymo integravimas.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ce4f7bf8185e6f3f942df14d30d7b8d0a3e4444a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998691"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="68707-103">„Project Operations“ dvigubo rašymo integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="68707-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="68707-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="68707-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="68707-105">„Project Operations“ naudoja [dvigubo rašymo galimybes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) duomenims tarp „Microsoft Dataverse“ ir „Dynamics 365 Finance“ sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="68707-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="68707-106">Toliau pateiktoje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami atliekant šį „Dataverse“ ir „Finance“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="68707-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![„Project Operations“ duomenų srautų apžvalga](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="68707-108">„Project Operations“ naudojant „Dataverse“ suteikia modernią vartotojo sąsają (UI) ir lengvo išplėtimo galimybę nenaudojant kodo / naudojant nedaug kodo ir taikant „Power Platform“ galimybes.</span><span class="sxs-lookup"><span data-stu-id="68707-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="68707-109">Pasitelkę „Project Operations“ naudodami „Dataverse“, savo veiklą vykdo projektų vadovai, išteklių vadovai, projekto komandų nariai ir kiti vadovaujantieji asmenys.</span><span class="sxs-lookup"><span data-stu-id="68707-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="68707-110">„Project Operations“ naudojant „Finance“ palaiko projektų apskaitos ir pajamų pripažinimo galimybę.</span><span class="sxs-lookup"><span data-stu-id="68707-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="68707-111">„Project Operations“ papildo „Finance“ finansinę sistemą, kad būtų galima apskaičiuoti PVM, valiutos kursus, teikti finansinių išlaidų ataskaitas ir kt.</span><span class="sxs-lookup"><span data-stu-id="68707-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="68707-112">Projektų buhalterių funkcijos daugiausia pagrįstos sprendimu „Finance“.</span><span class="sxs-lookup"><span data-stu-id="68707-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="68707-113">„Project Operations“ integravimą sudaro toliau nurodytų komponentų integravimas.</span><span class="sxs-lookup"><span data-stu-id="68707-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="68707-114">„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="68707-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="68707-115">Projektų įvertinimai ir faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="68707-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="68707-116">Projektų sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="68707-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="68707-117">Išlaidų valdymas</span><span class="sxs-lookup"><span data-stu-id="68707-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="68707-118">Tiekėjo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="68707-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
