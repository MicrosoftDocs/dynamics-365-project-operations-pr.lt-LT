---
title: „Project Operations“ demonstracinių duomenų taikymas debesyje esančioje „Finance“ aplinkoje
description: Šioje temoje aiškinama, kaip taikyti demonstracinius „Project Operations“ duomenis „Dynamics 365 Finance“ debesyje esančioje aplinkoje.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b9af6c71b61840f4ffdf2892d8e7e5bbf0f8df67
ms.sourcegitcommit: 91ad491e94a421f256a378b0f4b26ed48c67bc93
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/22/2020
ms.locfileid: "4096632"
---
# <a name="apply-project-operations-demo-data-to-a-finance-cloud-hosted-environment"></a><span data-ttu-id="16927-103">„Project Operations“ demonstracinių duomenų taikymas debesyje esančioje „Finance“ aplinkoje</span><span class="sxs-lookup"><span data-stu-id="16927-103">Apply Project Operations demo data to a Finance Cloud-hosted environment</span></span>

<span data-ttu-id="16927-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="16927-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="16927-105">Ši tema taikoma tik 10.0.13 versijos „Microsoft Dynamics 365 Finance“ ir veiksmus galima atlikti tik debesyje esančiai aplinkai.</span><span class="sxs-lookup"><span data-stu-id="16927-105">This topic is only applicable only Microsoft Dynamics 365 Finance version 10.0.13 and can be performed only on a Cloud-hosted environment.</span></span> <span data-ttu-id="16927-106">Atlikite šioje temoje aprašytus veiksmus **PRIEŠ** taikydami kokybinius naujinimus aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="16927-106">Complete the steps in this topic **BEFORE** you apply quality updates to the environment.</span></span>

1. <span data-ttu-id="16927-107">LCS projekte atidarykite puslapį **Išsami aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="16927-107">In your LCS project, open the **Environment details** page.</span></span> <span data-ttu-id="16927-108">Atkreipkite dėmesį, kad jame yra išsami informacija, kurios reikia norint prisijungti prie aplinkos naudojant nuotolinio darbalaukio protokolą (RDP).</span><span class="sxs-lookup"><span data-stu-id="16927-108">Notice that it includes the details needed to connect to the environment by using Remote Desktop Protocol (RDP).</span></span>

![Išsami „“ aplinkos informacija](./media/1EnvironmentDetails.png)

<span data-ttu-id="16927-110">Pirmasis paryškintų kredencialų rinkinys yra vietinės paskyros kredencialai ir turi nuotolinio darbalaukio hipersaitą.</span><span class="sxs-lookup"><span data-stu-id="16927-110">The first set of highlighted credentials are the local account credentials and contain a hyperlink to the remote desktop connection.</span></span> <span data-ttu-id="16927-111">Kredencialai apima aplinkos administratoriaus vartotojo vardą ir slaptažodį.</span><span class="sxs-lookup"><span data-stu-id="16927-111">The credentials include the environment admin username and password.</span></span> <span data-ttu-id="16927-112">Antrasis kredencialų rinkinys naudojamas siekiant prisijungti prie „SQL Server“ šioje aplinkoje.</span><span class="sxs-lookup"><span data-stu-id="16927-112">The second set of credentials are used to log in to SQL Server in this environment.</span></span>

2. <span data-ttu-id="16927-113">Prisijunkite nuotoliniu būdu prie aplinkos naudodami hipersaitą, esantį dalyje **Vietinės paskyros** , ir naudokite **Vietinės paskyros kredencialai** , kad atliktumėte autentifikavimą.</span><span class="sxs-lookup"><span data-stu-id="16927-113">Remote to the environment by the hyperlink in **Local Accounts** , and use the **Local Account credentials** to authenticate.</span></span>
3. <span data-ttu-id="16927-114">Eikite į **Informacinės interneto paslaugos** > **Programų telkiniai** > **AOSService** ir sustabdykite tarnybą.</span><span class="sxs-lookup"><span data-stu-id="16927-114">Go to **Internet Information Services** > **Application Pools** > **AOSService** and stop the service.</span></span> <span data-ttu-id="16927-115">Dabar sustabdėte šią tarnybą, kad galėtumėte tęsti SQL duomenų bazės pakeitimo procesą.</span><span class="sxs-lookup"><span data-stu-id="16927-115">You are stopping the service at this point so that you can continue to replace the SQL database.</span></span>

