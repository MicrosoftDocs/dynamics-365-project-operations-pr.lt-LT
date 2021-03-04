---
title: Kaip tinkinti projekto etapų veiklos procesų sekas?
description: Peržiūra, kaip galima tinkinti projekto etapų veiklos procesų seką.
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
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
ms.openlocfilehash: 1d0168f187e6b0880713aac04bd87dbc2209197d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149013"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="39e3c-103">Kaip tinkinti projekto etapų veiklos procesų sekas?</span><span class="sxs-lookup"><span data-stu-id="39e3c-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="39e3c-104">Yra žinoma, kad ankstesnėse „Project Service“ programos versijose egzistuoja apribojimas, dėl kurio etapų pavadinimai projekto etapų veiklos procesų sekoje privalo būti lygiai tokie pat kaip ir numatytieji angliški pavadinimai (**Quote**, **Plan**, **Close**).</span><span class="sxs-lookup"><span data-stu-id="39e3c-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="39e3c-105">Kitu atveju, verslo logika, kuri yra paremta angliškais etapų pavadinimais, neveiks tinkamai.</span><span class="sxs-lookup"><span data-stu-id="39e3c-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="39e3c-106">Būtent dėl to negalite matyti žinomų ir projekto formoje galimų veiksmų, tokių kaip **Perjungti procesą** arba **Redaguoti procesą**, o veiklos procesų sekos tinkinimas nėra skatinamas.</span><span class="sxs-lookup"><span data-stu-id="39e3c-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="39e3c-107">Šis apribojimas panaikintas 2.4.5.48 ir naujesnėse versijose.</span><span class="sxs-lookup"><span data-stu-id="39e3c-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="39e3c-108">Šiame straipsnyje pateikiami siūlomi problemos sprendimai, skirti ankstesnėms versijoms, jei jums reikia tinkinti numatytąją veiklos procesų seką,</span><span class="sxs-lookup"><span data-stu-id="39e3c-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="39e3c-109">Verslo logikai reikalingas tikslus jos ir angliškų etapų pavadinimų atitikimas</span><span class="sxs-lookup"><span data-stu-id="39e3c-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="39e3c-110">Į projekto etapų veiklos procesų seką įtraukta verslo logika, kuri yra šių veiksmų priežastis:</span><span class="sxs-lookup"><span data-stu-id="39e3c-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="39e3c-111">Kai projektas yra susietas su pasiūlymu, kodu nustatomas veiklos procesų sekos etapas **Quote**.</span><span class="sxs-lookup"><span data-stu-id="39e3c-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="39e3c-112">Kai projektas yra susietas su sutartimi, kodu nustatomas veiklos procesų sekos etapas **Plan**.</span><span class="sxs-lookup"><span data-stu-id="39e3c-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="39e3c-113">Kai veiklos procesų seka yra perkeliama į etapą **Close**, projekto įrašas yra išjungiamas.</span><span class="sxs-lookup"><span data-stu-id="39e3c-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="39e3c-114">Kai projektas yra išjungiamas, projekto forma ir darbo paskirstymo struktūra (WBS) nustatomi į režimą „tik skaityti“, įvardyti išteklių rezervavimai yra paleidžiami, o visi susieti kainoraščiai išjungiami.</span><span class="sxs-lookup"><span data-stu-id="39e3c-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="39e3c-115">Ši verslo logika yra paremta angliškais projekto etapų pavadinimais.</span><span class="sxs-lookup"><span data-stu-id="39e3c-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="39e3c-116">Tokia priklausomybė nuo angliškų etapų vadinimų yra pagrindinė priežastis, kodėl nėra skatinamas projektų etapų veiklos procesų sekos tinkinimas, taip pat, kodėl projekto objekte negalite matyti bendrųjų veiklos procesų sekos veiksmų, pavyzdžiui, **„Perjungti procesą“** arba **„Redaguoti procesą“**.</span><span class="sxs-lookup"><span data-stu-id="39e3c-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="39e3c-117">Kas nutinka, jei etapų pavadinimai neatitinka angliškų pavadinimų?</span><span class="sxs-lookup"><span data-stu-id="39e3c-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="39e3c-118">Jei „Project Service“ programos 1.x versijos 8.2 platformoje etapų pavadinimai veiklos procesų sekoje nėra lygiai tokie pat kaip ir angliški etapų pavadinimai, verslo logika, kuria nustatomi tinkami pasiūlymų ar kontraktų etapai, arba uždaromas projektas, yra praleidžiama.</span><span class="sxs-lookup"><span data-stu-id="39e3c-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="39e3c-119">Joks klaidos pranešimas neparodomas.</span><span class="sxs-lookup"><span data-stu-id="39e3c-119">No error messages are displayed.</span></span> <span data-ttu-id="39e3c-120">Todėl atrodytų, kad galite tinkinti projekto etapų veiklos procesų seką.</span><span class="sxs-lookup"><span data-stu-id="39e3c-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="39e3c-121">Vis dėlto, negalėsite matyti jokių automatinių procesų, susijusių su pasiūlymais, sutartimis ir projekto uždarymu.</span><span class="sxs-lookup"><span data-stu-id="39e3c-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="39e3c-122">„Project Service“ programos 2.4.4.30 arba ankstesnės versijos 9.0 platformoje buvo atliktas esminis veiklos procesų sekos architektūros pakeitimas, kuriam buvo būtinas veiklos procesų sekos verslo logikos perrašymas.</span><span class="sxs-lookup"><span data-stu-id="39e3c-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="39e3c-123">To rezultatas – jei proceso etapo pavadinimas ir numatytasis angliškas pavadinimas neatitinka, apie tai informuojama klaidos pranešimu.</span><span class="sxs-lookup"><span data-stu-id="39e3c-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="39e3c-124">Todėl, norėdami tinkinti projekto objekto projekto etapų veiklos procesų seką, galite nebent prie projekto objekto numatytosios veiklos procesų sekos pridėti naujus etapus, **Quote**, **Plan** ir **Close** palikdami tokius, kokie jie yra.</span><span class="sxs-lookup"><span data-stu-id="39e3c-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="39e3c-125">Dėl šio apribojimo būsite tikri, kad jūs negausite klaidų pranešimų dėl verslo logikos, pagal kurią veiklos proceso sekoje turi būti angliški pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="39e3c-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="39e3c-126">Šiame straipsnyje aptariama verslo logika 2.4.5.48 arba naujesnėje versijoje bus pašalinta iš numatytosios projekto objekto veiklos procesų sekos.</span><span class="sxs-lookup"><span data-stu-id="39e3c-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="39e3c-127">Atnaujinę savąją programą į šią arba naujesnę versiją galėsite tinkinti arba pakeisti numatytąją veiklos procesų seką savąja.</span><span class="sxs-lookup"><span data-stu-id="39e3c-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="39e3c-128">Problemos sprendimai senesnėse versijose</span><span class="sxs-lookup"><span data-stu-id="39e3c-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="39e3c-129">Jei atnaujinti programos negalite, galimi du projekto objekto projekto etapų veiklos procesų sekos tinkinimo būdai:</span><span class="sxs-lookup"><span data-stu-id="39e3c-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="39e3c-130">Galite prie numatytosios konfigūracijos pridėti papildomus etapus, tuo pat metu palikdami angliškus etapų .**Quote**, **Plan** ir **Close** pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="39e3c-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![Etapų pridėjimo prie numatytosios konfigūracijos ekrano nuotrauka](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="39e3c-132">Galite sukurti savąją veiklos procesų seką bei ją paversti pirmine projekto objekto veiklos procesų seka, kas leistų jums etapus vadinti taip, kaip norite.</span><span class="sxs-lookup"><span data-stu-id="39e3c-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="39e3c-133">Tačiau jei norite naudoti tuos pačius standartinių projektų etapus **Quote**, **Plan** ir **Close**, turėsite atlikti keletą tinkinimų, po kurių bus pašalinti jūsų pasirinktiniai etapų pavadinimai.</span><span class="sxs-lookup"><span data-stu-id="39e3c-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="39e3c-134">Dar sudėtingesnė yra projekto uždarymo logika, kurią vis vien galite sužadinti tiesiog išjungdami projekto įrašą.</span><span class="sxs-lookup"><span data-stu-id="39e3c-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF tinkinimas](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="39e3c-136">Kitos pastabos dėl „Project Service“ programos 2.4.4.30 arba ankstesnės versijos 9.0 platformoje</span><span class="sxs-lookup"><span data-stu-id="39e3c-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="39e3c-137">„Project Service“ 2.4.4.30 arba ankstesnės versijos 9.0 platformoje, naudojant pasirinktinę veiklos procesų seką, projekto objekto laukas **„Etapo pavadinimas“**, kuris yra naudojamas diagramoje **„Projektas pagal etapą“**, ir projekto sąrašo rodiniai neatsinaujins, nes jie yra susieti su numatytąja projekto etapų veiklos procesų seka.</span><span class="sxs-lookup"><span data-stu-id="39e3c-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="39e3c-138">Šią problemą galite išspręsti atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="39e3c-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="39e3c-139">Įtraukite pasirinktinį lauką ir galėsite užfiksuoti dabartinį veiklos procesų sekos etapą, kuris yra naujinamas vartotojui žengiant per pasirinktinę veiklos procesų seką.</span><span class="sxs-lookup"><span data-stu-id="39e3c-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="39e3c-140">Modifikuokite diagramą **Projektas pagal etapą** ir galėsite dirbti su savo pasirinktiniu lauku, o ne numatytąja konfigūracija.</span><span class="sxs-lookup"><span data-stu-id="39e3c-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="39e3c-141">Asmeninės projekto objekto veiklos procesų sekos sukūrimo žingsniai</span><span class="sxs-lookup"><span data-stu-id="39e3c-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="39e3c-142">Norėdami sukurti asmeninę projekto objekto veiklos procesų seką atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="39e3c-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="39e3c-143">Eikite į **„Parametrai“** > **„Procesų centras“**.</span><span class="sxs-lookup"><span data-stu-id="39e3c-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="39e3c-144">Nekopijuokite projekto etapų veiklos procesų eilės, nes tuomet bus nukopijuota ir „Project Service“ verslo logika.</span><span class="sxs-lookup"><span data-stu-id="39e3c-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![Proceso kūrimas](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="39e3c-146">Naudodami procesų kūrimo įrankį sukurkite norimus etapų pavadinimus.</span><span class="sxs-lookup"><span data-stu-id="39e3c-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="39e3c-147">Jei norite, kad jūsų etapo funkcionalumas būtų toks pat kaip ir numatytųjų etapų **Quote**, **Plan** ir **Close**, kurti etapą turėsite remdamiesi savo pasirinktinės veiklos procesų eilės etapų pavadinimais.</span><span class="sxs-lookup"><span data-stu-id="39e3c-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![Procesų kūrimo įrankio, naudojamo veiklos procesų sekai tinkinti, ekrano nuotrauka](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="39e3c-149">Įėję į procesų kūrimo įrankį, spustelėkite **„Užsakymo proceso seka“** tam, kad pasirinktinę veiklos procesų seką padarytumėte pirmine projekto objekto veiklos procesų seka, ką atliksite ją perkėlę į sąrašo viršų, virš projekto etapų veiklos procesų sekos.</span><span class="sxs-lookup"><span data-stu-id="39e3c-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="39e3c-150">Parinkties Užsakymo proceso seka naudojimo ekrano nuotrauka</span><span class="sxs-lookup"><span data-stu-id="39e3c-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="39e3c-151">Šie veiksmai gali būti taikomi programos „Project Service“ 2.4.4.30 arba ankstesnės versijos 9.0 platformoje</span><span class="sxs-lookup"><span data-stu-id="39e3c-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="39e3c-152">Įtraukite naują pasirinktinį lauką į projekto objektą, kad užfiksuotumėte jūsų pasirinktinės veiklos procesų sekos pasirinktinius etapus.</span><span class="sxs-lookup"><span data-stu-id="39e3c-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="39e3c-153">Jums reikės pridėti verslo logiką (priedas/darbo eiga) tam, kad šis laukas būtų atnaujinamas, kada atnaujinamas ir pasirinktinės veiklos procesų sekos etapas.</span><span class="sxs-lookup"><span data-stu-id="39e3c-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![Projekto objekto tinkinimo ekrano nuotrauka](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="39e3c-155">Modifikuokite diagramą **„Projektas pagal etapą“** ir galėsite naudoti savo naujuosius pasirinktinius laukus etapams.</span><span class="sxs-lookup"><span data-stu-id="39e3c-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![Diagramos Projektas pagal etapą naudojimo ekrano nuotrauka](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="39e3c-157">Modifikuokite visus projekto objekto rodinius kad etapams galėtumėte įtraukti savo naujuosius pasirinktinius laukus.</span><span class="sxs-lookup"><span data-stu-id="39e3c-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![Rodinių modifikavimo projekto objekte ekrano nuotrauka](media/FAQ-Customize-BPF-8-720.png)

