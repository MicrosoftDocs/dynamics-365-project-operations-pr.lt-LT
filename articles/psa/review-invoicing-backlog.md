---
title: Sąskaitų faktūrų įsiskolinimų peržiūra projektuose ir projektų sutartyse
description: Šioje temoje pateikiama informacija apie tai, kaip peržiūrėti laiko, savikainos ir produktų įsiskolinimus ir kaip juos pažymėti kaip paruoštus išrašyti sąskaitą faktūrą.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: ''
ms.author: rumant
ms.date: 03/11/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: eb6d942d61bf8b5d20afb75c88716132a596bcbd
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081045"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="a16a0-103">Sąskaitų faktūrų įsiskolinimų peržiūra projektuose ir projektų sutartyse</span><span class="sxs-lookup"><span data-stu-id="a16a0-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="a16a0-104">Kai operacijai galima išrašyti sukurtą ir apdorotą sąskaitą faktūrą, operaciją reikia pažymėti kaip **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="a16a0-105">Šioje temoje aprašyti operacijų tipai, kuriuos galima sukurti.</span><span class="sxs-lookup"><span data-stu-id="a16a0-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="a16a0-106">Laiko ir medžiagų atsiskaitymo įsiskolinimų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a16a0-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="a16a0-107">Kai laiko arba savikainos įrašas yra pateikiamas ir patvirtinamas projektui, PSA sukuria faktinį projektą.</span><span class="sxs-lookup"><span data-stu-id="a16a0-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="a16a0-108">Jei projekto ir operacijos klasė yra susiejama su laiko ir medžiagų projekto sutarties eilute, sukuriami du faktiniai elementai, kai įrašas patvirtinamas:</span><span class="sxs-lookup"><span data-stu-id="a16a0-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="a16a0-109">Faktinė savikaina</span><span class="sxs-lookup"><span data-stu-id="a16a0-109">Cost actual</span></span> 
- <span data-ttu-id="a16a0-110">Pardavimas, už kurį neišrašyta sąskaita</span><span class="sxs-lookup"><span data-stu-id="a16a0-110">Unbilled sales actual</span></span>

<span data-ttu-id="a16a0-111">Pardavimo, už kurį neišrašyta sąskaita, faktiniai elementai nurodo atsiskaitymo įsiskolinimą, ir jų atsiskaitymo būsena turi būti nustatyta į **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="a16a0-112">Sukūrus projekto sąskaitą faktūrą, pardavimo, už kurį neapmokėta, faktiniai elementai, pažymėti kaip **Paruošta išrašyti sąskaitą faktūrą** , nukopijuojami kaip sąskaitos faktūros eilutės informacija.</span><span class="sxs-lookup"><span data-stu-id="a16a0-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="a16a0-113">Jei norite peržiūrėti laiko ir medžiagos sąskaitų siuntimo nežurnalą, pereikite į **Pardavimai** \> **Sąskaitos** \> **Laiko ir medžiagų atsiskaitymo peržiūra**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="a16a0-114">Pažymėkite visus pardavimo, už kurį neišrašyta sąskaita, faktinius elementus, kurie paruošti sąskaitos faktūros išrašymui, tada pažymėkite **Paruošta išrašyti sąskaitą faktūra**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="a16a0-115">Šių faktinių elementų atsiskaitymo būsena pakeičiama į **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![Laiko ir medžiagų atsiskaitymo įsiskolinimas](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="a16a0-117">Produktų atsiskaitymo įsiskolinimų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a16a0-117">Review the product billing backlog</span></span>

<span data-ttu-id="a16a0-118">PSA, kai projekto sutartyje yra produktu pagrįstų sutarties eilučių, šios eilutės laikomos paruoštos sąskaitos faktūros išrašymui, kai tik projekto sutarčiai sukuriama sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="a16a0-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="a16a0-119">Visi projektai, kurie turi sutarties eilučių, kurios pažymėtos kaip **Paruošta išrašyti sąskaitą faktūrą** , yra nukopijuojami į projekto sąskaitą faktūrą kaip projekto sąskaitos faktūros eilutės.</span><span class="sxs-lookup"><span data-stu-id="a16a0-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="a16a0-120">Norėdami peržiūrėti produktų sąskaitų siuntimo žurnalą **Pardavimai** \> **Sąskaitų išrašymas** \> **Produktų sąskaitų faktūrų išrašymas**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="a16a0-121">Pažymėkite visas produktu pagrįstas sutarties eilutes, kurios paruoštos sąskaitos faktūros išrašymui, tada pažymėkite **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="a16a0-122">Šių eilučių atsiskaitymo būsena pakeičiama į **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![Produktų atsiskaitymo įsiskolinimas](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="a16a0-124">Fiksuotos kainos sutarčių atsiskaitymo etapų peržiūra</span><span class="sxs-lookup"><span data-stu-id="a16a0-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="a16a0-125">Kiekvienoje projekto sutarties eilutėje, kuriai taikomas fiksuotos kainos atsiskaitymo metodas, turi būti apibrėžti sutarties etapai.</span><span class="sxs-lookup"><span data-stu-id="a16a0-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="a16a0-126">Šiems sutarties etapams sąskaitą faktūrą galima išrašyti, tik jei jie pažymėti kaip **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="a16a0-127">Norėdami peržiūrėti atsiskaitymo etapus, į **Pardavimai** \> **Sąskaitos** \> **Fiksuotas kainų gairės.**</span><span class="sxs-lookup"><span data-stu-id="a16a0-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="a16a0-128">Pažymėkite visus etapus, kurie paruošti sąskaitos faktūros išrašymui, tada pažymėkite **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="a16a0-129">Šių etapų atsiskaitymo būsena pakeičiama į **Paruošta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="a16a0-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![Fiksuotos kainos etapai](media/FPBacklog.png)
