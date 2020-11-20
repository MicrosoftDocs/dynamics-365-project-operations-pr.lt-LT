---
title: Apibrėžti išlaidų strategijas
description: Galite apibrėžti išlaidų strategijas, kurias turi atlikti darbuotojai, įvesdami ir pateikdami išlaidų ataskaitas ir kelionės paraiškas.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: c55cec132649daf9ee08ea4d8db3668860247934
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128428"
---
# <a name="define-expense-policies"></a><span data-ttu-id="6f117-103">Apibrėžti išlaidų strategijas</span><span class="sxs-lookup"><span data-stu-id="6f117-103">Define expense policies</span></span>

<span data-ttu-id="6f117-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="6f117-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="6f117-105">Galite apibrėžti išlaidų strategijas, kurias turi atlikti darbuotojai, įvesdami ir pateikdami išlaidų ataskaitas ir kelionės paraiškas.</span><span class="sxs-lookup"><span data-stu-id="6f117-105">You can define policies that your workers must follow when entering and submitting expense reports and travel requisitions.</span></span>         
<span data-ttu-id="6f117-106">Įgyvendinus išlaidų politiką gali būti lengviau veiksmingai valdyti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="6f117-106">Implementing expense policies can help you manage expenses effectively.</span></span>         

<span data-ttu-id="6f117-107">Pavyzdžiui, galite nustatyti Niujorke esančio viešbučio išlaidų strategijas, kuriose nurodoma, kad kaina už naktį negali būti didesnė nei USD 250.</span><span class="sxs-lookup"><span data-stu-id="6f117-107">For example, you can set a policy for hotel expenses in New York City, which states that the per night expense cannot exceed USD 250.</span></span>       
<span data-ttu-id="6f117-108">Jei darbuotojas pateikia išlaidų ataskaitą arba kelionių paraiškas, kai kambario kaina viršija šią sumą, sistema praneš</span><span class="sxs-lookup"><span data-stu-id="6f117-108">If a worker submits an expense report or travel requisition where the room rate exceeds this amount, the system will notify the</span></span>         
<span data-ttu-id="6f117-109">darbuotojui, kad strategijoje nurodyta išlaidų suma buvo viršyta.</span><span class="sxs-lookup"><span data-stu-id="6f117-109">worker that the policy amount for the expense has been exceeded.</span></span> <span data-ttu-id="6f117-110">Galite konfigūruoti pranešimą, kurį darbuotojas, kai jūs</span><span class="sxs-lookup"><span data-stu-id="6f117-110">You can configure the message that the worker will receive when you</span></span>        
<span data-ttu-id="6f117-111">apibrėžite strategiją.</span><span class="sxs-lookup"><span data-stu-id="6f117-111">define the policy.</span></span>      
        
<span data-ttu-id="6f117-112">Galite apibrėžti trijų tipų strategijas:</span><span class="sxs-lookup"><span data-stu-id="6f117-112">You can define three types of policies:</span></span>         
        
- <span data-ttu-id="6f117-113">**Įspėjimas** – leidžia darbuotojui pateikti išlaidų ataskaitą arba kelionių rekvizavimą, tačiau sąskaita bus pažymėta visiems tvirtintojams ir</span><span class="sxs-lookup"><span data-stu-id="6f117-113">**Warning**: Allows the worker to submit an expense report or travel requisition but the expense will be marked for all approvers and</span></span>         
  <span data-ttu-id="6f117-114">vėlesnei ataskaitai.</span><span class="sxs-lookup"><span data-stu-id="6f117-114">for later reporting.</span></span>        

- <span data-ttu-id="6f117-115">**Klaida** – reikalaujama, kad darbuotojas peržiūrės išlaidas, kad įvykdytų šią strategiją prieš pateikdama išlaidų ataskaitą arba kelionės paraišką.</span><span class="sxs-lookup"><span data-stu-id="6f117-115">**Error**: Requires the worker to revise the expense to comply with the policy before submitting the expense report or travel requisition.</span></span>        
 
 - <span data-ttu-id="6f117-116">**Pagrindimas** – reikalaujama, kad darbuotojas arba vadovas pateiktų paaiškinimą, kad viršytų politikos sumą prieš pateikdami išlaidų ataskaitą arba kelionės paraišką.</span><span class="sxs-lookup"><span data-stu-id="6f117-116">**Justification**: Requires the worker or a manager to enter a justification for exceeding the policy amount before submitting the expense report or travel requisition.</span></span>        

