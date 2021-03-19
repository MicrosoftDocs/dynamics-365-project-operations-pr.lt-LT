---
title: Projekto etapai
description: Šioje temoje pateikta informacija apie „Microsoft Dynamics Project Operations“ projektų etapus.
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: a5c695e0cd39f8a222e719cc6c9ffe984fe80b07
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286798"
---
# <a name="project-stages"></a><span data-ttu-id="4ae7b-103">Projekto etapai</span><span class="sxs-lookup"><span data-stu-id="4ae7b-103">Project stages</span></span>

<span data-ttu-id="4ae7b-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="4ae7b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4ae7b-105">Projekto etapai sukurti atspindėti projekto būseną, kol jis yra vykdomas.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="4ae7b-106">Tinkinimą galima naudoti automatiškai atnaujinant etapus su verslo procesų srautais, Power Automate arba priedų plėtiniais.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="4ae7b-107">Toliau nurodyti etapai nustatomi numatytojoje veiklos proceso sekoje:</span><span class="sxs-lookup"><span data-stu-id="4ae7b-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="4ae7b-108">Kurti</span><span class="sxs-lookup"><span data-stu-id="4ae7b-108">New</span></span>
- <span data-ttu-id="4ae7b-109">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="4ae7b-109">Quote</span></span>
- <span data-ttu-id="4ae7b-110">Planas</span><span class="sxs-lookup"><span data-stu-id="4ae7b-110">Plan</span></span>
- <span data-ttu-id="4ae7b-111">Pristatyti</span><span class="sxs-lookup"><span data-stu-id="4ae7b-111">Deliver</span></span>
- <span data-ttu-id="4ae7b-112">Užbaigti</span><span class="sxs-lookup"><span data-stu-id="4ae7b-112">Complete</span></span>
- <span data-ttu-id="4ae7b-113">Uždaryti objektą </span><span class="sxs-lookup"><span data-stu-id="4ae7b-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="4ae7b-114">Kurti</span><span class="sxs-lookup"><span data-stu-id="4ae7b-114">New</span></span>

<span data-ttu-id="4ae7b-115">Kuriant projektą, projekto etapas nustatomas į **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="4ae7b-116">Jei projektas buvo sukurtas pagal šabloną, jis gali turėti grafiką, sąmatą ir komandos duomenis.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="4ae7b-117">Kitaip tai yra projekto planas, o likusius komponentus reikia įvesti.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="4ae7b-118">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="4ae7b-118">Quote</span></span>

<span data-ttu-id="4ae7b-119">Kai projektą susiejate su pasiūlymu ar jį sukuriate iš pasiūlymo, projekto etapas nustatomas į **Pasiūlymas**, taip pat atnaujinamos numatomos pradžios bei pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="4ae7b-120">Kai projektas yra etape **Pasiūlymas**, skirtuke **Pardavimas**, puslapyje **Projekto objektas**, rodoma išsami informacija apie pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="4ae7b-121">Planas</span><span class="sxs-lookup"><span data-stu-id="4ae7b-121">Plan</span></span>

<span data-ttu-id="4ae7b-122">Kai laimite su projektu susietą pasiūlymą ir kai bendravimas išsiplėtoja iki etapo **Sutartis**, projekto etapas atnaujinamas į **Planas**.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="4ae7b-123">Kai projektas yra etape **Pasiūlymas**, puslapyje **Projekto objektas** rodoma išsami informacija apie sutartį.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="4ae7b-124">Pristatyti</span><span class="sxs-lookup"><span data-stu-id="4ae7b-124">Deliver</span></span>

<span data-ttu-id="4ae7b-125">Kai projekto planas bus baigtas ir esate pasirengę pradėti projektą, projekto vadovas turėtų atnaujinti projekto etapą į **Pristatyti**, kad parodytų, jog projektas pradėtas.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="4ae7b-126">Užbaigti</span><span class="sxs-lookup"><span data-stu-id="4ae7b-126">Complete</span></span> 

<span data-ttu-id="4ae7b-127">Kai projekto veikla baigiama, projektų vadovas gali atnaujinti etapą į **Užbaigti**.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="4ae7b-128">Atnaujindamas projekto etapą į **Užbaigti**, projekto vadovas nurodo, kad darbai yra visiškai užbaigti, tačiau projektas yra atviras, kad būtų galima įrašyti visus laukiančius laiko arba išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="4ae7b-129">Uždaryti</span><span class="sxs-lookup"><span data-stu-id="4ae7b-129">Close</span></span>

<span data-ttu-id="4ae7b-130">Kai visos projekto operacijos įrašytos, projektų vadovas gali atnaujinti etapą **Uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="4ae7b-131">Po to, jokių operacijų nebus galima įrašyti, o projektas nustatomas tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="4ae7b-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]