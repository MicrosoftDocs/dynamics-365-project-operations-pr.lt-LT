---
title: Darbo standartinių kainų ir išlaidų konfigūravimas
description: Šioje temoje paaiškinama, kaip nustatyti projekto darbo standartines kainas ir išlaidas.
author: Yowelle
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 517e5ae776cff18aec81e5446a7aaedfba61ac0c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011021"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="7c6b1-103">Darbo standartinių kainų ir išlaidų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="7c6b1-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="7c6b1-104">Šioje temoje paaiškinama, kaip nustatyti projekto darbo standartines kainas ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="7c6b1-105">Šiai užduočiai atlikti naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="7c6b1-106">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Savikaina (val.)**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="7c6b1-107">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-107">Select **New**.</span></span>
3. <span data-ttu-id="7c6b1-108">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="7c6b1-109">Lauke **Savikaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="7c6b1-110">Galite nustatyti projekto kategorijos standartinę savikainą arba galite nustatyti savikainą pagal darbuotojo numerį, projekto numerį, kategoriją, datą arba bet kokią jų kombinaciją.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="7c6b1-111">Taikoma savikaina yra pati išsamiausia savikaina.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="7c6b1-112">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-112">Select **Save**.</span></span>
6. <span data-ttu-id="7c6b1-113">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (val.)**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="7c6b1-114">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-114">Select **New**.</span></span>
8. <span data-ttu-id="7c6b1-115">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="7c6b1-116">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="7c6b1-117">Lauke **Kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="7c6b1-118">Galite nustatyti standartinę valandinių operacijų arba projekto kategorijos pardavimo kainą.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="7c6b1-119">Taip pat galite nustatyti pardavimo kainas pagal darbuotojo numerį, projekto numerį, kategoriją, operacijos datą arba bet kokią jų kombinaciją.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="7c6b1-120">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operaciją į valandų žurnalą, yra išsamiausia pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="7c6b1-121">Pavyzdžiui, jei nustatyta bendra pardavimo kaina ir konkreti darbuotojo pardavimo kaina, naudojama konkreti darbuotojo pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="7c6b1-122">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-122">Select **Save**.</span></span>
12. <span data-ttu-id="7c6b1-123">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-123">Close the page.</span></span>
13. <span data-ttu-id="7c6b1-124">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Savikaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="7c6b1-125">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-125">Select **New**.</span></span>
15. <span data-ttu-id="7c6b1-126">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="7c6b1-127">Lauke **Savikaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="7c6b1-128">Galima užpildyti kelis laukus ir tai yra minimumas norint įrašyti įrašą.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="7c6b1-129">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-129">Select **Save**.</span></span>
18. <span data-ttu-id="7c6b1-130">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Pardavimo kaina (išlaidos)**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="7c6b1-131">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-131">Select **New**.</span></span>
20. <span data-ttu-id="7c6b1-132">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="7c6b1-133">Lauke **Galioja iki** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="7c6b1-134">Lauke **Kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="7c6b1-135">Faktinė pardavimo kaina, taikoma darbuotojui įvedus operacijas į išlaidų žurnalą, yra išsamiausia pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="7c6b1-136">Pavyzdžiui, jei nustatyta bendra ir konkreti darbuotojo pardavimo kaina, naudojama konkreti darbuotojo pardavimo kaina.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="7c6b1-137">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7c6b1-137">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]