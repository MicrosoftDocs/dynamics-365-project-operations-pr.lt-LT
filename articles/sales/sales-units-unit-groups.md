---
title: Vienetai ir vienetų grupės
description: Šioje temoje pateikta informacija apie tai, kaip kurti vienetus ir vienetų grupes programoje „Dynamics 365 Project Operations“.
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
ms.openlocfilehash: ea5399368214a293ca7c10fabf21d82407b5c76f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898766"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="7d621-103">Vienetai ir vienetų grupės</span><span class="sxs-lookup"><span data-stu-id="7d621-103">Units and unit groups</span></span>

<span data-ttu-id="7d621-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="7d621-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d621-105">Vienetai yra kiekiai arba matavimo vienetai, kuriais skaičiuojami parduodami produktai arba paslaugos.</span><span class="sxs-lookup"><span data-stu-id="7d621-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="7d621-106">Pavyzdžiui, jeigu parduodate sodo prekes, sėklas galite parduoti pakelių, dėžių arba padėklų vienetais.</span><span class="sxs-lookup"><span data-stu-id="7d621-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="7d621-107">Vienetų grupė yra šių skirtingų vienetų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="7d621-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="7d621-108">Norėdami atlikti veiksmus šioje temoje, įsitikinkite, kad buvote priskirtas sistemos administratoriaus arba pardavimo specialisto vadovui arba turite atitinkamas teises.</span><span class="sxs-lookup"><span data-stu-id="7d621-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="7d621-109">Vienetų grupės kūrimas</span><span class="sxs-lookup"><span data-stu-id="7d621-109">Create a unit group</span></span>

1. <span data-ttu-id="7d621-110">Svetainės struktūroje pasirinkite **Vienetai**.</span><span class="sxs-lookup"><span data-stu-id="7d621-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="7d621-111">Pažymėkite **Naujas** ir dialogo lange **kurti vienetų grupę**įveskite vieneto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7d621-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="7d621-112">Lauke **Pirminis vienetas** įveskite mažiausią bendrąjį matavimo vienetą, pagal kurį produktas bus parduodamas.</span><span class="sxs-lookup"><span data-stu-id="7d621-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="7d621-113">Pavyzdžiui, galite įvesti „dalis“ arba „uncija“.</span><span class="sxs-lookup"><span data-stu-id="7d621-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="7d621-114">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="7d621-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="7d621-115">Vienetų įtraukimas į vienetų grupę</span><span class="sxs-lookup"><span data-stu-id="7d621-115">Add units to a unit group</span></span>

1. <span data-ttu-id="7d621-116">Atidarykite vienetų grupę ir skirtuke **Susiję** pažymėkite **Vienetai**.</span><span class="sxs-lookup"><span data-stu-id="7d621-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="7d621-117">Matysite jau įtrauktą pagrindinį vienetą.</span><span class="sxs-lookup"><span data-stu-id="7d621-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="7d621-118">Pažymėkite **Įtraukti naują vienetą** ir puslapyje **Spartusis kūrimas: vienetas**, lauke **Pavadinimas** įveskite vieneto pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="7d621-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="7d621-119">Lauke **Kiekis** įveskite kiekį, kuris sudarys vienetą.</span><span class="sxs-lookup"><span data-stu-id="7d621-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="7d621-120">Pavyzdžiui, jeigu dėžėje yra du vienetai, įveskite „2“.</span><span class="sxs-lookup"><span data-stu-id="7d621-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="7d621-121">Lauke  **Pradinis vienetas** pažymėkite pradinį vienetą žemiausiam vieneto matavimo vienetui nustatyti.</span><span class="sxs-lookup"><span data-stu-id="7d621-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="7d621-122">Pavyzdžiui, galite pažymėti „dalis“.</span><span class="sxs-lookup"><span data-stu-id="7d621-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="7d621-123">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7d621-123">Select **Save**:</span></span>
