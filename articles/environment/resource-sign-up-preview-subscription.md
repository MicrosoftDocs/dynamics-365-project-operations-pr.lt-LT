---
title: Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacijos, kaip užsiprenumeruoti ir įdiegti „Project Operations“, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080722"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="091d9-103">Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams</span><span class="sxs-lookup"><span data-stu-id="091d9-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="091d9-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="091d9-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="091d9-105">Šioje temoje aiškinama, kaip užsiprenumeruoti peržiūros versijos / partnerio pasiūlymą ir visuotinai įdiegti „Project Operations“ aplinką, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="091d9-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="091d9-106">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="091d9-106">Prerequisites</span></span>

- <span data-ttu-id="091d9-107">Gausite el. laišką, kviečiantį išbandyti peržiūros versiją.</span><span class="sxs-lookup"><span data-stu-id="091d9-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="091d9-108">Galite pateikti užklausą dėl peržiūros versijos [„Project Operations“ svetainėje](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="091d9-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="091d9-109">Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises.</span><span class="sxs-lookup"><span data-stu-id="091d9-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="091d9-110">Norint diegti „Finance“ aplinką, reikia tinkamos „Azure“ prenumeratos, pagal kurią mokama už aplinką.</span><span class="sxs-lookup"><span data-stu-id="091d9-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="091d9-111">Norėdami pradėti, galite naudoti esamą organizacijos prenumeratą arba naudoti [„Azure“ bandomąją versiją](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="091d9-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="091d9-112">CDS aplinka bus pasiekiama nemokamai 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="091d9-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="091d9-113">Prenumeruoti</span><span class="sxs-lookup"><span data-stu-id="091d9-113">Subscribe</span></span>

<span data-ttu-id="091d9-114">Patvirtinus jūsų [peržiūros versijos užklausą](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), el. paštu gausite iš „Microsoft“ tris pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="091d9-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive three offers from Microsoft by email.</span></span> <span data-ttu-id="091d9-115">Šie pasiūlymai leidžia visuotinai įdiegti „Project Operations“ peržiūros versiją:</span><span class="sxs-lookup"><span data-stu-id="091d9-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="091d9-116">„Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="091d9-116">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span>
- <span data-ttu-id="091d9-117">„Office 365 Project Operations“ – bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="091d9-117">Office 365 Project Operations - Preview Trial</span></span>
- <span data-ttu-id="091d9-118">„Dynamics 365 Finance“ – bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="091d9-118">Dynamics 365 Finance - Preview Trial</span></span>

> [!IMPORTANT]
> <span data-ttu-id="091d9-119">Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="091d9-119">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="091d9-120">Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="091d9-120">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations-crm---preview-trial"></a><span data-ttu-id="091d9-121">„Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="091d9-121">Dynamics 365 Project Operations (CRM) - Preview Trial</span></span> 

<span data-ttu-id="091d9-122">Prieš pradėdami įsitikinkite, kad esate prisijungę prie naršyklės naudodami vartotojo darbo klientą nuomotojuje, kuriame norite atlikti „Project Operations“ peržiūrą.</span><span class="sxs-lookup"><span data-stu-id="091d9-122">Before you begin, make sure you are logged in to a browser with the user work account in the tenant where you want the Project Operations preview.</span></span>

1. <span data-ttu-id="091d9-123">Pasinaudokite pirmuoju pasiūlymo kodu **„Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija** , įklijuodami jį į naršyklės URL lauką.</span><span class="sxs-lookup"><span data-stu-id="091d9-123">Redeem the first offer code, **Dynamics 365 Project Operations (CRM) - Preview Trial** by pasting it into the browser URL.</span></span>

![Pasinaudoti pasiūlymu](./media/16RedeemFirstOfferNew.png)

2. <span data-ttu-id="091d9-125">Patvirtinkite užsakymą.</span><span class="sxs-lookup"><span data-stu-id="091d9-125">Confirm your order.</span></span>

![Patvirtinkite užsakymą](./media/17ConfirmOrderNew.png)

<span data-ttu-id="091d9-127">Pamatysite sėkmingai panaudotą patvirtinimo pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="091d9-127">You will see confirmation offer was successfully redeemed.</span></span>

![Patvirtinimas](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a><span data-ttu-id="091d9-129">„Office 365 Project Operations“ – bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="091d9-129">Office 365 Project Operations - Preview Trial</span></span>

<span data-ttu-id="091d9-130">Pakartokite veiksmus, kaip ir taikydami pirmąjį pasiūlymo kodą.</span><span class="sxs-lookup"><span data-stu-id="091d9-130">Repeat the same steps as with the first offer code.</span></span> <span data-ttu-id="091d9-131">Būtinai įtraukite antrą pasiūlymo kodą, naudodami tą patį vartotojo klientą, kuris buvo naudojamas su pirmuoju pasiūlymo kodu.</span><span class="sxs-lookup"><span data-stu-id="091d9-131">Make sure to add the second offer code using the same user account that was used with the first offer code.</span></span>

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="091d9-132">„Dynamics 365 Finance“ bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="091d9-132">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="091d9-133">Pakartokite tuos pačius veiksmus su paskutiniu pasiūlymu, esančiu pasveikinimo el. laiške.</span><span class="sxs-lookup"><span data-stu-id="091d9-133">Repeat the same steps with the last offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="091d9-134">Licencijų priskyrimas</span><span class="sxs-lookup"><span data-stu-id="091d9-134">Assign licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="091d9-135">Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365 Portal“.</span><span class="sxs-lookup"><span data-stu-id="091d9-135">You will need administrative access to your organization's Microsoft 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="091d9-136">Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas vartotojams.</span><span class="sxs-lookup"><span data-stu-id="091d9-136">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign the licenses to your users.</span></span>

![Administravimo centro pagrindinis puslapis](./media/14AdminPortal.png)

2. <span data-ttu-id="091d9-138">Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.</span><span class="sxs-lookup"><span data-stu-id="091d9-138">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Licencijų priskyrimas](./media/15AssignLicenses.png)

3. <span data-ttu-id="091d9-140">Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“ (CRM) peržiūros versijos** ir **„Office 365 Project Operations“ – peržiūros versijos** licencija, tada pasirinkite **Išsaugoti pakeitimus**.</span><span class="sxs-lookup"><span data-stu-id="091d9-140">Verify that the **Dynamics 365 Project Operations (CRM) Preview** and **Office 365 Project Operations - Preview** license have been selected and select **Save changes**.</span></span>

> [!NOTE]
> <span data-ttu-id="091d9-141">„Finance“ bandomosios versijos pasiūlymo nereikia priskirti vartotojui.</span><span class="sxs-lookup"><span data-stu-id="091d9-141">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="091d9-142">Pradėkite naują LCS projektą</span><span class="sxs-lookup"><span data-stu-id="091d9-142">Start a new project in LCS</span></span>

<span data-ttu-id="091d9-143">Sukurkite naują LCS projektą, kaip aprašytą temoje [Naujo LCS projekto pradėjimas](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="091d9-143">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="091d9-144">„Azure“ prenumeratos įtraukimas į LCS projektą</span><span class="sxs-lookup"><span data-stu-id="091d9-144">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="091d9-145">Norėdami atlikti šią užduotį, atlikite veiksmus, nurodytus temoje [„Azure“ prenumeratos įtraukimas į LCS projektą](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="091d9-145">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="091d9-146">„Finance“ demonstracinės aplinkos ir „Project Operations“, skirtos ištekliais / ne atsargomis pagrįstiems scenarijams, visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="091d9-146">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="091d9-147">Vadovaukitės nurodymais, pateiktais temoje [Naujos aplinkos parengimas](resource-provision-new-environment.md), kad užbaigtumėte visuotinį diegimą.</span><span class="sxs-lookup"><span data-stu-id="091d9-147">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="091d9-148">Naudokite [demonstracinės aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) visuotinio diegimo tipą, skirtą peržiūros versijai.</span><span class="sxs-lookup"><span data-stu-id="091d9-148">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span> 

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="091d9-149">CDS sąrankos ir konfigūracijos duomenų diegimas</span><span class="sxs-lookup"><span data-stu-id="091d9-149">Install CDS setup and configuration data</span></span>

<span data-ttu-id="091d9-150">Įdiekite CDS sąrankos ir konfigūracijos duomenis, kaip aprašyta temoje [Konfigūracijos duomenų nustatymas ir taikymas sistemoje „Common Data Service“](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="091d9-150">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>
<span data-ttu-id="091d9-151">Atlikite šį veiksmą tik tada, kai įdiegiama „Finance“ demonstracinė aplinka ir demonstraciniai duomenys yra paruošti FO.</span><span class="sxs-lookup"><span data-stu-id="091d9-151">Complete this step only after Finance demo environment is deployed and demo data in FO is ready.</span></span>
