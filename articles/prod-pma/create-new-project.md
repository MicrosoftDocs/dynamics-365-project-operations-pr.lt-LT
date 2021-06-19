---
title: Kurti naują projektą
description: Šioje temoje pateikta informacija apie tai, kaip sukurti naują projektą.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8218747366be8536601cb007318c642ac122536b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6006251"
---
# <a name="create-a-new-project"></a><span data-ttu-id="b7188-103">Kurti naują projektą</span><span class="sxs-lookup"><span data-stu-id="b7188-103">Create a new project</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b7188-104">Atlikite šiuos veiksmus, kad sukurtumėte naują projektą.</span><span class="sxs-lookup"><span data-stu-id="b7188-104">Complete the following steps to create a new project.</span></span>

1. <span data-ttu-id="b7188-105">Puslapyje **Projektų valdymas** pasirinkite **Naujas projektas** ir įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b7188-105">On the **Project management** page, select **New project**, and enter the following values:</span></span>

    - <span data-ttu-id="b7188-106">**Projekto tipas:** laikas ir medžiagos</span><span class="sxs-lookup"><span data-stu-id="b7188-106">**Project type:** Time and material</span></span>
    - <span data-ttu-id="b7188-107">**Projekto pavadinimas:** XYZ Upgrade Phase 2</span><span class="sxs-lookup"><span data-stu-id="b7188-107">**Project name:** XYZ Upgrade Phase 2</span></span>
    - <span data-ttu-id="b7188-108">**Projektų grupė:** TM\_WIP</span><span class="sxs-lookup"><span data-stu-id="b7188-108">**Project group:** TM\_WIP</span></span>
    - <span data-ttu-id="b7188-109">**Projekto sutarties ID:** 00000002</span><span class="sxs-lookup"><span data-stu-id="b7188-109">**Project contract ID:** 00000002</span></span>

2. <span data-ttu-id="b7188-110">Pasirinkite **Kurti projektą**.</span><span class="sxs-lookup"><span data-stu-id="b7188-110">Select **Create project**.</span></span>

## <a name="assign-a-resource-to-a-project"></a><span data-ttu-id="b7188-111">Išteklių priskyrimas projektui</span><span class="sxs-lookup"><span data-stu-id="b7188-111">Assign a resource to a project</span></span>

1. <span data-ttu-id="b7188-112">Puslapio **Darbuotojai** sąraše **Darbuotojai** pasirinkite darbuotojo, kuriam anksčiau nustatėte kompetencijas, įrašą, ir atidarykite darbuotojo įrašą.</span><span class="sxs-lookup"><span data-stu-id="b7188-112">On the **Workers** page, in the **Workers** list, select the record for the worker that you previously set up competencies for, and open the worker record.</span></span>
2. <span data-ttu-id="b7188-113">Veiksmų srityje, skirtuke **Projektas**, grupėje **Sąranka**, pasirinkite **Priskirti projektus**.</span><span class="sxs-lookup"><span data-stu-id="b7188-113">On the Action Pane, on the **Project** tab, in the **Setup** group, select **Assign projects**.</span></span>
3. <span data-ttu-id="b7188-114">Puslapyje **Išteklių tikrinimo projekto priskyrimai**, skirtuke **Projektai**, lauke **Įtraukti projektą į pasirinktus projektus** filtruokite projektą **XYZ Upgrade Phase 2**.</span><span class="sxs-lookup"><span data-stu-id="b7188-114">On the **Resource validation project assignments** page, on the **Projects** tab, in the **Add the project to selected projects** field, filter on the **XYZ Upgrade Phase 2** project.</span></span>
4. <span data-ttu-id="b7188-115">Srityje **Likę projektai** pasirinkite projektą, tada pasirinkite rodyklės mygtuką, kad įtrauktumėte jį į sritį **Pasirinkti projektai**.</span><span class="sxs-lookup"><span data-stu-id="b7188-115">In the **Remaining projects** pane, select a project, and then select the arrow button to add it to the **Selected projects** pane.</span></span>

