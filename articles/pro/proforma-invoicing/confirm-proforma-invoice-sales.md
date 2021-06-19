---
title: Išankstinės projekto sąskaitos faktūros patvirtinimas
description: Šioje temoje pateikiama informacija apie išankstinių projektu pagrįstų sąskaitų faktūrų patvirtinimą „Project Operations“.
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0ab40e38f221e57368949b7491578caa8ba88c02
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004136"
---
# <a name="confirm-a-proforma-project-invoice"></a><span data-ttu-id="bdeef-103">Išankstinės projekto sąskaitos faktūros patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="bdeef-103">Confirm a proforma project invoice</span></span> 

<span data-ttu-id="bdeef-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="bdeef-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="bdeef-105">Patvirtinus išankstinę sąskaitą faktūrą, projekto sąskaitos faktūros būsena atnaujinama į **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="bdeef-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="bdeef-106">Patvirtinus sąskaitą faktūrą, ji tampa tik skaitoma.</span><span class="sxs-lookup"><span data-stu-id="bdeef-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="bdeef-107">Ateityje sąskaitą faktūrą bus galima pakoreguoti tik tada, jei bus kliento pradėtų taisymų arba kreditų.</span><span class="sxs-lookup"><span data-stu-id="bdeef-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits.</span></span>

<span data-ttu-id="bdeef-108">Šioje lentelėje išvardyti sistemos sukurtos faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="bdeef-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="bdeef-109">Šie faktiniai duomenys kuriami tuo metu, kai prieš patvirtinant atliekamos tam tikros operacijos projekto sąskaitos faktūros juodraštyje.</span><span class="sxs-lookup"><span data-stu-id="bdeef-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="bdeef-110">
                    <strong>Scenarijus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bdeef-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="bdeef-111">
                    <strong>Faktiniai duomenys, sukurti patvirtinant</strong>
                </span><span class="sxs-lookup"><span data-stu-id="bdeef-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-112">Avansinio arba išankstinio apmokėjimo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="bdeef-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-113">Tipo <strong>Išankstinis apmokėjimas</strong> faktinės pardavimo sumos, už kurias išrašyta sąskaita faktūra, sukuriamos kaip avansinio arba išankstinio apmokėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="bdeef-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-114">Neapmokestinamo faktinio pardavimo neigiama išankstinio arba avansinio apmokėjimo suma, kuri bus naudojama derinant.</span><span class="sxs-lookup"><span data-stu-id="bdeef-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-115">Visiškai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="bdeef-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-116">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="bdeef-117">Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-118">Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="bdeef-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bdeef-119">Dalinai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="bdeef-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-120">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="bdeef-121">Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-122">Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="bdeef-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-123">Neapmokestinta faktinė likusio išankstinio arba avansinio apmokėjimo pardavimo neigiama suma, kuri bus naudojama būsimose sąskaitose faktūrose.</span><span class="sxs-lookup"><span data-stu-id="bdeef-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-124">Laiko operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="bdeef-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-125">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="bdeef-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-126">Apmokestintos faktinės pardavimo valandos ir suma pradiniame laiko patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="bdeef-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bdeef-127">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="bdeef-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-128">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="bdeef-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-129">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-130">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusias valandas bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-131">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="bdeef-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-132">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="bdeef-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-133">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-134">Išlaidų operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="bdeef-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-135">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="bdeef-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-136">Apmokestina faktinis pardavimo kiekis ir suma pradiniame išlaidų patvirtinime</span><span class="sxs-lookup"><span data-stu-id="bdeef-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bdeef-137">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="bdeef-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-138">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="bdeef-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-139">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-140">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusį kiekį bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-141">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="bdeef-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-142">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="bdeef-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-143">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-144">Sąskaitų faktūrų už medžiagų operacijas išrašymas neredagavus juodraštinės sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="bdeef-144">Invoicing a material transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-145">Pardavimo, už kurį neišrašyta sąskaita, atšaukimas pagal pradiniame medžiagos naudojimo patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-145">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-146">Faktinis pardavimas, už kurį išrašyta sąskaita, pagal pradiniame medžiagos naudojimo patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-146">A billed sales actual for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="bdeef-147">Redaguotų siekiant sumažinti kiekį sąskaitų faktūrų už medžiagų operacijas išrašymas.</span><span class="sxs-lookup"><span data-stu-id="bdeef-147">Invoicing a material transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-148">Pardavimo, už kurį neišrašyta sąskaita, atšaukimas pagal pradiniame laiko patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-148">An unbilled sales reversal for the quantity and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-149">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-149">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-150">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusį kiekį bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-150">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-151">Redaguotų siekiant padidinti kiekį sąskaitų faktūrų už medžiagų operacijas išrašymas.</span><span class="sxs-lookup"><span data-stu-id="bdeef-151">Invoicing a material transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-152">Pardavimo, už kurį neišrašyta sąskaita, atšaukimas pagal pradiniame medžiagos naudojimo patvirtinime nurodytą kiekį ir sumą.</span><span class="sxs-lookup"><span data-stu-id="bdeef-152">An unbilled sales reversal for the quantity and amount on the original material usage approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-153">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="bdeef-153">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="bdeef-154">Sąskaitos faktūros išrašymo už mokestį.</span><span class="sxs-lookup"><span data-stu-id="bdeef-154">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-155">Pradinės žurnalo eilutės neapmokestinto pardavimo anuliavimo sąskaitos faktūros mokesčio suma.</span><span class="sxs-lookup"><span data-stu-id="bdeef-155">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-156">Apmokestinti faktiniai pardavimo kiekis ir suma pradinėje mokesčio žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="bdeef-156">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="bdeef-157">Etapo sąskaitų faktūrų išrašymas.</span><span class="sxs-lookup"><span data-stu-id="bdeef-157">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-158">Projekto sutarties eilutės pradinio etapo apmokestinta faktinė pardavimo suma.</span><span class="sxs-lookup"><span data-stu-id="bdeef-158">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="bdeef-159">Produktais pagrįstos sutarties eilutės sąskaitos faktūros išrašymas.</span><span class="sxs-lookup"><span data-stu-id="bdeef-159">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="bdeef-160">Produkto eilutės apmokestintas faktinis pardavimo kiekis ir suma, nuskaityti iš produktais pagrįstos sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="bdeef-160">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
