---
title: Koreguojamosios projektu pagrįstos sąskaitos faktūros
description: Šioje temoje pateikiama informacija apie tai, kaip sukurti ir patvirtinti koreguojamąsias projektu pagrįstas sąskaitas faktūras „Project Operations“.
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012281"
---
# <a name="corrective-project-based-invoices"></a><span data-ttu-id="10530-103">Koreguojamosios projektu pagrįstos sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="10530-103">Corrective project-based invoices</span></span>

<span data-ttu-id="10530-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="10530-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="10530-105">Patvirtintą projekto sąskaitą faktūrą galima pataisyti, kad būtų apdoroti pakeitimai arba kreditai, dėl kurių susitarta su klientu ir projekto vadovu.</span><span class="sxs-lookup"><span data-stu-id="10530-105">A confirmed project invoice can be corrected to process changes or credits as negotiated with the customer and project manager.</span></span>

<span data-ttu-id="10530-106">Norėdami redaguoti patvirtintą sąskaitą faktūrą, atidarykite patvirtintą sąskaitą faktūrą ir pasirinkite **Taisyti šią sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="10530-106">To make edits to a confirmed invoice, open the confirmed invoice and select **Correct this Invoice**.</span></span> 

> [!NOTE]
> <span data-ttu-id="10530-107">Šį pasirinkimą galima atlikti tik tada, jei projekto sąskaita faktūra yra patvirtinta arba projektu pagrįstoje sąskaitoje faktūroje yra nurodyti avansai arba išankstiniai apmokėjimai ar avansų arba išankstinių apmokėjimų suderinimai.</span><span class="sxs-lookup"><span data-stu-id="10530-107">This selection isn't available unless a project invoice is confirmed or the project-based invoice has advances or retainers or reconciliations of advances or retainers.</span></span>

<span data-ttu-id="10530-108">Iš patvirtintos sąskaitos faktūros sukuriama naujas sąskaitos faktūros juodraštis.</span><span class="sxs-lookup"><span data-stu-id="10530-108">A new draft invoice is created from the confirmed invoice.</span></span> <span data-ttu-id="10530-109">Visa sąskaitos faktūros eilučių informacija iš anksčiau patvirtintos sąskaitos faktūros kopijuojama į naują juodraštį.</span><span class="sxs-lookup"><span data-stu-id="10530-109">All invoice line details from the previously confirmed invoice are copied to the new draft.</span></span> <span data-ttu-id="10530-110">Toliau pateikiami keli svarbiausi dalykai, kuriuos reikia suprasti apie naujai pataisytos sąskaitos faktūros eilučių informaciją.</span><span class="sxs-lookup"><span data-stu-id="10530-110">The following are some of the key points to understand about the line details on the new corrected invoice:</span></span>

- <span data-ttu-id="10530-111">Visi kiekiai yra atnaujinti į nulį.</span><span class="sxs-lookup"><span data-stu-id="10530-111">All quantities are updated to zero.</span></span> <span data-ttu-id="10530-112">„Dynamics 365 Project Operations“ reiškia, kad bus sukurtos visos prekės, kurioms išrašyta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="10530-112">Dynamics 365 Project Operations assumes that all invoiced items are fully credited.</span></span> <span data-ttu-id="10530-113">Jei reikia, galite neautomatiškai atnaujinti šiuos kiekius, kad nurodytumėte kiekį, už kurį išrašyta sąskaita faktūra, įskaitomą kiekį.</span><span class="sxs-lookup"><span data-stu-id="10530-113">If needed, you can manually update these quantities to reflect the quantity that is being invoiced, and not the quantity that is being credited.</span></span> <span data-ttu-id="10530-114">Atsižvelgiant į įvestą kiekį, programa apskaičiuoja įskaitytą kiekį.</span><span class="sxs-lookup"><span data-stu-id="10530-114">Based on the quantity you enter, the application calculates the credited quantity.</span></span> <span data-ttu-id="10530-115">Šią sumą atspindi faktiniai duomenys, sukurti patvirtinus pataisytą sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="10530-115">This amount is reflected in the actuals that are created when the corrected invoice is confirmed.</span></span> <span data-ttu-id="10530-116">Jei norite pakeisti mokesčio sumą, turite įvesti teisingą mokesčio sumą, o ne mokesčio sumą, kuri yra įskaitoma.</span><span class="sxs-lookup"><span data-stu-id="10530-116">If you are making changes to the tax amount, you must enter the correct tax amount and not the tax amount that is being credited.</span></span>
- <span data-ttu-id="10530-117">Etapų pataisymai visada apdorojami kaip visapusiški įskaitymai.</span><span class="sxs-lookup"><span data-stu-id="10530-117">Milestone corrections are always processed as full credits.</span></span>


