---
title: Rezervacija į projektą
description: Šioje temoje pateikiama informacija apie projekto išteklių rezervavimą.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 19128264ed3db7efeeba948155f0ddbdc806c2a0
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080688"
---
# <a name="book-to-a-project"></a><span data-ttu-id="80686-103">Rezervacija į projektą</span><span class="sxs-lookup"><span data-stu-id="80686-103">Book to a project</span></span>

<span data-ttu-id="80686-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="80686-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="80686-105">Yra atvejų, kai projekto vadovas arba išteklių vadovas turės priskirti išteklių projektui be konkretaus reikalavimo, apibrėžto bendrosios komandos nario.</span><span class="sxs-lookup"><span data-stu-id="80686-105">There are times where a Project manager or Resource manager will need to allocate a resource to project without a specific requirement being defined from a generic team member.</span></span> <span data-ttu-id="80686-106">Tai galima pasiekti vienu iš trijų būdu.</span><span class="sxs-lookup"><span data-stu-id="80686-106">This can be achieved in one of three ways.</span></span>

- <span data-ttu-id="80686-107">Rezervavimas iš komados nario tinklelio</span><span class="sxs-lookup"><span data-stu-id="80686-107">Book from the team member grid</span></span>
- <span data-ttu-id="80686-108">Rezervavimas iš grafiko lentos</span><span class="sxs-lookup"><span data-stu-id="80686-108">Book from the schedule board</span></span>
- <span data-ttu-id="80686-109">Rezervavimas iš formos **Projektas**</span><span class="sxs-lookup"><span data-stu-id="80686-109">Book from the **Project** form</span></span>

## <a name="book-from-the-team-member-grid"></a><span data-ttu-id="80686-110">Rezervavimas iš komados nario tinklelio</span><span class="sxs-lookup"><span data-stu-id="80686-110">Book from the team member grid</span></span>

<span data-ttu-id="80686-111">Jei jūsų organizacija veikia hibridiniame išteklių paskirstymo režime, projektų vadovas gali užsakyti išteklių tiesiogiai projektui atlikdamas toliau nurodytus žingsnius.</span><span class="sxs-lookup"><span data-stu-id="80686-111">If your organization is operating in hybrid Resource allocation mode, the Project manager can book a resource directly to the project by completing the following steps.</span></span>

1. <span data-ttu-id="80686-112">Iš projekto eikite į komandos narių tinklelį ir pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="80686-112">From the project, go to the team member grid and select **New**.</span></span>
2. <span data-ttu-id="80686-113">Apibrėžkite ištekliaus pozicijos pavadinimą ir vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="80686-113">Define the position name and the role of the resource.</span></span>
3. <span data-ttu-id="80686-114">Pažymėkite rezervuojamą išteklių iš galimos peržvalgos.</span><span class="sxs-lookup"><span data-stu-id="80686-114">Select the bookable resource from the available lookup.</span></span>
4. <span data-ttu-id="80686-115">Pasirinkę išteklių apibrėžkite šią lauko informaciją, kad užrezervuotumėte išteklių:</span><span class="sxs-lookup"><span data-stu-id="80686-115">After you select the resource, define the following field information to book the resource:</span></span>

    - <span data-ttu-id="80686-116">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="80686-116">Start date</span></span>
    - <span data-ttu-id="80686-117">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="80686-117">Finish date</span></span>
    - <span data-ttu-id="80686-118">Paskirstymo metodas</span><span class="sxs-lookup"><span data-stu-id="80686-118">Allocation method</span></span>
    - <span data-ttu-id="80686-119">Valandos, jei taikoma</span><span class="sxs-lookup"><span data-stu-id="80686-119">Hours, if applicable</span></span>
    - <span data-ttu-id="80686-120">Projekto tvirtintojas</span><span class="sxs-lookup"><span data-stu-id="80686-120">Project approver</span></span>

6. <span data-ttu-id="80686-121">Pasirinkite **Įrašyti ir uždaryti**</span><span class="sxs-lookup"><span data-stu-id="80686-121">Select **Save and Close**</span></span>

## <a name="book-from-the-schedule-board"></a><span data-ttu-id="80686-122">Rezervavimas iš grafiko lentos</span><span class="sxs-lookup"><span data-stu-id="80686-122">Book from the schedule board</span></span>

