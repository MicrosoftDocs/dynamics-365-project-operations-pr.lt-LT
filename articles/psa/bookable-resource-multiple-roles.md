---
title: Projekto pardavimo ir išlaidų įvertinimas, kai rezervuojami ištekliai projekte atlieka kelis vaidmenis
description: Šioje temoje pateikiama informacija apie tai, kaip naudoti kainodaros dimensijas, skirtas išteklių, kurie projekte atlieka kelis vaidmenis, kainodarai ir įkainojimui palaikyti.
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
ms.openlocfilehash: 67e24156e960b9b09cf92f7f0cd77f6c74a982b8
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145053"
---
# <a name="estimate-project-sales-and-costs-when-a-bookable-resource-fills-multiple-roles-for-a-project"></a><span data-ttu-id="05945-103">Projekto pardavimo ir išlaidų įvertinimas, kai rezervuojami ištekliai projekte atlieka kelis vaidmenis</span><span class="sxs-lookup"><span data-stu-id="05945-103">Estimate project sales and costs when a bookable resource fills multiple roles for a project</span></span> 

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="05945-104">Projektu pagrįstoms įmonėms dažnai reikia vieno ištekliaus, kad projekte atliktų kelis vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="05945-104">Project-based companies often have the need for one resource to perform multiple roles on a project.</span></span> <span data-ttu-id="05945-105">Kiekvienas iš šių vaidmenų gali būti įkainotas skirtingai, o tai reiškia, kad tas pats ištekliaus laikas projekto metu, priklausomai nuo sąskaitos ir išlaidų tarifų kiekvienam vaidmeniui, gali būti skirtingai finansiškai įvertintas.</span><span class="sxs-lookup"><span data-stu-id="05945-105">Each of these roles could be priced and costed differently, which means the same resource's time on the project could get a different financial estimate depending on the bill and cost rates for each of the roles.</span></span> <span data-ttu-id="05945-106">„Project Service Automation“ leidžia nustatyti nurodyto ištekliaus komandos nario įrašo reikšmes ir atlikti įvairius, kiekvienos, komandos nariui priskirtos užduoties perrašymus.</span><span class="sxs-lookup"><span data-stu-id="05945-106">Project Service Automation allows the setup of the values on the team member record for the named resource and allows for different overrides on each of the tasks that the team member is assigned to.</span></span>

<span data-ttu-id="05945-107">Toliau pateiktame pavyzdyje aiškinama, kaip paprastas šios reikšmės perrašymas leidžia ištekliui turėti kelis vaidmenis projekte su skirtingais išlaidų ir sąskaitų tarifais.</span><span class="sxs-lookup"><span data-stu-id="05945-107">The following example  explains how the simple override of this value allows a resource to have multiple roles on a project with different cost and bill rates.</span></span>

## <a name="create-tasks"></a><span data-ttu-id="05945-108">Kurti užduotis</span><span class="sxs-lookup"><span data-stu-id="05945-108">Create tasks</span></span>
<span data-ttu-id="05945-109">Sukurkite dvi, 40 valandų trukmės A ir B projekto užduotis. Pasirinkite A užduotį kaip pirmtaką B užduočiai vykdyti.</span><span class="sxs-lookup"><span data-stu-id="05945-109">Create two project tasks for 40 hours each, Task A and Task B. Select Task A as a predecessor to Task B.</span></span>

## <a name="set-up-role-and-organization-unit-for-a-generic-project-team-member"></a><span data-ttu-id="05945-110">Priskirkite vaidmenį ir organizacijos vienetą bendrajam projekto komandos nariui</span><span class="sxs-lookup"><span data-stu-id="05945-110">Set up Role and Organization Unit for a generic project team member</span></span>

