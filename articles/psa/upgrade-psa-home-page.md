---
title: Pagrindinio puslapio atnaujinimas
description: Šioje temoje nurodoma, kur rasti svarbią informaciją apie naujas ir pakeistas „Dynamics 365 Project Service Automation“ funkcijas bei naujinimo į naujausią versiją procesą.
manager: kfend
ms.prod: ''
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
author: rumant
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: e30da3a5ade6d8bafcdc45801b830196841997bf
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5150093"
---
# <a name="upgrade-home-page"></a><span data-ttu-id="d3ad3-103">Pagrindinio puslapio atnaujinimas</span><span class="sxs-lookup"><span data-stu-id="d3ad3-103">Upgrade home page</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a><span data-ttu-id="d3ad3-104">Atnaujinti iš PSA versijos 2.x arba 1.x į versiją 3.x</span><span class="sxs-lookup"><span data-stu-id="d3ad3-104">Upgrade from PSA version 2.x or 1.x to version 3.x</span></span>

### <a name="new-instances"></a><span data-ttu-id="d3ad3-105">Nauji egzemplioriai</span><span class="sxs-lookup"><span data-stu-id="d3ad3-105">New instances</span></span>

<span data-ttu-id="d3ad3-106">Nuo 2019 m. gegužės 17 d., kai kuriant naują egzempliorių pasirenkama „Project Service Automation“, pagal numatytuosius nustatymus įdiegiama 3.x versija.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-106">As of May 17, 2019, when Project Service Automation is selected during the provisioning of a new instance, version 3.x is installed by default.</span></span>

### <a name="existing-instances"></a><span data-ttu-id="d3ad3-107">Esami egzemplioriai</span><span class="sxs-lookup"><span data-stu-id="d3ad3-107">Existing instances</span></span>

<span data-ttu-id="d3ad3-108">Anksčiau klientai, kurie turi PSA 2.x versijos egzempliorių ir turėjo jį atnaujinti į 3.x versiją, kuri yra vieningąja kliento sąsaja (UCI) pagrįsta PSA versija, turėjo susisiekti su „Microsoft“ palaikymo tarnyba ir pateikti išsamią informaciją apie savo egzempliorių, kad palaikymo tarnyba galėtų nustatyti, kad egzempliorių būtų galima atnaujinti į 3.x versiją.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-108">Previously, customers who have an instance of PSA version 2.x and needed to upgrade to version 3.x, which is the Unified client interface-based (UCI) version of PSA, had to contact Microsoft Support and provide the details of their instance so that support could enable the instance for upgrade to version 3.x.</span></span> <span data-ttu-id="d3ad3-109">Nuo 2020 m. kovo 1 d. klientai, turintys PSA 2.x versijos egzempliorių ir kuriems reikia atnaujinti versiją į 3.x versiją, galės atnaujinti savo egzempliorius tiesiai iš administravimo portalo, neturėdami susisiekti su „Microsoft“ palaikymo tarnyba.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-109">As of March 1, 2020, customers who have an instance of PSA version 2.x and need to upgrade to version 3.x, will able to upgrade their instances directly from the Admin portal without having to contact Microsoft Support.</span></span>  

> [!NOTE]
> <span data-ttu-id="d3ad3-110">PSA 3.x versijoje yra reikšmingų pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-110">PSA version 3.x includes significant changes.</span></span> <span data-ttu-id="d3ad3-111">Ji sukurta naudojant vieningosios sąsajos sistemą siekiant užtikrinti patobulintą vartotojų patirtį.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-111">It has been built on the Unified Interface framework to help provide an improved user experience.</span></span> <span data-ttu-id="d3ad3-112">Pertvarkyta programa užtikrina nuoseklią, vienodą vartotojo sąsają (UI), kurią rengiant pasirinktas poreikius atitinkantis dizainas, kad būtų galima optimaliai peržiūrėti bet kokio dydžio ekrane arba bet kokiame įrenginyje.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-112">The redesigned app delivers a consistent, uniform user interface (UI), and it follows responsive design principles for optimal viewing on any screen size or device.</span></span> <span data-ttu-id="d3ad3-113">Programoje atlikta ir kitų pakeitimų.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-113">There have been other changes throughout the application.</span></span> <span data-ttu-id="d3ad3-114">Kai kurios iš pakeistų sričių yra išteklių kainodara, rezervavimas ir priskyrimas, laikas, išlaidos ir patvirtinimai.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-114">Some of the areas that have been changed include pricing, booking and assigning resources, time, expenses, and approvals.</span></span>

<span data-ttu-id="d3ad3-115">Prieš pradedant naujinimo procesą rekomenduojame atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="d3ad3-115">Before you begin the upgrade process, we recommend that you complete the following tasks:</span></span>

