---
title: Konfigūracijos duomenų nustatymas ir taikymas programoje „Common Data Service”
description: Šioje temoje pateikta informacija apie konfigūracijos duomenų nustatymą ir taikymą dalyje „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 1651d3b3b85d3dc581bf61976fada249bafd6b7b
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289829"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="bfe11-103">Konfigūracijos duomenų nustatymas ir taikymas programoje „Common Data Service”</span><span class="sxs-lookup"><span data-stu-id="bfe11-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="bfe11-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="bfe11-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="bfe11-105">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="bfe11-105">Prerequisites</span></span>

<span data-ttu-id="bfe11-106">Prieš pradėdami konfigūruoti duomenis programoje „Common Data Service” (CDS), turite atitikti toliau pateikiamas būtinąsias sąlygas.</span><span class="sxs-lookup"><span data-stu-id="bfe11-106">Before you beging to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="bfe11-107">CDS aplinkos ir „Dynamics 365 Finance” aplinkos parengimas, skirtas „Project Operations”.</span><span class="sxs-lookup"><span data-stu-id="bfe11-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="bfe11-108">Juridinio objekto informacija iš „Dynamics 365 Finance” bendrinama su CDS aplinka.</span><span class="sxs-lookup"><span data-stu-id="bfe11-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="bfe11-109">Tai reiškia, kad CDS esančiame objekte **Įmonė** yra toliau pateikiami įmonės įrašai.</span><span class="sxs-lookup"><span data-stu-id="bfe11-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="bfe11-110">THPM</span><span class="sxs-lookup"><span data-stu-id="bfe11-110">THPM</span></span>
  - <span data-ttu-id="bfe11-111">USPM</span><span class="sxs-lookup"><span data-stu-id="bfe11-111">USPM</span></span>
  - <span data-ttu-id="bfe11-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="bfe11-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="bfe11-113">Sąrankos ir konfigūracijos duomenų diegimas</span><span class="sxs-lookup"><span data-stu-id="bfe11-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="bfe11-114">Atsisiųskite, atblokuokite ir išskleiskite [sąrankos ir konfigūracijos duomenų paketą](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="bfe11-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="bfe11-115">Nueikite į neišskleistą aplanką ir vykdykite vykdomąjį failą *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="bfe11-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="bfe11-116">„Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="bfe11-118">CMT vedlio 2 puslapyje pažymėkite **Microsoft 365** kaip **Visuotinio diegimo tipą**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="bfe11-119">Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="bfe11-120">Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus ir pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="bfe11-122">3 puslapyje nuomotojo organizacijų sąraše pasirinkite organizaciją, į kurią norite importuoti demonstracinius duomenis, ir pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="bfe11-123">4 puslapyje pasirinkite suglaudintą failą *SampleSetupAndConfigData* neišskleistame aplanke.</span><span class="sxs-lookup"><span data-stu-id="bfe11-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Suglaudinto failo pasirinkimas](./media/3ZipFile.png)

![Pasirinkite failą](./media/4SelectAFile.png)

9. <span data-ttu-id="bfe11-126">Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-126">After the zip file is selected, select **Import Data**.</span></span>

![Importuoti duomenis](./media/5ImportData.png)

10. <span data-ttu-id="bfe11-128">Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių.</span><span class="sxs-lookup"><span data-stu-id="bfe11-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="bfe11-129">Baigus importuoti uždarykite CMT vediklį.</span><span class="sxs-lookup"><span data-stu-id="bfe11-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="bfe11-130">Patikrinkite savo organizacijos duomenis šiuose 19 objektų:</span><span class="sxs-lookup"><span data-stu-id="bfe11-130">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="bfe11-131">Valiuta</span><span class="sxs-lookup"><span data-stu-id="bfe11-131">Currency</span></span>
  - <span data-ttu-id="bfe11-132">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="bfe11-132">Organizational Unit</span></span>
  - <span data-ttu-id="bfe11-133">Susisiekite</span><span class="sxs-lookup"><span data-stu-id="bfe11-133">Contact</span></span>
  - <span data-ttu-id="bfe11-134">Mokesčių grupė</span><span class="sxs-lookup"><span data-stu-id="bfe11-134">Tax Group</span></span>
  - <span data-ttu-id="bfe11-135">Klientų grupė</span><span class="sxs-lookup"><span data-stu-id="bfe11-135">Customer Group</span></span>
  - <span data-ttu-id="bfe11-136">Vienetas</span><span class="sxs-lookup"><span data-stu-id="bfe11-136">Unit</span></span>
  - <span data-ttu-id="bfe11-137">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="bfe11-137">Unit Group</span></span>
  - <span data-ttu-id="bfe11-138">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="bfe11-138">Price List</span></span>
  - <span data-ttu-id="bfe11-139">Projekto parametrų kainoraštis</span><span class="sxs-lookup"><span data-stu-id="bfe11-139">Project Parameter Price List</span></span>
  - <span data-ttu-id="bfe11-140">Sąskaitos faktūros dažnumas</span><span class="sxs-lookup"><span data-stu-id="bfe11-140">Invoice Frequency</span></span>
  - <span data-ttu-id="bfe11-141">Rezervuojamų išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="bfe11-141">Bookable Resource Category</span></span>
  - <span data-ttu-id="bfe11-142">Operacijos kategorija</span><span class="sxs-lookup"><span data-stu-id="bfe11-142">Transaction Category</span></span>
  - <span data-ttu-id="bfe11-143">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="bfe11-143">Expense Category</span></span>
  - <span data-ttu-id="bfe11-144">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="bfe11-144">Role Price</span></span>
  - <span data-ttu-id="bfe11-145">Operacijos kategorijos kaina</span><span class="sxs-lookup"><span data-stu-id="bfe11-145">Transaction Category Price</span></span>
  - <span data-ttu-id="bfe11-146">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="bfe11-146">Characteristic</span></span>
  - <span data-ttu-id="bfe11-147">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="bfe11-147">Bookable Resource</span></span>
  - <span data-ttu-id="bfe11-148">Rezervuojamų išteklių kategorijos sąsaja</span><span class="sxs-lookup"><span data-stu-id="bfe11-148">Bookable resource category Assn</span></span>
  - <span data-ttu-id="bfe11-149">Rezervuojamų išteklių charakteristika</span><span class="sxs-lookup"><span data-stu-id="bfe11-149">Bookable Resource Characteristic</span></span>

