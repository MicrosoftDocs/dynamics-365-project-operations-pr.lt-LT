---
title: Rezervacijos ir priskyrimai
description: Šioje temoje pateikta informacija apie skirtumus tarp išteklių rezervavimų ir išteklių priskyrimų.
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012776"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="d8359-103">Rezervacijos ir priskyrimai</span><span class="sxs-lookup"><span data-stu-id="d8359-103">Bookings vs assignments</span></span>

<span data-ttu-id="d8359-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="d8359-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d8359-105">Rezervacijos yra galutinis arba preliminarus išteklių paskirstymas projektui.</span><span class="sxs-lookup"><span data-stu-id="d8359-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="d8359-106">Galutinės rezervacijos naudoja išteklių pajėgumus.</span><span class="sxs-lookup"><span data-stu-id="d8359-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="d8359-107">Rezervacijos yra komandų organizavimo sąvokos, padedančios komandoms suprasti, kaip ištekliai bus panaudoti įvairiuose projektuose.</span><span class="sxs-lookup"><span data-stu-id="d8359-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="d8359-108">„Dynamics 365 Project Operations“ rezervavimus laiko projekto lygio sąvoka.</span><span class="sxs-lookup"><span data-stu-id="d8359-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="d8359-109">Kitaip nei rezervacijos, priskyrimai yra išteklių projekto užduotims priskyrimas projekto grafike.</span><span class="sxs-lookup"><span data-stu-id="d8359-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="d8359-110">Ištekliai gali būti įvardytieji arba bendrieji.</span><span class="sxs-lookup"><span data-stu-id="d8359-110">The resources can be named or generic.</span></span>  <span data-ttu-id="d8359-111">Kai išteklių reikalavimas išvedamas iš projekto užduoties priskyrimų, „Project Operations“ naudoja išteklių priskyrimo pastangų kontūrus išteklių reikalavimo išsamios informacijos kontūrams kurti.</span><span class="sxs-lookup"><span data-stu-id="d8359-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="d8359-112">Tačiau ištekliaus priskyrimų nuoroda nėra išlaikoma.</span><span class="sxs-lookup"><span data-stu-id="d8359-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="d8359-113">Rezervavimų, išvestų iš išteklių reikalavimo, naujinimai neatnaujina jokių išteklių priskyrimų.</span><span class="sxs-lookup"><span data-stu-id="d8359-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="d8359-114">Paprastai ištekliaus rezervacijų suma sudaro išteklių paskyrimų vienai ar kelioms užduotims, sumą.</span><span class="sxs-lookup"><span data-stu-id="d8359-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="d8359-115">Tačiau „Project Operations“ šio susitarimo laikytis neverčia.</span><span class="sxs-lookup"><span data-stu-id="d8359-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="d8359-116">Rodinyje **Derinimas** rodomos projektų vadovo vietos, kuriose išteklių rezervacijos ir priskyrimai nesutampa.</span><span class="sxs-lookup"><span data-stu-id="d8359-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]