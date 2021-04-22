---
title: Užsakymų ir priskyrimų derinimas
description: Šioje temoje pateikta informacija apie faktinius duomenis.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 11/27/2019
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
ms.openlocfilehash: 30af3cca9b4c3dc3f1a9412de7380c963bde88f0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5283423"
---
# <a name="reconcile-bookings-and-assignments"></a><span data-ttu-id="77843-103">Užsakymų ir priskyrimų derinimas</span><span class="sxs-lookup"><span data-stu-id="77843-103">Reconcile bookings and assignments</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="77843-104">Projekto komandos nario projektų užsakymai ir projekto užduočių priskyrimai yra silpnai susiję.</span><span class="sxs-lookup"><span data-stu-id="77843-104">A project team member's project bookings and project task assignments are loosely coupled.</span></span> <span data-ttu-id="77843-105">Todėl ištekliams gali būti užduočių priskyrimų, kurie neatitinka užsakymų, o užsakymai, gali neatitikti užduočių priskyrimų.</span><span class="sxs-lookup"><span data-stu-id="77843-105">Therefore, a resource can have task assignments that don't correspond to bookings and bookings that don't correspond to task assignments.</span></span> <span data-ttu-id="77843-106">Geriausia, kad projektų užsakymai ir užduotys būtų suderinti, kad ištekliams būtų priskirta pajėgumas atlikti užduočių priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="77843-106">Ideally, project bookings and assignments are aligned, so that resources have committed capacity to perform their task assignments.</span></span> <span data-ttu-id="77843-107">Tačiau tikrovė yra tokia, kad užsakymai gali būti atliekami atsižvelgiant į užimtumą, o užduoties laikas gali pasikeisti projekto įgyvendinimo tąsos laikotarpiu.</span><span class="sxs-lookup"><span data-stu-id="77843-107">However, the reality is that bookings can occur based on availability, and task timings can change as the project continues through its lifecycle.</span></span> <span data-ttu-id="77843-108">Todėl dėl laisvo siejimo galimas lankstumas.</span><span class="sxs-lookup"><span data-stu-id="77843-108">Therefore, the loose coupling allows for flexibility.</span></span>

<span data-ttu-id="77843-109">Dėl projekto užsakymų ir užduočių priskyrimų laisvo siejimo į projekto objektą įtraukiamas skirtukas **Derinimas**.</span><span class="sxs-lookup"><span data-stu-id="77843-109">Because of the loose coupling of project bookings and task assignments, a **Reconciliation** tab is included on the Project entity.</span></span> <span data-ttu-id="77843-110">Šis skirtukas padeda projektų vadovams suderinti komandos narių rezervavimą ir jų projekto komandos priskyrimus.</span><span class="sxs-lookup"><span data-stu-id="77843-110">This tab helps project managers reconcile team members' bookings and their assignments for their project team.</span></span>

<span data-ttu-id="77843-111">Kiekvieno pavadinto komandos nario skirtuke **Derinimas** rodomi užsakymai ir priskyrimai iki atskiro užduoties priskyrimo.</span><span class="sxs-lookup"><span data-stu-id="77843-111">For each named team member, the **Reconciliation** tab shows bookings and assignments down to the individual task assignment.</span></span> <span data-ttu-id="77843-112">Jame rodomos valandos langeliuose, kurie gali nurodyti laikotarpius nuo mėnesių iki dienų.</span><span class="sxs-lookup"><span data-stu-id="77843-112">It shows hours in cells that can represent periods from months down to days.</span></span>

