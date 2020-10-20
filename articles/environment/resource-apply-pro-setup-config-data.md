---
title: Konfigūracijos duomenų nustatymas ir taikymas „Common Data Service“, skirtoje „Project Operations“
description: Šioje temoje pateikta informacija apie konfigūracijos duomenų nustatymą ir taikymą dalyje „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d99ab4c7b2ebf6ba56b86a3e0151036c6247e484
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948980"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service-for-project-operations"></a><span data-ttu-id="637cc-103">Konfigūracijos duomenų nustatymas ir taikymas „Common Data Service“, skirtoje „Project Operations“</span><span class="sxs-lookup"><span data-stu-id="637cc-103">Set up and apply configuration data in the Common Data Service for Project Operations</span></span>

<span data-ttu-id="637cc-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="637cc-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="637cc-105">Sąrankos ir konfigūracijos duomenų diegimas</span><span class="sxs-lookup"><span data-stu-id="637cc-105">Install setup and configuration data</span></span>

1. <span data-ttu-id="637cc-106">Atsisiųskite, atblokuokite ir išskleiskite [sąrankos ir konfigūracijos duomenų paketą](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span><span class="sxs-lookup"><span data-stu-id="637cc-106">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).</span></span>
2. <span data-ttu-id="637cc-107">Nueikite į neišskleistą aplanką ir vykdykite vykdomąjį failą *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="637cc-107">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="637cc-108">„Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="637cc-108">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="637cc-110">CMT vedlio 2 puslapyje pažymėkite **„Office 365“** kaip **Visuotinio diegimo tipą**.</span><span class="sxs-lookup"><span data-stu-id="637cc-110">On Page 2 of the CMT Wizard, select **Office 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="637cc-111">Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.</span><span class="sxs-lookup"><span data-stu-id="637cc-111">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="637cc-112">Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus ir pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="637cc-112">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="637cc-114">3 puslapyje nuomotojo organizacijų sąraše pasirinkite organizaciją, į kurią norite importuoti demonstracinius duomenis, ir pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="637cc-114">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="637cc-115">4 puslapyje pasirinkite suglaudintą failą *SampleSetupAndConfigData* neišskleistame aplanke.</span><span class="sxs-lookup"><span data-stu-id="637cc-115">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Suglaudinto failo pasirinkimas](./media/3ZipFile.png)

![Pasirinkite failą](./media/4SelectAFile.png)

9. <span data-ttu-id="637cc-118">Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="637cc-118">After the zip file is selected, select **Import Data**.</span></span>

![Importuoti duomenis](./media/5ImportData.png)

10. <span data-ttu-id="637cc-120">Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių.</span><span class="sxs-lookup"><span data-stu-id="637cc-120">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="637cc-121">Baigus importuoti uždarykite CMT vediklį.</span><span class="sxs-lookup"><span data-stu-id="637cc-121">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="637cc-122">Patikrinkite savo organizacijos duomenis šiuose 19 objektų:</span><span class="sxs-lookup"><span data-stu-id="637cc-122">Check your organization for data in the following 19 entities:</span></span>

  - <span data-ttu-id="637cc-123">Valiuta</span><span class="sxs-lookup"><span data-stu-id="637cc-123">Currency</span></span>
  - <span data-ttu-id="637cc-124">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="637cc-124">Organizational Unit</span></span>
  - <span data-ttu-id="637cc-125">Susisiekite</span><span class="sxs-lookup"><span data-stu-id="637cc-125">Contact</span></span>
  - <span data-ttu-id="637cc-126">Mokesčių grupė</span><span class="sxs-lookup"><span data-stu-id="637cc-126">Tax Group</span></span>
  - <span data-ttu-id="637cc-127">Klientų grupė</span><span class="sxs-lookup"><span data-stu-id="637cc-127">Customer Group</span></span>
  - <span data-ttu-id="637cc-128">Vienetas</span><span class="sxs-lookup"><span data-stu-id="637cc-128">Unit</span></span>
  - <span data-ttu-id="637cc-129">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="637cc-129">Unit Group</span></span>
  - <span data-ttu-id="637cc-130">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="637cc-130">Price List</span></span>
  - <span data-ttu-id="637cc-131">Projekto parametrų kainoraštis</span><span class="sxs-lookup"><span data-stu-id="637cc-131">Project Parameter Price List</span></span>
  - <span data-ttu-id="637cc-132">Sąskaitos faktūros dažnumas</span><span class="sxs-lookup"><span data-stu-id="637cc-132">Invoice Frequency</span></span>
  - <span data-ttu-id="637cc-133">Rezervuojamų išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="637cc-133">Bookable Resource Category</span></span>
  - <span data-ttu-id="637cc-134">Operacijos kategorija</span><span class="sxs-lookup"><span data-stu-id="637cc-134">Transaction Category</span></span>
  - <span data-ttu-id="637cc-135">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="637cc-135">Expense Category</span></span>
  - <span data-ttu-id="637cc-136">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="637cc-136">Role Price</span></span>
  - <span data-ttu-id="637cc-137">Operacijos kategorijos kaina</span><span class="sxs-lookup"><span data-stu-id="637cc-137">Transaction Category Price</span></span>
  - <span data-ttu-id="637cc-138">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="637cc-138">Characteristic</span></span>
  - <span data-ttu-id="637cc-139">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="637cc-139">Bookable Resource</span></span>
  - <span data-ttu-id="637cc-140">Rezervuojamų išteklių kategorijos sąsaja</span><span class="sxs-lookup"><span data-stu-id="637cc-140">Bookable resource category Assn</span></span>
  - <span data-ttu-id="637cc-141">Rezervuojamų išteklių charakteristika</span><span class="sxs-lookup"><span data-stu-id="637cc-141">Bookable Resource Characteristic</span></span>

