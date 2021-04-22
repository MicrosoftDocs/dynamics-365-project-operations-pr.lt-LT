---
title: Projekto atsiskaitymo nebaigtų užduočių valdymas
description: Šioje temoje pateikiama informacija apie įvairius galimus naudoti rodinius valdant projektų nebaigtas užduotis.
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 25dc9cff6aeb6daed9a27ba843a74b892ca4751c
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867006"
---
# <a name="manage-project-billing-backlog"></a><span data-ttu-id="f9f82-103">Projekto atsiskaitymo nebaigtų užduočių valdymas</span><span class="sxs-lookup"><span data-stu-id="f9f82-103">Manage project billing backlog</span></span> 

<span data-ttu-id="f9f82-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="f9f82-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f9f82-105">„Dynamics 365 Project Operations“ programoje yra specialieji rodiniai, kad būtų lengviau tvarkyti nebaigtas atsiskaitymo užduotis.</span><span class="sxs-lookup"><span data-stu-id="f9f82-105">Dynamics 365 Project Operations has dedicated views to help manage the billing backlog.</span></span> <span data-ttu-id="f9f82-106">Norėdami tvarkyti nebaigtas atsiskaitymo užduotis, pasirinkite saitus dalies **Atsiskaitymas** srityje **Pardavimas**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-106">To manage the billing backlog, select the links in the **Sales** area, under **Billing**.</span></span> 

<span data-ttu-id="f9f82-107">Yra tolesni rodiniai.</span><span class="sxs-lookup"><span data-stu-id="f9f82-107">The following views available:</span></span>

- <span data-ttu-id="f9f82-108">Išankstiniai apmokėjimai ir avansai</span><span class="sxs-lookup"><span data-stu-id="f9f82-108">Retainers and Advances</span></span>
- <span data-ttu-id="f9f82-109">Galimi išankstiniai apmokėjimai ir avansai</span><span class="sxs-lookup"><span data-stu-id="f9f82-109">Available Retainers and Advances</span></span>
- <span data-ttu-id="f9f82-110">Fiksuotos kainos gairės</span><span class="sxs-lookup"><span data-stu-id="f9f82-110">Fixed Price Milestones</span></span>
- <span data-ttu-id="f9f82-111">Produktų atsiskaitymo nebaigtos užduotys</span><span class="sxs-lookup"><span data-stu-id="f9f82-111">Product Billing Backlog</span></span>
- <span data-ttu-id="f9f82-112">Laiko ir medžiagų atsiskaitymo nebaigtos užduotys</span><span class="sxs-lookup"><span data-stu-id="f9f82-112">Time and Material Billing Backlog</span></span>

## <a name="retainers-and-advances"></a><span data-ttu-id="f9f82-113">Išankstiniai apmokėjimai ir avansai</span><span class="sxs-lookup"><span data-stu-id="f9f82-113">Retainers and Advances</span></span>

<span data-ttu-id="f9f82-114">Rodinyje **Išankstiniai apmokėjimai ir avansai** išvardyti visi išankstiniai apmokėjimai ir avansai, esantys visose sistemos projektų sutartyse.</span><span class="sxs-lookup"><span data-stu-id="f9f82-114">The **Retainers and Advances** view lists all the retainers and advances across all project contracts in the system.</span></span> <span data-ttu-id="f9f82-115">Kai išrašoma sąskaita faktūra už išankstinį apmokėjimą ar avansą, avanso suma tampa pasiekiama naudoti.</span><span class="sxs-lookup"><span data-stu-id="f9f82-115">After a retainer or advance is invoiced, the amount of the advance becomes available to use.</span></span>

## <a name="available-retainers-and-advances"></a><span data-ttu-id="f9f82-116">Galimi išankstiniai apmokėjimai ir avansai</span><span class="sxs-lookup"><span data-stu-id="f9f82-116">Available Retainers and Advances</span></span>

