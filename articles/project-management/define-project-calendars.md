---
title: Projekto kalendorių apibrėžimas
description: Šioje temoje pateikiama informacijos apie tai, kaip projektui taikyti kalendoriaus šabloną projekto grafikui sekti.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 0d1a2c4bd2d4022bbf79afcef79170eb482e6418
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999006"
---
# <a name="define-project-calendars"></a><span data-ttu-id="1d9b0-103">Projekto kalendorių apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="1d9b0-103">Define project calendars</span></span>

<span data-ttu-id="1d9b0-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="1d9b0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1d9b0-105">Norėdami sukurti ir tvarkyti projektą, projektui turite pritaikyti kalendoriaus šabloną.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="1d9b0-106">Kalendoriaus šablonas apibrėžia toliau nurodytus projekto atributus.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="1d9b0-107">Darbo valandos, įskaitant pradžios ir pabaigos laiką</span><span class="sxs-lookup"><span data-stu-id="1d9b0-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="1d9b0-108">Darbo dienos</span><span class="sxs-lookup"><span data-stu-id="1d9b0-108">Working days</span></span>
- <span data-ttu-id="1d9b0-109">Kalendoriaus išimtys, pvz., ne darbo dienos</span><span class="sxs-lookup"><span data-stu-id="1d9b0-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="1d9b0-110">Projektui taikomas kalendoriaus šablonas yra kalendoriaus šablono, apibrėžto organizacijos parametruose, kopija.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="1d9b0-111">Jei kalendoriaus šabloną pakeičiate, šie pakeitimai neišplatinami į projekto darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="1d9b0-112">Norint pakeisti projekto darbo valandas, reikia pritaikyti naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="1d9b0-113">Norint sukurti savo organizacijos kalendoriaus šabloną, taikomi du pagrindiniai toliau nurodyti reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="1d9b0-114">Apibrėžkite norimas šablono darbo valandas naudodami naują arba esamą rezervuojamąjį išteklių.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="1d9b0-115">Sukurkite naują kalendoriaus šabloną ir jį susiekite su rezervuojamuoju ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="1d9b0-116">**Šablono darbo valandų apibrėžimas**</span><span class="sxs-lookup"><span data-stu-id="1d9b0-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="1d9b0-117">Eikite į **Ištekliai** \> **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="1d9b0-118">Sukurkite naują išteklių, kurį norite nurodyti kalendoriaus šablone, arba pasirinkite esamą išteklių.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="1d9b0-119">Pasirinkite ištekliaus skirtuką **Darbo valandos** ir vykdykite nurodymus, pateiktus dalyje [Ištekliaus darbo valandų nustatymas](/dynamics365/field-service/set-work-hours-resource.md), kad būtų sukonfigūruotos kalendoriaus taisyklės.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="1d9b0-120">**Naujo kalendoriaus šablono sukūrimas**</span><span class="sxs-lookup"><span data-stu-id="1d9b0-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="1d9b0-121">Nueikite į **Parametrai** \> **Kalendoriaus šablonas**.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="1d9b0-122">Pasirinkite **Naujas** ir įveskite pavadinimą, aprašą bei šablono išteklių.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="1d9b0-123">Kai išteklius yra nurodomas kalendoriaus šablone, ištekliaus kalendoriaus kopija susiejama su kalendoriaus šablonu.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="1d9b0-124">Jei nukopijuoto šablono darbo valandos pasikeičia, šie pakeitimai neišplatinami į kalendoriaus šabloną.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="1d9b0-125">Dabar galite susieti darbo šabloną su projekto kalendoriaus šablonu.</span><span class="sxs-lookup"><span data-stu-id="1d9b0-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

