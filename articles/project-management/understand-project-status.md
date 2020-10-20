---
title: Projekto būsenos supratimas
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Operations“ projektams priskirtas būsenas.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 336e479ad39653af14cca7930fe63e906b7de489
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965686"
---
# <a name="understand-project-status"></a><span data-ttu-id="1e158-103">Projekto būsenos supratimas</span><span class="sxs-lookup"><span data-stu-id="1e158-103">Understand project status</span></span>

<span data-ttu-id="1e158-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="1e158-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="1e158-105">Puslapio **Projekto objektas** skyriuje **Būsena** pateikiama projekto būklės suvestinė, atsižvelgiant į savikainą ir pastangas.</span><span class="sxs-lookup"><span data-stu-id="1e158-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="1e158-106">Būsenos suvestinės laukai</span><span class="sxs-lookup"><span data-stu-id="1e158-106">Status summary fields</span></span>

- <span data-ttu-id="1e158-107">Laukas **Bendroji projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="1e158-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="1e158-108">Šiame lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, siekiant nurodyti didėjančią riziką.</span><span class="sxs-lookup"><span data-stu-id="1e158-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="1e158-109">Lauke **Komentarai** projekto vadovas gali įvesti konkrečius komentarus apie būseną.</span><span class="sxs-lookup"><span data-stu-id="1e158-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="1e158-110">Lauko **Būsena atnaujinta** redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="1e158-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="1e158-111">Šio lauko reikšmė yra laiko žyma, nurodanti, kada paskutinį kartą buvo atnaujinta būsena.</span><span class="sxs-lookup"><span data-stu-id="1e158-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="1e158-112">Laukai **Grafiko efektyvumas** ir **Išlaidų efektyvumas** nustatomi pagal sekimo tinklelį.</span><span class="sxs-lookup"><span data-stu-id="1e158-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="1e158-113">Kai rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite nustatyti šiuos laukus į **Lenkia**.</span><span class="sxs-lookup"><span data-stu-id="1e158-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="1e158-114">Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti laukus į **Atsilieka**.</span><span class="sxs-lookup"><span data-stu-id="1e158-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
