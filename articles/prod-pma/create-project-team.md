---
title: Projekto komandos kūrimas
description: Šioje temoje pateikta informacija apie tai, kaip sukurti ir valdyti projekto komandas.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 121a007d91c2da4f3b9951901781757b8bcca8fe
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270868"
---
# <a name="create-a-project-team"></a><span data-ttu-id="33570-103">Kurti projekto komandą</span><span class="sxs-lookup"><span data-stu-id="33570-103">Create a project team</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33570-104">Norėdamas naudoti vaidmenis, kurie buvo anksčiau nustatyti projekte, projekto vadovas turi susieti šiuos vaidmenis su projektu.</span><span class="sxs-lookup"><span data-stu-id="33570-104">To use the roles that were previously set up in a project, a project manager must associate the roles with the project.</span></span> <span data-ttu-id="33570-105">Projektui galima priskirti kelis vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="33570-105">Multiple roles can be assigned for a project.</span></span> <span data-ttu-id="33570-106">Siekiant išvengti painiavos, šie vaidmenys rezervavimo metu pažymimi automatiškai.</span><span class="sxs-lookup"><span data-stu-id="33570-106">To prevent confusion, these roles are automatically labeled during reservation.</span></span> <span data-ttu-id="33570-107">Pavyzdžiui, jei projekto vadovui reikia trijų programinės įrangos inžinierių, automatiškai generuojami trys programinės įrangos inžinierių vaidmenys, turintys žymas **1-as programinės įrangos inžinierius**, **2-as programinės įrangos inžinierius** ir **3-ias programinės įrangos inžinierius**.</span><span class="sxs-lookup"><span data-stu-id="33570-107">For example, if the project manager requires three software engineers, three Software engineer roles that have **software engineer 1**, **software engineer 2**, and **software engineer 3** as their labels are automatically generated.</span></span> <span data-ttu-id="33570-108">Jei vaidmens charakteristikos anksčiau buvo nustatytos, ieškant išteklių jos taikomos kaip filtras.</span><span class="sxs-lookup"><span data-stu-id="33570-108">If role characteristics were previously set for the role, they are applied as a filter during searches for a resource.</span></span> <span data-ttu-id="33570-109">Jeigu reikia, galima įtraukti papildomų charakteristikų, siekiant dar labiau patikslinti iešką.</span><span class="sxs-lookup"><span data-stu-id="33570-109">Additional characteristics can be added as required to further refine the search.</span></span>

<span data-ttu-id="33570-110">Taip pat galima tinkinti rodinio parametrus, siekiant suteikti geresnį išteklių pasiekiamumo rodinį.</span><span class="sxs-lookup"><span data-stu-id="33570-110">View settings can also be customized to give a better view of resource availability.</span></span> <span data-ttu-id="33570-111">Galima rodyti pasiekiamumą pagal valandas, dienas, savaites, mėnesius, ketvirčius ir metus.</span><span class="sxs-lookup"><span data-stu-id="33570-111">There are options to show hourly, daily, weekly, monthly, quarterly, and annual availability.</span></span> <span data-ttu-id="33570-112">Taip pat galima rodyti pasiekiamą ir likusį išteklių pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="33570-112">There is also an option to show available and remaining capacity on resources.</span></span> <span data-ttu-id="33570-113">Ši parinktis naudinga valdant laiką, kai įvertinate galimą veiklos arba išteklių pasiekiamumo laiką.</span><span class="sxs-lookup"><span data-stu-id="33570-113">This option is useful for time management, when you're estimating available time for activities or resource availability.</span></span>

