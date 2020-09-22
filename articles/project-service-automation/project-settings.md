---
title: Projekto parametrai
description: Šioje temoje pateikta informacija apie projektų valdymo parametrus.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 7c5be6ff-8f92-4dfc-9f9d-4abc76f96638
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 843192092598fd713b3bc59bf90c5362d0dad8b4
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753671"
---
# <a name="project-settings"></a><span data-ttu-id="9dc4f-103">Projekto parametrai</span><span class="sxs-lookup"><span data-stu-id="9dc4f-103">Project settings</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="9dc4f-104">Norėdami pasiekti projekto planavimo funkcijas, naudokite šiuos parametrus.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-104">Use the following settings to access the project planning features.</span></span>

## <a name="work-template"></a><span data-ttu-id="9dc4f-105">Darbo šablonas</span><span class="sxs-lookup"><span data-stu-id="9dc4f-105">Work template</span></span>

<span data-ttu-id="9dc4f-106">Norėdami sukurti projekto grafiką, sukuriate projekto kalendoriaus šabloną, nurodydami dienos darbo valandų skaičių ir kada įmonės nedirba.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-106">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="9dc4f-107">Norėdami sukurti projekto kalendoriaus šabloną, susiejate darbo šabloną su projekto **Kalendoriaus šablonas** lauku.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-107">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="9dc4f-108">Norėdami sukurti darbo šabloną, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-108">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="9dc4f-109">Naudodamiesi PSA, kairiojoje naršymo srityje spustelėkite **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-109">In PSA, in the left navigation pane, click **Resources**.</span></span> 
2. <span data-ttu-id="9dc4f-110">Sąrašo puslapyje **Ištekliai** atidarykite vartotojo įrašą, tada pažymėkite **Rodyti darbo valandas**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-110">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="9dc4f-111">Įsitikinkite, kad naršyklėje leidžiami iššokantieji langai.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-111">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="9dc4f-112">Taip galėsite matyti ištekliui nustatytas darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-112">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="9dc4f-113">Skirtuke **Mėnesio rodinys** spustelėkite **Nustatyti**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-113">On the **Monthly View** tab, click **Set Up**.</span></span> <span data-ttu-id="9dc4f-114">Bus rodomas trijų parinkčių sąrašas:</span><span class="sxs-lookup"><span data-stu-id="9dc4f-114">A list of three options appears:</span></span> 

  - <span data-ttu-id="9dc4f-115">Naujas savaitės grafikas</span><span class="sxs-lookup"><span data-stu-id="9dc4f-115">New Weekly Schedule</span></span>
  - <span data-ttu-id="9dc4f-116">Vienos dienos darbo grafikas</span><span class="sxs-lookup"><span data-stu-id="9dc4f-116">Work Schedule for One Day</span></span>
  - <span data-ttu-id="9dc4f-117">Laisvas laikas</span><span class="sxs-lookup"><span data-stu-id="9dc4f-117">Time Off</span></span>

> ![Nustatymų parinktys](media/project-13.png)

4. <span data-ttu-id="9dc4f-119">Pažymėkite **Naujas savaitės grafikas** ir nustatykite šio išteklių grafiko parinktis.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-119">Select **New Weekly Schedule**, and then set the options for this resource schedule.</span></span> <span data-ttu-id="9dc4f-120">Galite nustatyti pasikartojantį savaitinį grafiką, dienos darbo valandų parametrus, įmonės ne darbo laiką ir kt.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-120">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="9dc4f-121">Nustatykite datų intervalą pasirinkdami **Įrašyti**, tada spustelėkite **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-121">Set the date range, select **Save**, and then click **Close**.</span></span> 
6. <span data-ttu-id="9dc4f-122">Grįžkite į sąrašo puslapį **Ištekliai** ir pažymėkite išteklių, kuriam nustatėte darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-122">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="9dc4f-123">Pažymėkite **Nustatyti kalendorių kaip** nustatyti darbo šabloną.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-123">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="9dc4f-124">Dialogo lange **Darbo šablonas** įveskite darbo šablono pavadinimą, tada pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-124">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="9dc4f-125">Dabar galite susieti darbo šabloną su projekto kalendoriaus šablonu.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-125">You can now associate the work template with a project calendar template.</span></span>

## <a name="resource-roles"></a><span data-ttu-id="9dc4f-126">Išteklių vaidmenys</span><span class="sxs-lookup"><span data-stu-id="9dc4f-126">Resource roles</span></span>

<span data-ttu-id="9dc4f-127">Terminas „*išteklių vaidmuo*“ nurodo įgūdžių, kompetencijų ir sertifikavimo rinkinį, kurį asmuo turi turėti, kad atliktų tam tikrą projekto užduočių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-127">The term *resource role* refers to the set of skills, competencies, and certifications that a person must have to perform a specific set of tasks on a project.</span></span> <span data-ttu-id="9dc4f-128">PSA leidžia nustatyti savikainą ir išrašyti sąskaitą pagal ištekliaus laiką, pagrįstą ištekliaus vaidmeniu, su kuriuo jis susietas.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-128">PSA lets you cost and bill a resource's time based on the role that the resource is associated with.</span></span> <span data-ttu-id="9dc4f-129">Visos organizacijos turi nustatyti šiuos vaidmenis naudodami kairiąją naršymo juostą meniu **Project Service**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-129">Every organization must set up these roles by using the left navigation on the **Project Service** menu.</span></span>

<span data-ttu-id="9dc4f-130">Kiekviena organizacija turi nustatyti šiuos vaidmenis puslapyje **Aktyvių išteklių kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-130">Every organization must set up these roles on the **Active Resource Categories** page.</span></span> <span data-ttu-id="9dc4f-131">Norėdami atidaryti šį puslapį, kairiojoje naršymo srityje pažymėkite **Išteklių vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-131">To open this page, in the left navigation pane, select **Resource Roles**.</span></span>

## <a name="price-lists"></a><span data-ttu-id="9dc4f-132">Kainoraščiai</span><span class="sxs-lookup"><span data-stu-id="9dc4f-132">Price lists</span></span>

<span data-ttu-id="9dc4f-133">Kainoraščiais galima nustatyti išteklių vaidmenų, išlaidų kategorijų, produktų ir kitų organizacijos elementų savikainą ir pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-133">Price lists let you set cost and sales prices for resource roles, expense categories, products, and other elements in an organization.</span></span> <span data-ttu-id="9dc4f-134">Norėdami sukurti finansines sąmatas už darbą, kuris bus atliekamas vykdant projektą, įsitikinkite, kad yra sudarytas atsarginis savikainos ir pardavimo kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-134">Before you set financial estimates for the work that must be delivered for a project, you should create a backing cost and sales price list.</span></span> <span data-ttu-id="9dc4f-135">Parametrų skyriuje taip pat turite nustatyti numatytąją savikainos ir pardavimo kainoraštį, taikomą visiems organizacijoje sukurtiems projektams.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-135">In the parameters section, you should also set up a default cost and sales price list that applies to all projects that are created in the organization.</span></span> <span data-ttu-id="9dc4f-136">Puslapyje **Aktyvieji projekto parametrai** įsitikinkite, kad nustatėte numatytąjį savikainos ir pardavimo kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="9dc4f-136">On the **Active Project Parameters** page, make sure that you set up a default cost and sales price list.</span></span>
