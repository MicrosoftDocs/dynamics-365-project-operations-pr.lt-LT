---
title: Produktu pagrįsto pasiūlymo eilučių sudėtinių vienetų valdymas, pvz., pagal vartotoją ar pagal mėnesį – „Lite“ versija
description: Šioje temoje pateikiama informacija apie produktu pagrįstų pasiūlymo eilučių sudėtinių vienetų valdymą.
author: rumant
manager: Annbe
ms.date: 10/06/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4a075ae5a7329f241cc31afceab0e085c771f72
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272893"
---
# <a name="managing-complex-units-such-as-per-user-per-month-for-product-based-quote-lines---lite"></a><span data-ttu-id="10b84-103">Produktu pagrįsto pasiūlymo eilučių sudėtinių vienetų valdymas, pvz., pagal vartotoją ar pagal mėnesį – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="10b84-103">Managing complex units such as per-user, per-month for product-based quote lines - lite</span></span>

<span data-ttu-id="10b84-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="10b84-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="10b84-105">„Dynamics 365 Project Operations“ programoje naudojami kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas.</span><span class="sxs-lookup"><span data-stu-id="10b84-105">Dynamics 365 Project Operations uses quantity factors to support the sale of subscription-based products.</span></span> <span data-ttu-id="10b84-106">Prenumerata pagrįstiems produktams pasiūlymo arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.</span><span class="sxs-lookup"><span data-stu-id="10b84-106">For subscription-based products, the quantity on the quote or project contract line is expressed as the number of user-months.</span></span>

<span data-ttu-id="10b84-107">Paprastai prenumeratos programinės įrangos kaina kataloge yra kaina vienam vartotojui per mėnesį.</span><span class="sxs-lookup"><span data-stu-id="10b84-107">Usually, the price of subscription software is stored in the catalog as the price per user per month.</span></span> <span data-ttu-id="10b84-108">Per pardavimo procesą pasiūlymo eilutėje nurodyta kaina paprastai yra vienam vartotojui per mėnesį, dėl kurios susitarė ir nuolaidą pritaikė IT pardavimo agentas.</span><span class="sxs-lookup"><span data-stu-id="10b84-108">During the sales process, the price on the quote line is usually the per-user, per-month price that was negotiated and discounted by the IT sales agent.</span></span> <span data-ttu-id="10b84-109">Kiekvienas sandoris turi skirtingą vartotojų skaičių ir skirtingą prenumeratos mėnesių skaičių.</span><span class="sxs-lookup"><span data-stu-id="10b84-109">Each deal has a different number of users and a different number of subscription months.</span></span> <span data-ttu-id="10b84-110">Kiekis, naudojamas pasiūlymo eilutei apskaičiuoti, yra vartotojų skaičiaus ir prenumeratos mėnesių skaičiaus produktas.</span><span class="sxs-lookup"><span data-stu-id="10b84-110">The quantity used to compute the quote line is a product of the number of users and the number of subscription months.</span></span>

<span data-ttu-id="10b84-111">Norėdami paremti šį pardavimo tipą, „Project Operations“ pristatė kiekio koeficientų koncepciją.</span><span class="sxs-lookup"><span data-stu-id="10b84-111">To support this type of sale, Project Operations introduced the concept of quantity factors.</span></span> <span data-ttu-id="10b84-112">Kiekio koeficientai priklauso nuo „Dynamics 365“ produkto atributų.</span><span class="sxs-lookup"><span data-stu-id="10b84-112">Quantity factors rely on the product attributes in Dynamics 365.</span></span> <span data-ttu-id="10b84-113">Konfigūruojant konkrečias produkto ypatybes, „Project Operations“ leidžia žymėti pogrupį arba visas ypatybes kaip kiekio koeficientus.</span><span class="sxs-lookup"><span data-stu-id="10b84-113">When you configure specific properties for a product, Project Operations lets you flag a subset, or all of the properties, as quantity factors.</span></span>

<span data-ttu-id="10b84-114">„Project Operations“ tikrina, kad tik skaitinės ypatybės arba produkto, turinčio skaitinių duomenų tipą, ypatybės būtų žymimos kaip kiekio koeficientai.</span><span class="sxs-lookup"><span data-stu-id="10b84-114">Project Operations validates that only numeric properties or product properties that have a numeric data type are flagged as quantity factors.</span></span> <span data-ttu-id="10b84-115">Kai į pasiūlymo eilutę įtraukiate produktą su kiekio faktoriais, laukas **Kiekis** tampa tik skaitomu.</span><span class="sxs-lookup"><span data-stu-id="10b84-115">When you add a product with quantity factors to a quote line, the **Quantity** field becomes read-only.</span></span> <span data-ttu-id="10b84-116">Įvedus produktų ypatybių reikšmes, kurios yra kiekio koeficientai, „Project Operations“ apskaičiuoja pasiūlymo eilutės kiekį.</span><span class="sxs-lookup"><span data-stu-id="10b84-116">After you enter values for product properties that are quantity factors, Project Operations calculates the quantity of the quote line.</span></span>

