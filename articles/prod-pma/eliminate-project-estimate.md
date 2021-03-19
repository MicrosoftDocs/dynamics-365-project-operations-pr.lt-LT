---
title: Projekto įvertinimo šalinimas
description: Šioje temoje pateikta informacija apie užbaigto projekto įvertinimo pašalinimą.
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270688"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="44498-103">Projekto įvertinimo šalinimas</span><span class="sxs-lookup"><span data-stu-id="44498-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="44498-104">Projekto įvertinimai nurodomi finansiniame rodinyje to projekto darbo, kuris įvertintas ir suplanuotas.</span><span class="sxs-lookup"><span data-stu-id="44498-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="44498-105">Norėdami naudoti projekto įvertinimus, turite pridėti projektą prie įvertinimo projekto.</span><span class="sxs-lookup"><span data-stu-id="44498-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="44498-106">Įvertinimo projektas visada paremtas esamu projektu, tačiau keli projektai gali nurodyti vieną įvertinimo projektą.</span><span class="sxs-lookup"><span data-stu-id="44498-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="44498-107">Prie įvertinimo projektų galima pridėti tik fiksuotos kainos ir investicinius projektus, o tie projektai turi priklausyti tai pačiai projektų grupei kaip ir įvertinimo projektas.</span><span class="sxs-lookup"><span data-stu-id="44498-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="44498-108">Jei norite pašalinti įvertinamo projektą, jis turi būti užbaigtas.</span><span class="sxs-lookup"><span data-stu-id="44498-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="44498-109">Toliau aprašyti veiksmai paaiškina, kaip pašalinti įvertinimą.</span><span class="sxs-lookup"><span data-stu-id="44498-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="44498-110">Pasirinkite **Projektų valdymas ir apskaita** > **Visi projektai** ir atidarykite projektą.</span><span class="sxs-lookup"><span data-stu-id="44498-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="44498-111">Skirtuke **Tvarkyti** pasirinkite **Įvertinimai** ir puslapyje **Įvertinimas** pasirinkite **Šalinti**.</span><span class="sxs-lookup"><span data-stu-id="44498-111">On the **Manage** tab, select **Estimates**, and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="44498-112">Puslapio **Šalinti įvertinimą** skirtuke **Bendra** nustatykite toliau nurodytas parinktis.</span><span class="sxs-lookup"><span data-stu-id="44498-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="44498-113">**Laikotarpio kodas**: pasirinkite laikotarpio kodą, kad pasirinktumėte tinkamus įvertinimo projektus.</span><span class="sxs-lookup"><span data-stu-id="44498-113">**Period code**: Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="44498-114">**Įvertinimo data**: pasirinkite tinkamą įvertinimo šalinimo datą.</span><span class="sxs-lookup"><span data-stu-id="44498-114">**Estimate date**: Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="44498-115">**Šalinti su NG įspėjimais**: įjunkite šią parinktį norėdami pateikti pranešimą, kai pašalinamas įvertinimas, susietas su nebaigta gamyba (NG).</span><span class="sxs-lookup"><span data-stu-id="44498-115">**Eliminate with WIP warnings**: Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="44498-116">Kai ši parinktis neįjungta, pašalinimo tęsti negalima, jei yra neįvertintų operacijų.</span><span class="sxs-lookup"><span data-stu-id="44498-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="44498-117">Ši parinktis galima tik tada, kai šalinimas taikomas įvertinimo projektui.</span><span class="sxs-lookup"><span data-stu-id="44498-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="44498-118">Ji nepasiekiama, jei naudojate periodinius registravimus.</span><span class="sxs-lookup"><span data-stu-id="44498-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="44498-119">Šis parametras suderinamas su parametrais, esančiais puslapio **Projekto parametrai** skirtuke **Įvertinimas**, laukų grupėje **Leisti pašalinti, kai yra neįvertintų operacijų**.</span><span class="sxs-lookup"><span data-stu-id="44498-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="44498-120">**Nustatyti etapą kaip baigtą**: įjunkite šią parinktį, kad atlikus šalinimą būtų nustatytas įvertinimo projekto etapas **Baigtas**.</span><span class="sxs-lookup"><span data-stu-id="44498-120">**Set stage to Finished**: Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="44498-121">**Spausdinti įvertinimo sąrašą**: pasirinkite, kad informacija būtų įtraukta į spausdinamą įvertinimo sąrašą.</span><span class="sxs-lookup"><span data-stu-id="44498-121">**Print estimate list**: Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="44498-122">**Rodyti sistemos pranešimą**: įjunkite šią parinktį, kad būtų rodomas sistemos pranešimas.</span><span class="sxs-lookup"><span data-stu-id="44498-122">**Show Infolog**: Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="44498-123">**Registravimo data**: pasirinkite įvertinimo DK registravimo datą.</span><span class="sxs-lookup"><span data-stu-id="44498-123">**Posting date**: Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="44498-124">Pasirinkite **Gerai**.</span><span class="sxs-lookup"><span data-stu-id="44498-124">Select **OK**.</span></span>
5. <span data-ttu-id="44498-125">Baigus šalinimo procesą, pašalintas įvertinimo projektas rodomas su neigiama reikšme.</span><span class="sxs-lookup"><span data-stu-id="44498-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="44498-126">Jei neketinote panaikinti įvertinimo, galite pasirinkti pašalintus įvertinimus ir pasirinkti **Anuliuoti**.</span><span class="sxs-lookup"><span data-stu-id="44498-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   


[!INCLUDE[footer-include](../includes/footer-banner.md)]