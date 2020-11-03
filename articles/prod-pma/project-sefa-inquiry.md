---
title: Federalinių subsidijų tyrimo išlaidų grafikas
description: Šioje temoje pateikta informacija apie federalinių subsidijų tyrimo išlaidų grafiką.
author: velofog
manager: Ann Beebe
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: eaf523ab147cbe974fed6e7eab21967404583fe6
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080820"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="98876-103">Federalinių subsidijų tyrimo išlaidų grafikas</span><span class="sxs-lookup"><span data-stu-id="98876-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="98876-104">Pagal Valdymo biuro ir biudžeto aplinkraštį A-133, agentūroms, gaunančioms federalinių lėšų, taikomi audito reikalavimai, kurie dar vadinami pavieniu auditu.</span><span class="sxs-lookup"><span data-stu-id="98876-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="98876-105">Auditas naudojamas siekiant reguliariai pranešti apie federalinių subsidijų pajamas ir išlaidas.</span><span class="sxs-lookup"><span data-stu-id="98876-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="98876-106">Pavienio audito ataskaitos dalyje įtrauktas federalinių subsidijų išlaidų grafikas (SEFA).</span><span class="sxs-lookup"><span data-stu-id="98876-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="98876-107">Federalinių subsidijų tyrimo išlaidų grafike yra vietinės federalinės pagalbos katalogo (CFDA) pavadinimas ir numeris, subsidijos numeris, subsidijos metai, lėšas suteikiančios federalinės agentūros pavadinimas ir tarpininkaujančio subjekto pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="98876-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="98876-108">Tyrimas yra skirtas konkrečiam laikotarpiui.</span><span class="sxs-lookup"><span data-stu-id="98876-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="98876-109">Paprastai tas laikotarpis sutampa su finansinių ataskaitų laikotarpiu – tai yra finansiniai metai.</span><span class="sxs-lookup"><span data-stu-id="98876-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="98876-110">Tyrimas apima subsidijas, kurias planuojama skirti pasirinktą laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="98876-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="98876-111">Tyrimo stulpelyje **Cedento agentūra** rodomas subsidijos klientas arba cedento agentūra (jei subsidija perduodama).</span><span class="sxs-lookup"><span data-stu-id="98876-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="98876-112">Dėl perduodamos subsidijos stulpelyje **Tarpininkavimo agentūra** rodomas subsidijos klientas.</span><span class="sxs-lookup"><span data-stu-id="98876-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="98876-113">Jei subsidija nėra perduodama, stulpelis **Tarpininkavimo agentūra** yra tuščias.</span><span class="sxs-lookup"><span data-stu-id="98876-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="98876-114">CFDA grupių nustatymas</span><span class="sxs-lookup"><span data-stu-id="98876-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="98876-115">Reikia nustatyti CFDA grupes, kurios gali būti susietos su CFDA numeriais federalinių subsidijų tyrimo išlaidų grafike.</span><span class="sxs-lookup"><span data-stu-id="98876-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="98876-116">Eikite į **Projektų valdymas ir apskaita \> Sąranka \> Subsidijos \> Federalinės vietinės pagalbos grupių katalogas**.</span><span class="sxs-lookup"><span data-stu-id="98876-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="98876-117">Pasirinkite **Naujas** norėdami sukurti CFDA grupę.</span><span class="sxs-lookup"><span data-stu-id="98876-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="98876-118">Įveskite grupės pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="98876-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="98876-119">Pasirinkite **Įrašyti** , kad įrašytumėte keitimus.</span><span class="sxs-lookup"><span data-stu-id="98876-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="98876-120">CFDA numerių nustatymas</span><span class="sxs-lookup"><span data-stu-id="98876-120">Set up CFDA numbers</span></span>