> [!IMPORTANT]
> <span data-ttu-id="10530-118">Kai sąskaitos faktūros eilutės išsami informacija apima kitų jau apmokėtų mokesčių korekcijas, laukas **Taisymas** nustatomas kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="10530-118">For invoice line details that are corrections to other already invoiced charges, the **Correction** field is set to **Yes**.</span></span> <span data-ttu-id="10530-119">Kai sąskaitose faktūrose pateikiama pakoreguota SF eilutės išsami informacija, laukas **Yra taisymų** nustatomas kaip **Taip**.</span><span class="sxs-lookup"><span data-stu-id="10530-119">For invoices that have corrected invoice line details, the **Has corrections** field is set to **Yes**.</span></span>

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a><span data-ttu-id="10530-120">Faktiniai duomenys, kai patvirtinta koreguojamoji sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="10530-120">Actuals created when a corrective invoice is confirmed</span></span>

<span data-ttu-id="10530-121">Toliau esančioje lentelėje pateikti faktiniai duomenys, sukuriami patvirtinus koreguojamąją sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="10530-121">The following table lists the actuals that are created when a corrective invoice is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="10530-122">
                    <strong>Scenarijus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10530-122">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="10530-123">
                    <strong>Faktiniai duomenys, sukurti patvirtinant</strong>
                </span><span class="sxs-lookup"><span data-stu-id="10530-123">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10530-124">Viso kredito sąskaitų faktūrų išrašymas už ankstesnes laiko operacijas, kurių sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-124">Invoicing the full credit of a previously invoiced time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-125">Pradinės laiko sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-125">A billed sales reversal for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-126">Pradinės laiko sąskaitos faktūros eilutės informacijos naujos faktinės pardavimo reikšmės, už kurią sąskaita faktūra neišrašyta, valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-126">A new unbilled sales actual for the hours and amount on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10530-127">Dalinio kredito už laiko operaciją išrašymas.</span><span class="sxs-lookup"><span data-stu-id="10530-127">Invoicing the partial credit on a time transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-128">Pradinės laiko sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros valandos ir suma, už kurias sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-128">A billed sales reversal for the hours and amount invoiced on the original invoice line detail for time.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-129">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-130">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra apmokestinama už likusias valandas ir sumą, atėmus pakoreguotus skaičius sąskaitos faktūros eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="10530-130">A new unbilled sales actual that is chargeable for the remaining hours and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10530-131">Viso kredito sąskaitų faktūrų išrašymas už ankstesnes išlaidų operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-131">Invoicing the full credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-132">Pradinės išlaidų sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-132">A billed sales reversal for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-133">Pradinės išlaidų sąskaitos faktūros eilutės informacijos faktinės pardavimo sumos, už kurią sąskaita faktūra neišrašyta, kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-133">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10530-134">Da;omop kredito sąskaitų faktūrų išrašymas už ankstesnes išlaidų operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-134">Invoicing the partial credit of a previously invoiced expense transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-135">Pradinės išlaidų sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma, už kuriuos sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-135">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for an expense.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-136">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą pataisytoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-136">A new unbilled sales actual that is chargeable for the quantity and amount on the corrected invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-137">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra apmokestinama už likusius kiekį ir sumą, atėmus pakoreguotus skaičius sąskaitos faktūros eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="10530-137">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
                <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10530-138">Sąskaitos faktūros išrašymas už visą anksčiau į sąskaitą faktūrą įtrauktos medžiagos operacijos kreditą.</span><span class="sxs-lookup"><span data-stu-id="10530-138">Invoicing the full credit of a previously invoiced material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-139">Pardavimo, už kurį išrašyta sąskaita, atšaukimas pagal pradinės sąskaitos faktūros medžiagos eilutės informacijos srityje nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="10530-139">A billed sales reversal for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-140">Naujas faktinis pardavimas, už kurį neišrašyta sąskaita, susijęs su pradinės sąskaitos faktūros medžiagos eilutės informacijos srityje nurodytu kiekiu ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-140">A new unbilled sales actual for the quantity and amount on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="10530-141">Sąskaitos faktūros išrašymas už dalinį medžiagos operacijos kreditą.</span><span class="sxs-lookup"><span data-stu-id="10530-141">Invoicing the partial credit on a material transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-142">Pardavimo, už kurį išrašyta sąskaita, atšaukimas pagal pradinės sąskaitos faktūros medžiagos eilutės informacijos srityje nurodytą kiekį ir sumą, už kurią išrašyta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="10530-142">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for material.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-143">Naujas faktinis pardavimas, už kurį neišrašyta sąskaita, apmokestinamas pagal kiekį ir sumą, nurodytą redaguotos sąskaitos faktūros eilutės išsamios informacijos srityje, jo atšaukimas ir atitinkamas faktinis pardavimas, už kurį išrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="10530-143">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-144">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra apmokestinama už likusius kiekį ir sumą, atėmus pakoreguotus skaičius sąskaitos faktūros eilutės informacijoje.</span><span class="sxs-lookup"><span data-stu-id="10530-144">A new unbilled sales actual that is chargeable for the remaining quantity and amount after deducting the corrected figures on the invoice line detail.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10530-145">Viso kredito sąskaitų faktūrų išrašymas už ankstesnes mokesčių operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-145">Invoicing the full credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-146">Pradinės mokesčio sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-146">A billed sales reversal for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-147">Pradinės mokesčio sąskaitos faktūros eilutės informacijos faktinės pardavimo sumos, už kurią sąskaita faktūra neišrašyta, kiekis ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-147">A new unbilled sales actual for the quantity and amount on the original invoice line detail for the fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="10530-148">Dalinio kredito sąskaitų faktūrų išrašymas už ankstesnes mokesčių operacijas, kurių sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-148">Invoicing the partial credit of a previously invoiced fee transaction.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-149">Pradinės mokesčio sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros kiekis ir suma, už kuriuos sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-149">A billed sales reversal for the quantity and amount invoiced on the original invoice line detail for fee.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-150">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą pataisytoje sąskaitos faktūros eilučių informacijoje, taip pat – šio proceso atšaukimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-150">A new unbilled sales actual that is chargeable for the quantity and amount on the edited corrective invoice line detail, a reversal of this, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="10530-151">Viso kredito sąskaitų faktūrų išrašymas už ankstesnį etapą, už kurį sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-151">Invoicing the full credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-152">Pradinės etapo sąskaitos faktūros eilutės informacijos pardavimo atšaukimo sąskaitos faktūros ir suma.</span><span class="sxs-lookup"><span data-stu-id="10530-152">A billed sales reversal for the amount on the original invoice line detail for the milestone.</span></span>
                </p>
                <p>
<span data-ttu-id="10530-153">Etapo sąskaitos faktūros būsena atnaujinta iš <b>Kliento sąskaita faktūra užregistruota</b> į <b>Parengta išrašyti sąskaitą faktūrą</b>.</span><span class="sxs-lookup"><span data-stu-id="10530-153">The invoice status of the milestone is updated from <b>Customer Invoice Posted</b> to <b>Ready to Invoice</b>.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="10530-154">Dalinio kredito sąskaitų faktūrų išrašymas už ankstesnį etapą, už kurį sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="10530-154">Invoicing the partial credit of a previously invoiced milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="10530-155">Šis scenarijus nepalaikomas.</span><span class="sxs-lookup"><span data-stu-id="10530-155">This scenario isn't supported.</span></span>
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
