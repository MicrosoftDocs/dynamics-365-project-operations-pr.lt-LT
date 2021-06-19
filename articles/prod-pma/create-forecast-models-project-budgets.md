---
title: Projektų biudžetų prognozės modelių kūrimas
description: Šioje temoje aprašoma, kaip kurti likusių biudžetų prognozės modelį.
author: Yowelle
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 3549b41fce72b44230ab27de081dade15a912266
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006299"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="e08b7-103">Projektų biudžetų prognozės modelių kūrimas</span><span class="sxs-lookup"><span data-stu-id="e08b7-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e08b7-104">Šioje temoje aprašoma, kaip kurti likusių biudžetų prognozės modelį.</span><span class="sxs-lookup"><span data-stu-id="e08b7-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="e08b7-105">Projektas, kuriam taikoma biudžeto kontrolė, naudoja dviejų tipų biudžetus: pradinį ir likusį.</span><span class="sxs-lookup"><span data-stu-id="e08b7-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="e08b7-106">Kurdami projekto biudžetą turite nurodyti pradinio ir likusio biudžeto prognozės modelius, sukurtus puslapyje **Prognozės modeliai**.</span><span class="sxs-lookup"><span data-stu-id="e08b7-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="e08b7-107">Projektų biudžetai, pagrįsti nurodytais modeliais, kuriami patvirtinant projekto biudžetą.</span><span class="sxs-lookup"><span data-stu-id="e08b7-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="e08b7-108">Prognozės modelis, naudojamas biudžeto kontrolėje, negali turėti papildomo modelio arba būti naudojamas kaip papildomas modelis.</span><span class="sxs-lookup"><span data-stu-id="e08b7-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="e08b7-109">Pasirinkite **Projektų valdymas ir apskaita** > **Sąranka** > **Prognozės**  > **Prognozės modeliai**.</span><span class="sxs-lookup"><span data-stu-id="e08b7-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="e08b7-110">Pasirinkite **Naujas**, kad sukurtumėte naują prognozės modelį, tada įveskite modelio ID numerį ir naujo modelio pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="e08b7-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="e08b7-111">Nustatykite parinktį **Sustabdytas** į parametrą **Taip**, kad būtų išvengta bet kokių prognozės modelio prognozės eilučių pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="e08b7-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="e08b7-112">Jei prognozės eilutės, su kuriomis susietas modelis, turėtų generuoti grynųjų pinigų srauto prognozes didžiojoje knygoje, nustatykite parinktį **Įtraukti į pinigų srauto prognozes** į parametrą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e08b7-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="e08b7-113">Norėdami naudoti projekto datą kaip sąskaitos faktūros datą, nustatykite parinktį **Prognozės sąskaitos faktūros data** į parametrą **Taip**.</span><span class="sxs-lookup"><span data-stu-id="e08b7-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="e08b7-114">Lauke **Biudžeto tipas** pasirinkite vieną iš toliau nurodytų modelių tipų.</span><span class="sxs-lookup"><span data-stu-id="e08b7-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="e08b7-115">**Pradinis biudžetas**: naudokite pradinio biudžeto sumas, kurios patvirtintos sukūrus ir patvirtinus pradinį biudžetą.</span><span class="sxs-lookup"><span data-stu-id="e08b7-115">**Original budget**: Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="e08b7-116">**Likęs biudžetas**: projekto vykdymo metu naudokite likusio biudžeto sumas.</span><span class="sxs-lookup"><span data-stu-id="e08b7-116">**Remaining budget**: Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="e08b7-117">Šio prognozės modelio likučiai sumažinami pagal faktines organizacijas ir padidinami arba sumažinami pagal biudžeto peržiūras.</span><span class="sxs-lookup"><span data-stu-id="e08b7-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="e08b7-118">**Perkėlimas**: naudokite projekto perkeliamas biudžeto sumas.</span><span class="sxs-lookup"><span data-stu-id="e08b7-118">**Carry-forward**: Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="e08b7-119">Perkėlimas – tai pasirinktinis procesas, kurį galima vykdyti, norint perkelti nepanaudotas biudžeto sumas iš vienų finansinių metų į kitus.</span><span class="sxs-lookup"><span data-stu-id="e08b7-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="e08b7-120">Nustatykite toliau nurodytas parinktis pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="e08b7-120">Set the following options as required:</span></span>

   - <span data-ttu-id="e08b7-121">Įjunkite parinktį **Prognozės sąskaitos faktūros data**, norėdami naudoti projekto datą kaip sąskaitos faktūros datą.</span><span class="sxs-lookup"><span data-stu-id="e08b7-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="e08b7-122">Įjunkite parinktį **Prognozė su NG**, norėdami kurti prognozę pagal nebaigtą gamybą (NG), tada pasirinkite NG tipą.</span><span class="sxs-lookup"><span data-stu-id="e08b7-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="e08b7-123">Numatytąjį **biudžeto tipą** galite palikti kaip **nenurodytą** arba galite įvesti naują tipą.</span><span class="sxs-lookup"><span data-stu-id="e08b7-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="e08b7-124">Pakeitus įrašą, biudžeto tipas nekeičiamas.</span><span class="sxs-lookup"><span data-stu-id="e08b7-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="e08b7-125">Jei pakeisite numatytąjį biudžeto tipą, visos kitos parinktys nebus pasiekiamos atnaujinus, o šio prognozės modelio pakartotinai naudoti negalima.</span><span class="sxs-lookup"><span data-stu-id="e08b7-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]