<span data-ttu-id="77843-113">Lauke **Laiko skalė** galite pasirinkti **Mėnesis**, **Savaitė** arba **Diena**.</span><span class="sxs-lookup"><span data-stu-id="77843-113">In the **Timescale** field, you can select **Month**, **Week**, or **Day**.</span></span> <span data-ttu-id="77843-114">**Savaitė** yra numatytoji parinktis.</span><span class="sxs-lookup"><span data-stu-id="77843-114">By default, **Week** is selected.</span></span> <span data-ttu-id="77843-115">Tačiau numatytąją reikšmę galite pakeisti spustelėję mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="77843-115">However, you can change the default value by selecting the **Settings** button.</span></span> <span data-ttu-id="77843-116">Kai skirtukas **Derinimas** atidaromas, rodoma dabartinė data, tačiau galite naudoti kalendoriaus valdiklį ir pereiti laike į priekį arba atgal.</span><span class="sxs-lookup"><span data-stu-id="77843-116">When the **Reconciliation** tab is opened, it shows the current date, but you can use the calendar control to move forward or backward in time.</span></span> <span data-ttu-id="77843-117">Kai projekto pradžios data yra ateityje, skirtuke rodoma data, kai jis atidaromas.</span><span class="sxs-lookup"><span data-stu-id="77843-117">When a project has a start date that is in the future, the tab shows that date when it's opened.</span></span> <span data-ttu-id="77843-118">Kalendoriaus valdiklis taip pat turi parinkčių, leisiančių pereiti prie projekto pradžios ir laiko datų.</span><span class="sxs-lookup"><span data-stu-id="77843-118">The calendar control also has options that let you move to the project start and end dates.</span></span>

<span data-ttu-id="77843-119">Galite naudoti kiekvieno ištekliaus plėstuvo valdiklius, kad būtų rodoma išsami informacija apie išteklių rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="77843-119">You can use the expander controls on each resource to show the details of that resource's bookings.</span></span> <span data-ttu-id="77843-120">Taip pat galite išplėsti kiekvieno ištekliaus priskyrimus pagal atskirų užduočių lygį.</span><span class="sxs-lookup"><span data-stu-id="77843-120">You can also expand each resource's assignments to the level of the individual task.</span></span>

<span data-ttu-id="77843-121">Skirtuko **Derinimas** apačioje rodoma bendra bendroji projekto suma bei skirtuke yra bendras stulpelis.</span><span class="sxs-lookup"><span data-stu-id="77843-121">The bottom of the **Reconciliation** tab shows an overall net total for the project, and the tab also includes a total column.</span></span> <span data-ttu-id="77843-122">Kiekvienam ištekliui skirtuke atsižvelgiama į skirtumus tarp komandos nario projekto užsakymų ir tos komandos narių užduočių priskyrimų.</span><span class="sxs-lookup"><span data-stu-id="77843-122">For each resource, the tab takes the difference between a team member's bookings on the project and rollup of that team member's task assignments.</span></span> <span data-ttu-id="77843-123">Geriausiu atveju skirtumas turi būti 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="77843-123">Ideally, the difference should be 0 (zero).</span></span> <span data-ttu-id="77843-124">Kitaip sakant, išteklių rezervavimai ir jų užduočių priskyrimai neturėtų skirtis.</span><span class="sxs-lookup"><span data-stu-id="77843-124">In other words, there should be no difference between the resource's bookings and its task assignments.</span></span> <span data-ttu-id="77843-125">Bet kokius skirtumus nurodo spalva ir atspalvis atkreipti dėmesį į dvi sąlygas:</span><span class="sxs-lookup"><span data-stu-id="77843-125">Any differences are indicated by color and shading to call out two conditions:</span></span>

- <span data-ttu-id="77843-126">**Užsakymų trūkumas** – užsakymo trūkumo įvyksta, kai ištekliai turi daugiau užduočių nei užsakymų.</span><span class="sxs-lookup"><span data-stu-id="77843-126">**Booking shortage** – Booking shortages occur when a resource has more assignments than bookings.</span></span> <span data-ttu-id="77843-127">Kadangi šis pajėgumas nebuvo rezervuotas, projektų vadovas šią sąlygą gali pataisyti išplėsdamas išteklių rezervavimą, kad padengtų trūkumą.</span><span class="sxs-lookup"><span data-stu-id="77843-127">Because this capacity hasn't been reserved, a project manager can correct this condition by extending the resource's bookings to cover the shortage.</span></span>
- <span data-ttu-id="77843-128">**Užsakymų perteklius** – užsakymų perteklius įvyksta, kai ištekliai buvo rezervuoti projektui, tačiau nebuvo priskirti užduotims.</span><span class="sxs-lookup"><span data-stu-id="77843-128">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="77843-129">Ši sąlyga gali būti priimtina, jei, pvz., ištekliai buvo rezervuoti iki užduočių priskyrimo.</span><span class="sxs-lookup"><span data-stu-id="77843-129">This condition might be acceptable if, for example, the resource has been booked before task assignment occurs.</span></span> <span data-ttu-id="77843-130">Tačiau kitais atvejais ištekliai gali būti neplanuoti priskirti.</span><span class="sxs-lookup"><span data-stu-id="77843-130">However, in other cases, the resource might not be planned to be assigned.</span></span> <span data-ttu-id="77843-131">Tokiais atvejais projektų vadovas turėtų apsvarstyti išteklių rezervavimo atšaukimą, kad pajėgumą būtų galima naudoti kitam projektui.</span><span class="sxs-lookup"><span data-stu-id="77843-131">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

