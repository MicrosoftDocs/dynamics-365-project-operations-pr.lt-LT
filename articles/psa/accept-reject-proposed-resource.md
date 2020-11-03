---
title: Pasiūlyto projekto išteklių priėmimas arba atmetimas
description: Šioje temoje pateikta informacija apie tai, kaip patvirtinti arba atmesti siūlomą projekto išteklių.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/07/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4c10c55961c74c2dc53fabd1d041a935ca9a4870
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081000"
---
# <a name="accept-or-reject-a-proposed-project-resource"></a><span data-ttu-id="151b0-103">Pasiūlyto projekto išteklių priėmimas arba atmetimas</span><span class="sxs-lookup"><span data-stu-id="151b0-103">Accept or reject a proposed project resource</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="151b0-104">Šioje temoje pateikta informacija apie tai, kaip patvirtinti arba atmesti siūlomą projekto išteklių.</span><span class="sxs-lookup"><span data-stu-id="151b0-104">This topic provides information about how to approve or reject a proposed project resource.</span></span>

<span data-ttu-id="151b0-105">Kai išteklių valdytojas pasiūlo įvardytą šaltinį užpildyti bendrąją projekto išteklių užklausą, bendrosios komandos nario **Užklausos būsena** laukas bus atnaujintas į **Reikia peržiūros**.</span><span class="sxs-lookup"><span data-stu-id="151b0-105">When a resource manager proposes a named resource to fill the generic resource request for a project, the **Request Status** field for the generic team member will be updated to **Needs Review**.</span></span> <span data-ttu-id="151b0-106">Užklausa bus išsiųsta projekto vadovui patvirtinti arba atmesti.</span><span class="sxs-lookup"><span data-stu-id="151b0-106">The request will be sent to the project manager for approval or rejection.</span></span>

![Pasiūlymą turintis bendrosios komandos narys](media/RM-how-to-19.png)

<span data-ttu-id="151b0-108">Tinklelis **Siūlomi Ištekliai** skirtuke **Projekto Komandos Narys** puslapyje rodo pasiūlytų išteklių dabartines rezervacijas.</span><span class="sxs-lookup"><span data-stu-id="151b0-108">The grid on the **Proposed Resources** tab on the **Project Team Member** page shows the proposed resource’s current bookings.</span></span> <span data-ttu-id="151b0-109">Priėmus pasiūlymą, tinklelis atnaujinamas atsižvelgiant į atliktą rezervaciją.</span><span class="sxs-lookup"><span data-stu-id="151b0-109">After the proposal is accepted, the grid is updated to reflect that booking.</span></span> 

<span data-ttu-id="151b0-110">Norėdami priimti siūlomą išteklių ir užsakyti išteklių savo komandai, spustelėkite **Priimti Pasiūlymus**.</span><span class="sxs-lookup"><span data-stu-id="151b0-110">To accept the proposed resource and book that resource on your team, click **Accept Proposals**.</span></span>  
<span data-ttu-id="151b0-111">Norėdami atmesti pasiūlymą, spustelėkite **Atmesti išteklius**.</span><span class="sxs-lookup"><span data-stu-id="151b0-111">To reject the proposal, click **Reject Resource**.</span></span>

![Išteklių pasiūlymo priėmimas](media/RM-how-to-20.png) 

<span data-ttu-id="151b0-113">Panašiai į tiesioginį bendrosios išteklių užklausos užpildymą naudojant įvardytą išteklių, bendrasis išteklius bus pakeistas, o priskirtos užduotys bus atnaujintos kartu su įvardytu komandos nariu.</span><span class="sxs-lookup"><span data-stu-id="151b0-113">Similar to directly fulfilling a generic resource request with a named resource, the generic resource will be replaced and the assigned tasks will be updated with the named team member.</span></span>
