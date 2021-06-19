---
title: Fiksuotos kainos pajamų įvertinimo projektai
description: Šioje temoje pateikiama informacijos apie fiksuotos kainos pajamų naudojimą projektuose.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 639c6a104f2a90366a0f477c0d7cf384f19cdd81
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013811"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="cc48c-103">Fiksuotos kainos pajamų įvertinimo projektai</span><span class="sxs-lookup"><span data-stu-id="cc48c-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="cc48c-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="cc48c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="cc48c-105">Kai kuriate projekto sutarties eilutę naudodami toliau nurodytus atributus programoje „Dynamics 365 Project Operations“, esančioje „Microsoft Dataverse“, sistema automatiškai sukuria fiksuotos kainos pajamų įvertinimo projektą.</span><span class="sxs-lookup"><span data-stu-id="cc48c-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="cc48c-106">Šio projekto informacija pagrįsta toliau nurodytais elementais.</span><span class="sxs-lookup"><span data-stu-id="cc48c-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="cc48c-107">Fiksuotos kainos atsiskaitymo metodas.</span><span class="sxs-lookup"><span data-stu-id="cc48c-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="cc48c-108">Susietas projektas.</span><span class="sxs-lookup"><span data-stu-id="cc48c-108">An associated project.</span></span>
  - <span data-ttu-id="cc48c-109">Bent vienas etapas, apibrėžtas puslapio **Projekto sutarties eilutė** skirtuke **Sąskaitos faktūros grafikas**.</span><span class="sxs-lookup"><span data-stu-id="cc48c-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="cc48c-110">Fiksuotos kainos pajamų įvertinimo projektų peržiūra</span><span class="sxs-lookup"><span data-stu-id="cc48c-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="cc48c-111">Norėdami peržiūrėti fiksuotos kainos pajamų įvertinimo projektus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="cc48c-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="cc48c-112">„Dynamics 365 Finance“ aplinkoje eikite į **Projektų valdymas ir apskaita** > **Projektai** > **Fiksuotos kainos pajamų įvertinimo projektai**.</span><span class="sxs-lookup"><span data-stu-id="cc48c-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="cc48c-113">Pasirinkite projektą, kurį norite peržiūrėti, ir dukart spustelėkite **Vertinamo projekto ID**, kad atidarytumėte įrašą ir peržiūrėtumėte projekto informaciją.</span><span class="sxs-lookup"><span data-stu-id="cc48c-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="cc48c-114">Išplėskite skirtuką **Projektas**. Matysite vieną projektą tinklelyje **Pasirinkti projektai**.</span><span class="sxs-lookup"><span data-stu-id="cc48c-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="cc48c-115">Sistema naudoja jį kaip numatytąjį projektą, nes tai yra projektas, susietas su projekto sutarties eilute.</span><span class="sxs-lookup"><span data-stu-id="cc48c-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="cc48c-116">Norėdami pakeisti susiejimą, pasirinkite papildomus projektus ir pridėkite juos prie tinklelio **Pasirinkti projektai**.</span><span class="sxs-lookup"><span data-stu-id="cc48c-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="cc48c-117">Jei šiame tinklelyje pasirenkami keli projektai, projekto įvykdymo procentinė vertė ir pajamų įvertinimai apskaičiuojami kartu visiems pasirinktiems projektams.</span><span class="sxs-lookup"><span data-stu-id="cc48c-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="cc48c-118">Projekto išlaidas, pajamų profilį, sąnaudų šabloną ir laikotarpio kodą galima nustatyti rankiniu būdu.</span><span class="sxs-lookup"><span data-stu-id="cc48c-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="cc48c-119">Jei jie nenustatomi rankiniu būdu, nustatomos numatytosios reikšmės atliekant pirmąjį įvertinimo skaičiavimą remiantis sukonfigūruotomis projekto išlaidų ir pajamų profilių taisyklėmis.</span><span class="sxs-lookup"><span data-stu-id="cc48c-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]