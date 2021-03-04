---
title: Kas nauja arba pakeista „Project Service Automation“ V3 20 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 20 naujinimo leidime
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/12/2020
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
ms.openlocfilehash: ee3be43da401af405ab329b9b5a724a2e95c0219
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147123"
---
# <a name="project-service-automation-update-release-20-v3"></a><span data-ttu-id="73074-103">„Project Service Automation“ V3 20 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="73074-103">Project Service Automation Update Release 20, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="73074-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="73074-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="73074-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="73074-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="73074-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="73074-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="73074-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="73074-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="73074-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="73074-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="73074-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 20 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="73074-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 20.</span></span> <span data-ttu-id="73074-110">Šios versijos komponavimo versijos numeris yra V 3.10.31.37 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. birželio mėn.</span><span class="sxs-lookup"><span data-stu-id="73074-110">This version has a build number of V 3.10.31.37 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-20"></a><span data-ttu-id="73074-111">20 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="73074-111">Update Release 20</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="73074-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="73074-112">Bug fixes</span></span>

<span data-ttu-id="73074-113">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="73074-113">**Project Management**</span></span>

<span data-ttu-id="73074-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="73074-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="73074-115">Projekto komandos narių importavimo metu naudojant paskirstymo metodą, kuriam reikalingos valandos, pateikiamas neaiškus klaidos pranešimas, jei nurodytos valandos yra nulis.</span><span class="sxs-lookup"><span data-stu-id="73074-115">Importing project team members with an allocation method that requires hours results in an unclear error message when the specified hours are zero.</span></span>
- <span data-ttu-id="73074-116">Vartotojams nurodoma neteisinga klaida, kai projekto užduoties lauke **Aprašas** įvedamas didžiausias simbolių skaičius.</span><span class="sxs-lookup"><span data-stu-id="73074-116">Users receive an incorrect error when the maximum number of characters have been entered into the **Description** field for a project task.</span></span>
- <span data-ttu-id="73074-117">Puslapyje **„Microsoft Dynamics 365 Project Service Automation” papildinio atsisiuntimas** nukreipiama į anglišką atsisiuntimo puslapį, kai vartotojo kalbos parametrai nustatyti kaip japonų kalba.</span><span class="sxs-lookup"><span data-stu-id="73074-117">The **Microsoft Dynamics 365 Project Service Automation add-in download** page redirects to the English download page when the user’s language settings are set to Japanese.</span></span>
- <span data-ttu-id="73074-118">Įvykus serverio klaidai, kartais lieka sinchronizavimo žyma skirtuke **Grafikas**, esančiame formoje **Projektai**.</span><span class="sxs-lookup"><span data-stu-id="73074-118">When a server error occurs, the synchronization label on the **Schedule** tab of the **Projects** form sometimes remains.</span></span>
- <span data-ttu-id="73074-119">Kai užduotis modifikuojama, į serverį siunčiami nereikalingi užduočių naujinimai.</span><span class="sxs-lookup"><span data-stu-id="73074-119">Redundant task updates are being sent to the server when a task is modified.</span></span>

<span data-ttu-id="73074-120">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="73074-120">**Sales**</span></span>

<span data-ttu-id="73074-121">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="73074-121">The following issues have been fixed:</span></span>

