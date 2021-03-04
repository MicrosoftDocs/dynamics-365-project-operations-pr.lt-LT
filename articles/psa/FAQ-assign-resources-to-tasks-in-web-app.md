---
title: Kaip, naudojantis „Web App“, užduočiai priskirti rezervuojamus išteklius?
description: Peržiūrėkite, kaip galite priskirti rezervuojamus išteklius.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 27a93c41243f300cadb632c697672180e5a3817b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146583"
---
# <a name="how-do-i-assign-a-bookable-resource-to-a-task-in-the-web-app-project-service-app-v2x"></a><span data-ttu-id="20a20-103">Kaip žiniatinklio programoje užduočiai priskirti rezervuotinus išteklius („Project Service“ programa v2.x)?</span><span class="sxs-lookup"><span data-stu-id="20a20-103">How do I assign a bookable resource to a task in the web app (Project Service app v2.x)?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="20a20-104">Ištekliams priskirti užduotį „Project Service“ programoje galima dviem būdais.</span><span class="sxs-lookup"><span data-stu-id="20a20-104">There are two ways to assign a resource to a task in Project Service.</span></span> <span data-ttu-id="20a20-105">Išteklius galite rezervuoti kaip komandos narys ir tada priskirti juos užduočiai.</span><span class="sxs-lookup"><span data-stu-id="20a20-105">You can book a resource as a team member and then assign it to a task.</span></span> <span data-ttu-id="20a20-106">Arba, naudodami vaidmenų paskyrimą užduotims atlikti, galite sukurti bendrąjį komandos narį ir tada įvykdyti atsarginius reikalavimus su įvardytais ištekliais.</span><span class="sxs-lookup"><span data-stu-id="20a20-106">Or, you can create a generic team member through role assignment on tasks, generate a team, and then fulfill the backing requirements with a named resource.</span></span>

<span data-ttu-id="20a20-107">Atminkite, kad norėdami užduočiai priskirti rezervuotinus išteklius, rezervuotinų išteklių komandos narys privalo turėti pakankamai galimų rezervavimų.</span><span class="sxs-lookup"><span data-stu-id="20a20-107">Note that if you’d like to assign a bookable resource to a task, the bookable resource team member must have enough available bookings.</span></span> <span data-ttu-id="20a20-108">Rezervavimo būsena turi būti „Patvirtinti galutinio rezervavimo tipą“ ir „Būsena patvirtinta“.</span><span class="sxs-lookup"><span data-stu-id="20a20-108">The status of the booking must be Commit Type Hard Book and Status Committed.</span></span> <span data-ttu-id="20a20-109">Jei ištekliams rezervuoti nėra pakankamai rezervavimų, Project Service paskyrimą pašalina ir parodo tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="20a20-109">If there aren’t enough bookings for the resource, Project Service removes the assignment and displays the following error message:</span></span>

<span data-ttu-id="20a20-110">*Užduočiai paskirti išteklių nepavyko – nepakanka toliau nurodytiems ištekliams rezervuotų valandų, susietų su šiuo projektu.*</span><span class="sxs-lookup"><span data-stu-id="20a20-110">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project*</span></span>

## <a name="book-a-resource-as-a-team-member-and-then-assign-the-resource-to-a-task"></a><span data-ttu-id="20a20-111">Išteklių rezervavimas būnant komandos nariu ir išteklio priskyrimas užduočiai</span><span class="sxs-lookup"><span data-stu-id="20a20-111">Book a resource as a team member and then assign the resource to a task</span></span>

