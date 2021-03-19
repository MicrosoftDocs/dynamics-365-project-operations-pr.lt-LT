---
title: Išteklių įvertinimai
description: Šioje temoje pateikta informacija apie tai, kaip „Project Operations“ nustatomi išteklių įvertinimai.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 98a61746f172b50bf6fa29cb0d21462cd616f417
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286528"
---
# <a name="resource-estimates"></a><span data-ttu-id="9dc92-103">Išteklių įvertinimai</span><span class="sxs-lookup"><span data-stu-id="9dc92-103">Resource estimates</span></span>

<span data-ttu-id="9dc92-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="9dc92-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9dc92-105">Išteklių įvertinimai pateikiami remiantis laikotarpių pastangomis, apibrėžtomis darbo paskirstymo struktūroje, ir atitinkamomis kainų dimensijomis.</span><span class="sxs-lookup"><span data-stu-id="9dc92-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="9dc92-106">Paprastai skaičiuojama pagal tokią formulę: **kiekvieno vaidmens valandinis įkainis x val.**</span><span class="sxs-lookup"><span data-stu-id="9dc92-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="9dc92-107">Kiekvienos ištekliaus laikotarpio pastangų duomenys įrašomi ištekliaus priskyrimo įraše.</span><span class="sxs-lookup"><span data-stu-id="9dc92-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="9dc92-108">Kainų duomenys laikomi iš anksto apibrėžtame kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="9dc92-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="9dc92-109">Vienetų konvertavimas atliekamas pagal taikomą kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="9dc92-109">Unit conversion is applied based on the applicable price list.</span></span>

![Išteklių įvertinimai](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="9dc92-111">Numatytoji savikainos ir sąnaudų valiuta</span><span class="sxs-lookup"><span data-stu-id="9dc92-111">Default cost price and cost currency</span></span>

<span data-ttu-id="9dc92-112">Numatytosios savikainos reikšmės pateikiamos remiantis organizaciniu vienetu.</span><span class="sxs-lookup"><span data-stu-id="9dc92-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="9dc92-113">Numatytasis sąskaitų tarifas ir pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="9dc92-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="9dc92-114">Pardavimo kainos taikomos vieną kartą sandoriui.</span><span class="sxs-lookup"><span data-stu-id="9dc92-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="9dc92-115">Numatytojo pardavimo kainoraščio sąrašo hierarchija:</span><span class="sxs-lookup"><span data-stu-id="9dc92-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="9dc92-116">Organizacija</span><span class="sxs-lookup"><span data-stu-id="9dc92-116">Organization</span></span>
2. <span data-ttu-id="9dc92-117">Klientas</span><span class="sxs-lookup"><span data-stu-id="9dc92-117">Customer</span></span>
3. <span data-ttu-id="9dc92-118">Pasiūlymas / sutartis</span><span class="sxs-lookup"><span data-stu-id="9dc92-118">Quote/contract</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]