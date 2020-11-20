---
title: Kodėl numatytoji faktinių duomenų laiko savikaina nustatoma kaip nulis?
description: Trikčių šalinimas klausimu kodėl numatytoji faktinių duomenų laiko savikaina nustatoma kaip 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
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
ms.openlocfilehash: 124719410f89dea506d43a1b64cb91c85d4f3968
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131383"
---
# <a name="why-is-the-price-defaulting-to-zero-on-time-cost-actuals"></a><span data-ttu-id="d87b0-103">Kodėl numatytoji faktinių duomenų laiko savikaina nustatoma kaip nulis?</span><span class="sxs-lookup"><span data-stu-id="d87b0-103">Why is the price defaulting to zero on time cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d87b0-104">Šie DUK taikomi faktiniams duomenims, kai nustatyta operacijos klasė „Laikas“, o operacijos tipas „Savikaina“.</span><span class="sxs-lookup"><span data-stu-id="d87b0-104">This FAQ applies to actuals where the transaction class is set to Time and transaction type is Cost.</span></span> <span data-ttu-id="d87b0-105">Šios trys patikros padės jums diagnozuoti triktis, susijusius su klausimu, kodėl faktinių duomenų laiko savikaina nustatoma kaip nulis.</span><span class="sxs-lookup"><span data-stu-id="d87b0-105">The following three checks will help you troubleshoot why the price is defaulting to 0 on time cost actuals.</span></span>
 
## <a name="check-1-identify-the-cost-price-list-for-the-project"></a><span data-ttu-id="d87b0-106">1 patikra: nustatykite projekto savikainos kainoraštį</span><span class="sxs-lookup"><span data-stu-id="d87b0-106">Check 1: Identify the cost price list for the project</span></span>

<span data-ttu-id="d87b0-107">Raskite projektą faktinių duomenų projekto lauke ir eikite į projekto puslapį.</span><span class="sxs-lookup"><span data-stu-id="d87b0-107">Find the project from the project field of the actual and then go to the project page.</span></span> <span data-ttu-id="d87b0-108">Lauke spustelėkite sutartį sudarančio vieneto nuorodą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-108">Click on the contracting unit link in the field.</span></span> <span data-ttu-id="d87b0-109">Sutartį sudarančio vieneto puslapyje, savikainos kainoraščių tinklelyje patikrinkite, ar sutartį sudarantis vienetas turi kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="d87b0-109">On the Contracting Unit page, check if the contracting unit has a price list in the Cost Price Lists grid.</span></span>

<span data-ttu-id="d87b0-110">Jei kainoraščių yra daugiau nei vienas, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-110">If there is more than one price list, you have isolated the problem.</span></span> <span data-ttu-id="d87b0-111">„Project Service“ programoje palaikomas tik vienas kainoraštis vienam organizacijos vienetui.</span><span class="sxs-lookup"><span data-stu-id="d87b0-111">Project Service only supports one price list per organizational unit.</span></span> <span data-ttu-id="d87b0-112">Šalinkite visus kainoraščius iš šio objekto tol, kol organizacijos vieneto savikainos kainoraščių tinklelyje liks tik vienas kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="d87b0-112">Remove all prices lists from this entity until there is only one price list attached in the Cost Price Lists grid of the Organizational Unit.</span></span>

<span data-ttu-id="d87b0-113">Jei prie organizacijos vieneto nėra prikabintų kainoraščių, pasižymėkite, kokia yra organizacijos vieneto valiuta.</span><span class="sxs-lookup"><span data-stu-id="d87b0-113">If there are no price lists attached to the Organizational Unit, make a note of the currency of the Organizational unit.</span></span> <span data-ttu-id="d87b0-114">Eikite į „Project Service“, pasirinkite Parametrai ir atidarykite skirtuką „Projekto kainoraščiai“. Patikrinkite ar yra kainoraščių, kurių kontekstas yra „Kaina“, o valiuta sutampa su organizacijos vieneto valiuta.</span><span class="sxs-lookup"><span data-stu-id="d87b0-114">Go to the Project Service and then Parameters and open the Price Lists tab. Check if there are any price lists with context set to Cost and currency that matches the currency of the Organizational Unit.</span></span>
 
