---
title: Išlaidų valdymo konfigūravimas
description: Šiame straipsnyje aprašomos pastabos ir sprendimai, kuriuos turite padaryti planavimo proceso metu, prieš konfigūruodami išlaidų valdymą programoje „Microsoft Dynamics 365 Finance“.
author: KimANelson
manager: AnnBe
ms.date: 08/29/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: GlobalCategory, ProjCategory, TrvLocations, TrvParameters, TrvPaymethod, TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 23001
ms.assetid: aa3fd14d-7e94-4603-985f-ca26d6f860ea
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 74a8435464c8573ca831b7886f00c2695fd29827
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271363"
---
# <a name="configure-expense-management"></a><span data-ttu-id="afefa-103">Išlaidų valdymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="afefa-103">Configure expense management</span></span>

<span data-ttu-id="afefa-104">Šioje temoje aprašomos pastabos ir sprendimai, kuriuos turite padaryti planavimo proceso metu, prieš konfigūruodami išlaidų valdymą.</span><span class="sxs-lookup"><span data-stu-id="afefa-104">This topic describes the considerations and the decisions that you must make during the planning process before you configure Expense management.</span></span> <span data-ttu-id="afefa-105">Išlaidų valdyme galite saugoti informaciją apie mokėjimo būdus, kelionių paraiškas, išlaidų ataskaitas, strategijas ir kt.</span><span class="sxs-lookup"><span data-stu-id="afefa-105">In Expense management, you can store information about payment methods, travel requisitions, expense reports, policies, and so on.</span></span>

<span data-ttu-id="afefa-106">Kadangi daugelis sprendimų, kuriuos turite atlikti planuodami savo išlaidų valdymo konfigūraciją, priklauso nuo organizacijos hierarchijos ir finansinės struktūros, turite nurodyti šių sričių planavimo dokumentus.</span><span class="sxs-lookup"><span data-stu-id="afefa-106">Because many of the decisions that you make when you plan your configuration for Expense management are based on your organization’s hierarchy and financial structure, you must refer to the planning documents for those areas.</span></span>

## <a name="intercompany-expenses"></a><span data-ttu-id="afefa-107">Vidinės įmonės išlaidos</span><span class="sxs-lookup"><span data-stu-id="afefa-107">Intercompany expenses</span></span>

<span data-ttu-id="afefa-108">Kai įjungiate vidinės įmonės išlaidas, leidžiate juridiniams subjektams ir darbuotojams patirti išlaidų kito juridinio subjekto vardu ir rinkti mokėjimus iš jūsų organizacijos darbo juridinio subjekto.</span><span class="sxs-lookup"><span data-stu-id="afefa-108">When you enable intercompany expenses, you allow legal entities and employees to incur expenses on behalf of another legal entity, and collect payment from the legal entity of employment within your organization.</span></span> <span data-ttu-id="afefa-109">Pavyzdžiui, darbuotojas, esantis juridiniame subjekte A, baigia projektą, skirtą juridiniam subjektui B, o vykdant projektą patirta su kelionėmis susijusių išlaidų.</span><span class="sxs-lookup"><span data-stu-id="afefa-109">For example, an employee in legal entity A completes a project for legal entity B, and the project incurs travel related expenses.</span></span> <span data-ttu-id="afefa-110">Jei vidinės įmonės išlaidos įjungtos, darbuotojas gali pateikti išlaidų ataskaitą, kuria registruotos išlaidos bus priskirtos juridiniam subjektui B, o išlaidas apmokėti turės juridinis subjektas A. Jei jūsų organizacija neturi kelių juridinių subjektų, jums nereikia įjungti vidinės įmonės išlaidų.</span><span class="sxs-lookup"><span data-stu-id="afefa-110">If intercompany expenses are enabled, the employee can then file an expense report that will post the expense to legal entity B, and the expense must then be paid by legal entity A. If your organization doesn’t have multiple legal entities, you don’t have to enable intercompany expenses.</span></span>

<span data-ttu-id="afefa-111">**Sprendimas:** ar norite įjungti vidinės įmonės išlaidas?</span><span class="sxs-lookup"><span data-stu-id="afefa-111">**Decision:** Do you want to enable intercompany expenses?</span></span>

