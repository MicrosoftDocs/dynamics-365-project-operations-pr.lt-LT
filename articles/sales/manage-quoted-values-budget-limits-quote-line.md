---
title: Projekto pasiūlymo eilučių apžvalga
description: Šioje temoje pateikiama informacija apie projekto pasiūlymo eilučių naudojimą projekto darbe.
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996306"
---
# <a name="project-quote-lines-overview"></a><span data-ttu-id="0c109-103">Projekto pasiūlymo eilučių apžvalga</span><span class="sxs-lookup"><span data-stu-id="0c109-103">Project quote lines overview</span></span>

<span data-ttu-id="0c109-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="0c109-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="0c109-105">Projektu pagrįstos pasiūlymo eilutės yra skirtos padėti įvertinti projekto darbą.</span><span class="sxs-lookup"><span data-stu-id="0c109-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="0c109-106">Projektu pagrįstos pasiūlymo eilutės struktūra yra pratęsta projekto sąmatoms pagal šias sąvokas:</span><span class="sxs-lookup"><span data-stu-id="0c109-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="0c109-107">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="0c109-107">Billing Method</span></span>
- <span data-ttu-id="0c109-108">Projektų susiejimas</span><span class="sxs-lookup"><span data-stu-id="0c109-108">Project Mapping</span></span>
- <span data-ttu-id="0c109-109">Įtrauktų operacijų klasės</span><span class="sxs-lookup"><span data-stu-id="0c109-109">Included Transaction classes</span></span>
- <span data-ttu-id="0c109-110">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="0c109-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="0c109-111">Apmokestinimo sąranka</span><span class="sxs-lookup"><span data-stu-id="0c109-111">Chargeability setup</span></span>
- <span data-ttu-id="0c109-112">Vertinimas pagal pasiūlymo eilutės išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="0c109-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="0c109-113">Pasiūlymo eilutės klientai</span><span class="sxs-lookup"><span data-stu-id="0c109-113">Quote line Customers</span></span>

