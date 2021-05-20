---
title: „Azure“ prenumeratos įtraukimas į LCS projektą
description: Šioje temoje pateikta informacija apie tai, kaip prijungti „Azure“ prenumeratą prie LCS projekto.
author: sigitac
manager: Annbe
ms.date: 04/12/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a80c926ba67a1620e39d8c7677a05678454e6340
ms.sourcegitcommit: 7468d668c48c1d87934aab9a034decd51e56dec6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/13/2021
ms.locfileid: "5880548"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a><span data-ttu-id="62d69-103">„Azure“ prenumeratos įtraukimas į LCS projektą</span><span class="sxs-lookup"><span data-stu-id="62d69-103">Add an Azure subscription to an LCS project</span></span>

<span data-ttu-id="62d69-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="62d69-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="62d69-105">Naudojant esamą „Azure“ prenumeratą būtina įdiegti debesyje esančią aplinką.</span><span class="sxs-lookup"><span data-stu-id="62d69-105">Cloud-hosted environments must be deployed using an existing Azure subscription.</span></span> <span data-ttu-id="62d69-106">Šioje temoje paaiškinta, kaip prijungti esamą „Azure“ prenumeratą prie LCS projekto.</span><span class="sxs-lookup"><span data-stu-id="62d69-106">This topic explains how to connect your existing Azure subscription to an LCS project.</span></span> 

## <a name="grant-admin-consent"></a><span data-ttu-id="62d69-107">Administratoriaus sutikimo davimas</span><span class="sxs-lookup"><span data-stu-id="62d69-107">Grant admin consent</span></span>

1. <span data-ttu-id="62d69-108">Savo LCS projekte, skyriuje **Aplinkos**, pasirinkite **„Microsoft Azure“ parametrai**.</span><span class="sxs-lookup"><span data-stu-id="62d69-108">In your LCS project, in the **Environments** section, select **Microsoft Azure settings**.</span></span>

![„Microsoft Azure“, parametrai](./media/1MicrosoftAzureSettings.png)

2. <span data-ttu-id="62d69-110">Puslapyje **Projekto parametrai**, skirtuke **„Azure“ jungtys** pažymėkite **Leisti**.</span><span class="sxs-lookup"><span data-stu-id="62d69-110">On the **Project settings** page, on the **Azure connectors** tab, select **Authorize**.</span></span> <span data-ttu-id="62d69-111">Taip leidžiama aplinkas įdiegti į šį projektą.</span><span class="sxs-lookup"><span data-stu-id="62d69-111">This allows environments to be deployed to this project.</span></span>

![„Azure” jungtys](./media/2AzureConnectors.png)

3. <span data-ttu-id="62d69-113">Dar kartą pasirinkite **Leisti**, kad būtų duotas administratoriaus sutikimas.</span><span class="sxs-lookup"><span data-stu-id="62d69-113">Select **Authorize** again to provide admin consent.</span></span>

![Administratoriaus sutikimo davimas](./media/3GrantAdminConsent.png)

4. <span data-ttu-id="62d69-115">Sutikite su teisių užklausa.</span><span class="sxs-lookup"><span data-stu-id="62d69-115">Accept the permissions request.</span></span>

![Sutikite su teisių užklausa](./media/4AcceptPermissionRequest.png)

<span data-ttu-id="62d69-117">Dabar autorizavimas baigtas.</span><span class="sxs-lookup"><span data-stu-id="62d69-117">The authorization is now complete.</span></span> 

