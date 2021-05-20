---
title: Kas nauja arba pakeista „Project Service Automation“ V3 12 atnaujintame leidime
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 12 atnaujintame leidime V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: 58a12ded135712d8194499ce4a9ba9e4e2aa99bd
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949509"
---
# <a name="project-service-automation-update-release-12-v3"></a><span data-ttu-id="7a776-103">„Project Service Automation“ V3 12 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="7a776-103">Project Service Automation Update Release 12, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7a776-104">Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą.</span><span class="sxs-lookup"><span data-stu-id="7a776-104">We’re pleased to announce the latest update for the Dynamics 365 Project Service Automation (PSA) application.</span></span> <span data-ttu-id="7a776-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="7a776-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="7a776-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="7a776-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="7a776-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="7a776-107">To update to this release, visit the Admin Center for Dynamics 365 online, and go to the solutions page to install the update.</span></span> <span data-ttu-id="7a776-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="7a776-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="7a776-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 12 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="7a776-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 12.</span></span> <span data-ttu-id="7a776-110">Ši versija turi naują komponavimo versijos numerį V3.10.2.34 ir ją galima pasiekti per 2019 m. spalio mėn. automatinį naujinimą.</span><span class="sxs-lookup"><span data-stu-id="7a776-110">This version has a build number of V3.10.2.34 and is generally available through a self-update in October 2019.</span></span>

## <a name="update-release-12"></a><span data-ttu-id="7a776-111">12 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="7a776-111">Update Release 12</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="7a776-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="7a776-112">Bug fixes</span></span>

- <span data-ttu-id="7a776-113">Laikas ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="7a776-113">Time and Expense</span></span>

    - <span data-ttu-id="7a776-114">Sutaisyta: laiko įrašų klaidų pranešimai turi labiau susijusį kontekstą.</span><span class="sxs-lookup"><span data-stu-id="7a776-114">Fixed: Time entry error messaging has been updated with more relevant context.</span></span>
    - <span data-ttu-id="7a776-115">Sutaisyta: laiko įrašų tinklelyje ir grafike tinkamai rodoma vertikali slinkties juosta, kai reikia.</span><span class="sxs-lookup"><span data-stu-id="7a776-115">Fixed: Time entry grid and schedule correctly displays the vertical scrollbar when required.</span></span>
    - <span data-ttu-id="7a776-116">Sutaisyta: pateiktas išlaidas ir laiko įrašus galima patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="7a776-116">Fixed: Submitted expense and time entries can be approved.</span></span>
    - <span data-ttu-id="7a776-117">Sutaisyta: sutvarkytas atšaukimo patvirtinimo patvirtinimo dialogo lango pranešimas, kad atspindėtų patvirtinimo būseną, kai pakeičiama iš **Patvirtinta** į **Pateikta**.</span><span class="sxs-lookup"><span data-stu-id="7a776-117">Fixed: Cancel approval confirmation dialog message has been corrected to reflect the status of the approval when changed from **Approved** to **Submitted**.</span></span>
    - <span data-ttu-id="7a776-118">Sutaisyta: laukai **Kaina**, **Vienetas** ir **Kiekis** dabar užrakinami išlaidų įraše po to, kai patvirtinami.</span><span class="sxs-lookup"><span data-stu-id="7a776-118">Fixed: **Price**, **Unit**, and **Quantity** fields are now locked on the Expense record after it is has been approved.</span></span>

- <span data-ttu-id="7a776-119">Projektų valdymas</span><span class="sxs-lookup"><span data-stu-id="7a776-119">Project Management</span></span>

    - <span data-ttu-id="7a776-120">Sutaisyta: pašalintas **Naujas** veiksmas **Komandos narys** pagrindinėje formoje.</span><span class="sxs-lookup"><span data-stu-id="7a776-120">Fixed: **New** action on **Team member** main form has been removed.</span></span>
    - <span data-ttu-id="7a776-121">Sutaisyta: išteklių priskyrimai atnaujinti, kad reaguotų į netikslaus apvalinimo klaidas, dėl kurių pasikeičia užduoties pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="7a776-121">Fixed: Resource assignments have been updated to account for inaccurate rounding errors, which lead to a shift in a task’s end date.</span></span>
    - <span data-ttu-id="7a776-122">Sutaisyta: užduočių tinklelyje su serveriu susijusios klaidos bus rodomos vartotojui.</span><span class="sxs-lookup"><span data-stu-id="7a776-122">Fixed: In the task grid, relevant server-side errors will be surfaced to the user.</span></span>
    - <span data-ttu-id="7a776-123">Sutaisyta: komandos nario vardas, o ne pareigų pavadinimas dabar pateikiamas užduoties žmonių parinkiklyje.</span><span class="sxs-lookup"><span data-stu-id="7a776-123">Fixed: The team member’s name now renders in the task people picker instead of the position name.</span></span>

- <span data-ttu-id="7a776-124">Išteklių valdymas</span><span class="sxs-lookup"><span data-stu-id="7a776-124">Resource Management</span></span>

    - <span data-ttu-id="7a776-125">Sutaisyta: išteklių projektams reikalavimų išsami informacija, sukurta pagal šabloną, dabar naujo projekto kalendorių.</span><span class="sxs-lookup"><span data-stu-id="7a776-125">Fixed: Resource requirement details for projects created from a template now use the project calendar.</span></span>
    - <span data-ttu-id="7a776-126">Sutaisyta: įgūdžiai ir kompetencijos dabar perkeliamos iš vaidmens pagrindinių duomenų į išteklių reikalavimą, sukurtą tam vaidmeniui.</span><span class="sxs-lookup"><span data-stu-id="7a776-126">Fixed: Skills and competencies now default from role master data to the resource requirement created for that role.</span></span>

- <span data-ttu-id="7a776-127">Sales</span><span class="sxs-lookup"><span data-stu-id="7a776-127">Sales</span></span>

    - <span data-ttu-id="7a776-128">Sutaisyta: dubliuoti objekto ID, randami **Sutarties pagrindinėje** formoje.</span><span class="sxs-lookup"><span data-stu-id="7a776-128">Fixed: Duplicate object IDs found on the **Contract main** form.</span></span>
    - <span data-ttu-id="7a776-129">Sutaisyta: logika buvo atnaujinta taip, kad skirtuke **Pasiūlymo analizė** būtų rodomi skirtuko sąrankos metaduomenys.</span><span class="sxs-lookup"><span data-stu-id="7a776-129">Fixed: Logic has been updated to make the **Quote Analysis** tab visible so that it displays the metadata setup of the tab.</span></span>
    - <span data-ttu-id="7a776-130">Sutaisyta: apskaitos data faktiniame įraše dabar gaunama iš laiko datos / išlaidų įrašo datos, o ne patvirtinimo datos.</span><span class="sxs-lookup"><span data-stu-id="7a776-130">Fixed: Accounting date on the actual record now comes from the date of the time/expense entry date and not the date of the approval.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]