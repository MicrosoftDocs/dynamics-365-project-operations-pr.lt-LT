---
title: Produktais pagrįstų pasiūlymo eilučių įkainojimas
description: Šioje temoje pateikta informacija apie tai, kaip taikyti savikainą produktu pagrįstai pasiūlymo eilutei.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 17b377eab5bcbc1a2327cb3ff87cc75d8de40953
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080739"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="31b28-103">Produktais pagrįstų pasiūlymo eilučių įkainojimas</span><span class="sxs-lookup"><span data-stu-id="31b28-103">Costing product-based quote lines</span></span>

<span data-ttu-id="31b28-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="31b28-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="31b28-105">„Dynamics 365 Project Operations“ produktu pagrįstose pasiūlymo eilutėse taip pat yra laukas **Savikaina**.</span><span class="sxs-lookup"><span data-stu-id="31b28-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="31b28-106">Šis laukas naudojamas, kad būtų sekama pasiūlymo eilutės produkto savikaina ir tolesnio pelningumo skaičiavimai.</span><span class="sxs-lookup"><span data-stu-id="31b28-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="31b28-107">Kai katalogo produktui sukuriama produktų pagrįsta pasiūlymo eilutė, produktu pagrįsta pasiūlymo elutė naudojama kaip numatytoji remiantis produkto katalogo lauku **Standartinė savikaina**.</span><span class="sxs-lookup"><span data-stu-id="31b28-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="31b28-108">Standartinės savikainos laukas produktų kataloge nustatomas organizacijos pagrindine valiuta.</span><span class="sxs-lookup"><span data-stu-id="31b28-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="31b28-109">Numatytoji vieneto savikaina produktu pagrįstoje pasiūlymo eilutėje konvertuojama į pardavimo valiutą pasiūlyme.</span><span class="sxs-lookup"><span data-stu-id="31b28-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="31b28-110">Vieneto savikaina produktu pagrįstoje pasiūlymo eilutėje</span><span class="sxs-lookup"><span data-stu-id="31b28-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="31b28-111">Produktu pagrįstoje pasiūlymo eilutėje turi būti vieneto savikaina, kad būtų leidžiama naudoti skirtingas kiekvieno pardavimo produkto išlaidas.</span><span class="sxs-lookup"><span data-stu-id="31b28-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="31b28-112">Tai nėra įprastas scenarijus, tačiau kartais produkto savikainą gali sumažinti tiekėjas, atsižvelgdamas į galutinio pardavimo klientą.</span><span class="sxs-lookup"><span data-stu-id="31b28-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="31b28-113">Pavyzdžiui:</span><span class="sxs-lookup"><span data-stu-id="31b28-113">For example:</span></span>

<span data-ttu-id="31b28-114">„Fabrikam Robotics“ diegia roboto rankas „Datum Corporation“ rinkinio eilutėse.</span><span class="sxs-lookup"><span data-stu-id="31b28-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="31b28-115">„Fabrikam“ teikia diegimo paslaugas, tačiau robotų rankos įsigyjamos iš „Trey Robotics“.</span><span class="sxs-lookup"><span data-stu-id="31b28-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="31b28-116">Jei roboto rankų diegimas įmonėje „Datum Corporation“ atveria naują pramonės segmentą įmonės „Trey“ robotų rankoms, už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“.</span><span class="sxs-lookup"><span data-stu-id="31b28-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="31b28-117">Tokiu atveju „Fabrikam“ sukurs produktu pagrįstą pasiūlymo eilutę, skirtą robotų rankoms, ir įves šio pasiūlymo specialią vieneto kainą.</span><span class="sxs-lookup"><span data-stu-id="31b28-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="31b28-118">Ši kaina skirsis nuo standartinės „Trey“ robotų rankų savikainos.</span><span class="sxs-lookup"><span data-stu-id="31b28-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
