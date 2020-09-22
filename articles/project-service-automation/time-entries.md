---
title: Laiko įrašų kūrimas
description: Šioje temoje pateikiama informacija apie tai, kaip kurti laiko įrašus.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 90f6450b-e0c4-4d86-b8f5-ffb1a2b1e38a
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: ae3af7d62d93884c7fa9881394b7129daeb8bf7e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753738"
---
# <a name="create-time-entries"></a><span data-ttu-id="5daaf-103">Laiko įrašų kūrimas</span><span class="sxs-lookup"><span data-stu-id="5daaf-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="5daaf-104">Ankstesnėse Dynamics 365 Project Service Automation versijose laiko įrašai buvo įvedami kas savaitę.</span><span class="sxs-lookup"><span data-stu-id="5daaf-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="5daaf-105">„Project Service Automation“ 3 versijoje laiko įrašai įvedami kasdien.</span><span class="sxs-lookup"><span data-stu-id="5daaf-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="5daaf-106">Tačiau sukūrus kelis laiko įrašus, galite atlikti masinį kūrimą arba juos kopijuoti.</span><span class="sxs-lookup"><span data-stu-id="5daaf-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="5daaf-107">Laiko įrašo kūrimas</span><span class="sxs-lookup"><span data-stu-id="5daaf-107">Create a time entry</span></span>

<span data-ttu-id="5daaf-108">Norėdami sukurti laiko įrašą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="5daaf-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="5daaf-109">Puslapyje **Laiko įrašai** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="5daaf-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="5daaf-110">Dialogo lange **Spartusis kūrimas: laiko įrašas** įveskite laiko įrašo trukmę minutėmis, valandomis arba dienomis.</span><span class="sxs-lookup"><span data-stu-id="5daaf-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="5daaf-111">Trukmę įveskite šiuo formatu: *x* minutės, *x* valandos arba *x* dienos.</span><span class="sxs-lookup"><span data-stu-id="5daaf-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="5daaf-112">Valandas ir dienas taip pat galite įvesti naudodami dešimtaines reikšmes, pavyzdžiui, *x.x* valandos arba *x.x* dienos.</span><span class="sxs-lookup"><span data-stu-id="5daaf-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="5daaf-113">Pažymėkite laiko įrašo tipą ir projektą, kuriam įvedate laiko įrašą.</span><span class="sxs-lookup"><span data-stu-id="5daaf-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="5daaf-114">Lauke **Projekto užduotis** raskite šio laiko įrašo užduotį.</span><span class="sxs-lookup"><span data-stu-id="5daaf-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="5daaf-115">Jei kuriate laiko įrašą užduočiai, kuri nėra priskirta naudotojui, lauke **Projekto užduotis** pažymėkite mygtuką **Ieškoti**, pažymėkite **Keisti rodinį**, tada pažymėkite**Visos aktyvios projekto užduotus**, kad sudarytumėte visų užduočių sąrašą.</span><span class="sxs-lookup"><span data-stu-id="5daaf-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View**, and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="5daaf-116">Įveskite parašymą, jei jo reikia, tada pasirinkite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="5daaf-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="5daaf-117">Sukūrę ir įrašę laiko įrašą, galite redaguoti jį laiko įrašų tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="5daaf-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="5daaf-118">Laiko įrašų tinklelis palaiko du formatus:</span><span class="sxs-lookup"><span data-stu-id="5daaf-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="5daaf-119">Galite įvesti laiko įrašus formatu **hh: mm**.</span><span class="sxs-lookup"><span data-stu-id="5daaf-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="5daaf-120">Tada šis formatas konvertuojamas į valandas ir trupmenas.</span><span class="sxs-lookup"><span data-stu-id="5daaf-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="5daaf-121">Galite tiesiogiai įvesti valandas ir trupmenas.</span><span class="sxs-lookup"><span data-stu-id="5daaf-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="5daaf-122">Atkreipkite dėmesį, kad valandos trupmena nėra minutės.</span><span class="sxs-lookup"><span data-stu-id="5daaf-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="5daaf-123">Todėl 1,5 valandos atitinka 1 valandą ir 30 minučių.</span><span class="sxs-lookup"><span data-stu-id="5daaf-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="5daaf-124">Ta pati taisyklė taikoma dienos trupmenoms.</span><span class="sxs-lookup"><span data-stu-id="5daaf-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="5daaf-125">Viena diena yra 24 valandos, o 0,5 dienos yra 12 valandų.</span><span class="sxs-lookup"><span data-stu-id="5daaf-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="5daaf-126">Masinis laiko įrašų kūrimas</span><span class="sxs-lookup"><span data-stu-id="5daaf-126">Bulk create time entries</span></span>