<span data-ttu-id="f9f82-117">Rodinyje **Galimi išankstiniai apmokėjimai ir avansai** išvardyti visi galimi išankstiniai apmokėjimai ir avansai, esantys visose sistemos projektų sutartyse.</span><span class="sxs-lookup"><span data-stu-id="f9f82-117">The **Available Retainers and Advances** view lists all available retainers and advances across all project contracts in the system.</span></span> <span data-ttu-id="f9f82-118">Kai išrašoma sąskaita faktūra už išankstinį apmokėjimą ar avansą, avanso suma tampa pasiekiama naudoti ir yra įtraukiama į sąrašą.</span><span class="sxs-lookup"><span data-stu-id="f9f82-118">After a retainer or advance is invoiced, the amount of the advance becomes available to use and is added to the list.</span></span> <span data-ttu-id="f9f82-119">Visiškai išnaudojus išankstinio apmokėjimo ar avanso sumą, ji pašalinama iš sąrašo.</span><span class="sxs-lookup"><span data-stu-id="f9f82-119">After the amount of the retainer or advance is used completely, it is removed from the list.</span></span>

## <a name="fixed-price-milestones"></a><span data-ttu-id="f9f82-120">Fiksuotos kainos gairės</span><span class="sxs-lookup"><span data-stu-id="f9f82-120">Fixed Price Milestones</span></span>

<span data-ttu-id="f9f82-121">Rodinyje **Fiksuotos kainos etapai** išvardyti visi fiksuotos kainos etapai, esantys visose sistemos projekto sutarties eilutėse.</span><span class="sxs-lookup"><span data-stu-id="f9f82-121">The **Fixed Price Milestones** view lists all fixed price milestones across all project contract lines in the system.</span></span> <span data-ttu-id="f9f82-122">Vieną ar kelis etapus šiame rodinyje galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-122">Single or multiple milestones can be marked as **Ready to invoice** or **Not ready to invoice** from this view.</span></span> <span data-ttu-id="f9f82-123">Etapą pažymėjus **Parengta išrašyti sąskaitą faktūrą**, jį galima įdėti į sąskaitos faktūros juodraštį.</span><span class="sxs-lookup"><span data-stu-id="f9f82-123">Marking a milestone as **Ready to invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="f9f82-124">Kai kelių klientų sutarties eilutėse taikomas fiksuotos kainos atsiskaitymo metodas, etapas sukuriamas kiekvienam sutarties eilutės klientui.</span><span class="sxs-lookup"><span data-stu-id="f9f82-124">When multi-customer contract lines have a fixed price billing method, a milestone is created for each customer on the contract line.</span></span> <span data-ttu-id="f9f82-125">Sukūrus etapą, ji galima išskaidyti į atskirus konkrečiam klientui taikomus etapų įrašus.</span><span class="sxs-lookup"><span data-stu-id="f9f82-125">A milestone can be created and then split into individual customer-specific milestone records.</span></span> <span data-ttu-id="f9f82-126">Šis išskaidymas yra vidinis ir atitinka sąskaitų išrašymo procentinę dalį, apibrėžtą kiekvienam sutarties eilutės klientui.</span><span class="sxs-lookup"><span data-stu-id="f9f82-126">This split is internal and in accordance with the billing percentage split defined for each customer on the contract line.</span></span> <span data-ttu-id="f9f82-127">Rodinyje **Fiksuotos kainos etapai** matysite atskirus konkrečiam klientui skirtus etapų įrašus.</span><span class="sxs-lookup"><span data-stu-id="f9f82-127">In the **Fixed Price Milestones** view, you will see the individual customer-specific milestone records.</span></span> <span data-ttu-id="f9f82-128">Kiekvienas iš šių etapų įrašų gali būti pažymėtas kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio.</span><span class="sxs-lookup"><span data-stu-id="f9f82-128">Each of these milestone records can be marked as **Ready to Invoice** separately from this view.</span></span> <span data-ttu-id="f9f82-129">Kai vienas ar daugiau susijusių etapų išskaidymų pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**, antraštės būsena iš **Nepradėta** atnaujinama į **Vykdoma**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-129">When one or more of the related milestone splits are marked as **Ready to Invoice**, the header status is updated to **In Progress** from **Not Started**.</span></span> <span data-ttu-id="f9f82-130">Kai sąskaita faktūra išrašoma visiems išskaidytiems etapams, antraštės etapo būsena atnaujinama į **Baigta**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-130">When all of the milestone splits are invoiced, the header milestone status is updated to **Completed**.</span></span>

