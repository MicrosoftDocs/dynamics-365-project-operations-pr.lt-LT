---
title: Projektu pagrįstos pasiūlymo eilutės (Pro)
description: Šioje temoje pateikiama informacija apie projektu pagrįstų pasiūlymo eilučių naudojimą projektiniam darbui. (Pro)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: a409d1e378afe97de7fb6c77cf3ad6703661bdff
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908387"
---
# <a name="project-based-quote-lines-pro"></a><span data-ttu-id="cb8cf-104">Projektu pagrįstos pasiūlymo eilutės (Pro)</span><span class="sxs-lookup"><span data-stu-id="cb8cf-104">Project-based quote lines (Pro)</span></span>

<span data-ttu-id="cb8cf-105">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="cb8cf-105">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cb8cf-106">Projektu pagrįstos pasiūlymo eilutės yra skirtos padėti įvertinti projekto darbą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-106">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="cb8cf-107">Projektu pagrįstos pasiūlymo eilutės struktūra yra pratęsta projekto sąmatoms pagal šias sąvokas:</span><span class="sxs-lookup"><span data-stu-id="cb8cf-107">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="cb8cf-108">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-108">Billing Method</span></span>
- <span data-ttu-id="cb8cf-109">Projektų ir užduočių susiejimas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-109">Project and Task Mapping</span></span>
- <span data-ttu-id="cb8cf-110">Įtrauktų operacijų klasės</span><span class="sxs-lookup"><span data-stu-id="cb8cf-110">Included Transaction classes</span></span>
- <span data-ttu-id="cb8cf-111">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="cb8cf-111">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="cb8cf-112">Apmokestinimo sąranka</span><span class="sxs-lookup"><span data-stu-id="cb8cf-112">Chargeability setup</span></span>
- <span data-ttu-id="cb8cf-113">Vertinimas pagal pasiūlymo eilutės išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="cb8cf-113">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="cb8cf-114">Pasiūlymo eilutės klientai</span><span class="sxs-lookup"><span data-stu-id="cb8cf-114">Quote line Customers</span></span>

