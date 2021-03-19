---
title: Vienetų grupės ir vienetai
description: Šioje temoje pateikiama informacija apie vienetų grupes ir vienetus.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
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
ms.openlocfilehash: 45e4a95b429cd9d1f174653bd28cf567f690676d
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291629"
---
# <a name="unit-groups-and-units"></a><span data-ttu-id="a6bbd-103">Vienetų grupės ir vienetai</span><span class="sxs-lookup"><span data-stu-id="a6bbd-103">Unit groups and units</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a6bbd-104">Vienetų grupės ir vienetai yra pagrindiniai „Microsoft Dynamics 365“ objektai.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-104">Unit groups and units are basic entities in Microsoft Dynamics 365.</span></span> <span data-ttu-id="a6bbd-105">Vienetas – tai vienas matavimo vienetas, o kelis vienetus galima sugrupuoti į vienetų grupes.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-105">A unit is a single unit of measure, and multiple units can be grouped into unit groups.</span></span> <span data-ttu-id="a6bbd-106">Vienetų grupė kartais „Dynamics 365“ vartotojo sąsajoje (UI) vadinama vienetų grafiku.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-106">A unit group is sometimes referred to as a unit schedule in the Dynamics 365 user interface (UI).</span></span> 

<span data-ttu-id="a6bbd-107">Toliau pateikiami keli vienetų ir vienetų grupių pavyzdžiai.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-107">Here are some examples of units and unit groups:</span></span>
 
- <span data-ttu-id="a6bbd-108">**Vienetų grupė**: atstumas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-108">**Unit group**: Distance</span></span> 
    - <span data-ttu-id="a6bbd-109">**Vienetai**: mylia, kilometras ir pan.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-109">**Units**: Mile, Kilometer, and so on.</span></span>
- <span data-ttu-id="a6bbd-110">**Vienetų grupė**: laikas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-110">**Unit group**: Time</span></span>
    - <span data-ttu-id="a6bbd-111">**Vienetai**: valanda, diena, savaitė ir pan.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-111">**Units**: Hour, day, week, and so on.</span></span> 

<span data-ttu-id="a6bbd-112">Nustatę kelis vienetų grupės vienetus, taip pat turite nustatyti jų konvertavimo koeficientą, nurodydami pirmąjį vienetą, kurį nustatote kaip numatytąjį arba pagrindinį vienetų grupės vienetą.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-112">When you set up multiple units in a unit group, you must also set up a conversion factor between them by designating the first unit that you set up as the default or primary unit for the unit group.</span></span> 

<span data-ttu-id="a6bbd-113">Pavyzdžiui, jei vienetų grupėje **Laikas** nustatysite parinktį **Valanda** kaip pirmąjį vienetą, sistema paskirs reikšmę **Valanda** kaip numatytąjį vienetą.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-113">For example, in a **Time** unit group, if you set up **Hour** as the first unit, the system designates **Hour** as the default unit.</span></span> <span data-ttu-id="a6bbd-114">Jei kitas nustatytas vienetas yra **Diena**, turite nustatyti vieneto **Diena** konvertavimo koeficientą **Valanda**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-114">If the next unit that you set up is **Day**, you must set up a conversion factor for **Day** to **Hour**.</span></span> <span data-ttu-id="a6bbd-115">Jei tada kaip trečią vienetą įtrauksite **Savaitė**, reikės nustatyti vieneto **Savaitė** konvertavimo koeficientą **Diena** arba **Valanda**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-115">If you then add **Week** as a third unit, you must set up a conversion factor for **Week** in terms of **Day** or **Hour**.</span></span> 

<span data-ttu-id="a6bbd-116">Tolesniame paveiksle pateikiamas vieneto **Diena**, kurio lauke **Kiekis** rodomas dienos valandų skaičius, ir vieneto **Savaitė**, kurio lauke **Kiekis** rodomas, savaitės dienų skaičius, sąrankos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-116">The following image shows an example setup for the **Day** unit, where the **Quantity** field shows the number of hours that are in a day, and **Week**, where the **Quantity** field show the number of days that are in a week.</span></span>

