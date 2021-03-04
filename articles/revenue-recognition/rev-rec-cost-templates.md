---
title: Sąnaudų šablonų nustatymas
description: Šioje temoje pateikiama informacijos apie tai, kaip kurti ir naudoti sąnaudų šablonus programoje „Project Operations”.
author: sigitac
manager: tfehr
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 786b2b9b140f82d406044c2ed05761d7f46ee9e0
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642733"
---
# <a name="set-up-cost-templates"></a><span data-ttu-id="f7feb-103">Sąnaudų šablonų nustatymas</span><span class="sxs-lookup"><span data-stu-id="f7feb-103">Set up cost templates</span></span>

<span data-ttu-id="f7feb-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="f7feb-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="f7feb-105">Šioje temoje pateikiama informacijos apie tai, kaip kurti ir naudoti sąnaudų šablonus programoje „Project Operations”.</span><span class="sxs-lookup"><span data-stu-id="f7feb-105">This topic provides information about how to create and use cost templates in Project Operations.</span></span> <span data-ttu-id="f7feb-106">Sąnaudų šablonas nustato:</span><span class="sxs-lookup"><span data-stu-id="f7feb-106">A cost template determines:</span></span>

- <span data-ttu-id="f7feb-107">projekto kategorijas, taikomas prognozuojamoms ir faktinėms operacijoms, kurios bus įtrauktos į projekto atlikimo skaičiavimo procentinę vertę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-107">The project categories for forecast and actual transactions to be included in a percentage of the project completion calculation.</span></span> <span data-ttu-id="f7feb-108">Tada atlikimo procentais vertė naudojama siekiant apskaičiuoti pajamas;</span><span class="sxs-lookup"><span data-stu-id="f7feb-108">The percent-complete value is then used to calculate how much revenue is recognized.</span></span>
- <span data-ttu-id="f7feb-109">ar galima modifikuoti atlikimo procentinę vertę, jei ji apskaičiuojama automatiškai;</span><span class="sxs-lookup"><span data-stu-id="f7feb-109">Whether the percentage of completion can be modified if it's automatically calculated.</span></span>
- <span data-ttu-id="f7feb-110">ar atlikimo procentais vertė apskaičiuojama pagal sumas ar vienetus.</span><span class="sxs-lookup"><span data-stu-id="f7feb-110">Whether the percent complete is calculated based on amounts or units.</span></span>

## <a name="cost-template-example"></a><span data-ttu-id="f7feb-111">Sąnaudų šablono pavyzdys</span><span class="sxs-lookup"><span data-stu-id="f7feb-111">Cost template example</span></span>

<span data-ttu-id="f7feb-112">Dirbate su kliento žiniatinklio svetainės dizaino projektu ir už jį imate fiksuotą 10 000 USD mokestį.</span><span class="sxs-lookup"><span data-stu-id="f7feb-112">You are working on a web site design project for a customer in which you charge a flat fee of USD 10,000.</span></span> <span data-ttu-id="f7feb-113">Prognozuojate, kad jums reikės 100 valandų (5 000 USD) projektui užbaigti.</span><span class="sxs-lookup"><span data-stu-id="f7feb-113">You forecast that it will take 100 hours (USD 5,000) to complete the project.</span></span> <span data-ttu-id="f7feb-114">Taip pat numatote, kad reikės pirkti du lėktuvo bilietus ir užsisakyti keturias nakvynes viešbutyje, nes reikės nuvykti pas klientą (1 800 USD).</span><span class="sxs-lookup"><span data-stu-id="f7feb-114">You also forecast two plane tickets and four nights in a hotel for trips to the customer's site (USD 1,800).</span></span> <span data-ttu-id="f7feb-115">Taigi bendra prognozuojama savikaina yra 6 800 USD.</span><span class="sxs-lookup"><span data-stu-id="f7feb-115">This results in a total forecasted cost of USD 6,800.</span></span>

