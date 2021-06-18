---
title: Projektu pagrįstų pasiūlymo eilučių apžvalga
description: Šioje temoje pateikiama informacija apie projektu pagrįstų pasiūlymo eilučių naudojimą projektiniam darbui.
author: rumant
ms.date: 03/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 32337b05f09ef7c5b84fdff9870744d6367e2693
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994866"
---
# <a name="project-based-quote-lines-overview"></a><span data-ttu-id="4e1da-103">Projektu pagrįstų pasiūlymo eilučių apžvalga</span><span class="sxs-lookup"><span data-stu-id="4e1da-103">Project-based quote lines overview</span></span> 

<span data-ttu-id="4e1da-104">_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="4e1da-104">_**Applies To:** Lite deployment - deal to proforma invoicing, Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="4e1da-105">Projektu pagrįstos pasiūlymo eilutės yra skirtos padėti įvertinti projekto darbą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-105">Project-based quote lines are designed to help estimate the project work on an engagement.</span></span> <span data-ttu-id="4e1da-106">Projektu pagrįstos pasiūlymo eilutės struktūra yra pratęsta projekto sąmatoms pagal šias sąvokas:</span><span class="sxs-lookup"><span data-stu-id="4e1da-106">The structure of a project-based quote line is extended for project estimates with the following concepts:</span></span>

- <span data-ttu-id="4e1da-107">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="4e1da-107">Billing Method</span></span>
- <span data-ttu-id="4e1da-108">Projektų ir užduočių susiejimas</span><span class="sxs-lookup"><span data-stu-id="4e1da-108">Project and Task Mapping</span></span>
- <span data-ttu-id="4e1da-109">Įtrauktų operacijų klasės</span><span class="sxs-lookup"><span data-stu-id="4e1da-109">Included Transaction classes</span></span>
- <span data-ttu-id="4e1da-110">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="4e1da-110">Not-to-Exceed Limit</span></span>
- <span data-ttu-id="4e1da-111">Apmokestinimo sąranka</span><span class="sxs-lookup"><span data-stu-id="4e1da-111">Chargeability setup</span></span>
- <span data-ttu-id="4e1da-112">Vertinimas pagal pasiūlymo eilutės išsamią informaciją</span><span class="sxs-lookup"><span data-stu-id="4e1da-112">Estimation using Quote Line Details</span></span>
- <span data-ttu-id="4e1da-113">Pasiūlymo eilutės klientai</span><span class="sxs-lookup"><span data-stu-id="4e1da-113">Quote line Customers</span></span>

<span data-ttu-id="4e1da-114">Šioje lentelėje pateikiama informacija apie laukus, esančius projektu pagrįsto pasiūlymo eilutės skirtuke **Bendroji informacija**.</span><span class="sxs-lookup"><span data-stu-id="4e1da-114">The following table provides information about the fields on the **General** tab of project-based quote line.</span></span> <span data-ttu-id="4e1da-115">Šie laukai padeda nustatyti išsamaus projekto darbo įvertinimo pagrindą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-115">These fields help set up the basis for a detailed, ground-up estimation for project work.</span></span>

| <span data-ttu-id="4e1da-116">**Laukas**</span><span class="sxs-lookup"><span data-stu-id="4e1da-116">**Field**</span></span> | <span data-ttu-id="4e1da-117">**Aprašas**</span><span class="sxs-lookup"><span data-stu-id="4e1da-117">**Description**</span></span> | <span data-ttu-id="4e1da-118">**Tolesnis poveikis**</span><span class="sxs-lookup"><span data-stu-id="4e1da-118">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4e1da-119">Pavadinimas / vardas ir pavardė</span><span class="sxs-lookup"><span data-stu-id="4e1da-119">Name</span></span> | <span data-ttu-id="4e1da-120">Pasiūlymo eilutės pavadinimas, padedantis nustatyti diskretišką vertinamo pasiūlymo komponentą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-120">The name of quote line that helps you to identify the discrete component of the quote that is being estimated.</span></span> | <span data-ttu-id="4e1da-121">Nukopijuota į projekto sutarties eilutę, kuri sukuriama iš šios pasiūlymo eilutės laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-121">Copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-122">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="4e1da-122">Billing Method</span></span> | <span data-ttu-id="4e1da-123">Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš atitinkamo galimybių eilutės lauko.</span><span class="sxs-lookup"><span data-stu-id="4e1da-123">On a quote created from an opportunity, this value is copied from the corresponding field on the opportunity line.</span></span> <span data-ttu-id="4e1da-124">Į šį lauką įtraukti du pagrindiniai sutarties modeliai, kuriuos palaiko „Dynamics 365 Project Operations“:</span><span class="sxs-lookup"><span data-stu-id="4e1da-124">This field includes the two main contracting models supported by Dynamics 365 Project Operations:</span></span></br><span data-ttu-id="4e1da-125">- Fiksuota kaina</span><span class="sxs-lookup"><span data-stu-id="4e1da-125">- Fixed price</span></span></br><span data-ttu-id="4e1da-126">- Laikas ir medžiaga.</span><span class="sxs-lookup"><span data-stu-id="4e1da-126">- Time and material.</span></span>| <span data-ttu-id="4e1da-127">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-127">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-128">Project</span><span class="sxs-lookup"><span data-stu-id="4e1da-128">Project</span></span> | <span data-ttu-id="4e1da-129">Naudokite šį pasirinktinį lauką, kad nustatytumėte projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti.</span><span class="sxs-lookup"><span data-stu-id="4e1da-129">Use this optional field to identify the project that will be used to deliver the work on this engagement.</span></span> <span data-ttu-id="4e1da-130">Kai projektas susiejamas su pasiūlymo eilute, jis padeda nustatyti apmokestinamąsias užduotis ir su projektu pagrįstu vertinimu pateikti pasiūlymo eilutę kaip pasiūlymo eilutės išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="4e1da-130">When a project is mapped to a quote line, it helps with setting up chargeable tasks and also with bringing in a project-based estimate to the quote line as quote line details.</span></span> <span data-ttu-id="4e1da-131">Kai projektas nesusietas su projektu pagrįsta pasiūlymo eilute, įvertis turėtų būti kuriamas rankiniu būdu sukūrus kiekvienos pasiūlymo eilutės išsamią informaciją.</span><span class="sxs-lookup"><span data-stu-id="4e1da-131">When a project is not mapped to a project-based quote line, the estimate should be created manually by creating each quote line detail.</span></span> | <span data-ttu-id="4e1da-132">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-132">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span>|
| <span data-ttu-id="4e1da-133">Įtrauktos užduotys</span><span class="sxs-lookup"><span data-stu-id="4e1da-133">Included Tasks</span></span> | <span data-ttu-id="4e1da-134">Nurodo, ar ši pasiūlymo eilutė naudojama visoms ar kai kurioms pasirinkto projekto užduotims.</span><span class="sxs-lookup"><span data-stu-id="4e1da-134">Indicates if this quote line is used for all or some of the project tasks for the selected project.</span></span> <span data-ttu-id="4e1da-135">Šis laukas gali turėti tokias reikšmes:</span><span class="sxs-lookup"><span data-stu-id="4e1da-135">This field has the following possible values:</span></span></br><span data-ttu-id="4e1da-136">- Visos projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="4e1da-136">- All project tasks</span></span></br><span data-ttu-id="4e1da-137">- Tik pasirinktos projekto užduotys</span><span class="sxs-lookup"><span data-stu-id="4e1da-137">- Selected project tasks only</span></span></br><span data-ttu-id="4e1da-138">Tuščia šio lauko reikšmė yra lygiavertė parinkčiai **Visos projekto užduotys**.</span><span class="sxs-lookup"><span data-stu-id="4e1da-138">A blank value in this field is equivalent to the **All project tasks** option.</span></span> | <span data-ttu-id="4e1da-139">Kai projekto puslapyje pasirinkta **Tik pasirinktos projekto užduotys**, skirtuke **Užduočių atsiskaitymo sąranka** galima pasirinkti konkrečias užduotis ir susieti jas su pasiūlymo eilute.</span><span class="sxs-lookup"><span data-stu-id="4e1da-139">When **Selected project tasks only** is selected on the project page, the **Task billing setup** tab allows you to select specific tasks to associate them to this quote line.</span></span> <span data-ttu-id="4e1da-140">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-140">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-141">Įtraukti laiką</span><span class="sxs-lookup"><span data-stu-id="4e1da-141">Include Time</span></span> | <span data-ttu-id="4e1da-142">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto laiko operacijos arba darbo savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-142">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-143">**Ne** vertė nurodo, kad laiko operacijos arba darbo sąnaudos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-143">A **No** value indicates that the time transactions or labor cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-144">**Taip** vertė nurodo, kad laiko operacijos arba darbo sąnaudos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-144">A **Yes** value indicates that the time transactions or labor cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4e1da-145">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-145">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-146">Įtraukti išlaidas</span><span class="sxs-lookup"><span data-stu-id="4e1da-146">Include Expense</span></span> | <span data-ttu-id="4e1da-147">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto išlaidos savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-147">A **Yes**/**No** value indicates if expense costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-148">**Ne** vertė nurodo, kad išlaidos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-148">A **No** value indicates that the expense cost will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-149">**Taip** vertė nurodo, kad išlaidos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-149">A **Yes** value indicates that the expense cost will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4e1da-150">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-150">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-151">Įtraukti medžiagą</span><span class="sxs-lookup"><span data-stu-id="4e1da-151">Include Material</span></span> | <span data-ttu-id="4e1da-152">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto medžiagos savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-152">A **Yes**/**No** value indicates if material costs on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-153">Reikšme **Ne** nurodoma, kad medžiagos savikainos nebus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-153">A **No** value indicates that the material costs will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-154">Reikšme **Taip** nurodoma, kad medžiagos savikainos bus įtrauktos į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-154">A **Yes** value indicates that the material costs will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4e1da-155">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-155">This value is copied over to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-156">Įtraukti mokestį</span><span class="sxs-lookup"><span data-stu-id="4e1da-156">Include Fee</span></span> | <span data-ttu-id="4e1da-157">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-157">A **Yes**/**No** value indicates if fees on the selected project will be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-158">Reikšme **Ne** nurodoma, kad mokesčiai nebus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-158">A **No** value indicates that the fees will not be included in the estimate on this quote line.</span></span> <span data-ttu-id="4e1da-159">Reikšme **Taip** nurodoma, kad mokesčiai bus įtraukti į šio pasiūlymo eilutės įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-159">A **Yes** value indicates that the fees will be included in the estimate on this quote line.</span></span> | <span data-ttu-id="4e1da-160">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-160">This value is copied to the Project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-161">Pasiūlyta suma</span><span class="sxs-lookup"><span data-stu-id="4e1da-161">Quoted Amount</span></span> | <span data-ttu-id="4e1da-162">Tai suma, kuri bus pasiūlyta pirkėjui už visą prognozuojamą darbą šioje projektu pagrįstoje pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4e1da-162">This is the amount that will be quoted to the customer for all the work forecasted on this project-based quote line.</span></span> <span data-ttu-id="4e1da-163">Pasiūlyme, sukurtame iš galimybės, ši vertė nukopijuojama iš galimybių eilutės lauko **Kliento biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="4e1da-163">On a quote created from an opportunity, this value is copied from the **Customer Budget** field on the opportunity line.</span></span> <span data-ttu-id="4e1da-164">Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal sumą, esančią pasiūlymo eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="4e1da-164">When the project-based quote line has line details, this field is locked for editing and is summarized from the amount on the quote line details.</span></span> | <span data-ttu-id="4e1da-165">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-165">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-166">Įvertintas mokestis</span><span class="sxs-lookup"><span data-stu-id="4e1da-166">Estimated Tax</span></span> | <span data-ttu-id="4e1da-167">Tai yra redaguojamas vartotojo laukas, į kurį reikia įtraukti numatomą mokesčio sumą, nurodytą pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="4e1da-167">This is an editable field for the user to add the estimated tax amount on the quote line.</span></span> <span data-ttu-id="4e1da-168">Kai projektu pagrįsto pasiūlymo eilutėje yra eilutės informacija, šis laukas užrakintas (jo redaguoti negalima) ir yra apibendrintas pagal mokesčio sumą, esančią pasiūlymo eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="4e1da-168">When a project-based quote line has line details, this field is locked for editing and is summarized from the tax amount on the quote line details.</span></span> | <span data-ttu-id="4e1da-169">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-169">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-170">Pasiūlyta suma išskaičius mokestį</span><span class="sxs-lookup"><span data-stu-id="4e1da-170">Quoted Amount after Tax</span></span> | <span data-ttu-id="4e1da-171">Šis laukas yra pasiūlymo eilutės suma išskaičius mokesčius; jį galima tik skaityti.</span><span class="sxs-lookup"><span data-stu-id="4e1da-171">This field is the quote line amount after tax and is read-only.</span></span> <span data-ttu-id="4e1da-172">Šio lauko suma apskaičiuojama kaip *Pasiūlyta suma + mokestis*.</span><span class="sxs-lookup"><span data-stu-id="4e1da-172">The amount in this field is calculated as *Quoted Amount + Tax*.</span></span> | <span data-ttu-id="4e1da-173">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-173">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-174">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="4e1da-174">Not-to-exceed Limit</span></span> | <span data-ttu-id="4e1da-175">Šį lauką galima redaguoti ir jis yra tik projektu pagrįsto pasiūlymo eilutėse, kuriose yra atsiskaitymo būdas **Laikas ir medžiagos**.</span><span class="sxs-lookup"><span data-stu-id="4e1da-175">This field is editable and is only available on project-based quote lines that have a **Time and Material** billing method.</span></span> | <span data-ttu-id="4e1da-176">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-176">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |
| <span data-ttu-id="4e1da-177">Kliento biudžetas</span><span class="sxs-lookup"><span data-stu-id="4e1da-177">Customer Budget</span></span> | <span data-ttu-id="4e1da-178">Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo galimybių eilutės lauko, jei pasiūlymas buvo sukurtas iš galimybės.</span><span class="sxs-lookup"><span data-stu-id="4e1da-178">This field is editable and is copied from the corresponding field on the opportunity line if the quote was created from an opportunity.</span></span> | <span data-ttu-id="4e1da-179">Ši reikšmė nukopijuojama į projekto sutarties eilutę, sukuriamą pagal šio pasiūlymo eilutę laimėjus pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="4e1da-179">This value is copied to the project contract line that is created from this quote line when the quote is won.</span></span> |


## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a><span data-ttu-id="4e1da-180">Su projektu pagrįstų pasiūlymo eilučių skirtuke Bendra laukų tikrinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="4e1da-180">Validation rules for fields on the General tab of project-based quote lines</span></span>

<span data-ttu-id="4e1da-181">**1 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, projektas įtraukiamas į pasiūlymo eilutę.</span><span class="sxs-lookup"><span data-stu-id="4e1da-181">**Rule 1**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project is included in the quote line.</span></span>

<span data-ttu-id="4e1da-182">**2 taisyklė**: jei laukas **Įtrauktos užduotys** yra tuščias arba jei jis nustatytas kaip **Visos projekto užduotys**, į vieną pasiūlymo projektu pagrįsto pasiūlymo eilutę galima įtraukti tik projektą ir tam tikros klasės operacijas.</span><span class="sxs-lookup"><span data-stu-id="4e1da-182">**Rule 2**: If the **Included Tasks** field is blank, or if it is set to **All project tasks**, a project and a certain transaction class can only be included on one project-based quote line of a quote.</span></span>

<span data-ttu-id="4e1da-183">**3 taisyklė**: jei laukas **Įtrauktos užduotys** nustatytas kaip **Tik pasirinktos projekto užduotys**, į kelias pasiūlymo projektu pagrįsto pasiūlymo eilutes galima įtraukti projektą ir tam tikros klasės operacijas.</span><span class="sxs-lookup"><span data-stu-id="4e1da-183">**Rule 3**: If the **Included Tasks** field is set to **Selected project tasks only**, a project and a certain transaction class can be included on multiple project-based quote lines of a quote.</span></span>

