---
title: Projekto būsenos sekimas
description: Kaip sekti projekto būseną „Project Service“
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
ms.openlocfilehash: e9c8b594d468016264d0b4d9745597a35f55e50e
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149598"
---
# <a name="track-a-projects-status-project-service"></a><span data-ttu-id="7f8ad-103">Sekite projekto būseną („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="7f8ad-103">Track a project’s status (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="7f8ad-104">Naudodami „[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]‟ galite sekti kliento projekto eigą.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-104">Use the [!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)] to track the progress of a client’s project.</span></span>  

<span data-ttu-id="7f8ad-105">Bendravimui plėtojantis, projekto etapai atnaujinami, siekiant atspindėti bendravimo etapą.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-105">As the engagement progresses, the project stages update to reflect the stage of the engagement:</span></span>  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   <span data-ttu-id="7f8ad-106">**Naujas**</span><span class="sxs-lookup"><span data-stu-id="7f8ad-106">**New**</span></span>    | <span data-ttu-id="7f8ad-107">Kuriant projektą, etapas nustatomas į **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-107">When you create a project, the stage is set to **New**.</span></span> <span data-ttu-id="7f8ad-108">Jei projektą sukūrėte iš šablono, šiame etape projektas gali turėti grafiką, sąmatas ir komandos duomenis.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-108">If you created the project from a template, at this stage the project may have a schedule, estimates, and team data.</span></span> <span data-ttu-id="7f8ad-109">Priešingu atveju tai bus projekto schema, ir jums reikės rankiniu būdu įvesti likusius projekto komponentus.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-109">Otherwise, it will be the outline of the project and you need to manually enter the rest of the project components.</span></span> |
|  <span data-ttu-id="7f8ad-110">**Pasiūlymas**</span><span class="sxs-lookup"><span data-stu-id="7f8ad-110">**Quote**</span></span>   |      <span data-ttu-id="7f8ad-111">Kai projektą susiejate su pasiūlymu ar jį sukuriate iš pasiūlymo, projekto etapas nustatomas į **Pasiūlymas**, ir taip pat atnaujinamos numatomos pradžios bei pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-111">When you associate a project to a quote or create it from a quote, the project stage is set to **Quote**, and the estimated start and end datesare updated as well.</span></span> <span data-ttu-id="7f8ad-112">Kai projektas yra pasiūlymo etape, pasiūlymo informacija rodoma **Projekto** puslapio skirtuke **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-112">When the project is in the quote stage, details on the quote display on the **Sales** tab on the **Project** page.</span></span>      |
|   <span data-ttu-id="7f8ad-113">**Planas**</span><span class="sxs-lookup"><span data-stu-id="7f8ad-113">**Plan**</span></span>   |                                     <span data-ttu-id="7f8ad-114">Kai laimite su projektu susietą pasiūlymą, ir kai bendravimas išsiplėtoja iki sutarties etapo, projekto etapas atnaujinamas į **Planas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-114">When you win a quote associated with a project, and when the engagement progresses to the contract stage, the project stage updates to **Plan**.</span></span> <span data-ttu-id="7f8ad-115">Sutarties informacija rodoma **Projekto** puslapio skirtuke **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-115">Contract details display on the **Sales** tab on the **Project** page.</span></span>                                      |
| <span data-ttu-id="7f8ad-116">**Atlikti**</span><span class="sxs-lookup"><span data-stu-id="7f8ad-116">**Complete**</span></span> |                    <span data-ttu-id="7f8ad-117">Kai projekto darbas baigtas, etapą galite nustatyti į **Baigtas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-117">When the project work is complete, you can flip the stage to **Complete**.</span></span> <span data-ttu-id="7f8ad-118">Kai nustatytas baigtas projekto etapas, suprantama, kad darbas 100 proc. baigtas, bet projektas lieka atidarytas, kad būtų galima įrašyti laukimo laiko ar išlaidų įrašų.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-118">When the project stage is set to complete, it’s understood that the work is 100% complete but the project is kept open for any pending time or expense entries to be recorded.</span></span>                     |
|  <span data-ttu-id="7f8ad-119">**Uždaryti**</span><span class="sxs-lookup"><span data-stu-id="7f8ad-119">**Close**</span></span>   |           <span data-ttu-id="7f8ad-120">Kai įrašytos visos projekto operacijos, ir nemanote, kad jų bus daugiau, etapą galite rankiniu būdu nustatyti į **Uždarytas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-120">When all transactions have been recorded on the project and you don't expect any more to be logged, you can manually set the stage to **Close**.</span></span> <span data-ttu-id="7f8ad-121">Kai projektas nustatytas į **Uždarytas**, jame registruoti operacijų nebegalite, ir projektą bus galima tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-121">When the project is set to **Close**, you can’t log any more transactions on the project and the project will be read only.</span></span>           |

## <a name="to-track-a-projects-status"></a><span data-ttu-id="7f8ad-122">Norėdami sekti projekto būseną</span><span class="sxs-lookup"><span data-stu-id="7f8ad-122">To track a project’s status</span></span>  

1.  <span data-ttu-id="7f8ad-123">Pasirinkite **Project Service > Projektai**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-123">Go to **Project Service > Projects**.</span></span>  

2.  <span data-ttu-id="7f8ad-124">Spustelėkite projektą, su kuriuo norite dirbti.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-124">Click the project you want to work on.</span></span>  

3.  <span data-ttu-id="7f8ad-125">Juostoje ekrano viršuje pasirinkite žemyn nukreiptą rodyklę prie projekto pavadinimo, o tada spustelėkite **Projekto sekimas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-125">In the bar across the top of the screen, select the down arrow next to the project name, and then click **Project Tracking**.</span></span>  

4.  <span data-ttu-id="7f8ad-126">Išplečiamajame sąraše, esančiame virš užduočių sąrašo, pasirinkite **Pastangų sekimas** arba **Išlaidų sekimas**.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-126">Select **Effort Tracking** or **Cost Tracking** in the drop-down list above the task list.</span></span>  

5.  <span data-ttu-id="7f8ad-127">Norėdami redaguoti bet kurią užduotį, ją dukart spustelėkite.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-127">Double-click any task to edit it.</span></span> <span data-ttu-id="7f8ad-128">Taip pat galite perkelti Ganto diagramos juostas ar keisti jų dydį, kad pakeistumėte užduoties trukmę ir eigą.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-128">You can also move or resize the bars in the Gantt chart to change the time and progress for a task.</span></span>  

### <a name="see-also"></a><span data-ttu-id="7f8ad-129">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="7f8ad-129">See Also</span></span>  
 [<span data-ttu-id="7f8ad-130">Projekto vadovo vadovas</span><span class="sxs-lookup"><span data-stu-id="7f8ad-130">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