<span data-ttu-id="f7feb-116">Paleidę fiksuotos kainos įplaukų pripažinimo procesą, kad mėnesio pabaigoje sukurtumėte įvertinimą, pamatote, kad projektui skyrėte 35 valandas.</span><span class="sxs-lookup"><span data-stu-id="f7feb-116">When you run the fixed-price revenue recognition process to create an estimate at the end of the month, you find that you have worked 35 hours on the project.</span></span> <span data-ttu-id="f7feb-117">Tai dar neapima skrydžių arba viešbučio išlaidų.</span><span class="sxs-lookup"><span data-stu-id="f7feb-117">This doesn't yet include flights or hotel costs.</span></span> <span data-ttu-id="f7feb-118">Jūs taip pat turėjote padėjėją, kuris atliko penkių valandų trukmės tyrimą, susijusį su projektu, kuriam sumokėjote 100 USD, ir šios išlaidos nebuvo suplanuotos.</span><span class="sxs-lookup"><span data-stu-id="f7feb-118">You also had an assistant perform five hours of research for the project at a cost of USD 100, which you hadn't planned for.</span></span>

<span data-ttu-id="f7feb-119">Norėdami apskaičiuoti šio projekto atlikimo procentais vertę, turite atsakyti į toliau nurodytus klausimus.</span><span class="sxs-lookup"><span data-stu-id="f7feb-119">When you calculate the percent complete value for this project, you have the following choices to make:</span></span>

- <span data-ttu-id="f7feb-120">Ar norite įtraukti visas išlaidas (valandas ir išlaidas) ar tik valandas?</span><span class="sxs-lookup"><span data-stu-id="f7feb-120">Do you want to include all costs (hours and expenses) or just hours?</span></span>
- <span data-ttu-id="f7feb-121">Ar norite įtraukti visas valandas ir tik suplanuotas valandas?</span><span class="sxs-lookup"><span data-stu-id="f7feb-121">Do you want to include all hours or only planned hours?</span></span>
- <span data-ttu-id="f7feb-122">Ar norite apskaičiuoti atlikimo procentais vertę remdamiesi suplanuotų valandų (5 000 USD) savikaina doleriais ar tik remdamiesi valandų skaičiumi (100)?</span><span class="sxs-lookup"><span data-stu-id="f7feb-122">Do you want to calculate the percent complete based on the dollar cost of the planned hours (USD 5,000) or just on the number of hours (100)?</span></span>

<span data-ttu-id="f7feb-123">Nuo jūsų atsakymų į šiuos klausimus priklauso sąnaudų šablono parinktys, kurias nustatysite, ir kategorijos, kurias pasirinksite sąnaudų šablono eilutėse.</span><span class="sxs-lookup"><span data-stu-id="f7feb-123">Your answers to these questions determine the options that you set on the cost template and the categories that you select on the cost template lines.</span></span>

<span data-ttu-id="f7feb-124">Toliau esančioje lentelėje parodyti skirtingų šio scenarijaus atlikimo procentais vertės apskaičiavimo metodų rezultatai.</span><span class="sxs-lookup"><span data-stu-id="f7feb-124">The following table illustrates the results of different methods of calculating the percent-complete value for this scenario.</span></span>

