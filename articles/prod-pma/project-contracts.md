---
title: Projekto sutartys
description: Šioje temoje pateikiami projekto sutarčių, kurias galite kurti įvairiems projektų tipams ir finansavimo šaltiniams, pavyzdžiai, taip pat sutarčių tvarkymo ir sąskaitų faktūrų išrašymo projektų klientams pavyzdžiai.
author: Yowelle
ms.date: 11/03/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjProjectsListPage
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23561
ms.assetid: bfd18d9b-d9a6-4e21-bc95-bf4af45f617f
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a794ec38ac07c1418f9e95b741941a83492bb3d5
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999771"
---
# <a name="project-contracts"></a><span data-ttu-id="0a42d-103">Projekto sutartys</span><span class="sxs-lookup"><span data-stu-id="0a42d-103">Project contracts</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0a42d-104">Šiame straipsnyje pateikiami projekto sutarčių, kurias galite kurti įvairiems projektų tipams ir finansavimo šaltiniams, pavyzdžiai, taip pat sutarčių tvarkymo ir sąskaitų faktūrų išrašymo projektų klientams pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="0a42d-104">This article provides examples of the project contracts that you can create for various types of projects and funding sources, and how you can manage contracts and invoice project customers.</span></span>

<span data-ttu-id="0a42d-105">Projekto, kurį kuriate projekto sutarčiai, tipu nustatomas būdas, naudojamas sąskaitoms faktūroms išrašyti projekto klientams.</span><span class="sxs-lookup"><span data-stu-id="0a42d-105">The type of project that you create for a project contract determines the method that is used to invoice project customers.</span></span> <span data-ttu-id="0a42d-106">Galite keisti projekto sutartį ir susijusį projektą, tačiau negalite keisti projekto tipo.</span><span class="sxs-lookup"><span data-stu-id="0a42d-106">You can change a project contract and the related project, but you can't change the project type.</span></span> 

<span data-ttu-id="0a42d-107">Naudodami projekto sutartį vienu metu galite išrašyti vieno ar kelių projektų sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-107">By using a project contract, you can invoice one or more projects at the same time.</span></span> <span data-ttu-id="0a42d-108">Projekto sutartis taip pat padeda užtikrinti nuoseklią sąskaitų faktūrų išrašymo tvarką kiekvienam projekto struktūroje esančiam subprojektui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-108">The project contract also helps guarantee a consistent invoicing procedure for every subproject in a project structure.</span></span> 

<span data-ttu-id="0a42d-109">Kiekvienas projektas, kuriam bus išrašyta sąskaita faktūra, turi būti susietas su projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="0a42d-109">Every project that will be invoiced must be associated with a project contract.</span></span> <span data-ttu-id="0a42d-110">Projekto sutarties parametrai taikomi visiems su ta projekto sutartimi susietiems projektams ir subprojektams.</span><span class="sxs-lookup"><span data-stu-id="0a42d-110">The settings for a project contract apply to all projects and subprojects that are associated with that project contract.</span></span> 

<span data-ttu-id="0a42d-111">Projekto sutartyje gali būti nurodytas vienas ar daugiau finansavimo šaltinių.</span><span class="sxs-lookup"><span data-stu-id="0a42d-111">A project contract can specify one or more sources of funding.</span></span> <span data-ttu-id="0a42d-112">Todėl galite išskaidyti sąskaitas tarp kelių skyrėjų, nustatyti finansavimo limitus, kad finansavimo šaltiniams teikiamos sąskaitos neviršytų nustatytos sumos, ir konfigūruoti apmokestinamų išlaidų finansavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="0a42d-112">Therefore, you can split the billing among multiple funders, set up funding limits so that funding sources are not billed more than a specified amount, and configure funding rules for charging expenditures.</span></span>

## <a name="funding-for-project-contracts"></a><span data-ttu-id="0a42d-113">Projektų sutarčių finansavimas</span><span class="sxs-lookup"><span data-stu-id="0a42d-113">Funding for project contracts</span></span>
<span data-ttu-id="0a42d-114">Kai kuriose projektų sutartyse nurodyta, kad projekto išlaidų finansavimo atsakomybė atitenka kelioms šalims.</span><span class="sxs-lookup"><span data-stu-id="0a42d-114">Some project contracts specify that multiple parties share the responsibility for funding the project costs.</span></span> <span data-ttu-id="0a42d-115">Štai keli pavyzdžiai:</span><span class="sxs-lookup"><span data-stu-id="0a42d-115">Here are some examples:</span></span>

-   <span data-ttu-id="0a42d-116">Stambus klientas, turintis keletą padalinių, prašo, kad projekto finansavimas būtų išskaidytas padaliniams.</span><span class="sxs-lookup"><span data-stu-id="0a42d-116">A large customer that has multiple divisions requests that funding of a project be split by division.</span></span>
-   <span data-ttu-id="0a42d-117">Jūsų įmonė patiria bendrų didelio projekto išlaidų su išorine organizacija.</span><span class="sxs-lookup"><span data-stu-id="0a42d-117">Your company shares the costs of a large project with an external organization.</span></span>
-   <span data-ttu-id="0a42d-118">Kelių projektą bendrai finansuoja dvi savivaldybės.</span><span class="sxs-lookup"><span data-stu-id="0a42d-118">A  road project is co-funded by two municipalities.</span></span>
-   <span data-ttu-id="0a42d-119">Tilto statybos projektą finansuoja valstybinė institucija ir privati korporacija.</span><span class="sxs-lookup"><span data-stu-id="0a42d-119">A bridge project is funded by a government grant and a private corporation.</span></span>

<span data-ttu-id="0a42d-120">Programoje „Dynamics 365 Finance” galite išskaidyti vienos operacijos arba viso projekto sąskaitas tarp kelių klientų, dotacijų arba organizacijų.</span><span class="sxs-lookup"><span data-stu-id="0a42d-120">In Dynamics 365 Finance, you can split the billing for a single transaction or an entire project among multiple customers, grants, or organizations.</span></span> 

<span data-ttu-id="0a42d-121">Projektuose, kuriuose yra keletas finansuotojų, visos šalys, prisidedančios prie išplėstinio finansavimo projekto finansavimo, vadinamos finansavimo šaltiniais.</span><span class="sxs-lookup"><span data-stu-id="0a42d-121">In projects that have multiple funders, all parties that contribute to the funding of an advanced funding project are called funding sources.</span></span> <span data-ttu-id="0a42d-122">Apibrėžus klientą, organizaciją arba dotaciją kaip finansavimo šaltinį, galima juos priskirti vienai arba keletui finansavimo taisyklių.</span><span class="sxs-lookup"><span data-stu-id="0a42d-122">After a customer, organization, or grant is defined as a funding source, it can be assigned to one or more funding rules.</span></span> <span data-ttu-id="0a42d-123">Finansavimo taisyklėse nurodomi kriterijai, apibrėžiantys, kaip mokesčiai paskirstomi tarp įvairių projekto finansavimo šaltinių.</span><span class="sxs-lookup"><span data-stu-id="0a42d-123">Funding rules contain the criteria that determines how charges are allocated to the various funding sources for a project.</span></span> 

