---
title: Išlaidų kvito apdorojimas
description: Šioje temoje pateikiama informacija apie optinio simbolių atpažinimo (OCR) apdorojimą kvitams. Ši funkcija skirta pagerinti vartotojų aplinką kuriant išlaidų ataskaitas programoje „Microsoft Dynamics 365 Finance“.
author: stsporen
ms.date: 05/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: stsporen
ms.search.validFrom: 2019-11-20
ms.dyn365.ops.version: 10.0.8
ms.openlocfilehash: ed9c97ba9cc505106599c2896dc2112358d0c408
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993516"
---
# <a name="expense-receipt-processing"></a><span data-ttu-id="2a84a-104">Išlaidų kvito apdorojimas</span><span class="sxs-lookup"><span data-stu-id="2a84a-104">Expense receipt processing</span></span>

<span data-ttu-id="2a84a-105">Išlaidų įrašas buvo patobulintas diegiant optinio simbolių atpažinimo (OCR) duomenų apdorojimą kvitams.</span><span class="sxs-lookup"><span data-stu-id="2a84a-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="2a84a-106">Ši funkcija skirta pagerinti vartotojų aplinką kuriant išlaidų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="2a84a-106">This feature is designed to improve the user experience when expense reports are created.</span></span>

## <a name="key-features"></a><span data-ttu-id="2a84a-107">Pagrindinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="2a84a-107">Key features</span></span>

- <span data-ttu-id="2a84a-108">Iš kvitų nuskaitomi pardavėjo pavadinimas, data ir bendra suma.</span><span class="sxs-lookup"><span data-stu-id="2a84a-108">The merchant name, date, and total amount are extracted from receipts.</span></span>
- <span data-ttu-id="2a84a-109">Funkcija bandys gretinti nepridėtus kvitus su nepridėtų išlaidų operacijomis.</span><span class="sxs-lookup"><span data-stu-id="2a84a-109">The feature tries to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="2a84a-110">Vartotojai gali kurti neautomatiniu būdu įvestas išlaidų operacijas iš kvitų.</span><span class="sxs-lookup"><span data-stu-id="2a84a-110">Users can create manually entered expense transactions from receipts.</span></span>

## <a name="usage-examples"></a><span data-ttu-id="2a84a-111">Naudojimo pavyzdžiai</span><span class="sxs-lookup"><span data-stu-id="2a84a-111">Usage examples</span></span>

<span data-ttu-id="2a84a-112">Norėdami automatiškai pridėti kvitus, kuriuose yra kredito kortelių operacijų, kai sukuriama išlaidų ataskaita, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2a84a-112">To automatically attach receipts that include credit card transactions when an expense report is created, do the following:</span></span>

  1. <span data-ttu-id="2a84a-113">Atidarykite **Išlaidų valdymo** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="2a84a-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="2a84a-114">Skirtuke **Kvitai** patikrinkite ar yra nepridėtų kvitų.</span><span class="sxs-lookup"><span data-stu-id="2a84a-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="2a84a-115">Taip pat galite įkelti kvitus skirtuke **Kvitai**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="2a84a-116">Skirtuke **Išlaidos** patikrinkite ar yra nepridėtų išlaidų.</span><span class="sxs-lookup"><span data-stu-id="2a84a-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="2a84a-117">Paprastai išlaidų administratorius importuoja šias išlaidas iš kredito kortelės tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="2a84a-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="2a84a-118">Pažymėkite **Naują išlaidų ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-118">Select **New expense report**.</span></span> <span data-ttu-id="2a84a-119">Atkreipkite dėmesį, kad kurdami išlaidų ataskaitą galite įtraukti išlaidas ir kvitus.</span><span class="sxs-lookup"><span data-stu-id="2a84a-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="2a84a-120">Jei pridėsite išlaidas ir kvitus, automatiškai sugretinami kvitai ir išlaidos.</span><span class="sxs-lookup"><span data-stu-id="2a84a-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