<span data-ttu-id="0c109-114">Šioje lentelėje pateikiama informacija apie laukus, esančius projektu pagrįsto pasiūlymo eilutės skirtuke **Bendroji informacija**.</span><span class="sxs-lookup"><span data-stu-id="0c109-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="0c109-115">Šie laukai padeda nustatyti išsamaus projekto darbo įvertinimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="0c109-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="0c109-116">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="0c109-116">**Field**</span></span> | <span data-ttu-id="0c109-117">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="0c109-117">**Description**</span></span> | <span data-ttu-id="0c109-118">**Tolesnis poveikis**</span><span class="sxs-lookup"><span data-stu-id="0c109-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="0c109-119">Pavadinimas / vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="0c109-119">Name</span></span> | <span data-ttu-id="0c109-120">Pasiūlymo eilutės pavadinimas, kuris turėtų padėti nustatyti atskirą vertinamo pasiūlymo komponentą.</span><span class="sxs-lookup"><span data-stu-id="0c109-120">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="0c109-121">Nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šios pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-122">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="0c109-122">Billing Method</span></span> | <span data-ttu-id="0c109-123">Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš atitinkamo galimybių eilutės lauko.</span><span class="sxs-lookup"><span data-stu-id="0c109-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="0c109-124">Į šį lauką įtraukti du pagrindiniai sutarties modeliai, kuriuos palaiko „Dynamics 365 Project Operations“:</span><span class="sxs-lookup"><span data-stu-id="0c109-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="0c109-125">- Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="0c109-125">- Fixed price</span></span></br><span data-ttu-id="0c109-126">- Laikas ir medžiaga.</span><span class="sxs-lookup"><span data-stu-id="0c109-126">- Time and material.</span></span>| <span data-ttu-id="0c109-127">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-127">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-128">Project</span><span class="sxs-lookup"><span data-stu-id="0c109-128">Project</span></span> | <span data-ttu-id="0c109-129">Naudokite šį pasirinktinį lauką, kad nustatytumėte projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti.</span><span class="sxs-lookup"><span data-stu-id="0c109-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="0c109-130">Kai projektas susiejamas su pasiūlymo eilute, jis padeda nustatyti apmokestinamąsias užduotis ir su projektu pagrįstu vertinimu pateikti pasiūlymo eilutę kaip pasiūlymo eilutės išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="0c109-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="0c109-131">Kai projektas nesusietas su projektu pagrįsta pasiūlymo eilute, įvertis turėtų būti kuriamas rankiniu būdu sukūrus kiekvienos pasiūlymo eilutės išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="0c109-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="0c109-132">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-132">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-133">Įtraukti laiką</span><span class="sxs-lookup"><span data-stu-id="0c109-133">Include Time</span></span> | <span data-ttu-id="0c109-134">**Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto laiko operacijos arba darbo išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-134">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0c109-135">**Ne** vertė nurodo, kad laiko operacijos arba darbo sąnaudos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-135">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0c109-136">**Taip** vertė nurodo, kad laiko operacijos arba darbo sąnaudos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-136">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0c109-137">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-137">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-138">Įtraukti išlaidas</span><span class="sxs-lookup"><span data-stu-id="0c109-138">Include Expense</span></span> | <span data-ttu-id="0c109-139">**Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-139">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0c109-140">**Ne** vertė nurodo, kad išlaidos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-140">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0c109-141">**Taip** vertė nurodo, kad išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-141">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0c109-142">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-142">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-143">Įtraukti mokestį</span><span class="sxs-lookup"><span data-stu-id="0c109-143">Include Fee</span></span> | <span data-ttu-id="0c109-144">**Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-144">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="0c109-145">**Ne** vertė nurodo, kad mokesčiai nebus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-145">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="0c109-146">**Taip** vertė nurodo, kad mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="0c109-146">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="0c109-147">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-147">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-148">Pasiūlyta suma</span><span class="sxs-lookup"><span data-stu-id="0c109-148">Quoted Amount</span></span> | <span data-ttu-id="0c109-149">Tai yra suma, kuri bus pasiūlyta klientui už visus šio projektu pagrįsto pasiūlymo eilutės numatytus darbus.</span><span class="sxs-lookup"><span data-stu-id="0c109-149">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="0c109-150">Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš galimybių eilutės lauko **Kliento biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="0c109-150">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="0c109-151">Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal sumą, esančią pasiūlymo eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="0c109-151">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="0c109-152">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-152">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-153">Įvertintas mokestis</span><span class="sxs-lookup"><span data-stu-id="0c109-153">Estimated Tax</span></span> | <span data-ttu-id="0c109-154">Tai yra redaguojamas vartotojo laukas, į kurį reikia įtraukti numatomą mokesčio sumą, nurodytą pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="0c109-154">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="0c109-155">Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal mokesčio sumą, esančią pasiūlymo eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="0c109-155">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="0c109-156">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-156">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-157">Pasiūlyta suma išskaičius mokestį</span><span class="sxs-lookup"><span data-stu-id="0c109-157">Quoted Amount after Tax</span></span> | <span data-ttu-id="0c109-158">Šis laukas yra pasiūlymo eilutės suma išskaičius mokesčius; jį galima tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="0c109-158">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="0c109-159">Šio lauko suma apskaičiuojama kaip *Pasiūlyta suma + mokestis*.</span><span class="sxs-lookup"><span data-stu-id="0c109-159">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="0c109-160">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-160">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-161">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="0c109-161">Not-to-exceed Limit</span></span> | <span data-ttu-id="0c109-162">Šį lauką galima redaguoti ir jis yra tik projektu pagrįsto pasiūlymo eilutėse, kuriose yra atsiskaitymo būdas **Laikas ir medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="0c109-162">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="0c109-163">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-163">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="0c109-164">Kliento biudžetas</span><span class="sxs-lookup"><span data-stu-id="0c109-164">Customer Budget</span></span> | <span data-ttu-id="0c109-165">Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo galimybių eilutės lauko, jei pasiūlymas buvo sukurtas iš galimybės.</span><span class="sxs-lookup"><span data-stu-id="0c109-165">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="0c109-166">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="0c109-166">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="0c109-167">Su projektu pagrįstų pasiūlymo eilučių skirtuke Bendra laukų tikrinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="0c109-167">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="0c109-168">**1 taisyklė**: tam tikra pasirinkto projekto operacijų klasė gali būti įtraukta tik į vieną pasiūlymo projektu pagrįsto pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="0c109-168">**Rule 1**: A certain transaction class on the selected project can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="0c109-169">**2 taisyklė**: jei galimybė turi kelis pasiūlymus, gali būti pasiūlymo eilučių iš skirtingų pasiūlymų, kurie visi nurodo tą patį projektą ir įtraukia tą pačią operacijos klasę.</span><span class="sxs-lookup"><span data-stu-id="0c109-169">**Rule 2**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="0c109-170">**3 taisyklė**: jei pasiūlymai nepriklauso tai pačiai galimybei, jie negali apimti to paties projekto ir operacijos klasės.</span><span class="sxs-lookup"><span data-stu-id="0c109-170">**Rule 3**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="0c109-171">
                    <strong>Galimybė</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-171">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="0c109-172">
                    <strong>Pasiūlymas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-172">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0c109-173">
                    <strong>Pasiūlymo eilutė</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-173">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0c109-174">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-174">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0c109-175">
                    <strong>Įtraukti laiką</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-175">
                    <strong>Include time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="0c109-176">
                    <strong>Įtraukti išlaidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-176">
                    <strong>Include expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="0c109-177">
                    <strong>Įterpti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-177">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="0c109-178">
                    <strong>mokestis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-178">
                    <strong>fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="0c109-179">
                    <strong>Galioja / negalioja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-179">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="0c109-180">
                    <strong>Priežastis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="0c109-180">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-181">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-181">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-182">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-182">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-183">QL1</span><span class="sxs-lookup"><span data-stu-id="0c109-183">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-184">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-184">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-185">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-185">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-186">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-186">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-187">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-187">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-188">Negalioja</span><span class="sxs-lookup"><span data-stu-id="0c109-188">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-189">1 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="0c109-189">Violation of Rule #1.</span></span> <span data-ttu-id="0c109-190">Laikas, išlaidos ir mokesčiai už P1 projektą įtraukiami į abi pasiūlymo eilutes – QL1 ir QL2.</span><span class="sxs-lookup"><span data-stu-id="0c109-190">Time, Expense, and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-191">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-191">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-192">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-192">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-193">QL2</span><span class="sxs-lookup"><span data-stu-id="0c109-193">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-194">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-194">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-195">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-195">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-196">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-196">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-197">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-197">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-198">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-198">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-199">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-199">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-200">QL1</span><span class="sxs-lookup"><span data-stu-id="0c109-200">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-201">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-201">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-202">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-202">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-203">No</span><span class="sxs-lookup"><span data-stu-id="0c109-203">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-204">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-204">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-205">Negalioja</span><span class="sxs-lookup"><span data-stu-id="0c109-205">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-206">1 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="0c109-206">Violation of Rule #1.</span></span> <span data-ttu-id="0c109-207">Laikas ir mokesčiai už P1 projektą įtraukiami į abi pasiūlymo eilutes – QL1 ir QL2.</span><span class="sxs-lookup"><span data-stu-id="0c109-207">Time and Fees on P1 project are included on both quote lines, QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-208">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-208">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-209">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-209">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-210">QL2</span><span class="sxs-lookup"><span data-stu-id="0c109-210">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-211">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-211">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-212">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-212">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-213">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-213">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-214">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-214">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-215">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-215">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-216">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-216">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-217">QL1</span><span class="sxs-lookup"><span data-stu-id="0c109-217">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-218">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-218">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-219">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-219">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-220">No</span><span class="sxs-lookup"><span data-stu-id="0c109-220">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-221">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-221">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-222">Tinkama</span><span class="sxs-lookup"><span data-stu-id="0c109-222">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
<span data-ttu-id="0c109-223">P1 projekto laikas ir mokesčiai yra įtraukti į QL1.</span><span class="sxs-lookup"><span data-stu-id="0c109-223">Time and fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="0c109-224">P1 projekto išlaidos yra įtrauktos į QL2.</span><span class="sxs-lookup"><span data-stu-id="0c109-224">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="0c109-225">Nepersidengia tai, kas įtraukta į kiekvieną pasiūlymo eilutę, todėl ji galioja.</span><span class="sxs-lookup"><span data-stu-id="0c109-225">There is no overlap in what is being included on each quote line so it is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-226">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-226">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-227">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-227">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-228">QL2</span><span class="sxs-lookup"><span data-stu-id="0c109-228">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-229">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-229">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-230">No</span><span class="sxs-lookup"><span data-stu-id="0c109-230">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-231">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-231">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-232">No</span><span class="sxs-lookup"><span data-stu-id="0c109-232">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-233">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-233">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-234">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-234">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-235">QL1</span><span class="sxs-lookup"><span data-stu-id="0c109-235">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-236">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-236">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-237">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-237">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-238">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-238">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-239">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-239">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-240">Negalioja</span><span class="sxs-lookup"><span data-stu-id="0c109-240">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-241">Aukščiau pateiktos 1 taisyklės pažeidimas</span><span class="sxs-lookup"><span data-stu-id="0c109-241">Violation of Rule #1 above</span></span> </p>
                <p>
