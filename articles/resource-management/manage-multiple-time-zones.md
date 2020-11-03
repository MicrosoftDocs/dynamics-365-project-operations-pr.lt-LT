---
title: Laiko juostų valdymas
description: Sukūrus projektą, jo laiko juosta yra pagrįsta laiko juosta, nurodyta taikomame darbo valandų šablone.
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080774"
---
# <a name="manage-time-zones"></a><span data-ttu-id="0f0f0-103">Laiko juostų valdymas</span><span class="sxs-lookup"><span data-stu-id="0f0f0-103">Manage time zones</span></span>

<span data-ttu-id="0f0f0-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="0f0f0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


## <a name="projects"></a><span data-ttu-id="0f0f0-105">Projektai</span><span class="sxs-lookup"><span data-stu-id="0f0f0-105">Projects</span></span>

<span data-ttu-id="0f0f0-106">Sukūrus projektą, laiko juosta yra pagrįsta laiko juosta, nurodyta taikomame darbo valandų šablone.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-106">When a project is created, the time zone is based on the time zone defined in the applied work hour template.</span></span> <span data-ttu-id="0f0f0-107">**Projektuose** datos visada yra santykinai susijusios su vartotojo, prisijungusio prie kiekvieno skirtuko, laiko zona, išskyrus skirtuką **Užduotis**. Kai peržiūrite darbo paskirstymo struktūrą, datos visada bus rodomos projekto laiko juostoje.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-107">On the **Project** for, the dates are always relative to the time zone of the user that is logged in on each tab, except the **Task** tab. When you view the work breakdown structure, the dates will always be displayed in the project’s time zone.</span></span>

## <a name="tasks"></a><span data-ttu-id="0f0f0-108">Užduotys</span><span class="sxs-lookup"><span data-stu-id="0f0f0-108">Tasks</span></span>

<span data-ttu-id="0f0f0-109">Sukūrus užduotį, pradžios laiką, pabaigo laiką ir valandas / dienas valdo projekto darbo valandos.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-109">When a task is created, the start time, end time, and hours/day is controlled by the working hours of the project.</span></span> <span data-ttu-id="0f0f0-110">Pavyzdžiui, jei užduotis sukuriama su projektu, kurio laiko juosta yra -8 PST ir turi tokias darbo valandas: 9:00 iki 17:00, nuo pirmadienio iki penktadienio, bet kokia užduotis, sukurta be priskyrimo, laikysis projekto kalendoriaus pradžios ir pabaigos laiko.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-110">For example, if a task is created with a project whose time zone is -8 PST and has the following working hours: 9:00 AM to 5:00 PM Monday to Friday, any task created without an assignment will respect the start time and end time of the project calendar.</span></span>

## <a name="manage-resources-with-time-zones"></a><span data-ttu-id="0f0f0-111">Išteklių valdymas naudojant laiko zonas</span><span class="sxs-lookup"><span data-stu-id="0f0f0-111">Manage resources with time zones</span></span>

<span data-ttu-id="0f0f0-112">Norint gauti tikslius ir nuspėjamus rezultatus naudojant parinktį **Išplėsti rezervavimą** , reikia atlikti dvi pagrindines būtinąsias sąlygas:</span><span class="sxs-lookup"><span data-stu-id="0f0f0-112">For accurate and predictable results when using **Extend Booking** , there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="0f0f0-113">Vartotojas turi sukonfigūruoti savo įrenginio laiko juostą, kad ji atitiktų laiko juostą, apibrėžtą sistemos **tinkinimo parametruose**.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-113">The user must configure their device's time zone to match the time zone defined in the system's **Personalization Settings**.</span></span>
 
  ![Laiko juostos parametrai „Windows 10“](media/reconcile-assignments-03.png)

  ![Laiko juostos parametrai personalizavimo parametruose](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="0f0f0-116">Rezervuojami ištekliai turi turėti bent vieną minutę darbo laiko, kuri sutampa su kontūrais, kurie naudojami pageidaujamo išplėtimo apibrėžimui.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-116">The bookable resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="0f0f0-117">Pavyzdžiui, šie ištekliai su darbo valandomis, kurie patenka nuo 9:00 iki 19:00.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-117">For example, the following resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Išteklių kontūrų palyginimas](media/reconcile-assignments-05.png)