<span data-ttu-id="cb8cf-115">Šioje lentelėje pateikiama informacija apie laukus, esančius projektu pagrįsto pasiūlymo eilutės skirtuke **Bendroji informacija**.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-115">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="cb8cf-116">Šie laukai padeda nustatyti išsamaus projekto darbo įvertinimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-116">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="cb8cf-117">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="cb8cf-117">**Field**</span></span> | <span data-ttu-id="cb8cf-118">**Atitiktis, tikslas ir gairės**</span><span class="sxs-lookup"><span data-stu-id="cb8cf-118">**Relevance, purpose, and guidance**</span></span> | <span data-ttu-id="cb8cf-119">**Tolesnis poveikis**</span><span class="sxs-lookup"><span data-stu-id="cb8cf-119">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cb8cf-120">Pavadinimas / vardas, pavardė</span><span class="sxs-lookup"><span data-stu-id="cb8cf-120">Name</span></span> | <span data-ttu-id="cb8cf-121">Pasiūlymo eilutės pavadinimas, kuris turėtų padėti nustatyti atskirą vertinamo pasiūlymo komponentą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-121">The name of quote line which should help you identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="cb8cf-122">Nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šios pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-122">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-123">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-123">Billing Method</span></span> | <span data-ttu-id="cb8cf-124">Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš atitinkamo galimybių eilutės lauko.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-124">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="cb8cf-125">Šiame lauke yra du pagrindiniai sutarčių sudarymo modeliai, palaikomi „Dynamics 365 Project Operations":</span><span class="sxs-lookup"><span data-stu-id="cb8cf-125">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="cb8cf-126">- Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="cb8cf-126">- Fixed price</span></span></br><span data-ttu-id="cb8cf-127">- Laikas ir medžiaga.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-127">- Time and material.</span></span>| <span data-ttu-id="cb8cf-128">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-128">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-129">Project</span><span class="sxs-lookup"><span data-stu-id="cb8cf-129">Project</span></span> | <span data-ttu-id="cb8cf-130">Naudokite šį pasirinktinį lauką, kad nustatytumėte projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-130">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="cb8cf-131">Kai projektas susiejamas su pasiūlymo eilute, jis padeda nustatyti apmokestinamąsias užduotis ir su projektu pagrįstu vertinimu pateikti pasiūlymo eilutę kaip pasiūlymo eilutės išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-131">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="cb8cf-132">Kai projektas nesusietas su projektu pagrįsta pasiūlymo eilute, įvertis turėtų būti kuriamas rankiniu būdu sukūrus kiekvienos pasiūlymo eilutės išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-132">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="cb8cf-133">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-133">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="cb8cf-134">Įtrauktos užduotys</span><span class="sxs-lookup"><span data-stu-id="cb8cf-134">Included Tasks</span></span> | <span data-ttu-id="cb8cf-135">Nurodo, ar ši pasiūlymo eilutė naudojama visoms ar kai kurioms pasirinkto projekto užduotims.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-135">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="cb8cf-136">Šis laukas gali turėti tokias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="cb8cf-136">This field has the following possible values:</span></span></br><span data-ttu-id="cb8cf-137">- Visos projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="cb8cf-137">- All project tasks</span></span></br><span data-ttu-id="cb8cf-138">- Tik pasirinktos projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="cb8cf-138">- Selected project tasks only</span></span></br><span data-ttu-id="cb8cf-139">Tuščia šio lauko reikšmė yra lygiavertė parinkčiai **Visos projekto užduotys**.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-139">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="cb8cf-140">Kai pasirinkta **Tik pasirinktos projekto užduotys**, projekto puslapio skirtuke **Užduočių atsiskaitymo sąranka** galite pasirinkti konkrečias užduotis ir susieti jas su šia pasiūlymo eilute.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-140">When **Selected project tasks only** is selected then on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="cb8cf-141">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-141">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-142">Įtraukti laiką</span><span class="sxs-lookup"><span data-stu-id="cb8cf-142">Include Time</span></span> | <span data-ttu-id="cb8cf-143">**Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto laiko operacijos arba darbo išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-143">A **Yes**/**No** flag indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="cb8cf-144">**Ne** vertė nurodo, kad laiko operacijos arba darbo sąnaudos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-144">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="cb8cf-145">**Taip** vertė nurodo, kad laiko operacijos arba darbo sąnaudos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-145">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="cb8cf-146">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-146">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-147">Įtraukti išlaidas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-147">Include Expense</span></span> | <span data-ttu-id="cb8cf-148">**Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-148">A **Yes**/**No** flag indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="cb8cf-149">**Ne** vertė nurodo, kad išlaidos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-149">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="cb8cf-150">**Taip** vertė nurodo, kad išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-150">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="cb8cf-151">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-151">This field value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-152">Įtraukti mokestį</span><span class="sxs-lookup"><span data-stu-id="cb8cf-152">Include Fee</span></span> | <span data-ttu-id="cb8cf-153">**Taip**/**Ne** vėliavėlė nurodo, ar pasirinkto projekto mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-153">A **Yes**/**No** flag indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="cb8cf-154">**Ne** vertė nurodo, kad mokesčiai nebus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-154">A **No** value indicates that the Fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="cb8cf-155">**Taip** vertė nurodo, kad mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-155">A **Yes** value indicates that the Fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="cb8cf-156">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-156">This field value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-157">Pasiūlyta suma</span><span class="sxs-lookup"><span data-stu-id="cb8cf-157">Quoted Amount</span></span> | <span data-ttu-id="cb8cf-158">Tai yra suma, kuri bus pasiūlyta klientui už visus šio projektu pagrįsto pasiūlymo eilutės numatytus darbus.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-158">This is amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="cb8cf-159">Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš galimybių eilutės lauko **Kliento biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-159">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="cb8cf-160">Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal sumą, esančią pasiūlymo eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-160">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="cb8cf-161">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-161">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-162">Įvertintas mokestis</span><span class="sxs-lookup"><span data-stu-id="cb8cf-162">Estimated Tax</span></span> | <span data-ttu-id="cb8cf-163">Tai yra redaguojamas vartotojo laukas, į kurį reikia įtraukti numatomą mokesčio sumą, nurodytą pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-163">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="cb8cf-164">Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal mokesčio sumą, esančią pasiūlymo eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-164">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="cb8cf-165">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-165">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-166">Pasiūlyta suma išskaičius mokestį</span><span class="sxs-lookup"><span data-stu-id="cb8cf-166">Quoted Amount after Tax</span></span> | <span data-ttu-id="cb8cf-167">Šis laukas yra pasiūlymo eilutės suma išskaičius mokesčius; jį galima tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-167">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="cb8cf-168">Šio lauko suma apskaičiuojama kaip *Pasiūlyta suma + mokestis*.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-168">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="cb8cf-169">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-169">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-170">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="cb8cf-170">Not-to-exceed Limit</span></span> | <span data-ttu-id="cb8cf-171">Šį lauką galima redaguoti ir jis yra tik projektu pagrįsto pasiūlymo eilutėse, kuriose yra atsiskaitymo būdas **Laikas ir medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-171">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="cb8cf-172">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-172">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="cb8cf-173">Kliento biudžetas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-173">Customer Budget</span></span> | <span data-ttu-id="cb8cf-174">Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo galimybių eilutės lauko, jei pasiūlymas buvo sukurtas iš galimybės.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-174">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="cb8cf-175">Šio lauko vertė nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šio pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-175">This field value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="cb8cf-176">Su projektu pagrįstų pasiūlymo eilučių skirtuke Bendra laukų tikrinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="cb8cf-176">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="cb8cf-177">**1 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, projektas įtraukiamas į pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-177">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="cb8cf-178">**2 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, į vieną pasiūlymo projektu pagrįsto pasiūlymo eilutę galima įtraukti tik projektą ir tam tikros klasės operacijas.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-178">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="cb8cf-179">**3 taisyklė**: jei laukas **Įtrauktos užduotys** nustatytas kaip **Tik pasirinktos projekto užduotys**, į kelias pasiūlymo projektu pagrįsto pasiūlymo eilutes galima įtraukti projektą ir tam tikros klasės operacijas.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-179">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="cb8cf-180">**4 taisyklė**: jei galimybė turi kelis pasiūlymus, gali būti pasiūlymo eilučių iš skirtingų pasiūlymų, kurie visi nurodo tą patį projektą ir įtraukia tą pačią operacijos klasę.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-180">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="cb8cf-181">**5 taisyklė**: jei pasiūlymai nepriklauso tai pačiai galimybei, jie negali apimti to paties projekto ir operacijos klasės.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-181">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p><span data-ttu-id="cb8cf-182">
                    <strong>Galimybė</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-182">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="cb8cf-183">
                    <strong>Pasiūlymas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-183">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="cb8cf-184">
                    <strong>Pasiūlymo eilutė</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-184">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="cb8cf-185">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-185">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="90" valign="top">
                <p><span data-ttu-id="cb8cf-186">
                    <strong>Įtrauktos užduotys</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-186">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="cb8cf-187">
                    <strong>Įtraukti laiką</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-187">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="cb8cf-188">
                    <strong>Įtraukti išlaidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-188">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="cb8cf-189">
                    <strong>Įterpti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-189">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="cb8cf-190">
                    <strong>Rinkliava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-190">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="54" valign="top">
                <p><span data-ttu-id="cb8cf-191">
                    <strong>Galioja / negalioja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-191">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="308" valign="top">
                <p><span data-ttu-id="cb8cf-192">
                    <strong>Priežastis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="cb8cf-192">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-193">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-193">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-194">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-194">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-195">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-195">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-196">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-196">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-197">Tuščias</span><span class="sxs-lookup"><span data-stu-id="cb8cf-197">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-198">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-198">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-199">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-199">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-200">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-200">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-201">Negalioja</span><span class="sxs-lookup"><span data-stu-id="cb8cf-201">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-202">2 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-202">Violation of Rule #2.</span></span> <span data-ttu-id="cb8cf-203">Laikas, išlaidos ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-203">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-204">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-204">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-205">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-205">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-206">QL2</span><span class="sxs-lookup"><span data-stu-id="cb8cf-206">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-207">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-207">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-208">Tuščias</span><span class="sxs-lookup"><span data-stu-id="cb8cf-208">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-209">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-209">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-210">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-210">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-211">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-211">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="cb8cf-212">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-212">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-213">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-213">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-214">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-214">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-215">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-215">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-216">Tuščias</span><span class="sxs-lookup"><span data-stu-id="cb8cf-216">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-217">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-217">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-218">No</span><span class="sxs-lookup"><span data-stu-id="cb8cf-218">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-219">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-219">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-220">Negalioja</span><span class="sxs-lookup"><span data-stu-id="cb8cf-220">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-221">2 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-221">Violation of Rule #2.</span></span> <span data-ttu-id="cb8cf-222">Laikas ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-222">Time and Fees on P1 project are included on quote lines QL1 and QL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-223">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-223">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-224">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-224">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-225">QL2</span><span class="sxs-lookup"><span data-stu-id="cb8cf-225">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-226">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-226">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-227">Tuščias</span><span class="sxs-lookup"><span data-stu-id="cb8cf-227">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-228">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-228">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-229">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-229">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-230">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-230">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-231">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-231">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-232">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-232">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-233">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-233">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-234">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-234">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-235">Tuščias</span><span class="sxs-lookup"><span data-stu-id="cb8cf-235">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-236">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-236">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-237">No</span><span class="sxs-lookup"><span data-stu-id="cb8cf-237">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-238">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-238">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-239">Tinkama</span><span class="sxs-lookup"><span data-stu-id="cb8cf-239">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                  <p>
