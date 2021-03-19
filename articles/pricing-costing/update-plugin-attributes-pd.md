---
title: Priedo atributų atnaujinimas siekiant įtraukti naujas kainodaros dimensijas
description: Šioje temoje pateikta informacijos, kaip atnaujinti priedo atributus, kad būtų galima naudoti kainodaros dimensijas.
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7999c003a0cf670d586ebf4445901e106fbee39f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274693"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="00dd6-103">Priedo atributų atnaujinimas siekiant įtraukti naujas kainodaros dimensijas</span><span class="sxs-lookup"><span data-stu-id="00dd6-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="00dd6-104">Šioje temoje pateikta informacijos, kaip atnaujinti priedo atributus, kad būtų galima naudoti kainodaros dimensijas.</span><span class="sxs-lookup"><span data-stu-id="00dd6-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="00dd6-105">Ši tema taikoma tik „Dynamics 365 Project Operations“ pasiūlymo ir sutarties funkcijoms.</span><span class="sxs-lookup"><span data-stu-id="00dd6-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="00dd6-106">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="00dd6-106">Prerequisites</span></span>
<span data-ttu-id="00dd6-107">Kad galėtumėte atlikti šioje temoje nurodytus veiksmus, pirmiau turite būti užbaigę toliau nurodytose temose aprašytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="00dd6-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="00dd6-108">Pasirinktinių laukų ir objektų kūrimas</span><span class="sxs-lookup"><span data-stu-id="00dd6-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="00dd6-109">Pasirinktinių laukų įtraukimas į kainų sąranką ir operacijų objektus </span><span class="sxs-lookup"><span data-stu-id="00dd6-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="00dd6-110">[Pasirinktinių laukų kaip kainodaros dimensijų nustatymas](set-up-custom-fields-pricing-dimensions.md).</span><span class="sxs-lookup"><span data-stu-id="00dd6-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="00dd6-111">Jei neatlikote šių procedūrų, atlikite jas ir tada grįžkite į šią temą.</span><span class="sxs-lookup"><span data-stu-id="00dd6-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="00dd6-112">Priedo užregistravimas</span><span class="sxs-lookup"><span data-stu-id="00dd6-112">Register a plug-in</span></span>
<span data-ttu-id="00dd6-113">Kai puslapyje **Pasiūlymo eilutė** sukuriama projekto pasiūlymo eilutei skirta pasiūlymo eilutės informacija, sistema sukuria dvi įvertinimo eilutes.</span><span class="sxs-lookup"><span data-stu-id="00dd6-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="00dd6-114">Viena įvertinimo eilutė skirta sąnaudoms, o kita eilutė – pardavimui.</span><span class="sxs-lookup"><span data-stu-id="00dd6-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="00dd6-115">Tas pats taikoma projekto sutarties eilutėms.</span><span class="sxs-lookup"><span data-stu-id="00dd6-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="00dd6-116">Kai sąnaudų dalyje keičiate kiekį arba lauką, šis pakeitimas taip pat perkeliamas į pardavimo dalį.</span><span class="sxs-lookup"><span data-stu-id="00dd6-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="00dd6-117">Tai įmanoma padaryti, nes priedas PreOperation, esantis Quotelinedetail ir Contractlinedetail objektuose, susieja konkrečius operacijos sąnaudų atributus su pardavimo atributais.</span><span class="sxs-lookup"><span data-stu-id="00dd6-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="00dd6-118">Jei norite, kad pardavimo dalyje atlikti kainodaros dimensijų verčių pakeitimai būtų atlikti ir sąnaudų dalyje, pakeitus kainodaros dimensiją reikia iš naujo užregistruoti toliau nurodytus priedus.</span><span class="sxs-lookup"><span data-stu-id="00dd6-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="00dd6-119">Toliau pateikiami priedai, kuriuos reikia atnaujinti ir iš naujo užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="00dd6-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="00dd6-120">PreOperationContractLineDetailUpdate – **msdyn_orderlinetransaction naujinimas**</span><span class="sxs-lookup"><span data-stu-id="00dd6-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="00dd6-121">PreOperationQuoteLineDetailUpdate – **msdyn_quotelinetransaction naujinimas**</span><span class="sxs-lookup"><span data-stu-id="00dd6-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="00dd6-122">Norėdami atnaujinti ir iš naujo užregistruoti priedus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="00dd6-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="00dd6-123">Atidarykite **PluginRegistrationTool** ir prijunkite prie savo „Project Operations Dataverse“ aplinkos.</span><span class="sxs-lookup"><span data-stu-id="00dd6-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="00dd6-124">Pasirinkite **Ieškoti** ir įveskite kelias pirmąsias priedo, kurį reikia atnaujinti, pavadinimo raides.</span><span class="sxs-lookup"><span data-stu-id="00dd6-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="00dd6-125">Radę priedą, pasirinkite jį ir spustelėkite **Pasirinkti pagrindinėje formoje**.</span><span class="sxs-lookup"><span data-stu-id="00dd6-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="00dd6-126">Pasirinkite veiksmą **msdyn_orderlinetransaction naujinimas**, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="00dd6-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="00dd6-127">Dialogo lange **Atnaujinimas** filtravimo atributų dalyje pasirinkite daugtaškį (**...**).</span><span class="sxs-lookup"><span data-stu-id="00dd6-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="00dd6-128">Atidaromas filtravimo atributų langas ir pateikiamas visų objekto ir kainodaros dimensijų atributų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="00dd6-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="00dd6-129">Pažymėkite kainodaros dimensijų atributų žymės langelius.</span><span class="sxs-lookup"><span data-stu-id="00dd6-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="00dd6-130">Pasirinkite **Gerai**, kad uždarytumėte puslapį, tada pasirinkite **Atnaujinti veiksmą**.</span><span class="sxs-lookup"><span data-stu-id="00dd6-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="00dd6-131">Pakartokite 2–7 veiksmus ir su antru priedu **PreOperationQuoteLineDetail**.</span><span class="sxs-lookup"><span data-stu-id="00dd6-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="00dd6-132">Pasirinkus šį priedą reikia atnaujinti veiksmą **msdyn_quotelinetransaction naujinimas**.</span><span class="sxs-lookup"><span data-stu-id="00dd6-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="00dd6-133">Uždarykite **PluginRegistrationTool**.</span><span class="sxs-lookup"><span data-stu-id="00dd6-133">Close **PluginRegistrationTool**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]