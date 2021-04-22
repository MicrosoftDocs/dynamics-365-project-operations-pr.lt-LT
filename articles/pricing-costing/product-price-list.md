---
title: Produkto kainoraščiai
description: Šioje temoje pateikta informacija apie kainoraščius katalogo kainodara, naudojama projektų pasiūlymams ir sutartims.
author: rumant
manager: AnnBe
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: e37f0bf9eef946ab4ebd658cef4e1269cbaf686d
ms.sourcegitcommit: ac90be6106592f883a0de39a75836fb40255d65a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/09/2021
ms.locfileid: "5877500"
---
# <a name="product-price-lists"></a><span data-ttu-id="fd448-103">Produkto kainoraščiai</span><span class="sxs-lookup"><span data-stu-id="fd448-103">Product price lists</span></span>

<span data-ttu-id="fd448-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="fd448-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

 <span data-ttu-id="fd448-105">„Project Operations“ **Produkto kainoraščiai** ir susiję kainoraščio objektai palaiko produktų įkainojimo funkciją produktu pagrįsto pasiūlymo ir sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="fd448-105">In Project Operations, **Product price lists** and related price list item entities support functionality for pricing products on product-based quote and contract lines.</span></span> <span data-ttu-id="fd448-106">Kai produktai naudojami projektuose, naudojami projekto kainoraščių kainų sąrašo elemento įrašai.</span><span class="sxs-lookup"><span data-stu-id="fd448-106">For products used on projects, the price list item records for project price lists are used.</span></span> 

<span data-ttu-id="fd448-107">Produktus reikia nustatyti taip, kad produktų kataloge jie turėtų numatytąją savikainą ir kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="fd448-107">Products should be set up so that they have default cost and price lists in the product catalog.</span></span> <span data-ttu-id="fd448-108">Norėdami konfigūruoti numatytąją savikainą ir kainoraščius, naudokite sąrašo kainą, standartinę kainą ir dabartinę kainą.</span><span class="sxs-lookup"><span data-stu-id="fd448-108">Use the list price, standard cost, and current cost to configure default cost and list prices.</span></span> <span data-ttu-id="fd448-109">Numatytosios sąrašo kainos naudojamos pasiūlymo eilutėje arba projekto sutarties eilutėje tik tada, kai sistema negali rasti to produkto kainoraščio eilutės produkto kainoraštyje pasiūlymui ar projekto sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="fd448-109">The default list prices are used on a quote line or a project contract line only when the system can't find a price list line for that product in the product price list for the quote or project contract.</span></span>

<span data-ttu-id="fd448-110">Produkto katalogo eilučių savikainą galima keisti tarp pasiūlymų.</span><span class="sxs-lookup"><span data-stu-id="fd448-110">The cost price of product catalog lines can be changed between quotes.</span></span> <span data-ttu-id="fd448-111">Šis pajėgumas svarbus, nes jei tiksliai neseksite savikainos, negalėsite nustatyti operacijų pelno projektų rezervavime.</span><span class="sxs-lookup"><span data-stu-id="fd448-111">This capability is important, because if you don't accurately track costs, you can't determine operational profits on project engagements.</span></span> <span data-ttu-id="fd448-112">Pagal numatytuosius nustatymus, produkto standartinė savikaina naudojama kaip savikaina.</span><span class="sxs-lookup"><span data-stu-id="fd448-112">By default, the standard cost of the product is used as the cost price.</span></span> <span data-ttu-id="fd448-113">Tačiau numatytąją savikainą galima atnaujinti pasiūlymo eilutėje, jei yra kita to pasiūlymo savikaina.</span><span class="sxs-lookup"><span data-stu-id="fd448-113">However, the default cost price can be updated on the quote line if there's a different cost price for that quote.</span></span>

## <a name="price-list-items"></a><span data-ttu-id="fd448-114">Kainų sąrašo elementai</span><span class="sxs-lookup"><span data-stu-id="fd448-114">Price list items</span></span>

<span data-ttu-id="fd448-115">Galite įtraukti produktus iš produktų katalogo į skirtingus kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="fd448-115">You can add products from a product catalog to different price lists.</span></span> <span data-ttu-id="fd448-116">Produktų kainoraščių eilutės visada nurodo konkretų vienetą.</span><span class="sxs-lookup"><span data-stu-id="fd448-116">Price list lines for products always reference a specific unit.</span></span> <span data-ttu-id="fd448-117">Produktų kainodara kainų sąrašo elementams galima sukonfigūruoti kaip valiutos sumą.</span><span class="sxs-lookup"><span data-stu-id="fd448-117">Pricing for a product on price list items can be configured as a currency amount.</span></span> <span data-ttu-id="fd448-118">Arba ją galima sukonfigūruoti kaip kainų sąrašo, dabartinės kainos arba standartinės kainos funkciją.</span><span class="sxs-lookup"><span data-stu-id="fd448-118">Alternatively, it can be configured as a function of the list price, current cost, or standard cost.</span></span>

