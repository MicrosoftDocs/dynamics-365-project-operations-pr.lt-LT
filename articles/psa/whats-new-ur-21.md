---
title: Kas nauja arba pakeista „Project Service Automation“ V3 21 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 21 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 799be481c365e82e8ffb59ba242e30378644008b
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4126718"
---
# <a name="project-service-automation-update-release-21-v3"></a><span data-ttu-id="e7b15-103">„Project Service Automation“ V3 21 naujinimo leidimas</span><span class="sxs-lookup"><span data-stu-id="e7b15-103">Project Service Automation Update Release 21, V3</span></span>

<span data-ttu-id="e7b15-104">Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą.</span><span class="sxs-lookup"><span data-stu-id="e7b15-104">We’re pleased to announce the latest update for the Project Service Automation application for Dynamics 365.</span></span> <span data-ttu-id="e7b15-105">Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.</span><span class="sxs-lookup"><span data-stu-id="e7b15-105">This release includes some important improvements to quality, performance, and usability.</span></span> <span data-ttu-id="e7b15-106">Šis leidimas suderinamas su „Dynamics 365“ 9.x versija.</span><span class="sxs-lookup"><span data-stu-id="e7b15-106">This release is compatible with Dynamics 365 9.x.</span></span> <span data-ttu-id="e7b15-107">Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą.</span><span class="sxs-lookup"><span data-stu-id="e7b15-107">To update to this release, visit the Admin Center for Dynamics 365 online solutions page to install the update.</span></span> <span data-ttu-id="e7b15-108">Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span><span class="sxs-lookup"><span data-stu-id="e7b15-108">For more information, see [Install, update, or remove a preferred solution](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).</span></span>

<span data-ttu-id="e7b15-109">Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 21 atnaujintame leidime.</span><span class="sxs-lookup"><span data-stu-id="e7b15-109">This topic lists the features and fixes that are new or changed for Project Service Automation V3, Update Release 21.</span></span> <span data-ttu-id="e7b15-110">Šios versijos komponavimo versijos numeris yra V 3.10.32.50 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. birželio mėn.</span><span class="sxs-lookup"><span data-stu-id="e7b15-110">This version has a build number of V 3.10.32.50 and is generally available through a self-update in June 2020.</span></span>

## <a name="update-release-21"></a><span data-ttu-id="e7b15-111">21 atnaujintas leidimas</span><span class="sxs-lookup"><span data-stu-id="e7b15-111">Update Release 21</span></span>

### <a name="bug-fixes"></a><span data-ttu-id="e7b15-112">Ištaisytos klaidos</span><span class="sxs-lookup"><span data-stu-id="e7b15-112">Bug fixes</span></span>

<span data-ttu-id="e7b15-113">**Laikas ir išlaidos**</span><span class="sxs-lookup"><span data-stu-id="e7b15-113">**Time and Expense**</span></span>

<span data-ttu-id="e7b15-114">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="e7b15-114">The following issues have been fixed:</span></span>

- <span data-ttu-id="e7b15-115">Kai ataskaitų srityje veikia **Laiko įrašo tinklelio valdymas**, tinklelis nenaudoja viso ataskaitų srities tinklelio talpyklės pločio.</span><span class="sxs-lookup"><span data-stu-id="e7b15-115">When hosting the **Time Entry Grid Control** in Dashboards, the grid does not utilize the full width of the dashboard grid container.</span></span>
- <span data-ttu-id="e7b15-116">Tam tikroms laiko juostoms **Laiko įrašo** tinklelio valdiklis nerodo įrašų.</span><span class="sxs-lookup"><span data-stu-id="e7b15-116">For specific time zones, the **Time Entry** grid control does not display records.</span></span>
- <span data-ttu-id="e7b15-117">Laiko įrašai, vėlesni nei 21:00, rodomi netinkamą parą.</span><span class="sxs-lookup"><span data-stu-id="e7b15-117">Time entries that are after 9:00 PM appear on the wrong day.</span></span>
- <span data-ttu-id="e7b15-118">Vartotojai negali pateikti išlaidų, jei išlaidų kategorijai **Būtinas išlaidų kvitas** nėra nustatytos reikšmės.</span><span class="sxs-lookup"><span data-stu-id="e7b15-118">Users are unable to submit expenses if the expense category, **Expense receipt required** has no value.</span></span>

<span data-ttu-id="e7b15-119">**Išteklių valdymas**</span><span class="sxs-lookup"><span data-stu-id="e7b15-119">**Resource Management**</span></span>

<span data-ttu-id="e7b15-120">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="e7b15-120">The following issues have been fixed:</span></span>

- <span data-ttu-id="e7b15-121">Nesuaktyvinti užsakymai rodomi rodinyje **Suderinimas**.</span><span class="sxs-lookup"><span data-stu-id="e7b15-121">Inactive bookings are displayed in the **Reconciliation** view.</span></span>
- <span data-ttu-id="e7b15-122">Bendrojo ištekliaus užpildymas nebuvo patikrintas siekiant užtikrinti, kad egzistuotų tinkama rezervavimo būsena.</span><span class="sxs-lookup"><span data-stu-id="e7b15-122">Generic resource fulfillment was missing validation to ensure that a valid booking status exists.</span></span>

<span data-ttu-id="e7b15-123">**Projektų valdymas**</span><span class="sxs-lookup"><span data-stu-id="e7b15-123">**Project Management**</span></span>

<span data-ttu-id="e7b15-124">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="e7b15-124">The following issues have been fixed:</span></span>

