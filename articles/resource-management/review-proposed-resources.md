---
title: Peržiūrėti siūlomus išteklius
description: Šioje temoje pateikiama informacija apie tai, kaip siūlyti projekto išteklius.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080803"
---
# <a name="review-proposed-resources"></a><span data-ttu-id="0e20b-103">Peržiūrėti siūlomus išteklius</span><span class="sxs-lookup"><span data-stu-id="0e20b-103">Review proposed resources</span></span>

<span data-ttu-id="0e20b-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="0e20b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="0e20b-105">Išteklių valdytojai projektų vadovui gali pasiūlyti išteklius naudodami išteklių užklausą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-105">Resource managers can propose a resource to the project manager by using a resource request.</span></span>

1. <span data-ttu-id="0e20b-106">Išteklių užklausos tinklelyje pažymėkite **Rasti išteklius**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-106">From the request grid or the request itself, select **Find Resources**.</span></span>
2. <span data-ttu-id="0e20b-107">Puslapyje **Planavimo pagalbinė priemonė** pažymėkite išteklius, tada skyde **Kurti išteklių rezervaciją** lauke **Rezervacijos būsena** pažymėkite **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-107">On the **Schedule Assistant** page, select the resource, and then, in the **Create Resource Booking** pane, in the **Booking Status** field, select **Book**.</span></span>

<span data-ttu-id="0e20b-108">Galimi šie būsenos naujinimai:</span><span class="sxs-lookup"><span data-stu-id="0e20b-108">The following status updates occur:</span></span>

- <span data-ttu-id="0e20b-109">Puslapyje **Planavimo pagalbinė priemonė** būsenos indikatoriai atnaujinami, kad rodytų, kad rezervacija yra pasiūlyta, o ne galutinai rezervuota.</span><span class="sxs-lookup"><span data-stu-id="0e20b-109">On the **Schedule Assistant** page, the status indicators are updated to indicate that the booking is proposed, not hard-booked.</span></span>
- <span data-ttu-id="0e20b-110">Išteklių užklausoje būsena pakeičiama į **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-110">On the resource request, the status is changed to **Needs Review**.</span></span>
- <span data-ttu-id="0e20b-111">Projekto skirtuke **Komanda** bendrosios komandos nario reikšmė **Pageidauti būsenos** pakeičiama į **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-111">On the **Team** tab of the project, the generic team member's **Request Status** value is changed to **Needs Review**.</span></span>

<span data-ttu-id="0e20b-112">Projekto vadovas gali priimti arba atmesti pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-112">The project manager can either accept or reject the proposal.</span></span>

<span data-ttu-id="0e20b-113">Kai išteklių valdytojas apdoroja išteklių užklausas, jis gali naudoti bet kurį iš toliau nurodytų metodų.</span><span class="sxs-lookup"><span data-stu-id="0e20b-113">When resource managers process resource requests, they can use any of the following approaches:</span></span>