<span data-ttu-id="0c109-242">Pirmasis ketvirtis apima laiką, išlaidas ir mokesčius už visą projektą P1.</span><span class="sxs-lookup"><span data-stu-id="0c109-242">Q1 includes Time, Expenses, and Fees for the whole project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="0c109-243">QL2 apima laiką, išlaidas ir mokesčius už visą projektą P1 ir sutampa su tuo, kas įtraukta į pirmąjį ketvirtį.</span><span class="sxs-lookup"><span data-stu-id="0c109-243">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-244">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-244">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-245">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-245">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-246">QL2</span><span class="sxs-lookup"><span data-stu-id="0c109-246">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-247">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-247">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-248">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-248">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-249">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-250">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-250">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-251">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-252">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-253">QL1</span><span class="sxs-lookup"><span data-stu-id="0c109-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-254">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-254">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-255">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-255">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-256">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-257">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-257">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0c109-258">Tinkama</span><span class="sxs-lookup"><span data-stu-id="0c109-258">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-259">Remiantis taisykle Nr. 2, Q1 ir Q2 yra du tos pačios galimybės pasiūlymai, todėl jie abu gali įvertinti tuos pačius projekto komponentus.</span><span class="sxs-lookup"><span data-stu-id="0c109-259">Based on Rule #2, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-260">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-260">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-261">2 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-261">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-262">QL1 Q2</span><span class="sxs-lookup"><span data-stu-id="0c109-262">QL1 on Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-263">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-263">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-264">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-264">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-265">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-266">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-266">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-267">O1</span><span class="sxs-lookup"><span data-stu-id="0c109-267">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-268">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-268">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-269">QL1</span><span class="sxs-lookup"><span data-stu-id="0c109-269">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-270">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-270">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-271">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-271">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-272">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-272">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-273">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-273">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0c109-274">Tinkama</span><span class="sxs-lookup"><span data-stu-id="0c109-274">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="0c109-275">Remiantis taisykle Nr. 3, Q1 ir Q2 yra du skirtingų galimybių pasiūlymai, todėl jie abu negali įvertinti tų pačių to paties projekto komponentų.</span><span class="sxs-lookup"><span data-stu-id="0c109-275">Based on Rule #3, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="0c109-276">O2</span><span class="sxs-lookup"><span data-stu-id="0c109-276">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="0c109-277">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="0c109-277">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-278">QL1</span><span class="sxs-lookup"><span data-stu-id="0c109-278">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-279">P1</span><span class="sxs-lookup"><span data-stu-id="0c109-279">P1</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-280">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-280">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="0c109-281">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-281">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="0c109-282">Taip</span><span class="sxs-lookup"><span data-stu-id="0c109-282">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="0c109-283">Negalioja</span><span class="sxs-lookup"><span data-stu-id="0c109-283">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
