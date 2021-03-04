---
title: Tvarkyti išteklius
description: Šioje temoje pateikiama informacija apie tai, kaip galite tvarkyti išteklius.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 05/13/2019
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
ms.openlocfilehash: 37377367751592fc533447748b80b124cb6548ad
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151353"
---
# <a name="manage-resources"></a><span data-ttu-id="6c6ad-103">Tvarkyti išteklius</span><span class="sxs-lookup"><span data-stu-id="6c6ad-103">Manage resources</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="6c6ad-104">Į Dynamics 365 Project Service Automation įeina išteklių valdymo ataskaitų sritis, teikianti vaizdinį išteklių poreikio ir naudojimo visoje organizacijoje apžvalgą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-104">Dynamics 365 Project Service Automation includes a resource manager dashboard that provides a visual overview of resource demand and utilization throughout the organization.</span></span> <span data-ttu-id="6c6ad-105">Šioje ataskaitų srityje galite naudoti diagramas, kad galėtumėte vizualizuoti šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-105">You can use the charts on this dashboard to visualize the following information:</span></span>

- <span data-ttu-id="6c6ad-106">**Išteklių poreikis** – diagramoje **Aktyvių išteklių užklausa** rodomi pateikt ištekliai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-106">**Resource demand** – The **Active Resource Request** chart shows resources that have been submitted.</span></span> <span data-ttu-id="6c6ad-107">Ištekliai yra agreguojami pagal vaidmenį arba projektą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-107">The resources are aggregated by either role or project.</span></span>
- <span data-ttu-id="6c6ad-108">**Nepateiktų išteklių poreikis** – diagramoje **Nepriskirtų išteklių poreikis** rodomi visi nepateikti išteklių reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-108">**Unsubmitted resource demand** – The **Unassigned Resource Demand** chart shows all the resource requirements that haven't been submitted.</span></span> <span data-ttu-id="6c6ad-109">Tai padeda išteklių vadovams peržiūrėti poreikį, kuris nėra patvirtintas ir gali būti pateiktas naudojant išteklių užklausą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-109">It helps resource managers view demand that isn't firm and might be submitted through a resource request.</span></span>
- <span data-ttu-id="6c6ad-110">**Apmokėtinas realizavimas per paskutinę savaitę** – diagramoje **Naudojimas pagal vaidmenį** rodoma organizacijos faktinis apmokamas realizavimas pagal vaidmenį lyginant su tiksliniu apmokėtinu realizavimu pagal vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-110">**Billable utilization for the past week** – The **Utilization by Role** chart shows the percentage of the organization's actual billable utilization by role against its target billable utilization by role.</span></span>

    > [!NOTE]
    > <span data-ttu-id="6c6ad-111">Kad pasiektumėte diagramą **Naudojimas pagal vaidmenį**, sukurkite užduotį, kuri vykdo darbo eigą UpdateRoleUtilization.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-111">To make the **Utilization by Role** chart available, create a job that runs the UpdateRoleUtilization workflow.</span></span> <span data-ttu-id="6c6ad-112">Ši pasikartojanti užduotis vykdoma kas septynias dienas, kad apskaičiuotų apmokėtiną realizavimą per ankstesnes septynias dienas.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-112">This recurring job runs every seven days to calculate billable utilization for the previous seven days.</span></span> <span data-ttu-id="6c6ad-113">Rezultatai sujungiami pagal vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-113">The results are aggregated by role.</span></span>

## <a name="manage-project-team-members"></a><span data-ttu-id="6c6ad-114">Projekto komandos narių valdymas</span><span class="sxs-lookup"><span data-stu-id="6c6ad-114">Manage project team members</span></span>

<span data-ttu-id="6c6ad-115">Projektų vadovai gali naudoti išteklių vadovo ataskaitų sritį, kad valdytų projektų išteklius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-115">Project managers can use the resource manager dashboard to manage the resources on projects.</span></span> <span data-ttu-id="6c6ad-116">Pavyzdžiui, jie gali įtraukti komandos narį tiesiogiai į projektą ir rezervuoti komandos narį vykdyti išteklių reikalavimus, kurie buvo užfiksuoti bendrųjų išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-116">For example, they can add a team member directly to a project and book a team member to fulfill the resource requirements that were captured by a generic resource.</span></span>

### <a name="add-a-team-member-directly-to-a-project"></a><span data-ttu-id="6c6ad-117">Komandos nario įtraukimas tiesiogiai į projektą</span><span class="sxs-lookup"><span data-stu-id="6c6ad-117">Add a team member directly to a project</span></span>

<span data-ttu-id="6c6ad-118">Norėdami įtraukti komandos narį tiesiogiai į projektą, puslapio **Projektai** skirtuke **Komanda** pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-118">To add a team member directly to a project, on the **Projects** page, on the **Team** tab, select **New**.</span></span> <span data-ttu-id="6c6ad-119">Atsiras dialogo langas **Spartusis kūrimas: projekto komandos narys**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-119">The **Quick Create:Project Team Member** dialog box appears.</span></span> <span data-ttu-id="6c6ad-120">Šiame dialogo lange galite atlikti šias užduotis:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-120">In this dialog box, you can perform these tasks:</span></span>

- <span data-ttu-id="6c6ad-121">**Rezervuokite įvardytuosius išteklius** – lauke **Rezervuojami ištekliai** pasirinkite ištekliaus pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-121">**Book a named resource** – In the **Bookable Resource** field, select the name of the resource.</span></span> <span data-ttu-id="6c6ad-122">Tada pažymėkite vaidmenį, nustatykite laikotarpį ir pažymėkite paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-122">Then select the role, set the period, and select an allocation method.</span></span> <span data-ttu-id="6c6ad-123">Jūsų pažymėtas įvardytas išteklius įtraukiamas į projektą naudojant pasirinktą paskirstymo metodą ir išteklių kalendorių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-123">The named resource that you selected is added to the project by using the selected allocation method and the resources calendar.</span></span>
- <span data-ttu-id="6c6ad-124">**Įtraukite bendrąjį išteklių** – palikite lauką **Rezervuojami ištekliai** tuščią, o tada pažymėkite vaidmenį, nustatykite laikotarpį ir pažymėkite pageidaujamą paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-124">**Add a generic resource** – Leave the **Bookable resource** field blank, and then select the role, set the period, and select the preferred allocation method.</span></span> <span data-ttu-id="6c6ad-125">Bendrasis išteklius įtraukiamas į komandą kaip vietos rezervavimo ženklas, kad būtų išlaikytas poreikio modelis, kuris naudojamas įvardytiesiems ištekliams komandoje užsakyti.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-125">A generic resource is added to the team as a placeholder to hold the demand pattern that is used to book named resources on the team.</span></span> <span data-ttu-id="6c6ad-126">Reikalavimas pateikiamas pagal projekto kalendorių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-126">The requirement is made according to the project calendar.</span></span>
- <span data-ttu-id="6c6ad-127">**Įtraukite įvardytąjį išteklių į komandą nenaudojant išteklių pajėgumo** – lauke **Rezervuojami ištekliai** pažymėkite išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-127">**Add a named resource to the team without consuming resource capacity** – In the **Bookable Resource** field, select a resource.</span></span> <span data-ttu-id="6c6ad-128">Tada pasirinkite laikotarpį ir pažymėkite **Nėra** kaip paskirstymo metodą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-128">Then select the period, and select **None** as the allocation method.</span></span> <span data-ttu-id="6c6ad-129">Išteklius įtraukiamas į komandą, tačiau ištekliaus pajėgumas užsakyme nenaudojamas.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-129">The resource is added to the team, but the resource's capacity isn't consumed through a booking.</span></span>

