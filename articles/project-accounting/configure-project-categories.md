---
title: Projekto kategorijų nustatymas
description: Šioje temoje pateikta informacija apie projektų kategorijų nustatymą.
author: sigitac
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d82302f12ba75a92f2de0e9746ad7e61ce0cdc6b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995181"
---
# <a name="configure-project-categories"></a><span data-ttu-id="fbb22-103">Projekto kategorijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="fbb22-103">Configure project categories</span></span>

<span data-ttu-id="fbb22-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="fbb22-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="fbb22-105">„Project Operations“ teikia patikimas galimybes skirstyti projektų pajamas ir išlaidas į kategorijas.</span><span class="sxs-lookup"><span data-stu-id="fbb22-105">Project Operations offers robust capabilities for categorizing revenue and expenses on projects.</span></span> <span data-ttu-id="fbb22-106">Kategorijos leidžia teikti ataskaitas apie projekto operacijas ir jas analizuoti bei vykdyti registravimą DK.</span><span class="sxs-lookup"><span data-stu-id="fbb22-106">Categories provide the ability to report on and analyze project transactions, and drive posting to the general ledger.</span></span>

<span data-ttu-id="fbb22-107">Šioje diagramoje vaizduojama sąsaja tarp operacijų kategorijų, bendrai naudojamų kategorijų ir projektų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="fbb22-107">The following diagram illustrates the correlation between transaction categories, shared categories, and project categories.</span></span> 

<span data-ttu-id="fbb22-108">Operacijų kategorijos yra pagrindinis projektų operacijų grupavimas.</span><span class="sxs-lookup"><span data-stu-id="fbb22-108">Transaction categories are the basic grouping for project transactions.</span></span> <span data-ttu-id="fbb22-109">Šiame grupavime yra bendrai naudojamų kategorijų, kurias galima bendrai naudoti programose ir moduliuose, rinkinys.</span><span class="sxs-lookup"><span data-stu-id="fbb22-109">Within that grouping, there is a set of shared categories that can be shared across applications and modules.</span></span> <span data-ttu-id="fbb22-110">Norint dar labiau atsižvelgti į specifiką, projektų kategorijos yra detaliausias kategorijų lygis.</span><span class="sxs-lookup"><span data-stu-id="fbb22-110">Getting even further into specifics, project categories are the most granular level of categories.</span></span> <span data-ttu-id="fbb22-111">Projektų kategorijos yra būdingos juridiniam subjektui, moduliui ir programai.</span><span class="sxs-lookup"><span data-stu-id="fbb22-111">Project categories are specific to legal entity, module, and application.</span></span>

![Sąsaja tarp operacijų kategorijų, bendrai naudojamų kategorijų ir projektų kategorijų](media/project-categories.png)

## <a name="transaction-categories"></a><span data-ttu-id="fbb22-113">Operacijų kategorijos</span><span class="sxs-lookup"><span data-stu-id="fbb22-113">Transaction categories</span></span>

<span data-ttu-id="fbb22-114">Operacijų kategorijos atitinka pagrindinį projektų operacijų grupavimą ir jos nėra specifinis įmonės ar operacijos tipas.</span><span class="sxs-lookup"><span data-stu-id="fbb22-114">Transaction categories represent the basic grouping for project transactions and are not company or transaction type-specific.</span></span> <span data-ttu-id="fbb22-115">Pavyzdžiui, Contoso naudoja kategorijas Dizainas, Kelionė, Diegimas ir Aptarnavimo operacija projekto operacijoms grupuoti.</span><span class="sxs-lookup"><span data-stu-id="fbb22-115">For example, Contoso Robotics uses Design, Travel, Installation, and Service Transaction categories to group Project transactions.</span></span>

<span data-ttu-id="fbb22-116">Operacijų kategorijos apibrėžiamos „Project Operations“ modulyje.</span><span class="sxs-lookup"><span data-stu-id="fbb22-116">Transaction categories are defined in the Project Operations module.</span></span> 
1. <span data-ttu-id="fbb22-117">Eikite į **Nustatymai**\>**Operacijų kategorijos**, kad atidarytumėte formą.</span><span class="sxs-lookup"><span data-stu-id="fbb22-117">Go to **Settings** \> **Transaction Categories** to open the form.</span></span> 
2. <span data-ttu-id="fbb22-118">Sukurkite naują operacijos kategoriją pasirinkdami **Nauja** arba pažymėdami **Importuoti iš „Excel“**.</span><span class="sxs-lookup"><span data-stu-id="fbb22-118">Create a new transaction category either by selecting **New** or by selecting **Import from Excel**.</span></span>

## <a name="shared-categories"></a><span data-ttu-id="fbb22-119">Bendrai naudojamos kategorijos</span><span class="sxs-lookup"><span data-stu-id="fbb22-119">Shared categories</span></span>