<span data-ttu-id="20a20-112">Naudodami šį metodą prie projekto komandos pridedate išteklius ir tada projekto grafike ištekliams priskiriate užduotis.</span><span class="sxs-lookup"><span data-stu-id="20a20-112">With this method you add a resource to the project team and then assign tasks to the resource in the project schedule.</span></span> <span data-ttu-id="20a20-113">Štai kaip galite tai padaryti:</span><span class="sxs-lookup"><span data-stu-id="20a20-113">Here’s how you do this:</span></span>
1.  <span data-ttu-id="20a20-114">Komandos nario tinklelyje pridėkite naują komandos narį, pasirinkę **„Naujas“**.</span><span class="sxs-lookup"><span data-stu-id="20a20-114">On the team member grid, add a new team member by selecting **New**.</span></span>
2.  <span data-ttu-id="20a20-115">Ekrane „Spartusis komandos nario kūrimas“ pasirinkite rezervuotinų išteklių pavadinimą ir nustatykite vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="20a20-115">On the Team Member Quick Create screen, select the bookable resource name and set a role.</span></span>
3.  <span data-ttu-id="20a20-116">Pasirinkite **„Nuo“** ir **„Iki“** datas.</span><span class="sxs-lookup"><span data-stu-id="20a20-116">Select the **From** and **To** dates.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="20a20-117">![Komandos nario įtraukimo ekrano kopija](media/FAQ-Resources-to-Tasks2-1.png "Komandos nario įtraukimo ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="20a20-117">![Screenshot of adding team member](media/FAQ-Resources-to-Tasks2-1.png "Screenshot of adding team member")</span></span>
 
4.  <span data-ttu-id="20a20-118">Pasirinkite vieną iš šių išteklių rezervavimo paskirstymo metodų:</span><span class="sxs-lookup"><span data-stu-id="20a20-118">Select one of the following allocation methods for booking the resource:</span></span>
    - <span data-ttu-id="20a20-119">**Visas pajėgumo metodas** – rezervuojamas visas išteklių pajėgumas tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="20a20-119">**Full Capacity** books the resource’s full capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="20a20-120">**Pajėgumo procentinės dalies rezervavimo metodas** – rezervuojama išteklių pajėgumo dalis procentais tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="20a20-120">**Percentage Capacity** books the resource for a percentage of the resource's capacity for the specified from and to dates.</span></span>
    - <span data-ttu-id="20a20-121">**Tolygiai paskirstomų valandų metodas** – ištekliai rezervuojami nurodytam valandų skaičiui, kiekvienai dienai skirtą laiką tolygiai paskirstant tarp nustatytų pradžios ir pabaigos datų esančiam laikotarpiui</span><span class="sxs-lookup"><span data-stu-id="20a20-121">**By Hours Distribute Evenly** books the resource for a specified number of hours, distributing it evenly per day over the specified from and to dates.</span></span>
    - <span data-ttu-id="20a20-122">**Pirminės apkrovos metodas** – ištekliai rezervuojami į išteklių naudojimo pradžios dieną keliant didžiausią dienos valandų skaičių tarp nurodytų pradžios ir pabaigos datų esančiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="20a20-122">**By Hours Front Load** books the resource for a specified number of hours, front-loading the per-day hours over the specified from and to dates.</span></span>

    <span data-ttu-id="20a20-123">Nesirinkite parinkties **Joks**, nes tuomet ištekliai bus pridėti komandai, bet nebus sukuriami jokie išteklių pajėgumą naudojantys rezervavimai.</span><span class="sxs-lookup"><span data-stu-id="20a20-123">Don’t select **None** because it adds the resource to the team but doesn’t create any bookings that absorb the resource's capacity.</span></span>
5.  <span data-ttu-id="20a20-124">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="20a20-124">Select **Save**.</span></span>

    <span data-ttu-id="20a20-125">Atkreipkite dėmesį, kad turi būti rezervuota pakankamai valandų, kad būtų padengtos pastangų valandos bei datų intervalai, kuriems priskyrėte šiuos išteklius.</span><span class="sxs-lookup"><span data-stu-id="20a20-125">Note that the hours of the booking must be enough to cover the effort hours and date ranges of the tasks that you assign this resource to.</span></span> <span data-ttu-id="20a20-126">Jei tai nebus suderinta, užduočiai priskirti resursų nepavyks.</span><span class="sxs-lookup"><span data-stu-id="20a20-126">If they aren’t in alignment, you can’t assign the resource to the task.</span></span>

6.  <span data-ttu-id="20a20-127">Užduoties darbo paskirstymo struktūroje (WBS), spustelėkite išteklių langelio išplečiamąjį meniu.</span><span class="sxs-lookup"><span data-stu-id="20a20-127">On the work breakdown structure (WBS) for the task, click the resource cell dropdown.</span></span> <span data-ttu-id="20a20-128">Tada:</span><span class="sxs-lookup"><span data-stu-id="20a20-128">Then:</span></span> 

    1. <span data-ttu-id="20a20-129">Pasirinkite **Įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="20a20-129">Select **Add**.</span></span>
    2. <span data-ttu-id="20a20-130">Pasirinkite po parinktimi **„Ištekliai“** esantį išplečiamąjį meniu ir pasirinkite komandos narį, kurį pridėjote aukščiau.</span><span class="sxs-lookup"><span data-stu-id="20a20-130">Select the dropdown under **Resources** and select the team member you added above.</span></span>
    3. <span data-ttu-id="20a20-131">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="20a20-131">Select **OK**.</span></span> <span data-ttu-id="20a20-132">Dabar komandos nariui yra priskirta užduotis.</span><span class="sxs-lookup"><span data-stu-id="20a20-132">The team member is now assigned to the task.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="20a20-133">![Išteklių su WBS įtraukimo ekrano kopija](media/FAQ-Resources-to-Tasks2-2.png "Išteklių su WBS įtraukimo ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="20a20-133">![Screenshot of adding resources with WBS](media/FAQ-Resources-to-Tasks2-2.png "Screenshot of adding resources with WBS")</span></span>
 
<span data-ttu-id="20a20-134">Komandos nario tinklelyje, po parinktimi „Paskirtos valandos“ matysite visas paskirtas valandas.</span><span class="sxs-lookup"><span data-stu-id="20a20-134">On the team member grid, you’ll see the aggregate of the resource’s assigned hours under Assigned Hours.</span></span> <span data-ttu-id="20a20-135">Ši reikšmė bus mažesnė arba lygi rezervuotoms išteklių valandoms.</span><span class="sxs-lookup"><span data-stu-id="20a20-135">It will be less than or equal to the booked hours for the resource.</span></span> 

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20a20-136">![Ištekliams priskirtų valandų ekrano kopija](media/FAQ-Resources-to-Tasks2-3.png "Ištekliams priskirtų valandų ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="20a20-136">![Screenshot of assigned hours for a resource](media/FAQ-Resources-to-Tasks2-3.png "Screenshot of assigned hours for a resource")</span></span>
 
<span data-ttu-id="20a20-137">Ištekliai nebus matomi išplečiamajame meniu, jei užduotis, kurią bandote priskirti ištekliams, prasidės po išteklių rezervavimo pabaigos datos.</span><span class="sxs-lookup"><span data-stu-id="20a20-137">If the task you’re attempting to assign to the resource starts after the end date of the resources bookings, the resource won’t appear in the dropdown.</span></span>

<span data-ttu-id="20a20-138">Atkreipkite dėmesį – jei ištekliuose yra likusių nepriskirtų pajėgumų, ištekliams galite priskirti daugiau valandų nei jų buvo rezervuota.</span><span class="sxs-lookup"><span data-stu-id="20a20-138">Note that you can assign a resource to more hours than their booked hours if the resource has some remaining unassigned capacity.</span></span> <span data-ttu-id="20a20-139">Tokiu atveju rezervavimams ištekliai bus priskirti tik iš dalies.</span><span class="sxs-lookup"><span data-stu-id="20a20-139">In this case the resource will only be partially assigned up to their bookings.</span></span> <span data-ttu-id="20a20-140">Galėsite peržiūrėti likusias nepriskirtas užduoties valandas, jei prie darbo paskirstymo struktūros pridėsite stulpelį „Valandos, kurioms nepriskirtas personalas“.</span><span class="sxs-lookup"><span data-stu-id="20a20-140">You can see these remaining unassigned task hours by adding the Unstaffed Hours column to the work breakdown structure.</span></span>

<span data-ttu-id="20a20-141">Jei ištekliai yra priskirti toms valandoms, kurioms buvo rezervuoti (rezervuotų valandų skaičius lygus paskirtų valandų skaičiui), mėginant juos priskirti kitoms užduotims, pamatysite tokį klaidos pranešimą:</span><span class="sxs-lookup"><span data-stu-id="20a20-141">If resources are assigned to their booked hours (their booked hours equals their assigned hours), you’ll see the following error message when you attempt to assign them further tasks:</span></span>

<span data-ttu-id="20a20-142">*Užduočiai paskirti išteklių nepavyko – nepakanka toliau nurodytiems ištekliams rezervuotų valandų, susietų su šiuo projektu.*</span><span class="sxs-lookup"><span data-stu-id="20a20-142">*Unable to assign resource to task - Following resource(s) do not have sufficient hours booked against project.*</span></span>

<span data-ttu-id="20a20-143">Jie nebus rodomi išteklių išplečiamajame sąraše užduočių.</span><span class="sxs-lookup"><span data-stu-id="20a20-143">Additionally, the default project manager team member that is added to the team when you create the project is added without any bookings and can’t be assigned to any task.</span></span> <span data-ttu-id="20a20-144">Jie nebus rodomi išteklių išplečiamajame sąraše užduotims atlikti.</span><span class="sxs-lookup"><span data-stu-id="20a20-144">They won’t show up in the resource dropdown for tasks.</span></span>

<span data-ttu-id="20a20-145">Jei norite priskirti šiuos išteklius, turite juos pašalinti iš komandos ir tada iš juos įtraukti iš naujo, pasirinkdami bet kokį paskirstymo būdą, išskyrus „Joks“.</span><span class="sxs-lookup"><span data-stu-id="20a20-145">If you want to assign this resource, you need to remove them from the team and then re-add them with an allocation method other than None.</span></span> <span data-ttu-id="20a20-146">Sukūrus projektą jie yra įtraukiami į komandą todėl, kad pagal numatytuosius nustatymus projekte yra bent vienas projekto tvirtintojas.</span><span class="sxs-lookup"><span data-stu-id="20a20-146">The reason they’re added to the team when the project is created is so that a project has at least one project approver by default.</span></span>

## <a name="create-a-generic-team-member-through-role-assignment-on-tasks"></a><span data-ttu-id="20a20-147">Sukurkite bendrąjį komandos narį, naudojant užduočių vaidmenų paskyrimą.</span><span class="sxs-lookup"><span data-stu-id="20a20-147">Create a generic team member through role assignment on tasks</span></span>

<span data-ttu-id="20a20-148">Šiuo metodu užtikrinama, kad ištekliai rezervuoti užduotims atlikti reikalingam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="20a20-148">This method assures that resources have enough bookings for tasks.</span></span> <span data-ttu-id="20a20-149">Visų pirma, sukuriate vietos rezervavimo ženklo arba bendrinius išteklius, kuriais būtų nurodoma įvardytų išteklių, su kuriais norite dirbti atlikdami užduotis, charakteristika, baigus vaidmenų užduotims sukūrimą sugeneruojant komandą.</span><span class="sxs-lookup"><span data-stu-id="20a20-149">First, you create a placeholder or generic resource that describes the characteristics of the named resource you ultimately want to work on the tasks by generating a team after assigning roles to tasks.</span></span> <span data-ttu-id="20a20-150">Štai kaip galite tai padaryti:</span><span class="sxs-lookup"><span data-stu-id="20a20-150">Here’s how you do this:</span></span>

1. <span data-ttu-id="20a20-151">Darbo paskirstymo struktūros srityje pasirinkite užduotį.</span><span class="sxs-lookup"><span data-stu-id="20a20-151">On the work breakdown structure, select a task.</span></span>
2. <span data-ttu-id="20a20-152">Išteklių langelyje pasirinkite išskleidžiamąją piktogramą **„Priskirtas vaidmuo“**.</span><span class="sxs-lookup"><span data-stu-id="20a20-152">Select the **Assigned Role** dropdown icon in the resource cell.</span></span>
3. <span data-ttu-id="20a20-153">Pasirinkite išskleidžiamąją parinktį **„Vaidmuo“** ir pasirinkite bendrųjų išteklių vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="20a20-153">Select the **Role** dropdown and select the role for the generic resource.</span></span>
4. <span data-ttu-id="20a20-154">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="20a20-154">Select **OK**.</span></span>

    > [!div class="mx-imgBorder"] 
    > <span data-ttu-id="20a20-155">![IWBS naudojimo išteklių įtraukimui ekrano kopija](media/FAQ-Resources-to-Tasks2-4.png "IWBS naudojimo išteklių įtraukimui ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="20a20-155">![Screenshot of using WBS to add resource](media/FAQ-Resources-to-Tasks2-4.png "Screenshot of using WBS to add resource")</span></span>
 
<span data-ttu-id="20a20-156">Baigę vaidmenų priskyrimą užduotims WBS, pasirinkite **„Generuoti projekto komandą“**.</span><span class="sxs-lookup"><span data-stu-id="20a20-156">Once you’ve completed assigning roles to the tasks in the WBS, select **Generate Project Team**.</span></span> <span data-ttu-id="20a20-157">Agreguojant užduoties paskyrimus, „Project Service“ programoje sukuriamas mažiausias galimas bendrųjų komandos narių skaičius, remiantis jų vaidmenimis, išteklių paskirstymo organizacijos vienetais ir projekto kalendoriumi.</span><span class="sxs-lookup"><span data-stu-id="20a20-157">Project Service creates the minimum number of generic team members based on the roles, resourcing organization units, and project calendar by aggregating the task assignments.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20a20-158">![Projekto komandos generavimo ekrano kopija](media/FAQ-Resources-to-Tasks2-5.png "Projekto komandos generavimo ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="20a20-158">![Screenshot of generating project team](media/FAQ-Resources-to-Tasks2-5.png "Screenshot of generating project team")</span></span>
 
<span data-ttu-id="20a20-159">Komandos nario tinklelyje matysite bendrųjų išteklių tipo išteklius, kur bus nurodytas jų vaidmuo ir pareigų pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="20a20-159">On the Team Member grid, you’ll see resources of the Generic Resource type with the role and position name.</span></span> <span data-ttu-id="20a20-160">Jei norint pabaigti darbą vaidmeniui reikia dviejų išteklių, naudojantis funkcija „Generuoti komandą“ galima sukurti du komandos narius ir, naudojant pareigų pavadinimą, juos atskirti.</span><span class="sxs-lookup"><span data-stu-id="20a20-160">If two resources are needed for a role to complete the work, the Generate Team feature creates two team members and uses position name to set them apart.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20a20-161">![Dviejų bendrųjų išteklių įtraukimo ekrano kopija](media/FAQ-Resources-to-Tasks2-6.png "Dviejų bendrųjų išteklių įtraukimo ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="20a20-161">![Screenshot of adding two generic resources](media/FAQ-Resources-to-Tasks2-6.png "Screenshot of adding two generic resources")</span></span>
 
<span data-ttu-id="20a20-162">Galite atidaryti atsarginių išteklių reikalavimus bendrajam komandos nariui, paspausdami nuorodą po parinktimi „Išteklių reikalavimai“.</span><span class="sxs-lookup"><span data-stu-id="20a20-162">You can open the backing resource requirement for the generic team member by selecting the link under Resource Requirement.</span></span>

> [!div class="mx-imgBorder"] 
> <span data-ttu-id="20a20-163">![Atsarginės išteklių įrangos atidarymo ekrano kopija](media/FAQ-Resources-to-Tasks2-7.png "Atsarginės išteklių įrangos atidarymo ekrano kopija")</span><span class="sxs-lookup"><span data-stu-id="20a20-163">![Screenshot of opening backing resource requirement](media/FAQ-Resources-to-Tasks2-7.png "Screenshot of opening backing resource requirement")</span></span>

<span data-ttu-id="20a20-164">Bendriniams ištekliams pasirinkite **„Rezervuoti“** ir tada galėsite naudoti grafiko lentą tam, kad rastumėte ir rezervuotumėte tikrus išteklius.</span><span class="sxs-lookup"><span data-stu-id="20a20-164">Select **Book** for the generic resource, and then you can use the schedule board to find and book a real resource.</span></span> <span data-ttu-id="20a20-165">Taip pat galite išteklių vadovui pateikti reikalavimą, kad jis būtų įvykdytas. pasirinkdami **„Pateikti prašymą“**.</span><span class="sxs-lookup"><span data-stu-id="20a20-165">You can also submit the requirement for fulfillment by a resource manager by selecting **Submit Request**.</span></span>

<span data-ttu-id="20a20-166">Kai bendrieji ištekliai pakeičiami įvardytais ištekliais, bendrieji ištekliai yra pašalinami iš komandos, o jiems paskirtos užduotys paskiriamos įvardytiems ištekliams, kuriais pakeičiami bendrųjų išteklių išteklių reikalavimai.</span><span class="sxs-lookup"><span data-stu-id="20a20-166">When the generic resource is fulfilled with a named resource, the generic resource is removed from the team and the task assignments for the generic resource are assigned to the named resource that fulfilled the generic resource’s resource requirement.</span></span>
 