### <a name="book-a-team-member-to-fulfill-resource-requirements-for-a-generic-resource"></a><span data-ttu-id="6c6ad-130">Užsakykite komandos narį, kad būtų galima vykdyti išteklių reikalavimus bendriesiems ištekliams</span><span class="sxs-lookup"><span data-stu-id="6c6ad-130">Book a team member to fulfill resource requirements for a generic resource</span></span>

<span data-ttu-id="6c6ad-131">Naudodami PSA galite užsakyti bendrąjį išteklių projekto komandoje ir nurodyti vaidmenį, būtiną pajėgumą ir šio pajėgumo paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-131">In PSA, you can book a generic resource on a project team, and can specify the role, the required capacity, and how that capacity is distributed.</span></span> <span data-ttu-id="6c6ad-132">Kaip išteklių reikalavimus galite nurodyti su bendruoju ištekliumi susietus atributus.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-132">On the resource requirement, you can specify attributes that are associated with the generic resource.</span></span> <span data-ttu-id="6c6ad-133">Į šiuos atributus įtraukti būtini įgūdžiai, pageidaujamas organizacijos vienetas ir pageidautini ištekliai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-133">These attributes include required skills, the preferred organizational unit, and preferred resources.</span></span>

<span data-ttu-id="6c6ad-134">Vadovaukitės šiais veiksmais, kad nustatytumėte bendrūjų išteklių kūrėjams būtinus įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-134">Follow these steps to specify required skills on a generic resource for a developer.</span></span>

1. <span data-ttu-id="6c6ad-135">Puslapio **Projektai** skirtuke **Komanda** pažymėkite **Naujas**, kad rezervuotumėte bendrąjį išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-135">On the **Projects** page, on the **Team** tab, select **New** to book a generic resource.</span></span>

    ![Komandoje rezervuotas bendrasis išteklius](media/Resource-Management-image9.png)

2. <span data-ttu-id="6c6ad-137">Rodinyje **Viso komandos nariai**, stulpelyje **Ištekliaus reikalavimas** pažymėkite nuorodą, kad įtrauktumėte bendriesiems ištekliams būtinus įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-137">In the **All Team Members** view, in the **Resource Requirement** column, select the link to add required skills for the generic resource.</span></span>

    ![Reikalavimų nuoroda](media/Resource-Management-image10.png)

3. <span data-ttu-id="6c6ad-139">Pasirodžiusio puslapio **Ištekliaus reikalavimas** tinklelyje **Įgūdžiai** pasirinkite elipsę (**...**), o tada pažymėkite **Įtraukti naują reikalavimo charakteristiką**, kad įtrauktumėte kūrėjui būtinus įgūdžius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-139">On the **Resource Requirement** page that appears, in the **Skills** grid, select the ellipsis (**...**) and then select **Add New Requirement Characteristic** to add the required skills for your developer.</span></span>

    ![Komanda „Įtraukti naują reikalavimo charakteristiką“](media/Resource-Management-image11.png)

4. <span data-ttu-id="6c6ad-141">Pasirodžiusiame dialogo lange **Spartusis kūrimas: reikalavimo charakteristika** esančiame lauke **Charakteristika** pasirinkite būtiną įgūdį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-141">In the **Quick Create: Requirement Characteristic** dialog box that appears, in the **Characteristic** field, select the required skill.</span></span> <span data-ttu-id="6c6ad-142">Tada lauke **Įvertinimo reikšmė** pažymėkite šio įgūdžio kompetencijos lygį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-142">Then, in the **Rating value** field, select the proficiency level for that skill.</span></span> <span data-ttu-id="6c6ad-143">Galiausiai lauke **Ištekliaus reikalavimas** nustatykite reikalavimą šaltinio ištekliams iš organizacijos vienetų arba net įvardytų išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-143">Finally, in the **Resource Requirement** field, set the requirement to source resources from organizational units or even named resources.</span></span> <span data-ttu-id="6c6ad-144">Baigę pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-144">When you've finished, select **Save**.</span></span>

    ![Spartusis kūrimas: dialogo langas „Reikalavimo charakteristika“](media/Resource-Management-image12.png)

5. <span data-ttu-id="6c6ad-146">Puslapyje **Ištekliaus reikalavimas** pažymėkite **Rezervuoti**, kad būtų įvykdyti ištekliaus reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-146">On the **Resource Requirement** page, select **Book** to fulfill the resource requirement.</span></span>

    ![Rezervavimo mygtukas puslapyje „Ištekliaus reikalavimas“](media/Resource-Management-image13.png)

    <span data-ttu-id="6c6ad-148">Bendrąjį išteklių taip pat galite pasirinkti tinklelyje **Visi komandos nariai**, o tada pažymėti **Rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-148">You can also select the generic resource in the **All Team Members** grid and then select **Book**.</span></span>

    ![Rezervavimo mygtukas virš tinklelio „Visi komandos nariai“](media/Resource-Management-image14.png)

    > [!NOTE]
    > <span data-ttu-id="6c6ad-150">Šiame pavyzdyje yra 40 reikiamų valandų, tačiau nėra faktinių rezervuotų valandų, nes bendrieji ištekliai neturi užsakymų.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-150">In this example, there are 40 required hours but no actual booked hours, because generic resources don't have bookings.</span></span> <span data-ttu-id="6c6ad-151">Be to, nėra priskirtų valandų, nes bendrasis išteklius buvo įtrauktas tiesiogiai į komandą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-151">Additionally, there are no assigned hours, because the generic resource was added directly to the team.</span></span> <span data-ttu-id="6c6ad-152">Jis nebuvo įtrauktas naudojant užduočių priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-152">It wasn't added by using task assignment.</span></span>

    <span data-ttu-id="6c6ad-153">Puslapyje **Planavimo pagalbinė priemonė** galite filtruoti prieinamus išteklius pagal reikalavimus, nurodytus ištekliaus reikalavime.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-153">On the **Scheduling Assistant** page, you can filter available resources by the requirements that are specified on the resource requirement.</span></span> <span data-ttu-id="6c6ad-154">Ištekliai rūšiuojami pagal rūšiavimo parametrus, apibrėžtus grafiko lentoje.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-154">Resources are sorted according to the sorting parameters that are specified on the Schedule Board.</span></span>

    ![Planavimo pagalbinės priemonės puslapis](media/Resource-Management-image15.png)

    <span data-ttu-id="6c6ad-156">Toliau pateikiami keli dažnai naudojami filtrai:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-156">Here are some filters that are often used:</span></span>

    - <span data-ttu-id="6c6ad-157">**Charakteristikos kartu su įvertinimu** – filtruoja pagal įgūdžius, sertifikatus ir kitas išteklių ypatybes bei pateikia kompetencijos įvertinimus.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-157">**Characteristics along with a rating** – Filter by skills, certifications, and other resource qualities, in addition to ratings of proficiency.</span></span>
    - <span data-ttu-id="6c6ad-158">**Vaidmenys** – filtruoja pagal rezervuojamiems ištekliams priskirtus numatytuosius vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-158">**Roles** – Filter by the default roles that are assigned to bookable resources.</span></span>
    - <span data-ttu-id="6c6ad-159">**Organizacijos vienetai** – filtruoja rezervuojamus išteklius pagal organizacijos vienetus, kuriems jie yra priskirti.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-159">**Organizational units** – Filter bookable resources by the organizational units that they are assigned to.</span></span>

