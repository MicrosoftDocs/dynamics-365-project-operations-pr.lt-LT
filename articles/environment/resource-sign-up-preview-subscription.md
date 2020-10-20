---
title: Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacijos, kaip užsiprenumeruoti ir įdiegti „Project Operations“, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 4d35a8bf9e8a841b45808b26ae2587c5b7d99d72
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948982"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a><span data-ttu-id="3df9d-103">Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams</span><span class="sxs-lookup"><span data-stu-id="3df9d-103">Sign up for Project Operations preview subscriptions for resource/ non-stocked scenarios</span></span>

<span data-ttu-id="3df9d-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="3df9d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3df9d-105">Šioje temoje aiškinama, kaip užsiprenumeruoti peržiūros versijos / partnerio pasiūlymą ir visuotinai įdiegti „Project Operations“ aplinką, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.</span><span class="sxs-lookup"><span data-stu-id="3df9d-105">This topic explains how to subscribe to the preview/partner offer and deploy Project Operations environment for resource/ non-stocked based scenarios.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3df9d-106">Būtinosios sąlygos</span><span class="sxs-lookup"><span data-stu-id="3df9d-106">Prerequisites</span></span>

- <span data-ttu-id="3df9d-107">Gausite el. laišką, kviečiantį išbandyti peržiūros versiją.</span><span class="sxs-lookup"><span data-stu-id="3df9d-107">You will receive an email inviting you to participate in the preview.</span></span> <span data-ttu-id="3df9d-108">Galite pateikti užklausą dėl peržiūros versijos [„Project Operations“ svetainėje](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span><span class="sxs-lookup"><span data-stu-id="3df9d-108">You can request a preview on the [Project Operations website](https://dynamics.microsoft.com/en-us/project-operations/overview/).</span></span>
- <span data-ttu-id="3df9d-109">Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises.</span><span class="sxs-lookup"><span data-stu-id="3df9d-109">The user who deploys the preview must have Azure tenant global administrator rights.</span></span>
- <span data-ttu-id="3df9d-110">Norint diegti „Finance“ aplinką, reikia tinkamos „Azure“ prenumeratos, pagal kurią mokama už aplinką.</span><span class="sxs-lookup"><span data-stu-id="3df9d-110">Deploying a Finance environment requires a valid Azure subscription that will be billed per environment.</span></span> <span data-ttu-id="3df9d-111">Norėdami pradėti, galite naudoti esamą organizacijos prenumeratą arba naudoti [„Azure“ bandomąją versiją](https://azure.microsoft.com/en-us/free/).</span><span class="sxs-lookup"><span data-stu-id="3df9d-111">You can use your organizations existing subscription or use an [Azure trial](https://azure.microsoft.com/en-us/free/) to get started.</span></span> <span data-ttu-id="3df9d-112">CDS aplinka bus pasiekiama nemokamai 30 dienų.</span><span class="sxs-lookup"><span data-stu-id="3df9d-112">The CDS environment will be provided free for a limited 30 day period.</span></span>

## <a name="subscribe"></a><span data-ttu-id="3df9d-113">Prenumeruoti</span><span class="sxs-lookup"><span data-stu-id="3df9d-113">Subscribe</span></span>

<span data-ttu-id="3df9d-114">Patvirtinus jūsų [peržiūros versijos užklausą](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), el. paštu gausite iš „Microsoft“ du pasiūlymus.</span><span class="sxs-lookup"><span data-stu-id="3df9d-114">When your [preview request](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) is approved, you will receive two offers from Microsoft by email.</span></span> <span data-ttu-id="3df9d-115">Šie pasiūlymai leidžia visuotinai įdiegti „Project Operations“ peržiūros versiją:</span><span class="sxs-lookup"><span data-stu-id="3df9d-115">These offers allow you to deploy the Project Operations Preview:</span></span>

- <span data-ttu-id="3df9d-116">„Dynamics 365 Project Operations“ – bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="3df9d-116">Dynamics 365 Project Operations – Preview Trial</span></span>
- <span data-ttu-id="3df9d-117">„Dynamics 365 for Finance and Operations“ bandomoji peržiūros versija.</span><span class="sxs-lookup"><span data-stu-id="3df9d-117">Dynamics 365 for Finance and Operations Preview Trial.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3df9d-118">Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="3df9d-118">Only one person, the tenant administrator, in an organization needs to perform this task.</span></span> <span data-ttu-id="3df9d-119">Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.</span><span class="sxs-lookup"><span data-stu-id="3df9d-119">If you aren't the subscriber to this release, wait until your organization has been signed up and you've received your user credentials.</span></span>

### <a name="dynamics-365-project-operations--preview-trial"></a><span data-ttu-id="3df9d-120">„Dynamics 365 Project Operations“ – bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="3df9d-120">Dynamics 365 Project Operations – Preview trial</span></span>

1. <span data-ttu-id="3df9d-121">Pasinaudokite pirmu pasiūlymu **„Dynamics 365 Project Operations“ bandomoji versija** naudodami pasveikinimo el. laiške pateiktą URL.</span><span class="sxs-lookup"><span data-stu-id="3df9d-121">Redeem the first offer, **Dynamics 365 Project Operations Trial**, with the URL provided in your welcome email.</span></span>

![Pirmasis pasiūlymas](./media/1FirstOffer.png)

2. <span data-ttu-id="3df9d-123">Įsitikinkite, kad esate įėję kaip vartotojas, priklausantis organizacijai, kuri prenumeruos paslaugą.</span><span class="sxs-lookup"><span data-stu-id="3df9d-123">Verify that you are logged in as the user who belongs to the organization who will be subscribing to the service.</span></span>
3. <span data-ttu-id="3df9d-124">Tęskite pasinaudojimo pasiūlymu procesą.</span><span class="sxs-lookup"><span data-stu-id="3df9d-124">Proceed with redeeming the offer.</span></span> 
4. <span data-ttu-id="3df9d-125">Pasirinkite **Taip, įtraukti į mano paskyrą**.</span><span class="sxs-lookup"><span data-stu-id="3df9d-125">Select **Yes, add it to my account**.</span></span>

![Pasinaudoti pasiūlymu](./media/2RedeemFirstOffer.png)

![Patvirtinti pasiūlymą](./media/3ConfirmFirstOffer.png)

![Pasiūlymu pasinaudota](./media/4OfferSuccessfulyRedeemed.png)

### <a name="dynamics-365-finance-preview-trial"></a><span data-ttu-id="3df9d-129">„Dynamics 365 Finance“ bandomoji peržiūros versija</span><span class="sxs-lookup"><span data-stu-id="3df9d-129">Dynamics 365 Finance preview trial</span></span>

<span data-ttu-id="3df9d-130">Pakartokite šiuos veiksmus su antruoju pasiūlymu, esančiu pasveikinimo el. laiške.</span><span class="sxs-lookup"><span data-stu-id="3df9d-130">Repeat the same steps with the second offer from the Welcome email.</span></span>

## <a name="assign-licenses"></a><span data-ttu-id="3df9d-131">Priskirti licencijas</span><span class="sxs-lookup"><span data-stu-id="3df9d-131">Assign Licenses</span></span>

> [!IMPORTANT]
> <span data-ttu-id="3df9d-132">Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Office 365“ portalo.</span><span class="sxs-lookup"><span data-stu-id="3df9d-132">You will need administrative access to your organization's Office 365 Portal to complete the following steps.</span></span>

1. <span data-ttu-id="3df9d-133">Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas vartotojams.</span><span class="sxs-lookup"><span data-stu-id="3df9d-133">Go to [Microsoft 365 admin center](https://portal.office.com/) to assign licenses to your users.</span></span>

![„Office“ administravimo portalas](./media/5OfficeAdminPortal.png)

2. <span data-ttu-id="3df9d-135">Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.</span><span class="sxs-lookup"><span data-stu-id="3df9d-135">On the **Active users** page, select the users that you want to assign a license to.</span></span>

![Priskirti licencijas](./media/6AssignLicenses.png)

3. <span data-ttu-id="3df9d-137">Įsitikinkite, kad pasirinkta „Project Operations“ licencija, ir pasirinkite **Įrašyti keitimus**.</span><span class="sxs-lookup"><span data-stu-id="3df9d-137">Verify that the Project Operations license has been selected and select **Save changes**.</span></span> 

> [!NOTE]
> <span data-ttu-id="3df9d-138">„Finance“ bandomosios versijos pasiūlymo nereikia priskirti vartotojui.</span><span class="sxs-lookup"><span data-stu-id="3df9d-138">The Finance trial offer does not need to be assigned to a user.</span></span>

## <a name="start-a-new-project-in-lcs"></a><span data-ttu-id="3df9d-139">Pradėkite naują LCS projektą</span><span class="sxs-lookup"><span data-stu-id="3df9d-139">Start a new project in LCS</span></span>

<span data-ttu-id="3df9d-140">Sukurkite naują LCS projektą, kaip aprašytą temoje [Naujo LCS projekto pradėjimas](create-lcs-project.md)</span><span class="sxs-lookup"><span data-stu-id="3df9d-140">Create a new LCS project as described in the topic, [Start a new project in LCS](create-lcs-project.md)</span></span>

## <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="3df9d-141">„Azure“ prenumeratos įtraukimas į LCS projektą</span><span class="sxs-lookup"><span data-stu-id="3df9d-141">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="3df9d-142">Norėdami atlikti šią užduotį, atlikite veiksmus, nurodytus temoje [„Azure“ prenumeratos įtraukimas į LCS projektą](resource-add-azure-subscription-lcs-project.md).</span><span class="sxs-lookup"><span data-stu-id="3df9d-142">To complete this task, follow the steps in the topic, [Add an Azure subscription to LCS project](resource-add-azure-subscription-lcs-project.md).</span></span>

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="3df9d-143">„Finance“ demonstracinės aplinkos ir „Project Operations“, skirtos ištekliais / ne atsargomis pagrįstiems scenarijams, visuotinis diegimas</span><span class="sxs-lookup"><span data-stu-id="3df9d-143">Deploy Finance demo environment with Project Operations for resource/non-stocked scenarios</span></span>

<span data-ttu-id="3df9d-144">Vadovaukitės nurodymais, pateiktais temoje [Naujos aplinkos parengimas](resource-provision-new-environment.md), kad užbaigtumėte visuotinį diegimą.</span><span class="sxs-lookup"><span data-stu-id="3df9d-144">Follow the guidance in the topic, [Provision a new environment](resource-provision-new-environment.md) to complete the deployment.</span></span> <span data-ttu-id="3df9d-145">Naudokite [demonstracinės aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) visuotinio diegimo tipą, skirtą peržiūros versijai.</span><span class="sxs-lookup"><span data-stu-id="3df9d-145">Use the [demo environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) deployment type for preview.</span></span>

## <a name="install-cds-setup-and-configuration-data"></a><span data-ttu-id="3df9d-146">CDS sąrankos ir konfigūracijos duomenų diegimas</span><span class="sxs-lookup"><span data-stu-id="3df9d-146">Install CDS setup and configuration data</span></span>

<span data-ttu-id="3df9d-147">Įdiekite CDS sąrankos ir konfigūracijos duomenis, kaip aprašyta temoje [Konfigūracijos duomenų nustatymas ir taikymas sistemoje „Common Data Service“](resource-apply-pro-setup-config-data.md).</span><span class="sxs-lookup"><span data-stu-id="3df9d-147">Install CDS setup and configuration data as described in the topic, [Set up and apply configuration data in the Common Data Service](resource-apply-pro-setup-config-data.md).</span></span>

