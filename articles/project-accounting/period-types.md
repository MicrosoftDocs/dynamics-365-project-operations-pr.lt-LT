---
title: Laikotarpių tipai
description: Šioje temoje pateikiama informacijos, kaip tvarkyti pajamų įvertinimo laikotarpių tipus.
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013496"
---
# <a name="period-types"></a><span data-ttu-id="91d3c-103">Laikotarpių tipai</span><span class="sxs-lookup"><span data-stu-id="91d3c-103">Period types</span></span>

<span data-ttu-id="91d3c-104">_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_</span><span class="sxs-lookup"><span data-stu-id="91d3c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="91d3c-105">Laikotarpio tipas apibrėžia, kaip dažnai apskaičiuojamos projekto pajamos.</span><span class="sxs-lookup"><span data-stu-id="91d3c-105">A period type defines how frequently revenue on a project is estimated.</span></span> <span data-ttu-id="91d3c-106">Šioje temoje pateikiama informacijos, kaip tvarkyti pajamų įvertinimo laikotarpių tipus.</span><span class="sxs-lookup"><span data-stu-id="91d3c-106">This topic provides information about how to set up period types for revenue estimation.</span></span> 

## <a name="create-and-work-with-period-types"></a><span data-ttu-id="91d3c-107">Laikotarpių tipų kūrimas ir naudojimas</span><span class="sxs-lookup"><span data-stu-id="91d3c-107">Create and work with period types</span></span>
<span data-ttu-id="91d3c-108">Norėdami kurti ir naudoti laikotarpių tipus, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="91d3c-108">To create and work with period types, complete the following steps:</span></span>

1. <span data-ttu-id="91d3c-109">„Dynamics 365 Finance“ aplinkoje eikite į **Projektų valdymas ir apskaita** > **sąranka** > **Įvertinimai** > **Laikotarpių tipai**.</span><span class="sxs-lookup"><span data-stu-id="91d3c-109">In your Dynamics 365 Finance environment, go to **Project management and accounting** > **Setup** > **Estimates** > **Period types**.</span></span>
2. <span data-ttu-id="91d3c-110">Pasirinkite **Naujas**, kad sukurtumėte naują laikotarpio tipą.</span><span class="sxs-lookup"><span data-stu-id="91d3c-110">Select **New** to create new period type.</span></span> <span data-ttu-id="91d3c-111">Įveskite pavadinimą ir aprašą.</span><span class="sxs-lookup"><span data-stu-id="91d3c-111">Enter a name and description.</span></span>
3. <span data-ttu-id="91d3c-112">Lauke **Dažnumas** pasirinkite atitinkamą reikšmę.</span><span class="sxs-lookup"><span data-stu-id="91d3c-112">In the **Frequency** field, select a value:</span></span>

    - <span data-ttu-id="91d3c-113">Jei pasirinksite **Savaitė**, **Kas dvi savaites**, **Kas pusę mėnesio**, **Mėnuo**, **Diena**, **Ketvirtis** arba **Metai**, šie laikotarpiai bus generuojami remiantis kalendoriumi.</span><span class="sxs-lookup"><span data-stu-id="91d3c-113">If you select **Week**, **Bi-weekly**, **Semi-monthly**, **Month**, **Day**, **Quarter**, or **Year**, the calendar will be used to generate the periods.</span></span> 
    - <span data-ttu-id="91d3c-114">Jei pasirinksite **DK laikotarpis**, laikotarpiai bus generuojami remiantis DK laikotarpiais, sukonfigūruotais didžiojoje knygoje.</span><span class="sxs-lookup"><span data-stu-id="91d3c-114">If you select **Ledger period**, ledger periods from the General ledger configuration will be used to generate periods.</span></span>
    - <span data-ttu-id="91d3c-115">Jei pasirinksite **Neribotas**, galite nurodyti pasirinktinius laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="91d3c-115">If you select **Unlimited**, you can specify custom periods.</span></span>
4. <span data-ttu-id="91d3c-116">Pasirinkite laikotarpio tipo įrašą, tada pasirinkite **Generuoti laikotarpius**, kad sukurtumėte laikotarpius pagal laikotarpio tipą.</span><span class="sxs-lookup"><span data-stu-id="91d3c-116">Select the period type record and then select **Generate periods** to create periods for the period type.</span></span> <span data-ttu-id="91d3c-117">Atsižvelgiant į jūsų pasirinktą laikotarpio dažnumą, gali būti leidžiama nurodyti pradžios datą arba laikotarpių, kuriuos reikia sugeneruoti, skaičių.</span><span class="sxs-lookup"><span data-stu-id="91d3c-117">Based on the period frequency that you selected, you might have the option to specify a start date or the number of periods to generate.</span></span>
5. <span data-ttu-id="91d3c-118">Pasirinkite **Laikotarpiai**, kad peržiūrėtumėte sugeneruotus laikotarpius.</span><span class="sxs-lookup"><span data-stu-id="91d3c-118">Select **Periods** to review generated periods.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]