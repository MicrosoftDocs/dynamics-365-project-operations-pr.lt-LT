---
title: Projektų etapų tipai
description: Šioje temoje pateikta informacija apie projektų etapus.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 3503b17e54fc0b321582c30ce534e4cb3f497a5f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283693"
---
# <a name="project-stage-types"></a><span data-ttu-id="a5b73-103">Projektų etapų tipai</span><span class="sxs-lookup"><span data-stu-id="a5b73-103">Project stage types</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a5b73-104">Projekto etapai sukurti atspindėti projekto būseną, kol jis yra vykdomas.</span><span class="sxs-lookup"><span data-stu-id="a5b73-104">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="a5b73-105">Tinkinimą galima naudoti automatiškai atnaujinant etapus su verslo procesų srautais, Power Automate arba priedų plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="a5b73-105">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="a5b73-106">Toliau nurodyti etapai nustatomi numatytojoje veiklos proceso sekoje:</span><span class="sxs-lookup"><span data-stu-id="a5b73-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="a5b73-107">Nauja</span><span class="sxs-lookup"><span data-stu-id="a5b73-107">New</span></span>
- <span data-ttu-id="a5b73-108">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="a5b73-108">Quote</span></span>
- <span data-ttu-id="a5b73-109">Planas</span><span class="sxs-lookup"><span data-stu-id="a5b73-109">Plan</span></span>
- <span data-ttu-id="a5b73-110">Pristatyti</span><span class="sxs-lookup"><span data-stu-id="a5b73-110">Deliver</span></span>
- <span data-ttu-id="a5b73-111">Užbaigti</span><span class="sxs-lookup"><span data-stu-id="a5b73-111">Complete</span></span>
- <span data-ttu-id="a5b73-112">Uždaryti</span><span class="sxs-lookup"><span data-stu-id="a5b73-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="a5b73-113">Naujas</span><span class="sxs-lookup"><span data-stu-id="a5b73-113">New</span></span>

<span data-ttu-id="a5b73-114">Kuriant projektą, projekto etapas nustatomas į **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="a5b73-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="a5b73-115">Jei projektas buvo sukurtas pagal šabloną, jis gali turėti grafiką, sąmatą ir komandos duomenis.</span><span class="sxs-lookup"><span data-stu-id="a5b73-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="a5b73-116">Kitaip tai tik projekto planas, o likusius komponentus reikia įvesti.</span><span class="sxs-lookup"><span data-stu-id="a5b73-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="a5b73-117">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="a5b73-117">Quote</span></span>

<span data-ttu-id="a5b73-118">Kai projektą susiejate su pasiūlymu ar jį sukuriate iš pasiūlymo, projekto etapas nustatomas į **Pasiūlymas**, taip pat atnaujinamos numatomos pradžios bei pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="a5b73-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="a5b73-119">Kai projektas yra etape **Pasiūlymas**, skirtuke **Pardavimas**, puslapyje **Projekto objektas**, rodoma išsami informacija apie pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="a5b73-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="a5b73-120">Planas</span><span class="sxs-lookup"><span data-stu-id="a5b73-120">Plan</span></span>

<span data-ttu-id="a5b73-121">Kai laimite su projektu susietą pasiūlymą ir kai bendravimas išsiplėtoja iki etapo **Sutartis**, projekto etapas atnaujinamas į **Planas**.</span><span class="sxs-lookup"><span data-stu-id="a5b73-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="a5b73-122">Kai projektas yra etape **Pasiūlymas**, puslapyje **Projekto objektas** rodoma išsami informacija apie sutartį.</span><span class="sxs-lookup"><span data-stu-id="a5b73-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="a5b73-123">Pristatyti</span><span class="sxs-lookup"><span data-stu-id="a5b73-123">Deliver</span></span>

<span data-ttu-id="a5b73-124">Kai projekto planas bus baigtas ir esate pasirengę pradėti projektą, projekto vadovas turėtų atnaujinti projekto etapą į **Pristatyti**, kad parodytų, jog projektas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="a5b73-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="a5b73-125">Užbaigti</span><span class="sxs-lookup"><span data-stu-id="a5b73-125">Complete</span></span> 

<span data-ttu-id="a5b73-126">Kai projekto veikla baigiama, projektų vadovas gali atnaujinti etapą į **Užbaigti**.</span><span class="sxs-lookup"><span data-stu-id="a5b73-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="a5b73-127">Atnaujindamas projekto etapą į **Užbaigti**, projekto vadovas nurodo, kad darbai yra visiškai užbaigti, tačiau projektas yra atviras, kad būtų galima įrašyti visus laukiančius laiko arba išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="a5b73-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="a5b73-128">Uždaryti</span><span class="sxs-lookup"><span data-stu-id="a5b73-128">Close</span></span>

<span data-ttu-id="a5b73-129">Kai visos projekto operacijos įrašytos, projektų vadovas gali atnaujinti etapą **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="a5b73-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="a5b73-130">Po to, jokių operacijų nebus galima įrašyti, o projektas nustatomas tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="a5b73-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]