---
title: Išlaidų kategorijų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti išlaidų kategorijas ir bendrai naudojamas išlaidų ataskaitų kategorijas.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: f051d70f3dfe3b241dc0a206c0cdfda000f87c76
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080726"
---
# <a name="set-up-expense-categories"></a><span data-ttu-id="6d79e-103">Išlaidų kategorijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="6d79e-103">Set up expense categories</span></span>

<span data-ttu-id="6d79e-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="6d79e-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="6d79e-105">Kai darbuotojai kuria išlaidų ataskaitas, visos užregistruotos išlaidos turi būti susietos su išlaidų kategorija.</span><span class="sxs-lookup"><span data-stu-id="6d79e-105">When employees create expense reports, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="6d79e-106">Išlaidų kategorijos gaunamos iš bendrai naudojamų kategorijų, kurias galima bendrai naudoti jūsų organizacijos juridiniuose subjektuose.</span><span class="sxs-lookup"><span data-stu-id="6d79e-106">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="6d79e-107">Atsižvelgiant į jūsų organizacijos pobūdį, šias išlaidų kategorijas taip pat galima bendrai naudoti kitose srityse.</span><span class="sxs-lookup"><span data-stu-id="6d79e-107">Depending on how your organization is defined, these expense categories can also be shared in other areas.</span></span> <span data-ttu-id="6d79e-108">Atsižvelgdami į savo organizacijos pobūdį ir diegimo komandos pateiktus nurodymus, turite nustatyti, ar kategorijos, naudojamos dalyje Išlaidų valdymas, bus naudojamos tik dalyje Išlaidų valdymas ar bus bendrai naudojamos ir kitose srityse.</span><span class="sxs-lookup"><span data-stu-id="6d79e-108">Based on the definition of your organization and guidance from the implementation team, you must determine whether the categories that are used in Expense management will be used only in Expense management or should be shared in other areas.</span></span>

> [!NOTE]
> <span data-ttu-id="6d79e-109">Šias kategorijas galima bendrai naudoti dalyse Projektų valdymas ir apskaita ir Išlaidų valdymas arba dalyse Projektų valdymas ir apskaita ir Gamyba.</span><span class="sxs-lookup"><span data-stu-id="6d79e-109">These categories can be shared between Project management and accounting and Expense management, or between Project management and accounting and Production.</span></span> <span data-ttu-id="6d79e-110">Tačiau jų negalima bendrai naudoti dalyse Išlaidų valdymas ir Gamyba.</span><span class="sxs-lookup"><span data-stu-id="6d79e-110">However, they can't be shared between Expense management and Production.</span></span>

<span data-ttu-id="6d79e-111">Kad galėtumėte pradėti sąrankos procesą, reikia priimti toliau nurodytus sprendimus dėl kiekvienos išlaidų kategorijos:</span><span class="sxs-lookup"><span data-stu-id="6d79e-111">Before you can begin the setup process, the following decisions must be made for each expense category:</span></span>

