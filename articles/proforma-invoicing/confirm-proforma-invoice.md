---
title: Išankstinės projektu pagrįstos sąskaitos faktūros patvirtinimas
description: Šioje temoje pateikiama informacija apie išankstinės projektu pagrįstos sąskaitos faktūros patvirtinimą.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1e4591d97e9d895dade42b2bcce57f22208cba96
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012146"
---
# <a name="confirm-a-proforma-project-based-invoice"></a><span data-ttu-id="82cb1-103">Išankstinės projektu pagrįstos sąskaitos faktūros patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="82cb1-103">Confirm a proforma project-based invoice</span></span>

<span data-ttu-id="82cb1-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="82cb1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="82cb1-105">Patvirtinus išankstinę sąskaitą faktūrą, projekto sąskaitos faktūros būsena atnaujinama į **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="82cb1-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="82cb1-106">Patvirtinus sąskaitą faktūrą, ji tampa tik skaitoma.</span><span class="sxs-lookup"><span data-stu-id="82cb1-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="82cb1-107">Ateityje sąskaitą faktūrą bus galima pakoreguoti tik tada, jei bus kliento pradėtų taisymų arba kreditų.</span><span class="sxs-lookup"><span data-stu-id="82cb1-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="82cb1-108">Šioje lentelėje išvardyti sistemos sukurtos faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="82cb1-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="82cb1-109">Šie faktiniai duomenys kuriami tuo metu, kai prieš patvirtinant atliekamos tam tikros operacijos projekto sąskaitos faktūros juodraštyje.</span><span class="sxs-lookup"><span data-stu-id="82cb1-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="82cb1-110">
                    <strong>Scenarijus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="82cb1-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="82cb1-111">
                    <strong>Faktiniai duomenys, sukurti patvirtinant</strong>
                </span><span class="sxs-lookup"><span data-stu-id="82cb1-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-112">Avansinio arba išankstinio apmokėjimo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="82cb1-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-113">Tipo <strong>Išankstinis apmokėjimas</strong> faktinės pardavimo sumos, už kurias išrašyta sąskaita faktūra, sukuriamos kaip avansinio arba išankstinio apmokėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="82cb1-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-114">Pardavimas, už kurį neišrašyta sąskaita, kai išankstinio apmokėjimo arba sandorio suma, kurią norima naudoti suderinimo tikslais, yra neigiama.</span><span class="sxs-lookup"><span data-stu-id="82cb1-114">An unbilled sales actual with a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-115">Visiškai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="82cb1-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-116">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="82cb1-117">Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-118">Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="82cb1-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="82cb1-119">Dalinai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="82cb1-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-120">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="82cb1-121">Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-122">Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="82cb1-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-123">Neapmokestinta faktinė likusio išankstinio arba avansinio apmokėjimo pardavimo neigiama suma, kuri bus naudojama būsimose sąskaitose faktūrose.</span><span class="sxs-lookup"><span data-stu-id="82cb1-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-124">Laiko operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="82cb1-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-125">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="82cb1-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-126">Apmokestintos faktinės pardavimo valandos ir suma pradiniame laiko patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="82cb1-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="82cb1-127">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="82cb1-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-128">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="82cb1-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-129">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-130">Naujas pardavimas, už kurį neišrašyta sąskaita, kuris nėra apmokestinamas pagal likusį valandų skaičių ir sumą išskaičiavus pataisytus redaguotos sąskaitos faktūros eilutės informacijos skaičius, atšauktą faktinį pardavimą ir atitinkamą faktinį pardavimą, už kurį išrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="82cb1-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-131">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="82cb1-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-132">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="82cb1-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-133">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-134">Išlaidų operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="82cb1-134">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-135">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="82cb1-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-136">Apmokestinti faktiniai pardavimo kiekis ir suma pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="82cb1-136">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="82cb1-137">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="82cb1-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-138">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="82cb1-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-139">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-140">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusį kiekį bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-141">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="82cb1-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-142">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="82cb1-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-143">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-144">Sąskaitų faktūrų už medžiagų operacijas išrašymas neredagavus juodraštinės sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="82cb1-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-145">Pardavimo, už kurį neišrašyta sąskaita, atšaukimas pagal pradiniame medžiagos naudojimo patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-146">Faktinis pardavimas, už kurį išrašyta sąskaita, pagal pradiniame medžiagos naudojimo patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="82cb1-147">Redaguotų siekiant sumažinti kiekį sąskaitų faktūrų už medžiagų operacijas išrašymas.</span><span class="sxs-lookup"><span data-stu-id="82cb1-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-148">Pardavimo, už kurį neišrašyta sąskaita, atšaukimas pagal pradiniame laiko patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-149">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-150">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusį kiekį bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-151">Redaguotų siekiant padidinti kiekį sąskaitų faktūrų už medžiagų operacijas išrašymas.</span><span class="sxs-lookup"><span data-stu-id="82cb1-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-152">Pardavimo, už kurį neišrašyta sąskaita, atšaukimas pagal pradiniame medžiagos naudojimo patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="82cb1-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-153">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="82cb1-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="82cb1-154">Sąskaitos faktūros išrašymo už mokestį.</span><span class="sxs-lookup"><span data-stu-id="82cb1-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-155">Pradinės žurnalo eilutės neapmokestinto pardavimo anuliavimo sąskaitos faktūros mokesčio suma.</span><span class="sxs-lookup"><span data-stu-id="82cb1-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-156">Apmokestinti faktiniai pardavimo kiekis ir suma pradinėje mokesčio žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="82cb1-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="82cb1-157">Etapo sąskaitų faktūrų išrašymas.</span><span class="sxs-lookup"><span data-stu-id="82cb1-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="82cb1-158">Projekto sutarties eilutės pradinio etapo apmokestinta faktinė pardavimo suma.</span><span class="sxs-lookup"><span data-stu-id="82cb1-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
       
    </tbody>
</table>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
