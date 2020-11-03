---
title: Produktu pagrįstos pasiūlymo eilutės
description: Šioje temoje pateikta informacija apie produktu pagrįstas pasiūlymo eilutes.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55a5b5041a494892e6d96bf24e1bc132a26521dc
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081016"
---
# <a name="product-based-quote-lines"></a><span data-ttu-id="043e0-103">Produktu pagrįstos pasiūlymo eilutės</span><span class="sxs-lookup"><span data-stu-id="043e0-103">Product-based quote lines</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


<span data-ttu-id="043e0-104">Galite kurti produktu pagrįstas pasiūlymo eilutes programoje Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="043e0-104">You can create product-based quote lines in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="043e0-105">Produktu pagrįstos pasiūlymo eilutės gali būti „įrašomos“ eilutės arba produktų katalogo elementai.</span><span class="sxs-lookup"><span data-stu-id="043e0-105">Product-based quote lines can be "write-in" lines, or they can be items from the product catalog.</span></span>

## <a name="product-catalog"></a><span data-ttu-id="043e0-106">Produktų katalogas</span><span class="sxs-lookup"><span data-stu-id="043e0-106">Product catalog</span></span>

<span data-ttu-id="043e0-107">Produktai, esantys „Dynamics 365“ produktų kataloge, turi numatytąjį vienetą ir vieneto grupę.</span><span class="sxs-lookup"><span data-stu-id="043e0-107">The products in a Dynamics 365 product catalog have a default unit and unit group.</span></span> <span data-ttu-id="043e0-108">Jei keli produktai turi tą patį atributų rinkinį, galite sukurti produktų šeimą, kuri taip pat turi šiuos atributus.</span><span class="sxs-lookup"><span data-stu-id="043e0-108">If several products share the same set of attributes, you can create a product family that also has those attributes.</span></span> <span data-ttu-id="043e0-109">Visi vienos produktų šeimos produktai turi tą patį atributų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="043e0-109">All the products in one product family inherit the same set of attributes.</span></span>

<span data-ttu-id="043e0-110">Pavyzdžiui, įmonė parduoda prenumeratos licencijas įvairioms programinėms įrangoms.</span><span class="sxs-lookup"><span data-stu-id="043e0-110">For example, a company sells subscription licenses for a variety of software.</span></span> <span data-ttu-id="043e0-111">Visa prenumeratos programinė įranga turi šiuos du atributus:</span><span class="sxs-lookup"><span data-stu-id="043e0-111">All subscription software has the following two attributes:</span></span>

- <span data-ttu-id="043e0-112">Vartotojų skaičius</span><span class="sxs-lookup"><span data-stu-id="043e0-112">Number of users</span></span> 
- <span data-ttu-id="043e0-113">Prenumeratos trukmė (mėnesiais)</span><span class="sxs-lookup"><span data-stu-id="043e0-113">Subscription duration (in months)</span></span>

<span data-ttu-id="043e0-114">Geras būdas išlaikyti šio tipo katalogą yra sukurti produktų šeimą, pavadintą **Prenumeratos programinė įranga** , ir kuri turi atributus **Vartotojų skaičius** bei **Prenumeratos trukmė**.</span><span class="sxs-lookup"><span data-stu-id="043e0-114">A good way to maintain this type of catalog is to create a product family that is named **Subscription Software** , and that has **Number of users** and **Subscription duration** as attributes.</span></span> <span data-ttu-id="043e0-115">Tada galite įtraukti individualius produktus, pavyzdžiui, **Dynamics 365 Sales** arba **Dynamics 365 Field Service** , į produktų šeimą **Prenumeratos programinė įranga**.</span><span class="sxs-lookup"><span data-stu-id="043e0-115">You can then add individual products, such as **Dynamics 365 Sales** or **Dynamics 365 Field Service** to the **Subscription Software** product family.</span></span>

## <a name="adding-product-catalog-items-to-a-project-quote"></a><span data-ttu-id="043e0-116">Produktų katalogo elementų įtraukimas į projekto pasiūlymą</span><span class="sxs-lookup"><span data-stu-id="043e0-116">Adding product catalog items to a project quote</span></span>

