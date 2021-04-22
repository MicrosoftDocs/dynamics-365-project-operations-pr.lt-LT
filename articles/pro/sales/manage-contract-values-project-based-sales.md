---
title: Projektu pagrįstų sutarties eilučių apžvalga
description: Šioje temoje pateikta informacija apie darbą su projektu pagrįstomis sutarčių eilutėmis.
author: rumant
manager: Annbe
ms.date: 10/28/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 824fdd54d7b513b49afd1a6d76d3387df81418e2
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5858168"
---
# <a name="project-based-contract-lines-overview"></a><span data-ttu-id="8b5ba-103">Projektu pagrįstų sutarties eilučių apžvalga</span><span class="sxs-lookup"><span data-stu-id="8b5ba-103">Project-based contract lines overview</span></span>

<span data-ttu-id="8b5ba-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="8b5ba-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8b5ba-105">Projektu pagrįstos sutarčių eilutės programoje „Dynamics 365 Project Operations“ sukurtos tam tikriems projekto darbo komponentams įvertinti ir atsiskaitymo sutartims pateikti.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-105">Project-based contract lines in Dynamics 365 Project Operations are designed to hold the estimate and billing agreements for specific components of project work on an engagement.</span></span> <span data-ttu-id="8b5ba-106">Projektu pagrįstos sutarties eilutės struktūra išplečiama projektų sąmatų ir sąskaitų išrašymo scenarijams, taikant tolesnes koncepcijas.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-106">The structure of a project–based contract line is extended for project estimates and billing scenarios with the following concepts:</span></span>

- <span data-ttu-id="8b5ba-107">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="8b5ba-107">Billing method</span></span>
- <span data-ttu-id="8b5ba-108">Projektų ir užduočių susiejimas</span><span class="sxs-lookup"><span data-stu-id="8b5ba-108">Project and task mapping</span></span>
- <span data-ttu-id="8b5ba-109">Įtrauktų operacijų klasės</span><span class="sxs-lookup"><span data-stu-id="8b5ba-109">Included transaction classes</span></span>
- <span data-ttu-id="8b5ba-110">Limitas, kurio negalima viršyti</span><span class="sxs-lookup"><span data-stu-id="8b5ba-110">Not-to-exceed limit</span></span>
- <span data-ttu-id="8b5ba-111">Apmokestinimo sąranka</span><span class="sxs-lookup"><span data-stu-id="8b5ba-111">Chargeability setup</span></span>
- <span data-ttu-id="8b5ba-112">Sąmatos naudojant išsamią sutarties eilutės informaciją</span><span class="sxs-lookup"><span data-stu-id="8b5ba-112">Estimates using contract line details</span></span>
- <span data-ttu-id="8b5ba-113">Sutarties eilutės klientai</span><span class="sxs-lookup"><span data-stu-id="8b5ba-113">Contract line customers</span></span>

<span data-ttu-id="8b5ba-114">Šioje lentelėje yra projektu pagrįstų sutarčių eilučių skirtukas **Bendra**, kurio laukai padeda nustatyti detaliojo, visapusiško projektinio darbo sąmatų ir sąskaitų išrašymo tvarką.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-114">The following table includes the fields on the **General** tab of project–based contract lines that help set up the basis for a detailed, ground–up estimate and billing arrangements for project–based work.</span></span>

