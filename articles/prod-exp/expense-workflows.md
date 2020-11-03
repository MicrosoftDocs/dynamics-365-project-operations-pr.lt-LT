---
title: Išlaidų valdymo darbo eigų nustatymas
description: Galite nustatyti darbo eigos procesą kelionių ir išlaidų dokumentų peržiūrai ir tvirtinimui.
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
ms.openlocfilehash: 0af23ed2cf172e4c90de72f5db389c349303c039
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080990"
---
# <a name="set-up-expense-management-workflows"></a><span data-ttu-id="49cd8-103">Išlaidų valdymo darbo eigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="49cd8-103">Set up Expense management workflows</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="49cd8-104">Galite nustatyti darbo eigos procesą, naudojamą kelionių ir išlaidų dokumentų peržiūrai ir tvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="49cd8-104">You can set up a workflow process that is used to review and approve travel and expense documents.</span></span> <span data-ttu-id="49cd8-105">Dokumentai, kurių darbo eigas galite apibrėžti, apima išlaidų ataskaitas, kelionių paraiškas ir avansinio mokėjimo užklausas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-105">The documents for which workflows can be defined include expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="49cd8-106">Darbo eiga yra įmonės procesas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-106">A workflow represents a business process.</span></span> <span data-ttu-id="49cd8-107">Ji apibrėžia, kaip dokumentas apdorojamas sistemoje, ir nurodo, kas turi atlikti užduotį arba patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="49cd8-107">It defines how a document flows through the system and indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="49cd8-108">Jūsų organizacijoje yra keli darbo eigos sistemos naudojimo pranašumai:</span><span class="sxs-lookup"><span data-stu-id="49cd8-108">There are several benefits of using the workflow system in your organization:</span></span>

-   <span data-ttu-id="49cd8-109">**Nuoseklūs procesai** – galite apibrėžti tam tikrų dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="49cd8-109">**Consistent processes** — You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="49cd8-110">Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai būtų apdorojami ir tvirtinami nuosekliai bei efektyviai.</span><span class="sxs-lookup"><span data-stu-id="49cd8-110">Using the workflow system helps to ensure that documents are processed and approved in a consistent and efficient manner.</span></span>

-   <span data-ttu-id="49cd8-111">Proceso matomumas – galite sekti tam tikro darbo eigos egzemplioriaus būseną, retrospektyvą ir našumą.</span><span class="sxs-lookup"><span data-stu-id="49cd8-111">Process visibility — You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="49cd8-112">Taip galėsite nustatyti, ar darbo eiga turi būti keičiama efektyvumui padidinti.</span><span class="sxs-lookup"><span data-stu-id="49cd8-112">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>

-   <span data-ttu-id="49cd8-113">Centralizuotas darbo sąrašas – vartotojai gali peržiūrėti centralizuotą darbo sąrašą, kad galėtų peržiūrėti jiems priskirtas darbo eigos užduotis ir patvirtinimus.</span><span class="sxs-lookup"><span data-stu-id="49cd8-113">Centralized work list — Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

<span data-ttu-id="49cd8-114">**Darbo eigų, kurias galite kurti, tipai**</span><span class="sxs-lookup"><span data-stu-id="49cd8-114">**The types of workflows you can create**</span></span>

<span data-ttu-id="49cd8-115">Šioje lentelėje išvardyti darbo eigų tipai, kuriuos galite sukurti **Išlaidose**.</span><span class="sxs-lookup"><span data-stu-id="49cd8-115">The following table lists the types of workflows that you can create in **Expense**.</span></span>


|              <span data-ttu-id="49cd8-116"><strong>Tipas</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-116"><strong>Type</strong></span></span>              |                   <span data-ttu-id="49cd8-117"><strong>Naudokite šį tipą, kad</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-117"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|         <span data-ttu-id="49cd8-118"><strong>Išlaidų ataskaita</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-118"><strong>Expense report</strong></span></span>         |            <span data-ttu-id="49cd8-119">Kurti išlaidų ataskaitų patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-119">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="49cd8-120"><strong>Išlaidų ataskaitų automatinis publikavimas</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-120"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="49cd8-121">Kurti išlaidų ataskaitų automatinio publikavimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-121">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="49cd8-122"><strong>Išlaidų eilutės elementas</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-122"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="49cd8-123">Kurti išlaidų ataskaitų eilučių elementų patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-123">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="49cd8-124"><strong>Išlaidų eilutės elemento automatinis publikavimas</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-124"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="49cd8-125">Kurti išlaidų ataskaitų eilučių elementų automatinio publikavimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-125">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="49cd8-126"><strong>Kelionės paraiška</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-126"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="49cd8-127">Kurkite kelionių paraiškų patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-127">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="49cd8-128"><strong>Avansinis mokėjimo užklausa</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-128"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="49cd8-129">Grynųjų pinigų avanso užklausų patvirtinimo darbo eigų kūrimas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-129">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="49cd8-130"><strong>PVM mokesčių grąžinimas</strong></span><span class="sxs-lookup"><span data-stu-id="49cd8-130"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="49cd8-131">Kurti pridėtinės vertės mokesčio (PVM) susigrąžinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="49cd8-131">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |

