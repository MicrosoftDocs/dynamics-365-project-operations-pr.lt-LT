---
title: Kvitų gretinimas su išlaidomis naudojant OCR
description: Šioje temoje pateikiama informacija apie optinio simbolių atpažinimo (OCR) apdorojimą kvitams.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 02c1bafbe907a657689b610ae792f88085320903
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897011"
---
# <a name="match-a-receipt-to-an-expense-using-ocr"></a><span data-ttu-id="69b74-103">Kvitų gretinimas su išlaidomis naudojant OCR</span><span class="sxs-lookup"><span data-stu-id="69b74-103">Match a receipt to an expense using OCR</span></span>

<span data-ttu-id="69b74-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="69b74-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="69b74-105">Išlaidų įrašas buvo patobulintas diegiant optinio simbolių atpažinimo (OCR) duomenų apdorojimą kvitams.</span><span class="sxs-lookup"><span data-stu-id="69b74-105">Expense entry has been enhanced through the introduction of optical character recognition (OCR) processing for receipts.</span></span> <span data-ttu-id="69b74-106">Šios funkcijos skirtos pagerinti vartotojų patirtį kuriant išlaidų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="69b74-106">This functionality is designed to improve the user experience when creating expense reports.</span></span>

## <a name="key-features"></a><span data-ttu-id="69b74-107">Pagrindinės funkcijos</span><span class="sxs-lookup"><span data-stu-id="69b74-107">Key features</span></span>

- <span data-ttu-id="69b74-108">Sistema išskleidžia pardavėjo vardą, datą ir bendrą kvitų sumą.</span><span class="sxs-lookup"><span data-stu-id="69b74-108">The system extracts the merchant name, date, and total amount from receipts.</span></span>
- <span data-ttu-id="69b74-109">Sistema bandys gretinti nepridėtus kvitus su nepridėtų išlaidų operacijomis.</span><span class="sxs-lookup"><span data-stu-id="69b74-109">The system will try to match unattached receipts to unattached expense transactions.</span></span>
- <span data-ttu-id="69b74-110">Galite kurti neautomatiniu būdu įvestas išlaidų operacijas iš kvitų.</span><span class="sxs-lookup"><span data-stu-id="69b74-110">You can create manually entered expense transactions from receipts.</span></span>

## <a name="attach-receipts-to-an-expense-report"></a><span data-ttu-id="69b74-111">Kvitų pridėjimas prie išlaidų ataskaitos</span><span class="sxs-lookup"><span data-stu-id="69b74-111">Attach receipts to an expense report</span></span>

<span data-ttu-id="69b74-112">Norėdami automatiškai pridėti kvitus, kuriuose yra kredito kortelių operacijų, kai sukuriama išlaidų ataskaita, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69b74-112">To automatically attach receipts that include credit card transactions when an expense report is created, complete the following steps.</span></span>

  1. <span data-ttu-id="69b74-113">Atidarykite **Išlaidų valdymo** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="69b74-113">Open the **Expense management** workspace.</span></span>
  2. <span data-ttu-id="69b74-114">Skirtuke **Kvitai** patikrinkite ar yra nepridėtų kvitų.</span><span class="sxs-lookup"><span data-stu-id="69b74-114">On the **Receipts** tab, verify that unattached receipts exist.</span></span> <span data-ttu-id="69b74-115">Taip pat galite įkelti kvitus skirtuke **Kvitai**.</span><span class="sxs-lookup"><span data-stu-id="69b74-115">You can also upload receipts on the **Receipts** tab.</span></span>
  3. <span data-ttu-id="69b74-116">Skirtuke **Išlaidos** patikrinkite ar yra nepridėtų išlaidų.</span><span class="sxs-lookup"><span data-stu-id="69b74-116">On the **Expenses** tab, verify that unattached expenses exist.</span></span> <span data-ttu-id="69b74-117">Paprastai išlaidų administratorius importuoja šias išlaidas iš kredito kortelės tiekėjo.</span><span class="sxs-lookup"><span data-stu-id="69b74-117">Typically, the expense administrator imports these expenses from the credit card provider.</span></span>
  4. <span data-ttu-id="69b74-118">Pažymėkite **Naują išlaidų ataskaitą**.</span><span class="sxs-lookup"><span data-stu-id="69b74-118">Select **New expense report**.</span></span> <span data-ttu-id="69b74-119">Atkreipkite dėmesį, kad kurdami išlaidų ataskaitą galite įtraukti išlaidas ir kvitus.</span><span class="sxs-lookup"><span data-stu-id="69b74-119">Notice that you can include expenses, and receipts, now as well, when you create an expense report.</span></span> <span data-ttu-id="69b74-120">Jei pridėsite išlaidas ir kvitus, automatiškai sugretinami kvitai ir išlaidos.</span><span class="sxs-lookup"><span data-stu-id="69b74-120">If you add both expenses and receipts, automatic matching of the receipts against the expenses is triggered.</span></span>

