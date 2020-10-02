---
title: Pardavimų kainoraščio nustatymas
description: Šioje temoje pateikta informacija apie pardavimų kainoraščius, skirtus projektų kainodarai.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: 2a66802adfcadab7b4d34149b146ca3cb27c903e
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896471"
---
# <a name="sales-price-list-setup"></a><span data-ttu-id="ee8df-103">Pardavimų kainoraščio nustatymas</span><span class="sxs-lookup"><span data-stu-id="ee8df-103">Sales price list setup</span></span>

<span data-ttu-id="ee8df-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="ee8df-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="ee8df-105">Projekto pasiūlymams ir sutartims taikomas kitoks projekto kainoraščio kainų keitimo modelis nei produktų kainoraščiui.</span><span class="sxs-lookup"><span data-stu-id="ee8df-105">For project quotes and contracts, a project price list has a different price override pattern than a product price list.</span></span> <span data-ttu-id="ee8df-106">Produktų katalogu pagrįstoje pasiūlymo eilutėje galite pakeisti vaidmenų ir kategorijų kainas tiesiog pasiūlymo eilutėje, nes kiekviena pasiūlymo eilutė nurodo tik vieną katalogo prekę.</span><span class="sxs-lookup"><span data-stu-id="ee8df-106">On a product catalog–based quote line, you can override the price to roles and categories directly on the quote line, because each quote line points to exactly one catalog item.</span></span> <span data-ttu-id="ee8df-107">Tačiau projektu pagrįstoje pasiūlymo eilutėje negalima keisti vaidmenų ir kategorijų kainų tiesiog pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="ee8df-107">However, on a project-based quote line, you can't override the price to roles and categories directly on the quote line.</span></span> <span data-ttu-id="ee8df-108">Galite naudoti projekto kainoraštį, kad dirbtumėte su dviem skirtingais perrašymo modeliais.</span><span class="sxs-lookup"><span data-stu-id="ee8df-108">You can use the project price list to work with the two distinct override patterns.</span></span>

> [!NOTE]
> <span data-ttu-id="ee8df-109">Rekomenduojame turėti atskirą projekto išteklių kainoraštį ir katalogo prekių kainoraštį, nes keičiant kainas jie veikia skirtingai.</span><span class="sxs-lookup"><span data-stu-id="ee8df-109">We recommend that you have a separate price list for your project resources and your catalog items, because of the behavior differences between the two when you override pricing.</span></span>

<span data-ttu-id="ee8df-110">Kiekvienam iš toliau nurodytų objektų galima sudaryti vieną arba kelis susijusius projekto kainodaros pardavimo kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="ee8df-110">Each of the following entities can have one or more associated sales price lists for project pricing:</span></span>

- <span data-ttu-id="ee8df-111">Klientas (kodas)</span><span class="sxs-lookup"><span data-stu-id="ee8df-111">Customer (account)</span></span> 
- <span data-ttu-id="ee8df-112">Galimybė</span><span class="sxs-lookup"><span data-stu-id="ee8df-112">Opportunity</span></span> 
- <span data-ttu-id="ee8df-113">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="ee8df-113">Quote</span></span> 
- <span data-ttu-id="ee8df-114">Projekto sutartis</span><span class="sxs-lookup"><span data-stu-id="ee8df-114">Project Contract</span></span>

<span data-ttu-id="ee8df-115">Šių objektų susiejimą su kainoraščiu nurodo projekto kainoraščiai.</span><span class="sxs-lookup"><span data-stu-id="ee8df-115">The association of these entities with a price list is indicated by the project price lists.</span></span> <span data-ttu-id="ee8df-116">Su pardavimo objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis galite susieti vieną arba kelis kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="ee8df-116">You can associate one or more price lists with the Customer, Opportunity, Quote, and Project Contract sales entities.</span></span>

