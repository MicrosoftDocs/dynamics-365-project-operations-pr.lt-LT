---
title: Išplėstinių atsiskaitymo sutarčių kūrimas atsižvelgiant į eigą
description: Šioje temoje paaiškinama, kaip kurti projektų sutartis, kad galėtumėte generuoti klientų sąskaitas faktūras remdamiesi atlikto darbo procentine dalimi.
author: RadhikaRS
manager: AnnBe
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: b1de330df8cf85ed30c0ee4e4f2f2fe74d05dbff
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289514"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a><span data-ttu-id="ccf25-103">Išplėstinių atsiskaitymo sutarčių kūrimas atsižvelgiant į eigą</span><span class="sxs-lookup"><span data-stu-id="ccf25-103">Create advanced contracts for billing based on progress</span></span>
[!include [banner](../includes/banner.md)]

<span data-ttu-id="ccf25-104">Šioje temoje paaiškinama, kaip kurti projektų sutartis, kad galėtumėte sukurti klientų sąskaitas faktūras remdamiesi atlikto darbo procentine dalimi.</span><span class="sxs-lookup"><span data-stu-id="ccf25-104">This topic explains how to create project contracts so that you can create invoices for customers, based on a percentage of completed work.</span></span> <span data-ttu-id="ccf25-105">Sąskaitos faktūros sumos automatiškai apskaičiuojamos pagal darbo, kurį nustatėte projekte, biudžeto kategorijas.</span><span class="sxs-lookup"><span data-stu-id="ccf25-105">Invoice amounts are automatically calculated for the budget categories of work that you set up for a project.</span></span> <span data-ttu-id="ccf25-106">Sąskaitų faktūrų išrašymo laikas nustatomas jums derantis su klientu dėl projekto sutarties.</span><span class="sxs-lookup"><span data-stu-id="ccf25-106">The invoice timing is set when you negotiate the project contract with the customer.</span></span>

<span data-ttu-id="ccf25-107">Naudodami šioje temoje nurodytas procedūras galite nustatyti sutartį, susijusį projektą ir atsiskaitymo taisykles, pagal kurias apskaičiuojamos darbo, nustatyto projekte, biudžeto kategorijų sąskaitų sumos.</span><span class="sxs-lookup"><span data-stu-id="ccf25-107">Use the procedures in this topic to set up a contract, an associated project, and the billing rules that calculate invoice amounts for the budget categories of work that you set up for the project.</span></span>

<span data-ttu-id="ccf25-108">Sukūrę sutartį ir projektą, galite nustatyti projekto išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="ccf25-108">After you've created the contract and the project, you can set up the details of the project.</span></span> <span data-ttu-id="ccf25-109">Pavyzdžiui, galite apibrėžti veiklos rūšis ir priskirti projektui darbuotojus.</span><span class="sxs-lookup"><span data-stu-id="ccf25-109">For example, you can define activities and assign workers to the project.</span></span>

## <a name="example"></a><span data-ttu-id="ccf25-110">Pavyzdžiui</span><span class="sxs-lookup"><span data-stu-id="ccf25-110">Example</span></span>

<span data-ttu-id="ccf25-111">Jūsų organizacija yra programinės įrangos kūrimo įmonė.</span><span class="sxs-lookup"><span data-stu-id="ccf25-111">Your organization is a software development firm.</span></span> <span data-ttu-id="ccf25-112">Jūs sutinkate sukurti klientui algalapių apskaitos paketą už bendrą 20 000 JAV dolerių (USD) mokestį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-112">You agree to develop a payroll accounting package for a customer for a total fee of 20,000 US dollars (USD).</span></span> <span data-ttu-id="ccf25-113">Jūsų organizacija sutinka klientui išrašyti sąskaitą faktūrą, kai baigsite tam tikrą projekto procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-113">Your organization agrees to invoice the customer as you complete specific percentages of the project.</span></span> <span data-ttu-id="ccf25-114">Galite nustatyti toliau nurodytas darbo projektų kategorijas, kad jas galėtumėte naudoti atsiskaitydami:</span><span class="sxs-lookup"><span data-stu-id="ccf25-114">You set up the following project categories for the work, so that you can use them in the billing process:</span></span>

