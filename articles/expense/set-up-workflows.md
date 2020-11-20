---
title: Išlaidų valdymo darbo eigų nustatymas
description: Galite nustatyti darbo eigos procesą, naudojamą kelionių ir išlaidų dokumentų peržiūrai ir tvirtinimui.
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
ms.openlocfilehash: af6463b07e282ae1ff6aa7dc1a540ff7c8cc318a
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127708"
---
# <a name="set-up-workflows-for-expense-management"></a><span data-ttu-id="247a8-103">Išlaidų valdymo darbo eigų nustatymas</span><span class="sxs-lookup"><span data-stu-id="247a8-103">Set up workflows for Expense management</span></span>

<span data-ttu-id="247a8-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="247a8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="247a8-105">Galite nustatyti darbo eigos procesą kelionių ir išlaidų dokumentų peržiūrai ir tvirtinimui.</span><span class="sxs-lookup"><span data-stu-id="247a8-105">You can set up a workflow process to review and approve travel and expense documents.</span></span> <span data-ttu-id="247a8-106">Galite apibrėžti išlaidų ataskaitų, kelionių paraiškų ir grynųjų pinigų išankstinių užklausų darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="247a8-106">You can define workflows for expense reports, travel requisitions, and cash advance requests.</span></span>

<span data-ttu-id="247a8-107">Darbo eiga yra verslo procesų ir apibrėžia, kaip dokumentas teka sistema.</span><span class="sxs-lookup"><span data-stu-id="247a8-107">A workflow represents a business process and defines how a document flows through the system.</span></span> <span data-ttu-id="247a8-108">Darbo eiga taip pat nurodo, kas turi atlikti užduotį arba patvirtinti dokumentą.</span><span class="sxs-lookup"><span data-stu-id="247a8-108">The workflow also indicates who must complete a task or approve a document.</span></span> <span data-ttu-id="247a8-109">Jūsų organizacijoje yra keli darbo eigos sistemos naudojimo pranašumai:</span><span class="sxs-lookup"><span data-stu-id="247a8-109">There are several benefits of using the workflow system in your organization:</span></span>

- <span data-ttu-id="247a8-110">**Nuoseklūs procesai** – galite apibrėžti tam tikrų dokumentų, pvz., pirkimo paraiškų ir išlaidų ataskaitų, patvirtinimo procesą.</span><span class="sxs-lookup"><span data-stu-id="247a8-110">**Consistent processes**: You can define the approval process for specific documents, such as purchase requisitions and expense reports.</span></span> <span data-ttu-id="247a8-111">Darbo eigos sistemos naudojimas padeda užtikrinti, kad dokumentai būtų apdorojami ir tvirtinami nuosekliai bei efektyviai.</span><span class="sxs-lookup"><span data-stu-id="247a8-111">Using the workflow system helps ensure that documents are processed and approved in a consistent and efficient manner.</span></span>
- <span data-ttu-id="247a8-112">**Proceso matomumas** – galite sekti tam tikro darbo eigos egzemplioriaus būseną, retrospektyvą ir našumą.</span><span class="sxs-lookup"><span data-stu-id="247a8-112">**Process visibility**: You can track the status, history, and performance metrics of a specific workflow instance.</span></span> <span data-ttu-id="247a8-113">Taip galėsite nustatyti, ar darbo eiga turi būti keičiama efektyvumui padidinti.</span><span class="sxs-lookup"><span data-stu-id="247a8-113">This helps you determine whether changes should be made to the workflow to improve efficiency.</span></span>
- <span data-ttu-id="247a8-114">**Centralizuotas darbo sąrašas** – vartotojai gali peržiūrėti centralizuotą darbo sąrašą, kad galėtų peržiūrėti jiems priskirtas darbo eigos užduotis ir patvirtinimus.</span><span class="sxs-lookup"><span data-stu-id="247a8-114">**Centralized work list**: Users can view a centralized work list to view the workflow tasks and approvals assigned to them.</span></span> 

## <a name="workflow-types"></a><span data-ttu-id="247a8-115">Darbo eigos tipai</span><span class="sxs-lookup"><span data-stu-id="247a8-115">Workflow types</span></span>

<span data-ttu-id="247a8-116">Šioje lentelėje išvardyti darbo eigų tipai, kuriuos galite sukurti **Išlaidų valdyme**.</span><span class="sxs-lookup"><span data-stu-id="247a8-116">The following table lists the types of workflows that you can create in **Expense Management**.</span></span>


|              <span data-ttu-id="247a8-117"><strong>Tipas</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-117"><strong>Type</strong></span></span>              |                   <span data-ttu-id="247a8-118"><strong>Naudokite šį tipą, kad</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-118"><strong>Use this type to</strong></span></span>                   |
|-------------------------------------------------|-----------------------------------------------------------------------|
|   <span data-ttu-id="247a8-119"><strong>Išlaidų ataskaitos automatinis patvirtinimas</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-119"><strong>Expense report auto approval</strong></span></span> |            <span data-ttu-id="247a8-120">Kurti išlaidų ataskaitų patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="247a8-120">Create approval workflows for expense reports.</span></span>             |
|  <span data-ttu-id="247a8-121"><strong>Išlaidų ataskaitų automatinis publikavimas</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-121"><strong>Expense report auto posting</strong></span></span>   |        <span data-ttu-id="247a8-122">Kurti išlaidų ataskaitų automatinio publikavimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="247a8-122">Create automatic posting workflows for expense reports.</span></span>        |
|       <span data-ttu-id="247a8-123"><strong>Išlaidų eilutės elementas</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-123"><strong>Expense line item</strong></span></span>        |     <span data-ttu-id="247a8-124">Kurti išlaidų ataskaitų eilučių elementų patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="247a8-124">Create approval workflows for line items on expense reports.</span></span>      |
| <span data-ttu-id="247a8-125"><strong>Išlaidų eilutės elemento automatinis publikavimas</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-125"><strong>Expense line item auto posting</strong></span></span> | <span data-ttu-id="247a8-126">Kurti išlaidų ataskaitų eilučių elementų automatinio publikavimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="247a8-126">Create automatic posting workflows for line items on expense reports.</span></span> |
|       <span data-ttu-id="247a8-127"><strong>Kelionės paraiška</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-127"><strong>Travel requisition</strong></span></span>       |          <span data-ttu-id="247a8-128">Kurkite kelionių paraiškų patvirtinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="247a8-128">Create approval workflows for travel requisitions.</span></span>           |
|      <span data-ttu-id="247a8-129"><strong>Avansinis mokėjimo užklausa</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-129"><strong>Cash advance request</strong></span></span>      |         <span data-ttu-id="247a8-130">Grynųjų pinigų avanso užklausų patvirtinimo darbo eigų kūrimas.</span><span class="sxs-lookup"><span data-stu-id="247a8-130">Create approval workflows for cash advance requests.</span></span>          |
|        <span data-ttu-id="247a8-131"><strong>PVM mokesčių grąžinimas</strong></span><span class="sxs-lookup"><span data-stu-id="247a8-131"><strong>VAT tax recovery</strong></span></span>        | <span data-ttu-id="247a8-132">Kurti pridėtinės vertės mokesčio (PVM) susigrąžinimo darbo eigas.</span><span class="sxs-lookup"><span data-stu-id="247a8-132">Create approval workflows for the recovery of value-added tax (VAT).</span></span>  |