<span data-ttu-id="4e1da-184">**4 taisyklė**: jei galimybė turi kelis pasiūlymus, gali būti pasiūlymo eilučių iš skirtingų pasiūlymų, kurie visi nurodo tą patį projektą ir įtraukia tą pačią operacijos klasę.</span><span class="sxs-lookup"><span data-stu-id="4e1da-184">**Rule 4**: If an opportunity has multiple quotes, there can be quote lines from different quotes that all reference the same project and include the same transaction class.</span></span>

<span data-ttu-id="4e1da-185">**5 taisyklė**: jei pasiūlymai nepriklauso tai pačiai galimybei, jie negali apimti to paties projekto ir operacijos klasės.</span><span class="sxs-lookup"><span data-stu-id="4e1da-185">**Rule 5**: If the quotes do not belong to the same opportunity, they can't include the same project and transaction class.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="59" valign="top">
                <p><span data-ttu-id="4e1da-186">
                    <strong>Galimybė</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-186">
                    <strong>Opportunity</strong>
                </span></span></p>
            </td>
            <td width="39" valign="top">
                <p><span data-ttu-id="4e1da-187">
                    <strong>Pasiūlymas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-187">
                    <strong>Quote</strong>
                </span></span></p>
            </td>
            <td width="40" valign="top">
                <p><span data-ttu-id="4e1da-188">
                    <strong>Pasiūlymo eilutė</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-188">
                    <strong>Quote line</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="4e1da-189">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-189">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="77" valign="top">
                <p><span data-ttu-id="4e1da-190">
                    <strong>Įtrauktos užduotys</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-190">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="45" valign="top">
                <p><span data-ttu-id="4e1da-191">
                    <strong>Įtraukti laiką</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-191">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="46" valign="top">
                <p><span data-ttu-id="4e1da-192">
                    <strong>Įtraukti išlaidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-192">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="43" valign="top">
                <p><span data-ttu-id="4e1da-193">
                    <strong>Įtraukti medžiagą</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-193">
                    <strong>Include Material</strong>
                </span></span></p>
            </td>
            <td width="41" valign="top">
                <p><span data-ttu-id="4e1da-194">
                    <strong>Įtraukti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-194">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="4e1da-195">
                    <strong>Rinkliava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-195">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="49" valign="top">
                <p><span data-ttu-id="4e1da-196">
                    <strong>Galioja / negalioja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-196">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="200" valign="top">
                <p><span data-ttu-id="4e1da-197">
                    <strong>Priežastis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="4e1da-197">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-198">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-198">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-199">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-199">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-200">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-200">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-201">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-201">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-202">Tuščias</span><span class="sxs-lookup"><span data-stu-id="4e1da-202">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-203">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-203">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-204">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-204">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-205">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-205">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-206">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-206">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-207">Negalioja</span><span class="sxs-lookup"><span data-stu-id="4e1da-207">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-208">2 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="4e1da-208">Violation of Rule #2.</span></span> <span data-ttu-id="4e1da-209">Laikas, išlaidos ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-209">Time, Expense, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-210">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-210">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-211">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-211">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-212">QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-212">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-213">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-213">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-214">Tuščias</span><span class="sxs-lookup"><span data-stu-id="4e1da-214">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-215">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-215">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-216">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-216">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-217">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-217">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-218">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-218">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-219">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-219">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-220">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-220">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-221">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-221">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-222">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-222">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-223">Tuščias</span><span class="sxs-lookup"><span data-stu-id="4e1da-223">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-224">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-224">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-225">No</span><span class="sxs-lookup"><span data-stu-id="4e1da-225">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-226">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-226">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-227">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-227">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-228">Negalioja</span><span class="sxs-lookup"><span data-stu-id="4e1da-228">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-229">2 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="4e1da-229">Violation of Rule #2.</span></span> <span data-ttu-id="4e1da-230">Laikas, medžiagos, išlaidos ir mokesčiai už P1 projektą įtraukiami į pasiūlymo eilutes – QL1 ir QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-230">Time, Material, and Fees on P1 project are included on quote lines QL1 and QL2</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-231">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-231">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-232">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-232">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-233">QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-233">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-234">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-234">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-235">Tuščias</span><span class="sxs-lookup"><span data-stu-id="4e1da-235">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-236">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-236">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-237">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-237">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-238">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-238">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-239">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-239">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-240">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-240">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-241">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-241">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-242">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-242">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-243">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-243">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-244">Tuščias</span><span class="sxs-lookup"><span data-stu-id="4e1da-244">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-245">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-245">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-246">No</span><span class="sxs-lookup"><span data-stu-id="4e1da-246">No</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-247">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-247">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-248">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-248">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-249">Tinkama</span><span class="sxs-lookup"><span data-stu-id="4e1da-249">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-250">P1 projekto laikas, medžiagos ir mokesčiai įtraukiami į QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-250">Time, Material, and Fees on P1 project are included on QL1</span></span> <br>
