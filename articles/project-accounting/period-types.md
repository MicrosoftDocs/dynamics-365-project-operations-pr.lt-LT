---
title: Laikotarpių tipai
description: Šioje temoje pateikiama informacijos, kaip tvarkyti pajamų įvertinimo laikotarpių tipus.
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 107cecbc1dabdf13147d847bf1816f44cc2703c5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287293"
---
# <a name="period-types"></a><span data-ttu-id="f9722-103">Laikotarpių tipai</span><span class="sxs-lookup"><span data-stu-id="f9722-103">Period types</span></span>

<span data-ttu-id="f9722-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="f9722-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="f9722-105">Laikotarpio tipas apibrėžia, kaip dažnai apskaičiuojamos projekto pajamos.</span><span class="sxs-lookup"><span data-stu-id="f9722-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="f9722-106">Šioje temoje pateikiama informacijos, kaip tvarkyti pajamų įvertinimo laikotarpių tipus.</span><span class="sxs-lookup"><span data-stu-id="f9722-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="f9722-107">Laikotarpių tipų kūrimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="f9722-107">Create and work with period types</span></span>
<span data-ttu-id="f9722-108">Norėdami kurti ir naudoti laikotarpių tipus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="f9722-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="f9722-109">„Dynamics 365 Finance“ aplinkoje eikite į **Projektų valdymas ir apskaita** > **sąranka** > **Įvertinimai** > **Laikotarpių tipai**.</span><span class="sxs-lookup"><span data-stu-id="f9722-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="f9722-110">Pasirinkite **Naujas**, kad sukurtumėte naują laikotarpio tipą.</span><span class="sxs-lookup"><span data-stu-id="f9722-110">Select **New** to create new period type.</span></span> <span data-ttu-id="f9722-111">Įveskite pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="f9722-111">Enter a name and description.</span></span>
3. <span data-ttu-id="f9722-112">Lauke **Dažnumas** pasirinkite atitinkamą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f9722-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="f9722-113">Jei pasirinksite **Savaitė**, **Kas dvi savaites**, **Kas pusę mėnesio**, **Mėnuo**, **Diena**, **Ketvirtis** arba **Metai**, šie laikotarpiai bus generuojami remiantis kalendoriumi.</span><span class="sxs-lookup"><span data-stu-id="f9722-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="f9722-114">Jei pasirinksite **DK laikotarpis**, laikotarpiai bus generuojami remiantis DK laikotarpiais, sukonfigūruotais didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="f9722-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="f9722-115">Jei pasirinksite **Neribotas**, galite nurodyti pasirinktinius laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="f9722-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="f9722-116">Pasirinkite laikotarpio tipo įrašą, tada pasirinkite **Generuoti laikotarpius**, kad sukurtumėte laikotarpius pagal laikotarpio tipą.</span><span class="sxs-lookup"><span data-stu-id="f9722-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="f9722-117">Atsižvelgiant į jūsų pasirinktą laikotarpio dažnumą, gali būti leidžiama nurodyti pradžios datą arba laikotarpių, kuriuos reikia sugeneruoti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="f9722-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="f9722-118">Pasirinkite **Laikotarpiai**, kad peržiūrėtumėte sugeneruotus laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="f9722-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]