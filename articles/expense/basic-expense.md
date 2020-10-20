---
title: Išlaidų įrašas („Lite“ versija)
description: Šioje temoje pateikta informacija apie tai, kaip dirbti su išlaidų įrašu „Lite“ visuotiniame diegime.
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965843"
---
# <a name="expense-entry-lite"></a><span data-ttu-id="4b58c-103">Išlaidų įrašas („Lite“ versija)</span><span class="sxs-lookup"><span data-stu-id="4b58c-103">Expense entry (lite)</span></span>

<span data-ttu-id="4b58c-104">_**Taikoma:** „Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros kūrimui_</span><span class="sxs-lookup"><span data-stu-id="4b58c-104">_**Applies to:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="4b58c-105">Pagrindinių (arba supaprastintų) išlaidų valdymas yra galimybė įrašyti paprastas išlaidas.</span><span class="sxs-lookup"><span data-stu-id="4b58c-105">Basic, or lite, expense management is the capability to record simple expenses.</span></span> <span data-ttu-id="4b58c-106">Galite įrašyti projekto išlaidas, o tada projektų tvirtintojas jas peržiūrės ir patvirtins.</span><span class="sxs-lookup"><span data-stu-id="4b58c-106">You can record expenses against a project, and then the project approver will review and approve them.</span></span>

<span data-ttu-id="4b58c-107">Daugiau informacijos apie išlaidų galimybes naudojant „Dynamics 365 Project Operations“ žr. [Išlaidų apžvalga](expense-overview.md).</span><span class="sxs-lookup"><span data-stu-id="4b58c-107">For more information about expense capabilities in Dynamics 365 Project Operations, see [Expense overview](expense-overview.md).</span></span>

## <a name="capture-a-basic-expense"></a><span data-ttu-id="4b58c-108">Pagrindinių išlaidų fiksavimas</span><span class="sxs-lookup"><span data-stu-id="4b58c-108">Capture a basic expense</span></span>

<span data-ttu-id="4b58c-109">Galite fiksuoti savo išlaidas, kad galėtumėte jas pateikti tvirtintojui.</span><span class="sxs-lookup"><span data-stu-id="4b58c-109">You can capture your expenses so that you can submit them to the approver.</span></span>

1. <span data-ttu-id="4b58c-110">Eikite į **Išlaidos** ir pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="4b58c-110">Go to **Expenses**, and select **New**.</span></span>
2. <span data-ttu-id="4b58c-111">Puslapyje **Naujos išlaidos** įveskite reikiamą išlaidų informaciją, o tada pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="4b58c-111">On the **New Expense** page, enter the required expense information, and then select **Save**.</span></span>

## <a name="submit-a-basic-expense"></a><span data-ttu-id="4b58c-112">Pagrindinių išlaidų pateikimas</span><span class="sxs-lookup"><span data-stu-id="4b58c-112">Submit a basic expense</span></span>

<span data-ttu-id="4b58c-113">Kai baigsite fiksuoti visas išlaidas ir jūs būsite pasirengę jas patvirtinti, turite jas pateikti.</span><span class="sxs-lookup"><span data-stu-id="4b58c-113">After you've finished capturing all your expenses, and you're ready to have them approved, you must submit them.</span></span>

1. <span data-ttu-id="4b58c-114">Eikite į **Išlaidos** ir pasirinkite išlaidas.</span><span class="sxs-lookup"><span data-stu-id="4b58c-114">Go to **Expenses**, and select an expense.</span></span> <span data-ttu-id="4b58c-115">Arba pažymėkite visas išlaidas naudodami antraštės žymės langelį.</span><span class="sxs-lookup"><span data-stu-id="4b58c-115">Or, select all the expenses by using the check box on the header.</span></span>
2. <span data-ttu-id="4b58c-116">Pasirinkite **Pateikti**.</span><span class="sxs-lookup"><span data-stu-id="4b58c-116">Select **Submit**.</span></span> <span data-ttu-id="4b58c-117">Sistema apdoroja pažymėtus įrašus ir sukuria išlaidų patvirtinimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="4b58c-117">The system processes the selected entries and then creates expense approval requests.</span></span>