| <span data-ttu-id="f7feb-125">Atlikimo pagrindas</span><span class="sxs-lookup"><span data-stu-id="f7feb-125">Completion based on</span></span> | <span data-ttu-id="f7feb-126">Savikaina doleriais arba vienetai</span><span class="sxs-lookup"><span data-stu-id="f7feb-126">Dollar cost or units</span></span> | <span data-ttu-id="f7feb-127">Atlikimo procentas</span><span class="sxs-lookup"><span data-stu-id="f7feb-127">Percent complete</span></span> | <span data-ttu-id="f7feb-128">Skaičiavimas</span><span class="sxs-lookup"><span data-stu-id="f7feb-128">Calculation</span></span> |
| --- | --- | --- | --- |
| <span data-ttu-id="f7feb-129">Visos valandos, be išlaidų</span><span class="sxs-lookup"><span data-stu-id="f7feb-129">All hours, no expenses</span></span> | <span data-ttu-id="f7feb-130">Savikaina doleriais</span><span class="sxs-lookup"><span data-stu-id="f7feb-130">Dollar cost</span></span> | <span data-ttu-id="f7feb-131">37 % 35 x 50 USD + 100 USD = 1 850 USD 1 850 USD iš 5 000 USD</span><span class="sxs-lookup"><span data-stu-id="f7feb-131">37% 35 x USD 50 + USD 100 = USD 1,850 USD 1,850/USD 5,000</span></span> |
| <span data-ttu-id="f7feb-132">Visos valandos, be išlaidų</span><span class="sxs-lookup"><span data-stu-id="f7feb-132">All hours, no expenses</span></span> | <span data-ttu-id="f7feb-133">Vienetai</span><span class="sxs-lookup"><span data-stu-id="f7feb-133">Units</span></span> | <span data-ttu-id="f7feb-134">40 %</span><span class="sxs-lookup"><span data-stu-id="f7feb-134">40%</span></span> | <span data-ttu-id="f7feb-135">40 valandų iš 100 valandų (įskaitant penkias nesuplanuotas valandas)</span><span class="sxs-lookup"><span data-stu-id="f7feb-135">40 hours/100 hours (including five unplanned hours)</span></span> |
| <span data-ttu-id="f7feb-136">Suplanuotos valandos, be išlaidų</span><span class="sxs-lookup"><span data-stu-id="f7feb-136">Planned hours, no expenses</span></span> | <span data-ttu-id="f7feb-137">Savikaina doleriais arba vienetai</span><span class="sxs-lookup"><span data-stu-id="f7feb-137">Dollar cost or unit</span></span> | <span data-ttu-id="f7feb-138">35 %</span><span class="sxs-lookup"><span data-stu-id="f7feb-138">35%</span></span> | <span data-ttu-id="f7feb-139">35 iš 100 valandų arba 35 x 50 USD / 5 000 USD</span><span class="sxs-lookup"><span data-stu-id="f7feb-139">35/100 hours or 35 x USD 50/5,000</span></span> |
| <span data-ttu-id="f7feb-140">Visos valandos ir išlaidos</span><span class="sxs-lookup"><span data-stu-id="f7feb-140">All hours and expenses</span></span> | <span data-ttu-id="f7feb-141">Savikaina doleriais</span><span class="sxs-lookup"><span data-stu-id="f7feb-141">Dollar cost</span></span> | <span data-ttu-id="f7feb-142">27,2 %</span><span class="sxs-lookup"><span data-stu-id="f7feb-142">27.2%</span></span> | <span data-ttu-id="f7feb-143">1 850 USD iš 6 800 USD</span><span class="sxs-lookup"><span data-stu-id="f7feb-143">USD 1,850/USD 6,800</span></span> |

<span data-ttu-id="f7feb-144">Sprendimas, kokį sąnaudų šabloną kurti, priklauso nuo įvairių aspektų.</span><span class="sxs-lookup"><span data-stu-id="f7feb-144">Deciding which approach to take to create a cost template can depend on several considerations:</span></span>