> [!NOTE]
> <span data-ttu-id="77843-132">Šių sąlygų legenda gali būti paslėpta, kad liktų daugiau vietos tinkleliui.</span><span class="sxs-lookup"><span data-stu-id="77843-132">The legend for these conditions might be hidden to leave more room for the grid.</span></span> <span data-ttu-id="77843-133">Šiuo atveju galite padaryti legendą matomą spustelėdami mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="77843-133">In this case, you can make the legend visible by selecting the **Settings** button.</span></span>

<span data-ttu-id="77843-134">Kai kuriais atvejais, kai laukas **Laiko skalė** nustatomas kaip lygis, kuris yra didesnis nei **Diena**, skirtumai gali būti apskaičiuojami kaip 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="77843-134">In some cases, when the **Timescale** field is set to a level that is higher than **Day**, differences might be calculated as 0 (zero).</span></span> <span data-ttu-id="77843-135">Pavyzdžiui, lygyje **Mėnesis** grynasis ištekliaus skirtumas gali būti 0 (nulis), kad nurodytų, jog užsakymai yra lygūs priskyrimams.</span><span class="sxs-lookup"><span data-stu-id="77843-135">For example, at the **Month** level, the net difference for a resource might be 0 (zero) to indicate that bookings equal assignments.</span></span> <span data-ttu-id="77843-136">Tačiau, jei peržiūrite lygį **Savaitė**, galite matyti, kad ten yra 0 (nulis) priskyrimų valandų ir rezervuota 40 valandų pirmojoje mėnesio savaitėje bei 40 priskyrimų valandų ir 0 (nulinių) valandų užsakymui antrą mėnesio savaitę.</span><span class="sxs-lookup"><span data-stu-id="77843-136">However, if you look at the **Week** level, you might see that there are assignments of 0 (zero) hours and bookings of 40 hours in the first week of the month, and assignments of 40 hours and bookings of 0 (zero) hours in the second week of the month.</span></span> <span data-ttu-id="77843-137">Nors bendras mėnesio užsakymų ir priskyrimų kiekis yra vienodas, jis skiriasi pagal savaitę.</span><span class="sxs-lookup"><span data-stu-id="77843-137">Although the total bookings and assignments for the month are equal, they differ by week.</span></span>

<span data-ttu-id="77843-138">Kai peržiūrite stambesnius laiko lygius, skirtuke **Derinimas** rodomas langelio indikatorius, kuris jums praneš, kad yra skirtumų esant smulkesniems laiko lygiams.</span><span class="sxs-lookup"><span data-stu-id="77843-138">When you view higher time levels, the **Reconciliation** tab shows a cell indicator to notify you that there are differences at lower time levels.</span></span> <span data-ttu-id="77843-139">Pavyzdžiui, šioje iliustracijoje rodomas langelio indikatorius, esantis 2018 m. spalio mėnesio langelyje, skirtame ištekliams, pavadintame Margarita Ambrazaitytė.</span><span class="sxs-lookup"><span data-stu-id="77843-139">For example, in the following illustration, a cell indicator appears in the cell for the month of October 2018 for the resource that is named Katelyn Merritt.</span></span> <span data-ttu-id="77843-140">Todėl galite matyti, kad net jei išteklių užsakymai ir priskyrimai lygūs lygiu **Mėnesis**, jie nesutampa su smulkesniais lygiais.</span><span class="sxs-lookup"><span data-stu-id="77843-140">Therefore, you can see that, even though the resource's bookings and assignments are equal when they are aggregated at the **Month** level, they don't match at lower levels.</span></span>

![Nesuderinti užsakymai ir prieskyros mėnesio lygiu](media/reconcile-assignments-01.JPG)