| <span data-ttu-id="8b5ba-115">Laukas</span><span class="sxs-lookup"><span data-stu-id="8b5ba-115">Field</span></span> | <span data-ttu-id="8b5ba-116">Aprašo</span><span class="sxs-lookup"><span data-stu-id="8b5ba-116">Description</span></span> | <span data-ttu-id="8b5ba-117">Tolesnis poveikis</span><span class="sxs-lookup"><span data-stu-id="8b5ba-117">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8b5ba-118">**Pavadinimas**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-118">**Name**</span></span> | <span data-ttu-id="8b5ba-119">Sutarties eilutės pavadinimas.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-119">Name of the contract line.</span></span> <span data-ttu-id="8b5ba-120">Taip nustatomas atskiras sutarties komponentas, kuris yra vertinamas.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-120">This identifies the discrete component of the contract that is being estimated.</span></span> <span data-ttu-id="8b5ba-121">Vykdant projekto sutartį, sukurtą pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamos projektu pagrįstos pasiūlymo eilutės reikšmės.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-121">For a project contract created from a quote, this value is copied from a corresponding value of the project-based quote line.</span></span> | <span data-ttu-id="8b5ba-122">Pavadinimas, nukopijuotas į projekto sąskaitos faktūros eilutę, sukurtą pagal šią sutarties eilutę sukūrus sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-122">The name copied over to the project invoice line that is created from this contract line when the invoice is created.</span></span> |
| <span data-ttu-id="8b5ba-123">**Atsiskaitymo metodas**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-123">**Billing Method**</span></span> | <span data-ttu-id="8b5ba-124">Vykdant projekto sutartį, sukurtą pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamo lauko pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-124">On a project contract created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8b5ba-125">Tai parinkčių rinkinys, vaizduojantis du pagrindinius sutarčių modelius, kuriuos palaiko „Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-125">This is an option set that represents the two main contracting models supported by Project Operations:</span></span></br><span data-ttu-id="8b5ba-126">- **Fiksuota kaina**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-126">- **Fixed Price**</span></span></br><span data-ttu-id="8b5ba-127">- **Laikas ir medžiagos**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-127">- **Time and Material**</span></span> | <span data-ttu-id="8b5ba-128">Pagal nurodytos sutarties eilutės atsiskaitymo metodą faktinė operacija bus apdorota.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-128">Based on the billing method of the referenced contract line, the actual transaction will be processed.</span></span> <span data-ttu-id="8b5ba-129">Jei sutarties eilutė, į kurią nurodo faktinis įrašas, turi sąskaitų už laiką ir medžiagas išrašymo būdą, kuriami išlaidų ir faktinio pardavimo be sąskaitų įrašai.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-129">If the contract line referenced by the actual has a time and material billing method, cost and unbilled sales actual records are created.</span></span> <span data-ttu-id="8b5ba-130">Jei faktiniame įraše nurodyta sutarties eilutė turi fiksuotą kainos išrašymo metodą, sukuriami tik faktiniai kaštai.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-130">If the contract line referenced by the actual has a fixed price billing method, only a cost actual is created.</span></span> |
| <span data-ttu-id="8b5ba-131">**Project**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-131">**Project**</span></span> | <span data-ttu-id="8b5ba-132">Šį lauką naudokite, jei norite nustatyti projektą, kuris bus naudojamas šiam įsipareigojimui vykdyti.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-132">Use this field to identify the project that will be used to deliver the work on this engagement.</span></span> | <span data-ttu-id="8b5ba-133">Ši reikšmė bus naudojama kartu su **įtrauktomis užduotimis** ir **įtrauktomis operacijos klasėmis**, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-133">This value will be used in conjunction with **Included Tasks** and **Included Transaction Classes** to resolve the contract line reference on an actual or estimate line record.</span></span> |
| <span data-ttu-id="8b5ba-134">**Įtrauktos užduotys**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-134">**Included Tasks**</span></span> | <span data-ttu-id="8b5ba-135">Nurodo, ar šioje sutarties eilutėje yra visos pasirinkto projekto užduotys, ar tik rinkinio užduočių pogrupis.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-135">Indicates if this contract line includes all project tasks for the selected project or only a subset of the tasks.</span></span> <span data-ttu-id="8b5ba-136">Tai yra parinkčių rinkinys, galintis apimti toliau nurodytas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-136">This is an option set that has the following possible values:</span></span></br><span data-ttu-id="8b5ba-137">- **Visos projekto užduotys**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-137">- **All Project Tasks**</span></span></br><span data-ttu-id="8b5ba-138">- **Tik pasirinktos projekto užduotys**.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-138">- **Selected Project Tasks Only**.</span></span> <span data-ttu-id="8b5ba-139">Tuščia šio lauko reikšmė yra lygi **visų projekto užduočių** pasirinkimui.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-139">A blank value in this field is equal to selecting **All Project Tasks**.</span></span> | <span data-ttu-id="8b5ba-140">Jei pasirenkama **Tik pasirinktos užduotys**, galite pažymėti specifines užduotis ir susieti jas su šia sutarties eilute puslapio **Projektas** skirtuke **Sąskaitų išrašymo sąranka**.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-140">If **Selected Tasks Only** is selected, you can select specific tasks and associate them to this contract line on the **Task Billing Setup** tab on the **Project** page.</span></span> <span data-ttu-id="8b5ba-141">Ši reikšmė bus naudojama kartu su klasėmis **Projektas** ir **Įtraukta operacija**, kad būtų išspręsta sutarties eilutės nuoroda faktiniame arba įvertintame eilutės įraše.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-141">The value will be used in conjunction with **Project** and **Included Transaction** classes to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8b5ba-142">**Įtraukti laiką**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-142">**Include Time**</span></span> | <span data-ttu-id="8b5ba-143">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto laiko operacijos arba darbo savikainos bus įtrauktos į sutarties eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-143">A **Yes**/**No** value indicates if time transactions or labor costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8b5ba-144">Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje nebus įtrauktos laiko operacijos ar darbo išlaidos.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-144">A **No** value indicates that the time transactions or labor cost will not be included on this contract line.</span></span> <span data-ttu-id="8b5ba-145">Reikšmė **Taip** nurodo, kad jos bus įtrauktos.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-145">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8b5ba-146">Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-146">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8b5ba-147">**Įtraukti išlaidas**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-147">**Include Expense**</span></span> | <span data-ttu-id="8b5ba-148">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto išlaidos savikainos bus įtrauktos į sutarties eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-148">A **Yes**/**No** value indicates if expense costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8b5ba-149">Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje išlaidų kaštai nebus įtraukti.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-149">A **No** value indicates that the expense cost will not be included on this contract line.</span></span> <span data-ttu-id="8b5ba-150">Reikšmė **Taip** nurodo, kad tai bus įtraukta.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-150">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="8b5ba-151">Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-151">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8b5ba-152">**Įtraukti medžiagas**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-152">**Include Materials**</span></span> | <span data-ttu-id="8b5ba-153">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto medžiagos savikainos bus įtrauktos į sutarties eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-153">A **Yes**/**No** value indicates if material costs on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8b5ba-154">Reikšme **Ne** nurodoma, kad medžiagos savikainos nebus įtrauktos į sutarties eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-154">A **No** value indicates that the material costs will not be included on this contract line.</span></span> <span data-ttu-id="8b5ba-155">Reikšmė **Taip** nurodo, kad tai bus įtraukta.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-155">A **Yes** value indicates that it will.</span></span> | <span data-ttu-id="8b5ba-156">Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-156">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8b5ba-157">**Įtraukti mokestį**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-157">**Include Fee**</span></span> | <span data-ttu-id="8b5ba-158">Reikšme **Taip**/**Ne** nurodoma, ar pasirinkto projekto mokesčiai bus įtraukti į sutarties eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-158">A **Yes**/**No** value indicates if fees on the selected project will be included on this contract line.</span></span> <span data-ttu-id="8b5ba-159">Reikšmė **Ne** nurodo, kad šioje sutarties eilutėje mokesčiai nebus įtraukti.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-159">A **No** value indicates that the fees will not be included on this contract line.</span></span> <span data-ttu-id="8b5ba-160">Reikšmė **Taip** nurodo, kad jos bus įtrauktos.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-160">A **Yes** value indicates that they will.</span></span> | <span data-ttu-id="8b5ba-161">Ši reikšmė naudojama kartu su projektu, kad faktinių duomenų arba įvertinimo eilutės įraše būtų nustatyta sutarties eilutės nuoroda.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-161">This value is used in conjunction with the project to resolve the contract line reference on an actual or an estimate line record.</span></span> |
| <span data-ttu-id="8b5ba-162">**Sutarties suma**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-162">**Contracted Amount**</span></span> | <span data-ttu-id="8b5ba-163">Fiksuotos kainos sutarties eilutėje ši suma yra sutarta reikšmė, kuri bus išrašyta klientui už visus su šia sutarties eilute susietus darbo komponentus.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-163">On a fixed price contract line, this amount is the agreed-on value that will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="8b5ba-164">Laiko ir medžiagų sutarties eilutėje ši suma yra įvertinta reikšmė, kuri bus išrašyta klientui už visus su šia sutarties eilute susietus darbo komponentus.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-164">On a time and material contract line, this amount is an estimated value of what will be invoiced to the customer for all the work components associated to this contract line.</span></span> <span data-ttu-id="8b5ba-165">Vykdant projekto sutartį, kuri sukurta pagal pasiūlymą, ši reikšmė kopijuojama iš atitinkamo lauko pasiūlymo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-165">On a project contract that is created from a quote, this value is copied from the corresponding field on the quote line.</span></span> <span data-ttu-id="8b5ba-166">Kai projektu pagrįstoje sutarties eilutėje pateikiama eilutės informacija, šio lauko neleidžiama redaguoti ir jis apibendrinamas iš sumos, nurodytos sutarties eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-166">When a project–based contract line has line details, this field is locked for editing and is summarized from the amount on the contract line details.</span></span> | <span data-ttu-id="8b5ba-167">Kai sutarties eilutėje yra eilutės informacija, šią reikšmę galima modifikuoti keičiant eilutės išsamios informacijos sumas.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-167">When the contract line has line details, this value can be modified by changing the amounts on the line details.</span></span> <span data-ttu-id="8b5ba-168">Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama sumai iki mokesčių generuoti periodinio atsiskaitymo etapuose.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-168">On a fixed price contract line, this value is used to generate the amount before tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8b5ba-169">**Įvertintas mokestis**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-169">**Estimated Tax**</span></span> | <span data-ttu-id="8b5ba-170">Vartotojas gali redaguoti šį lauką ir įvesti numatomą mokesčio sumą sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-170">The user can edit this field to input the estimated tax amount on the contract line.</span></span> <span data-ttu-id="8b5ba-171">Kai projektu pagrįstoje sutarties eilutėje pateikiama eilutės informacija, šio lauko neleidžiama redaguoti ir jis apibendrinamas iš mokesčių sumos, nurodytos sutarties eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-171">When a project–based contract line has line details, this field is locked for editing and is summarized from the tax amount on the contract line details.</span></span> | <span data-ttu-id="8b5ba-172">Kai sutarties eilutėje yra eilutės informacija, šią reikšmę galima modifikuoti keičiant eilutės išsamios informacijos mokesčių sumas.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-172">When the contract line has line details, this value can be modified by changing the tax amounts on the line details.</span></span> <span data-ttu-id="8b5ba-173">Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama mokesčiams generuoti periodinio atsiskaitymo etapuose.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-173">On a fixed price contract line, this value is used to generate the tax on periodic billing milestones.</span></span> |
| <span data-ttu-id="8b5ba-174">**Sutarties suma po mokesčių**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-174">**Contracted Amount after Tax**</span></span> | <span data-ttu-id="8b5ba-175">Sutarties eilutės suma po mokesčių.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-175">The contract line amount after tax.</span></span> <span data-ttu-id="8b5ba-176">Šis laukas yra tik skaitomas ir apskaičiuojamas kaip **sutarties suma + mokesčiai**.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-176">This field is read only and is calculated as **Contracted Amount + Tax**.</span></span> | <span data-ttu-id="8b5ba-177">Fiksuotos kainos sutarties eilutėje ši reikšmė naudojama periodinio atsiskaitymo etapams generuoti.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-177">On a fixed price contract line, this value is used to generate periodic billing milestones.</span></span> |
| <span data-ttu-id="8b5ba-178">**Limitas, kurio negalima viršyti**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-178">**Not-to-Exceed Limit**</span></span> | <span data-ttu-id="8b5ba-179">Vartotojas gali redaguoti šį lauką ir jis yra prieinamas tik projektu pagrįstose sutarties eilutėse, kurių atsiskaitymo metodas nustatytas kaip laikas ir medžiagos.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-179">The user can edit this field and it is only available on project-based contract lines that have the billing method set as time and material.</span></span> | <span data-ttu-id="8b5ba-180">Vartotojas gali redaguoti šį lauką.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-180">The user can edit this field.</span></span> <span data-ttu-id="8b5ba-181">Kai faktinis laiko ir medžiagų įrašas nurodo šią laiko ir medžiagų sutarties eilutę, faktinio įrašo sumos dydis įvertinamas pagal sutarties eilutės neviršijamą ribą.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-181">When an actual for time and material references this contract line for time and material, the amount on the actual is evaluated against the not-to-exceed limit on the contract line.</span></span> <span data-ttu-id="8b5ba-182">Šis vertinimas baigiamas po to, kai už jau panaudotas ir paskirtas sumas atsiskaitoma.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-182">This evaluation is completed after  the already spent and committed amounts are accounted for.</span></span> |
| <span data-ttu-id="8b5ba-183">**Kliento biudžetas**</span><span class="sxs-lookup"><span data-stu-id="8b5ba-183">**Customer Budget**</span></span> | <span data-ttu-id="8b5ba-184">Šį lauką galima redaguoti ir jis nukopijuojamas iš atitinkamo lauko pasiūlymo eilutėje, jei sutartis buvo sukurta pagal pasiūlymą.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-184">This field is editable and is copied from the corresponding field on the quote line if the contract was created from a quote.</span></span> | <span data-ttu-id="8b5ba-185">Šis laukas naudojamas tik informacijai ir neturi jokios reikšmės tolesnėms operacijoms.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-185">This field is only used for information and does not have any downstream significance.</span></span> |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a><span data-ttu-id="8b5ba-186">Projektu pagrįstų sutarčių eilučių skirtuke Bendra pateiktos parinkčių tikrinimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="8b5ba-186">Validation rules for the options on the General tab of project-based contract lines</span></span>

