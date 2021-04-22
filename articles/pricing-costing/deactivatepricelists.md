---
title: Kainoraščių išjungimas
description: Šioje temoje aiškinama, kaip išjungti arba pašalinti nenaudojamus ar senus kainoraščius.
author: rumant
manager: AnnBe
ms.date: 03/19/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Professional Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 3fa902e93815002be7d6915880cd7759dbbde5ef
ms.sourcegitcommit: 386921f44f1e9a8a828b140206d52945de07aee7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/22/2021
ms.locfileid: "5701954"
---
# <a name="deactivate-price-lists"></a><span data-ttu-id="7d644-103">Kainoraščių išjungimas</span><span class="sxs-lookup"><span data-stu-id="7d644-103">Deactivate price lists</span></span> 

<span data-ttu-id="7d644-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="7d644-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="7d644-105">Norėdami iš „Dynamics 365 Project Operations“ pašalinti senus arba nenaudojamus kainoraščius, turite atlikti du veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7d644-105">To remove old or unused price lists from Dynamics 365 Project Operations, there are two steps you must complete.</span></span> 

1. <span data-ttu-id="7d644-106">Pašalinkite arba panaikinkite kainoraštį iš konkretaus puslapio.</span><span class="sxs-lookup"><span data-stu-id="7d644-106">Remove or delete the price list from specific pages.</span></span>
2. <span data-ttu-id="7d644-107">Išjunkite arba panaikinkite kainoraštį iš aktyvių kainoraščių sąrašų puslapyje **Kainoraščiai**.</span><span class="sxs-lookup"><span data-stu-id="7d644-107">Deactivate or delete the price list from the Active price lists on the **Price Lists** page.</span></span>

>[!IMPORTANT]
> <span data-ttu-id="7d644-108">Norėdami visiškai pašalinti kainoraštį, turite atlikti abu veiksmus.</span><span class="sxs-lookup"><span data-stu-id="7d644-108">You must complete both steps to fully remove a price list.</span></span> <span data-ttu-id="7d644-109">Atlikti tik 2 veiksmą, kuriuo tiesiogiai panaikinamas arba išjungiamas kainoraštis rodinyje Aktyvieji kainoraščiai, nepakanka.</span><span class="sxs-lookup"><span data-stu-id="7d644-109">Only performing step 2, which is to directly delete or deactivate the price list from the Active Price Lists view, is not sufficient.</span></span> <span data-ttu-id="7d644-110">Taip pat turite panaikinti šio kainoraščio susiejimą iš visų vietų, nurodytų atliekant 1 veiksmą.</span><span class="sxs-lookup"><span data-stu-id="7d644-110">You must also delete the association of this price list from all the places mentioned in step 1.</span></span>

## <a name="delete-the-price-list-from-specific-pages"></a><span data-ttu-id="7d644-111">Panaikinkite kainoraštį iš konkrečių puslapių</span><span class="sxs-lookup"><span data-stu-id="7d644-111">Delete the price list from specific pages</span></span>
1. <span data-ttu-id="7d644-112">Norėdami panaikinti „Project Operations“ kainoraštį, eikite į toliau nurodytus puslapius.</span><span class="sxs-lookup"><span data-stu-id="7d644-112">To delete a price list from Project Operations, go to the following pages:</span></span>  

      - <span data-ttu-id="7d644-113">Puslapis **Projekto parametrai** > skirtukas **Kainoraščiai**</span><span class="sxs-lookup"><span data-stu-id="7d644-113">**Project parameters** page > **Price Lists** tab</span></span>
      - <span data-ttu-id="7d644-114">Puslapis **Organizacijos vienetas** > tinklelis **Kainoraščiai**</span><span class="sxs-lookup"><span data-stu-id="7d644-114">**Organizational Unit** page > **Price Lists** grid</span></span>
      - <span data-ttu-id="7d644-115">Puslapis **Paskyra** > tinklelis **Kainoraščiai**</span><span class="sxs-lookup"><span data-stu-id="7d644-115">**Account** page > **Project Price Lists** grid</span></span>
      - <span data-ttu-id="7d644-116">Puslapis **Projekto pasiūlymai** > tinklelis **Projekto kainoraščiai**: taikoma visiems aktyviesiems projekto pasiūlymams.</span><span class="sxs-lookup"><span data-stu-id="7d644-116">**Project Quotes** page > **Project Price Lists** grid: This applies to all active project quotes.</span></span>
      - <span data-ttu-id="7d644-117">Puslapis **Projekto sutartys** > tinklelis **Projekto kainoraščiai**: taikoma visoms aktyviosioms projekto sutartims.</span><span class="sxs-lookup"><span data-stu-id="7d644-117">**Project Contracts** page > **Project Price Lists** grid: This applies to all active project contracts.</span></span>

 2. <span data-ttu-id="7d644-118">Kiekviename puslapyje turite pasirinkti norimą panaikinti kainoraštį, tada pasirinkti **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="7d644-118">For each page, you need to select the price list that you want to delete, and then select **Delete**.</span></span> 
 
## <a name="delete-or-deactivate-the-price-list-from-the-price-lists-page"></a><span data-ttu-id="7d644-119">Panaikinkite arba įjunkite kainoraštį puslapyje Kainoraščiai</span><span class="sxs-lookup"><span data-stu-id="7d644-119">Delete or deactivate the price list from the Price Lists page</span></span>
 
1. <span data-ttu-id="7d644-120">Norėdami panaikinti kainoraštį iš aktyviųjų kainoraščių, eikite į **Pardavimas** > **Klientai** > **Kainoraščiai**.</span><span class="sxs-lookup"><span data-stu-id="7d644-120">To delete a price list from the active price lists, go to **Sales** > **Customers** > **Price Lists**.</span></span> 
2. <span data-ttu-id="7d644-121">Pasirinkite norimą panaikinti kainoraštį, tada pasirinkite **Naikinti**.</span><span class="sxs-lookup"><span data-stu-id="7d644-121">Select the price list that you want to delete and then select **Delete**.</span></span> <span data-ttu-id="7d644-122">Jei į kainoraštį nurodoma esamose operacijose, jo panaikinti negalėsite.</span><span class="sxs-lookup"><span data-stu-id="7d644-122">If the price list is referenced on any existing transactions, you won't be able to delete it.</span></span> <span data-ttu-id="7d644-123">Tokiu atveju kainoraštį galite išjungti, kad jis nebūtų rodomas rodiniuose.</span><span class="sxs-lookup"><span data-stu-id="7d644-123">If this happens, you can deactivate the price list so that it doesn't appear in any views.</span></span> 
3. <span data-ttu-id="7d644-124">Norėdami kainoraštį išjungti, kainoraštį pasirinkite dar kartą, tada pasirinkite **Išjungti**.</span><span class="sxs-lookup"><span data-stu-id="7d644-124">To deactivate the price list, select the price list again, and then select **Deactivate**.</span></span>   
