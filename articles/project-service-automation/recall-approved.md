---
title: Patvirtintas laiko arba išlaidų įrašų atšaukimas
description: Šioje temoje pateikta informacija apie tai, kaip atšaukti anksčiau patvirtintą laiko arba išlaidų operaciją.
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/08/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 74df6e196c9f060f957d79aebc9640a162fb2913
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753778"
---
# <a name="recall-approved-time-or-expense-entries"></a><span data-ttu-id="dcbcf-103">Patvirtintas laiko arba išlaidų įrašų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="dcbcf-103">Recall approved time or expense entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="dcbcf-104">Projekto komandos narys arba kitas asmuo, kuris pateikia laiko arba išlaidų įrašą, gali atšaukti tą laiko arba išlaidų įrašą, kai jis buvo patvirtintas.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-104">A project team member or an other person who submits a time or expense entry can recall that time or expense entry after it has been approved.</span></span> <span data-ttu-id="dcbcf-105">Patvirtinto laiko arba išlaidų įrašo atšaukimo procesą sudaro du veiksmai:</span><span class="sxs-lookup"><span data-stu-id="dcbcf-105">The process for recalling an approved time or expense entry has two steps:</span></span>

1. <span data-ttu-id="dcbcf-106">Pateikėjas prašo atšaukti.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-106">A submitter requests a recall.</span></span>
2. <span data-ttu-id="dcbcf-107">Tvirtintojas patvirtina atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-107">An approver approves the recall.</span></span>

## <a name="request-a-recall"></a><span data-ttu-id="dcbcf-108">Prašymas atšaukti</span><span class="sxs-lookup"><span data-stu-id="dcbcf-108">Request a recall</span></span>

<span data-ttu-id="dcbcf-109">Norėdami prašyti atšaukti patvirtintą laiko arba išlaidų įrašą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-109">Follow these steps to request a recall of an approved time or expense entry.</span></span>

1. <span data-ttu-id="dcbcf-110">Norėdami gauti laiko įrašus, pereikite į **Projektai** \> **Mano projektai** \> **Laiko įrašas**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-110">For time entries, go to **Projects** \> **My Work** \> **Time Entry**.</span></span>

    <span data-ttu-id="dcbcf-111">-arba-</span><span class="sxs-lookup"><span data-stu-id="dcbcf-111">–or–</span></span>

    <span data-ttu-id="dcbcf-112">Norėdami gauti išlaidų įrašus, pereikite į **Projektai** \> **Mano projektai** \> **Išlaidų įrašai**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-112">For expense entries, go to **Projects** \> **My Work** \> **Expenses**.</span></span>

2. <span data-ttu-id="dcbcf-113">Jei naudojate laiko įrašus, pažymėkite visus laiko įrašus, skirtus konkrečiam projekto ir užduoties deriniui.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-113">For time entries, select all the time entries for a specific combination of a project and a task.</span></span> <span data-ttu-id="dcbcf-114">Arba tinklelyje pažymėkite pavienius laiko langelius, nurodyti tam tikro projekto konkrečiai datai.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-114">Alternatively, in the grid, select the individual cells for time on a specific date for a specific project.</span></span>

    <span data-ttu-id="dcbcf-115">-arba-</span><span class="sxs-lookup"><span data-stu-id="dcbcf-115">–or–</span></span>

    <span data-ttu-id="dcbcf-116">Jei tai išlaidų įrašai, pažymėkite išlaidų įrašo, skirto atšaukti, eilutę.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-116">For expense entries, select the row for the expense entry to recall.</span></span>

3. <span data-ttu-id="dcbcf-117">Pažymėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-117">Select **Recall**.</span></span> <span data-ttu-id="dcbcf-118">Rodomos patvirtinimo dialogo langas.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-118">A confirmation dialog box appears.</span></span> <span data-ttu-id="dcbcf-119">Jei pažymėti laiko ir išlaidų įrašai jau buvo patvirtinti, būsite paraginti įvesti grąžinimo priežastį.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-119">If the selected time and expense entries were already approved, you're prompted to enter a reason for the recall.</span></span>
4. <span data-ttu-id="dcbcf-120">Įveskite atšaukimo priežastį, tada pažymėkite **Gerai**, kad patvirtintumėte operaciją.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-120">Enter a reason for the recall, and then select **OK** to confirm the operation.</span></span> <span data-ttu-id="dcbcf-121">Sistema siunčia asmeniui, patvirtinusiam įrašus, užklausą patvirtinti atšaukimą.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-121">The system sends the person who approved the entries a request to approve the recall.</span></span>