6. <span data-ttu-id="6c6ad-160">Jei netenkina pradinio reikalavimo ieškos rezultatai, galite pakeisti filtro kriterijus.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-160">If you aren't satisfied with the results of the initial requirement search, you can change the filter criteria.</span></span> <span data-ttu-id="6c6ad-161">Kairėje pusėje išplėskite skydą **Filtro rodinys**, o tada pažymėkite **Ieškoti**, kad rastumėte papildomų išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-161">Expand the **Filter View** pane on the left, and then select **Search** to find additional resources.</span></span>

    ![Filtro rodinio skydas](media/Resource-Management-image16.png)

7. <span data-ttu-id="6c6ad-163">Norėdami pakeisti rezultatų rikiavimą, pažymėkite **Rūšiuoti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-163">To change how the results are sorted, select **Sort**.</span></span>

    ![Rikiavimo komanda](media/Resource-Management-image17.png)

8. <span data-ttu-id="6c6ad-165">Pasirinkite išteklius pagal reikalavime nurodytą poreikį, kaip nurodyta tinklelio viršuje.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-165">Select resources according to the demand that is specified on the requirement, as indicated at the top of the grid.</span></span> <span data-ttu-id="6c6ad-166">Galite išvalyti tinklelio langelių žymėjimą ir palikti tą išteklių pajėgumą atvirą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-166">You can clear the selection of cells in the grid and leave that resource capacity open.</span></span> <span data-ttu-id="6c6ad-167">Vienu metu tik vieną išteklių galima pažymėti kaip rezervuotą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-167">Only one resource at a time can be selected as booked.</span></span>

9. <span data-ttu-id="6c6ad-168">Pasirinkite **Rezervuoti**, kad rezervuotumėte pažymėtą išteklių ir palikite grafiko lentą atvirą, kad galėtumėte pažymėti papildomus išteklius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-168">Select **Book** to book the selected resource and leave the Schedule Board open, so that you can select additional resources.</span></span> <span data-ttu-id="6c6ad-169">Arba pažymėkite **Rezervuoti ir išeiti**, kad rezervuotumėte pasirinktą išteklių ir uždarytumėte grafiko lentą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-169">Alternatively, select **Book & Exit** to book the selected resource and close the Schedule Board.</span></span>

    ![Ištekliai, skirti rezervavimui](media/Resource-Management-image19.png)

    <span data-ttu-id="6c6ad-171">Gaunate pranešimą apie rezervuotas valandas.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-171">You receive a notification about booked hours.</span></span> <span data-ttu-id="6c6ad-172">Poreikio rodikliai rodo kiek rezervavimo reikalavimas yra tenkinamas ir kiek lieka.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-172">The demand indicators show how much the booking requirement is satisfied and how much remains.</span></span> <span data-ttu-id="6c6ad-173">Taip pat galite matyti, kiek suvartojama pasirinkto ištekliaus pajėgumo.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-173">You can also see how much of the selected resource's capacity is consumed.</span></span> <span data-ttu-id="6c6ad-174">Pasirinkite **Išplėsti**, kad peržiūrėtumėte daugiau informacijos apie išteklių rezervavimus.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-174">Select **Expand** to view more details about resource bookings.</span></span>

9. <span data-ttu-id="6c6ad-175">Grįžkite į rodinį **Visi komandos nariai**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-175">Return to the **All Team Members** view.</span></span> <span data-ttu-id="6c6ad-176">Atkreipkite dėmesį, kad tinklelyje bendrasis išteklius pakeistas į įvardytąjį išteklių, o 40 valandos įvardytos kaip rezervuotos tam ištekliui.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-176">In the grid, notice that the generic resource has been replaced by the named resource, and 40 hours are listed as booked for that resource.</span></span>

    ![Atnaujintas visų komandos narių tinklelis](media/Resource-Management-image20.png)

    > [!NOTE]
    > <span data-ttu-id="6c6ad-178">Nerodomos paskirtos valandos, nes jos buvo rezervuotos tiesiogiai komandoje.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-178">No assigned hours are shown, because they were booked directly on the team.</span></span> <span data-ttu-id="6c6ad-179">Jos nebuvo rezervuotos naudojant užduočių priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-179">They weren't booked by using task assignment.</span></span>

## <a name="assign-generic-resources-to-tasks-and-generate-resource-requirements"></a><span data-ttu-id="6c6ad-180">Bendrųjų išteklių priskyrimas užduotims atlikti ir išteklių reikalavimams generuoti</span><span class="sxs-lookup"><span data-stu-id="6c6ad-180">Assign generic resources to tasks and generate resource requirements</span></span>

<span data-ttu-id="6c6ad-181">Programoje PSA galite kurti užduotis, o tada joms priskirti bendruosius išteklius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-181">In PSA, you can create tasks and then assign generic resources to them.</span></span> <span data-ttu-id="6c6ad-182">Tokiu būdu išteklių poreikį gali pavaizduoti vietos rezervavimo ženklai, kol įvertinate savo grafiką ir finansinius skaičius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-182">In this way, resource demand can be represented by placeholders while you estimate your schedule and financial numbers.</span></span> <span data-ttu-id="6c6ad-183">Tada galite generuoti išteklių reikalavimus, skirtus bendriesiems ištekliams ir juos vykdyti.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-183">You can then generate resource requirements for the generic resources and fulfill them.</span></span>

1. <span data-ttu-id="6c6ad-184">Puslapio **Projektai** skirtuke **Grafikas** pasirinkite **Įtraukti**, kad sukurtumėte užduotį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-184">On the **Projects** page, on the **Schedule** tab, select **Add** to create a task.</span></span>

    ![Kurti naują užduotį](media/Resource-Management-image21.png)

2. <span data-ttu-id="6c6ad-186">Lauke **Ištekliai** pažymėkite simbolį **Išteklių parinkiklis**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-186">In the **Resources** field, select the **Resource Picker** symbol.</span></span> <span data-ttu-id="6c6ad-187">Atsiras išteklių parinkiklis ir bus rodomi esami projekto komandos nariai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-187">The Resource Picker appears and shows existing team members for the project.</span></span>

    ![Išteklių parinkiklis](media/Resource-Management-image22.png)

3. <span data-ttu-id="6c6ad-189">Įveskite naujo bendrojo ištekliaus pavadinimą, o tada pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-189">Enter the name of the new generic resource, and then select **Create**.</span></span>

    ![Įvesti naujo bendrojo ištekliaus pavadinimą](media/Resource-Management-image23.png)

