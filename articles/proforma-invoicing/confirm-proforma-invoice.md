---
title: „Proforma“ sąskaitos faktūros patvirtinimas
description: Šioje temoje pateikta informacija, kaip patvirtinti „Proforma“ sąskaitą faktūrą.
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: fa1e6c17fbda76a283c2ec68760a00e846decf83
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4128113"
---
# <a name="confirm-a-proforma-invoice"></a><span data-ttu-id="b275c-103">„Proforma“ sąskaitos faktūros patvirtinimas</span><span class="sxs-lookup"><span data-stu-id="b275c-103">Confirm a proforma invoice</span></span>

<span data-ttu-id="b275c-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="b275c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b275c-105">Patvirtinus išankstinę sąskaitą faktūrą, projekto sąskaitos faktūros būsena atnaujinama į **Patvirtinta**.</span><span class="sxs-lookup"><span data-stu-id="b275c-105">After a proforma invoice is confirmed, the status of the project invoice updates to **Confirmed**.</span></span> <span data-ttu-id="b275c-106">Patvirtinus sąskaitą faktūrą, ji tampa tik skaitoma.</span><span class="sxs-lookup"><span data-stu-id="b275c-106">When an invoice is confirmed, it becomes read-only.</span></span> <span data-ttu-id="b275c-107">Ateityje sąskaitą faktūrą galima pataisyti tik tuo atveju, jei yra klientų inicijuotų pataisymų ar kreditų arba jei sąskaita faktūra pažymėta kaip apmokėta.</span><span class="sxs-lookup"><span data-stu-id="b275c-107">Going forward, the invoice can only be corrected if there are any customer-initiated corrections or credits, or when it's marked as paid.</span></span>

<span data-ttu-id="b275c-108">Šioje lentelėje išvardyti sistemos sukurtos faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="b275c-108">The following table lists the actuals created by the system.</span></span> <span data-ttu-id="b275c-109">Šie faktiniai duomenys kuriami tuo metu, kai prieš patvirtinant atliekamos tam tikros operacijos projekto sąskaitos faktūros juodraštyje.</span><span class="sxs-lookup"><span data-stu-id="b275c-109">These actuals are created when certain operations are performed on the draft project invoice before it is confirmed.</span></span>

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p><span data-ttu-id="b275c-110">
                    <strong>Scenarijus</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b275c-110">
                    <strong>Scenario</strong>
                </span></span></p>
            </td>
            <td width="608" valign="top">
                <p><span data-ttu-id="b275c-111">
                    <strong>Faktiniai duomenys, sukurti patvirtinant</strong>
                </span><span class="sxs-lookup"><span data-stu-id="b275c-111">
                    <strong>Actuals created on confirmation</strong>
                </span></span></p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b275c-112">Laiko operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="b275c-112">Invoicing a time transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-113">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="b275c-113">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-114">Apmokestintos faktinės pardavimo valandos ir suma pradiniame laiko patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="b275c-114">A billed sales actual for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b275c-115">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="b275c-115">Invoicing a time transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-116">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="b275c-116">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-117">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="b275c-117">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-118">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusias valandas bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="b275c-118">A new unbilled sales actual that is non-chargeable for the remaining hours and amount after deducting the corrected figures on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b275c-119">Sąskaitos faktūros išrašymas už laiko operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="b275c-119">Invoicing a time transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-120">Pradinio laiko patvirtinimo neapmokestinto pardavimo anuliavimo sąskaitos faktūros valandos ir suma.</span><span class="sxs-lookup"><span data-stu-id="b275c-120">An unbilled sales reversal for the hours and amount on the original time approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-121">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už valandas bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta.</span><span class="sxs-lookup"><span data-stu-id="b275c-121">A new unbilled sales actual that is chargeable for the hours and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b275c-122">Išlaidų operacijos sąskaitos faktūros išrašymas neredaguojant sąskaitos faktūros juodraščio.</span><span class="sxs-lookup"><span data-stu-id="b275c-122">Invoicing an expense transaction without any edits on the draft invoice.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-123">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="b275c-123">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-124">Apmokestinti faktiniai pardavimo kiekis ir suma pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="b275c-124">A billed sales actual for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
<span data-ttu-id="b275c-125">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint sumažinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="b275c-125">Invoicing an expense transaction that was edited to reduce the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-126">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="b275c-126">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-127">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="b275c-127">A new unbilled sales actual that is chargeable for the quantity and amount on the edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent billed sales actual.</span></span> 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-128">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri nėra mokama už likusį kiekį bei sumą, redaguotoje sąskaitos faktūros eilučių informacijoje atėmus pataisytas sumas, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="b275c-128">A new unbilled sales actual that is non-chargeable for the remaining quantity and amount after deducting the corrected figures on edited invoice line detail, a reversal of the unbilled sales actual, and an equivalent of the billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b275c-129">Sąskaitos faktūros išrašymas už išlaidų operaciją, redaguotą norint padidinti kiekį.</span><span class="sxs-lookup"><span data-stu-id="b275c-129">Invoicing an expense transaction that was edited to increase the quantity.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-130">Neapmokestinto pardavimo kiekio ir sumos anuliavimas pradiniame išlaidų patvirtinime.</span><span class="sxs-lookup"><span data-stu-id="b275c-130">An unbilled sales reversal for the quantity and amount on the original expense approval.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-131">Nauja faktinė pardavimo suma, už kurią sąskaita faktūra neišrašyta ir kuri yra mokama už kiekį bei sumą redaguotoje sąskaitos faktūros eilučių informacijoje, taip pat – neapmokestintos faktinės pardavimo sumos anuliavimas ir lygiavertė faktinė pardavimo suma, už kurią sąskaita faktūra išrašyta.</span><span class="sxs-lookup"><span data-stu-id="b275c-131">A new unbilled sales actual that is chargeable for quantity and amount on the edited invoice line detail, a reversal of the untilled sales actual, and an equivalent billed sales actual.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
<span data-ttu-id="b275c-132">Sąskaitos faktūros išrašymo už mokestį.</span><span class="sxs-lookup"><span data-stu-id="b275c-132">Invoicing a fee.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-133">Pradinės žurnalo eilutės neapmokestinto pardavimo anuliavimo sąskaitos faktūros mokesčio suma.</span><span class="sxs-lookup"><span data-stu-id="b275c-133">An unbilled sales reversal for the fee amount on the original journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-134">Apmokestinti faktiniai pardavimo kiekis ir suma pradinėje mokesčio žurnalo eilutėje.</span><span class="sxs-lookup"><span data-stu-id="b275c-134">A billed sales actual for the quantity and amount on the original fee journal line.</span></span>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
<span data-ttu-id="b275c-135">Etapo sąskaitų faktūrų išrašymas.</span><span class="sxs-lookup"><span data-stu-id="b275c-135">Invoicing a milestone.</span></span>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
<span data-ttu-id="b275c-136">Projekto sutarties eilutės pradinio etapo apmokestinta faktinė pardavimo suma.</span><span class="sxs-lookup"><span data-stu-id="b275c-136">A billed sales actual for the milestone amount on the original milestone on the project contract line.</span></span>
                </p>
            </td>
        </tr>
    </tbody>
</table>
