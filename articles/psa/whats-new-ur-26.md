---
title: Kas nauja arba pakeista „Project Service Automation“ V3 26 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 26 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 669b3ca4601bdac483db4e1d7f55a8bf5b3d9661
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5948834"
---
# <a name="project-service-automation-update-release-26-v3"></a><span data-ttu-id="a29d1-103">„Project Service Automation“ V3 26 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="a29d1-103">Project Service Automation Update Release 26, V3</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a29d1-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="a29d1-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="a29d1-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="a29d1-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="a29d1-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="a29d1-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="a29d1-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="a29d1-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="a29d1-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="a29d1-108">For more information, see [Install, update, or remove a preferred solution](/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="a29d1-109">Šioje temoje išvardytos naujos arba pakeistos funkcijos ir pataisos, susijusios su 3 versijos „Project Service Automation“ 26 atnaujintu leidimu.</span><span class="sxs-lookup"><span data-stu-id="a29d1-109">This topic lists the features and fixes that are new or changed for Project Service Automation Update Release 26, V3.</span></span> <span data-ttu-id="a29d1-110">Šios versijos komponavimo versijos numeris yra V3.10.44.59 ir ji visuotinai pasiekiama įdiegiant savaiminį 2020 m. gruodžio mėn. naujinimą.</span><span class="sxs-lookup"><span data-stu-id="a29d1-110">This version has a build number of V3.10.44.59 and is generally available through a self-update in December 2020.</span></span>

## <a name="update-release-26"></a><span data-ttu-id="a29d1-111">26 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="a29d1-111">Update Release 26</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="a29d1-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="a29d1-112">Bug fixes</span></span>

<span data-ttu-id="a29d1-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="a29d1-113">**Time and Expense**</span></span>

<span data-ttu-id="a29d1-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="a29d1-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="a29d1-115">Vartotojai gali pakeisti užduotį laiko įraše, kuris buvo patvirtintas / pateiktas.</span><span class="sxs-lookup"><span data-stu-id="a29d1-115">Users are able to change the task on a time entry that has been approved/submitted.</span></span>
- <span data-ttu-id="a29d1-116">Įrašant laiko įrašą pateikiama klaida Objekto nuoroda nenustatyta.</span><span class="sxs-lookup"><span data-stu-id="a29d1-116">"Object Reference Not Set" error when saving time entry.</span></span>
- <span data-ttu-id="a29d1-117">Importuojant laiko įrašus iš išteklių priskyrimo sukuriami laiko įrašai su netinkamomis DateTime reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="a29d1-117">Time entry import from resource assignments creates time entries with the incorrect DateTime values.</span></span>
- <span data-ttu-id="a29d1-118">Įdiegus „Project Service Automation“ ir „Field Service“ programą, mygtukas **Naujas** rodomas du kartus „Field Service“ programos laiko įrašų komandų juostoje.</span><span class="sxs-lookup"><span data-stu-id="a29d1-118">When Project Service Automation and the Field Service app are both installed, the **New** button is displaying twice on the command bar for time entries in the Field Service app.</span></span>
- <span data-ttu-id="a29d1-119">Langelių **Leisti vienetą** ir **Vienetų grupė** atnaujinimai nuo šiol veikia tinklelyje **Išlaidų sąmatos**.</span><span class="sxs-lookup"><span data-stu-id="a29d1-119">**Allow Unit** and **Unit group** cells updates now work on the **Expense Estimates** grid.</span></span>
- <span data-ttu-id="a29d1-120">Į formą **Laiko įrašo redagavimas** įtraukta **Laiko planavimo juosta**.</span><span class="sxs-lookup"><span data-stu-id="a29d1-120">**Update Time Entry Edit** form includes **Timeline**.</span></span>
- <span data-ttu-id="a29d1-121">Patvirtinus ne projekto laiko įrašų laiką užblokuojama sistema, kai ieškoma projekto tvirtintojo vaidmens.</span><span class="sxs-lookup"><span data-stu-id="a29d1-121">Time approval for non-project time entries blocks the system when searching for a project approver role.</span></span>

<span data-ttu-id="a29d1-122">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="a29d1-122">**Resource Management**</span></span>

<span data-ttu-id="a29d1-123">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="a29d1-123">The following issues have been fixed:</span></span>