<span data-ttu-id="8b5ba-187">1 taisyklė: jei laukas **Įtrauktos užduotys** yra tuščias arba nustatytas kaip **Visos projekto užduotys**, visos projekto užduotys įtraukiamos į sutarties eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-187">Rule 1: If the **Included Tasks** field is blank or set to **All Project Tasks**, all tasks of the project are included on the contract line.</span></span>

<span data-ttu-id="8b5ba-188">2 taisyklė: kai laukas **Įtrauktos užduotys** yra tuščias arba aiškiai nustatytas kaip **Visos projekto užduotys**, projektas ir tam tikra operacijų klasė gali būti įtraukti tik į vieną projektu pagrįstą sutarties eilutę.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-188">Rule 2: When the **Included Tasks** field is blank or explicitly set to **All Project Tasks**, a project and a certain transaction class can only be included on one project-based contract line of a contract.</span></span>

<span data-ttu-id="8b5ba-189">3 taisyklė: kai laukas **Įtrauktos užduotys** yra nustatytas kaip **Tik pasirinktos projekto užduotys**, projektas ir tam tikra operacijų klasė gali būti įtraukti į kelias projektu pagrįstas sutarties eilutes.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-189">Rule 3: When the **Included Tasks** field is set to **Selected Project Tasks Only**, a project and a certain transaction class can be included on multiple project-based contract lines of a contract.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p><span data-ttu-id="8b5ba-190">
                    <strong>Sutartis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-190">
                    <strong>Contract</strong>
                </span></span></p>
            </td>
            <td width="65" valign="top">
                <p><span data-ttu-id="8b5ba-191">
                    <strong>Sutarties eilutė</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-191">
                    <strong>Contract line</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8b5ba-192">
                    <strong>Project</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-192">
                    <strong>Project</strong>
                </span></span></p>
            </td>
            <td width="67" valign="top">
                <p><span data-ttu-id="8b5ba-193">
                    <strong>Įtrauktos užduotys</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-193">
                    <strong>Included tasks</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8b5ba-194">
                    <strong>Įtraukti laiką</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-194">
                    <strong>Include Time</strong>
                </span></span></p>
            </td>
            <td width="48" valign="top">
                <p><span data-ttu-id="8b5ba-195">
                    <strong>Įtraukti išlaidas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-195">
                    <strong>Include Expense</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8b5ba-196">
                    <strong>Įtraukti medžiagas</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-196">
                    <strong>Include Materials</strong>
                </span></span></p>
            </td>
            <td width="42" valign="top">
                <p><span data-ttu-id="8b5ba-197">
                    <strong>Įtraukti</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-197">
                    <strong>Include</strong>
                </span></span></p>
                <p><span data-ttu-id="8b5ba-198">
                    <strong>Rinkliava</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-198">
                    <strong>Fee</strong>
                </span></span></p>
            </td>
            <td width="53" valign="top">
                <p><span data-ttu-id="8b5ba-199">
                    <strong>Galioja / negalioja</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-199">
                    <strong>Valid/ Not valid</strong>
                </span></span></p>
            </td>
            <td width="250" valign="top">
                <p><span data-ttu-id="8b5ba-200">
                    <strong>Priežastis</strong>
                </span><span class="sxs-lookup"><span data-stu-id="8b5ba-200">
                    <strong>Reason</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-201">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-201">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-202">CL1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-202">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-203">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-203">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-204">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8b5ba-204">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-205">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-205">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-206">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-206">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-207">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-207">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-208">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-208">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-209">Negalioja</span><span class="sxs-lookup"><span data-stu-id="8b5ba-209">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-210">2 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-210">Violation of Rule #2.</span></span> <span data-ttu-id="8b5ba-211">P1 projekto laikas, išlaidos, medžiagos ir mokesčiai įtraukiami ir abi sutarties eilutes CL1 ir CL2.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-211">Time, Expense, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-212">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-212">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-213">CL2</span><span class="sxs-lookup"><span data-stu-id="8b5ba-213">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-214">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-214">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-215">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8b5ba-215">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-216">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-216">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-217">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-217">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-218">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-218">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-219">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-219">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-220">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-220">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-221">CL1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-221">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-222">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-222">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-223">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8b5ba-223">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-224">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-224">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-225">No</span><span class="sxs-lookup"><span data-stu-id="8b5ba-225">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-226">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-226">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-227">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-227">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-228">Negalioja</span><span class="sxs-lookup"><span data-stu-id="8b5ba-228">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-229">2 taisyklės pažeidimas.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-229">Violation of Rule #2.</span></span> <span data-ttu-id="8b5ba-230">P1 projekto laikas, medžiagos ir mokesčiai įtraukiami ir abi sutarties eilutes CL1 ir CL2.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-230">Time, Materials, and Fees on P1 project are included on both Contract lines CL1 and CL2.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-231">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-231">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-232">CL2</span><span class="sxs-lookup"><span data-stu-id="8b5ba-232">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-233">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-233">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-234">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8b5ba-234">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-235">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-235">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-236">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-236">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-237">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-237">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-238">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-238">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-239">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-239">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-240">CL1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-240">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-241">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-241">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-242">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8b5ba-242">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-243">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-243">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-244">No</span><span class="sxs-lookup"><span data-stu-id="8b5ba-244">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-245">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-245">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-246">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-246">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-247">Tinkama</span><span class="sxs-lookup"><span data-stu-id="8b5ba-247">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-248">P1 projekto laikas, medžiagos ir mokesčiai įtraukiami į CL1.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-248">Time, Materials, and Fees on P1 project are included on CL1.</span></span>
                </p>
                <ul>
                    <li>