- <span data-ttu-id="ccf25-115">Konsultavimas</span><span class="sxs-lookup"><span data-stu-id="ccf25-115">Consulting</span></span>
- <span data-ttu-id="ccf25-116">Dizainas</span><span class="sxs-lookup"><span data-stu-id="ccf25-116">Design</span></span>
- <span data-ttu-id="ccf25-117">Diegimas</span><span class="sxs-lookup"><span data-stu-id="ccf25-117">Installation</span></span>

<span data-ttu-id="ccf25-118">Be to, nustatote atsiskaitymo taisykles, pagal kurias automatiškai apskaičiuojamos sąskaitos faktūros sumos už atlikto kiekvienos kategorijos projekto darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-118">You also set up billing rules that automatically calculate the invoice amounts for the percentage of project work that is completed in each category.</span></span>

<span data-ttu-id="ccf25-119">Biudžeto tvarkytuvas sukuria projektų kategorijų biudžetą.</span><span class="sxs-lookup"><span data-stu-id="ccf25-119">The budget manager creates a budget for the project categories.</span></span> <span data-ttu-id="ccf25-120">Atlikto darbo suma automatiškai apskaičiuojama kaip faktinio darbo procentinė dalis, palyginti su sąmatos sumomis.</span><span class="sxs-lookup"><span data-stu-id="ccf25-120">The amount of completed work is automatically calculated as a percentage of actual work in comparison to the budgeted amounts.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="ccf25-121">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="ccf25-121">Prerequisites</span></span>

<span data-ttu-id="ccf25-122">Prieš kurdami projektą, kuris naudoja atsiskaitymo taisykles, turite nustatyti atsiskaitymo taisyklių numeraciją ir mokesčių žurnalą, naudojamą registruoti vykdomus atsiskaitymus.</span><span class="sxs-lookup"><span data-stu-id="ccf25-122">Before you create a project that uses billing rules, you must set up the number sequences for billing rules and a fee journal that is used to post progress billings.</span></span>

1. <span data-ttu-id="ccf25-123">Eikite į **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-123">Go to **Project management and accounting** \> **Setup** \> **Project management and accounting parameters**.</span></span>
2. <span data-ttu-id="ccf25-124">Puslapyje **Projektų valdymo ir apskaitos parametrai**, skirtuke **Numeracijos**, nustatykite numeraciją, kurią norite naudoti, kai kuriamos atsiskaitymo taisyklės.</span><span class="sxs-lookup"><span data-stu-id="ccf25-124">On the **Project management and accounting parameters** page, on the **Number sequences** tab, set up the number sequence that you want to use when billing rules are created.</span></span>
3. <span data-ttu-id="ccf25-125">Eikite į **Projektų valdymas ir apskaita** \> **Žurnalai** \> **Mokestis**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-125">Go to **Project management and accounting** \> **Journals** \> **Fee**.</span></span>
4. <span data-ttu-id="ccf25-126">Puslapyje **Mokesčių žurnalas** pasirinkite **Naujas** ir įveskite žurnalo pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="ccf25-126">On the **Fee journal** page, select **New**, and enter the journal name.</span></span>

## <a name="create-a-contract-for-progress-billings"></a><span data-ttu-id="ccf25-127">Vykdomų atsiskaitymų sutarties kūrimas</span><span class="sxs-lookup"><span data-stu-id="ccf25-127">Create a contract for progress billings</span></span>

<span data-ttu-id="ccf25-128">Naudodami šią procedūrą sukurkite fiksuotos kainos projekto sutartį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-128">Use this procedure to create a project contract for a fixed-price project.</span></span> <span data-ttu-id="ccf25-129">Projekto sąskaitą faktūrą sukuriate, kai atliktas projekto darbas pasiekia nurodytą procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-129">You create a project invoice when the work that is completed on the project reaches a specified percentage.</span></span>

