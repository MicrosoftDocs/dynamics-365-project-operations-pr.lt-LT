---
title: Išteklių valdymo režimų apžvalga
description: Šioje temoje pateikiama informacija apie išteklių valdymo funkciją programoje „Dynamics 365 Project Operations“.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.custom: intro-internal
ms.openlocfilehash: 41265534661e51565bf31105ef69cec9b3b181c3
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6367901"
---
# <a name="resource-management-modes-overview"></a><span data-ttu-id="a0bea-103">Išteklių valdymo režimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="a0bea-103">Resource management modes overview</span></span>

<span data-ttu-id="a0bea-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="a0bea-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a0bea-105">„Dynamics 365 Project Operations“ palaiko du režimus, kad galėtumėte vykdyti bendrą rezervavimo srautą.</span><span class="sxs-lookup"><span data-stu-id="a0bea-105">Dynamics 365 Project Operations supports two modes in order for you to execute the overall booking flow.</span></span> <span data-ttu-id="a0bea-106">Valdymo režimas apibrėžiamas kaip projekto parametras ir jį galima keisti, jei pasikeičia jūsų verslo poreikiai.</span><span class="sxs-lookup"><span data-stu-id="a0bea-106">The mode of management is defined as a project parameter and can be modified if your business needs change.</span></span>    

## <a name="central-mode"></a><span data-ttu-id="a0bea-107">Centralizuotas režimas</span><span class="sxs-lookup"><span data-stu-id="a0bea-107">Central mode</span></span>
<span data-ttu-id="a0bea-108">Organizacijoms, kuriose išteklių priskyrimas projektams yra centralizuotas, centralizuotas režimas suteikia galimybę užtikrinti, kad projektų vadovai galėtų apibrėžti išteklių reikalavimus projekto lygiu.</span><span class="sxs-lookup"><span data-stu-id="a0bea-108">For organizations who centralize the allocation for resources to projects, the Central mode provides a way to ensure Project managers can define resource requirements at the project level.</span></span> <span data-ttu-id="a0bea-109">Išteklių reikalavimų vykdymas deleguojamas išteklių vadovui.</span><span class="sxs-lookup"><span data-stu-id="a0bea-109">Fulfillment of the resource requirements is delegated to a Resource manager.</span></span> <span data-ttu-id="a0bea-110">Projektų vadovai gali priimti arba atmesti išteklių vadovo siūlomus išteklius.</span><span class="sxs-lookup"><span data-stu-id="a0bea-110">Project managers can accept or reject resources that are proposed by the Resource manager.</span></span>

![Centralizuotas režimas](./media/resource-management-central.png)

<span data-ttu-id="a0bea-112">Jei norite valdyti išteklius naudodami centralizuotą režimą, žr.:</span><span class="sxs-lookup"><span data-stu-id="a0bea-112">To manage resources with the Central mode, see:</span></span>

- [<span data-ttu-id="a0bea-113">Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas</span><span class="sxs-lookup"><span data-stu-id="a0bea-113">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="a0bea-114">Įvardytų išteklių rezervavimas iš išteklių reikalavimų</span><span class="sxs-lookup"><span data-stu-id="a0bea-114">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)
- [<span data-ttu-id="a0bea-115">Išteklių užklausos pateikimas</span><span class="sxs-lookup"><span data-stu-id="a0bea-115">Submit a resource request</span></span>](/dynamics365/project-service/submit-resource-request)
- [<span data-ttu-id="a0bea-116">Išteklių užklausos vykdymas</span><span class="sxs-lookup"><span data-stu-id="a0bea-116">Fulfill a resource request</span></span>](/dynamics365/project-service/resource-management-fulfill-requests)
- [<span data-ttu-id="a0bea-117">Pasiūlyto projekto ištekliaus iš ištekliaus užklausos priėmimas arba atmetimas</span><span class="sxs-lookup"><span data-stu-id="a0bea-117">Accept or reject a proposed project resource from a resource request</span></span>](/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a><span data-ttu-id="a0bea-118">Hibridinis režimas</span><span class="sxs-lookup"><span data-stu-id="a0bea-118">Hybrid mode</span></span>
<span data-ttu-id="a0bea-119">Organizacijoms, kurioms reikia lankstumo priskiriant išteklius, hibridinis režimas suteikia projektų vadovams ir išteklių vadovams galimybę rezervuoti išteklius.</span><span class="sxs-lookup"><span data-stu-id="a0bea-119">For organizations who require flexibility in the allocation of resources, the hybrid mode enables both Project managers and Resource managers the ability to book resources.</span></span>

![Hibridinis režimas](./media/resource-management-hybrid.png)

<span data-ttu-id="a0bea-121">Be palaikomo centralizuoto režimo proceso, peržiūrėkite toliau pateiktas temas, kad galėtumėte valdyti visas kitas palaikomas hibridinio režimo rezervavimo eigas:</span><span class="sxs-lookup"><span data-stu-id="a0bea-121">In addition to the supported Central mode process, see the following topics to manage all other supported booking flows in the Hybrid mode:</span></span>

<span data-ttu-id="a0bea-122">Tiesioginis ištekliaus rezervavimas projekte:</span><span class="sxs-lookup"><span data-stu-id="a0bea-122">Book a resource directly to a project:</span></span>
- [<span data-ttu-id="a0bea-123">Įvardytų rezervuojamų išteklių rezervavimas projekto komandai ir užduočių priskyrimas</span><span class="sxs-lookup"><span data-stu-id="a0bea-123">Book named bookable resources to a project team and assign tasks</span></span>](/dynamics365/project-service/assign-named-bookable-resource)

<span data-ttu-id="a0bea-124">Ištekliaus rezervavimas iš ištekliaus reikalavimo:</span><span class="sxs-lookup"><span data-stu-id="a0bea-124">Book a resource from a resource requirement:</span></span>
- [<span data-ttu-id="a0bea-125">Bendrųjų rezervuojamų išteklių priskyrimas užduočiai ir išteklių reikalavimų generavimas</span><span class="sxs-lookup"><span data-stu-id="a0bea-125">Assign generic bookable resources to a task and generate resource requirements</span></span>](/dynamics365/project-service/assign-generic-bookable-resource)
- [<span data-ttu-id="a0bea-126">Įvardytų išteklių rezervavimas iš išteklių reikalavimų</span><span class="sxs-lookup"><span data-stu-id="a0bea-126">Book named resources from resource requirements</span></span>](/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]