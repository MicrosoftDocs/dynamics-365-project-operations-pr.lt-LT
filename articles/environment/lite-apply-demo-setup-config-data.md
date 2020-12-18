---
title: Demonstracinės sąrankos ir konfigūracijos duomenų taikymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip taikyti demonstracinę sąranką ir konfigūracijos programai „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 421c9d28088c92617687641d93b3ad5d6bfea73c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642103"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a><span data-ttu-id="ba8bd-103">Demonstracinės sąrankos ir konfigūracijos duomenų taikymas naudojant „Project Operations“ – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="ba8bd-103">Apply demo setup and configuration data for Project Operations - lite</span></span> 

<span data-ttu-id="ba8bd-104">_\*\* „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą_</span><span class="sxs-lookup"><span data-stu-id="ba8bd-104">_\*\*Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

## <a name="prerequisites"></a><span data-ttu-id="ba8bd-105">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="ba8bd-105">Prerequisites</span></span>

<span data-ttu-id="ba8bd-106">Prieš pradėdami konfigūraciją, turite turėti „Common Data Service“ (CDS) aplinką, sukonfigūruotą programai „Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-106">Before you begin the configuration, you must have a Common Data Service (CDS) environment provisioned for Dynamics 365 Project Operations.</span></span>


## <a name="instructions"></a><span data-ttu-id="ba8bd-107">Instrukcijos</span><span class="sxs-lookup"><span data-stu-id="ba8bd-107">Instructions</span></span>

