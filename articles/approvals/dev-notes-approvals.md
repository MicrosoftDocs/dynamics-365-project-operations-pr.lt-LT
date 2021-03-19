---
title: Kūrėjų pastabos dėl patvirtinimų
description: Šioje temoje pateikta papildoma kūrėjų informacija apie darbą su patvirtinimais.
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290279"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="69637-103">Kūrėjų pastabos dėl patvirtinimų</span><span class="sxs-lookup"><span data-stu-id="69637-103">Developer notes for Approvals</span></span>

<span data-ttu-id="69637-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="69637-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69637-105">Į „Dynamics 365 Project Operations“ įtraukta tikrinimo logika, užtikrinanti tinkamą įrašų perėjimą per patvirtinimo etapus.</span><span class="sxs-lookup"><span data-stu-id="69637-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="69637-106">Tinkamas įrašų perėjimas užtikrina tolesnius dalykus.</span><span class="sxs-lookup"><span data-stu-id="69637-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="69637-107">Visos palaikančiosios eilutės sukuriamos susijusiose lentelėse, pvz., žurnaluose ir faktiniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="69637-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="69637-108">Prieš tęsiant tvirtintojas projekte pažymimas **projekto tvirtintoju**.</span><span class="sxs-lookup"><span data-stu-id="69637-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]