<span data-ttu-id="cb8cf-240">P1 projekto laikas ir mokesčiai yra įtraukti į QL1.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-240">Time and Fees on P1 project are included on QL1.</span></span>
<span data-ttu-id="cb8cf-241">P1 projekto išlaidos yra įtrauktos į QL2.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-241">Expense on P1 project is included on QL2.</span></span>
<span data-ttu-id="cb8cf-242">Nepersidengia tai, kas įtraukta į kiekvieną pasiūlymo eilutę, todėl ji galioja.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-242">There is no overlap in what is being included on each quote line and is valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-243">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-243">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-244">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-244">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-245">QL2</span><span class="sxs-lookup"><span data-stu-id="cb8cf-245">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-246">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-246">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-247">Tuščias</span><span class="sxs-lookup"><span data-stu-id="cb8cf-247">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-248">No</span><span class="sxs-lookup"><span data-stu-id="cb8cf-248">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-249">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-249">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-250">No</span><span class="sxs-lookup"><span data-stu-id="cb8cf-250">No</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="cb8cf-251">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-251">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-252">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-252">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-253">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-253">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-254">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-254">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-255">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="cb8cf-255">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-256">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-256">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-257">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-257">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-258">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-258">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-259">Negalioja</span><span class="sxs-lookup"><span data-stu-id="cb8cf-259">Not valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-260">Aukščiau pateiktos 2 taisyklės pažeidimas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-260">Violation of Rule #2 above</span></span> </p>
                <p>
