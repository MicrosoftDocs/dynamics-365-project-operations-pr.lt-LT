---
title: Pakoreguotos sąskaitos faktūros
description: Šioje temoje pateikta informacija apie koreguotų sąskaitų faktūrų išrašymą.
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 734dc01e15339a31ac21f92bb3fb20d634a075ad
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287833"
---
# <a name="corrected-invoices"></a><span data-ttu-id="d67a0-103">Pakoreguotos sąskaitos faktūros</span><span class="sxs-lookup"><span data-stu-id="d67a0-103">Corrected invoices</span></span>

<span data-ttu-id="d67a0-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="d67a0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="d67a0-105">Patvirtintas sąskaitas faktūras galima redaguoti.</span><span class="sxs-lookup"><span data-stu-id="d67a0-105">Confirmed invoices can be edited.</span></span> <span data-ttu-id="d67a0-106">Pataisius patvirtintą sąskaitą faktūrą, sukuriama juodraštinė pakoreguota sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="d67a0-106">When you edit a confirmed invoice, a draft of the corrected invoice is created.</span></span> <span data-ttu-id="d67a0-107">Kadangi daroma prielaida, kad norite atšaukti visas operacijas ir kiekius iš pradinės sąskaitos faktūros, į šią koreguotą sąskaitą faktūrą įeina visos operacijos iš pradinės sąskaitos faktūros, o visi joje esantys kiekiai yra nulis (0).</span><span class="sxs-lookup"><span data-stu-id="d67a0-107">Because the assumption is that you want to reverse all the transactions and quantities from the original invoice, the corrected invoice includes all the transactions from the original invoice, and all the quantities on it are zero (0).</span></span>

<span data-ttu-id="d67a0-108">Kai operacijų taisyti nereikia, galite jas pašalinti iš juodraštinės koreguojamosios sąskaitos faktūros.</span><span class="sxs-lookup"><span data-stu-id="d67a0-108">When transactions don't require correction, you can remove them from the draft corrective invoice.</span></span> <span data-ttu-id="d67a0-109">Jei norite atšaukti arba grąžinti tik dalinį kiekį, galite redaguoti eilutės informacijos lauką „Kiekis“.</span><span class="sxs-lookup"><span data-stu-id="d67a0-109">To reverse or return only a partial quantity, you can edit the Quantity field on the line detail.</span></span> <span data-ttu-id="d67a0-110">Jei atidarote sąskaitos faktūros eilutės išsamią informaciją, galite peržiūrėti pradines sąskaitos faktūros kiekį.</span><span class="sxs-lookup"><span data-stu-id="d67a0-110">If you open the invoice line detail, you can see the original invoice quantity.</span></span> <span data-ttu-id="d67a0-111">Tada galite redaguoti dabartinės sąskaitos faktūros kiekį, kad jis būtų mažesnis arba didesnis nei pradinės sąskaitos faktūros kiekis.</span><span class="sxs-lookup"><span data-stu-id="d67a0-111">You can then edit the current invoice quantity so that it's less than or more than the original invoice quantity.</span></span>

<span data-ttu-id="d67a0-112">Patvirtinus koreguojamąją sąskaitą faktūrą, pradinis faktinis pardavimas, už kurį išrašyta sąskaita, yra atšaukiamas ir sukuriamas naujas faktinis pardavimas, už kurį išrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d67a0-112">When you confirm a corrective invoice, the original billed sales actual is reversed, and a new billed sales actual is created.</span></span> <span data-ttu-id="d67a0-113">Jei kiekis sumažintas, dėl skirtumo taip pat bus sukuriamas naujas faktinis pardavimas, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d67a0-113">If the quantity was reduced, the difference will cause a new unbilled sales actual to be created too.</span></span> <span data-ttu-id="d67a0-114">Pavyzdžiui, jei pradinio pardavimo, už kurį išrašyta sąskaita, kiekis yra aštuonios valandos, o koreguotos sąskaitos faktūros eilutės išsamioje informacijoje nurodomas sumažintas šešių valandų kiekis, pradinio pardavimo, už kurį išrašyta sąskaita faktūra, eilutė atšaukiama ir sukuriami du nauji faktiniai duomenys:</span><span class="sxs-lookup"><span data-stu-id="d67a0-114">For example, if the original billed sale was for eight hours, and the corrected invoice line detail has a reduced quantity of six hours, the original billed sales line is revered and two new actuals are created:</span></span>

- <span data-ttu-id="d67a0-115">Šešių valandų faktinis pardavimas, už kurį išrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d67a0-115">A billed sales actual for six hours.</span></span>
- <span data-ttu-id="d67a0-116">Likusių dviejų valandų faktinis pardavimas, už kurį neišrašyta sąskaita.</span><span class="sxs-lookup"><span data-stu-id="d67a0-116">An unbilled sales actual for the remaining two hours.</span></span> <span data-ttu-id="d67a0-117">Šiai operacijai vėliau galima išrašyti sąskaitą arba pažymėti ją kaip neapmokestinamąją, atsižvelgiant į derybas su klientu.</span><span class="sxs-lookup"><span data-stu-id="d67a0-117">This transaction can either be billed later or marked as non-chargeable, depending on the negotiations with the customer.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]