![Sustabdyti AOS](./media/2StopAOS.png)

4. <span data-ttu-id="16927-117">Eikite į **Tarnybos** ir sustabdykite du toliau nurodytus elementus:</span><span class="sxs-lookup"><span data-stu-id="16927-117">Go to **Services** and stop the following two items:</span></span>

- <span data-ttu-id="16927-118">„Microsoft Dynamics 365 Unified Operations“: paketų valdymo tarnyba</span><span class="sxs-lookup"><span data-stu-id="16927-118">Microsoft Dynamics 365 Unified Operations: Batch Management Service</span></span>
- <span data-ttu-id="16927-119">„Microsoft Dynamics 365 Unified Operations“: duomenų importavimo / eksportavimo sistema</span><span class="sxs-lookup"><span data-stu-id="16927-119">Microsoft Dynamics 365 Unified Operations: Data Import Export Framework</span></span>

![Sustabdyti tarnybas](./media/3StopServices.png)

5. <span data-ttu-id="16927-121">Atidarykite „Microsoft SQL Server Management Studio“.</span><span class="sxs-lookup"><span data-stu-id="16927-121">Open Microsoft SQL Server Management Studio.</span></span> <span data-ttu-id="16927-122">Prisijunkite naudodami SQL serverio kredencialus ir naudokite axdbadmin vartotojo vardą ir slaptažodį iš LCS puslapio **Išsami aplinkos informacija**.</span><span class="sxs-lookup"><span data-stu-id="16927-122">Log in with SQL server credentials and use the axdbadmin user and password from the LCS **Environments details** page.</span></span>

![„SQL Server Management Studio“](./media/4SSMS.png)