1. <span data-ttu-id="05945-111">**Grafiko** puslapyje, pasirinkite **užduoties** A eilutę.</span><span class="sxs-lookup"><span data-stu-id="05945-111">On the **Schedule** page, select the **Task** row for Task A.</span></span> 
2. <span data-ttu-id="05945-112">**Išteklių** lauke, išskleidžiamame sąraše pasirinkite **sukurti**.</span><span class="sxs-lookup"><span data-stu-id="05945-112">In the **Resources** field, select **Create** in the drop-down list.</span></span>
3. <span data-ttu-id="05945-113">**Komandos nario sparčiojo kūrimo** puslapyje nurodykite bendrojo komandos nario, kuris gali atlikti šią užduotį, atributus.</span><span class="sxs-lookup"><span data-stu-id="05945-113">On the **Team Member Quick Create** page, specify the attributes of the generic team member who can perform this task.</span></span>
4. <span data-ttu-id="05945-114">Pasirinkite atitinkamą vaidmenį ir organizacijos vienetą, tada spauskite **Įrašyti ir uždaryti**.</span><span class="sxs-lookup"><span data-stu-id="05945-114">Select the appropriate role and organizational unit, and then select **Save and Close**.</span></span> <span data-ttu-id="05945-115">Bendrinis komandos narys sukurtas ir priskirtas šiai užduočiai.</span><span class="sxs-lookup"><span data-stu-id="05945-115">A generic team member is created and assigned to this task.</span></span> 

<span data-ttu-id="05945-116">Pakartokite šiuos veiksmus su užduotimi B ir įsitikinkite, kad bendrojo komandos nario vaidmuo ir organizacijos vienetas, sukurtas B užduočiai, skiriasi nuo A užduoties.</span><span class="sxs-lookup"><span data-stu-id="05945-116">Repeat these steps for Task B and make sure that the role and organizational unit on the generic team member created for Task B is different than Task A.</span></span> 

## <a name="set-up-role-and-organization-unit-for-a-project-task"></a><span data-ttu-id="05945-117">Priskirkite vaidmenį ir organizacijos vienetą projekto užduočiai</span><span class="sxs-lookup"><span data-stu-id="05945-117">Set up role and organization unit for a project task</span></span>

1. <span data-ttu-id="05945-118">Kai sukuriate A užduotį, ją pažymėkite ir pasirinkite **Redaguoti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="05945-118">After you create Task A, select the task, and then select **Edit task**.</span></span>
2. <span data-ttu-id="05945-119">**Užduoties išsami informacija** puslapyje raskite **vaidmens** ir **organizacijos vieneto** laukus, pridėkite reikšmes, būtinas ištekliui, atliekančiam šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="05945-119">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="05945-120">Jei šiuos scenarijus užbaigiate naudodami „Project Service Automation“ demonstracinės versijos duomenis, pasirinkite **Konsultavimo vadovą** ir **„Fabrikam“ JAV** kaip organizacijos vienetą.</span><span class="sxs-lookup"><span data-stu-id="05945-120">If you are completing this scenarios using Project Service Automation demo data, select **Consulting Lead** for the role, and **Fabrikam US** as the organizational unit.</span></span>

3. <span data-ttu-id="05945-121">Pasirinkite B užduotį ir tada spauskite **Redaguoti užduotį**.</span><span class="sxs-lookup"><span data-stu-id="05945-121">Select Task B and then select **Edit task**.</span></span>
4. <span data-ttu-id="05945-122">**Užduoties išsami informacija** puslapyje raskite **vaidmens** ir **organizacijos vieneto** laukus, pridėkite reikšmes, būtinas ištekliui, atliekančiam šią užduotį.</span><span class="sxs-lookup"><span data-stu-id="05945-122">On the **Task Details** page, find the **Role** and **Organizational Unit** fields, add the values that are required of a resource that would perform this task.</span></span> <span data-ttu-id="05945-123">Įsitikinkite, kad laukų **Vaidmuo** ir **Organizacinis vienetas** reikšmės B užduočiai skiriasi nuo reikšmių A užduočiai.</span><span class="sxs-lookup"><span data-stu-id="05945-123">Make sure that the values in the **Role** and **Organizational Unit** fields are different for Task B from the values for Task A.</span></span> 

  > [!NOTE]
  > <span data-ttu-id="05945-124">Jei šiuos scenarijus užbaigiate naudodami „Project Service Automation“ demonstracinės versijos duomenis, pasirinkite **Tinklo techniką** vaidmeniui ir **„Fabrikam“ JAV** kaip organizacijos vienetą.</span><span class="sxs-lookup"><span data-stu-id="05945-124">If you are completing this scenarios using Project Service Automation demo data, select **Network Technician** for the role, and **Fabrikam US** as the organizational unit.</span></span>

5. <span data-ttu-id="05945-125">Išsaugokite ir uždarykite **išsamios užduoties informacijos** puslapį.</span><span class="sxs-lookup"><span data-stu-id="05945-125">Save and close the **Task Details** page.</span></span> 

