---
title: Naujinti projektą
description: Šioje temoje pateikta informacija apie „Project Operations“ projektų naujinimą.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27444b072bdf7de55d6b38c30c1ea5fe66ed46ac
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286393"
---
# <a name="update-a-project"></a><span data-ttu-id="eb308-103">Naujinti projektą</span><span class="sxs-lookup"><span data-stu-id="eb308-103">Update a project</span></span>

<span data-ttu-id="eb308-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="eb308-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="eb308-105">Toliau pateikiama laukų, kuriuos galima atnaujinti projekte po to, kai jis buvo sukurtas, suvestinė ir bet kokios galimos naujinimų pasekmės.</span><span class="sxs-lookup"><span data-stu-id="eb308-105">Below is a summary of the fields that can be updated on a project after it has been created and any applicable implications of the updates.</span></span>

## <a name="project-detail-fields"></a><span data-ttu-id="eb308-106">Projekto išsamios informacijos laukai</span><span class="sxs-lookup"><span data-stu-id="eb308-106">Project detail fields</span></span>

- <span data-ttu-id="eb308-107">**Pavadinimas**: projekto pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="eb308-107">**Name**: The title of the project.</span></span>
- <span data-ttu-id="eb308-108">**Aprašas**: projekto apžvalga.</span><span class="sxs-lookup"><span data-stu-id="eb308-108">**Description**: An overview of the project.</span></span>
- <span data-ttu-id="eb308-109">**Klientas**: įmonė, kuriai daromas projektas.</span><span class="sxs-lookup"><span data-stu-id="eb308-109">**Customer**: The company the project will be delivered to.</span></span>
- <span data-ttu-id="eb308-110">**Kalendoriaus šablonas**: projekto darbo valandos.</span><span class="sxs-lookup"><span data-stu-id="eb308-110">**Calendar template**: The working hours of the project.</span></span> <span data-ttu-id="eb308-111">Kai laukas pakeičiamas, perskaičiuojamas visas grafikas.</span><span class="sxs-lookup"><span data-stu-id="eb308-111">When the field is changed, the entire schedule is recalculated.</span></span>
- <span data-ttu-id="eb308-112">**Valiuta**: projekto valiuta.</span><span class="sxs-lookup"><span data-stu-id="eb308-112">**Currency**: The currency for the project.</span></span> <span data-ttu-id="eb308-113">Šio lauko numatytosios reikšmės nustatomos pagal valiutą, apibrėžtą sutartį sudarančiame vienete.</span><span class="sxs-lookup"><span data-stu-id="eb308-113">This field defaults based on the currency defined in the contracting unit.</span></span> <span data-ttu-id="eb308-114">Atnaujinus sutartį sudarantį vienetą, laukas taip pat atnaujinamas.</span><span class="sxs-lookup"><span data-stu-id="eb308-114">When the contracting unit is updated, the field is also updated.</span></span>
- <span data-ttu-id="eb308-115">**Sutartį sudarantis vienetas**: organizacinis vienetas, atstovaujantis įmonių grupę arba padalinį, kuris yra atsakingas už laimėtą pardavimą ir darbo bei paslaugų pristatymą klientui.</span><span class="sxs-lookup"><span data-stu-id="eb308-115">**Contracting Unit**: The organizational unit that represents the company group or division that is primarily responsible for winning the sale and managing the delivery of work and services to the customer.</span></span> 
- <span data-ttu-id="eb308-116">**Projekto vadovas**: projekto komandos narys, turintis įgaliojimus peržiūrėti ir patvirtinti laiko įrašus ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="eb308-116">**Project Manager**: The project team member who has the authority to review and approve time entries and expenses.</span></span>

## <a name="estimate-fields"></a><span data-ttu-id="eb308-117">Įvertinimo laukai</span><span class="sxs-lookup"><span data-stu-id="eb308-117">Estimate fields</span></span>

- <span data-ttu-id="eb308-118">**Numatoma pradžios data**: data, kada prasidės projektas.</span><span class="sxs-lookup"><span data-stu-id="eb308-118">**Estimated Start Date**: The date that the project will begin.</span></span> <span data-ttu-id="eb308-119">Atnaujinus šį lauką, bet kokios projekto užduotys bus proporcingai atnaujintos atsižvelgiant į naują pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="eb308-119">When this field is updated, any tasks on the project will move proportionately with the start new start date.</span></span>
- <span data-ttu-id="eb308-120">**Pabaigos data**: numatyta projekto pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="eb308-120">**Finish Date**: The date that the project is scheduled to end.</span></span>
- <span data-ttu-id="eb308-121">**Pastangos**: numatytos projekto pastangos.</span><span class="sxs-lookup"><span data-stu-id="eb308-121">**Effort**: The estimated effort of the project.</span></span> <span data-ttu-id="eb308-122">Kai užduotys įtraukiamos į projektą, šis laukas neberedaguojamas.</span><span class="sxs-lookup"><span data-stu-id="eb308-122">When tasks are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="eb308-123">**Įvertintos darbo sąnaudos**: įvertintos projekto darbo sąnaudos.</span><span class="sxs-lookup"><span data-stu-id="eb308-123">**Estimated Labor Cost**: The estimated labor cost of the project.</span></span> <span data-ttu-id="eb308-124">Kai darbo sąnaudos įtraukiamos į projektą, šis laukas neberedaguojamas.</span><span class="sxs-lookup"><span data-stu-id="eb308-124">When labor costs are added to the project, this field is no longer editable.</span></span>
- <span data-ttu-id="eb308-125">**Numatomos išlaidos**: numatomos projekto išlaidos.</span><span class="sxs-lookup"><span data-stu-id="eb308-125">**Estimated Expenses**: The estimated expenses of the project.</span></span> <span data-ttu-id="eb308-126">Kai išlaidos įtraukiamos į projektą, šis laukas neberedaguojamas.</span><span class="sxs-lookup"><span data-stu-id="eb308-126">When expenses are added to the project, this field is no longer editable.</span></span>

## <a name="project-actual-fields"></a><span data-ttu-id="eb308-127">Projekto faktinių duomenų laukai</span><span class="sxs-lookup"><span data-stu-id="eb308-127">Project actual fields</span></span>
- <span data-ttu-id="eb308-128">**Faktinė pradžia**: data, kada prasidėjo projektas.</span><span class="sxs-lookup"><span data-stu-id="eb308-128">**Actual Start**: The date that the project started.</span></span>
- <span data-ttu-id="eb308-129">**Faktinė pabaiga**: laukas atnaujinamas baigus projektą.</span><span class="sxs-lookup"><span data-stu-id="eb308-129">**Actual Finish**: To be updated when a project has been completed.</span></span>

## <a name="project-status-fields"></a><span data-ttu-id="eb308-130">Projekto būsenos laukai</span><span class="sxs-lookup"><span data-stu-id="eb308-130">Project status fields</span></span>

- <span data-ttu-id="eb308-131">**Bendroji projekto būsena**: bendroji projekto būsena, kurią pateikia projekto vadovas.</span><span class="sxs-lookup"><span data-stu-id="eb308-131">**Overall Project Status**: The overall project health provided by the Project manager.</span></span>
- <span data-ttu-id="eb308-132">**Komentarai**: projekto vadovo pastabos apie esamą projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="eb308-132">**Comments**: A narrative regarding the current health of the project provided by the Project manager.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]