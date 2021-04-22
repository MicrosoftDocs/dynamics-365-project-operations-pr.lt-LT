---
title: Išlaidų valdymo darbo eiga
description: Šioje temoje aiškinama, kaip „Microsoft Dynamics 365 Finance“ galima naudoti darbo eigos sistemą, norint nustatyti išlaidų valdymo išlaidų ataskaitų peržiūros procesą.
author: ShylaThompson
manager: AnnBe
ms.date: 09/13/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WorkflowtableListPageRnr
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fde336f53d72e9ddf38c5123d9e774a4c3a22a28
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271678"
---
# <a name="expense-management-workflow"></a><span data-ttu-id="3cf9f-103">Išlaidų valdymo darbo eiga</span><span class="sxs-lookup"><span data-stu-id="3cf9f-103">Expense management workflow</span></span>

<span data-ttu-id="3cf9f-104">Galite naudoti darbo eigos sistemą, norėdami nustatyti išlaidų valdymo išlaidų ataskaitų peržiūros procesą.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-104">You can use the workflow system to set up a review process for expense reports in Expense management.</span></span> <span data-ttu-id="3cf9f-105">Galite nustatyti darbo eigą, kuri naudoja šiuos kriterijus, kad nustatytų, kas patvirtina išlaidų ataskaitas.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-105">You can set up a workflow that uses the following criteria to determine who approves expense reports:</span></span>

- <span data-ttu-id="3cf9f-106">Darbuotojų ataskaitų hierarchija ir iš anksto nustatyti patvirtinimo apribojimai</span><span class="sxs-lookup"><span data-stu-id="3cf9f-106">The employee reporting hierarchy and predefined approval limits</span></span>
- <span data-ttu-id="3cf9f-107">Daugiapakopis patvirtinimas, palaikantis laikinuosius tvirtintojus ir galutinį tvirtintoją</span><span class="sxs-lookup"><span data-stu-id="3cf9f-107">Multi-level approval that supports interim approvers and a final approver</span></span>
- <span data-ttu-id="3cf9f-108">Finansinės dimensijos ir projektų vykdymo atsakomybė</span><span class="sxs-lookup"><span data-stu-id="3cf9f-108">Financial dimensions and project responsibility</span></span>
- <span data-ttu-id="3cf9f-109">Priskyrimas konkretiems vartotojams arba vartotojų grupėms</span><span class="sxs-lookup"><span data-stu-id="3cf9f-109">Assignment to specific users or user groups</span></span>

<span data-ttu-id="3cf9f-110">Galima kurti išlaidų ataskaitų, kelionių paraiškų, avansinių mokėjimų ir pridėtinės vertės mokesčio (PVM) susigrąžinimo darbo eigos patvirtinimus.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-110">Workflow approvals can be created for expense reports, travel requisitions, cash advances, and value-added tax (VAT) recovery.</span></span>

<span data-ttu-id="3cf9f-111">**Pavyzdžiui**</span><span class="sxs-lookup"><span data-stu-id="3cf9f-111">**Example**</span></span>

<span data-ttu-id="3cf9f-112">Toliau pateikiamas išlaidų ataskaitos išlaidų valdymo darbo eigos pavyzdys.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-112">The following process is an example of the expense management workflow for an expense report.</span></span>

1. <span data-ttu-id="3cf9f-113">Darbuotojas sukuria ir išsaugo išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-113">An employee creates and saves an expense report.</span></span>
2. <span data-ttu-id="3cf9f-114">Darbuotojas pateikia išlaidų ataskaitą patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-114">The employee submits the expense report for approval.</span></span> <span data-ttu-id="3cf9f-115">Tvirtintojas identifikuojamas pagal taisykles, apibrėžtas nustatant darbo eigą.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-115">The approver is identified based on the rules that were defined when the workflow was set up.</span></span>
3. <span data-ttu-id="3cf9f-116">Tvirtintojas gauna pranešimą, kad išlaidų ataskaita paruošta patvirtinti.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-116">The approver receives a notification that an expense report is ready for approval.</span></span> <span data-ttu-id="3cf9f-117">Tvirtintojas patikrina išlaidų ataskaitą ir patvirtina, kad tenkinamos toliau nurodytos sąlygos.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-117">The approver reviews the expense report and verifies that the following conditions are met:</span></span>

    - <span data-ttu-id="3cf9f-118">Išlaidos nepažeidžia jokios išlaidų strategijos.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-118">The expenses don't violate any expense policies.</span></span> <span data-ttu-id="3cf9f-119">Jei išlaidos pažeidžia strategiją, tvirtintojas patikrina, ar išlaidų ataskaitoje yra galiojantis įmonės pagrindimas.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-119">If an expense violates a policy, the approver verifies that the expense report includes a valid business justification.</span></span>
    - <span data-ttu-id="3cf9f-120">Elektroniniai kvitai pridėti prie išlaidų ataskaitos.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-120">Electronic receipts are attached to the expense report.</span></span>

4. <span data-ttu-id="3cf9f-121">Tvirtintojas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-121">The approver approves the expense report.</span></span>
5. <span data-ttu-id="3cf9f-122">Išlaidų ataskaita priskirta mokėtinų sumų koordinatoriui užregistruoti.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-122">The expense report is assigned to the Accounts payable coordinator for posting.</span></span>
6. <span data-ttu-id="3cf9f-123">Atliekamas vienas iš toliau nurodytų veiksmų, atsižvelgiant į tai, ar sukonfigūruotas automatinis registravimas.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-123">One of the following steps occurs, depending on whether automatic posting is configured:</span></span>

    - <span data-ttu-id="3cf9f-124">Jei automatinis registravimas sukonfigūruotas, išlaidų ataskaita apdorojama ir vykdomas mokėjimas, o išlaidų ataskaitos būsena atnaujinama.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-124">If automatic posting is configured, the expense report is processed for payment, and the status of the expense report is updated.</span></span>
    - <span data-ttu-id="3cf9f-125">Jei automatinis registravimas nesukonfigūruotas, mokėtinos sumos koordinatorius patikrina, ar yra pateikti visi pradiniai kvitai ir kad kvitai suderinti su išlaidų ataskaitos išlaidomis.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-125">If automatic posting isn't configured, the Accounts payable coordinator verifies that all original receipts have been submitted, and that the receipts are aligned with the expenses on the expense report.</span></span> <span data-ttu-id="3cf9f-126">Visi mokesčių kodai, įvesti išlaidų ataskaitoje, taip pat turi būti patvirtinti kaip teisingi.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-126">All tax codes that are entered on the expense report must also be verified as correct.</span></span>

<span data-ttu-id="3cf9f-127">Kai šie reikalavimai patvirtinti, užregistruojama išlaidų ataskaita.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-127">After these requirements are verified, the expense report is posted.</span></span>

<span data-ttu-id="3cf9f-128">Užregistravus išlaidų ataskaitą, leidžiama atlikti išlaidų ataskaitos mokėjimą ir kompensuoti darbuotojo išlaidas.</span><span class="sxs-lookup"><span data-stu-id="3cf9f-128">After the expense report is posted, payment is authorized for the expense report, and the employee is reimbursed.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]