<span data-ttu-id="b7188-116">Jeigu reikia, taip pat galite priskirti ištekliaus kategorijas.</span><span class="sxs-lookup"><span data-stu-id="b7188-116">You can also assign categories for a resource as you require.</span></span> <span data-ttu-id="b7188-117">Kategorijos tipas yra arba **Išlaidos**, arba **Pajamos**.</span><span class="sxs-lookup"><span data-stu-id="b7188-117">The category type is either **Cost** or **Revenue**.</span></span> <span data-ttu-id="b7188-118">Kategorijos tipą nustato jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="b7188-118">The category type is determined by your organization.</span></span> <span data-ttu-id="b7188-119">Jeigu ištekliui nepriskirta jokių kategorijų, „Finance” ieško numatytosios kategorijos pagal išlaidų ir pajamų valandos kainą.</span><span class="sxs-lookup"><span data-stu-id="b7188-119">If no categories are assigned for a resource, Finance looks up the default category on hour prices for cost and revenue.</span></span>

## <a name="set-up-project-resource-and-role-characteristics"></a><span data-ttu-id="b7188-120">Projektų išteklių ir vaidmens ypatybių nustatymas</span><span class="sxs-lookup"><span data-stu-id="b7188-120">Set up project resource and role characteristics</span></span>

<span data-ttu-id="b7188-121">Projektų vadovas gali naudoti projekto išteklių paskirstymo funkcijas, kad sukurtų projektui reikiamus vaidmenis.</span><span class="sxs-lookup"><span data-stu-id="b7188-121">A project manager can use the project resourcing functionality to create the roles that are required for the project.</span></span> <span data-ttu-id="b7188-122">Vaidmenys gali būti naudojami, kai rezervuojant išteklius, patvirtinti ištekliai vis dar nėra žinomi.</span><span class="sxs-lookup"><span data-stu-id="b7188-122">Roles can be used if confirmed resources are still unknown when resources are being reserved.</span></span> <span data-ttu-id="b7188-123">Vaidmenys gali būti laikinai rezervuojami kaip planuojami ištekliai, kad galėtumėte toliau vykdyti projekto planavimo etapus.</span><span class="sxs-lookup"><span data-stu-id="b7188-123">Roles can be temporarily reserved as planned resources, so that you can continue the project planning stages.</span></span>

