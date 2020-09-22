---
title: Anksčiau patvirtintų laiko ir išlaidų įrašų atšaukimas
description: Šioje temoje pateikta informacija apie tai, kaip atšaukti anksčiau patvirtintą projekto laiko ir išlaidų operaciją.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 2fc74aba2a837b7cdff55385ffa20d78c2678bb7
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753610"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a><span data-ttu-id="35acd-103">Anksčiau patvirtintų laiko ar išlaidų įrašų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="35acd-103">Cancel previously approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="35acd-104">Naudodami naujausią Dynamics 365 Project Service Automation versiją tvirtintojai gali atšaukti laiko arba išlaidų įrašus, kuriuos anksčiau patvirtino.</span><span class="sxs-lookup"><span data-stu-id="35acd-104">In the latest version of Dynamics 365 Project Service Automation, approvers can cancel time or expense entries that they previously approved.</span></span>

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a><span data-ttu-id="35acd-105">Anksčiau patvirtinto laiko ar išlaidų įrašų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="35acd-105">Cancel a previously approved time or expense entry</span></span>

<span data-ttu-id="35acd-106">Norėdami atšaukti laiko ar išlaidų įrašą, kurį anksčiau patvirtinote, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="35acd-106">Follow these steps to cancel a time or expense entry that you previously approved.</span></span>

1. <span data-ttu-id="35acd-107">Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="35acd-107">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="35acd-108">**Patvirtinimų** sąrašo puslapyje pakeiskite rodinį į **Mano ankstesni patvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="35acd-108">On the **Approvals** list page, change the view to **My past approvals**.</span></span> <span data-ttu-id="35acd-109">Rodomas jūsų anksčiau patvirtintų laiko ir išlaidų įrašų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="35acd-109">A list of the time and expense entries that you previously approved is shown.</span></span>
3. <span data-ttu-id="35acd-110">Pasirinkite vieną arba kelis įrašus, tada pasirinkite **Atšaukti patvirtinimą**.</span><span class="sxs-lookup"><span data-stu-id="35acd-110">Select one or more entries, and then select **Cancel approval**.</span></span> <span data-ttu-id="35acd-111">Bus pateiktas įspėjimo pranešimas.</span><span class="sxs-lookup"><span data-stu-id="35acd-111">You receive a warning message.</span></span>
4. <span data-ttu-id="35acd-112">Norėdami atšaukti patvirtinimą, pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="35acd-112">Select **OK** to cancel the approval.</span></span>

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a><span data-ttu-id="35acd-113">Poveikio atšaukus laiko arba išlaidų įrašo patvirtinimą išsiaiškinimas</span><span class="sxs-lookup"><span data-stu-id="35acd-113">Understand the impact of canceling a time or expense entry approval</span></span>

<span data-ttu-id="35acd-114">Atšaukus patvirtinimą, patiriamas veiklos ir finansinis poveikis.</span><span class="sxs-lookup"><span data-stu-id="35acd-114">When an approval is canceled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="35acd-115">Veiklos poveikis</span><span class="sxs-lookup"><span data-stu-id="35acd-115">Operational impact</span></span>

<span data-ttu-id="35acd-116">Kai patvirtinimas atšaukiamas, veiklos požiūriu įrašo būsena iš naujo nustatoma į **juodraštį**, o patvirtinimas neberodomas rodinyje **Mano ankstesni patvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="35acd-116">On the operations side, when an approval is canceled, the status of the record is reset to **Draft**, and the approval no longer appears in the **My past approvals** view.</span></span> <span data-ttu-id="35acd-117">Vietoj to, atšauktas patvirtinimas rodomas rodinyje **Laiko įrašai, skirti patvirtinti** arba rodinyje **Išlaidų įrašai, skirti patvirtinti**, priklausomai nuo to, ar įrašas buvo laiko, ar išlaidų įrašas.</span><span class="sxs-lookup"><span data-stu-id="35acd-117">Instead, the canceled approval appears in either the **Time entries for approval** view or the **Expense entries for approval** view, depending on whether it was a time entry or an expense entry.</span></span> <span data-ttu-id="35acd-118">Be to, susijusio laiko arba išlaidų įrašo būsena pakeičiama į **Pateikta**, kad susijęs įrašas atitiktų patvirtinimus, kurių būsena – **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="35acd-118">Additionally, the status of the related time or expense entry is changed to **Submitted**, so that the related entry is consistent with approvals that have a status of **Draft**.</span></span>

