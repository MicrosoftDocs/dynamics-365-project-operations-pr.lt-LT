---
title: Planavimo pagalbinės priemonės apžvalga
description: Šioje temoje pateikta informacija, kaip naudojant planavimo pagalbinę priemonę rezervuoti išteklius.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080692"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="b3454-103">Planavimo pagalbinės priemonės apžvalga</span><span class="sxs-lookup"><span data-stu-id="b3454-103">Schedule assistant overview</span></span>

<span data-ttu-id="b3454-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="b3454-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b3454-105">Naudojant planavimo pagalbinę priemonę galima rezervuoti išteklius pagal projekto vadovo apibrėžtus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="b3454-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="b3454-106">Planavimo pagalbinė priemonė ieško išteklių pagal parametrus, pateiktus išteklių reikalavime.</span><span class="sxs-lookup"><span data-stu-id="b3454-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="b3454-107">Planavimo pagalbinė priemonė rekomenduoja išteklius, atitinkančius atitinkamus reikalavimus, pvz., laiko langus arba reikiamus įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="b3454-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="b3454-108">Nustačius tinkamus išteklius, išteklių arba projekto vadovas gali rezervuoti išteklius darbui.</span><span class="sxs-lookup"><span data-stu-id="b3454-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b3454-109">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="b3454-109">Prerequisites</span></span>

<span data-ttu-id="b3454-110">Planavimo pagalbinė priemonė yra „Universal Resource Scheduling“ sprendimo dalis.</span><span class="sxs-lookup"><span data-stu-id="b3454-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="b3454-111">Šis sprendimas yra įtrauktas ir įdiegiamas su „Dynamics 365 Project Operations“, „Dynamics 365 Field Service“ ir „Dynamics 365 Customer Service“.</span><span class="sxs-lookup"><span data-stu-id="b3454-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="b3454-112">Reikalavimų ir išteklių derinimas</span><span class="sxs-lookup"><span data-stu-id="b3454-112">Matching requirements and resources</span></span>

<span data-ttu-id="b3454-113">Sugeneruotas išteklių reikalavimas yra pagrįstas išsamia informacija, pvz.:</span><span class="sxs-lookup"><span data-stu-id="b3454-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="b3454-114">Charakteristikos</span><span class="sxs-lookup"><span data-stu-id="b3454-114">Characteristics</span></span>
-   <span data-ttu-id="b3454-115">Vaidmenys</span><span class="sxs-lookup"><span data-stu-id="b3454-115">Roles</span></span>
-   <span data-ttu-id="b3454-116">Verslo vienetai</span><span class="sxs-lookup"><span data-stu-id="b3454-116">Business units</span></span>
-   <span data-ttu-id="b3454-117">Ištekliaus nuostatos</span><span class="sxs-lookup"><span data-stu-id="b3454-117">Resource preferences</span></span>
-   <span data-ttu-id="b3454-118">Pastangų kontūrai</span><span class="sxs-lookup"><span data-stu-id="b3454-118">Effort contours</span></span>
-   <span data-ttu-id="b3454-119">Laiko juosta</span><span class="sxs-lookup"><span data-stu-id="b3454-119">Time zone</span></span>

<span data-ttu-id="b3454-120">Planavimo pagalbinė priemonė naudoja šią informaciją ištekliams filtruoti.</span><span class="sxs-lookup"><span data-stu-id="b3454-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="b3454-121">Planavimo pagalbinės priemonės paleidimas</span><span class="sxs-lookup"><span data-stu-id="b3454-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="b3454-122">Planavimo pagalbinę priemonę galima paleisti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="b3454-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="b3454-123">Jei naudojate hibridinį režimą, komandos narių tinklelyje galite pasirinkti bet kurį komandos narį, kuris netenkina ištekliaus reikalavimo, ir pasirinkti **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="b3454-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="b3454-124">Jei naudojate centralizuotą režimą, išteklių vadovas randa ir pasirenka išteklių.</span><span class="sxs-lookup"><span data-stu-id="b3454-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="b3454-125">Planavimo pagalbinės priemonės filtrai</span><span class="sxs-lookup"><span data-stu-id="b3454-125">Schedule assistant filters</span></span>

<span data-ttu-id="b3454-126">Paleidus planavimo pagalbinę priemonę, išsami išteklių reikalavimo informacija rodoma kaip filtruotos reikšmės kairiojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="b3454-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="b3454-127">Išteklių vadovas arba projekto vadovas gali patikslinti rezultatus koreguodamas filtrus pagal planavimo poreikius.</span><span class="sxs-lookup"><span data-stu-id="b3454-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="b3454-128">Filtro srityje rodomos su darbu susijusios parinktys, įskaitant:</span><span class="sxs-lookup"><span data-stu-id="b3454-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="b3454-129">Darbo pradžia ir pabaiga</span><span class="sxs-lookup"><span data-stu-id="b3454-129">Work start and end</span></span>
-   <span data-ttu-id="b3454-130">Charakteristikos</span><span class="sxs-lookup"><span data-stu-id="b3454-130">Characteristics</span></span>
-   <span data-ttu-id="b3454-131">Vaidmenys</span><span class="sxs-lookup"><span data-stu-id="b3454-131">Roles</span></span>
-   <span data-ttu-id="b3454-132">Organizaciniai vienetai</span><span class="sxs-lookup"><span data-stu-id="b3454-132">Organizational units</span></span>
-   <span data-ttu-id="b3454-133">Išteklių įmonė</span><span class="sxs-lookup"><span data-stu-id="b3454-133">Resourcing company</span></span>
-   <span data-ttu-id="b3454-134">Išteklių tipai</span><span class="sxs-lookup"><span data-stu-id="b3454-134">Resource types</span></span>
-   <span data-ttu-id="b3454-135">Pageidaujami ištekliai</span><span class="sxs-lookup"><span data-stu-id="b3454-135">Preferred resources</span></span>
