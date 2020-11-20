---
title: Peržiūrėti siūlomus išteklius
description: Šioje temoje pateikiama informacija apie tai, kaip siūlyti projekto išteklius.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401183"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="47200-103">Peržiūrėti siūlomus išteklius</span><span class="sxs-lookup"><span data-stu-id="47200-103">Review proposed resources</span></span>

<span data-ttu-id="47200-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="47200-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="47200-105">Išteklių valdytojai projektų vadovui gali pasiūlyti išteklius naudodami išteklių užklausą.</span><span class="sxs-lookup"><span data-stu-id="47200-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="47200-106">Išteklių užklausos tinklelyje pažymėkite **Rasti išteklius**.</span><span class="sxs-lookup"><span data-stu-id="47200-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="47200-107">Puslapyje **Planavimo pagalbinė priemonė** pažymėkite išteklius, tada skyde **Kurti išteklių rezervaciją** lauke **Rezervacijos būsena** pažymėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="47200-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="47200-108">Galimi šie būsenos naujinimai:</span><span class="sxs-lookup"><span data-stu-id="47200-108">The following status updates occur:</span></span>

- <span data-ttu-id="47200-109">Puslapyje **Planavimo pagalbinė priemonė** būsenos indikatoriai atnaujinami, kad rodytų, kad rezervacija yra pasiūlyta, o ne galutinai rezervuota.</span><span class="sxs-lookup"><span data-stu-id="47200-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="47200-110">Išteklių užklausoje būsena pakeičiama į **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="47200-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="47200-111">Projekto skirtuke **Komanda** bendrosios komandos nario reikšmė **Pageidauti būsenos** pakeičiama į **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="47200-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="47200-112">Projekto vadovas gali priimti arba atmesti pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="47200-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="47200-113">Kai išteklių valdytojas apdoroja išteklių užklausas, jis gali naudoti bet kurį iš toliau nurodytų metodų.</span><span class="sxs-lookup"><span data-stu-id="47200-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="47200-114">Pasiūlyti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užpildytų pageidaujamas valandas.</span><span class="sxs-lookup"><span data-stu-id="47200-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="47200-115">Tada pasiūlytos valandos padalinamos keliams ištekliams, kurie gali patenkinti pageidaujamas valandas.</span><span class="sxs-lookup"><span data-stu-id="47200-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="47200-116">Tokiu atveju valandos negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="47200-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="47200-117">Pasiūlyti mažiau išteklių, nei pageidaujama.</span><span class="sxs-lookup"><span data-stu-id="47200-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="47200-118">Tokiu atveju pasiūlytas išteklių pajėgumas yra mažesnis nei pageidaujamos valandos, kurias nurodė pageidaujantis asmuo.</span><span class="sxs-lookup"><span data-stu-id="47200-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="47200-119">Todėl, kai pageidaujantis asmuo sutinka su pasiūlytais ištekliais, sukuriamas neįvykdytas išteklių reikalavimas, kuris fiksuoja likusią poreikio dalį.</span><span class="sxs-lookup"><span data-stu-id="47200-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="47200-120">Rezervuoti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užbaigtų darbą.</span><span class="sxs-lookup"><span data-stu-id="47200-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="47200-121">Rezervuoti mažiau išteklių, nei pageidaujama.</span><span class="sxs-lookup"><span data-stu-id="47200-121">Book fewer resources than are required.</span></span> <span data-ttu-id="47200-122">Tokiu atveju rezervuotų valandų yra mažiau nei pageidautų valandų.</span><span class="sxs-lookup"><span data-stu-id="47200-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="47200-123">Sistema parodys, kaip pasiūlyti išteklius, o ne rezervacijas, kad pageidaujantis asmuo galėtų patikrinti ir stebėti likusią poreikio dalį.</span><span class="sxs-lookup"><span data-stu-id="47200-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="47200-124">Išteklių pasiekiamumą</span><span class="sxs-lookup"><span data-stu-id="47200-124">Resource availability</span></span>

<span data-ttu-id="47200-125">Labai svarbu, kad išteklių valdytojai galėtų peržiūrėti išteklių pasiekiamumą ir naujinti rezervacijas.</span><span class="sxs-lookup"><span data-stu-id="47200-125">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="47200-126">Kai kuriais atvejais nėra formalaus poreikio (išteklių užklausos), tačiau išteklių valdytojas turi reaguoti į neplanuotą poreikį, kurį gauna per tokius kanalus kaip el. paštas, telefono skambutis ar tiesioginis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="47200-126">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="47200-127">Išteklių valdytojai naudoja grafiko lentą, kad naujintų išteklius ir rezervacijas.</span><span class="sxs-lookup"><span data-stu-id="47200-127">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="47200-128">Išteklių darbo valandos naudojamos kaip išteklių pasiekiamumo skaičiavimo pagrindas.</span><span class="sxs-lookup"><span data-stu-id="47200-128">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="47200-129">Išteklių rezervacijos naudoja išteklių pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="47200-129">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="47200-130">Grafiko lentoje naudojamos spalvos ir atspalviai, kurie rodo rezervacijas, pasiekiamumą ir per daug rezervacijų, taip pat rezervacijų būseną.</span><span class="sxs-lookup"><span data-stu-id="47200-130">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="47200-131">Grafiko lentos parametrai leidžia rodyti legendą.</span><span class="sxs-lookup"><span data-stu-id="47200-131">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="47200-132">Jei grafiko lentoje šalia atskiro rezervuojamo ištekliaus atsiranda į dešinę rodanti rodyklė, išteklių galima išplėsti, kad būtų rodoma darbo, kuriam rezervuotas išteklius, informacija.</span><span class="sxs-lookup"><span data-stu-id="47200-132">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="47200-133">Kadangi „Dynamics 365 Project Operations“ naudoja „Universal Resource Scheduling“ modulį, jei jūs taip pat esate įdiegę „Dynamics 365 Field Service“, galėsi peržiūrėti projektams skirtų išteklių rezervavimų, darbo užsakymų ir bet kokių kitų objektų, kuriuos išplėtėte planavimui, išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="47200-133">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="47200-134">Norėdami peržiūrėti daugiau informacijos apie atskirą išteklių, spustelėkite dešiniu pelės klavišu, kad atidarytumėte išteklių kortelę.</span><span class="sxs-lookup"><span data-stu-id="47200-134">To view more details about an individual resource, right-click it to open the resource card.</span></span>

