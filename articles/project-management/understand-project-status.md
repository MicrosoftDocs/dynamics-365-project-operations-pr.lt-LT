---
title: Projekto būsenos supratimas
description: Šioje temoje pateikiama informacija apie projektams priskirtą būseną programoje „Dynamics 365 Project Operations“.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: ad8c012b93bc65595dca33df1770562916c557e0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993426"
---
# <a name="understand-project-status"></a><span data-ttu-id="63abe-103">Projekto būsenos paaiškinimas</span><span class="sxs-lookup"><span data-stu-id="63abe-103">Understand project status</span></span>

<span data-ttu-id="63abe-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="63abe-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="63abe-105">Puslapio **Projekto objektas** skyriuje **Būsena** pateikiama projekto būklės suvestinė, atsižvelgiant į savikainą ir pastangas.</span><span class="sxs-lookup"><span data-stu-id="63abe-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="63abe-106">Būsenos suvestinės laukai</span><span class="sxs-lookup"><span data-stu-id="63abe-106">Status summary fields</span></span>

- <span data-ttu-id="63abe-107">Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="63abe-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="63abe-108">Šiame lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, siekiant nurodyti didėjančią riziką.</span><span class="sxs-lookup"><span data-stu-id="63abe-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="63abe-109">Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną.</span><span class="sxs-lookup"><span data-stu-id="63abe-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="63abe-110">Lauko **Būsena atnaujinta** redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="63abe-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="63abe-111">Šio lauko reikšmė yra laiko žyma, nurodanti, kada paskutinį kartą buvo atnaujinta būsena.</span><span class="sxs-lookup"><span data-stu-id="63abe-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="63abe-112">Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo tinklelį.</span><span class="sxs-lookup"><span data-stu-id="63abe-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="63abe-113">Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite atnaujinti šiuos laukus į **Prieš laiką**.</span><span class="sxs-lookup"><span data-stu-id="63abe-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="63abe-114">Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti laukus į **Atsilieka**.</span><span class="sxs-lookup"><span data-stu-id="63abe-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]