<span data-ttu-id="d87b0-115">Jei kriterijus atitinkančių kainoraščių nėra, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-115">If there are no price lists that match that criteria, you have isolated the problem.</span></span> <span data-ttu-id="d87b0-116">Įsitikinkite, kad yra bent vienas kainoraštis, kurio kontekstas nustatytas kaip „Kaina“, ir kurio valiuta sutampa su organizacijos vieneto valiuta.</span><span class="sxs-lookup"><span data-stu-id="d87b0-116">Make sure to have at least one price list whose context is set to Cost and whose currency matches the currency of the Organizational Unit.</span></span>

<span data-ttu-id="d87b0-117">Jei šiuos kriterijus atitinkančių kainoraščių yra daugiau, skaitykite toliau ir atlikite kitas patikras.</span><span class="sxs-lookup"><span data-stu-id="d87b0-117">If there is more than one price list that match that criteria, continue reading this document to make more checks.</span></span>

## <a name="check-2-are-any-of-the-price-lists-identified-above-valid-for-the-specific-date-of-the-time-cost-actual"></a><span data-ttu-id="d87b0-118">2 patikra: ar anksčiau nurodyti kainoraščiai galioja konkrečiai faktinių duomenų laiko savikainos datai?</span><span class="sxs-lookup"><span data-stu-id="d87b0-118">Check 2: Are any of the price lists identified above valid for the specific date of the time cost actual?</span></span>

<span data-ttu-id="d87b0-119">Tam, kad „Project Service“ programoje būtų atsižvelgiama į kainoraštį, kai nustatoma numatytoji kaina, šis kainoraštis turi būti taikytinas faktinės savikainos laiko datai.</span><span class="sxs-lookup"><span data-stu-id="d87b0-119">For Project Service to consider a price list for defaulting price, that price list should be applicable for the date on the time cost actual.</span></span> <span data-ttu-id="d87b0-120">Tam, kad pamatytumėte, ar anksčiau nurodytas (-i) kainoraštis (-iai) yra taikytini, patikrinkite šiuos dalykus:</span><span class="sxs-lookup"><span data-stu-id="d87b0-120">Check the following to see if the price list(s) identified above are applicable:</span></span>

- <span data-ttu-id="d87b0-121">Patikrinkite, ar pradžios ir pabaigos datos įvestos pridėtų kainoraščių skirtuke „Bendra“.</span><span class="sxs-lookup"><span data-stu-id="d87b0-121">Check if the start and end dates on the general tab for the price lists attached aren’t empty.</span></span> <span data-ttu-id="d87b0-122">Jei pradžios ir pabaigos datos anksčiau nurodytuose kainoraščiuose neįvestos, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-122">If the start and end dates on price lists identified above are empty, you have isolated the problem.</span></span> 
- <span data-ttu-id="d87b0-123">Užsirašykite pradžios datą, esančią faktinių savikainos laiko duomenų lauke ir patikrinkite, ar nors vienas nurodytų kainoraščių tinka šiai datai.</span><span class="sxs-lookup"><span data-stu-id="d87b0-123">Make a note of the start date field on your time cost actual and check if any of the price lists identified is applicable for that date.</span></span> <span data-ttu-id="d87b0-124">Pavyzdžiui, faktinių savikainos laiko data turėtų atitikti laikotarpį nuo pradžios datos iki pabaigos datos, nurodytų kainoraštyje.</span><span class="sxs-lookup"><span data-stu-id="d87b0-124">For example, the date of the time cost actual should fall within the start date and end date on the price list.</span></span> 
    - <span data-ttu-id="d87b0-125">Jei nėra kainoraščio, atitinkančio datą, nurodytą faktiniuose savikainos laiko duomenyse, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-125">If there is no price list that covers that date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="d87b0-126">Pakeiskite kainoraščio pradžios ir pabaigos datas, užtikrindami, kad kainoraštis atitinka faktinių savikainos laiko duomenų datą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-126">Modify the start and end dates of the price list to ensure that the price list covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="d87b0-127">Jei yra daugiau nei vienas kainoraštis, atitinkantis faktinių savikainos laiko duomenų datą, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-127">If there is more than one price list that covers the date on the time cost actual, you have isolated the problem.</span></span> <span data-ttu-id="d87b0-128">Galite ją išspręsti pakeitę kainoraščio (-ių) pradžios ir pabaigos datas, kad būtų tik vienas kainoraštis, atitinkantis faktinių savikainos laiko duomenų datą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-128">You can fix this by editing the start and end dates of the price list(s) so that there is only one price list that covers the date of the time cost actual.</span></span> 
    - <span data-ttu-id="d87b0-129">Jei yra tik vienas kainoraštis, kuris apima faktinių savikainos laiko duomenų datą, pereikite prie kitos dokumento patikros.</span><span class="sxs-lookup"><span data-stu-id="d87b0-129">If there is only one price list that covers that date of the time cost actual, move to the next check in the document.</span></span>
