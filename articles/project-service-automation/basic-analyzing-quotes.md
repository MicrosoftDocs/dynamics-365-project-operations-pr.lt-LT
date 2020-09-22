---
title: Projekto pasiūlymų analizė
description: Šioje temoje pateikiama informacija apie projekto pasiūlymų analizę.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 57ac8407-26f5-49dd-97ea-e97642789ff5
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 63c826d27863df62301ec1548fdc94158220c3a2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753637"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="e204a-103">Projekto pasiūlymų analizė</span><span class="sxs-lookup"><span data-stu-id="e204a-103">Analysis of project quotes</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e204a-104">„Dynamics 365 Project Service Automation“ analizuoja projekto pasiūlymus ir įvertina jų pelningumą.</span><span class="sxs-lookup"><span data-stu-id="e204a-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="e204a-105">Ji taip pat analizuoja, kiek pasiūlymas atitinka kliento lūkesčius dėl pristatymo datos arba įvykdymo datos ir biudžeto.</span><span class="sxs-lookup"><span data-stu-id="e204a-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="e204a-106">Pelningumo analizė</span><span class="sxs-lookup"><span data-stu-id="e204a-106">Profitability analysis</span></span>

<span data-ttu-id="e204a-107">Programos „Project Service Automation“ vykdomai pelningumo analizei naudojama bruto marža ir pakoreguota bruto marža.</span><span class="sxs-lookup"><span data-stu-id="e204a-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="e204a-108">Bruto maržos apskaičiuojamos pagal toliau nurodytą formulę.</span><span class="sxs-lookup"><span data-stu-id="e204a-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="e204a-109">Pakoreguota bruto marža apskaičiuojama pagal toliau nurodytą formulę.</span><span class="sxs-lookup"><span data-stu-id="e204a-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="e204a-110">Jei bruto maržos ir pakoreguotos bruto maržos reikšmės stipriai skiriasi, didelė pasiūlymo darbų dalis klasifikuojama kaip neapmokestinama.</span><span class="sxs-lookup"><span data-stu-id="e204a-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="e204a-111">Kliento lūkesčių analizė</span><span class="sxs-lookup"><span data-stu-id="e204a-111">Analysis of customer expectations</span></span>

<span data-ttu-id="e204a-112">Jei įvedate toliau nurodytų laukų reikšmes, galite analizuoti pasiūlymus ir kurti kliento lūkesčių, susijusių su grafiku ir biudžetu, diagramas.</span><span class="sxs-lookup"><span data-stu-id="e204a-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="e204a-113">Laukas **Pageidaujama pristatymo data** pasiūlymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="e204a-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="e204a-114">Kiekvienos pasiūlymo eilutės (projektu pagrįstų eilučių ir produktu pagrįstų eilučių) laukas **Kliento biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="e204a-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="e204a-115">Kliento lūkesčių dėl grafiko analizė atliekama lyginant vėliausią pasiūlymo eilutės informacijos pabaigos datą su pageidaujama visų pasiūlymo eilučių pristatymo data.</span><span class="sxs-lookup"><span data-stu-id="e204a-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="e204a-116">Klientų lūkesčių dėl biudžeto analizė atliekama lyginant visą kliento biudžeto sumą su visų pasiūlymo eilučių pasiūlyta suma.</span><span class="sxs-lookup"><span data-stu-id="e204a-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