- <span data-ttu-id="0e20b-114">Pasiūlyti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užpildytų pageidaujamas valandas.</span><span class="sxs-lookup"><span data-stu-id="0e20b-114">Propose multiple resources to satisfy the demand if no single resource is available to fulfill the required hours.</span></span> <span data-ttu-id="0e20b-115">Tada pasiūlytos valandos padalinamos keliams ištekliams, kurie gali patenkinti pageidaujamas valandas.</span><span class="sxs-lookup"><span data-stu-id="0e20b-115">Proposed hours are then split among multiple resources that can satisfy the required hours.</span></span> <span data-ttu-id="0e20b-116">Tokiu atveju valandos negali persidengti.</span><span class="sxs-lookup"><span data-stu-id="0e20b-116">In this scenario, the hours can't overlap.</span></span>
- <span data-ttu-id="0e20b-117">Pasiūlyti mažiau išteklių, nei pageidaujama.</span><span class="sxs-lookup"><span data-stu-id="0e20b-117">Propose fewer resources than are required.</span></span> <span data-ttu-id="0e20b-118">Tokiu atveju pasiūlytas išteklių pajėgumas yra mažesnis nei pageidaujamos valandos, kurias nurodė pageidaujantis asmuo.</span><span class="sxs-lookup"><span data-stu-id="0e20b-118">In this scenario, the proposed resource capacity is less than the required hours that the requestor specified.</span></span> <span data-ttu-id="0e20b-119">Todėl, kai pageidaujantis asmuo sutinka su pasiūlytais ištekliais, sukuriamas neįvykdytas išteklių reikalavimas, kuris fiksuoja likusią poreikio dalį.</span><span class="sxs-lookup"><span data-stu-id="0e20b-119">Therefore, when the requestor accepts the proposed resources, an unfulfilled resource requirement is created to capture the remaining demand.</span></span>
- <span data-ttu-id="0e20b-120">Rezervuoti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užbaigtų darbą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-120">Book multiple resources to satisfy the demand if no single resource is available to complete the work.</span></span>
- <span data-ttu-id="0e20b-121">Rezervuoti mažiau išteklių, nei pageidaujama.</span><span class="sxs-lookup"><span data-stu-id="0e20b-121">Book fewer resources than are required.</span></span> <span data-ttu-id="0e20b-122">Tokiu atveju rezervuotų valandų yra mažiau nei pageidautų valandų.</span><span class="sxs-lookup"><span data-stu-id="0e20b-122">In this scenario, the booked hours are fewer than the required hours.</span></span> <span data-ttu-id="0e20b-123">Sistema parodys, kaip pasiūlyti išteklius, o ne rezervacijas, kad pageidaujantis asmuo galėtų patikrinti ir stebėti likusią poreikio dalį.</span><span class="sxs-lookup"><span data-stu-id="0e20b-123">The system guides you to propose resources instead of bookings, so that the requestor can verify and keep track of remaining demand.</span></span>

## <a name="billable-utilization"></a><span data-ttu-id="0e20b-124">Apmokėtinas naudojimas</span><span class="sxs-lookup"><span data-stu-id="0e20b-124">Billable utilization</span></span>

<span data-ttu-id="0e20b-125">Ištekliai gali turėti tikslinį apmokėtiną naudojimą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-125">Resources can have a target billable utilization.</span></span> <span data-ttu-id="0e20b-126">Šis tikslinis naudojimas apibrėžiamas kaip atributas išteklių numatytame vaidmenyje arba nustatomas atskiro rezervuojamo ištekliaus įraše.</span><span class="sxs-lookup"><span data-stu-id="0e20b-126">This target utilization is either defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="0e20b-127">Naudojimo skaičiavimai pagrįsti faktinėmis valandomis, apie kurias ištekliai pranešė naudodami patvirtintus laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="0e20b-127">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="0e20b-128">Naudojimo skaičiavimui naudojamos toliau nurodytos formulės.</span><span class="sxs-lookup"><span data-stu-id="0e20b-128">The following formulas are used to calculate utilization:</span></span>

- <span data-ttu-id="0e20b-129">Apmokėtinas naudojimas = apmokestinamos faktinės valandos ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="0e20b-129">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
- <span data-ttu-id="0e20b-130">Neapmokėtinas naudojimas = faktinis laikas su apmokėtino tipo ID = neapmokestinamas, papildomas arba negalimas ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="0e20b-130">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
- <span data-ttu-id="0e20b-131">Vidinis = faktinis laikas be pardavimo sutarties ÷ išteklių pajėgumas</span><span class="sxs-lookup"><span data-stu-id="0e20b-131">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
- <span data-ttu-id="0e20b-132">Išteklių pajėgumas = išteklių darbo valandos – išvykęs – ne darbo dienos</span><span class="sxs-lookup"><span data-stu-id="0e20b-132">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="0e20b-133">Rodinį **Išteklių naudojimas** galite rasti skyde **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-133">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="0e20b-134">Kiekvienas tinklelio langelis nurodo išteklių apmokėtiną naudojimą pagal laiką, pavyzdžiui, dieną, savaitę arba mėnesį.</span><span class="sxs-lookup"><span data-stu-id="0e20b-134">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="0e20b-135">Langeliams naudojamos toliau nurodytos spalvos.</span><span class="sxs-lookup"><span data-stu-id="0e20b-135">The following formulas are used to color the cells:</span></span>

