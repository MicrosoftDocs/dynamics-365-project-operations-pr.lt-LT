---
title: Rezervacijos ir priskyrimai
description: Šioje temoje pateikta informacija apie skirtumus tarp išteklių rezervavimų ir išteklių priskyrimų.
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130228"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="5ac64-103">Rezervacijos ir priskyrimai</span><span class="sxs-lookup"><span data-stu-id="5ac64-103">Bookings vs assignments</span></span>

<span data-ttu-id="5ac64-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="5ac64-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5ac64-105">Rezervacijos yra galutinis arba preliminarus išteklių paskirstymas projektui.</span><span class="sxs-lookup"><span data-stu-id="5ac64-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="5ac64-106">Galutinės rezervacijos naudoja išteklių pajėgumus.</span><span class="sxs-lookup"><span data-stu-id="5ac64-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="5ac64-107">Rezervacijos yra komandų organizavimo sąvokos, padedančios komandoms suprasti, kaip ištekliai bus panaudoti įvairiuose projektuose.</span><span class="sxs-lookup"><span data-stu-id="5ac64-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="5ac64-108">Programoje „Dynamics 365 Project Operations“ rezervacijos laikomos projekto lygio koncepcija.</span><span class="sxs-lookup"><span data-stu-id="5ac64-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="5ac64-109">Kitaip nei rezervacijos, priskyrimai yra išteklių projekto užduotims priskyrimas projekto grafike.</span><span class="sxs-lookup"><span data-stu-id="5ac64-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="5ac64-110">Ištekliai gali būti įvardytieji arba bendrieji.</span><span class="sxs-lookup"><span data-stu-id="5ac64-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="5ac64-111">Paprastai ištekliaus rezervacijų suma sudaro išteklių paskyrimų vienai ar kelioms užduotims, sumą.</span><span class="sxs-lookup"><span data-stu-id="5ac64-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="5ac64-112">Tačiau „Project Operations“ šio susitarimo laikytis neverčia.</span><span class="sxs-lookup"><span data-stu-id="5ac64-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="5ac64-113">Rodinyje **Derinimas** rodomos projektų vadovo vietos, kuriose išteklių rezervacijos ir priskyrimai nesutampa.</span><span class="sxs-lookup"><span data-stu-id="5ac64-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