<span data-ttu-id="0a42d-124">Atsargose laikomos prekės, pvz., tokios, kurios atsiranda pirkimo paraiškose ir pirkimo užsakymuose, negali būti išskaidytos, todėl išlaidų suma negali būti išskaidyta tarp kelių finansavimo šaltinių paskirstymo metu.</span><span class="sxs-lookup"><span data-stu-id="0a42d-124">Because stocked items, such as those that appear on purchase requisitions and purchase orders, can't be split, the cost amount can't be split among multiple funding sources at the time of distribution.</span></span> <span data-ttu-id="0a42d-125">Todėl finansavimo šaltinio reikšmė lieka 0 (nulis), kol neužregistruojama atsargų problema.</span><span class="sxs-lookup"><span data-stu-id="0a42d-125">Therefore, the funding source value remains 0 (zero) until the inventory issue is posted.</span></span> <span data-ttu-id="0a42d-126">Užregistravus atsargų problemą, išlaidų suma paskirstoma pagal projektui taikomas kliento paskirstymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="0a42d-126">When the inventory issue is posted, the cost amount is distributed according to the account distribution rules for the project.</span></span>

<span data-ttu-id="0a42d-127">Čia pateikiami keli veiksmai, kuriuos atlikę lengviau paskirstysite atsiskaitymą tarp kelių finansavimo šaltinių.</span><span class="sxs-lookup"><span data-stu-id="0a42d-127">Here are some steps that you can take to make it easier to split the billing among multiple funding sources:</span></span>

-   <span data-ttu-id="0a42d-128">Nurodykite, kad visose įvestose projekto operacijose naudojama tokia pati pardavimo valiuta kaip ir projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="0a42d-128">Specify that all transactions that are entered for a project use the same sales currency as the project contract.</span></span>
-   <span data-ttu-id="0a42d-129">Nustatykite finansavimo limitus, kad finansavimo šaltiniui nebūtų išrašyta sąskaita, kurios suma viršytų sumą, nurodytą projekte.</span><span class="sxs-lookup"><span data-stu-id="0a42d-129">Set up funding limits, so that a funding source isn't invoiced more than a specified amount toward a project.</span></span>
-   <span data-ttu-id="0a42d-130">Konfigūruokite kiekvieno darbuotojo, elemento, kategorijos, kategorijos grupės ir operacijų tipo (arba visų transakcijų tipų) finansavimo taisykles ir finansavimo limitus.</span><span class="sxs-lookup"><span data-stu-id="0a42d-130">Configure funding rules and funding limits for each worker, item, category, category group, and transaction type (or for all transaction types).</span></span>
-   <span data-ttu-id="0a42d-131">Pažymėkite pasirinktines pradžios ir pabaigos datas, kad nustatytumėte kiekvienos finansavimo taisyklės galiojimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="0a42d-131">Select optional start and end dates to define the period when each funding rule is valid.</span></span>
-   <span data-ttu-id="0a42d-132">Nurodykite procentinę dalį, už kurią atsako kiekvienas finansavimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="0a42d-132">Specify the percentage that each funding source is responsible for.</span></span>
-   <span data-ttu-id="0a42d-133">Nurodykite, kuris finansavimo šaltinis yra atsakingas už apvalinimo skirtumus, atsiradusius skaičiuojant finansavimo paskirstymą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-133">Specify which funding source is responsible for rounding differences that are caused by funding allocation calculations.</span></span>
-   <span data-ttu-id="0a42d-134">Nustatykite taisykles, kuriomis apibrėžiama, kaip projekto išlaidų sąskaitos išrašomos išoriniams klientams ir teikiamos vidinėms organizacijoms.</span><span class="sxs-lookup"><span data-stu-id="0a42d-134">Set up rules that determine how project costs are invoiced to external customers and charged to internal organizations.</span></span>
-   <span data-ttu-id="0a42d-135">Įrašykite operacijas į atidėtą finansavimo klientą, kol bus gautas papildomas finansavimas arba kol nuspręsite dengti išlaidas organizacijos viduje.</span><span class="sxs-lookup"><span data-stu-id="0a42d-135">Record transactions in an on-hold funding account until additional funding can be obtained, or until you decide to bear the costs internally.</span></span>

<span data-ttu-id="0a42d-136">Siekiant nustatyti, kokią mokesčių grupę sieti su operacija, projekte ieškoma mokesčių grupės priskyrimo.</span><span class="sxs-lookup"><span data-stu-id="0a42d-136">To determine which tax group to associate with a transaction, the project is searched for a tax group assignment.</span></span> <span data-ttu-id="0a42d-137">Jeigu projekto lygyje nebuvo atliktas mokesčių grupės priskyrimas, ieškoma projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="0a42d-137">If no tax group assignment has been made at the project level, the project contract is searched.</span></span>

### <a name="example-multiple-funding-sources-simple"></a><span data-ttu-id="0a42d-138">Pavyzdys: keli finansavimo šaltiniai (paprasti)</span><span class="sxs-lookup"><span data-stu-id="0a42d-138">Example: Multiple funding sources (simple)</span></span>

<span data-ttu-id="0a42d-139">Šioje lentelėje pateikiami kelių finansavimo šaltinių finansavimo paskirstymo scenarijai.</span><span class="sxs-lookup"><span data-stu-id="0a42d-139">The following table provides scenarios for managing funding allocation among multiple funding sources.</span></span> <span data-ttu-id="0a42d-140">Šie scenarijai grindžiami toliau pateikiamomis prielaidomis.</span><span class="sxs-lookup"><span data-stu-id="0a42d-140">These scenarios are based on the following assumptions:</span></span>