<span data-ttu-id="d87b0-130">Atlikę reikiamus taisymus, iš naujo sukurkite laiko įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose savikainos laiko duomenyse rodoma tinkama kaina.</span><span class="sxs-lookup"><span data-stu-id="d87b0-130">Once you’ve done made the required fixes, recreate a time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>

## <a name="check-3-is-there-a-price-in-the-price-list-for-the-pricing-dimensions-on-the-time-cost-actual"></a><span data-ttu-id="d87b0-131">3 patikra: ar faktinių savikainos laiko duomenų kainodaros dimensijų kainoraštyje nurodyta kaina?</span><span class="sxs-lookup"><span data-stu-id="d87b0-131">Check 3: Is there a price in the price list for the pricing dimensions on the time cost actual?</span></span>

<span data-ttu-id="d87b0-132">Jei sėkmingai atlikote 1 ir 2 patikras, dabar turite tik vieną kainoraštį, taikytiną faktinių savikainos laiko duomenų datai.</span><span class="sxs-lookup"><span data-stu-id="d87b0-132">If you have successfully completed Check 1 and Check 2, you should now have only one price list that is applicable for the date of the time cost actual.</span></span> <span data-ttu-id="d87b0-133">Atidarykite šio projekto kainoraštį ir pereikite į skirtuką „Vaidmenų kainos“. Įsitikinkite, kad tinklelyje yra eilutė, skirta faktinių savikainos laiko duomenų kainodaros dimensijoms.</span><span class="sxs-lookup"><span data-stu-id="d87b0-133">Open this Price List and go to the Role Prices tab. Make sure that there is a row in the grid for the pricing dimensions on the time cost actual.</span></span>

<span data-ttu-id="d87b0-134">Jei faktinių savikainos laiko duomenų kainodaros dimensijų vaidmenų kainų tinklelyje nėra eilutės, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-134">If there is no row in the role price grid for the pricing dimensions on the time cost actual, then you have isolated the problem.</span></span> <span data-ttu-id="d87b0-135">Sukurkite eilutę faktinių savikainos laiko duomenų kainodaros dimensijų vaidmenų kainų tinklelyje.</span><span class="sxs-lookup"><span data-stu-id="d87b0-135">Create a row in the Role prices grid for the pricing dimensions on your time cost actual.</span></span> <span data-ttu-id="d87b0-136">Atlikę šį veiksmą, iš naujo sukurkite laiko įrašą, patvirtinkite jį ir patikrinkite, kad faktiniuose savikainos laiko duomenyse rodoma tinkama kaina.</span><span class="sxs-lookup"><span data-stu-id="d87b0-136">Once this is done, recreate time entry, approve it, and verify that the time cost actual shows a valid price.</span></span>
 
<span data-ttu-id="d87b0-137">Jei atlikote visas tris anksčiau minėtas patikras ir vis dar nematote tinkamos kainos faktiniuose savikainos laiko duomenyse, užregistruokite palaikymo kvitą.</span><span class="sxs-lookup"><span data-stu-id="d87b0-137">If you still don't see a valid price on your time cost actual after you’ve done the three checks above, please log a support ticket.</span></span>



