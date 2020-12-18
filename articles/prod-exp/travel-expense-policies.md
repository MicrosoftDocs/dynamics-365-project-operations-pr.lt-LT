---
title: Išlaidų strategijų nustatymas
description: Galite nustatyti išlaidų strategijas, kurių darbuotojai turi laikytis įvesdami ir pateikdami išlaidų ataskaitas bei kelionių paraiškas „Microsoft Dynamics 365 Finance“.
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6240a7be175800ce6f3b066de9e935ab370629ef
ms.sourcegitcommit: 13a4e58eddbb0f81aca07c1ff452c420dbd8a68f
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/30/2020
ms.locfileid: "4650104"
---
# <a name="set-up-expense-policies"></a><span data-ttu-id="b1a30-103">Išlaidų strategijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="b1a30-103">Set up expense policies</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b1a30-104">Galite apibrėžti išlaidų strategijas, kurias turi atlikti darbuotojai, įvesdami ir pateikdami išlaidų ataskaitas ir kelionės paraiškas.</span><span class="sxs-lookup"><span data-stu-id="b1a30-104">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="b1a30-105">Įgyvendinus išlaidų politiką gali būti lengviau veiksmingai valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="b1a30-105">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="b1a30-106">Pavyzdžiui, galite nustatyti Niujorke esančio viešbučio išlaidų strategijas, kuriose nurodoma, kad kaina už naktį negali būti didesnė nei USD 250.</span><span class="sxs-lookup"><span data-stu-id="b1a30-106">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="b1a30-107">Jei darbuotojas pateikia išlaidų ataskaitą arba kelionės paraišką, kai kambario kaina viršija šią sumą, sistema praneš</span><span class="sxs-lookup"><span data-stu-id="b1a30-107">If a worker submits an expense report or a travel requisition in which the room rate exceeds this amount, the system will notify the</span></span>        
<span data-ttu-id="b1a30-108">darbuotojui, kad strategijoje nurodyta išlaidų suma buvo viršyta.</span><span class="sxs-lookup"><span data-stu-id="b1a30-108">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="b1a30-109">Galite konfigūruoti pranešimą, kurį darbuotojas, kai jūs</span><span class="sxs-lookup"><span data-stu-id="b1a30-109">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="b1a30-110">apibrėžite strategiją.</span><span class="sxs-lookup"><span data-stu-id="b1a30-110">define the policy.</span></span>      
        
<span data-ttu-id="b1a30-111">Galite apibrėžti trijų tipų strategijas:</span><span class="sxs-lookup"><span data-stu-id="b1a30-111">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="b1a30-112">Įspėjimas – leidžia darbuotojui pateikti išlaidų ataskaitą arba kelionės paraišką, tačiau išlaidos bus pažymėtos visiems tvirtintojams ir</span><span class="sxs-lookup"><span data-stu-id="b1a30-112">Warning – Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>        
  <span data-ttu-id="b1a30-113">vėlesnei ataskaitai.</span><span class="sxs-lookup"><span data-stu-id="b1a30-113">for later reporting.</span></span>        

- <span data-ttu-id="b1a30-114">Klaida – reikalaujama, kad darbuotojas peržiūrėtų išlaidas, kad įvykdytų šią strategiją prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką.</span><span class="sxs-lookup"><span data-stu-id="b1a30-114">Error – Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>       
 
 - <span data-ttu-id="b1a30-115">Pagrindimas – reikalaujama, kad darbuotojas arba vadovas pateiktų paaiškinimą, kodėl viršijama strategijoje nustatyta suma, prieš pateikdamas išlaidų ataskaitą arba kelionės paraišką.</span><span class="sxs-lookup"><span data-stu-id="b1a30-115">Justification – Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="b1a30-116">Strategijos patarimai</span><span class="sxs-lookup"><span data-stu-id="b1a30-116">Policy tips</span></span>
<span data-ttu-id="b1a30-117">Pateikiame kelis pasiūlymus, kurie gali padėti jums kuriant naujas išlaidų valdymo strategijas.</span><span class="sxs-lookup"><span data-stu-id="b1a30-117">Here are a few suggestions that can assist you when creating new policies for expense management.</span></span> 
* <span data-ttu-id="b1a30-118">Strategijos galioja nustatytą laikotarpį ir negalios, jei bus sukurtos po to, kai patiriamos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="b1a30-118">Policies are date effective and won't take effect if the policy is created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="b1a30-119">Pavyzdžiui, jei šiandien kuriate naują strategiją, kad būtų galima maksimaliai padidinti maisto kainą 50 USD, tada bet kokios esamos išlaidos, įrašytos kaip vakarykštės, nebus tikrinamos pagal šią strategiją.</span><span class="sxs-lookup"><span data-stu-id="b1a30-119">For example, if you are creating a new policy today to enforce a maximum meal expense of $50, then any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
* <span data-ttu-id="b1a30-120">Kurdami išlaidų kategorijos, kurią galima detaliai, strategiją, galite įtraukti sąlygą dėl išlaidų eilutės tipo.</span><span class="sxs-lookup"><span data-stu-id="b1a30-120">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="b1a30-121">Kai kurios strategijos, pvz., kvito reikalavimas, gali būti beprasmės detalizuotose eilutėse ir turėtų būti taikomos tik antraštės eilutei arba nedetalizuotai eilutei.</span><span class="sxs-lookup"><span data-stu-id="b1a30-121">Some policies such as requiring a receipt may not make sense for itemized lines and should only be applied to the header line or a non-itemized line.</span></span> 
* <span data-ttu-id="b1a30-122">Pagal numatytuosius nustatymus išlaidų valdymo strategijos yra vertinamos pagal šaltinio objektą.</span><span class="sxs-lookup"><span data-stu-id="b1a30-122">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="b1a30-123">Jei naudojate vidinės įmonės scenarijus, galite nustatyti, kad strategija būtų vertinama pagal paskirties objektą (skolinimosi objektas).</span><span class="sxs-lookup"><span data-stu-id="b1a30-123">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="b1a30-124">Norėdami vykdyti strategijas pagal paskirties objektą, įjunkite funkciją „Vertinti išlaidų strategiją skolinant juridiniam subjektui“ **Funkcijų valdymo** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="b1a30-124">To run the policies against the destination entity, turn on the "Evaluate Expense policy against borrowing legal entity" feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="b1a30-125">Kada vertinti strategijas</span><span class="sxs-lookup"><span data-stu-id="b1a30-125">When to evaluate policies</span></span>

<span data-ttu-id="b1a30-126">Išlaidų valdymo parametruose yra parinktis įvertinti išlaidų valdymo strategijas įrašius eilutę arba pateikus išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="b1a30-126">In expense management parameters, there is an option to either evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="b1a30-127">Jei pasirinksite įvertinti įrašius eilutę, tai užtikrins, kad naudotojai galės anksčiau matyti, ką reikia daryti norint iš karto užbaigti savo išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="b1a30-127">If you choose to evaluate when a line is saved this ensures that users have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="b1a30-128">Kitu atveju galite atidėti strategijos įvertinimą ir sutaupyti laiko tvirtindami pabaigoje, kai pateikiama į darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="b1a30-128">Otherwise, you can delay policy evaluation and save time if you have validation occur at the end, during submission to workflow.</span></span>