-   <span data-ttu-id="0a42d-141">Prioriteto parametrai įtraukiami į lėšų paskirstymą prieš taikant kitus finansavimo taisyklių kriterijus.</span><span class="sxs-lookup"><span data-stu-id="0a42d-141">Priority settings are factored into the allocation of funds before other funding rule criteria are applied.</span></span>
-   <span data-ttu-id="0a42d-142">Nenurodytas datų diapazonas, apibrėžiantis finansavimo taisyklės galiojimo laikotarpį.</span><span class="sxs-lookup"><span data-stu-id="0a42d-142">No date range has been specified to define the period d when the funding rule is valid.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a42d-143"><strong>Scenarijus</strong></span><span class="sxs-lookup"><span data-stu-id="0a42d-143"><strong>Scenario</strong></span></span></td>
<td><span data-ttu-id="0a42d-144"><strong>Finansavimo šaltinis</strong></span><span class="sxs-lookup"><span data-stu-id="0a42d-144"><strong>Funding source</strong></span></span></td>
<td><span data-ttu-id="0a42d-145"><strong>Paskirstymo procentinė dalis</strong></span><span class="sxs-lookup"><span data-stu-id="0a42d-145"><strong>Allocation percentage</strong></span></span></td>
<td><span data-ttu-id="0a42d-146"><strong>Paskirstymo prioritetas</strong></span><span class="sxs-lookup"><span data-stu-id="0a42d-146"><strong>Allocation priority</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a42d-147">Norite skirti išlaidas vienam finansavimo šaltiniui tol, kol jo lėšos bus išeikvotos, skirti išlaidas antram finansavimo šaltiniui tol, kol jo lėšos bus išeikvotos ir pagaliau skirti likusias išlaidas trečiam finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-147">You want to allocate costs to one funding source until its funds are exhausted, allocate costs to a second funding source until its funds are exhausted, and finally allocate the remaining costs to a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a42d-148">1-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-148">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a42d-149">2-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-149">Funding　source　2</span></span></li>
<li><span data-ttu-id="0a42d-150">3-ias finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-150">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-151">100 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-151">100%</span></span></li>
<li><span data-ttu-id="0a42d-152">100 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-152">100%</span></span></li>
<li><span data-ttu-id="0a42d-153">100 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-153">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-154">1</span><span class="sxs-lookup"><span data-stu-id="0a42d-154">1</span></span></li>
<li><span data-ttu-id="0a42d-155">2</span><span class="sxs-lookup"><span data-stu-id="0a42d-155">2</span></span></li>
<li><span data-ttu-id="0a42d-156">3</span><span class="sxs-lookup"><span data-stu-id="0a42d-156">3</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a42d-157">Norite skirti 75 procentus išlaidų vienam finansavimo šaltiniui ir 25 procentus antram finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-157">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="0a42d-158">Kai bus išeikvotas bet kuris šių finansavimo šaltinių, norite, kad likusios išlaidos būtų sumokėtos iš trečio finansavimo šaltinio.</span><span class="sxs-lookup"><span data-stu-id="0a42d-158">When either of those funding sources is exhausted, you want to pay the remaining costs from a third funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a42d-159">1-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-159">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a42d-160">2-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-160">Funding　source　2</span></span></li>
<li><span data-ttu-id="0a42d-161">3-ias finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-161">Funding　source　3</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-162">75 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-162">75%</span></span></li>
<li><span data-ttu-id="0a42d-163">25 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-163">25%</span></span></li>
<li><span data-ttu-id="0a42d-164">100 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-164">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-165">1</span><span class="sxs-lookup"><span data-stu-id="0a42d-165">1</span></span></li>
<li><span data-ttu-id="0a42d-166">1</span><span class="sxs-lookup"><span data-stu-id="0a42d-166">1</span></span></li>
<li><span data-ttu-id="0a42d-167">2</span><span class="sxs-lookup"><span data-stu-id="0a42d-167">2</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a42d-168">Norite skirti 75 procentus išlaidų vienam finansavimo šaltiniui ir 25 procentus antram finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-168">You want to allocate 75 percent of costs to one funding source and 25 percent to a second funding source.</span></span> <span data-ttu-id="0a42d-169">Kai bus išeikvotas bet kuris šių finansavimo šaltinių, norite, kad likusios išlaidos būtų išskaidytos tarp trečio ir ketvirto finansavimo šaltinio.</span><span class="sxs-lookup"><span data-stu-id="0a42d-169">When either of those funding sources is exhausted, you want to split the remaining costs between a third funding source and a fourth funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a42d-170">1-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-170">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a42d-171">2-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-171">Funding　source　2</span></span></li>
<li><span data-ttu-id="0a42d-172">3-ias finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-172">Funding　source　3</span></span></li>
<li><span data-ttu-id="0a42d-173">4 finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-173">Funding　source　4</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-174">75 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-174">75%</span></span></li>
<li><span data-ttu-id="0a42d-175">25 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-175">25%</span></span></li>
<li><span data-ttu-id="0a42d-176">50 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-176">50%</span></span></li>
<li><span data-ttu-id="0a42d-177">50 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-177">50%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-178">1</span><span class="sxs-lookup"><span data-stu-id="0a42d-178">1</span></span></li>
<li><span data-ttu-id="0a42d-179">1</span><span class="sxs-lookup"><span data-stu-id="0a42d-179">1</span></span></li>
<li><span data-ttu-id="0a42d-180">2</span><span class="sxs-lookup"><span data-stu-id="0a42d-180">2</span></span></li>
<li><span data-ttu-id="0a42d-181">2</span><span class="sxs-lookup"><span data-stu-id="0a42d-181">2</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a42d-182">Norite skirti pirmus 25 procentus išlaidų vienam finansavimo šaltiniui ir likusią dalį antram finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-182">You want to allocate the first 25 percent of costs to one funding source and the rest to a second funding source.</span></span></td>
<td><ul>
<li><span data-ttu-id="0a42d-183">1-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-183">Funding　source　1</span></span></li>
<li><span data-ttu-id="0a42d-184">2-as finansavimo šaltinis</span><span class="sxs-lookup"><span data-stu-id="0a42d-184">Funding　source　2</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-185">25 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-185">25%</span></span></li>
<li><span data-ttu-id="0a42d-186">100 %</span><span class="sxs-lookup"><span data-stu-id="0a42d-186">100%</span></span></li>
</ul></td>
<td><ul>
<li><span data-ttu-id="0a42d-187">1</span><span class="sxs-lookup"><span data-stu-id="0a42d-187">1</span></span></li>
<li><span data-ttu-id="0a42d-188">2</span><span class="sxs-lookup"><span data-stu-id="0a42d-188">2</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

### <a name="example-multiple-funding-sources-complex"></a><span data-ttu-id="0a42d-189">Pavyzdys: keli finansavimo šaltiniai (sudėtiniai)</span><span class="sxs-lookup"><span data-stu-id="0a42d-189">Example: Multiple funding sources (complex)</span></span>

<span data-ttu-id="0a42d-190">Turite tris finansavimo šaltinius, kuriuos norite naudoti toliau pateikiama tvarka.</span><span class="sxs-lookup"><span data-stu-id="0a42d-190">You have three funding sources that you want to use in the following order:</span></span>

1.  <span data-ttu-id="0a42d-191">Vienodai naudoti 2-ą finansavimo šaltinį ir 3-ią finansavimo šaltinį tol, kol bus išeikvotas 2-as finansavimo šaltinis.</span><span class="sxs-lookup"><span data-stu-id="0a42d-191">Use funding source 2 and funding source 3 equally until funding source 2 is exhausted.</span></span>
2.  <span data-ttu-id="0a42d-192">Toliau naudoti 3-ią finansavimo šaltinį tol, kol jis bus išeikvotas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-192">Continue to use funding source 3 until it is exhausted.</span></span>
3.  <span data-ttu-id="0a42d-193">Išeikvojus 3-ią finansavimo šaltinį, naudoti 1-ą finansavimo šaltinį.</span><span class="sxs-lookup"><span data-stu-id="0a42d-193">Use funding source 1 after funding source 3 is exhausted.</span></span>

<span data-ttu-id="0a42d-194">Norėdami pasiekti šį tikslą, turite atlikti toliau nurodytus veiksmus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="0a42d-194">To accomplish this goal, you must do the following:</span></span>

-   <span data-ttu-id="0a42d-195">Nustatykite 2-o finansavimo šaltinio ir 3-io finansavimo šaltinio atitinkamas finansavimo limito sumas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-195">Set up funding limits for funding source 2 and funding source 3, for their respective amounts.</span></span>
-   <span data-ttu-id="0a42d-196">Sukurkite tolesnes finansavimo taisykles.</span><span class="sxs-lookup"><span data-stu-id="0a42d-196">Create the following funding rules:</span></span>
    -   <span data-ttu-id="0a42d-197">1 taisyklė (1 prioritetas): skirti 50 procentų operacijų 2-am finansavimo šaltiniui ir 50 procentų 3-iam finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-197">Rule 1 (Priority 1): Allocate 50 percent of transactions to funding source 2 and 50 percent to funding source 3.</span></span>
    -   <span data-ttu-id="0a42d-198">2 taisyklė (2 prioritetas): skirti 100 procentų operacijų 3-iam finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-198">Rule 2 (Priority 2): Allocate 100 percent of transactions to funding source 3.</span></span>
    -   <span data-ttu-id="0a42d-199">3 taisyklė (3 prioritetas): skirti 100 procentų operacijų 1-am finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-199">Rule 3 (Priority 3): Allocate 100 percent of transactions to funding source 1.</span></span>

<span data-ttu-id="0a42d-200">Ši sąranka veikia, nes operacijos tikrinamos pagal taisykles ir limitus, siekiant nustatyti, ar kuri nors iš jų taikoma operacijai.</span><span class="sxs-lookup"><span data-stu-id="0a42d-200">This setup works because transactions are checked against rules and limits to determine whether any of them apply to the transaction.</span></span> <span data-ttu-id="0a42d-201">Jei operacijai netaikomos jokios konkrečios taisyklės ar limitai, taikoma visų operacijų taisyklė.</span><span class="sxs-lookup"><span data-stu-id="0a42d-201">If no specific rules or limits apply to the transaction, the All transactions rule applies.</span></span> <span data-ttu-id="0a42d-202">Visų operacijų taisyklė taikoma visoms operacijoms.</span><span class="sxs-lookup"><span data-stu-id="0a42d-202">The All transactions rule matches all transactions.</span></span> 