![Sėkmingas leidimas](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a><span data-ttu-id="62d69-119">„Dynamics Deployment Services“ prieigos prie jūsų „Azure“ prenumeratos suteikimas</span><span class="sxs-lookup"><span data-stu-id="62d69-119">Provide Dynamics Deployment Services access to your Azure subscription</span></span>

1. <span data-ttu-id="62d69-120">Eikite į [„Microsoft Azure“ atsiskaitymas](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) ir pasirinkite savo prenumeratą.</span><span class="sxs-lookup"><span data-stu-id="62d69-120">Go to [Microsoft Azure billing](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) and select your subscription.</span></span> <span data-ttu-id="62d69-121">„Dynamics Deployment Services“ reikia pasiekti šią prenumeratą, kad būtų galima visuotinai diegti aplinkas.</span><span class="sxs-lookup"><span data-stu-id="62d69-121">Dynamics Deployment Services needs to access this subscription to be able to deploy environments.</span></span>

![„Azure“ prenumeratos informacija](./media/6AzureSubscription.png)

2. <span data-ttu-id="62d69-123">Naršymo srityje pasirinkite **Prieigos valdymas (IAM)**, tada pažymėkite **Įtraukti vaidmens priskyrimą**.</span><span class="sxs-lookup"><span data-stu-id="62d69-123">Select **Access control (IAM)** in the navigation pane, and then select **Add role assignment**.</span></span>
3. <span data-ttu-id="62d69-124">Dešinėje pusėje esančiame slankiklyje pasirinkite **Dalyvio vaidmuo**, pateiktame sąraše raskite ir pažymėkite **Dynamics Deployment Services**.</span><span class="sxs-lookup"><span data-stu-id="62d69-124">In the slider on the right side, select **Contributor role**, and in the list provided, find and select **Dynamics Deployment Services**.</span></span> 
4. <span data-ttu-id="62d69-125">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="62d69-125">Select **Save**.</span></span>

![Prenumeratos prieiga](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a><span data-ttu-id="62d69-127">Įtraukti prenumeratos jungtį į LCS projektą</span><span class="sxs-lookup"><span data-stu-id="62d69-127">Add a subscription connector to an LCS project</span></span>

1. <span data-ttu-id="62d69-128">Savo LCS projekto puslapyje **„Microsoft Azure“ parametrai** pasirinkite **Įtraukti**, kad įtrauktumėte naują jungtį.</span><span class="sxs-lookup"><span data-stu-id="62d69-128">In your LCS project, on the **Microsoft Azure settings** page, select **Add** to add a new connector.</span></span>
2. <span data-ttu-id="62d69-129">Įveskite savo „Azure“ prenumeratos ID.</span><span class="sxs-lookup"><span data-stu-id="62d69-129">Enter your Azure subscription ID.</span></span> <span data-ttu-id="62d69-130">Savo „Azure“ prenumeratos ID galite rasti [„Azure“ portale](https://ms.portal.azure.com/) dalyje **Parametrai** apatiniame kairiajame ekrano kampe.</span><span class="sxs-lookup"><span data-stu-id="62d69-130">You can find your Azure subscription ID in the [Azure portal](https://ms.portal.azure.com/), under  **Settings**  in the lower left of the screen.</span></span>
3. <span data-ttu-id="62d69-131">Lauke **Konfigūruoti naudoti „Azure Resource Manager“** pasirinkite **Taip**.</span><span class="sxs-lookup"><span data-stu-id="62d69-131">In the **Configure to use Azure Resource Manager** field, select **Yes**.</span></span>
4. <span data-ttu-id="62d69-132">Įsitikinkite, kad „Azure“ prenumeratos AAD nuomotojo domenas atitinka domeno „Azure“ prenumeratą, kurią naudojate, ir pažymėkite **Kitas**.</span><span class="sxs-lookup"><span data-stu-id="62d69-132">Make sure Azure's Subscription AAD Tenant Domain matches the domain-owning Azure subscription that you are using, and select **Next**.</span></span>
5. <span data-ttu-id="62d69-133">Ekrane **„Microsoft Azure“ sąranka** pasirinkite **Kitas**, kad patvirtintumėte.</span><span class="sxs-lookup"><span data-stu-id="62d69-133">On the **Microsoft Azure Setup** screen, select **Next** to confirm.</span></span> <span data-ttu-id="62d69-134">Jei šiame ekrane įvyksta klaida, grįžkite į skyrių [„Dynamics Deployment Services“ prieigos prie jūsų „Azure“ prenumeratos suteikimas](#provide)ir įsitikinkite, kad atlikote visus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="62d69-134">If you receive an error on this screen, return to the section [Provide Dynamics Deployment Services access to Azure subscription](#provide) in this topic and make sure you have completed all of the steps.</span></span>
6. <span data-ttu-id="62d69-135">Į vietinį aplanką savo kompiuteryje atsisiųskite „Azure“ tvarkymo sertifikatą.</span><span class="sxs-lookup"><span data-stu-id="62d69-135">Download the Azure Management Certificate to a local folder on your computer.</span></span> <span data-ttu-id="62d69-136">Paprašykite savo „Azure“ prenumeratos administratoriaus sertifikatą nusiųsti į „Azure“ tvarkymo portalą (reikia pasirinkti prenumeratą ir nueiti į **Parametrai** > **Tvarkymo sertifikatai**).</span><span class="sxs-lookup"><span data-stu-id="62d69-136">Ask your Azure subscription administrator to upload the certificate to Azure Management Portal by selecting the subscription and going to **Settings** > **Management Certificates**.</span></span> <span data-ttu-id="62d69-137">Šis sertifikatas leidžia LCS palaikyti ryšį su „Azure“ jūsų vardu.</span><span class="sxs-lookup"><span data-stu-id="62d69-137">This certificate enables LCS to communicate with Azure on your behalf.</span></span> <span data-ttu-id="62d69-138">Šį veiksmą galite praleisti, jei jūsų vartotojas turi prieigą prie prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="62d69-138">You can skip this step if your user has access to the subscription.</span></span>
7. <span data-ttu-id="62d69-139">Pasirinkite **Toliau**.</span><span class="sxs-lookup"><span data-stu-id="62d69-139">Select  **Next**.</span></span>
8. <span data-ttu-id="62d69-140">Pažymėkite „Azure“ regioną, skirtą visuotinai diegti, ir pasirinkite duomenų centrą, esantį netoli tos sistemos, kurią ketinate naudoti.</span><span class="sxs-lookup"><span data-stu-id="62d69-140">Select the Azure region to deploy in and select a data center that is close to where you plan to use this system.</span></span>
9.  <span data-ttu-id="62d69-141">Pasirinkite **Prisijungti**.</span><span class="sxs-lookup"><span data-stu-id="62d69-141">Select  **Connect**.</span></span>

<span data-ttu-id="62d69-142">Sėkmingai prisijungėte prie „Azure“ prenumeratos.</span><span class="sxs-lookup"><span data-stu-id="62d69-142">You have successfully connected your Azure subscription.</span></span> <span data-ttu-id="62d69-143">Dabar galite įdiegti „Dynamics 365 Finance“ debesyje veikiančias aplinkas.</span><span class="sxs-lookup"><span data-stu-id="62d69-143">You can now deploy Dynamics 365 Finance cloud-hosted environments.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]