<span data-ttu-id="2a84a-121">Jei norite kurti išlaidas arba sugretinti išlaidas iš kvito, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="2a84a-121">To create an expense, or match an expense from a receipt, do the following:</span></span>

  1. <span data-ttu-id="2a84a-122">Išlaidų ataskaitoje, skirtuke **Kvitai**, pridėkite kvitą pažymėdami **Įtraukti kvitus**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-122">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="2a84a-123">Atkreipkite dėmesį į parinktis **Kurti** ir **Gretinti**, esančias po nusiųsto kvito vaizdu.</span><span class="sxs-lookup"><span data-stu-id="2a84a-123">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="2a84a-124">Pasirinkite **Kurti**, kad sukurtumėte rankiniu būdu įvestą išlaidų operaciją ir užpildytumėte iš kvito gautas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="2a84a-124">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="2a84a-125">Jei pažymėjote **Gretinti**, sistema bandys sugretinti esamas išlaidas su kvitu.</span><span class="sxs-lookup"><span data-stu-id="2a84a-125">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="2a84a-126">Diegimas</span><span class="sxs-lookup"><span data-stu-id="2a84a-126">Installation</span></span>

<span data-ttu-id="2a84a-127">Ši funkcija veikia kartu su funkcija **Išlaidų ataskaitų pertvarkymas**, kad išlaidų tvarkymas būtų paprastesnis.</span><span class="sxs-lookup"><span data-stu-id="2a84a-127">This feature works in combination with the **Expense reports re-imagined** feature to help simplify the expense experience.</span></span> <span data-ttu-id="2a84a-128">Ši funkcija pasiekiama tik 2 pakopos ir aplinkose, kurios yra smėlio dėžė ir gamyba.</span><span class="sxs-lookup"><span data-stu-id="2a84a-128">This feature is only available for Tier 2+ environments, which are Sandbox and Production.</span></span>

<span data-ttu-id="2a84a-129">Norėdami naudoti šias išplėstinių išlaidų galimybes, įdiekite „Expense Management Service“ papildinį, skirtą „Microsoft Dynamics 365 Finance“ ir įgalinkite savo egzempliorių funkcijas.</span><span class="sxs-lookup"><span data-stu-id="2a84a-129">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="2a84a-130">Galite pasiekti papildinį iš savo projekto programoje „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="2a84a-130">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="2a84a-131">Prisijunkite prie LCS ir atidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="2a84a-131">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="2a84a-132">Eikite į **Pilna išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-132">Go to **Full details**.</span></span>
3. <span data-ttu-id="2a84a-133">Pažymėkite **Prižiūrėti** arba slinkite žemyn į  **Aplinkos papildinių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="2a84a-133">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="2a84a-134">Pažymėkite **Įdiegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-134">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="2a84a-135">Pasirinkite **„Expense Management Service“**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-135">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="2a84a-136">Vadovaukitės įdiegimo vadovu ir sutikite su terminais ir sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="2a84a-136">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="2a84a-137">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-137">Select **Install**.</span></span>