<span data-ttu-id="0a42d-203">Jei randama operacijai taikoma taisyklė, šioje taisyklėje paskirstoma procentinė dalis taikoma pirmiausiai, bet tik patikrinus, ar neviršijama nustatytų limitų.</span><span class="sxs-lookup"><span data-stu-id="0a42d-203">If a rule is found that matches a transaction, the percentage that has been allocated in that rule is applied first, but only after the matches are checked against any limits that have been set up.</span></span> <span data-ttu-id="0a42d-204">Jei pasiektas limitas, o finansavimo šaltinio lėšos išeikvotos, su šiuo finansavimo limitu susijusios taisyklės nepaisoma ir programa tikrina kitą taikomą taisyklę.</span><span class="sxs-lookup"><span data-stu-id="0a42d-204">If a limit has been met, and a funding source’s funds are exhausted, the funding rule that is associated with the funding limit is disregarded, and the program checks for the next rule that applies.</span></span> 

<span data-ttu-id="0a42d-205">Kai kuriais atvejais pagal taisyklę galima paskirstyti tik dalį operacijos.</span><span class="sxs-lookup"><span data-stu-id="0a42d-205">In some cases, only part of a transaction can be allocated under a rule.</span></span> <span data-ttu-id="0a42d-206">Taip gali nutikti, jei limito pasiekiama skiriant operaciją.</span><span class="sxs-lookup"><span data-stu-id="0a42d-206">This might happen because a limit is reached when the transaction is allocated.</span></span> <span data-ttu-id="0a42d-207">Šiuo atveju tik tam tikra suma paskirstoma pagal šią taisyklę, pvz., po 50 procentų kiekvienam finansavimo šaltiniui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-207">In this case, only a certain amount is allocated according to that rule, such as 50 percent to each funding source.</span></span> <span data-ttu-id="0a42d-208">Tai yra 1 taisyklės atvejis, aprašytas anksčiau šiame skyriuje.</span><span class="sxs-lookup"><span data-stu-id="0a42d-208">This is the case in rule 1, which is described earlier in this section.</span></span> <span data-ttu-id="0a42d-209">Likusi dalis paskirstoma pagal kitą sekoje esančią taisyklę.</span><span class="sxs-lookup"><span data-stu-id="0a42d-209">The remainder is allocated according to the next rule in the sequence.</span></span> 

<span data-ttu-id="0a42d-210">Toliau pateikiamoje lentelėje šis scenarijus nagrinėjamas išsamiau.</span><span class="sxs-lookup"><span data-stu-id="0a42d-210">The following table examines this scenario in more detail.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="0a42d-211"><strong>Aktyvinimas</strong></span><span class="sxs-lookup"><span data-stu-id="0a42d-211"><strong>Focus</strong></span></span></td>
<td><span data-ttu-id="0a42d-212"><strong>Išsami informacija</strong></span><span class="sxs-lookup"><span data-stu-id="0a42d-212"><strong>Details</strong></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a42d-213">Finansavimo taisyklės</span><span class="sxs-lookup"><span data-stu-id="0a42d-213">Funding rules</span></span></td>
<td><ul>
<li><span data-ttu-id="0a42d-214">1 taisyklė (1 prioritetas): visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="0a42d-214">Rule 1 (Priority 1): All transactions.</span></span> <span data-ttu-id="0a42d-215">2-am finansavimo šaltiniui skirti 50 % ir 3-iam finansavimo šaltiniui – 50 %.</span><span class="sxs-lookup"><span data-stu-id="0a42d-215">Allocate funding source 2 at 50% and funding source 3 at 50%.</span></span></li>
<li><span data-ttu-id="0a42d-216">2 taisyklė (2 prioritetas): visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="0a42d-216">Rule 2 (Priority 2): All transactions.</span></span> <span data-ttu-id="0a42d-217">3-iam finansavimo šaltiniui skirti 100 %.</span><span class="sxs-lookup"><span data-stu-id="0a42d-217">Allocate funding source 3 at 100%.</span></span></li>
<li><span data-ttu-id="0a42d-218">3 taisyklė (2 prioritetas): visos operacijos.</span><span class="sxs-lookup"><span data-stu-id="0a42d-218">Rule 3 (Priority 2): All transactions.</span></span> <span data-ttu-id="0a42d-219">1-am finansavimo šaltiniui skirti 100 %.</span><span class="sxs-lookup"><span data-stu-id="0a42d-219">Allocate funding source 1 at 100%.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a42d-220">Finansavimo limitai</span><span class="sxs-lookup"><span data-stu-id="0a42d-220">Funding limits</span></span></td>
<td><ul>
<li><span data-ttu-id="0a42d-221">1-o finansavimo šaltinio limitas yra 10 000,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-221">Funding source 1 limit = 10,000.00</span></span></li>
<li><span data-ttu-id="0a42d-222">2-o finansavimo šaltinio limitas yra 500,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-222">Funding source 2 limit = 500.00</span></span></li>
<li><span data-ttu-id="0a42d-223">3-io finansavimo šaltinio limitas yra 750,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-223">Funding source 3 limit = 750.00</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a42d-224">1 operacija</span><span class="sxs-lookup"><span data-stu-id="0a42d-224">Transaction 1</span></span></td>
<td><span data-ttu-id="0a42d-225"><strong>Operacijos suma:</strong> 100,00<strong>Finansavimas:</strong> operacija apmokama tik pagal 1 taisyklę, nes taikoma tai, kad operacija visiškai apmokama pagal 1 taisyklę.</span><span class="sxs-lookup"><span data-stu-id="0a42d-225"><strong>Transaction amount:</strong> 100.00<strong>Funding:</strong> The transaction is paid according to rule 1 only, because the transaction is fully paid after rule 1 is applied.</span></span> <span data-ttu-id="0a42d-226">Operacija finansuojama po lygiai 2-o finansavimo šaltinio ir 3-io finansavimo šaltinio.</span><span class="sxs-lookup"><span data-stu-id="0a42d-226">The transaction is funded equally between funding source 2 and funding source 3.</span></span>
<ul>
<li><span data-ttu-id="0a42d-227">2-as finansavimo šaltinis: 50,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-227">Funding source 2: 50.00</span></span></li>
<li><span data-ttu-id="0a42d-228">3-ias finansavimo šaltinis: 50,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-228">Funding source 3: 50.00</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="0a42d-229">2 operacija</span><span class="sxs-lookup"><span data-stu-id="0a42d-229">Transaction 2</span></span></td>
<td><span data-ttu-id="0a42d-230"><strong>Operacijos suma:</strong> 5000,00<strong>Finansavimas:</strong> operacija apmokama pagal visas tris taisykles.</span><span class="sxs-lookup"><span data-stu-id="0a42d-230"><strong>Transaction amount:</strong> 5,000.00<strong>Funding:</strong> The transaction is paid according to all three rules.</span></span> <span data-ttu-id="0a42d-231"><strong>1 taisyklė</strong>
</span><span class="sxs-lookup"><span data-stu-id="0a42d-231"><strong>Rule 1</strong>
</span></span><ul>
<li><span data-ttu-id="0a42d-232">2-as finansavimo šaltinis: 450,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-232">Funding source 2: 450.00</span></span></li>
<li><span data-ttu-id="0a42d-233">3-ias finansavimo šaltinis: 450,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-233">Funding source 3: 450.00</span></span></li>
</ul><span data-ttu-id="0a42d-234">
<strong>2 taisyklė</strong>
</span><span class="sxs-lookup"><span data-stu-id="0a42d-234">
<strong>Rule 2</strong>
</span></span><ul>
<li><span data-ttu-id="0a42d-235">3-ias finansavimo šaltinis: 250,00 (= 750,00 – 50,00 – 450,00)</span><span class="sxs-lookup"><span data-stu-id="0a42d-235">Funding source 3: 250.00 (= 750.00 – 50.00 – 450.00)</span></span></li>
</ul><span data-ttu-id="0a42d-236">
<strong>3 taisyklė</strong>
</span><span class="sxs-lookup"><span data-stu-id="0a42d-236">
<strong>Rule 3</strong>
</span></span><ul>
<li><span data-ttu-id="0a42d-237">1-as finansavimo šaltinis: 3850,00 (= 5000,00 – 450,00 – 450,00 – 250,00)</span><span class="sxs-lookup"><span data-stu-id="0a42d-237">Funding source 1: 3,850.00 (= 5,000.00 – 450.00 – 450.00 – 250.00)</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="0a42d-238">Iš viso lėšų, skirtų kiekvienam finansavimo šaltiniui</span><span class="sxs-lookup"><span data-stu-id="0a42d-238">Total funds that are distributed for each funding source</span></span></td>
<td><ul>
<li><span data-ttu-id="0a42d-239">1-as finansavimo šaltinis: 3850,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-239">Funding source 1: 3,850.00</span></span></li>
<li><span data-ttu-id="0a42d-240">2-as finansavimo šaltinis: 500,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-240">Funding source 2: 500.00</span></span></li>
<li><span data-ttu-id="0a42d-241">3-ias finansavimo šaltinis: 750,00</span><span class="sxs-lookup"><span data-stu-id="0a42d-241">Funding source 3: 750.00</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="billing-rules"></a><span data-ttu-id="0a42d-242">Atsiskaitymo taisyklės</span><span class="sxs-lookup"><span data-stu-id="0a42d-242">Billing rules</span></span>
<span data-ttu-id="0a42d-243">Kai aptariate projekto sutartį su klientu, nustatote kaip ir kada galite išrašyti klientui sąskaitą faktūrą už darbą su projektu.</span><span class="sxs-lookup"><span data-stu-id="0a42d-243">When you negotiate a project contract with a customer, you define how and when you can invoice the customer for work on a project.</span></span> <span data-ttu-id="0a42d-244">Nustatę projekto sutartį ir projektą, galite nustatyti projekto sąskaitų išrašymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="0a42d-244">After you set up the project contract and the project, you can set up billing rules for the project.</span></span> <span data-ttu-id="0a42d-245">Sąskaitų išrašymo taisyklės grindžiamos projekto terminais, nustatytais projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="0a42d-245">Billing rules are based on the project terms that are specified in the project contract.</span></span> <span data-ttu-id="0a42d-246">Kokias atsiskaitymo taisykles galite sukurti priklauso nuo projekto sutarties ir projekto tipo sąlygų, pvz., laiko ir medžiagų arba fiksuotos kainos, kurias siejate su atsiskaitymo taisykle.</span><span class="sxs-lookup"><span data-stu-id="0a42d-246">The billing rules that you can create depend on the terms of the project contract and the project type, such as Time and material or Fixed-price, that you associate with the billing rule.</span></span> <span data-ttu-id="0a42d-247">Galite sukurti daugiau nei vieną projekto sutarties atsiskaitymo taisyklę.</span><span class="sxs-lookup"><span data-stu-id="0a42d-247">You can create more than one billing rule for a project contract.</span></span> <span data-ttu-id="0a42d-248">Taip pat galite priskirti atsiskaitymo taisyklę keliems projektams, susijusiems su ta pačia projekto sutartimi ir turintiems panašias atsiskaitymo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-248">You can also assign a billing rule to multiple projects that are associated with the same project contract and have similar billing terms.</span></span> 

