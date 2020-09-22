---
title: Projekto darbo įvertinimų teikimas pardavimo proceso metu
description: Projekto darbo įvertinimų teikimas pardavimo proceso metu „Project Service“
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 8e6fbba8-2908-4555-9470-43c37e66efea
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8edb91010dd1227bc7947b59664d08430c219638
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753753"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="9b413-103">Projekto darbo įvertinimų teikimas pardavimo proceso metu („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="9b413-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="9b413-104">Pardavimo proceso metu galima apskaičiuoti pardavimo įvertinimus iš esmės pagal pasiūlymo eilutes.</span><span class="sxs-lookup"><span data-stu-id="9b413-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> <span data-ttu-id="9b413-105">„[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ galimybės programoje „[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]” teikia moksliškesnį ir labiau determinuotą būdą pardavimo įvertinimams apskaičiuoti skirstant darbo elementus ir siejant atitinkamus atributus, kurie prisideda vertinant projekto darbo paskirstymo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="9b413-105">[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="9b413-106">Laimėjus pardavimą, susijusią darbo paskirstymo struktūrą galima naudoti projekto plane, reikiamai patobulinus siekiant sėkmingai užbaigti projektą.</span><span class="sxs-lookup"><span data-stu-id="9b413-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="9b413-107">Projekto siejimas su pasiūlymo eilute</span><span class="sxs-lookup"><span data-stu-id="9b413-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="9b413-108">Kurdami projektu grindžiamą pasiūlymo eilutę, galite sukurti naują projektą iš pasiūlymo eilutės.</span><span class="sxs-lookup"><span data-stu-id="9b413-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="9b413-109">Tuomet galite naudoti projekto šablonus, kurie yra arba iš anksto sukonfigūruoti standartiniai projekto planai ir jūsų organizacijai įprastos finansinės sąmatos, arba projekto plano kopija ir ankstesnio projekto įvertinimai.</span><span class="sxs-lookup"><span data-stu-id="9b413-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="9b413-110">Kuriant projektą pasirinktas projekto šablonas suteikia pagrindą patobulinti projekto planą, įvertinimus ir vaidmenų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="9b413-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="9b413-111">Kuriant projektą iš pasiūlymo, jis yra automatiškai susiejamas su pasiūlymo eilute.</span><span class="sxs-lookup"><span data-stu-id="9b413-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="9b413-112">Projekto įvertinimo komponentai</span><span class="sxs-lookup"><span data-stu-id="9b413-112">Project estimate components</span></span>  
 <span data-ttu-id="9b413-113">Projekto darbo paskirstymo struktūra leidžia suskirstyti darbą į užduotis, palaikyti užduočių hierarchiją ir priskirti užduočiai įvykdyti reikalingų pastangų įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="9b413-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="9b413-114">Taip pat galima susieti vaidmenis su užduotimi, siekiant nurodyti išteklių, reikalingų užduočiai užbaigti, tipo įvertinimą ir grafiką.</span><span class="sxs-lookup"><span data-stu-id="9b413-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="9b413-115">Darbo paskirstymo struktūra padeda nustatyti darbo pastangas ir suplanuoti įvertinimus.</span><span class="sxs-lookup"><span data-stu-id="9b413-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="9b413-116">Pagal numatytuosius parametrus projektui naudojami anksčiau apibrėžti numatytieji kainoraščiai.</span><span class="sxs-lookup"><span data-stu-id="9b413-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="9b413-117">Savikaina ir pardavimo kainos, nurodytos kainoraštyje, padeda sudaryti finansines projekto darbo paskirstymo sąmatas.</span><span class="sxs-lookup"><span data-stu-id="9b413-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="9b413-118">Jei projektas yra susietas su pasiūlymu, o pasiūlymo kainoraštis skiriasi nuo numatytojo, finansinėms sąmatoms naudojamas pasiūlymo kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="9b413-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="9b413-119">Įvertinimų importavimas iš projekto į pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="9b413-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="9b413-120">Sudarę projekto įvertinimus, galite juos importuoti į pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="9b413-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="9b413-121">Srityje **Pasiūlymo eilutės informacija** spustelėkite **Importuoti iš įvertinimų**.</span><span class="sxs-lookup"><span data-stu-id="9b413-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="9b413-122">Pasirinkite, ar importuoti projekto įvertinimus, susumuotus pagal operacijos tipą, vaidmenį ar darbo paskirstymo struktūros mazgo lygį.</span><span class="sxs-lookup"><span data-stu-id="9b413-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="9b413-123">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="9b413-123">See Also</span></span>  
 [<span data-ttu-id="9b413-124">Projekto vadovo vadovas</span><span class="sxs-lookup"><span data-stu-id="9b413-124">Project Manager Guide</span></span>](../project-service/project-manager-guide.md)
