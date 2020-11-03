---
title: Koregavimo žurnalų kūrimas ir patvirtinimas
description: Šioje temoje pateikta informacija apie tai, kaip sukurti ir patvirtinti koregavimo žurnalą.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 855593df1ea14827f06961dda5b4becd2fa75c18
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080833"
---
# <a name="create-and-confirm-correction-journals"></a><span data-ttu-id="d4c0f-103">Koregavimo žurnalų kūrimas ir patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="d4c0f-103">Create and confirm Correction journals</span></span>

<span data-ttu-id="d4c0f-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="d4c0f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d4c0f-105">Kartais laiko arba išlaidų įrašas gali būti įvestas neteisingai.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-105">Occasionally a time or expense entry may be entered incorrectly.</span></span> <span data-ttu-id="d4c0f-106">Pavyzdžiui, konsultantas gali pasirinkti neteisingą laiko įrašo sukūrimo datą arba gali perkelti skaičius įvesdamas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-106">For example, a consultant might select the wrong date when creating a time entry or they might transpose the numbers when entering an expense.</span></span> <span data-ttu-id="d4c0f-107">Jei konsultantas negali atnaujinti pateiktų įrašų, administratorius gali tiesiogiai pataisyti projekto įrašą.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-107">If a consultant can’t make the updates to the submitted entries, an administrator can directly correct the entry for a project.</span></span>

<span data-ttu-id="d4c0f-108">Norėdami atlikti procedūras šioje temoje, turite turėti administratoriaus teises.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-108">To complete the procedures in this topic, you will need Administrator permissions.</span></span>

## <a name="correct-approved-time-entries"></a><span data-ttu-id="d4c0f-109">Teisingi patvirtinti laiko įrašai</span><span class="sxs-lookup"><span data-stu-id="d4c0f-109">Correct approved time entries</span></span>     

<span data-ttu-id="d4c0f-110">Atlikite toliau nurodytus veiksmus norėdami pataisyti vieną ar kelis projekto laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-110">Complete the following steps to correct single or multiple time entries for a project.</span></span>

1. <span data-ttu-id="d4c0f-111">Srityje **Pardavimas** pasirinkite **Operacijos** , tada pasirinkite **Patvirtintas laikas**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-111">In the **Sales** area, select **Transactions** , and then select **Approved Time**.</span></span> 

2. <span data-ttu-id="d4c0f-112">Sąraše **Patvirtintas laikas** raskite ir pasirinkite vieną ar kelis taisytinus patvirtintus laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-112">In the **Approved Time** list, locate and select one or more approved time entries to correct.</span></span> <span data-ttu-id="d4c0f-113">Galite naudoti filtrą susijusiems įrašams rasti.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-113">You can use the filter to locate related entries.</span></span> <span data-ttu-id="d4c0f-114">Pavyzdžiui, galite filtruoti pagal projekto ID ir pasirinkti visus patvirtintus laiko įrašus su tuo projekto ID.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-114">For example, you might filter on a Project ID, and select all approved time entries with that Project ID.</span></span>

3. <span data-ttu-id="d4c0f-115">Pasirinkite **Teisingi įrašai**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-115">Select **Correct entries**.</span></span> <span data-ttu-id="d4c0f-116">Automatiškai sukuriamas naujas pataisymų žurnalas su priskirtu tipu **Laiko koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-116">A new correction journal is automatically created, with the assigned type **Time correction**.</span></span> <span data-ttu-id="d4c0f-117">Į šį žurnalą įtraukiami jūsų pasirinkti įrašai.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-117">The entries you selected are added to the journal.</span></span> 

4. <span data-ttu-id="d4c0f-118">Puslapyje **Naujas žurnalas** įveskite pataisymų žurnalo **Aprašas** , tada pasirinkite skirtuką **Laiko koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-118">On the **New Journal** page, enter a **Description** for your correction journal, and then select the **Time Entry Corrections** tab.</span></span>  

5. <span data-ttu-id="d4c0f-119">Dalyje **Naujos laiko įrašų reikšmės** atnaujinkite laukus įvesdami teisingą informaciją, jei reikia.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-119">In the **New Values for Time Entries** section, update the fields with the correct information as necessary.</span></span> <span data-ttu-id="d4c0f-120">Pavyzdžiui, galite keisti priskirtą projektą arba rezervuotiną išteklių.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-120">For example, you can change the assigned project or the bookable resource.</span></span>