<span data-ttu-id="0a42d-249">Galite nustatyti toliau nurodytus atsiskaitymo taisyklių tipus.</span><span class="sxs-lookup"><span data-stu-id="0a42d-249">You can set up the following types of billing rules:</span></span>

-   <span data-ttu-id="0a42d-250">**Pristatymo vienetas** – klientui išrašoma sąskaita faktūra atlikus pristatymo vienetą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-250">**Unit of delivery** – Invoice a customer when you complete a unit of delivery.</span></span> <span data-ttu-id="0a42d-251">Pristatymo vienetai apibrėžiami sutartyje.</span><span class="sxs-lookup"><span data-stu-id="0a42d-251">You define the units of delivery in the contract.</span></span>
-   <span data-ttu-id="0a42d-252">**Vykdymo eiga** – klientui išrašoma sąskaita faktūra, kai įvykdote nurodytą procentinę dalį projekto.</span><span class="sxs-lookup"><span data-stu-id="0a42d-252">**Progress** – Invoice a customer when you complete a specified percentage of the project.</span></span> <span data-ttu-id="0a42d-253">Galite nustatyti atsiskaitymo taisyklę, kad būtų automatiškai skaičiuojama atlikto darbo procentinė dalis, arba galite rankiniu būdu skaičiuoti atlikto darbo procentinę dalį ir klientui išrašomos sąskaitos faktūros sumą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-253">You can set up a billing rule to automatically calculate the percentage of work completed, or you can manually calculate the percentage of work completed and the amount to invoice the customer.</span></span>
-   <span data-ttu-id="0a42d-254">**Etapas** – klientui išrašoma sąskaita faktūra už visą projekto etapą jį pasiekus.</span><span class="sxs-lookup"><span data-stu-id="0a42d-254">**Milestone** – Invoice a customer for the full amount of a project milestone when the milestone is reached.</span></span>
-   <span data-ttu-id="0a42d-255">**Mokestis** – klientui išrašoma sąskaita faktūra už jūsų paslaugas ir pridedamas administravimo mokestis, kuris paprastai yra paslaugų sumos procentinė dalis.</span><span class="sxs-lookup"><span data-stu-id="0a42d-255">**Fee** – Invoice a customer for your services plus a management fee, which is typically a percentage of the cost of services.</span></span>
-   <span data-ttu-id="0a42d-256">**Laikas ir medžiagos** – klientui išrašoma sąskaita faktūra už laiko pardavimo vertę ir medžiagas, naudojamas projekte.</span><span class="sxs-lookup"><span data-stu-id="0a42d-256">**Time and material** – Invoice a customer for the value of time and materials that are used on a project.</span></span>

<span data-ttu-id="0a42d-257">Visiems atsiskaitymo taisyklių tipams galite nurodyti užlaikymo procentinį dydį, kuris išskaičiuojamas iš kliento sąskaitų faktūrų tol, kol projektas pasieks sutarto etapo.</span><span class="sxs-lookup"><span data-stu-id="0a42d-257">For all types of billing rules, you can specify a retention percentage that is deducted from customer invoices until a project reaches an agreed-upon stage.</span></span> <span data-ttu-id="0a42d-258">Mokėjimo užlaikymo procentinis dydis nurodomas projekto sutartyje.</span><span class="sxs-lookup"><span data-stu-id="0a42d-258">The payment retention percentage is specified in the project contract.</span></span> <span data-ttu-id="0a42d-259">Suma apskaičiuojama pagal visą kliento sąskaitoje faktūroje esančių eilučių vertę ir atimama iš jos.</span><span class="sxs-lookup"><span data-stu-id="0a42d-259">The amount is calculated based on, and subtracted from, the total value of the lines in a customer invoice.</span></span> 