4. <span data-ttu-id="6c6ad-191">Dialogo lange **Spartusis kūrimas: projekto komandos narys**, esančiame lauke **Vaidmuo**, pažymėkite bendrajam ištekliui skirtą vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-191">In the **Quick Create: Project Team Member** dialog box that appears, in the **Role** field, select the role for the generic resource.</span></span> <span data-ttu-id="6c6ad-192">Lauke **Išteklių paskirstymo vienetas** pažymėkite bendrajam ištekliui skirtą organizacijos vienetą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-192">In the **Resourcing Unit** field, select the organizational unit for the generic resource.</span></span> <span data-ttu-id="6c6ad-193">Tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-193">Then select **Save**.</span></span>

    ![Spartusis kūrimas: projekto komandos nario dialogo langas](media/Resource-Management-image24.png)

    <span data-ttu-id="6c6ad-195">Dabar užduotis priskirta bendrajam komandos nariui.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-195">The generic team member is now assigned to the task.</span></span>

    ![Bendrojo komandos natio priskyrimas užduočiai](media/Resource-Management-image25.png)

    <span data-ttu-id="6c6ad-197">Skirtuke **Komanda** matysite naują bendrąjį komandos narį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-197">On the **Team** tab, you will see the new generic team member.</span></span> <span data-ttu-id="6c6ad-198">Atkreipkite dėmesį, kad jam priskirtos tik valandos.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-198">Notice that it has only assigned hours.</span></span> <span data-ttu-id="6c6ad-199">Šios valandos yra visų užduočių, priskirtų bendrajam komandos nariui, suma.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-199">These hours are the sum of all tasks that are assigned to the generic team member.</span></span> <span data-ttu-id="6c6ad-200">Bendrasis komandos narys dar neturi reikiamų valandų arba ištekliaus reikalavimo.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-200">The generic team member doesn't yet have required hours or a resource requirement.</span></span>

    ![Bendrasis komandos narys skirtuke „Komanda“](media/Resource-Management-image26.png)

5. <span data-ttu-id="6c6ad-202">Dabar galite priskirti bendrąjį komandos narį kitoms užduotims naudodami išteklių parinkiklį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-202">You can now assign the generic team member to other tasks by using the Resource Picker.</span></span>

    ![Bendrasis komandos narys išteklių parinkiklyje](media/Resource-Management-image27.png)

    <span data-ttu-id="6c6ad-204">Baigę priskirti bendrąjį išteklių užduotims, galite generuoti bendrajam ištekliui skirtą išteklio reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-204">When you've finished assigning the generic resource to tasks, you can generate a resource requirement for the generic resource.</span></span>

5. <span data-ttu-id="6c6ad-205">Skirtuke **Komanda** pasirinkite bendrąjį išteklių, o tada pasirinkite **Generuoti reikalavimą**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-205">On the **Team** tab, select the generic resource, and then select **Generate Requirement**.</span></span>

    ![Komanda „Generuoti reikalavimą“](media/Resource-Management-image28.png)

    <span data-ttu-id="6c6ad-207">Sugeneravus reikalavimą, bendrasis komandos narys turės reikiamas valandas ir nuorodą į ištekliaus reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-207">When the requirement is generated, the generic team member will have required hours and a link for the resource requirement.</span></span>

    ![Ištekliaus reikalavimo nuoroda](media/Resource-Management-image29.png)

    <span data-ttu-id="6c6ad-209">Rezervavus įvardytąjį išteklių, bendrasis išteklius pašalinamas iš komandos ir pakeičiamas įvardytuoju ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-209">After you book a named resource, the generic resource is removed from the team and replaced by the named resource.</span></span>

    ![Bendrojo ištekliaus keitimas įvardytuoju ištekliumi](media/Resource-Management-image30.png)

    <span data-ttu-id="6c6ad-211">Skirtuke **Grafikas** bendrojo ištekliaus užduotys pašalinamos ir pakeičiamos įvardytuoju ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-211">On the **Schedule** tab, the generic resource assignments are removed and replaced by the named resource.</span></span>

    ![Bendrojo ištekliaus užduočių keitimas įvardytuoju ištekliumi grafiko skirtuke](media/Resource-Management-image31.png)

    > [!NOTE]
    > <span data-ttu-id="6c6ad-213">Taip nutinka tik tada, kai nurodytas įvardytasis išteklius yra visiškai rezervuotas bendrojo ištekliaus reikalavimui.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-213">This behavior occurs only when a named resource is fully booked for the generic resource requirement.</span></span> <span data-ttu-id="6c6ad-214">Kai įvardytasis išteklius iš dalies pakeičia bendrojo ištekliaus reikalavimą arba kai keli įvardytieji ištekliai pakeičia bendrojo ištekliaus reikalavimą, bendrasis išteklius išlieka priskirtas užduočiai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-214">When either a named resource partially replaces the generic resource requirement or multiple named resources replace the generic resource requirement, the generic resource remains assigned to the task.</span></span>

    <span data-ttu-id="6c6ad-215">Šioje iliustracijoje pateikiama 80 valandų užduotis planuojama penkioms dienoms (16 valandų per dieną per penkias dienas) ir yra priskirta bendrajam ištekliui, kurio pavadinimas yra **Funkcinis**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-215">In the following illustration, an 80-hour task has been planned for a five-day duration (16 hours per day over five days) and assigned to the generic resource that is named **Functional**.</span></span>

    ![80 valandų, penkių dienų užduotis, priskirta funkciniam bendrajam ištekliui](media/Resource-Management-image32.png)

    <span data-ttu-id="6c6ad-217">Kai generuojate reikalavimą, jis skirtas 80 valandų penkioms dienoms.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-217">When you generate the requirement, it's for 80 hours over five days.</span></span>

    ![Reikalavimas, sugeneruotas 80 valandų per penkias dienas](media/Resource-Management-image33.png)

    <span data-ttu-id="6c6ad-219">Kadangi prieinami ištekliai veikia tik aštuonias valandas per dieną, reikalavimui įvykdyti reikia dviejų išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-219">Because available resources work only eight hours per day, two resources are needed to fulfill the requirement.</span></span>

    ![Antras išteklius](media/Resource-Management-image35.png)

    <span data-ttu-id="6c6ad-221">Skirtuke **Komanda** dabar galite matyti, kad bendrasis išteklius neturi reikiamų valandų, tačiau priskirtos valandos vis tiek rodomos kartu su dviem įvardytaisiais ištekliais, kurie įtraukti į vykdymą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-221">On the **Team** tab, you can now see that the generic resource has no required hours, but the assigned hours still appear together with the two named resources that make up the fulfillment.</span></span>

    ![Du įvardytieji ištekliai komandos skirtuke](media/Resource-Management-image36.png)

    <span data-ttu-id="6c6ad-223">Skirtuke **Grafikas** bendrasis išteklius lieka priskirtas užduočiai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-223">On the **Schedule** tab, the generic resource remains assigned to the task.</span></span>

    ![Bendrieji ištekliai grafiko skirtuke](media/Resource-Management-image37.png)

<span data-ttu-id="6c6ad-225">PSA nepriskiria abiejų išteklių užduočiai, nes tai lemtų mažiau nuspėjamą grafiką.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-225">PSA doesn't assign both resources to the task, because that behavior would produce a less predictable schedule.</span></span> <span data-ttu-id="6c6ad-226">Šiame paprastame pavyzdyje nesunku po lygiai padalinti valandas tarp dviejų išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-226">In this simple example, it's easy to divide the hours equally between two resources.</span></span> <span data-ttu-id="6c6ad-227">Tačiau sudėtingesniais atvejais, į kuriuos įeina kelios užduotys ar keli ištekliai, PSA turėtų daryti prielaidas apie tai, kaip reikėtų paskirstyti rezervavimus, kurie gaunami keliems ištekliams keliose užduotyse.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-227">However, in more complex scenarios that involve multiple tasks and multiple resources, PSA would have to make assumptions about how it should allocate the bookings that are received for multiple resources across multiple tasks.</span></span>

