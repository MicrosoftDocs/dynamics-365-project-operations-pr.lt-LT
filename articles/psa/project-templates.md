---
title: Projekto šablonai
description: Šioje temoje pateikta informacija apie tai, kaip naudoti projektų šablonus, skirtus greitam projektų nustatymui.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: bedcbc76d932a81e0c78bb58ce6a161446a26dde
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5998286"
---
# <a name="project-templates"></a><span data-ttu-id="44f8f-103">Projekto šablonai</span><span class="sxs-lookup"><span data-stu-id="44f8f-103">Project templates</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="44f8f-104">Projekto šablonas yra iš anksto nustatyta sistema, padedanti greitai ir paprastai pradėti projektą.</span><span class="sxs-lookup"><span data-stu-id="44f8f-104">A project template is a predefined framework that helps you quickly and easily start a project.</span></span> <span data-ttu-id="44f8f-105">Galite naudoti iš anksto nustatytą šabloną ir sukurti naują projektą vienu spustelėjimu.</span><span class="sxs-lookup"><span data-stu-id="44f8f-105">You can use a predefined template to create a new project with a single click.</span></span> <span data-ttu-id="44f8f-106">Kalbant apie projektus, turite apibrėžti būtinąsias projektų šablonų sąlygas.</span><span class="sxs-lookup"><span data-stu-id="44f8f-106">As for projects, you must define the prerequisites for project templates.</span></span> <span data-ttu-id="44f8f-107">Turite apibrėžti kiekvieno projekto šablono projekto kalendorių, o vaidmenis ir kainoraščius reikia iš anksto nustatyti organizacijoje, kad šablono komponentuose būtų naudingų duomenų.</span><span class="sxs-lookup"><span data-stu-id="44f8f-107">You must define a project calendar for each project template, and roles and price lists must be predefined in the organization, so that the components of the template have useful data.</span></span>

<span data-ttu-id="44f8f-108">Projekto šabloną sudaro trys komponentai: grafikas, projektų sąmatos ir projekto komandos nariai.</span><span class="sxs-lookup"><span data-stu-id="44f8f-108">A project template consists of three components: a schedule, project estimates, and project team members.</span></span>

## <a name="schedule"></a><span data-ttu-id="44f8f-109">Tvarkaraštis</span><span class="sxs-lookup"><span data-stu-id="44f8f-109">Schedule</span></span>

<span data-ttu-id="44f8f-110">Projekto šablono grafikas turi tą patį elementų rinkinį kaip ir projekto grafikas.</span><span class="sxs-lookup"><span data-stu-id="44f8f-110">A schedule in a project template has the same set of elements as a schedule in a project.</span></span> <span data-ttu-id="44f8f-111">Galite kurti užduočių hierarchiją, susieti vaidmenis su užduotimis, nustatyti grafiko atributus, nustatyti priklausomybes.</span><span class="sxs-lookup"><span data-stu-id="44f8f-111">You can create a task hierarchy, associate roles with tasks, define schedule attributes, and set dependencies.</span></span> <span data-ttu-id="44f8f-112">Projekto šablono grafikas taip pat palaiko užduočių režimus kiekvienai užduočiai.</span><span class="sxs-lookup"><span data-stu-id="44f8f-112">A schedule in a project template also supports task modes for each task.</span></span> <span data-ttu-id="44f8f-113">Todėl jis palaiko planavimo modulį.</span><span class="sxs-lookup"><span data-stu-id="44f8f-113">Therefore, it supports the scheduling engine.</span></span> <span data-ttu-id="44f8f-114">Projekto kalendorių turite susieti su projektu.</span><span class="sxs-lookup"><span data-stu-id="44f8f-114">You must associate a project calendar with the project.</span></span> <span data-ttu-id="44f8f-115">Kuriant darbo grafiką, skirtumų tarp projekto šablono ir projekto nėra.</span><span class="sxs-lookup"><span data-stu-id="44f8f-115">When you create a work schedule, there is no difference between a project template and a project.</span></span>

## <a name="project-estimates"></a><span data-ttu-id="44f8f-116">Projekto įvertinimai</span><span class="sxs-lookup"><span data-stu-id="44f8f-116">Project estimates</span></span>

<span data-ttu-id="44f8f-117">Projekto sąmatos projekto šablone veikia taip pat kaip projekto sąmatos projekte.</span><span class="sxs-lookup"><span data-stu-id="44f8f-117">Project estimates in a project template work the same way as project estimates in a project.</span></span> <span data-ttu-id="44f8f-118">Tačiau savikaina ir pardavimo kainos yra gaunamos iš numatytųjų savikainos ir pardavimo kainoraščių, apibrėžtų parametruose.</span><span class="sxs-lookup"><span data-stu-id="44f8f-118">However, the cost and sales prices are pulled from the default cost and sales price lists that are defined in the parameters.</span></span>

## <a name="creating-a-project-from-a-template"></a><span data-ttu-id="44f8f-119">Projekto kūrimas pagal šabloną</span><span class="sxs-lookup"><span data-stu-id="44f8f-119">Creating a project from a template</span></span>
 
<span data-ttu-id="44f8f-120">Yra keli būdai kurti projektą iš projekto šablono:</span><span class="sxs-lookup"><span data-stu-id="44f8f-120">There are several ways to create a project from a project template:</span></span>

- <span data-ttu-id="44f8f-121">Kurdami projektą pagal pasiūlymą, projekto šabloną galite pasirinkti dialogo lange **Spartusis kūrimas: Projektas**.</span><span class="sxs-lookup"><span data-stu-id="44f8f-121">When you create a project from a quote, you can select a project template in the **Quick Create: Project** dialog box.</span></span>