## <a name="create-or-match-receipts-to-an-expense-report"></a><span data-ttu-id="69b74-121">Kvitų kūrimas ar gretinimas prie išlaidų ataskaitos</span><span class="sxs-lookup"><span data-stu-id="69b74-121">Create or match receipts to an expense report</span></span>
<span data-ttu-id="69b74-122">Jei norite kurti išlaidas arba sugretinti išlaidas iš kvito, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="69b74-122">To create an expense, or match an expense from a receipt, complete the following steps.</span></span>

  1. <span data-ttu-id="69b74-123">Išlaidų ataskaitoje, skirtuke **Kvitai**, pridėkite kvitą pažymėdami **Įtraukti kvitus**.</span><span class="sxs-lookup"><span data-stu-id="69b74-123">On an expense report, on the **Receipts** tab, attach a receipt by selecting **Add receipts**.</span></span>
  2. <span data-ttu-id="69b74-124">Atkreipkite dėmesį į parinktis **Kurti** ir **Gretinti**, esančias po nusiųsto kvito vaizdu.</span><span class="sxs-lookup"><span data-stu-id="69b74-124">Under the uploaded image of the receipt, notice the **Create** and **Match** options.</span></span>

      - <span data-ttu-id="69b74-125">Pasirinkite **Kurti**, kad sukurtumėte rankiniu būdu įvestą išlaidų operaciją ir užpildytumėte iš kvito gautas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="69b74-125">Select **Create** to create a manually entered expense transaction and fill in the values that are extracted from the receipt.</span></span>
      - <span data-ttu-id="69b74-126">Jei pažymėjote **Gretinti**, sistema bandys sugretinti esamas išlaidas su kvitu.</span><span class="sxs-lookup"><span data-stu-id="69b74-126">If you select **Match**, the system tries to match an existing expense to the receipt.</span></span>

## <a name="installation"></a><span data-ttu-id="69b74-127">Diegimas</span><span class="sxs-lookup"><span data-stu-id="69b74-127">Installation</span></span>

<span data-ttu-id="69b74-128">Norėdami naudoti šias išplėstinių išlaidų galimybes, įdiekite „Expense Management Service“ papildinį, skirtą „Microsoft Dynamics 365 Finance“ ir įgalinkite savo egzempliorių funkcijas.</span><span class="sxs-lookup"><span data-stu-id="69b74-128">To use these advanced expense capabilities, install the Expense Management Service add-in for Microsoft Dynamics 365 Finance, and turn on the features in your instance.</span></span> <span data-ttu-id="69b74-129">Galite pasiekti papildinį iš savo projekto programoje „Microsoft Dynamics Lifecycle Services“ (LCS).</span><span class="sxs-lookup"><span data-stu-id="69b74-129">You can access the add-in from your project in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

