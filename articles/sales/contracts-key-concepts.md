---
title: Projekto sutartys – pagrindinės sąvokos
description: Šioje temoje pateikta informacija apie pagrindines projekto sutarčių sąvokas programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b0e0280cb94e6f0186f59024c233e8fcb9e86abf
ms.sourcegitcommit: df30839484ef278675c5c712af0f7ba66ed9cdd3
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/17/2021
ms.locfileid: "5663732"
---
# <a name="concepts-unique-to-project-based-contracts"></a><span data-ttu-id="7f0c3-103">Unikalios projektu pagrįstų sutarčių sąvokos</span><span class="sxs-lookup"><span data-stu-id="7f0c3-103">Concepts unique to Project-based Contracts</span></span>

<span data-ttu-id="7f0c3-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="7f0c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="7f0c3-105">Šioje temoje pateikiamos pagrindinės sąvokos, kurias reikia žinoti prieš pradedant naudoti projektų sutartis programoje „Dynamics 365 Project Operations“:</span><span class="sxs-lookup"><span data-stu-id="7f0c3-105">This topic provides the key concepts to be aware of before you begin using Project contracts in Dynamics 365 Project Operations:</span></span>

## <a name="owning-company"></a><span data-ttu-id="7f0c3-106">Įmonė, kuriai priklauso</span><span class="sxs-lookup"><span data-stu-id="7f0c3-106">Owning Company</span></span>

<span data-ttu-id="7f0c3-107">Valdančioji įmonė yra juridinis subjektas iš „Project Operations“ modulis **Projekto valdymas ir apskaita** iš „Dynamics 365 Finance“.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-107">The owning company is the legal entity from the **Project management and accounting** module for Project Operations from Dynamics 365 Finance.</span></span> <span data-ttu-id="7f0c3-108">Valdanti įmonė yra juridinis subjektas, kuris bus atsakingas už išlaidas ir pajamas, susidariusias iš sandorio.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-108">The owning company represents the legal entity that will account for the cost and revenue that accrues from a deal.</span></span>

## <a name="contracting-unit"></a><span data-ttu-id="7f0c3-109">Sutartį sudarantis vienetas</span><span class="sxs-lookup"><span data-stu-id="7f0c3-109">Contracting Unit</span></span>

<span data-ttu-id="7f0c3-110">Sutartį sudarantis vienetas yra padalinys arba praktika, kuriai priklauso projekto pristatymas.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-110">The contracting unit represents the division or practice that owns the delivery of the project.</span></span> <span data-ttu-id="7f0c3-111">Galite nustatyti kiekvieno sutarties vieneto išteklių savikainą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-111">You can set up resource costs for each contracting unit.</span></span> <span data-ttu-id="7f0c3-112">Kai nurodote ištekliaus savikainą, taip pat galėsite nustatyti skirtingus išteklių savikainos tarifus.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-112">When you specify the resource cost for a resource, you will also be able to set up different cost rates for resources.</span></span> <span data-ttu-id="7f0c3-113">Šis sutartį sudarantis vienetas skolinasi šiuos išteklius iš kito įmonės padalinio arba praktikos.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-113">This contracting unit borrows these resources from other division or practices within the enterprise.</span></span> <span data-ttu-id="7f0c3-114">Išteklių savikainos tarifai yra pervedimų kainos, išteklių skolinimasis arba valiutų kainos.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-114">The cost rates for the resources are referred to as transfer prices, resource borrowing, or exchange prices.</span></span> <span data-ttu-id="7f0c3-115">Nustatydami išteklių skolinimosi iš kitų padalinių savikainos tarifus, naudokite skolinimo padalinio valiutą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-115">When you set up the cost rates to borrow resources from other divisions, use the currency of the lending division.</span></span>

## <a name="cost-currency"></a><span data-ttu-id="7f0c3-116">Savikainos valiuta</span><span class="sxs-lookup"><span data-stu-id="7f0c3-116">Cost Currency</span></span>

<span data-ttu-id="7f0c3-117">Savikainos valiuta yra valiuta, kuria ekrane pateikiama savikaina.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-117">Cost currency is the currency in which costs are reported on screen.</span></span> <span data-ttu-id="7f0c3-118">Ši valiuta gaunama iš valiutos, susietos su lauku **Sutartį sudarantis vienetas**, esančiu sutartyje ir projekte.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-118">This currency is derived from the currency attached to the **Contracting Unit** field on the contract and the project.</span></span> <span data-ttu-id="7f0c3-119">Išlaidas galima registruoti bet kuria valiuta projekte.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-119">Costs can be logged in any currency against a project.</span></span> <span data-ttu-id="7f0c3-120">Tačiau tada nurodomas valiutos konvertavimas iš valiutos, kuria užregistruota savikaina, į projekto išlaidų valiutą, kai rodoma ekrane.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-120">However, there is currency conversion from the currency the costs were recorded in, to the cost currency of the project when shown on the screen.</span></span>