1. <span data-ttu-id="ccf25-130">Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projektų sutartys**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-130">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="ccf25-131">Puslapyje **Projektų sutartys** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-131">On the **Project contracts** page, select **New**.</span></span>
3. <span data-ttu-id="ccf25-132">Dialogo lange **Nauja projekto sutartis** nustatykite šiuos laukus:</span><span class="sxs-lookup"><span data-stu-id="ccf25-132">In the **New project contract** dialog box, set the following fields:</span></span>

    - <span data-ttu-id="ccf25-133">**Pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="ccf25-133">**Name**</span></span>
    - <span data-ttu-id="ccf25-134">**Finansavimo tipas**</span><span class="sxs-lookup"><span data-stu-id="ccf25-134">**Funding type**</span></span>
    - <span data-ttu-id="ccf25-135">**Finansavimo šaltinis**</span><span class="sxs-lookup"><span data-stu-id="ccf25-135">**Funding source**</span></span>
    - <span data-ttu-id="ccf25-136">**Pardavimo valiuta** – pagal numatytuosius nustatymus ši valiuta naudojama kliento sąskaitoms faktūroms, susijusioms su projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="ccf25-136">**Sales currency** – By default, this currency is used for customer invoices that are associated with the project contract.</span></span> <span data-ttu-id="ccf25-137">Tačiau pardavimo valiutą galite pakeisti konkrečioje kliento sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="ccf25-137">However, you can change the sales currency on a specific customer invoice.</span></span>

4. <span data-ttu-id="ccf25-138">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-138">Select **OK**.</span></span> <span data-ttu-id="ccf25-139">Informacija nukopijuojama į puslapio **Projektų sutartys** antraštę.</span><span class="sxs-lookup"><span data-stu-id="ccf25-139">The information is copied to the header of the **Project contracts** page.</span></span>
5. <span data-ttu-id="ccf25-140">Puslapyje **Projektų sutartys** įrašykite likusią reikiamą projekto informaciją.</span><span class="sxs-lookup"><span data-stu-id="ccf25-140">On the **Project contracts** page, fill in the rest of the required information for the project.</span></span>

## <a name="create-a-project-for-progress-billings"></a><span data-ttu-id="ccf25-141">Vykdomų atsiskaitymų projekto kūrimas</span><span class="sxs-lookup"><span data-stu-id="ccf25-141">Create a project for progress billings</span></span>

<span data-ttu-id="ccf25-142">Atlikite šiuos veiksmus, kad sukurtumėte projektą ir bet kokius papildomus projektus, susijusius su projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="ccf25-142">Follow these steps to create a project and any subprojects that are associated with a project contract.</span></span>

1. <span data-ttu-id="ccf25-143">Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-143">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="ccf25-144">Puslapyje **Visi projektai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-144">On the **All projects** page, select **New**.</span></span>
3. <span data-ttu-id="ccf25-145">Dialogo lange **Naujas projektas**, lauke **Projekto tipas**, pasirinkite **Laikas ir medžiaga**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-145">In the **New project** dialog box, in the **Project type** field, select **Time and material**.</span></span>
4. <span data-ttu-id="ccf25-146">Pasirinkite projekto grupę.</span><span class="sxs-lookup"><span data-stu-id="ccf25-146">Select a project group.</span></span> <span data-ttu-id="ccf25-147">Projektų grupė apibrėžia grupei priskirtų projektų registravimo informaciją.</span><span class="sxs-lookup"><span data-stu-id="ccf25-147">A project group defines the posting information for the projects that are assigned to the group.</span></span>
5. <span data-ttu-id="ccf25-148">Pasirinkite **Kurti projektą**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-148">Select **Create project**.</span></span>
6. <span data-ttu-id="ccf25-149">Sukūrę projektą nustatykite projekto etapą į **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-149">After the project is created, set the project stage to **In process**.</span></span>

## <a name="create-a-budget-for-a-project"></a><span data-ttu-id="ccf25-150">Projekto biudžeto kūrimas</span><span class="sxs-lookup"><span data-stu-id="ccf25-150">Create a budget for a project</span></span>

<span data-ttu-id="ccf25-151">Biudžeto kategorijos naudojamos norint automatiškai apskaičiuoti sąskaitos faktūros sumas už atlikto kiekvienos kategorijos darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-151">Budget categories are used to automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="ccf25-152">Norėdami sukurti numatytų išlaidų biudžeto kategorijas, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ccf25-152">Follow these steps to create budget categories for the estimated costs.</span></span>

