---
title: Įvertinimo pabaigoje atnaujinimas
description: Šioje temoje pateikta informacija apie projekto pastangų projekcijos naujinimą.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 59d04869839cebd6e197f94f2ada8ab12c495c3b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127213"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="694e0-103">Įvertinimo pabaigoje atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="694e0-103">Update estimate at completion</span></span>

<span data-ttu-id="694e0-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="694e0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="694e0-105">Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas.</span><span class="sxs-lookup"><span data-stu-id="694e0-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="694e0-106">Projekto pakartotinės prognozės yra projekto vadovo numatyta sąmata, apskaičiuota pagal dabartinę projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="694e0-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="694e0-107">Tačiau nerekomenduojame projekto vadovams keisti pradinių skaičių, nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.</span><span class="sxs-lookup"><span data-stu-id="694e0-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="694e0-108">Projektų vadovas gali iš naujo sukurti užduoties pastangų prognozę dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="694e0-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="694e0-109">Perrašyti numatytuosius ETC nustatymus su nauju užduoties likusių pastangų įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="694e0-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="694e0-110">Perrašyti numatytuosius eigos procentais nustatymus su nauju užduoties patikslintos eigos įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="694e0-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="694e0-111">Dėl kiekvieno iš šių metodų perskaičiuojamos užduoties ETC, EAC bei eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis.</span><span class="sxs-lookup"><span data-stu-id="694e0-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="694e0-112">Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.</span><span class="sxs-lookup"><span data-stu-id="694e0-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