<span data-ttu-id="33570-114">Projekto vadovas gali puslapyje pasirinkti vaidmenį, tada, jeigu yra pasiekiamas reikalavimus atitinkantis išteklius, pasirinkti rezervuoti išteklių, kad jis atliktų šį vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="33570-114">The project manager can select a role on the page and then, if there is an available resource that fits the requirement, select to reserve a resource to fill the role.</span></span> <span data-ttu-id="33570-115">Atkreipkite dėmesį, kad šiame planavimo etape išteklių rezervuoti nereikia.</span><span class="sxs-lookup"><span data-stu-id="33570-115">Note that the resources don't have to be reserved at this point in the planning stage.</span></span> <span data-ttu-id="33570-116">Kai sukursite WBS, galėsite keisti projekto vaidmenis darbuotojams priskirtais ištekliais.</span><span class="sxs-lookup"><span data-stu-id="33570-116">When you create a WBS, you can replace roles with staffed resources for the project.</span></span> <span data-ttu-id="33570-117">Jei vaidmenys keičiami darbuotojams priskirtais ištekliais WBS, išteklių sąranka automatiškai atnaujina projekto komandos sąrašą ir grafiką.</span><span class="sxs-lookup"><span data-stu-id="33570-117">If roles are replaced with staffed resources in the WBS, the resource setup automatically updates the project team listing and scheduling.</span></span>

