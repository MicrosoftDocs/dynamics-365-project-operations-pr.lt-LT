---
title: Išteklių pajėgumo sinchronizavimas
description: Šioje temoje pateikta informacija, kaip sinchronizuoti ištekliaus pajėgumą kalendoriuose ir projektuose.
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 006ebbfea42572f17663fab324a20a10321b78f0
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080814"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="5a274-103">Išteklių pajėgumo sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="5a274-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5a274-104">Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija naudojama planuojant projekto išteklius.</span><span class="sxs-lookup"><span data-stu-id="5a274-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="5a274-105">Jei pakeičiamas kalendorius, procesai atlieka reikiamus projekto išteklių planavimo atnaujinimus.</span><span class="sxs-lookup"><span data-stu-id="5a274-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="5a274-106">Procesai taip pat padeda gerinti efektyvumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto.</span><span class="sxs-lookup"><span data-stu-id="5a274-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="5a274-107">Todėl išteklių planavimo informacija atnaujinama greičiau.</span><span class="sxs-lookup"><span data-stu-id="5a274-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="5a274-108">Rekomenduojame planuoti procesus kaip paketą, o ne po vieną.</span><span class="sxs-lookup"><span data-stu-id="5a274-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="5a274-109">Priešingu atveju kyla pavojus, kad kas nors pamirš įtraukti paskutinį kartą sinchronizuotos informacijos datas.</span><span class="sxs-lookup"><span data-stu-id="5a274-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="5a274-110">Jei paskutinį kartą nurodytos datos nebus naudojamos, sinchronizuojant datas gali atsirasti tarpų.</span><span class="sxs-lookup"><span data-stu-id="5a274-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendoriaus sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="5a274-112">Išteklių pajėgumų sumavimų sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="5a274-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="5a274-113">Sinchronizavimo procesas skirtas visai išteklių kalendoriaus informacijai sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="5a274-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="5a274-114">Į šią informacija įtraukta pagrindinio kalendoriaus informacija apie visus projekto išteklių kalendoriaus pajėgumo lentelės pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="5a274-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="5a274-115">Jei į projektą įtraukiami nauji ištekliai, sinchronizavimas padeda užtikrinti, kad atnaujinta kalendoriaus informacija yra pasiekiama.</span><span class="sxs-lookup"><span data-stu-id="5a274-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="5a274-116">Šis sinchronizavimas gali būti atliktas bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="5a274-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="5a274-117">Rekomenduojame naudoti paketą.</span><span class="sxs-lookup"><span data-stu-id="5a274-117">We recommend that you use a batch.</span></span> <span data-ttu-id="5a274-118">Šios parinktys yra pasiekiamos pajėgumų rezervavimų sinchronizavimo metu.</span><span class="sxs-lookup"><span data-stu-id="5a274-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="5a274-119">Pasirinkite **Projektų valdymas ir apskaita** &gt; **Periodinis** &gt; **Pajėgumų sinchronizavimas** &gt; **Išteklių pajėgumų sumavimų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="5a274-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="5a274-120">Nustatykite parinktis toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="5a274-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="5a274-121">Parinktis</span><span class="sxs-lookup"><span data-stu-id="5a274-121">Option</span></span>      | <span data-ttu-id="5a274-122">Aprašo</span><span class="sxs-lookup"><span data-stu-id="5a274-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="5a274-123">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="5a274-123">Period code</span></span> | <span data-ttu-id="5a274-124">Arba pasirinkite didžiosios knygos datų intervalo kodą, kad nustatytumėte išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="5a274-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="5a274-125">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="5a274-125">Start date</span></span>  | <span data-ttu-id="5a274-126">Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="5a274-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="5a274-127">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="5a274-127">End date</span></span>    | <span data-ttu-id="5a274-128">Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="5a274-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="5a274-129">[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="5a274-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>
