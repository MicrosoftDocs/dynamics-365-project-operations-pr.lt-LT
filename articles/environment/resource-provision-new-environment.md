---
title: Naujos aplinkos parengimas
description: Šioje temoje pateikiama informacija, kaip parengti naują „Project Operations“ aplinką.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727800"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="ecbda-103">Naujos aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="ecbda-103">Provision a new environment</span></span>

<span data-ttu-id="ecbda-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="ecbda-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="ecbda-105">Šioje temoje pateikiama informacijos, kaip sukonfigūruoti naują „Dynamics 365 Project Operations“ aplinką, skirtą ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="ecbda-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="ecbda-106">Automatinio „Project Operations“ parengimo įjungimas LCS projekte</span><span class="sxs-lookup"><span data-stu-id="ecbda-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="ecbda-107">Atlikite toliau nurodytus veiksmus, kad įjungtumėte automatinį „Project Operations“ parengimą LCS projekte.</span><span class="sxs-lookup"><span data-stu-id="ecbda-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="ecbda-108">Eikite į [LCS](https://lcs.dynamics.com/v2) ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="ecbda-109">Sąraše **Peržiūros versijos funkcija** pasirinkite **„Project Operations“ funkcija**, tada pasirinkite **Peržiūros versijos funkcija įjungta**, kad įjungtumėte „Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="ecbda-109">In the **Preview feature** list, select **Project Operations Feature**, and then select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="ecbda-110">Šį veiksmą reikia atlikti tik vieną kartą LCS projekte.</span><span class="sxs-lookup"><span data-stu-id="ecbda-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="ecbda-111">„Project Operations“ aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="ecbda-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="ecbda-112">Atidarykite naują „Dynamics 365 Finance“ [demonstracinės aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) arba [smėlio dėžės / gamybos aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) visuotinio diegimo paketą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="ecbda-113">Atlikite vediklio **Aplinkos parengimas** veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ecbda-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="ecbda-114">Įsitikinkite, kad naudojama 10.0.13 arba naujesnė programos versija.</span><span class="sxs-lookup"><span data-stu-id="ecbda-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="ecbda-115">Norėdami parengti „Project Operations“, dalyje **Išplėstiniai parametrai** pasirinkite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="ecbda-116">Įjunkite parametrą **„Common Data Service“ parametras** pasirinkdami **Taip** ir įveskite informaciją privalomuose laukuose:</span><span class="sxs-lookup"><span data-stu-id="ecbda-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="ecbda-117">Pavadinimas / vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="ecbda-117">Name</span></span>
  - <span data-ttu-id="ecbda-118">Regiono ID</span><span class="sxs-lookup"><span data-stu-id="ecbda-118">Region</span></span>
  - <span data-ttu-id="ecbda-119">Kalba</span><span class="sxs-lookup"><span data-stu-id="ecbda-119">Language</span></span>
  - <span data-ttu-id="ecbda-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="ecbda-120">Currency</span></span>
 
5. <span data-ttu-id="ecbda-121">Lauke **„Common Data Service“ šablonas** pasirinkite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="ecbda-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="ecbda-122">Pasirinkite visuotinio diegimo aplinkos tipą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="ecbda-123">Jei naudojate prenumeruojamą bandomąją versiją, CDS aplinka galės būti įdiegta 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="ecbda-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Visuotinio diegimo parametrai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="ecbda-125">Pasirinkite **Sutinku**, kad sutiktumėte su paslaugos teikimo sąlygomis, tada pasirinkite **Atlikta**, kad grįžtumėte į visuotinio diegimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="ecbda-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Visuotinio diegimo sutikimas](./media/2DeploymentConsent.png)

7. <span data-ttu-id="ecbda-127">Pasirinktinai – aplinkai taikykite demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="ecbda-127">Optional - Apply demo data to the environment.</span></span> <span data-ttu-id="ecbda-128">Eikite į **Išplėstiniai parametrai**, pasirinkite **Tinkinti SQL duomenų bazės konfigūraciją** ir nustatykite parinktį **Nurodykite programos duomenų bazės duomenų rinkinį** į **Demonstracinis**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-128">Go to **Advanced settings**, select **Customize SQL Database Configuration**, and set **Specify a dataset for Application database** to **Demo**.</span></span>

