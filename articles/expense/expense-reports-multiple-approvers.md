---
title: Išlaidų ataskaitos ir keli tvirtintojai
description: Šioje temoje pateikta informacija apie išlaidų ataskaitas, kurias patvirtinti reikalauja daugiau nei vienas asmuo.
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: cfa8677f38e9468aa3236f587d2e9bd5af839054
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121003"
---
# <a name="expense-reports-and-multiple-approvers"></a><span data-ttu-id="88e2a-103">Išlaidų ataskaitos ir keli tvirtintojai</span><span class="sxs-lookup"><span data-stu-id="88e2a-103">Expense reports and multiple approvers</span></span>

<span data-ttu-id="88e2a-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="88e2a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="88e2a-105">Atsižvelgiant į organizacijos išlaidų patvirtinimo strategijas, daugiau nei vienas asmuo gali turėti patvirtinti pateiktą išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="88e2a-105">Depending on your organization's expense approval policies, more than one person might have to approve a submitted expense report.</span></span> <span data-ttu-id="88e2a-106">Nustatę išlaidų ataskaitos patvirtinimo darbo eigos procesą, galite įtraukti darbo eigos elementų, kuriuose yra vieno ar kelių išlaidų ataskaitos tvirtintojų užduočių ar veiksmų.</span><span class="sxs-lookup"><span data-stu-id="88e2a-106">When you set up the workflow process for expense report approval, you can add workflow elements that include tasks or steps for one or more expense report approvers.</span></span> <span data-ttu-id="88e2a-107">Pavyzdžiui, jums gali prireikti, kad visas išlaidų ataskaitas patvirtintų du atskiri asmenys, darbuotojo, kuris pateikė ataskaitą, vadovas, ir mokėtinų sumų koordinatorius.</span><span class="sxs-lookup"><span data-stu-id="88e2a-107">For example, you might require that all expense reports be approved by two separate people, the manager of the employee who submitted the report and the Accounts payable coordinator.</span></span>

<span data-ttu-id="88e2a-108">Jei nuspręsite, kad reikia kelių išlaidų ataskaitų tvirtintojų, galite įtraukti darbo eigos elementų į bet kurį iš šių būdų:</span><span class="sxs-lookup"><span data-stu-id="88e2a-108">If you decide to require multiple expense report approvers, you can add the workflow elements in any of the following ways:</span></span>

- <span data-ttu-id="88e2a-109">Pridėkite vieną patvirtinimo elementą, kuris turi vieną žingsnį.</span><span class="sxs-lookup"><span data-stu-id="88e2a-109">Add one approval element that has one step.</span></span> <span data-ttu-id="88e2a-110">Pavyzdžiui, norint atlikti šiuos veiksmus, gali prireikti, kad išlaidų ataskaita būtų priskirta vartotojų grupei, o ją patvirtintų 50 procentų vartotojų grupės narių.</span><span class="sxs-lookup"><span data-stu-id="88e2a-110">For example, the step might require that an expense report be assigned to a user group, and that it be approved by 50 percent of the user group's members.</span></span>
- <span data-ttu-id="88e2a-111">Pridėkite vieną patvirtinimo elementą, kuris turi kelis žingsnius.</span><span class="sxs-lookup"><span data-stu-id="88e2a-111">Add one approval element that has multiple steps.</span></span> <span data-ttu-id="88e2a-112">Pavyzdžiui, patvirtinimo elementas gali turėti šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="88e2a-112">For example, the approval element might have the following steps:</span></span>

    1. <span data-ttu-id="88e2a-113">Darbuotojo, kuris pateikė išlaidų ataskaitą, vadovas jį patvirtina.</span><span class="sxs-lookup"><span data-stu-id="88e2a-113">The manager of the employee who submitted the expense report approves it.</span></span>
    2. <span data-ttu-id="88e2a-114">Mokėtinos sąskaitos tarnautojas patikrina gavimo ir išlaidų ataskaitos elementus.</span><span class="sxs-lookup"><span data-stu-id="88e2a-114">The Accounts payable clerk verifies the receipts and the expense report items.</span></span>
    3. <span data-ttu-id="88e2a-115">Biudžeto savininkas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="88e2a-115">The budget owner approves the expense report.</span></span>

- <span data-ttu-id="88e2a-116">Įtraukite kelis patvirtinimo elementus, kurių kiekvienas turi vieną žingsnį.</span><span class="sxs-lookup"><span data-stu-id="88e2a-116">Add multiple approval elements, each of which has one step.</span></span> <span data-ttu-id="88e2a-117">Pavyzdžiui, galite įtraukti atskirą patvirtinimo elementą į šiuos žingsnius:</span><span class="sxs-lookup"><span data-stu-id="88e2a-117">For example, you might add a separate approval element for each of the following steps:</span></span>

    1. <span data-ttu-id="88e2a-118">Darbuotojo vadovas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="88e2a-118">The employee's manager approves the expense report.</span></span>
    2. <span data-ttu-id="88e2a-119">Biudžeto savininkas patvirtina išlaidų ataskaitą.</span><span class="sxs-lookup"><span data-stu-id="88e2a-119">The budget owner approves the expense report.</span></span>