- <span data-ttu-id="f7feb-145">Jei į sąnaudų šabloną įtrauksite neplanuotas valandas, kyla rizika, kad pasieksite 100 procentų dar nebaigę projekto.</span><span class="sxs-lookup"><span data-stu-id="f7feb-145">If you include unplanned hours in the cost template, you risk reaching 100 percent complete before the project is finished.</span></span> <span data-ttu-id="f7feb-146">Taip bus todėl, kad faktinės valandos viršys suplanuotas valandas.</span><span class="sxs-lookup"><span data-stu-id="f7feb-146">This is because actual hours will be greater than planned hours.</span></span> <span data-ttu-id="f7feb-147">Jei naudosite vieną iš pirmųjų dviejų metodų, pateiktų lentelėje, turėtumėte pakeisti planą (prognozuojamus vienetus), kai yra nuokrypių.</span><span class="sxs-lookup"><span data-stu-id="f7feb-147">If you use either of the first two methods listed in the table, you should change the plan (forecasted units) when you become aware of deviations.</span></span> <span data-ttu-id="f7feb-148">Tokiu atveju turėsite pridėti arba atimti valandas remdamiesi savo žiniomis apie tai, ko reikia projektui baigti.</span><span class="sxs-lookup"><span data-stu-id="f7feb-148">In this case, you would add or subtract hours based on your knowledge of what is required to finish the project.</span></span> <span data-ttu-id="f7feb-149">Jei projektui užbaigti reikės dar 65 valandų, į planą įtrauksite penkias valandas ir iš viso bus 105 valandos.</span><span class="sxs-lookup"><span data-stu-id="f7feb-149">If the project will require another 65 hours to complete, you would add five hours to the plan for a total of 105.</span></span> <span data-ttu-id="f7feb-150">Jei žinote, kad jūsų padėjėjas atliks dar vieną penkių valandų tyrimą, iš viso bus 110 valandų.</span><span class="sxs-lookup"><span data-stu-id="f7feb-150">If you know that your assistant will perform another five hours of research, the total will become 110 hours.</span></span>
- <span data-ttu-id="f7feb-151">Jei naudojate trečiąjį lentelėje pateiktą metodą, reikės tik atnaujinti suplanuotas savo laiko valandas, kad užtikrintumėte tikslų atlikimo procentais skaičiavimą.</span><span class="sxs-lookup"><span data-stu-id="f7feb-151">If you use the third method listed in the table, you would only update the planned hours for your own time to keep the percent-complete calculation accurate.</span></span> <span data-ttu-id="f7feb-152">Jūsų pelningumo vertė pasikeis užregistravus neplanuotas valandas, bet žinosite atlikimo procentais vertę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-152">Your profitability will change when unplanned hours are logged, but you will remain on a known percent-complete trajectory.</span></span>
- <span data-ttu-id="f7feb-153">Jei naudojate ketvirtąjį lentelėje pateiktą metodą, kyla rizika, kad išlaidos bus nereguliarios ir jos gali neatsispindėti atlikimo eigoje.</span><span class="sxs-lookup"><span data-stu-id="f7feb-153">If you use the fourth method listed in the table, the risk is that expenses will occur at irregular times and may not be reflected in your completion progress.</span></span> <span data-ttu-id="f7feb-154">Todėl, jei bus įtrauktos išlaidos, jūsų atlikimo procentinė dalis gali svyruoti labiau, nei norite.</span><span class="sxs-lookup"><span data-stu-id="f7feb-154">Therefore, if the expenses are included, they can cause your percent complete to fluctuate more than is desirable.</span></span> <span data-ttu-id="f7feb-155">Pavyzdžiui, jūsų skrydžio dar nebuvo, todėl atlikimo procentinė vertė yra 27 proc. vietoj 35 proc. arba 37 proc., jei skaičiavimas grindžiamas tik laiko duomenimis.</span><span class="sxs-lookup"><span data-stu-id="f7feb-155">For example, because you didn't take a flight yet, your percent complete was 27 percent instead of 35 percent or 37 percent if you were to base the calculation on time alone.</span></span> <span data-ttu-id="f7feb-156">Jei vieną kartą skridote pas klientą ir dvi naktis praleidote viešbutyje, ir tiksliai numatėte skrydžio ir viešbučio išlaidas, atlikimo procentinė vertė būtų 40,4 proc. (1 850 USD už darbą ir 900 USD išlaidoms = 2 750 USD iš 6 800 USD = 40,4 proc.).</span><span class="sxs-lookup"><span data-stu-id="f7feb-156">If you had taken one trip for two nights and forecasted your flight and hotel costs accurately, the percent complete would have been 40.4 percent (USD 1850 for labor and USD 900 for expenses = USD 2750/USD 6800 = 40.4 percent).</span></span> <span data-ttu-id="f7feb-157">Todėl įtraukus tik vienos kelionės lėktuvu išlaidas, atlikimo procentinė vertė pasikeistų iš 27 proc. į 40 proc.</span><span class="sxs-lookup"><span data-stu-id="f7feb-157">Therefore, incurring the expenses for just one plane trip would change the percent complete from 27 percent to 40 percent.</span></span>

## <a name="create-cost-templates"></a><span data-ttu-id="f7feb-158">Sąnaudų šablonų kūrimas</span><span class="sxs-lookup"><span data-stu-id="f7feb-158">Create cost templates</span></span>
<span data-ttu-id="f7feb-159">Norėdami sukurti sąnaudų šabloną, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f7feb-159">To create cost templates, follow these steps:</span></span>

