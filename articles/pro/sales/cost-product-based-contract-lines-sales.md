---
title: Produktu pagrįstų sutarties eilučių įkainojimas
description: Šioje temoje pateikta informacija apie tai, kaip kurti
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081067"
---
# <a name="costing-product-based-contract-lines"></a><span data-ttu-id="001b3-103">Produktu pagrįstų sutarties eilučių įkainojimas</span><span class="sxs-lookup"><span data-stu-id="001b3-103">Costing product-based contract lines</span></span>

<span data-ttu-id="001b3-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="001b3-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="001b3-105">Produktais pagrįstos sutarties eilutės programoje „Dynamics 365 Project Operations“ apima lauką **Savikaina** , kuriame saugoma produkto savikaina tolesniems pelningumo skaičiavimams.</span><span class="sxs-lookup"><span data-stu-id="001b3-105">Product-based contract lines in Dynamics 365 Project Operations include the **Cost Price** field, which stores the cost price of the product for downstream profitability calculations.</span></span>

<span data-ttu-id="001b3-106">Kai katalogo produktui sukuriama produktais pagrįsta sutarties eilutė, produktu pagrįsta sutarties eilutė naudojama kaip numatytoji remiantis produkto katalogo lauku **Standartinė savikaina**.</span><span class="sxs-lookup"><span data-stu-id="001b3-106">When a product-based contract line is created for a catalog product, the cost of the product-based contract line defaults from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="001b3-107">Laukas **Standartinė savikaina** produktų kataloge nustatomas organizacijos pagrindine valiuta.</span><span class="sxs-lookup"><span data-stu-id="001b3-107">The **Standard Cost** field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="001b3-108">Kai sutarties eilutėje nustatoma vieneto savikaina, ji konvertuojama į sutarties pardavimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="001b3-108">When the unit cost defaults on the contract line, it's converted into the sales currency on the contract.</span></span>

## <a name="unit-cost-on-a-product-based-contract-line"></a><span data-ttu-id="001b3-109">Vieneto savikaina produktais pagrįstoje sutarties eilutėje</span><span class="sxs-lookup"><span data-stu-id="001b3-109">Unit cost on a product-based contract line</span></span>

<span data-ttu-id="001b3-110">Produktais pagrįstoje sutarties eilutėje esant vieneto savikainai, galima naudoti skirtingas kiekvieno vieneto pardavimo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="001b3-110">Having a unit cost on a product-based contract line allows for different product costs for each sale of a unit.</span></span> <span data-ttu-id="001b3-111">Nors tai ne visada būtina, yra tam tikrų atvejų, kai tiekėjas klientui gali pritaikyti produkto savikainos nuolaidą.</span><span class="sxs-lookup"><span data-stu-id="001b3-111">While not always necessary, there are certain scenarios where the cost of the product may be discounted for the customer by the supplier.</span></span> <span data-ttu-id="001b3-112">Apsvarstykite toliau pateiktą situaciją.</span><span class="sxs-lookup"><span data-stu-id="001b3-112">Consider the following scenario:</span></span>

<span data-ttu-id="001b3-113">„Fabrikam Robotics“ diegia roboto rankas „Adatum Corporation“ rinkinio eilutėse.</span><span class="sxs-lookup"><span data-stu-id="001b3-113">Fabrikam Robotics is installing robotic arms at Adatum Corporation's assembly lines.</span></span> <span data-ttu-id="001b3-114">„Fabrikam“ teikia diegimo paslaugas, tačiau robotų rankos įsigyjamos iš „Trey Research“.</span><span class="sxs-lookup"><span data-stu-id="001b3-114">Fabrikam provides installation services but the robotic arms are procured from Trey Research.</span></span> <span data-ttu-id="001b3-115">Jei roboto rankų diegimas įmonėje „ADatum Corporation“ atveria naują pramonės segmentą įmonės „Trey Research“; už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="001b3-115">If the installation of robotic arms at Adatum Corporation opens a new industry vertical for Trey Research, they could offer a special discount for this deal to Fabrikam.</span></span> <span data-ttu-id="001b3-116">Šiuo atveju „Fabrikam“ sukuria produktais pagrįstą robotų rankų sutarties eilutę ir nurodo šios sutarties vieneto savikainą, kuri skiriasi nuo standartinės robotų rankų savikainos „Trey Research“.</span><span class="sxs-lookup"><span data-stu-id="001b3-116">In this case, Fabrikam creates a product-based contract line for Robotic Arms and inputs a per unit cost for this contract that is different from the standard cost of robotic arms from Trey Research.</span></span>
