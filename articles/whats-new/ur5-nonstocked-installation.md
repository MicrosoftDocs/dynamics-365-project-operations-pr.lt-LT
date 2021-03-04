---
title: „Project Operations“ naujinimas „Finance“ aplinkoje
description: Šioje temoje pateikiama informacija apie tai, kaip atnaujinti „Project Operations” „Dynamics 365 Finance“ aplinkoje.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816635"
---
# <a name="update-project-operations-in-your-finance-environment"></a><span data-ttu-id="df4a8-103">„Project Operations“ naujinimas „Finance“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="df4a8-103">Update Project Operations in your Finance environment</span></span>

<span data-ttu-id="df4a8-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="df4a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="df4a8-105">Šioje temoje pateikiama informacija apie tai, kaip atnaujinti „Dynamics 365 Project Operations“ „Dynamics 365 Finance“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="df4a8-105">This topic provides information about how to update Dynamics 365 Project Operations in your Dynamics 365 Finance environment.</span></span> <span data-ttu-id="df4a8-106">Yra trys procedūros, kurių reikia norint atnaujinti „Project Operations“ į 5 naujinimą (UR5):</span><span class="sxs-lookup"><span data-stu-id="df4a8-106">There are three procedures that are required to update Project Operations to Update 5 (UR5):</span></span>

