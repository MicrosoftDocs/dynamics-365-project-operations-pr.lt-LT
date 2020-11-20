---
title: „Project Operations“ integracijos konfigūravimas juridiniam subjektui
description: Šioje temoje pateikta informacija apie juridinio subjekto integracijos nustatymą naudojant „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/21/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 5d2bb415362a088e01253fbe54f9f06569b4a921
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122893"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="ddd2d-103">„Project Operations“ integracijos konfigūravimas juridiniam subjektui</span><span class="sxs-lookup"><span data-stu-id="ddd2d-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="ddd2d-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="ddd2d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ddd2d-105">Šioje temoje nurodyta, kokius veiksmus reikia atlikti norint sukonfigūruoti „Dynamics 365 Project Operations“ juridiniam subjektui.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="ddd2d-106">Funkcijų klavišų įjungimas naudojant „Dynamics 365 Finance“</span><span class="sxs-lookup"><span data-stu-id="ddd2d-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="ddd2d-107">Norėdami įjungti būtinas funkcijas atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="ddd2d-108">Naudodami „Dynamics 365 Finance“ eikite į **Funkcijų valdymo** darbo sritį.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="ddd2d-109">**Funkcijų sąraše** raskite ir įjunkite šias funkcijas:</span><span class="sxs-lookup"><span data-stu-id="ddd2d-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="ddd2d-110">**Įjungti keletą projekto sutarties eilučių**</span><span class="sxs-lookup"><span data-stu-id="ddd2d-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="ddd2d-111">**Įjungti „Project Operations“ naudojant „Dynamics 365 Customer Engagement“**</span><span class="sxs-lookup"><span data-stu-id="ddd2d-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="ddd2d-112">Jei nematote išvardytų **Funkcijų klavišų**, patikrinkite, ar jūsų „Finance“ versija atitinka mažiausią versijos reikalavimą (programos 10.0.13 versija su visais kokybės atnaujinimais arba naujesnė).</span><span class="sxs-lookup"><span data-stu-id="ddd2d-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="ddd2d-113">Norėdami atnaujinti funkcijų sąrašą pasirinkite **Tikrinti, ar yra naujinimų**.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="ddd2d-114">„Project Operations“ juridinio subjekto visuotinio diegimo scenarijaus apibrėžimas</span><span class="sxs-lookup"><span data-stu-id="ddd2d-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="ddd2d-115">Galite įjungti „Project Operations“ „Dynamics 365 Customer Engagement“ juridinio subjekto lygiu.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="ddd2d-116">Galite turėti vieną juridinį subjektą naudodami „Project Operations“ „Dynamics 365 Customer Engagement“ išteklių / ne atsargomis pagrįstuose scenarijuose.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="ddd2d-117">Toje pačioje aplinkoje galite turėti kitą juridinį subjektą naudodami „Project Operations“ atsargų / gamybos užsakymų scenarijuose.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="ddd2d-118">Naudodami „Dynamics 365 Finance“ eikite į **Projektų valdymas ir apskaita** > **Sąranka** > **Visuotinio projektų valdymo ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="ddd2d-119">Galimų juridinių subjektų sąraše pasirinkite subjektus, kuriuose bus įgalintos kelios sutarčių eilučių ir „Project Operations“ „Dynamics 365 Customer Engagement“ funkcijos.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="ddd2d-120">Palikite nepasirinktus juridinius subjektus, kurie naudos „Project Operations“ atsargų / gamybos užsakymų scenarijams.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="ddd2d-121">Juridinį subjektą galima pasirinkti tik tuo atveju, jeigu jis neturi esamų projektų.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="ddd2d-122">Projektų valdymo ir apskaitos parametrų konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="ddd2d-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="ddd2d-123">Kiekvienas juridinis subjektas, naudojantis „Project Operations“ „Dynamics 365 Customer Engagement“, turi turėti numatytųjų parametrų rinkinį.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="ddd2d-124">Šie parametrai sukonfigūruoti skirtuke **Project Operations**, puslapyje **Projektų valdymo ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="ddd2d-125">Parametrai:</span><span class="sxs-lookup"><span data-stu-id="ddd2d-125">The parameters are:</span></span>

  - <span data-ttu-id="ddd2d-126">**Atsiskaitymo tipo numatytosios reikšmės**: „Project Operations“ naudoja nustatytą atsiskaitymo tipo numatytųjų reikšmių rinkinį, kuris turi būti susietas su eilučių ypatybėms Finansai.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="ddd2d-127">Sukurkite kiekvieno atsiskaitymo tipo įrašą: **Nenurodyta**, **Apmokestinama**, **Neapmokestinama**, **Nemokama** ir **Nepasiekiama**.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="ddd2d-128">**Projekto kategorijų numatytosios reikšmės** : pasirinkite numatytąsias projekto kategorijas, kurios bus naudojamos kiekvienam operacijų tipui.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="ddd2d-129">Šios numatytosios reikšmės bus naudojamos **„Project Operations“ integracijos žurnale** ir įvertinimuose, kur nėra nurodytos faktinio projekto operacijos kategorijos.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="ddd2d-130">**Prognozės** : pasirinkite prognozės modelį, kuris bus naudojamas laiko ir išlaidų įvertinimams.</span><span class="sxs-lookup"><span data-stu-id="ddd2d-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>
