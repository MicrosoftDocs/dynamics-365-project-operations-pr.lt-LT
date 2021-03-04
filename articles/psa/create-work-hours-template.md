---
title: Darbo valandų šablono kūrimas
description: Darbo valandų šablono kūrimas „Project Service“
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 54d7385a2bb161c7dd02d882090790debaef3bdb
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148788"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="4ef10-103">Darbo valandų šablono kūrimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="4ef10-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4ef10-104">Prieš kuriant projektų grafikus, reikia nustatyti projekto kalendorių, apibrėžiantį darbo valandų skaičių per dieną, atsižvelgiant į grafiką ir įmonės ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="4ef10-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="4ef10-105">Tai atliekama darbo valandų šablonu, kuriame pateikiama informacija apie darbo valandas per dieną, laisvadienius ir bet kokį kitą įmonės ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="4ef10-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="4ef10-106">Kurdami projektą, darbo šabloną susiejate su projekto kalendoriumi, kad grafikas būtų pritaikytas projektui.</span><span class="sxs-lookup"><span data-stu-id="4ef10-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="4ef10-107">Darbo valandų šabloną galite sukurti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="4ef10-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="4ef10-108">Darbo valandų šabloną kurti pagal ištekliaus kalendorių.</span><span class="sxs-lookup"><span data-stu-id="4ef10-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="4ef10-109">Sukurti naują darbo valandų šabloną.</span><span class="sxs-lookup"><span data-stu-id="4ef10-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="4ef10-110">Norėdami darbo valandų šabloną kurti pagal ištekliaus kalendorių</span><span class="sxs-lookup"><span data-stu-id="4ef10-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="4ef10-111">Pasirinkite **Project Service > Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="4ef10-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="4ef10-112">Pasirinkite išteklių, pagal kurį norite nustatyti darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="4ef10-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="4ef10-113">Spustelėkite **Įrašyti kalendorių kaip**, įveskite darbo valandų šablono pavadinimą ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4ef10-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="4ef10-114">Baigę keisti parinktis, spustelėkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="4ef10-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="4ef10-115">Viršutiniame dešiniajame ekrano kampe spustelėkite mygtuką **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4ef10-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="4ef10-116">Norėdami sukurti naują darbo valandų šabloną</span><span class="sxs-lookup"><span data-stu-id="4ef10-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="4ef10-117">Eikite į **Project Service > Darbo valandų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="4ef10-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="4ef10-118">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4ef10-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="4ef10-119">Įveskite darbo valandų šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="4ef10-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="4ef10-120">Pasirinkite išteklių, pagal kurį norite nustatyti darbo valandas ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4ef10-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="4ef10-121">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="4ef10-121">See Also</span></span>  
 [<span data-ttu-id="4ef10-122">Rezervuojamų išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="4ef10-122">Set up resources</span></span>](../psa/set-up-resources.md)