<span data-ttu-id="fbb22-120">„Dynamics 365“ bendro naudojimo kategorijų sąvoka naudojama išlaidoms suskirstyti skirtingose programose, pvz., „Dynamics 365 Finance“ „Dynamics 365 Supply Chain“ ir „Dynamics 365 Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="fbb22-120">Dynamics 365 uses the Shared categories concept to categorize expenses in different applications, such as Dynamics 365 Finance, Dynamics 365 Supply Chain, and Dynamics 365 Project Operations.</span></span> <span data-ttu-id="fbb22-121">Kiekvienai sukurtai operacijos kategorijai „Project Operations“ automatiškai sukuria keturias susijusias bendrai naudojamas kategorijas: valandos, išlaidos, mokesčiai ir elementas.</span><span class="sxs-lookup"><span data-stu-id="fbb22-121">For each Transaction category created, Project Operations automatically creates four related Shared categories: Hours, Expense, Fees, and Item.</span></span> <span data-ttu-id="fbb22-122">Bendrai naudojamas kategorijas galite peržiūrėti ir koreguoti nuėję į **Projektų valdymas ir apskaita**\>**Nustatymas**\>**Kategorijas**\>**Bendrai naudojamos kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="fbb22-122">You can review and adjust the shared categories by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Shared Categories**.</span></span>

## <a name="project-categories"></a><span data-ttu-id="fbb22-123">Projekto kategorijos</span><span class="sxs-lookup"><span data-stu-id="fbb22-123">Project categories</span></span>

<span data-ttu-id="fbb22-124">Projekto kategorijos atitinka detaliausią kategorijos konfigūravimo lygį ir jas turi atskirai kiekvienai įmonei konfigūruoti projekto apskaitininkas.</span><span class="sxs-lookup"><span data-stu-id="fbb22-124">Project categories represent most granular level of category configuration and must be configured separately, and for each company, by a Project accountant.</span></span>

1. <span data-ttu-id="fbb22-125">Eikite į **Projektų valdymas ir apskaita**\>**Nustatymas**\>**Kategorijos**\>**Projekto kategorijos**.</span><span class="sxs-lookup"><span data-stu-id="fbb22-125">Go to **Project Management and Accounting** \> **Setup** \> **Categories** \> **Project categories**.</span></span>
2. <span data-ttu-id="fbb22-126">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="fbb22-126">Select **New**.</span></span>
3. <span data-ttu-id="fbb22-127">Pasirinkite bendrai naudojamos kategorijos, kurią sukūrėte ankstesniame skyriuje, **Kategorijos ID**.</span><span class="sxs-lookup"><span data-stu-id="fbb22-127">Select the **Category ID** of the Shared category you created in the previous section.</span></span> <span data-ttu-id="fbb22-128">„Project Operations“ leidžia naudoti tik tas bendrai naudojamas kategorijas, kurios susietos su operacijų kategorijomis.</span><span class="sxs-lookup"><span data-stu-id="fbb22-128">Project Operations allows using only those shared categories that are associated with transaction categories.</span></span>
4. <span data-ttu-id="fbb22-129">Kategorijos grupės pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="fbb22-129">Select a category group.</span></span>

## <a name="category-groups"></a><span data-ttu-id="fbb22-130">Kategorijos grupės</span><span class="sxs-lookup"><span data-stu-id="fbb22-130">Category groups</span></span>

<span data-ttu-id="fbb22-131">Kategorijų grupės naudojamos norint dalytis ypatybėms, visų pirma registravimo profiliais, tarp susijusių projektų kategorijų.</span><span class="sxs-lookup"><span data-stu-id="fbb22-131">Category groups are used to share properties, primarily posting profiles, between related Project categories.</span></span> <span data-ttu-id="fbb22-132">Kiekvienam operacijos tipui turi būti bent viena kategorijos grupė, o kiekvienai projekto kategorijai priskiriama grupė.</span><span class="sxs-lookup"><span data-stu-id="fbb22-132">There must be at least one category group for each transaction type and each project category is assigned a group.</span></span>

<span data-ttu-id="fbb22-133">„Project Operations“ registravimo specifikacijas apibrėžia projekto išlaidų ir pajamų profilio taisyklės, projektų kategorijos ir kategorijų grupės.</span><span class="sxs-lookup"><span data-stu-id="fbb22-133">The posting specifications in Project Operations are defined by the project cost and revenue profile rules, project categories, and category groups.</span></span> <span data-ttu-id="fbb22-134">Galite nustatyti kategorijų grupes nuėję į **Projektų valdymas ir apskaita**\>**Nustatymai**\>**Kategorijos**\>**Kategorijų grupės**.</span><span class="sxs-lookup"><span data-stu-id="fbb22-134">You can set up category groups by going to **Project management and accounting** \> **Setup** \> **Categories** \> **Category groups**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]