---
title: Vidinės įmonės projekto SF išrašymo konfigūravimas
description: Šioje temoje parodyta, kaip nustatyti projekto SF išrašymą tarp dviejų jūsų organizacijos įmonių.
author: Yowelle
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: ad25aba492b7902ddd8955be87f88f96f6d4508f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001211"
---
# <a name="configure-intercompany-project-invoicing"></a><span data-ttu-id="f24f2-103">Vidinės įmonės projekto SF išrašymo konfigūravimas</span><span class="sxs-lookup"><span data-stu-id="f24f2-103">Configure intercompany project invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f24f2-104">Šioje temoje parodyta, kaip nustatyti projekto SF išrašymą tarp dviejų jūsų organizacijos įmonių.</span><span class="sxs-lookup"><span data-stu-id="f24f2-104">This topic shows how to set up project invoicing between two companies in your organization.</span></span> <span data-ttu-id="f24f2-105">Šiai užduočiai atlikti naudojamas USSI duomenų rinkinys.</span><span class="sxs-lookup"><span data-stu-id="f24f2-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="f24f2-106">Naršymo srityje eikite į **Moduliai > Mokėtinos sumos > Tiekėjai > Visi tiekėjai**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-106">In the navigation pane, go to **Modules > Accounts payable > Vendors > All vendors**.</span></span>
2. <span data-ttu-id="f24f2-107">Sąraše **Visi teikėjai** raskite ir pažymėkite norimą įrašą.</span><span class="sxs-lookup"><span data-stu-id="f24f2-107">In the **All vendors** list, find and select the desired record.</span></span>
3. <span data-ttu-id="f24f2-108">Veiksmų srityje pasirinkite **Bendri**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-108">On the Action Pane, select **General**.</span></span>
4. <span data-ttu-id="f24f2-109">Pažymėkite **Vidinė įmonė**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-109">Select **Intercompany**.</span></span>
5. <span data-ttu-id="f24f2-110">Nustatykite **Aktyvusis** kaip **Taip**, kad įgalintumėte vidinės įmonės prekybą.</span><span class="sxs-lookup"><span data-stu-id="f24f2-110">Set **Active** to **Yes** to enable intercompany trading.</span></span>
6. <span data-ttu-id="f24f2-111">Lauke **Kliento įmonė** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f24f2-111">In the **Customer company** field, enter or select a value.</span></span>
7. <span data-ttu-id="f24f2-112">Lauke **Mano klientas** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f24f2-112">In the **My account** field, enter or select a value.</span></span>
8. <span data-ttu-id="f24f2-113">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-113">Select **Save**.</span></span>
9. <span data-ttu-id="f24f2-114">Uždarykite puslapius, kad grįžtumėte į pagrindinį puslapį.</span><span class="sxs-lookup"><span data-stu-id="f24f2-114">Close the pages to return to the home page.</span></span>
10. <span data-ttu-id="f24f2-115">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Projektų valdymo ir apskaitos parametrai**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-115">In the navigation pane, go to **Modules > Project management and accounting > Setup > Project management and accounting parameters**.</span></span>
11. <span data-ttu-id="f24f2-116">Pažymėkite skirtuką **Vidinė įmonė**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-116">Select the **Intercompany** tab.</span></span>
12. <span data-ttu-id="f24f2-117">Perkelki slankiklį į **Taip**, kad įgalintumėte vidinės įmonės išteklių planavimą ir grafikus.</span><span class="sxs-lookup"><span data-stu-id="f24f2-117">Move the slider to **Yes** to enable intercompany resource scheduling and timesheets.</span></span>
13. <span data-ttu-id="f24f2-118">Sąraše pažymėkite pasirinktą eilutę.</span><span class="sxs-lookup"><span data-stu-id="f24f2-118">In the list, mark the selected row.</span></span>
14. <span data-ttu-id="f24f2-119">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-119">Select **New**.</span></span>
15. <span data-ttu-id="f24f2-120">Lauke **Besiskolinančio juridinio subjekto ID** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f24f2-120">In the **Borrowing legal entity** field, enter or select a value.</span></span>
16. <span data-ttu-id="f24f2-121">Pažymėkite žymės langelį **Kaupti pajamas**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-121">Select the **Accrue revenue** check box.</span></span>
17. <span data-ttu-id="f24f2-122">Lauke **Numatytoji grafiko kategorija** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f24f2-122">In the **Default timesheet category** field, enter or select a value.</span></span>
18. <span data-ttu-id="f24f2-123">Lauke **Numatytoji išlaidų kategorija** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f24f2-123">In the **Default expense category** field, enter or select a value.</span></span>
19. <span data-ttu-id="f24f2-124">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-124">Select **Save**.</span></span>
20. <span data-ttu-id="f24f2-125">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f24f2-125">Close the page.</span></span>
21. <span data-ttu-id="f24f2-126">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Registravimas > DK registravimo sąranka**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-126">In the navigation pane, go to **Modules > Project management and accounting > Setup > Posting > Ledger posting setup**.</span></span>
22. <span data-ttu-id="f24f2-127">Lauke **DK klientų tipai** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f24f2-127">In the **Ledger account types** field, select an option.</span></span>
23. <span data-ttu-id="f24f2-128">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-128">Select **New**.</span></span>
24. <span data-ttu-id="f24f2-129">Naujos eilutės lauke **Mano klientas** nurodykite pageidaujamas reikšmes.</span><span class="sxs-lookup"><span data-stu-id="f24f2-129">In the **Main account** field of the new row, specify the desired values.</span></span>
25. <span data-ttu-id="f24f2-130">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-130">Select **Save**.</span></span>
26. <span data-ttu-id="f24f2-131">Uždarykite puslapį.</span><span class="sxs-lookup"><span data-stu-id="f24f2-131">Close the page.</span></span>
27. <span data-ttu-id="f24f2-132">Naršymo srityje eikite į **Moduliai > Projektų valdymas ir apskaita > Sąranka > Kainos > Perkėlimo kaina**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-132">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Transfer price**.</span></span>
28. <span data-ttu-id="f24f2-133">Pasirinkite **Naujas**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-133">Select **New**.</span></span>
29. <span data-ttu-id="f24f2-134">Lauke **Įsigaliojimo data** įveskite datą.</span><span class="sxs-lookup"><span data-stu-id="f24f2-134">In the **Effective date** field, enter a date.</span></span>
30. <span data-ttu-id="f24f2-135">Lauke **Besiskolinančio juridinio subjekto ID** įveskite arba pasirinkite reikšmę.</span><span class="sxs-lookup"><span data-stu-id="f24f2-135">In the **Borrowing legal entity** field, enter or select a value.</span></span>
31. <span data-ttu-id="f24f2-136">Lauke **Perkėlimo kainos modelis** pažymėkite parinktį.</span><span class="sxs-lookup"><span data-stu-id="f24f2-136">In the **Transfer price model** field, select an option.</span></span>
32. <span data-ttu-id="f24f2-137">Lauke **Kaina** įveskite skaičių.</span><span class="sxs-lookup"><span data-stu-id="f24f2-137">In the **Pricing** field, enter a number.</span></span>
33. <span data-ttu-id="f24f2-138">Pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="f24f2-138">Select **Save**.</span></span>



[!INCLUDE[footer-include](../../includes/footer-banner.md)]