- <span data-ttu-id="0e20b-136">**Žalia:** apmokėtinas naudojimas \>= išteklių tikslinis naudojimas</span><span class="sxs-lookup"><span data-stu-id="0e20b-136">**Green:** Billable utilization \>= Resource target utilization</span></span>
- <span data-ttu-id="0e20b-137">**Geltona:** tikslinis naudojimas – 20 \<= apmokėtinas naudojimas \< tikslinis naudojimas</span><span class="sxs-lookup"><span data-stu-id="0e20b-137">**Yellow:** Target utilization – 20 \<= Billable utilization \< Target utilization</span></span>
- <span data-ttu-id="0e20b-138">**Raudona:** apmokėtinas naudojimas \< tikslinis naudojimas – 20</span><span class="sxs-lookup"><span data-stu-id="0e20b-138">**Red:** Billable utilization \< Target utilization – 20</span></span>

<span data-ttu-id="0e20b-139">Kadangi rodinys **Išteklių naudojimas** pagrįstas grafiko lenta, galite naudoti grafiko lentos filtravimo galimybes, kad filtruotumėte rezultatus.</span><span class="sxs-lookup"><span data-stu-id="0e20b-139">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="0e20b-140">Reikia, kad tinkleliui nustatytumėte tikslinį naudojimą arba pagal vaidmenį, arba individualų išteklių.</span><span class="sxs-lookup"><span data-stu-id="0e20b-140">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="0e20b-141">Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** \> **Išteklių vaidmenys**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-141">To do this setup, go to **Resources** \> **Resource roles**.</span></span>

<span data-ttu-id="0e20b-142">Be to, kiekvienam rezervuojamam ištekliui reikia priskirti numatytąjį vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="0e20b-142">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="0e20b-143">Eikite į **Ištekliai** \> **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-143">Go to **Resources** \> **Resources**.</span></span> <span data-ttu-id="0e20b-144">Skirtuke **Project Service** patikrinkite, kad nustatytas išteklių vaidmuo ir kad laukas **Yra numatytasis** nustatytas kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-144">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field for it is set to **Yes**.</span></span> <span data-ttu-id="0e20b-145">Galite įtraukti papildomų vaidmenų, kai **Kaip numatytasis = ne**.</span><span class="sxs-lookup"><span data-stu-id="0e20b-145">You can add additional roles where **Is Default = No**.</span></span> <span data-ttu-id="0e20b-146">Vaidmuo, kai **Yra numatytasis = taip** , naudojamas išteklių naudojimui įvertinti pagal to vaidmens tikslą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-146">The role where the **Is Default = Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="0e20b-147">Skirtuke **Project Service** taip pat galite ištekliui nustatyti individualų tikslinį naudojimą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-147">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="0e20b-148">Tada naudojimo skaičiavimui naudojamas šis tikslinis naudojamas, kad būtų įvertintas išteklių tikslas, o ne išteklių numatytojo vaidmens tikslas.</span><span class="sxs-lookup"><span data-stu-id="0e20b-148">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="0e20b-149">Išteklių naudojimas rodomas, tik jei šis išteklius turi patvirtintą ir apmokestinamą laiką periode, kuris rodomas tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="0e20b-149">Utilization is shown for a resource only if that resource has approved, chargeable time during the period that is shown in the grid.</span></span>

## <a name="resource-availability"></a><span data-ttu-id="0e20b-150">Išteklių pasiekiamumą</span><span class="sxs-lookup"><span data-stu-id="0e20b-150">Resource availability</span></span>