<span data-ttu-id="7f0c3-121">Kadangi „Common Data Service“ (CDS) platformos valiutų kursai nėra galiojantys pagal datą, todėl, jei atnaujinate valiutos keitimo kursus, ekrane savikainos sumos gali pasikeisti.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-121">Because the exchange rates in the Common Data Service (CDS) platform can't be date effective, the on-screen totals for cost may change over time if you update the currency exchange rates.</span></span> <span data-ttu-id="7f0c3-122">Tačiau savikainos, įrašytos į duomenų bazę, lieka nepakitusios, nes sumos saugomos valiuta, kuria jos patirtos.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-122">However, costs as recorded in the database remain unchanged because the amounts are stored in the currency that were incurred in.</span></span>

## <a name="sales-currency"></a><span data-ttu-id="7f0c3-123">Pardavimo valiuta</span><span class="sxs-lookup"><span data-stu-id="7f0c3-123">Sales Currency</span></span>

<span data-ttu-id="7f0c3-124">Pardavimo valiuta, naudojama „Project Operations“, yra valiuta, kuria yra įrašytos ir rodomos apskaičiuotos bei faktinės pardavimo sumos.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-124">Sales currency in Project Operations is the currency in which the estimated and actual sales amounts are recorded and shown.</span></span> <span data-ttu-id="7f0c3-125">Pardavimo valiuta taip pat yra valiuta, kuria klientui išrašyta sąskaita faktūra už sandorį.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-125">Sales currency is also the currency in which the customer is invoiced for the deal.</span></span> <span data-ttu-id="7f0c3-126">Projekto sutartyje pardavimo valiuta gaunama iš kliento įrašo ir ją galima pakeisti, kai sukuriama sutartis.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-126">On a project contract, the sales currency defaults from the customer or account record and can be changed during when the contract is created.</span></span> <span data-ttu-id="7f0c3-127">Kai sutartis sukuriama uždarant pasiūlymą kaip laimėtą, sutarties valiuta nustatoma pagal pasiūlymo valiutą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-127">When a contract is created by closing a quote as won, the currency on the contract is defaulted from the currency on the quote.</span></span>

<span data-ttu-id="7f0c3-128">Kai kuriate projekto sutartį nuo nulio, lauko **Pardavimo valiuta** redaguoti negalima.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-128">When you create a project contract from scratch, the **Sales Currency** field can't be edited.</span></span> <span data-ttu-id="7f0c3-129">Produkto ir projekto kainoraščiai yra numatytieji sąrašai pagal šią sutarties valiutą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-129">Product and project price lists default based on this currency on the contract.</span></span>

<span data-ttu-id="7f0c3-130">Kitaip nei savikainos, pardavimo reikšmės gali būti įrašytos tik pardavimo valiuta.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-130">Unlike costs, sales values can only be recorded in the sales currency.</span></span>

## <a name="billing-method"></a><span data-ttu-id="7f0c3-131">Atsiskaitymo metodas</span><span class="sxs-lookup"><span data-stu-id="7f0c3-131">Billing Method</span></span>

<span data-ttu-id="7f0c3-132">Projektuose paprastai yra dviejų tipų sutarties sudarymo modeliai – pagrįsti fiksuotais mokesčiais ir suvartojimu.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-132">There are typically two types of contracting models for projects, fixed fee and consumption-based.</span></span> <span data-ttu-id="7f0c3-133">„Project Operations“ šie modeliai nurodomi kaip atsiskaitymo būdai su dviem galimomis reikšmėmis.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-133">These models are represented in Project Operations as billing methods with two possible values:</span></span>

- <span data-ttu-id="7f0c3-134">Laikas ir Medžiaga: suvartojimu pagrįstas sutarties sudarymo modelis, kai kiekvienas patirtas išlaidas kompensuoja atitinkamos pajamos.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-134">Time and Material: A consumption-based contracting model where each incurred cost is backed by corresponding revenue.</span></span> <span data-ttu-id="7f0c3-135">Kai numatote arba patiriate daugiau išlaidų, atitinkami numatyti ir faktiniai pardavimai taip pat bus padidinti.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-135">As you estimate or incur more costs, the corresponding estimated and actual sales also increase.</span></span> <span data-ttu-id="7f0c3-136">Nurodykite neviršytinus limitus sutarties eilutėse, naudojančiose šį atsiskaitymo būdą, kuris panaikina faktinių pajamų viršutinę ribą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-136">Specify not-to-exceed limits on contract lines that have this billing method, which caps off the actual revenue.</span></span> <span data-ttu-id="7f0c3-137">Numatytų pajamų ribos neviršijimo apribojimas įtakos neturi.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-137">Estimated revenue isn't impacted by not-to-exceed limits.</span></span>
- <span data-ttu-id="7f0c3-138">Fiksuota kaina: fiksuoto mokesčio sutarties sudarymo modelis, nurodantis, kad pardavimo reikšmės bus nepriklausomos nuo patirtų išlaidų.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-138">Fixed Price: A fixed fee contracting model that indicates the sales values will be independent of the costs incurred.</span></span> <span data-ttu-id="7f0c3-139">Pardavimo reikšmė yra fiksuota ir ji nekinta, kai numatote arba patiriate daugiau išlaidų.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-139">The sales value is fixed and doesn't change as you estimate or incur more costs.</span></span>