<span data-ttu-id="fd448-119">Įkainojimo funkcija palaiko įvairias apvalinimo parinktis, kai produkto kainos konfigūruojamos kaip kainų sąrašo, standartinės kainos arba dabartinės kainos funkcija.</span><span class="sxs-lookup"><span data-stu-id="fd448-119">Pricing functionality supports various rounding options when product prices are configured as a function of the list price, standard cost, or current cost.</span></span> <span data-ttu-id="fd448-120">Be to, kad galite pasinaudoti kelių kainodaros metodų ir apvalinimo parinkčių privalumais, jūs taip pat galite susieti nuolaidų sąrašus su kainoraščio elementais.</span><span class="sxs-lookup"><span data-stu-id="fd448-120">In addition to taking advantage of multiple pricing methods and rounding options, you can associate discount lists with price list items.</span></span> 

 
## <a name="default-product-price-list"></a><span data-ttu-id="fd448-121">Numatytasis produkto kainoraštis</span><span class="sxs-lookup"><span data-stu-id="fd448-121">Default product price list</span></span>
<span data-ttu-id="fd448-122">Kiekvienas kliento įrašas turi lauką **Numatytasis kainoraštis**, kuriame galite nurodyti kainoraštį, atitinkantį kliento valiutą.</span><span class="sxs-lookup"><span data-stu-id="fd448-122">Each customer record has a **Default Price List** field, where you can specify a price list that matches the currency of the customer.</span></span> <span data-ttu-id="fd448-123">Šiame lauke numatytoji reikšmė automatiškai neįvesta.</span><span class="sxs-lookup"><span data-stu-id="fd448-123">A default value isn't automatically entered in this field.</span></span> <span data-ttu-id="fd448-124">Kai egzistuoja pasirinktinės kainodaros sutartis su konkrečiu klientu, galite naudoti šį lauką, kad susietumėte kainoraštį su tuo klientu.</span><span class="sxs-lookup"><span data-stu-id="fd448-124">When a custom pricing agreement with a specific customer exists, you can use this field to associate a price list with that customer.</span></span>

<span data-ttu-id="fd448-125">Galimybės, pasiūlymo ir projekto sutarties objektai naudoja toliau pateikiamą tvarką, kad būtų įvesti numatytieji produktų kainoraščiai.</span><span class="sxs-lookup"><span data-stu-id="fd448-125">The Opportunity, Quote, and Project Contract entities use the following order to enter default product price lists.</span></span> <span data-ttu-id="fd448-126">Tas pats užsakymas naudojamas projektų kainoraščiams.</span><span class="sxs-lookup"><span data-stu-id="fd448-126">The same order is used for project price lists.</span></span>

1.  <span data-ttu-id="fd448-127">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="fd448-127">Quote</span></span>
2.  <span data-ttu-id="fd448-128">Galimybė</span><span class="sxs-lookup"><span data-stu-id="fd448-128">Opportunity</span></span>
3.  <span data-ttu-id="fd448-129">Klientas</span><span class="sxs-lookup"><span data-stu-id="fd448-129">Customer</span></span>
4.  <span data-ttu-id="fd448-130">Visuotiniai parametrai</span><span class="sxs-lookup"><span data-stu-id="fd448-130">Global settings</span></span> 

<span data-ttu-id="fd448-131">Pagal numatytuosius nustatymus, pasiūlymo eilutėje esančiame lauke **Produktas** pateikiamas visų aktyviųjų produktų, esančių pasiūlymo produkto kainoraštyje, sąrašas.</span><span class="sxs-lookup"><span data-stu-id="fd448-131">By default, the **Product** field on the quote line lists all the active products in the product price list of the quote.</span></span> <span data-ttu-id="fd448-132">Jei produktas nebuvo suaktyvintas arba jei tai yra juodraštinis produktas, jis nepateikiamas sąraše, net jei jis yra kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="fd448-132">If a product has been inactivated, or if it's a draft product, it isn't listed, even if it's in the price list.</span></span> 

<span data-ttu-id="fd448-133">Produktų katalogo eilutės įtraukiamos kaip sąskaitos faktūros eilutės pirmoje sąskaitoje faktūroje, sukurtoje projekto sutarčiai.</span><span class="sxs-lookup"><span data-stu-id="fd448-133">Product catalog lines are added as invoice lines on the first invoice that is created for a project contract.</span></span> <span data-ttu-id="fd448-134">Juodraštinėje sąskaitoje faktūroje šias sąskaitų faktūrų eilutes galima panaikinti.</span><span class="sxs-lookup"><span data-stu-id="fd448-134">On a draft invoice, those invoice lines can be deleted.</span></span> <span data-ttu-id="fd448-135">Tokiu atveju eilutės bus rodomos kitoje sąskaitoje faktūroje tol, kol joms nebus išrašyta sąskaita faktūra, arba kol sąskaita faktūra nebus išsiųsta klientui.</span><span class="sxs-lookup"><span data-stu-id="fd448-135">In that case, the lines will appear on a subsequent invoice until they are invoiced, or until the invoice is sent to the customer.</span></span> <span data-ttu-id="fd448-136">Negalite sukurti sąskaitos faktūros daliniui produkto sąskaitos faktūros eilutės kiekiui.</span><span class="sxs-lookup"><span data-stu-id="fd448-136">You can't invoice a partial quantity of a product invoice line.</span></span> <span data-ttu-id="fd448-137">Kai projekto sutarties produktų eilutėms išrašoma sąskaita faktūra, sukuriami faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="fd448-137">When the product lines from the project contract are invoiced, actuals are created.</span></span> <span data-ttu-id="fd448-138">Tačiau šie faktiniai duomenys nesusieti su susijusio projekto objektu.</span><span class="sxs-lookup"><span data-stu-id="fd448-138">However, those actuals aren't linked to the related project entity.</span></span> <span data-ttu-id="fd448-139">Kitaip tariant, produktu pagrįsto projekto sutarties eilutės nepriklauso nuo jokio projektu pagrįsto naudojimo.</span><span class="sxs-lookup"><span data-stu-id="fd448-139">In other words, product-based project contract lines are independent of any project-based use.</span></span> 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
