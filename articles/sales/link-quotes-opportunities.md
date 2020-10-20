---
title: Projektų pasiūlymų kūrimas iš galimybių
description: Šioje temoje pateikta informacija apie projekto pasiūlymo kūrimą iš galimybės.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 606098473db479d0015e3a7a3c01a3d3b6de9db1
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898542"
---
# <a name="create-project-quotes-from-opportunities"></a><span data-ttu-id="77f6c-103">Projektų pasiūlymų kūrimas iš galimybių</span><span class="sxs-lookup"><span data-stu-id="77f6c-103">Create project quotes from opportunities</span></span>

<span data-ttu-id="77f6c-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="77f6c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="77f6c-105">Pasiūlymus galima kurti naudojant projekto galimybes šiais būdais:</span><span class="sxs-lookup"><span data-stu-id="77f6c-105">Quotes can be created from project opportunities in the following ways:</span></span>

- <span data-ttu-id="77f6c-106">Skirtuke **Pasiūlymai**, esančiame puslapyje **Projekto galimybė**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-106">From the **Quotes** tab on the **Project Opportunity** page</span></span>
- <span data-ttu-id="77f6c-107">Iš galimybės pardavimų proceso srauto</span><span class="sxs-lookup"><span data-stu-id="77f6c-107">From the Opportunity sales process flow</span></span>
- <span data-ttu-id="77f6c-108">Atnaujinant galimybės nuorodą esamame pasiūlyme</span><span class="sxs-lookup"><span data-stu-id="77f6c-108">By updating the opportunity reference on an existing quote</span></span>

## <a name="from-the-quotes-tab-of-the-project-opportunity-page"></a><span data-ttu-id="77f6c-109">Skirtuke „Pasiūlymai“, esančiame puslapyje „Projekto galimybė“.</span><span class="sxs-lookup"><span data-stu-id="77f6c-109">From the Quotes tab of the Project Opportunity page</span></span>

<span data-ttu-id="77f6c-110">Norėdami sukurti projekto pasiūlymą iš galimybės, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="77f6c-110">To create a project quote from an opportunity, complete the following steps.</span></span>

1. <span data-ttu-id="77f6c-111">Atidarykite puslapį **Projekto pasiūlymai** ir pasirinkite skirtuką **Pasiūlyma**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-111">Open the **Project Opportunity** page and select the **Quotes** tab.</span></span> 
2. <span data-ttu-id="77f6c-112">Papildomame tinklelyje **Pasiūlymai** pasirinkite **+**, kad sukurtumėte naują projekto pasiūlymą pagal galimybę.</span><span class="sxs-lookup"><span data-stu-id="77f6c-112">On the **Quotes** sub-grid, select the **+** to create a new project quote based on the opportunity.</span></span> <span data-ttu-id="77f6c-113">Visos galimybių eilutės ir susiję projektų kainoraščiai kopijuojami į naują pasiūlymą iš galimybės.</span><span class="sxs-lookup"><span data-stu-id="77f6c-113">All of the opportunity lines and related Project price lists are copied to the new quote from the opportunity.</span></span>

## <a name="from-the-opportunity-sales-process-flow"></a><span data-ttu-id="77f6c-114">Iš galimybės pardavimų proceso srauto</span><span class="sxs-lookup"><span data-stu-id="77f6c-114">From the Opportunity sales process flow</span></span>

<span data-ttu-id="77f6c-115">Norėdami sukurti pasiūlymą iš galimybės pardavimų proceso srauto, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="77f6c-115">To create a quote from the Opportunity sales process flow, complete the following steps.</span></span>