- <span data-ttu-id="d3ad3-116">Patikrinkite, ar nustatytame egzemplioriuje yra įdiegta ir „Dynamics 365 Field Service“, ir „Project Service Automation“.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-116">Verify whether both Dynamics 365 Field Service and Project Service Automation are installed on the identified instance.</span></span> <span data-ttu-id="d3ad3-117">Jei abu sprendimai įdiegti, prieš tęsdami įprastą egzemplioriaus naudojimą turėtumėte suplanuoti atnaujinti juos abu.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-117">If both solutions are installed, you should plan to upgrade both before you resume regular use of the instance.</span></span>
- <span data-ttu-id="d3ad3-118">Atidžiai peržiūrėkite toliau pateiktas temas.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-118">Carefully review the following topics.</span></span> <span data-ttu-id="d3ad3-119">Žinodami apie versijų skirtumus ir juos suprasdami galėsite lengviau vykdyti atnaujinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-119">Awareness and understanding of the changes between versions will help you with the upgrade process.</span></span> <span data-ttu-id="d3ad3-120">Šiose temose pateikta informacija apie svarbiausius PSA pakeitimus kartu su dalykais, į kuriuos reikia atsižvelgti, ir rekomendacijomis planuojant atnaujinimą į 3.x versiją.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-120">These topics provide information about the major changes in PSA, together with considerations and recommendations for planning your upgrade to version 3.x.</span></span>

    - [<span data-ttu-id="d3ad3-121">Kas nauja arba pakeista programos „Project Service Automation“ 3 versijoje</span><span class="sxs-lookup"><span data-stu-id="d3ad3-121">What's new or changed in Project Service Automation version 3</span></span>](whats-new-changed-v3.md)
    - [<span data-ttu-id="d3ad3-122">Atnaujinimo aptarimas - iš „Project Service Automation“ 2.x arba 1.x versijos į 3 versiją</span><span class="sxs-lookup"><span data-stu-id="d3ad3-122">Upgrade considerations - Project Service Automation version 2.x or 1.x to version 3</span></span>](upgrade-v3.md)

- <span data-ttu-id="d3ad3-123">Prieš naujindami gamybos egzempliorius, atnaujinkite smėlio dėžės egzempliorius, kad įvertintumėte diegimo keitimus.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-123">Upgrade your sandbox instance to evaluate the changes in your implementation before you upgrade your production instance.</span></span>

<span data-ttu-id="d3ad3-124">Kai peržiūrėsite temas, kurios buvo paminėtos anksčiau, ir būsite pasiruošę atnaujinti į PSA 3.x versiją arba UCI pagrįstą versiją, pateikite „Microsoft“ palaikymo tarnybai užklausą, kad atnaujinimas būtų pasiekiamas iš administravimo centro.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-124">After you've reviewed the topics that were mentioned earlier and are ready to upgrade to PSA version 3.x or the UCI-based version, submit a request to Microsoft support to make the upgrade available from Admin center.</span></span> <span data-ttu-id="d3ad3-125">Užklausoje nurodykite savo egzemplioriaus išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-125">In your request, provide the details of your instance.</span></span>

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a><span data-ttu-id="d3ad3-126">Senesnės PSA versijos (PSA 2.x versija) naujai sukurtame egzemplioriuje</span><span class="sxs-lookup"><span data-stu-id="d3ad3-126">Older versions of PSA (PSA version 2.x) in a newly created instance</span></span>

<span data-ttu-id="d3ad3-127">Nuo 2019 m. gegužės 17 d. visų naujų egzempliorių numatytasis klientas bus UCI.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-127">As of May 17, 2019, all new instances will have UCI as the default client.</span></span> <span data-ttu-id="d3ad3-128">Norint suderinti su šiuo pakeitimu, PSA 3.x versija ir „Field Service“ 8.x versija bus parengta pagal numatytuosius nustatymus, nes šios versijos skirtos darbui su UCI klientu.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-128">For alignment with this change, PSA version 3.x and Field Service version 8.x will be provisioned by default, because these versions are designed to work with the UCI client.</span></span>

<span data-ttu-id="d3ad3-129">Nuo 2020 m. kovo 1 d. „Dynamics PSA“ klientai nebegalės kurti naujos aplinkos su senesnėmis PSA versijomis, pvz., PSA 2.x arba senesne versija.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-129">Starting March 1, 2020, customers of Dynamics PSA will no longer be able to create a new environment with older versions of PSA, for example PSA version 2.x or lower.</span></span> <span data-ttu-id="d3ad3-130">Bet kokią naują aplinką bus galima gauti tik naudojant PSA 3.x versiją.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-130">Any new environment will be to get only version 3.x of PSA.</span></span>

> [!NOTE]
> <span data-ttu-id="d3ad3-131">Norėdami gauti geriausią patirtį, kai naudojatės senesnėmis „Field Service“ ir PSA programomis, eikite į puslapį **Sistemos parametrai** ir lauke **Naudoti tik naują vieningąją sąsają (rekomenduojama)** pasirinkite **Ne**, nes šios versijos nėra sukurtos taip, kad jas būtų galima tinkamai įkelti į UCI.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-131">For the best experience when you use older versions of the Field Service and PSA applications, go to the **System settings** page and for the field, **Use the new Unified Interface only (recommended)** field, select **No** as these versions aren't designed to be correctly loaded in UCI.</span></span> <span data-ttu-id="d3ad3-132">Išjungę UCI, galite atidaryti ir paleisti šias „Field Service“ ir PSA versijas naudodami senąjį žiniatinklio klientą.</span><span class="sxs-lookup"><span data-stu-id="d3ad3-132">After you have turned off UCI, you can open and run these versions of Field Service and PSA by using the old web client.</span></span> 
