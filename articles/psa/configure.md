---
title: „Project Service Automation“ konfigūravimas
description: „Project Service“ konfigūravimo veiksmai
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8a219ef0166565a550a7836ffeae37ffd514a001
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4129193"
---
# <a name="configure-project-service"></a><span data-ttu-id="f6a45-103">„Project Service“ konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f6a45-103">Configure Project Service</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="f6a45-104">Prieš naudodami „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ galimybes programoje „[!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)]“, skirtas valdyti sąskaitas, projektus ir išteklius, turite atlikti keletą konfigūravimo veiksmų, užtikrindami, kad „[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]“ sprendimas atitinka jūsų organizacijos poreikius.</span><span class="sxs-lookup"><span data-stu-id="f6a45-104">Before you can use the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] automation capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] to manage your accounts, projects, and resources, you need to complete a few configuration steps to ensure the [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] solution matches your organization’s needs.</span></span> <span data-ttu-id="f6a45-105">Šie veiksmai apima:</span><span class="sxs-lookup"><span data-stu-id="f6a45-105">These steps include:</span></span>  
  
-   <span data-ttu-id="f6a45-106">[Laiko vienetų nustatymas](../psa/set-up-time-units.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-106">[Set up time units](../psa/set-up-time-units.md).</span></span> <span data-ttu-id="f6a45-107">Sukonfigūruokite laiko vienetus prekių kataloge, kurį naudosite kaip pagrindą planuodami ir teikdami sąskaitas už savo projektus.</span><span class="sxs-lookup"><span data-stu-id="f6a45-107">Configure the time units in the product catalog that you’ll use as a base for scheduling and billing your projects.</span></span>  
  
-   <span data-ttu-id="f6a45-108">[Valiutų ir valiutų kursų nustatymas](../psa/set-up-currencies-exchange-rates.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-108">[Set up currencies and exchange rates](../psa/set-up-currencies-exchange-rates.md).</span></span> <span data-ttu-id="f6a45-109">Nustatykite valiutas, kurios bus naudojamos jūsų projektuose.</span><span class="sxs-lookup"><span data-stu-id="f6a45-109">Set up the currencies to use for your projects.</span></span>  
  
-   <span data-ttu-id="f6a45-110">[Organizacijos vienetų kūrimas](../psa/create-organizational-units.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-110">[Create organizational units](../psa/create-organizational-units.md).</span></span> <span data-ttu-id="f6a45-111">Nustatykite grupes, kurias naudoja jūsų įmonė, kad suskirstytų savo verslą pagal geografiją, verslo funkcijas ar kitus logiškus kriterijus.</span><span class="sxs-lookup"><span data-stu-id="f6a45-111">Set up the groups that your company uses to divide its business, whether by geography, business function, or other logical division.</span></span>  
  
-   <span data-ttu-id="f6a45-112">[SF dažnumo nustatymas](../psa/set-up-invoice-frequencies.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-112">[Set up invoice frequencies](../psa/set-up-invoice-frequencies.md).</span></span> <span data-ttu-id="f6a45-113">Nustatykite laikotarpius, kuriuos norite naudoti teikdami sąskaitas savo klientams.</span><span class="sxs-lookup"><span data-stu-id="f6a45-113">Set up time periods that you want to use for billing your clients.</span></span>  
  
-   <span data-ttu-id="f6a45-114">[Operacijų kategorijų nustatymas](../psa/configure-transaction-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-114">[Configure transaction categories](../psa/configure-transaction-categories.md).</span></span> <span data-ttu-id="f6a45-115">Nustatykite operacijų kategorijas, pagal kurias jūsų konsultantai gali apmokestinti savo apmokamas ar neapmokamas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="f6a45-115">Set up transaction categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f6a45-116">[Išlaidų kategorijų nustatymas](../psa/configure-expense-categories.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-116">[Configure expense categories](../psa/configure-expense-categories.md).</span></span> <span data-ttu-id="f6a45-117">Nustatykite kategorijas, pagal kurias jūsų konsultantai gali apmokestinti savo apmokamas ar neapmokamas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="f6a45-117">Set up the categories your consultants can charge their billable and unbillable expenses to.</span></span>  
  
-   <span data-ttu-id="f6a45-118">[Produktų katalogo elementų kūrimas](../psa/create-product-catalog-items.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-118">[Create product catalog items](../psa/create-product-catalog-items.md).</span></span> <span data-ttu-id="f6a45-119">Įtraukite savo parduodamus produktus, pvz., programinės įrangos licencijas, į produktų katalogą.</span><span class="sxs-lookup"><span data-stu-id="f6a45-119">Add the products you sell, such as software licenses, to the product catalog.</span></span>  
  
-   <span data-ttu-id="f6a45-120">[Kainoraščio kūrimas](../psa/create-price-list.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-120">[Create a price list](../psa/create-price-list.md).</span></span> <span data-ttu-id="f6a45-121">Sukonfigūruokite skirtingus kainoraščius, atsižvelgdami į tai, kokį mokestį norite taikyti savo klientams už kiekvieno vaidmenį, kurio reikia jų projektui.</span><span class="sxs-lookup"><span data-stu-id="f6a45-121">Configure different price lists, depending on how much you want to charge your clients for each role their project requires.</span></span>  
  
-   <span data-ttu-id="f6a45-122">[Rezervuojamų išteklių nustatymas](../psa/set-up-resources.md).</span><span class="sxs-lookup"><span data-stu-id="f6a45-122">[Set up resources](../psa/set-up-resources.md).</span></span> <span data-ttu-id="f6a45-123">Įtraukite įgūdžius, patirtį, išteklių vaidmenis ir kitą išteklių informaciją, kurios jums reikės savo projektams atlikti.</span><span class="sxs-lookup"><span data-stu-id="f6a45-123">Add the skills, proficiencies, resource roles, and other resource information that you’ll need for your projects.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="f6a45-124">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="f6a45-124">See Also</span></span>  
 <span data-ttu-id="f6a45-125">[„Project Service Automation“ apžvalga](../psa/overview.md) </span><span class="sxs-lookup"><span data-stu-id="f6a45-125">[Overview of Project Service Automation](../psa/overview.md) </span></span>  
 <span data-ttu-id="f6a45-126">[„Project Service Automation“ konfigūravimas](../psa/configure.md) </span><span class="sxs-lookup"><span data-stu-id="f6a45-126">[Configure Project Service Automation](../psa/configure.md) </span></span>  
 <span data-ttu-id="f6a45-127">[Klientų vadovo vadovas](../psa/account-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f6a45-127">[Account Manager Guide](../psa/account-manager-guide.md) </span></span>  
 <span data-ttu-id="f6a45-128">[Projekto vadovo vadovas](../psa/project-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f6a45-128">[Project Manager Guide](../psa/project-manager-guide.md) </span></span>  
 <span data-ttu-id="f6a45-129">[Išteklių vadovo vadovas](../psa/resource-manager-guide.md) </span><span class="sxs-lookup"><span data-stu-id="f6a45-129">[Resource Manager Guide](../psa/resource-manager-guide.md) </span></span>  
 [<span data-ttu-id="f6a45-130">Laiko, išlaidų ir bendradarbiavimo vadovas</span><span class="sxs-lookup"><span data-stu-id="f6a45-130">Time, Expense, and Collaboration Guid</span></span>](../psa/time-expense-collaboration-guide.md)