<span data-ttu-id="ee8df-117">Numatytasis projekto kainoraštis nėra automatiškai pridedamas prie kliento įrašo.</span><span class="sxs-lookup"><span data-stu-id="ee8df-117">A default project price list isn't automatically entered on a customer record.</span></span> <span data-ttu-id="ee8df-118">Tačiau projekto kainoraštį prie kliento įrašo galite pridėti patys.</span><span class="sxs-lookup"><span data-stu-id="ee8df-118">However, you can manually attach a project price list to the customer record.</span></span> <span data-ttu-id="ee8df-119">Vis dėlto projekto kainoraštį pridėti patys turėtumėte, tik jei su klientu esate sudarę pasirinktinės kainodaros sutartį.</span><span class="sxs-lookup"><span data-stu-id="ee8df-119">Nevertheless, you should manually attach a project price list only when you have a custom pricing agreement with the customer.</span></span> 

<span data-ttu-id="ee8df-120">Kai projekto kainoraštis pridedamas prie pardavimo objekto, tikrinama toliau nurodyta informacija:</span><span class="sxs-lookup"><span data-stu-id="ee8df-120">When a project price list is attached to a sales entity, the following information is validated:</span></span>

- <span data-ttu-id="ee8df-121">Kainoraščio kontekstas yra **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="ee8df-121">The price list has a context of **Sales**.</span></span> 
- <span data-ttu-id="ee8df-122">Kainoraščio valiuta atitinka kliento valiutą.</span><span class="sxs-lookup"><span data-stu-id="ee8df-122">The price list currency matches the customer currency.</span></span> 

<span data-ttu-id="ee8df-123">Automatiškai nustatant susijusius projekto kainoraščius projekto sutartyje naudojama toliau nurodytą pirmumo seka:</span><span class="sxs-lookup"><span data-stu-id="ee8df-123">On a project contract, the following order of precedence is used to automatically set related project price lists:</span></span>

1. <span data-ttu-id="ee8df-124">Pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="ee8df-124">Quote</span></span>
2. <span data-ttu-id="ee8df-125">Galimybė</span><span class="sxs-lookup"><span data-stu-id="ee8df-125">Opportunity</span></span>
3. <span data-ttu-id="ee8df-126">Klientas</span><span class="sxs-lookup"><span data-stu-id="ee8df-126">Customer</span></span> 
4. <span data-ttu-id="ee8df-127">Visuotiniai parametrai</span><span class="sxs-lookup"><span data-stu-id="ee8df-127">Global settings</span></span> 

<span data-ttu-id="ee8df-128">Kai projekto kainoraštis įvedamas pagal numatytuosius parametrus, sistema tikrina, ar valiuta atitinka kliento valiutą, ir įvestų numatytųjų kainoraščių kontekstas yra **Pardavimai**.</span><span class="sxs-lookup"><span data-stu-id="ee8df-128">When a project price list is entered by default, the system validates that the currency matches the customer’s currency, and that the default price lists that have been entered have a context of **Sales**.</span></span>

<span data-ttu-id="ee8df-129">Galite susieti kelis kainoraščius su objektais Klientas, Galimybė, Pasiūlymas ir Projekto sutartis.</span><span class="sxs-lookup"><span data-stu-id="ee8df-129">You can associate multiple project price lists with the Customer, Opportunity, Quote, and Project Contract entities.</span></span> <span data-ttu-id="ee8df-130">Jei sudarant ilgalaikių projektų sutartis jums gali prireikti daugiau nei vieno kainoraščio, siekiant įtraukti dėl infliacijos atnaujintas kainas, šis pajėgumas palaiko konkrečiai datai nustatomas kainas.</span><span class="sxs-lookup"><span data-stu-id="ee8df-130">This capability supports date-specific default prices for a long-running project contract, where you might require more than one price list to account for price updates that occur because of inflation.</span></span> <span data-ttu-id="ee8df-131">Tačiau jei su objektais Klientas, Galimybė, Pasiūlymas arba Projekto sutartis susietų kainoraščių galiojimo datos persidengia, numatytosios kainos gali būti netinkamos.</span><span class="sxs-lookup"><span data-stu-id="ee8df-131">However, if the price lists that you associate with the Customer, Opportunity, Quote, or Project Contract entity have overlapping date effectivity, the default prices might be incorrect.</span></span> <span data-ttu-id="ee8df-132">Todėl reikia užtikrinti, kad projekto kainoraščiai, kurių galiojimo datos persidengia, nebūtų susieti su šiais objektais.</span><span class="sxs-lookup"><span data-stu-id="ee8df-132">Therefore, you should make sure that project price lists that have overlapping date effectivity aren't associated with those entities.</span></span>
