---
title: Naujos aplinkos parengimas
description: Šioje temoje pateikiama informacija, kaip parengti naują „Project Operations“ aplinką.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949372"
---
# <a name="provision-a-new-environment"></a><span data-ttu-id="f31b7-103">Naujos aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="f31b7-103">Provision a new environment</span></span>

<span data-ttu-id="f31b7-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="f31b7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f31b7-105">Šioje temoje pateikiama informacija, kaip parengti naują „Dynamics 365 Project Operations“ aplinką, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="f31b7-105">This topic provides information about how to provision a new Dynamics 365 Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a><span data-ttu-id="f31b7-106">Automatinio „Project Operations“ parengimo įjungimas LCS projekte</span><span class="sxs-lookup"><span data-stu-id="f31b7-106">Enable Project Operations automated provisioning in an LCS project</span></span>

<span data-ttu-id="f31b7-107">Atlikite toliau nurodytus veiksmus, kad įjungtumėte automatinį „Project Operations“ parengimą LCS projekte.</span><span class="sxs-lookup"><span data-stu-id="f31b7-107">Use following steps to enable the Project Operations automated provisioning flow for your LCS project.</span></span>

1. <span data-ttu-id="f31b7-108">Eikite į [LCS](https://lcs.dynamics.com/v2) ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-108">Go to [LCS](https://lcs.dynamics.com/v2) and select the **Preview Feature management** tile.</span></span>
2. <span data-ttu-id="f31b7-109">Sąraše **Peržiūros versijos funkcija** pasirinkite **Project Operations** ir pasirinkite **Peržiūros versijos funkcija įjungta**, kad įjungtumėte „Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="f31b7-109">In the **Preview feature** list, select **Project Operations** and the select **Preview feature enabled** to enable Project Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="f31b7-110">Šį veiksmą reikia atlikti tik vieną kartą LCS projekte.</span><span class="sxs-lookup"><span data-stu-id="f31b7-110">This step is performed only one time per LCS project.</span></span>

## <a name="provision-a-project-operations-environment"></a><span data-ttu-id="f31b7-111">„Project Operations“ aplinkos parengimas</span><span class="sxs-lookup"><span data-stu-id="f31b7-111">Provision a Project Operations environment</span></span>

1. <span data-ttu-id="f31b7-112">Atidarykite naują „Dynamics 365 Finance“ [demonstracinės aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) arba [smėlio dėžės / gamybos aplinkos](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) visuotinio diegimo paketą.</span><span class="sxs-lookup"><span data-stu-id="f31b7-112">Open a new Dynamics 365 Finance [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) or [sandbox/ production environment](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) deployment.</span></span> 
2. <span data-ttu-id="f31b7-113">Atlikite vediklio **Aplinkos parengimas** veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f31b7-113">Walk through the **Environment provisioning** wizard.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="f31b7-114">Įsitikinkite, kad naudojama 10.0.13 arba naujesnė programos versija.</span><span class="sxs-lookup"><span data-stu-id="f31b7-114">Make sure selected application version is 10.0.13 or higher.</span></span>

3. <span data-ttu-id="f31b7-115">Norėdami parengti „Project Operations“, dalyje **Išplėstiniai parametrai** pasirinkite **Common Data Service**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-115">To provision Project Operations, under **Advance settings**, select **Common Data Service**.</span></span> 
4. <span data-ttu-id="f31b7-116">Įjunkite parametrą **„Common Data Service“ parametras** pasirinkdami **Taip** ir įveskite informaciją privalomuose laukuose:</span><span class="sxs-lookup"><span data-stu-id="f31b7-116">Enable the **Common Data Service Setting** by selecting **Yes** and then enter information in the required fields:</span></span>

  - <span data-ttu-id="f31b7-117">Pavadinimas / vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="f31b7-117">Name</span></span>
  - <span data-ttu-id="f31b7-118">Regiono ID</span><span class="sxs-lookup"><span data-stu-id="f31b7-118">Region</span></span>
  - <span data-ttu-id="f31b7-119">Kalba</span><span class="sxs-lookup"><span data-stu-id="f31b7-119">Language</span></span>
  - <span data-ttu-id="f31b7-120">Valiuta</span><span class="sxs-lookup"><span data-stu-id="f31b7-120">Currency</span></span>
 
5. <span data-ttu-id="f31b7-121">Lauke **„Common Data Service“ šablonas** pasirinkite **Project Operations**</span><span class="sxs-lookup"><span data-stu-id="f31b7-121">In the **Common Data Service Template** field, select **Project Operations**</span></span> 

6. <span data-ttu-id="f31b7-122">Pasirinkite visuotinio diegimo aplinkos tipą.</span><span class="sxs-lookup"><span data-stu-id="f31b7-122">Select the environment type for your deployment.</span></span> <span data-ttu-id="f31b7-123">Jei naudojate prenumeruojamą bandomąją versiją, CDS aplinka galės būti įdiegta 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="f31b7-123">A subscription-based trial will let you deploy a CDS environment for 30 days.</span></span> 

![Visuotinio diegimo parametrai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> <span data-ttu-id="f31b7-125">Pasirinkite **Sutinku**, kad sutiktumėte su paslaugos teikimo sąlygomis, tada pasirinkite **Atlikta**, kad grįžtumėte į visuotinio diegimo parametrus.</span><span class="sxs-lookup"><span data-stu-id="f31b7-125">Select **Agree** to acknowledge the terms of service and then select **Done** to return to the deployment settings.</span></span>

![Visuotinio diegimo sutikimas](./media/2DeploymentConsent.png)

7. <span data-ttu-id="f31b7-127">Užpildykite likusius būtinus vediklio laukus ir patvirtinkite visuotinį diegimą.</span><span class="sxs-lookup"><span data-stu-id="f31b7-127">Complete the remaining required fields in the wizard and confirm the deployment.</span></span> <span data-ttu-id="f31b7-128">Aplinkos parengimo laikas priklauso nuo aplinkos tipo.</span><span class="sxs-lookup"><span data-stu-id="f31b7-128">Environment provisioning time varies based on the environment type.</span></span> <span data-ttu-id="f31b7-129">Parengimo procesas gali užtrukti iki šešių valandų.</span><span class="sxs-lookup"><span data-stu-id="f31b7-129">Provisioning might take up to six hours.</span></span>

  <span data-ttu-id="f31b7-130">Sėkmingai užbaigus visuotinį diegimą, bus rodoma aplinkos būsena **Įdiegta**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-130">After the deployment completes successfully, the environment will show as **Deployed**.</span></span>

8. <span data-ttu-id="f31b7-131">Norėdami įsitikinti, kad aplinka sėkmingai įdiegta, pasirinkite **Prisijungti** ir prisijunkite prie aplinkos, kad patvirtintumėte.</span><span class="sxs-lookup"><span data-stu-id="f31b7-131">To confirm the environment has deployed successfully, select **Login** and log on to the environment to confirm.</span></span>

![Išsami „“ aplinkos informacija](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a><span data-ttu-id="f31b7-133">„Project Operations Finance“ demonstracinių duomenų taikymas (pasirinktinis veiksmas)</span><span class="sxs-lookup"><span data-stu-id="f31b7-133">Apply Project Operations Finance demo data (optional step)</span></span>

<span data-ttu-id="f31b7-134">Taikykite „Project Operations Finance“ demonstracinius duomenis 10.0.13 paslaugų leidimo debesyje esančiai aplinkai, kaip aprašyta [šiame straipsnyje](resource-apply-finance-demo-data.md).</span><span class="sxs-lookup"><span data-stu-id="f31b7-134">Apply Project Operations Finance demo data to 10.0.13 service release Cloud Hosted Environment as described in [this article](resource-apply-finance-demo-data.md).</span></span>

## <a name="apply-updates-to-the-finance-environment"></a><span data-ttu-id="f31b7-135">Naujinimų taikymas „Finance“ aplinkai</span><span class="sxs-lookup"><span data-stu-id="f31b7-135">Apply updates to the Finance environment</span></span>

<span data-ttu-id="f31b7-136">„Project Operations“ reikalinga „Finance“ aplinka su **10.0.13 (10.0.569.20009)** arba naujesnės versijos programa.</span><span class="sxs-lookup"><span data-stu-id="f31b7-136">Project Operations requires a Finance environment with application version **10.0.13 (10.0.569.20009)** or higher.</span></span>

<span data-ttu-id="f31b7-137">Kad galėtumėte gauti šią versiją, gali reikėti „Finance“ aplinkai taikyti kokybinius naujinimus.</span><span class="sxs-lookup"><span data-stu-id="f31b7-137">You might need to apply quality updates to your Finance environment to receive this version.</span></span>

1. <span data-ttu-id="f31b7-138">LCS puslapio **Išsami aplinkos informacija** skyriuje **Pasiekimai naujiniai** pasirinkite **Peržiūrėti naujinį**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-138">In LCS, on the **Environment details** page, in the **Available Updates** section, select **View Update**.</span></span>

![Peržiūrėti naujinius](./media/5ViewUpdates.png)

2. <span data-ttu-id="f31b7-140">Puslapyje **Dvejetainiai naujinimai** pasirinkite **Įrašyti paketą**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-140">On the **Binary updates** page, select **Save package.**</span></span>

![Įrašyti paketą](./media/6SavePackage.png)

3. <span data-ttu-id="f31b7-142">Spustelėkite **Pasirinkti viską** ir pasirinkite **Įrašyti paketą**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-142">Click **Select all** and then select **Save package**.</span></span>

![Peržiūrėti ir įrašyti naujinius](./media/7ReviewAndSaveUpdates.png)

4. <span data-ttu-id="f31b7-144">Įveskite paketo pavadinimą ir aprašą, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-144">Enter a name and a description of the package, and then select **Save**.</span></span> <span data-ttu-id="f31b7-145">Atsižvelgiant į interneto ryšį, šis procesas gali šiek tiek užtrukti.</span><span class="sxs-lookup"><span data-stu-id="f31b7-145">Depending on the internet connection, this process might take some time.</span></span>

![Paketo nusiuntimas į išteklių biblioteką](./media/8UploadPackageToAssetsLibrary.png)

5. <span data-ttu-id="f31b7-147">Įrašę paketą pasirinkite **Atlikta** ir įrašykite šį paketą LCS projekto išteklių bibliotekoje.</span><span class="sxs-lookup"><span data-stu-id="f31b7-147">After the package is saved, select **Done** and save this package to the Assets library in your LCS project.</span></span>

<span data-ttu-id="f31b7-148">Paketo įrašymo ir tikrinimo procesas gali užtrukti maždaug 15 minučių.</span><span class="sxs-lookup"><span data-stu-id="f31b7-148">Saving and validating the package might take ~15 minutes.</span></span>

6. <span data-ttu-id="f31b7-149">Norėdami taikyti naujinį, eikite į LCS puslapį **Išsami aplinkos informacija** ir pasirinkite **Tvarkyti** > **Taikyti naujinius**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-149">To apply the update, navigate to the **Environment details** page in LCS and select **Maintain** > **Apply updates**.</span></span>

![Aplinkų tvarkymas](./media/9MaintainEnvironment.png)

7. <span data-ttu-id="f31b7-151">Naujinių sąraše pasirinkite sukurtą paketą ir pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-151">In the updates list select the package you created, and select **Apply**.</span></span>

![Naujinių taikymas](./media/10ApplyUpdates.png)

<span data-ttu-id="f31b7-153">Aplinkos paruošimas gali šiek tiek užtrukti.</span><span class="sxs-lookup"><span data-stu-id="f31b7-153">Environment servicing will take some time.</span></span> <span data-ttu-id="f31b7-154">Baigus vėl bus nustatyta aplinkos būsena Įdiegta.</span><span class="sxs-lookup"><span data-stu-id="f31b7-154">After it is complete, the environment will return to a deployed state.</span></span>

![Aplinka įdiegta](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a><span data-ttu-id="f31b7-156">Dvigubo rašymo ryšio nustatymas</span><span class="sxs-lookup"><span data-stu-id="f31b7-156">Establish a Dual Write connection</span></span> 

1. <span data-ttu-id="f31b7-157">LCS projekte eikite į puslapį **Išsami aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-157">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f31b7-158">Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-158">Under **Common Data Service Environment Information**, select **Link to CDS for Apps**.</span></span>
3. <span data-ttu-id="f31b7-159">Susiejus dar kartą pasirinkite **Susieti su CDS programoms**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-159">After the link is complete, select **Link to CDS for Apps** again.</span></span> <span data-ttu-id="f31b7-160">Būsite nukreipti į dvigubo rašymo sistemą modulyje „Finance“.</span><span class="sxs-lookup"><span data-stu-id="f31b7-160">You will be redirected to Dual Write in Finance.</span></span>

![Susiejimas su CDS](./media/12LinktoCDS.png)

4. <span data-ttu-id="f31b7-162">Pasirinkite **Taikyti sprendimą**, kad pasiektumėte objektus, kurie bus susieti atliekant integravimą.</span><span class="sxs-lookup"><span data-stu-id="f31b7-162">Select **Apply Solution** to access the entities that will be mapped in the integration.</span></span>

![Taikyti sprendimus](./media/13ApplySolutions.png)

5. <span data-ttu-id="f31b7-164">Pasirinkite abu sprendimus: **„Dynamics 365 Finance and Operations“ dvigubo rašymo objektų schema** ir **„Dynamics 365 Project Operations“ dvigubo rašymo objektų schemos**, tada pasirinkite **Taikyti**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-164">Select both solutions, **Dynamics 365 Finance and Operations Dual Write Entity Map** and **Dynamics 365 Project Operations Dual Write Entity Maps**, and then select **Apply**.</span></span>

![Sprendimų patvirtinimas](./media/14ConfirmSolutions.png)

<span data-ttu-id="f31b7-166">Pritaikius sprendimus, į aplinką įtraukiami dvigubo rašymo objektai.</span><span class="sxs-lookup"><span data-stu-id="f31b7-166">After the solutions are applied, the Dual Write entities are applied to the environment.</span></span>

![Sprendimų taikymas](./media/15ApplyingSolutions.png)

<span data-ttu-id="f31b7-168">Pritaikius objektus visi galimi susiejimai pateikiami aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="f31b7-168">After the entities are applied, all available mappings are listed in the environment.</span></span>

![Dvigubo rašymo schemos](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a><span data-ttu-id="f31b7-170">Duomenų objektų atnaujinimas atlikus naujinimą</span><span class="sxs-lookup"><span data-stu-id="f31b7-170">Refresh the data entities after the update</span></span>

1. <span data-ttu-id="f31b7-171">Modulyje „Finance“ eikite į darbo sritį **Duomenų valdymas**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-171">In Finance, go to the **Data management** workspace.</span></span>

![Duomenų valdymo darbo sritis](./media/16DataManagement.png)

2. <span data-ttu-id="f31b7-173">Pasirinkite plytelę **Sistemos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-173">Select the **Framework parameters** tile.</span></span>

![Sistemos parametrai](./media/17FrameworkParameters.png)

3. <span data-ttu-id="f31b7-175">Puslapyje **Objektų parametrai** pasirinkite **Atnaujinti objektų sąrašą**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-175">On the **Entity settings** page, select **Refresh Entity list**.</span></span>

![Objektų sąrašo atnaujinimas](./media/18RefreshEntityList.png)

<span data-ttu-id="f31b7-177">Atnaujinimas truks apie 20 minučių.</span><span class="sxs-lookup"><span data-stu-id="f31b7-177">The refresh is going to take approximately 20 minutes.</span></span> <span data-ttu-id="f31b7-178">Kai jis bus baigtas, gausite įspėjimą.</span><span class="sxs-lookup"><span data-stu-id="f31b7-178">You will receive an alert when it is complete.</span></span>

![Patvirtinimo atnaujinimas](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a><span data-ttu-id="f31b7-180">„Project Operations“ dvigubo rašymo schemų vykdymas</span><span class="sxs-lookup"><span data-stu-id="f31b7-180">Run Project Operations Dual Write maps</span></span>

1. <span data-ttu-id="f31b7-181">LCS projekte eikite į puslapį **Išsami aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-181">In your LCS project, go to the **Environment details** page.</span></span>
2. <span data-ttu-id="f31b7-182">Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-182">Under **Common Data Service Environment Information**, select **Link to CDS for Apps.**</span></span> <span data-ttu-id="f31b7-183">Pasirinkus saitą būsite nukreipti į susiejimų objektų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f31b7-183">After you select the link, you will be redirected to the list of entities in the mappings.</span></span>
3. <span data-ttu-id="f31b7-184">Paleiskite schemas, kaip aprašyta toliau esančioje lentelėje.</span><span class="sxs-lookup"><span data-stu-id="f31b7-184">Start the maps as described in the following table.</span></span> <span data-ttu-id="f31b7-185">Būtinai viską darykite iš eilės, kaip nurodyta.</span><span class="sxs-lookup"><span data-stu-id="f31b7-185">Make sure to follow the sequence as listed.</span></span>

| <span data-ttu-id="f31b7-186">**Objekto schema**</span><span class="sxs-lookup"><span data-stu-id="f31b7-186">**Entity Map**</span></span> | <span data-ttu-id="f31b7-187">**Atnaujinti objektą**</span><span class="sxs-lookup"><span data-stu-id="f31b7-187">**Refresh entity**</span></span> | <span data-ttu-id="f31b7-188">**Pradinis sinchronizavimas**</span><span class="sxs-lookup"><span data-stu-id="f31b7-188">**Initial sync**</span></span> | <span data-ttu-id="f31b7-189">**Pradinio sinchronizavimo šablonas**</span><span class="sxs-lookup"><span data-stu-id="f31b7-189">**Master for initial sync**</span></span> | <span data-ttu-id="f31b7-190">**Vykdymo būtinosios sąlygos**</span><span class="sxs-lookup"><span data-stu-id="f31b7-190">**Run prerequisites**</span></span> | <span data-ttu-id="f31b7-191">**Būtinas pradinis sinchronizavimas**</span><span class="sxs-lookup"><span data-stu-id="f31b7-191">**Prerequisites initial sync**</span></span> |
| --- | --- | --- | --- | --- | --- |
| <span data-ttu-id="f31b7-192">**Projekto išteklių vaidmenys visoms įmonėms (bookableresourcecategories)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-192">**Project Resource Roles for All Companies (bookableresourcecategories)**</span></span> | <span data-ttu-id="f31b7-193">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-193">No</span></span> | <span data-ttu-id="f31b7-194">Taip</span><span class="sxs-lookup"><span data-stu-id="f31b7-194">Yes</span></span> | <span data-ttu-id="f31b7-195">„Common Data Service“</span><span class="sxs-lookup"><span data-stu-id="f31b7-195">Common Data Service</span></span> | <span data-ttu-id="f31b7-196">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-196">No</span></span> | <span data-ttu-id="f31b7-197">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-197">N\A</span></span> |
| <span data-ttu-id="f31b7-198">**Juridiniai subjektai (cdm\_companies)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-198">**Legal entities (cdm\_companies)**</span></span> | <span data-ttu-id="f31b7-199">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-199">No</span></span> | <span data-ttu-id="f31b7-200">Taip</span><span class="sxs-lookup"><span data-stu-id="f31b7-200">Yes</span></span> | <span data-ttu-id="f31b7-201">„Finance and Operations“ programos</span><span class="sxs-lookup"><span data-stu-id="f31b7-201">Finance and Operations apps</span></span> | <span data-ttu-id="f31b7-202">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-202">No</span></span> | <span data-ttu-id="f31b7-203">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-203">N\A</span></span> |
| <span data-ttu-id="f31b7-204">**„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-204">**Project Operations integration actuals (msdyn\_actuals)**</span></span> | <span data-ttu-id="f31b7-205">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-205">No</span></span> | <span data-ttu-id="f31b7-206">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-206">No</span></span> | <span data-ttu-id="f31b7-207">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-207">N\A</span></span> | <span data-ttu-id="f31b7-208">Taip</span><span class="sxs-lookup"><span data-stu-id="f31b7-208">Yes</span></span> | <span data-ttu-id="f31b7-209">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-209">No</span></span> |
| <span data-ttu-id="f31b7-210">**Projekto sutarties eilutės (salesorderdetails)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-210">**Project contract lines (salesorderdetails)**</span></span> | <span data-ttu-id="f31b7-211">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-211">No</span></span> | <span data-ttu-id="f31b7-212">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-212">No</span></span> | <span data-ttu-id="f31b7-213">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-213">N\A</span></span> | <span data-ttu-id="f31b7-214">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-214">No</span></span> | <span data-ttu-id="f31b7-215">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-215">No</span></span> |
| <span data-ttu-id="f31b7-216">**Projekto operacijų ryšių integravimo objektas (msdyn\_transactionconnections)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-216">**Integration entity for project transaction relationships (msdyn\_transactionconnections)**</span></span> | <span data-ttu-id="f31b7-217">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-217">No</span></span> | <span data-ttu-id="f31b7-218">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-218">No</span></span> | <span data-ttu-id="f31b7-219">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-219">N\A</span></span> | <span data-ttu-id="f31b7-220">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-220">No</span></span> | <span data-ttu-id="f31b7-221">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-221">N\A</span></span> |
| <span data-ttu-id="f31b7-222">**„Project Operations“ integravimo sutarties eilučių etapai (msdyn\_contractlinesscheduleofvalues)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-222">**Project Operations integration contract line milestones (msdyn\_contractlinesscheduleofvalues)**</span></span> | <span data-ttu-id="f31b7-223">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-223">No</span></span> | <span data-ttu-id="f31b7-224">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-224">No</span></span> | <span data-ttu-id="f31b7-225">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-225">N\A</span></span> | <span data-ttu-id="f31b7-226">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-226">No</span></span> | <span data-ttu-id="f31b7-227">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-227">N\A</span></span> |
| <span data-ttu-id="f31b7-228">**„Project Operations“ integravimo objektas, skirtas išlaidų įvertinimams (msdyn\_estimateslines)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-228">**Project Operations integration entity for expense estimates (msdyn\_estimateslines)**</span></span> | <span data-ttu-id="f31b7-229">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-229">No</span></span> | <span data-ttu-id="f31b7-230">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-230">No</span></span> | <span data-ttu-id="f31b7-231">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-231">N\A</span></span> | <span data-ttu-id="f31b7-232">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-232">No</span></span> | <span data-ttu-id="f31b7-233">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-233">N\A</span></span> |
| <span data-ttu-id="f31b7-234">**„Project Operations“ integravimo objektas, skirtas valandų įvertinimams (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-234">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="f31b7-235">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-235">No</span></span> | <span data-ttu-id="f31b7-236">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-236">No</span></span> | <span data-ttu-id="f31b7-237">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-237">N\A</span></span> | <span data-ttu-id="f31b7-238">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-238">No</span></span> | <span data-ttu-id="f31b7-239">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-239">N\A</span></span> |
| <span data-ttu-id="f31b7-240">**„Project Operations“ integravimo projekto išlaidų eksportavimo objektas (msdyn\_expenses)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-240">**Project Operations integration project expenses export entity (msdyn\_expenses)**</span></span> | <span data-ttu-id="f31b7-241">Taip</span><span class="sxs-lookup"><span data-stu-id="f31b7-241">Yes</span></span> | <span data-ttu-id="f31b7-242">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-242">No</span></span> | <span data-ttu-id="f31b7-243">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-243">N\A</span></span> | <span data-ttu-id="f31b7-244">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-244">No</span></span> | <span data-ttu-id="f31b7-245">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-245">N\A</span></span> |
| <span data-ttu-id="f31b7-246">**„Project Operations“ integravimo objektas, skirtas valandų įvertinimams (msdyn\_resourceassignments)**</span><span class="sxs-lookup"><span data-stu-id="f31b7-246">**Project Operations integration entity for hour estimates (msdyn\_resourceassignments)**</span></span> | <span data-ttu-id="f31b7-247">Taip</span><span class="sxs-lookup"><span data-stu-id="f31b7-247">Yes</span></span> | <span data-ttu-id="f31b7-248">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-248">No</span></span> | <span data-ttu-id="f31b7-249">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-249">N\A</span></span> | <span data-ttu-id="f31b7-250">No</span><span class="sxs-lookup"><span data-stu-id="f31b7-250">No</span></span> | <span data-ttu-id="f31b7-251">Nėra</span><span class="sxs-lookup"><span data-stu-id="f31b7-251">N\A</span></span> |

4. <span data-ttu-id="f31b7-252">Norėdami atnaujinti objektą, pasirinkite schemos pavadinimą ir pasirinkite **Atnaujinti objektus**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-252">To refresh the entity, select the map name, and then select **Refresh entities**.</span></span> 
5. <span data-ttu-id="f31b7-253">Atnaujinus paleiskite schemą.</span><span class="sxs-lookup"><span data-stu-id="f31b7-253">Proceed with running the map after the refresh is complete.</span></span>

![Schemos atnaujinimas](./media/20RefreshMapping.png)

<span data-ttu-id="f31b7-255">Prieš įjungdami kitą schemą patikrinkite, ar lentelėje schemos būsena yra **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-255">Before you enable the next map, verify that the map in the table is in a state of **Running**.</span></span> <span data-ttu-id="f31b7-256">Gali šiek tiek užtrukti, kol bus paleistos schemos, turinčios daug būtinųjų sąlygų.</span><span class="sxs-lookup"><span data-stu-id="f31b7-256">Running maps with a larger number of prerequisites might take some time.</span></span>

<span data-ttu-id="f31b7-257">Norėdami paleisti schemą su būtinosiomis sąlygomis, įjunkite perjungiklį **Rodyti susijusias objektų schemas**.</span><span class="sxs-lookup"><span data-stu-id="f31b7-257">To run a map with prerequisites, enable the **Show related entity maps** toggle.</span></span> <span data-ttu-id="f31b7-258">Jei lentelėje nurodyta **Būtinas pradinis sinchronizavimas** reikšmė **Ne**, įsitikinkite, kad žymės **Pradinis sinchronizavimas** būklė yra **Išjungta** visose būtinosiose schemose prieš ją vykdydami.</span><span class="sxs-lookup"><span data-stu-id="f31b7-258">If the table indicates **Prerequisite initial sync** is **No**, verify that the **Initial sync** flag is **Off** in all the prerequisite maps before you run it.</span></span>

![Schemos vykdymas](./media/21RunMap.png)

6. <span data-ttu-id="f31b7-260">Įsitikinkite, kad visos su projektu susijusios schemos yra vykdomos.</span><span class="sxs-lookup"><span data-stu-id="f31b7-260">Validate all project related maps are in the running state.</span></span>

![Visos schemos yra vykdomos](./media/22AllMapsRunning.png)

<span data-ttu-id="f31b7-262">Jūsų „Project Operations“ aplinka dabar parengta ir sukonfigūruota.</span><span class="sxs-lookup"><span data-stu-id="f31b7-262">Your Project Operations environment is now provisioned and configured.</span></span>