<span data-ttu-id="98876-121">Reikia nustatyti CFDA numerius, kurie gali būti įtraukti į subsidijas ir į federalinių subsidijų tyrimo išlaidų grafiką.</span><span class="sxs-lookup"><span data-stu-id="98876-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="98876-122">Eikite į **Projektų valdymas ir apskaita \> Sąranka \> Subsidijos \> Federalinės vietinės pagalbos numerių katalogas**.</span><span class="sxs-lookup"><span data-stu-id="98876-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="98876-123">Pasirinkite **Naujas** norėdami sukurti CFDA numerį.</span><span class="sxs-lookup"><span data-stu-id="98876-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="98876-124">Stulpelyje **Numeris** įveskite CFDA numerį.</span><span class="sxs-lookup"><span data-stu-id="98876-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="98876-125">Paspauskite **Tabuliavimo** klavišą.</span><span class="sxs-lookup"><span data-stu-id="98876-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="98876-126">Stulpelyje **Aprašas** įveskite CFDA pavadinimą.</span><span class="sxs-lookup"><span data-stu-id="98876-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="98876-127">Paspauskite **Tabuliavimo** klavišą.</span><span class="sxs-lookup"><span data-stu-id="98876-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="98876-128">Pasirinktinai: lauke **Programų grupė** įtraukite atitinkamą CFDA grupę.</span><span class="sxs-lookup"><span data-stu-id="98876-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="98876-129">Pasirinkite **Įrašyti** , kad įrašytumėte keitimus.</span><span class="sxs-lookup"><span data-stu-id="98876-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="98876-130">Federalinių subsidijų tyrimo išlaidų grafiko ataskaitos subsidijų nustatymas</span><span class="sxs-lookup"><span data-stu-id="98876-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="98876-131">Eikite į **Projektų valdymas ir apskaita \> Subsidijos \> Subsidijos** ir pasirinkite esamą subsidiją.</span><span class="sxs-lookup"><span data-stu-id="98876-131">Go to **Project management and accounting \> Grants \> Grants** , and select an existing grant.</span></span>
2. <span data-ttu-id="98876-132">„FastTab“ **Sąranka** lauke **Federalinės vietinės pagalbos katalogas** priskirkite CFDA numerį.</span><span class="sxs-lookup"><span data-stu-id="98876-132">On the **Setup** FastTab, in the  **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="98876-133">Subsidijos CFDA numeris nustato ataskaitų CFDA grupę.</span><span class="sxs-lookup"><span data-stu-id="98876-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="98876-134">„FastTab“ **Kontaktinė informacija** įveskite cedento informaciją atlikdami šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="98876-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="98876-135">Lauke **Subsidijos klientas** įveskite už subsidiją atsakingą klientą.</span><span class="sxs-lookup"><span data-stu-id="98876-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="98876-136">Esamos subsidijos informacija jau turbūt įvesta.</span><span class="sxs-lookup"><span data-stu-id="98876-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="98876-137">Nurodykite, ar subsidijos klientas yra finansuotojas.</span><span class="sxs-lookup"><span data-stu-id="98876-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="98876-138">Jei subsidijos klientas yra finansuotojas, žymės langelį **Perduoti** palikite tuščią.</span><span class="sxs-lookup"><span data-stu-id="98876-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="98876-139">Jei finansuotojas yra kitas klientas, o subsidijos klientas atsako už pinigų leidimą ir sekimą, pažymėkite žymės langelį **Perduoti**.</span><span class="sxs-lookup"><span data-stu-id="98876-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="98876-140">Jei ankstesniame veiksme pažymėjote žymės langelį **Perduoti** , lauke **Cedento agentūra** įveskite subsidiją suteikusį klientą.</span><span class="sxs-lookup"><span data-stu-id="98876-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="98876-141">Cedento agentūra ir subsidijos klientas negali būti tas pats klientas.</span><span class="sxs-lookup"><span data-stu-id="98876-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="98876-142">Čia pateikiamas perduodamos subsidijos pavyzdys:</span><span class="sxs-lookup"><span data-stu-id="98876-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="98876-143">Federalinė vyriausybė finansavo valstijos infrastruktūros projektą.</span><span class="sxs-lookup"><span data-stu-id="98876-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="98876-144">Federalinė vyriausybė skyrė lėšų valstijai.</span><span class="sxs-lookup"><span data-stu-id="98876-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="98876-145">Šiuo atveju federalinė vyriausybė yra cedento agentūra, o valstija yra subsidijos klientas.</span><span class="sxs-lookup"><span data-stu-id="98876-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="98876-146">Pirmą kartą įjungus funkciją, pradiniai CFDA numeriai bus įvesti naudojant esamus subsidijų numerius.</span><span class="sxs-lookup"><span data-stu-id="98876-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="98876-147">Subsidijų šalinimas iš SEFA ataskaitų remiantis subsidijų tipu</span><span class="sxs-lookup"><span data-stu-id="98876-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="98876-148">Eikite į **Projektų valdymas ir apskaita \> Sąranka \> Subsidijos \> Subsidijų tipai**.</span><span class="sxs-lookup"><span data-stu-id="98876-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="98876-149">„FastTab“ **Numatytoji informacija** pažymėkite žymės langelį **Pašalinti iš federalinių subsidijų išlaidų grafiko**.</span><span class="sxs-lookup"><span data-stu-id="98876-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="98876-150">Pasirinkite **Įrašyti** , kad įrašytumėte keitimus.</span><span class="sxs-lookup"><span data-stu-id="98876-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="98876-151">Federalinių subsidijų tyrimo išlaidų grafiko vykdymas</span><span class="sxs-lookup"><span data-stu-id="98876-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="98876-152">Eikite į **Projektų valdymas ir apskaita \> Tyrimai ir ataskaitos \> Subsidijos tyrimas \> Federalinių subsidijų išlaidų grafikas**.</span><span class="sxs-lookup"><span data-stu-id="98876-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="98876-153">Skyriuje **Parametrai** atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="98876-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="98876-154">Lauke **Datų intervalas** pasirinkite datų intervalo kodą.</span><span class="sxs-lookup"><span data-stu-id="98876-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="98876-155">Arba laukuose **Pradžios data** ir **Pabaigos data** nustatykite datų intervalą.</span><span class="sxs-lookup"><span data-stu-id="98876-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="98876-156">Pasirinktinai: jei į tyrimą kaip pajamas norite įtraukti tik išrašytų sąskaitų faktūrų operacijas, parinktį **Įtraukti tik išrašytų sąskaitų faktūrų pajamas** nustatykite į **Taip**.</span><span class="sxs-lookup"><span data-stu-id="98876-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="98876-157">Stulpeliai</span><span class="sxs-lookup"><span data-stu-id="98876-157">Columns</span></span>

