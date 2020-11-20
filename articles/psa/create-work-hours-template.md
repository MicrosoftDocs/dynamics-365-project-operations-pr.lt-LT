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
ms.openlocfilehash: a0fce327587940e557e0214c8c0897116ac91901
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4133063"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="333d8-103">Darbo valandų šablono kūrimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="333d8-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="333d8-104">Prieš kuriant projektų grafikus, reikia nustatyti projekto kalendorių, apibrėžiantį darbo valandų skaičių per dieną, atsižvelgiant į grafiką ir įmonės ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="333d8-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="333d8-105">Tai atliekama darbo valandų šablonu, kuriame pateikiama informacija apie darbo valandas per dieną, laisvadienius ir bet kokį kitą įmonės ne darbo laiką.</span><span class="sxs-lookup"><span data-stu-id="333d8-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="333d8-106">Kurdami projektą, darbo šabloną susiejate su projekto kalendoriumi, kad grafikas būtų pritaikytas projektui.</span><span class="sxs-lookup"><span data-stu-id="333d8-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="333d8-107">Darbo valandų šabloną galite sukurti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="333d8-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="333d8-108">Darbo valandų šabloną kurti pagal ištekliaus kalendorių.</span><span class="sxs-lookup"><span data-stu-id="333d8-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="333d8-109">Sukurti naują darbo valandų šabloną.</span><span class="sxs-lookup"><span data-stu-id="333d8-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="333d8-110">Norėdami darbo valandų šabloną kurti pagal ištekliaus kalendorių</span><span class="sxs-lookup"><span data-stu-id="333d8-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="333d8-111">Pasirinkite **Project Service > Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="333d8-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="333d8-112">Pasirinkite išteklių, pagal kurį norite nustatyti darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="333d8-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="333d8-113">Spustelėkite **Įrašyti kalendorių kaip**, įveskite darbo valandų šablono pavadinimą ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="333d8-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="333d8-114">Baigę keisti parinktis, spustelėkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="333d8-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="333d8-115">Viršutiniame dešiniajame ekrano kampe spustelėkite mygtuką **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="333d8-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="333d8-116">Norėdami sukurti naują darbo valandų šabloną</span><span class="sxs-lookup"><span data-stu-id="333d8-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="333d8-117">Eikite į **Project Service > Darbo valandų šablonai**.</span><span class="sxs-lookup"><span data-stu-id="333d8-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="333d8-118">Spustelėkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="333d8-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="333d8-119">Įveskite darbo valandų šablono pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="333d8-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="333d8-120">Pasirinkite išteklių, pagal kurį norite nustatyti darbo valandas ir spustelėkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="333d8-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="333d8-121">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="333d8-121">See Also</span></span>  
 [<span data-ttu-id="333d8-122">Rezervuojamų išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="333d8-122">Set up resources</span></span>](../psa/set-up-resources.md)
