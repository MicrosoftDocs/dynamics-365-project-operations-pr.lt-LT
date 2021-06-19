---
title: Planavimo režimai
description: Šioje temoje pateikta informacijos apie planavimo režimus.
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 508ff1df8f7e31066712fab6f8871dfdb107a43b
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116717"
---
# <a name="scheduling-modes"></a><span data-ttu-id="2fa01-103">Planavimo režimai</span><span class="sxs-lookup"><span data-stu-id="2fa01-103">Scheduling modes</span></span>

<span data-ttu-id="2fa01-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="2fa01-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2fa01-105">„Dynamics 365 Project Operations“ organizacijoms suteikia galimybę apibrėžti, kaip jos valdo pagrindinių kintamųjų pakeitimus darbo paskirstymo struktūros užduotyse.</span><span class="sxs-lookup"><span data-stu-id="2fa01-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="2fa01-106">Atsižvelgdami į konkrečius organizacijos poreikius, projektų vadovai kurdami projektą gali atlikti planavimo režimo pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="2fa01-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="2fa01-107">Sprendime „Project Operations“ galimi trys toliau nurodyti planavimo režimai.</span><span class="sxs-lookup"><span data-stu-id="2fa01-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="2fa01-108">Fiksuota trukmė (tai yra numatytasis režimas)</span><span class="sxs-lookup"><span data-stu-id="2fa01-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="2fa01-109">Fiksuotos pastangos (*Darbas*)</span><span class="sxs-lookup"><span data-stu-id="2fa01-109">Fixed effort (*Work*)</span></span>
  - <span data-ttu-id="2fa01-110">Fiksuoti vienetai</span><span class="sxs-lookup"><span data-stu-id="2fa01-110">Fixed units</span></span>

<span data-ttu-id="2fa01-111">Reikšmės, kurioms turi įtakos konkretaus planavimo režimo apibrėžimas, nustatomos pagal toliau nurodytą formulę.</span><span class="sxs-lookup"><span data-stu-id="2fa01-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="2fa01-112">Pastangos = trukmė x vienetai</span><span class="sxs-lookup"><span data-stu-id="2fa01-112">Effort  = Duration x Units</span></span>

<span data-ttu-id="2fa01-113">Kai nustatote projekto planavimo režimą, nustatote vieną iš šių reikšmių, kurių keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="2fa01-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="2fa01-114">Laikant šią reikšmę vienodą, jai suteikiama pirmenybė, o sistemai pranešama jos nekeisti pasikeitus kitoms dviem reikšmėms.</span><span class="sxs-lookup"><span data-stu-id="2fa01-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="2fa01-115">Toliau pateiktoje lentelėje pateikiama informacija apie konkretaus režimo pasirinkimo poveikį.</span><span class="sxs-lookup"><span data-stu-id="2fa01-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="2fa01-116">**Šioje užduotyje**</span><span class="sxs-lookup"><span data-stu-id="2fa01-116">**In this task**</span></span>             | <span data-ttu-id="2fa01-117">**Jei peržiūrite vienetus**</span><span class="sxs-lookup"><span data-stu-id="2fa01-117">**If you revise units**</span></span>   | <span data-ttu-id="2fa01-118">**Jei peržiūrite trukmę**</span><span class="sxs-lookup"><span data-stu-id="2fa01-118">**If you revise duration**</span></span> | <span data-ttu-id="2fa01-119">**Jei peržiūrite pastangas**</span><span class="sxs-lookup"><span data-stu-id="2fa01-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="2fa01-120">Fiksuotų vienetų užduotis</span><span class="sxs-lookup"><span data-stu-id="2fa01-120">Fixed units task</span></span>     | <span data-ttu-id="2fa01-121">Trukmė perskaičiuojama.</span><span class="sxs-lookup"><span data-stu-id="2fa01-121">Duration is recalculated.</span></span> | <span data-ttu-id="2fa01-122">Pastangos perskaičiuojamos.</span><span class="sxs-lookup"><span data-stu-id="2fa01-122">Effort is recalculated.</span></span>    | <span data-ttu-id="2fa01-123">Trukmė perskaičiuojama.</span><span class="sxs-lookup"><span data-stu-id="2fa01-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="2fa01-124">Fiksuotų pastangų užduotis</span><span class="sxs-lookup"><span data-stu-id="2fa01-124">Fixed effort task</span></span>    | <span data-ttu-id="2fa01-125">Trukmė perskaičiuojama.</span><span class="sxs-lookup"><span data-stu-id="2fa01-125">Duration is recalculated.</span></span> | <span data-ttu-id="2fa01-126">Vienetai perskaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="2fa01-126">Units are recalculated.</span></span>    | <span data-ttu-id="2fa01-127">Trukmė perskaičiuojama.</span><span class="sxs-lookup"><span data-stu-id="2fa01-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="2fa01-128">Fiksuotos trukmės užduotis</span><span class="sxs-lookup"><span data-stu-id="2fa01-128">Fixed duration task</span></span>  | <span data-ttu-id="2fa01-129">Pastangos perskaičiuojamos.</span><span class="sxs-lookup"><span data-stu-id="2fa01-129">Effort is recalculated.</span></span>   | <span data-ttu-id="2fa01-130">Pastangos perskaičiuojamos.</span><span class="sxs-lookup"><span data-stu-id="2fa01-130">Effort is recalculated.</span></span>    | <span data-ttu-id="2fa01-131">Vienetai perskaičiuojami.</span><span class="sxs-lookup"><span data-stu-id="2fa01-131">Units are recalculated.</span></span>   |

