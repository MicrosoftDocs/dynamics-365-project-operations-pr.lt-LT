---
title: Įvertinti projekto pardavimus ir kaštus, kai rezervuojamas išteklius užpildo kelis projekto vaidmenis
description: Šioje temoje pateikta informacija apie tai, kaip kainų dimensijas galima naudoti išteklių kainodarai, kuri užpildo kelis projekto vaidmenis, palaikyti.
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 8ddc827a4170c5576c0a4350b51e6a119094ac50
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080888"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-mulitple-roles-on-a-project"></a><span data-ttu-id="53a6f-103">Įvertinti projekto pardavimus ir kaštus, kai rezervuojamas išteklius užpildo kelis projekto vaidmenis</span><span class="sxs-lookup"><span data-stu-id="53a6f-103">Estimate project sales and costs when a bookable resource fills mulitple roles on a project</span></span> 

<span data-ttu-id="53a6f-104">Projektų įmonėms dažnai reikia vieno ištekliaus keliems projekto vaidmenims.</span><span class="sxs-lookup"><span data-stu-id="53a6f-104">Project-based companies often have the need for one resource to perform mulitple roles on a project.</span></span> <span data-ttu-id="53a6f-105">Kiekvienas iš šių vaidmenų gali būti įkainotas skirtingai, o tai reiškia, kad tas pats ištekliaus laikas projekto metu, priklausomai nuo sąskaitos ir kainų tarifų kiekvienam vaidmeniui, gali būti skirtingai finansiškai įvertintas.</span><span class="sxs-lookup"><span data-stu-id="53a6f-105">Each of these roles could be priced and costed differently which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="53a6f-106">„Project Service Automation“ leidžia nustatyti nurodyto ištekliaus komandos nario įrašo reikšmes ir atlikti įvairius, kiekvienos, komandos nariui priskirtos užduoties perrašymus.</span><span class="sxs-lookup"><span data-stu-id="53a6f-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="53a6f-107">Toliau pateiktame pavyzdyje aiškinama, kaip paprastas šios reikšmės perrašymas leidžia ištekliui turėti kelis vaidmenis projekte su skirtingais išlaidų ir sąskaitų tarifais.</span><span class="sxs-lookup"><span data-stu-id="53a6f-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="53a6f-108">Kurti užduotis</span><span class="sxs-lookup"><span data-stu-id="53a6f-108">Create tasks</span></span>
<span data-ttu-id="53a6f-109">Sukurkite dvi, 40 valandų trukmės A ir B projekto užduotis. Pasirinkite A užduotį kaip pirmtaką B užduočiai vykdyti.</span><span class="sxs-lookup"><span data-stu-id="53a6f-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="53a6f-110">Priskirkite vaidmenį ir organizacijos vienetą bendrajam projekto komandos nariui</span><span class="sxs-lookup"><span data-stu-id="53a6f-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="53a6f-111">**Grafiko** puslapyje, pasirinkite **užduoties** A eilutę.</span><span class="sxs-lookup"><span data-stu-id="53a6f-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="53a6f-112">**Išteklių** lauke, išskleidžiamame sąraše pasirinkite **sukurti**.</span><span class="sxs-lookup"><span data-stu-id="53a6f-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="53a6f-113">**Komandos nario sparčiojo kūrimo** puslapyje nurodykite bendrojo komandos nario, kuris gali atlikti šią užduotį, atributus.</span><span class="sxs-lookup"><span data-stu-id="53a6f-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="53a6f-114">Pasirinkite atitinkamą vaidmenį ir organizacijos vienetą, tada spauskite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="53a6f-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="53a6f-115">Bendrinis komandos narys sukurtas ir priskirtas šiai užduočiai.</span><span class="sxs-lookup"><span data-stu-id="53a6f-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="53a6f-116">Pakartokite šiuos veiksmus su užduotimi B ir įsitikinkite, kad bendrojo komandos nario vaidmuo ir organizacijos vienetas, sukurtas B užduočiai, skiriasi nuo A užduoties.</span><span class="sxs-lookup"><span data-stu-id="53a6f-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="53a6f-117">Priskirkite vaidmenį ir organizacijos vienetą projekto užduočiai</span><span class="sxs-lookup"><span data-stu-id="53a6f-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="53a6f-118">Kai sukuriate A užduotį, ją pažymėkite ir pasirinkite **Redaguoti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="53a6f-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="53a6f-119">**Užduoties išsami informacija** puslapyje raskite **vaidmens** ir **organizacijos vieneto** laukus, pridėkite reikšmes, būtinas ištekliui, atliekančiam šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="53a6f-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="53a6f-120">Jei šiuos scenarijus užbaigiate naudodami „Project Service Automation“ demonstracinės versijos duomenis, pasirinkite **Konsultavimo vadovą** ir **„Fabrikam“ JAV** kaip organizacijos vienetą.</span><span class="sxs-lookup"><span data-stu-id="53a6f-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="53a6f-121">Pasirinkite B užduotį ir tada spauskite **Redaguoti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="53a6f-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="53a6f-122">**Užduoties išsami informacija** puslapyje raskite **vaidmens** ir **organizacijos vieneto** laukus, pridėkite reikšmes, būtinas ištekliui, atliekančiam šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="53a6f-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="53a6f-123">Įsitikinkite, kad B užduoties reikšmės **vaidmens** ir **organizacijos vieneto** laukuose yra skirtingos nuo A užduoties.</span><span class="sxs-lookup"><span data-stu-id="53a6f-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from those for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="53a6f-124">Jei šiuos scenarijus užbaigiate naudodami „Project Service Automation“ demonstracinės versijos duomenis, pasirinkite **Tinklo techniką** vaidmeniui ir **„Fabrikam“ JAV** kaip organizacijos vienetą.</span><span class="sxs-lookup"><span data-stu-id="53a6f-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="53a6f-125">Išsaugokite ir uždarykite **išsamios užduoties informacijos** puslapį.</span><span class="sxs-lookup"><span data-stu-id="53a6f-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behaviour"></a><span data-ttu-id="53a6f-126">Komandos narys ir sąmatos elgsena</span><span class="sxs-lookup"><span data-stu-id="53a6f-126">Team member and estimates behaviour</span></span> 