- <span data-ttu-id="73074-122">Formoje **Sutartis** dukart spustelėjus **Kurti sąskaitą faktūrą** sukuriamos dvi vieno faktinių duomenų įrašo sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="73074-122">On the **Contract** form, double-clicking **Create Invoice** creates two invoices for a single actuals record.</span></span>
- <span data-ttu-id="73074-123">Naršyklės „Internet Explorer 11” vartotojai negali kurti išlaidų įrašų.</span><span class="sxs-lookup"><span data-stu-id="73074-123">In Internet Explorer 11, users are unable to create expense entries.</span></span>
- <span data-ttu-id="73074-124">Išlaidų anuliavimas ir pardavimo faktinių duomenų, už kuriuos nebuvo išrašyta sąskaita, anuliavimas nesusieti.</span><span class="sxs-lookup"><span data-stu-id="73074-124">Reversal of Cost and reversal of Unbilled Sales Actuals are not linked.</span></span>
- <span data-ttu-id="73074-125">Mygtuku **Atnaujinti faktinius duomenis**, esančiu formoje **Projektas**, neatnaujinamos **Užduoties faktinės valandos**.</span><span class="sxs-lookup"><span data-stu-id="73074-125">The **Refresh Actuals** button on the **Project** form does not refresh **Task Actual Hours**.</span></span>
- <span data-ttu-id="73074-126">Priedu **PreValidateProjectTeamMemberCreate** galima kurti pasikartojančių bendrųjų rezervuojamų išteklių, kai atributas **msdyn_isgenericresourceprojectscoped** nustatytas kaip **Klaidingas**.</span><span class="sxs-lookup"><span data-stu-id="73074-126">The **PreValidateProjectTeamMemberCreate** plug-in can create duplicate generic bookable resources when the attribute **msdyn_isgenericresourceprojectscoped** is set to **False**.</span></span>
- <span data-ttu-id="73074-127">Parinktimi **Perskaičiuoti** išvalomos apmokestinamos produktu pagrįstos pasiūlymo eilutės išsamios informacijos ir sutarties eilutės išsamios informacijos išlaidos.</span><span class="sxs-lookup"><span data-stu-id="73074-127">**Recalculate** clears chargeable costs of product-based quote line details and contract line details.</span></span>
- <span data-ttu-id="73074-128">Konkrečiose situacijose priede **PostEstimateLineUpdate** rodoma neapibrėžtos nuorodos išimties klaida.</span><span class="sxs-lookup"><span data-stu-id="73074-128">In specific scenarios, the **PostEstimateLineUpdate** plug-in displays a null teference exception error.</span></span>
- <span data-ttu-id="73074-129">Laiko fazės trukmė, esanti **pelningumo analizės diagramoje**, nedera su fiksuotos kainos pasiūlymo eilutės išsamios informacijos apie pasiūlymą trukme.</span><span class="sxs-lookup"><span data-stu-id="73074-129">Time phase duration on the **Profitability Analysis Chart** does not match duration of the costs in the fixed-price quote line detail of the quote.</span></span>
- <span data-ttu-id="73074-130">Vienetų ir vienetų grupių reikšmės išlaidų kategorijose, esančiose **Sutarties eilutės išsami informacija** ir **Pasiūlymo eilutės išsami informacija** formose, nurodomos neteisingai.</span><span class="sxs-lookup"><span data-stu-id="73074-130">Unit and unit group values do not default correctly for expense categories on the **Contract Line Details** and **Quote Line Details** forms.</span></span>
- <span data-ttu-id="73074-131">Sąrašuose **Organizacijos vieneto savikaina** leidžiami datos efektyvumo persidengimai.</span><span class="sxs-lookup"><span data-stu-id="73074-131">**Org Unit Cost Price** lists permit overlaps in the date effectivity.</span></span>
- <span data-ttu-id="73074-132">Vartotojams neleidžiama keisti **OrgUnit**, kai užsakymo tipas nesusijęs su darbu, nes dėl jo bus pateikiama neapibrėžtos nuorodos išimties klaida.</span><span class="sxs-lookup"><span data-stu-id="73074-132">Users are not permitted to change the **OrgUnit** when the order type is not work-based because it will lead to a null reference exception error.</span></span>
- <span data-ttu-id="73074-133">Bandant pereiti iš formos **Pasiūlymo eilutės išsami informacija**, atgal į skirtuką **Pasiūlymas**, forma atnaujinama ir rodomas skirtukas **Suvestinė**.</span><span class="sxs-lookup"><span data-stu-id="73074-133">When attempting to navigate from the **Quote Line Details** form, back to the **Quote** tab, the form refreshes and displays the **Summary** tab.</span></span>
