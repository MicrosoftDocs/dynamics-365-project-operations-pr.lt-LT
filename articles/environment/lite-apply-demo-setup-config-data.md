---
title: Demonstracinės sąrankos ir konfigūracijos duomenų taikymas
description: Šioje temoje pateikta informacija apie tai, kaip taikyti demonstracinę sąranką ir konfigūracijos programai „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 33b85115963f3561718b8951e5b518fd34de7723
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080701"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="3044b-103">Demonstracinės sąrankos ir konfigūracijos duomenų taikymas „Project Operations“ programos „lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros formą</span><span class="sxs-lookup"><span data-stu-id="3044b-103">Apply demo setup and configuration data for Project Operations lite deployment - deal to proforma invoicing</span></span>

<span data-ttu-id="3044b-104">_\*\* „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą_</span><span class="sxs-lookup"><span data-stu-id="3044b-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

1. <span data-ttu-id="3044b-105">Atsisiųskite [pagrindinių duomenų paketą](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="3044b-105">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="3044b-106">Eikite į aplanką *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ir vykdykite vykdomą failą *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="3044b-106">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="3044b-107">„Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis** , o tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="3044b-107">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="3044b-109">CMT vedlio 2 puslapyje pažymėkite **Microsoft 365** kaip **Visuotinio diegimo tipą**.</span><span class="sxs-lookup"><span data-stu-id="3044b-109">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="3044b-110">Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.</span><span class="sxs-lookup"><span data-stu-id="3044b-110">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="3044b-111">Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="3044b-111">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="3044b-113">3 puslapyje iš nuomotojo organizacijų sąrašo pasirinkite į kurią organizaciją norite importuoti demonstracinius duomenis, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="3044b-113">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="3044b-114">4 puslapyje pasirinkite suglaudintą failą *MasterAndSetupData* , esantį išpakuotame aplanke *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="3044b-114">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Suglaudintas failas](./media/3ZipFile.png)

![Pasirinkite failą](./media/4SelectAFile.png)

9. <span data-ttu-id="3044b-117">Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="3044b-117">After the zip file is selected, select **Import Data**.</span></span>

![Importuoti duomenis](./media/5ImportData.png)

10. <span data-ttu-id="3044b-119">Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių.</span><span class="sxs-lookup"><span data-stu-id="3044b-119">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="3044b-120">Baigę importuoti uždarykite CMT vediklį.</span><span class="sxs-lookup"><span data-stu-id="3044b-120">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="3044b-121">Patikrinkite savo organizacijos duomenis šiuose 20 objektų:</span><span class="sxs-lookup"><span data-stu-id="3044b-121">Check your organization for data in the following 20 entities:</span></span>

- <span data-ttu-id="3044b-122">Valiuta</span><span class="sxs-lookup"><span data-stu-id="3044b-122">Currency</span></span>
- <span data-ttu-id="3044b-123">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="3044b-123">Organizational Unit</span></span>
- <span data-ttu-id="3044b-124">Susisiekite</span><span class="sxs-lookup"><span data-stu-id="3044b-124">Contact</span></span>
- <span data-ttu-id="3044b-125">Mokesčių grupė</span><span class="sxs-lookup"><span data-stu-id="3044b-125">Tax Group</span></span>
- <span data-ttu-id="3044b-126">Klientų grupė</span><span class="sxs-lookup"><span data-stu-id="3044b-126">Customer Group</span></span>
- <span data-ttu-id="3044b-127">Vienetas</span><span class="sxs-lookup"><span data-stu-id="3044b-127">Unit</span></span>
- <span data-ttu-id="3044b-128">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="3044b-128">Unit Group</span></span>
- <span data-ttu-id="3044b-129">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="3044b-129">Price List</span></span>
- <span data-ttu-id="3044b-130">Projekto parametrų kainoraštis</span><span class="sxs-lookup"><span data-stu-id="3044b-130">Project Parameter Price List</span></span>
- <span data-ttu-id="3044b-131">Sąskaitos faktūros dažnumas</span><span class="sxs-lookup"><span data-stu-id="3044b-131">Invoice Frequency</span></span>
- <span data-ttu-id="3044b-132">Sąskaitos faktūros dažnumo informacija</span><span class="sxs-lookup"><span data-stu-id="3044b-132">Invoice Frequency Detail</span></span>
- <span data-ttu-id="3044b-133">Rezervuojamų išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="3044b-133">Bookable Resource Category</span></span>
- <span data-ttu-id="3044b-134">Operacijos kategorija</span><span class="sxs-lookup"><span data-stu-id="3044b-134">Transaction Category</span></span>
- <span data-ttu-id="3044b-135">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="3044b-135">Expense Category</span></span>
- <span data-ttu-id="3044b-136">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="3044b-136">Role Price</span></span>
- <span data-ttu-id="3044b-137">Operacijos kategorijos kaina</span><span class="sxs-lookup"><span data-stu-id="3044b-137">Transaction Category Price</span></span>
- <span data-ttu-id="3044b-138">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="3044b-138">Characteristic</span></span>
- <span data-ttu-id="3044b-139">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="3044b-139">Bookable Resource</span></span>
- <span data-ttu-id="3044b-140">Rezervuojamų išteklių kategorijos sąsaja</span><span class="sxs-lookup"><span data-stu-id="3044b-140">Bookable resource category Assn</span></span>
- <span data-ttu-id="3044b-141">Rezervuojamų išteklių charakteristika</span><span class="sxs-lookup"><span data-stu-id="3044b-141">Bookable Resource Characteristic</span></span>

![Importavimo užbaigimas](./media/6CompleteImport.png)