<span data-ttu-id="8b5ba-249">P1 projekto išlaidos yra įtrauktos į CL2.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-249">Expense on P1 project is included on CL2.</span></span>
                    </li>
                </ul>
                <p>
<span data-ttu-id="8b5ba-250">Tarp įtraukiamų į kiekvieną sutarties eilutę duomenų persidengimo nėra, todėl jie yra tinkami.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-250">No overlap in what is being included on each Contract line and therefore valid.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-251">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-251">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-252">CL2</span><span class="sxs-lookup"><span data-stu-id="8b5ba-252">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-253">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-253">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-254">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8b5ba-254">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-255">No</span><span class="sxs-lookup"><span data-stu-id="8b5ba-255">No</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-256">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-256">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-257">No</span><span class="sxs-lookup"><span data-stu-id="8b5ba-257">No</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-258">No</span><span class="sxs-lookup"><span data-stu-id="8b5ba-258">No</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-259">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-259">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-260">CL1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-260">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-261">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-261">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-262">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="8b5ba-262">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-263">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-263">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-264">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-264">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-265">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-265">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-266">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-266">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-267">Negalioja</span><span class="sxs-lookup"><span data-stu-id="8b5ba-267">Not valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-268">2 taisyklės pažeidimas</span><span class="sxs-lookup"><span data-stu-id="8b5ba-268">Violation of Rule #2</span></span> </p>
                <p>