<span data-ttu-id="6c6ad-228">Todėl šiais atvejais projektų vadovas yra atsakingas už kelių rezervavimų analizavimą ir jų priskyrimą pagal poreikį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-228">Therefore, in these scenarios, the project manager is responsible for parsing the multiple bookings and assigning them as needed.</span></span> <span data-ttu-id="6c6ad-229">Norėdamas priskirti rezervavimus, projektų vadovas priskiria užduotis iš bendrųjų išteklių įvardytiems ištekliams, o tada naudoja rodinį **Derinimas**, kad įsitikintų, jog paskirstymas veikia su rezervavimais.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-229">To allocate the bookings, the project manager assigns the tasks from the generic resources to the named resources and then uses the **Reconciliation** view to make sure that the allocation works with the bookings.</span></span>

### <a name="edit-a-resource-requirement"></a><span data-ttu-id="6c6ad-230">Redaguoti ištekliaus reikalavimą</span><span class="sxs-lookup"><span data-stu-id="6c6ad-230">Edit a resource requirement</span></span>

<span data-ttu-id="6c6ad-231">Sukūręs ištekliaus reikalavimą, projektų vadovas arba išteklių vadovas gali norėti redaguoti išsamią informaciją, kad patikslintų ieškos kriterijus, kai naudojama grafiko lenta.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-231">After a resource requirement has been created, a project manager or resource manager might want to edit the details to refine the search criteria when the Schedule Board is used.</span></span> <span data-ttu-id="6c6ad-232">Norėdami redaguoti išteklių reikalavimą, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-232">To edit the resource requirement, follow these steps.</span></span>

1. <span data-ttu-id="6c6ad-233">Puslapio **Projektai** skirtuke **Komanda** pasirinkite nuorodą bet kuriam reikalavimui, esančiam bendrajame ištekliuje.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-233">On the **Projects** page, on the **Team** tab, select the link to any requirement on a generic resource.</span></span>
2. <span data-ttu-id="6c6ad-234">Pasirodžiusiame puslapyje **Ištekliaus reikalavimas** galite atnaujinti kelis atributus.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-234">On the **Resource Requirement** page that appears, you can update several attributes.</span></span> <span data-ttu-id="6c6ad-235">Štai keli pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-235">Here are some examples:</span></span>

    - <span data-ttu-id="6c6ad-236">Pavadinimas</span><span class="sxs-lookup"><span data-stu-id="6c6ad-236">Name</span></span>
    - <span data-ttu-id="6c6ad-237">Pradžios data</span><span class="sxs-lookup"><span data-stu-id="6c6ad-237">From Date</span></span>
    - <span data-ttu-id="6c6ad-238">Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="6c6ad-238">To Date</span></span>
    - <span data-ttu-id="6c6ad-239">Trukmė</span><span class="sxs-lookup"><span data-stu-id="6c6ad-239">Duration</span></span>
    - <span data-ttu-id="6c6ad-240">Išteklių tipas</span><span class="sxs-lookup"><span data-stu-id="6c6ad-240">Resource Type</span></span>

<span data-ttu-id="6c6ad-241">Puslapyje **Ištekliaus reikalavimas** projektų vadovas arba išteklių vadovas taip pat gali apibrėžti šią informaciją:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-241">On the **Resource Requirement** page, the project manager or resource manager can also define the following information:</span></span>

- <span data-ttu-id="6c6ad-242">Įgūdžiai</span><span class="sxs-lookup"><span data-stu-id="6c6ad-242">Skills</span></span>
- <span data-ttu-id="6c6ad-243">Vaidmenys</span><span class="sxs-lookup"><span data-stu-id="6c6ad-243">Roles</span></span>
- <span data-ttu-id="6c6ad-244">Ištekliaus nuostatos</span><span class="sxs-lookup"><span data-stu-id="6c6ad-244">Resource preferences</span></span>
- <span data-ttu-id="6c6ad-245">Pageidaujamas organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="6c6ad-245">Preferred organizational unit</span></span>

### <a name="update-resource-bookings-after-they-are-booked-on-a-project"></a><span data-ttu-id="6c6ad-246">Atnaujinti išteklių rezervavimus po to, kai jie užrezervuoti projekte</span><span class="sxs-lookup"><span data-stu-id="6c6ad-246">Update resource bookings after they are booked on a project</span></span>

<span data-ttu-id="6c6ad-247">Įtraukę bendrąjį arba įvardytąjį išteklių į projekto komandą, galite pakeisti ištekliaus rezervavimus.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-247">After you've added a generic or named resource to a project team, you can change the resource's bookings.</span></span>

1. <span data-ttu-id="6c6ad-248">Puslapio **Projektai** skirtuke **Komanda** pasirinkite komandos narį, o tada pažymėkite **Išlaikyti rezervavimus**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-248">On the **Projects** page, on the **Team** tab, select a team member, and then select **Maintain Bookings**.</span></span>

    ![Grafiko lentos atidarymas pasirinktam komandos nariui](media/Resource-Management-image40.png)

    <span data-ttu-id="6c6ad-250">Atsiranda grafiko lenta ir rodomi projekto komandos nario rezervavimai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-250">The Schedule Board appears and shows the project team member's bookings.</span></span> <span data-ttu-id="6c6ad-251">Išplėskite komandos nario įrašą, kad peržiūrėtumėte valandas, užrezervuotas pagal šį projektą, ir kitus projektus, naudojančius komandos nario pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-251">Expand the team member's record to view the hours that have been booked against this project and other projects that are consuming the team member's capacity.</span></span>

2. <span data-ttu-id="6c6ad-252">Pažymėkite ir tempkite rezervavimą, kad jį išplėstumėte arba sumažintumėte.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-252">Select and drag the booking to extend or shorten it.</span></span> <span data-ttu-id="6c6ad-253">Atsiras dialogo langas **Kurti ištekliaus rezervavimą**, kuris leidžia koreguoti rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-253">A **Create Resource Booking** dialog box appears that lets you adjust the booking.</span></span>

    ![Dialogo langas „Kurti išteklių rezervavimą“](media/Resource-Management-image41.png)

3. <span data-ttu-id="6c6ad-255">Dešiniuoju pelės klavišu spustelėkite rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-255">Right-click the booking.</span></span> <span data-ttu-id="6c6ad-256">Tada galite naudoti santrumpų meniu, kad užbaigtumėte šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-256">You can then use the shortcut menu to complete the following actions:</span></span>

    - <span data-ttu-id="6c6ad-257">Keisti rezervavimo būseną.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-257">Change the booking status.</span></span>
    - <span data-ttu-id="6c6ad-258">Redaguoti rezervavimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-258">Edit the booking.</span></span>
    - <span data-ttu-id="6c6ad-259">Pakeisti projekto komandos išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-259">Substitute a resource on the project team.</span></span>

### <a name="change-the-booking-status"></a><span data-ttu-id="6c6ad-260">Pakeisti rezervavimo būseną.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-260">Change the booking status</span></span>

<span data-ttu-id="6c6ad-261">Galite keisti bet kurią numatytąją arba pasirinktinę rezervavimo būseną.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-261">You can change any default or custom booking status.</span></span>

![Komanda „Keisti būseną“](media/Resource-Management-image42.png)

<span data-ttu-id="6c6ad-263">Į PSA įtrauktos šios būsenos:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-263">The following statuses are included in PSA:</span></span>

