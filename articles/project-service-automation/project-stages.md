---
title: Projekto etapai
description: Šioje temoje pateikta informacija apie projektų etapus.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753670"
---
# <a name="project-stages"></a><span data-ttu-id="e9953-103">Projekto etapai</span><span class="sxs-lookup"><span data-stu-id="e9953-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e9953-104">Projekto etapai yra atnaujinti, kad atspindėtų projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="e9953-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="e9953-105">Numatytoji veiklos procesų seka automatiškai atnaujina keletą projekto etapų, o kitus rankiniu būdu atnaujina projekto vadovas.</span><span class="sxs-lookup"><span data-stu-id="e9953-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="e9953-106">Toliau nurodyti etapai nustatomi numatytojoje veiklos proceso sekoje:</span><span class="sxs-lookup"><span data-stu-id="e9953-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="e9953-107">Naujas</span><span class="sxs-lookup"><span data-stu-id="e9953-107">New</span></span>
- <span data-ttu-id="e9953-108">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="e9953-108">Quote</span></span>
- <span data-ttu-id="e9953-109">Planas</span><span class="sxs-lookup"><span data-stu-id="e9953-109">Plan</span></span>
- <span data-ttu-id="e9953-110">Pristatyti</span><span class="sxs-lookup"><span data-stu-id="e9953-110">Deliver</span></span>
- <span data-ttu-id="e9953-111">Užbaigti</span><span class="sxs-lookup"><span data-stu-id="e9953-111">Complete</span></span>
- <span data-ttu-id="e9953-112">Uždaryti</span><span class="sxs-lookup"><span data-stu-id="e9953-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="e9953-113">Naujas</span><span class="sxs-lookup"><span data-stu-id="e9953-113">New</span></span>

<span data-ttu-id="e9953-114">Kuriant projektą, projekto etapas nustatomas į **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="e9953-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="e9953-115">Jei projektas buvo sukurtas pagal šabloną, jis gali turėti grafiką, sąmatą ir komandos duomenis.</span><span class="sxs-lookup"><span data-stu-id="e9953-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="e9953-116">Kitaip tai tik projekto planas, o likusius komponentus reikia įvesti.</span><span class="sxs-lookup"><span data-stu-id="e9953-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="e9953-117">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="e9953-117">Quote</span></span>

<span data-ttu-id="e9953-118">Kai projektą susiejate su pasiūlymu ar jį sukuriate iš pasiūlymo, projekto etapas nustatomas į **Pasiūlymas**, taip pat atnaujinamos numatomos pradžios bei pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="e9953-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="e9953-119">Kai projektas yra etape **Pasiūlymas**, skirtuke **Pardavimas**, puslapyje **Projekto objektas**, rodoma išsami informacija apie pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="e9953-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="e9953-120">Planas</span><span class="sxs-lookup"><span data-stu-id="e9953-120">Plan</span></span>

<span data-ttu-id="e9953-121">Kai laimite su projektu susietą pasiūlymą ir kai bendravimas išsiplėtoja iki etapo **Sutartis**, projekto etapas atnaujinamas į **Planas**.</span><span class="sxs-lookup"><span data-stu-id="e9953-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="e9953-122">Kai projektas yra etape **Pasiūlymas**, puslapyje **Projekto objektas** rodoma išsami informacija apie sutartį.</span><span class="sxs-lookup"><span data-stu-id="e9953-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="e9953-123">Pristatyti</span><span class="sxs-lookup"><span data-stu-id="e9953-123">Deliver</span></span>

<span data-ttu-id="e9953-124">Kai projekto planas bus baigtas ir esate pasirengę pradėti projektą, projekto vadovas turėtų atnaujinti projekto etapą į **Pristatyti**, kad parodytų, jog projektas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="e9953-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="e9953-125">Užbaigti</span><span class="sxs-lookup"><span data-stu-id="e9953-125">Complete</span></span> 

<span data-ttu-id="e9953-126">Kai projekto veikla baigiama, projektų vadovas gali atnaujinti etapą į **Užbaigti**.</span><span class="sxs-lookup"><span data-stu-id="e9953-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="e9953-127">Atnaujindamas projekto etapą į **Užbaigti**, projekto vadovas nurodo, kad darbai yra visiškai užbaigti, tačiau projektas yra atviras, kad būtų galima įrašyti visus laukiančius laiko arba išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="e9953-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="e9953-128">Uždaryti</span><span class="sxs-lookup"><span data-stu-id="e9953-128">Close</span></span>

<span data-ttu-id="e9953-129">Kai visos projekto operacijos įrašytos, projektų vadovas gali atnaujinti etapą **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="e9953-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="e9953-130">Po to, jokių operacijų nebus galima įrašyti, o projektas nustatomas tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="e9953-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