<span data-ttu-id="5daaf-127">Sukūrus kelis laiko įrašus, galite juos nukopijuoti, kad sukurtumėte didelį kiekį papildomų laiko įrašų.</span><span class="sxs-lookup"><span data-stu-id="5daaf-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="5daaf-128">Puslapyje **Laiko įrašai** pasirinkite **Kopijuoti savaitę**.</span><span class="sxs-lookup"><span data-stu-id="5daaf-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="5daaf-129">Laukų grupėje **Nuo laikotarpio** laukuose **Pradžios data** ir **Pabaigos data** apibrėžkite datų intervalą, iš kurio kopijuosite laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="5daaf-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="5daaf-130">Laukų grupėje **Iki laikotarpio** lauke **Pradžios data** nurodykite datą, kuriai kurti laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="5daaf-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="5daaf-131">Pažymėkite **Kopijuoti**, kad sukurtumėte laiko įrašų, kurie atitinka savaitės dieną, kuri nurodyta laukų grupėje **Iki laikotarpio**, kopiją.</span><span class="sxs-lookup"><span data-stu-id="5daaf-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="5daaf-132">Pavyzdžiui, praeitos savaitės pirmadienio laiko įrašas yra nukopijuojamas į savaitės, kuri nurodytą laukų grupėje **Iki periodo**, pirmadienį.</span><span class="sxs-lookup"><span data-stu-id="5daaf-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="5daaf-133">Duomenų importavimas laiko įrašams</span><span class="sxs-lookup"><span data-stu-id="5daaf-133">Import data for time entries</span></span>

<span data-ttu-id="5daaf-134">Galite importuoti duomenis iš projekto rezervacijų ir priskyrimų.</span><span class="sxs-lookup"><span data-stu-id="5daaf-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="5daaf-135">Importuodami duomenis galite nurodyti importuotinų rezervacijų datų intervalą, tada konkrečiai pasirinkti rezervacijas, kurios turėtų būti sukurtos kaip laiko įrašų **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="5daaf-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="5daaf-136">Grupavimo pagal, rūšiavimo, ieškos ir filtravimo galimybės</span><span class="sxs-lookup"><span data-stu-id="5daaf-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="5daaf-137">Galite grupuoti ir filtruoti laiko įrašus pagal dimensijas, nurodytas stulpeliuose.</span><span class="sxs-lookup"><span data-stu-id="5daaf-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="5daaf-138">Lauke **Grupuoti pagal** pažymėkite dimensiją, kurią norite naudoti laiko įrašams filtruoti.</span><span class="sxs-lookup"><span data-stu-id="5daaf-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="5daaf-139">Taip pat galite rikiuoti laiko įrašus didėjimo arba mažėjimo tvarka naudodami stulpelių antraščių rūšiavimo rodyklę.</span><span class="sxs-lookup"><span data-stu-id="5daaf-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="5daaf-140">Be to, galite rodyti arba slėpti įrašus pažymėdami mygtuką **Filtras** stulpelių antraštėse, tada dialogo lange **Ieška** įvesdami tekstą, kuris turi būti naudojamas laiko įrašų ieškai pagal projekto pavadinimą, projekto užduotį, laiko įrašą arba išteklius.</span><span class="sxs-lookup"><span data-stu-id="5daaf-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