<span data-ttu-id="35acd-119">Būdami tvirtintoju galite redaguoti kai kuriuos patvirtinimo laukus, kurių būsena – **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="35acd-119">As an approver, you can edit some of the fields of an approval that has a status of **Draft**.</span></span> <span data-ttu-id="35acd-120">Šie laukai – tai **Atsiskaitymo tipas** ir **Apmokėtinos valandos pagal laiko įrašus**.</span><span class="sxs-lookup"><span data-stu-id="35acd-120">These fields include **Billing Type** and **Billable Hours for Time Entries**.</span></span> <span data-ttu-id="35acd-121">Atlikę keitimų galite patvirtinti įrašą dar kartą.</span><span class="sxs-lookup"><span data-stu-id="35acd-121">After you make changes, you can approve the record again.</span></span> <span data-ttu-id="35acd-122">Taip pat galite atmesti įrašą.</span><span class="sxs-lookup"><span data-stu-id="35acd-122">Alternatively, you can reject the entry.</span></span> <span data-ttu-id="35acd-123">Atmetus laiko įrašo patvirtinimą, įrašo būsena pakeičiama į **Grąžinta**.</span><span class="sxs-lookup"><span data-stu-id="35acd-123">If you reject the approval of a time entry, the status of the entry is changed to **Returned**.</span></span> <span data-ttu-id="35acd-124">Atmetus išlaidų įrašo patvirtinimą, būsena pakeičiama į **Atmesta**.</span><span class="sxs-lookup"><span data-stu-id="35acd-124">If you reject the approval of an expense entry, the status is changed to **Rejected**.</span></span> <span data-ttu-id="35acd-125">Funkciniu požiūriu grąžinti ir atmesti įrašai veikia taip pat kaip ir įrašas, kurio būsena – **Juodraštis**.</span><span class="sxs-lookup"><span data-stu-id="35acd-125">Functionally, both returned and rejected entries behave the same as an entry that has a status of **Draft**.</span></span> <span data-ttu-id="35acd-126">Projekto komandos narys gali atlikti reikiamus įrašo keitimus, tada iš naujo pateikti įrašą patvirtinti arba visiškai jį panaikinti.</span><span class="sxs-lookup"><span data-stu-id="35acd-126">A project team member can either make any required changes to the entry and then resubmit it for approval, or delete the entry entirely.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="35acd-127">Finansinis poveikis</span><span class="sxs-lookup"><span data-stu-id="35acd-127">Financial impact</span></span>

<span data-ttu-id="35acd-128">Atšaukus patvirtinimą, projektas taip pat paveikiamas finansiškai.</span><span class="sxs-lookup"><span data-stu-id="35acd-128">A project is also affected financially when an approval is canceled.</span></span> <span data-ttu-id="35acd-129">Pirmiausia, atitinkami savikainos ir pardavimo faktiniai duomenys atnaujinami taip, kaip nurodyta toliau.</span><span class="sxs-lookup"><span data-stu-id="35acd-129">First, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="35acd-130">Koregavimo būsena nustatoma į **Koreguota**.</span><span class="sxs-lookup"><span data-stu-id="35acd-130">The adjustment status is set to **Adjusted**.</span></span>
- <span data-ttu-id="35acd-131">Atsiskaitymo būsena nustatoma į **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="35acd-131">The billing status is set to **Canceled**.</span></span>

<span data-ttu-id="35acd-132">Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai.</span><span class="sxs-lookup"><span data-stu-id="35acd-132">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="35acd-133">Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes.</span><span class="sxs-lookup"><span data-stu-id="35acd-133">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="35acd-134">Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės.</span><span class="sxs-lookup"><span data-stu-id="35acd-134">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="35acd-135">Vietoj to, šios reikšmės yra atšaukiamos.</span><span class="sxs-lookup"><span data-stu-id="35acd-135">These values are reversed instead.</span></span> <span data-ttu-id="35acd-136">Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="35acd-136">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="35acd-137">Laukui **Koregavimo būsena**, esančiam atvirkštinių faktinių duomenų srityje, nustatoma būsena **Nekoreguojama**, o atsiskaitymo būsenai nustatoma būsena **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="35acd-137">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the billing status is set to **Canceled**.</span></span>

<span data-ttu-id="35acd-138">Atlikus šiuos pakeitimus, suma, kuri įrašoma kaip išleista vykdant projektą, ir nepanaudotos projekto pajamos nebelems sumų, kurias šie faktiniai duomenys iš tikrųjų reiškia.</span><span class="sxs-lookup"><span data-stu-id="35acd-138">After these changes are made, the amount that is recorded as spent on the project and the revenue backlog on the project will longer account for the amounts that these actuals represent.</span></span>
