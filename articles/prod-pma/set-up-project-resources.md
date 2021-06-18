---
title: Projekto išteklių nustatymas
description: Šioje temoje pateikiama informacija, kaip nustatyti arba prašyti projekto išteklių.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 49e0ca6254518079d2e01d92ac2e31d119468c4b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997701"
---
# <a name="set-up-project-resources"></a><span data-ttu-id="37024-103">Projekto išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="37024-103">Set up project resources</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37024-104">Turite nustatyti kalendorių ir susieti jį su darbuotoju.</span><span class="sxs-lookup"><span data-stu-id="37024-104">You must set up a calendar and associate it with an employee or a worker.</span></span> <span data-ttu-id="37024-105">Kalendorius naudojamas projekto ir projektui rezervuotų išteklių darbo laiko grafikui sudaryti.</span><span class="sxs-lookup"><span data-stu-id="37024-105">The calendar is used to schedule the project and the working time of the resources that are reserved for the project.</span></span> <span data-ttu-id="37024-106">Atlikdami kalendoriaus sąranką, projekto vadovai išteklių optimizavimo metu gali koreguoti išteklių paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="37024-106">During calendar setup, project managers can do resource leveling as part of resource optimization.</span></span> <span data-ttu-id="37024-107">Ištekliams gali būti taikomi apribojimai pagal kalendoriaus grafiką.</span><span class="sxs-lookup"><span data-stu-id="37024-107">Based on the calendar schedule, restrictions can be put on resources.</span></span> <span data-ttu-id="37024-108">Kalendorių galite nustatyti puslapyje **Kalendorius**.</span><span class="sxs-lookup"><span data-stu-id="37024-108">You can set up a calendar on the **Calendars** page.</span></span>

<span data-ttu-id="37024-109">Kai nustatote darbuotoją kaip projekto išteklių, galite pasirinkti iš darbuotojų, dirbančių įmonėje, kuriai nustatote išteklius.</span><span class="sxs-lookup"><span data-stu-id="37024-109">When you set up a worker as a project resource, you can select from workers who work in the company that you're setting up resources for.</span></span> <span data-ttu-id="37024-110">Arba galite pasirinkti darbuotojus iš kitų jūsų organizacijoje esančių įmonių.</span><span class="sxs-lookup"><span data-stu-id="37024-110">Alternatively, you can select workers from other companies in your organization.</span></span> <span data-ttu-id="37024-111">Šie darbuotojai vadinami vidinės įmonės ištekliais.</span><span class="sxs-lookup"><span data-stu-id="37024-111">These workers are known as intercompany resources.</span></span>

<span data-ttu-id="37024-112">Toliau pateikiamose procedūrose paaiškinama, kaip nustatyti darbuotoją kaip jūsų įmonės projekto išteklių ir kaip nustatyti vidinės įmonės projekto išteklius.</span><span class="sxs-lookup"><span data-stu-id="37024-112">The following procedures explain how to set up a worker as a project resource in your company and how to set up an intercompany project resource.</span></span>

## <a name="set-up-a-worker-as-a-project-resource"></a><span data-ttu-id="37024-113">Darbuotojo kaip projekto ištekliaus nustatymas</span><span class="sxs-lookup"><span data-stu-id="37024-113">Set up a worker as a project resource</span></span>

1. <span data-ttu-id="37024-114">Puslapyje **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotoją, kurį įtraukiate kaip projekto išteklių, ir atidarykite darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="37024-114">On the **Workers** page, in the **Workers** list, select the worker that you're adding as a project resource, and open the worker record.</span></span>
2. <span data-ttu-id="37024-115">Veiksmų srityje pasirinkite **Projektas** &gt; **Sąranka** &gt; **Projekto sąranka**.</span><span class="sxs-lookup"><span data-stu-id="37024-115">On the Action Pane, select **Project** &gt; **Setup** &gt; **Project setup**.</span></span>
3. <span data-ttu-id="37024-116">Pasirinkite kalendorių, tada uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="37024-116">Select a calendar, and then close the page.</span></span>

