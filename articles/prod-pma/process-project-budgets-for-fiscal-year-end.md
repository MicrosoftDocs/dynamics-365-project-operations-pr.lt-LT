---
title: Projektų biudžetų perkėlimas finansinių metų pabaigoje
description: Šiame straipsnyje pateikiama informacijos, kaip perkelti likusias biudžeto sumas į būsimus metus ir sukurti biudžeto registro duomenis.
author: Yowelle
manager: AnnBe
ms.date: 03/23/2020
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
ms.openlocfilehash: 1f601be072e84fc04246cd55a260c8004f6fb3e5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289739"
---
# <a name="transfer-project-budgets-at-fiscal-year-end"></a><span data-ttu-id="a3252-103">Projektų biudžetų perkėlimas finansinių metų pabaigoje</span><span class="sxs-lookup"><span data-stu-id="a3252-103">Transfer project budgets at fiscal year end</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="a3252-104">Dirbdami su daugiamečiu projektu, finansinių metų pabaigoje galite turėti likusių biudžeto lėšų.</span><span class="sxs-lookup"><span data-stu-id="a3252-104">When working on a multi-year project, you might have remaining budget at the end of the fiscal year.</span></span> <span data-ttu-id="a3252-105">Likusias biudžeto sumas galite perkelti į būsimus metus ir sukurti jų biudžeto registro duomenis susijusiose didžiosios knygos sąskaitose.</span><span class="sxs-lookup"><span data-stu-id="a3252-105">You can transfer the remaining budget amounts to a future year, and create budget register details for the amounts in the associated general ledger accounts.</span></span> <span data-ttu-id="a3252-106">Prieš perkeldami likusias biudžeto sumas peržiūrėkite jas ir išanalizuokite.</span><span class="sxs-lookup"><span data-stu-id="a3252-106">Before you carry forward the remaining amounts, review and analyze the remaining budget amounts.</span></span>

## <a name="review-and-analyze-remaining-budget-amounts"></a><span data-ttu-id="a3252-107">Likusių biudžeto sumų peržiūra ir analizė</span><span class="sxs-lookup"><span data-stu-id="a3252-107">Review and analyze remaining budget amounts</span></span>

<span data-ttu-id="a3252-108">Atlikite toliau nurodytus veiksmus norėdami peržiūrėti projektų metų pabaigos biudžeto sumas, bet sumų neperkelkite.</span><span class="sxs-lookup"><span data-stu-id="a3252-108">Complete the following steps to review the year-end budget amounts for projects, but not carry the amounts forward.</span></span>

1. <span data-ttu-id="a3252-109">Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Biudžetai** > **Perkelti biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="a3252-109">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="a3252-110">Puslapio **Projekto biudžeto perkėlimo procesas** skirtuke **Metų pabaigos parinktys** patikrinkite, ar neįjungta **Perkelti likusias projekto biudžeto sumas**.</span><span class="sxs-lookup"><span data-stu-id="a3252-110">On the **Project budget carry-forward process** page, on the **Year-end options** tab, verify that **Carry forward remaining project budget amounts** is not enabled.</span></span>
3. <span data-ttu-id="a3252-111">Skirtuko **Parametrai** lauke **Projekto biudžeto metai** pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="a3252-111">On the **Parameters** tab, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
4. <span data-ttu-id="a3252-112">Lauke **Finansinių metų atidarymas** pasirinkite finansinius metus, kurių likusią biudžeto sumą norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="a3252-112">In the **Opening fiscal year** field, select the fiscal year for which you want to view the remaining budget amount.</span></span> 
5. <span data-ttu-id="a3252-113">Lauke **Iš prognozės modelio** pasirinkite **Likęs biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="a3252-113">In the **From forecast model** field, select **Remaining budget**.</span></span> 
6. <span data-ttu-id="a3252-114">Jei norite įtraukti projektus, atitinkančius jūsų pasirinktus kriterijus ir neturinčius likusio biudžeto, pasirinkite **Rodyti nulinį likutį**.</span><span class="sxs-lookup"><span data-stu-id="a3252-114">To include projects that meet your selected criteria and have no remaining budget, select **Show zero remaining**.</span></span>  
7. <span data-ttu-id="a3252-115">Skirtuke **Pasirinkti biudžetus** pasirinkite **Nuskaityti visus biudžetus** norėdami įkelti visus biudžetus, kurie atitinka jūsų pasirinktus kriterijus, tada pasirinkite **Apdoroti**.</span><span class="sxs-lookup"><span data-stu-id="a3252-115">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match your selected criteria, and then select **Process**.</span></span> 
8. <span data-ttu-id="a3252-116">Norėdami sukurti duomenų bazės užklausą, kuri į sritį įkelia tam tikrą biudžetų rinkinį, pasirinkite **Nuskaityti pasirinktus biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="a3252-116">To design a database query that loads a specific set of budgets into the pane, select **Retrieve selected budgets**.</span></span>