<span data-ttu-id="4e1da-251">P1 projekto išlaidos yra įtrauktos į QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-251">Expense on P1 project is included on QL2</span></span> <br>
<span data-ttu-id="4e1da-252">Tarp įtraukiamų į kiekvieną pasiūlymo eilutę duomenų persidengimo nėra, todėl jie yra tinkami.</span><span class="sxs-lookup"><span data-stu-id="4e1da-252">No overlap in what is being included on each quote line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-253">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-253">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-254">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-254">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-255">QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-255">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-256">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-256">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-257">Tuščias</span><span class="sxs-lookup"><span data-stu-id="4e1da-257">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-258">No</span><span class="sxs-lookup"><span data-stu-id="4e1da-258">No</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-259">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-259">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-260">No</span><span class="sxs-lookup"><span data-stu-id="4e1da-260">No</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-261">No</span><span class="sxs-lookup"><span data-stu-id="4e1da-261">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-262">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-262">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-263">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-263">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-264">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-264">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-265">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-265">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-266">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="4e1da-266">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-267">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-267">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-268">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-268">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-269">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-269">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-270">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-270">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-271">Negalioja</span><span class="sxs-lookup"><span data-stu-id="4e1da-271">Not valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-272">2 taisyklės pažeidimas</span><span class="sxs-lookup"><span data-stu-id="4e1da-272">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="4e1da-273">Q1 apima P1 projekto antrinio užduočių rinkinio laiką, medžiagą, išlaidas ir mokesčius</span><span class="sxs-lookup"><span data-stu-id="4e1da-273">Q1 includes Time, Material, Expenses and Fees on a subset of tasks on project P1</span></span> </p>
                <p>
