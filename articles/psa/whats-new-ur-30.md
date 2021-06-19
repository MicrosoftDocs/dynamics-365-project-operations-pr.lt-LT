---
title: Kas nauja arba pakeista „Project Service Automation“ V3 30 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 30 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 3b6b7dba9c2a22587d27006b9972c950fbb454f2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010436"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a><span data-ttu-id="405aa-103">Kas nauja arba pakeista „Project Service Automation“ V3 30 atnaujintame leidime</span><span class="sxs-lookup"><span data-stu-id="405aa-103">What's new or changed in Project Service Automation Update Release 30, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="405aa-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="405aa-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="405aa-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="405aa-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="405aa-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="405aa-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="405aa-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="405aa-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="405aa-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution.md).</span><span class="sxs-lookup"><span data-stu-id="405aa-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution.md).</span></span>

<span data-ttu-id="405aa-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 30 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="405aa-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 30.</span></span> <span data-ttu-id="405aa-110">Šios versijos komponavimo versijos numeris yra V3.10.51.61 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2021 m. balandžio mėn.</span><span class="sxs-lookup"><span data-stu-id="405aa-110">This version has a build number of V3.10.51.61 and is generally available through a self-update in April 2021.</span></span>

## <a name="update-release-30"></a><span data-ttu-id="405aa-111">30 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="405aa-111">Update Release 30</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="405aa-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="405aa-112">Bug fixes</span></span>

<span data-ttu-id="405aa-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="405aa-113">**Time and Expense**</span></span>

<span data-ttu-id="405aa-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="405aa-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="405aa-115">Kuriant ir įrašant laiko įrašą puslapyje **Spartusis kūrimas** įvyksta klaida, jei pašalintas laukas **Vaidmuo**.</span><span class="sxs-lookup"><span data-stu-id="405aa-115">An error occurs when you create and save a time entry on the **Quick Create** page if the **Role** field is removed.</span></span>
- <span data-ttu-id="405aa-116">Laiko įvesties filtre pritaikomas netinkamas filtro operatorius.</span><span class="sxs-lookup"><span data-stu-id="405aa-116">The Time Entry filter applies the wrong filter operator.</span></span>
- <span data-ttu-id="405aa-117">Nukopijuoti grafikai automatiškai nerodomi laiko įrašo valdiklyje pasirinkus **Kopijuoti savaitę**.</span><span class="sxs-lookup"><span data-stu-id="405aa-117">Copied timesheets aren't automatically displayed when you select **Copy Week** on the time entry control.</span></span>

<span data-ttu-id="405aa-118">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="405aa-118">**Resource Management**</span></span>

<span data-ttu-id="405aa-119">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="405aa-119">The following issues have been fixed:</span></span>

- <span data-ttu-id="405aa-120">Pratęsus rezervavimą, rodoma neteisinga galutiniam rezervavimui priskirta rezervavimo būsena.</span><span class="sxs-lookup"><span data-stu-id="405aa-120">When you extend a booking, the booking status assigned to the hard booking is incorrect.</span></span> <span data-ttu-id="405aa-121">Pratęsus rezervavimą, paisoma rezervavimo būsenos, rezervavimo sąrankos metaduomenyse apibrėžtos kaip **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="405aa-121">Extending a booking respects the booking status defined as **Committed** in the booking setup metadata.</span></span>
- <span data-ttu-id="405aa-122">Nenurodžius tinkamos rezervavimo būsenos, klaidos pranešimas yra neteisingai lokalizuotas.</span><span class="sxs-lookup"><span data-stu-id="405aa-122">When a valid booking status isn't specified, the error message is not correctly localized.</span></span>

<span data-ttu-id="405aa-123">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="405aa-123">**Project Management**</span></span>

<span data-ttu-id="405aa-124">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="405aa-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="405aa-125">Projektų negalima sukurti viena valiuta ir įtraukti susijusių užduočių kita valiuta.</span><span class="sxs-lookup"><span data-stu-id="405aa-125">Projects can't be created in one currency and include related tasks in another currency.</span></span>

<span data-ttu-id="405aa-126">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="405aa-126">**Sales**</span></span>

<span data-ttu-id="405aa-127">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="405aa-127">The following issues have been fixed:</span></span>

- <span data-ttu-id="405aa-128">Nukopijavus kainoraštį, neatnaujinamos kainos.</span><span class="sxs-lookup"><span data-stu-id="405aa-128">When a price list is copied, prices aren't updated.</span></span>
- <span data-ttu-id="405aa-129">Kai savikainos informacijos srityje pateikta kilmės reikšmė, nepavyksta uždaryti pasiūlymo kaip laimėto.</span><span class="sxs-lookup"><span data-stu-id="405aa-129">Closing a quote as won fails when the cost detail has a value for origin.</span></span>
- <span data-ttu-id="405aa-130">Objekte **Projekto užduotis** dalis **Įvertinta savikaina** pervardyta į **Suplanuotos savikainos (bazinės)**.</span><span class="sxs-lookup"><span data-stu-id="405aa-130">On the **Project Task** entity, **Estimated Cost** has been renamed to **Planned Cost (Base)**.</span></span>
- <span data-ttu-id="405aa-131">Sukūrus sąskaitų faktūrų arba jas panaikinus, sugeneruojama neapibrėžtos nuorodos išimtis.</span><span class="sxs-lookup"><span data-stu-id="405aa-131">A null reference exception is generated when invoices are created or deleted.</span></span>
