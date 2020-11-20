---
title: Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip kurti
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177251"
---
# <a name="cost-product-based-contract-lines---lite"></a><span data-ttu-id="53b0f-103">Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="53b0f-103">Cost product-based contract lines - lite</span></span>

<span data-ttu-id="53b0f-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="53b0f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="53b0f-105">Produktais pagrįstos sutarties eilutės programoje „Dynamics 365 Project Operations“ apima lauką **Savikaina**, kuriame saugoma produkto savikaina tolesniems pelningumo skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="53b0f-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="53b0f-106">Kai katalogo produktui sukuriama produktais pagrįsta sutarties eilutė, produktu pagrįsta sutarties eilutė naudojama kaip numatytoji remiantis produkto katalogo lauku **Standartinė savikaina**.</span><span class="sxs-lookup"><span data-stu-id="53b0f-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="53b0f-107">Laukas **Standartinė savikaina** produktų kataloge nustatomas organizacijos pagrindine valiuta.</span><span class="sxs-lookup"><span data-stu-id="53b0f-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="53b0f-108">Kai sutarties eilutėje nustatoma vieneto savikaina, ji konvertuojama į sutarties pardavimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="53b0f-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="53b0f-109">Vieneto savikaina produktais pagrįstoje sutarties eilutėje</span><span class="sxs-lookup"><span data-stu-id="53b0f-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="53b0f-110">Produktais pagrįstoje sutarties eilutėje esant vieneto savikainai, galima naudoti skirtingas kiekvieno vieneto pardavimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="53b0f-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="53b0f-111">Nors tai ne visada būtina, yra tam tikrų atvejų, kai tiekėjas klientui gali pritaikyti produkto savikainos nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="53b0f-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="53b0f-112">Apsvarstykite toliau pateiktą situaciją.</span><span class="sxs-lookup"><span data-stu-id="53b0f-112">Consider the following scenario:</span></span>

<span data-ttu-id="53b0f-113">„Fabrikam Robotics“ diegia roboto rankas „Adatum Corporation“ rinkinio eilutėse.</span><span class="sxs-lookup"><span data-stu-id="53b0f-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="53b0f-114">„Fabrikam“ teikia diegimo paslaugas, tačiau robotų rankos įsigyjamos iš „Trey Research“.</span><span class="sxs-lookup"><span data-stu-id="53b0f-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="53b0f-115">Jei roboto rankų diegimas įmonėje „ADatum Corporation“ atveria naują pramonės segmentą įmonės „Trey Research“; už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="53b0f-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="53b0f-116">Šiuo atveju „Fabrikam“ sukuria produktais pagrįstą robotų rankų sutarties eilutę ir nurodo šios sutarties vieneto savikainą, kuri skiriasi nuo standartinės robotų rankų savikainos „Trey Research“.</span><span class="sxs-lookup"><span data-stu-id="53b0f-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
