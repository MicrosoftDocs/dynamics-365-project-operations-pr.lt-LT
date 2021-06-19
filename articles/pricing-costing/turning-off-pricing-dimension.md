---
title: Kainodaros dimensijos išjungimas
description: Šioje temoje pateikiama informacija apie tai, kaip išjungti kainodaros dimensijas.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 7b7c1d1b3363c0d158fcf6fda532822354b852a3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004541"
---
# <a name="turning-off-a-pricing-dimension"></a><span data-ttu-id="1234b-103">Kainodaros dimensijos išjungimas</span><span class="sxs-lookup"><span data-stu-id="1234b-103">Turning off a pricing dimension</span></span>

<span data-ttu-id="1234b-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="1234b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="1234b-105">Kas kelerius metus gali reikėti peržiūrėti ir atnaujinti savo kainodaros strategiją.</span><span class="sxs-lookup"><span data-stu-id="1234b-105">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="1234b-106">Dėl bet kokių atliktų atnaujinimų gali reikėti išjungti esamą kainodaros dimensiją ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="1234b-106">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="1234b-107">Pavyzdžiui, galbūt anksčiau kainą nustatėte pagal **Vaidmenį**, tačiau dabar nusprendėte kainą nustatyti pagal **Darbo patirtį**.</span><span class="sxs-lookup"><span data-stu-id="1234b-107">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="1234b-108">Tam gali reikėti išjungti **Vaidmenį** kaip kainodaros dimensiją ir sukurti **Darbo patirtį** kaip naują kainodaros dimensiją.</span><span class="sxs-lookup"><span data-stu-id="1234b-108">This may require you to turn off **Role** as a pricing dimension and create **Work Experience** as a new pricing dimension.</span></span> 

<span data-ttu-id="1234b-109">Kainodaros dimensiją, neatsižvelgiant į tai, ar ji yra iš anksto nustatyta, ar pasirinktinė, galima išjungti kainodaros dimensijos laukus **Taikomai savikainai** ir **Taikoma pardavimui** nustačius kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="1234b-109">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="1234b-110">Tačiau, kai tai padarysite, gali būti parodytas klaidos pranešimas **Kainodaros dimensija negalima atnaujinti arba panaikinti, jei yra susietųjų kainų įrašai.**</span><span class="sxs-lookup"><span data-stu-id="1234b-110">However, when you do this, you might receive the error message, **Pricing dimension cannot be updated or deleted if there are associated price records.**</span></span>

![Išjungus kainodaros dimensiją gali įvykti veiklos proceso klaida](media/Business-Process-Error.png)

<span data-ttu-id="1234b-112">Šis klaidos pranešimas rodo, kad yra kainų įrašų, kurie prieš tai buvo nustatyti dimensijai, kuri išjungiama.</span><span class="sxs-lookup"><span data-stu-id="1234b-112">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="1234b-113">Reikia panaikinti visus dimensiją nurodančius įrašus **Vaidmens kaina** ir **Vaidmens kainos antkainis**, o tik tada dimensijos taikymą galima nustatyti kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="1234b-113">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="1234b-114">Ši taisyklė taikoma ir iš anksto nustatytoms kainodaros dimensijoms, ir bet kurioms jūsų sukurtoms pasirinktinėms kainodaros dimensijoms.</span><span class="sxs-lookup"><span data-stu-id="1234b-114">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="1234b-115">Šio tikrinimo priežastis yra ta, kad kiekvienas įrašas **Vaidmens kaina** turi turėti unikalų dimensijų derinį.</span><span class="sxs-lookup"><span data-stu-id="1234b-115">The reason for this validation is because each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="1234b-116">Pavyzdžiui, kainų sąraše, pavadintame **JAV išlaidų tarifai 2018**, yra šios **Vaidmens kainos** eilutės.</span><span class="sxs-lookup"><span data-stu-id="1234b-116">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="1234b-117">Standartinis pavadinimas</span><span class="sxs-lookup"><span data-stu-id="1234b-117">Standard Title</span></span>         | <span data-ttu-id="1234b-118">Org. vienetai</span><span class="sxs-lookup"><span data-stu-id="1234b-118">Org Unit</span></span>    |<span data-ttu-id="1234b-119">Vienetas</span><span class="sxs-lookup"><span data-stu-id="1234b-119">Unit</span></span>   |<span data-ttu-id="1234b-120">Kainos</span><span class="sxs-lookup"><span data-stu-id="1234b-120">Price</span></span>  |<span data-ttu-id="1234b-121">Valiuta</span><span class="sxs-lookup"><span data-stu-id="1234b-121">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="1234b-122">Sistemos inžinierius</span><span class="sxs-lookup"><span data-stu-id="1234b-122">Systems Engineer</span></span>|<span data-ttu-id="1234b-123">„Contoso“ JAV</span><span class="sxs-lookup"><span data-stu-id="1234b-123">Contoso US</span></span>|<span data-ttu-id="1234b-124">Valanda</span><span class="sxs-lookup"><span data-stu-id="1234b-124">Hour</span></span>| <span data-ttu-id="1234b-125">100</span><span class="sxs-lookup"><span data-stu-id="1234b-125">100</span></span>|<span data-ttu-id="1234b-126">USD</span><span class="sxs-lookup"><span data-stu-id="1234b-126">USD</span></span>|
| <span data-ttu-id="1234b-127">Vyresnysis sistemos inžinierius</span><span class="sxs-lookup"><span data-stu-id="1234b-127">Senior Systems Engineer</span></span>|<span data-ttu-id="1234b-128">„Contoso“ JAV</span><span class="sxs-lookup"><span data-stu-id="1234b-128">Contoso US</span></span>|<span data-ttu-id="1234b-129">Valanda</span><span class="sxs-lookup"><span data-stu-id="1234b-129">Hour</span></span>| <span data-ttu-id="1234b-130">150</span><span class="sxs-lookup"><span data-stu-id="1234b-130">150</span></span>| <span data-ttu-id="1234b-131">USD</span><span class="sxs-lookup"><span data-stu-id="1234b-131">USD</span></span>|


<span data-ttu-id="1234b-132">Kai **Standartinį pavadinimą** išjungsite kaip kainodaros dimensiją, o kainodaros modulis ieškos kainos, iš įvesties konteksto ji naudos tik reikšmę **Org. vienetas**.</span><span class="sxs-lookup"><span data-stu-id="1234b-132">When you turn off **Standard Title** as the pricing dimension, and the pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="1234b-133">Jei įvesties konteksto **Org. vienetas** yra „Contoso US“, rezultatas bus nedeterminuotas, nes abi eilutės sutaps.</span><span class="sxs-lookup"><span data-stu-id="1234b-133">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="1234b-134">Kad būtų išvengta tokio scenarijaus, kai kuriate įrašus **Vaidmens kaina** sistema tikrina, ar dimensijų derinys yra unikalus.</span><span class="sxs-lookup"><span data-stu-id="1234b-134">To avoid this scenario, when you create **Role Price** records, the system validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="1234b-135">Jei sukūrus **Vaidmens kainos** įrašus dimensija išjungiama, šis apribojimas gali būti pažeistas.</span><span class="sxs-lookup"><span data-stu-id="1234b-135">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="1234b-136">Todėl prieš išjungiant dimensiją reikia panaikinti visas **Vaidmens kainos** ir **Vaidmens kainos antkainio** eilutes, kuriose yra ta dimensijos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="1234b-136">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]