## <a name="recall-a-basic-expense"></a><span data-ttu-id="4b58c-118">Pagrindinių išlaidų atšaukimas</span><span class="sxs-lookup"><span data-stu-id="4b58c-118">Recall a basic expense</span></span>

<span data-ttu-id="4b58c-119">Kai per klaidą pateikiate išlaidas, galite jas atšaukti.</span><span class="sxs-lookup"><span data-stu-id="4b58c-119">When you submit an expense by mistake, you can recall it.</span></span> <span data-ttu-id="4b58c-120">Laikas, reikalingas išlaidų įrašui atšaukti, priklauso nuo jo tvirtinimo etapo.</span><span class="sxs-lookup"><span data-stu-id="4b58c-120">The time that is required to recall an expense entry depends on its approval stage.</span></span>  <span data-ttu-id="4b58c-121">Jei tvirtintojas dar nepatvirtino įrašo, jis gali būti nedelsiant atšauktas.</span><span class="sxs-lookup"><span data-stu-id="4b58c-121">If the approver hasn't yet approved the entry, the recall can occur immediately.</span></span> <span data-ttu-id="4b58c-122">Tačiau, jei įrašas jau buvo patvirtintas, tvirtintoją prašoma patvirtinti atšaukimą ir atšaukti operacijas.</span><span class="sxs-lookup"><span data-stu-id="4b58c-122">However, if the entry has already been approved, the approver is asked to approve the recall and reverse the transactions.</span></span>

1. <span data-ttu-id="4b58c-123">Eikit į **išlaidos**, o tada išlaidų sąraše pažymėkite išlaidas, kurias reikia atšaukti.</span><span class="sxs-lookup"><span data-stu-id="4b58c-123">Go to **Expenses**, and then, in the list of expenses, select the expense to recall.</span></span>
2. <span data-ttu-id="4b58c-124">Pažymėkite **Atšaukti**.</span><span class="sxs-lookup"><span data-stu-id="4b58c-124">Select **Recall**.</span></span> <span data-ttu-id="4b58c-125">Jei išlaidų įrašas dar nepatvirtintas, sistema iš karto jį atšaukia.</span><span class="sxs-lookup"><span data-stu-id="4b58c-125">If the expense entry hasn't yet been approved, the system immediately recalls it.</span></span> <span data-ttu-id="4b58c-126">Jei išlaidų įrašas jau patvirtintas, bus sukurta atšaukimo užklausa, kad praneštų tvirtintojui, jog norite atšaukti išlaidas.</span><span class="sxs-lookup"><span data-stu-id="4b58c-126">If the expense entry has already been approved, a recall request is created to notify the approver that you want to reverse the expense.</span></span> <span data-ttu-id="4b58c-127">Tvirtintojas patvirtina, kad galima atšaukti, o įrašas bus grąžintas.</span><span class="sxs-lookup"><span data-stu-id="4b58c-127">The approver will then confirm that the reversal can be done, and the entry will be returned.</span></span>

## <a name="delete-a-basic-expense"></a><span data-ttu-id="4b58c-128">Pagrindinių išlaidų naikinimas</span><span class="sxs-lookup"><span data-stu-id="4b58c-128">Delete a basic expense</span></span>

<span data-ttu-id="4b58c-129">Išlaidos, kurios dar nebuvo pateiktos, gali būti panaikintos.</span><span class="sxs-lookup"><span data-stu-id="4b58c-129">Expenses that haven't yet been submitted can be deleted.</span></span> <span data-ttu-id="4b58c-130">Norėdami panaikinti jau pateiktas išlaidas, pirmiausia turite jas atšaukti.</span><span class="sxs-lookup"><span data-stu-id="4b58c-130">To delete an expense that has already been submitted, you must first recall it.</span></span>

## <a name="see-also"></a><span data-ttu-id="4b58c-131">Taip pat žr.</span><span class="sxs-lookup"><span data-stu-id="4b58c-131">See also</span></span>

- [<span data-ttu-id="4b58c-132">Tvirtinimų apžvalga</span><span class="sxs-lookup"><span data-stu-id="4b58c-132">Approvals overview</span></span>](../approvals/approvals-overview.md)