<span data-ttu-id="f9f82-131">Šiame rodinyje rodomas sąskaitos faktūros juodraščio etapas su atsiskaitymo būsena **Kliento sąskaita faktūra sukurta**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-131">A milestone on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="f9f82-132">Patvirtinus sąskaitos faktūros juodraštį, įrašo sąskaitų išrašymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-132">When the draft invoice is confirmed, the billing status on the record is updated to **Customer Invoice Posted**.</span></span> <span data-ttu-id="f9f82-133">Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą.</span><span class="sxs-lookup"><span data-stu-id="f9f82-133">Don't update this status value by using custom code.</span></span> <span data-ttu-id="f9f82-134">Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.</span><span class="sxs-lookup"><span data-stu-id="f9f82-134">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>

## <a name="product-billing-backlog"></a><span data-ttu-id="f9f82-135">Produktų atsiskaitymo nebaigtos užduotys</span><span class="sxs-lookup"><span data-stu-id="f9f82-135">Product Billing Backlog</span></span>

<span data-ttu-id="f9f82-136">Rodinyje **Nebaigtos atsiskaitymo už produktus užduotys** išvardytos visos su produktais susijusios sutarties eilutės, esančios visose sistemos projektų sutartyse.</span><span class="sxs-lookup"><span data-stu-id="f9f82-136">The **Product Billing Backlog** view lists all product-based contract lines across all project contracts in the system.</span></span> <span data-ttu-id="f9f82-137">Vieną ar kelias su produktais susijusias sutarčių eilutes šiame rodinyje galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-137">Single or multiple product-based contract lines can be marked as **Ready to Invoice** or **Not Ready to Invoice** from this view.</span></span> <span data-ttu-id="f9f82-138">Su produktais susijusią sutarties eilutę pažymėjus **Parengta išrašyti sąskaitą faktūrą**, ją galima įdėti į sąskaitos faktūros juodraštį.</span><span class="sxs-lookup"><span data-stu-id="f9f82-138">Marking a product-based contract line as **Ready to Invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="f9f82-139">Su produktais susijusi sutarties eilutė, esanti sąskaitos faktūros juodraštyje, šiame rodinyje rodoma nustačius būseną **Kliento sąskaita faktūra sukurta**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-139">A product-based contract line that is on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="f9f82-140">Patvirtinus sąskaitos faktūros juodraštį, šio įrašo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-140">When the draft invoice is confirmed, the billing status on this record is updated to **Customer Invoice Posted**.</span></span> <span data-ttu-id="f9f82-141">Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą.</span><span class="sxs-lookup"><span data-stu-id="f9f82-141">Don't update this status value by using custom code.</span></span> <span data-ttu-id="f9f82-142">Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.</span><span class="sxs-lookup"><span data-stu-id="f9f82-142">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>

## <a name="time-and-material-billing-backlog"></a><span data-ttu-id="f9f82-143">Laiko ir medžiagų atsiskaitymo nebaigtos užduotys</span><span class="sxs-lookup"><span data-stu-id="f9f82-143">Time and Material Billing Backlog</span></span>

