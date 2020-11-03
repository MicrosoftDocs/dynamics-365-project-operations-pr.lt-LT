---
title: Tiekėjo mokėjimo sulaikymo sąlygų kūrimas ir taikymas
description: Šioje temoje pateikta informacija apie tai, kaip nustatyti ir tvarkyti tiekėjo mokėjimų sulaikymo sąlygas.
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
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080973"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="be193-103">Tiekėjo mokėjimo sulaikymo sąlygų kūrimas ir taikymas</span><span class="sxs-lookup"><span data-stu-id="be193-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="be193-104">Projekto tiekėjo mokėjimų sulaikymo sąlygų nustatymas yra naudingas, kai jūsų organizacija nori sulaikyti tiekėjui atliktų mokėjimų dalį.</span><span class="sxs-lookup"><span data-stu-id="be193-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="be193-105">Pavyzdžiui, jei norite sulaikyti mokėjimą tiekėjui, kol pristatyti produktai atitiks jūsų lūkesčius.</span><span class="sxs-lookup"><span data-stu-id="be193-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="be193-106">Tariantis dėl tiekėjo sutarties, galima nurodyti tiekėjo mokėjimo sulaikymo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="be193-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="be193-107">Tiekėjo mokėjimo sulaikymo sąlygų kūrimas</span><span class="sxs-lookup"><span data-stu-id="be193-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="be193-108">Galite įvesti tiekėjo mokėjimo sulaikymo procentą ir anksčiau sulaikytų sumų, kurios dabar bus pervestos, procentą.</span><span class="sxs-lookup"><span data-stu-id="be193-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="be193-109">Sumos automatiškai sulaikomos tiekėjo sąskaitose faktūrose, kol sutarties būsena tampa užbaigta.</span><span class="sxs-lookup"><span data-stu-id="be193-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="be193-110">Nustatę sulaikymo sąlygas, galite jas taikyti bet kuriam to tiekėjo projektui.</span><span class="sxs-lookup"><span data-stu-id="be193-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="be193-111">Atlikite toliau nurodytus veiksmus, kad nustatytumėte ir tvarkytumėte tiekėjui atliekamų mokėjimų sulaikymo sąlygas.</span><span class="sxs-lookup"><span data-stu-id="be193-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="be193-112">Pasirinkite **Projektų valdymas ir apskaita** > **Sulaikymas** > **Tiekėjui atliekamų mokėjimų sulaikymo sąlygos**.</span><span class="sxs-lookup"><span data-stu-id="be193-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="be193-113">Pasirinkite **Naujas** , jei norite įtraukti naują tiekėjo sulaikymo sąlygą.</span><span class="sxs-lookup"><span data-stu-id="be193-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="be193-114">Naujos sąlygos lauko **Taisyklės ID** reikšmė įvedama automatiškai.</span><span class="sxs-lookup"><span data-stu-id="be193-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="be193-115">Įveskite trumpą aprašymą lauke **Aprašas** , o „FastTab“ **Sąlygos** pasirinkite **Įtraukti eilutę** ir įveskite šias sąlygų reikšmes.</span><span class="sxs-lookup"><span data-stu-id="be193-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="be193-116">**Pristatytų vienetų procentinė dalis** : įveskite sąlygos įvykdymo procentą.</span><span class="sxs-lookup"><span data-stu-id="be193-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="be193-117">Sumos automatiškai sulaikomos tiekėjo sąskaitose faktūrose, kol projekto baigimo etapas sutaps su nurodyta būsena.</span><span class="sxs-lookup"><span data-stu-id="be193-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="be193-118">Pavyzdžiui, jei įvesite 50,00, sumos sulaikomos tol, kol 50 % projekto bus baigta.</span><span class="sxs-lookup"><span data-stu-id="be193-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="be193-119">**Sulaikymo procentas** : įveskite tiekėjo sąskaitos faktūros sumos procentinę dalį, kuri bus sulaikyta.</span><span class="sxs-lookup"><span data-stu-id="be193-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="be193-120">Pavyzdžiui, jei įvesite 10,00, tada 10 procentų tiekėjo sąskaitos faktūros sumos bus sulaikyti, kol projektas pasieks baigimo procentą, nustatytą lauke **Pristatytų vienetų skaičius**.</span><span class="sxs-lookup"><span data-stu-id="be193-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="be193-121">**Išleidimo procentas** : pasirinkite **Įtraukti eilutę** ir įveskite bet kurių anksčiau sulaikytų sumų, kurios bus išliestos, pasirinkto projekto baigimo lygio procentą.</span><span class="sxs-lookup"><span data-stu-id="be193-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="be193-122">Jei skirtingiems projekto baigimo lygiams taikote daugiau nei vieną etapą, įveskite atskirą kiekvienos sulaikymo taisyklės tiekėjo sulaikymo sąlygos eilutę.</span><span class="sxs-lookup"><span data-stu-id="be193-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="be193-123">Kiekviena eilutė gali nurodyti skirtingą sulaikymo procentą ir skirtingą kiekvieno skirto projekto baigimo lygio procentą.</span><span class="sxs-lookup"><span data-stu-id="be193-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="be193-124">Sukūrę tiekėjo sulaikymo sąlygas, galite jas taikyti projektui.</span><span class="sxs-lookup"><span data-stu-id="be193-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="be193-125">Tiekėjo sulaikymo sąlygų taikymas projektui</span><span class="sxs-lookup"><span data-stu-id="be193-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="be193-126">Pasirinkite **Projektų valdymas ir apskaita** > **Projektai** > **Visi projektai** ir atidarykite projektą iš projektų sąrašo puslapio.</span><span class="sxs-lookup"><span data-stu-id="be193-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="be193-127">„FastTab“ **Tiekėjų sutartys** pasirinkite **Įtraukti eilutę**.</span><span class="sxs-lookup"><span data-stu-id="be193-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="be193-128">Lauke **Kliento kodas** pasirinkite vieną iš pateiktų parinkčių.</span><span class="sxs-lookup"><span data-stu-id="be193-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="be193-129">**Lentelė** : tiekėjo sulaikymo sąlygos taikomos vienam tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="be193-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="be193-130">**Grupė** : tiekėjo sulaikymo sąlygos taikomos visiems tiekėjams, priklausantiems tiekėjų grupei.</span><span class="sxs-lookup"><span data-stu-id="be193-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="be193-131">**Visi** : tiekėjo sulaikymo sąlygos taikomos visiems tiekėjams.</span><span class="sxs-lookup"><span data-stu-id="be193-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="be193-132">Lauke **Tiekėjas / tiekėjų grupė** pasirinkite tiekėją arba tiekėjų grupę, kuriai taikomos tiekėjo sulaikymo sąlygos.</span><span class="sxs-lookup"><span data-stu-id="be193-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="be193-133">Jei ankstesniame veiksme pasirinkote **Visi** , šis laukas nepasiekiamas.</span><span class="sxs-lookup"><span data-stu-id="be193-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="be193-134">Lauke **Tiekėjo sulaikymo sąlygos** pasirinkite sulaikymo sąlygas, kurias sukūrėte ankstesnėje procedūroje.</span><span class="sxs-lookup"><span data-stu-id="be193-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="be193-135">Jei projekte taip pat nustatytos tiekėjo „mokėjimo sumokėjus“ (PWP) sąlygos, įveskite ribinę projekto dalį lauke **PWP ribinės vertės procentas**.</span><span class="sxs-lookup"><span data-stu-id="be193-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="be193-136">Tiekėjo saugojimo sąlygos taip pat rodomos pardavimo užsakymuose, kuriuos kuriate tiekėjui.</span><span class="sxs-lookup"><span data-stu-id="be193-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