<span data-ttu-id="2fa01-132">Norėdami daugiau sužinoti apie tam tikro režimo poveikį, žr. [Užduoties tipo keitimas norint tiksliau planuoti](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span><span class="sxs-lookup"><span data-stu-id="2fa01-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="2fa01-133">Temoje vietoj termino **Pastangos** naudojamas terminas **Darbas**.</span><span class="sxs-lookup"><span data-stu-id="2fa01-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="2fa01-134">Organizacijos planavimo režimo keitimas</span><span class="sxs-lookup"><span data-stu-id="2fa01-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="2fa01-135">Norėdami apibrėžti organizacijos planavimo režimą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2fa01-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="2fa01-136">Nueikite į **Parametrai** \> **Bendra** \>**Parametrai** ir pasirinkite projekto parametrą.</span><span class="sxs-lookup"><span data-stu-id="2fa01-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="2fa01-137">Puslapyje **Projekto parametrai** pasirinkite numatytąjį organizacijos planavimo režimą, tada apibrėžkite projekto vadovo galimybę perrašyti parametrą kuriant naują projektą.</span><span class="sxs-lookup"><span data-stu-id="2fa01-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="2fa01-138">Projekto planavimo režimo parametro keitimas</span><span class="sxs-lookup"><span data-stu-id="2fa01-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="2fa01-139">Jei organizacija projekto vadovui leidžia perrašyti numatytąjį planavimo režimą, projekto vadovas gali jį pakeisti kurdami naują projektą.</span><span class="sxs-lookup"><span data-stu-id="2fa01-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="2fa01-140">Tačiau įrašius projektą planavimo režimo keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="2fa01-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="2fa01-141">Nukopijuoti projektai</span><span class="sxs-lookup"><span data-stu-id="2fa01-141">Copied projects</span></span>

<span data-ttu-id="2fa01-142">Kadangi projektas sukuriamas atliekant projekto kopijavimo veiksmą, projekto vadovas negali nustatyti planavimo režimo.</span><span class="sxs-lookup"><span data-stu-id="2fa01-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="2fa01-143">Numatyta, kad paskirties projektas visada bus nustatytas kaip organizacijos lygiu apibrėžtas projektas.</span><span class="sxs-lookup"><span data-stu-id="2fa01-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="2fa01-144">Nukopijuotos užduotys</span><span class="sxs-lookup"><span data-stu-id="2fa01-144">Copied tasks</span></span>

<span data-ttu-id="2fa01-145">Kai užduotis nukopijuojama iš vieno projekto į kitą, ji paveldi paskirties projekto planavimo režimą.</span><span class="sxs-lookup"><span data-stu-id="2fa01-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
