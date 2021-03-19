---
title: Pirkimo užsakymo elementų gavimas iš elementų reikalavimo
description: Šioje temoje paaiškinama, kaip iš elementų reikalavimo gauti pirkimo užsakymo elementus.
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c2083516ff929113fd6db377acfe5aeb104666dd
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5288238"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="dd055-103">Pirkimo užsakymo elementų gavimas iš elementų reikalavimo</span><span class="sxs-lookup"><span data-stu-id="dd055-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="dd055-104">Šioje temoje paaiškinama, kaip iš elementų reikalavimo gauti pirkimo užsakymo elementus.</span><span class="sxs-lookup"><span data-stu-id="dd055-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="dd055-105">Naudodami elementų reikalavimą, o ne elementų operaciją, galite planuoti pristatymą prieš pat panaudojant elementą, sukurti pirkimo užsakymą, įtraukti elementą į prekybos sutarčių sistemą ir įtraukti elementų reikalavimą į gamybos planavimą.</span><span class="sxs-lookup"><span data-stu-id="dd055-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="dd055-106">Šiai užduočiai atlikti naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="dd055-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="dd055-107">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Projektai > Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="dd055-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="dd055-108">Sąraše pažymėkite norimos eilutės saitą.</span><span class="sxs-lookup"><span data-stu-id="dd055-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="dd055-109">Veiksmų srityje pasirinkite **Planuoti**.</span><span class="sxs-lookup"><span data-stu-id="dd055-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="dd055-110">Pažymėkite **Elementų reikalavimas**.</span><span class="sxs-lookup"><span data-stu-id="dd055-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="dd055-111">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="dd055-111">Select **New**.</span></span>
6. <span data-ttu-id="dd055-112">Naujoje eilutėje įveskite arba pasirinkite reikšmę lauke **Elemento numeris**.</span><span class="sxs-lookup"><span data-stu-id="dd055-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="dd055-113">Lauke **Kiekis** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="dd055-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="dd055-114">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="dd055-114">Select **Save**.</span></span>
9. <span data-ttu-id="dd055-115">Veiksmų srityje pasirinkite **Valdyti**.</span><span class="sxs-lookup"><span data-stu-id="dd055-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="dd055-116">Pasirinkite **Funkcijos**.</span><span class="sxs-lookup"><span data-stu-id="dd055-116">Select **Functions**.</span></span>
11. <span data-ttu-id="dd055-117">Pasirinkite **Pirkimo užsakymo kūrimas**.</span><span class="sxs-lookup"><span data-stu-id="dd055-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="dd055-118">Pažymėkite žymės langelį **Įtraukti viską**.</span><span class="sxs-lookup"><span data-stu-id="dd055-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="dd055-119">Lauke **Tiekėjo klientas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dd055-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="dd055-120">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="dd055-120">Select **OK**.</span></span>
15. <span data-ttu-id="dd055-121">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Pirkimo užsakymai > Visi pirkimo užsakymai**.</span><span class="sxs-lookup"><span data-stu-id="dd055-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="dd055-122">Sąraše pažymėkite norimos eilutės saitą.</span><span class="sxs-lookup"><span data-stu-id="dd055-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="dd055-123">Veiksmų srityje pasirinkite **Pirkti**.</span><span class="sxs-lookup"><span data-stu-id="dd055-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="dd055-124">Spustelėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="dd055-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="dd055-125">Veiksmų srityje pasirinkite **Gauti**.</span><span class="sxs-lookup"><span data-stu-id="dd055-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="dd055-126">Pažymėkite **Produktų gavimas**.</span><span class="sxs-lookup"><span data-stu-id="dd055-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="dd055-127">Lauke **Produktų gavimas** įveskite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="dd055-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="dd055-128">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="dd055-128">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]