<span data-ttu-id="8b5ba-269">C1 apima P1 projekto antrinio užduočių rinkinio laiką, medžiagas, išlaidas ir mokesčius.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-269">C1 includes Time, Materials, Expenses and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8b5ba-270">CL2 apima viso P1 projekto laiką, medžiagas, išlaidas ir mokesčius, todėl persidengia su duomenimis, įtrauktais į C1.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-270">CL2 includes Time, Materials, Expenses and Fees for the whole project P1 and therefore overlaps with what is included on C1.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-271">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-271">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-272">CL2</span><span class="sxs-lookup"><span data-stu-id="8b5ba-272">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-273">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-273">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-274">Tuščias</span><span class="sxs-lookup"><span data-stu-id="8b5ba-274">Blank</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-275">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-275">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-276">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-276">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-277">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-277">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-278">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-278">Yes</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-279">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-279">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-280">CL1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-280">CL1</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-281">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-281">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-282">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="8b5ba-282">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-283">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-283">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-284">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-284">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-285">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-285">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-286">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-286">Yes</span></span> </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-287">Tinkama</span><span class="sxs-lookup"><span data-stu-id="8b5ba-287">Valid</span></span> </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
<span data-ttu-id="8b5ba-288">Pagal taisyklę Nr. 3</span><span class="sxs-lookup"><span data-stu-id="8b5ba-288">Per Rule #3</span></span> </p>
                <p>