1. <span data-ttu-id="f7feb-160">Norėdami pasiekti sąnaudų šablonus, „Dynamics 365 Finance“ aplinkoje eikite į **Projektų valdymas ir apskaita** > **Sąranka** > **Įvertinimai** > **Sąnaudų šablonas**.</span><span class="sxs-lookup"><span data-stu-id="f7feb-160">To access cost templates, in the Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Cost template**.</span></span>
2. <span data-ttu-id="f7feb-161">Norėdami sukurti naują sąnaudų šabloną, pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f7feb-161">Select **New** to create new cost template.</span></span> <span data-ttu-id="f7feb-162">Įveskite pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="f7feb-162">Enter a name and description.</span></span>
3. <span data-ttu-id="f7feb-163">Nurodykite kiekvieno tipo operacijos sąnaudų eilutės ID.</span><span class="sxs-lookup"><span data-stu-id="f7feb-163">Provide cost line ID for each transaction type.</span></span>
4. <span data-ttu-id="f7feb-164">Pasirinkite numatytąjį atlikimo skaičiavimo metodą:</span><span class="sxs-lookup"><span data-stu-id="f7feb-164">Select a default completion method:</span></span>

  - <span data-ttu-id="f7feb-165">**Automatinis**: projekto atlikimo procentinė vertė apskaičiuojama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="f7feb-165">**Automatic**: Percentage of completion is calculated automatically on a project.</span></span> <span data-ttu-id="f7feb-166">Gautos vertės pakeisti negalima.</span><span class="sxs-lookup"><span data-stu-id="f7feb-166">The resulting value can't be changed.</span></span>
  - <span data-ttu-id="f7feb-167">**Rankinis**: projekto atlikimo procentinė vertė apskaičiuojama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="f7feb-167">**Manual**: Percentage of completion is calculated automatically on a project.</span></span> <span data-ttu-id="f7feb-168">Gautą vertę galima pakeisti.</span><span class="sxs-lookup"><span data-stu-id="f7feb-168">The resulting value can be changed.</span></span>

  > [!NOTE]
  > <span data-ttu-id="f7feb-169">Atliekant skaičiavimus rankiniu būdu, atlikimo procentinė vertė tvarkoma puslapio **Įvertinimas** skirtuko **Bendra** dalyje **Skaičiavimas rankiniu būdu**.</span><span class="sxs-lookup"><span data-stu-id="f7feb-169">For manual calculations, the percentage of completion is maintained in **Manual calculation** on the **General** tab on the **Estimate** page.</span></span>

5. <span data-ttu-id="f7feb-170">Dalyje **Užbaigimas pagrįstas** pasirinkite vieną iš toliau nurodytų verčių:</span><span class="sxs-lookup"><span data-stu-id="f7feb-170">In **Completion based on**, select one of the following values:</span></span>

  - <span data-ttu-id="f7feb-171">**Suma**: suma apskaitos valiuta apskaičiuoja atlikimo procentinę vertę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-171">**Amount**: The amount in accounting currency calculates the percentage of completion.</span></span>
  - <span data-ttu-id="f7feb-172">**Vienetas**: kiekis apskaičiuoja atlikimo procentinę vertę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-172">**Unit**: The quantity calculates the percentage of completion.</span></span>
  - <span data-ttu-id="f7feb-173">**Tiesiogiai proporcingas metodas**: sistema proporcingai apskaičiuoja atlikimo procentinę vertę naudodama projekto pradžios ir pabaigos datas, kad nustatytų projekto trukmę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-173">**Straight line**: The system calculates the percentage of completion on a proportionate basis by using the project start and end dates to determine the length of the project.</span></span>

6. <span data-ttu-id="f7feb-174">Pasirinkite **Sąnaudų eilutės**, kad peržiūrėtumėte sąnaudų šablono sąnaudų eilutes.</span><span class="sxs-lookup"><span data-stu-id="f7feb-174">Select **Cost lines** to review the cost lines of the cost template.</span></span> <span data-ttu-id="f7feb-175">Kiekvienas operacijos tipas turi turėti bent vieną sąnaudų eilutę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-175">At least one cost line is required for every transaction type.</span></span> <span data-ttu-id="f7feb-176">Tačiau galite kurti kelias sąnaudų eilutes tiems patiems operacijos tipams ir nustatyti norimus šių eilučių atributus.</span><span class="sxs-lookup"><span data-stu-id="f7feb-176">However, you can create multiple cost lines for the same transaction types and set the desired attributes for these lines.</span></span>
7. <span data-ttu-id="f7feb-177">Skirtuke **Kategorijos** pasirinkite projekto kategorijas, kurios bus įtrauktos į sąnaudų šablono eilutę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-177">On the **Categories** tab, select the project categories to be included on the cost template line.</span></span>
8. <span data-ttu-id="f7feb-178">Skirtuke **Bendra** pasirinkite, ar ši eilutė bus įtraukta apskaičiuojant atlikimo procentinę vertę.</span><span class="sxs-lookup"><span data-stu-id="f7feb-178">On the **General** tab, select if this line will be included in the percentage of completion calculation.</span></span>
9. <span data-ttu-id="f7feb-179">Pasirinkite užbaigimo išlaidų apskaičiavimo metodą, kuris bus naudojamas atlikimo procentinei vertei apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="f7feb-179">Select the cost to complete method to be used when calculating the percentage of completion.</span></span>