6. <span data-ttu-id="d4c0f-121">Pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-121">Select **Preview**.</span></span> <span data-ttu-id="d4c0f-122">Dialogo lange pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-122">In the dialog box, select **OK**.</span></span> <span data-ttu-id="d4c0f-123">Skirtuke **Žurnalo eilutės** galite peržiūrėti pirminių faktinių duomenų, kurie yra susieti su pasirinktais laiko įrašais, kurie buvo anuliuoti, ir pataisytomis eilutėmis, kurios buvo sukurtos, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-123">On the **Journal lines** tab, you can view a list of the original actuals that are related to the selected time entries that have been reversed and the corrected corresponding lines that have been created.</span></span> <span data-ttu-id="d4c0f-124">Jei reikia atlikti papildomų pataisymų, pakartokite 5 ir 6 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-124">If additional corrections need to be made, repeat steps 5 and 6.</span></span> 

> [!NOTE]
> <span data-ttu-id="d4c0f-125">Visos pataisytos faktinių duomenų reikšmės turės tas pačias reikšmes, kurias pasirinkote skyriuje **Laiko įrašų naujos reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-125">All the corrected actuals will have the same values that you selected in the **New values for Time Entries** section.</span></span>

7. <span data-ttu-id="d4c0f-126">Jei pataisymai rodomi taip, kaip tikėjotės, pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-126">If the corrections appear as expected, select **Confirm**.</span></span> <span data-ttu-id="d4c0f-127">Dialogo lange pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-127">In the dialog box, select **OK**.</span></span>

8. <span data-ttu-id="d4c0f-128">Grįžkite į sritį **Pardavimas** , pasirinkite **Projektai** , tada atidarykite projektą, kuriame ką tik atnaujinote laiko įrašus.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-128">Return to the **Sales** area, select **Projects** , and then open the project for which you just updated the time entries.</span></span> 

9. <span data-ttu-id="d4c0f-129">Puslapio **Projektai** skirtuke **Faktiniai duomenys** peržiūrėkite atliktus pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-129">On the **Projects** page, on the **Actuals** tab, view the changes that you made.</span></span> 

> [!NOTE]
> <span data-ttu-id="d4c0f-130">Jei skirtuko **Faktiniai duomenys** nesimato, pasirinkite **Susijęs** > **Faktiniai duomenys**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-130">If the **Actuals** tab is not visible, select **Related** > **Actuals**.</span></span>  

10. <span data-ttu-id="d4c0f-131">Sąraše **Faktinis susietasis rodinys** galite matyti, kad vis dar rodomi anuliuoti pradiniai laiko įrašai ir atitinkami pataisyti laiko įrašai.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-131">In the **Actual Associated View** list, you can see that the original time entries that have been reversed are still listed, as are the corresponding corrected time entries.</span></span> 

<span data-ttu-id="d4c0f-132">Pavyzdžiui, šiame grafiniame elemente yra du eilutės elementai, kurių kiekis yra 8,00 ir kurių debetai išvardinti stulpelyje „Suma“.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-132">For example, in the following graphic, there are two line items with a quantity of 8.00 that have debits listed in the Amount column.</span></span> <span data-ttu-id="d4c0f-133">Be to, yra du eilutės elementai, kurių kiekis yra -8,00 ir kurių kredito sumos rodomos stulpelyje „Suma“.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-133">Additionally, there are two line items with a quantity of -8.00 that show credited amounts in the Amount column.</span></span> <span data-ttu-id="d4c0f-134">Šie pataisymai suteikia kiekiui nulinę reikšmę.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-134">These corrections bring the quantity to zero.</span></span>

 
## <a name="correct-approved-expense-entries"></a><span data-ttu-id="d4c0f-135">Patvirtintų išlaidų įrašų taisymas</span><span class="sxs-lookup"><span data-stu-id="d4c0f-135">Correct approved expense entries</span></span>

<span data-ttu-id="d4c0f-136">Atlikite toliau nurodytus veiksmus norėdami pataisyti vieną ar daugiau išlaidų įrašų.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-136">Complete the following steps to correct one or more expense entries.</span></span> 

1. <span data-ttu-id="d4c0f-137">Srityje **Pardavimas** kairiojoje naršymo srityje pasirinkite **Operacijos** , tada pasirinkite **Patvirtintos išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-137">In the **Sales** area, in the left navigation pane, under **Transactions** , select **Approved Expenses**.</span></span>