![Importavimo užbaigimas](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="637cc-143">„Project Operations“ konfigūracijų naujinimas</span><span class="sxs-lookup"><span data-stu-id="637cc-143">Update Project Operations configurations</span></span>

1. <span data-ttu-id="637cc-144">Eikite į CE aplinką.</span><span class="sxs-lookup"><span data-stu-id="637cc-144">Navigate to the CE environment.</span></span> <span data-ttu-id="637cc-145">Ją rasite atidarę [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/environments), pasirinkę aplinką ir pasirinkę **Atidaryti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="637cc-145">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Aplinkos atidarymas](./media/7OpenEnvironment.png)

2. <span data-ttu-id="637cc-147">Eikite į **Projektai** > **Ištekliai**, tada pasirinkite **Naujas**, kad vartotojui sukurtumėte išteklių, kurį galima rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="637cc-147">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervuojami ištekliai](./media/8BookableResources.png)

3. <span data-ttu-id="637cc-149">Skirtuke **Bendra** pasirinkite administratoriaus vartotoją.</span><span class="sxs-lookup"><span data-stu-id="637cc-149">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="637cc-150">Patikrinkite, ar laiko juosta atitinka tą, kurioje esate jūs.</span><span class="sxs-lookup"><span data-stu-id="637cc-150">Verify that the time zone matches the one you are in.</span></span> 

![Naujas rezervuojamas išteklius](./media/9NewBookableResource.png)

4. <span data-ttu-id="637cc-152">Skirtuko **Planavimas** lauke **Įmonė** pasirinkite įmonę **USPM** ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="637cc-152">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planavimo skirtukas](./media/10SchedulingTab.png)

5. <span data-ttu-id="637cc-154">Pasirinkite skirtuką **Darbo valandos**.</span><span class="sxs-lookup"><span data-stu-id="637cc-154">Select the **Work hours** tab.</span></span>  

![Darbo valandos](./media/11WorkHours.png)

6. <span data-ttu-id="637cc-156">Kalendoriuje dukart spustelėkite bet kokią reikšmę ir pasirinkite **Redaguoti** > **Visi sekos įvykiai**.</span><span class="sxs-lookup"><span data-stu-id="637cc-156">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Darbo kalendorius](./media/12WorkCalendar.png)

7. <span data-ttu-id="637cc-158">Pakeiskite darbo valandas į aštuonių (8) valandų darbo dieną, pažymėkite savaitgalius kaip ne darbo dienas ir įsitikinkite, kad laiko juosta atitinka jūsų.</span><span class="sxs-lookup"><span data-stu-id="637cc-158">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="637cc-159">Pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="637cc-159">Select **Save and close**.</span></span>

![Kalendoriaus naujinimas](./media/13UpdateCalendar.png)

9. <span data-ttu-id="637cc-161">Eikite į **Parametrai** > **Kalendoriaus šablonas** ir pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="637cc-161">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendoriaus šablonai](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="637cc-163">Įveskite pavadinimą, pasirinkite sukurtą šablono išteklių, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="637cc-163">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendoriaus šablono įrašymas](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="637cc-165">Eikite į **Parametrai** ir dukart spustelėkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="637cc-165">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekto parametrai](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="637cc-167">Atnaujinkite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="637cc-167">Update the following fields:</span></span>

 - <span data-ttu-id="637cc-168">**Numatytoji įmonė**: USPM</span><span class="sxs-lookup"><span data-stu-id="637cc-168">**Default company**: USPM</span></span>
 - <span data-ttu-id="637cc-169">**Numatytasis organizacinis vienetas**: „Contoso Robotics Global“</span><span class="sxs-lookup"><span data-stu-id="637cc-169">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="637cc-170">**Sąskaitų faktūrų dažnumas**: septintoji diena ir paskutinė diena</span><span class="sxs-lookup"><span data-stu-id="637cc-170">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="637cc-171">**Darbo valandų šablonas**: pakeiskite į savo sukurtą šabloną.</span><span class="sxs-lookup"><span data-stu-id="637cc-171">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="637cc-172">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="637cc-172">Select **Save**.</span></span> 

![Projekto parametrai atnaujinti](./media/17UpdatedProjectParameters.png)