## <a name="policy-tips"></a><span data-ttu-id="6f117-117">Strategijos patarimai</span><span class="sxs-lookup"><span data-stu-id="6f117-117">Policy tips</span></span>
<span data-ttu-id="6f117-118">Pateikiame kelis pasiūlymus, kurie gali padėti jums kuriant naujas išlaidų valdymo strategijas:</span><span class="sxs-lookup"><span data-stu-id="6f117-118">Here are a few suggestions that can assist you when creating new policies for expense management:</span></span> 

- <span data-ttu-id="6f117-119">Strategijos yra datos efektyvios, o tai reiškia, kad strategija neįsigalios, jei ji bus sukurta naudojant datą, kai sąskaita įvyko.</span><span class="sxs-lookup"><span data-stu-id="6f117-119">Policies are date effective which means a policy won't take effect if it's created with a date after the date that the expense occurred.</span></span> <span data-ttu-id="6f117-120">Pavyzdžiui, šiuo metu kuriate naują strategiją, kad būtų užtikrintas maksimalus $50.</span><span class="sxs-lookup"><span data-stu-id="6f117-120">For example, you create a new policy today to enforce a maximum meal expense of $50.</span></span> <span data-ttu-id="6f117-121">Visos iš vakar įvedamos išlaidos nebus tikrinamos pagal šią strategiją.</span><span class="sxs-lookup"><span data-stu-id="6f117-121">Any existing expenses entered as of yesterday won't be checked against this policy.</span></span>
- <span data-ttu-id="6f117-122">Kurdami išlaidų kategorijos, kurią galima detaliai, strategiją, galite įtraukti sąlygą dėl išlaidų eilutės tipo.</span><span class="sxs-lookup"><span data-stu-id="6f117-122">When creating a policy for an expense category that can be itemized, consider adding a condition for expense line type.</span></span> <span data-ttu-id="6f117-123">Kai kurios strategijos, pvz., gavimo reikalavimas, gali būti neprašomos detaliam detalizavimui.</span><span class="sxs-lookup"><span data-stu-id="6f117-123">Some policies, such as requiring a receipt, may not make sense for itemized lines.</span></span> <span data-ttu-id="6f117-124">Tokiu atveju strategija taikoma tik antraštės eilutei arba nedetalizuotai eilutei.</span><span class="sxs-lookup"><span data-stu-id="6f117-124">In this situation, the policy only is applied to the header line or a non-itemized line.</span></span> 
- <span data-ttu-id="6f117-125">Pagal numatytuosius nustatymus išlaidų valdymo strategijos yra vertinamos pagal šaltinio objektą.</span><span class="sxs-lookup"><span data-stu-id="6f117-125">Expense management policies are evaluated against the source entity by default.</span></span> <span data-ttu-id="6f117-126">Jei naudojate vidinės įmonės scenarijus, galite nustatyti, kad strategija būtų vertinama pagal paskirties objektą (skolinimosi objektas).</span><span class="sxs-lookup"><span data-stu-id="6f117-126">For intercompany scenarios, you can set the policy to be evaluated against the destination entity (borrowing entity) instead.</span></span> <span data-ttu-id="6f117-127">Norėdami vykdyti strategijas pagal paskirties objektą, įjunkite **Vertinti išlaidų strategiją prieš skolindami juridinį objektą** funkciją **Funkcijų valdymo** darbo srityje.</span><span class="sxs-lookup"><span data-stu-id="6f117-127">To run the policies against the destination entity, turn on the **Evaluate Expense policy against borrowing legal entity** feature in the **Feature Management** workspace.</span></span>

## <a name="when-to-evaluate-policies"></a><span data-ttu-id="6f117-128">Kada vertinti strategijas</span><span class="sxs-lookup"><span data-stu-id="6f117-128">When to evaluate policies</span></span>

<span data-ttu-id="6f117-129">Išlaidų valdymo parametruose galite pažymėti, kad, įrašius eilutę arba pateikus išlaidų ataskaitą, išlaidų valdymo strategijos būtų įvertintos.</span><span class="sxs-lookup"><span data-stu-id="6f117-129">In expense management parameters, you can select to evaluate expense management policies when a line is saved or when an expense report is submitted.</span></span> <span data-ttu-id="6f117-130">Jei pasirinksite įvertinti, kada eilutė bus įrašyta, vartotojai galės anksčiau matyti, ką reikia daryti norint iš karto užbaigti savo išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="6f117-130">If you choose to evaluate when a line is saved, users will have earlier visibility into what they need to do to complete their expense report all at once.</span></span> <span data-ttu-id="6f117-131">Kitu atveju galite atidėti strategijos įvertinimą ir sutaupyti laiko, kol jis nepasibaigs pateikimo darbo eigos metu.</span><span class="sxs-lookup"><span data-stu-id="6f117-131">Otherwise, you can delay policy evaluation and save time by validating at the end, during the submission to workflow.</span></span>