1. <span data-ttu-id="53a6f-127">**Užduoties išsami informacija** puslapyje, **komandos nario** sekcijoje pažymėkite du bendruosius komandos narius ir pažymėkite **Generuoti reikalavimus**.</span><span class="sxs-lookup"><span data-stu-id="53a6f-127">On the **Task Details** page, on the **Team Member** , select the two generic team Members and then select **Generate Requirements**.</span></span> <span data-ttu-id="53a6f-128">Tai sukurs reikalavimus ištekliui.</span><span class="sxs-lookup"><span data-stu-id="53a6f-128">This will generate resource requirements.</span></span> 
2. <span data-ttu-id="53a6f-129">Pasirinkite komandos nario eilutę **konsultacijų vadovui** ir spauskite **rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="53a6f-129">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="53a6f-130">Atsidaro tvarkaraščio lenta ir rezervuojamas išteklius pagal reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="53a6f-130">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="53a6f-131">Pasirinkite komandos nario eilutę **tinklo technikui** ir spauskite **rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="53a6f-131">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="53a6f-132">Atsidaro tvarkaraščio lenta ir rezervuojamas tas pats išteklius pagal reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="53a6f-132">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="53a6f-133">Komandos nario tinklelis</span><span class="sxs-lookup"><span data-stu-id="53a6f-133">Team Member grid</span></span> 
<span data-ttu-id="53a6f-134">**Komandos nario** tinklelyje atkreipkite dėmesį, kad du bendrojo komandos nario įrašai yra ištrinti, o juos pakeitė vienas išteklius.</span><span class="sxs-lookup"><span data-stu-id="53a6f-134">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="53a6f-135">Yra vienas to ištekliaus reikšmių rinkinys, kuris rodo numatytąjį **vaidmens** ir **organizacijos vieneto** reikšmių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="53a6f-135">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="53a6f-136">Išplėtus tos komandos nario įrašo eilutę, galite matyti atskiras paskirtas užduotis abiems užduotims.</span><span class="sxs-lookup"><span data-stu-id="53a6f-136">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="53a6f-137">Kiekviena paskyrimo eilutė turi tam tikras **vaidmens** ir **organizacijos vieneto** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="53a6f-137">Each assignment row has task specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="53a6f-138">Įvertinimo tinklelis</span><span class="sxs-lookup"><span data-stu-id="53a6f-138">Estimates grid</span></span> 
<span data-ttu-id="53a6f-139">Kai pereisite į **sąmatų** tinklelį, pastebėsite, kad abi to paties ištekliaus užduotys įkainojamos skirtingai.</span><span class="sxs-lookup"><span data-stu-id="53a6f-139">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="53a6f-140">A užduoties priskyrimas ištekliui yra įkainotas naudojant **Vaidmens** **Konsultavimo vadovo** atributo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53a6f-140">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="53a6f-141">B užduoties priskyrimas tam pačiam ištekliui yra įkainotas naudojant **Vaidmens** **Tinklo techniko** atributo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="53a6f-141">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>