- [<span data-ttu-id="df4a8-107">Importuokite paketą į savo peržiūros projektą</span><span class="sxs-lookup"><span data-stu-id="df4a8-107">Import the package into your preview project</span></span>](#import)
- [<span data-ttu-id="df4a8-108">Taikykite naujinimą</span><span class="sxs-lookup"><span data-stu-id="df4a8-108">Apply the update</span></span>](#apply)
- [<span data-ttu-id="df4a8-109">Atnaujinkite „Dataverse“ aplinką</span><span class="sxs-lookup"><span data-stu-id="df4a8-109">Update your Dataverse environment</span></span>](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a><span data-ttu-id="df4a8-110">Importuokite paketą į savo LCS projektą</span><span class="sxs-lookup"><span data-stu-id="df4a8-110">Import the package into your LCS project</span></span>

1. <span data-ttu-id="df4a8-111">Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/) kaip projekto savininkas arba aplinkos vadovas.</span><span class="sxs-lookup"><span data-stu-id="df4a8-111">Sign in to [Lifecycle Services (LCS)](https://lcs.dynamics.com/) as a Project Owner or Environment manager.</span></span>
2. <span data-ttu-id="df4a8-112">Projektų sąraše pažymėkite savo LCS projektą.</span><span class="sxs-lookup"><span data-stu-id="df4a8-112">From the list of projects, select your LCS project.</span></span>
3. <span data-ttu-id="df4a8-113">Puslapyje **Projektas**, grupėje **Aplinka** atidarykite norimą naujinti aplinką.</span><span class="sxs-lookup"><span data-stu-id="df4a8-113">On the **Project** page, in the **Environments** group, open the environment that you want to update.</span></span>
4. <span data-ttu-id="df4a8-114">Patikrinkite, ar veikia aplinka.</span><span class="sxs-lookup"><span data-stu-id="df4a8-114">Verify that the environment is running.</span></span> <span data-ttu-id="df4a8-115">Jei ji nevykdoma, paleiskite aplinką.</span><span class="sxs-lookup"><span data-stu-id="df4a8-115">If it isn't started, start the environment.</span></span>
5. <span data-ttu-id="df4a8-116">Dalies **Galimi naujinimai** skyriuje **Naujas leidimas** pasirinkite **Peržiūrėti naujinimą**, skirtą 10.0.15.</span><span class="sxs-lookup"><span data-stu-id="df4a8-116">In the **New release** section under **Available updates**, select **View update** for 10.0.15.</span></span>

![Naujinimo peržiūros mygtukas](media/view-update.png)

6. <span data-ttu-id="df4a8-118">Puslapyje **Dvejetainiai naujinimai** pasirinkite **Įrašyti paketą**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-118">On the **Binary updates** page, select **Save package**.</span></span>
7. <span data-ttu-id="df4a8-119">Puslapyje **Peržiūrėti ir įrašyti naujinimus** pasirinkite **Įrašyti paketą**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-119">On the **Review and save updates** page, select **Save package**.</span></span>
8. <span data-ttu-id="df4a8-120">Atidaromoje srityje **Įrašyti paketą į turto biblioteką** įveskite paketo pavadinimą, o tada pasirinkite **Įrašyti paketą**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-120">On the **Save package to asset library** pane that opens, enter the package name and then select **Save package**.</span></span>
9. <span data-ttu-id="df4a8-121">Kai LCS baigia įrašyti paketą, įjungiamas mygtukas **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-121">When LCS has finished saving the package, the **Done** button is enabled.</span></span> <span data-ttu-id="df4a8-122">Pasirinkite **Atlikta**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-122">Select **Done**.</span></span> <span data-ttu-id="df4a8-123">LCS patikrins paketą.</span><span class="sxs-lookup"><span data-stu-id="df4a8-123">LCS will verify the package.</span></span> <span data-ttu-id="df4a8-124">Tikrinimas gali užtrukti kelias minutes arba iki vienos valandos.</span><span class="sxs-lookup"><span data-stu-id="df4a8-124">Verification can take a few minutes or up to one hour.</span></span>


## <a name="apply-the-package-update"></a><a name="apply"></a><span data-ttu-id="df4a8-125">Taikykite paketo naujinimą</span><span class="sxs-lookup"><span data-stu-id="df4a8-125">Apply the package update</span></span>

1. <span data-ttu-id="df4a8-126">LCS programos puslapyje **Išsami aplinkos informacija** pasirinkite **Prižiūrėti** > **Taikyti naujinimus**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-126">In LCS, on the **Environment details** page, select **Maintain** > **Apply Updates**.</span></span>
2. <span data-ttu-id="df4a8-127">Sąraše pažymėkite anksčiau įrašytą paketą, o tada pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-127">From the list, select the package that you saved earlier, and then select **Apply**.</span></span>
3. <span data-ttu-id="df4a8-128">Pasirinkite **Taip**, kad patvirtintumėte, jog norite visuotinai įdiegti paketą.</span><span class="sxs-lookup"><span data-stu-id="df4a8-128">Select **Yes** to confirm that you want to deploy the package.</span></span>

![Paketo visuotinio diegimo dialogo lango patvirtinimas](media/confirm-package-deployment.png)

4. <span data-ttu-id="df4a8-130">Pasirinkite **Taip**, kad patvirtintumėte, jog norite atnaujinti programą.</span><span class="sxs-lookup"><span data-stu-id="df4a8-130">Select **Yes** to confirm that you want to update the application.</span></span>

![Programos naujinimo dialogo lango patvirtinimas](media/confirm-application-update.png)

<span data-ttu-id="df4a8-132">Bus pradėta diegti ir naujinti programą.</span><span class="sxs-lookup"><span data-stu-id="df4a8-132">The deployment and application update will start.</span></span> 

<span data-ttu-id="df4a8-133">Puslapyje **Išsami aplinkos informacija**, viršutiniame dešiniajame kampe, aplinkos būsena bus atnaujinta į **Aptarnavimas**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-133">On the **Environment details** page, in the top-right corner, the environment status will update to **Servicing**.</span></span> <span data-ttu-id="df4a8-134">Po maždaug dviejų valandų naujinimas bus baigtas.</span><span class="sxs-lookup"><span data-stu-id="df4a8-134">In approximately two hours, the update will be complete.</span></span> <span data-ttu-id="df4a8-135">Programos leidimo informacija bus atnaujinta į **„Microsoft Dynamics 365 for Finance and Operations“ 10.0.15)**, o aplinkos būsena bus atnaujina į **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-135">The application release information will update to **Microsoft Dynamics 365 for Finance and Operations 10.0.15)** and the environment status will update to **Deployed**.</span></span>


## <a name="update-your-dataverse-environment"></a><a name="update"></a><span data-ttu-id="df4a8-136">Atnaujinkite „Dataverse“ aplinką</span><span class="sxs-lookup"><span data-stu-id="df4a8-136">Update your Dataverse environment</span></span>

1. <span data-ttu-id="df4a8-137">Prisijunkite prie [„Power Platform“ administravimo centro](https://admin.powerplatform.com/).</span><span class="sxs-lookup"><span data-stu-id="df4a8-137">Sign in to the [Power Platform admin center](https://admin.powerplatform.com/).</span></span>
2. <span data-ttu-id="df4a8-138">Sąraše raskite ir atidarykite aplinką, kurią naudojote diegdami „Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="df4a8-138">In the list, find and open the environment that you used to install Project Operations.</span></span>
3. <span data-ttu-id="df4a8-139">Puslapyje **Aplinkos** pažymėkite **Išteklius** > **„Dynamics 365“ programos**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-139">On the **Environments** page, select **Resource** > **Dynamics 365 apps**.</span></span>
4. <span data-ttu-id="df4a8-140">Sąraše raskite **„Microsoft Dynamics 365 Project Operations“** ir stulpelyje **Būsena** pasirinkite **Galimas naujinimas**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-140">In the list, locate **Microsoft Dynamics 365 Project Operations**, and in the **Status** column, select **Update Available**.</span></span>
5. <span data-ttu-id="df4a8-141">Pažymėkite žymės langelį **Sutinku su aptarnavimo sąlygomis**, o tada pažymėkite **Atnaujinti**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-141">Select the **I agree to the terms of service** check box, and then select **Update**.</span></span> <span data-ttu-id="df4a8-142">Bus įdiegta naujausia sprendimo versija.</span><span class="sxs-lookup"><span data-stu-id="df4a8-142">The latest version of the solution will be installed.</span></span>

<span data-ttu-id="df4a8-143">Baigę diegti turėsite įdiegtą 4.5.0.134 versiją.</span><span class="sxs-lookup"><span data-stu-id="df4a8-143">After the installation is complete, you'll have version 4.5.0.134 installed.</span></span>

## <a name="configure-new-features"></a><span data-ttu-id="df4a8-144">Naujų funkcijų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="df4a8-144">Configure new features</span></span>

### <a name="enable-dual-write-mapping"></a><span data-ttu-id="df4a8-145">Dvigubo rašymo susiejimo įgalinimas</span><span class="sxs-lookup"><span data-stu-id="df4a8-145">Enable dual-write mapping</span></span>

<span data-ttu-id="df4a8-146">Baigę naujinti „Finance“ ir „Dataverse“ aplinkas, galite įjungti reikiamus dvigubo rašymo susiejimus.</span><span class="sxs-lookup"><span data-stu-id="df4a8-146">After you complete the update on the Finance and Dataverse environments, you can enable the required dual-write mappings.</span></span> <span data-ttu-id="df4a8-147">Norėdami įgalinti dvigubo rašymo susiejimus, atlikite toliau nurodytas procedūras.</span><span class="sxs-lookup"><span data-stu-id="df4a8-147">Complete the following procedures to enable dual-write mappings.</span></span>

- [<span data-ttu-id="df4a8-148">„Customer Engagement“ aplinkos saugos parametrų naujinimas</span><span class="sxs-lookup"><span data-stu-id="df4a8-148">Update security settings on Customer Engagement environment</span></span>](#security)
- [<span data-ttu-id="df4a8-149">Duomenų objektų atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="df4a8-149">Refresh data entities</span></span>](#refresh)
- [<span data-ttu-id="df4a8-150">Dvigubo rašymo susiejimų atnaujinimas ir paleidimas</span><span class="sxs-lookup"><span data-stu-id="df4a8-150">Update and run the dual-write mappings</span></span>](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a><span data-ttu-id="df4a8-151">Atnaujinkite „Dataverse“ aplinkos saugos parametrus</span><span class="sxs-lookup"><span data-stu-id="df4a8-151">Update security settings on the Dataverse environment</span></span>

<span data-ttu-id="df4a8-152">Toliau nurodyti objektų saugos teisių naujinimai būtini kaip UR5 naujinimo dalis.</span><span class="sxs-lookup"><span data-stu-id="df4a8-152">The following updates to the security privileges for entities are required as part of the update to UR5.</span></span>

1. <span data-ttu-id="df4a8-153">Savo „Dataverse“ aplinkoje eikite į **Parametrai**, o grupėje **Sistema** pasirinkite **Sauga**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-153">In your Dataverse environment, go to **Settings**, and in the **System** group, select **Security**.</span></span>

![„Dataverse“ aplinkos nustatymai](media/Picture21.png)

2. <span data-ttu-id="df4a8-155">Pasirinkite **Saugos vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-155">Select **Security Roles**.</span></span>
3. <span data-ttu-id="df4a8-156">Vaidmenų sąraše pasirinkite **dvigubo rašymo programos vartotoją** ir pasirinkite skirtuką **Tinkinti objektai**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-156">From the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span> 
4. <span data-ttu-id="df4a8-157">Patikrinkite, ar vaidmuo turi **Skaityti** ir **Pridėti prie** teises, skirtas:</span><span class="sxs-lookup"><span data-stu-id="df4a8-157">Verify that the role has **Read** and **Append To** permissions for:</span></span>

      - <span data-ttu-id="df4a8-158">**Valiutos kurso tipas**</span><span class="sxs-lookup"><span data-stu-id="df4a8-158">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="df4a8-159">**Sąskaitų diagrama**</span><span class="sxs-lookup"><span data-stu-id="df4a8-159">**Chart Of Accounts**</span></span> 
      - <span data-ttu-id="df4a8-160">**Finansinis kalendorius**</span><span class="sxs-lookup"><span data-stu-id="df4a8-160">**Fiscal Calendar**</span></span> 
      - <span data-ttu-id="df4a8-161">**Didžioji knyga**</span><span class="sxs-lookup"><span data-stu-id="df4a8-161">**Ledger**</span></span>

5. <span data-ttu-id="df4a8-162">Atnaujinus saugos vaidmenį, eikite į **Parametrai** > **Sauga** > **Komandos**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-162">After the security role is updated, go to **Settings** > **Security** > **Teams**.</span></span> <span data-ttu-id="df4a8-163">Patikrinkite, ar komandai buvo pritaikytas **dvigubo rašymo programos vartotojo** vaidmuo.</span><span class="sxs-lookup"><span data-stu-id="df4a8-163">Verify that the **dual-write app user** role has been applied to the team.</span></span> 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a><span data-ttu-id="df4a8-164">Atnaujinkite duomenų objektus iš naujinimo</span><span class="sxs-lookup"><span data-stu-id="df4a8-164">Refresh data entities from the update</span></span>

1. <span data-ttu-id="df4a8-165">Savo „Finance“ aplinkoje atidarykite darbo sritį **Duomenų valdymas**, o tada atidarykite puslapį **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-165">In your Finance environment, open the **Data management** workspace, and then open the **Framework parameters** page.</span></span>
2. <span data-ttu-id="df4a8-166">Skirtuke **Objekto parametrai** pasirinkite **Atnaujinti objektų sąrašą**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-166">On the **Entity settings** tab, select **Refresh entity list**.</span></span>
3. <span data-ttu-id="df4a8-167">Pažymėkite **Uždaryti**, kad patvirtintumėte objekto atnaujinimą.</span><span class="sxs-lookup"><span data-stu-id="df4a8-167">Select **Close** to confirm the entity refresh.</span></span>

 > [!NOTE]
 > <span data-ttu-id="df4a8-168">Tai užtruks maždaug 20 minučių.</span><span class="sxs-lookup"><span data-stu-id="df4a8-168">This process will take approximately 20 minutes to complete.</span></span> <span data-ttu-id="df4a8-169">Jums bus pranešta, kai bus baigtas naujinimas.</span><span class="sxs-lookup"><span data-stu-id="df4a8-169">You will be notified when the refresh is complete.</span></span>

### <a name="update-dual-write-mappings"></a><a name="run"></a><span data-ttu-id="df4a8-170">Atnaujinkite dvigubo rašymo susiejimus</span><span class="sxs-lookup"><span data-stu-id="df4a8-170">Update dual-write mappings</span></span>

1. <span data-ttu-id="df4a8-171">Darbo srityje **Duomenų valdymas** pasirinkite **Dvigubas rašymas**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-171">In the **Data management** workspace, select **Dual-write**.</span></span>
2. <span data-ttu-id="df4a8-172">Pažymėkite **Taikyti sprendimus**, pasirinkite abu sprendimus, o tada pažymėkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-172">Select **Apply solutions**, select both solutions in the list, and then select **Apply**.</span></span>
3. <span data-ttu-id="df4a8-173">Puslapyje **Dvigubas rašymas** pažymėkite toliau nurodytas lentelių struktūras, o tada pasirinkite **Sustabdyti**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-173">On the **Dual-write** page, select the following table maps, and then select **Stop**.</span></span>

    - <span data-ttu-id="df4a8-174">**„Project Operations“ integravimo faktiniai duomenys (msdyn_actuals)**</span><span class="sxs-lookup"><span data-stu-id="df4a8-174">**Project Operations integration actuals (msdyn_actuals)**</span></span>
    - <span data-ttu-id="df4a8-175">**„Project Operations“ integravimo projekto išlaidų kategorijos (msdyn_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="df4a8-175">**Project Operations integration project expense categories (msdyn_expensecategories)**</span></span>
    - <span data-ttu-id="df4a8-176">**„Project Operations“ integravimo faktinių duomenų projekto išlaidų eksportavimo objektas (msdyn_expenses)**</span><span class="sxs-lookup"><span data-stu-id="df4a8-176">**Project Operations integration actuals project expenses export entity (msdyn_expenses)**</span></span>

4. <span data-ttu-id="df4a8-177">Puslapyje **Lentelės struktūros versija** taikykite naują struktūros versiją kiekvienam iš trijų objektų.</span><span class="sxs-lookup"><span data-stu-id="df4a8-177">On the **Table map version** page, apply a new version of the map to each of the three entities.</span></span>
5. <span data-ttu-id="df4a8-178">Puslapyje **Dvigubas rašymas** pasirinkite vykdyti ir iš naujo paleisti struktūras.</span><span class="sxs-lookup"><span data-stu-id="df4a8-178">On the **Dual-write** page, select run to restart the maps.</span></span>
6. <span data-ttu-id="df4a8-179">Struktūrų sąraše pažymėkite **Didžioji knyga (msdyn_ledgers)** struktūrą su visomis būtinosiomis sąlygomis ir pasirinkite žymės langelį **Pradinis sinchronizavimas**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-179">From the list of maps, select the **Ledger (msdyn_ledgers)** map with all prerequisites and select the **Initial sync** check box.</span></span> 
7. <span data-ttu-id="df4a8-180">Lauke **Pradinio sinchronizavimo šablonas** pasirinkite **„Finance and Operations“ programos**, o tada pasirinkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="df4a8-180">In the **Master for initial sync** field, select **Finance and Operations apps** and then select **Run**.</span></span>
 
 ![Didžiosios knygos struktūros sinchronizavimas](media/DW6.png)
 