## <a name="financial-management"></a><span data-ttu-id="afefa-112">Finansų valdymas</span><span class="sxs-lookup"><span data-stu-id="afefa-112">Financial management</span></span>

<span data-ttu-id="afefa-113">Išlaidų valdymas glaudžiai integruotas su jūsų organizacijos finansų valdymu.</span><span class="sxs-lookup"><span data-stu-id="afefa-113">Expense management is tightly integrated with the financial management of your organization.</span></span> <span data-ttu-id="afefa-114">Daug jūsų išlaidų valdymo konfigūracijų priklausys nuo sprendimų, susijusių su jūsų organizacijos finansais.</span><span class="sxs-lookup"><span data-stu-id="afefa-114">Lots of your configuration for Expense management will be based on the decisions that you’ve made about your organization’s finances.</span></span> <span data-ttu-id="afefa-115">Tolesniuose skyriuose aprašomos įvairios sritys, kuriose reikia planuoti ir priimti sprendimus, atsižvelgiant į jūsų organizacijos finansinius sprendimus ir vadovų komandos rekomendacijas.</span><span class="sxs-lookup"><span data-stu-id="afefa-115">The following sections describe the various areas that require planning and decisions, based on your organization’s financial decisions and guidance from your leadership team.</span></span>

### <a name="per-diems"></a><span data-ttu-id="afefa-116">Dienpinigiai</span><span class="sxs-lookup"><span data-stu-id="afefa-116">Per diems</span></span>

<span data-ttu-id="afefa-117">Turite nustatyti darbuotojų dienpinigius, kuriuos teikia jūsų organizacija.</span><span class="sxs-lookup"><span data-stu-id="afefa-117">You must define the employee per diems that your organization provides.</span></span> <span data-ttu-id="afefa-118">Kadangi dienpinigiai paprastai skirti tokioms išlaidoms kaip maitinimo, apgyvendinimo ir kitos atsitiktinės išlaidos, galite sukurti jūsų organizacijos siūlomų dienpinigių taisykles.</span><span class="sxs-lookup"><span data-stu-id="afefa-118">Because per diems are typically used to cover expenses such as meals, lodging, and other incidental expenses, you can create rules for the per diem allowances that your organization offers.</span></span> <span data-ttu-id="afefa-119">Dienpinigiai gali būti pagrįsti metų laiku, kelionės vieta arba abiem.</span><span class="sxs-lookup"><span data-stu-id="afefa-119">per diem rates can be based on the time of year, the travel location, or both.</span></span> <span data-ttu-id="afefa-120">Kai sukuriate dienpinigius, galite nurodyti, kad už dienpinigius procentinė dalis bus išskaičiuota, jei darbuotojas gaus papildomą maitinimą ar aptarnavimą.</span><span class="sxs-lookup"><span data-stu-id="afefa-120">When you define a per diem rule, you can specify that a percentage of the per diem rate will be withheld if a worker receives complimentary meals or services.</span></span> <span data-ttu-id="afefa-121">Be to, galite apibrėžti dienpinigių normas ir nustatyti mažiausią bei didžiausią valandų skaičių, už kurias būtų skiriami dienpinigiai darbuotojui keliaujant.</span><span class="sxs-lookup"><span data-stu-id="afefa-121">You can also define per diem rate tiers to set the minimum and maximum number of hours that the per diem rate can be applied to a worker’s travel.</span></span>

<span data-ttu-id="afefa-122">**Sprendimai**</span><span class="sxs-lookup"><span data-stu-id="afefa-122">**Decisions:**</span></span>