## <a name="project-price-lists"></a><span data-ttu-id="7f0c3-140">Projekto kainoraščiai</span><span class="sxs-lookup"><span data-stu-id="7f0c3-140">Project Price lists</span></span>

<span data-ttu-id="7f0c3-141">Projekto kainoraščiai naudojami numatytajai kainai (ne išlaidų tarifams), laikui, išlaidoms ir kitiems su projektu susijusiems komponentams.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-141">Project price lists are used to default prices, not cost rates, for time, expense, and other project-related components.</span></span> <span data-ttu-id="7f0c3-142">Gali būti keletas kainoraščių.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-142">There can be multiple prices lists.</span></span> <span data-ttu-id="7f0c3-143">Kiekviename kainoraštyje nustatoma atskira kiekvienos projekto sutarties įsigaliojimo data.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-143">Each price list has its own date effectivity for each project contract.</span></span> <span data-ttu-id="7f0c3-144">„Project Operations“ nepalaiko persidengiančių projekto kainoraščių galiojimo datų.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-144">Overlapping date-effectivity on project price lists isn't supported in Project Operations.</span></span>

<span data-ttu-id="7f0c3-145">Kai projekto sutartis sukuriama laimėjus projekto pasiūlymą, projekto kainoraščiai nukopijuojami nurodant sutarties pavadinimą ir datą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-145">When a project contract is created by winning a project quote, project price lists are copied with the contract name and date included.</span></span> <span data-ttu-id="7f0c3-146">Šios informacijos kopijavimas yra projekto komponentų pasirinktinė kainodara šioje projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-146">Copying this information constitutes custom pricing for project components on this project contract.</span></span>

## <a name="transaction-classes"></a><span data-ttu-id="7f0c3-147">Operacijų klasės</span><span class="sxs-lookup"><span data-stu-id="7f0c3-147">Transaction Classes</span></span>

<span data-ttu-id="7f0c3-148">„Project Operations“ palaiko keturis operacijų klasių tipus:</span><span class="sxs-lookup"><span data-stu-id="7f0c3-148">Project Operations supports four types of transaction classes:</span></span>

- <span data-ttu-id="7f0c3-149">Laikas</span><span class="sxs-lookup"><span data-stu-id="7f0c3-149">Time</span></span>
- <span data-ttu-id="7f0c3-150">Išlaidos</span><span class="sxs-lookup"><span data-stu-id="7f0c3-150">Expense</span></span>
- <span data-ttu-id="7f0c3-151">Medžiaga</span><span class="sxs-lookup"><span data-stu-id="7f0c3-151">Material</span></span>
- <span data-ttu-id="7f0c3-152">Rinkliava</span><span class="sxs-lookup"><span data-stu-id="7f0c3-152">Fee</span></span>

<span data-ttu-id="7f0c3-153">Išlaidų ir pardavimo reikšmės gali būti numatytos ir patirtos pagal laiko, išlaidų ir medžiagų operacijų klases.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-153">Cost and sales values can be estimated and incurred on Time, Expense, and Material transaction classes.</span></span> <span data-ttu-id="7f0c3-154">Mokestis yra tik pajamų operacijų klasė.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-154">Fee is a revenue-only transaction class.</span></span>

## <a name="work-entities-and-billing-entities"></a><span data-ttu-id="7f0c3-155">Darbo objektai ir atsiskaitymo objektai</span><span class="sxs-lookup"><span data-stu-id="7f0c3-155">Work entities and Billing entities</span></span>

<span data-ttu-id="7f0c3-156">Objektai, nurodantys darbą, yra projektai ir užduotys.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-156">Entities that represent work are projects and tasks.</span></span> <span data-ttu-id="7f0c3-157">Objektai, kurie nurodo atsiskaitymą aspektus, yra sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-157">Entities that represent billing aspects are contract lines.</span></span> <span data-ttu-id="7f0c3-158">Galite susieti skirtingus darbo objektus su atsiskaitymo parinktimis, susiedami juos su sutarties eilutėmis.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-158">You can tie different work entities to billing options by tying them to contract lines.</span></span>