<span data-ttu-id="8b5ba-289">C1 apima P1 projekto antrinio užduočių rinkinio laiką, išlaidas, medžiagas ir mokesčius.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-289">C1 includes Time, Expenses, Materials, and Fees on a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8b5ba-290">CL2 apima rinkinio laiką, išlaidas, medžiagas ir mokesčius, skirtus P1 projekto antriniam užduočių rinkiniui.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-290">CL2 includes Time, Expenses, Materials, and Fees for a subset of tasks on project P1.</span></span>
                </p>
                <p>
<span data-ttu-id="8b5ba-291">Vienintelis papildomas tikrinimas atliekamas apie CL1 antrinį užduočių rinkinį ir skiriasi nuo CL2 antrinio užduočių rinkinio, siekiant užtikrinti, kad jame nebus persidengimų.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-291">The only additional validation is around the subset of tasks on CL1 is different from the subset of tasks on CL2 to ensure that there are no overlaps there.</span></span> <span data-ttu-id="8b5ba-292">Tai atlieka sistema, kai užduotys yra susietos.</span><span class="sxs-lookup"><span data-stu-id="8b5ba-292">This is done by the system when tasks are associated.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
<span data-ttu-id="8b5ba-293">C1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-293">C1</span></span> </p>
            </td>
            <td width="65" valign="top">
                <p>
<span data-ttu-id="8b5ba-294">CL2</span><span class="sxs-lookup"><span data-stu-id="8b5ba-294">CL2</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-295">P1</span><span class="sxs-lookup"><span data-stu-id="8b5ba-295">P1</span></span> </p>
            </td>
            <td width="67" valign="top">
                <p>
<span data-ttu-id="8b5ba-296">Tik pasirinktos užduotys</span><span class="sxs-lookup"><span data-stu-id="8b5ba-296">Selected tasks only</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-297">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-297">Yes</span></span> </p>
            </td>
            <td width="48" valign="top">
                <p>
<span data-ttu-id="8b5ba-298">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-298">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-299">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-299">Yes</span></span> </p>
            </td>
            <td width="42" valign="top">
                <p>
<span data-ttu-id="8b5ba-300">Taip</span><span class="sxs-lookup"><span data-stu-id="8b5ba-300">Yes</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