2. <span data-ttu-id="d4c0f-138">Sąraše **Patvirtintos išlaidos** pasirinkite taisytiną projektą, tada pasirinkite **Teisingi įrašai**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-138">In the **Approved Expenses** list, select the project that you want to correct, and then select **Correct entries**.</span></span> <span data-ttu-id="d4c0f-139">Automatiškai bus sukurtas naujas pataisymų žurnalas su priskirtu tipu **Išlaidų koregavimas**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-139">A new correction journal will be created automatically with the assigned type of **Expense correction**.</span></span> 

3. <span data-ttu-id="d4c0f-140">Puslapyje **Naujas žurnalas** įveskite pataisymo **Aprašas** , o skirtuke **Išlaidų koregavimas** skyriuje **Naujos išlaidų reikšmės** pasirinkite duomenų lauką, kurį norite pataisyti pasirinktoms išlaidų eilutėms.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-140">On the **New Journal** page, enter a **Description** for the correction, and on the **Expense Correction** tab, in the **New Values for Expenses** section, select the data fields that you want to correct for the selected expense lines.</span></span> <span data-ttu-id="d4c0f-141">Pavyzdžiui, galite priskirti išlaidas kitam **Projektas** arba pataisyti **Išlaidų kategorija** , **Išlaidų data** arba **Rezervuotini ištekliai**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-141">For example, you can assign the expense to another **Project** , or correct the **Expense Category** , **Expense Date** , or **Bookable Resource**.</span></span>

4. <span data-ttu-id="d4c0f-142">Pasirinkite **Peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-142">Select **Preview**.</span></span> <span data-ttu-id="d4c0f-143">Dialogo lange pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-143">In the dialog box, select **OK**.</span></span> 

5. <span data-ttu-id="d4c0f-144">Skirtuke **Žurnalo eilutės** patvirtinkite pataisymus. Galite peržiūrėti pirminių faktinių duomenų, kurie yra susieti su pasirinktais išlaidų įrašais, kurie buvo anuliuoti, ir pataisytomis eilutėmis, kurios buvo sukurtos, sąrašą.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-144">Verify the corrections on the **Journal lines** tab. You can view a list of the original actuals that are related to the selected expense entries that have been reversed and the corrected corresponding lines that have been created.</span></span>

6. <span data-ttu-id="d4c0f-145">Jei pataisytos reikšmės rodomos taip, kaip tikėjotės, pasirinkite **Patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-145">If the corrected values are as expected, select **Confirm**.</span></span> <span data-ttu-id="d4c0f-146">Dialogo lange pasirinkite **Gerai.**</span><span class="sxs-lookup"><span data-stu-id="d4c0f-146">In the dialog box, select **OK.**</span></span> <span data-ttu-id="d4c0f-147">Jei rodomos ne tos reikšmės, kurių tikėjotės, pasirinkite **Atšaukti** , kas grįžtumėte į sąrašą **Patvirtintos išlaidos**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-147">If the values are not showing as expected, select **Cancel** to return to the **Approved Expenses** list.</span></span> <span data-ttu-id="d4c0f-148">Pakartokite 2–5 veiksmus.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-148">Repeat steps 2 through 5.</span></span> 

> [!NOTE]
> <span data-ttu-id="d4c0f-149">Pataisytos faktinių duomenų reikšmės turės tas pačias reikšmes, kurias pasirinkote skyriuje **Išlaidų įrašų naujos reikšmės**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-149">The corrected actuals will have the same values that you selected in the **New values for Expenses** section.</span></span>

7. <span data-ttu-id="d4c0f-150">Patvirtinę pataisymų žurnalą, grįžkite prie atnaujintų projekto arba projektų ir peržiūrėkite savo pakeitimus.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-150">After you confirm the correction journal, navigate back to the project or projects that you updated, to view your changes.</span></span>  

8. <span data-ttu-id="d4c0f-151">Projekto puslapyje skirtuke **Faktiniai duomenys** peržiūrėkite **Faktinis susietasis rodinys**.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-151">In the project page, on the **Actuals** tab, review the **Actual Associated View**.</span></span> <span data-ttu-id="d4c0f-152">Rodomi pradiniai įrašai ir pataisyti įrašai.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-152">The original entries and the corrected entries are listed.</span></span> <span data-ttu-id="d4c0f-153">Šiame grafike rodomos pradinės išlaidų įrašų sumos ir atitinkamos pataisytų išlaidų įrašų sumos.</span><span class="sxs-lookup"><span data-stu-id="d4c0f-153">The following graphic shows original expense entry amounts and the corresponding corrected expense entry amounts.</span></span> 


