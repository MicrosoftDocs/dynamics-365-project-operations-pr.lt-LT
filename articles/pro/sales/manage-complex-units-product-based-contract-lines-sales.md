---
title: Produktu pagrįstų sutarties eilučių sudėtinių vienetų valdymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip palaikomas prenumeruojamų produktų pardavimas.
author: rumant
ms.date: 10/28/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 86da5a96919438e883b56fc8ecfe765f70a789ff
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003191"
---
# <a name="manage-complex-units-for-product-based-contract-lines---lite"></a><span data-ttu-id="72d09-103">Produktu pagrįstų sutarties eilučių sudėtinių vienetų valdymas – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="72d09-103">Manage complex units for product-based contract lines - lite</span></span>

<span data-ttu-id="72d09-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="72d09-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="72d09-105">„Dynamics 365 Project Operations“ programoje naudojami kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas.</span><span class="sxs-lookup"><span data-stu-id="72d09-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="72d09-106">Prenumerata pagrįstiems produktams sutarties arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.</span><span class="sxs-lookup"><span data-stu-id="72d09-106">For subscription-based products, the quantity on the contract or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="72d09-107">Prenumeruojamos programinės įrangos kaina kataloge saugoma kaip kaina vienam vartotojui per mėnesį.</span><span class="sxs-lookup"><span data-stu-id="72d09-107">The price of subscription software is stored in the catalog as the price per-user, per-month.</span></span> <span data-ttu-id="72d09-108">Pardavimo proceso metu sutarties eilutėje nurodyta kaina paprastai yra vienam vartotojui per mėnesį, dėl kurios susitarė ir kuriai nuolaidą pritaikė pardavimo agentas.</span><span class="sxs-lookup"><span data-stu-id="72d09-108">During the sales process, the price on the contract line is usually the per-user, per-month price that was negotiated and discounted by the sales agent.</span></span> <span data-ttu-id="72d09-109">Kiekvienas sandoris turi skirtingą vartotojų skaičių ir skirtingą prenumeratos mėnesių skaičių.</span><span class="sxs-lookup"><span data-stu-id="72d09-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="72d09-110">Kiekis, naudojamas sutarties eilutės sumai apskaičiuoti, yra vartotojų skaičiaus ir prenumeratos mėnesių skaičiaus sandauga.</span><span class="sxs-lookup"><span data-stu-id="72d09-110">The quantity used to calculate the amount of the contract line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="72d09-111">Kad būtų palaikomas šis pardavimo tipas, „Project Operations“ palaiko *kiekio koeficientų* koncepciją.</span><span class="sxs-lookup"><span data-stu-id="72d09-111">To support this type of sale, Project Operations supports the concept of *quantity factors*.</span></span> <span data-ttu-id="72d09-112">Kiekio koeficientai priklauso nuo produkto atributų.</span><span class="sxs-lookup"><span data-stu-id="72d09-112">Quantity factors rely on product attributes.</span></span> <span data-ttu-id="72d09-113">Konfigūruojant konkrečias produkto ypatybes, galite žymėti tų ypatybių pogrupį arba visas ypatybes kaip kiekio koeficientus.</span><span class="sxs-lookup"><span data-stu-id="72d09-113">When you configure specific properties for a product, you can flag a subset of those properties, or all the properties, as quantity factors.</span></span>

<span data-ttu-id="72d09-114">„Project Operations“ tikrina, kad tik skaitinės ypatybės arba produkto, turinčio skaitinių duomenų tipą, ypatybės būtų žymimos kaip kiekio koeficientai.</span><span class="sxs-lookup"><span data-stu-id="72d09-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="72d09-115">Kai į sutarties eilutę įtraukiamas produktas su sukonfigūruotais kiekio koeficientais, laukas **Kiekis** tampa tik skaitomas.</span><span class="sxs-lookup"><span data-stu-id="72d09-115">When a product with configured quantity factors is added to a contract line, the **Quantity** field  becomes read-only.</span></span> <span data-ttu-id="72d09-116">Įvedus produktų ypatybių reikšmes, kurios yra kiekio koeficientai, „Project Operations“ apskaičiuoja sutarties eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="72d09-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the contract line.</span></span>