<span data-ttu-id="cb8cf-261">Q1 apima laiką, išlaidas ir mokesčius P1 projekto antriniame užduočių rinkinyje.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-261">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="cb8cf-262">QL2 apima laiką, išlaidas ir mokesčius už visą projektą P1 ir sutampa su tuo, kas įtraukta į pirmąjį ketvirtį.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-262">QL2 includes Time, Expenses, and Fees for the whole project P1 and overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-263">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-263">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-264">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-264">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-265">QL2</span><span class="sxs-lookup"><span data-stu-id="cb8cf-265">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-266">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-266">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-267">Tuščias</span><span class="sxs-lookup"><span data-stu-id="cb8cf-267">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-268">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-268">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-269">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-269">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-270">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-270">Yes</span></span> </p>
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
            <td width="90" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="108" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-271">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-271">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-272">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-272">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-273">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-273">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-274">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-274">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-275">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="cb8cf-275">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-276">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-276">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-277">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-278">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-278">Yes</span></span> </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-279">Tinkama</span><span class="sxs-lookup"><span data-stu-id="cb8cf-279">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-280">Pagal pirmiau nurodytą taisyklę nr. 3</span><span class="sxs-lookup"><span data-stu-id="cb8cf-280">Per Rule #3 above,</span></span> </p>
                <p>