6. <span data-ttu-id="16927-124">Objektų naršyklėje raskite **Duomenų bazės** ir raskite **AXDB**.</span><span class="sxs-lookup"><span data-stu-id="16927-124">In Object Explorer, **Databases** and locate **AXDB**.</span></span> <span data-ttu-id="16927-125">Duomenų bazę pakeisite nauja duomenų baze, esančia [Atsisiuntimo centre](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span><span class="sxs-lookup"><span data-stu-id="16927-125">You will replace database with a new database that is located in the [Download Center](https://download.microsoft.com/download/1/a/3/1a314bd2-b082-4a87-abdc-1ba26c92b63d/ProjOpsDemoDataFOGARelease.zip).</span></span> 
7. <span data-ttu-id="16927-126">Nukopijuokite suglaudintą failą į VM, prie kurios esate prisijungę nuotoliniu būdu, ir išskleiskite suglaudinto failo turinį.</span><span class="sxs-lookup"><span data-stu-id="16927-126">Copy the zip file to the VM you are remoted into and extract zip contents.</span></span>
8. <span data-ttu-id="16927-127">„SQL Server Management Studio“ spustelėkite dešiniuoju pelės mygtuku **AxDB** , tada pasirinkite **Užduotys** > **Atkūrimas** > **Duomenų bazė**.</span><span class="sxs-lookup"><span data-stu-id="16927-127">In SQL Server Management Studio, right-click **AxDB** , and then select **Tasks** > **Restore** > **Database**.</span></span>

![Duomenų bazės atkūrimas](./media/5RestoreDatabase.png)

9. <span data-ttu-id="16927-129">Pasirinkite **Šaltinio įrenginys** ir eikite į failą, kurį išskleidėte iš nukopijuoto suglaudinto failo.</span><span class="sxs-lookup"><span data-stu-id="16927-129">Select **Source Device** and navigate to the file extracted from zip you copied.</span></span>

![Šaltinio įrenginiai](./media/6SourceDevice.png)

10. <span data-ttu-id="16927-131">Pasirinkite **Parinktys** , tada pasirinkite **Perrašyti esamą duomenų bazę** ir **Uždaryti esamus ryšius su paskirties duomenų baze**.</span><span class="sxs-lookup"><span data-stu-id="16927-131">Select **Options** , and then select **Overwrite the existing database** and **Close existing connections to destination database**.</span></span> 
11. <span data-ttu-id="16927-132">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="16927-132">Select **OK**.</span></span>

![Parametrų atkūrimas](./media/7RestoreSetting.png)

<span data-ttu-id="16927-134">Gausite patvirtinimą, kad AXDB atkūrimas atliktas sėkmingai.</span><span class="sxs-lookup"><span data-stu-id="16927-134">You will receive confirmation that the AXDB restore was successful.</span></span> <span data-ttu-id="16927-135">Gavę šį patvirtinimą galite uždaryti „SQL Services Management Studio“.</span><span class="sxs-lookup"><span data-stu-id="16927-135">After you receive this confirmation, you can close SQL Services Management Studio.</span></span>

12. <span data-ttu-id="16927-136">Grįžkite atgal į **Informacinės interneto paslaugos** > **Programų telkiniai** > **AOSService** ir paleiskite AOSService.</span><span class="sxs-lookup"><span data-stu-id="16927-136">Go back to **Internet Information Services** > **Application Pools** > **AOSService** and start the AOSService.</span></span>
13. <span data-ttu-id="16927-137">Eikite į **Tarnybos** ir paleiskite dvi tarnybas, kurias buvote sustabdę anksčiau.</span><span class="sxs-lookup"><span data-stu-id="16927-137">Go to **Services** and start the two services you stopped earlier.</span></span>

14. <span data-ttu-id="16927-138">Šioje VM raskite įrankį AdminUserProvisioning.</span><span class="sxs-lookup"><span data-stu-id="16927-138">Locate the AdminUserProvisioning tool on this VM.</span></span> <span data-ttu-id="16927-139">Ieškokite dalyje K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span><span class="sxs-lookup"><span data-stu-id="16927-139">Look under, K:\AosService\PackagesLocalDirectory\bin\AdminUserProvisioning.exe.</span></span>
15. <span data-ttu-id="16927-140">Vykdykite .ext failą naudodami savo vartotojo adresą, nurodytą lauke **El. pašto adresas**.</span><span class="sxs-lookup"><span data-stu-id="16927-140">Run the .ext file using your user address in the **Email Address** field.</span></span> 
16. <span data-ttu-id="16927-141">Pasirinkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="16927-141">Select **Submit**.</span></span>

![Administratoriaus vartotojo parengimas](./media/8AdminUserProvisioning.png)

<span data-ttu-id="16927-143">Tai užtruks keletą minučių.</span><span class="sxs-lookup"><span data-stu-id="16927-143">This takes a couple of minutes to complete.</span></span> <span data-ttu-id="16927-144">Turėtumėte gauti patvirtinimo pranešimą, kad administratoriaus vartotojas sėkmingai atnaujintas.</span><span class="sxs-lookup"><span data-stu-id="16927-144">You should receive a confirmation message that the Admin user was successfully updated.</span></span>

17. <span data-ttu-id="16927-145">Galiausiai paleiskite komandinę eilutę kaip administratorius ir atlikite iisreset</span><span class="sxs-lookup"><span data-stu-id="16927-145">Lastly, run Command Prompt as Administrator and perform iisreset</span></span>

![IIS nustatymas iš naujo](./media/9IISReset.png)

18. <span data-ttu-id="16927-147">Uždarykite nuotolinio darbalaukio seansą ir naudokite LCS puslapį **Išsami aplinkos informacija** , kad prisijungtumėte prie aplinkos ir įsitikintumėte, kad ji veikia taip, kaip tikimasi.</span><span class="sxs-lookup"><span data-stu-id="16927-147">Close the remote desktop session and use the LCS **Environment details** page to log in to the environment to confirm it is working as expected.</span></span>

![Finance and Operations](./media/10FinanceAndOperations.png)