- <span data-ttu-id="afefa-123">Pirmosios ir paskutinės dienų numatytosios dienpinigių taisyklės.</span><span class="sxs-lookup"><span data-stu-id="afefa-123">Default per diem rules for the first and last days:</span></span>

    - <span data-ttu-id="afefa-124">Koks minimalus skaičius valandų, už kurias per dieną darbuotojas gali prašyti ir gauti dienpinigių?</span><span class="sxs-lookup"><span data-stu-id="afefa-124">What is the minimum number of hours that an employee can claim for a day and still receive a per diem?</span></span>
    - <span data-ttu-id="afefa-125">Ar maisto išlaidoms padengti siūlomos sumos už pirmąją ir paskutinę dienas sumažintos?</span><span class="sxs-lookup"><span data-stu-id="afefa-125">Is there a reduction in the amount that is offered for meals for the first day and last day?</span></span> <span data-ttu-id="afefa-126">Jei sumažintos, kokiu procentu?</span><span class="sxs-lookup"><span data-stu-id="afefa-126">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="afefa-127">Ar apgyvendinimo išlaidoms padengti siūlomos sumos už pirmąją ir paskutinę dienas sumažintos?</span><span class="sxs-lookup"><span data-stu-id="afefa-127">Is there a reduction in the amount that is offered for a hotel for the first day and last day?</span></span> <span data-ttu-id="afefa-128">Jei sumažintos, kokiu procentu?</span><span class="sxs-lookup"><span data-stu-id="afefa-128">If there is a reduction, what is the percentage of the reduction?</span></span>
    - <span data-ttu-id="afefa-129">Ar kitoms išlaidoms padengti siūlomos sumos už pirmąją ir paskutinę dienas sumažintos?</span><span class="sxs-lookup"><span data-stu-id="afefa-129">Is there a reduction in the amount that is offered for other expenses that are incurred on the first day and last day?</span></span> <span data-ttu-id="afefa-130">Jei sumažintos, kokiu procentu?</span><span class="sxs-lookup"><span data-stu-id="afefa-130">If there is a reduction, what is the percentage of the reduction?</span></span>

- <span data-ttu-id="afefa-131">Numatytosios dienpinigių taisyklės.</span><span class="sxs-lookup"><span data-stu-id="afefa-131">Default per diem rules:</span></span>

    - <span data-ttu-id="afefa-132">Ar maisto išlaidoms skirta dienpinigių suma sumažinama, jei, pavyzdžiui, maistas yra nemokamas?</span><span class="sxs-lookup"><span data-stu-id="afefa-132">Is there a percentage reduction in the per diem allowance for each meal if, for example, the meal is complimentary?</span></span> <span data-ttu-id="afefa-133">Jei sumažinama, kokiu procentu sumažinama suma už kiekvieną patiekala?</span><span class="sxs-lookup"><span data-stu-id="afefa-133">If there is a reduction, what is the reduction percentage for each meal?</span></span>
    - <span data-ttu-id="afefa-134">Ar maistui skirtos sumos sumažinimas apskaičiuojamas pagal dieną, kelionę, ar pagal patiekalų skaičių per dieną?</span><span class="sxs-lookup"><span data-stu-id="afefa-134">Is the meal reduction calculated per day, per trip, or by the number of meals per day?</span></span>
    - <span data-ttu-id="afefa-135">Ar dienpinigių sumas reikia suapvalinti reguliariai, ar iki artimiausios didesnės apvalinimo sumos?</span><span class="sxs-lookup"><span data-stu-id="afefa-135">Should per diem amounts be rounded in the regular manner or rounded up?</span></span>
    - <span data-ttu-id="afefa-136">Ar dienpinigiai apskaičiuojami pagal 24 valandų laikotarpį, ar kalendorinę dieną?</span><span class="sxs-lookup"><span data-stu-id="afefa-136">Are per diems calculated on a 24-hour period or on a calendar day?</span></span>

- <span data-ttu-id="afefa-137">Dienpinigių taisyklės, pagrįstos vieta.</span><span class="sxs-lookup"><span data-stu-id="afefa-137">Per diem rules that are based on location:</span></span>

    - <span data-ttu-id="afefa-138">Ar dienpinigių suma priklauso nuo vietos?</span><span class="sxs-lookup"><span data-stu-id="afefa-138">Do per diem rates vary according to location?</span></span> <span data-ttu-id="afefa-139">Kokios vietos įtrauktos?</span><span class="sxs-lookup"><span data-stu-id="afefa-139">What locations are included?</span></span>
    - <span data-ttu-id="afefa-140">Jei dienpinigių suma priklauso nuo vietos, kokio dydžio procentinė suma skiriama kiekvienai vietai, atsižvelgiant į toliau nurodytus išlaidų tipus?</span><span class="sxs-lookup"><span data-stu-id="afefa-140">If per diem rates vary according to location, for each location, what percentage amount is provided for the following types of expenses:</span></span>

        - <span data-ttu-id="afefa-141">Maitinimas</span><span class="sxs-lookup"><span data-stu-id="afefa-141">Meals</span></span>
        - <span data-ttu-id="afefa-142">Viešbutis</span><span class="sxs-lookup"><span data-stu-id="afefa-142">Hotel</span></span>
        - <span data-ttu-id="afefa-143">Kitos išlaidos</span><span class="sxs-lookup"><span data-stu-id="afefa-143">Other expenses</span></span>

