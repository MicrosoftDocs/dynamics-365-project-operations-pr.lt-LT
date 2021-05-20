---
title: Kas nauja arba pakeista „Project Service Automation“ V3 31 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 31 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 04/26/2021
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
ms.openlocfilehash: a595c0a129ac35d3416984e57908e73e1eaef2fd
ms.sourcegitcommit: 6e1498502461e86cff722ccaf8795ff11c7c47ad
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5945545"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-31-v3"></a><span data-ttu-id="4ad5f-103">Kas nauja arba pakeista „Project Service Automation“ V3 31 atnaujintame leidime</span><span class="sxs-lookup"><span data-stu-id="4ad5f-103">What's new or changed in Project Service Automation Update Release 31, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="4ad5f-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="4ad5f-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="4ad5f-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="4ad5f-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="4ad5f-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="4ad5f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="4ad5f-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 31 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 31.</span></span> <span data-ttu-id="4ad5f-110">Šios versijos komponavimo versijos numeris yra V3.10.52.77 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2021 m. gegužės mėn.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-110">This version has a build number of V3.10.52.77 and is generally available through a self-update in May 2021.</span></span>

## <a name="update-release-31"></a><span data-ttu-id="4ad5f-111">31 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="4ad5f-111">Update Release 31</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="4ad5f-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="4ad5f-112">Bug fixes</span></span>

<span data-ttu-id="4ad5f-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="4ad5f-113">**Time and Expense**</span></span>

<span data-ttu-id="4ad5f-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="4ad5f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="4ad5f-115">Buvo painūs laiko įrašų valdymo komandų mygtukai puslapyje **Rezervuojamasis išteklius**.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-115">Time entry control command buttons on the **Bookable Resource** page were confusing.</span></span>
- <span data-ttu-id="4ad5f-116">Tvirtinant laiko įrašą, dalyje **Project.SetTrackingFields** buvo generuojama neapibrėžtos nuorodos išimtis.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-116">A null reference exception was generated in **Project.SetTrackingFields** when approving a time entry.</span></span>

<span data-ttu-id="4ad5f-117">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="4ad5f-117">**Resource Management**</span></span>

<span data-ttu-id="4ad5f-118">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="4ad5f-118">The following issues have been fixed:</span></span>

- <span data-ttu-id="4ad5f-119">Pasirinkus **Kurti komandos narį**, netinkamai rodomas elemento **Numatytoji patvirtinto rezervavimo būsena** rezervavimo sąrankos metaduomenų parametras.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-119">**Create Team Member** doesn't correctly display the booking setup metadata setting for **Default Booking Committed Status**.</span></span>
- <span data-ttu-id="4ad5f-120">PSA 1.X versiją naujinant į 3.X, įvyksta versijos naujinimo proceso triktis etape **UpgradeResourceRequirements**.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-120">When upgrading from PSA 1.X to 3.X, the upgrade process fails at **UpgradeResourceRequirements**.</span></span>


<span data-ttu-id="4ad5f-121">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="4ad5f-121">**Sales**</span></span>

<span data-ttu-id="4ad5f-122">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="4ad5f-122">The following issues have been fixed:</span></span>

- <span data-ttu-id="4ad5f-123">Sekimo tinklelyje faktinės pajamos sumas konvertuoja į projekto valiutą.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-123">Actual revenue converts the amounts to the project currency in the tracking grid.</span></span>
- <span data-ttu-id="4ad5f-124">Kai organizacijos pagrindinė valiuta skiriasi nuo projekto valiutos, numatytoji valiuta yra neaiški kuriant žurnalų eilutes, pasiūlymų eilutes ir sutarčių eilutes.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-124">The currency default is unclear when creating journal lines, quote lines, and contract lines in scenarios where an organization's base currency differs from the project currency.</span></span>
- <span data-ttu-id="4ad5f-125">Užklausa **Laukiamo taisymo žurnalo tikrinimas** nefiltruojama pagal projektą.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-125">**Pending correction journal validation** query doesn't filter by project.</span></span>
- <span data-ttu-id="4ad5f-126">Likęs projekto pardavimas neteisingai apskaičiuojamas.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-126">Remaining sales are calculated incorrectly on a project.</span></span>
- <span data-ttu-id="4ad5f-127">Pasiūlymai, pagrįsti kontaktu, neįvykdomi, kai jie sukuriami be kainoraščio.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-127">Quotes based on a contact fail when they are created without a price list.</span></span>
- <span data-ttu-id="4ad5f-128">Pasirinkus **Patvirtinti sąskaitą faktūrą** nerodomas joks apdorojimo suktukas.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-128">No processing spinner is shown when you select **Confirm Invoice**.</span></span>
- <span data-ttu-id="4ad5f-129">Pasirinkus **Kurti sąskaitą faktūrą** nerodomas joks apdorojimo suktukas.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-129">No processing spinner is shown when you select **Create Invoice**.</span></span>
- <span data-ttu-id="4ad5f-130">Jei pasiūlymą uždarysite kaip pralaimėtą, rezervavimai nebus atšaukti.</span><span class="sxs-lookup"><span data-stu-id="4ad5f-130">Closing a quote as lost doesn't cancel the bookings.</span></span>