<span data-ttu-id="0a42d-260">Galite priskirti apmokestinamas kategorijas atsiskaitymo taisyklėms **Laikas ir medžiagos** ir **Vykdymo eiga**.</span><span class="sxs-lookup"><span data-stu-id="0a42d-260">For **Time and material** and **Progress** billing rules, you can assign chargeable categories.</span></span> <span data-ttu-id="0a42d-261">Apmokestinamosiomis kategorijomis nurodomos operacijos, kurios turi būti įtrauktos į kliento sąskaitas faktūras.</span><span class="sxs-lookup"><span data-stu-id="0a42d-261">Chargeable categories indicate the transactions that should be included in customer invoices.</span></span> 

<span data-ttu-id="0a42d-262">Kai būsite pasirengę išrašyti klientui sąskaitą faktūrą, pagal atsiskaitymo taisykles bus paskaičiuota projekto sąskaitos faktūros suma ir sugeneruotas projekto sąskaitos faktūros pasiūlymas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-262">When you are ready to invoice the customer, the amount to invoice for the project is calculated based on the billing rules, and a project invoice proposal is generated.</span></span> 

<span data-ttu-id="0a42d-263">Tolesniuose skyriuose pateikiami pavyzdžiai, kaip nustatyti ir tvarkyti projekto atsiskaitymo taisykles.</span><span class="sxs-lookup"><span data-stu-id="0a42d-263">The following sections provide examples that show how to set up and manage billing rules for a project.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-the-number-of-units-delivered"></a><span data-ttu-id="0a42d-264">Pavyzdys: atsiskaitymo taisyklės, pagrįstos pristatytų vienetų skaičiumi, kūrimas</span><span class="sxs-lookup"><span data-stu-id="0a42d-264">Example: Create a billing rule that is based on the number of units delivered</span></span>

<span data-ttu-id="0a42d-265">Jūsų organizacija sudaro sutartį, pagal kurią ji surengs kliento darbuotojams iš viso penkis mokymo seansus, kurių kiekvieno savikaina yra 10 000.</span><span class="sxs-lookup"><span data-stu-id="0a42d-265">Your organization enters into an agreement to provide a total of five training sessions to a customer’s employees at a cost of 10,000 per training session.</span></span> <span data-ttu-id="0a42d-266">Sąskaitą faktūrą klientui išrašote po kiekvieno mokymo seanso.</span><span class="sxs-lookup"><span data-stu-id="0a42d-266">You invoice the customer after each training session.</span></span> 

<span data-ttu-id="0a42d-267">Nustatydami sutarties atsiskaitymo taisykles, naudojate tolesnes reikšmes.</span><span class="sxs-lookup"><span data-stu-id="0a42d-267">When you set up the billing rules for the contract, you use the following values:</span></span>

-   <span data-ttu-id="0a42d-268">Pristatymo vienetas yra vienas mokymo seansas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-268">The unit of delivery is one training session.</span></span>
-   <span data-ttu-id="0a42d-269">Vieneto kaina yra 10 000 už vieną mokymo seansą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-269">The unit price is 10,000 per training session.</span></span>
-   <span data-ttu-id="0a42d-270">Bendras vienetų skaičius yra penki mokymo seansai.</span><span class="sxs-lookup"><span data-stu-id="0a42d-270">The total number of units is five training sessions.</span></span>

<span data-ttu-id="0a42d-271">Baigę vieną mokymo seansą, galite sukurti pirmo pristatyto vieneto sąskaitą faktūrą, kurios suma yra 10 000, ir išsiųsti šią sąskaitą faktūrą klientui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-271">When you have completed one training session, you can create an invoice for 10,000, for the first unit that was delivered, and send the invoice to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-manual-calculation"></a><span data-ttu-id="0a42d-272">Pavyzdys: atsiskaitymo taisyklės, pagrįstos nustatyta projekto įvykdymo procentine dalimi, kūrimas (skaičiuojama rankiniu būdu)</span><span class="sxs-lookup"><span data-stu-id="0a42d-272">Example: Create a billing rule that is based on a specified percentage of project completion (manual calculation)</span></span>

<span data-ttu-id="0a42d-273">Jūsų organizacija, įmonė, konsultuojanti programinės įrangos klausimais, sudaro su klientu sutartį, pagal kurią ji sukurs dalį produkto, kurį kuria klientas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-273">Your organization, a software consulting firm, enters into an agreement with a customer to develop part of a product that the customer is developing.</span></span> <span data-ttu-id="0a42d-274">Sutariama, kad jūsų organizacija pateiks programinės įrangos kodą per šešis mėnesius.</span><span class="sxs-lookup"><span data-stu-id="0a42d-274">Your organization agrees to deliver the software code over a period of six months.</span></span> <span data-ttu-id="0a42d-275">Sutariama, kad už šį darbą klientas sumokės jūsų organizacijai iš viso 100 000.</span><span class="sxs-lookup"><span data-stu-id="0a42d-275">The customer agrees to pay your organization a total of 100,000 for the work.</span></span> <span data-ttu-id="0a42d-276">Kaip nurodyta sutartyje, kuriate atsiskaitymo taisyklę išrašyti klientui sąskaitą faktūrą, pagrįstą atlikto darbo procentine dalimi.</span><span class="sxs-lookup"><span data-stu-id="0a42d-276">You create a billing rule to invoice the customer based on the percentage of work that is completed on the project, as specified in the contract.</span></span>

-   <span data-ttu-id="0a42d-277">Pirmo mėnesio pabaigoje susitinkate su klientu, kad nustatytumėte atlikto darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="0a42d-277">At the end of the first month, you meet with the customer to determine the percentage of work completed.</span></span> <span data-ttu-id="0a42d-278">Kartu su klientu peržiūrėję projektą, nusprendžiate, kad įvykdyta 15 proc. projekto.</span><span class="sxs-lookup"><span data-stu-id="0a42d-278">After you and the customer review the project, you decide that the project is 15 percent completed.</span></span>
-   <span data-ttu-id="0a42d-279">Išrašote sąskaitą faktūrą, kurios suma yra 15 000 (15 proc. 100 000), ir išsiunčiate ją klientui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-279">You create an invoice for 15,000 (15 percent of 100,000) and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-a-specified-percentage-of-project-completion-automatic-calculation"></a><span data-ttu-id="0a42d-280">Pavyzdys: atsiskaitymo taisyklės, pagrįstos nustatyta projekto įvykdymo procentine dalimi, kūrimas (skaičiuojama automatiškai)</span><span class="sxs-lookup"><span data-stu-id="0a42d-280">Example: Create a billing rule that is based on a specified percentage of project completion (automatic calculation)</span></span>