<span data-ttu-id="77843-142">Dukart spustelėkite langelį, jei norite priartinti kitą apatinį lygį ir peržiūrėti skirtumą.</span><span class="sxs-lookup"><span data-stu-id="77843-142">Double-click a cell to zoom in to the next lower level and view the difference.</span></span> <span data-ttu-id="77843-143">Pavyzdžiui, jei dukart spustelėjate 2018 m. spalio mėnesio skirtumą, langelyje Margarita Ambrazaitytė, galite detalizuoti lygį **Savaitė**.</span><span class="sxs-lookup"><span data-stu-id="77843-143">For example, if you double-click the October 2018 difference for Katelyn Merritt, you drill down to the **Week** level.</span></span> <span data-ttu-id="77843-144">Tada galite matyti, kad ištekliai yra rezervuoti 16 valandų, bet jokių priskyrimų, esančių pirmąsias dvi spalio mėnesio savaites, ir 16 valandų priskyrimų, tačiau jokių užsakymų trečią spalio savaitę.</span><span class="sxs-lookup"><span data-stu-id="77843-144">You can then see that the resource has bookings of 16 hours but no assignments in the first two weeks of October, and 16 hours of assignments but no bookings in the third week of October.</span></span>

![Nesuderinti užsakymai ir prieskyros savaitės lygiu](media/reconcile-assignments-02.JPG)

<span data-ttu-id="77843-146">Galite dešiniuoju pelės mygtuku spustelėti langelį ir sumažinti tolimesnį stambesnį lygį.</span><span class="sxs-lookup"><span data-stu-id="77843-146">You can right-click a cell to zoom out the next higher level.</span></span> <span data-ttu-id="77843-147">Taip pat galite išjungti langelio indikatorių pažymėdami mygtuką **Parametrai**.</span><span class="sxs-lookup"><span data-stu-id="77843-147">You can also turn off the cell indicator by selecting the **Settings** button.</span></span> 

<span data-ttu-id="77843-148">Taip pat galite naudoti mygtukus **Ankstesnis** ir **Kitas**, esančius virš tinklelio, ir peržvelgti visus projekto skirtumus.</span><span class="sxs-lookup"><span data-stu-id="77843-148">You can also use the **Previous** and **Next** buttons above the grid to move through any differences in your project.</span></span> <span data-ttu-id="77843-149">Norėdami naudoti šiuos mygtukus, pirmiausia turite pažymėti išteklių.</span><span class="sxs-lookup"><span data-stu-id="77843-149">To use these buttons, you must first select a resource.</span></span> <span data-ttu-id="77843-150">Pasirinkite **Kitas**, kad pereitumėte prie kito skirtumo tarp to ištekliaus užsakymų ir priskyrimų.</span><span class="sxs-lookup"><span data-stu-id="77843-150">Select **Next** to go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="77843-151">Pasirinkite **Ankstesnis**, kad pereitumėte prie ankstesnio skirtumo.</span><span class="sxs-lookup"><span data-stu-id="77843-151">Select **Previous** to go to the previous difference.</span></span>

<span data-ttu-id="77843-152">Situacijose, kai ištekliams yra užduočių priskyrimų, bet nėra užsakymų, galite pažymėti rezervavimo trūkumą ir pažymėti **Pratęsti rezervavimą**.</span><span class="sxs-lookup"><span data-stu-id="77843-152">In situations where you have task assignments for a resource but no bookings, you can select the booking shortage and then select **Extend Booking**.</span></span> <span data-ttu-id="77843-153">Tada galite peržiūrėti rezervavimą, reikalingą norint spręsti išteklių trūkumą.</span><span class="sxs-lookup"><span data-stu-id="77843-153">You can then see the booking that is required in order to address the resource's shortage.</span></span> <span data-ttu-id="77843-154">Taip pat galite peržiūrėti išteklių užsakymus dabartiniame projekte ir kituose projektuose.</span><span class="sxs-lookup"><span data-stu-id="77843-154">You can also view the resource's bookings on the current project and other projects.</span></span> <span data-ttu-id="77843-155">Pasirinkite **Gerai**, kad sukurtumėte išteklių rezervavimą neatsižvelgdami į dabartinį pasiekiamumą.</span><span class="sxs-lookup"><span data-stu-id="77843-155">Select **OK** to create the booking for the resource without regard to current availability.</span></span> <span data-ttu-id="77843-156">Tada projektų vadovas arba išteklių vadovas gali naudoti grafiko lentą valdyti situacijas, kai ištekliams priskirta per daug užsakymų lyginant su pajėgumu dėl to, kad užsakymai buvo pratęsti.</span><span class="sxs-lookup"><span data-stu-id="77843-156">The project manager or resource manager can then use Schedule Board to manage situations where a resource has become overbooked beyond capacity because its bookings were extended.</span></span>

