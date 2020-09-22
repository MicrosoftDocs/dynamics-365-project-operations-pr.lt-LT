---
title: Darbo standartinių kainų ir išlaidų konfigūravimas
description: Šioje temoje paaiškinama, kaip nustatyti projekto darbo standartines kainas ir išlaidas.
author: KimANelson
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.assetid: fa7c024f-4b18-4d29-9fd4-9c430cd83fad
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f3e796cc03aeaa28938c56ce37d5075755248dfa
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753787"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="d4825-103">Darbo standartinių kainų ir išlaidų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="d4825-103">Configure standard costs for labor and expenses</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d4825-104">Šioje temoje paaiškinama, kaip nustatyti projekto darbo standartines kainas ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="d4825-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="d4825-105">Šiai užduočiai atlikti naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="d4825-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="d4825-106">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Savikaina (val.)**.</span><span class="sxs-lookup"><span data-stu-id="d4825-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="d4825-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d4825-107">Select **New**.</span></span>
3. <span data-ttu-id="d4825-108">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d4825-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="d4825-109">Lauke **Savikaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d4825-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="d4825-110">Galite nustatyti projekto kategorijos standartinę savikainą arba galite nustatyti savikainą pagal darbuotojo numerį, projekto numerį, kategoriją, datą arba bet kokią jų kombinaciją.</span><span class="sxs-lookup"><span data-stu-id="d4825-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="d4825-111">Taikoma savikaina yra pati išsamiausia savikaina.</span><span class="sxs-lookup"><span data-stu-id="d4825-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="d4825-112">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d4825-112">Select **Save**.</span></span>
6. <span data-ttu-id="d4825-113">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (val.)**.</span><span class="sxs-lookup"><span data-stu-id="d4825-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="d4825-114">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d4825-114">Select **New**.</span></span>
8. <span data-ttu-id="d4825-115">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d4825-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="d4825-116">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="d4825-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="d4825-117">Lauke **Kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d4825-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="d4825-118">Galite nustatyti standartinę valandinių operacijų arba projekto kategorijos pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="d4825-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="d4825-119">Taip pat galite nustatyti pardavimo kainas pagal darbuotojo numerį, projekto numerį, kategoriją, operacijos datą arba bet kokią jų kombinaciją.</span><span class="sxs-lookup"><span data-stu-id="d4825-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="d4825-120">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operaciją į valandų žurnalą, yra išsamiausia pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="d4825-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="d4825-121">Pavyzdžiui, jei nustatyta bendra pardavimo kaina ir konkreti darbuotojo pardavimo kaina, naudojama konkreti darbuotojo pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="d4825-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="d4825-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d4825-122">Select **Save**.</span></span>
12. <span data-ttu-id="d4825-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="d4825-123">Close the page.</span></span>
13. <span data-ttu-id="d4825-124">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Savikaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="d4825-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="d4825-125">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d4825-125">Select **New**.</span></span>
15. <span data-ttu-id="d4825-126">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d4825-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="d4825-127">Lauke **Savikaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d4825-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="d4825-128">Galima užpildyti kelis laukus ir tai yra minimumas norint įrašyti įrašą.</span><span class="sxs-lookup"><span data-stu-id="d4825-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="d4825-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d4825-129">Select **Save**.</span></span>
18. <span data-ttu-id="d4825-130">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="d4825-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="d4825-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="d4825-131">Select **New**.</span></span>
20. <span data-ttu-id="d4825-132">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="d4825-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="d4825-133">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="d4825-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="d4825-134">Lauke **Kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="d4825-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="d4825-135">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operacijas į išlaidų žurnalą, yra išsamiausia pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="d4825-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="d4825-136">Pavyzdžiui, jei nustatyta bendra ir konkreti darbuotojo pardavimo kaina, naudojama konkreti darbuotojo pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="d4825-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="d4825-137">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="d4825-137">Select **Save**.</span></span>

