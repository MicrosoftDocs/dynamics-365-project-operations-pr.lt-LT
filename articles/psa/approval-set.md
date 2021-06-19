---
title: Patvirtinimo rinkiniai
description: Šioje temoje pateikiama informacija apie patvirtinimo rinkinį, užklausas ir šių operacijų antrinius rinkinius.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116881"
---
# <a name="approval-sets"></a><span data-ttu-id="cd140-103">Patvirtinimo rinkiniai</span><span class="sxs-lookup"><span data-stu-id="cd140-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="cd140-104">Patvirtinimo grupės patvirtinimo užklausos nustatomos pagal mažesnius operacijų antrinius rinkinius.</span><span class="sxs-lookup"><span data-stu-id="cd140-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="cd140-105">Šis grupavimas leidžia apdoroti patvirtinimus pagal projektą ir leidžia pakartotinai bandyti bei nustatyti eiliškumą.</span><span class="sxs-lookup"><span data-stu-id="cd140-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="cd140-106">Grupavimas pagerina didžiulių patvirtinimo kiekių patvirtinimo proceso patikimumą ir atsekamumą.</span><span class="sxs-lookup"><span data-stu-id="cd140-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="cd140-107">Patvirtinimo rinkiniuose nurodoma bendra su jais susijusių įrašų apdorojimo būsena.</span><span class="sxs-lookup"><span data-stu-id="cd140-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="cd140-108">Kai patvirtinimo įrašas apdorojamas naudojant patvirtinimo rinkinį, įrašas perkeliamas iš **Pateikta** į **Patvirtinta** ir atsiejamas nuo patvirtinimo rinkinio.</span><span class="sxs-lookup"><span data-stu-id="cd140-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="cd140-109">Jei pateikti patvirtinti įrašą nepavyksta, įrašo būsena lieka **Pateikta**, o rinkinys pažymimas kaip nepavykęs.</span><span class="sxs-lookup"><span data-stu-id="cd140-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="cd140-110">Patvirtinimo rinkinys registruoja klaidos pranešimą apie triktį.</span><span class="sxs-lookup"><span data-stu-id="cd140-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="cd140-111">Patvirtinimų ir patvirtinimo rinkinių apdorojimas</span><span class="sxs-lookup"><span data-stu-id="cd140-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="cd140-112">Į eilę įtraukti apdorojimo patvirtinimai matomi rodinyje **Apdorojimo patvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="cd140-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="cd140-113">Sistema bando apdoroti visus įrašus kelis kartus asinchroniškai, įskaitant pakartotinius bandymus patvirtinti, jei ankstesni bandymų nepavyko.</span><span class="sxs-lookup"><span data-stu-id="cd140-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="cd140-114">Lauke **Patvirtinimo rinkinio galiojimo laikas** įrašomas bandymų apdoroti rinkinį skaičius, tik tada pažymimas kaip nepavykęs.</span><span class="sxs-lookup"><span data-stu-id="cd140-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="cd140-115">Patvirtinimų ir patvirtinimo rinkinių pažymėjimas kaip nepavykusių</span><span class="sxs-lookup"><span data-stu-id="cd140-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="cd140-116">Rodinyje **Nepavykę patvirtinimai** išvardyti visi patvirtinimai, kuriems reikia vartotojo įsikišimo.</span><span class="sxs-lookup"><span data-stu-id="cd140-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="cd140-117">Atidarykite susijusių patvirtinimo rinkinių žurnalus, kad būtų galima nustatyti nesėkmės priežastį.</span><span class="sxs-lookup"><span data-stu-id="cd140-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="cd140-118">Jei pažymėsite **Bandyti dar kartą**, bus pridedamas patvirtinimo rinkinio laiko skaičiavimas, patvirtinimo rinkinys vėl nustatomas į būseną **Apdorojama** ir bandoma apdoroti likusius įrašus.</span><span class="sxs-lookup"><span data-stu-id="cd140-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="cd140-119">Patvirtinimo rinkinių konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cd140-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="cd140-120">Įjungti patvirtinimo rinkinių funkciją</span><span class="sxs-lookup"><span data-stu-id="cd140-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="cd140-121">Prieš įjungdami patvirtinimo rinkinių funkciją patikrinkite, ar šiuo metu nėra apdorojamų patvirtinimų.</span><span class="sxs-lookup"><span data-stu-id="cd140-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="cd140-122">Eikite į puslapį **Projekto parametrai** ir pasirinkite **Funkcijų valdymas** > **Įjungti modernius patvirtinimus**.</span><span class="sxs-lookup"><span data-stu-id="cd140-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="cd140-123">Išjungti patvirtinimo rinkinių funkciją</span><span class="sxs-lookup"><span data-stu-id="cd140-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="cd140-124">Prieš išjungdami patvirtinimo rinkinių funkciją patikrinkite, ar šiuo metu nėra apdorojamų patvirtinimų.</span><span class="sxs-lookup"><span data-stu-id="cd140-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="cd140-125">Eikite į puslapį **Projekto parametrai** ir pasirinkite **Funkcijų valdymas** > **Išjungti modernius patvirtinimus**.</span><span class="sxs-lookup"><span data-stu-id="cd140-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="cd140-126">Asinchroninės ribinės vertės konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="cd140-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="cd140-127">Kai sukuriami patvirtinimo rinkiniai, apdorojimas pereina į foną, kai pažymėtas patvirtinti įrašų skaičius viršija nurodytą ribinę vertę.</span><span class="sxs-lookup"><span data-stu-id="cd140-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="cd140-128">Naudokite lauką **Asinchroninė ribinė reikšmė** ir konfigūruokite, kada patvirtinimo apdorojimas turėtų būti vykdomas sinchroniškai arba asinchroniškai.</span><span class="sxs-lookup"><span data-stu-id="cd140-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="cd140-129">Tinkamos vertės:</span><span class="sxs-lookup"><span data-stu-id="cd140-129">Valid values are:</span></span>

  - <span data-ttu-id="cd140-130">Nulinė: visos užklausos turi būti apdorojamos asinchroniškai.</span><span class="sxs-lookup"><span data-stu-id="cd140-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="cd140-131">Skaičiai, didesni nei nulis: patvirtinimai asinchroniškai apdorojami tik tada, kai pateiktas patvirtinimų skaičius viršija šią reikšmę.</span><span class="sxs-lookup"><span data-stu-id="cd140-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
