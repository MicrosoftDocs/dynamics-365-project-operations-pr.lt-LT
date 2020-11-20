---
title: Koreguotos sąskaitos faktūros – „Lite“ versija
description: Šioje temoje pateikta informacija apie pataisytas sąskaita faktūras programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 55bec8ad1d9c2b55cabb453321f13df8b7cd1614
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176441"
---
# <a name="corrected-invoices---lite"></a><span data-ttu-id="dd45e-103">Koreguotos sąskaitos faktūros – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="dd45e-103">Corrected invoices - lite</span></span>

<span data-ttu-id="dd45e-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="dd45e-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="dd45e-105">Patvirtintą projekto sąskaitą faktūrą galima pataisyti, kad būtų apdoroti pakeitimai arba kreditai, dėl kurių susitarta su klientu ir projekto vadovu.</span><span class="sxs-lookup"><span data-stu-id="dd45e-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="dd45e-106">Norėdami redaguoti patvirtintą sąskaitą faktūrą, atidarykite patvirtintą sąskaitą faktūrą ir pasirinkite **Taisyti šią sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="dd45e-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="dd45e-107">Šis pasirinkimas nepasiekiamas, jei projekto sąskaita faktūra nepatvirtinta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-107">This selection isn't available unless a project invoice is confirmed.</span></span>

<span data-ttu-id="dd45e-108">Iš patvirtintos sąskaitos faktūros sukuriama naujas sąskaitos faktūros juodraštis.</span><span class="sxs-lookup"><span data-stu-id="dd45e-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="dd45e-109">Visa sąskaitos faktūros eilučių informacija iš anksčiau patvirtintos sąskaitos faktūros kopijuojama į naują juodraštį.</span><span class="sxs-lookup"><span data-stu-id="dd45e-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="dd45e-110">Toliau pateikiami keli svarbiausi dalykai, kuriuos reikia suprasti apie naujai pataisytos sąskaitos faktūros eilučių informaciją.</span><span class="sxs-lookup"><span data-stu-id="dd45e-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="dd45e-111">Visi kiekiai yra atnaujinti į nulį.</span><span class="sxs-lookup"><span data-stu-id="dd45e-111">All quantities are updated to zero.</span></span> <span data-ttu-id="dd45e-112">Programoje daroma prielaida, kad visi elementai, už kuriuos išrašyta sąskaita faktūra, yra visiškai įskaityti.</span><span class="sxs-lookup"><span data-stu-id="dd45e-112">The application assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="dd45e-113">Jei reikia, galite neautomatiškai atnaujinti šiuos kiekius, kad nurodytumėte kiekį, už kurį išrašyta sąskaita faktūra, įskaitomą kiekį.</span><span class="sxs-lookup"><span data-stu-id="dd45e-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="dd45e-114">Atsižvelgiant į įvestą kiekį, programa apskaičiuoja įskaitytą kiekį.</span><span class="sxs-lookup"><span data-stu-id="dd45e-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="dd45e-115">Šią sumą atspindi faktiniai duomenys, sukurti patvirtinus pataisytą sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="dd45e-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="dd45e-116">Jei norite pakeisti mokesčio sumą, turite įvesti teisingą mokesčio sumą, o ne mokesčio sumą, kuri yra įskaitoma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="dd45e-117">Anksčiau patvirtintos produktais pagrįstos sutarties eilutės nėra kopijuojamos.</span><span class="sxs-lookup"><span data-stu-id="dd45e-117">Previously confirmed product-based contract lines are not copied over.</span></span> <span data-ttu-id="dd45e-118">Produktai pagrįstų projekto sąskaitos faktūros pataisymų apdorojimas nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="dd45e-118">Processing corrections on a product-based project invoice is not supported.</span></span>
- <span data-ttu-id="dd45e-119">Etapų pataisymai visada apdorojami kaip visapusiški įskaitymai.</span><span class="sxs-lookup"><span data-stu-id="dd45e-119">Milestone corrections are always processed as full credits.</span></span>
- <span data-ttu-id="dd45e-120">Išankstinio apmokėjimo arba avanso sumos gali būti pataisytos, jei klientui išrašyta sąskaita faktūra už klaidingą sumą.</span><span class="sxs-lookup"><span data-stu-id="dd45e-120">Retainer or advance amounts can be corrected if the customer was invoiced for an incorrect amount.</span></span>
- <span data-ttu-id="dd45e-121">Išankstinių apmokėjimų ir avansų derinimą galima pataisyti, jei klaidinga suma buvo naudojama derinant pagal anksčiau patvirtintos sąskaitos faktūros mokesčius.</span><span class="sxs-lookup"><span data-stu-id="dd45e-121">Reconciliations of retainers and advances can be corrected if an incorrect amount was used to reconcile against the charges on a previously confirmed invoice.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd45e-122">Sąskaitos faktūros eilučių informacija yra kitų išlaidų, už kurias sąskaita faktūra jau išrašyta, pataisymai ir jos laukas **Pataisymas** nustatytas į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="dd45e-122">Invoice line details that are corrections to other already invoiced charges have the field **Correction** set to **Yes**.</span></span> <span data-ttu-id="dd45e-123">Sąskaitos faktūros, kurių eilučių informacija pataisyta, turi lauką **Yra pataisymų**, kuris taip pat nustatytas į parinktį **Taip**.</span><span class="sxs-lookup"><span data-stu-id="dd45e-123">Invoices that have corrected invoice line details have a field called **Has corrections** that is also set to **Yes**.</span></span>

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a><span data-ttu-id="dd45e-124">Faktiniai duomenys sukuriami patvirtinus pataisytą sąskaitą faktūrą</span><span class="sxs-lookup"><span data-stu-id="dd45e-124">Actuals created on Confirmation of a corrective invoice:</span></span>