1. <span data-ttu-id="ba8bd-108">Atsisiųskite [pagrindinių duomenų paketą](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span><span class="sxs-lookup"><span data-stu-id="ba8bd-108">Download the [Master Data Package](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip).</span></span> 
2. <span data-ttu-id="ba8bd-109">Eikite į aplanką *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ir vykdykite vykdomą failą *DataMigrationUtility*.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-109">Navigate to the folder *ProjOpsDemoDataSetupAndMaster - Integrated CMT* and run the executable file, *DataMigrationUtility*.</span></span>
3. <span data-ttu-id="ba8bd-110">„Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-110">On page 1 of the Common Data Service Configuration Migration (CMT) Wizard, select **Import Data** and then select **Continue**.</span></span>

![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. <span data-ttu-id="ba8bd-112">CMT vedlio 2 puslapyje pažymėkite **Microsoft 365** kaip **Visuotinio diegimo tipą**.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-112">On Page 2 of the CMT Wizard, select **Microsoft 365** as the **Deployment Type**.</span></span>
5. <span data-ttu-id="ba8bd-113">Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-113">Select the **Display a list of available organizations** and **Show Advanced** check boxes.</span></span>
6. <span data-ttu-id="ba8bd-114">Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-114">Select the region of your tenant, enter your credentials, and then select **Login**.</span></span>

![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. <span data-ttu-id="ba8bd-116">3 puslapyje iš nuomotojo organizacijų sąrašo pasirinkite į kurią organizaciją norite importuoti demonstracinius duomenis, o tada pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-116">On page 3, from the list of Organizations on the Tenant, select which organization you want to import the demo data into and then select **Login**.</span></span>
8. <span data-ttu-id="ba8bd-117">4 puslapyje pasirinkite suglaudintą failą *MasterAndSetupData*, esantį išpakuotame aplanke *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-117">On page 4, select the zip file, *MasterAndSetupData* from the unpacked folder, *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.</span></span>

![Suglaudintas failas](./media/3ZipFile.png)

![Pasirinkite failą](./media/4SelectAFile.png)

9. <span data-ttu-id="ba8bd-120">Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-120">After the zip file is selected, select **Import Data**.</span></span>

![Importuoti duomenis](./media/5ImportData.png)

10. <span data-ttu-id="ba8bd-122">Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-122">Import will run for approximately two-ten minutes depending on your network speed.</span></span> <span data-ttu-id="ba8bd-123">Baigę importuoti uždarykite CMT vediklį.</span><span class="sxs-lookup"><span data-stu-id="ba8bd-123">After it completes, exit the CMT Wizard.</span></span> 
11. <span data-ttu-id="ba8bd-124">Patikrinkite savo organizacijos duomenis šiuose 20 objektų:</span><span class="sxs-lookup"><span data-stu-id="ba8bd-124">Check your organization for data in the following 20 entities:</span></span>

-   <span data-ttu-id="ba8bd-125">Valiuta</span><span class="sxs-lookup"><span data-stu-id="ba8bd-125">Currency</span></span>
-   <span data-ttu-id="ba8bd-126">Paskyra</span><span class="sxs-lookup"><span data-stu-id="ba8bd-126">Account</span></span>
-   <span data-ttu-id="ba8bd-127">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="ba8bd-127">Organizational Unit</span></span>
-   <span data-ttu-id="ba8bd-128">Susisiekite</span><span class="sxs-lookup"><span data-stu-id="ba8bd-128">Contact</span></span>
-   <span data-ttu-id="ba8bd-129">Mokesčių grupė</span><span class="sxs-lookup"><span data-stu-id="ba8bd-129">Tax Group</span></span>
-   <span data-ttu-id="ba8bd-130">Klientų grupė</span><span class="sxs-lookup"><span data-stu-id="ba8bd-130">Customer Group</span></span>
-   <span data-ttu-id="ba8bd-131">Vienetas</span><span class="sxs-lookup"><span data-stu-id="ba8bd-131">Unit</span></span>
-   <span data-ttu-id="ba8bd-132">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="ba8bd-132">Unit Group</span></span>
-   <span data-ttu-id="ba8bd-133">Kainoraštis</span><span class="sxs-lookup"><span data-stu-id="ba8bd-133">Price List</span></span>
-   <span data-ttu-id="ba8bd-134">Projekto parametrų kainoraštis</span><span class="sxs-lookup"><span data-stu-id="ba8bd-134">Project Parameter Price List</span></span> 
-   <span data-ttu-id="ba8bd-135">Sąskaitos faktūros dažnumas</span><span class="sxs-lookup"><span data-stu-id="ba8bd-135">Invoice Frequency</span></span>
-   <span data-ttu-id="ba8bd-136">Rezervuojamų išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="ba8bd-136">Bookable Resource Category</span></span>
-   <span data-ttu-id="ba8bd-137">Operacijos kategorija</span><span class="sxs-lookup"><span data-stu-id="ba8bd-137">Transaction Category</span></span>
-   <span data-ttu-id="ba8bd-138">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="ba8bd-138">Expense Category</span></span>
-   <span data-ttu-id="ba8bd-139">Vaidmens kaina</span><span class="sxs-lookup"><span data-stu-id="ba8bd-139">Role Price</span></span>
-   <span data-ttu-id="ba8bd-140">Operacijos kategorijos kaina</span><span class="sxs-lookup"><span data-stu-id="ba8bd-140">Transaction Category Price</span></span>
-   <span data-ttu-id="ba8bd-141">Charakteristika</span><span class="sxs-lookup"><span data-stu-id="ba8bd-141">Characteristic</span></span>
-   <span data-ttu-id="ba8bd-142">Rezervuojamas išteklius</span><span class="sxs-lookup"><span data-stu-id="ba8bd-142">Bookable Resource</span></span>
-   <span data-ttu-id="ba8bd-143">Rezervuojamų išteklių kategorijos sąsaja</span><span class="sxs-lookup"><span data-stu-id="ba8bd-143">Bookable resource category Assn</span></span>
-   <span data-ttu-id="ba8bd-144">Rezervuojamų išteklių charakteristika</span><span class="sxs-lookup"><span data-stu-id="ba8bd-144">Bookable Resource Characteristic</span></span>

![Importavimo užbaigimas](./media/6CompleteImport.png)
