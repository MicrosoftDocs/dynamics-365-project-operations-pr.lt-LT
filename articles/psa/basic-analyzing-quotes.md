---
title: Projekto pasiūlymų analizė
description: Šioje temoje pateikiama informacija apie projekto pasiūlymų analizę.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 361a940261811467c46222c3d58c9504434ec882
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5145233"
---
# <a name="analysis-of-project-quotes"></a><span data-ttu-id="27fe8-103">Projekto pasiūlymų analizė</span><span class="sxs-lookup"><span data-stu-id="27fe8-103">Analysis of project quotes</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="27fe8-104">„Dynamics 365 Project Service Automation“ analizuoja projekto pasiūlymus ir įvertina jų pelningumą.</span><span class="sxs-lookup"><span data-stu-id="27fe8-104">Dynamics 365 Project Service Automation analyzes project quotes to estimate profitability.</span></span> <span data-ttu-id="27fe8-105">Ji taip pat analizuoja, kiek pasiūlymas atitinka kliento lūkesčius dėl pristatymo datos arba įvykdymo datos ir biudžeto.</span><span class="sxs-lookup"><span data-stu-id="27fe8-105">It also analyzes how well the quote is aligned with customer expectations about the delivery date or completion date, and about the budget.tions.</span></span>

## <a name="profitability-analysis"></a><span data-ttu-id="27fe8-106">Pelningumo analizė</span><span class="sxs-lookup"><span data-stu-id="27fe8-106">Profitability analysis</span></span>

<span data-ttu-id="27fe8-107">Programos „Project Service Automation“ vykdomai pelningumo analizei naudojama bruto marža ir pakoreguota bruto marža.</span><span class="sxs-lookup"><span data-stu-id="27fe8-107">Project Service Automation analyzes profitability by using the gross margin and the adjusted gross margin.</span></span>

- <span data-ttu-id="27fe8-108">Bruto maržos apskaičiuojamos pagal toliau nurodytą formulę.</span><span class="sxs-lookup"><span data-stu-id="27fe8-108">Gross margins are calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- <span data-ttu-id="27fe8-109">Pakoreguota bruto marža apskaičiuojama pagal toliau nurodytą formulę.</span><span class="sxs-lookup"><span data-stu-id="27fe8-109">The adjusted gross margin is calculated by using the following formula:</span></span>

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

<span data-ttu-id="27fe8-110">Jei bruto maržos ir pakoreguotos bruto maržos reikšmės stipriai skiriasi, didelė pasiūlymo darbų dalis klasifikuojama kaip neapmokestinama.</span><span class="sxs-lookup"><span data-stu-id="27fe8-110">If the values for gross margin and adjusted gross margin differ by a wide margin, much of the work in the quote is classified as non-chargeable.</span></span>

## <a name="analysis-of-customer-expectations"></a><span data-ttu-id="27fe8-111">Kliento lūkesčių analizė</span><span class="sxs-lookup"><span data-stu-id="27fe8-111">Analysis of customer expectations</span></span>

<span data-ttu-id="27fe8-112">Jei įvedate toliau nurodytų laukų reikšmes, galite analizuoti pasiūlymus ir kurti kliento lūkesčių, susijusių su grafiku ir biudžetu, diagramas.</span><span class="sxs-lookup"><span data-stu-id="27fe8-112">You can analyze quotes and generate charts for customer expectations about the schedule and budget if you enter values for the following fields:</span></span>

- <span data-ttu-id="27fe8-113">Laukas **Pageidaujama pristatymo data** pasiūlymo antraštėje.</span><span class="sxs-lookup"><span data-stu-id="27fe8-113">The **Requested delivery date** field on the quote header.</span></span>
- <span data-ttu-id="27fe8-114">Kiekvienos pasiūlymo eilutės (projektu pagrįstų eilučių ir produktu pagrįstų eilučių) laukas **Kliento biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="27fe8-114">The **Customer budget** field for each quote line (for project-based lines and product-based lines).</span></span>

<span data-ttu-id="27fe8-115">Kliento lūkesčių dėl grafiko analizė atliekama lyginant vėliausią pasiūlymo eilutės informacijos pabaigos datą su pageidaujama visų pasiūlymo eilučių pristatymo data.</span><span class="sxs-lookup"><span data-stu-id="27fe8-115">Analysis of customer expectations about the schedule is done by comparing the latest end date of the quote line detail with the requested delivery date across all quote lines in the quote.</span></span>

<span data-ttu-id="27fe8-116">Klientų lūkesčių dėl biudžeto analizė atliekama lyginant visą kliento biudžeto sumą su visų pasiūlymo eilučių pasiūlyta suma.</span><span class="sxs-lookup"><span data-stu-id="27fe8-116">Analysis of customer expectations about the budget is done by comparing the sum of the total customer budget with the quoted amount across all quote lines.</span></span>