- <span data-ttu-id="6c6ad-264">**Atšaukta** – ši būsena atšaukia ištekliaus rezervavimą ir atlaisvina ištekliaus pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-264">**Canceled** – This status cancels a resource's booking and frees up the resource's capacity.</span></span>
- <span data-ttu-id="6c6ad-265">**Rezervuoti galutinai** – ši būsena sunaudoja ištekliaus pajėgumą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-265">**Hard Book** – This status consumes a resource's capacity.</span></span> <span data-ttu-id="6c6ad-266">Paprastai rezervavimas turi šią būseną, kai atidarote parinktį **Išlaikyti rezervavimus** tinklelyje **Visi komandos nariai** puslapyje **Projektai**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-266">A booking typically has this status when you open **Maintain Bookings** from the **All Team Members** grid on the **Projects** page.</span></span>
- <span data-ttu-id="6c6ad-267">**Rezervuoti preliminariai** – ši būsena įtraukia išteklių į komandą, tačiau nenaudoja ištekliaus pajėgumo.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-267">**Soft Book** – This status adds a resource to a team but doesn't consume the resource's capacity.</span></span> <span data-ttu-id="6c6ad-268">Ši būsena nurodo, kad išteklius buvo rezervuotas galimam darbui, bet vis tiek turi pajėgumo, jei jo reikia kitoms užduotims.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-268">It indicates that the resource has been reserved for potential work but still has capacity if it's needed on other jobs.</span></span> <span data-ttu-id="6c6ad-269">Peržiūrėjus bendro ištekliaus pasiekiamumą, preliminarūs rezervavimai turi skirtingą būseną nei galutiniai rezervavimai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-269">In the view of overall resource availability, soft bookings have a different status than hard bookings.</span></span>
- <span data-ttu-id="6c6ad-270">**Siūloma** – ši būsena rodo išteklių vadovo arba projekto vadovo pasiūlymą ištekliui.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-270">**Proposed** – This status represents a resource manager's or project manager's proposal for a resource.</span></span> <span data-ttu-id="6c6ad-271">Pasiūlymai nenaudoja ištekliaus pajėgumo, o išteklius neįtraukiamas į projekto komandą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-271">Proposals don't consume the capacity of a resource, and the resource isn't added to the project team.</span></span> <span data-ttu-id="6c6ad-272">Norėdami galutinai rezervuoti išteklių komandoje, projekto vadomas turi priimti pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-272">To hard-book the resource on the team, the project manager must accept the proposal.</span></span>

### <a name="submit-resource-requests"></a><span data-ttu-id="6c6ad-273">Išteklių užklausų teikimas</span><span class="sxs-lookup"><span data-stu-id="6c6ad-273">Submit resource requests</span></span>

<span data-ttu-id="6c6ad-274">Išteklių užklausos naudojamos poreikiui, kurį turi įvykdyti išteklių vadovas, vykdyti (ištekliaus reikalavimas).</span><span class="sxs-lookup"><span data-stu-id="6c6ad-274">Resource requests are used to carry the demand (resource requirement) that must be fulfilled by a resource manager.</span></span> <span data-ttu-id="6c6ad-275">Jei tai bendras išteklius, kuris jau yra komandoje, galite ištekliaus užklausą galite pateikti tiesiogiai.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-275">For a generic resource that is already on the team, you can submit a resource request directly.</span></span> <span data-ttu-id="6c6ad-276">Ištekliaus užklausą galima įvykdyti dviem būdais:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-276">A resource request can be fulfilled in two ways:</span></span>

- <span data-ttu-id="6c6ad-277">Išteklių vadovas tiesiogiai įvykdo užklausą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-277">The resource manager directly fulfills the request.</span></span> <span data-ttu-id="6c6ad-278">Šiuo atveju bendrasis išteklius pakeičiamas galutiniu rezervavimu, į kurį įeina įvardytasis išteklius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-278">In this case, the generic resource is replaced by a hard booking that has a named resource.</span></span>
- <span data-ttu-id="6c6ad-279">Išteklių vadovas siūlo išteklių projektų vadovui, o projektų vadovas patvirtina arba atmeta siūlomą išteklių.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-279">The resource manager proposes a resource to the project manager, and the project manager approves or rejects the proposed resource.</span></span>

#### <a name="direct-fulfillment-of-resource-requests"></a><span data-ttu-id="6c6ad-280">Tiesioginis išteklių prašymų vykdymas</span><span class="sxs-lookup"><span data-stu-id="6c6ad-280">Direct fulfillment of resource requests</span></span>

<span data-ttu-id="6c6ad-281">Sugeneravus išteklių reikalavimą, projektų vadovas gali pateikti ištekliaus užklausą bendriesiems ištekliams, pažymėdamas išteklių, o tada pasirinkdamas **Pateikti užklausą**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-281">When a resource requirement is generated, a project manager can submit a resource request for a generic resource by selecting the resource and then selecting **Submit Request**.</span></span>

![Pateikti užklausą](media/Resource-Management-image45.png)

<span data-ttu-id="6c6ad-283">Pastabas apie išteklius galima pateikti išteklių vadovui, kuris vykdo užklausą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-283">Comments about the resource can be provided to the resource manager who is fulfilling the request.</span></span> <span data-ttu-id="6c6ad-284">Pateikus prašymą, komandos nariui skirtas laukas **Būsena** pakeičiamas į **Pateikta**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-284">After the request is submitted, the **Status** field for the team member is changed to **Submitted**.</span></span>

![Įvesti pasirinktinius komentarus](media/Resource-Management-image46.png)

<span data-ttu-id="6c6ad-286">Projektų vadovui įvykdžius užklausą, bendrasis komandos narys pakeičiamas įvardytuoju ištekliumi tinklelyje **Visi komandos nariai**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-286">When the resource manager fulfills the request, the generic team member is replaced by the named resource in the **All Team Members** grid.</span></span>

![Bendrojo komandos nario keitimas įvardytuoju ištekliumi tinklelyje „Visi komandos nariai“](media/Resource-Management-image47.png)

#### <a name="use-a-resource-proposal-for-resource-requests"></a><span data-ttu-id="6c6ad-288">Išteklių pasiūlymas išteklių užklausoms</span><span class="sxs-lookup"><span data-stu-id="6c6ad-288">Use a resource proposal for resource requests</span></span>

<span data-ttu-id="6c6ad-289">Užuot tiesiogiai rezervuodamas išteklius išteklių užklausoje, išteklių vadovas gali siūlyti išteklių projektų vadovui.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-289">Instead of directly booking a resource on a resource request, a resource manager can propose a resource to the project manager.</span></span> <span data-ttu-id="6c6ad-290">Išteklių vadovas gali naudoti šią parinktį, kai nėra tikslaus reikalavimų atitikimo.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-290">A resource manager might use this option when an exact match for the requirements isn't available.</span></span> <span data-ttu-id="6c6ad-291">Išteklių vadovui pasiūlius išteklių, projektų vadovas mato, kad bendrajam komandos nariui skirtas laukas **Būsena** pakeičiamas į **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-291">When a resource manager proposes a resource, the project manager sees that the **Status** field for the generic team member is changed to **Needs Review**.</span></span>

![Bendrosios komandos nario būsenos pasikeitimas į „Reikia peržiūrėti“](media/Resource-Management-image48.png)

<span data-ttu-id="6c6ad-293">Norėdami peržiūrėti siūlomą išteklių ir pasiūlymo rezervavimo efekto vizualizavimą, dukart spustelėkite komandos narį, kurio būsena yra **Reikia peržiūrėti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-293">To view the proposed resource together with a visualization of the effect of the proposal's booking, double-click the team member that has a status of **Needs Review**.</span></span> <span data-ttu-id="6c6ad-294">Tada pasirinkite skirtuką **Siūlomi ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-294">Then select the **Proposed Resources** tab.</span></span>

![Siūlomi ištekliai](media/Resource-Management-image49.png)