1. <span data-ttu-id="69b74-130">Prisijunkite prie LCS ir atidarykite pageidaujamą aplinką.</span><span class="sxs-lookup"><span data-stu-id="69b74-130">Sign in to LCS, and open the desired environment.</span></span>
2. <span data-ttu-id="69b74-131">Eikite į **Pilna išsami informacija**.</span><span class="sxs-lookup"><span data-stu-id="69b74-131">Go to **Full details**.</span></span>
3. <span data-ttu-id="69b74-132">Pažymėkite **Prižiūrėti** arba slinkite žemyn į  **Aplinkos papildinių** „FastTab“.</span><span class="sxs-lookup"><span data-stu-id="69b74-132">Select **Maintain**, or scroll down to the **Environment add-ins** FastTab.</span></span>
4. <span data-ttu-id="69b74-133">Pažymėkite **Įdiegti naują papildinį**.</span><span class="sxs-lookup"><span data-stu-id="69b74-133">Select **Install a new add-in**.</span></span>
5. <span data-ttu-id="69b74-134">Pasirinkite **„Expense Management Service“**.</span><span class="sxs-lookup"><span data-stu-id="69b74-134">Select **Expense Management Service**.</span></span>
6. <span data-ttu-id="69b74-135">Vadovaukitės įdiegimo vadovu ir sutikite su terminais ir sąlygomis.</span><span class="sxs-lookup"><span data-stu-id="69b74-135">Follow the installation guide, and agree to the terms and conditions.</span></span>
7. <span data-ttu-id="69b74-136">Pasirinkti **Diegti**.</span><span class="sxs-lookup"><span data-stu-id="69b74-136">Select **Install**.</span></span>

<span data-ttu-id="69b74-137">**Funkcijų valdymo** darbo srityje Įjunkite šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="69b74-137">In the **Feature management** workspace, turn on the following features:</span></span>

- <span data-ttu-id="69b74-138">Išlaidų ataskaitų pertvarkymas</span><span class="sxs-lookup"><span data-stu-id="69b74-138">Expense reports re-imagined</span></span>
- <span data-ttu-id="69b74-139">Automatiškai gretinti ir kurti išlaidas iš kvito</span><span class="sxs-lookup"><span data-stu-id="69b74-139">Auto-match and create expense from receipt</span></span>

<span data-ttu-id="69b74-140">Įjungus šias funkcijas atliekami šie veiksmai:</span><span class="sxs-lookup"><span data-stu-id="69b74-140">When you turn on these features the following actions occur:</span></span>

- <span data-ttu-id="69b74-141">Esama **Išlaidų valdymo** darbo sritis pakeičiama nauja darbo sritimi.</span><span class="sxs-lookup"><span data-stu-id="69b74-141">The existing **Expense management** workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="69b74-142">Įtraukiamas naujas išlaidų lauko matomumo meniu elementas.</span><span class="sxs-lookup"><span data-stu-id="69b74-142">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="69b74-143">Dar galite atidaryti buvusių **Išlaidų ataskaitų** puslapį nuėję į **Išlaidų valdymas > Mano išlaidos > Išlaidų ataskaitos**.</span><span class="sxs-lookup"><span data-stu-id="69b74-143">You can still open the former **Expense reports** page by going to **Expense management > My expenses > Expense reports**.</span></span>
- <span data-ttu-id="69b74-144">Darbo eigos ir bet kokie patvirtinimai vis dar pateksite į esamų išlaidų ataskaitų puslapį.</span><span class="sxs-lookup"><span data-stu-id="69b74-144">Workflows and any approvals still take you to the existing expense reports page.</span></span>
- <span data-ttu-id="69b74-145">Kvitai bus apdorojami per „Microsoft Azure Cognitive Services“, o metaduomenys bus išskleisti ir įtraukti.</span><span class="sxs-lookup"><span data-stu-id="69b74-145">Receipts will be processed through Microsoft Azure Cognitive Services, and metadata will be extracted and added.</span></span>
- <span data-ttu-id="69b74-146">Įtraukiama parinktis, leidžianti kurti išlaidų ataskaitą, kurioje yra suderintų nepridėtų kvitų.</span><span class="sxs-lookup"><span data-stu-id="69b74-146">An option is added that lets you create an expense report that includes matched unattached receipts.</span></span>
- <span data-ttu-id="69b74-147">Prie išlaidų ataskaitų pridėta parinktis leidžia sukurti išlaidų eilutę iš kvito arba bando sugretinti esamą kvitą su esama išlaidų eilute.</span><span class="sxs-lookup"><span data-stu-id="69b74-147">An option that is added to expense reports lets you create an expense line from a receipt, or attempts to match an existing receipt to an existing expense line.</span></span>

