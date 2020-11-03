---
title: Išteklių užklausos pateikimas
description: Kaip išteklių užklausą galite pateikti sugeneruotus išteklių reikalavimus. Tada užklausa siunčiama išteklių valdytojui, kad ją įvykdytų.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080730"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="1835b-104">Išteklių užklausos pateikimas</span><span class="sxs-lookup"><span data-stu-id="1835b-104">Submit a resource request</span></span>

<span data-ttu-id="1835b-105">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="1835b-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1835b-106">Kaip išteklių užklausą galite pateikti sugeneruotus išteklių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="1835b-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="1835b-107">Tada užklausa siunčiama išteklių valdytojui, kad ją įvykdytų.</span><span class="sxs-lookup"><span data-stu-id="1835b-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="1835b-108">„Dynamics 365 Project Operations“ puslapyje **Projektai** pasirinkite skirtuką **Komanda** , kad peržiūrėtumėte rezervuojamų išteklių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="1835b-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="1835b-109">Sąraše pažymėkite bendrąjį išteklių, kuriam taikomas išteklių reikalavimas, tada spustelėkite **Pateikti užklausą.**</span><span class="sxs-lookup"><span data-stu-id="1835b-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="1835b-110">Bendrosios komandos nario užklausos būsena bus pakeista į **Pateikta**.</span><span class="sxs-lookup"><span data-stu-id="1835b-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="1835b-111">Įvykdžius užklausą, bendrasis išteklius bus pakeistas įvardintu ištekliu, jei išteklių vadovas įvykdo užklausą rezervuodamas įvardintą išteklių.</span><span class="sxs-lookup"><span data-stu-id="1835b-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="1835b-112">Kitu atveju, jei išteklių vadovas pasiūlo įvardintą išteklių, bendrasis išteklius lieka komandoje ir užklausos būsena pasikeičia į **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="1835b-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