### <a name="expense-management-journals-and-accounts"></a><span data-ttu-id="afefa-144">Išlaidų valdymo žurnalai ir klientai</span><span class="sxs-lookup"><span data-stu-id="afefa-144">Expense management journals and accounts</span></span>

<span data-ttu-id="afefa-145">Vykdant išlaidų valdymą reikia naudoti kelis žurnalus ir klientus.</span><span class="sxs-lookup"><span data-stu-id="afefa-145">Expense management requires that you use multiple journals and accounts.</span></span> <span data-ttu-id="afefa-146">Pavyzdžiui, turite nuspręsti, ar tas pats klientas naudojamas tiek tvarkant avansinius mokėjimus, tiek sprendžiant kredito kortelių ginčus.</span><span class="sxs-lookup"><span data-stu-id="afefa-146">You must decide, for example, whether the same account is used for cash advances and credit card disputes.</span></span>

<span data-ttu-id="afefa-147">**Sprendimai**</span><span class="sxs-lookup"><span data-stu-id="afefa-147">**Decisions:**</span></span>

- <span data-ttu-id="afefa-148">Kuriame DK žurnalae registruojamos patvirtintos išlaidų ataskaitos?</span><span class="sxs-lookup"><span data-stu-id="afefa-148">Which ledger journal are approved expense reports posted to?</span></span>
- <span data-ttu-id="afefa-149">Kuris klientas naudojamas tvarkant avansinius mokėjimus?</span><span class="sxs-lookup"><span data-stu-id="afefa-149">Which account is used for cash advances?</span></span>
- <span data-ttu-id="afefa-150">Ar avansiniai mokėjimai turi būti registruojami nedelsiant?</span><span class="sxs-lookup"><span data-stu-id="afefa-150">Should cash advances be posted immediately?</span></span>

### <a name="payment-methods"></a><span data-ttu-id="afefa-151">Mokėjimo būdai</span><span class="sxs-lookup"><span data-stu-id="afefa-151">Payment methods</span></span>

<span data-ttu-id="afefa-152">Kai leidžiate darbuotojams registruoti išlaidas jūsų įmonės vardu, turite nustatyti mokėjimo būdus, kuriuos darbuotojai gali naudoti.</span><span class="sxs-lookup"><span data-stu-id="afefa-152">When you allow employees to incur expenses on behalf of your business, you must define the payment methods that employees are allowed to use.</span></span> <span data-ttu-id="afefa-153">Pavyzdžiui, galite leisti darbuotojams naudoti grynuosius pinigus arba įmonės kredito kortelę.</span><span class="sxs-lookup"><span data-stu-id="afefa-153">For example, you might allow employees to use cash or a corporate credit card.</span></span> <span data-ttu-id="afefa-154">Taip pat galite leisti darbuotojams naudoti asmenines kredito korteles, o tada grąžinti darbuotojams pinigus.</span><span class="sxs-lookup"><span data-stu-id="afefa-154">You might also allow employees to use personal credit cards, and then reimburse the employees.</span></span> <span data-ttu-id="afefa-155">Turite nustatyti šiuos sprendimus, skirtus kiekvienam leidžiam mokėjimo būdui.</span><span class="sxs-lookup"><span data-stu-id="afefa-155">You must make the following decisions for each payment method that you allow.</span></span>

<span data-ttu-id="afefa-156">**Sprendimai**</span><span class="sxs-lookup"><span data-stu-id="afefa-156">**Decisions:**</span></span>