## <a name="team-member-and-estimates-behavior"></a><span data-ttu-id="05945-126">Komandos nario ir įvertinimų veikimo būdas</span><span class="sxs-lookup"><span data-stu-id="05945-126">Team member and estimates behavior</span></span> 

1. <span data-ttu-id="05945-127">**Užduoties išsami informacija** puslapyje, **komandos nario** sekcijoje pažymėkite du bendruosius komandos narius ir pažymėkite **Generuoti reikalavimus**.</span><span class="sxs-lookup"><span data-stu-id="05945-127">On the **Task Details** page, on the **Team Member**, select the two generic team Members and then select **Generate Requirements**.</span></span> 
2. <span data-ttu-id="05945-128">Pasirinkite komandos nario eilutę **konsultacijų vadovui** ir spauskite **rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="05945-128">Select the team member row for **Consulting Lead** and then select **Book**.</span></span> <span data-ttu-id="05945-129">Atsidaro tvarkaraščio lenta ir rezervuojamas išteklius pagal reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="05945-129">The schedule board opens and books a resource to that requirement.</span></span>
3. <span data-ttu-id="05945-130">Pasirinkite komandos nario eilutę **tinklo technikui** ir spauskite **rezervuoti**.</span><span class="sxs-lookup"><span data-stu-id="05945-130">Select the team member row for **Network Technician** and the select **Book**.</span></span> <span data-ttu-id="05945-131">Atsidaro tvarkaraščio lenta ir rezervuojamas tas pats išteklius pagal reikalavimą.</span><span class="sxs-lookup"><span data-stu-id="05945-131">The schedule board opens and books the same resource on that requirement.</span></span>

### <a name="team-member-grid"></a><span data-ttu-id="05945-132">Komandos nario tinklelis</span><span class="sxs-lookup"><span data-stu-id="05945-132">Team Member grid</span></span> 
<span data-ttu-id="05945-133">**Komandos nario** tinklelyje atkreipkite dėmesį, kad du bendrojo komandos nario įrašai yra ištrinti, o juos pakeitė vienas išteklius.</span><span class="sxs-lookup"><span data-stu-id="05945-133">On the **Team Member** grid, notice that the two generic team member records are deleted and have been replaced one resource.</span></span> <span data-ttu-id="05945-134">Yra vienas to ištekliaus reikšmių rinkinys, kuris rodo numatytąjį **vaidmens** ir **organizacijos vieneto** reikšmių rinkinį.</span><span class="sxs-lookup"><span data-stu-id="05945-134">There is one set of values for that resource that shows a default set of values for **Role** and **Organizational Unit**.</span></span>
<span data-ttu-id="05945-135">Išplėtus tos komandos nario įrašo eilutę, galite matyti atskiras paskirtas užduotis abiems užduotims.</span><span class="sxs-lookup"><span data-stu-id="05945-135">When you expand the row of that Team Member record, you can see distinct assignments on the team member record for both of those tasks.</span></span> <span data-ttu-id="05945-136">Kiekviena priskyrimo eilutė turi tam tikras **vaidmens** ir **organizacijos vieneto** reikšmes.</span><span class="sxs-lookup"><span data-stu-id="05945-136">Each assignment row has task-specific values for **Role** and **Organizational Unit**.</span></span> 

### <a name="estimates-grid"></a><span data-ttu-id="05945-137">Įvertinimo tinklelis</span><span class="sxs-lookup"><span data-stu-id="05945-137">Estimates grid</span></span> 
<span data-ttu-id="05945-138">Kai pereisite į **sąmatų** tinklelį, pastebėsite, kad abi to paties ištekliaus užduotys įkainojamos skirtingai.</span><span class="sxs-lookup"><span data-stu-id="05945-138">When you navigate to the **Estimates** grid, you will notice that both assignments for the same resource are priced differently.</span></span>
<span data-ttu-id="05945-139">A užduoties priskyrimas ištekliui yra įkainotas naudojant **Vaidmens** **Konsultavimo vadovo** atributo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="05945-139">The assignment for the resource on Task A is priced using the **Role** attribute value of **Consulting Lead**.</span></span> <span data-ttu-id="05945-140">B užduoties priskyrimas tam pačiam ištekliui yra įkainotas naudojant **Vaidmens** **Tinklo techniko** atributo reikšmę.</span><span class="sxs-lookup"><span data-stu-id="05945-140">The assignment for the same resource on Task B is priced using the **Role** attribute value of **Network Technician**.</span></span>

