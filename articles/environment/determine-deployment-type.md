---
title: Visuotinio diegimo tipai
description: Šioje temoje pateikta informacija padės jums nustatyti teisingą visuotinio diegimo tipą, skirtą jūsų įmonės „Project Operations“.
author: stsporen
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: c3cf378caae4510482a8ee6771bf2e6decfe3b48
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948978"
---
# <a name="deployment-types"></a><span data-ttu-id="1b5e1-103">Visuotinio diegimo tipai</span><span class="sxs-lookup"><span data-stu-id="1b5e1-103">Deployment types</span></span>

<span data-ttu-id="1b5e1-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="1b5e1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

> [!IMPORTANT]
> <span data-ttu-id="1b5e1-105">Įsigiję licenciją, pradėkite čia, kad nustatytumėte geriausią „Dynamics 365 Project Operations“ visuotinio diegimo modelį, pasitelkdami [Interaktyvųjį diegimo srautą](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-105">After you purchase the license, start here to determine the best deployment model of Dynamics 365 Project Operations using the [Guided installation flow](https://aka.ms/provisionprojectoperations).</span></span>
> <span data-ttu-id="1b5e1-106">Baigę interaktyvųjį diegimo srautą, būsite nukreipti į tinkamą valdymo portalą, kur galėsite baigti diegimą.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-106">After you have finshed the Guided installation flow, you will be directed to the correct management portal to complete your installation.</span></span> <span data-ttu-id="1b5e1-107">Norėdami baigti diegimą, žr. toliau pateiktą diegimo išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-107">See the deployment details below to complete the installation.</span></span>


## <a name="existing-customers-of-dynamics-using-dynamics-365-project-service-automation"></a><span data-ttu-id="1b5e1-108">Esami „Dynamics“ klientai, naudojantys „Dynamics 365 Project Service Automation“</span><span class="sxs-lookup"><span data-stu-id="1b5e1-108">Existing customers of Dynamics using Dynamics 365 Project Service Automation</span></span>
<span data-ttu-id="1b5e1-109">„Project Operations“ pateikiamos galimybės, pristatytos su „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-109">Project Operations includes the capabilities that shipped with Project Service Automation.</span></span> <span data-ttu-id="1b5e1-110">Ateityje bus išleistas šiems klientams skirtas naujinimo kelias.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-110">An upgrade path will be released for these customers in the future.</span></span>

## <a name="existing-customers-of-dynamics-365-finance-using-project-management-and-accounting"></a><span data-ttu-id="1b5e1-111">Esami „Dynamics 365 Finance“ klientai, naudojantys projektų valdymą ir apskaitą</span><span class="sxs-lookup"><span data-stu-id="1b5e1-111">Existing customers of Dynamics 365 Finance using Project management and accounting</span></span> 

<span data-ttu-id="1b5e1-112">Esami „Finance“ klientai, naudojantys projektų valdymo ir apskaitos funkcijas, gali toliau juos naudoti kaip įprasta.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-112">Existing customers of Finance who use the Project management and accounting functionality can continue use this as is.</span></span> <span data-ttu-id="1b5e1-113">Žr. [„Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams](#pma).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-113">See [Project Operations for stocked/production order scenarios](#pma).</span></span>

<span data-ttu-id="1b5e1-114">„Project Operations“ palaiko kelias visuotinio diegimo parinktis, atitinkančias jūsų reikalavimus.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-114">Project Operations supports multiple deployment options to match your requirements.</span></span> <span data-ttu-id="1b5e1-115">Jei esate naujas ar esamas „Dynamics 365“ klientas, „Project Operations“ gali atitikti jūsų poreikius.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-115">Whether you are a new or existing Dynamics 365 customer, Project Operations can support your needs.</span></span>

<span data-ttu-id="1b5e1-116">Mūsų [Vsuotinio diegimo klausimynas](https://aka.ms/provisionprojectoperations) padės nustatyti tinkamą visuotinį diegimą.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-116">Our [Deployment questionnaire](https://aka.ms/provisionprojectoperations) will help you determine the right deployment.</span></span> <span data-ttu-id="1b5e1-117">Remiantis rezultatais, galėsite pasirinkti vieną iš šių visuotinio diegimo tipų:</span><span class="sxs-lookup"><span data-stu-id="1b5e1-117">The results will guide you toward one of the following deployment types:</span></span>

- [<span data-ttu-id="1b5e1-118">„Lite“ įdiegtis – sandoris į išankstinės sąskaitos faktūros formą</span><span class="sxs-lookup"><span data-stu-id="1b5e1-118">Lite deployment – deal to proforma invoicing</span></span>](#lite)
- [<span data-ttu-id="1b5e1-119">„Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams</span><span class="sxs-lookup"><span data-stu-id="1b5e1-119">Project Operations for resource/non-stocked scenarios</span></span>](#integrated)
- [<span data-ttu-id="1b5e1-120">„Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams</span><span class="sxs-lookup"><span data-stu-id="1b5e1-120">Project Operations for stocked/production order scenarios</span></span>](#pma)

<span data-ttu-id="1b5e1-121">„Project Operations“ palaiko laikomų medžiagų / gamybos užsakymo scenarijus ir nelaikomų medžiagų / ištekliais pagrįstus scenarijus toje pačioje aplinkoje, naudojant juridinio objekto lygio konfigūracijas.</span><span class="sxs-lookup"><span data-stu-id="1b5e1-121">Project Operations support stocked/production order scenarios and non-stocked/resource-based scenarios on the same environment through legal entity-level configurations.</span></span> <span data-ttu-id="1b5e1-122">Pavyzdžiui, „Contoso“ gali išnaudoti laikomų medžiagų / gamybos užsakymo galimybes JAV gamybos įmonėje (juridinis objektas = „Contoso Manufacturing United States“), o nelaikomų medžiagų / ištekliais pagrįstas galimybes – „Contoso Robotics Arms“ priežiūros įmonėje Jungtinėje Karalystėje (juridinis objektas = „Contoso Robotics United Kingdom“).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-122">For example, Contoso can leverage stocked/production order capabilities in their US manufacturing facility (Legal entity = Contoso Manufacturing United States) and non-stocked/resource-based capabilities in their Contoso Robotics Arms servicing facility in UK (Legal entity = Contoso Robotics United Kingdom).</span></span>

## <a name="a-namelitelite-deployment---deal-to-proforma-invoicing"></a><span data-ttu-id="1b5e1-123"><a name="lite"><a/>Supaprastinta įdiegtis – sandoris į išankstinės sąskaitos faktūros formą</span><span class="sxs-lookup"><span data-stu-id="1b5e1-123"><a name="lite"><a/>Lite deployment - deal to proforma invoicing</span></span>
<span data-ttu-id="1b5e1-124">„Lite“ visuotinis diegimas turi šias galimybes:</span><span class="sxs-lookup"><span data-stu-id="1b5e1-124">The lite deployment includes the following capabilities:</span></span>

- <span data-ttu-id="1b5e1-125">Projekto planavimas naudojant „Microsoft Project“, skirtą žiniatinkliui</span><span class="sxs-lookup"><span data-stu-id="1b5e1-125">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="1b5e1-126">Kelių dimensijų įkainiai</span><span class="sxs-lookup"><span data-stu-id="1b5e1-126">Multi-dimensional pricing</span></span>
- <span data-ttu-id="1b5e1-127">Vieningasis išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-127">Unified Resource Management</span></span>
- <span data-ttu-id="1b5e1-128">Laiko sekimas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-128">Time Tracking</span></span>
- <span data-ttu-id="1b5e1-129">Pagrindinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="1b5e1-129">Basic Expense</span></span>
- <span data-ttu-id="1b5e1-130">Sąskaitos faktūros pasiūlymas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-130">Invoice Proposal</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="1b5e1-131">Visuotinio diegimo veiksmai:</span><span class="sxs-lookup"><span data-stu-id="1b5e1-131">Deployment steps:</span></span>
<span data-ttu-id="1b5e1-132">Nustatykite geriausią „Project Operations“ visuotinio diegimo modelį naudodami [Visuotinio diegimo klausimyną](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-132">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1b5e1-133">Šio diegimo ieškokite skiltyse [Užsiregistruokite prenumeratų peržiūros versijai](lite-preview-subscription-sign-up.md) ir [Naujos aplinkos konfigūravimas](lite-deployment.md).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-133">For this deployment, see [Sign-up for preview subscriptions](lite-preview-subscription-sign-up.md) and [Provision new environment](lite-deployment.md).</span></span> 


## <a name="a-nameintegratedproject-operations-for-resourcenon-stocked-scenarios"></a><span data-ttu-id="1b5e1-134"><a name="integrated"><a/>„Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams</span><span class="sxs-lookup"><span data-stu-id="1b5e1-134"><a name="integrated"><a/>Project Operations for resource/non-stocked scenarios</span></span>
<span data-ttu-id="1b5e1-135">„Project Operations“, skirtos ištekliams / nelaikomų medžiagų scenarijams, yra šios galimybės:</span><span class="sxs-lookup"><span data-stu-id="1b5e1-135">The Project Operations for resource/non-stocked scenarios includes the following capabilities:</span></span>
  
- <span data-ttu-id="1b5e1-136">Projekto planavimas naudojant „Microsoft Project“, skirtą žiniatinkliui</span><span class="sxs-lookup"><span data-stu-id="1b5e1-136">Project planning using Microsoft Project for the Web</span></span>
- <span data-ttu-id="1b5e1-137">Kelių dimensijų įkainiai</span><span class="sxs-lookup"><span data-stu-id="1b5e1-137">Multi-dimensional pricing</span></span>
- <span data-ttu-id="1b5e1-138">Vieningasis išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-138">Unified Resource Management</span></span>
- <span data-ttu-id="1b5e1-139">Laiko sekimas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-139">Time Tracking</span></span>
- <span data-ttu-id="1b5e1-140">Pagrindinės išlaidos</span><span class="sxs-lookup"><span data-stu-id="1b5e1-140">Basic Expense</span></span>
- <span data-ttu-id="1b5e1-141">Visos išlaidos</span><span class="sxs-lookup"><span data-stu-id="1b5e1-141">Full Expense</span></span>
- <span data-ttu-id="1b5e1-142">OCR kvitas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-142">Receipt OCR</span></span>
- <span data-ttu-id="1b5e1-143">Pilnas SF išrašymas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-143">Full Invoicing</span></span>
- <span data-ttu-id="1b5e1-144">Pajamų pripažinimas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-144">Revenue Recognition</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="1b5e1-145">Visuotinio diegimo veiksmai:</span><span class="sxs-lookup"><span data-stu-id="1b5e1-145">Deployment steps:</span></span>
<span data-ttu-id="1b5e1-146">Nustatykite geriausią „Project Operations“ visuotinio diegimo modelį naudodami [Visuotinio diegimo klausimyną](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-146">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1b5e1-147">Šio diegimo ieškokite skiltyse [Užsiregistruokite prenumeratų peržiūros versijai](resource-sign-up-preview-subscription.md) ir [Naujos aplinkos konfigūravimas](resource-provision-new-environment.md).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-147">For this deployment, see [Sign-up for preview subscriptions](resource-sign-up-preview-subscription.md) and [Provision new environment](resource-provision-new-environment.md).</span></span> 


## <a name="project-operations-for-stockedproduction-order-scenarios"></a><a name="pma"></a><span data-ttu-id="1b5e1-148">„Project Operations“, skirta laikomų medžiagų / gamybos užsakymo scenarijams</span><span class="sxs-lookup"><span data-stu-id="1b5e1-148">Project Operations for stocked/production order scenarios</span></span>

- <span data-ttu-id="1b5e1-149">Projekto planavimo naudojant WBS</span><span class="sxs-lookup"><span data-stu-id="1b5e1-149">Project planning using WBS</span></span>
- <span data-ttu-id="1b5e1-150">Išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-150">Resource Management</span></span>
- <span data-ttu-id="1b5e1-151">Laiko sekimas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-151">Time Tracking</span></span>
- <span data-ttu-id="1b5e1-152">Visos išlaidos</span><span class="sxs-lookup"><span data-stu-id="1b5e1-152">Full Expense</span></span>
- <span data-ttu-id="1b5e1-153">OCR kvitas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-153">Receipt OCR</span></span>
- <span data-ttu-id="1b5e1-154">Pilnas SF išrašymas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-154">Full Invoicing</span></span>
- <span data-ttu-id="1b5e1-155">Pajamų pripažinimas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-155">Revenue Recognition</span></span>
- <span data-ttu-id="1b5e1-156">Gamybos užsakymai</span><span class="sxs-lookup"><span data-stu-id="1b5e1-156">Production Orders</span></span>
- <span data-ttu-id="1b5e1-157">Medžiagų palaikymas</span><span class="sxs-lookup"><span data-stu-id="1b5e1-157">Materials support</span></span>

### <a name="deployment-steps"></a><span data-ttu-id="1b5e1-158">Visuotinio diegimo veiksmai:</span><span class="sxs-lookup"><span data-stu-id="1b5e1-158">Deployment steps:</span></span>
<span data-ttu-id="1b5e1-159">Nustatykite geriausią „Project Operations“ visuotinio diegimo modelį naudodami [Visuotinio diegimo klausimyną](https://aka.ms/provisionprojectoperations).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-159">Determine the best deployment model of Project Operations using the [Deployment questionnaire](https://aka.ms/provisionprojectoperations).</span></span>

<span data-ttu-id="1b5e1-160">Šio diegimo ieškokite skiltyse [Užsiregistruokite prenumeratų peržiūros versijai](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) ir [Naujos aplinkos konfigūravimas](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span><span class="sxs-lookup"><span data-stu-id="1b5e1-160">For this deployment, see [Sign-up for preview subscriptions](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/dev-tools/sign-up-preview-subscription?toc=/dynamics365/finance/toc.json) and [Provision new environment](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment?toc=/dynamics365/finance/toc.json).</span></span> 