> [!NOTE]
> <span data-ttu-id="dcbcf-122">Nors patvirtinti laiko ir išlaidų įrašai gali būti atšaukti, jei patvirtintas laikas arba išlaidos jau buvo išrašyti klientui sąskaita faktūra, nebus galima sukurti atšaukimo užklausos.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-122">Although approved time and expense entries can be recalled, if an approved time or expense has already been invoiced to the customer, a recall request can't be created.</span></span> <span data-ttu-id="dcbcf-123">Naudotojas, kuris bando sukurti atšaukimo užklausą, gaus pranešimą, kuriame teigiama, kad laiko ar išlaidų negalima atšaukti, nes jau buvo išrašyta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-123">A user who tries to create a recall request will receive a message that states that the time or expense can't be recalled because it was already invoiced.</span></span>

## <a name="approve-or-reject-a-recall-request"></a><span data-ttu-id="dcbcf-124">Atšaukimo užklausos patvirtinimas arba atmetimas</span><span class="sxs-lookup"><span data-stu-id="dcbcf-124">Approve or reject a recall request</span></span>

<span data-ttu-id="dcbcf-125">Norėdami patvirtinti arba atmesti atšaukimo užklausą, atlikite šiuos veiksmus.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-125">Follow these steps to approve or reject a recall request.</span></span>

1. <span data-ttu-id="dcbcf-126">Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-126">Go to **Projects** \> **My Work** \> **Approvals**.</span></span>
2. <span data-ttu-id="dcbcf-127">Sąrašo puslapyje **Patvirtinimai** pakeiskite rodinį į **Atšaukimo užklausos patvirtinti**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-127">On the **Approvals** list page, change the view to **Recall requests for approval**.</span></span> <span data-ttu-id="dcbcf-128">Rodomas pateiktų atšaukimo užklausų sąrašas.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-128">A list of submitted recall requests is shown.</span></span>
3. <span data-ttu-id="dcbcf-129">Pažymėkite vieną arba kelis įrašus, tada pasirinkite **Patvirtinti** arba **Atmesti**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-129">Select one or more entries, and then select either **Approve** or **Reject**.</span></span>
4. <span data-ttu-id="dcbcf-130">Jei pažymėjote **Patvirtinti**, gausite įspėjimo pranešimą, paaiškinantį patvirtinimo poveikį.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-130">If you selected **Approve**, you receive a warning message that explains the impact of the approval.</span></span> <span data-ttu-id="dcbcf-131">Pasirinkite **Gerai** norėdami patvirtinti operaciją.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-131">Select **OK** to confirm the operation.</span></span> <span data-ttu-id="dcbcf-132">Atšaukimo užklausa patvirtinta.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-132">The recall request is approved.</span></span>

    <span data-ttu-id="dcbcf-133">-arba-</span><span class="sxs-lookup"><span data-stu-id="dcbcf-133">–or–</span></span>

    <span data-ttu-id="dcbcf-134">Jei pasirinkote **Atmesti**, atšaukimo užklausa atmetama.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-134">If you selected **Reject**, the recall request is rejected.</span></span>

> [!NOTE]
> <span data-ttu-id="dcbcf-135">Kai atšaukimas patvirtinamas, sistema tikrina, ar nėra sąskaitų faktūrų išrašymo veiklos pagal laiko arba išlaidų įrašus.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-135">As when a recall is requested, when a recall is approved, the system checks for any invoicing activity on the time or expense entries.</span></span> <span data-ttu-id="dcbcf-136">Jei įrašui jau buvo išrašyta sąskaita faktūra arba jis yra juodraščio sąskaitoje faktūroje, tvirtintojas gaus klaidos pranešimą, kuriame nurodoma, kad laiko ar išlaidų negalima patvirtinti atšaukti, nes jau buvo išrašyta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-136">If an entry was already invoiced, or if it's on a draft invoice, the approver will receive an error message that states that the time or expense can't be approved for recall, because it was already invoiced.</span></span>

## <a name="impact-of-a-recall-request"></a><span data-ttu-id="dcbcf-137">Atšaukimo užklausos poveikis</span><span class="sxs-lookup"><span data-stu-id="dcbcf-137">Impact of a recall request</span></span>

<span data-ttu-id="dcbcf-138">Kai patvirtinama atšaukti, atsiranda operatyvinis ir finansinis poveikis.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-138">When an approval is recalled, there is both operational impact and financial impact.</span></span>

### <a name="operational-impact"></a><span data-ttu-id="dcbcf-139">Operatyvinis poveikis</span><span class="sxs-lookup"><span data-stu-id="dcbcf-139">Operational impact</span></span>

<span data-ttu-id="dcbcf-140">Jei atšaukimo užklausa patvirtinama, patvirtinimo įrašas pažymimas kaip **Atmesta**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-140">If a recall request is approved, the approval record is marked as **Rejected**.</span></span> <span data-ttu-id="dcbcf-141">Įrašo būsena pakeičiama į **Grąžinta** arba **Atmesta**, atsižvelgiant į tai, ar tai yra laiko įrašas, ar išlaidų įrašas.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-141">The status of the entry is changed to either **Returned** or **Rejected**, depending on whether it's a time entry or an expense entry.</span></span>

