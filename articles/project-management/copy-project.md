---
title: Kopijuoti projektą
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Operations“ projektų kopijavimą.
author: ruhercul
ms.date: 05/21/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c3055ab5b8c07faa2bc9167956d283e2a66029dd
ms.sourcegitcommit: 173f2b1f4e063c440a5f78d76d456c62aadbd89e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/24/2021
ms.locfileid: "6091264"
---
# <a name="copy-a-project"></a><span data-ttu-id="8fb03-103">Projekto kopijavimas</span><span class="sxs-lookup"><span data-stu-id="8fb03-103">Copy a project</span></span>

<span data-ttu-id="8fb03-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="8fb03-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8fb03-105">Naudodami „Dynamics 365 Project Operations“ galite greitai kurti naujus projektus formoje **Projektai** pasirinkdami **Kopijuoti projektą**.</span><span class="sxs-lookup"><span data-stu-id="8fb03-105">With Dynamics 365 Project Operations, you can quickly build new projects by selecting **Copy Project** on the **Projects** form.</span></span> <span data-ttu-id="8fb03-106">Jei norite kopijuoti projektą, atidarykite norimą kopijuoti projektą ir pasirinkite **Kopijuoti projektą**.</span><span class="sxs-lookup"><span data-stu-id="8fb03-106">To copy a project, open the project you want to copy, and then select **Copy project**.</span></span> <span data-ttu-id="8fb03-107">Veiksmas nukopijuos šiuos duomenis:</span><span class="sxs-lookup"><span data-stu-id="8fb03-107">The action will copy the following:</span></span>

- <span data-ttu-id="8fb03-108">Projekto ypatybes</span><span class="sxs-lookup"><span data-stu-id="8fb03-108">Project properties</span></span> 
- <span data-ttu-id="8fb03-109">Darbo paskirstymo struktūra</span><span class="sxs-lookup"><span data-stu-id="8fb03-109">Work breakdown structure</span></span>
- <span data-ttu-id="8fb03-110">Projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="8fb03-110">Project team members</span></span>
- <span data-ttu-id="8fb03-111">Projekto įvertinimai</span><span class="sxs-lookup"><span data-stu-id="8fb03-111">Project estimates</span></span>
- <span data-ttu-id="8fb03-112">Projekto išlaidų įvertinimai</span><span class="sxs-lookup"><span data-stu-id="8fb03-112">Project expense estimates</span></span>
- <span data-ttu-id="8fb03-113">Projekto medžiagų įvertinimai</span><span class="sxs-lookup"><span data-stu-id="8fb03-113">Project material estimates</span></span>

## <a name="project-properties"></a><span data-ttu-id="8fb03-114">Projekto ypatybes</span><span class="sxs-lookup"><span data-stu-id="8fb03-114">Project properties</span></span>

<span data-ttu-id="8fb03-115">Kai projektas kopijuojamas, kopijuojamos šių laukų reikšmės:</span><span class="sxs-lookup"><span data-stu-id="8fb03-115">When the project is copied, the values in the following fields are copied:</span></span>

- <span data-ttu-id="8fb03-116">Pavadinimas / vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="8fb03-116">Name</span></span>
- <span data-ttu-id="8fb03-117">Aprašo</span><span class="sxs-lookup"><span data-stu-id="8fb03-117">Description</span></span>
- <span data-ttu-id="8fb03-118">Klientas</span><span class="sxs-lookup"><span data-stu-id="8fb03-118">Customer</span></span>
- <span data-ttu-id="8fb03-119">Kalendoriaus šablonas</span><span class="sxs-lookup"><span data-stu-id="8fb03-119">Calendar Template</span></span>
- <span data-ttu-id="8fb03-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="8fb03-120">Currency</span></span>
- <span data-ttu-id="8fb03-121">Sutartį sudarantis vienetas</span><span class="sxs-lookup"><span data-stu-id="8fb03-121">Contracting Unit</span></span>
- <span data-ttu-id="8fb03-122">Projekto vadovas</span><span class="sxs-lookup"><span data-stu-id="8fb03-122">Project Manager</span></span>
- <span data-ttu-id="8fb03-123">Būsena</span><span class="sxs-lookup"><span data-stu-id="8fb03-123">Status</span></span>
- <span data-ttu-id="8fb03-124">Bendroji projekto būsena</span><span class="sxs-lookup"><span data-stu-id="8fb03-124">Overall Project Status</span></span>
- <span data-ttu-id="8fb03-125">Komentarai</span><span class="sxs-lookup"><span data-stu-id="8fb03-125">Comments</span></span>
- <span data-ttu-id="8fb03-126">Įvertinimai</span><span class="sxs-lookup"><span data-stu-id="8fb03-126">Estimates</span></span>
- <span data-ttu-id="8fb03-127">Numatoma pradžios data: tai yra data, kai projektas kuriamas iš kopijos.</span><span class="sxs-lookup"><span data-stu-id="8fb03-127">Estimated Start Date: This is the date that the project is created from the copy.</span></span>
- <span data-ttu-id="8fb03-128">Numatoma pabaigos data: ši data tikslinama pagal naujo projekto, sukurto iš kopijos, pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="8fb03-128">Estimated Finish Date: This date is adjusted based on the start date of the new project that was made from the copy.</span></span>
- <span data-ttu-id="8fb03-129">Pastangos (valandos)</span><span class="sxs-lookup"><span data-stu-id="8fb03-129">Effort (Hours)</span></span>
- <span data-ttu-id="8fb03-130">Įvertintos darbo sąnaudos</span><span class="sxs-lookup"><span data-stu-id="8fb03-130">Estimated Labor Cost</span></span>
- <span data-ttu-id="8fb03-131">Įvertinta išlaidų savikaina</span><span class="sxs-lookup"><span data-stu-id="8fb03-131">Estimated Expense Cost</span></span>
- <span data-ttu-id="8fb03-132">Įvertinta medžiagos savikaina</span><span class="sxs-lookup"><span data-stu-id="8fb03-132">Estimated Material Cost</span></span>

