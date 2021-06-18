---
title: Demonstracinės sąrankos ir konfigūracijos duomenų taikymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip taikyti demonstracinę sąranką ir konfigūracijos programai „Project Operations“.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7729b4a9ef5f498b78af298f7233d7dd45434bb3
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997161"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="f85eb-103">Demonstracinės sąrankos ir konfigūracijos duomenų taikymas naudojant „Project Operations“ – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="f85eb-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="f85eb-104">_\*\* „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą_</span><span class="sxs-lookup"><span data-stu-id="f85eb-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="f85eb-105">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="f85eb-105">Prerequisites</span></span>

<span data-ttu-id="f85eb-106">Prieš pradėdami konfigūraciją, turite turėti „Common Data Service“ (CDS) aplinką, sukonfigūruotą programai „Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="f85eb-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="f85eb-107">Instrukcijos</span><span class="sxs-lookup"><span data-stu-id="f85eb-107">Instructions</span></span>

1. <span data-ttu-id="f85eb-108">Atsisiųskite [pagrindinių duomenų paketą](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span><span class="sxs-lookup"><span data-stu-id="f85eb-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip).</span></span> 
2. <span data-ttu-id="f85eb-109">Eikite į aplanką *ProjOpsSampleSetupData - CE only CMT* ir paleiskite vykdomą failą *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="f85eb-109">Navigate to the folder *ProjOpsSampleSetupData - CE only CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="f85eb-110">„Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="f85eb-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="f85eb-112">CMT vedlio 2 puslapyje pažymėkite **Microsoft 365** kaip **Visuotinio diegimo tipą**.</span><span class="sxs-lookup"><span data-stu-id="f85eb-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="f85eb-113">Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.</span><span class="sxs-lookup"><span data-stu-id="f85eb-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="f85eb-114">Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="f85eb-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="f85eb-116">3 puslapyje iš nuomotojo organizacijų sąrašo pasirinkite į kurią organizaciją norite importuoti demonstracinius duomenis, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="f85eb-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="f85eb-117">4 puslapyje pasirinkite zip. failą *SampleSetupAndConfigData* nesupakuotame aplanke *ProjOpsSampleSetupData - CE only CMT*.</span><span class="sxs-lookup"><span data-stu-id="f85eb-117">On page 4, select the zip file, *SampleSetupAndConfigData* from the unpacked folder, *ProjOpsSampleSetupData - CE only CMT*.</span></span>

   ![Suglaudintas failas](./media/3ZipFile.png)

   ![Pasirinkti failą](./media/4SelectAFile.png)

9. <span data-ttu-id="f85eb-120">Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="f85eb-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importuoti duomenis](./media/5ImportData.png)

10. <span data-ttu-id="f85eb-122">Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių.</span><span class="sxs-lookup"><span data-stu-id="f85eb-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="f85eb-123">Baigę importuoti uždarykite CMT vediklį.</span><span class="sxs-lookup"><span data-stu-id="f85eb-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="f85eb-124">Patikrinkite savo organizacijos duomenis šiuose 18 objektų:</span><span class="sxs-lookup"><span data-stu-id="f85eb-124">Check your organization for data in the following 18 entities:</span></span>

    -   <span data-ttu-id="f85eb-125">Valiuta</span><span class="sxs-lookup"><span data-stu-id="f85eb-125">Currency</span></span>
    -   <span data-ttu-id="f85eb-126">Paskyra</span><span class="sxs-lookup"><span data-stu-id="f85eb-126">Account</span></span>
    -   <span data-ttu-id="f85eb-127">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="f85eb-127">Organizational Unit</span></span>
    -   <span data-ttu-id="f85eb-128">Susisiekite</span><span class="sxs-lookup"><span data-stu-id="f85eb-128">Contact</span></span>
    -   <span data-ttu-id="f85eb-129">Vienetas</span><span class="sxs-lookup"><span data-stu-id="f85eb-129">Unit</span></span>
    -   <span data-ttu-id="f85eb-130">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="f85eb-130">Unit Group</span></span>
    -   <span data-ttu-id="f85eb-131">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="f85eb-131">Price List</span></span>
    -   <span data-ttu-id="f85eb-132">Projekto parametrų kainoraštis</span><span class="sxs-lookup"><span data-stu-id="f85eb-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="f85eb-133">Sąskaitos faktūros dažnumas</span><span class="sxs-lookup"><span data-stu-id="f85eb-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="f85eb-134">Rezervuojamų išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="f85eb-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="f85eb-135">Operacijos kategorija</span><span class="sxs-lookup"><span data-stu-id="f85eb-135">Transaction Category</span></span>
    -   <span data-ttu-id="f85eb-136">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="f85eb-136">Expense Category</span></span>
    -   <span data-ttu-id="f85eb-137">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="f85eb-137">Role Price</span></span>
    -   <span data-ttu-id="f85eb-138">Operacijos kategorijos kaina</span><span class="sxs-lookup"><span data-stu-id="f85eb-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="f85eb-139">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="f85eb-139">Characteristic</span></span>
    -   <span data-ttu-id="f85eb-140">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="f85eb-140">Bookable Resource</span></span>
    -   <span data-ttu-id="f85eb-141">Rezervuojamų išteklių kategorijos sąsaja</span><span class="sxs-lookup"><span data-stu-id="f85eb-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="f85eb-142">Rezervuojamų išteklių charakteristika</span><span class="sxs-lookup"><span data-stu-id="f85eb-142">Bookable Resource Characteristic</span></span>

    ![Importavimo užbaigimas](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
