---
title: Išteklių užklausos pateikimas
description: Šioje temoje pateikiama informacija apie tai, kaip pateikti užklausą projekto ištekliams.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
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
ms.openlocfilehash: bcea3d640d7e9ee2b071c55bff9ade3268edb319
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080929"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="7cedc-103">Išteklių užklausos pateikimas</span><span class="sxs-lookup"><span data-stu-id="7cedc-103">Submitting a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7cedc-104">Kaip išteklių užklausą galite pateikti sugeneruotus išteklių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="7cedc-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="7cedc-105">Tada užklausa siunčiama išteklių valdytojui, kad ją įvykdytų.</span><span class="sxs-lookup"><span data-stu-id="7cedc-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="7cedc-106">„Project Service Automation“ (PSA) lange **Projektai** spustelėkite skirtuką **Komanda** , kad peržiūrėtumėte rezervuojamų išteklių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="7cedc-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="7cedc-107">Sąraše pažymėkite bendruosius išteklius, kuriems taikomas išteklių reikalavimas, tada spustelėkite **Pateikti užklausą.**</span><span class="sxs-lookup"><span data-stu-id="7cedc-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Išteklių užklausos pateikimas](media/RM-how-to-18.png)

<span data-ttu-id="7cedc-109">Bendrosios komandos nario užklausos būsena bus pakeista į **Pateikta**.</span><span class="sxs-lookup"><span data-stu-id="7cedc-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="7cedc-110">Išteklių valdytojui įvykdžius užklausą, bendrieji ištekliai bus pakeisti įvardintais ištekliais, jei išteklių valdytojas įvykdo užklausą naudodamas įvardintų išteklių pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7cedc-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="7cedc-111">Kitu atveju bendrieji ištekliai liks komandoje, o užklausos būsena bus pakeista į **Reikia peržiūrėti** , jei išteklių valdytojas pasiūlė įvardintus išteklius.</span><span class="sxs-lookup"><span data-stu-id="7cedc-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review** , if the resource manager has proposed a named resource.</span></span>