<span data-ttu-id="0e20b-151">Labai svarbu, kad išteklių valdytojai galėtų peržiūrėti išteklių pasiekiamumą ir naujinti rezervacijas.</span><span class="sxs-lookup"><span data-stu-id="0e20b-151">It's critical that resource managers be able to view the availability of resources and update bookings.</span></span> <span data-ttu-id="0e20b-152">Kai kuriais atvejais nėra formalaus poreikio (išteklių užklausos), tačiau išteklių valdytojas turi reaguoti į neplanuotą poreikį, kurį gauna per tokius kanalus kaip el. paštas, telefono skambutis ar tiesioginis pranešimas.</span><span class="sxs-lookup"><span data-stu-id="0e20b-152">In some cases, there is no formal demand (resource request), but a resource manager must respond to an unplanned demand that comes through channels such as an email, phone call, or instant message.</span></span> <span data-ttu-id="0e20b-153">Išteklių valdytojai naudoja grafiko lentą, kad naujintų išteklius ir rezervacijas.</span><span class="sxs-lookup"><span data-stu-id="0e20b-153">Resource managers use the Schedule Board to update resources and bookings.</span></span>

<span data-ttu-id="0e20b-154">Išteklių darbo valandos naudojamos kaip išteklių pasiekiamumo skaičiavimo pagrindas.</span><span class="sxs-lookup"><span data-stu-id="0e20b-154">Resource work hours are used as the basis for calculating the availability of a resource.</span></span> <span data-ttu-id="0e20b-155">Išteklių rezervacijos naudoja išteklių pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-155">Resource bookings consume the capacity of the resources.</span></span>

<span data-ttu-id="0e20b-156">Grafiko lentoje naudojamos spalvos ir atspalviai, kurie rodo rezervacijas, pasiekiamumą ir per daug rezervacijų, taip pat rezervacijų būseną.</span><span class="sxs-lookup"><span data-stu-id="0e20b-156">The Schedule Board uses colors and shading to show bookings, availability, and overbookings, and also the status of bookings.</span></span> <span data-ttu-id="0e20b-157">Grafiko lentos parametrai leidžia rodyti legendą.</span><span class="sxs-lookup"><span data-stu-id="0e20b-157">A setting in the Schedule Board settings lets you show a legend.</span></span>

<span data-ttu-id="0e20b-158">Jei grafiko lentoje šalia atskiro rezervuojamo ištekliaus atsiranda į dešinę rodanti rodyklė, išteklių galima išplėsti, kad būtų rodoma darbo, kuriam rezervuotas išteklius, informacija.</span><span class="sxs-lookup"><span data-stu-id="0e20b-158">If a right-pointing arrow appears next to an individual bookable resource on the Schedule Board, the resource can be expanded to show details of the work that the resource is booked on.</span></span>

<span data-ttu-id="0e20b-159">Kadangi „Dynamics 365 Project Operations“ naudoja „Universal Resource Scheduling“ modulį, jei jūs taip pat esate įdiegę „Dynamics 365 Field Service“, galėsi peržiūrėti projektams skirtų išteklių rezervavimų, darbo užsakymų ir bet kokių kitų objektų, kuriuos išplėtėte planavimui, išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="0e20b-159">Because Dynamics 365 Project Operations uses the Universal Resource Scheduling engine, if you also have Dynamics 365 Field Service installed, you can view the details of resource bookings for projects, work orders, and any other entities that you've extended scheduling to.</span></span>

<span data-ttu-id="0e20b-160">Norėdami peržiūrėti daugiau informacijos apie atskirą išteklių, spustelėkite dešiniu pelės klavišu, kad atidarytumėte išteklių kortelę.</span><span class="sxs-lookup"><span data-stu-id="0e20b-160">To view more details about an individual resource, right-click it to open the resource card.</span></span>