<span data-ttu-id="dd45e-125">Toliau pateikti faktiniai duomenys, kuriuos programa sukūrė patvirtinus pataisytą sąskaitą faktūrą, atsižvelgiant į operacijas, atliktas pataisytos sąskaitos faktūros juodraštyje prieš patvirtinant.</span><span class="sxs-lookup"><span data-stu-id="dd45e-125">Below are the actuals created by the application on confirmation of a corrective based on the operations performed on the draft corrective invoice before confirmation.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="dd45e-126">
                    <strong>Scenarijus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dd45e-126">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="dd45e-127">
                    <strong>Faktiniai duomenys, sukurti patvirtinant</strong>
                </span><span class="sxs-lookup"><span data-stu-id="dd45e-127">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="dd45e-128">Patvirtinkite avanso arba išankstinio apmokėjimo, už kurį išrašyta sąskaita faktūra, pataisymą.<strong></strong>
                </span><span class="sxs-lookup"><span data-stu-id="dd45e-128">Confirm the correction of an invoiced advance or retainer.<strong></strong>
                </span></span></p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-129">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="dd45e-129">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="dd45e-130">Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.</span><span class="sxs-lookup"><span data-stu-id="dd45e-130">This amount is positive because it is meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-131">Pardavimo atšaukimo sąskaitos faktūros faktiniai duomenys sukuriami už išankstinio apmokėjimo arba avanso sumą, kad būtų atšauktas pradinis pardavimas, už kurį išrašyta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="dd45e-131">A billed sales reversal actual is created for the amount on the retainer or advance to reverse the original billed sales.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-132">Sukuriami nauji pardavimo sąskaitos faktūros duomenys pagal išankstinio apmokėjimo arba avanso pagrindu pataisytą sąskaitos faktūros eilutę.</span><span class="sxs-lookup"><span data-stu-id="dd45e-132">A new billed sales actual is created for the corrected amount on the retainer or advance-based corrected invoice line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-133">Neapmokestinamo faktinio pardavimo neigiama išankstinio apmokėjimo arba avanso pagrindu pataisyta sąskaitos faktūros eilutė, kuri bus naudojama derinant.</span><span class="sxs-lookup"><span data-stu-id="dd45e-133">An unbilled sales actual of negative amount of the retainer or advance-based corrected invoice line, which will be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