- <span data-ttu-id="6d79e-112">Kokia tai yra išlaidų kategorija?</span><span class="sxs-lookup"><span data-stu-id="6d79e-112">What is the expense category?</span></span> <span data-ttu-id="6d79e-113">Pavyzdžiui, skrydžių, viešbučių arba kilometražo kategorijos.</span><span class="sxs-lookup"><span data-stu-id="6d79e-113">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="6d79e-114">Ar išlaidų kategoriją taip pat galima naudoti dalyje Projektų valdymas ir apskaita?</span><span class="sxs-lookup"><span data-stu-id="6d79e-114">Can the expense category also be used in Project management and accounting?</span></span> <span data-ttu-id="6d79e-115">Jei galima, taip pat reikia priimti toliau nurodytus sprendimus:</span><span class="sxs-lookup"><span data-stu-id="6d79e-115">If it can, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6d79e-116">Kokios išlaidų sąskaitos bus naudojamos šioms išlaidoms?</span><span class="sxs-lookup"><span data-stu-id="6d79e-116">Which cost accounts will be used for the following expenses?</span></span>

        - <span data-ttu-id="6d79e-117">Savikaina</span><span class="sxs-lookup"><span data-stu-id="6d79e-117">Cost</span></span>
        - <span data-ttu-id="6d79e-118">Atlyginimo paskirstymas</span><span class="sxs-lookup"><span data-stu-id="6d79e-118">Payroll allocation</span></span>
        - <span data-ttu-id="6d79e-119">NG – Savikaina</span><span class="sxs-lookup"><span data-stu-id="6d79e-119">WIP-cost value</span></span>
        - <span data-ttu-id="6d79e-120">Išlaidos – Prekė</span><span class="sxs-lookup"><span data-stu-id="6d79e-120">Cost-item</span></span>
        - <span data-ttu-id="6d79e-121">NG – Išlaidų vertė – Prekė</span><span class="sxs-lookup"><span data-stu-id="6d79e-121">WIP-cost value-item</span></span>
        - <span data-ttu-id="6d79e-122">Sukauptas nuostolis</span><span class="sxs-lookup"><span data-stu-id="6d79e-122">Accrued loss</span></span>
        - <span data-ttu-id="6d79e-123">NG – sukauptas nuostolis</span><span class="sxs-lookup"><span data-stu-id="6d79e-123">WIP-accrued loss</span></span>

    - <span data-ttu-id="6d79e-124">Kokios įplaukų sąskaitos bus naudojamos šiems įplaukų šaltiniams?</span><span class="sxs-lookup"><span data-stu-id="6d79e-124">Which revenue accounts will be used for the following sources of revenue?</span></span>

        - <span data-ttu-id="6d79e-125">Įplaukos, kurioms išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="6d79e-125">Invoiced revenue</span></span>
        - <span data-ttu-id="6d79e-126">Sukauptos įplaukos – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="6d79e-126">Accrued revenue-sales value</span></span>
        - <span data-ttu-id="6d79e-127">NG – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="6d79e-127">WIP-sales value</span></span>
        - <span data-ttu-id="6d79e-128">Sukauptos įplaukos – Gamyba</span><span class="sxs-lookup"><span data-stu-id="6d79e-128">Accrued revenue-production</span></span>
        - <span data-ttu-id="6d79e-129">NG – Gamyba</span><span class="sxs-lookup"><span data-stu-id="6d79e-129">WIP-production</span></span>
        - <span data-ttu-id="6d79e-130">Sukauptos įplaukos – Pelnas</span><span class="sxs-lookup"><span data-stu-id="6d79e-130">Accrued revenue-profit</span></span>
        - <span data-ttu-id="6d79e-131">NG – Pelnas</span><span class="sxs-lookup"><span data-stu-id="6d79e-131">WIP-profit</span></span>
        - <span data-ttu-id="6d79e-132">Sukauptos įplaukos – Abonementas</span><span class="sxs-lookup"><span data-stu-id="6d79e-132">Accrued revenue-subscription</span></span>
        - <span data-ttu-id="6d79e-133">NG – Abonementas</span><span class="sxs-lookup"><span data-stu-id="6d79e-133">WIP-subscription</span></span>

- <span data-ttu-id="6d79e-134">Koks tai yra išlaidų tipas?</span><span class="sxs-lookup"><span data-stu-id="6d79e-134">What is the expense type?</span></span>
- <span data-ttu-id="6d79e-135">Koks yra numatytasis išlaidų kategorijos mokėjimo būdas?</span><span class="sxs-lookup"><span data-stu-id="6d79e-135">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="6d79e-136">Ar išlaidų kategorijos išlaidos turi būti detaliai išvardytos?</span><span class="sxs-lookup"><span data-stu-id="6d79e-136">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="6d79e-137">Kokia yra pagrindinė numatytoji išlaidų kategorijos sąskaita?</span><span class="sxs-lookup"><span data-stu-id="6d79e-137">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="6d79e-138">Kokia yra numatytoji išlaidų kategorijos prekės PVM grupė?</span><span class="sxs-lookup"><span data-stu-id="6d79e-138">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="6d79e-139">Ar leidžiami papildomi išlaidų kategorijos mokėjimo būdai?</span><span class="sxs-lookup"><span data-stu-id="6d79e-139">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="6d79e-140">Jei taip, kokie jie?</span><span class="sxs-lookup"><span data-stu-id="6d79e-140">If so, what are they?</span></span>
- <span data-ttu-id="6d79e-141">Ar šioje išlaidų kategorijoje yra subkategorijų?</span><span class="sxs-lookup"><span data-stu-id="6d79e-141">Are there subcategories in this expense category?</span></span> <span data-ttu-id="6d79e-142">Jei yra subkategorijų, taip pat reikia priimti toliau nurodytus sprendimus:</span><span class="sxs-lookup"><span data-stu-id="6d79e-142">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="6d79e-143">Ar kokioms nors subkategorijoms netaikomas mokesčių susigrąžinimas?</span><span class="sxs-lookup"><span data-stu-id="6d79e-143">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="6d79e-144">Kokia yra subkategorijų prekės PVM grupė?</span><span class="sxs-lookup"><span data-stu-id="6d79e-144">What is the item sales tax group of the subcategories?</span></span>
