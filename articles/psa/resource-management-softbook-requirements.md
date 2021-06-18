---
title: Preliminaraus rezervavimo reikalavimai
description: Šioje temoje pateikiama informacija apie preliminaraus rezervavimo reikalavimus.
author: ruhercul
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
ms.openlocfilehash: bc58c805bfe1a3087600b8d4a6be2d1bcdd18188
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997926"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="a473b-103">Preliminaraus rezervavimo reikalavimai</span><span class="sxs-lookup"><span data-stu-id="a473b-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="a473b-104">Išteklių reikalavimas gali būti galutinė rezervacija.</span><span class="sxs-lookup"><span data-stu-id="a473b-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="a473b-105">Galutinė rezervacija sukuria pasiūlymą, kuris naudoja išteklių pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="a473b-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="a473b-106">Tada pasiūlymas siunčiamas prašytojo patvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="a473b-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="a473b-107">Preliminari rezervacija preliminariai įtraukia išteklius į projekto komandą ir turi skirtingas būsenas grafiko lentoje, tačiau nenaudoja išteklių pajėgumo.</span><span class="sxs-lookup"><span data-stu-id="a473b-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="a473b-108">Norėdami atlikti preliminarią rezervaciją iš grafiko lentos, nustatykite lauką **Rezervacijos būsena** į **Preliminari**.</span><span class="sxs-lookup"><span data-stu-id="a473b-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![Rezervacijos būsena nustatyta į „Preliminari“](media/Resource-Management-image77.png)

<span data-ttu-id="a473b-110">Kai skirtukas **Komanda** yra rodinyje **Įvardinti komandos nariai**, ten pradedami rodyti ištekliai.</span><span class="sxs-lookup"><span data-stu-id="a473b-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="a473b-111">Preliminariai rezervuotos valandos rodomos stulpelyje **Preliminariai rezervuotos valandos**.</span><span class="sxs-lookup"><span data-stu-id="a473b-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![Preliminariai rezervuotos valandos rodinyje „Įvardinti komandos nariai“](media/Resource-Management-image78.png)

<span data-ttu-id="a473b-113">Preliminariai rezervuotiems komandos nariams gali būti priskiriamos užduotys.</span><span class="sxs-lookup"><span data-stu-id="a473b-113">Soft-booked team members can be assigned to tasks.</span></span>

![Preliminariai rezervuotam komandos nariui priskirta užduotis](media/Resource-Management-image79.png)

<span data-ttu-id="a473b-115">Skirtuke **Derinimas** nerodomos preliminariai rezervuotų išteklių rezervacijos, nes skirtuke **Derinimas** rodomos tik galutinės rezervacijos.</span><span class="sxs-lookup"><span data-stu-id="a473b-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![Preliminariai rezervuoti ištekliai be rezervacijos skirtuke „Derinimas“](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="a473b-117">Negalite preliminariai rezervuoti išteklių iš reikalavimo, kuris buvo sugeneruotas iš bendrosios komandos nario.</span><span class="sxs-lookup"><span data-stu-id="a473b-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="a473b-118">Grafiko lentoje preliminarioms išteklių rezervacijoms naudojamos skirtingos spalvos.</span><span class="sxs-lookup"><span data-stu-id="a473b-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![Preliminarios rezervacijos grafiko lentoje](media/Resource-Management-image81.png)

<span data-ttu-id="a473b-120">Jei norite konvertuoti preliminarų rezervavimą į galutinį užsakymą, grafiko lentoje dešiniuoju pelės mygtuku spustelėkite **Keisti būseną** \> **Galutiniai užsakymai** \> **Galutiniai**.</span><span class="sxs-lookup"><span data-stu-id="a473b-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![Rezervavimo būsena pakeista į „Galutinė“](media/Resource-Management-image82.png)

<span data-ttu-id="a473b-122">Rezervacija pakeista, būsena taip pat pakeista grafiko lentoje.</span><span class="sxs-lookup"><span data-stu-id="a473b-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="a473b-123">Kadangi rezervacijos būsena dabar yra **Galutinė**, ištekliai rodomi kaip rezervuoti, o jų pajėgumas ir pasiekiamumas pakeisti.</span><span class="sxs-lookup"><span data-stu-id="a473b-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="a473b-124">Tą patį metodą galite naudoti, kad atšauktumėte galutinę rezervaciją arba preliminarią rezervaciją grafiko lentoje.</span><span class="sxs-lookup"><span data-stu-id="a473b-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="a473b-125">Norėdami preliminariai rezervuotus išteklius pakeisti į galutinai rezervuotus projekto skirtuke **Komanda**, pažymėkite išteklius, tada pažymėkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="a473b-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![Komanda „Patvirtinti“](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]