![Importavimo užbaigimas](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="bfe11-151">„Project Operations“ konfigūracijų naujinimas</span><span class="sxs-lookup"><span data-stu-id="bfe11-151">Update Project Operations configurations</span></span>

1. <span data-ttu-id="bfe11-152">Eikite į CE aplinką.</span><span class="sxs-lookup"><span data-stu-id="bfe11-152">Navigate to the CE environment.</span></span> <span data-ttu-id="bfe11-153">Ją rasite atidarę [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/environments), pasirinkę aplinką ir pasirinkę **Atidaryti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-153">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Aplinkos atidarymas](./media/7OpenEnvironment.png)

2. <span data-ttu-id="bfe11-155">Eikite į **Projektai** > **Ištekliai**, tada pasirinkite **Naujas**, kad vartotojui sukurtumėte išteklių, kurį galima rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="bfe11-155">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervuojami ištekliai](./media/8BookableResources.png)

3. <span data-ttu-id="bfe11-157">Skirtuke **Bendra** pasirinkite administratoriaus vartotoją.</span><span class="sxs-lookup"><span data-stu-id="bfe11-157">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="bfe11-158">Patikrinkite, ar laiko juosta atitinka tą, kurioje esate jūs.</span><span class="sxs-lookup"><span data-stu-id="bfe11-158">Verify that the time zone matches the one you are in.</span></span> 

![Naujas rezervuojamas išteklius](./media/9NewBookableResource.png)

4. <span data-ttu-id="bfe11-160">Skirtuko **Planavimas** lauke **Įmonė** pasirinkite įmonę **USPM** ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-160">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planavimo skirtukas](./media/10SchedulingTab.png)

5. <span data-ttu-id="bfe11-162">Pasirinkite skirtuką **Darbo valandos**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-162">Select the **Work hours** tab.</span></span>  

![Darbo valandos](./media/11WorkHours.png)

6. <span data-ttu-id="bfe11-164">Kalendoriuje dukart spustelėkite bet kokią reikšmę ir pasirinkite **Redaguoti** > **Visi sekos įvykiai**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-164">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Darbo kalendorius](./media/12WorkCalendar.png)

7. <span data-ttu-id="bfe11-166">Pakeiskite darbo valandas į aštuonių (8) valandų darbo dieną, pažymėkite savaitgalius kaip ne darbo dienas ir įsitikinkite, kad laiko juosta atitinka jūsų.</span><span class="sxs-lookup"><span data-stu-id="bfe11-166">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="bfe11-167">Pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-167">Select **Save and close**.</span></span>

![Kalendoriaus naujinimas](./media/13UpdateCalendar.png)

9. <span data-ttu-id="bfe11-169">Eikite į **Parametrai** > **Kalendoriaus šablonas** ir pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-169">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendoriaus šablonai](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="bfe11-171">Įveskite pavadinimą, pasirinkite sukurtą šablono išteklių, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-171">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendoriaus šablono įrašymas](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="bfe11-173">Eikite į **Parametrai** ir dukart spustelėkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="bfe11-173">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekto parametrai](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="bfe11-175">Atnaujinkite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="bfe11-175">Update the following fields:</span></span>

 - <span data-ttu-id="bfe11-176">**Numatytoji įmonė**: USPM</span><span class="sxs-lookup"><span data-stu-id="bfe11-176">**Default company**: USPM</span></span>
 - <span data-ttu-id="bfe11-177">**Numatytasis organizacinis vienetas**: „Contoso Robotics Global“</span><span class="sxs-lookup"><span data-stu-id="bfe11-177">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="bfe11-178">**Sąskaitų faktūrų dažnumas**: septintoji diena ir paskutinė diena</span><span class="sxs-lookup"><span data-stu-id="bfe11-178">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="bfe11-179">**Darbo valandų šablonas**: pakeiskite į savo sukurtą šabloną.</span><span class="sxs-lookup"><span data-stu-id="bfe11-179">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="bfe11-180">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="bfe11-180">Select **Save**.</span></span> 

![Projekto parametrai atnaujinti](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]