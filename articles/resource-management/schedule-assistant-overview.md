---
title: Planavimo pagalbinės priemonės apžvalga
description: Šioje temoje pateikta informacija, kaip naudojant planavimo pagalbinę priemonę rezervuoti išteklius.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: e14dbe5abb69a547e2d09ef9e6bcba48e1f89455
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279238"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="e65b9-103">Planavimo pagalbinės priemonės apžvalga</span><span class="sxs-lookup"><span data-stu-id="e65b9-103">Schedule assistant overview</span></span>

<span data-ttu-id="e65b9-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="e65b9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e65b9-105">Naudojant planavimo pagalbinę priemonę galima rezervuoti išteklius pagal projekto vadovo apibrėžtus reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="e65b9-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="e65b9-106">Planavimo pagalbinė priemonė ieško išteklių pagal parametrus, pateiktus išteklių reikalavime.</span><span class="sxs-lookup"><span data-stu-id="e65b9-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="e65b9-107">Planavimo pagalbinė priemonė rekomenduoja išteklius, atitinkančius atitinkamus reikalavimus, pvz., laiko langus arba reikiamus įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="e65b9-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="e65b9-108">Nustačius tinkamus išteklius, išteklių arba projekto vadovas gali rezervuoti išteklius darbui.</span><span class="sxs-lookup"><span data-stu-id="e65b9-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e65b9-109">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="e65b9-109">Prerequisites</span></span>

<span data-ttu-id="e65b9-110">Planavimo pagalbinė priemonė yra „Universal Resource Scheduling“ sprendimo dalis.</span><span class="sxs-lookup"><span data-stu-id="e65b9-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="e65b9-111">Šis sprendimas įtrauktas ir įdiegtas su „Dynamics 365 Project Operations“, „Dynamics 365 Field Service“ ir „Dynamics 365 Customer Service“.</span><span class="sxs-lookup"><span data-stu-id="e65b9-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="e65b9-112">Reikalavimų ir išteklių derinimas</span><span class="sxs-lookup"><span data-stu-id="e65b9-112">Matching requirements and resources</span></span>

<span data-ttu-id="e65b9-113">Sugeneruotas išteklių reikalavimas yra pagrįstas išsamia informacija, pvz.:</span><span class="sxs-lookup"><span data-stu-id="e65b9-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="e65b9-114">Charakteristikos</span><span class="sxs-lookup"><span data-stu-id="e65b9-114">Characteristics</span></span>
-   <span data-ttu-id="e65b9-115">Vaidmenys</span><span class="sxs-lookup"><span data-stu-id="e65b9-115">Roles</span></span>
-   <span data-ttu-id="e65b9-116">Verslo vienetai</span><span class="sxs-lookup"><span data-stu-id="e65b9-116">Business units</span></span>
-   <span data-ttu-id="e65b9-117">Ištekliaus nuostatos</span><span class="sxs-lookup"><span data-stu-id="e65b9-117">Resource preferences</span></span>
-   <span data-ttu-id="e65b9-118">Pastangų kontūrai</span><span class="sxs-lookup"><span data-stu-id="e65b9-118">Effort contours</span></span>
-   <span data-ttu-id="e65b9-119">Laiko juosta</span><span class="sxs-lookup"><span data-stu-id="e65b9-119">Time zone</span></span>

<span data-ttu-id="e65b9-120">Planavimo pagalbinė priemonė naudoja šią informaciją ištekliams filtruoti.</span><span class="sxs-lookup"><span data-stu-id="e65b9-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="e65b9-121">Planavimo pagalbinės priemonės paleidimas</span><span class="sxs-lookup"><span data-stu-id="e65b9-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="e65b9-122">Planavimo pagalbinę priemonę galima paleisti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="e65b9-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="e65b9-123">Jei naudojate hibridinį režimą, komandos narių tinklelyje galite pasirinkti bet kurį komandos narį, kuris netenkina ištekliaus reikalavimo, ir pasirinkti **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="e65b9-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="e65b9-124">Jei naudojate centralizuotą režimą, išteklių vadovas randa ir pasirenka išteklių.</span><span class="sxs-lookup"><span data-stu-id="e65b9-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="e65b9-125">Planavimo pagalbinės priemonės filtrai</span><span class="sxs-lookup"><span data-stu-id="e65b9-125">Schedule assistant filters</span></span>

<span data-ttu-id="e65b9-126">Paleidus planavimo pagalbinę priemonę, išsami išteklių reikalavimo informacija rodoma kaip filtruotos reikšmės kairiojoje srityje.</span><span class="sxs-lookup"><span data-stu-id="e65b9-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="e65b9-127">Išteklių vadovas arba projekto vadovas gali patikslinti rezultatus koreguodamas filtrus pagal planavimo poreikius.</span><span class="sxs-lookup"><span data-stu-id="e65b9-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="e65b9-128">Filtro srityje rodomos su darbu susijusios parinktys, įskaitant:</span><span class="sxs-lookup"><span data-stu-id="e65b9-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="e65b9-129">Darbo pradžia ir pabaiga</span><span class="sxs-lookup"><span data-stu-id="e65b9-129">Work start and end</span></span>
-   <span data-ttu-id="e65b9-130">Charakteristikos</span><span class="sxs-lookup"><span data-stu-id="e65b9-130">Characteristics</span></span>
-   <span data-ttu-id="e65b9-131">Vaidmenys</span><span class="sxs-lookup"><span data-stu-id="e65b9-131">Roles</span></span>
-   <span data-ttu-id="e65b9-132">Organizaciniai vienetai</span><span class="sxs-lookup"><span data-stu-id="e65b9-132">Organizational units</span></span>
-   <span data-ttu-id="e65b9-133">Išteklių įmonė</span><span class="sxs-lookup"><span data-stu-id="e65b9-133">Resourcing company</span></span>
-   <span data-ttu-id="e65b9-134">Išteklių tipai</span><span class="sxs-lookup"><span data-stu-id="e65b9-134">Resource types</span></span>
-   <span data-ttu-id="e65b9-135">Pageidaujami ištekliai</span><span class="sxs-lookup"><span data-stu-id="e65b9-135">Preferred resources</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]