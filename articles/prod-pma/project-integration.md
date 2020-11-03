---
title: „Microsoft Project Client” integravimas
description: Gali būti sudėtinga planuoti ir laikytis projekto grafiko, todėl projektų vadovai turi naudoti įrankius, padedančius susitvarkyti su šia užduotimi. Integravimas su „Microsoft Project Client” padeda atidaryti ir valdyti projekto darbo paskirstymo struktūrą.
author: Yowelle
manager: AnnBe
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 732b72d9819fc149c4b2c783b3dc7f7eec3f0393
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080897"
---
# <a name="microsoft-project-client-integration"></a><span data-ttu-id="bcbae-104">„Microsoft Project Client” integravimas</span><span class="sxs-lookup"><span data-stu-id="bcbae-104">Microsoft Project client integration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcbae-105">Gali būti sudėtinga planuoti ir laikytis projekto grafiko, todėl projektų vadovai turi naudoti įrankius, padedančius susitvarkyti su šia užduotimi.</span><span class="sxs-lookup"><span data-stu-id="bcbae-105">Planning and maintaining a project schedule can be complex, so project managers need to use tools that help them manage this task.</span></span> <span data-ttu-id="bcbae-106">Integravimas su „Microsoft Project Client” padeda atidaryti ir valdyti projekto darbo paskirstymo struktūrą.</span><span class="sxs-lookup"><span data-stu-id="bcbae-106">Integration with Microsoft Project Client provides support to open and manage a project work breakdown structure.</span></span> <span data-ttu-id="bcbae-107">Projektų vadovas gali bet kokius keitimus publikuoti „Dynamics 365 Finance” projekto darbo paskirstymo struktūroje.</span><span class="sxs-lookup"><span data-stu-id="bcbae-107">The project manager can publish any changes back to the Dynamics 365 Finance project work breakdown structure.</span></span>

> [!NOTE]
> <span data-ttu-id="bcbae-108">Jei naudojate liepos mėn. naujinimą (10.0.4 versija), turite įdiegti KB 4054797 ir 4055884.</span><span class="sxs-lookup"><span data-stu-id="bcbae-108">If you are using the July update (version 10.0.4), you must install KB 4054797 and 4055884.</span></span>

## <a name="configure-the-microsoft-project-client-add-in"></a><span data-ttu-id="bcbae-109">„Microsoft Project Client” papildinio konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="bcbae-109">Configure the Microsoft Project Client add-in</span></span>
<span data-ttu-id="bcbae-110">Siekiant įgalinti integravimą su „Microsoft Project Client”, reikalaujama įdiegti „Microsoft Dynamics 365” papildinį į vartotojo programą „Microsoft Project Client”.</span><span class="sxs-lookup"><span data-stu-id="bcbae-110">To enable the integration with Microsoft Project Client, a Microsoft Dynamics 365 add-in is required to be installed in the user’s client Microsoft Project application.</span></span> <span data-ttu-id="bcbae-111">Tai atliekama atidarius **projektų valdymo darbo sritį**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-111">This is done by opening the **Project management workspace**.</span></span>

<span data-ttu-id="bcbae-112">• Spustelėkite **Konfigūruoti projekto kliento papildinį** iš darbo srities skyriaus **Saitai** > **Sąranka**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-112">•   Click **Configure project client add-in** from the **Links** > **Setup** section of the workspace.</span></span>

<span data-ttu-id="bcbae-113">• Spustelėkite **Atidaryti** , tada paraginti, spustelėkite **Vykdyti**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-113">•   Click **Open** , then click **Run** when prompted.</span></span>

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a><span data-ttu-id="bcbae-114">Programoje „Microsoft Project Client” atidarykite ir redaguokite darbo paskirstymo struktūros juodraštį</span><span class="sxs-lookup"><span data-stu-id="bcbae-114">Open and edit an existing draft work breakdown structure in Microsoft Project Client</span></span>
<span data-ttu-id="bcbae-115">Jei „Dynamics 365 Finance” esantis projektas jau turi sukurtą darbo paskirstymo struktūrą, šią darbo paskirstymo struktūrą galima atidaryti programoje „Microsoft Project Client”, jeigu darbo paskirstymo struktūra yra juodraščio būsenos.</span><span class="sxs-lookup"><span data-stu-id="bcbae-115">If a project in Dynamics 365 Finance already has a work breakdown structure created, the work breakdown structure can be opened in the Microsoft Project Client application if the work breakdown structure is in a draft status.</span></span> <span data-ttu-id="bcbae-116">Norėdami atidaryti puslapį **Projektas** , spustelėkite skirtuke **Planas** esantį saitą **Atidaryti programoje „Microsoft Project”**. Šis puslapis taip pat gali būti atidarytas programoje „Microsoft Project Client”, skirtuke **„Microsoft Dynamics 365”** spustelint **Atidaryti**. Sąraše pasirinkite **Juridinis subjektas** ir **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-116">To open from the **Project** page, click **Open in Microsoft Project** link from the **Plan** tab. This page can also be opened from within the Microsoft Project Client application by clicking **Open** in the **Microsoft Dynamics 365** tab. Select the **Legal entity** and **Project** from the list.</span></span>