<span data-ttu-id="b7188-124">[![Vaidmens pavyzdys](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span><span class="sxs-lookup"><span data-stu-id="b7188-124">[![Example of a role](./media/projectresourcing05.jpg)](./media/projectresourcing05.jpg)</span></span> 

<span data-ttu-id="b7188-125">**Scenarijus:** Contoso buvo pasamdyta užbaigti laiko ir medžiagų projektą, kuriame yra patvirtinta projekto diagrama.</span><span class="sxs-lookup"><span data-stu-id="b7188-125">**Scenario:** Contoso was hired to complete a Time and material project that has an approved project charter.</span></span> <span data-ttu-id="b7188-126">Jaunesnysis projekto vadovas vis dar nustato projekto aprėptį.</span><span class="sxs-lookup"><span data-stu-id="b7188-126">The junior project manager is still completing the scope of the project.</span></span> <span data-ttu-id="b7188-127">Išteklių vadovas dabar nustato konkrečius išteklius, kurie bus rezervuojami darbui naujame projekte.</span><span class="sxs-lookup"><span data-stu-id="b7188-127">The resource manager is currently identifying specific resources that will be reserved to work on the new project.</span></span> <span data-ttu-id="b7188-128">Projektas yra svarbus, todėl projekto rėmėjas paprašė nustatyti vyresniojo projekto vadovo vaidmenį kaip vieną iš vaidmenų.</span><span class="sxs-lookup"><span data-stu-id="b7188-128">Because of the critical nature of the project, the project sponsor requested Senior project manager as one of the roles.</span></span> <span data-ttu-id="b7188-129">Išteklių vadovas turi gauti naują išteklių ir apibrėžti vaidmenį sistemoje, nes jaunesniajam projekto vadovui planuojant projektą gali prireikti ištekliaus informacijos.</span><span class="sxs-lookup"><span data-stu-id="b7188-129">The resource manager must acquire the new resource and define the role in the system in case the junior project manager requires the resource information during project planning.</span></span>

<span data-ttu-id="b7188-130">Toliau pateikiamais veiksmais parodoma, kaip išteklių vadovas gali nustatyti vyresniojo projekto vadovo vaidmenį ir susieti su juo ištekliaus charakteristikas.</span><span class="sxs-lookup"><span data-stu-id="b7188-130">The following steps show how the resource manager can set up the Senior project manager role and associate resource characteristics with it.</span></span> <span data-ttu-id="b7188-131">Vėliau vaidmenį galima naudoti norint ieškoti galimų išteklių, atitinkančių reikiamas išteklių kompetencijas.</span><span class="sxs-lookup"><span data-stu-id="b7188-131">Later, the role can be used to search for available resources that match the required resource competencies.</span></span>

1. <span data-ttu-id="b7188-132">Puslapyje **Vaidmenų nustatymas** pasirinkite **Naujas** ir įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b7188-132">On the **Setup roles** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b7188-133">**Vaidmens ID:** vyresnysis projekto vadovas</span><span class="sxs-lookup"><span data-stu-id="b7188-133">**Role ID:** Senior Project Manager</span></span>
    - <span data-ttu-id="b7188-134">**Aprašas:** vyresnysis projekto vadovas</span><span class="sxs-lookup"><span data-stu-id="b7188-134">**Description:** Senior Project Manager</span></span>

2. <span data-ttu-id="b7188-135">Pasirinkite **Kurti**.</span><span class="sxs-lookup"><span data-stu-id="b7188-135">Select **Create**.</span></span>
3. <span data-ttu-id="b7188-136">Pasirinkite vaidmenį **Vyresnysis projekto vadovas**, tada pasirinkite **Konfigūruoti ypatybes**.</span><span class="sxs-lookup"><span data-stu-id="b7188-136">Select the **Senior Project Manager** role, and then select **Configure characteristics**.</span></span>
4. <span data-ttu-id="b7188-137">Lauke **Charakteristikų tipas** pažymėkite **Įgūdis**.</span><span class="sxs-lookup"><span data-stu-id="b7188-137">In the **Characteristics type** field, select **Skill**.</span></span>
5. <span data-ttu-id="b7188-138">Lauke **Galimos charakteristikos** įveskite ieškomą įgūdį.</span><span class="sxs-lookup"><span data-stu-id="b7188-138">In the **Available characteristics** field, enter the skill to search for.</span></span>
6. <span data-ttu-id="b7188-139">Lauke **Charakteristikų tipas** pažymėkite **Sertifikatas**.</span><span class="sxs-lookup"><span data-stu-id="b7188-139">In the **Characteristic type** field, select **Certificate**.</span></span>
7. <span data-ttu-id="b7188-140">Lauke **Galimos charakteristikos** įveskite ieškomą sertifikato tipą.</span><span class="sxs-lookup"><span data-stu-id="b7188-140">In the **Available characteristics** field, enter the certificate type to search for.</span></span>

## <a name="assign-a-project-resource-to-a-project"></a><span data-ttu-id="b7188-141">Projekto išteklių priskyrimas projektui</span><span class="sxs-lookup"><span data-stu-id="b7188-141">Assign a project resource to a project</span></span>

1. <span data-ttu-id="b7188-142">Puslapyje **Visi projektai** pasirinkite projektą **XYZ Upgrade Phase 2**.</span><span class="sxs-lookup"><span data-stu-id="b7188-142">On the **All projects** page, select the **XYZ Upgrade Phase 2** project.</span></span>
2. <span data-ttu-id="b7188-143">Skirtuke **Projekto komanda ir planavimas** pasirinkite **įtraukti**.</span><span class="sxs-lookup"><span data-stu-id="b7188-143">On the **Project team and scheduling** tab, select **Add**.</span></span>
3. <span data-ttu-id="b7188-144">Lauke **Vaidmuo** pasirinkite **Komandos narys**.</span><span class="sxs-lookup"><span data-stu-id="b7188-144">In the **Role** field, select **Team member**.</span></span>
4. <span data-ttu-id="b7188-145">Pasirinkite **Rezervuoti iš kalendoriaus**.</span><span class="sxs-lookup"><span data-stu-id="b7188-145">Select **Book from calendar**.</span></span>
5. <span data-ttu-id="b7188-146">Puslapyje **Išteklių pasiekiamumas** pasirinkite **Peržiūrėti parametrus**.</span><span class="sxs-lookup"><span data-stu-id="b7188-146">On the **Resource availability** page, select **View settings**.</span></span>
6. <span data-ttu-id="b7188-147">Puslapyje **Koreguoti rodinio parametrus** įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b7188-147">On the **Adjust view settings** page, enter the following values:</span></span>

    - <span data-ttu-id="b7188-148">**Datų diapazono rodinio formatas:** diena</span><span class="sxs-lookup"><span data-stu-id="b7188-148">**Format for date range view:** Day</span></span>
    - <span data-ttu-id="b7188-149">**Rodyti pasiekiamumo aprašus:** taip</span><span class="sxs-lookup"><span data-stu-id="b7188-149">**Display availability descriptions:** Yes</span></span>
    - <span data-ttu-id="b7188-150">**Rodyti likusį pajėgumą:** taip</span><span class="sxs-lookup"><span data-stu-id="b7188-150">**Display remaining capacity:** Yes</span></span>

7. <span data-ttu-id="b7188-151">Išteklių sąraše pasirinkite išteklių.</span><span class="sxs-lookup"><span data-stu-id="b7188-151">In the list of resources, select a resource.</span></span>
8. <span data-ttu-id="b7188-152">Pasirinkite **Rezervuoti galutinai** ir **Viso pajėgumo metodas**.</span><span class="sxs-lookup"><span data-stu-id="b7188-152">Select **Hard book** and **Full capacity**.</span></span>

## <a name="assign-a-resource-to-a-default-role"></a><span data-ttu-id="b7188-153">Ištekliaus priskyrimas numatytajam vaidmeniui</span><span class="sxs-lookup"><span data-stu-id="b7188-153">Assign a resource to a default role</span></span>

<span data-ttu-id="b7188-154">Norint padėti projekto ar išteklių vadovams, galima toliau detalizuoti projektui rezervuojamus išteklius.</span><span class="sxs-lookup"><span data-stu-id="b7188-154">To help project or resource managers can drill down further on the resources that can be reserved for a project.</span></span> <span data-ttu-id="b7188-155">Numatytąjį vaidmenį galite susieti su esamais ištekliais arba su naujai gautu ištekliumi.</span><span class="sxs-lookup"><span data-stu-id="b7188-155">You can associate a default role with an existing resource or a newly acquired resource.</span></span> <span data-ttu-id="b7188-156">Pavyzdžiui, kai Danielis buvo pasamdytas, jis turėjo patirtį ir įgūdžius, atitinkančius verslo analitiko vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="b7188-156">For example, when Daniel was hired, he had the experience and skills to fill the Business analyst role.</span></span> <span data-ttu-id="b7188-157">Išteklių vadovas priskyrė šį vaidmenį kaip numatytąjį Danieliaus vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="b7188-157">The resource manager assigned this role as Daniel's default role.</span></span> <span data-ttu-id="b7188-158">Todėl išteklių vadovas įtraukė Danielį į verslo analitikų, galinčių dirbti projektuose, telkinį.</span><span class="sxs-lookup"><span data-stu-id="b7188-158">Therefore, the resource manager added Daniel to a pool of business analysts who are available to work on projects.</span></span>

<span data-ttu-id="b7188-159">Rezervuodami išteklius, projektų vadovai gali filtruoti vaidmens išteklius, galinčius dirbti projektuose.</span><span class="sxs-lookup"><span data-stu-id="b7188-159">During resource reservation, project managers can filter the role resources that are available to work on projects.</span></span> <span data-ttu-id="b7188-160">Jie gali naudoti šią informaciją kaip vieną kriterijų, kai atlieka keliais kriterijais grindžiamą sprendimų analizę išteklių panaudojimo metu.</span><span class="sxs-lookup"><span data-stu-id="b7188-160">They can use this information as one criterion when they perform multi-criteria decision analysis during resource fulfillment.</span></span> <span data-ttu-id="b7188-161">Be to, filtruodami jie gali įtraukti kitų išteklių charakteristikų, kad galėtų ieškoti išteklių, turinčių konkrečių įgūdžių, išsilavinimą ir patirtį, kurių reikia dirbant nurodytame projekte.</span><span class="sxs-lookup"><span data-stu-id="b7188-161">They can also add other resource characteristics to the filter to search for resources that have specific skills, education, and experience for a given project.</span></span>

<span data-ttu-id="b7188-162">**Scenarijus:** pradėtas vykdyti patvirtintas projektas, o vyresniojo projekto vadovo vaidmuo buvo rezervuotas kaip planuotas išteklius projekto planavimo etape.</span><span class="sxs-lookup"><span data-stu-id="b7188-162">**Scenario:** An approved project has started, and the Senior project manager role was reserved as a planned resource during the project planning stage.</span></span> <span data-ttu-id="b7188-163">Dabar išteklių vadovas gavo išteklių, kuris atitinka vyresniojo projekto vadovo vaidmenį.</span><span class="sxs-lookup"><span data-stu-id="b7188-163">The resource manager has now acquired a resource to fulfill the Senior project manager role.</span></span>

1. <span data-ttu-id="b7188-164">Puslapyje **Išteklių sąrašas** pasirinkite **Danielis Goldschmidtas**.</span><span class="sxs-lookup"><span data-stu-id="b7188-164">On the **Resources list** page, select **Daniel Goldschmidt**.</span></span>
2. <span data-ttu-id="b7188-165">Puslapyje **Ištekliaus vaidmuo** pasirinkite **Naujas** ir įveskite toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="b7188-165">On the **Resource role** page, select **New**, and enter the following values:</span></span>

    - <span data-ttu-id="b7188-166">**Įsigaliojimo data:** įveskite šiandienos datą.</span><span class="sxs-lookup"><span data-stu-id="b7188-166">**Effective:** Enter the current date.</span></span>
    - <span data-ttu-id="b7188-167">**Galiojimo pabaigos data:** įveskite **Niekada**.</span><span class="sxs-lookup"><span data-stu-id="b7188-167">**Expiration:** Enter **Never**.</span></span>
    - <span data-ttu-id="b7188-168">**Vaidmuo:** įveskite **vyresnysis projekto vadovas**.</span><span class="sxs-lookup"><span data-stu-id="b7188-168">**Role:** Enter **Senior Project Manager**.</span></span>

3. <span data-ttu-id="b7188-169">Spustelėkite **Įrašyti** ir uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="b7188-169">Select **Save**, and then close the page.</span></span>
4. <span data-ttu-id="b7188-170">Skirtuke **Kompetencijos** įtraukite įgūdį **ProjectMgmt** ir sertifikatą **PMP**.</span><span class="sxs-lookup"><span data-stu-id="b7188-170">On the **Competencies** tab, add the **ProjectMgmt** skill and the **PMP** certificate.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]