<span data-ttu-id="37024-117">Taip pat galite nurodyti išteklių numatytuosius projektus kaip išankstinio priskyrimo tipą.</span><span class="sxs-lookup"><span data-stu-id="37024-117">You can also specify default projects for a resource as a type of pre-assignment.</span></span> <span data-ttu-id="37024-118">Išankstinius priskyrimus galima naudoti, kai išteklių vadovas arba projektų vadovas iš anksto žino, su kuriais projektais dirbs išteklius.</span><span class="sxs-lookup"><span data-stu-id="37024-118">Pre-assignments can be used when the resource manager or project manager knows which projects the resource will be working on in advance.</span></span> <span data-ttu-id="37024-119">Išankstiniai priskyrimai taip pat gali būti grindžiami projekto rėmėjo ar kliento prašymu.</span><span class="sxs-lookup"><span data-stu-id="37024-119">Pre-assignments can also be based on the request of a project sponsor or customer.</span></span> <span data-ttu-id="37024-120">Norėdami iš anksto priskirti projektą, puslapio **Projektų priskyrimas** skirtuko **Projektai** sąraše **Likę projektai** pažymėkite atitinkamą projektą.</span><span class="sxs-lookup"><span data-stu-id="37024-120">To pre-assign a project, on the **Assign projects** page, on the **Projects** tab, in the **Remaining projects** list, select the appropriate project.</span></span>

## <a name="set-up-an-intercompany-resource"></a><span data-ttu-id="37024-121">Vidinės įmonės išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="37024-121">Set up an intercompany resource</span></span>

<span data-ttu-id="37024-122">Kai nustatote darbuotoją kaip vidinės įmonės išteklių, turite atlikti sąranką ir nuomojančioje, ir besiskolinančioje įmonėje.</span><span class="sxs-lookup"><span data-stu-id="37024-122">When you set up a worker as an intercompany resource, you must complete the setup in both the lending company and the borrowing company.</span></span>

### <a name="in-the-lending-company"></a><span data-ttu-id="37024-123">Nuomojančioje įmonėje</span><span class="sxs-lookup"><span data-stu-id="37024-123">In the lending company</span></span>

1. <span data-ttu-id="37024-124">Programoje „Finance” patikrinkite, ar pažymėta nuomojanti įmonė, tada atlikite ankstesniame skyriuje „Darbuotojo kaip projekto ištekliaus nustatymas” pateiktą procedūrą.</span><span class="sxs-lookup"><span data-stu-id="37024-124">In Finance, verify that the lending company is selected, and then complete the procedure in the previous section, "Set up a worker as a project resource."</span></span>
2. <span data-ttu-id="37024-125">Puslapyje **Vidinės įmonės apskaita** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="37024-125">On the **Intercompany accounting** page, select **New**.</span></span>
3. <span data-ttu-id="37024-126">Lauke **Juridinio subjekto ID** pažymėkite nuomojančią įmonę.</span><span class="sxs-lookup"><span data-stu-id="37024-126">In the **Legal entity ID** field, select the lending company.</span></span> <span data-ttu-id="37024-127">Tinkamai užpildykite likusius laukus ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="37024-127">Fill in the remaining fields as appropriate, and then select **Save**.</span></span>
4. <span data-ttu-id="37024-128">Puslapyje **Perkėlimo kaina** pasirinkite **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="37024-128">On the **Transfer price** page, select **New**.</span></span>
5. <span data-ttu-id="37024-129">Lauke **Besiskolinančio juridinio subjekto ID** pažymėkite tinkamą įmonę.</span><span class="sxs-lookup"><span data-stu-id="37024-129">In the **Borrowing legal entity** field, select the appropriate company.</span></span>
6. <span data-ttu-id="37024-130">Jeigu norite besiskolinančiai įmonei išnuomoti tik tą išteklių, kurį sukūrėte šio skyriaus pradžioje, lauke **Ištekliai**, pasirinkite sukurto ištekliaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="37024-130">To lend the borrowing company only the resource that you created at the beginning of this section, in the **Resource** field, select the name of the resource that you created.</span></span> <span data-ttu-id="37024-131">Jeigu norite, kad besiskolinančioji įmonė galėtų pasiekti visus nuomojančios įmonės išteklius, palikite lauką **Ištekliai** tuščią.</span><span class="sxs-lookup"><span data-stu-id="37024-131">To make all resources in the lending company available to the borrowing company, leave the **Resource** field blank.</span></span>
7. <span data-ttu-id="37024-132">Puslapio **Projektų valdymo ir apskaitos parametrai** skirtuke **Vidinė įmonė** nustatykite parinktį **Įgalinti vidinės įmonės išteklių planavimą ir grafikų sudarymą** kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="37024-132">On the **Project management and accounting parameters** page, on the **Intercompany** tab, set the **Enable intercompany resource scheduling and timesheets** option to **Yes**.</span></span>