<span data-ttu-id="6c6ad-296">Pasirinkite **Priimti visus pasiūlymus**, kad priimtumėte visus siūlomus išteklius arba **Atmesti visus pasiūlymus**, kad juos atmestumėte.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-296">Select **Accept All Proposals** to accept all proposed resources or **Reject All Proposals** to reject them.</span></span> <span data-ttu-id="6c6ad-297">Jei priimate siūlomus išteklius, jie yra galutinai rezervuojami projekte kaip komandos nariai ir pakeičia bendruosius išteklius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-297">If you accept the proposed resources, they are hard-booked on the project as team members and replace the generic resources.</span></span>

> [!NOTE]
> <span data-ttu-id="6c6ad-298">Turite priimti arba atmesti visus siūlomus išteklius.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-298">You must either accept or reject all proposed resources.</span></span> <span data-ttu-id="6c6ad-299">Negalite jų priimti arba atmesti iš dalies.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-299">You can't partially accept or reject them.</span></span>

### <a name="substitute-a-resource-on-the-project-team"></a><span data-ttu-id="6c6ad-300">Pakeiskite išteklių projekto komandoje</span><span class="sxs-lookup"><span data-stu-id="6c6ad-300">Substitute a resource on the project team</span></span>

<span data-ttu-id="6c6ad-301">Kartais projekto vadovas projekte turi pakeisti rezervuotos komandos narį.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-301">Sometimes, a project manager must substitute a booked team member on a project.</span></span>

1. <span data-ttu-id="6c6ad-302">Puslapio **Projektai** skirtuke **Komanda** pažymėkite išteklių, kurį reikia pakeisti, o tada pasirinkite **Išlaikyti rezervavimus**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-302">On the **Projects** page, on the **Team** tab, select the resource that needs a substitute, and then select **Maintain Bookings**.</span></span>
2. <span data-ttu-id="6c6ad-303">Išplėskite išteklių, kad peržiūrėtumėte projektus, kuriems jis priskirtas.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-303">Expand the resource to view the projects that it's assigned to.</span></span>

    ![Išplėstas išteklius priskirtiems projektams rodyti](media/Resource-Management-image50.png)

3. <span data-ttu-id="6c6ad-305">Dešiniuoju pelės mygtuku spustelėkite projektą, o tada pažymėkite **Pakeisti išteklius**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-305">Right-click the project, and then select **Substitute Resource**.</span></span>
4. <span data-ttu-id="6c6ad-306">Jei žinote išteklių, kurį norite pakeisti dabartiniu ištekliumi, pažymėkite arba įveskite pavadinimą, o tada pasirinkite **Iš naujo priskirti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-306">If you know the resource that you want to substitute for the current resource, select or type the name, and then select **Re-assign**.</span></span>

    ![Pakaitinio ištekliaus nurodymas](media/Resource-Management-image51.png)

    <span data-ttu-id="6c6ad-308">Taip pat galite atlikti šiuos veiksmus, kad ieškotumėte ištekliaus:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-308">Alternatively, follow these steps to search for a resource:</span></span>

    1. <span data-ttu-id="6c6ad-309">Pažymėkite **Rasti pakaitalą**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-309">Select **Find Substitution**.</span></span>

        ![Pakaitinio ištekliaus paieška](media/Resource-Management-image52.png)

        <span data-ttu-id="6c6ad-311">Planavimo pagalbinė priemonė pateikia galimų pakaitų sąrašą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-311">The Schedule Assistant returns a list of available substitutes.</span></span> <span data-ttu-id="6c6ad-312">Planavimo pagalbinėje priemonėje galite toliau filtruoti galimus išteklius, kad rastumėte tinkamą pakaitą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-312">In the Schedule Assistant, you can further filter the available resources to find a suitable substitute.</span></span>

        ![Galimų pakaitų sąrašas](media/Resource-Management-image53.png)

    2. <span data-ttu-id="6c6ad-314">Norėdami pakeisti išteklių, pasirinkite norimą išteklių ir pažymėkite **Pakeisti**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-314">To substitute the resource, select the resource that you want, and then select **Substitute**.</span></span>

        ![Pakeisti pasirinktus išteklius](media/Resource-Management-image54.png)

    <span data-ttu-id="6c6ad-316">Rezervavimai ir priskyrimai pakeičiami naujais ištekliais.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-316">The bookings and assignments are substituted with the new resource.</span></span>

    ![Rezervavimų ir priskyrimų keitimas naujais ištekliais](media/Resource-Management-image55.png)

## <a name="reconcile-team-member-bookings-and-assignments"></a><span data-ttu-id="6c6ad-318">Komandos narių rezervavimų ir priskyrimų derinimas</span><span class="sxs-lookup"><span data-stu-id="6c6ad-318">Reconcile team member bookings and assignments</span></span>

<span data-ttu-id="6c6ad-319">Komandos nariams rezervavimai ir priskyrimai yra laisvai susiję.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-319">For team members, bookings and assignments are loosely coupled.</span></span> <span data-ttu-id="6c6ad-320">Kitaip tariant, ištekliai gali turėti priskyrimų, bet ne rezervavimų, arba jie gali turėti rezervavimų, bet ne priskyrimų.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-320">In other words, resources can have assignments but no bookings, or they can have bookings but no assignments.</span></span> <span data-ttu-id="6c6ad-321">Geriausiu atveju rezervavimai ir priskyrimai turėtų būti suderinti, kad ištekliai turėtų patvirtintą pajėgumą užduočių priskyrimams atlikti.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-321">Ideally, bookings and assignments should be aligned, so that resources have committed capacity to perform the task assignments.</span></span> <span data-ttu-id="6c6ad-322">Tačiau rezervavimai gali būti pagrįsti prieinamumu, o užduoties laikas gali keistis projektui tęsiantis.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-322">However, the bookings might be based on availability, and task timings might change as the project continues.</span></span> <span data-ttu-id="6c6ad-323">Todėl laisvas rezervavimų ir priskyrimų siejimas suteikia lankstumą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-323">Therefore, the loose coupling of bookings and assignments provides flexibility.</span></span>

<span data-ttu-id="6c6ad-324">PSA turi skirtuką **Derinimas**, kuris leidžia projektų vadovams derinti komandos narių rezervavimus ir priskyrimus projekto komandoms.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-324">PSA has a **Reconciliation** tab that lets project managers reconcile team members' bookings and their assignments for project teams.</span></span>

![Derinimas](media/Resource-Management-image56.png)

<span data-ttu-id="6c6ad-326">Skirtuke **Derinimas** rodomi rezervavimai ir priskyrimai iki atskiro kiekvieno komandos nario užduoties priskyrimo lygio.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-326">The **Reconciliation** tab shows bookings and assignments down to the level of the individual task assignment for each team member.</span></span> <span data-ttu-id="6c6ad-327">Skirtuke rodomos langeliuose nurodytos valandos, kurios nurodo laikotarpius nuo mėnesių iki dienų.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-327">It shows hours in cells that represent time periods from months down to days.</span></span>

<span data-ttu-id="6c6ad-328">Skirtuke taip pat rodoma bendra grynoji projekto suma kartu su stulpeliu „Iš viso“.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-328">The tab also shows an overall net total for the project, together with a total column.</span></span>

