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
ms.openlocfilehash: e6b63ccb5b0f04dedb8a942e22d6e1993204dc20
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288575"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="7b6b7-103">Išteklių pajėgumo sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="7b6b7-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7b6b7-104">Išteklių sinchronizavimo procesai padeda užtikrinti, kad kalendoriaus ir pagrindinio kalendoriaus informacija naudojama planuojant projekto išteklius.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="7b6b7-105">Jei pakeičiamas kalendorius, procesai atlieka reikiamus projekto išteklių planavimo atnaujinimus.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="7b6b7-106">Procesai taip pat padeda gerinti efektyvumą, nes kalendoriaus išteklių informacija sinchronizuojama iš anksto.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="7b6b7-107">Todėl išteklių planavimo informacija atnaujinama greičiau.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="7b6b7-108">Rekomenduojame planuoti procesus kaip paketą, o ne po vieną.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="7b6b7-109">Priešingu atveju kyla pavojus, kad kas nors pamirš įtraukti paskutinį kartą sinchronizuotos informacijos datas.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="7b6b7-110">Jei paskutinį kartą nurodytos datos nebus naudojamos, sinchronizuojant datas gali atsirasti tarpų.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![Kalendoriaus sinchronizavimas](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="7b6b7-112">Išteklių pajėgumų sumavimų sinchronizavimas</span><span class="sxs-lookup"><span data-stu-id="7b6b7-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="7b6b7-113">Sinchronizavimo procesas skirtas visai išteklių kalendoriaus informacijai sinchronizuoti.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="7b6b7-114">Į šią informacija įtraukta pagrindinio kalendoriaus informacija apie visus projekto išteklių kalendoriaus pajėgumo lentelės pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="7b6b7-115">Jei į projektą įtraukiami nauji ištekliai, sinchronizavimas padeda užtikrinti, kad atnaujinta kalendoriaus informacija yra pasiekiama.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="7b6b7-116">Šis sinchronizavimas gali būti atliktas bet kuriuo metu.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="7b6b7-117">Rekomenduojame naudoti paketą.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-117">We recommend that you use a batch.</span></span> <span data-ttu-id="7b6b7-118">Šios parinktys yra pasiekiamos pajėgumų rezervavimų sinchronizavimo metu.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="7b6b7-119">Pasirinkite **Projektų valdymas ir apskaita** &gt; **Periodinis** &gt; **Pajėgumų sinchronizavimas** &gt; **Išteklių pajėgumų sumavimų sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="7b6b7-120">Nustatykite parinktis toliau pateiktoje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="7b6b7-121">Parinktis</span><span class="sxs-lookup"><span data-stu-id="7b6b7-121">Option</span></span>      | <span data-ttu-id="7b6b7-122">Aprašo</span><span class="sxs-lookup"><span data-stu-id="7b6b7-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="7b6b7-123">Laikotarpio kodas</span><span class="sxs-lookup"><span data-stu-id="7b6b7-123">Period code</span></span> | <span data-ttu-id="7b6b7-124">Arba pasirinkite didžiosios knygos datų intervalo kodą, kad nustatytumėte išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios ir pabaigos datas.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="7b6b7-125">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="7b6b7-125">Start date</span></span>  | <span data-ttu-id="7b6b7-126">Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="7b6b7-127">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="7b6b7-127">End date</span></span>    | <span data-ttu-id="7b6b7-128">Įveskite išteklių pajėgumų sumavimų sinchronizavimo proceso pabaigos datą.</span><span class="sxs-lookup"><span data-stu-id="7b6b7-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="7b6b7-129">[![Sinchronizavimo procesas](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="7b6b7-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]