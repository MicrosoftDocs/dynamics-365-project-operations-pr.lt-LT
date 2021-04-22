---
title: Priedo atributų atnaujinimas norint įtraukti naujų kainodaros dimensijų
description: Šioje temoje pateikta informacija apie kainodaros dimensijų priedo atributų atnaujinimą.
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: project-operations
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 958646c9e06a15e265bc0caa8b0f3eb9f79fc347
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5281803"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="79e0d-103">Priedo atributų atnaujinimas norint įtraukti naujų kainodaros dimensijų</span><span class="sxs-lookup"><span data-stu-id="79e0d-103">Update plug-in attributes to include new pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!NOTE]
> <span data-ttu-id="79e0d-104">Jei nenaudojate „Project Service Automation“ (PSA) pasiūlymo teikimo ir sutarties sudarymo funkcijų, galite praleisti šią temą.</span><span class="sxs-lookup"><span data-stu-id="79e0d-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="79e0d-105">Šioje temoje daroma prielaida, kad atlikote temose [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities.md), [Pasirinktinių laukų įtraukimas į kainos sąranką ir operacijų objektus](field-references.md) bei [Pasirinktinių laukų kaip kainodaros dimensijų nustatymas](set-up-pricing-dimensions.md) nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="79e0d-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="79e0d-106">Jei neatlikote šių procedūrų, grįžkite ir jas atlikite, o tada grįžkite į šią temą.</span><span class="sxs-lookup"><span data-stu-id="79e0d-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="79e0d-107">Kai pasiūlymo eilutės informacija sukuriama projekto pasiūlymo eilutės puslapyje **Pasiūlymo eilutė**, sistema sukuria dvi įvertinimo eilutes fone – vieną eilutę įvertinimo savikainos pusei, ir vieną pardavimo pusei.</span><span class="sxs-lookup"><span data-stu-id="79e0d-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="79e0d-108">Tas pats taikoma projekto sutarties eilutėms.</span><span class="sxs-lookup"><span data-stu-id="79e0d-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="79e0d-109">Kai keičiate kiekį arba lauką savikainos pusėje, šis pakeitimas perkeliamas į pardavimo pusę.</span><span class="sxs-lookup"><span data-stu-id="79e0d-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="79e0d-110">Tai įmanoma dėl šių priedų, kuriuos pakeitus kainodaros dimensijas reikia iš naujo užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="79e0d-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="79e0d-111">PreOperationContractLineDetailUpdate - atnaujina **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="79e0d-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="79e0d-112">PreOperationQuoteLineDetailUpdate - atnaujina **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="79e0d-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="79e0d-113">Toliau aprašytuose veiksmuose paaiškinta, kaip užregistruoti priedus.</span><span class="sxs-lookup"><span data-stu-id="79e0d-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="79e0d-114">Atidarykite **PluginRegistrationTool** ir prisijunkite prie savo internetinio egzemplioriaus.</span><span class="sxs-lookup"><span data-stu-id="79e0d-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="79e0d-115">Spustelėkite **Ieška** ir ieškokite priedo, kurį norite naujinti.</span><span class="sxs-lookup"><span data-stu-id="79e0d-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![Ieškos medžio ekrano kopija](media/PRT-1.png)

3. <span data-ttu-id="79e0d-117">Kai priedas bus rastas, pasirinkite jį, tada spustelėkite **Pasirinkti pagrindinėje formoje**.</span><span class="sxs-lookup"><span data-stu-id="79e0d-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="79e0d-118">Pasirinkite norimo naujinti priedo veiksmą, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Naujinti**.</span><span class="sxs-lookup"><span data-stu-id="79e0d-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![Priedo, kuris bus atnaujintas, ekrano kopija](media/PRT-2.png)
 
5. <span data-ttu-id="79e0d-120">Naujinimo lange filtravimo atributuose spustelėkite daugtaškį (**...**).</span><span class="sxs-lookup"><span data-stu-id="79e0d-120">In the update window, click the ellipsis (**...**) in the filtering attributes.</span></span>

 ![Esamo veiksmo konfigūravimo informacijos naujinimo ekrano kopija](media/PRT-3.png)
 
6. <span data-ttu-id="79e0d-122">Pažymėkite kainodaros atributo žymės langelius.</span><span class="sxs-lookup"><span data-stu-id="79e0d-122">Select the pricing attribute check boxes.</span></span>

 ![Ekrano kopija, kurioje matomas kainodaros atributų žymės langelių pasirinkimas](media/PRT-4.png)

7. <span data-ttu-id="79e0d-124">Spustelėkite **Gerai**, kad uždarytumėte puslapį, tada pasirinkite **Atnaujinti veiksmą**.</span><span class="sxs-lookup"><span data-stu-id="79e0d-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![Ekrano kopija, kurioje rodomas mygtukas „Atnaujinti veiksmą“](media/PRT-5.png)
 
8. <span data-ttu-id="79e0d-126">Šį procesą pakartokite su antru priedu **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction naujinimas**.</span><span class="sxs-lookup"><span data-stu-id="79e0d-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="79e0d-127">Uždarykite priedų registravimo įrankį.</span><span class="sxs-lookup"><span data-stu-id="79e0d-127">Close the plug-in registration tool.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]