<span data-ttu-id="0a42d-281">Jūsų organizacija, programinės įrangos kūrimo įmonė, sutinka sukurti klientui atlyginimų apskaitos paketą už 30 000.</span><span class="sxs-lookup"><span data-stu-id="0a42d-281">Your organization, a software development firm, agrees to develop a payroll accounting package for a customer for 30,000.</span></span> <span data-ttu-id="0a42d-282">Sutariama, kad klientas mokės jūsų organizacijai pagal atlikto darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="0a42d-282">The customer agrees to pay your organization based on the percentage of work completed.</span></span> <span data-ttu-id="0a42d-283">Numatomos projekto išlaidos yra 20 000.</span><span class="sxs-lookup"><span data-stu-id="0a42d-283">You estimate that the project costs are 20,000.</span></span> <span data-ttu-id="0a42d-284">Projekto sutartyje nurodomos darbo kategorijos, kurias naudojate atsiskaitymo procese.</span><span class="sxs-lookup"><span data-stu-id="0a42d-284">The project contract specifies the categories of work that you use in the billing process.</span></span> <span data-ttu-id="0a42d-285">Nustatote atsiskaitymo taisykles, pagal kurias automatiškai apskaičiuojamos sąskaitos faktūros sumos už atlikto kiekvienos kategorijos darbo procentinę dalį.</span><span class="sxs-lookup"><span data-stu-id="0a42d-285">You set up billing rules that automatically calculate the invoice amounts for the percentage of work that is completed for each category.</span></span> <span data-ttu-id="0a42d-286">Nustatote kiekvienos kategorijos biudžetą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-286">You set up a budget for each category:</span></span>

-   <span data-ttu-id="0a42d-287">**Kūrimas** – išlaidos – 15 000, o pajamos – 20 000</span><span class="sxs-lookup"><span data-stu-id="0a42d-287">**Development** – Cost of 15,000 and revenue of 20,000</span></span>
-   <span data-ttu-id="0a42d-288">**Diegimas** – išlaidos – 5000, o pajamos – 10 000</span><span class="sxs-lookup"><span data-stu-id="0a42d-288">**Installation** – Cost of 5,000 and revenue of 10,000</span></span>

<span data-ttu-id="0a42d-289">Kai pirmą kartą kuriate sąskaitą faktūrą klientui, sąskaitos faktūros suma skaičiuojama automatiškai pagal toliau pateikiamą informaciją.</span><span class="sxs-lookup"><span data-stu-id="0a42d-289">When you create a customer invoice for the first time, the invoice amount is automatically calculated based on the following information:</span></span>

-   <span data-ttu-id="0a42d-290">Praėjus mėnesiui, projekto darbuotojas pateikia projekto grafiką.</span><span class="sxs-lookup"><span data-stu-id="0a42d-290">After a month, the worker on the project submits a timesheet for the project.</span></span> <span data-ttu-id="0a42d-291">Darbuotojo darbo valandų savikaina yra 5000 už kūrimą ir 1000 už diegimą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-291">The cost of the worker’s hours is 5,000 for development and 1,000 for installation.</span></span> <span data-ttu-id="0a42d-292">Atlikta 33 proc. kūrimo darbo (5000 – faktinė savikaina / 15 000 – biudžeto išlaidos) ir 20 proc. diegimo darbo (1000 – faktinė savikaina / 5000 – biudžeto išlaidos).</span><span class="sxs-lookup"><span data-stu-id="0a42d-292">The development work is 33 percent completed (5,000 actual cost/15,000 budget cost), and the installation work is 20 percent completed (1,000 actual cost/5,000 budget cost).</span></span>
-   <span data-ttu-id="0a42d-293">Sąskaitos faktūros suma – 8667 apskaičiuojama automatiškai (33 proc. 20 000 + 20 proc. 10 000).</span><span class="sxs-lookup"><span data-stu-id="0a42d-293">The invoice amount of 8,667 is automatically calculated (33 percent of 20,000 + 20 percent of 10,000).</span></span>
-   <span data-ttu-id="0a42d-294">Išrašote sąskaitą faktūrą, kurios suma yra 8667, ir išsiunčiate ją klientui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-294">You create an invoice for 8,667 and send it to the customer.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-agreed-upon-milestones"></a><span data-ttu-id="0a42d-295">Pavyzdys: sutartais etapais pagrįstos atsiskaitymo taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="0a42d-295">Example: Create a billing rule that is based on agreed-upon milestones</span></span>

<span data-ttu-id="0a42d-296">Jūsų organizacija, įmonė, konsultuojanti vadybos klausimais, sutaria atlikti vartojimo prekės, kurią klientas ketina pardavinėti, rinkos tyrimą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-296">Your organization, a management consulting firm, agrees to conduct market research for a consumer product that the customer plans to sell.</span></span> <span data-ttu-id="0a42d-297">Sutariama, kad klientas naudosis jūsų paslaugomis tris mėnesius, pradedant kovą, ir sumokės jūsų organizacijai 50 000.</span><span class="sxs-lookup"><span data-stu-id="0a42d-297">The customer agrees to use your services for a period of three months, starting in March, and agrees to pay your organization 50,000.</span></span> <span data-ttu-id="0a42d-298">Projektas susideda iš trijų etapų.</span><span class="sxs-lookup"><span data-stu-id="0a42d-298">The project has three milestones:</span></span>

-   <span data-ttu-id="0a42d-299">1 etapas: vartotojų duomenų rinkimas – kovo 31 d.</span><span class="sxs-lookup"><span data-stu-id="0a42d-299">Milestone 1: Collect consumer data – March 31</span></span>
-   <span data-ttu-id="0a42d-300">2 etapas: vartotojų duomenų analizė – balandžio 30 d.</span><span class="sxs-lookup"><span data-stu-id="0a42d-300">Milestone 2: Analyze consumer data – April 30</span></span>
-   <span data-ttu-id="0a42d-301">3 etapas: produkto perspektyvumo pasiūlymo pateikimas – gegužės 31 d.</span><span class="sxs-lookup"><span data-stu-id="0a42d-301">Milestone 3: Present a product viability proposal – May 31</span></span>

<span data-ttu-id="0a42d-302">Sutariama, kad klientas sumokės jūsų organizacijai 10 000 už pirmą etapą, 20 000 už antrą etapą ir 20 000 už trečią etapą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-302">The customer agrees to pay your organization 10,000 for the first milestone, 20,000 for the second milestone, and 20,000 for the third milestone.</span></span> 

<span data-ttu-id="0a42d-303">Rengdami projekto sutartį, sutariate, kad išrašysite klientui sąskaitas faktūras pagal įvykdytus etapus.</span><span class="sxs-lookup"><span data-stu-id="0a42d-303">When you set up the project contract, you agree to bill the customer based on the milestone that has been completed.</span></span> <span data-ttu-id="0a42d-304">Į atsiskaitymo taisyklės sąranką įtraukiami tolesni veiksmai.</span><span class="sxs-lookup"><span data-stu-id="0a42d-304">The billing rule setup includes the following steps:</span></span>

-   <span data-ttu-id="0a42d-305">Projekto etapus apibrėžimas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-305">Define the project milestones.</span></span>
-   <span data-ttu-id="0a42d-306">Įvykdžius kiekvieną etapą, klientui išrašomos sąskaitos faktūros sumos nustatymas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-306">Define the amount to invoice the customer when each milestone is completed.</span></span>

<span data-ttu-id="0a42d-307">Kovo 31 d. įvykdžius pirmą etapą, pažymite etapą kaip įvykdytą, tada kuriate sąskaitą faktūrą, kurios suma yra 10 000, ir siunčiate ją klientui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-307">When the first milestone is completed on March 31, you mark the milestone as completed, and then create an invoice for 10,000 and send it to the customer.</span></span> <span data-ttu-id="0a42d-308">Negalite sukurti sąskaitos faktūros už etapą, kol nepažymėjote jo kaip įvykdytą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-308">You can’t create an invoice for a milestone until you have marked the milestone as completed.</span></span>

### <a name="example-create-a-billing-rule-that-is-based-on-services-plus-a-management-fee"></a><span data-ttu-id="0a42d-309">Pavyzdys: paslaugomis ir administravimo mokesčiu pagrįstos atsiskaitymo taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="0a42d-309">Example: Create a billing rule that is based on services plus a management fee</span></span>

