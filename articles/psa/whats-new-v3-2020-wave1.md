---
title: Kas naujo arba pakeista programos „Project Service Automation“ 3.x wave 1 2020 versijoje
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 3 wave 1 2020 versijoje.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
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
ms.openlocfilehash: fef9cb62e989c693c8b3d00cb15441c284f66554
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5280183"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="6ef1d-103">Kas naujo arba pakeista programos „Project Service Automation“ 3 wave 1 2020 versijoje</span><span class="sxs-lookup"><span data-stu-id="6ef1d-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="6ef1d-104">Šioje temoje aprašomi pagrindiniai naujinimai pereinant į naujausią „Project Service Automation“ (PSA) 3.x wave 1 2020 versijos leidimą.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="6ef1d-105">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="6ef1d-105">Time entry</span></span>
<span data-ttu-id="6ef1d-106">Laiko įrašo patirtis išplėsta, kad laiko įrašo išplėtimo galimybes būtų galima įtraukti į daugiau kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="6ef1d-107">Tai apima galimybę įtraukti įrašų tipus, kuri dabar pasižymi nauju specifiniu elgesiu, pagrįstu lauko schemos pavadinimu **Laiko įrašo parametrai**, rodomu kaip **Laiko ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span> <span data-ttu-id="6ef1d-108">Naujas sprendimas, vadinamas Laiku, išlaidomis, būsenų nustatymu ir patvirtinimais (santr. angl. TESA), buvo įtrauktas palaikyti šią funkciją.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-108">A new solution, called Time, Expense, Statusing, and Approvals (TESA) has been added to support this functionality.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="6ef1d-109">Pastabos dėl naujinimo</span><span class="sxs-lookup"><span data-stu-id="6ef1d-109">Upgrade consideration</span></span>
<span data-ttu-id="6ef1d-110">Norint palaikyti šią funkciją, PSA vaidmenys atnaujinti įtraukiant naujas teises.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-110">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="6ef1d-111">Šios teisės suteikia skaitymo prieigą prie naujo objekto, **Laiko įrašo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-111">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="6ef1d-112">Vartotojams, kuriems reikia registruoti laiką, be esamų vaidmenų turi būti suteiktas vartotojo vaidmuo **Laiko įrašo vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-112">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="6ef1d-113">Šį vaidmenį sudaro naujos funkcijos ir jis užtikrina, kad laiko įrašas toliau veiks.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-113">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

<span data-ttu-id="6ef1d-114">Be to, jei turite pasirinktinių programų modulių, kuriuose yra visos laiko įrašo objekto formos, turėsite iš modulio pašalinti **TESA laiko įrašo sparčiojo kūrimo forma**.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-114">Additionally, if you have any custom app modules that include all forms for the time entry entity, you will be required to remove the **TESA time Entry Quick Create Form** from the module.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="6ef1d-115">Neseniai išplėstų laiko įrašų pakeitimai</span><span class="sxs-lookup"><span data-stu-id="6ef1d-115">Currently extended time entry changes</span></span>
<span data-ttu-id="6ef1d-116">Kad būtų sumažintas poveikis esamiems vartotojo laiko įrašams, šis vaidmens pakeitimas yra vienintelis pagrindinis reikalavimas, būtinas norint naudoti laiko įrašą.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-116">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="6ef1d-117">Jei sukūrėte pasirinktinius rodinius arba atskiras laiko įrašo patirtis, laukus **Laiko įrašo parametras** turite nustatyti į teisingą PSA reikšmę.</span><span class="sxs-lookup"><span data-stu-id="6ef1d-117">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]