- <span data-ttu-id="afefa-157">Kokie mokėjimo būdai leidžiami?</span><span class="sxs-lookup"><span data-stu-id="afefa-157">What payment methods are allowed?</span></span>
- <span data-ttu-id="afefa-158">Kam priklauso mokėjimo būdo išlaidos?</span><span class="sxs-lookup"><span data-stu-id="afefa-158">Who owns the payment method expenses?</span></span>
- <span data-ttu-id="afefa-159">Ar naudojama korespondentinio tipo sąskaita?</span><span class="sxs-lookup"><span data-stu-id="afefa-159">Is there an offset account type?</span></span> <span data-ttu-id="afefa-160">Jei korespondentinio tipo sąskaita naudojama, kokia ji?</span><span class="sxs-lookup"><span data-stu-id="afefa-160">If there is an offset account type, what is it?</span></span>
- <span data-ttu-id="afefa-161">Jei korespondentinio tipo sąskaita naudojama, kokia tai sąskaita?</span><span class="sxs-lookup"><span data-stu-id="afefa-161">If there is an offset account, what is the account?</span></span>
- <span data-ttu-id="afefa-162">Jei mokėjimo būdas yra kredito kortelė, ar mokėjimo būdą reikia naudoti tik apdorojant importuojamas operacijas?</span><span class="sxs-lookup"><span data-stu-id="afefa-162">If the payment method is a credit card, should the payment method be used only with imported transactions?</span></span>

### <a name="expense-categories-and-shared-categories"></a><span data-ttu-id="afefa-163">Išlaidų kategorijos ir bendrai naudojamos kategorijos</span><span class="sxs-lookup"><span data-stu-id="afefa-163">Expense categories and shared categories</span></span>

<span data-ttu-id="afefa-164">Kai darbuotojai kuria išlaidų ataskaitą, visos užregistruotos išlaidos turi būti susietos su išlaidų kategorija.</span><span class="sxs-lookup"><span data-stu-id="afefa-164">When employees create an expense report, each expense that they record must be associated with an expense category.</span></span> <span data-ttu-id="afefa-165">Išlaidų kategorijos gaunamos iš bendrai naudojamų kategorijų, kurias galima bendrai naudoti jūsų organizacijos juridiniuose subjektuose.</span><span class="sxs-lookup"><span data-stu-id="afefa-165">Expense categories are derived from shared categories that can be shared across the legal entities in your organization.</span></span> <span data-ttu-id="afefa-166">Šias kategorijas taip pat galima bendrai naudoti srityje Projektų valdymas ir apskaita, atsižvelgiant į jūsų organizacijos sąranką.</span><span class="sxs-lookup"><span data-stu-id="afefa-166">These categories can also be shared in Project management and accounting, depending on the way that your organization is defined.</span></span> <span data-ttu-id="afefa-167">Atsižvelgdami į savo organizacijos pobūdį ir diegimo komandos pateiktus nurodymus, nustatykite, ar kategorijos, naudojamos dalyje Išlaidų valdymas, bus naudojamos tik dalyje Išlaidų valdyma,s ar bus bendrai naudojamos srityse Projekto valdymas ir apskaita bei Išlaidų valdymas.</span><span class="sxs-lookup"><span data-stu-id="afefa-167">Based on the definition of your organization and guidance from the implementation team, determine whether the categories that are used in Expense management will be used only in Expense management, or whether they should be shared between Project management and accounting and Expense management.</span></span> <span data-ttu-id="afefa-168">Atminkite: šias kategorijas galima bendrai naudoti dalyse Projektas ir Apskaita arba Projektas ir Gamyba, bet ne Išlaidos ir Gamyba.</span><span class="sxs-lookup"><span data-stu-id="afefa-168">Note that these categories can be shared between Project and Expense or Project and Production, but not between Expense and Production.</span></span> <span data-ttu-id="afefa-169">Turite atlikti šiuos kiekvienos išlaidų kategorijos sprendimus.</span><span class="sxs-lookup"><span data-stu-id="afefa-169">You must make the following decisions for each expense category.</span></span>

