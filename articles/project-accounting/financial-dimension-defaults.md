---
title: Finansinės dimensijos numatytosios reikšmės
description: Šioje temoje pateikta informacija apie tai, kaip nustatyti finansinių dimensijų numatytąsias reikšmes.
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950139"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="667db-103">Finansinės dimensijos numatytosios reikšmės</span><span class="sxs-lookup"><span data-stu-id="667db-103">Financial dimension defaults</span></span>

<span data-ttu-id="667db-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="667db-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="667db-105">„Dynamics 365 Project Operations“ naudoja [finansinių dimensijų](/dynamics365/finance/general-ledger/financial-dimensions) sistemą programoje „Dynamics 365 Finance“, kad teiktų papildomų įžvalgų apie projekto papildomos knygos ir DK operacijas.</span><span class="sxs-lookup"><span data-stu-id="667db-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="667db-106">Numatytąsias finansines dimensijas galima nustatyti klientui, projekto finansavimo šaltiniui, etapui, projekto sutarties eilutei arba projektui.</span><span class="sxs-lookup"><span data-stu-id="667db-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="667db-107">Numatytųjų finansinių dimensijų apibrėžimas klientui</span><span class="sxs-lookup"><span data-stu-id="667db-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="667db-108">Kliento dimensijų numatytosios reikšmės nurodomos programoje „Finance“.</span><span class="sxs-lookup"><span data-stu-id="667db-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="667db-109">Norėdami nustatyti numatytąsias dimensijų reikšmes, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="667db-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="667db-110">Nueikite į **Gautinos sumos** > **Klientai** > **Visi klientai**.</span><span class="sxs-lookup"><span data-stu-id="667db-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="667db-111">Puslapio **Klientai** skirtuke **Finansinės dimensijos** nustatykite konkretaus kliento finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="667db-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="667db-112">Numatytųjų finansinių dimensijų apibrėžimas projekto sutartims</span><span class="sxs-lookup"><span data-stu-id="667db-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="667db-113">Projekto sutartys kuriamos ir tvarkomos naudojant „Common Data Service“ (CDS).</span><span class="sxs-lookup"><span data-stu-id="667db-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="667db-114">Projekto sutarčių apskaitos atributai nustatyti „Finance“ modulyje **Projektų valdymas ir apskaita**.</span><span class="sxs-lookup"><span data-stu-id="667db-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="667db-115">Finansinių dimensijų nustatymas projekto finansavimo šaltiniui</span><span class="sxs-lookup"><span data-stu-id="667db-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="667db-116">Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Projektų sutartys**.</span><span class="sxs-lookup"><span data-stu-id="667db-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="667db-117">Pažymėkite įrašą, kurį norite atnaujinti, ir skirtuke **Projekto sutartis** pasirinkite **Rodyti numatytąją apskaitą**.</span><span class="sxs-lookup"><span data-stu-id="667db-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="667db-118">Išplėskite **Susijusi informacija** ir pasirinkite skirtuką **Finansavimo šaltiniai**.</span><span class="sxs-lookup"><span data-stu-id="667db-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="667db-119">Nustatykite numatytąsias finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="667db-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="667db-120">Atkreipkite dėmesį, kad numatytosios finansinių dimensijų reikšmės gaunamos iš kliento paskyros.</span><span class="sxs-lookup"><span data-stu-id="667db-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="667db-121">Finansinių dimensijų nustatymas projekto sutarties eilutei</span><span class="sxs-lookup"><span data-stu-id="667db-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="667db-122">Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Projektų sutartys**.</span><span class="sxs-lookup"><span data-stu-id="667db-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="667db-123">Pažymėkite įrašą, kurį norite atnaujinti, ir skirtuke **Projekto sutartis** pasirinkite **Rodyti numatytąją apskaitą**.</span><span class="sxs-lookup"><span data-stu-id="667db-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="667db-124">Išplėskite **Susijusi informacija** ir pasirinkite skirtuką **Sutarties eilutės**.</span><span class="sxs-lookup"><span data-stu-id="667db-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="667db-125">Nustatykite numatytąsias finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="667db-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="667db-126">Numatytosios finansinių dimensijų reikšmės taikytinos ir jas galima naudoti tik su fiksuotos kainos (etapų) sutarties eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="667db-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="667db-127">Šios numatytosios reikšmės naudojamos susijusių projektų klientų operacijose ir sąskaitų faktūrų eilutėse.</span><span class="sxs-lookup"><span data-stu-id="667db-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="667db-128">Numatytųjų finansinių dimensijų apibrėžimas projektams</span><span class="sxs-lookup"><span data-stu-id="667db-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="667db-129">Projektai kuriami ir tvarkomi naudojant (CDS).</span><span class="sxs-lookup"><span data-stu-id="667db-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="667db-130">Projektų apskaitos atributai nustatyti „Finance“ modulyje **Projektų valdymas ir apskaita**.</span><span class="sxs-lookup"><span data-stu-id="667db-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="667db-131">Eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai**.</span><span class="sxs-lookup"><span data-stu-id="667db-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="667db-132">Pažymėkite įrašą, kurį norite atnaujinti, ir skirtuke **Projektas** pasirinkite **Rodyti numatytąją apskaitą**.</span><span class="sxs-lookup"><span data-stu-id="667db-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="667db-133">Išplėskite **Susijusi informacija** ir pasirinkite skirtuką **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="667db-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="667db-134">Nustatykite numatytąsias finansinių dimensijų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="667db-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="667db-135">Atkreipkite dėmesį, kad numatytosios finansinių dimensijų reikšmės gaunamos iš kliento paskyros.</span><span class="sxs-lookup"><span data-stu-id="667db-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="667db-136">Jei projektas yra susietas su sutarties eilute, turinčia kelis projektų sutarčių klientus, numatytosioms finansinių dimensijų reikšmėms nustatyti naudojamas pirminis klientas.</span><span class="sxs-lookup"><span data-stu-id="667db-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="667db-137">Projekto numatytosios finansinės dimensijos naudojamos norint nustatyti laiko, išlaidų ir mokesčių operacijų žurnalų eilučių numatytąsias reikšmes **„Project Operations“ integravimo žurnale** ir susijusiose projekto sąskaitų faktūrų eilutėse.</span><span class="sxs-lookup"><span data-stu-id="667db-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]