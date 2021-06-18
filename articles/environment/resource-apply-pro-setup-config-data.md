---
title: Konfigūracijos duomenų nustatymas ir taikymas programoje „Common Data Service”
description: Šioje temoje pateikta informacija apie konfigūracijos duomenų nustatymą ir taikymą dalyje „Project Operations“.
author: sigitac
ms.date: 05/10/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ea00df6112fb69b61f1889463424fdfee79aec9
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001301"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a><span data-ttu-id="927ae-103">Konfigūracijos duomenų nustatymas ir taikymas programoje „Common Data Service”</span><span class="sxs-lookup"><span data-stu-id="927ae-103">Set up and apply configuration data in the Common Data Service</span></span> 

<span data-ttu-id="927ae-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="927ae-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="927ae-105">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="927ae-105">Prerequisites</span></span>

<span data-ttu-id="927ae-106">Prieš pradedant konfigūruoti duomenis Common Data Service (CDS), reikia įvykdyti šias būtinąsias sąlygas:</span><span class="sxs-lookup"><span data-stu-id="927ae-106">Before you begin to configure data in the Common Data Service (CDS), the following prerequisites must be met:</span></span>

1.  <span data-ttu-id="927ae-107">CDS aplinkos ir „Dynamics 365 Finance” aplinkos parengimas, skirtas „Project Operations”.</span><span class="sxs-lookup"><span data-stu-id="927ae-107">Provision a CDS environment and a Dynamics 365 Finance environment for Project Operations.</span></span>
2.  <span data-ttu-id="927ae-108">Juridinio objekto informacija iš „Dynamics 365 Finance” bendrinama su CDS aplinka.</span><span class="sxs-lookup"><span data-stu-id="927ae-108">Legal entity information from Dynamics 365 Finance is shared to the CDS environment.</span></span> <span data-ttu-id="927ae-109">Tai reiškia, kad CDS esančiame objekte **Įmonė** yra toliau pateikiami įmonės įrašai.</span><span class="sxs-lookup"><span data-stu-id="927ae-109">This means that the **Company** entity in CDS has the following company records:</span></span>
  - <span data-ttu-id="927ae-110">THPM</span><span class="sxs-lookup"><span data-stu-id="927ae-110">THPM</span></span>
  - <span data-ttu-id="927ae-111">USPM</span><span class="sxs-lookup"><span data-stu-id="927ae-111">USPM</span></span>
  - <span data-ttu-id="927ae-112">GBPM</span><span class="sxs-lookup"><span data-stu-id="927ae-112">GBPM</span></span>

## <a name="install-setup-and-configuration-data"></a><span data-ttu-id="927ae-113">Sąrankos ir konfigūracijos duomenų diegimas</span><span class="sxs-lookup"><span data-stu-id="927ae-113">Install setup and configuration data</span></span>