<span data-ttu-id="afefa-170">**Sprendimai**</span><span class="sxs-lookup"><span data-stu-id="afefa-170">**Decisions:**</span></span>

- <span data-ttu-id="afefa-171">Kokia tai yra išlaidų kategorija?</span><span class="sxs-lookup"><span data-stu-id="afefa-171">What is the expense category?</span></span> <span data-ttu-id="afefa-172">Pavyzdžiui, skrydžių, viešbučių arba kilometražo kategorijos.</span><span class="sxs-lookup"><span data-stu-id="afefa-172">Examples include categories for flights, hotel, or mileage.</span></span>
- <span data-ttu-id="afefa-173">Ar išlaidų kategoriją taip pat galima naudoti dalyje Projektų valdymas ir apskaita?</span><span class="sxs-lookup"><span data-stu-id="afefa-173">Can the expense category also be used in Project management and accounting?</span></span>
- <span data-ttu-id="afefa-174">Koks tai yra išlaidų tipas?</span><span class="sxs-lookup"><span data-stu-id="afefa-174">What is the expense type?</span></span>
- <span data-ttu-id="afefa-175">Koks yra numatytasis išlaidų kategorijos mokėjimo būdas?</span><span class="sxs-lookup"><span data-stu-id="afefa-175">What is the default payment method for the expense category?</span></span>
- <span data-ttu-id="afefa-176">Ar išlaidų kategorijos išlaidos turi būti detaliai išvardytos?</span><span class="sxs-lookup"><span data-stu-id="afefa-176">Do expenses in the expense category have to be itemized?</span></span>
- <span data-ttu-id="afefa-177">Kokia yra pagrindinė numatytoji išlaidų kategorijos sąskaita?</span><span class="sxs-lookup"><span data-stu-id="afefa-177">What is the main default account for the expense category?</span></span>
- <span data-ttu-id="afefa-178">Kokia yra numatytoji išlaidų kategorijos prekės PVM grupė?</span><span class="sxs-lookup"><span data-stu-id="afefa-178">What is the default item sales tax group for the expense category?</span></span>
- <span data-ttu-id="afefa-179">Ar leidžiami papildomi išlaidų kategorijos mokėjimo būdai?</span><span class="sxs-lookup"><span data-stu-id="afefa-179">Are additional payment methods allowed for the expense category?</span></span> <span data-ttu-id="afefa-180">Jei leidžiama taikyti papildomus mokėjimo būdus, kokie jie yra?</span><span class="sxs-lookup"><span data-stu-id="afefa-180">If additional payment methods are allowed, what are they?</span></span>
- <span data-ttu-id="afefa-181">Ar šioje išlaidų kategorijoje yra subkategorijų?</span><span class="sxs-lookup"><span data-stu-id="afefa-181">Are there subcategories in this expense category?</span></span> <span data-ttu-id="afefa-182">Jei yra subkategorijų, taip pat reikia priimti toliau nurodytus sprendimus:</span><span class="sxs-lookup"><span data-stu-id="afefa-182">If there are subcategories, you must also make the following decisions:</span></span>

    - <span data-ttu-id="afefa-183">Ar kokioms nors subkategorijoms netaikomas mokesčių susigrąžinimas?</span><span class="sxs-lookup"><span data-stu-id="afefa-183">Are any of the subcategories excluded from tax recovery?</span></span>
    - <span data-ttu-id="afefa-184">Kokia yra subkategorijų prekės PVM grupė?</span><span class="sxs-lookup"><span data-stu-id="afefa-184">What is the item sales tax group of the subcategories?</span></span>

<span data-ttu-id="afefa-185">Jei išlaidų kategorija taip pat naudojama srityje Projektų valdymas ir apskaita, atsakykite į likusius klausimus.</span><span class="sxs-lookup"><span data-stu-id="afefa-185">If the expense category is also used in Project management and accounting, answer the remaining questions.</span></span> <span data-ttu-id="afefa-186">Kitu atveju pereikite prie kito skyriaus.</span><span class="sxs-lookup"><span data-stu-id="afefa-186">Otherwise, move on to the next section.</span></span>

