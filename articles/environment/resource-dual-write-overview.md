---
title: „Project Operations“ dvigubo rašymo integravimas
description: Šioje temoje apžvelgiamas „Project Operations“ dvigubo rašymo integravimas.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955668"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="80ec1-103">„Project Operations“ dvigubo rašymo integravimo apžvalga</span><span class="sxs-lookup"><span data-stu-id="80ec1-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="80ec1-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="80ec1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="80ec1-105">„Project Operations“ naudoja [dvigubo rašymo galimybes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) duomenims tarp „Microsoft Dataverse“ ir „Dynamics 365 Finance“ sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="80ec1-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="80ec1-106">Toliau pateiktoje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami atliekant šį „Dataverse“ ir „Finance“ integravimą.</span><span class="sxs-lookup"><span data-stu-id="80ec1-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![„Project Operations“ duomenų srautų apžvalga](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="80ec1-108">„Project Operations“ naudojant „Dataverse“ suteikia modernią vartotojo sąsają (UI) ir lengvo išplėtimo galimybę nenaudojant kodo / naudojant nedaug kodo ir taikant „Power Platform“ galimybes.</span><span class="sxs-lookup"><span data-stu-id="80ec1-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="80ec1-109">Pasitelkę „Project Operations“ naudodami „Dataverse“, savo veiklą vykdo projektų vadovai, išteklių vadovai, projekto komandų nariai ir kiti vadovaujantieji asmenys.</span><span class="sxs-lookup"><span data-stu-id="80ec1-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="80ec1-110">„Project Operations“ naudojant „Finance“ palaiko projektų apskaitos ir pajamų pripažinimo galimybę.</span><span class="sxs-lookup"><span data-stu-id="80ec1-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="80ec1-111">„Project Operations“ papildo „Finance“ finansinę sistemą, kad būtų galima apskaičiuoti PVM, valiutos kursus, teikti finansinių išlaidų ataskaitas ir kt.</span><span class="sxs-lookup"><span data-stu-id="80ec1-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="80ec1-112">Projektų buhalterių funkcijos daugiausia pagrįstos sprendimu „Finance“.</span><span class="sxs-lookup"><span data-stu-id="80ec1-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="80ec1-113">„Project Operations“ integravimą sudaro toliau nurodytų komponentų integravimas.</span><span class="sxs-lookup"><span data-stu-id="80ec1-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="80ec1-114">„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas</span><span class="sxs-lookup"><span data-stu-id="80ec1-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="80ec1-115">Projektų įvertinimai ir faktiniai duomenys</span><span class="sxs-lookup"><span data-stu-id="80ec1-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="80ec1-116">Projektų sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="80ec1-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="80ec1-117">Išlaidų valdymas</span><span class="sxs-lookup"><span data-stu-id="80ec1-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="80ec1-118">Tiekėjo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="80ec1-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
