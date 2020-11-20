---
title: Projekto būsenos supratimas
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Operations“ projektams priskirtas būsenas.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc5bc174518e46b32cf88ea7231bb2df10fde292
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127303"
---
# <a name="understand-project-status"></a><span data-ttu-id="844db-103">Projekto būsenos supratimas</span><span class="sxs-lookup"><span data-stu-id="844db-103">Understand project status</span></span>

<span data-ttu-id="844db-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="844db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="844db-105">Puslapio **Projekto objektas** skyriuje **Būsena** pateikiama projekto būklės suvestinė, atsižvelgiant į savikainą ir pastangas.</span><span class="sxs-lookup"><span data-stu-id="844db-105">The **Status** section on the **Project Entity** page provides a summary of a project's health based upon cost and effort.</span></span>


## <a name="status-summary-fields"></a><span data-ttu-id="844db-106">Būsenos suvestinės laukai</span><span class="sxs-lookup"><span data-stu-id="844db-106">Status summary fields</span></span>

- <span data-ttu-id="844db-107">Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="844db-107">The **Overall project status** field is an editable field that shows the overall status of the project.</span></span> <span data-ttu-id="844db-108">Šiame lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, siekiant nurodyti didėjančią riziką.</span><span class="sxs-lookup"><span data-stu-id="844db-108">This field uses color-coding, such as green, yellow, and red, to indicate increasing risk.</span></span> 
- <span data-ttu-id="844db-109">Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną.</span><span class="sxs-lookup"><span data-stu-id="844db-109">The **Comments** field lets the project manager enter specific comments about the status.</span></span> 
- <span data-ttu-id="844db-110">Lauko **Būsena atnaujinta** redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="844db-110">The **Status updated on** field isn't editable.</span></span> <span data-ttu-id="844db-111">Šio lauko reikšmė yra laiko žyma, nurodanti, kada paskutinį kartą buvo atnaujinta būsena.</span><span class="sxs-lookup"><span data-stu-id="844db-111">The value in this field is a timestamp that indicates when the status was last updated.</span></span>
- <span data-ttu-id="844db-112">Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo tinklelį.</span><span class="sxs-lookup"><span data-stu-id="844db-112">The **Schedule performance** and **Cost performance** fields are set from the tracking grid.</span></span> <span data-ttu-id="844db-113">Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite atnaujinti šiuos laukus į **Prieš laiką**.</span><span class="sxs-lookup"><span data-stu-id="844db-113">When the schedule and cost variance for the root node in the **Effort tracking** view are positive, these fields are updated to **Ahead**.</span></span> <span data-ttu-id="844db-114">Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti laukus į **Atsilieka**.</span><span class="sxs-lookup"><span data-stu-id="844db-114">When the schedule and cost variance for the root node are negative, these fields are set to **Behind**.</span></span>