- <span data-ttu-id="afefa-187">Kokios išlaidų sąskaitos bus naudojamos šioms išlaidoms?</span><span class="sxs-lookup"><span data-stu-id="afefa-187">Which cost accounts will be used for the following expenses?</span></span>

    - <span data-ttu-id="afefa-188">Savikaina</span><span class="sxs-lookup"><span data-stu-id="afefa-188">Cost</span></span>
    - <span data-ttu-id="afefa-189">Atlyginimo paskirstymas</span><span class="sxs-lookup"><span data-stu-id="afefa-189">Payroll allocation</span></span>
    - <span data-ttu-id="afefa-190">NG – Savikaina</span><span class="sxs-lookup"><span data-stu-id="afefa-190">WIP-cost value</span></span>
    - <span data-ttu-id="afefa-191">Išlaidos – Prekė</span><span class="sxs-lookup"><span data-stu-id="afefa-191">Cost-item</span></span>
    - <span data-ttu-id="afefa-192">NG – Išlaidų vertė – Prekė</span><span class="sxs-lookup"><span data-stu-id="afefa-192">WIP-cost value-item</span></span>
    - <span data-ttu-id="afefa-193">Sukauptas nuostolis</span><span class="sxs-lookup"><span data-stu-id="afefa-193">Accrued loss</span></span>
    - <span data-ttu-id="afefa-194">NG – sukauptas nuostolis</span><span class="sxs-lookup"><span data-stu-id="afefa-194">WIP-accrued loss</span></span>

- <span data-ttu-id="afefa-195">Kokios įplaukų sąskaitos bus naudojamos tolesniais atvejais?</span><span class="sxs-lookup"><span data-stu-id="afefa-195">Which revenue accounts will be used for the following?</span></span>

    - <span data-ttu-id="afefa-196">Įplaukos, kurioms išrašyta SF</span><span class="sxs-lookup"><span data-stu-id="afefa-196">Invoiced revenue</span></span>
    - <span data-ttu-id="afefa-197">Sukauptos įplaukos – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="afefa-197">Accrued revenue-sales value</span></span>
    - <span data-ttu-id="afefa-198">NG – Pardavimo vertė</span><span class="sxs-lookup"><span data-stu-id="afefa-198">WIP-sales value</span></span>
    - <span data-ttu-id="afefa-199">Sukauptos įplaukos – Gamyba</span><span class="sxs-lookup"><span data-stu-id="afefa-199">Accrued revenue-production</span></span>
    - <span data-ttu-id="afefa-200">NG – Gamyba</span><span class="sxs-lookup"><span data-stu-id="afefa-200">WIP-production</span></span>
    - <span data-ttu-id="afefa-201">Sukauptos įplaukos – Pelnas</span><span class="sxs-lookup"><span data-stu-id="afefa-201">Accrued revenue-profit</span></span>
    - <span data-ttu-id="afefa-202">NG – Pelnas</span><span class="sxs-lookup"><span data-stu-id="afefa-202">WIP-profit</span></span>
    - <span data-ttu-id="afefa-203">Sukauptos įplaukos – Abonementas</span><span class="sxs-lookup"><span data-stu-id="afefa-203">Accrued revenue-subscription</span></span>
    - <span data-ttu-id="afefa-204">NG – Abonementas</span><span class="sxs-lookup"><span data-stu-id="afefa-204">WIP-subscription</span></span>

### <a name="taxes"></a><span data-ttu-id="afefa-205">Mokesčiai</span><span class="sxs-lookup"><span data-stu-id="afefa-205">Taxes</span></span>

<span data-ttu-id="afefa-206">Su išlaidomis susiję mokesčiai: turite nustatyti, kas įtraukta arba įjungta išlaidų ataskaitose.</span><span class="sxs-lookup"><span data-stu-id="afefa-206">For expense-related taxes, you must determine what is included or enabled on expense reports.</span></span>

<span data-ttu-id="afefa-207">**Sprendimai**</span><span class="sxs-lookup"><span data-stu-id="afefa-207">**Decisions:**</span></span>

