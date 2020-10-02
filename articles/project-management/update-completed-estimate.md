---
title: Įvertinimo pabaigoje atnaujinimas
description: Šioje temoje pateikta informacija apie projekto pastangų projekcijos naujinimą.
author: ruhercul
manager: AnnBe
ms.date: 09/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 42824cc4cfc2b934f69d319944fe7ee43183955c
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897776"
---
# <a name="update-estimate-at-completion"></a><span data-ttu-id="35cfc-103">Įvertinimo pabaigoje atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="35cfc-103">Update estimate at completion</span></span>

<span data-ttu-id="35cfc-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="35cfc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="35cfc-105">Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas.</span><span class="sxs-lookup"><span data-stu-id="35cfc-105">It's common for a project manager to revise the original estimates on a task.</span></span> <span data-ttu-id="35cfc-106">Projekto pakartotinės prognozės yra projekto vadovo numatyta sąmata, apskaičiuota pagal dabartinę projekto būseną.</span><span class="sxs-lookup"><span data-stu-id="35cfc-106">Project reprojections are a project manager's perception of estimates, given the current state of a project.</span></span> <span data-ttu-id="35cfc-107">Tačiau nerekomenduojame projekto vadovams keisti pradinių skaičių, nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.</span><span class="sxs-lookup"><span data-stu-id="35cfc-107">However, we don't recommend that project managers change the baseline numbers, because the project baseline represents the established source of truth for the project's schedule and cost estimate, and all project stakeholders have agreed to it.</span></span>

<span data-ttu-id="35cfc-108">Projektų vadovas gali iš naujo sukurti užduoties pastangų prognozę dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="35cfc-108">There are two ways that a project manager can reproject effort on tasks:</span></span>

- <span data-ttu-id="35cfc-109">Perrašyti numatytuosius ETC nustatymus su nauju užduoties likusių pastangų įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="35cfc-109">Override the default estimate to complete (ETC) with a new estimate of the actual remaining effort on the task.</span></span> 
- <span data-ttu-id="35cfc-110">Perrašyti numatytuosius eigos procentais nustatymus su nauju užduoties patikslintos eigos įvertinimu.</span><span class="sxs-lookup"><span data-stu-id="35cfc-110">Override the default progress percentage with a new estimate of the true progress on the task.</span></span>

<span data-ttu-id="35cfc-111">Dėl kiekvieno iš šių metodų perskaičiuojamos užduoties ETC, EAC bei eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis.</span><span class="sxs-lookup"><span data-stu-id="35cfc-111">Each of these approaches cause a recalculation of the task's ETC, estimate at complete (EAC), and progress percentage, and the projected effort variance on a task.</span></span> <span data-ttu-id="35cfc-112">Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.</span><span class="sxs-lookup"><span data-stu-id="35cfc-112">The EAC, ETC, and progress percentage on the summary tasks are recalculated, and produce a new projection of effort variance.</span></span>