## <a name="frequently-asked-questions"></a><span data-ttu-id="69b74-148">Dažnai užduodami klausimai</span><span class="sxs-lookup"><span data-stu-id="69b74-148">Frequently asked questions</span></span>

<span data-ttu-id="69b74-149">**Ar „Microsoft“ naudoja mano duomenis savo modeliams?**</span><span class="sxs-lookup"><span data-stu-id="69b74-149">**Does Microsoft use my data for its models?**</span></span>

<span data-ttu-id="69b74-150">Ne, „Microsoft“ sukūrė bendrąjį mašininio mokymo modelį, skirtą kvito apdorojimo paslaugai.</span><span class="sxs-lookup"><span data-stu-id="69b74-150">No, Microsoft has built a general machine learning model for its receipt processing service.</span></span> <span data-ttu-id="69b74-151">Šis modelis nėra pagrįstas jūsų įkeliamais kvitais.</span><span class="sxs-lookup"><span data-stu-id="69b74-151">This model isn't based on the receipts that you upload.</span></span>

<span data-ttu-id="69b74-152">**Kur ši funkciją prieinama ir apdorojama?**</span><span class="sxs-lookup"><span data-stu-id="69b74-152">**Where is this feature available and processed?**</span></span>

<span data-ttu-id="69b74-153">Šiuo metu funkcija palaikoma Jungtinėse Valstijose.</span><span class="sxs-lookup"><span data-stu-id="69b74-153">Currently, the United States is supported.</span></span>

<span data-ttu-id="69b74-154">**Kur yra mano kvitai?**</span><span class="sxs-lookup"><span data-stu-id="69b74-154">**Where do my receipts go?**</span></span>

<span data-ttu-id="69b74-155">Jei norite išskleisti lauko duomenis, „Finance“ susisieks su „Cognitive Services“.</span><span class="sxs-lookup"><span data-stu-id="69b74-155">Finance will contact Cognitive Services to extract the field data.</span></span> <span data-ttu-id="69b74-156">„Cognitive Services“ išsaugos jūsų kvito kopiją iki 24 valandų, kol vyksta apdorojimas.</span><span class="sxs-lookup"><span data-stu-id="69b74-156">Cognitive Services will retain a copy of your receipt for up to 24 hours while processing occurs.</span></span> <span data-ttu-id="69b74-157">Baigus apdorojimą „Cognitive Services“ pašalins kvitą.</span><span class="sxs-lookup"><span data-stu-id="69b74-157">After processing is completed, Cognitive Services will remove the receipt.</span></span> <span data-ttu-id="69b74-158">Kvitai vis tiek saugomi programoje „Finance“.</span><span class="sxs-lookup"><span data-stu-id="69b74-158">Receipts are still stored in Finance.</span></span>

<span data-ttu-id="69b74-159">Daugiau informacijos žr [Kvitų supratimo įjungimas naudojant naują formų atpažinimo funkciją](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span><span class="sxs-lookup"><span data-stu-id="69b74-159">For more information, see [Enable receipt understanding with Form Recognizer's new capability](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/).</span></span>