- <span data-ttu-id="a29d1-124">Prie priedo **PostProjectCreate** pridėta patikra, tikrinanti pirminį reikalavimą prieš jį sukuriant.</span><span class="sxs-lookup"><span data-stu-id="a29d1-124">Added validation in the **PostProjectCreate** plug-in to check for a primary requirement before creating one.</span></span>
- <span data-ttu-id="a29d1-125">Sparčiojo kūrimo forma **Projekto komandos narys** pateikia „null“ nuorodos išimtį, kai iš formos pašalinami laukai.</span><span class="sxs-lookup"><span data-stu-id="a29d1-125">**Project Team Member** quick create form throws a null reference exception if fields are removed from the form.</span></span>
- <span data-ttu-id="a29d1-126">Nepavyks generuoti 12 valandų reikalavimų 1 metų laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="a29d1-126">Generate requirements for 12 hours over 1 year will fail.</span></span>
- <span data-ttu-id="a29d1-127">Patobulintas klaidos pranešimas dėl „null“ nuorodos išimties, pateikiamos kuriant išteklių reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="a29d1-127">Improved error message null reference exception during resource requirement creation.</span></span>

<span data-ttu-id="a29d1-128">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="a29d1-128">**Project Management**</span></span>

<span data-ttu-id="a29d1-129">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="a29d1-129">The following issues have been fixed:</span></span>

- <span data-ttu-id="a29d1-130">Patobulinta patikra, siekiant išspręsti „null“ nuorodos išimties problemą, kylančią priede **PreProjectUpdate**.</span><span class="sxs-lookup"><span data-stu-id="a29d1-130">Improved validation to address null reference exception generated in the **PreProjectUpdate** plug-in.</span></span>
- <span data-ttu-id="a29d1-131">Projektai, kuriuos paskelbė „Microsoft Project“ kompiuterio papildinys, panaikina nepriskirtus priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="a29d1-131">Projects published by the Microsoft Project desktop add-in delete unassigned assignments.</span></span>
- <span data-ttu-id="a29d1-132">Pridėta nauja patikra, kai užduoties projekto nuoroda yra netinkama dėl „null“ nuorodos išimties, pateikiamos priede **PreValidateProjectTaskUpdate**.</span><span class="sxs-lookup"><span data-stu-id="a29d1-132">Added new validation when a task’s project reference is invalid due to null reference exception in **PreValidateProjectTaskUpdate** plug-in.</span></span>
- <span data-ttu-id="a29d1-133">Komandos narių tinklelyje nerodomi atskiri priskyrimai komandos nario įraše.</span><span class="sxs-lookup"><span data-stu-id="a29d1-133">Team Member grid does not show distinct assignments on the team member record.</span></span>
- <span data-ttu-id="a29d1-134">Pridėta nauja patikra ir klaidos pranešimai dėl „null“ nuorodos išimties, pateikiamos priede **PreProjectTaskDelete**.</span><span class="sxs-lookup"><span data-stu-id="a29d1-134">Added new validation and error messages due to null reference exception in **PreProjectTaskDelete** plug-in.</span></span>

<span data-ttu-id="a29d1-135">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="a29d1-135">**Sales**</span></span>

<span data-ttu-id="a29d1-136">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="a29d1-136">The following issues have been fixed:</span></span>

- <span data-ttu-id="a29d1-137">Pasiūlyme arba sutartyje pasirinkus projektu pagrįstą eilutę, mygtukas **Pasiūlymas** turėtų būti rodomas tik tada, kai pasirenkam produktu pagrįsta eilutė, susieta su esamu produktu.</span><span class="sxs-lookup"><span data-stu-id="a29d1-137">When selecting a project-based line in quote or contract, the **Suggestion** button should only be visible when selecting a product-based line associated with an existing product.</span></span>
- <span data-ttu-id="a29d1-138">Teisė **Create_Product** atskirta nuo teisės **Create_ProjectContract**.</span><span class="sxs-lookup"><span data-stu-id="a29d1-138">Split **Create_Product** privilege from **Create_ProjectContract** privilege.</span></span>
- <span data-ttu-id="a29d1-139">Panaikinus sąskaitos faktūros eilutę pateikiama „null“ nuorodos klaida dėl **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span><span class="sxs-lookup"><span data-stu-id="a29d1-139">Deleting an invoice line causes null reference failure on **MarkReadyToInvoiceForProductContractLineAfterDeletingInvoice**.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]