### <a name="in-the-borrowing-company"></a><span data-ttu-id="37024-133">Besiskolinančioje įmonėje</span><span class="sxs-lookup"><span data-stu-id="37024-133">In the borrowing company</span></span>

- <span data-ttu-id="37024-134">Puslapio **Išteklių sąrašas** ieškos filtre įveskite ištekliaus, kurį sukūrėte nuomojančiai įmonei, pavadinimą, kad patikrintumėte, ar pavadinimas įtrauktas į besiskolinančios įmonės išteklių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="37024-134">On the **Resources list** page, in the search filter, enter the name of the resource that you created for the lending company, to verify that the name is included in the resource list for the borrowing company.</span></span>

## <a name="request-project-resources"></a><span data-ttu-id="37024-135">Projektų išteklių prašymas</span><span class="sxs-lookup"><span data-stu-id="37024-135">Request project resources</span></span>
<span data-ttu-id="37024-136">Projektų išteklių planavimo funkcijos leidžia išteklių vadovams tik paskirstyti darbuotojams įtraukimuose ar projektuose priskirtus išteklius.</span><span class="sxs-lookup"><span data-stu-id="37024-136">The functionality for project resource scheduling only lets resource managers distribute staffed resources on engagements or projects.</span></span> <span data-ttu-id="37024-137">Norėdami įgalinti šias funkcijas, atlikite toliau pateikiamas užduotis arba patikrinkite, ar jos buvo atliktos.</span><span class="sxs-lookup"><span data-stu-id="37024-137">To enable this functionality, complete the following tasks, or verify that they have been completed:</span></span>

- <span data-ttu-id="37024-138">Nustatykite numerių sekas.</span><span class="sxs-lookup"><span data-stu-id="37024-138">Set up number sequences.</span></span>
- <span data-ttu-id="37024-139">Nustatykite projektų valdymo ir apskaitos darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="37024-139">Set up project management and accounting workflows.</span></span>
- <span data-ttu-id="37024-140">Įgalinkite išteklių užklausos darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="37024-140">Enable resource request workflows.</span></span>

<span data-ttu-id="37024-141">Jeigu reikia, atlikę ankstesnes užduotis, galite atlikti toliau pateikiamas užduotis.</span><span class="sxs-lookup"><span data-stu-id="37024-141">After the preceding tasks have been completed, you can complete the following tasks as you require:</span></span>

- <span data-ttu-id="37024-142">Sukurkite ištekliaus užklausą iš preliminariai rezervuoto darbuotojui priskirto ištekliaus.</span><span class="sxs-lookup"><span data-stu-id="37024-142">Create a resource request from a soft-booked staffed resource.</span></span>
- <span data-ttu-id="37024-143">Stebėkite išteklių užklausas.</span><span class="sxs-lookup"><span data-stu-id="37024-143">Monitor resource requests.</span></span>
- <span data-ttu-id="37024-144">Vykdykite išteklių užklausas.</span><span class="sxs-lookup"><span data-stu-id="37024-144">Fulfill resource requests.</span></span>
- <span data-ttu-id="37024-145">Prašykite darbuotojui priskirto ištekliaus iš WBS.</span><span class="sxs-lookup"><span data-stu-id="37024-145">Request a staffed resource from a WBS.</span></span>
- <span data-ttu-id="37024-146">Rezervuokite išteklius projektui, neturėdami darbuotojui priskirto ištekliaus užklausos.</span><span class="sxs-lookup"><span data-stu-id="37024-146">Book resources to a project without having a request for a staffed resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]