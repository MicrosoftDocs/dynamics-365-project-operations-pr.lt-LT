---
title: Projekto pirkimo užsakymai
description: Šiame straipsnyje aprašomi įvairūs būdai, kuriuos galite naudoti, kad sukurtumėte projekto pirkimo užsakymus. Naudojamas būdas priklauso nuo pirkimo užsakymo tikslo ir nuo to, kada nupirktos prekės yra panaudojamos ir priskirtos projektui.
author: Yowelle
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 5f3f5d196e0d7db4a6d8c4cfe834a335f4ef737c
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289199"
---
# <a name="purchase-orders-for-a-project"></a><span data-ttu-id="1b102-104">Projekto pirkimo užsakymai</span><span class="sxs-lookup"><span data-stu-id="1b102-104">Purchase orders for a project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1b102-105">Šiame straipsnyje aprašomi įvairūs būdai, kuriuos galite naudoti, kad sukurtumėte projekto pirkimo užsakymus.</span><span class="sxs-lookup"><span data-stu-id="1b102-105">This article describes the various methods that you can use to create purchase orders for a project.</span></span> <span data-ttu-id="1b102-106">Naudojamas būdas priklauso nuo pirkimo užsakymo tikslo ir nuo to, kada nupirktos prekės yra panaudojamos ir priskirtos projektui.</span><span class="sxs-lookup"><span data-stu-id="1b102-106">The method that you use depends on the purpose of the purchase order, and when the purchased items are consumed and charged to a project.</span></span>

### <a name="methods-for-creating-a-purchase-order"></a><span data-ttu-id="1b102-107">Pirkimo užsakymo kūrimo būdai</span><span class="sxs-lookup"><span data-stu-id="1b102-107">Methods for creating a purchase order</span></span>

<span data-ttu-id="1b102-108">Galite naudoti vieną iš toliau pateikiamų būdų, kad sukurtumėte pirkimo užsakymą projekto valdymo ir apskaitos srityje.</span><span class="sxs-lookup"><span data-stu-id="1b102-108">You can use one of the following methods to create a purchase order in Project management and accounting.</span></span> <span data-ttu-id="1b102-109">Pirkimo užsakymo tikslas lemia, kada pirkimo užsakymas bus panaudotas, o elementai priskirti projektui.</span><span class="sxs-lookup"><span data-stu-id="1b102-109">The purpose of the purchase order determines when the purchase order is consumed and, therefore, when items are charged to a project.</span></span>

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1b102-110">Metodas</span><span class="sxs-lookup"><span data-stu-id="1b102-110">Method</span></span></th>
<th><span data-ttu-id="1b102-111">Tikslas</span><span class="sxs-lookup"><span data-stu-id="1b102-111">Purpose</span></span></th>
<th><span data-ttu-id="1b102-112">Prekių sunaudojimas</span><span class="sxs-lookup"><span data-stu-id="1b102-112">Consumption of items</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="1b102-113">Sukurkite pirkimo užsakymą tiesiogiai projekte.</span><span class="sxs-lookup"><span data-stu-id="1b102-113">Create a purchase order directly from a project.</span></span></td>
<td><span data-ttu-id="1b102-114">Naudokite šį būdą, jei norite iš išorinio tiekėjo įsigyti prekių, kurias naudosite projekte.</span><span class="sxs-lookup"><span data-stu-id="1b102-114">Use this method to purchase items from an external vendor for consumption on a project.</span></span> <span data-ttu-id="1b102-115">Pirkimo užsakymą galite sukurti dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="1b102-115">You can create the purchase order in two ways:</span></span>
<ul>
<li><span data-ttu-id="1b102-116">Iš paties projekto.</span><span class="sxs-lookup"><span data-stu-id="1b102-116">From the project itself.</span></span> <span data-ttu-id="1b102-117">Šiuo atveju pirkimo užsakymo projektas jau yra nustatytas.</span><span class="sxs-lookup"><span data-stu-id="1b102-117">In this case, the project is already defined for the purchase order.</span></span></li>
<li><span data-ttu-id="1b102-118">Pereidami į projekto pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1b102-118">By navigating to the project purchase order.</span></span> <span data-ttu-id="1b102-119">Turite pasirinkti ir tiekėją, ir projektą, kuriems kursite pirkimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1b102-119">You must select both the vendor and the project to create the purchase order for.</span></span></li>
</ul></td>
<td><span data-ttu-id="1b102-120">Prekės yra sunaudojamos, kai atnaujinama tiekėjo SF.</span><span class="sxs-lookup"><span data-stu-id="1b102-120">Items are consumed when the vendor invoice is updated.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="1b102-121">Sukurkite pirkimo užsakymą iš pardavimo užsakymo.</span><span class="sxs-lookup"><span data-stu-id="1b102-121">Create a purchase order from a sales order.</span></span></td>
<td><span data-ttu-id="1b102-122">Naudokite šį būdą, pirkdami prekes, kai kuriate pardavimo užsakymą projekte.</span><span class="sxs-lookup"><span data-stu-id="1b102-122">Use this method to purchase items when you create a sales order from a project.</span></span></td>
<td><span data-ttu-id="1b102-123">Prekės yra sunaudojamos, kai klientui išrašoma SF už pardavimo užsakymą.</span><span class="sxs-lookup"><span data-stu-id="1b102-123">Items are consumed when the sales order is invoiced to the customer.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="1b102-124">Sukurkite pirkimo užsakymą iš prekės poreikio.</span><span class="sxs-lookup"><span data-stu-id="1b102-124">Create a purchase order from an item requirement.</span></span></td>
<td><span data-ttu-id="1b102-125">Naudokite šį būdą, pirkdami prekes, kai kuriate elemento reikalavimą projekte.</span><span class="sxs-lookup"><span data-stu-id="1b102-125">Use this method to purchase items when you create an item requirement from a project.</span></span></td>
<td><span data-ttu-id="1b102-126">Prekės ura sunaudojamos, kai atnaujinamas prekės poreikio važtaraštis.</span><span class="sxs-lookup"><span data-stu-id="1b102-126">Items are consumed when the item requirement packing slip is updated.</span></span></td>
</tr>
</tbody>
</table>

> [!NOTE] 
> <span data-ttu-id="1b102-127">Kai atnaujinsite tiekėjo sąskaitą faktūrą arba važtaraštį, būsite paraginti atnaujinti elemento reikalavimo važtaraštį.</span><span class="sxs-lookup"><span data-stu-id="1b102-127">When you update the vendor invoice or packing slip, you're prompted to update the packing slip on the item requirement.</span></span>

<span data-ttu-id="1b102-128">Norėdami gauti daugiau informacijos žr. [Pirkimo užsakymo elementų gavimas iš elementų reikalavimo](tasks/receive-items-purchase-order-item-requirement.md).</span><span class="sxs-lookup"><span data-stu-id="1b102-128">For more information, see [Receive items on purchase order from item requirement](tasks/receive-items-purchase-order-item-requirement.md).</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]