<span data-ttu-id="98876-158">Federalinių subsidijų tyrimo išlaidų grafike yra šie stulpeliai:</span><span class="sxs-lookup"><span data-stu-id="98876-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="98876-159">Federalinės vietinės pagalbos grupės pavadinimo katalogas</span><span class="sxs-lookup"><span data-stu-id="98876-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="98876-160">Cedento agentūra</span><span class="sxs-lookup"><span data-stu-id="98876-160">Grantor agency</span></span>
- <span data-ttu-id="98876-161">Tarpininkavimo agentūra</span><span class="sxs-lookup"><span data-stu-id="98876-161">Pass-through agency</span></span>
- <span data-ttu-id="98876-162">Subsidijos pavadinimas</span><span class="sxs-lookup"><span data-stu-id="98876-162">Grant name</span></span>
- <span data-ttu-id="98876-163">Subsidijos ID</span><span class="sxs-lookup"><span data-stu-id="98876-163">Grant ID</span></span>
- <span data-ttu-id="98876-164">Subsidijos paraiškos ID</span><span class="sxs-lookup"><span data-stu-id="98876-164">Grant application ID</span></span>
- <span data-ttu-id="98876-165">Federalinė vietinės pagalbos katalogas</span><span class="sxs-lookup"><span data-stu-id="98876-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="98876-166">Kvitai</span><span class="sxs-lookup"><span data-stu-id="98876-166">Receipts</span></span>
- <span data-ttu-id="98876-167">Išlaidos</span><span class="sxs-lookup"><span data-stu-id="98876-167">Expenditures</span></span>
