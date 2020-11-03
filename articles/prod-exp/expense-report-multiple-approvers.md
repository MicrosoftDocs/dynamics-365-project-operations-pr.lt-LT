---
title: Keli išlaidų ataskaitos tvirtintojai
description: Šioje temoje pateikta informacija apie išlaidų ataskaitas, kurias patvirtinti reikalauja daugiau nei vienas asmuo.
author: saraschi2
manager: AnnBe
ms.date: 02/23/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvExpensesReportList
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce24b156a268f9f5aada35f9314d2d9c6607200b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080992"
---
# <a name="multiple-approvers-on-an-expense-report"></a><span data-ttu-id="fd574-103">Keli išlaidų ataskaitos tvirtintojai</span><span class="sxs-lookup"><span data-stu-id="fd574-103">Multiple approvers on an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="fd574-104">Atsižvelgiant į organizacijos išlaidų patvirtinimo strategijas, daugiau nei vienas asmuo gali turėti patvirtinti darbuotojo pateiktą išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fd574-104">Depending on your organization's expense approval policies, more than one person might have to approve an expense report that is submitted by an employee.</span></span> <span data-ttu-id="fd574-105">Nustatę išlaidų ataskaitos patvirtinimo darbo eigos procesą, galite įtraukti darbo eigos elementų, kuriuose yra vieno ar kelių išlaidų ataskaitos tvirtintojų užduočių ar veiksmų.</span><span class="sxs-lookup"><span data-stu-id="fd574-105">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="fd574-106">Pavyzdžiui, jums gali prireikti, kad visas išlaidų ataskaitas pirmiausia patvirtintų darbuotojo, kuris pateikė ataskaitą, vadovas, o tada – mokėtinų sumų koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="fd574-106">For example, you might require that all expense reports be approved first by the manager of the employee who submitted the report and then by the Accounts payable coordinator.</span></span>

<span data-ttu-id="fd574-107">Jei nuspręsite, kad reikia kelių išlaidų ataskaitų tvirtintojų, galite įtraukti darbo eigos elementų į bet kurį iš šių būdų:</span><span class="sxs-lookup"><span data-stu-id="fd574-107">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="fd574-108">Pridėkite vieną patvirtinimo elementą, kuris turi vieną žingsnį.</span><span class="sxs-lookup"><span data-stu-id="fd574-108">Add one approval element that has one step.</span></span> <span data-ttu-id="fd574-109">Pavyzdžiui, norint atlikti šiuos veiksmus, gali prireikti, kad išlaidų ataskaita būtų priskirta vartotojų grupei, o ją patvirtintų 50 procentų vartotojų grupės narių.</span><span class="sxs-lookup"><span data-stu-id="fd574-109">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="fd574-110">Pridėkite vieną patvirtinimo elementą, kuris turi kelis žingsnius.</span><span class="sxs-lookup"><span data-stu-id="fd574-110">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="fd574-111">Pavyzdžiui, patvirtinimo elementas gali turėti šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="fd574-111">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="fd574-112">Darbuotojo, kuris pateikė išlaidų ataskaitą, vadovas jį patvirtina.</span><span class="sxs-lookup"><span data-stu-id="fd574-112">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="fd574-113">Mokėtinos sąskaitos tarnautojas patikrina gavimo ir išlaidų ataskaitos elementus.</span><span class="sxs-lookup"><span data-stu-id="fd574-113">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="fd574-114">Biudžeto savininkas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fd574-114">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="fd574-115">Įtraukite kelis patvirtinimo elementus, kurių kiekvienas turi vieną žingsnį.</span><span class="sxs-lookup"><span data-stu-id="fd574-115">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="fd574-116">Pavyzdžiui, galite įtraukti atskirą patvirtinimo elementą į šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="fd574-116">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="fd574-117">Darbuotojo vadovas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fd574-117">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="fd574-118">Biudžeto savininkas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="fd574-118">The budget owner approves the expense report.</span></span>
