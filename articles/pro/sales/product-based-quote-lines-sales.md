---
title: Produktu pagrįstų pasiūlymo eilučių apžvalga – „Lite“ versija
description: Šioje temoje pateikta informacija apie darbą su produktu pagrįstomis pasiūlymo eilutėmis.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178198"
---
# <a name="product-based-quote-lines-overview---lite"></a><span data-ttu-id="09740-103">Produktu pagrįstų pasiūlymo eilučių apžvalga – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="09740-103">Product-based quote lines overview - lite</span></span>

<span data-ttu-id="09740-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="09740-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="09740-105">Galite kurti produktu pagrįstas pasiūlymo eilutes programoje „Dynamics 365 Project Operations”.</span><span class="sxs-lookup"><span data-stu-id="09740-105">You can create product-based quote lines in Dynamics 365 Project Operations.</span></span> <span data-ttu-id="09740-106">Produktu pagrįstos pasiūlymo eilutės gali būti pridedamos rankiniu būdu arba jos gali būti produktų katalogo elementais.</span><span class="sxs-lookup"><span data-stu-id="09740-106">Product-based quote lines can be manually added, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="09740-107">Produktų katalogas</span><span class="sxs-lookup"><span data-stu-id="09740-107">Product catalog</span></span>

<span data-ttu-id="09740-108">Kiekvienas produktų kataloge esantis produktas turi numatytąjį vienetą ir vieneto grupę.</span><span class="sxs-lookup"><span data-stu-id="09740-108">Each product in the product catalog has a default unit and unit group.</span></span> <span data-ttu-id="09740-109">Jei keli produktai turi tą patį atributų rinkinį, galite sukurti produktų šeimą, kuri taip pat turi šiuos atributus.</span><span class="sxs-lookup"><span data-stu-id="09740-109">If multiple products share the same set of attributes, you can create a product family that share those attributes.</span></span> 

<span data-ttu-id="09740-110">Pavyzdžiui, įmonė parduoda prenumeratos licencijas įvairiai programinei įrangai.</span><span class="sxs-lookup"><span data-stu-id="09740-110">For example, a company sells subscription licenses for different kinds of software.</span></span> <span data-ttu-id="09740-111">Visa prenumeratos programinė įranga turi šiuos du atributus:</span><span class="sxs-lookup"><span data-stu-id="09740-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="09740-112">Vartotojų skaičius</span><span class="sxs-lookup"><span data-stu-id="09740-112">Number of users</span></span>
- <span data-ttu-id="09740-113">Prenumeratos trukmė mėnesiais</span><span class="sxs-lookup"><span data-stu-id="09740-113">A subscription duration measured in months</span></span>

<span data-ttu-id="09740-114">Siekdami išlaikyti šio tipo katalogą, sukurkite produktų šeimą, pavadintą **Prenumeratos programinė įranga**, pridėkite vartotojų skaičių ir prenumeratos trukmę kaip atributus.</span><span class="sxs-lookup"><span data-stu-id="09740-114">To maintain this type of catalog, create a product family named **Subscription Software** and add the number of users and the subscription duration as attributes.</span></span> <span data-ttu-id="09740-115">Tada galite įtraukti atskirus produktus į produktų šeimą **Prenumeratos programinė įranga**.</span><span class="sxs-lookup"><span data-stu-id="09740-115">Next, you can add individual products to the **Subscription Software** product family.</span></span>

## <a name="add-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="09740-116">Produktų katalogo elementų įtraukimas į projekto pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="09740-116">Add product catalog items to a project quote</span></span>

