---
title: Išteklių užklausos pateikimas
description: Šioje temoje pateikiama informacija apie tai, kaip pateikti užklausą projekto ištekliams.
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
author: JohnPBurrows
ms.assetid: 9f4a6315-3905-4b15-8d06-e5dae30ccbb8
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2b706ae25af5ba85647c98353b5950663fafc292
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753741"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="646c9-103">Išteklių užklausos pateikimas</span><span class="sxs-lookup"><span data-stu-id="646c9-103">Submit a resource request</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="646c9-104">Kaip išteklių užklausą galite pateikti sugeneruotus išteklių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="646c9-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="646c9-105">Tada užklausa siunčiama išteklių valdytojui, kad ją įvykdytų.</span><span class="sxs-lookup"><span data-stu-id="646c9-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="646c9-106">„Project Service Automation“ (PSA) lange **Projektai** spustelėkite skirtuką **Komanda**, kad peržiūrėtumėte rezervuojamų išteklių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="646c9-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="646c9-107">Sąraše pažymėkite bendruosius išteklius, kuriems taikomas išteklių reikalavimas, tada spustelėkite **Pateikti užklausą.**</span><span class="sxs-lookup"><span data-stu-id="646c9-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![Išteklių užklausos pateikimas](media/RM-how-to-18.png)

<span data-ttu-id="646c9-109">Bendrosios komandos nario užklausos būsena bus pakeista į **Pateikta**.</span><span class="sxs-lookup"><span data-stu-id="646c9-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="646c9-110">Išteklių valdytojui įvykdžius užklausą, bendrieji ištekliai bus pakeisti įvardintais ištekliais, jei išteklių valdytojas įvykdo užklausą naudodamas įvardintų išteklių pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="646c9-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="646c9-111">Kitu atveju bendrieji ištekliai liks komandoje, o užklausos būsena bus pakeista į **Reikia peržiūrėti**, jei išteklių valdytojas pasiūlė įvardintus išteklius.</span><span class="sxs-lookup"><span data-stu-id="646c9-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>