<span data-ttu-id="a3252-117">Norėdami gauti daugiau informacijos apie tam tikrą srities eilutę, ją pasirinkite ir pažymėkite **Peržiūrėti biudžeto informaciją** arba **Peržiūrėti sąskaitas**.</span><span class="sxs-lookup"><span data-stu-id="a3252-117">For more information about a specific line in the pane, select the line, and then select **View budget details** or **View accounts**.</span></span>

## <a name="carry-forward-remaining-budget-amounts"></a><span data-ttu-id="a3252-118">Likusių biudžeto sumų perkėlimas</span><span class="sxs-lookup"><span data-stu-id="a3252-118">Carry forward remaining budget amounts</span></span> 

<span data-ttu-id="a3252-119">Kai apdorojate likusias biudžeto sumas, galite sukurti perkeliamų sumų operacijas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="a3252-119">When you process remaining budget amounts, you can create transactions in the general ledger for the amounts that you are carrying forward.</span></span> <span data-ttu-id="a3252-120">Norėdami sukurti didžiosios knygos operacijas, atlikite veiksmus, nurodytus skyriuje [Biudžeto sumų perkėlimas ir didžiosios knygos operacijų kūrimas](#carry-forward).</span><span class="sxs-lookup"><span data-stu-id="a3252-120">To create general ledger transactions, complete the steps in the section, [Carry forward budget amounts and create general ledger transactions](#carry-forward).</span></span> 

> [!NOTE]
> <span data-ttu-id="a3252-121">Perkeltos biudžeto sumos perkeliamos į prognozės modelį, kuris puslapyje **Prognozės modeliai** yra pasirinktas kaip perkėlimo prognozės modelis.</span><span class="sxs-lookup"><span data-stu-id="a3252-121">Budget amounts that are carried forward are transferred to the forecast model that is selected in the **Forecast models** page as the carry-forward forecast model.</span></span>  

## <a name="carry-forward-budget-amounts-and-create-general-ledger-transactions"></a><a name="carry-forward"></a><span data-ttu-id="a3252-122">Biudžeto sumų perkėlimas ir didžiosios knygos operacijų kūrimas</span><span class="sxs-lookup"><span data-stu-id="a3252-122">Carry forward budget amounts and create general ledger transactions</span></span>

1.  <span data-ttu-id="a3252-123">Pasirinkite **Projektų valdymas ir apskaita** > **Periodinis** > **Biudžetai** > **Perkelti biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="a3252-123">Select **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span> 
2. <span data-ttu-id="a3252-124">Puslapyje **Projekto biudžeto perkėlimo procesas** pasirinkite **Metų pabaiga**, tada įjunkite **Perkelti likusias projekto biudžeto sumas** ir **Sukurti biudžeto registro įrašus didžiojoje knygoje**.</span><span class="sxs-lookup"><span data-stu-id="a3252-124">On the **Project budget carry-forward process** page, select **Year-end**, and then enable **Carry forward remaining project budget amounts** and **Create budget register entries in general ledger**.</span></span> 
3. <span data-ttu-id="a3252-125">Skirtuke **Parametrai**, laukų grupėje **Projekto parametrai**, pasirinkite tai:</span><span class="sxs-lookup"><span data-stu-id="a3252-125">On the **Parameters** tab, in the **Project parameters** field group, select the following:</span></span>

   - <span data-ttu-id="a3252-126">**Projekto biudžeto metai**: pasirinkite finansinių metų, kurių likusias biudžeto sumas norite peržiūrėti, pradžią.</span><span class="sxs-lookup"><span data-stu-id="a3252-126">**Project budget year**: Select the beginning of the fiscal year for which you want to view the remaining budget amounts.</span></span> 
   - <span data-ttu-id="a3252-127">**Pelnas ir nuostolis**: sukurkite pelno ir nuostolio operacijas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="a3252-127">**Profit and loss**: Create profit and loss transactions in the general ledger.</span></span> 
   -  <span data-ttu-id="a3252-128">**NG**: sukurkite nebaigtos gamybos (NG) operacijas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="a3252-128">**WIP**: Create Work in Progress (WIP) transactions in the general ledger.</span></span>
   -  <span data-ttu-id="a3252-129">**Algalapis**: sukurkite algalapio paskirstymo operacijas didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="a3252-129">**Payroll**: Create payroll allocation transactions in the general ledger.</span></span> 

5. <span data-ttu-id="a3252-130">Laukų grupėje **Didžioji knyga** pateikite nurodytą informaciją:</span><span class="sxs-lookup"><span data-stu-id="a3252-130">In the **General ledger** field group, provide the following information:</span></span> 

   - <span data-ttu-id="a3252-131">Lauke **Finansinių metų atidarymas** pasirinkite finansinius metus, kurių likusias projektų biudžetų sumas norite perkelti.</span><span class="sxs-lookup"><span data-stu-id="a3252-131">In the **Opening fiscal year** field, select the fiscal year that you want to transfer remaining budget amounts to for the projects.</span></span> <span data-ttu-id="a3252-132">Numatytoji reikšmė yra vieneri metai po lauke **Projekto biudžeto metai** nurodytos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="a3252-132">The default value is one year after the value in the **Project budget year** field.</span></span>
   -  <span data-ttu-id="a3252-133">Lauke **Perkėlimo laikotarpis** pasirinkite laikotarpį, kurio biudžeto registro duomenis norite sukurti didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="a3252-133">In the **Carry-forward period** field, select the period that you want to create the budget register details for in the general ledger.</span></span> <span data-ttu-id="a3252-134">Paprastai tai yra pirmasis atidarytų finansinių metų laikotarpis.</span><span class="sxs-lookup"><span data-stu-id="a3252-134">This is typically the first period in the opening fiscal year.</span></span>

6. <span data-ttu-id="a3252-135">Laukų grupėje **Kopijuoti iš / į** pateikite nurodytą informaciją:</span><span class="sxs-lookup"><span data-stu-id="a3252-135">In the **Copy from/to** field group, provide the following information:</span></span>

   - <span data-ttu-id="a3252-136">Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis projektų biudžetų sumomis, kurias norite perkelti.</span><span class="sxs-lookup"><span data-stu-id="a3252-136">In the **From forecast model** field, select the project budget forecast model associated with the remaining budget amounts you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="a3252-137">Lauke **Į didžiosios knygos biudžeto modelį** pasirinkite didžiosios knygos biudžeto modelį, susietą su biudžetų sumomis, kurias norite perkelti į didžiąją knygą.</span><span class="sxs-lookup"><span data-stu-id="a3252-137">In the **To ledger budget model** field, select the ledger budget model associated with the budget amounts you want to transfer to the general ledger.</span></span> 
   -  <span data-ttu-id="a3252-138">Pasirinkite **Perkelti pardavimo valiutą** norėdami naudoti didžiosios knygos operacijų, sukuriamų perkeliant projektų biudžetų sumas, projekto pardavimo valiutą.</span><span class="sxs-lookup"><span data-stu-id="a3252-138">Select **Transfer sales currency** to use the project's sales currency for the general ledger transactions that are created when you transfer the budget amounts for the projects.</span></span> <span data-ttu-id="a3252-139">Kai parinktis nepažymėta, operacijose naudojama apskaitos valiuta.</span><span class="sxs-lookup"><span data-stu-id="a3252-139">When the option is not selected, the transactions use the accounting currency.</span></span> 
   -  <span data-ttu-id="a3252-140">Pasirinkite **Rodyti likutinį nulį**, kad būtų įtraukti projektai, kuriuose nėra likusių biudžeto sumų, bet atitinka kitus kriterijus, kuriuos pasirinkote apatinėje srityje rodomuose projektuose.</span><span class="sxs-lookup"><span data-stu-id="a3252-140">Select **Show zero remaining** to include projects that have no remaining budget amounts, but meet the other criteria that you select in the projects displayed in the bottom pane.</span></span>

7. <span data-ttu-id="a3252-141">Skirtuke **Pasirinkti biudžetus** pasirinkite **Nuskaityti visus biudžetus** norėdami įkelti visus biudžetus, kurie atitinka jūsų pasirinktus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="a3252-141">On the **Select Budgets** tab, select **Retrieve all budgets** to load all budgets that match the criteria you selected.</span></span> <span data-ttu-id="a3252-142">Norėdami sukurti duomenų bazės užklausą, kuri į sritį įkelia tam tikrą projektų biudžetų rinkinį, pasirinkite **Nuskaityti pasirinktus biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="a3252-142">If you prefer to design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>
8. <span data-ttu-id="a3252-143">Pasirinkite kiekvieno projekto, kurį norite apdoroti, parinktį, esančią projekto eilutės pradžioje.</span><span class="sxs-lookup"><span data-stu-id="a3252-143">For each project that you want to process, select the option at the beginning of the line for the project.</span></span>

    > [!TIP]
    > <span data-ttu-id="a3252-144">Jei norite pasirinkti visus arba daugelį projektų, pažymėkite varnelę viršutiniame kairiajame kampe.</span><span class="sxs-lookup"><span data-stu-id="a3252-144">To select all or most of the projects, select the check mark in the top upper-left corner.</span></span> <span data-ttu-id="a3252-145">Jei kurio nors projekto apdoroti nenorite, pašalinkite jo varnelę.</span><span class="sxs-lookup"><span data-stu-id="a3252-145">To exclude processing any project, clear the check mark for that project.</span></span>

9. <span data-ttu-id="a3252-146">Jei norite perkelti likusias pasirinktų projektų biudžetų sumas į pasirinktus finansinius metus ir sukurti biudžeto registro duomenis didžiojoje knygoje, pažymėkite **Apdoroti**.</span><span class="sxs-lookup"><span data-stu-id="a3252-146">To transfer the remaining budget amounts for the selected projects to the selected fiscal year and create budget register details in the general ledger, select **Process**.</span></span>

## <a name="carry-forward-budget-amounts-without-creating-general-ledger-transactions"></a><span data-ttu-id="a3252-147">Biudžeto sumų perkėlimas nekuriant didžiosios knygos operacijų</span><span class="sxs-lookup"><span data-stu-id="a3252-147">Carry forward budget amounts without creating general ledger transactions</span></span>

1. <span data-ttu-id="a3252-148">Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Biudžetai** > **Perkelti biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="a3252-148">Go to **Project management and accounting** > **Periodic** > **Budgets** > **Carry forward budgets**.</span></span>
2. <span data-ttu-id="a3252-149">Puslapio **Projekto biudžeto perkėlimo procesas** lauke **Metų pabaigos parinktys** pasirinkite **Perkelti likusias projekto biudžeto sumas**.</span><span class="sxs-lookup"><span data-stu-id="a3252-149">On the **Project budget carry-forward process** page, in the **Year-end options** field, select **Carry forward remaining project budget amounts**.</span></span>
3. <span data-ttu-id="a3252-150">Grupės **Parametrai** lauke **Projekto biudžeto metai** pasirinkite finansinius metus, kurių likusias biudžeto sumas norite peržiūrėti.</span><span class="sxs-lookup"><span data-stu-id="a3252-150">In the **Parameters** group, in the **Project budget year** field, select the fiscal year for which you want to view the remaining budget amounts.</span></span>
4. <span data-ttu-id="a3252-151">Grupėje **Kopijuoti iš / į** pateikite nurodytą informaciją:</span><span class="sxs-lookup"><span data-stu-id="a3252-151">In the **Copy from/to** group, provide the following information:</span></span>

   - <span data-ttu-id="a3252-152">Lauke **Iš prognozės modelio** pasirinkite projekto biudžeto prognozės modelį, susietą su likusiomis projektų biudžetų sumomis, kurias norite perkelti.</span><span class="sxs-lookup"><span data-stu-id="a3252-152">In the **From forecast model** field, select the project budget forecast model that is associated with the remaining budget amounts that you want to transfer for the projects.</span></span> 
   - <span data-ttu-id="a3252-153">Pasirinkite **Rodyti nulinį likutį**, jei norite įtraukti projektus, neturinčius likusių biudžeto sumų, bet atitinkančius kitus jūsų pasirinktus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="a3252-153">Select **Show zero remaining** to include projects that have no remaining budget amounts, but that meet the other criteria you selected.</span></span>
   - <span data-ttu-id="a3252-154">Grupėje **Pasirinkti biudžetus** pasirinkite **Nuskaityti visus biudžetus** norėdami įkelti visus biudžetus, kurie atitinka jūsų pasirinktus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="a3252-154">In the **Select Budgets** group, select **Retrieve all budgets** to load all budgets that match the criteria that you selected.</span></span> <span data-ttu-id="a3252-155">Norėdami sukurti duomenų bazės užklausą, kuri į sritį įkelia tam tikrą projektų biudžetų rinkinį, pasirinkite **Nuskaityti pasirinktus biudžetus**.</span><span class="sxs-lookup"><span data-stu-id="a3252-155">To design a database query that loads a specific set of project budgets into the pane, select **Retrieve selected budgets**.</span></span>

5. <span data-ttu-id="a3252-156">Pasirinkite kiekvieno projekto, kurį norite apdoroti, parinktį, esančią projekto eilutės pradžioje.</span><span class="sxs-lookup"><span data-stu-id="a3252-156">For each project that you want to process, select the option at the beginning of the line for the project.</span></span> 
6. <span data-ttu-id="a3252-157">Pasirinkite **Apdoroti**, jei norite perkelti likusias pasirinktų projektų biudžetų sumas į pasirinktus finansinius metus.</span><span class="sxs-lookup"><span data-stu-id="a3252-157">Select **Process** to transfer the remaining budget amounts for the selected projects to the selected fiscal year.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]