<span data-ttu-id="043e0-117">Projekto pasiūlymo ir projekto sutarties puslapiuose yra dviejų tipų eilučių skyriai: projektu pagrįstos eilutės ir produktu pagrįstos eilutės.</span><span class="sxs-lookup"><span data-stu-id="043e0-117">Project quote and project contract pages have sections for two types of lines: project-based lines and product-based lines.</span></span> <span data-ttu-id="043e0-118">Produktu pagrįstoms eilutėms naudojama „Dynamics 365“, kad įtrauktų elementus iš produktų katalogo į pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="043e0-118">For product-based lines, Dynamics 365 is used to add items from a product catalog to a quote.</span></span> <span data-ttu-id="043e0-119">Pasiūlymo eilutės arba projekto sutarties eilutės išplečiamajame sąraše yra visi produktai ir vienetai, esantys produktų kainoraštyje, kuris pridėtas prie pasiūlymo arba projekto sutarties.</span><span class="sxs-lookup"><span data-stu-id="043e0-119">The drop-down list on the quote line or project contract line includes all the products and units in the product price list that is attached to the quote or project contract.</span></span> <span data-ttu-id="043e0-120">Taip pat galite įtraukti produktų, kurie neįvardyti pasiūlymo produktų kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="043e0-120">You can also add products that aren't part of quote's product price list.</span></span>

<span data-ttu-id="043e0-121">Be to, galite pažymėti produktus iš kitų kainoraščių arba galite pažymėti produktus tiesiogiai iš produktų katalogo.</span><span class="sxs-lookup"><span data-stu-id="043e0-121">Additionally, you can select products from other price lists, or you can select products directly from the product catalog.</span></span> <span data-ttu-id="043e0-122">Kai produktus tiesiogiai žymite iš produktų katalogo, produkto numatytasis kainoraštis naudojamas produkto pardavimo kainai gauti.</span><span class="sxs-lookup"><span data-stu-id="043e0-122">When you select products directly from a product catalog, the default price list of that product is used to get the product's sales price.</span></span> <span data-ttu-id="043e0-123">Jei numatytojo kainoraščio nėra, kaina nurodoma kaip 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="043e0-123">If a default price list isn't set, the price is set to 0 (zero).</span></span>

<span data-ttu-id="043e0-124">Jei pasiūlymo eilutė pagrįsta produktų katalogu, galite perrašyti pardavimo kainą tiesiogiai pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="043e0-124">If a quote line is based on a product catalog, you can override the sales price directly on the quote line.</span></span> <span data-ttu-id="043e0-125">Atminkite, kad pasiūlymo eilutė, esanti „Dynamics 365“ turi lauką **Kainodara**.</span><span class="sxs-lookup"><span data-stu-id="043e0-125">Note that a quote line in Dynamics 365 has a **Pricing** field.</span></span> <span data-ttu-id="043e0-126">Galimos dvi reikšmės:</span><span class="sxs-lookup"><span data-stu-id="043e0-126">Two values are available:</span></span>

- <span data-ttu-id="043e0-127">Perrašyti kainodarą</span><span class="sxs-lookup"><span data-stu-id="043e0-127">Override pricing</span></span>  
- <span data-ttu-id="043e0-128">Naudoti numatytąją</span><span class="sxs-lookup"><span data-stu-id="043e0-128">Use default</span></span>

<span data-ttu-id="043e0-129">Jei šį lauką nustatysite į **Perrašyti kainodarą** , „Dynamics 365“ nenustato numatytosios kainos.</span><span class="sxs-lookup"><span data-stu-id="043e0-129">If you set this field to **Override pricing** , Dynamics 365 doesn't set a default price.</span></span> <span data-ttu-id="043e0-130">Pasiūlymo eilutėje turite įvesti produkto kainą.</span><span class="sxs-lookup"><span data-stu-id="043e0-130">You must enter a price for the product on the quote line.</span></span> <span data-ttu-id="043e0-131">Jei šį lauką nustatysite į **Naudoti numatytąją** , „Dynamics 365“ naudoja numatytąją pardavimo kainą ir užrakina lauką, kad jo nebūtų galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="043e0-131">If you set this field to **Use default** , Dynamics 365 uses the default sales price and locks the field to prevent editing.</span></span>

<span data-ttu-id="043e0-132">Įdiegus PSA numatytąsias pardavimo kainas galima įvesti pasiūlymo produktu pagrįstose eilutėse.</span><span class="sxs-lookup"><span data-stu-id="043e0-132">After you install PSA, default sales prices are entered on the product-based lines on a quote.</span></span> <span data-ttu-id="043e0-133">Tada laukas **Kainodara** nustatomas į **Perrašyti kainodarą** , kad galėtumėte redaguoti numatytąją kainą pasiūlymo eilutėse.</span><span class="sxs-lookup"><span data-stu-id="043e0-133">The **Pricing** field is then set to **Override pricing** so that you can edit the default price on the quote lines.</span></span>