## <a name="multi-customer-deals"></a><span data-ttu-id="7f0c3-159">Kelių klientų sandoriai</span><span class="sxs-lookup"><span data-stu-id="7f0c3-159">Multi-customer deals</span></span>

<span data-ttu-id="7f0c3-160">Su kelių klientų sandoriais susiduriama, kai sandorį sudaro daugiau nei vienas sąskaitos faktūros klientas.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-160">Multi- customer deals have more than one customer to invoice on a deal.</span></span> <span data-ttu-id="7f0c3-161">Įprasti pavyzdžiai gali būti:</span><span class="sxs-lookup"><span data-stu-id="7f0c3-161">Common examples of this include:</span></span>

- <span data-ttu-id="7f0c3-162">„OEM Enterprises“ ir jos partneriai: partneriai ir pardavėjai parduoda produktą su tam tikromis pridėtinės vertės paslaugomis ir paprastai įtraukia konkretų pasiūlymą klientui.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-162">OEM Enterprises and their partners: Partners and resellers sell a product with some value-added services, typically involving a particular deal with a customer.</span></span> <span data-ttu-id="7f0c3-163">OEM siūlo finansuoti projekto dalį.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-163">The OEM offers to finance a portion of the project.</span></span> 

- <span data-ttu-id="7f0c3-164">Viešojo sektoriaus projektai keli vietos valdžios institucijų skyriai sutaria finansuoti projektą ir į sąskaitą faktūrą įtraukiami pagal anksčiau suderintas dalis.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-164">Public sector projects: Multiple departments of a local government agree to fund a project and are invoiced according to a previously agreed split.</span></span> <span data-ttu-id="7f0c3-165">Pavyzdžiui, mokyklos skyrius ir vietos valstybinė institucija susitaria finansuoti baseino pastatą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-165">For example, s school district and the local government agree to fund the building of a swimming pool.</span></span>

## <a name="invoice-schedules"></a><span data-ttu-id="7f0c3-166">Sąskaitos faktūros grafikai</span><span class="sxs-lookup"><span data-stu-id="7f0c3-166">Invoice Schedules</span></span>

<span data-ttu-id="7f0c3-167">Sąskaitos faktūros grafikai taikomi kiekvienai konkrečiai sutarties eilutei ir jie reikalingi išrašant automatines sąskaita faktūras.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-167">Invoice schedules are specific to each contract line and are required for automatic invoicing to work.</span></span> <span data-ttu-id="7f0c3-168">Sąskaitų faktūrų grafikai kuriami pagal tam tikras pradžios ir pabaigos datas bei sąskaitų faktūrų dažnumą.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-168">Invoice schedules are created based on certain start and finish dates and invoice frequency.</span></span> <span data-ttu-id="7f0c3-169">Grafikai naudojami sutarties etape, kai konfigūruojamas automatinis sąskaitos faktūros kūrimo procesas.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-169">The schedules are used in the contract stage when the automatic invoice creation process is configured.</span></span> <span data-ttu-id="7f0c3-170">Kai projekto sutartis sukuriama iš pasiūlymo, sąskaitos faktūros grafikas nukopijuojamas į projekto sutartį iš pasiūlymo.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-170">When a project contract is created from a quote, the invoice schedule is copied to the project contract from the quote.</span></span>

## <a name="changes-from-dynamics-365-sales-orders"></a><span data-ttu-id="7f0c3-171">Pasikeitimai iš „Dynamics 365 Sales“ pasiūlymų</span><span class="sxs-lookup"><span data-stu-id="7f0c3-171">Changes from Dynamics 365 Sales Orders</span></span>

<span data-ttu-id="7f0c3-172">„Project Operations“ sutartys kuriamos „Dynamics 365 Sales“ užsakymuose.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-172">Contracts in Project Operations are built on Orders in Dynamics 365 Sales.</span></span> <span data-ttu-id="7f0c3-173">Tačiau yra svarbių funkcijų skirtumų.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-173">However, there are important deviations and differences in functionality.</span></span> <span data-ttu-id="7f0c3-174">Sutartys turi savus formos ir UI elementus, verslo taisykles, verslo logiką papildiniuose ir kliento scenarijus, kuriais jos ir skiriasi nuo užsakymų.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-174">Contracts have their own form and UI elements, business rules, business logic in plug-ins, and client-side scripts that make them unique from Orders.</span></span> <span data-ttu-id="7f0c3-175">Dėl šių priežasčių „Sales“ užsakymo ir „Project Operations“ sutarties apkeisti vietomis negalima.</span><span class="sxs-lookup"><span data-stu-id="7f0c3-175">For these reasons, don't use a Sales order and Project Operations contract interchangeably.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]