<span data-ttu-id="2a84a-138">**Funkcijų valdymo** darbo srityje Įjunkite šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="2a84a-138">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="2a84a-139">Išlaidų ataskaitų pertvarkymas</span><span class="sxs-lookup"><span data-stu-id="2a84a-139">Expense reports re-imagined</span></span>
- <span data-ttu-id="2a84a-140">Automatiškai gretinti ir kurti išlaidas iš kvito</span><span class="sxs-lookup"><span data-stu-id="2a84a-140">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="2a84a-141">Įjungus šias funkcijas atliekami šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="2a84a-141">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="2a84a-142">Esama **Išlaidų valdymo** darbo sritis pakeičiama nauja darbo sritimi.</span><span class="sxs-lookup"><span data-stu-id="2a84a-142">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="2a84a-143">Įtraukiamas naujas išlaidų lauko matomumo meniu elementas.</span><span class="sxs-lookup"><span data-stu-id="2a84a-143">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="2a84a-144">Dar galite atidaryti buvusių **Išlaidų ataskaitų** puslapį nuėję į **Išlaidų valdymas > Mano išlaidos > Išlaidų ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="2a84a-144">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="2a84a-145">Darbo eigos ir bet kokie patvirtinimai vis dar pateksite į esamų išlaidų ataskaitų puslapį.</span><span class="sxs-lookup"><span data-stu-id="2a84a-145">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="2a84a-146">Kvitai bus apdorojami per „Microsoft Azure Cognitive Services“, o metaduomenys bus išskleisti ir įtraukti.</span><span class="sxs-lookup"><span data-stu-id="2a84a-146">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="2a84a-147">Įtraukiama parinktis, leidžianti kurti išlaidų ataskaitą, kurioje yra suderintų nepridėtų kvitų.</span><span class="sxs-lookup"><span data-stu-id="2a84a-147">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="2a84a-148">Prie išlaidų ataskaitų pridėta parinktis leidžia sukurti išlaidų eilutę iš kvito arba bando sugretinti esamą kvitą su esama išlaidų eilute.</span><span class="sxs-lookup"><span data-stu-id="2a84a-148">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

<span data-ttu-id="2a84a-149">Daugiau informacijos apie funkciją Išlaidų ataskaitų pertvarkymas žr. [Išlaidų ataskaitų pertvarkymas](ExpenseWorkspaceNew.md).</span><span class="sxs-lookup"><span data-stu-id="2a84a-149">For more information about the Expense reports re-imagined feature, see [Expense reports reimagined](ExpenseWorkspaceNew.md).</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="2a84a-150">Dažnai užduodami klausimai</span><span class="sxs-lookup"><span data-stu-id="2a84a-150">Frequently asked questions</span></span>

<span data-ttu-id="2a84a-151">**Ar „Microsoft“ naudoja mano duomenis savo modeliams?**</span><span class="sxs-lookup"><span data-stu-id="2a84a-151">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="2a84a-152">Ne, „Microsoft“ sukūrė bendrąjį mašininio mokymo modelį, skirtą kvito apdorojimo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="2a84a-152">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="2a84a-153">Šis modelis nėra pagrįstas jūsų įkeliamais kvitais.</span><span class="sxs-lookup"><span data-stu-id="2a84a-153">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="2a84a-154">**Kur ši funkciją prieinama ir apdorojama?**</span><span class="sxs-lookup"><span data-stu-id="2a84a-154">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="2a84a-155">Šiuo metu funkcija palaikoma Jungtinėse Valstijose.</span><span class="sxs-lookup"><span data-stu-id="2a84a-155">Currently, the United States is supported.</span></span>

<span data-ttu-id="2a84a-156">**Kur yra mano kvitai?**</span><span class="sxs-lookup"><span data-stu-id="2a84a-156">**Where do my receipts go?**</span></span>

<span data-ttu-id="2a84a-157">Jei norite išskleisti lauko duomenis, „Finance“ susisieks su „Cognitive Services“.</span><span class="sxs-lookup"><span data-stu-id="2a84a-157">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="2a84a-158">„Cognitive Services“ išsaugos jūsų kvito kopiją iki 24 valandų, kol vyksta apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="2a84a-158">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="2a84a-159">Baigus apdorojimą „Cognitive Services“ pašalins kvitą.</span><span class="sxs-lookup"><span data-stu-id="2a84a-159">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="2a84a-160">Kvitai vis tiek saugomi programoje „Finance“.</span><span class="sxs-lookup"><span data-stu-id="2a84a-160">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="2a84a-161">Daugiau informacijos žr [Kvitų supratimo įjungimas naudojant naują formų atpažinimo funkciją](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="2a84a-161">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]