<span data-ttu-id="72d09-117">Pavyzdžiui, „Dynamics 365 Sales“ gali turėti šias ypatybes:</span><span class="sxs-lookup"><span data-stu-id="72d09-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="72d09-118">**Vartotojų skaičius** – vartotojų skaičius.</span><span class="sxs-lookup"><span data-stu-id="72d09-118">**No of users**: The number of users.</span></span>
- <span data-ttu-id="72d09-119">**Mėnesių skaičius** – prenumeratos mėnesių skaičius.</span><span class="sxs-lookup"><span data-stu-id="72d09-119">**No of Months**: The number of subscription months.</span></span>
- <span data-ttu-id="72d09-120">**Produkto SKU**: produkto sandėliavimo vienetas (SKU).</span><span class="sxs-lookup"><span data-stu-id="72d09-120">**Product SKU**: The stock keeping unit (SKU) for the product.</span></span>

<span data-ttu-id="72d09-121">Ypatybės **Vartotojų skaičius** ir **Mėnesių skaičius** gali būti pažymėtos kaip kiekio koeficientai redaguojant produkto eilutės ypatybes.</span><span class="sxs-lookup"><span data-stu-id="72d09-121">The **No of Users** and **No of Months** properties can be flagged as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="72d09-122">Norėdami kiekio koeficientus kurti pagal produktų ypatybes, atlikite toliau nurodytus veiksmus.</span><span class="sxs-lookup"><span data-stu-id="72d09-122">To create quantity factors from product properties, complete the following steps.</span></span>

1. <span data-ttu-id="72d09-123">Programoje **„Project Operations“** pasirinkite **Pardavimo produktai**.</span><span class="sxs-lookup"><span data-stu-id="72d09-123">On the **Project Operations**, select **Sales-Products**.</span></span>
2. <span data-ttu-id="72d09-124">Atidarykite produktą, kuriam reikia nustatyti kiekio koeficientus.</span><span class="sxs-lookup"><span data-stu-id="72d09-124">Open the product for which you need to set up quantity factors.</span></span> <span data-ttu-id="72d09-125">Įsitikinkite, kad produkto ypatybės jau nustatytos.</span><span class="sxs-lookup"><span data-stu-id="72d09-125">Make sure that the product has properties already set up.</span></span>
3. <span data-ttu-id="72d09-126">Puslapyje **Projekto informacija** pasirinkite skirtuką **Kiekio koeficientai**.</span><span class="sxs-lookup"><span data-stu-id="72d09-126">On the **Project Information** page, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="72d09-127">Antriniame tinklelyje pasirinkite **+ Naujo lauko apskaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="72d09-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="72d09-128">Įveskite **kiekio koeficiento** pavadinimą ir pasirinkite ypatybės reikšmę, kuri susieja ją su lauko apskaičiavimu.</span><span class="sxs-lookup"><span data-stu-id="72d09-128">Enter the name of the **Quantity Factor** and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="72d09-129">Įrašykite ir uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="72d09-129">Save and close the form.</span></span>
7. <span data-ttu-id="72d09-130">Pakartokite 2–6 veiksmus su visomis ypatybėmis, kurios kartu sudarys su produktais susijusios sutarties eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="72d09-130">Repeat steps 2-6 for all the properties that together will make up the quantity for the product-based contract line.</span></span>

<span data-ttu-id="72d09-131">Kai, nustatęs kiekio koeficientus, vartotojas sukuria šio produkto sutarties eilutę, jos kiekis yra užrakinamas.</span><span class="sxs-lookup"><span data-stu-id="72d09-131">With quantity factors set up, when the user creates a contract line for this product, the quantity of the contract line is locked.</span></span> <span data-ttu-id="72d09-132">Tada kiekis apskaičiuojamas kaip tos sutarties eilutės ypatybių reikšmių sandauga.</span><span class="sxs-lookup"><span data-stu-id="72d09-132">The quantity is then calculated as a product of the property values for that contract line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]