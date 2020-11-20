---
title: „Proforma“ sąskaitos faktūros patvirtinimas – „Lite“ versija
description: Šioje temoje pateikta informacija, kaip patvirtinti išankstines sąskaitas faktūras programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 02b671e4ad327b2448529d7119211613f3a9cb27
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176531"
---
# <a name="confirm-a-proforma-invoice---lite"></a><span data-ttu-id="945fd-103">„Proforma“ sąskaitos faktūros patvirtinimas – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="945fd-103">Confirm a proforma invoice - lite</span></span>

<span data-ttu-id="945fd-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="945fd-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="945fd-105">Patvirtinus išankstinę sąskaitą faktūrą, projekto sąskaitos faktūros būsena atnaujinama į **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="945fd-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="945fd-106">Patvirtinus sąskaitą faktūrą, ji tampa tik skaitoma.</span><span class="sxs-lookup"><span data-stu-id="945fd-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="945fd-107">Ateityje sąskaitą faktūrą galima pataisyti tik tuo atveju, jei yra klientų inicijuotų pataisymų ar kreditų arba jei sąskaita faktūra pažymėta kaip apmokėta.</span><span class="sxs-lookup"><span data-stu-id="945fd-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, of if the invoice is marked as paid.</span></span>

<span data-ttu-id="945fd-108">Šioje lentelėje išvardyti sistemos sukurtos faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="945fd-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="945fd-109">Šie faktiniai duomenys kuriami tuo metu, kai prieš patvirtinant atliekamos tam tikros operacijos projekto sąskaitos faktūros juodraštyje.</span><span class="sxs-lookup"><span data-stu-id="945fd-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p><span data-ttu-id="945fd-110">
                    <strong>Scenarijus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="945fd-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="808" valign="top">
                <p><span data-ttu-id="945fd-111">
                    <strong>Faktiniai duomenys, sukurti patvirtinant</strong>
                </span><span class="sxs-lookup"><span data-stu-id="945fd-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="945fd-112">Avansinio arba išankstinio apmokėjimo sąskaita faktūra</span><span class="sxs-lookup"><span data-stu-id="945fd-112">Invoicing an advance or retainer</span></span> </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-113">Tipo <strong>Išankstinis apmokėjimas</strong> faktinės pardavimo sumos, už kurias išrašyta sąskaita faktūra, sukuriamos kaip avansinio arba išankstinio apmokėjimo sumos.</span><span class="sxs-lookup"><span data-stu-id="945fd-113">A billed sales actual of type, <strong>Retainer</strong> is created for the amount on the advance or retainer.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-114">Neapmokestinamo faktinio pardavimo neigiama išankstinio arba avansinio apmokėjimo suma, kuri bus naudojama derinant.</span><span class="sxs-lookup"><span data-stu-id="945fd-114">An unbilled sales actual of a negative amount of the retainer or advance to be used for reconciliation.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="945fd-115">Visiškai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="945fd-115">After fully reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-116">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="945fd-116">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="945fd-117">Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.</span><span class="sxs-lookup"><span data-stu-id="945fd-117">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-118">Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="945fd-118">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="945fd-119">Dalinai suderinus išankstinį arba avansinį apmokėjimą sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="945fd-119">After partially reconciling a retainer or advance on an invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-120">Išankstinio arba avansinio apmokėjimo pardavimo sumos, už kurią sąskaita faktūra neišrašyta, anuliavimas, sukurtas atlikti derinimą.</span><span class="sxs-lookup"><span data-stu-id="945fd-120">An unbilled sales reversal of the retainer or advance that was created for reconciliation.</span></span> <span data-ttu-id="945fd-121">Ši suma yra teigiama, nes ji skirta padengti neigiamą sumą, kuri sukurta išrašius sąskaitą faktūrą už išankstinį apmokėjimą arba avansą.</span><span class="sxs-lookup"><span data-stu-id="945fd-121">This amount is positive as it's meant to cancel out the negative that was created when the retainer or advance was invoiced.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-122">Pardavimo faktinė suma, už kurią sąskaita faktūra išrašyta, šioje sąskaitoje faktūroje.</span><span class="sxs-lookup"><span data-stu-id="945fd-122">A billed sales actual for the amount on this invoice.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-123">Neapmokestinta faktinė likusio išankstinio arba avansinio apmokėjimo pardavimo neigiama suma, kuri bus naudojama būsimose sąskaitose faktūrose.</span><span class="sxs-lookup"><span data-stu-id="945fd-123">A negative unbilled sales actual of the remaining retainer or advance amount to be used for reconciliation on future invoices.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="945fd-124">Laiko operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="945fd-124">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-125">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="945fd-125">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-126">Apmokestintos faktinės pardavimo valandos ir suma pradiniame laiko patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="945fd-126">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="945fd-127">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="945fd-127">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-128">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="945fd-128">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-129">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="945fd-129">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-130">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusias valandas bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="945fd-130">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on edited invoice line detail, a reversal of the sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="945fd-131">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="945fd-131">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-132">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="945fd-132">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-133">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="945fd-133">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="945fd-134">Išlaidų operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="945fd-134">Invoicing an expense transaction without any edits on draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-135">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="945fd-135">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-136">Apmokestina faktinis pardavimo kiekis ir suma pradiniame išlaidų patvirtinime</span><span class="sxs-lookup"><span data-stu-id="945fd-136">A billed sales actual for the quantity and amount on the original expense approval</span></span> </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="945fd-137">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="945fd-137">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-138">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="945fd-138">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-139">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="945fd-139">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-140">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusį kiekį bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="945fd-140">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="945fd-141">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="945fd-141">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-142">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="945fd-142">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-143">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="945fd-143">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="945fd-144">Sąskaitos faktūros išrašymo už mokestį.</span><span class="sxs-lookup"><span data-stu-id="945fd-144">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-145">Pradinės žurnalo eilutės neapmokestinto pardavimo anuliavimo sąskaitos faktūros mokesčio suma.</span><span class="sxs-lookup"><span data-stu-id="945fd-145">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-146">Apmokestinti faktiniai pardavimo kiekis ir suma pradinėje mokesčio žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="945fd-146">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="945fd-147">Etapo sąskaitų faktūrų išrašymas.</span><span class="sxs-lookup"><span data-stu-id="945fd-147">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-148">Projekto sutarties eilutės pradinio etapo apmokestinta faktinė pardavimo suma.</span><span class="sxs-lookup"><span data-stu-id="945fd-148">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="945fd-149">Produktais pagrįstos sutarties eilutės sąskaitos faktūros išrašymas.</span><span class="sxs-lookup"><span data-stu-id="945fd-149">Invoicing a product-based contract line.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="945fd-150">Produkto eilutės apmokestintas faktinis pardavimo kiekis ir suma, nuskaityti iš produktais pagrįstos sutarties eilutės.</span><span class="sxs-lookup"><span data-stu-id="945fd-150">A billed sales actual for the product line with the quantity and amount coming from the product-based contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
