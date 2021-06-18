---
title: Kūrėjų pastabos dėl patvirtinimų
description: Šioje temoje pateikta papildoma kūrėjų informacija apie darbą su patvirtinimais.
author: stsporen
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: a89ea669a262c145b9f391fddc19e79a425fabb5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996801"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="51f3a-103">Kūrėjų pastabos dėl patvirtinimų</span><span class="sxs-lookup"><span data-stu-id="51f3a-103">Developer notes for Approvals</span></span>

<span data-ttu-id="51f3a-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="51f3a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="51f3a-105">Į „Dynamics 365 Project Operations“ įtraukta tikrinimo logika, užtikrinanti tinkamą įrašų perėjimą per patvirtinimo etapus.</span><span class="sxs-lookup"><span data-stu-id="51f3a-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="51f3a-106">Tinkamas įrašų perėjimas užtikrina tolesnius dalykus.</span><span class="sxs-lookup"><span data-stu-id="51f3a-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="51f3a-107">Visos palaikančiosios eilutės sukuriamos susijusiose lentelėse, pvz., žurnaluose ir faktiniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="51f3a-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="51f3a-108">Prieš tęsiant tvirtintojas projekte pažymimas **projekto tvirtintoju**.</span><span class="sxs-lookup"><span data-stu-id="51f3a-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]