<span data-ttu-id="09740-117">Puslapiuose **Projekto pasiūlymas** ir **Projekto sutartis** yra skyriai, skirti projektu pagrįstoms eilutėms ir produktu pagrįstoms eilutėms.</span><span class="sxs-lookup"><span data-stu-id="09740-117">The **Project Quote** and **Project Contract** pages have sections for project-based lines and product-based lines.</span></span> <span data-ttu-id="09740-118">Produktu pagrįstoms eilutėms pasiūlymo eilutės arba projekto sutarties eilutės išplečiamajame sąraše yra visi produktai ir vienetai, esantys produkto kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="09740-118">For product-based lines, the drop-down list on the quote line or project contract line includes all the products and units in the product price list.</span></span> <span data-ttu-id="09740-119">Taip pat galite įtraukti produktų, kurie neįvardyti produktų kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="09740-119">You can also add products that aren't part of the product price list.</span></span>

<span data-ttu-id="09740-120">Be to, galite pažymėti produktus iš kitų kainoraščių arba tiesiogiai iš produktų katalogo.</span><span class="sxs-lookup"><span data-stu-id="09740-120">Additionally, you can select products from other price lists or directly from the product catalog.</span></span> <span data-ttu-id="09740-121">Kai produktus tiesiogiai žymite iš produktų katalogo, produkto numatytasis kainoraštis naudojamas produkto pardavimo kainai gauti.</span><span class="sxs-lookup"><span data-stu-id="09740-121">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="09740-122">Jei numatytojo kainoraščio nėra, kaina nurodoma kaip nulis (0).</span><span class="sxs-lookup"><span data-stu-id="09740-122">If a default price list isn't set, the price is set to zero (0).</span></span>

<span data-ttu-id="09740-123">Kai pasiūlymo eilutė pagrįsta produktų katalogu, galite perrašyti pardavimo kainą tiesiogiai pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="09740-123">When a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="09740-124">Pasiūlymo eilutė lauke **Kainodara** su dviem galimomis reikšmėmis:</span><span class="sxs-lookup"><span data-stu-id="09740-124">A quote line in **Pricing** field with two available values:</span></span>

- <span data-ttu-id="09740-125">**Perrašyti kainodarą**</span><span class="sxs-lookup"><span data-stu-id="09740-125">**Override Pricing**</span></span>
- <span data-ttu-id="09740-126">**Naudoti numatytąjį**</span><span class="sxs-lookup"><span data-stu-id="09740-126">**Use Default**</span></span>

<span data-ttu-id="09740-127">Jei pažymėsite **Perrašyti kainodarą**, numatytoji kaina nenustatoma.</span><span class="sxs-lookup"><span data-stu-id="09740-127">If you select **Override Pricing**, the default price isn't set.</span></span> <span data-ttu-id="09740-128">Vietoje to pasiūlymo eilutėje turite įvesti produkto kainą.</span><span class="sxs-lookup"><span data-stu-id="09740-128">Instead, you must enter a price for the product on the quote line.</span></span> <span data-ttu-id="09740-129">Jei pažymėsite **Naudoti numatytąsias reikšmes**, naudojama numatytoji pardavimo kaina, o laukas užrakinamas ir negali būti redaguojamas.</span><span class="sxs-lookup"><span data-stu-id="09740-129">If you select **Use Default**, the default sales price is used and the field is locked for editing.</span></span>

<span data-ttu-id="09740-130">Numatytąsias pardavimo kainas galima įvesti pasiūlymo produktu pagrįstose eilutėse.</span><span class="sxs-lookup"><span data-stu-id="09740-130">Default sales prices are entered on the product-based lines of a quote.</span></span> <span data-ttu-id="09740-131">Tada laukas **Kainodara** nustatomas į **Perrašyti kainodarą**, kad galėtumėte redaguoti numatytąją kainą pasiūlymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="09740-131">The **Pricing** field is then set to **Override Pricing** so that you can edit the default price on the quote lines.</span></span> <span data-ttu-id="09740-132">Tai yra konkrečiai „Project Operations” naudojamas perrašymo į produktu pagrįstas eilutes veikimo būdas programoje „Dynamics 365 Sales”.</span><span class="sxs-lookup"><span data-stu-id="09740-132">This is a Project Operations-specific override to the product-based lines behavior in Dynamics 365 Sales.</span></span>