## <a name="managing-with-time-zones"></a><span data-ttu-id="77843-157">Laiko juostų valdymas</span><span class="sxs-lookup"><span data-stu-id="77843-157">Managing with time zones</span></span>
<span data-ttu-id="77843-158">Norint užtikrinti tikslius ir prognozuojamus rezultatus naudojat rezervavimo išplėtimą, reikia atitikti dvi pagrindines sąlygas:</span><span class="sxs-lookup"><span data-stu-id="77843-158">To ensure accurate and predictable results when using Extend Booking, there are two key prerequisites that must be met:</span></span>  

- <span data-ttu-id="77843-159">Naudotojas turi nustatyti savo įrenginio laiko juostą, kad ji atitiktų laiko juostą, apibrėžtą sistemos personalizavimo parametruose.</span><span class="sxs-lookup"><span data-stu-id="77843-159">The user must configure their device's time zone to match the time zone defined in your system's Personalization Settings.</span></span>
 
  ![Laiko juostos parametrai „Windows 10“](media/reconcile-assignments-03.png)

  ![Laiko juostos parametrai personalizavimo parametruose](media/reconcile-assignments-04.png)
 
- <span data-ttu-id="77843-162">Rezervuojami ištekliai turi turėti bent vieną minutę darbo laiko, kuri sutampa su kontūrais, kurie naudojami pageidaujamo išplėtimo apibrėžimui.</span><span class="sxs-lookup"><span data-stu-id="77843-162">The Bookable Resource must have at least one minute of working time that overlaps with the contours that are used to define the requested extension.</span></span> <span data-ttu-id="77843-163">Pavyzdžiui, toliau pateiktame pavyzdyje rodomi peržiūros ištekliai su darbo valandomis, kurios yra intervale nuo 9.00 iki 19.00.</span><span class="sxs-lookup"><span data-stu-id="77843-163">For instance, the following example shows review resources with working hours that fall between 9:00 AM and 7:00 PM.</span></span> 

  ![Išteklių kontūrų palyginimas](media/reconcile-assignments-05.png)

<span data-ttu-id="77843-165">Toliau esančioje lentelėje pateikiama:</span><span class="sxs-lookup"><span data-stu-id="77843-165">The following table shows:</span></span>

- <span data-ttu-id="77843-166">A projekto kalendoriaus šablonas.</span><span class="sxs-lookup"><span data-stu-id="77843-166">A project calendar template.</span></span>
- <span data-ttu-id="77843-167">A išteklius: šis išteklius turi tą patį kalendorių ir yra toje pačioje laiko juostoje kaip ir projektas.</span><span class="sxs-lookup"><span data-stu-id="77843-167">Resource A: This resource has the same calendar and is in the same time zone as the project.</span></span> <span data-ttu-id="77843-168">Rezervavimo pradžios laikas bus 9.00.</span><span class="sxs-lookup"><span data-stu-id="77843-168">The start time of the bookings will be 9:00 AM.</span></span>
- <span data-ttu-id="77843-169">B išteklius: šis išteklius yra kitoje nei projektas laiko zonoje, todėl jo pradžia yra 7.00 jo laiko juostoje.</span><span class="sxs-lookup"><span data-stu-id="77843-169">Resources B: This resource is located in a different time zone than the project and therefore starts at 7:00 AM in their time zone.</span></span> <span data-ttu-id="77843-170">Tačiau rezervavimai prasidės 9.00, nes tai yra anksčiausias priskyrimo kontūro pradžios laikas.</span><span class="sxs-lookup"><span data-stu-id="77843-170">However, the bookings will begin at 9:00 AM as that is the earliest start time of the assignment contour.</span></span>
- <span data-ttu-id="77843-171">C ir D ištekliai: šie ištekliai taip pat yra skirtingose laiko juostose, kurios abi skiriasi tarpusavyje ir nuo projekto, todėl jų rezervavimai prasidės ne anksčiau nei atitinkami galimi pradžios laikai.</span><span class="sxs-lookup"><span data-stu-id="77843-171">Resources C and D: The resources are also located in different time zones, both different from each other and the project, and their bookings start no earlier than their respective available start times.</span></span>