<span data-ttu-id="80686-123">Kai išteklių vadovas turi užsakyti išteklių tiesiogiai projektui, jis gali naudoti grafiko lentą ir projekto reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="80686-123">When a Resource manager needs to book a resource directly to a project, they can use the schedule board and the project requirement.</span></span> <span data-ttu-id="80686-124">Projekto reikalavimas – tai išteklių reikalavimas, kurį visada galima rezervuoti.</span><span class="sxs-lookup"><span data-stu-id="80686-124">The project requirement is a resource requirement that is always available to be booked against.</span></span> <span data-ttu-id="80686-125">Norėdami užsakyti tiesiogiai projektui iš grafiko lentos, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="80686-125">To book directly to a project form the schedule board, complete the following steps.</span></span>

1. <span data-ttu-id="80686-126">Nueikite į grafiko lentą ir kairiajame puslapyje filtruokite išteklius, kuriuos svarstote reikalavimui.</span><span class="sxs-lookup"><span data-stu-id="80686-126">Navigate to the schedule board and on the left page, filter for the resources you are considering for the requirement.</span></span>
2. <span data-ttu-id="80686-127">Apatinėje srityje pasirinkite skirtuką **Projektas** ir peržiūrėkite projekto reikalavimų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="80686-127">In the bottom pane, select the **Project** tab to view a list of project requirements.</span></span>
3. <span data-ttu-id="80686-128">Vilkite reikalavimą į išteklių ir apibrėžkite šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="80686-128">Drag the requirement onto a resource and define the following information:</span></span>

    - <span data-ttu-id="80686-129">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="80686-129">Start date</span></span>
    - <span data-ttu-id="80686-130">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="80686-130">Finish date</span></span>
    - <span data-ttu-id="80686-131">Rezervavimo būsena</span><span class="sxs-lookup"><span data-stu-id="80686-131">Booking status</span></span>
    - <span data-ttu-id="80686-132">Rezervavimo metodas</span><span class="sxs-lookup"><span data-stu-id="80686-132">Booking method</span></span>
    - <span data-ttu-id="80686-133">Trukmė</span><span class="sxs-lookup"><span data-stu-id="80686-133">Duration</span></span>

## <a name="book-from-the-project-form"></a><span data-ttu-id="80686-134">Rezervavimas iš Projekto formos</span><span class="sxs-lookup"><span data-stu-id="80686-134">Book from the Project form</span></span>

<span data-ttu-id="80686-135">Kaip projektų vadovui, jums gali tekti rezervuoti išteklių projektui, tačiau tik žinant kriterijus, o ne ištekliaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="80686-135">As a Project manager, you might need to book a resource to a project, but only know the criteria rather than the name of the resource.</span></span> <span data-ttu-id="80686-136">Atlikite šiuos veiksmus, kad naudodami pagalbinę planavimo priemonę rastumėte išteklių, pagrįstą bet kuriais galimais ištekliaus atributais.</span><span class="sxs-lookup"><span data-stu-id="80686-136">Complete the following steps to use the schedule assistant to find a resource based on any available attributes of the resource.</span></span> 

1. <span data-ttu-id="80686-137">Pereikite prie projekto ir pasirinkite **Rezervuoti** , kad atidarytumėte planavimo pagalbinę priemonę.</span><span class="sxs-lookup"><span data-stu-id="80686-137">Navigate to the project and select **Book** to open the Schedule Assistant.</span></span>
2. <span data-ttu-id="80686-138">Naudodami filtrus, esančius kairėje planavimo pagalbinės priemonės pusėje, susiaurinkite kriterijus ir pažymėkite **Ieškoti.**</span><span class="sxs-lookup"><span data-stu-id="80686-138">Using the filters on the left side of the Schedule Assistant, narrow the criteria and select **Search.**</span></span>
3. <span data-ttu-id="80686-139">Pagal rezultatuose grąžintus išteklius galite užsakyti išteklių.</span><span class="sxs-lookup"><span data-stu-id="80686-139">Based on resources returned in the results, you can book a resource.</span></span>

> [!NOTE]
> <span data-ttu-id="80686-140">Šis metodas nesukuria jokių išteklių rezervavimų.</span><span class="sxs-lookup"><span data-stu-id="80686-140">This method doesn't create any bookings for the resource.</span></span> <span data-ttu-id="80686-141">Šis metodas įtraukia išteklių į komandą.</span><span class="sxs-lookup"><span data-stu-id="80686-141">Instead, it adds the resource to the team.</span></span> <span data-ttu-id="80686-142">Įtraukę komandos narį į projektą, projektų vadovas gali naudoti išlaikytus rezervavimus arba išplėstus rezervavimus, kad įtrauktų reikiamus rezervavimus į išteklius.</span><span class="sxs-lookup"><span data-stu-id="80686-142">After the team member has been added to the project, the project manager can use maintain bookings or extend bookings to add the required bookings to the resource.</span></span>