> [!NOTE]
> <span data-ttu-id="8fb03-133">Projekto kopijavimas yra ilgo veikimo operacija.</span><span class="sxs-lookup"><span data-stu-id="8fb03-133">Copy project is a long running operation.</span></span> <span data-ttu-id="8fb03-134">Nukopijuojami projekto įrašai, jų atitinkami atributai ir daug susijusių objektų.</span><span class="sxs-lookup"><span data-stu-id="8fb03-134">Project records, their relevant attributes, and many related entities are also copied.</span></span> <span data-ttu-id="8fb03-135">Dėl ilgo operacijos veikimo pobūdžio, paleidus kopijavimą paskirties projekto puslapis užrakinamas ir jo redaguoti negalima, kol atliekama kopijavimo operacija.</span><span class="sxs-lookup"><span data-stu-id="8fb03-135">Because of the long running nature of the operation, after the copy starts, the target project page is locked for editing until the copy operation is complete.</span></span>

## <a name="work-breakdown-structure"></a><span data-ttu-id="8fb03-136">Darbo paskirstymo struktūra</span><span class="sxs-lookup"><span data-stu-id="8fb03-136">Work breakdown structure</span></span>

<span data-ttu-id="8fb03-137">Kai projektas kopijuojamas, nukopijuojama visa išteklių įkelta darbo paskirtstymo struktūra.</span><span class="sxs-lookup"><span data-stu-id="8fb03-137">When the project is copied, the entire resource-loaded work breakdown structure is copied.</span></span> <span data-ttu-id="8fb03-138">Įvardytieji ištekliai pakeičiami bendraisiais ištekliais.</span><span class="sxs-lookup"><span data-stu-id="8fb03-138">Named resources are replaced with generic resources.</span></span> <span data-ttu-id="8fb03-139">Jei įvardytieji ištekliai neturi tokių pačių darbo valandų kaip bendrasis išteklius, grafikas bus perskaičiuotas ir užduoties trukmė gali pasikeisti.</span><span class="sxs-lookup"><span data-stu-id="8fb03-139">If the named resources don't have the same working hours as the generic resource, the schedule will be recalculated and task durations may change.</span></span>

## <a name="project-team-members"></a><span data-ttu-id="8fb03-140">Projekto komandos nariai</span><span class="sxs-lookup"><span data-stu-id="8fb03-140">Project team members</span></span>

<span data-ttu-id="8fb03-141">Kai projekto komanda kopijuojama iš šaltinio projekto, kopijuojami bendrieji ištekliai.</span><span class="sxs-lookup"><span data-stu-id="8fb03-141">When a project team is copied from the source project, the generic resources are copied.</span></span> <span data-ttu-id="8fb03-142">Bendrųjų išteklių priskyrimai tvarkomi taip pat kaip ir šaltinio projekte.</span><span class="sxs-lookup"><span data-stu-id="8fb03-142">Generic resource assignments are also maintained as they were in the source project.</span></span> <span data-ttu-id="8fb03-143">Įvardytieji ištekliai bus konvertuoti į bendruosius komandos narius.</span><span class="sxs-lookup"><span data-stu-id="8fb03-143">Named resources will be converted to generic team members.</span></span>

## <a name="estimates"></a><span data-ttu-id="8fb03-144">Įvertinimai</span><span class="sxs-lookup"><span data-stu-id="8fb03-144">Estimates</span></span>

<span data-ttu-id="8fb03-145">Nukopijavus projektą, iš šaltinio projekto kopijuojamos išteklių, išlaidų ir medžiagų sąmatos eilutės.</span><span class="sxs-lookup"><span data-stu-id="8fb03-145">When the project is copied, resource, expense and material estimate lines are copied from the source project.</span></span> 

<span data-ttu-id="8fb03-146">Norėdami gauti informacijos apie tai, kaip programiškai pasiekti funkciją Kopijuoti projektą, žr. [Projektų šablonų kūrimas naudojant funkciją Kopijuoti projektą](dev-copy-project.md).</span><span class="sxs-lookup"><span data-stu-id="8fb03-146">For information on how to programmatically access Copy Project, see [Develop project templates with Copy Project](dev-copy-project.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