> ![Dialogo langas „Spartusis kūrimas: Projektas“](media/project-11.png)

- <span data-ttu-id="44f8f-123">Kai kuriate projektą pasirinkdami **Naujas projektas**, puslapis **Projektas** bus rodomas prieš įrašant įrašą.</span><span class="sxs-lookup"><span data-stu-id="44f8f-123">When you create a project by selecting **New Project**, the **Project** page appears before the record is saved.</span></span> <span data-ttu-id="44f8f-124">Lauke **išrinkti šabloną** pasirinkite vieną iš anksto nustatytų projekto šablonų organizacijoje.</span><span class="sxs-lookup"><span data-stu-id="44f8f-124">In the **Pick a Template** field, select one of the predefined project templates in the organization.</span></span>
- <span data-ttu-id="44f8f-125">Naudokite **Kurti projektą pagal šabloną** puslapyje **Šablono objektas**.</span><span class="sxs-lookup"><span data-stu-id="44f8f-125">Use **Create Project from a Template** on the **Template Entity** page.</span></span>

## <a name="copying-components-of-template-to-project"></a><span data-ttu-id="44f8f-126">Šablono komponentų kopijavimas į projektą</span><span class="sxs-lookup"><span data-stu-id="44f8f-126">Copying components of template to project</span></span>

<span data-ttu-id="44f8f-127">Kai į projektą kopijuojate projekto šablono komponentus, gali atsirasti kelių perrašymų, atsižvelgiant į projekto parametrus.</span><span class="sxs-lookup"><span data-stu-id="44f8f-127">When you copy the components of a project template to a project, a few overrides can occur, depending on the settings in the project.</span></span>

### <a name="copying-the-schedule"></a><span data-ttu-id="44f8f-128">Grafiko kopijavimas</span><span class="sxs-lookup"><span data-stu-id="44f8f-128">Copying the schedule</span></span>

<span data-ttu-id="44f8f-129">Kai kopijuojate grafiką iš projekto šablono, jei projekte nurodytas kitas projekto kalendorius nei šablone, projekto kalendoriaus darbo valandos taikomos užduočių grafikui.</span><span class="sxs-lookup"><span data-stu-id="44f8f-129">When you copy the schedule from a project template, if the project has a different project calendar than the template, work hours from the project's calendar are applied to the task schedule.</span></span> <span data-ttu-id="44f8f-130">Tokiu būdu grafikas yra pakoreguojamas pagal atsarginį projekto kalendorių.</span><span class="sxs-lookup"><span data-stu-id="44f8f-130">In this way, the schedule is adjusted to match the backing project calendar.</span></span> <span data-ttu-id="44f8f-131">Panašiai pirmoji užduotis grafike perima projekto pradžios datą, todėl likusios užduočių hierarchijos grafikas yra atnaujinamas pagal trukmę ir priklausomybes, nurodytas šablone.</span><span class="sxs-lookup"><span data-stu-id="44f8f-131">Similarly, the first task on the schedule takes the project's start date, and the schedule of the rest of the hierarchy is updated based on the duration and dependencies that are specified in the template.</span></span> 

### <a name="copying-project-estimates"></a><span data-ttu-id="44f8f-132">Projekto įvertinimų kopijavimas</span><span class="sxs-lookup"><span data-stu-id="44f8f-132">Copying project estimates</span></span> 

<span data-ttu-id="44f8f-133">Kai kopijuojate projekto įvertinimo eilutes, kainoraščiai naujinami.</span><span class="sxs-lookup"><span data-stu-id="44f8f-133">When you copy across project estimate lines, the price lists are updated.</span></span> <span data-ttu-id="44f8f-134">Kalbant apie savikainos kainoraštį, šie naujinimai priklauso nuo projektą valdančio vieneto.</span><span class="sxs-lookup"><span data-stu-id="44f8f-134">For the cost price list, these updates are based on the owning unit of the project.</span></span> <span data-ttu-id="44f8f-135">O kalbant apie pardavimo kainoraštį, jie priklauso nuo kliento.</span><span class="sxs-lookup"><span data-stu-id="44f8f-135">For the sales price list, they are based on the customer.</span></span> <span data-ttu-id="44f8f-136">Galiausiai, kalbant apie projektus, susietus su pardavimo objektu, vieneto savikaina ir pardavimo kainomis, jie nustatomi pagal minėtus kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="44f8f-136">For projects that are associated with a sales entity, the unit cost and sales prices are determined based on these price lists.</span></span>

### <a name="copying-a-project-team"></a><span data-ttu-id="44f8f-137">Projekto komandos kopijavimas</span><span class="sxs-lookup"><span data-stu-id="44f8f-137">Copying a project team</span></span>

<span data-ttu-id="44f8f-138">Kopijuojant projekto komandą iš šablono į projektą, nukopijuojami bendrieji ištekliai bei jos įgūdžiai ir kvalifikacija, nurodyti šablone.</span><span class="sxs-lookup"><span data-stu-id="44f8f-138">When a project team is copied from a project template to a project, the generic resources are copied, together with the skills and proficiencies that are defined in the template.</span></span> <span data-ttu-id="44f8f-139">Bendrųjų išteklių priskyrimai taip pat tvarkomi kaip ir projekto šablone.</span><span class="sxs-lookup"><span data-stu-id="44f8f-139">Generic resource assignments are also maintained as they were in the project template.</span></span> <span data-ttu-id="44f8f-140">Įvardyti ištekliai nepalaikomi projektų šablonuose.</span><span class="sxs-lookup"><span data-stu-id="44f8f-140">Named resources aren't supported in project templates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]