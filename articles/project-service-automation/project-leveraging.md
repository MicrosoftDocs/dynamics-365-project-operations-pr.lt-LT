---
title: Pardavimo sąmatos ir projektai
description: Šioje temoje pateikiama informacija apie tai, kaip pardavimo proceso metu pasinaudoti tvarkaraščio ir sąmatų privalumais.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: eb5ab6a1-fdff-490e-9c2a-19aef493de11
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 4431c1c894a01bfecc132575d8981ebc9fe50b51
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753674"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="792eb-103">Pardavimo sąmatos ir projektai</span><span class="sxs-lookup"><span data-stu-id="792eb-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="792eb-104">Pardavimo proceso metu galite kurti pardavimo sąmatas, susieję projektą su pardavimo pasiūlymu.</span><span class="sxs-lookup"><span data-stu-id="792eb-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="792eb-105">Tokiu būdu deterministinis vertinimas gali būti atliekamas pardavimo proceso metu, siekiant pasinaudoti projektų planavimo ir įvertinimo galimybėmis.</span><span class="sxs-lookup"><span data-stu-id="792eb-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="792eb-106">Jei pardavimas tęsiasi, grafiką, kuris buvo naudojamas pardavimo įvertinimo tikslams, galima naudoti kaip tolesnio projekto plano tobulinimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="792eb-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="792eb-107">Projekto siejimas su pasiūlymo eilute</span><span class="sxs-lookup"><span data-stu-id="792eb-107">Linking a project to a quote line</span></span>

<span data-ttu-id="792eb-108">Kurdami projektais pagrįstą pasiūlymo eilutę, galite sukurti naują projektą arba susieti esamą projektą PN **Pasiūlymo eilutės** puslapyje.</span><span class="sxs-lookup"><span data-stu-id="792eb-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![Pasiūlymo eilutės forma](media/project-8.png)
 
<span data-ttu-id="792eb-110">Kurdami naują projektą iš pasiūlymo eilutės informacijos galite pasinaudoti projektų šablonais.</span><span class="sxs-lookup"><span data-stu-id="792eb-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="792eb-111">Projektų šablonai yra modelio projektai, kurie atitinka standartinius organizacijos projekto planus ir finansines sąmatas.</span><span class="sxs-lookup"><span data-stu-id="792eb-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="792eb-112">Jie taip pat gali būti projektų planų ir ankstesnių projektų sąmatų kopijos.</span><span class="sxs-lookup"><span data-stu-id="792eb-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![Pasiūlymo eilučių informacija](media/project-9.png)
  
<span data-ttu-id="792eb-114">Kuriant projektą iš pasiūlymo, jis yra automatiškai susiejamas su pasiūlymo eilute.</span><span class="sxs-lookup"><span data-stu-id="792eb-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="792eb-115">Projekto sąmatos komponentai</span><span class="sxs-lookup"><span data-stu-id="792eb-115">Components of estimates in a project</span></span>

<span data-ttu-id="792eb-116">Grafike galite padalinti darbą į užduotis, prižiūrėti užduočių hierarchiją, nustatyti, kurių išteklių reikia norint užbaigti užduotį, ir priskirti pastangų, reikalingų užduočiai užbaigti, sąmatą.</span><span class="sxs-lookup"><span data-stu-id="792eb-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="792eb-117">Darbo pastangas ir grafiko sąmatas galite apibrėžti naudodami laukus, esančius skirtuke **Grafikas**, puslapyje **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="792eb-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="792eb-118">Kadangi kainoraštis susietas su projektu, finansinės sąmatos apskaičiuojamos naudojant kainoraštyje apibrėžtas savikainas ir pardavimo kainas.</span><span class="sxs-lookup"><span data-stu-id="792eb-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="792eb-119">Sąmatų importavimas iš projekto į pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="792eb-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="792eb-120">Nustatę projektų sąmatas galite importuoti jas į pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="792eb-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="792eb-121">Puslapyje **Pasiūlymo eilutės išsami informacija**, pažymėkite juostelėje **Importuoti iš sąmatų**, kad apibendrintumėte projektų sąmatas pagal operacijos tipą, vaidmenį arba užduoties lygį.</span><span class="sxs-lookup"><span data-stu-id="792eb-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