1. <span data-ttu-id="77f6c-116">Iš galimybių pardavimo proceso srauto atidarykite galimybę.</span><span class="sxs-lookup"><span data-stu-id="77f6c-116">From the Opportunity sales process flow, open the Opportunity.</span></span>
2. <span data-ttu-id="77f6c-117">Pasirinkite etapą **Patvirtinti tinkamumą**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-117">Select the **Qualify** stage.</span></span> 
3. <span data-ttu-id="77f6c-118">Pažymėkite **Kitas**, o tada pažymėkite **+ Kurti**, kad sukurtumėte naują pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="77f6c-118">Select **Next** and then select **+ Create** to create a new quote.</span></span> <span data-ttu-id="77f6c-119">Dauguma šio naujo pasiūlymo informacijos, pateiktos skirtuke **Suvestinė**, bus nustatyta iš galimybės pagal numatytuosius nustatymus.</span><span class="sxs-lookup"><span data-stu-id="77f6c-119">Most of the information on the **Summary** tab for this new quote will have defaulted from the opportunity.</span></span> 
4. <span data-ttu-id="77f6c-120">Įveskite būtiną trūkstamą informaciją arba atnaujinkite numatytąsias reikšmes skirtuke **Suvestinė**,</span><span class="sxs-lookup"><span data-stu-id="77f6c-120">Enter in any required information that is missing, or update defaulted values as necessary on the **Summary** tab,</span></span>
5. <span data-ttu-id="77f6c-121">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-121">Select **Save**.</span></span> <span data-ttu-id="77f6c-122">Naujas pasiūlymas sukuriamas ir susiejamas su galimybe.</span><span class="sxs-lookup"><span data-stu-id="77f6c-122">The new quote is created and associated to the opportunity.</span></span> <span data-ttu-id="77f6c-123">Dabar galite peržiūrėti pasiūlymo informaciją skirtuke **Pasiūlymai** puslapyje **Galimybė**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-123">You can now view the quote information on the **Quotes** tab of the **Opportunity** page.</span></span> 

   <span data-ttu-id="77f6c-124">Galimybės pardavimo procesas pereina į kitą etapą – **Siūlyti**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-124">The Opportunity sales process moves to the next stage, **Propose**.</span></span>


## <a name="by-updating-the-opportunity-reference-on-an-existing-quote"></a><span data-ttu-id="77f6c-125">Atnaujinant galimybės nuorodą esamame pasiūlyme</span><span class="sxs-lookup"><span data-stu-id="77f6c-125">By updating the opportunity reference on an existing quote</span></span>

<span data-ttu-id="77f6c-126">Esamas pasiūlymas gali būti susietas su galimybe.</span><span class="sxs-lookup"><span data-stu-id="77f6c-126">An existing quote can be linked to an Opportunity.</span></span> <span data-ttu-id="77f6c-127">Atlikite šiuos veiksmus ir atnaujinkite galimybės informaciją esamame pasiūlyme.</span><span class="sxs-lookup"><span data-stu-id="77f6c-127">Complete the following steps to update the Opportunity information on an existing quote.</span></span>

1. <span data-ttu-id="77f6c-128">Atidarykite puslapį **Pasiūlymas** ir pasirinkite skirtuką **Suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-128">Open the **Quote** page and select the **Summary** tab.</span></span>
2. <span data-ttu-id="77f6c-129">Lauke **Galimybė** pasirinkite galimybę, kurią norite susieti su pasiūlymu.</span><span class="sxs-lookup"><span data-stu-id="77f6c-129">In the **Opportunity** field, select the opportunity that you want to link to the quote.</span></span> <span data-ttu-id="77f6c-130">Pasiūlymą galite peržiūrėti galimybių tinklelyje **Pasiūlymai**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-130">You can see the quote in the **Quotes** grid of the Opportunity.</span></span> 
3. <span data-ttu-id="77f6c-131">Naudojant galimybių pardavimų procesą galimybę galima perkelti į kitą etapą – **Siūlyti**.</span><span class="sxs-lookup"><span data-stu-id="77f6c-131">Using the Opportunity sales process, the opportunity can be moved to the next stage, **Propose**.</span></span> 

   <span data-ttu-id="77f6c-132">Kai perkeliate galimybę į šį etapą, galite pažymėti šį pasiūlymą iš pasiūlymų, susijusių su šia galimybe, sąrašo.</span><span class="sxs-lookup"><span data-stu-id="77f6c-132">When you move an opportunity to this stage, you can select this quote from a list of quotes associated with this opportunity.</span></span> <span data-ttu-id="77f6c-133">Pažymėjus šį pasiūlymą nurodoma, kad su juo keliaujate pirmyn.</span><span class="sxs-lookup"><span data-stu-id="77f6c-133">Selecting this quote indicates that you're moving forward with it.</span></span>

   <span data-ttu-id="77f6c-134">Visi kiti su galimybe susieti pasiūlymai vis tiek bus pasiekiami ir būs aktyvūs tol, kol laimėsite vieną iš jų.</span><span class="sxs-lookup"><span data-stu-id="77f6c-134">All the other quotes associated with the Opportunity will still be available and active until one of them is won.</span></span> <span data-ttu-id="77f6c-135">Galite perkelti pardavimo procesą atgal į ankstesnį etapą – **Patvirtinti tinkamumą** – ir pasirinkti kitą pasiūlymą ir pereiti į priekį.</span><span class="sxs-lookup"><span data-stu-id="77f6c-135">You can move the sales process back to the previous stage **Qualify**, and pick another quote to move forward with.</span></span>
