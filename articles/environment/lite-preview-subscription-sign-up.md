---
title: Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip prenumeruoti ir diegti „Project Operations Lite“ visuotinį diegimą – sandoris į išankstinės sąskaitos faktūros formą.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334792"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a><span data-ttu-id="7919c-103">Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="7919c-103">Sign up for a preview subscription - lite</span></span> 

<span data-ttu-id="7919c-104">Šioje temoje paaiškinama, kaip užsiprenumeruoti bandomajam pasiūlymui ir įdiegti „Dynamics 365 Project Operations“ „Lite“ įdiegtį – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo.</span><span class="sxs-lookup"><span data-stu-id="7919c-104">This topic explains how to subscribe to the trial offer and deploy Dynamics 365 Project Operations lite deployment - deal to proforma invoicing.</span></span>

> [!NOTE]
> <span data-ttu-id="7919c-105">Šis procesas pasikeis būsimuose „Project Operations“ leidimuose.</span><span class="sxs-lookup"><span data-stu-id="7919c-105">This process will change in upcoming releases of Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="7919c-106">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="7919c-106">Prerequisites</span></span>
- <span data-ttu-id="7919c-107">Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises.</span><span class="sxs-lookup"><span data-stu-id="7919c-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="7919c-108">Pasinaudodami pirmuoju pasiūlymu, galite sukurti nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="7919c-108">You can create a tenant during the first offer redemption.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7919c-109">Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="7919c-109">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="7919c-110">Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="7919c-110">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="7919c-111">Bandomosios versijos nuomotojuje yra vienkartinės.</span><span class="sxs-lookup"><span data-stu-id="7919c-111">Trials are single use in the tenant.</span></span> <span data-ttu-id="7919c-112">Bandomąją versiją galite paleisti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="7919c-112">You can only run a trial one time.</span></span> <span data-ttu-id="7919c-113">Bandomajai versijai rekomenduojame sukurti naują nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="7919c-113">We recommend that you create a new tenant for the purpose of the trial.</span></span>

### <a name="dynamics-365-project-operations-trial"></a><span data-ttu-id="7919c-114">„Dynamics 365 Project Operations“ bandomoji versija</span><span class="sxs-lookup"><span data-stu-id="7919c-114">Dynamics 365 Project Operations trial</span></span> 

<span data-ttu-id="7919c-115">Prieš pradėdami įsitikinkite, kad esate prisijungę prie naršyklės naudodami vartotojo darbo klientą nuomotojuje, kuriame norite atlikti „Project Operations“ peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="7919c-115">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="7919c-116">Eikite į [„Project Operations“ bandomoji versija](https://aka.ms/try-po), kad panaudotumėte pirmąjį pasiūlymo kodą – **„Dynamics 365 Project Operations“**.</span><span class="sxs-lookup"><span data-stu-id="7919c-116">Go to [Project Operations Trial](https://aka.ms/try-po) to redeem the first offer code, **Dynamics 365 Project Operations**.</span></span>
2. <span data-ttu-id="7919c-117">Patvirtinkite užsakymą.</span><span class="sxs-lookup"><span data-stu-id="7919c-117">Confirm your order.</span></span>

  <span data-ttu-id="7919c-118">Pamatysite, kad patvirtinimo pasiūlymu sėkmingai pasinaudota.</span><span class="sxs-lookup"><span data-stu-id="7919c-118">You'll see the confirmation offer was successfully redeemed.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="7919c-119">Licencijų priskyrimas</span><span class="sxs-lookup"><span data-stu-id="7919c-119">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="7919c-120">Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365 Portal“.</span><span class="sxs-lookup"><span data-stu-id="7919c-120">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>


1. <span data-ttu-id="7919c-121">Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas vartotojams.</span><span class="sxs-lookup"><span data-stu-id="7919c-121">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>
2. <span data-ttu-id="7919c-122">Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.</span><span class="sxs-lookup"><span data-stu-id="7919c-122">On the **Active users** page, select the users that you want to assign a license to.</span></span>
3. <span data-ttu-id="7919c-123">Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“** licencija.</span><span class="sxs-lookup"><span data-stu-id="7919c-123">Verify that the **Dynamics 365 Project Operations** license is selected.</span></span> 
4. <span data-ttu-id="7919c-124">Pasirinkite **Įrašyti pakeitimus**.</span><span class="sxs-lookup"><span data-stu-id="7919c-124">Select **Save changes**.</span></span>

## <a name="create-a-new-dataverse-environment"></a><span data-ttu-id="7919c-125">Naujos „Dataverse” aplinkos kūrimas</span><span class="sxs-lookup"><span data-stu-id="7919c-125">Create a new Dataverse environment</span></span>

1. <span data-ttu-id="7919c-126">Parenkite naują „Project Operations“ „Dataverse“ visuotinio diegimo aplinką sekdami šioje temoje pateiktas instrukcijas – [„Dataverse“ visuotinio diegimo modelis](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="7919c-126">Provision a new Project Operations Dataverse deployment environment by following instructions in the topic, [Dataverse deployment model](lite-deployment.md).</span></span> <span data-ttu-id="7919c-127">Pasirinkę aplinkos tipą įsitikinkite, kad naudojate **bandomąją versiją (prenumeratos pagrindu)**.</span><span class="sxs-lookup"><span data-stu-id="7919c-127">When you select the environment type, make sure to use **Trial (Subscription based)**.</span></span>

  ![Nauja aplinka](./media/19CreateEnvironment.png)

2. <span data-ttu-id="7919c-129">Pasirinkite nustatymą **Įjungti „Dynamics 365“ programėles** ir palikite lauką **Automatiškai diegti šias programėles** tuščią.</span><span class="sxs-lookup"><span data-stu-id="7919c-129">Select the **Enable Dynamics 365 apps** setting, and leave **Automatically deploy these apps** blank.</span></span>  
3. <span data-ttu-id="7919c-130">Norėdami sukurti aplinką, pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="7919c-130">Select **Save** to create the environment.</span></span>

  ![Įtraukti duomenų bazę](./media/20CreateEnvironment1.png)

4. <span data-ttu-id="7919c-132">Sukūrę aplinką įdiekite **„Microsoft Dynamics 365 Project Operations“** sprendimą.</span><span class="sxs-lookup"><span data-stu-id="7919c-132">After the environment is created, install **Microsoft Dynamics 365 Project Operations** solution.</span></span> 

![Sprendimo diegimas](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a><span data-ttu-id="7919c-134">CDS konfigūracijos ir sąrankos demonstracinių duomenų diegimas</span><span class="sxs-lookup"><span data-stu-id="7919c-134">Install a CDS configuration and setup demo data</span></span>

<span data-ttu-id="7919c-135">Įdiekite CDS konfigūraciją ir nustatykite demonstracinius duomenis vadovaudamiesi šioje temoje pateikiamomis instrukcijomis – [Demonstracinės sąrankos ir konfigūravimo duomenų taikymas](lite-apply-demo-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="7919c-135">Install the CDS configuration and set up demo data by following instructions in the topic, [Apply demo setup and configuration data](lite-apply-demo-setup-config-data.md).</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