> [!NOTE]
> <span data-ttu-id="bcbae-117">Jei naudojate naršyklę „Internet Explorer” jums reikės spustelėti **Įrašyti** , kad rankiniu būdu atidarytumėte iš tos vietos, į kurią atsisiųstas failas.</span><span class="sxs-lookup"><span data-stu-id="bcbae-117">If you're using Internet Explorer as your browser, you will need to click **Save** to manually open from the location that the file is downloaded to.</span></span> <span data-ttu-id="bcbae-118">Arba spustelėkite **Įrašyti ir atidaryti** , kad atidarytumėte failą programoje „Microsoft Project Client”.</span><span class="sxs-lookup"><span data-stu-id="bcbae-118">Or, click **Save and open** to open the file in Microsoft Project Client.</span></span> <span data-ttu-id="bcbae-119">Įrašydami nepervardykite failo.</span><span class="sxs-lookup"><span data-stu-id="bcbae-119">Do not rename the file name when saving.</span></span>

<span data-ttu-id="bcbae-120">Prieš redaguodami failą programoje „Microsoft Project Client”, turite jį išregistruoti. Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Išregistruoti**. Taip kiti vartotojai negalės tuo pačiu metu redaguoti darbo paskirstymo struktūros programoje „Finance”.</span><span class="sxs-lookup"><span data-stu-id="bcbae-120">Before making any edits to the file using Microsoft Project Client, you need to check it out. Click **Check out** in the **Microsoft Dynamics 365** tab. This will prevent other users from editing the work breakdown structure from within Finance at the same time.</span></span> <span data-ttu-id="bcbae-121">Jei atlikę redagavimą, norite publikuoti darbo paskirstymo struktūrą, skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įregistruoti**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-121">To publish the work breakdown structure after completing any edits, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

<span data-ttu-id="bcbae-122">Jei projekto komanda jau buvo įtraukta į projektą programoje „Finance”, į išteklių sąrašą bus įrašyti komandos nariai.</span><span class="sxs-lookup"><span data-stu-id="bcbae-122">If a project team has already been added to the project in Finance, the resource list will be populated with the team members.</span></span> <span data-ttu-id="bcbae-123">Jeigu projekto komanda dar nebuvo įtraukta į projektą, galite pasirinkti išteklius ir sukurti komandą programoje „Microsoft Project Client” skirtuke **„Microsoft Dynamics 365”** spustelėdami mygtuką **Ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-123">If a project team has not yet been added to the project, you can select resources and build the team within Microsoft Project Client by clicking the **Resources** button on the **Microsoft Dynamics 365** tab.</span></span> 

<span data-ttu-id="bcbae-124">Vykdant įregistravimo procesą toliau pateikiami duomenys bus sinchronizuojami su „Finance”.</span><span class="sxs-lookup"><span data-stu-id="bcbae-124">The following data will be synced back to Finance as part of the check-in process:</span></span>

<span data-ttu-id="bcbae-125">•   Užduoties pavadinimas</span><span class="sxs-lookup"><span data-stu-id="bcbae-125">•   Task name</span></span>

<span data-ttu-id="bcbae-126">•   Pradžios data</span><span class="sxs-lookup"><span data-stu-id="bcbae-126">•   Start date</span></span>

<span data-ttu-id="bcbae-127">•   Pabaigos data</span><span class="sxs-lookup"><span data-stu-id="bcbae-127">•   Finish date</span></span>

<span data-ttu-id="bcbae-128">•   Ankstesnės užduotys</span><span class="sxs-lookup"><span data-stu-id="bcbae-128">•   Predecessors</span></span>

<span data-ttu-id="bcbae-129">•   Išteklių pavadinimai</span><span class="sxs-lookup"><span data-stu-id="bcbae-129">•   Resource names</span></span>

<span data-ttu-id="bcbae-130">•   Kategorija</span><span class="sxs-lookup"><span data-stu-id="bcbae-130">•   Category</span></span>

<span data-ttu-id="bcbae-131">•   Išteklių kategorija</span><span class="sxs-lookup"><span data-stu-id="bcbae-131">•   Resource category</span></span>

<span data-ttu-id="bcbae-132">•   Darbo valandos</span><span class="sxs-lookup"><span data-stu-id="bcbae-132">•   Work hours</span></span>

<span data-ttu-id="bcbae-133">•   Pastabos</span><span class="sxs-lookup"><span data-stu-id="bcbae-133">•   Notes</span></span>

<span data-ttu-id="bcbae-134">•   Pirmumas</span><span class="sxs-lookup"><span data-stu-id="bcbae-134">•   Priority</span></span>

> [!NOTE]
> <span data-ttu-id="bcbae-135">Jeigu į savo „Microsoft Project Client” failą įtrauksite kitų stulpelių, jie nebus įrašyti faile ir nebus rodomi, kai failas bus dar kartą atidarytas.</span><span class="sxs-lookup"><span data-stu-id="bcbae-135">If you add any other columns to your Microsoft Project Client file, they will not be saved to the file and will not be displayed when the file is opened again.</span></span>

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bcbae-136">Esamo projekto darbo paskirstymo struktūros kūrimas, naudojant „Microsoft Project Client”</span><span class="sxs-lookup"><span data-stu-id="bcbae-136">Create the work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bcbae-137">Norėdami sukurti naują darbo paskirstymo struktūrą, naudojant „Microsoft Project Client”, atlikite tolesnius veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bcbae-137">To create a new work breakdown structure using Microsoft Project Client, follow these steps:</span></span>