<span data-ttu-id="dcbcf-142">Projekto komandos narys gali peržiūrėti įrašus, redaguoti ir pakartotinai pateikti įrašus arba visiškai panaikinti įrašus.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-142">The project team member can view entries, edit and then resubmit entries, or delete entries entirely.</span></span>

<span data-ttu-id="dcbcf-143">Jei atšaukimo užklausa atmetama, įrašo būsena lieka **Patvirtinta**, o projekto komandos nariui ar projekto tvirtintojui negalima redaguoti įrašo.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-143">If a recall request is rejected, the status of the entry remains **Approved**, and the entry can't be edited by the project team member or the approver for the project.</span></span>

### <a name="financial-impact"></a><span data-ttu-id="dcbcf-144">Finansinis poveikis</span><span class="sxs-lookup"><span data-stu-id="dcbcf-144">Financial impact</span></span>

<span data-ttu-id="dcbcf-145">Jei atšaukimo užklausa patvirtinama, atitinkami savikainos ir pardavimo faktiniai duomenys atnaujinami tokiu būdu:</span><span class="sxs-lookup"><span data-stu-id="dcbcf-145">If a recall request is approved, the corresponding actuals for cost and sales are updated in the following manner:</span></span>

- <span data-ttu-id="dcbcf-146">Laukas **Koregavimo būsena** atnaujinamas į **Pakoreguota**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-146">The **Adjustment Status** field is updated to **Adjusted**.</span></span>
- <span data-ttu-id="dcbcf-147">Laukas **SF išrašymo būsena** atnaujinamas į **Pakoreguota**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-147">The **Billing Status** field is updated to **Canceled**.</span></span>

<span data-ttu-id="dcbcf-148">Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-148">Next, reversal entries are created in the Actuals table.</span></span> <span data-ttu-id="dcbcf-149">Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-149">To create reversal entries, the system copies over the field values from the original actuals.</span></span> <span data-ttu-id="dcbcf-150">Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-150">The only values that aren't copied over are the quantity values.</span></span> <span data-ttu-id="dcbcf-151">Vietoj to, šios reikšmės yra atšaukiamos.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-151">These values are reversed instead.</span></span> <span data-ttu-id="dcbcf-152">Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-152">Reversed actuals are created for both **Cost** and **Unbilled Sales** actuals.</span></span> <span data-ttu-id="dcbcf-153">Laukas **Koregavimo būsena**, esantis atvirkštinių faktinių duomenų srityje, nustatomas kaip **Nekoreguojamas**, o laukas **SF išrašymo būsena** nustatomas kaip **Atšaukta**.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-153">The **Adjustment Status** field on the reversed actuals is set to **Unadjustable**, and the **Billing status** field is set to **Canceled**.</span></span> <span data-ttu-id="dcbcf-154">Dėl šių pakeitimų įrašyto neužbaigto projekto išlaidos ir pajamos nebebus įtraukiamos į sumas, kurias atitinka šie faktiniai duomenys.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-154">Because of these changes, the recorded spending and the revenue backlog on the project will no longer account for the amounts that these actuals represent.</span></span>

<span data-ttu-id="dcbcf-155">Jei atšaukimo užklausa atmetama, ji neturi finansinio poveikio projektui.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-155">If a recall request is rejected, there is no financial impact on the project.</span></span>

## <a name="changes-to-time-entry-records"></a><span data-ttu-id="dcbcf-156">Laiko įrašų kitimai</span><span class="sxs-lookup"><span data-stu-id="dcbcf-156">Changes to time entry records</span></span>

<span data-ttu-id="dcbcf-157">Šioje iliustracijoje rodomi kitimai, kurie įvyksta dėl patvirtintų laiko įrašų, kai jie atšaukiami.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-157">The following illustration shows the changes that occur for approved time entries when they are recalled.</span></span>

![Laiko įrašo būsenos perėjimai](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a><span data-ttu-id="dcbcf-159">Išlaidų įrašų kitimai</span><span class="sxs-lookup"><span data-stu-id="dcbcf-159">Changes to expense entry records</span></span>

<span data-ttu-id="dcbcf-160">Šioje iliustracijoje rodomi kitimai, kurie įvyksta dėl patvirtintų išlaidų įrašų, kai jie atšaukiami.</span><span class="sxs-lookup"><span data-stu-id="dcbcf-160">The following illustration shows the changes that occur for approved expense entries when they are recalled.</span></span>

![Išlaidų įrašų būsenos perėjimai](media/ExpenseEntryStateTransitions.png)