<span data-ttu-id="4e1da-274">QL2 apima laiką, išlaidas ir mokesčius už visą P1 projektą, todėl persidengia su tuo, kas įtraukta į Q1.</span><span class="sxs-lookup"><span data-stu-id="4e1da-274">QL2 includes Time, Expenses, and Fees for the whole project P1 and therefore overlaps with what is included on Q1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-275">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-275">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-276">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-276">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-277">QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-277">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-278">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-278">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-279">Tuščias</span><span class="sxs-lookup"><span data-stu-id="4e1da-279">Blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-280">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-280">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-281">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-281">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-282">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-282">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-283">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-283">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-284">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-284">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-285">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-285">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-286">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-286">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-287">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-287">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-288">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="4e1da-288">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-289">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-289">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-290">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-290">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-291">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-291">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-292">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-292">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-293">Tinkama</span><span class="sxs-lookup"><span data-stu-id="4e1da-293">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-294">Pagal taisyklę Nr. 3,</span><span class="sxs-lookup"><span data-stu-id="4e1da-294">Per Rule #3,</span></span> </p>
                <p>
<span data-ttu-id="4e1da-295">Q1 apima P1 projekto antrinio užduočių rinkinio laiką, medžiagą, išlaidas ir mokesčius.</span><span class="sxs-lookup"><span data-stu-id="4e1da-295">Q1 includes Time, Material, Expenses, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4e1da-296">QL2 apima rinkinio laiką, medžiagą, išlaidas, medžiagas ir mokesčius, skirtus P1 projekto antriniam užduočių rinkiniui.</span><span class="sxs-lookup"><span data-stu-id="4e1da-296">QL2 includes Time, Material, Expenses, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="4e1da-297">Vienintelis papildomas tikrinimas atliekamas apie QL1 antrinį užduočių rinkinį, kuris skiriasi nuo QL2 antrinio užduočių rinkinio, siekiant užtikrinti, kad jame nebus persidengimo.</span><span class="sxs-lookup"><span data-stu-id="4e1da-297">The only additional validation is around the subset of tasks on QL1 which is different from the subset of tasks on QL2 to ensure that there is no overlap.</span></span> <span data-ttu-id="4e1da-298">Tai atlieka sistema, kai užduotys yra susietos.</span><span class="sxs-lookup"><span data-stu-id="4e1da-298">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-299">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-299">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-300">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-300">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-301">QL2</span><span class="sxs-lookup"><span data-stu-id="4e1da-301">QL2</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-302">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-302">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-303">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="4e1da-303">Selected tasks only</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-304">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-304">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-305">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-305">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-306">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-306">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-307">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-307">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-308">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-308">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-309">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-309">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-310">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-310">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-311">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-311">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-312">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="4e1da-312">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-313">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-313">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-314">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-314">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-315">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-315">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-316">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-316">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-317">Tinkama</span><span class="sxs-lookup"><span data-stu-id="4e1da-317">Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-318">Pagal 5 taisyklę, Q1 ir Q2 yra du tos pačios galimybės pasiūlymai, todėl juos abu galima taikyti vertinant tuos pačius projekto komponentus.</span><span class="sxs-lookup"><span data-stu-id="4e1da-318">Per Rule #5, Q1 and Q2 are two quotes on the same opportunity, so they can both estimate for the same components of a project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-319">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-319">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-320">2 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-320">Q2</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-321">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-321">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-322">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-322">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-323">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="4e1da-323">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-324">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-324">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-325">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-325">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-326">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-326">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-327">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-327">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
            </td>
            <td width="39" valign="top">
            </td>
            <td width="40" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="77" valign="top">
            </td>
            <td width="45" valign="top">
            </td>
            <td width="46" valign="top">
            </td>
            <td width="43" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="49" valign="top">
            </td>
            <td width="200" valign="top">
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-328">O1</span><span class="sxs-lookup"><span data-stu-id="4e1da-328">O1</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-329">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-329">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-330">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-330">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-331">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-331">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-332">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="4e1da-332">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-333">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-333">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-334">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-334">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-335">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-335">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-336">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-336">Yes</span></span> </p>
            </td>
            <td width="49" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-337">Negalioja</span><span class="sxs-lookup"><span data-stu-id="4e1da-337">Not Valid</span></span> </p>
            </td>
            <td width="200" rowspan="2" valign="top">
                <p>