<span data-ttu-id="33570-118">[![Projekto komandos sąrašas, kuriame išvardyti ir vaidmenys, ir faktiniai ištekliai](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span><span class="sxs-lookup"><span data-stu-id="33570-118">[![Project team listing that includes both roles and actual resources](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg)</span></span> 

<span data-ttu-id="33570-119">Projekto vadovas turi įvairių projekto ištekliaus rezervavimo parinkčių, pvz., **Pajėgumo likučio metodas**, **Viso pajėgumo metodas**, **Pajėgumo procentinės dalies rezervavimo metodas** ir **Nurodytos valandos**.</span><span class="sxs-lookup"><span data-stu-id="33570-119">The project manager has various options for booking a resource for a project, such as **Remaining capacity**, **Full capacity**, **Capacity percentage**, and **Specify hours**.</span></span> <span data-ttu-id="33570-120">Šios rezervavimo parinktys gali būti atšauktos bet kuriuo metu, jei pasikeičia išteklių priskyrimai.</span><span class="sxs-lookup"><span data-stu-id="33570-120">These booking options can be canceled at any time if resource assignments change.</span></span> <span data-ttu-id="33570-121">Palaikomi du rezervavimo tipai.</span><span class="sxs-lookup"><span data-stu-id="33570-121">Two types of booking are supported:</span></span>

- <span data-ttu-id="33570-122">**Rezervuoti galutinai** – rezervuotas išteklius buvo patvirtintas dirbti įtraukime nustatytą laiko tarpą.</span><span class="sxs-lookup"><span data-stu-id="33570-122">**Hard Book** – The resource reservation was approved and confirmed to work on the engagement for the specified duration.</span></span>
- <span data-ttu-id="33570-123">**Preliminarus rezervavimas** – rezervuotas išteklius buvo preliminariai paskirtas dirbti įtraukime nustatytą laiko tarpą.</span><span class="sxs-lookup"><span data-stu-id="33570-123">**Soft book** – The resource reservations was tentatively set to work on the engagement for the specified duration.</span></span>

<span data-ttu-id="33570-124">Tolesne procedūra paaiškinama, kaip sukurti projekto komandą.</span><span class="sxs-lookup"><span data-stu-id="33570-124">The following procedure explains how to create a project team.</span></span>

## <a name="create-a-project-team"></a><span data-ttu-id="33570-125">Kurti projekto komandą</span><span class="sxs-lookup"><span data-stu-id="33570-125">Create a project team</span></span>

1. <span data-ttu-id="33570-126">Sąrašo **Visi projektai** puslapyje pasirinkite projektą, tada pasirinkite **Redaguoti**.</span><span class="sxs-lookup"><span data-stu-id="33570-126">On the **All projects** list page, select a project, and then select **Edit**.</span></span>
2. <span data-ttu-id="33570-127">Skirtuko **Projekto komanda ir planavimas** lauke **Grafiko pabaigos data** įveskite grafiko pradžios datą plius vieną mėnesį.</span><span class="sxs-lookup"><span data-stu-id="33570-127">On the **Project team and scheduling** tab, in the **Schedule end date** field, enter the schedule start date plus one month.</span></span> <span data-ttu-id="33570-128">Pavyzdžiui, jei grafiko pradžios data yra 2017 m. birželio 24 d. (2017-06-24), įveskite **2017-07-24**.</span><span class="sxs-lookup"><span data-stu-id="33570-128">For example, if the schedule start date is June 24, 2017 (24/06/2017), enter **24/07/2017**.</span></span>
3. <span data-ttu-id="33570-129">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="33570-129">Select **Add**.</span></span>
4. <span data-ttu-id="33570-130">Srityje **Įtraukti vaidmenis į projektą**, lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.</span><span class="sxs-lookup"><span data-stu-id="33570-130">In the **Add roles to the project** pane, in the **Role** field, select **Senior Project Manager**.</span></span>
5. <span data-ttu-id="33570-131">Pasirinkite **Reikiamos kompetencijos**.</span><span class="sxs-lookup"><span data-stu-id="33570-131">Select **Required competencies**.</span></span>
6. <span data-ttu-id="33570-132">Puslapyje **Pasirinkite charakteristikas** charakteristikos, kurias anksčiau nustatėte vyresniojo projektų vadovo vaidmeniui, pasirenkamos pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="33570-132">On the **Choose characteristics** page, the characteristics that you previously set for the Senior project manager role are selected by default.</span></span> <span data-ttu-id="33570-133">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="33570-133">Select **OK**.</span></span>
7. <span data-ttu-id="33570-134">Puslapyje **Įtraukti vaidmenis į projektą**, lauke **Išteklių skaičius** įveskite **1**.</span><span class="sxs-lookup"><span data-stu-id="33570-134">On the **Add roles to project** page, in the **Number of resources** field, enter **1**.</span></span>
8. <span data-ttu-id="33570-135">Lauke **Ištekliai**, peržvalgos rodinyje parodomi visi ištekliai, turintys reikiamas kompetencijas.</span><span class="sxs-lookup"><span data-stu-id="33570-135">In the **Resource** field, the lookup shows all resources that have the required competencies.</span></span> <span data-ttu-id="33570-136">Pasirinkite **Danielis Goldschmidtas**, tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="33570-136">Select **Daniel Goldschmidt**, and then select **Create**.</span></span>
9. <span data-ttu-id="33570-137">Puslapyje **Projektas** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="33570-137">On the **Project** page, select **Add**.</span></span>
10. <span data-ttu-id="33570-138">Srityje **Įtraukti vaidmenis į projektą**, lauke **Vaidmuo** pasirinkite **Komandos narys**.</span><span class="sxs-lookup"><span data-stu-id="33570-138">In the **Add roles to the project** pane, in the **Role** field, select **Team member**.</span></span> <span data-ttu-id="33570-139">Lauke **Išteklių skaičius** įveskite **5**.</span><span class="sxs-lookup"><span data-stu-id="33570-139">In the **Number of resources** field, enter **5**.</span></span>
11. <span data-ttu-id="33570-140">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="33570-140">Select **Create**.</span></span>
12. <span data-ttu-id="33570-141">Puslapyje **Projektai** pasirinkite **Naudoti išteklių**.</span><span class="sxs-lookup"><span data-stu-id="33570-141">On the **Projects** page, select **Fulfill resource**.</span></span>

## <a name="monitor-project-teams"></a><span data-ttu-id="33570-142">Stebėkite projektų komandas</span><span class="sxs-lookup"><span data-stu-id="33570-142">Monitor project teams</span></span>
1. <span data-ttu-id="33570-143">Puslapyje **Visi projektai** pasirinkite projekto **XYZ Upgrade Phase 2** saitą **Projekto ID**.</span><span class="sxs-lookup"><span data-stu-id="33570-143">On the **All projects** page, select the **Project ID** link for the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="33570-144">„FastTab” skirtuke **Projekto komanda ir planavimas** patikrinkite, ar išvardyti projekto ištekliai yra tinkami.</span><span class="sxs-lookup"><span data-stu-id="33570-144">On the **Project team and scheduling** FastTab, verify that the project resources that are listed are correct.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]