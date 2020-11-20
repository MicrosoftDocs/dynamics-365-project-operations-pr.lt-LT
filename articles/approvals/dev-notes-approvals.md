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
ms.openlocfilehash: 9e4e910d0ff0a5f2603148fcc5daa0d423a4d174
ms.sourcegitcommit: a9dbcd3aff4c6ae495412e4980e105ae160fd1ec
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2020
ms.locfileid: "4483958"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="81aa3-103">Kūrėjų pastabos dėl patvirtinimų</span><span class="sxs-lookup"><span data-stu-id="81aa3-103">Developer notes for Approvals</span></span>

<span data-ttu-id="81aa3-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="81aa3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="81aa3-105">Į „Dynamics 365 Project Operations“ įtraukta tikrinimo logika, užtikrinanti tinkamą įrašų perėjimą per patvirtinimo etapus.</span><span class="sxs-lookup"><span data-stu-id="81aa3-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="81aa3-106">Tinkamas įrašų perėjimas užtikrina tolesnius dalykus.</span><span class="sxs-lookup"><span data-stu-id="81aa3-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="81aa3-107">Visos palaikančiosios eilutės sukuriamos susijusiose lentelėse, pvz., žurnaluose ir faktiniuose duomenyse.</span><span class="sxs-lookup"><span data-stu-id="81aa3-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="81aa3-108">Prieš tęsiant tvirtintojas projekte pažymimas **projekto tvirtintoju**.</span><span class="sxs-lookup"><span data-stu-id="81aa3-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>
