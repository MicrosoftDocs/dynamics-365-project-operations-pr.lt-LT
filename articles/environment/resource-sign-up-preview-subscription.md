---
title: Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacijos, kaip užsiprenumeruoti ir įdiegti „Project Operations“, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: da93fcf23ee3f255812842e31cb22b5d39daa963
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334837"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="63239-103">Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams</span><span class="sxs-lookup"><span data-stu-id="63239-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="63239-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="63239-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="63239-105">Šioje temoje paaiškinama, kaip užsiprenumeruoti bandomosios versijos pasiūlymą ir įdiegti „Project Operations“ aplinką, skirtą ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="63239-105">This topic explains how to subscribe to the trial offer and deploy Project Operations environment for resource/non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="63239-106">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="63239-106">Prerequisites</span></span>
- <span data-ttu-id="63239-107">Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises.</span><span class="sxs-lookup"><span data-stu-id="63239-107">The user who deploys the preview must have Azure tenant global administrator rights.</span></span> <span data-ttu-id="63239-108">Pasinaudodami pirmuoju pasiūlymu, galite sukurti nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="63239-108">You can create a tenant during the first offer redemption.</span></span> 
- <span data-ttu-id="63239-109">Norint diegti „Finance“ aplinką, reikia tinkamos „Azure“ prenumeratos, pagal kurią mokama už aplinką.</span><span class="sxs-lookup"><span data-stu-id="63239-109">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="63239-110">Norėdami pradėti, galite naudoti esamą organizacijos prenumeratą arba naudoti [„Azure“ bandomąją versiją](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="63239-110">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="63239-111">CDS aplinka bus pasiekiama nemokamai 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="63239-111">The CDS environment will be provided free for a limited 30 day period.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63239-112">Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="63239-112">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="63239-113">Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="63239-113">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>
> 
> <span data-ttu-id="63239-114">Bandomosios versijos nuomotojuje yra vienkartinės.</span><span class="sxs-lookup"><span data-stu-id="63239-114">Trials are single use in the tenant.</span></span> <span data-ttu-id="63239-115">Bandomąją versiją galite paleisti tik vieną kartą.</span><span class="sxs-lookup"><span data-stu-id="63239-115">You can only run a trial one time.</span></span> <span data-ttu-id="63239-116">Bandomajai versijai rekomenduojame sukurti naują nuomotoją.</span><span class="sxs-lookup"><span data-stu-id="63239-116">We recommend that you create a new tenant for the purpose of the trial.</span></span>


### <a name="dynamics-365-project-operations-ce---preview-trial"></a><span data-ttu-id="63239-117">„Dynamics 365 Project Operations“ (CE) – peržiūros bandomoji versija</span><span class="sxs-lookup"><span data-stu-id="63239-117">Dynamics 365 Project Operations (CE) - Preview Trial</span></span> 

<span data-ttu-id="63239-118">Prieš pradėdami įsitikinkite, kad esate prisijungę prie naršyklės naudodami vartotojo darbo klientą nuomotojuje, kuriame norite atlikti „Project Operations“ peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="63239-118">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="63239-119">Pirmąjį pasiūlymo kodą – **„Dynamics 365 Project Operations“** – panaudokite čia: [„Project Operations“ bandomoji versija](https://aka.ms/try-po).</span><span class="sxs-lookup"><span data-stu-id="63239-119">Redeem the first offer code, **Dynamics 365 Project Operations** here [Project Operations Trial](https://aka.ms/try-po).</span></span>
2. <span data-ttu-id="63239-120">Patvirtinkite užsakymą.</span><span class="sxs-lookup"><span data-stu-id="63239-120">Confirm your order.</span></span>

  <span data-ttu-id="63239-121">Pamatysite sėkmingai panaudotą patvirtinimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="63239-121">You will see confirmation offer was successfully redeemed.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="63239-122">„Dynamics 365 Finance“ bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="63239-122">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="63239-123">Eikite į [„Dynamics 365 for Finance“ peržiūros bandomoji versija](https://aka.ms/trypoche) ir pakartokite ankstesnio skyriaus veiksmus su pasiūlymu Registracija norint naudoti debesyje esančią aplinką.</span><span class="sxs-lookup"><span data-stu-id="63239-123">Go to [Dynamics 365 for Finance Preview Trial](https://aka.ms/trypoche) and repeat the steps from the previous section with the offer, Sign up for the Cloud Hosted Environment.</span></span>  

## <a name="assign-licenses"></a><span data-ttu-id="63239-124">Licencijų priskyrimas</span><span class="sxs-lookup"><span data-stu-id="63239-124">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="63239-125">Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365 Portal“.</span><span class="sxs-lookup"><span data-stu-id="63239-125">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="63239-126">Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas vartotojams.</span><span class="sxs-lookup"><span data-stu-id="63239-126">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

2. <span data-ttu-id="63239-127">Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.</span><span class="sxs-lookup"><span data-stu-id="63239-127">On the **Active users** page, select the users that you want to assign a license to.</span></span>

3. <span data-ttu-id="63239-128">Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“** licencija, ir pasirinkite **Įrašyti keitimus**.</span><span class="sxs-lookup"><span data-stu-id="63239-128">Verify that the **Dynamics 365 Project Operations** license has been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="63239-129">„Finance“ bandomosios versijos pasiūlymo nereikia priskirti vartotojui.</span><span class="sxs-lookup"><span data-stu-id="63239-129">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="63239-130">Pradėkite naują LCS projektą</span><span class="sxs-lookup"><span data-stu-id="63239-130">Start a new project in LCS</span></span>

<span data-ttu-id="63239-131">Sukurkite naują LCS projektą, kaip aprašytą temoje [Naujo LCS projekto pradėjimas](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="63239-131">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="63239-132">„Azure“ prenumeratos įtraukimas į LCS projektą</span><span class="sxs-lookup"><span data-stu-id="63239-132">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="63239-133">Norėdami atlikti šią užduotį, atlikite veiksmus, nurodytus temoje [„Azure“ prenumeratos įtraukimas į LCS projektą](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="63239-133">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="63239-134">„Finance“ demonstracinės aplinkos ir „Project Operations“, skirtos ištekliais / ne atsargomis pagrįstiems scenarijams, visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="63239-134">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="63239-135">Vadovaukitės nurodymais, pateiktais temoje [Naujos aplinkos parengimas](resource-provision-new-environment.md), kad užbaigtumėte visuotinį diegimą.</span><span class="sxs-lookup"><span data-stu-id="63239-135">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="63239-136">Naudokite [demonstracinės aplinkos](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) visuotinio diegimo tipą, skirtą peržiūros versijai.</span><span class="sxs-lookup"><span data-stu-id="63239-136">Use the [demo environment](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="63239-137">CDS sąrankos ir konfigūracijos duomenų diegimas</span><span class="sxs-lookup"><span data-stu-id="63239-137">Install CDS setup and configuration data</span></span>

<span data-ttu-id="63239-138">Įdiekite CDS sąrankos ir konfigūracijos duomenis, kaip aprašyta temoje [Konfigūracijos duomenų nustatymas ir taikymas sistemoje „Common Data Service“](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="63239-138">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="63239-139">Šį veiksmą atlikite tik įdiegę „Finance“ demonstracinę aplinką ir parengę demonstracinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="63239-139">Complete this step only after Finance demo environment is deployed and demo data is ready.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