8. <span data-ttu-id="ecbda-129">Užpildykite likusius būtinus vediklio laukus ir patvirtinkite visuotinį diegimą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-129">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="ecbda-130">Aplinkos rengimo laikas skiriasi atsižvelgiant į aplinkos tipą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-130">The time to provision the environment varies based on the environment type.</span></span> <span data-ttu-id="ecbda-131">Parengimo procesas gali užtrukti iki šešių valandų.</span><span class="sxs-lookup"><span data-stu-id="ecbda-131">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="ecbda-132">Sėkmingai užbaigus visuotinį diegimą, bus rodoma aplinkos būsena **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-132">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

9. <span data-ttu-id="ecbda-133">Jei norite patvirtinti, kad aplinka sėkmingai įdiegta, pasirinkite **Prisijungti** ir prissijungę prie aplinkos patvirtinkite.</span><span class="sxs-lookup"><span data-stu-id="ecbda-133">To confirm that the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Išsami „“ aplinkos informacija](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="ecbda-135">Naujinimų taikymas „Finance“ aplinkai</span><span class="sxs-lookup"><span data-stu-id="ecbda-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="ecbda-136">„Project Operations“ reikalinga „Finance“ aplinka su **10.0.13 (10.0.569.20009)** arba naujesnės versijos programa.</span><span class="sxs-lookup"><span data-stu-id="ecbda-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="ecbda-137">Kad galėtumėte gauti šią versiją, gali reikėti „Finance“ aplinkai taikyti kokybinius naujinimus.</span><span class="sxs-lookup"><span data-stu-id="ecbda-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="ecbda-138">LCS puslapio **Išsami aplinkos informacija** skyriuje **Pasiekimai naujiniai** pasirinkite **Peržiūrėti naujinį**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Peržiūrėti naujinius](./media/5ViewUpdates.png)

2. <span data-ttu-id="ecbda-140">Puslapyje **Dvejetainiai naujinimai** pasirinkite **Įrašyti paketą**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-140">On the **Binary updates** page, select **Save package.**</span></span>

![Įrašyti paketą](./media/6SavePackage.png)

3. <span data-ttu-id="ecbda-142">Spustelėkite **Pasirinkti viską** ir pasirinkite **Įrašyti paketą**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-142">Click **Select all** and then select **Save package**.</span></span>

![Peržiūrėti ir įrašyti naujinius](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="ecbda-144">Įveskite paketo pavadinimą ir aprašą, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="ecbda-145">Atsižvelgiant į interneto ryšį, šis procesas gali šiek tiek užtrukti.</span><span class="sxs-lookup"><span data-stu-id="ecbda-145">Depending on the internet connection, this process might take some time.</span></span>

![Paketo nusiuntimas į išteklių biblioteką](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="ecbda-147">Įrašę paketą pasirinkite **Atlikta** ir įrašykite šį paketą LCS projekto išteklių bibliotekoje.</span><span class="sxs-lookup"><span data-stu-id="ecbda-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="ecbda-148">Paketo įrašymo ir tikrinimo procesas gali užtrukti maždaug 15 minučių.</span><span class="sxs-lookup"><span data-stu-id="ecbda-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="ecbda-149">Norėdami taikyti naujinį, eikite į LCS puslapį **Išsami aplinkos informacija** ir pasirinkite **Tvarkyti** > **Taikyti naujinius**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Aplinkų tvarkymas](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="ecbda-151">Naujinių sąraše pasirinkite sukurtą paketą ir pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Naujinių taikymas](./media/10ApplyUpdates.png)

<span data-ttu-id="ecbda-153">Aplinkos paruošimas gali šiek tiek užtrukti.</span><span class="sxs-lookup"><span data-stu-id="ecbda-153">Environment servicing will take some time.</span></span> <span data-ttu-id="ecbda-154">Baigus vėl bus nustatyta aplinkos būsena Įdiegta.</span><span class="sxs-lookup"><span data-stu-id="ecbda-154">After it is complete, the environment will return to a deployed state.</span></span>

![Aplinka įdiegta](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="ecbda-156">Dvigubo rašymo ryšio nustatymas</span><span class="sxs-lookup"><span data-stu-id="ecbda-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="ecbda-157">LCS projekte eikite į puslapį **Išsami aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="ecbda-158">Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="ecbda-159">Susiejus dar kartą pasirinkite **Susieti su CDS programoms**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="ecbda-160">Būsite nukreipti į dvigubo rašymo sistemą modulyje „Finance“.</span><span class="sxs-lookup"><span data-stu-id="ecbda-160">You will be redirected to Dual Write in Finance.</span></span>

![Susiejimas su CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="ecbda-162">Pasirinkite **Taikyti sprendimą**, kad pasiektumėte objektus, kurie bus susieti atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Taikyti sprendimus](./media/13ApplySolutions.png)

5. <span data-ttu-id="ecbda-164">Pasirinkite abu sprendimus **Dynamics 365 Finance and Operations“ dvigubo rašymo objektų schema** ir **„Dynamics 365 Project Operations“ dvigubo rašymo objektų schemos**, tada pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Sprendimų patvirtinimas](./media/14ConfirmSolutions.png)

<span data-ttu-id="ecbda-166">Pritaikius sprendimus, į aplinką įtraukiami dvigubo rašymo objektai.</span><span class="sxs-lookup"><span data-stu-id="ecbda-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Sprendimų taikymas](./media/15ApplyingSolutions.png)

<span data-ttu-id="ecbda-168">Pritaikius objektus visi galimi susiejimai pateikiami aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ecbda-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Dvigubo rašymo schemos](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="ecbda-170">Duomenų objektų atnaujinimas atlikus naujinimą</span><span class="sxs-lookup"><span data-stu-id="ecbda-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="ecbda-171">Modulyje „Finance“ eikite į darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-171">In Finance, go to the **Data management** workspace.</span></span>

![Duomenų valdymo darbo sritis](./media/16DataManagement.png)

2. <span data-ttu-id="ecbda-173">Pasirinkite plytelę **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-173">Select the **Framework parameters** tile.</span></span>

![Sistemos parametrai](./media/17FrameworkParameters.png)

3. <span data-ttu-id="ecbda-175">Puslapyje **Objektų parametrai** pasirinkite **Atnaujinti objektų sąrašą**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Objektų sąrašo atnaujinimas](./media/18RefreshEntityList.png)

<span data-ttu-id="ecbda-177">Atnaujinimas truks apie 20 minučių.</span><span class="sxs-lookup"><span data-stu-id="ecbda-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="ecbda-178">Kai jis bus baigtas, gausite įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-178">You will receive an alert when it is complete.</span></span>

![Patvirtinimo atnaujinimas](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a><span data-ttu-id="ecbda-180">„Project Operations“ saugos parametrų naujinimas „Dataverse“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="ecbda-180">Update security settings on Project Operations on Dataverse</span></span>

1. <span data-ttu-id="ecbda-181">Eikite į „Project Operations“ „Dataverse“ aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="ecbda-181">Go to Project Operations on your Dataverse environment.</span></span> 
2. <span data-ttu-id="ecbda-182">Eikite į **Parametrai** > **Sauga** > **Saugos vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-182">Go to **Settings** > **Security** > **Security roles**.</span></span> 
3. <span data-ttu-id="ecbda-183">Puslapio **Saugos vaidmenys** vaidmenų sąraše pasirinkite **dvigubo rašymo programos vartotoją** ir pasirinkite skirtuką **Tinkinti objektai**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-183">On the **Security roles** page, in the list of roles, select **dual-write app user** and select the **Custom Entities** tab.</span></span>  
4. <span data-ttu-id="ecbda-184">Patikrinkite, ar vaidmuo turi **Skaityti** ir **Pridėti prie** teises, skirtas:</span><span class="sxs-lookup"><span data-stu-id="ecbda-184">Verify that the role has **Read** and **Append To** permissions for the:</span></span>
      
      - <span data-ttu-id="ecbda-185">**Valiutos kurso tipas**</span><span class="sxs-lookup"><span data-stu-id="ecbda-185">**Currency Exchange Rate Type**</span></span>
      - <span data-ttu-id="ecbda-186">**Sąskaitų diagrama**</span><span class="sxs-lookup"><span data-stu-id="ecbda-186">**Chart Of Accounts**</span></span>
      - <span data-ttu-id="ecbda-187">**Finansinis kalendorius**</span><span class="sxs-lookup"><span data-stu-id="ecbda-187">**Fiscal Calendar**</span></span>
      - <span data-ttu-id="ecbda-188">**Didžioji knyga**</span><span class="sxs-lookup"><span data-stu-id="ecbda-188">**Ledger**</span></span>

5. <span data-ttu-id="ecbda-189">Atnaujinus saugos vaidmenį, eikite į **Parametrai** > **Sauga** > **Komandos** ir komandos rodinyje **Vietinės įmonės savininkas** pasirinkite numatytąją komandą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-189">After the security role is updated, go to **Settings** > **Security** > **Teams**, and select the default team in the **Local Business Owner** team view.</span></span>
6. <span data-ttu-id="ecbda-190">Pasirinkite **Tvarkyti vaidmenis** ir patikrinkite, ar šiai komandai taikoma **dvigubo rašymo programos vartotojo** saugos teisė.</span><span class="sxs-lookup"><span data-stu-id="ecbda-190">Select **Manage Roles** and verify that the **dual-write app user** security privilege is applied to this team.</span></span>

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="ecbda-191">„Project Operations“ dvigubo rašymo schemų vykdymas</span><span class="sxs-lookup"><span data-stu-id="ecbda-191">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="ecbda-192">LCS projekte eikite į puslapį **Išsami aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-192">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="ecbda-193">Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-193">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="ecbda-194">Pasirinkus saitą būsite nukreipti į susiejimų objektų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-194">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="ecbda-195">Paleiskite schemas, kaip aprašyta toliau esančioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="ecbda-195">Start the maps as described in the following table.</span></span> <span data-ttu-id="ecbda-196">Būtinai viską darykite iš eilės, kaip nurodyta.</span><span class="sxs-lookup"><span data-stu-id="ecbda-196">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="ecbda-197">**Objekto schema**</span><span class="sxs-lookup"><span data-stu-id="ecbda-197">**Entity Map**</span></span> | <span data-ttu-id="ecbda-198">**Atnaujinti objektą**</span><span class="sxs-lookup"><span data-stu-id="ecbda-198">**Refresh entity**</span></span> | <span data-ttu-id="ecbda-199">**Pradinis sinchronizavimas**</span><span class="sxs-lookup"><span data-stu-id="ecbda-199">**Initial sync**</span></span> | <span data-ttu-id="ecbda-200">**Pradinio sinchronizavimo šablonas**</span><span class="sxs-lookup"><span data-stu-id="ecbda-200">**Master for initial sync**</span></span> | <span data-ttu-id="ecbda-201">**Vykdymo būtinosios sąlygos**</span><span class="sxs-lookup"><span data-stu-id="ecbda-201">**Run prerequisites**</span></span> | <span data-ttu-id="ecbda-202">**Būtinas pradinis sinchronizavimas**</span><span class="sxs-lookup"><span data-stu-id="ecbda-202">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="ecbda-203">**Projekto išteklių vaidmenys visoms įmonėms (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-203">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="ecbda-204">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-204">No</span></span> | <span data-ttu-id="ecbda-205">Taip</span><span class="sxs-lookup"><span data-stu-id="ecbda-205">Yes</span></span> | <span data-ttu-id="ecbda-206">„Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="ecbda-206">Common Data Service</span></span> | <span data-ttu-id="ecbda-207">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-207">No</span></span> | <span data-ttu-id="ecbda-208">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-208">N\A</span></span> |
| <span data-ttu-id="ecbda-209">**Juridiniai subjektai (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-209">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="ecbda-210">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-210">No</span></span> | <span data-ttu-id="ecbda-211">Taip</span><span class="sxs-lookup"><span data-stu-id="ecbda-211">Yes</span></span> | <span data-ttu-id="ecbda-212">„Finance and Operations“ programos</span><span class="sxs-lookup"><span data-stu-id="ecbda-212">Finance and Operations apps</span></span> | <span data-ttu-id="ecbda-213">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-213">No</span></span> | <span data-ttu-id="ecbda-214">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-214">N\A</span></span> |
| <span data-ttu-id="ecbda-215">**Didžioji knyga (msdyn_ledgers)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-215">**Ledger (msdyn_ledgers)**</span></span> | <span data-ttu-id="ecbda-216">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-216">No</span></span> | <span data-ttu-id="ecbda-217">Taip</span><span class="sxs-lookup"><span data-stu-id="ecbda-217">Yes</span></span> | <span data-ttu-id="ecbda-218">„Finance and Operations“ programos</span><span class="sxs-lookup"><span data-stu-id="ecbda-218">Finance and Operations apps</span></span> | <span data-ttu-id="ecbda-219">Taip</span><span class="sxs-lookup"><span data-stu-id="ecbda-219">Yes</span></span> | <span data-ttu-id="ecbda-220">Taip, „Finance and Operations“ programos</span><span class="sxs-lookup"><span data-stu-id="ecbda-220">Yes, Finance and Operations apps</span></span> |
| <span data-ttu-id="ecbda-221">**„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-221">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="ecbda-222">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-222">No</span></span> | <span data-ttu-id="ecbda-223">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-223">No</span></span> | <span data-ttu-id="ecbda-224">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-224">N\A</span></span> | <span data-ttu-id="ecbda-225">Taip</span><span class="sxs-lookup"><span data-stu-id="ecbda-225">Yes</span></span> | <span data-ttu-id="ecbda-226">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-226">No</span></span> |
| <span data-ttu-id="ecbda-227">**Projekto sutarties eilutės (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-227">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="ecbda-228">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-228">No</span></span> | <span data-ttu-id="ecbda-229">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-229">No</span></span> | <span data-ttu-id="ecbda-230">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-230">N\A</span></span> | <span data-ttu-id="ecbda-231">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-231">No</span></span> | <span data-ttu-id="ecbda-232">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-232">No</span></span> |
| <span data-ttu-id="ecbda-233">**Projekto operacijų ryšių integravimo objektas (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-233">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="ecbda-234">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-234">No</span></span> | <span data-ttu-id="ecbda-235">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-235">No</span></span> | <span data-ttu-id="ecbda-236">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-236">N\A</span></span> | <span data-ttu-id="ecbda-237">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-237">No</span></span> | <span data-ttu-id="ecbda-238">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-238">N\A</span></span> |
| <span data-ttu-id="ecbda-239">**„Project Operations“ integravimo sutarties eilučių etapai (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-239">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="ecbda-240">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-240">No</span></span> | <span data-ttu-id="ecbda-241">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-241">No</span></span> | <span data-ttu-id="ecbda-242">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-242">N\A</span></span> | <span data-ttu-id="ecbda-243">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-243">No</span></span> | <span data-ttu-id="ecbda-244">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-244">N\A</span></span> |
| <span data-ttu-id="ecbda-245">**„Project Operations“ integravimo objektas, skirtas išlaidų įvertinimams (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-245">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="ecbda-246">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-246">No</span></span> | <span data-ttu-id="ecbda-247">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-247">No</span></span> | <span data-ttu-id="ecbda-248">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-248">N\A</span></span> | <span data-ttu-id="ecbda-249">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-249">No</span></span> | <span data-ttu-id="ecbda-250">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-250">N\A</span></span> |
| <span data-ttu-id="ecbda-251">**„Project Operations“ integracijos projekto išlaidų kategorijų eksportavimo objektas (msdyn\_expensecategories)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-251">**Project Operations integration project expense categories export entity (msdyn\_expensecategories)**</span></span> | <span data-ttu-id="ecbda-252">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-252">No</span></span> | <span data-ttu-id="ecbda-253">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-253">No</span></span> | <span data-ttu-id="ecbda-254">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-254">N\A</span></span> | <span data-ttu-id="ecbda-255">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-255">No</span></span> | <span data-ttu-id="ecbda-256">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-256">N\A</span></span> |
| <span data-ttu-id="ecbda-257">**„Project Operations“ integravimo projekto išlaidų eksportavimo objektas (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-257">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="ecbda-258">Taip</span><span class="sxs-lookup"><span data-stu-id="ecbda-258">Yes</span></span> | <span data-ttu-id="ecbda-259">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-259">No</span></span> | <span data-ttu-id="ecbda-260">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-260">N\A</span></span> | <span data-ttu-id="ecbda-261">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-261">No</span></span> | <span data-ttu-id="ecbda-262">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-262">N\A</span></span> |
| <span data-ttu-id="ecbda-263">**„Project Operations“ integravimo objektas, skirtas valandų įvertinimams (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="ecbda-263">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="ecbda-264">Taip</span><span class="sxs-lookup"><span data-stu-id="ecbda-264">Yes</span></span> | <span data-ttu-id="ecbda-265">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-265">No</span></span> | <span data-ttu-id="ecbda-266">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-266">N\A</span></span> | <span data-ttu-id="ecbda-267">No</span><span class="sxs-lookup"><span data-stu-id="ecbda-267">No</span></span> | <span data-ttu-id="ecbda-268">Nėra</span><span class="sxs-lookup"><span data-stu-id="ecbda-268">N\A</span></span> |


4. <span data-ttu-id="ecbda-269">Norėdami atnaujinti objektą, pasirinkite schemos pavadinimą ir pasirinkite **Atnaujinti objektus**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-269">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 


![Schemos atnaujinimas](./media/20RefreshMapping.png)

5. <span data-ttu-id="ecbda-271">Atnaujinę paleiskite schemą.</span><span class="sxs-lookup"><span data-stu-id="ecbda-271">After the refresh is complete, run the map.</span></span> <span data-ttu-id="ecbda-272">Prieš įjungdami kitą schemą patikrinkite, ar lentelėje schemos būsena yra **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-272">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="ecbda-273">Gali šiek tiek užtrukti, kol bus paleistos schemos, turinčios daug būtinųjų sąlygų.</span><span class="sxs-lookup"><span data-stu-id="ecbda-273">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="ecbda-274">Norėdami paleisti schemą su būtinosiomis sąlygomis, įjunkite perjungiklį **Rodyti susijusias objektų schemas**.</span><span class="sxs-lookup"><span data-stu-id="ecbda-274">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="ecbda-275">Jei lentelėje nurodyta **Būtinas pradinis sinchronizavimas** reikšmė **Ne**, įsitikinkite, kad žymės **Pradinis sinchronizavimas** būklė yra **Išjungta** visose būtinosiose schemose prieš ją vykdydami.</span><span class="sxs-lookup"><span data-stu-id="ecbda-275">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Schemos vykdymas](./media/21RunMap.png)

6. <span data-ttu-id="ecbda-277">Įsitikinkite, kad visos su projektu susijusios schemos yra vykdomos.</span><span class="sxs-lookup"><span data-stu-id="ecbda-277">Validate all project related maps are in the running state.</span></span>

![Visos schemos yra vykdomos](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a><span data-ttu-id="ecbda-279">Konfigūracijos duomenų taikymas CDS, skirtoje „Project Operations“ (pasirenkama)</span><span class="sxs-lookup"><span data-stu-id="ecbda-279">Apply configuration data in CDS for Project Operations (optional)</span></span>

<span data-ttu-id="ecbda-280">Jeigu pritaikėte demonstracinius duomenis „Finance“ aplinkoje, žr. [Konfigūracijos duomenų nustatymas ir taikymas „Project Operations” skirtoje „Common Data Service”](resource-apply-pro-setup-config-data.md), kad pritaikytumėte demonstracinius duomenis CDS aplinkai.</span><span class="sxs-lookup"><span data-stu-id="ecbda-280">If you have applied demo data to the Finance environment, see [Set up and apply configuration data in the Common Data Service for Project Operations](resource-apply-pro-setup-config-data.md) to apply demo data to CDS environment.</span></span>


<span data-ttu-id="ecbda-281">Jūsų „Project Operations“ aplinka dabar parengta ir sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="ecbda-281">Your Project Operations environment is now provisioned and configured.</span></span> 
