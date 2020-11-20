---
title: Kas nauja arba pakeista „Project Service Automation“ V3 24 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 24 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/02/2020
ms.topic: article
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 3a37e71be2cce259d8aed0621d13393b6bbe4199
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126583"
---
# <a name="project-service-automation-update-release-24-v3"></a><span data-ttu-id="117df-103">„Project Service Automation“ V3 24 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="117df-103">Project Service Automation Update Release 24, V3</span></span>

<span data-ttu-id="117df-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="117df-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="117df-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="117df-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="117df-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="117df-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="117df-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="117df-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="117df-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="117df-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="117df-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 24 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="117df-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 24.</span></span> <span data-ttu-id="117df-110">Ši versija turi naują komponavimo versijos numerį V 3.10.42.43 ir ją galima pasiekti per 2020 m. spalio mėn. automatinį naujinimą.</span><span class="sxs-lookup"><span data-stu-id="117df-110">This version has a build number of V 3.10.42.43 and is generally available through a self-update in October 2020.</span></span>

## <a name="update-release-24"></a><span data-ttu-id="117df-111">24 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="117df-111">Update Release 24</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="117df-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="117df-112">Bug fixes</span></span>

<span data-ttu-id="117df-113">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="117df-113">**Sales**</span></span>

<span data-ttu-id="117df-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="117df-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="117df-115">Problema nustatant numatytąjį produktų kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="117df-115">Problem while setting default price list of products.</span></span>
- <span data-ttu-id="117df-116">Pasiūlymo laimėjimo efektyvumas yra lėtas dėl įterptųjų kainų sąrašo ir vaidmens kainos įrašų kopijos.</span><span class="sxs-lookup"><span data-stu-id="117df-116">Performance of Quote win is slow due to the embedded price list and role price records copy.</span></span>
- <span data-ttu-id="117df-117">**Projekto sutartis / pardavimų telkinys** > **Produkto linijos elementas / užsakymo linijos kiekis** yra automatiškai suapvalinamas iki artimiausio sveikojo skaičiaus.</span><span class="sxs-lookup"><span data-stu-id="117df-117">**Project Contract/Sales Hub** > **Product Line Item/Order Line Quantity** is automatically rounded to the nearest integer.</span></span>
- <span data-ttu-id="117df-118">Iškelti iki sistemos teisių, kai skaitomi kainoraščiai.</span><span class="sxs-lookup"><span data-stu-id="117df-118">Elevate to system privileges when reading price lists.</span></span>
- <span data-ttu-id="117df-119">Kopijuoti kliento adreso laukus **address1_freighttermscode** ir **address1_shippingmethodcode** į pasiūlymą / užsakymą.</span><span class="sxs-lookup"><span data-stu-id="117df-119">Copy customer address fields **address1_freighttermscode** and **address1_shippingmethodcode** to Quote/Order.</span></span> 


<span data-ttu-id="117df-120">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="117df-120">**Time and Expense**</span></span>

<span data-ttu-id="117df-121">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="117df-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="117df-122">**Laiko įrašo tinklelis** nepalaiko **tik datos** laiko elgsenos.</span><span class="sxs-lookup"><span data-stu-id="117df-122">The **Time Entry Grid** doesn't support **Date Only** time behavior.</span></span>
- <span data-ttu-id="117df-123">**Laiko įrašas** nėra atnaujinamas automatiškai.</span><span class="sxs-lookup"><span data-stu-id="117df-123">**Time Entry** is not refreshing automatically.</span></span> <span data-ttu-id="117df-124">Reikalingas rankinis atnaujinimas.</span><span class="sxs-lookup"><span data-stu-id="117df-124">A manual refresh is required.</span></span>
- <span data-ttu-id="117df-125">Neįmanoma importuoti laiko įrašų iš priskyrimo, kai ištekliaus priskyrimuose yra pertrauka (0 valandų).</span><span class="sxs-lookup"><span data-stu-id="117df-125">Unable to import the time entries from an assignment when there is a break (0 hours) in a resource's assignments.</span></span>
- <span data-ttu-id="117df-126">Kai kuriate laiko įrašą, nustatykite tokią pat pradžią kaip **msdyn_date**.</span><span class="sxs-lookup"><span data-stu-id="117df-126">When creating a time entry, set the start to the same as **msdyn_date**.</span></span>
- <span data-ttu-id="117df-127">Iš naujo įjungti masinį redagavimą laiko įrašui.</span><span class="sxs-lookup"><span data-stu-id="117df-127">Re-enable bulk edit for time entry.</span></span>