- <span data-ttu-id="afefa-208">Ar PVM įtrauktas į išlaidų sumas?</span><span class="sxs-lookup"><span data-stu-id="afefa-208">Is sales tax included in the expense amounts?</span></span>
- <span data-ttu-id="afefa-209">Ar reikia įjungti išlaidų mokesčių atkūrimą?</span><span class="sxs-lookup"><span data-stu-id="afefa-209">Should tax recovery be enabled on expenses?</span></span>

    > [!NOTE]
    > <span data-ttu-id="afefa-210">Jei planuojate didžiąją knygą ir nusprendžiate taikyti JAV PVM ir naudoti mokesčių taisykles, negalite įjungti išlaidų mokesčių susigrąžinimo.</span><span class="sxs-lookup"><span data-stu-id="afefa-210">When you were planning the general ledger, if you decided to apply U.S. sales tax and use tax rules, you can’t enable tax recovery on expenses.</span></span> <span data-ttu-id="afefa-211">(Norėdami taikyti JAV PVM ir naudoti mokesčių taisykles, nustatykite parinkties **Taikyti PVM mokesčių taisykles** parametrą **Taip**).</span><span class="sxs-lookup"><span data-stu-id="afefa-211">(To apply U.S. sales tax and use tax rules, set the **Apply sales tax taxations rules** option to **Yes**.)</span></span>

## <a name="policies"></a><span data-ttu-id="afefa-212">Strategijos</span><span class="sxs-lookup"><span data-stu-id="afefa-212">Policies</span></span>

<span data-ttu-id="afefa-213">Sukūrę išlaidų ataskaitų strategijas, galite padėti savo organizacijai sutaupyti laiko ir pinigų, kai darbuotojai registruoja išlaidas jos vardu.</span><span class="sxs-lookup"><span data-stu-id="afefa-213">By creating expense report policies, you can help your organization save time and money when employees incur expenses on its behalf.</span></span> <span data-ttu-id="afefa-214">Strategijos padeda užtikrinti, kad darbuotojai galėtų neviršyti biudžeto, pateiktų visą reikalingą informaciją ir leistų pinigus tik tada, kai tai būtina.</span><span class="sxs-lookup"><span data-stu-id="afefa-214">Policies help guarantee that employees stay in budget, provide all required information, and spend money only as they require it.</span></span> <span data-ttu-id="afefa-215">Turite priimti šiuos sprendimus dėl kiekvienos išlaidų ataskaitos strategijos ir kiekvienos jūsų sukurtos išlaidų ataskaitos patvirtinimo strategijos.</span><span class="sxs-lookup"><span data-stu-id="afefa-215">You must make the following decisions for each expense report policy and each expense report approval policy that you create.</span></span>

<span data-ttu-id="afefa-216">**Sprendimai**</span><span class="sxs-lookup"><span data-stu-id="afefa-216">**Decisions:**</span></span>

- <span data-ttu-id="afefa-217">Koks politikos pavadinimas?</span><span class="sxs-lookup"><span data-stu-id="afefa-217">What is the name of the policy?</span></span>
- <span data-ttu-id="afefa-218">Kam skirta išlaidų strategija?</span><span class="sxs-lookup"><span data-stu-id="afefa-218">What is the expense policy for?</span></span>
- <span data-ttu-id="afefa-219">Jei anksčiau nutarėte įjungti vidinės įmonės išlaidas, kurioms jūsų organizacijos įmonėms ši strategija taikoma?</span><span class="sxs-lookup"><span data-stu-id="afefa-219">If you previously decided to enable intercompany expenses, which companies in your organization will this policy apply to?</span></span>
- <span data-ttu-id="afefa-220">Kada strategija įsigalioja?</span><span class="sxs-lookup"><span data-stu-id="afefa-220">When does the policy become effective?</span></span>
- <span data-ttu-id="afefa-221">Kada strategijos galiojimas pasibaigia?</span><span class="sxs-lookup"><span data-stu-id="afefa-221">When does the policy expire?</span></span>
- <span data-ttu-id="afefa-222">Kas yra strategijos taisyklė?</span><span class="sxs-lookup"><span data-stu-id="afefa-222">What is the policy rule?</span></span>
- <span data-ttu-id="afefa-223">Koks politikos taisyklės rezultatas?</span><span class="sxs-lookup"><span data-stu-id="afefa-223">What is the outcome of the policy rule?</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]