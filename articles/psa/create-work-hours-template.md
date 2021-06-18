---
title: Darbo valandų šablono kūrimas
description: Šioje temoje paaiškinama, kaip sprendime „Project Service“ sukurti darbo valandų šabloną.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
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
ms.openlocfilehash: 105e3cb2ef7b904e96dc21013906e0b7444e3b88
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997206"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="e6d2d-103">Darbo valandų šablono kūrimas („Project Service“)</span><span class="sxs-lookup"><span data-stu-id="e6d2d-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e6d2d-104">Norėdami sukurti ir tvarkyti projektą, projektui turite pritaikyti kalendoriaus šabloną.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="e6d2d-105">Kalendoriaus šablonas apibrėžia toliau nurodytus projekto atributus.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="e6d2d-106">Darbo valandos, įskaitant pradžios ir pabaigos laiką</span><span class="sxs-lookup"><span data-stu-id="e6d2d-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="e6d2d-107">Darbo dienos</span><span class="sxs-lookup"><span data-stu-id="e6d2d-107">Working days</span></span>
- <span data-ttu-id="e6d2d-108">Kalendoriaus išimtys, pvz., ne darbo dienos</span><span class="sxs-lookup"><span data-stu-id="e6d2d-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="e6d2d-109">Projektui taikomas kalendoriaus šablonas yra kalendoriaus šablono, apibrėžto organizacijos parametruose, kopija.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="e6d2d-110">Jei kalendoriaus šabloną pakeičiate, šie pakeitimai neišplatinami į projekto darbo valandas.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="e6d2d-111">Norint pakeisti projekto darbo valandas, reikia pritaikyti naują šabloną.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="e6d2d-112">Norint sukurti savo organizacijos kalendoriaus šabloną, taikomi du pagrindiniai toliau nurodyti reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="e6d2d-113">Apibrėžkite norimas šablono darbo valandas naudodami naują arba esamą rezervuojamąjį išteklių.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="e6d2d-114">Sukurkite naują kalendoriaus šabloną ir jį susiekite su rezervuojamuoju ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="e6d2d-115">**Šablono darbo valandų apibrėžimas**</span><span class="sxs-lookup"><span data-stu-id="e6d2d-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="e6d2d-116">Eikite į **Ištekliai** \> **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="e6d2d-117">Sukurkite naują išteklių, kurį norite nurodyti kalendoriaus šablone, arba pasirinkite esamą išteklių.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="e6d2d-118">Pasirinkite ištekliaus skirtuką **Darbo valandos** ir vykdykite nurodymus, pateiktus dalyje [Ištekliaus darbo valandų nustatymas](/dynamics365/field-service/set-work-hours-resource.md), kad būtų sukonfigūruotos kalendoriaus taisyklės.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](/dynamics365/field-service/set-work-hours-resource.md) to configure the calendar rules.</span></span>

<span data-ttu-id="e6d2d-119">**Naujo kalendoriaus šablono sukūrimas**</span><span class="sxs-lookup"><span data-stu-id="e6d2d-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="e6d2d-120">Nueikite į **Parametrai** \> **Kalendoriaus šablonas**.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="e6d2d-121">Pasirinkite **Naujas** ir įveskite pavadinimą, aprašą bei šablono išteklių.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="e6d2d-122">Kai išteklius yra nurodomas kalendoriaus šablone, ištekliaus kalendoriaus kopija susiejama su kalendoriaus šablonu.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="e6d2d-123">Jei nukopijuoto šablono darbo valandos pasikeičia, šie pakeitimai neišplatinami į kalendoriaus šabloną.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="e6d2d-124">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="e6d2d-124">See Also</span></span>  
 [<span data-ttu-id="e6d2d-125">Išteklių nustatymas</span><span class="sxs-lookup"><span data-stu-id="e6d2d-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
