---
title: Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip kurti
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 001b0b54abcdd5fcd1eca7f3271cc78392f68860
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273703"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="f0568-103">Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="f0568-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="f0568-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="f0568-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="f0568-105">Į produktu pagrįstas „Dynamics 365 Project Operations“ sutarties eilutes įtraukiamas laukas **Savikaina**, kuriame saugoma produkto savikaina siekiant apskaičiuoti proceso pabaigos pelningumą.</span><span class="sxs-lookup"><span data-stu-id="f0568-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="f0568-106">Kai produktu pagrįsta sutarties eilutė sukūriama katalogo produktui, eilutės numatytoji savikaina nustatoma iš produktų katalogo lauko **Standartinė savikaina**.</span><span class="sxs-lookup"><span data-stu-id="f0568-106">When a product-based contract line is created for a catalog product, the cost of the line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="f0568-107">Laukas **Standartinė savikaina** produktų kataloge nustatomas organizacijos pagrindine valiuta.</span><span class="sxs-lookup"><span data-stu-id="f0568-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="f0568-108">Kai sutarties eilutėje nustatoma vieneto savikaina, ji konvertuojama į sutarties pardavimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="f0568-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="f0568-109">Vieneto savikaina produktais pagrįstoje sutarties eilutėje</span><span class="sxs-lookup"><span data-stu-id="f0568-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="f0568-110">Produktais pagrįstoje sutarties eilutėje esant vieneto savikainai, galima naudoti skirtingas kiekvieno vieneto pardavimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="f0568-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="f0568-111">Nors tai ne visada būtina, yra tam tikrų atvejų, kai tiekėjas klientui gali pritaikyti produkto savikainos nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="f0568-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="f0568-112">Apsvarstykite toliau pateiktą situaciją.</span><span class="sxs-lookup"><span data-stu-id="f0568-112">Consider the following scenario:</span></span>

<span data-ttu-id="f0568-113">„Fabrikam Robotics“ diegia roboto rankas „Adatum Corporation“ rinkinio eilutėse.</span><span class="sxs-lookup"><span data-stu-id="f0568-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="f0568-114">„Fabrikam“ teikia diegimo paslaugas, tačiau roboto rankos yra iš „Trey Research“.</span><span class="sxs-lookup"><span data-stu-id="f0568-114">Fabrikam provides installation services but the robotic arms are from Trey Research.</span></span> <span data-ttu-id="f0568-115">Jei roboto rankų diegimas įmonėje „ADatum Corporation“ atveria naują pramonės segmentą įmonės „Trey Research“; už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="f0568-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="f0568-116">Tokiu atveju „Fabrikam“ sukuria produktu pagrįstą sutarties eilutę, skirtą roboto rankoms.</span><span class="sxs-lookup"><span data-stu-id="f0568-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms.</span></span> <span data-ttu-id="f0568-117">Įvedama šios sutarties vieneto kaina.</span><span class="sxs-lookup"><span data-stu-id="f0568-117">A per unit cost is entered for this contract.</span></span> <span data-ttu-id="f0568-118">Savikaina skiriasi nuo roboto rankų iš „Trey Research“ savikainos.</span><span class="sxs-lookup"><span data-stu-id="f0568-118">The cost is different from the cost of robotic arms from Trey Research.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]