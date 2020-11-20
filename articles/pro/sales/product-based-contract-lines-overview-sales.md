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
ms.openlocfilehash: eb09140eae5383b882db73195d0360a836ece791
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177881"
---
# <a name="product-based-contract-lines-overview---lite"></a><span data-ttu-id="3d7e0-103">Produktu pagrįstų sutarties eilučių apžvalga – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="3d7e0-103">Product-based contract lines overview - lite</span></span>

<span data-ttu-id="3d7e0-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="3d7e0-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="3d7e0-105">Produktu pagrįstas sutarties eilutes galite sukurti naudodami „Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-105">You can create product-based contract lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="3d7e0-106">Produktu pagrįstos sutarties eilutės gali būti rankiniu būdu sukuriamos eilutės arba tai gali būti prekės iš produktų katalogo.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-106">Product-based contract lines can be manually created lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="3d7e0-107">Produktų katalogas</span><span class="sxs-lookup"><span data-stu-id="3d7e0-107">Product catalog</span></span>

<span data-ttu-id="3d7e0-108">Produktai, esantys produktų kataloge, turi numatytąjį vienetą ir vienetų grupę.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-108">The products in the product catalog have a default unit and unit group.</span></span> <span data-ttu-id="3d7e0-109">Jei keli produktai turi tą patį atributų rinkinį, galite sukurti produktų šeimą, kuri taip pat turi šiuos atributus.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-109">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="3d7e0-110">Visi vienos produktų šeimos produktai turi tą patį atributų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-110">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="3d7e0-111">Pavyzdžiui, įmonė parduoda prenumeratos licencijas įvairiai programinei įrangai.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-111">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="3d7e0-112">Visa prenumeratos programinė įranga turi šiuos du atributus:</span><span class="sxs-lookup"><span data-stu-id="3d7e0-112">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="3d7e0-113">Vartotojų skaičius</span><span class="sxs-lookup"><span data-stu-id="3d7e0-113">Number of users</span></span>
- <span data-ttu-id="3d7e0-114">Prenumeratos trukmė (mėnesiais)</span><span class="sxs-lookup"><span data-stu-id="3d7e0-114">Subscription duration (in months)</span></span>

<span data-ttu-id="3d7e0-115">Norėdami išlaikyti šį katalogo tipą sukurkite produktų šeimą, pavadintą **Prenumeratos programinė įranga**.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-115">To maintain this type of catalog, create a product family that is named **Subscription Software**.</span></span> <span data-ttu-id="3d7e0-116">Įtraukite produktų šeimos atributus **Vartotojų skaičius** ir **Prenumeratos trukmė**.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-116">Add the attributes, **Number of users** and **Subscription duration** to the product family.</span></span> <span data-ttu-id="3d7e0-117">Tada į **Prenumeratos programinės įrangos** produktų šeimą įtraukite konkrečius produktus.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-117">Then, add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-contract"></a><span data-ttu-id="3d7e0-118">Produktų katalogo prekių įtraukimas į projekto sutartį</span><span class="sxs-lookup"><span data-stu-id="3d7e0-118">Add product catalog items to a project Contract</span></span>

<span data-ttu-id="3d7e0-119">Projektų sutartyse yra dviejų tipų eilučių skyriai: pagrįstos projektu ir pagrįstos produktu.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-119">Project contracts have sections for two types of lines, project-based and product-based.</span></span> <span data-ttu-id="3d7e0-120">Produktu pagrįstos eilutės apima visus sutarties produktų kainoraščio produktus ir vienetus.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-120">Product-based lines include all of the products and units in the product price list on the contract.</span></span> <span data-ttu-id="3d7e0-121">Galima įtraukti produktus, kurių nėra sutarties produktų kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-121">Products that aren't part of contract's product price list can be added.</span></span>

<span data-ttu-id="3d7e0-122">Galite pasirinkti produktus iš kitų kainoraščių arba tiesiai iš produktų katalogo.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-122">You can select products from other price lists, or directly from the product catalog.</span></span> <span data-ttu-id="3d7e0-123">Kai produktus tiesiogiai pasirenkate iš produktų katalogo, produkto pardavimo kainai naudojamas to produkto numatytasis kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-123">When you select products directly from a product catalog, the default price list of that product is used for the product's sales price.</span></span> <span data-ttu-id="3d7e0-124">Jei numatytojo kainoraščio nėra, kaina nurodoma kaip 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="3d7e0-124">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="3d7e0-125">Jei sutarties eilutė pagrįsta produktų katalogu, galite perrašyti pardavimo kainą tiesiogiai eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-125">If a contract line is based on a product catalog, you can override the sales price directly on the line.</span></span> <span data-ttu-id="3d7e0-126">Sutarties eilutėje yra laukas **Kainodara** su dviem reikšmėmis:</span><span class="sxs-lookup"><span data-stu-id="3d7e0-126">A contract line has the **Pricing** field with the two values:</span></span>

- <span data-ttu-id="3d7e0-127">**Perrašyti kainodarą**</span><span class="sxs-lookup"><span data-stu-id="3d7e0-127">**Override pricing**</span></span>
- <span data-ttu-id="3d7e0-128">**Naudoti numatytąjį**</span><span class="sxs-lookup"><span data-stu-id="3d7e0-128">**Use default**</span></span>

<span data-ttu-id="3d7e0-129">Jei lauką **Kainodara** nustatysite į **Perrašyti kainodarą**, numatytoji kaina nebus nustatyta.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-129">If you set the **Pricing** field to **Override pricing**, the default price isn't set.</span></span> <span data-ttu-id="3d7e0-130">Įveskite produkto kainą sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-130">Enter a price for the product on the contract line.</span></span> <span data-ttu-id="3d7e0-131">Jei lauką nustatysite į **Naudoti numatytąją**, bus naudojama numatytoji pardavimo kaina ir lauko nebus galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-131">If you set the field to **Use default**, the default sales price is used and the field can't be edited.</span></span>

<span data-ttu-id="3d7e0-132">Įdiegus „Project Operations“ numatytąsias pardavimo kainas galima įvesti produktu pagrįstose sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-132">After you install Project Operations, default sales prices are entered on the product-based lines on a contract.</span></span> <span data-ttu-id="3d7e0-133">Laukas **Kainodara** nustatomas į **Perrašyti kainodarą**, kad galėtumėte redaguoti numatytąją kainą sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-133">The **Pricing** field is set to **Override pricing** so that you can edit the default price on the contract lines.</span></span> <span data-ttu-id="3d7e0-134">Tai yra „Project Operations“ būdingas perrašymas į produktu pagrįstų eilučių veikimą naudojant „Dynamics 365 Sales“.</span><span class="sxs-lookup"><span data-stu-id="3d7e0-134">This is a Project Operations-specific override to product-based lines behavior in Dynamics 365 Sales.</span></span>