<span data-ttu-id="4e1da-338">Pagal 4 taisyklę, Q1 ir Q2 yra du skirtingų galimybių pasiūlymai, todėl jų negalima taikyti vertinant tuos pačius to paties projekto komponentus.</span><span class="sxs-lookup"><span data-stu-id="4e1da-338">Per Rule #4, Q1 and Q2 are two quotes on different opportunities, so they can't estimate for the same components of same project.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="59" valign="top">
                <p>
<span data-ttu-id="4e1da-339">O2</span><span class="sxs-lookup"><span data-stu-id="4e1da-339">O2</span></span> </p>
            </td>
            <td width="39" valign="top">
                <p>
<span data-ttu-id="4e1da-340">1 KETV.</span><span class="sxs-lookup"><span data-stu-id="4e1da-340">Q1</span></span> </p>
            </td>
            <td width="40" valign="top">
                <p>
<span data-ttu-id="4e1da-341">QL1</span><span class="sxs-lookup"><span data-stu-id="4e1da-341">QL1</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-342">P1</span><span class="sxs-lookup"><span data-stu-id="4e1da-342">P1</span></span> </p>
            </td>
            <td width="77" valign="top">
                <p>
<span data-ttu-id="4e1da-343">Visos projekto užduotys arba tuščias laukas</span><span class="sxs-lookup"><span data-stu-id="4e1da-343">All project tasks or blank</span></span> </p>
            </td>
            <td width="45" valign="top">
                <p>
<span data-ttu-id="4e1da-344">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-344">Yes</span></span> </p>
            </td>
            <td width="46" valign="top">
                <p>
<span data-ttu-id="4e1da-345">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-345">Yes</span></span> </p>
            </td>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="4e1da-346">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-346">Yes</span></span> </p>
            </td>
            <td width="41" valign="top">
                <p>
<span data-ttu-id="4e1da-347">Taip</span><span class="sxs-lookup"><span data-stu-id="4e1da-347">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
