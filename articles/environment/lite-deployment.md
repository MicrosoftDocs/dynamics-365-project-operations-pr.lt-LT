---
title: „Project Operations“ visuotinis diegimas – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip įdiegti „Project Operations Lite“ visuotinį diegimą – sandoris į išankstinės sąskaitos faktūros formą.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0633585fcef91d9218d6140764addb7cf96ab31d
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4175676"
---
# <a name="deploy-project-operations---lite"></a><span data-ttu-id="9bb9f-103">„Project Operations“ visuotinis diegimas – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="9bb9f-103">Deploy Project Operations - lite</span></span>

<span data-ttu-id="9bb9f-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="9bb9f-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="9bb9f-105">Programoje „Project Operations“ palaikomi keli visuotinio diegimo modeliai.</span><span class="sxs-lookup"><span data-stu-id="9bb9f-105">Project Operations supports multiple deployment models.</span></span> <span data-ttu-id="9bb9f-106">Norėdami nustatyti geriausią visuotinio diegimo modelį, žr. [Visuotinio diegimo tipus](determine-deployment-type.md).</span><span class="sxs-lookup"><span data-stu-id="9bb9f-106">To determine the best deployment model, see [Deployment types](determine-deployment-type.md).</span></span>


> [!IMPORTANT]
> <span data-ttu-id="9bb9f-107">Šis visuotinis diegimas, „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą – yra **„Common Data Service“ vienintelio „Project Operations“ visuotinio diegimo** rezultatas.</span><span class="sxs-lookup"><span data-stu-id="9bb9f-107">This deployment, Lite deployment – deal to proforma invoicing, results in a **Common Data Service-only deployment of Project Operations**.</span></span>

- [<span data-ttu-id="9bb9f-108">„Project Operations“ diegimas į naują CDS aplinką</span><span class="sxs-lookup"><span data-stu-id="9bb9f-108">Install Project Operations into a new CDS environment</span></span>](#new)
- [<span data-ttu-id="9bb9f-109">Diegimas į esamą CDS aplinką</span><span class="sxs-lookup"><span data-stu-id="9bb9f-109">Install into an existing CDS environment</span></span>](#existing)



## <a name="install-project-operations-to-a-new-cds-environment"></a><a name="new"></a><span data-ttu-id="9bb9f-110">„Project Operations“ diegimas į nauja CDS aplinką</span><span class="sxs-lookup"><span data-stu-id="9bb9f-110">Install Project Operations to a new CDS environment</span></span>

1. <span data-ttu-id="9bb9f-111">Kaip [visuotinis arba „Power Platform“ administratorius](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, kurkite naują CDS aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com).</span><span class="sxs-lookup"><span data-stu-id="9bb9f-111">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, create a new CDS environment in the [PowerPlatform admin center](https://admin.powerplatform.com).</span></span> <span data-ttu-id="9bb9f-112">Įsitikinkite, kad įjungti **CDS duomenų bazė** ir **„Dynamics 365“ programos**.</span><span class="sxs-lookup"><span data-stu-id="9bb9f-112">Make sure that **CDS database** and **Dynamics 365 Apps** are enabled.</span></span> <span data-ttu-id="9bb9f-113">Norėdami gauti daugiau informacijos, žr. [Aplinkų kūrimas ir tvarkymas „Power Platform“ administravimo centre](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span><span class="sxs-lookup"><span data-stu-id="9bb9f-113">For more information, see [Create and manage environments in the Power Platform admin center](https://docs.microsoft.com/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).</span></span>
2. <span data-ttu-id="9bb9f-114">Pasirinkite **„Microsoft Dynamics 365 Project Operations“** iš „Dynamics 365“ programų visuotinio diegimo sąrašo.</span><span class="sxs-lookup"><span data-stu-id="9bb9f-114">Select **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span>


## <a name="install-project-operations-to-an-existing-cds-environment"></a><a name="existing"></a><span data-ttu-id="9bb9f-115">„Project Operations“ diegimas į esamą CDS aplinką</span><span class="sxs-lookup"><span data-stu-id="9bb9f-115">Install Project Operations to an existing CDS environment</span></span>

1. <span data-ttu-id="9bb9f-116">Kaip [visuotinis arba „Power Platform“ administratorius](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, raskite aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com), kur norite įdiegti „Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="9bb9f-116">As the [Global or Power Platform Administrator](https://docs.microsoft.com/power-platform/admin/global-service-administrators-can-administer-without-license) with a Project Operations license, locate the environment in the [PowerPlatform admin center](https://admin.powerplatform.com) where you want to install Project Operations.</span></span>
2. <span data-ttu-id="9bb9f-117">Įdiegite **„Microsoft Dynamics 365 Project Operations“** iš „Dynamics 365“ programų visuotinio diegimo sąrašo.</span><span class="sxs-lookup"><span data-stu-id="9bb9f-117">Install **Microsoft Dynamics 365 Project Operations** from the deployment list of Dynamics 365 apps.</span></span> <span data-ttu-id="9bb9f-118">Daugiau informacijos žr. [„Dynamics 365“ programų valdymas](https://docs.microsoft.com/power-platform/admin/manage-apps).</span><span class="sxs-lookup"><span data-stu-id="9bb9f-118">For more information, see [Manage Dynamics 365 apps](https://docs.microsoft.com/power-platform/admin/manage-apps).</span></span>