<span data-ttu-id="10b84-117">Pavyzdžiui, „Dynamics 365 Sales“ gali turėti šias ypatybes:</span><span class="sxs-lookup"><span data-stu-id="10b84-117">For example, Dynamics 365 Sales might have the following properties:</span></span>

- <span data-ttu-id="10b84-118">**Vartotojų skaičius** – vartotojų skaičius</span><span class="sxs-lookup"><span data-stu-id="10b84-118">**No of users**: The number of users</span></span>
- <span data-ttu-id="10b84-119">**Mėnesių skaičius** – prenumeratos mėnesių skaičius</span><span class="sxs-lookup"><span data-stu-id="10b84-119">**No of Months**: The number of subscription months</span></span>
- <span data-ttu-id="10b84-120">**Produkto SKU**</span><span class="sxs-lookup"><span data-stu-id="10b84-120">**Product SKU**</span></span>

<span data-ttu-id="10b84-121">Galite vėliavėle pažymėti ypatybes **Vartotojų skaičius** ir **Mėnesių skaičius** kaip kiekio koeficientus redaguodami produkto eilutės ypatybes.</span><span class="sxs-lookup"><span data-stu-id="10b84-121">You can flag the **No of Users** and **No of Months** properties as quantity factors by editing the properties of the product line.</span></span>

<span data-ttu-id="10b84-122">Norėdami kurti produkto ypatybių kiekio koeficientus, atlikite šiuos veiksmus:</span><span class="sxs-lookup"><span data-stu-id="10b84-122">To create Quantity factors from Product properties, follow these steps:</span></span>

1. <span data-ttu-id="10b84-123">Kairiojoje „Project Operations“ naršymo srityje eikite į **Pardavimas** > **Produktai**.</span><span class="sxs-lookup"><span data-stu-id="10b84-123">On the Project Operations left navigation pane, go to **Sales** > **Products**.</span></span>
2. <span data-ttu-id="10b84-124">Atidarykite produktą, kuriam reikia konfigūruoti kiekio koeficientus.</span><span class="sxs-lookup"><span data-stu-id="10b84-124">Open the product for which you need to configure quantity factors.</span></span> <span data-ttu-id="10b84-125">Patikrinkite, ar produkto ypatybės jau sukonfigūruotos.</span><span class="sxs-lookup"><span data-stu-id="10b84-125">Make sure the product has properties already configured.</span></span>
3. <span data-ttu-id="10b84-126">Produkto puslapyje **Projekto informacija** pažymėkite skirtuką **Kiekio koeficientai**.</span><span class="sxs-lookup"><span data-stu-id="10b84-126">On the **Project Information** page for the Product, select the **Quantity Factors** tab.</span></span>
4. <span data-ttu-id="10b84-127">Antriniame tinklelyje pasirinkite **+ Naujo lauko apskaičiavimas**.</span><span class="sxs-lookup"><span data-stu-id="10b84-127">In the subgrid, select **+ New field computation**.</span></span>
5. <span data-ttu-id="10b84-128">Įveskite kiekio koeficiento pavadinimą ir pasirinkite ypatybės reikšmę, kuri susieja ją su lauko apskaičiavimu.</span><span class="sxs-lookup"><span data-stu-id="10b84-128">Enter the name of the Quantity factor and select the property value that maps to the field computation.</span></span>
6. <span data-ttu-id="10b84-129">Įrašykite ir uždarykite formą.</span><span class="sxs-lookup"><span data-stu-id="10b84-129">Save and close the form.</span></span> <span data-ttu-id="10b84-130">Pakartokite šiuos veiksmus su visomis ypatybėmis, kurias reikia naudoti produktu pagrįsto pasiūlymo eilutės kiekiui apskaičiuoti.</span><span class="sxs-lookup"><span data-stu-id="10b84-130">Repeat these steps for all properties to use for computing the quantity for the product-based quote line.</span></span>

<span data-ttu-id="10b84-131">Kai kuriate produkto produktu pagrįsto pasiūlymo eilutę, pasiūlymo eilutės kiekis bus užrakintas.</span><span class="sxs-lookup"><span data-stu-id="10b84-131">When you create a product-based quote line for a product, the quantity of the quote line will be locked.</span></span> <span data-ttu-id="10b84-132">Kiekis bus skaičiuojamas kaip ypatybių reikšmių, kurias įvedate tai pasiūlymo eilutei, produktas.</span><span class="sxs-lookup"><span data-stu-id="10b84-132">The quantity will be computed as a product of the property values that you input for that quote line.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]