<span data-ttu-id="0f0f0-119">Toliau esančioje lentelėje pateikiama:</span><span class="sxs-lookup"><span data-stu-id="0f0f0-119">The following table shows:</span></span>

- <span data-ttu-id="0f0f0-120">A projekto kalendoriaus šablonas</span><span class="sxs-lookup"><span data-stu-id="0f0f0-120">A project calendar template</span></span>
- <span data-ttu-id="0f0f0-121">A išteklius: šis išteklius turi tą patį kalendorių ir yra toje pačioje laiko juostoje kaip ir projektas.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-121">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="0f0f0-122">Rezervavimo pradžios laikas bus 9.00.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-122">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="0f0f0-123">Išteklius B: šis išteklius yra kitoje laiko juostoje nei projektas ir prasideda 7:00 val. jų laiko juostoje.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-123">Resource B: This resource is located in a different time zone than the project and starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="0f0f0-124">Tačiau rezervavimai prasidės 9.00, nes tai yra anksčiausias priskyrimo kontūro pradžios laikas.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-124">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="0f0f0-125">Ištekliai C ir D: ištekliai yra skirtingose laiko juostose ir skiriasi nuo projekto ir vienas kito, o jų rezervavimai prasideda ne anksčiau nei atitinkamas jų pradžios laikas.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-125">Resources C and D: The resources are located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="0f0f0-126">Objektas</span><span class="sxs-lookup"><span data-stu-id="0f0f0-126">Entity</span></span>  |<span data-ttu-id="0f0f0-127">Kalendorius</span><span class="sxs-lookup"><span data-stu-id="0f0f0-127">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="0f0f0-128">Projekto kalendoriaus šablonas</span><span class="sxs-lookup"><span data-stu-id="0f0f0-128">Project calendar template</span></span>   | ![Projekto kalendorius](media/reconcile-assignments-06.png) |
|<span data-ttu-id="0f0f0-130">A išteklius</span><span class="sxs-lookup"><span data-stu-id="0f0f0-130">Resource A</span></span>  | ![A ištekliaus kalendorius](media/reconcile-assignments-06.png) |
|<span data-ttu-id="0f0f0-132">B išteklius</span><span class="sxs-lookup"><span data-stu-id="0f0f0-132">Resource B</span></span>  |  ![B ištekliaus kalendorius](media/reconcile-assignments-07.png) |
|<span data-ttu-id="0f0f0-134">C išteklius</span><span class="sxs-lookup"><span data-stu-id="0f0f0-134">Resource C</span></span>  |  ![C ištekliaus kalendorius](media/reconcile-assignments-08.png) |
|<span data-ttu-id="0f0f0-136">D išteklius</span><span class="sxs-lookup"><span data-stu-id="0f0f0-136">Resource D</span></span>  | ![D ištekliaus kalendorius](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="0f0f0-138">Kai pereisite į rodinį **Suderinimas** , rodomi išteklių priskyrimai ir susiję rezervavimo trūkumai.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-138">When you navigate to the **Reconciliation** view, the resource assignments and the associated booking shortages are displayed.</span></span>

![Suderinimo rodinys prieš išplėtimą](media/reconcile-assignments-10.png)

<span data-ttu-id="0f0f0-140">Po to, kai kiekvienam ištekliui buvo panaudota rezervavimo išplėtimo funkcija, rezervavimai sėkmingai pratęsiami kiekvienam ištekliui, nes kiekvieno ištekliaus darbo valandos sutapo su trūkumo kontūrais.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-140">After the extend booking functionality has been used for each resource, bookings are successfully extended for each resource because each resource’s working hours overlapped with the contours of the shortage.</span></span>

![Suderinimo rodinys po rezervavimo išplėtimo](media/reconcile-assignments-11.png) 

<span data-ttu-id="0f0f0-142">Atkreipkite dėmesį, kad išsamiau pažvelgus į rezervavimo detales, skiriasi rezervavimo pradžios laikas.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-142">Notice that a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="0f0f0-143">Rezervavimai pradedami ne anksčiau, nei priskyrimo kontūro pradžios laikas, bet ne anksčiau nei galimas ištekliaus pradžios laikas.</span><span class="sxs-lookup"><span data-stu-id="0f0f0-143">The bookings start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>

![Naujos išteklių rezervacijos grafiko lentoje](media/reconcile-assignments-12.png)
