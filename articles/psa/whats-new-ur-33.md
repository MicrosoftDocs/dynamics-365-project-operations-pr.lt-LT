---
title: Kas nauja arba pakeista „Project Service Automation“ V3 33 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 33 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/30/2021
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
ms.openlocfilehash: 2c96e4abd484bb66285421baaad82ead9589bbe9
ms.sourcegitcommit: be5beba71ee9770c0083b4fe5cc89e7ec6b741b8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334572"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-33-v3"></a><span data-ttu-id="f7d2f-103">Kas nauja arba pakeista „Project Service Automation“ V3 33 atnaujintame leidime</span><span class="sxs-lookup"><span data-stu-id="f7d2f-103">What's new or changed in Project Service Automation Update Release 33, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="f7d2f-104">Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-104">We're pleased to announce the latest update for the Microsoft Dynamics 365 Project Service Automation app.</span></span> <span data-ttu-id="f7d2f-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="f7d2f-106">Ji suderinama su „Dynamics 365 9.x“.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-106">It's compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="f7d2f-107">Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page, and install the update.</span></span> <span data-ttu-id="f7d2f-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="f7d2f-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="f7d2f-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 33 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 33.</span></span> <span data-ttu-id="f7d2f-110">Šios komponavimo versijos numeris yra V3.10.54.98 ir ji visuotinai pasiekiama naudojant savaimini naujinimą 2021 m. liepos mėn.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-110">This version has a build number of V3.10.54.98 and is generally available through a self-update in July 2021.</span></span>

## <a name="update-release-33"></a><span data-ttu-id="f7d2f-111">33 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="f7d2f-111">Update Release 33</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="f7d2f-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="f7d2f-112">Bug fixes</span></span>

<span data-ttu-id="f7d2f-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="f7d2f-113">**Time and Expense**</span></span>

<span data-ttu-id="f7d2f-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="f7d2f-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="f7d2f-115">Pateikus galima redaguoti du užrakintus laukus – **msdyn_description** ir **msdyn_externaldescription**.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-115">Two locked fields, **msdyn_description** and **msdyn_externaldescription** are editable after submission.</span></span>
- <span data-ttu-id="f7d2f-116">Jei sukuriamos išlaidos, kurios nėra susijusios su projektu, pateikiamas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-116">An error message occurs if an expense is created that isn't related to a project.</span></span>
- <span data-ttu-id="f7d2f-117">Sukūrus laiko įrašą, išteklių vaidmuo pagal numatytuosius parametrus nustatomas kaip neaktyvus.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-117">When a time entry is created, the resource role defaults to an inactive role.</span></span>
- <span data-ttu-id="f7d2f-118">Su atšauktomis ir panaikintomis išlaidomis susietos žurnalo eilutės nėra panaikinamos.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-118">Journal lines associated with a recalled and deleted expense aren't deleted.</span></span>
- <span data-ttu-id="f7d2f-119">**Laiko įrašo sparčiojo kūrimo formoje** atnaujinkite rodinį **Projekto užduočių sąrašas**, kad pagal numatytuosius parametrus rodomą datą pakeistumėte į užduoties pradžios datą.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-119">On the **Time entry Quick Create Form**, update the **Project Task List** view to change the date displayed by default to the start date of the task.</span></span>
- <span data-ttu-id="f7d2f-120">Kai sukuriate laiko įrašą rezervuojamojo ištekliaus skirtuke **Susiję**, netinkamai sukuriamas prisijungusio vartotojo, o ne pirminio rezervuojamojo ištekliaus laiko įrašas.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-120">When you create a time entry from the **Related** tab of the bookable resource, the time entry is incorrectly created for the signed-in user instead of the parent bookable resource.</span></span>
- <span data-ttu-id="f7d2f-121">Nauji laukai įtraukiami į dialogo langą **Masinio patvirtinimo MDD**.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-121">New fields are added to the **Bulk approval MDD** dialog box.</span></span>

<span data-ttu-id="f7d2f-122">**Projekto planavimas**</span><span class="sxs-lookup"><span data-stu-id="f7d2f-122">**Project planning**</span></span>

<span data-ttu-id="f7d2f-123">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="f7d2f-123">The following issues have been fixed:</span></span>
- <span data-ttu-id="f7d2f-124">Kai darbo valandų šablonai taikomi su sudėtingais kalendoriais, sulėtėja projektų kūrimo našumas.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-124">Slow project creation performance when project work hour templates are applied with complex calendars.</span></span>
- <span data-ttu-id="f7d2f-125">Kai pradžios data yra vėlesnė nei pabaigos data, kopijavimo projekto šablone rodoma klaida dėl kiekvieno lauko laiko komponento skirtumų.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-125">When the start date is greater than the end date, an error displays on the copy project template because of differences in the time component of each field.</span></span>

<span data-ttu-id="f7d2f-126">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="f7d2f-126">**Resource management**</span></span>

<span data-ttu-id="f7d2f-127">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="f7d2f-127">The following issues have been fixed:</span></span>
- <span data-ttu-id="f7d2f-128">Išteklių naudojimo užklausoje naudojamas netinkamas parametras, o dėl XML tinklelyje **Išteklių naudojimas** gaunami neteisingi rezultatai.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-128">An incorrect parameter is used in the resource utilization query and the XML leads to incorrect filter results on the **Resource Utilization** grid.</span></span>
- <span data-ttu-id="f7d2f-129">Patvirtinimo lange **Rezervacijų pratęsimas** rodoma neteisinga rezervacijų pabaigos data.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-129">The **Extend Bookings** confirmation displays incorrect end date for bookings.</span></span>

<span data-ttu-id="f7d2f-130">**Pardavimas**</span><span class="sxs-lookup"><span data-stu-id="f7d2f-130">**Sales**</span></span>

<span data-ttu-id="f7d2f-131">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="f7d2f-131">The following issues have been fixed:</span></span>
- <span data-ttu-id="f7d2f-132">Jei sukuriama kategorijos kaina su trūkstamomis reikšmėmis, pateikiamas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-132">An error message occurs if a category price is created with missing values.</span></span>
- <span data-ttu-id="f7d2f-133">Jei sutarties eilutės etapas sukuriamas be užsakymo eilutės, pateikiamas klaidos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="f7d2f-133">An error message occurs if a contract line milestone is created without an order line.</span></span>