1.  <span data-ttu-id="bcbae-138">Atidarykite „Microsoft Project Client”.</span><span class="sxs-lookup"><span data-stu-id="bcbae-138">Open Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bcbae-139">Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Atidaryti**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-139">On the **Microsoft Dynamics 365** tab, click **Open**.</span></span>

3.  <span data-ttu-id="bcbae-140">Pasirinkite projekto **Juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-140">Select the **Legal entity** for the project.</span></span>

4.  <span data-ttu-id="bcbae-141">Pasirinkite **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-141">Select the **Project**.</span></span>

5.  <span data-ttu-id="bcbae-142">Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Išregistruoti**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-142">Click **Check out** on the **Microsoft Dynamics 365** tab.</span></span>

6.  <span data-ttu-id="bcbae-143">Kai būsite pasirengę publikuoti programoje „Finance”, skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įregistruoti**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-143">When ready to publish to Finance, click **Check in** on the **Microsoft Dynamics 365** tab.</span></span>

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a><span data-ttu-id="bcbae-144">Esamo projekto esamos darbo paskirstymo struktūros keitimas, naudojant „Microsoft Project Client”</span><span class="sxs-lookup"><span data-stu-id="bcbae-144">Replace the existing work breakdown structure for an existing project using Microsoft Project Client</span></span>
<span data-ttu-id="bcbae-145">Jei norite sukurti naują darbo paskirstymo struktūrą naudodami „Microsoft Project Client” ir pakeisti esamo projekto darbo paskirstymo struktūrą, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="bcbae-145">To create a new work breakdown structure using Microsoft Project Client and replace an existing work breakdown structure for an existing project, follow these steps:</span></span>

1.  <span data-ttu-id="bcbae-146">Atidarykite „Microsoft Project Client”.</span><span class="sxs-lookup"><span data-stu-id="bcbae-146">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bcbae-147">Programoje „Microsoft Project Client” sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="bcbae-147">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bcbae-148">Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įrašyti pakeitimus** > **Keisti esamą projektą**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-148">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Replace existing project**.</span></span>

4.  <span data-ttu-id="bcbae-149">Pasirinkite projekto **Juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-149">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bcbae-150">Pasirinkite **Projektas**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-150">Select the **Project**.</span></span>

6.  <span data-ttu-id="bcbae-151">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-151">Click **OK**.</span></span>

## <a name="create-a-new-project-from-within-microsoft-project-client"></a><span data-ttu-id="bcbae-152">Naujo projekto kūrimas programoje „Microsoft Project Client”</span><span class="sxs-lookup"><span data-stu-id="bcbae-152">Create a new project from within Microsoft Project Client</span></span>


1.  <span data-ttu-id="bcbae-153">Atidarykite „Microsoft Project Client”.</span><span class="sxs-lookup"><span data-stu-id="bcbae-153">Open the Microsoft Project Client.</span></span>

2.  <span data-ttu-id="bcbae-154">Programoje „Microsoft Project Client” sukurkite grafiką.</span><span class="sxs-lookup"><span data-stu-id="bcbae-154">Create the schedule in Microsoft Project Client.</span></span>

3.  <span data-ttu-id="bcbae-155">Skirtuke **„Microsoft Dynamics 365”** spustelėkite **Įrašyti pakeitimus** > **Įrašyti į naują projektą**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-155">On the **Microsoft Dynamics 365** tab, click **Save changes** > **Save to new Project**.</span></span>

4.  <span data-ttu-id="bcbae-156">Pasirinkite projekto **Juridinį subjektą**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-156">Select the **Legal entity** for the project.</span></span>

5.  <span data-ttu-id="bcbae-157">Jeigu reikia, įveskite **Projekto ID**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-157">Enter the **Project ID** , if necessary.</span></span>

6.  <span data-ttu-id="bcbae-158">Įveskite **projekto pavadinimą**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-158">Enter the **Project name**.</span></span>

7.  <span data-ttu-id="bcbae-159">Pasirinkite **Projekto tipas** , **Projekto grupė** ir **Projekto sutarties ID**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-159">Select the **Project type** , **Project group** and the **Project contract ID**.</span></span> <span data-ttu-id="bcbae-160">Arba galite sukurti naują projekto sutartį spustelėję **Nauja**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-160">Alternatively, you can create a new project contract by clicking **New**.</span></span>

8.  <span data-ttu-id="bcbae-161">Pasirinkite **kalendorių** , kurį naudosite paskirstydami išteklius.</span><span class="sxs-lookup"><span data-stu-id="bcbae-161">Select the **Calendar** to be used for resourcing.</span></span>

11. <span data-ttu-id="bcbae-162">Spustelėkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="bcbae-162">Click **OK**.</span></span>