<span data-ttu-id="0a42d-310">Jūsų organizacija, įmonė, konsultuojanti vadybos klausimais, sutaria atlikti rinkos tyrimą, kad įvertintų produkto, kurį kuria klientas – mažmeninė įmonė – perspektyvumą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-310">Your organization, a management consulting firm, agrees to conduct market research to evaluate the viability of a product that the customer, a retail company, is developing.</span></span> <span data-ttu-id="0a42d-311">Sutarties sąlygose nurodoma, kad suteiksite trijų savo geriausių vadybos klausimais konsultuojančių specialistų paslaugas ir jie atliks tyrimą, grindžiamą laiku ir medžiagomis.</span><span class="sxs-lookup"><span data-stu-id="0a42d-311">The terms of the agreement specify that you will provide the services of your top three management consultants, who will conduct the research on a time-and-materials basis.</span></span> <span data-ttu-id="0a42d-312">Sutariama, kad klientas mokės 100 už valandą ir papildomą 10 proc. administravimo mokestį už konsultavimo valandas, priskiriamas projektui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-312">The customer agrees to pay 100 per hour, plus a 10 percent management fee for the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="0a42d-313">Rengdami projekto sutartį, sukurkite atsiskaitymo taisyklę pridėti 10 proc. administravimo mokestį prie konsultavimo valandų, kurios yra priskiriamos projektui.</span><span class="sxs-lookup"><span data-stu-id="0a42d-313">When you set up the project contract, create a billing rule to add a 10 percent management fee to the consulting hours that are charged to the project.</span></span> 

<span data-ttu-id="0a42d-314">Kai sukursite klientui sąskaitą faktūrą, į ją bus įtrauktas 10 proc. administravimo mokestis ir konsultavimo valandų savikaina.</span><span class="sxs-lookup"><span data-stu-id="0a42d-314">When you create an invoice for the customer, the customer is billed a 10 percent management fee plus the cost of the consulting hours.</span></span> <span data-ttu-id="0a42d-315">Pavyzdžiui, jei trys konsultantai su šiuo projektu iš viso dirbo 200 valandų, sąskaita faktūra, kurios suma yra 22 000, kuriama remiantis toliau pateikiamas skaičiavimais.</span><span class="sxs-lookup"><span data-stu-id="0a42d-315">For example, if the three consultants worked a total of 200 hours on the project, an invoice for 22,000 is created based on the following calculation:</span></span>

-   <span data-ttu-id="0a42d-316">200 valandų po 100 už valandą = 20 000</span><span class="sxs-lookup"><span data-stu-id="0a42d-316">200 hours at 100 per hour = 20,000</span></span>
-   <span data-ttu-id="0a42d-317">10 proc. administravimo mokestis = 2000</span><span class="sxs-lookup"><span data-stu-id="0a42d-317">10 percent management fee = 2,000</span></span>
-   <span data-ttu-id="0a42d-318">Bendra sąskaitos faktūros suma – 22 000</span><span class="sxs-lookup"><span data-stu-id="0a42d-318">Total invoice amount = 22,000</span></span>

<span data-ttu-id="0a42d-319">Jeigu mokesčius moka klientas, o jūs projekto sutartyje pasirinkote PVM grupę, PVM grupė automatiškai įvedama į atsiskaitymo taisyklę, susijusią su mokesčiais.</span><span class="sxs-lookup"><span data-stu-id="0a42d-319">If fees are taxable to a customer, and you select a sales tax group in the project contract, the sales tax group is automatically entered in a billing rule for fees.</span></span>

### <a name="example-create-a-billing-rule-for-the-value-of-time-and-materials"></a><span data-ttu-id="0a42d-320">Pavyzdys: laiko ir medžiagų vertės atsiskaitymo taisyklės kūrimas</span><span class="sxs-lookup"><span data-stu-id="0a42d-320">Example: Create a billing rule for the value of time and materials</span></span>

<span data-ttu-id="0a42d-321">Sutariama, kad jūsų organizacija, programinės įrangos klausimais konsultuojanti įmonė, suteiks penkis techninius konsultantus, kurie ateinančius šešis mėnesius dirbs klientui programinės įrangos kūrimo projekte.</span><span class="sxs-lookup"><span data-stu-id="0a42d-321">Your organization, a software consulting firm, agrees to provide five technical consultants to work on a software development project for a customer for the next six months.</span></span> <span data-ttu-id="0a42d-322">Sutariama, kad klientas mokės 150 už kiekvieną konsultavimo valandą, taip pat apmokės raštinės reikmenų išlaidas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-322">The customer agrees to pay 150 for each consulting hour, plus the cost of office supplies.</span></span> <span data-ttu-id="0a42d-323">Kiekvieno mėnesio pabaigoje jūsų organizacija siunčia klientui sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-323">Your organization sends an invoice to the customer at the end of each month.</span></span> 

<span data-ttu-id="0a42d-324">Rengdami projekto sutartį, sutariate, kad išrašysite klientui sąskaitą faktūrą kiekvieną mėnesį už projekte panaudotą laiką ir medžiagas.</span><span class="sxs-lookup"><span data-stu-id="0a42d-324">When you set up the project contract, you agree to bill the customer each month for time and materials on the project.</span></span> <span data-ttu-id="0a42d-325">Kuriate atsiskaitymo taisyklę, į kurią yra įtraukta tolesnė informacija.</span><span class="sxs-lookup"><span data-stu-id="0a42d-325">You create a billing rule that includes the following information:</span></span>

-   <span data-ttu-id="0a42d-326">Sutarties laikotarpis yra šeši mėnesiai.</span><span class="sxs-lookup"><span data-stu-id="0a42d-326">The contract period is six months.</span></span>
-   <span data-ttu-id="0a42d-327">Konsultavimo laikas skaičiuojamas pagal 150 už valandą tarifą.</span><span class="sxs-lookup"><span data-stu-id="0a42d-327">Consulting time is calculated at a rate of 150 per hour.</span></span>
-   <span data-ttu-id="0a42d-328">Sąskaita faktūra už raštinės reikmenis išrašoma pagal savikainą, o bendros projekto išlaidos negali viršyti 10 000.</span><span class="sxs-lookup"><span data-stu-id="0a42d-328">Office supplies are invoiced at cost, and the total cost for the project must not exceed 10,000.</span></span>
-   <span data-ttu-id="0a42d-329">Sąskaitą faktūrą klientui kuriate kiekvieno kalendorinio mėnesio pabaigoje projekto vykdymo metu.</span><span class="sxs-lookup"><span data-stu-id="0a42d-329">You create a customer invoice at the end of each calendar month during the project.</span></span>

<span data-ttu-id="0a42d-330">Per pirmą mėnesį projekto konsultantai iš viso užrašė 800 valandų.</span><span class="sxs-lookup"><span data-stu-id="0a42d-330">During the first month, a total of 800 hours are recorded by the consultants on the project.</span></span> <span data-ttu-id="0a42d-331">Projektui priskiriamų raštinės reikmenų išlaidų suma yra 2000.</span><span class="sxs-lookup"><span data-stu-id="0a42d-331">The cost of office supplies that are charged to the project is 2,000.</span></span> <span data-ttu-id="0a42d-332">Todėl mėnesio pabaigoje kuriate sąskaitą faktūrą, kurios suma yra 122 000. Suma skaičiuojama taip: 800 valandų po 150 už valandą ir 2000 už raštinės reikmenis.</span><span class="sxs-lookup"><span data-stu-id="0a42d-332">Therefore, at the end of the month, you create an invoice for 122,000, which is calculated as 800 hours at 150 per hour, plus 2,000 for office supplies.</span></span>





[!INCLUDE[footer-include](../includes/footer-banner.md)]