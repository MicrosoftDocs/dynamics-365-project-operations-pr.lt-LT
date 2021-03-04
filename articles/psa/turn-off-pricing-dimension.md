---
title: Kainodaros dimensijos išjungimas
description: Šioje temoje aprašyta, kaip nustatyti kainodaros dimensijas naudojant sprendimą „Project Service“.
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: da0ac942579ba8d9b2258a011b8eeef8e64ba9c9
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147303"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="af1fa-103">Kainodaros dimensijos išjungimas</span><span class="sxs-lookup"><span data-stu-id="af1fa-103">Turn off a pricing dimension</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="af1fa-104">Kas kelerius metus gali reikėti peržiūrėti ir atnaujinti savo kainodaros strategiją.</span><span class="sxs-lookup"><span data-stu-id="af1fa-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="af1fa-105">Dėl bet kokių atliktų atnaujinimų gali reikėti išjungti esamą kainodaros dimensiją ir sukurti naują.</span><span class="sxs-lookup"><span data-stu-id="af1fa-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="af1fa-106">Pavyzdžiui, galbūt anksčiau kainą nustatėte pagal **Vaidmenį**, tačiau dabar nusprendėte kainą nustatyti pagal **Darbo patirtį**.</span><span class="sxs-lookup"><span data-stu-id="af1fa-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="af1fa-107">Tam gali reikėti išjungti **Vaidmenį** kaip kainodaros dimensiją ir sukurti **Darbo patirtį** kaip naują kainodaros dimensiją.</span><span class="sxs-lookup"><span data-stu-id="af1fa-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="af1fa-108">Kainodaros dimensiją, neatsižvelgiant į tai, ar ji yra iš anksto nustatyta, ar pasirinktinė, galima išjungti kainodaros dimensijos laukus **Taikomai savikainai** ir **Taikoma pardavimui** nustačius kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="af1fa-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="af1fa-109">Tačiau tai padarius gali būti parodytas toliau pateiktas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="af1fa-109">However, when you do this, you might receive the following error message.</span></span>

![Išjungus kainodaros dimensiją gali įvykti veiklos proceso klaida](media/Business-Process-Error.png)


<span data-ttu-id="af1fa-111">Šis klaidos pranešimas rodo, kad yra kainų įrašų, kurie prieš tai buvo nustatyti dimensijai, kuri išjungiama.</span><span class="sxs-lookup"><span data-stu-id="af1fa-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="af1fa-112">Reikia panaikinti visus dimensiją nurodančius įrašus **Vaidmens kaina** ir **Vaidmens kainos antkainis**, o tik tada dimensijos taikymą galima nustatyti kaip **Ne**.</span><span class="sxs-lookup"><span data-stu-id="af1fa-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="af1fa-113">Ši taisyklė taikoma ir iš anksto nustatytoms kainodaros dimensijoms, ir bet kurioms jūsų sukurtoms pasirinktinėms kainodaros dimensijoms.</span><span class="sxs-lookup"><span data-stu-id="af1fa-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="af1fa-114">Šio tikrinimo priežastis yra ta, kad „Project Service“ taikomas apribojimas, kad kiekvienas įrašas **Vaidmens kaina** turi turėti unikalų dimensijų derinį.</span><span class="sxs-lookup"><span data-stu-id="af1fa-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="af1fa-115">Pavyzdžiui, kainų sąraše, pavadintame **JAV išlaidų tarifai 2018**, yra šios **Vaidmens kainos** eilutės.</span><span class="sxs-lookup"><span data-stu-id="af1fa-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="af1fa-116">Standartinis pavadinimas</span><span class="sxs-lookup"><span data-stu-id="af1fa-116">Standard Title</span></span>         | <span data-ttu-id="af1fa-117">Org. vienetas</span><span class="sxs-lookup"><span data-stu-id="af1fa-117">Org Unit</span></span>    |<span data-ttu-id="af1fa-118">Vienetas</span><span class="sxs-lookup"><span data-stu-id="af1fa-118">Unit</span></span>   |<span data-ttu-id="af1fa-119">Kaina</span><span class="sxs-lookup"><span data-stu-id="af1fa-119">Price</span></span>  |<span data-ttu-id="af1fa-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="af1fa-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="af1fa-121">Sistemos inžinierius</span><span class="sxs-lookup"><span data-stu-id="af1fa-121">Systems Engineer</span></span>|<span data-ttu-id="af1fa-122">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="af1fa-122">Contoso US</span></span>|<span data-ttu-id="af1fa-123">Hour</span><span class="sxs-lookup"><span data-stu-id="af1fa-123">Hour</span></span>| <span data-ttu-id="af1fa-124">100</span><span class="sxs-lookup"><span data-stu-id="af1fa-124">100</span></span>|<span data-ttu-id="af1fa-125">USD</span><span class="sxs-lookup"><span data-stu-id="af1fa-125">USD</span></span>|
| <span data-ttu-id="af1fa-126">Vyresnysis sistemos inžinierius</span><span class="sxs-lookup"><span data-stu-id="af1fa-126">Senior Systems Engineer</span></span>|<span data-ttu-id="af1fa-127">„Danys“, JAV</span><span class="sxs-lookup"><span data-stu-id="af1fa-127">Contoso US</span></span>|<span data-ttu-id="af1fa-128">Hour</span><span class="sxs-lookup"><span data-stu-id="af1fa-128">Hour</span></span>| <span data-ttu-id="af1fa-129">150</span><span class="sxs-lookup"><span data-stu-id="af1fa-129">150</span></span>| <span data-ttu-id="af1fa-130">USD</span><span class="sxs-lookup"><span data-stu-id="af1fa-130">USD</span></span>|


<span data-ttu-id="af1fa-131">Kai **Standartinį pavadinimą** išjungsite kaip kainodaros dimensiją, o „Project Service“ kainodaros sistema ieškos kainos, iš įvesties konteksto ji naudos tik reikšmę **Org. vienetas**.</span><span class="sxs-lookup"><span data-stu-id="af1fa-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="af1fa-132">Jei įvesties konteksto **Org. vienetas** yra „Danys JAV“, rezultatas bus nedeterminuotas, nes abi eilutės sutaps.</span><span class="sxs-lookup"><span data-stu-id="af1fa-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="af1fa-133">Kad būtų išvengta tokio scenarijaus, kai kuriate įrašus **Vaidmens kaina** „Project Service“ patikrina, ar dimensijų derinys yra unikalus.</span><span class="sxs-lookup"><span data-stu-id="af1fa-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="af1fa-134">Jei sukūrus **Vaidmens kainos** įrašus dimensija išjungiama, šis apribojimas gali būti pažeistas.</span><span class="sxs-lookup"><span data-stu-id="af1fa-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="af1fa-135">Todėl prieš išjungiant dimensiją reikia panaikinti visas **Vaidmens kainos** ir **Vaidmens kainos antkainio** eilutes, kuriose yra ta dimensijos reikšmė.</span><span class="sxs-lookup"><span data-stu-id="af1fa-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