<span data-ttu-id="6c6ad-329">Kiekvienam ištekliui skirtukas apskaičiuoja skirtumą tarp komandos narių rezervavimų ir komandos nario užduočių priskyrimo apibendrinamosios reikšmės.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-329">For each resource, the tab calculates the difference between the team member's bookings and a rollup of the team member's task assignments.</span></span> <span data-ttu-id="6c6ad-330">Geriausiu atveju šis skirtumas turi būti 0 (nulis).</span><span class="sxs-lookup"><span data-stu-id="6c6ad-330">Ideally, this difference should be 0 (zero).</span></span> <span data-ttu-id="6c6ad-331">Kitaip tariant, tarp rezervavimų ir priskyrimų neturėtų būti skirtumo.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-331">In other words, there should be no difference between bookings and assignments.</span></span> <span data-ttu-id="6c6ad-332">Skirtumai nuspalvinami ir nušešėliuojami, kad atkreiptų dėmesį į dvi sąlygas:</span><span class="sxs-lookup"><span data-stu-id="6c6ad-332">Differences are colored and shaded to draw attention to two conditions:</span></span>

- <span data-ttu-id="6c6ad-333">**Rezervavimo trūkumas** – rezervavimo trūkumas atsiranda, kai išteklius turi daugiau priskyrimų nei rezervavimų.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-333">**Booking shortage** – A booking shortage occurs when a resource has more assignments than bookings.</span></span> <span data-ttu-id="6c6ad-334">Kadangi šis pajėgumas nebuvo rezervuotas, projektų vadovas gali pataisyti šią sąlygą išplėsdamas ištekliaus rezervavimus, kad padengtų trūkumą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-334">Because this capacity hasn't been reserved, a project manager might want to correct this condition by extending the resource's bookings to cover the deficit.</span></span>
- <span data-ttu-id="6c6ad-335">**Užsakymų perteklius** – užsakymų perteklius įvyksta, kai ištekliai buvo rezervuoti projektui, tačiau nebuvo priskirti užduotims.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-335">**Excess bookings** – Excess bookings occur when a resource has been booked to the project but hasn't been assigned to tasks.</span></span> <span data-ttu-id="6c6ad-336">Ši sąlyga gali būti priimtina tais atvejais, kai išteklius buvo užrezervuotas projektui prieš užduoties priskyrimą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-336">This condition might be acceptable in the cases where the resource was booked to the project before task assignment occurred.</span></span> <span data-ttu-id="6c6ad-337">Tačiau kitais atvejais išteklius neplanuojamas priskirti užduotims.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-337">However, in other cases, the resource isn't planned to be assigned to tasks.</span></span> <span data-ttu-id="6c6ad-338">Tokiais atvejais projektų vadovas turėtų apsvarstyti išteklių rezervavimo atšaukimą, kad pajėgumą būtų galima naudoti kitam projektui.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-338">In these cases, the project manager should consider canceling the resource's bookings, so that the capacity can be used for another project.</span></span>

<span data-ttu-id="6c6ad-339">Kai kuriais atvejais, peržiūrint laiką aukštesniame nei dienos lygyje (pavyzdžiui, mėnesio lygyje), galite matyti ištekliaus grynąjį nulio skirtumą (kitaip tariant, rezervavimai = priskyrimai).</span><span class="sxs-lookup"><span data-stu-id="6c6ad-339">In some cases, when you view time at a higher level than the day level (for example, the month level), you might see a net difference of zero for a resource (in other words, bookings = assignments).</span></span> <span data-ttu-id="6c6ad-340">Tačiau, jei peržiūrite laiką savaitės lygyje, galite matyti nulio valandų priskyrimus ir 40 valandų rezervavimus pirmoje savaitėje, tačiau 40 valandų priskyrimus ir nulio valandų rezervavimus antroje savaitėje.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-340">However, if you view time at the week level, you might see that there are assignments of zero hours and bookings of 40 hours in the first week, but assignments of 40 hours and bookings of zero hours in the second week.</span></span> <span data-ttu-id="6c6ad-341">Apskritai rezervavimai ir priskyrimai yra suderinami, tačiau kiekvieną savaitę jie skiriasi.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-341">Overall, the bookings and assignments are reconciled, but they differ from one week to the next.</span></span>

<span data-ttu-id="6c6ad-342">Peržiūrint laiką aukštesniuose lygiuose, langeliai, esantys skirtuke **Derinimas**, turi indikatorių, kuris praneša, kad žemesniuose lygiuose yra skirtumų.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-342">When you view time at higher levels, cells in the **Reconciliation** tab have an indicator to inform you that there are differences at lower levels.</span></span> <span data-ttu-id="6c6ad-343">Dukart spustelėję langelį galite priartinti ir peržiūrėti skirtumą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-343">By double-clicking in a cell, you can zoom in to view the difference.</span></span> <span data-ttu-id="6c6ad-344">Tada galite spustelėti dešiniuoju pelės mygtuku ir nutolinti. Pažymėdami išteklių, o tada naudodami valdiklį **Kitas skirtumas**, esantį tinklelio įrankių juostoje, galite eiti į kitą skirtumą tarp šio ištekliaus rezervavimų ir priskyrimų.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-344">You can then right-click to zoom out. By selecting a resource and then using the **Next difference** control on the grid toolbar, you can go to the next difference between bookings and assignments for that resource.</span></span> <span data-ttu-id="6c6ad-345">Tada galite naudoti valdiklį **Ankstesnis skirtumas**, kad grįžtumėte atgal.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-345">You can then use the **Previous difference** control to go back.</span></span> <span data-ttu-id="6c6ad-346">Taip pat galite išjungti skirtumo indikatorių ir naršymą **Parametruose**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-346">You can also turn off the difference indicator and navigation behavior under **Settings**.</span></span>

![Skirtumo indikatorius](media/Resource-Management-image57.png)

<span data-ttu-id="6c6ad-348">Jei turite ištekliaus užduoties priskyrimus, bet ne rezervavimus, puslapio **Projektai** skirtuke **Derinimas** pažymėkite rezervavimo trūkumą, o tada pasirinkite **Išplėsti rezervavimą**.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-348">If you have task assignments for a resource but no bookings, on the **Projects** page, on the **Reconciliation** tab, select the booking shortage, and then select **Extend Booking**.</span></span> <span data-ttu-id="6c6ad-349">Atsiranda dialogo langas **Išplėsti rezervavimą** ir rodomas rezervavimas, reikalingas ištekliaus trūkumui spręsti.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-349">The **Extend Booking** dialog box appears and shows the booking that is needed to address the resource's shortage.</span></span> <span data-ttu-id="6c6ad-350">Jame taip pat nurodomi esami ištekliaus rezervavimai visuose projektuose arba kituose planiniuose objektuose.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-350">It also shows the resource's existing bookings across all projects or other schedulable entities.</span></span> <span data-ttu-id="6c6ad-351">Jei pasirinksite **Gerai**, kad sukurtumėte ištekliaus rezervavimą, neatsižvelgiant į ištekliaus pasiekiamumą, galite viršyti rezervavimo limitą.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-351">If you select **OK** to create the booking for the resource, regardless of that resource's availability, you might cause overbooking.</span></span>

![Dialogo langas „Išplėsti rezervavimą“](media/Resource-Management-image58.png)

<span data-ttu-id="6c6ad-353">Projektų vadovas arba išteklių vadovas gali naudoti grafiko lentą, kad valdytų situacijas, kai išteklius rezervuojamas per daug nepaisant jo pajėgumo.</span><span class="sxs-lookup"><span data-stu-id="6c6ad-353">The project manager or resource manager can then use the Schedule Board to manage any situations where a resource is overbooked beyond its capacity.</span></span>