- <span data-ttu-id="e7b15-125">**Projekto** formos tinklelius (rodiniai **Išteklių priskyrimas**, **Užduotis**, **Suderinimas**, **Išlaidų sąmatos**) galima redaguoti net tada, kai projektas nėra aktyvus.</span><span class="sxs-lookup"><span data-stu-id="e7b15-125">The **Project** form grids (**Resource Assignment**, **Task**, **Reconciliation** view, **Expense Estimates**) remain editable even when a project is not active.</span></span>
- <span data-ttu-id="e7b15-126">Dubliuotų klientų negalima sulieti su klientais, susijusiais su patvirtintomis projekto sutartimis.</span><span class="sxs-lookup"><span data-stu-id="e7b15-126">Duplicate customers can't be merged with customers that are linked to confirmed project contracts.</span></span>
- <span data-ttu-id="e7b15-127">Kai pridedamas išteklius, neturintis galiojančio kalendoriaus, sistema neparodo vartotojui patogaus klaidos pranešimo.</span><span class="sxs-lookup"><span data-stu-id="e7b15-127">When a resource who does not have a valid calendar is added, the system does not return a user friendly-error message.</span></span>
- <span data-ttu-id="e7b15-128">Mygtukas **Pridėti užduotį** įjungiamas užduočių tinklelyje tada, kai projektas susiejamas su **„Microsoft Project“ papildiniu**.</span><span class="sxs-lookup"><span data-stu-id="e7b15-128">The **Add Task** button on the task grid is enabled when the project is linked to **Microsoft Project add-in**.</span></span>
- <span data-ttu-id="e7b15-129">Pastangos didėja nevaldomai, kai užduotis su kategorija yra priskiriama ištekliui su vaidmeniu, kuriam yra nustatyta savikaina.</span><span class="sxs-lookup"><span data-stu-id="e7b15-129">Effort grows uncontrollably when a task with a category is assigned to a resource with a role for which there is a cost price defined.</span></span>

<span data-ttu-id="e7b15-130">**„Sales“**</span><span class="sxs-lookup"><span data-stu-id="e7b15-130">**Sales**</span></span>

<span data-ttu-id="e7b15-131">Buvo atlikti šie patobulinimai:</span><span class="sxs-lookup"><span data-stu-id="e7b15-131">The following enhancements have been made:</span></span>

- <span data-ttu-id="e7b15-132">**Sąskaitos faktūros dažnumas** ir **Atsiskaitymo pradžia** perkelti į skirtuką **Sąskaitų faktūrų grafikas**.</span><span class="sxs-lookup"><span data-stu-id="e7b15-132">**Invoice Frequency** and **Billing Start** have been moved to the **Invoice Schedule** tab.</span></span>

<span data-ttu-id="e7b15-133">Buvo pataisytos šios problemos:</span><span class="sxs-lookup"><span data-stu-id="e7b15-133">The following issues have been fixed:</span></span>

- <span data-ttu-id="e7b15-134">**Kategorijoje** **Bendroji pardavimo kaina** yra nulis (0) , nors vertė **Vaidmuo** turi bendrą pardavimo kainą, nelygią nuliui.</span><span class="sxs-lookup"><span data-stu-id="e7b15-134">**Total Sales Price** is zero (0) for **Category** even though **Role** has a total sales price that is not zero.</span></span>
- <span data-ttu-id="e7b15-135">Klientai negali pakeisti lauko **Sąskaitos faktūros būsenos** reikšmės į **Parengta išrašyti sąskaitą faktūrą**, kai kitas tinkinamas procesas naujina papildomą lauką.</span><span class="sxs-lookup"><span data-stu-id="e7b15-135">Customers can't change the value of the **Invoice Status** field to **Ready for invoicing** when another customized process is updating an additional field.</span></span>
- <span data-ttu-id="e7b15-136">Mygtuku **Atnaujinti sąskaitų faktūrų eilutes** galima sukurti kelias dubliuotas eilutes, jei jis yra pakartotinai paspaudžiamas.</span><span class="sxs-lookup"><span data-stu-id="e7b15-136">The **Refresh Invoice Lines** button can create multiple duplicated lines if it is repeatedly selected.</span></span>
- <span data-ttu-id="e7b15-137">Mygtukas **Naujinti kainas** neveikia papildomame tinklelyje **Vaidmens kainos** formoje **Sparčioji peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="e7b15-137">The **Update Prices** button doesn't work on the **Role Prices** subgrid in the **Quick View** form.</span></span>
- <span data-ttu-id="e7b15-138">**Pardavimo kainoraščio aprašo** algoritmas netinkamai apdoroja laiko juostas, todėl gaunamas netinkamas kainoraščių pasirinkimas.</span><span class="sxs-lookup"><span data-stu-id="e7b15-138">The **Sales Price List Resolution** logic improperly handles time zones, resulting in the incorrect selection of price lists.</span></span>
- <span data-ttu-id="e7b15-139">Patvirtinus vieno laiko įrašą, projekto **Faktinių išlaidų suma** gali turėti nežymią paklaidą.</span><span class="sxs-lookup"><span data-stu-id="e7b15-139">A project’s **Total Actual Cost** can be off by a fractional amount after a single time entry is approved.</span></span>
- <span data-ttu-id="e7b15-140">**Kainų aprašo** algoritmas nepateikia vartotojui patogaus pranešimo, jei **Gauta vaidmenų kaina** neturi reikšmių laukuose **Pagrindinis vienetas** ir **Kaina pagrindiniu vienetu**.</span><span class="sxs-lookup"><span data-stu-id="e7b15-140">The **Price Resolution** logic does not provide a user-friendly error message if **Retrieved RolePrice** doesn't have values in **'Primary Unit'** and **'Price In Primary Unit'** fields.</span></span>
