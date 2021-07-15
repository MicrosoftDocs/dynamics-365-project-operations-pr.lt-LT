---
title: Projekto sąskaitų faktūrų pasiūlymų efektyvumas
description: Šioje temoje pateikiama informacija apie projekto projekto sąskaitų faktūrų pasiūlymų efektyvumo patobulinimus.
author: Yowelle
ms.date: 06/16/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 20121-03-05
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 5a14acf51d277b16896d64c4b12ee00bfb326910
ms.sourcegitcommit: 3a4b181be08ef0428104d72b54a3e61ac2782f14
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/17/2021
ms.locfileid: "6269800"
---
# <a name="project-invoice-proposal-performance"></a><span data-ttu-id="253d3-103">Projekto sąskaitų faktūrų pasiūlymų efektyvumas</span><span class="sxs-lookup"><span data-stu-id="253d3-103">Project invoice proposal performance</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="253d3-104">Kurdami naują sąskaitos faktūros pasiūlymą, dėl didėjančio projektų ir subprojektų skaičiaus galite susidurti su efektyvumo problemomis.</span><span class="sxs-lookup"><span data-stu-id="253d3-104">When you create a new invoice proposal you might encounter performance issues as the number of projects and subprojects increase.</span></span> <span data-ttu-id="253d3-105">Norint pagerinti našumą, galima pasinaudoti funkcija, leidžiančia greičiau sukurti naują užregistruotų projekto operacijų sąskaitos faktūros pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="253d3-105">To improve performance, a feature is available that reduces the time needed to create a new invoice proposal for posted project transactions.</span></span>

## <a name="enable-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="253d3-106">Projekto sąskaitų faktūrų pasiūlymo efektyvumo patobulinimo įjungimas</span><span class="sxs-lookup"><span data-stu-id="253d3-106">Enable project invoice proposal performance enhancement</span></span>
<span data-ttu-id="253d3-107">Norėdami įjungti projekto sąskaitos faktūros pasiūlymo efektyvumo patobulinimo funkciją, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="253d3-107">To enable the project invoice proposal performance enhancement feature, complete the following steps.</span></span>

1.  <span data-ttu-id="253d3-108">Eikite į **Funkcijų valdymas** > **Visos**.</span><span class="sxs-lookup"><span data-stu-id="253d3-108">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="253d3-109">Funkcijų sąraše raskite **Projekto sąskaitų faktūrų pasiūlymo efektyvumo patobulinimas**.</span><span class="sxs-lookup"><span data-stu-id="253d3-109">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="253d3-110">Pasirinkite **Įjungti dabar**.</span><span class="sxs-lookup"><span data-stu-id="253d3-110">Select **Enable now**.</span></span>
3.  <span data-ttu-id="253d3-111">Atnaujinkite naršyklės vaizdą, tada sukurkite naują sąskaitos faktūros pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="253d3-111">Refresh your browser, and then create a new invoice proposal.</span></span>

## <a name="turn-off-project-invoice-proposal-performance-enhancement"></a><span data-ttu-id="253d3-112">Projekto sąskaitų faktūrų pasiūlymo efektyvumo patobulinimo išjungimas</span><span class="sxs-lookup"><span data-stu-id="253d3-112">Turn off project invoice proposal performance enhancement</span></span>
<span data-ttu-id="253d3-113">Atlikite toliau nurodytus veiksmus ir išjunkite projekto sąskaitos faktūros pasiūlymo efektyvumo patobulinimo funkciją.</span><span class="sxs-lookup"><span data-stu-id="253d3-113">Complete the following steps to turn off the project invoice proposal performance enhancement.</span></span>

1.  <span data-ttu-id="253d3-114">Eikite į **Funkcijų valdymas** > **Visos**.</span><span class="sxs-lookup"><span data-stu-id="253d3-114">Go to **Feature management** > **All**.</span></span> <span data-ttu-id="253d3-115">Funkcijų sąraše raskite **Projekto sąskaitų faktūrų pasiūlymo efektyvumo patobulinimas**.</span><span class="sxs-lookup"><span data-stu-id="253d3-115">In the feature list, locate **Project invoice proposal performance enhancement**.</span></span>
2.  <span data-ttu-id="253d3-116">Pasirinkite **Išjungti**.</span><span class="sxs-lookup"><span data-stu-id="253d3-116">Select **Disable**.</span></span>
3.  <span data-ttu-id="253d3-117">Atnaujinkite naršyklę.</span><span class="sxs-lookup"><span data-stu-id="253d3-117">Refresh your browser.</span></span>

> [!NOTE]
> <span data-ttu-id="253d3-118">SF pasiūlymo efektyvumo negalima taikyti įjungus atsiskaitymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="253d3-118">Invoice proposal performance can't be applied when billing rules are enabled.</span></span>
> 
> <span data-ttu-id="253d3-119">Paketinio SF pasiūlymų kūrimo proceso metu pagal antrinių užduočių skaičių užduotys bus išskaidytos į maksimalų užduočių skaičių pagal sutarčių su operacijomis, kurioms išrašoma SF, skaičių, neatsižvelgiant į tai, ką įvedėte.</span><span class="sxs-lookup"><span data-stu-id="253d3-119">During the batch process to create invoice proposals, the number of subtasks will split the tasks to a maximum number based on the number of contracts with invoiceable transactions, regardless of what you have entered.</span></span> <span data-ttu-id="253d3-120">Pavyzdžiui, jei kaip antrinių užduočių skaičių paketiniu būdu kurdami SF pasiūlymus įvedate **3**, bet yra tik dvi sutartys su operacijomis, kurioms išrašoma SF, sukuriamos tik dvi antrinės užduotys.</span><span class="sxs-lookup"><span data-stu-id="253d3-120">For example, if you enter **3** for the number of subtasks for invoice proposal creation in batch, and there are only two contracts with invoiceable transactions, only two subtasks are created.</span></span>