1. <span data-ttu-id="927ae-114">Atsisiųskite, atblokuokite ir išskleiskite [sąrankos ir konfigūracijos duomenų paketą](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span><span class="sxs-lookup"><span data-stu-id="927ae-114">Download, unblock, and unzip the [Setup and Configuration Data Package](https://download.microsoft.com/download/e/2/d/e2da6c98-d5dd-450c-aabe-fd6bf2ba374b/ProjOpsSampleSetupData-%20Integrated%20Latest.zip).</span></span>
2. <span data-ttu-id="927ae-115">Nueikite į neišskleistą aplanką ir vykdykite vykdomąjį failą *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="927ae-115">Navigate to the unzipped folder and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="927ae-116">„Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="927ae-116">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="927ae-118">CMT vedlio 2 puslapyje pažymėkite **Microsoft 365** kaip **Visuotinio diegimo tipą**.</span><span class="sxs-lookup"><span data-stu-id="927ae-118">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="927ae-119">Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.</span><span class="sxs-lookup"><span data-stu-id="927ae-119">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="927ae-120">Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus ir pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="927ae-120">Select the region of your tenant, enter your credentials, and select **Login**.</span></span>

![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="927ae-122">3 puslapyje nuomotojo organizacijų sąraše pasirinkite organizaciją, į kurią norite importuoti demonstracinius duomenis, ir pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="927ae-122">On page 3, from the list of organizations on the tenant, select the organization you want to import the demo data into and select **Login**.</span></span>
8. <span data-ttu-id="927ae-123">4 puslapyje pasirinkite suglaudintą failą *SampleSetupAndConfigData* neišskleistame aplanke.</span><span class="sxs-lookup"><span data-stu-id="927ae-123">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder.</span></span>

![Suglaudinto failo pasirinkimas](./media/3ZipFile.png)

![Pasirinkite failą](./media/4SelectAFile.png)

9. <span data-ttu-id="927ae-126">Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="927ae-126">After the zip file is selected, select **Import Data**.</span></span>

![Importuoti duomenis](./media/5ImportData.png)

10. <span data-ttu-id="927ae-128">Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių.</span><span class="sxs-lookup"><span data-stu-id="927ae-128">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="927ae-129">Baigus importuoti uždarykite CMT vediklį.</span><span class="sxs-lookup"><span data-stu-id="927ae-129">After import completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="927ae-130">Patikrinkite savo organizacijos duomenis šiuose 26 objektų:</span><span class="sxs-lookup"><span data-stu-id="927ae-130">Check your organization for data in the following 26 entities:</span></span>

  - <span data-ttu-id="927ae-131">Valiuta</span><span class="sxs-lookup"><span data-stu-id="927ae-131">Currency</span></span>
  - <span data-ttu-id="927ae-132">Sąskaitų diagrama</span><span class="sxs-lookup"><span data-stu-id="927ae-132">Chart of Accounts</span></span>
  - <span data-ttu-id="927ae-133">Finansinis kalendorius</span><span class="sxs-lookup"><span data-stu-id="927ae-133">Fiscal Calendar</span></span>
  - <span data-ttu-id="927ae-134">Valiutos kurso tipai</span><span class="sxs-lookup"><span data-stu-id="927ae-134">Currency Exchange Rate Types</span></span>
  - <span data-ttu-id="927ae-135">Mokėjimo diena</span><span class="sxs-lookup"><span data-stu-id="927ae-135">Payment Day</span></span>
  - <span data-ttu-id="927ae-136">Mokėjimo grafikas</span><span class="sxs-lookup"><span data-stu-id="927ae-136">Payment Schedule</span></span>
  - <span data-ttu-id="927ae-137">Mokėjimo sąlyga</span><span class="sxs-lookup"><span data-stu-id="927ae-137">Payment Term</span></span>
  - <span data-ttu-id="927ae-138">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="927ae-138">Organizational Unit</span></span>
  - <span data-ttu-id="927ae-139">Susisiekite</span><span class="sxs-lookup"><span data-stu-id="927ae-139">Contact</span></span>
  - <span data-ttu-id="927ae-140">Mokesčių grupė</span><span class="sxs-lookup"><span data-stu-id="927ae-140">Tax Group</span></span>
  - <span data-ttu-id="927ae-141">Klientų grupė</span><span class="sxs-lookup"><span data-stu-id="927ae-141">Customer Group</span></span>
  - <span data-ttu-id="927ae-142">Tiekėjų grupė</span><span class="sxs-lookup"><span data-stu-id="927ae-142">Vendor Group</span></span>
  - <span data-ttu-id="927ae-143">Vienetas</span><span class="sxs-lookup"><span data-stu-id="927ae-143">Unit</span></span>
  - <span data-ttu-id="927ae-144">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="927ae-144">Unit Group</span></span>
  - <span data-ttu-id="927ae-145">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="927ae-145">Price List</span></span>
  - <span data-ttu-id="927ae-146">Projekto parametrų kainoraštis</span><span class="sxs-lookup"><span data-stu-id="927ae-146">Project Parameter Price List</span></span>
  - <span data-ttu-id="927ae-147">Sąskaitos faktūros dažnumas</span><span class="sxs-lookup"><span data-stu-id="927ae-147">Invoice Frequency</span></span>
  - <span data-ttu-id="927ae-148">Rezervuojamų išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="927ae-148">Bookable Resource Category</span></span>
  - <span data-ttu-id="927ae-149">Operacijos kategorija</span><span class="sxs-lookup"><span data-stu-id="927ae-149">Transaction Category</span></span>
  - <span data-ttu-id="927ae-150">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="927ae-150">Expense Category</span></span>
  - <span data-ttu-id="927ae-151">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="927ae-151">Role Price</span></span>
  - <span data-ttu-id="927ae-152">Operacijos kategorijos kaina</span><span class="sxs-lookup"><span data-stu-id="927ae-152">Transaction Category Price</span></span>
  - <span data-ttu-id="927ae-153">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="927ae-153">Characteristic</span></span>
  - <span data-ttu-id="927ae-154">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="927ae-154">Bookable Resource</span></span>
  - <span data-ttu-id="927ae-155">Rezervuojamų išteklių kategorijos sąsaja</span><span class="sxs-lookup"><span data-stu-id="927ae-155">Bookable resource category Assn</span></span>
  - <span data-ttu-id="927ae-156">Rezervuojamų išteklių charakteristika</span><span class="sxs-lookup"><span data-stu-id="927ae-156">Bookable Resource Characteristic</span></span>

![Importavimo užbaigimas](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a><span data-ttu-id="927ae-158">„Project Operations“ konfigūracijų naujinimas</span><span class="sxs-lookup"><span data-stu-id="927ae-158">Update Project Operations configurations</span></span>

1. <span data-ttu-id="927ae-159">Eikite į CE aplinką.</span><span class="sxs-lookup"><span data-stu-id="927ae-159">Navigate to the CE environment.</span></span> <span data-ttu-id="927ae-160">Ją rasite atidarę [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/environments), pasirinkę aplinką ir pasirinkę **Atidaryti aplinką**.</span><span class="sxs-lookup"><span data-stu-id="927ae-160">You can find it by opening the [Power Platform Admin Center](https://admin.powerplatform.microsoft.com/environments), selecting the environment, and then selecting **Open Environment**.</span></span> 

![Aplinkos atidarymas](./media/7OpenEnvironment.png)

2. <span data-ttu-id="927ae-162">Eikite į **Projektai** > **Ištekliai**, tada pasirinkite **Naujas**, kad vartotojui sukurtumėte išteklių, kurį galima rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="927ae-162">Go to **Projects** > **Resources** and then select **New** to create a bookable resource for your user.</span></span>

![Rezervuojami ištekliai](./media/8BookableResources.png)

3. <span data-ttu-id="927ae-164">Skirtuke **Bendra** pasirinkite administratoriaus vartotoją.</span><span class="sxs-lookup"><span data-stu-id="927ae-164">On the **General** tab, select your admin user.</span></span> <span data-ttu-id="927ae-165">Patikrinkite, ar laiko juosta atitinka tą, kurioje esate jūs.</span><span class="sxs-lookup"><span data-stu-id="927ae-165">Verify that the time zone matches the one you are in.</span></span> 

![Naujas rezervuojamas išteklius](./media/9NewBookableResource.png)

4. <span data-ttu-id="927ae-167">Skirtuko **Planavimas** lauke **Įmonė** pasirinkite įmonę **USPM** ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="927ae-167">On the **Scheduling** tab, in the **Company** field, pick the **USPM** company, and then select **Save**.</span></span> 

![Planavimo skirtukas](./media/10SchedulingTab.png)

5. <span data-ttu-id="927ae-169">Pasirinkite skirtuką **Darbo valandos**.</span><span class="sxs-lookup"><span data-stu-id="927ae-169">Select the **Work hours** tab.</span></span>  

![Darbo valandos](./media/11WorkHours.png)

6. <span data-ttu-id="927ae-171">Kalendoriuje dukart spustelėkite bet kokią reikšmę ir pasirinkite **Redaguoti** > **Visi sekos įvykiai**.</span><span class="sxs-lookup"><span data-stu-id="927ae-171">Double-click on any value in the calendar and select **Edit** > **All events in the series**.</span></span> 

![Darbo kalendorius](./media/12WorkCalendar.png)

7. <span data-ttu-id="927ae-173">Pakeiskite darbo valandas į aštuonių (8) valandų darbo dieną, pažymėkite savaitgalius kaip ne darbo dienas ir įsitikinkite, kad laiko juosta atitinka jūsų.</span><span class="sxs-lookup"><span data-stu-id="927ae-173">Change work hours to an eight (8) hour work day, mark weekends as non-work days, and make sure time zone matches yours.</span></span> 
8. <span data-ttu-id="927ae-174">Pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="927ae-174">Select **Save and close**.</span></span>

![Kalendoriaus naujinimas](./media/13UpdateCalendar.png)

9. <span data-ttu-id="927ae-176">Eikite į **Parametrai** > **Kalendoriaus šablonas** ir pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="927ae-176">Go to **Settings** > **Calendar templates** and select **New**.</span></span>
 
 ![Kalendoriaus šablonai](./media/14CalendarTemplates.png)
 
 10. <span data-ttu-id="927ae-178">Įveskite pavadinimą, pasirinkite sukurtą šablono išteklių, tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="927ae-178">Enter a name, select the template resource you created, and then select **Save**.</span></span> 
 
 ![Kalendoriaus šablono įrašymas](./media/15SaveCalendarTemplate.png)
 
 11. <span data-ttu-id="927ae-180">Eikite į **Parametrai** ir dukart spustelėkite įrašą.</span><span class="sxs-lookup"><span data-stu-id="927ae-180">Go to **Parameters** and double-click the record.</span></span> 
 
 ![Projekto parametrai](./media/16ProjectParameters.png)
 
12. <span data-ttu-id="927ae-182">Atnaujinkite toliau nurodytus laukus:</span><span class="sxs-lookup"><span data-stu-id="927ae-182">Update the following fields:</span></span>

 - <span data-ttu-id="927ae-183">**Numatytoji įmonė**: USPM</span><span class="sxs-lookup"><span data-stu-id="927ae-183">**Default company**: USPM</span></span>
 - <span data-ttu-id="927ae-184">**Numatytasis organizacijos vienetas**: Contoso Robotics Global</span><span class="sxs-lookup"><span data-stu-id="927ae-184">**Default Organizational Unit**: Contoso Robotics Global</span></span>
 - <span data-ttu-id="927ae-185">**Sąskaitų faktūrų dažnumas**: septintoji diena ir paskutinė diena</span><span class="sxs-lookup"><span data-stu-id="927ae-185">**Invoice Frequency**: Seventh and Last day</span></span>
 - <span data-ttu-id="927ae-186">**Darbo valandų šablonas**: pakeiskite į savo sukurtą šabloną.</span><span class="sxs-lookup"><span data-stu-id="927ae-186">**Work hour template**: Change to the template you created.</span></span>

13. <span data-ttu-id="927ae-187">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="927ae-187">Select **Save**.</span></span> 

![Projekto parametrai atnaujinti](./media/17UpdatedProjectParameters.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