<span data-ttu-id="dd45e-134">Patvirtinimas apie anksčiau suderinto išankstinio apmokėjimo arba avanso pataisymą.</span><span class="sxs-lookup"><span data-stu-id="dd45e-134">A confirmation of the correction of a previously reconciled retainer or advance.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-135">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="dd45e-135">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="dd45e-136">Ši suma yra teigiama ir ji skirta padengti neigiamą sumą, kuri sukurta įvykdžius ankstesnį derinimą</span><span class="sxs-lookup"><span data-stu-id="dd45e-136">This amount is positive and is meant to cancel out the negative that was created when the previous reconciliation occurred.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-137">Pardavimo atšaukimo sąskaitos faktūros faktiniai duomenys pagal ankstesnės sąskaitos faktūros sumą.</span><span class="sxs-lookup"><span data-stu-id="dd45e-137">A billed sales reversal actual for the amount on the previous invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-138">Nauji pardavimo sąskaitos faktūros duomenys pagal pataisytą išankstinio apmokėjimo sumą, taikomą pataisytai sąskaita faktūrai.</span><span class="sxs-lookup"><span data-stu-id="dd45e-138">A new billed sales actual for the corrected retainer amount that is applied on the corrected invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-139">Neapmokestinamo faktinio pardavimo neigiama iš pataisyto likučio išankstinio apmokėjimo arba avanso, kurį naudojant bus derinamos būsimos sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="dd45e-139">An unbilled sales actual with a negative amount from the corrected leftover retainer or advance, which will be used for reconciliation on later invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dd45e-140">Viso kredito sąskaitų faktūrų išrašymas už ankstesnes laiko operacijas, kurių sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-140">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-141">Pradinės laiko sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-141">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-142">Pradinės laiko sąskaitos faktūros eilutės informacijos naujos faktinės pardavimo reikšmės, už kurią sąskaita faktūra neišrašyta, valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-142">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="dd45e-143">Dalinio kredito už laiko operaciją išrašymas.</span><span class="sxs-lookup"><span data-stu-id="dd45e-143">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-144">Pradinės laiko sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros valandos ir suma, už kurias sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-144">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-145">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-145">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-146">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra apmokestinama už likusias valandas ir sumą, atėmus pakoreguotus skaičius sąskaitos faktūros eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="dd45e-146">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dd45e-147">Viso kredito sąskaitų faktūrų išrašymas už ankstesnes išlaidų operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-147">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-148">Pradinės išlaidų sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-148">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-149">Pradinės išlaidų sąskaitos faktūros eilutės informacijos faktinės pardavimo sumos, už kurią sąskaita faktūra neišrašyta, kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-149">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="dd45e-150">Da;omop kredito sąskaitų faktūrų išrašymas už ankstesnes išlaidų operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-150">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-151">Pradinės išlaidų sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma, už kuriuos sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-151">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-152">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą pataisytoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-152">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-153">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra apmokestinama už likusius kiekį ir sumą, atėmus pakoreguotus skaičius sąskaitos faktūros eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="dd45e-153">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dd45e-154">Viso kredito sąskaitų faktūrų išrašymas už ankstesnes mokesčių operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-154">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-155">Pradinės mokesčio sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-155">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-156">Pradinės mokesčio sąskaitos faktūros eilutės informacijos faktinės pardavimo sumos, už kurią sąskaita faktūra neišrašyta, kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-156">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="dd45e-157">Dalinio kredito sąskaitų faktūrų išrašymas už ankstesnes mokesčių operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-157">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-158">Pradinės mokesčio sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma, už kuriuos sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-158">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-159">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą pataisytoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-159">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="dd45e-160">Viso kredito sąskaitų faktūrų išrašymas už ankstesnį etapą, už kurį sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-160">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-161">Pradinės etapo sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros ir suma.</span><span class="sxs-lookup"><span data-stu-id="dd45e-161">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="dd45e-162">Etapo sąskaita faktūra arba atsiskaitymo būsena projekto sutarties eilutėje atnaujinama į parinktį **Parengta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="dd45e-162">The milestone invoice or billing status on the project contract line is updated to **Ready to Invoice**.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="dd45e-163">Dalinio kredito sąskaitų faktūrų išrašymas už ankstesnį etapą, už kurį sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="dd45e-163">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-164">Nepalaikoma</span><span class="sxs-lookup"><span data-stu-id="dd45e-164">Unsupported</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="dd45e-165">Produktais pagrįstos sutarties eilutės, už kurią sąskaita faktūra išrašyta anksčiau, kreditai ir pataisymai.</span><span class="sxs-lookup"><span data-stu-id="dd45e-165">Credits and corrections of a previously invoiced product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="dd45e-166">Nepalaikoma</span><span class="sxs-lookup"><span data-stu-id="dd45e-166">Unsupported</span></span> </p>
            </td>
        </tr>
    </tbody>
</table>