<span data-ttu-id="f9f82-144">Rodinyje **Nebaigtos atsiskaitymo už laiką ir medžiagas užduotys** išvardyti visi pardavimų, už kuriuos neatsiskaityta, faktiniai duomenys, esantys visose sistemos projektų sutartyse, kurioms neišrašyta sąskaita faktūra.</span><span class="sxs-lookup"><span data-stu-id="f9f82-144">The **Time and Material Billing Backlog** view lists all unbilled sales actuals across all project contracts in the system that haven't been invoiced.</span></span> <span data-ttu-id="f9f82-145">Vieną ar kelias neapmokestinto pardavimo sumas galima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą** arba **Neparengta išrašyti sąskaitos faktūros** iš šio rodinio.</span><span class="sxs-lookup"><span data-stu-id="f9f82-145">Single or multiple unbilled sales actuals can be marked as **Ready to Invoice** or **Not Ready to Invoice** from this view.</span></span> <span data-ttu-id="f9f82-146">Pažymėjus neapmokestinto pardavimo faktines sumas kaip **Parengta išrašyti sąskaitą faktūrą**, jas galima įtraukti į sąskaitą faktūrą.</span><span class="sxs-lookup"><span data-stu-id="f9f82-146">Marking an unbilled sales actual as **Ready to Invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="f9f82-147">Faktinių pardavimo, už kurį neatsiskaityta, duomenų, kurių **Neviršyti** būsena yra **Nepavyko**, negalima pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-147">Unbilled sales actuals with a **Not-to-Exceed** status of **Failed** can't be marked as **Ready to Invoice**.</span></span> <span data-ttu-id="f9f82-148">Jei faktinius duomenis reikia pažymėti kaip **Parengta išrašyti sąskaitą faktūrą**, iš naujo nustatykite kitų paskirtų faktinių duomenų būseną sutarties eilutėje.</span><span class="sxs-lookup"><span data-stu-id="f9f82-148">If the actuals need to be marked as **Ready to Invoice**, reset the status on other actuals on the contract line that are committed.</span></span> <span data-ttu-id="f9f82-149">tada iš naujo įvertinkite **Neviršyti** būseną.</span><span class="sxs-lookup"><span data-stu-id="f9f82-149">and then reevaluate the **Not-to-Exceed** status.</span></span>

<span data-ttu-id="f9f82-150">Jei kelių klientų sutarčių eilutėse taikomas atsiskaitymo už laiką ir medžiagas metodas, patvirtinant laiką ir išlaidas, kiekvienam sutarties eilutės klientui pagal sutarties atsiskaitymo procento išskaidymą, apibrėžtą kiekvienam klientui, sukuriamas pardavimo, už kurį neatsiskaityta, duomuo.</span><span class="sxs-lookup"><span data-stu-id="f9f82-150">If multi-customer contract lines have a time and material billing method, when time and expenses are approved, one unbilled sales actual is created for each customer on the contract line according to the billing percentage split defined for each of the customers.</span></span> <span data-ttu-id="f9f82-151">Rodinyje **Nebaigtos atsiskaitymo už laiką ir medžiagas užduotys** matysite šiuos atskirus konkretiems klientams taikomus pardavimo, už kurį neatsiskaityta, faktinius duomenis.</span><span class="sxs-lookup"><span data-stu-id="f9f82-151">In the **Time and Material Billing Backlog** view, you will see these individual customer-specific unbilled sales actuals.</span></span> <span data-ttu-id="f9f82-152">Kiekviena iš šių neapmokestinto pardavimo sumų gali būti pažymėta kaip **Parengta išrašyti sąskaitą faktūrą** atskirai nuo šio rodinio.</span><span class="sxs-lookup"><span data-stu-id="f9f82-152">Each of these unbilled sales actual records can be marked as **Ready to Invoice** separately from this view.</span></span>

<span data-ttu-id="f9f82-153">Pardavimo, už kurį neatsiskaityta, faktinis duomuo, esantis sąskaitos faktūros juodraštyje, šiame rodinyje rodomas nustačius būseną **Kliento sąskaita faktūra sukurta**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-153">An unbilled sales actual that is on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="f9f82-154">Patvirtinus sąskaitos faktūros juodraštį, šio įrašo atsiskaitymo būsena atnaujinama į **Kliento sąskaita faktūra užregistruota**.</span><span class="sxs-lookup"><span data-stu-id="f9f82-154">When the draft invoice is confirmed, the billing status on this record is updated to **Customer Invoice Posted**.</span></span> <span data-ttu-id="f9f82-155">Neatnaujinkite šios būsenos reikšmės naudodami pasirinktinį kodą.</span><span class="sxs-lookup"><span data-stu-id="f9f82-155">Don't update this status value using custom code.</span></span> <span data-ttu-id="f9f82-156">Kai šios būsenos reikšmės atnaujinamos naudojant pasirinktinį kodą, „Project Operations“ veikia netinkamai.</span><span class="sxs-lookup"><span data-stu-id="f9f82-156">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]