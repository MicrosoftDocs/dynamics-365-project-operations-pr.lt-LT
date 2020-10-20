---
title: Rezervacijos ir priskyrimai
description: Šioje temoje pateikta informacija apie skirtumus tarp išteklių rezervavimų ir išteklių priskyrimų.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896021"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="c8429-103">Rezervacijos ir priskyrimai</span><span class="sxs-lookup"><span data-stu-id="c8429-103">Bookings vs assignments</span></span>

<span data-ttu-id="c8429-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="c8429-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c8429-105">Rezervacijos yra galutinis arba preliminarus išteklių paskirstymas projektui.</span><span class="sxs-lookup"><span data-stu-id="c8429-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="c8429-106">Galutinės rezervacijos naudoja išteklių pajėgumus.</span><span class="sxs-lookup"><span data-stu-id="c8429-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="c8429-107">Priskyrimai yra išteklių projekto užduotims priskyrimas projekto grafike.</span><span class="sxs-lookup"><span data-stu-id="c8429-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="c8429-108">Ištekliai gali būti faktiniai arba bendrieji.</span><span class="sxs-lookup"><span data-stu-id="c8429-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="c8429-109">Idealiu atveju faktinių išteklių rezervacijos ir priskyrimai turėtų sutapti, nes jie nesiskiria.</span><span class="sxs-lookup"><span data-stu-id="c8429-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="c8429-110">Tačiau „Microsoft Dynamics Project Operations“ neribojo šio sutapimo.</span><span class="sxs-lookup"><span data-stu-id="c8429-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="c8429-111">Rodinyje **Derinimas** projektų vadovui rodomos vietos, kuriose išteklių rezervacijos ir priskyrimai nesutampa.</span><span class="sxs-lookup"><span data-stu-id="c8429-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
