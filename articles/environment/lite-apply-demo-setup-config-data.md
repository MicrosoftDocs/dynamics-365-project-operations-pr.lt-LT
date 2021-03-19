---
title: Demonstracinės sąrankos ir konfigūracijos duomenų taikymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip taikyti demonstracinę sąranką ir konfigūracijos programai „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 01/27/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 694dbc74591de74895095a9da6e590069711fc83
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290144"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="9ef9b-103">Demonstracinės sąrankos ir konfigūracijos duomenų taikymas naudojant „Project Operations“ – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="9ef9b-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="9ef9b-104">_\*\* „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą_</span><span class="sxs-lookup"><span data-stu-id="9ef9b-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="9ef9b-105">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="9ef9b-105">Prerequisites</span></span>

<span data-ttu-id="9ef9b-106">Prieš pradėdami konfigūraciją, turite turėti „Common Data Service“ (CDS) aplinką, sukonfigūruotą programai „Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="9ef9b-107">Instrukcijos</span><span class="sxs-lookup"><span data-stu-id="9ef9b-107">Instructions</span></span>

1. <span data-ttu-id="9ef9b-108">Atsisiųskite [pagrindinių duomenų paketą](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="9ef9b-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="9ef9b-109">Eikite į aplanką *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ir vykdykite vykdomą failą *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="9ef9b-110">„Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

    ![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="9ef9b-112">CMT vedlio 2 puslapyje pažymėkite **Microsoft 365** kaip **Visuotinio diegimo tipą**.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="9ef9b-113">Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="9ef9b-114">Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

   ![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="9ef9b-116">3 puslapyje iš nuomotojo organizacijų sąrašo pasirinkite į kurią organizaciją norite importuoti demonstracinius duomenis, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="9ef9b-117">4 puslapyje pasirinkite suglaudintą failą *MasterAndSetupData*, esantį išpakuotame aplanke *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

   ![Suglaudintas failas](./media/3ZipFile.png)

   ![Pasirinkite failą](./media/4SelectAFile.png)

9. <span data-ttu-id="9ef9b-120">Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-120">After the zip file is selected, select **Import Data**.</span></span>

   ![Importuoti duomenis](./media/5ImportData.png)

10. <span data-ttu-id="9ef9b-122">Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="9ef9b-123">Baigę importuoti uždarykite CMT vediklį.</span><span class="sxs-lookup"><span data-stu-id="9ef9b-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="9ef9b-124">Patikrinkite savo organizacijos duomenis šiuose 20 objektų:</span><span class="sxs-lookup"><span data-stu-id="9ef9b-124">Check your organization for data in the following 20 entities:</span></span>

    -   <span data-ttu-id="9ef9b-125">Valiuta</span><span class="sxs-lookup"><span data-stu-id="9ef9b-125">Currency</span></span>
    -   <span data-ttu-id="9ef9b-126">Paskyra</span><span class="sxs-lookup"><span data-stu-id="9ef9b-126">Account</span></span>
    -   <span data-ttu-id="9ef9b-127">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="9ef9b-127">Organizational Unit</span></span>
    -   <span data-ttu-id="9ef9b-128">Susisiekite</span><span class="sxs-lookup"><span data-stu-id="9ef9b-128">Contact</span></span>
    -   <span data-ttu-id="9ef9b-129">Vienetas</span><span class="sxs-lookup"><span data-stu-id="9ef9b-129">Unit</span></span>
    -   <span data-ttu-id="9ef9b-130">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="9ef9b-130">Unit Group</span></span>
    -   <span data-ttu-id="9ef9b-131">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="9ef9b-131">Price List</span></span>
    -   <span data-ttu-id="9ef9b-132">Projekto parametrų kainoraštis</span><span class="sxs-lookup"><span data-stu-id="9ef9b-132">Project Parameter Price List</span></span> 
    -   <span data-ttu-id="9ef9b-133">Sąskaitos faktūros dažnumas</span><span class="sxs-lookup"><span data-stu-id="9ef9b-133">Invoice Frequency</span></span>
    -   <span data-ttu-id="9ef9b-134">Rezervuojamų išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="9ef9b-134">Bookable Resource Category</span></span>
    -   <span data-ttu-id="9ef9b-135">Operacijos kategorija</span><span class="sxs-lookup"><span data-stu-id="9ef9b-135">Transaction Category</span></span>
    -   <span data-ttu-id="9ef9b-136">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="9ef9b-136">Expense Category</span></span>
    -   <span data-ttu-id="9ef9b-137">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="9ef9b-137">Role Price</span></span>
    -   <span data-ttu-id="9ef9b-138">Operacijos kategorijos kaina</span><span class="sxs-lookup"><span data-stu-id="9ef9b-138">Transaction Category Price</span></span>
    -   <span data-ttu-id="9ef9b-139">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="9ef9b-139">Characteristic</span></span>
    -   <span data-ttu-id="9ef9b-140">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="9ef9b-140">Bookable Resource</span></span>
    -   <span data-ttu-id="9ef9b-141">Rezervuojamų išteklių kategorijos sąsaja</span><span class="sxs-lookup"><span data-stu-id="9ef9b-141">Bookable resource category Assn</span></span>
    -   <span data-ttu-id="9ef9b-142">Rezervuojamų išteklių charakteristika</span><span class="sxs-lookup"><span data-stu-id="9ef9b-142">Bookable Resource Characteristic</span></span>

    ![Importavimo užbaigimas](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]