<span data-ttu-id="117df-128">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="117df-128">**Resource Management**</span></span>

<span data-ttu-id="117df-129">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="117df-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="117df-130">Bandymas atnaujinti tarp dieninio rezervavimo būseną be reikalavimo, išmes null-ref išimtį.</span><span class="sxs-lookup"><span data-stu-id="117df-130">Trying to update the status of an inter-day booking without a requirement will throw a null-ref exception.</span></span>
- <span data-ttu-id="117df-131">Klaida įkeliant **suderinimo rodinį**.</span><span class="sxs-lookup"><span data-stu-id="117df-131">Error loading the **Reconciliation View**.</span></span>


<span data-ttu-id="117df-132">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="117df-132">**Project Management**</span></span>

<span data-ttu-id="117df-133">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="117df-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="117df-134">**Projekto grafike** keičiant iš **rankinio** į **automatinį**, automatinis įrašymas yra nebaigiamas.</span><span class="sxs-lookup"><span data-stu-id="117df-134">In the **Project Schedule**, when changing from **Manual** to **Auto**, auto save is not completing.</span></span>
- <span data-ttu-id="117df-135">Išlaidų sąnaudos neturėtų skaičiuoti **projekto stebėjimo tinklelio** nuokrypio.</span><span class="sxs-lookup"><span data-stu-id="117df-135">Expense costs should not calculate toward variance on the **Project Tracking Grid**.</span></span>
- <span data-ttu-id="117df-136">**Sąmatų žymės** stulpelių nenuosekli elgsena per įkėlimą prieš **Laiko fazės** tipo keitimą.</span><span class="sxs-lookup"><span data-stu-id="117df-136">Inconsistent behavior for **Estimates tag** columns during load versus changing the **Time-Phase** type.</span></span>
- <span data-ttu-id="117df-137">Faktinė projekto kaina gali neatspindėti galutinių sumų iš **faktinių duomenų**.</span><span class="sxs-lookup"><span data-stu-id="117df-137">The actual cost on a project may not reflect the totals from **Actuals**.</span></span>
- <span data-ttu-id="117df-138">**Numatoma pabaigos data** **Suvestinės** skirtuke nesutampa su **WBS grafiku**.</span><span class="sxs-lookup"><span data-stu-id="117df-138">**Estimated Finish Date** on the **Summary** tab does not match the **WBS Schedule**.</span></span>
- <span data-ttu-id="117df-139">**Faktinių valandų atnaujinimas** atvirkštinėje įtraukoje veikia neteisingai.</span><span class="sxs-lookup"><span data-stu-id="117df-139">**Update Actual Hours** on outdent does not work correctly.</span></span>
- <span data-ttu-id="117df-140">Projekto vadovas, nepriklausantis pagrindiniam **BU**, negali sukurti projekto.</span><span class="sxs-lookup"><span data-stu-id="117df-140">A Project manager outside of root **BU** can't create a project.</span></span>
- <span data-ttu-id="117df-141">Užduoties arba kategorijos pakeitimai **išlaidų sąmatose** neišlieka.</span><span class="sxs-lookup"><span data-stu-id="117df-141">Changes to task or category on **Expense Estimates** are not persisted.</span></span>
- <span data-ttu-id="117df-142">**Sutarties kopija** nukopijuoja sąskaitos faktūros grafikus ir vykdymo būseną.</span><span class="sxs-lookup"><span data-stu-id="117df-142">**Copy of contract** copies the invoice schedules and the run status.</span></span>
- <span data-ttu-id="117df-143">**Atnaujinti faktinius** mygtukas neteisingai apskaičiuoja suvestinės užduotis.</span><span class="sxs-lookup"><span data-stu-id="117df-143">**Refresh Actuals** button incorrectly calculates summary tasks.</span></span>
- <span data-ttu-id="117df-144">„Microsoft Project“ priedai: pataisyti nulinių nuorodų klaidas, jei bet kuris komandos narys turi tuščią išteklių vienetą.</span><span class="sxs-lookup"><span data-stu-id="117df-144">Microsoft Project Add-in: Fix null reference error if any team member has an empty resourcing unit.</span></span>