<span data-ttu-id="cb8cf-281">Q1 apima laiką, išlaidas ir mokesčius P1 projekto antriniame užduočių rinkinyje.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-281">Q1 includes Time, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="cb8cf-282">QL2 apima P1 projekto antrinio užduočių rinkinio laiką, išlaidas ir mokesčius.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-282">QL2 includes Time, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="cb8cf-283">Vienintelis papildomas tikrinimas yra apie QL1 užduočių antrinį rinkinį, kuris skiriasi nuo QL2 užduočių antrinio rinkinio.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-283">The only additional validation is around the subset of tasks on QL1 which are different from the subset of tasks on QL2.</span></span> <span data-ttu-id="cb8cf-284">Taip užtikrina persidengimų nebūvimą.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-284">This ensures that there are no overlaps.</span></span> <span data-ttu-id="cb8cf-285">Tai atlieka sistema, kai užduotys yra susietos.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-285">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-286">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-286">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-287">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-287">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-288">QL2</span><span class="sxs-lookup"><span data-stu-id="cb8cf-288">QL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-289">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-289">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-290">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="cb8cf-290">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-291">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-291">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-292">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-292">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-293">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-293">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="cb8cf-294">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-294">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-295">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-295">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-296">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-296">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-297">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-297">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-298">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-298">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-299">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-299">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-300">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-300">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-301">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-301">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="cb8cf-302">Tinkama</span><span class="sxs-lookup"><span data-stu-id="cb8cf-302">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-303">Remiantis taisykle Nr. 5, Q1 ir Q2 yra du tos pačios galimybės pasiūlymai, todėl jie abu gali įvertinti tuos pačius projekto komponentus.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-303">Based on Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-304">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-304">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-305">2 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-305">Q2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-306">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-306">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-307">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-307">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-308">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-308">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-309">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-309">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-310">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-310">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-311">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-311">Yes</span></span> </p>
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
            <td width="90" valign="top">
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
<span data-ttu-id="cb8cf-312">O1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-312">O1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-313">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-313">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-314">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-314">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-315">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-315">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-316">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-316">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-317">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-317">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-318">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-318">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-319">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-319">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="cb8cf-320">Tinkama</span><span class="sxs-lookup"><span data-stu-id="cb8cf-320">Valid</span></span> </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
<span data-ttu-id="cb8cf-321">Remiantis taisykle Nr. 4, Q1 ir Q2 yra du skirtingų galimybių pasiūlymai, todėl jie abu negali įvertinti tų pačių to paties projekto komponentų.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-321">Based on Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of the same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
<span data-ttu-id="cb8cf-322">O2</span><span class="sxs-lookup"><span data-stu-id="cb8cf-322">O2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="cb8cf-323">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="cb8cf-323">Q1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-324">QL1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-324">QL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-325">P1</span><span class="sxs-lookup"><span data-stu-id="cb8cf-325">P1</span></span> </p>
            </td>
            <td width="90" valign="top">
                <p>
<span data-ttu-id="cb8cf-326">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="cb8cf-326">All project tasks or blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-327">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-327">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="cb8cf-328">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-328">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="cb8cf-329">Taip</span><span class="sxs-lookup"><span data-stu-id="cb8cf-329">Yes</span></span> </p>
            </td>
            <td width="54" valign="top">
                <p>
<span data-ttu-id="cb8cf-330">Negalioja</span><span class="sxs-lookup"><span data-stu-id="cb8cf-330">Not Valid</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>