|<span data-ttu-id="77843-172">Objektas</span><span class="sxs-lookup"><span data-stu-id="77843-172">Entity</span></span>  |<span data-ttu-id="77843-173">Kalendorius</span><span class="sxs-lookup"><span data-stu-id="77843-173">Calendar</span></span>  |
|-|-|
|<span data-ttu-id="77843-174">Projekto kalendoriaus šablonas</span><span class="sxs-lookup"><span data-stu-id="77843-174">Project calendar template</span></span>   | ![Projekto kalendorius](media/reconcile-assignments-06.png) |
|<span data-ttu-id="77843-176">A išteklius</span><span class="sxs-lookup"><span data-stu-id="77843-176">Resource A</span></span>  | ![A ištekliaus kalendorius](media/reconcile-assignments-06.png) |
|<span data-ttu-id="77843-178">B išteklius</span><span class="sxs-lookup"><span data-stu-id="77843-178">Resource B</span></span>  |  ![B ištekliaus kalendorius](media/reconcile-assignments-07.png) |
|<span data-ttu-id="77843-180">C išteklius</span><span class="sxs-lookup"><span data-stu-id="77843-180">Resource C</span></span>  |  ![C ištekliaus kalendorius](media/reconcile-assignments-08.png) |
|<span data-ttu-id="77843-182">D išteklius</span><span class="sxs-lookup"><span data-stu-id="77843-182">Resource D</span></span>  | ![D ištekliaus kalendorius](media/reconcile-assignments-09.png)  |
 
<span data-ttu-id="77843-184">Kai pereisite į suderinimo rodinį, bus rodomi išteklių priskyrimai ir susiję rezervavimo trūkumai.</span><span class="sxs-lookup"><span data-stu-id="77843-184">When you navigate to the reconciliation view, the resource assignments and the associated booking shortages will be displayed.</span></span>
 <span data-ttu-id="77843-185">![Suderinimo rodinys prieš išplėtimą](media/reconcile-assignments-10.png)</span><span class="sxs-lookup"><span data-stu-id="77843-185">![Reconciliation view before extension](media/reconcile-assignments-10.png)</span></span>

<span data-ttu-id="77843-186">Po to, kai buvo įvykdyta kiekvieno ištekliaus rezervavimo pratęsimo funkcija, sėkmingai pratęsiamos kiekvieno ištekliaus rezervacijos.</span><span class="sxs-lookup"><span data-stu-id="77843-186">After the Extend Booking functionality has been executed on each resource, bookings are successfully extended for each resource.</span></span> <span data-ttu-id="77843-187">Taip yra todėl, kad kiekvieno ištekliaus darbo valandos sutapo su trūkumo kontūrais.</span><span class="sxs-lookup"><span data-stu-id="77843-187">This is because each resource’s working hours overlapped with the contours of the shortage.</span></span>
 <span data-ttu-id="77843-188">![Suderinimo rodinys po rezervavimo išplėtimo](media/reconcile-assignments-11.png)</span><span class="sxs-lookup"><span data-stu-id="77843-188">![Reconciliation view after booking extension](media/reconcile-assignments-11.png)</span></span> 

<span data-ttu-id="77843-189">Tačiau atidžiau apžvelgus rezervacijų išsamią informacija, matomi rezervacijų laiko pradžios skirtumai.</span><span class="sxs-lookup"><span data-stu-id="77843-189">However, a closer look at the details of the bookings shows differences in the start time of the bookings.</span></span> <span data-ttu-id="77843-190">Rezervavimai prasidės ne anksčiau nei priskyrimo kontūro pradžios laikas ir ne anksčiau nei galimas ištekliaus pradžios laikas.</span><span class="sxs-lookup"><span data-stu-id="77843-190">The bookings will start no earlier than the start time of the assignment contour and no earlier than the available start time of the resource.</span></span>
 <span data-ttu-id="77843-191">![Naujos išteklių rezervacijos grafiko lentoje](media/reconcile-assignments-12.png)</span><span class="sxs-lookup"><span data-stu-id="77843-191">![New bookings of the resources in the schedule board](media/reconcile-assignments-12.png)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]