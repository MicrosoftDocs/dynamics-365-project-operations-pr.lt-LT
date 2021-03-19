---
title: Produktu pagrįstų sutarties eilučių apžvalga – „Lite“ versija
description: Šioje temoje pateikta informacija apie produktu pagrįstas sutarties eilutes.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6e9ef33cc9c79f828e85733f4f5a199bce842700
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272668"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="280bb-103">Produktu pagrįstų sutarties eilučių apžvalga – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="280bb-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="280bb-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="280bb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="280bb-105">Galite kurti produktu pagrįstas sutarties eilutes programoje „Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="280bb-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="280bb-106">Produktu pagrįstos sutarties eilutės gali būti rankiniu būdu sukuriamos eilutės arba tai gali būti prekės iš produktų katalogo.</span><span class="sxs-lookup"><span data-stu-id="280bb-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="280bb-107">Produktų katalogas</span><span class="sxs-lookup"><span data-stu-id="280bb-107">Product catalog</span></span>

<span data-ttu-id="280bb-108">Produktai, esantys produktų kataloge, turi numatytąjį vienetą ir vienetų grupę.</span><span class="sxs-lookup"><span data-stu-id="280bb-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="280bb-109">Jei keli produktai turi tą patį atributų rinkinį, galite sukurti produktų šeimą, kuri taip pat turi šiuos atributus.</span><span class="sxs-lookup"><span data-stu-id="280bb-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="280bb-110">Visi vienos produktų šeimos produktai turi tą patį atributų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="280bb-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="280bb-111">Pavyzdžiui, įmonė parduoda prenumeratos licencijas įvairiai programinei įrangai.</span><span class="sxs-lookup"><span data-stu-id="280bb-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="280bb-112">Visa prenumeratos programinė įranga turi šiuos du atributus:</span><span class="sxs-lookup"><span data-stu-id="280bb-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="280bb-113">Vartotojų skaičius</span><span class="sxs-lookup"><span data-stu-id="280bb-113">Number of users</span></span>
- <span data-ttu-id="280bb-114">Prenumeratos trukmė (mėnesiais)</span><span class="sxs-lookup"><span data-stu-id="280bb-114">Subscription duration (in months)</span></span>

<span data-ttu-id="280bb-115">Norėdami išlaikyti šį katalogo tipą sukurkite produktų šeimą, pavadintą **Prenumeratos programinė įranga**.</span><span class="sxs-lookup"><span data-stu-id="280bb-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="280bb-116">Įtraukite produktų šeimos atributus **Vartotojų skaičius** ir **Prenumeratos trukmė**.</span><span class="sxs-lookup"><span data-stu-id="280bb-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="280bb-117">Tada į **Prenumeratos programinės įrangos** produktų šeimą įtraukite konkrečius produktus.</span><span class="sxs-lookup"><span data-stu-id="280bb-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="280bb-118">Produktų katalogo prekių įtraukimas į projekto sutartį</span><span class="sxs-lookup"><span data-stu-id="280bb-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="280bb-119">Projektų sutartyse yra dviejų tipų eilučių skyriai: pagrįstos projektu ir pagrįstos produktu.</span><span class="sxs-lookup"><span data-stu-id="280bb-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="280bb-120">Produktu pagrįstos eilutės apima visus sutarties produktų kainoraščio produktus ir vienetus.</span><span class="sxs-lookup"><span data-stu-id="280bb-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="280bb-121">Galima įtraukti produktus, kurių nėra sutarties produktų kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="280bb-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="280bb-122">Galite pasirinkti produktus iš kitų kainoraščių arba tiesiai iš produktų katalogo.</span><span class="sxs-lookup"><span data-stu-id="280bb-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="280bb-123">Kai produktus tiesiogiai pasirenkate iš produktų katalogo, produkto pardavimo kainai naudojamas to produkto numatytasis kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="280bb-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="280bb-124">Jei numatytojo kainoraščio nėra, kaina nurodoma kaip 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="280bb-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="280bb-125">Jei sutarties eilutė pagrįsta produktų katalogu, galite perrašyti pardavimo kainą tiesiogiai eilutėje.</span><span class="sxs-lookup"><span data-stu-id="280bb-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="280bb-126">Sutarties eilutėje yra laukas **Kainodara** su dviem reikšmėmis:</span><span class="sxs-lookup"><span data-stu-id="280bb-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="280bb-127">**Perrašyti kainodarą**</span><span class="sxs-lookup"><span data-stu-id="280bb-127">**Override pricing**</span></span>
- <span data-ttu-id="280bb-128">**Naudoti numatytąjį**</span><span class="sxs-lookup"><span data-stu-id="280bb-128">**Use default**</span></span>

<span data-ttu-id="280bb-129">Jei lauką **Kainodara** nustatysite į **Perrašyti kainodarą**, numatytoji kaina nebus nustatyta.</span><span class="sxs-lookup"><span data-stu-id="280bb-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="280bb-130">Įveskite produkto kainą sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="280bb-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="280bb-131">Jei lauką nustatysite į **Naudoti numatytąją**, bus naudojama numatytoji pardavimo kaina ir lauko nebus galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="280bb-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="280bb-132">Įdiegus „Project Operations“ numatytąsias pardavimo kainas galima įvesti produktu pagrįstose sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="280bb-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="280bb-133">Laukas **Kainodara** nustatomas į **Perrašyti kainodarą**, kad galėtumėte redaguoti numatytąją kainą sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="280bb-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="280bb-134">Tai yra „Project Operations“ būdingas perrašymas į produktu pagrįstų eilučių veikimą naudojant „Dynamics 365 Sales“.</span><span class="sxs-lookup"><span data-stu-id="280bb-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]