> ![Kainodaros perrašymo nustatymas](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a><span data-ttu-id="043e0-135">Produktų kiekio koeficientai</span><span class="sxs-lookup"><span data-stu-id="043e0-135">Quantity factors for products</span></span>

<span data-ttu-id="043e0-136">Programoje PSA naudojami kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas.</span><span class="sxs-lookup"><span data-stu-id="043e0-136">PSA uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="043e0-137">Prenumerata pagrįstiems produktams pasiūlymo arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.</span><span class="sxs-lookup"><span data-stu-id="043e0-137">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user months.</span></span>

<span data-ttu-id="043e0-138">Paprastai prenumeratos programinės įrangos kaina kataloge yra kaina vienam vartotojui per mėnesį.</span><span class="sxs-lookup"><span data-stu-id="043e0-138">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="043e0-139">Tačiau vietoje to galite naudoti kitus laiko aprašus.</span><span class="sxs-lookup"><span data-stu-id="043e0-139">However, you can use other time descriptions instead.</span></span> <span data-ttu-id="043e0-140">Per pardavimo procesą pasiūlymo eilutėje nurodyta kaina paprastai yra vienam vartotojui per mėnesį, dėl kurios susitarė ir nuolaidą pritaikė IT pardavimo agentas.</span><span class="sxs-lookup"><span data-stu-id="043e0-140">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="043e0-141">Kiekvienas sandoris turi skirtingą vartotojų skaičių ir skirtingą prenumeratos mėnesių skaičių.</span><span class="sxs-lookup"><span data-stu-id="043e0-141">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="043e0-142">Kiekis, naudojamas pasiūlymo eilutės sumai apskaičiuoti, yra vartotojų skaičiaus ir prenumeratos mėnesių skaičiaus produktas.</span><span class="sxs-lookup"><span data-stu-id="043e0-142">The quantity that is used to compute the amount of the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="043e0-143">Norėdami paremti šį pardavimo tipą, PSA pristatė kiekio koeficientų koncepciją.</span><span class="sxs-lookup"><span data-stu-id="043e0-143">To support this type of sale, PSA introduced the concept of quantity factors.</span></span> <span data-ttu-id="043e0-144">Kiekio koeficientai priklauso nuo „Dynamics 365“ produkto atributų.</span><span class="sxs-lookup"><span data-stu-id="043e0-144">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="043e0-145">Konfigūruojant konkrečias produkto ypatybes, PSA leidžia žymėti tų ypatybių pogrupį arba visas ypatybes kaip kiekio koeficientus.</span><span class="sxs-lookup"><span data-stu-id="043e0-145">When you configure specific properties for a product, PSA lets you flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="043e0-146">PSA tikrina, kad tik skaitinės ypatybės arba produkto, turinčio skaitinių duomenų tipą, ypatybės būtų žymimos kaip kiekio koeficientai.</span><span class="sxs-lookup"><span data-stu-id="043e0-146">PSA validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="043e0-147">Kai produktas, kuriam sukonfigūruoti kiekio koeficientai, yra įtraukiamas į pasiūlymo eilutę, pasiūlymo eilutėje esantis laukas **Kiekis** tampa tik skaitomu lauku.</span><span class="sxs-lookup"><span data-stu-id="043e0-147">When a product that quantity factors are configured for is added to a quote line, the **Quantity** field on the quote line becomes a read-only field.</span></span> <span data-ttu-id="043e0-148">Įvedus produktų ypatybių reikšmes, kurios yra kiekio koeficientai, PSA apskaičiuoja pasiūlymo eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="043e0-148">After you enter values for product properties that are quantity factors, PSA computes the quantity of the quote line.</span></span>

<span data-ttu-id="043e0-149">Pavyzdžiui, „Dynamics 365“ gali turėti šias ypatybes:</span><span class="sxs-lookup"><span data-stu-id="043e0-149">For example, Dynamics 365 might have the following properties:</span></span> 

- <span data-ttu-id="043e0-150">**Vartotojų skaičius** – vartotojų skaičius</span><span class="sxs-lookup"><span data-stu-id="043e0-150">**No of users** - The number of users</span></span> 
- <span data-ttu-id="043e0-151">**Mėnesių skaičius** – prenumeratos mėnesių skaičius</span><span class="sxs-lookup"><span data-stu-id="043e0-151">**No of Months** - The number of subscription months</span></span>
- <span data-ttu-id="043e0-152">**Produkto SKU**</span><span class="sxs-lookup"><span data-stu-id="043e0-152">**Product SKU**</span></span> 

<span data-ttu-id="043e0-153">Ypatybės **Vartotojų skaičius** ir **Mėnesių skaičius** gali būti pažymėtos kaip kiekio koeficientai redaguojant produkto eilutės ypatybes.</span><span class="sxs-lookup"><span data-stu-id="043e0-153">Tne **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span> 

> ![Vartotojų ir mėnesių skaičių žymėjimas kaip kiekio koeficientai](media/basic-guide-11.png)
 
