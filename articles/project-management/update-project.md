---
title: Naujinti projektą
description: Šioje temoje pateikta informacija apie „Project Operations“ projektų naujinimą.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 5c9cd0c7c6886bd454c5f2ef2ae7f20d1707293f
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080691"
---
# <a name="update-a-project"></a><span data-ttu-id="9ec5e-103">Naujinti projektą</span><span class="sxs-lookup"><span data-stu-id="9ec5e-103">Update a project</span></span>

<span data-ttu-id="9ec5e-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="9ec5e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9ec5e-105">Toliau pateikiama laukų, kuriuos galima atnaujinti projekte po to, kai jis buvo sukurtas, suvestinė ir bet kokios galimos naujinimų pasekmės.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="9ec5e-106">Projekto išsamios informacijos laukai</span><span class="sxs-lookup"><span data-stu-id="9ec5e-106">Project detail fields</span></span>

- <span data-ttu-id="9ec5e-107">**Pavadinimas** : projekto pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-107">**Name** : The title of the project.</span></span>
- <span data-ttu-id="9ec5e-108">**Aprašas** : projekto apžvalga.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-108">**Description** : An overview of the project.</span></span>
- <span data-ttu-id="9ec5e-109">**Klientas** : įmonė, kuriai daromas projektas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-109">**Customer** : The company the project will be delivered to.</span></span>
- <span data-ttu-id="9ec5e-110">**Kalendoriaus šablonas** : projekto darbo valandos.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-110">**Calendar template** : The working hours of the project.</span></span> <span data-ttu-id="9ec5e-111">Kai laukas pakeičiamas, perskaičiuojamas visas grafikas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="9ec5e-112">**Valiuta** : projekto valiuta.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-112">**Currency** : The currency for the project.</span></span> <span data-ttu-id="9ec5e-113">Šio lauko numatytosios reikšmės nustatomos pagal valiutą, apibrėžtą sutartį sudarančiame vienete.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="9ec5e-114">Atnaujinus sutartį sudarantį vienetą, laukas taip pat atnaujinamas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="9ec5e-115">**Sutartį sudarantis vienetas** : organizacinis vienetas, atstovaujantis įmonių grupę arba padalinį, kuris yra atsakingas už laimėtą pardavimą ir darbo bei paslaugų pristatymą klientui.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-115">**Contracting Unit** : The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="9ec5e-116">**Projekto vadovas** : projekto komandos narys, turintis įgaliojimus peržiūrėti ir patvirtinti laiko įrašus ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-116">**Project Manager** : The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="9ec5e-117">Įvertinimo laukai</span><span class="sxs-lookup"><span data-stu-id="9ec5e-117">Estimate fields</span></span>

- <span data-ttu-id="9ec5e-118">**Numatoma pradžios data** : data, kada prasidės projektas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-118">**Estimated Start Date** : The date that the project will begin.</span></span> <span data-ttu-id="9ec5e-119">Atnaujinus šį lauką, bet kokios projekto užduotys bus proporcingai atnaujintos atsižvelgiant į naują pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="9ec5e-120">**Pabaigos data** : numatyta projekto pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-120">**Finish Date** : The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="9ec5e-121">**Pastangos** : numatytos projekto pastangos.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-121">**Effort** : The estimated effort of the project.</span></span> <span data-ttu-id="9ec5e-122">Kai užduotys įtraukiamos į projektą, šis laukas neberedaguojamas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="9ec5e-123">**Įvertintos darbo sąnaudos** : įvertintos projekto darbo sąnaudos.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-123">**Estimated Labor Cost** : The estimated labor cost of the project.</span></span> <span data-ttu-id="9ec5e-124">Kai darbo sąnaudos įtraukiamos į projektą, šis laukas neberedaguojamas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="9ec5e-125">**Numatomos išlaidos** : numatomos projekto išlaidos.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-125">**Estimated Expenses** : The estimated expenses of the project.</span></span> <span data-ttu-id="9ec5e-126">Kai išlaidos įtraukiamos į projektą, šis laukas neberedaguojamas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="9ec5e-127">Projekto faktinių duomenų laukai</span><span class="sxs-lookup"><span data-stu-id="9ec5e-127">Project actual fields</span></span>
- <span data-ttu-id="9ec5e-128">**Faktinė pradžia** : data, kada prasidėjo projektas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-128">**Actual Start** : The date that the project started.</span></span>
- <span data-ttu-id="9ec5e-129">**Faktinė pabaiga** : laukas atnaujinamas baigus projektą.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-129">**Actual Finish** : To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="9ec5e-130">Projekto būsenos laukai</span><span class="sxs-lookup"><span data-stu-id="9ec5e-130">Project status fields</span></span>

- <span data-ttu-id="9ec5e-131">**Bendroji projekto būsena** : bendroji projekto būsena, kurią pateikia projekto vadovas.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-131">**Overall Project Status** : The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="9ec5e-132">**Komentarai** : projekto vadovo pastabos apie esamą projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="9ec5e-132">**Comments** : A narrative regarding the current health of the project provided by the Project manager.</span></span>