> ![Vienetų grupė: informacijos puslapis](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a><span data-ttu-id="a6bbd-118">Vienetų ir vienetų grupių naudojimas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-118">Using units and unit groups</span></span>

<span data-ttu-id="a6bbd-119">„Dynamics 365 Project Service Automation“ apdorojant įvertinimus ir įrašus naudoja vienetus ir vienetų grupes.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-119">Dynamics 365 Project Service Automation uses units and unit groups to process estimates and entries for both expenses and time.</span></span> 

<span data-ttu-id="a6bbd-120">Apdorojant išlaidas kiekvienai išlaidų kategorijai nustatoma numatytoji vienetų grupė ir vienetas.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-120">For expenses, each expense category has a default unit group and unit.</span></span> <span data-ttu-id="a6bbd-121">Šios reikšmės įvedamos kaip numatytosios reikšmės į išlaidų kategorijų kainoraščio įrašus.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-121">These values are entered as default values on price list entries for expense categories.</span></span> 

<span data-ttu-id="a6bbd-122">Pavyzdžiui, turite išlaidų kategoriją pavadinimu **Kilometražas**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-122">For example, you have an expense category that is named **Mileage**.</span></span> <span data-ttu-id="a6bbd-123">Joje yra vienetų grupė pavadinimu **Atstumas** ir numatytasis vienetas pavadinimu **Mylia**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-123">It has a unit group that is named **Distance** and a default unit that is named **Mile**.</span></span> <span data-ttu-id="a6bbd-124">Jei vienetų grupėje **Atstumas** nustatysite du vienetus (**Mylia** ir **Kilometras**), viename kainoraštyje galėsite nustatyti dvi kategorijos **Kilometražas** kainas: kainą už mylią ir kainą už kilometrą.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-124">If you set up the **Distance** unit group so that it has two units (**Mile** and **Kilometer**), you can set two prices for the **Mileage** category on one price list: price per mile and price per kilometer.</span></span>

| <span data-ttu-id="a6bbd-125">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="a6bbd-125">Expense category</span></span>  | <span data-ttu-id="a6bbd-126">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="a6bbd-126">Unit group</span></span>  | <span data-ttu-id="a6bbd-127">Vienetas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-127">Unit</span></span>      | <span data-ttu-id="a6bbd-128">Kainodaros metodas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-128">Pricing method</span></span>  | <span data-ttu-id="a6bbd-129">Vieneto kaina</span><span class="sxs-lookup"><span data-stu-id="a6bbd-129">Price per unit</span></span>  |
|-------------------|---------------|-----------|-------------------|-------------------|
| <span data-ttu-id="a6bbd-130">Kilometražas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-130">Mileage</span></span>           | <span data-ttu-id="a6bbd-131">Atstumas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-131">Distance</span></span>      | <span data-ttu-id="a6bbd-132">Mylia</span><span class="sxs-lookup"><span data-stu-id="a6bbd-132">Mile</span></span>      | <span data-ttu-id="a6bbd-133">Vieneto kaina</span><span class="sxs-lookup"><span data-stu-id="a6bbd-133">Price per unit</span></span>    | <span data-ttu-id="a6bbd-134">10 USD</span><span class="sxs-lookup"><span data-stu-id="a6bbd-134">10 USD</span></span>            |
| <span data-ttu-id="a6bbd-135">Kilometražas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-135">Mileage</span></span>           | <span data-ttu-id="a6bbd-136">Atstumas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-136">Distance</span></span>      | <span data-ttu-id="a6bbd-137">Kilometras</span><span class="sxs-lookup"><span data-stu-id="a6bbd-137">Kilometer</span></span> | <span data-ttu-id="a6bbd-138">Vieneto kaina</span><span class="sxs-lookup"><span data-stu-id="a6bbd-138">Price per unit</span></span>    |  <span data-ttu-id="a6bbd-139">6 USD</span><span class="sxs-lookup"><span data-stu-id="a6bbd-139">6 USD</span></span>            |

<span data-ttu-id="a6bbd-140">Kai įvedate projekto išlaidas, sistema nustato kainą naudodama išlaidų kategorijos ir vieneto derinį.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-140">When you enter an expense on a project, the system determines the price through the combination of the category and the unit on the expense.</span></span> 

| <span data-ttu-id="a6bbd-141">Išlaidų aprašas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-141">Expense description</span></span>        | <span data-ttu-id="a6bbd-142">Išlaidų kategorija</span><span class="sxs-lookup"><span data-stu-id="a6bbd-142">Expense category</span></span>  | <span data-ttu-id="a6bbd-143">Vienetas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-143">Unit</span></span>  | <span data-ttu-id="a6bbd-144">Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6bbd-144">Quantity</span></span>  | <span data-ttu-id="a6bbd-145">Vieneto kaina</span><span class="sxs-lookup"><span data-stu-id="a6bbd-145">Unit price</span></span>   |
|----------------------------|---------------------|-------|-----------|----------------|
| <span data-ttu-id="a6bbd-146">Važiavimas į kliento vietą</span><span class="sxs-lookup"><span data-stu-id="a6bbd-146">Drive to client location</span></span> | <span data-ttu-id="a6bbd-147">Kilometražas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-147">Mileage</span></span>             | <span data-ttu-id="a6bbd-148">Mylia</span><span class="sxs-lookup"><span data-stu-id="a6bbd-148">Mile</span></span>  | <span data-ttu-id="a6bbd-149">10</span><span class="sxs-lookup"><span data-stu-id="a6bbd-149">10</span></span>        | <span data-ttu-id="a6bbd-150">10 USD</span><span class="sxs-lookup"><span data-stu-id="a6bbd-150">10 USD</span></span>         |

<span data-ttu-id="a6bbd-151">Laiko kategorijoje kiekvieno kainoraščio antraštėje yra laukas **Numatytasis laiko vienetas**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-151">For time, each price list header has a **Default Time Unit** field.</span></span> <span data-ttu-id="a6bbd-152">Reikšmė nustatoma kuriant kainoraščio antraštę.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-152">The value is set when you create the price list header.</span></span> <span data-ttu-id="a6bbd-153">Tada šis vienetas naudojamas nustatant visas vaidmenimis pagrįstas kainas šiame kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-153">This unit is then used to set all role-based prices on that price list.</span></span>

<span data-ttu-id="a6bbd-154">Lauko **Pasiūlyme nurodytas laikas** įvertinimų eilutes galima išreikšti bet kuriuo laiko vienetu.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-154">Estimate lines for the **Time on Quote** field can be expressed in any unit of time.</span></span> <span data-ttu-id="a6bbd-155">Tačiau projektų įvertinimo eilutėse ir projektų laiko įrašuose galima naudoti tik vienetą **Valanda**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-155">However, estimate lines on projects and time entries for projects can use only the **Hour** unit of time.</span></span> <span data-ttu-id="a6bbd-156">Jei laiko įrašo arba įvertinimo eilutės vienetas neatitinka to vaidmens kainoraščio eilutės vieneto, sistema konvertuoja kainą į vienetus, nustatytus projekto įvertinime arba faktinėje projekto operacijoje.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-156">If the unit on the time entry or estimate line doesn't match the unit on the price list line for that role, the system converts the price to the units that are defined in the project estimate or the project actual transaction.</span></span>

<span data-ttu-id="a6bbd-157">Tolesniame pavyzdyje parodyta, kaip PSA naudoja vienetų grupę, vienetus ir konvertavimo koeficientus.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-157">The following example shows how PSA uses the unit group, units, and conversion factors.</span></span>
- <span data-ttu-id="a6bbd-158">Vienetai</span><span class="sxs-lookup"><span data-stu-id="a6bbd-158">Units</span></span>

   - <span data-ttu-id="a6bbd-159">**Vienetų grupė**: laikas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-159">**Unit group**: Time</span></span> 
   - <span data-ttu-id="a6bbd-160">**Vienetai**: valanda</span><span class="sxs-lookup"><span data-stu-id="a6bbd-160">**Units**: Hour</span></span> 
    
    - <span data-ttu-id="a6bbd-161">**Diena** – konvertavimo koeficientas: 8 valandos</span><span class="sxs-lookup"><span data-stu-id="a6bbd-161">**Day** - Conversion factor: 8 hours</span></span>       
    - <span data-ttu-id="a6bbd-162">**Savaitė** – konvertavimo koeficientas: 40 valandos</span><span class="sxs-lookup"><span data-stu-id="a6bbd-162">**Week** - Conversion factor: 40 hours</span></span>  
        
- <span data-ttu-id="a6bbd-163">A projekto kainoraščio sąranka</span><span class="sxs-lookup"><span data-stu-id="a6bbd-163">Price list setup on Project A:</span></span>

    - <span data-ttu-id="a6bbd-164">**Pavadinimas**: 2016 m. pardavimo JK kainos</span><span class="sxs-lookup"><span data-stu-id="a6bbd-164">**Name**: UK sales prices 2016</span></span> 
    - <span data-ttu-id="a6bbd-165">**Numatytasis laiko vienetas**: diena</span><span class="sxs-lookup"><span data-stu-id="a6bbd-165">**Default time unit**: Day</span></span> 
    - <span data-ttu-id="a6bbd-166">**Valiuta**: GBP</span><span class="sxs-lookup"><span data-stu-id="a6bbd-166">**Currency**: GBP</span></span>

| <span data-ttu-id="a6bbd-167">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="a6bbd-167">Role</span></span>      | <span data-ttu-id="a6bbd-168">Vienetų grupė</span><span class="sxs-lookup"><span data-stu-id="a6bbd-168">Unit group</span></span> | <span data-ttu-id="a6bbd-169">Vienetas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-169">Unit</span></span> | <span data-ttu-id="a6bbd-170">Organizacijos vienetas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-170">Organizational unit</span></span> | <span data-ttu-id="a6bbd-171">Kaina</span><span class="sxs-lookup"><span data-stu-id="a6bbd-171">Price</span></span>   |
|-----------|------------|------|---------------------|---------|
| <span data-ttu-id="a6bbd-172">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-172">Developer</span></span> | <span data-ttu-id="a6bbd-173">Time</span><span class="sxs-lookup"><span data-stu-id="a6bbd-173">Time</span></span>       | <span data-ttu-id="a6bbd-174">Day</span><span class="sxs-lookup"><span data-stu-id="a6bbd-174">Day</span></span>  | <span data-ttu-id="a6bbd-175">Danys</span><span class="sxs-lookup"><span data-stu-id="a6bbd-175">Contoso UK</span></span>          | <span data-ttu-id="a6bbd-176">800 GBP</span><span class="sxs-lookup"><span data-stu-id="a6bbd-176">800 GBP</span></span> |

### <a name="time-entry"></a><span data-ttu-id="a6bbd-177">Laiko įrašas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-177">Time entry</span></span>

<span data-ttu-id="a6bbd-178">Tolesnėje lentelėje parodyta PSA sukurta trijų valandų projekto pardavimo operacija.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-178">The following table shows the resulting sales-side transaction created by PSA for a three hour project.</span></span>


| <span data-ttu-id="a6bbd-179">Projektas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-179">Project</span></span>   | <span data-ttu-id="a6bbd-180">Užduotis</span><span class="sxs-lookup"><span data-stu-id="a6bbd-180">Task</span></span>    | <span data-ttu-id="a6bbd-181">Vaidmuo</span><span class="sxs-lookup"><span data-stu-id="a6bbd-181">Role</span></span>      | <span data-ttu-id="a6bbd-182">Kiekis</span><span class="sxs-lookup"><span data-stu-id="a6bbd-182">Quantity</span></span> | <span data-ttu-id="a6bbd-183">Vienetas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-183">Unit</span></span>  | <span data-ttu-id="a6bbd-184">Vieneto kaina</span><span class="sxs-lookup"><span data-stu-id="a6bbd-184">Unit price</span></span> | <span data-ttu-id="a6bbd-185">Pardavimo suma, kuriai neišrašyta sąskaita</span><span class="sxs-lookup"><span data-stu-id="a6bbd-185">Unbilled sales amount</span></span> |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| <span data-ttu-id="a6bbd-186">A projektas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-186">Project A</span></span> | <span data-ttu-id="a6bbd-187">Dizainas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-187">Design</span></span>  | <span data-ttu-id="a6bbd-188">Kūrėjas</span><span class="sxs-lookup"><span data-stu-id="a6bbd-188">Developer</span></span> | <span data-ttu-id="a6bbd-189">3</span><span class="sxs-lookup"><span data-stu-id="a6bbd-189">3</span></span>        | <span data-ttu-id="a6bbd-190">Hour</span><span class="sxs-lookup"><span data-stu-id="a6bbd-190">Hour</span></span>  | <span data-ttu-id="a6bbd-191">100 GBP</span><span class="sxs-lookup"><span data-stu-id="a6bbd-191">100 GBP</span></span>    | <span data-ttu-id="a6bbd-192">300 GBP</span><span class="sxs-lookup"><span data-stu-id="a6bbd-192">300 GBP</span></span>               |

## <a name="time-unit-faq"></a><span data-ttu-id="a6bbd-193">DUK apie laiko vienetus</span><span class="sxs-lookup"><span data-stu-id="a6bbd-193">Time unit FAQ</span></span>

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a><span data-ttu-id="a6bbd-194">Ar PSA konvertuoja išlaidas į kitus vienetus?</span><span class="sxs-lookup"><span data-stu-id="a6bbd-194">Does PSA convert to different units in the case of expenses?</span></span>
<span data-ttu-id="a6bbd-195">Ne.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-195">No.</span></span> <span data-ttu-id="a6bbd-196">Galimas tik laiko vienetų konvertavimas.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-196">Unit conversion works only for time.</span></span> <span data-ttu-id="a6bbd-197">Išlaidų atveju, jei sistemai nepavyksta rasti išlaidų kategorijos ir vieneto derinio kainos, pagal numatytuosius parametrus nustatoma 0,00 dydžio kaina.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-197">For expenses, if the system can't find a price for the combination of the expense category and unit, the price is set to 0.00 by default.</span></span>

### <a name="why-does-psa-convert-time-units"></a><span data-ttu-id="a6bbd-198">Kodėl PSA konvertuoja laiko vienetus?</span><span class="sxs-lookup"><span data-stu-id="a6bbd-198">Why does PSA convert time units?</span></span>
<span data-ttu-id="a6bbd-199">Kai kuriose šalyse arba regionuose įtaikomas teisinis reikalavimas sąskaitų tarifus nustatyti dienomis.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-199">In some countries or regions, there is a legal requirement that bill rates be set up in days.</span></span> <span data-ttu-id="a6bbd-200">Pasiūlymo ciklo metu derybos dėl kainų ir nuolaidų vyksta naudojant kiekvieno apmokėtino vaidmens dienos tarifus.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-200">Price negotiation and discounting during the quote cycle is done by using day rates for each billable role.</span></span> <span data-ttu-id="a6bbd-201">Grafikas įvertinamas ir laikas įvedamas valandomis.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-201">Schedule estimation and time entry are done in hours.</span></span> <span data-ttu-id="a6bbd-202">Siekiant palaikyti šį laiko vienetų skirtumą, PSA konvertuoja laiko vienetus.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-202">To support this difference in time units, PSA converts time units.</span></span>

### <a name="can-time-units-be-changed-on-project-estimates"></a><span data-ttu-id="a6bbd-203">Ar galima pakeisti laiko vienetus projektų įvertinimuose?</span><span class="sxs-lookup"><span data-stu-id="a6bbd-203">Can time units be changed on project estimates?</span></span>
<span data-ttu-id="a6bbd-204">Ne.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-204">No.</span></span> <span data-ttu-id="a6bbd-205">Grafiko įvertinimas šiuo metu apribotas naudoti tik valandas ir jo keisti negalima.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-205">Schedule estimation is currently restricted to hours and can’t be changed.</span></span>

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a><span data-ttu-id="a6bbd-206">Ar galima redaguoti, naikinti ir įtraukti vienetus bei vienetų grupes?</span><span class="sxs-lookup"><span data-stu-id="a6bbd-206">Can units and unit groups be edited, deleted, and added?</span></span>
<span data-ttu-id="a6bbd-207">Taip.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-207">Yes.</span></span> <span data-ttu-id="a6bbd-208">Išskyrus vienetų grupę **Laikas** ir vienetą **Valanda**, visus vienetus galima panaikinti arba redaguoti bei įtraukti naujų vienetų.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-208">With exception of the **Time** unit group and the **Hour** unit, all units can be deleted or edited, and new units can be added.</span></span> <span data-ttu-id="a6bbd-209">PSA negalima panaikinti vienetų grupės **Laikas** ir vieneto **Valanda**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-209">In PSA, the **Time** unit group and the **Hour** unit can't be deleted.</span></span> <span data-ttu-id="a6bbd-210">Tačiau juos galima atnaujinti įvedant vertimo tekstą lauke **Pavadinimas**.</span><span class="sxs-lookup"><span data-stu-id="a6bbd-210">However, they can be updated with a translated text for the **Name** field.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]