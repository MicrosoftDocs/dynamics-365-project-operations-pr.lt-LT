---
title: Išteklių valdymas DUK
description: Šioje temoje pateikiami atsakymai į dažniausiai užduodamus klausimus apie išteklių valdymą.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 395aa57d73e5d4a0c9c827c79bf4e7ef229c3981
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081047"
---
# <a name="resource-management-faq"></a><span data-ttu-id="3130e-103">Išteklių valdymas DUK</span><span class="sxs-lookup"><span data-stu-id="3130e-103">Resource management FAQ</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="3130e-104">Koks skirtumas tarp komandos nario ir ištekliaus reikalavimo?</span><span class="sxs-lookup"><span data-stu-id="3130e-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="3130e-105">Projekto komandos narys gali būti priskirtas užduotims, rezervuotas arba rezervuotas daugiau kartų ir nustatytas kaip tvirtintojas.</span><span class="sxs-lookup"><span data-stu-id="3130e-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="3130e-106">Ištekliaus reikalavimas gali egzistuoti be projekto komandos nario, kaip poreikio juodraščio pastaba.</span><span class="sxs-lookup"><span data-stu-id="3130e-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="3130e-107">Kuo skiriasi pasiūlytos ir preliminariai rezervuotos valandos?</span><span class="sxs-lookup"><span data-stu-id="3130e-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="3130e-108">Skiriasi pasiūlytų valandų ir preliminariai rezervuotų valandų matomumas.</span><span class="sxs-lookup"><span data-stu-id="3130e-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="3130e-109">Pasiūlytos valandos matomos tik išteklių valdytojui ir projektų vadovui, kuris inicijavo poreikį naudodamas išteklių užklausą.</span><span class="sxs-lookup"><span data-stu-id="3130e-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="3130e-110">Preliminariai rezervuotos valandos matomos visiems, kurie turi prieigą prie grafiko lentos.</span><span class="sxs-lookup"><span data-stu-id="3130e-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="3130e-111">Kaip galiu matyti išteklių komandai preliminariai rezervuotas valandas?</span><span class="sxs-lookup"><span data-stu-id="3130e-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="3130e-112">Preliminarios rezervacijos gali būti atliekamos, kai rezervuojate išteklių reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="3130e-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="3130e-113">Ištekliai, kurie projekto komandai rezervuojami preliminariai, rodomi kaip komandos nariai, kuriems rezervuotos preliminarios valandos.</span><span class="sxs-lookup"><span data-stu-id="3130e-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="3130e-114">Ši informacija taip pat rodoma grafiko lentoje.</span><span class="sxs-lookup"><span data-stu-id="3130e-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="3130e-115">Kaip pakeisti išteklių (bendrųjų arba turinčių pavadinimą), kuriuos rezervavau, būtinas valandas?</span><span class="sxs-lookup"><span data-stu-id="3130e-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="3130e-116">Rezervavę išteklius, pasirinkite **Tvarkyti rezervacijas** , kad atliktumėte visus reikiamus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="3130e-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="3130e-117">Kokius išteklių tipus palaiko „Project Service Automation“?</span><span class="sxs-lookup"><span data-stu-id="3130e-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="3130e-118">**Naudotojas** ir **Kontaktas** yra vieninteliai išteklių tipai, palaikomi Dynamics 365 Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="3130e-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="3130e-119">Nors galite kurti kitų tipų išteklius (pavyzdžiui, **Įranga** ir **Grupė** ), jų galutinis naudojimas nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="3130e-119">Although you can create other types of resources (for example, **Equipment** and **Group** ), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="3130e-120">Koks skirtumas tarp priskyrimo ir rezervacijos?</span><span class="sxs-lookup"><span data-stu-id="3130e-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="3130e-121">Priskyrimai yra išteklių projekto užduotims priskyrimas projekto grafike.</span><span class="sxs-lookup"><span data-stu-id="3130e-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="3130e-122">Ištekliai gali būti faktiniai arba bendrieji.</span><span class="sxs-lookup"><span data-stu-id="3130e-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="3130e-123">Rezervacijos yra galutinis arba preliminarus išteklių paskirstymas projektui.</span><span class="sxs-lookup"><span data-stu-id="3130e-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="3130e-124">Galutinės rezervacijos naudoja išteklių pajėgumus.</span><span class="sxs-lookup"><span data-stu-id="3130e-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="3130e-125">Idealiu atveju faktinių išteklių rezervacijos ir priskyrimai turėtų sutapti, nes jie nesiskiria.</span><span class="sxs-lookup"><span data-stu-id="3130e-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="3130e-126">Tačiau PSA neįgyvendina šio sutapimo.</span><span class="sxs-lookup"><span data-stu-id="3130e-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="3130e-127">Derinimo rodinyje rodomos projektų vadovo vietos, kuriose išteklių rezervacijos ir priskyrimai nesutampa.</span><span class="sxs-lookup"><span data-stu-id="3130e-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