1. <span data-ttu-id="ccf25-153">Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-153">Go to **Project management and accounting** \> **Projects** \> **All projects**.</span></span>
2. <span data-ttu-id="ccf25-154">Puslapyje **Visi projektai** pasirinkite ir atidarykite norimą projektą.</span><span class="sxs-lookup"><span data-stu-id="ccf25-154">On the **All projects** page, select and open the project that you want.</span></span>
3. <span data-ttu-id="ccf25-155">Puslapio **Projektai** veiksmų srityje, skirtuko **Planas** grupėje **Biudžetas** pasirinkite **Projekto biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-155">On the **Projects** page, on the Action Pane, on the **Plan** tab, in the **Budget** group, select **Project budget**.</span></span>
4. <span data-ttu-id="ccf25-156">Puslapyje **Projekto biudžetas** įveskite kiekvienos projekto kategorijos numatomą savikainą.</span><span class="sxs-lookup"><span data-stu-id="ccf25-156">On the **Project budget** page, enter an estimated cost for each category in the project.</span></span>

## <a name="create-billing-rules-for-progress-billings"></a><span data-ttu-id="ccf25-157">Vykdomų atsiskaitymų taisyklių kūrimas</span><span class="sxs-lookup"><span data-stu-id="ccf25-157">Create billing rules for progress billings</span></span>

1. <span data-ttu-id="ccf25-158">Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projektų sutartys**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-158">Go to **Project management and accounting** \> **Projects** \> **Project contracts**.</span></span>
2. <span data-ttu-id="ccf25-159">Puslapyje **Projektų sutartys** pasirinkite ir atidarykite projekto sutartį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-159">On the **Project contracts** page, select and open a project contract.</span></span>
3. <span data-ttu-id="ccf25-160">Projekto sutarties puslapio „FastTab“ **Atsiskaitymo taisyklės** pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-160">On the project contract page, on the **Billing rules** FastTab, select **Add**.</span></span>
4. <span data-ttu-id="ccf25-161">Puslapio **Atsiskaitymo taisyklė** lauke **Eilutės tipas** pasirinkite **Eiga**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-161">On the **Billing rule** page, in the **Line type** field, select **Progress**.</span></span>
5. <span data-ttu-id="ccf25-162">„FastTab“ **Atsiskaitymo taisyklės eilutės duomenys** lauke **Sutarties vertė** įveskite bendrą sutarties sumą.</span><span class="sxs-lookup"><span data-stu-id="ccf25-162">On the **Billing rule line details** FastTab, in the **Contract value** field, enter the total value of the contract.</span></span>
6. <span data-ttu-id="ccf25-163">Lauke **Kategorija** pasirinkite kategoriją, į kurią norite registruoti mokesčio operaciją.</span><span class="sxs-lookup"><span data-stu-id="ccf25-163">In the **Category** field, select the category to post the fee transaction to.</span></span>
7. <span data-ttu-id="ccf25-164">Lauke **Projektas** pasirinkite projektą, kuris naudoja šią atsiskaitymo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="ccf25-164">In the **Project** field, select the project that uses this billing rule.</span></span>
8. <span data-ttu-id="ccf25-165">Pasirinktinai: atsiskaitymo taisyklę priskirkite papildomiems projektams.</span><span class="sxs-lookup"><span data-stu-id="ccf25-165">Optional: Assign the billing rule to additional projects.</span></span> <span data-ttu-id="ccf25-166">„FastTab“ **Projektas** skyriuje **Esami projektai** pasirinkite projektą, tada pasirinkite dešiniosios rodyklės mygtuką norėdami įtraukti projektą į skyrių **Pasirinkti projektai**.</span><span class="sxs-lookup"><span data-stu-id="ccf25-166">On the **Project** FastTab, in the **Available projects** section, select a project, and then select the right arrow button to add the project to the **Selected projects** section.</span></span>
9. <span data-ttu-id="ccf25-167">Pasirinktinai: apskaičiuokite procentinę sumą, kurią klientas atšaukia iš sąskaitos faktūros mokėjimų.</span><span class="sxs-lookup"><span data-stu-id="ccf25-167">Optional: Calculate the percentage amount that the customer withholds from payments on an invoice.</span></span> <span data-ttu-id="ccf25-168">„FastTab“ **Mokėjimo sulaikymo sąlygos** pasirinkite finansavimo šaltinį, tada lauke **Sulaikymo procentinė dalis** įveskite sulaikymo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="ccf25-168">On the **Payment retention terms** FastTab, select the funding source, and then, in the **Retention percentage** field, enter the retention percentage.</span></span>
10. <span data-ttu-id="ccf25-169">Norėdami sukurti papildomas projekto sutarties atsiskaitymo taisykles, pakartokite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ccf25-169">Repeat these steps to create additional billing rules for the project contract.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]