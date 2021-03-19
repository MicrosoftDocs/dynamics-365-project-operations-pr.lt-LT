---
title: Išteklių užklausos pateikimas
description: Kaip išteklių užklausą galite pateikti sugeneruotus išteklių reikalavimus. Tada užklausa siunčiama išteklių valdytojui, kad ją įvykdytų.
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: bc97af1ec90e60417c502eb329a85004e769e05b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279148"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="f5ef0-104">Išteklių užklausos pateikimas</span><span class="sxs-lookup"><span data-stu-id="f5ef0-104">Submit a resource request</span></span>

<span data-ttu-id="f5ef0-105">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="f5ef0-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f5ef0-106">Kaip išteklių užklausą galite pateikti sugeneruotus išteklių reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="f5ef0-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="f5ef0-107">Tada užklausa siunčiama išteklių valdytojui, kad ją įvykdytų.</span><span class="sxs-lookup"><span data-stu-id="f5ef0-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="f5ef0-108">Programoje „Dynamics 365 Project Operations“, puslapyje **Projektai** pasirinkite skirtuką **Komanda**, kad peržiūrėtumėte rezercuojamų išteklių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f5ef0-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="f5ef0-109">Sąraše pažymėkite bendrąjį išteklių, kuriam taikomas išteklių reikalavimas, tada spustelėkite **Pateikti užklausą.**</span><span class="sxs-lookup"><span data-stu-id="f5ef0-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="f5ef0-110">Bendrosios komandos nario užklausos būsena bus pakeista į **Pateikta**.</span><span class="sxs-lookup"><span data-stu-id="f5ef0-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="f5ef0-111">Įvykdžius užklausą, bendrasis išteklius bus pakeistas įvardintu ištekliu, jei išteklių vadovas įvykdo užklausą rezervuodamas įvardintą išteklių.</span><span class="sxs-lookup"><span data-stu-id="f5ef0-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="f5ef0-112">Kitu atveju, jei išteklių vadovas pasiūlo įvardintą išteklių, bendrasis išteklius lieka komandoje ir užklausos būsena pasikeičia į **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="f5ef0-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]