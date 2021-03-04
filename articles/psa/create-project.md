---
title: Projekto kūrimas
description: Projekto kūrimas „Project Service“
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/13/2020
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
ms.openlocfilehash: 93958f8e7654ebc4cb038ba7ca0c5e4e02f39937
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148878"
---
# <a name="create-a-project-project-service"></a><span data-ttu-id="e0e44-103">Projekto kūrimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="e0e44-103">Create a project (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="e0e44-104">Sukurkite projektą naudodami „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ galimybes programoje „[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]“, kai norite sukurti projektinių paslaugų galimybę, pasiūlymą ar sutartį.</span><span class="sxs-lookup"><span data-stu-id="e0e44-104">Create a project using the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] when you want to create an opportunity, quote, or contract for project-based services.</span></span> <span data-ttu-id="e0e44-105">„[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ galimybės padeda tvarkyti projektą nuo galimybės iki užbaigimo.</span><span class="sxs-lookup"><span data-stu-id="e0e44-105">The [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities help you manage your project from opportunity through completion.</span></span> <span data-ttu-id="e0e44-106">Kai sukuriate projektą, taip pat sukuriate darbo paskirstymo struktūrą, kuri turi įtakos jūsų pasiūlymams, išlaidų sąmatoms ir išteklių valdymui.</span><span class="sxs-lookup"><span data-stu-id="e0e44-106">When you create a project, you’ll also create a work breakdown structure, which affects your quotes, cost estimates, and resource management.</span></span>  
  
1.  <span data-ttu-id="e0e44-107">Pasirinkite **Project Service > Projektai**.</span><span class="sxs-lookup"><span data-stu-id="e0e44-107">Go to **Project Service > Projects**.</span></span>  
  
2.  <span data-ttu-id="e0e44-108">Spustelėkite **Naujas projektas**.</span><span class="sxs-lookup"><span data-stu-id="e0e44-108">Click **New Project**.</span></span>  
  
3.  <span data-ttu-id="e0e44-109">Srityje **Santrauka** įveskite projekto pavadinimą, tada užpildykite kuo daugiau informacijos.</span><span class="sxs-lookup"><span data-stu-id="e0e44-109">In the **Summary** area, enter a name for your project, and then fill in as many of the details as you can.</span></span> <span data-ttu-id="e0e44-110">Būtini užpildyti elementai pažymėti raudona žvaigždute (\*).</span><span class="sxs-lookup"><span data-stu-id="e0e44-110">Items marked with a red asterisk (\*) are required.</span></span>  
  
4.  <span data-ttu-id="e0e44-111">Spustelėkite **Įrašyti**, kad sukurtumėte projektą, kurį vėliau galėsite redaguoti.</span><span class="sxs-lookup"><span data-stu-id="e0e44-111">Click **Save** to create your project so you can continue editing it.</span></span>  
  
<span data-ttu-id="e0e44-112">Tada sukursite projekto darbo paskirstymo struktūrą, kuri apibrėš projektui reikalingas užduotis, laiką ir išteklių vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="e0e44-112">Next, you’ll create a work breakdown structure for your project to define the tasks, timing, and resource roles needed for the project.</span></span>  

> [!NOTE]
> <span data-ttu-id="e0e44-113">Kai planuojate, „Project Service Automation“ atsižvelgia į **Darbo valandų** priskirtos laiko juostos šabloną.</span><span class="sxs-lookup"><span data-stu-id="e0e44-113">When scheduling, Project Service Automation respects the time zone of the applied **Work Hour** template.</span></span> <span data-ttu-id="e0e44-114">Vis dėlto, peržiūrint grafiko užduotis, užduoties pradžios ir laiko datos bus rodomos naudotojo laiko juostoje.</span><span class="sxs-lookup"><span data-stu-id="e0e44-114">However, when viewing the schedule tasks, the start and end dates of a task will be displayed in the user's time zone.</span></span> <span data-ttu-id="e0e44-115">Tai galioja kitiems laiko etapų rodiniams **projekto** formoje.</span><span class="sxs-lookup"><span data-stu-id="e0e44-115">This applies to other time-phased views in the **Project** form.</span></span> <span data-ttu-id="e0e44-116">Jei naudotojo laiko juosta neatitinka projektui taikomo darbo valandų šablono laiko juostos, atsiras skirtumą nurodantis įspėjimas. </span><span class="sxs-lookup"><span data-stu-id="e0e44-116">If the user's time zone does not match the time zone of the work hour template applied to the project, a warning which explains the difference will occur.</span></span> 
  
### <a name="see-also"></a><span data-ttu-id="e0e44-117">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="e0e44-117">See Also</span></span>  
 [<span data-ttu-id="e0e44-118">Projekto vadovo vadovas</span><span class="sxs-lookup"><span data-stu-id="e0e44-118">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
