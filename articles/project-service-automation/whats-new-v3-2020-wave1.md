---
title: Kas naujo arba pakeista programos „Project Service Automation“ 3.x wave 1 2020 versijoje
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 3 wave 1 2020 versijoje.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 01/24/2020
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 Project Service Automation 3.x wave 1 2020
author: stsporen
ms.assetid: 48b408c1-11e7-4005-abac-8fd7c0b064b1
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 478080c0570b71188c9f1e12b18b5aadc13903e5
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753691"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a><span data-ttu-id="d1480-103">Kas naujo arba pakeista programos „Project Service Automation“ 3 wave 1 2020 versijoje</span><span class="sxs-lookup"><span data-stu-id="d1480-103">What's new or changed in Project Service Automation version 3 wave 1 2020</span></span>
<span data-ttu-id="d1480-104">Šioje temoje aprašomi pagrindiniai naujinimai pereinant į naujausią „Project Service Automation“ (PSA) 3.x wave 1 2020 versijos leidimą.</span><span class="sxs-lookup"><span data-stu-id="d1480-104">The topic highlights key upgrade considerations when moving to the latest release of Project Service Automation (PSA) version 3.x wave 1 2020.</span></span>

## <a name="time-entry"></a><span data-ttu-id="d1480-105">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="d1480-105">Time entry</span></span>
<span data-ttu-id="d1480-106">Laiko įrašo patirtis išplėsta, kad laiko įrašo išplėtimo galimybes būtų galima įtraukti į daugiau kliento scenarijų.</span><span class="sxs-lookup"><span data-stu-id="d1480-106">The time entry experience has been extended to deliver capabilities for extending time entry into more customer scenarios.</span></span> <span data-ttu-id="d1480-107">Tai apima galimybę įtraukti įrašų tipus, kuri dabar pasižymi nauju specifiniu elgesiu, pagrįstu lauko schemos pavadinimu **Laiko įrašo parametrai**, rodomu kaip **Laiko ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="d1480-107">This includes the capability to add entry types, which now drive specific behavior based on the field schema name **Time Entry Settings**, displayed as **Time Source**.</span></span>

### <a name="upgrade-consideration"></a><span data-ttu-id="d1480-108">Pastabos dėl naujinimo</span><span class="sxs-lookup"><span data-stu-id="d1480-108">Upgrade consideration</span></span>
<span data-ttu-id="d1480-109">Norint palaikyti šią funkciją, PSA vaidmenys atnaujinti įtraukiant naujas teises.</span><span class="sxs-lookup"><span data-stu-id="d1480-109">To support this functionality, the roles within PSA have been updated to include new privileges.</span></span> <span data-ttu-id="d1480-110">Šios teisės suteikia skaitymo prieigą prie naujo objekto, **Laiko įrašo parametrai**.</span><span class="sxs-lookup"><span data-stu-id="d1480-110">These privileges grant read access to the new entity, **Time Entry Settings**.</span></span>

<span data-ttu-id="d1480-111">Vartotojams, kuriems reikia registruoti laiką, be esamų vaidmenų turi būti suteiktas vartotojo vaidmuo **Laiko įrašo vartotojas**.</span><span class="sxs-lookup"><span data-stu-id="d1480-111">Users who require the ability to log time should be granted the user role **Time Entry User** in addition to existing roles.</span></span> <span data-ttu-id="d1480-112">Šį vaidmenį sudaro naujos funkcijos ir jis užtikrina, kad laiko įrašas toliau veiks.</span><span class="sxs-lookup"><span data-stu-id="d1480-112">This role includes the new functionality and ensures that time entry will continue to work.</span></span>

### <a name="currently-extended-time-entry-changes"></a><span data-ttu-id="d1480-113">Neseniai išplėstų laiko įrašų pakeitimai</span><span class="sxs-lookup"><span data-stu-id="d1480-113">Currently extended time entry changes</span></span>
<span data-ttu-id="d1480-114">Kad būtų sumažintas poveikis esamiems vartotojo laiko įrašams, šis vaidmens pakeitimas yra vienintelis pagrindinis reikalavimas, būtinas norint naudoti laiko įrašą.</span><span class="sxs-lookup"><span data-stu-id="d1480-114">To minimize the impact to current users of time entry, this role change is the only core requirement necessary to continue utilizing time entry.</span></span> <span data-ttu-id="d1480-115">Jei sukūrėte pasirinktinius rodinius arba atskiras laiko įrašo patirtis, laukus **Laiko įrašo parametras** turite nustatyti į teisingą PSA reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d1480-115">If you have created custom views or separate time entry experiences, you must set the **Time Entry Setting** fields to the correct PSA value.</span></span>
