---
title: Pardavimo kainoraščio projekto perrašymas
description: Šioje temoje pateikiama informacija apie pasirinktinių pardavimo kainoraščių kūrimą.
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17a86e89f626cef720fe3c8db0cbd8d6a2a3ddd5
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275548"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="612de-103">Pardavimo kainoraščio projekto perrašymas</span><span class="sxs-lookup"><span data-stu-id="612de-103">Override project sales price lists</span></span>

<span data-ttu-id="612de-104">_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_</span><span class="sxs-lookup"><span data-stu-id="612de-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="612de-105">Konkrečiam klientui taikomi projekto kainoraščiai</span><span class="sxs-lookup"><span data-stu-id="612de-105">Customer-specific project price lists</span></span>

<span data-ttu-id="612de-106">Konkrečiam klientui taikomų kainų sutartys gali būti nustatytos kaip projekto kainoraščiai kliento įraše programoje „Dynamics 365 Project Operations”.</span><span class="sxs-lookup"><span data-stu-id="612de-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="612de-107">Norėdami nustatyti konkrečiam klientui taikomą projekto kainoraštį, srityje **Pardavimas** pereikite prie kliento įrašo.</span><span class="sxs-lookup"><span data-stu-id="612de-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="612de-108">Atidarykite sąrašo puslapį **Klientai**.</span><span class="sxs-lookup"><span data-stu-id="612de-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="612de-109">Raskite ir dukart spustelėkite kliento įrašą, kad atidarytumėte informacijos puslapį **Klientas**.</span><span class="sxs-lookup"><span data-stu-id="612de-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="612de-110">Skirtuke **Projekto kainoraščiai** pasirinkite **+ Naujas projekto kainoraštis**.</span><span class="sxs-lookup"><span data-stu-id="612de-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="612de-111">Puslapyje **Naujas projekto kainoraštis** išplečiamajame sąraše pasirinkite kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="612de-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="612de-112">Įtraukiami tik tie kainoraščiai, kurių kontekstas nustatytas kaip **Pardavimas** ir kurių valiuta atitinka kliento valiutą.</span><span class="sxs-lookup"><span data-stu-id="612de-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="612de-113">Suteikite sąsajai pavadinimą ir pasirinkite **Įrašyti**.</span><span class="sxs-lookup"><span data-stu-id="612de-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="612de-114">Konkrečiam klientui taikomas projekto kainoraštis sukurtas.</span><span class="sxs-lookup"><span data-stu-id="612de-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="612de-115">Šis kainoraštis bus naudojamas siekiant pagal numatytuosius nustatymus nustatyti projekto kainas projekto pasiūlymuose arba sutartyse, sukurtose šiam klientui, kai pasiūlymo arba projekto sutarties sukūrimo data patenka į kainoraščio galiojimo datų diapazoną.</span><span class="sxs-lookup"><span data-stu-id="612de-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="612de-116">Projekto pasiūlymų pasirinktinė kainodara</span><span class="sxs-lookup"><span data-stu-id="612de-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="612de-117">Projektų pasiūlymuose galite nustatyti projektų kainodarą, prasidedančią numatytuoju standartiniu kainoraščiu, kuris pagal numatytuosius nustatymus nustatomas naudojant kliento arba projekto parametrus.</span><span class="sxs-lookup"><span data-stu-id="612de-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="612de-118">Kai jums reikalinga pasirinktinė kainodara, skirta su projektu susijusiam darbui, esančiam konkrečiame pasiūlyme, galite gauti ją iš su projektu kainoraščiu susijusio objekto.</span><span class="sxs-lookup"><span data-stu-id="612de-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="612de-119">Atlikite toliau nurodytus veiksmus, kad nustatytumėte konkrečiam pasiūlymui taikomą projekto kainodarą.</span><span class="sxs-lookup"><span data-stu-id="612de-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="612de-120">Atidarykite projekto pasiūlymą ir pažymėkite skirtuką **Projekto kainoraščiai**.</span><span class="sxs-lookup"><span data-stu-id="612de-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="612de-121">Antriniame tinklelyje pasirinkite **Kurti pasirinktinę kainodarą**.</span><span class="sxs-lookup"><span data-stu-id="612de-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="612de-122">Visi projekto kainoraščiai, pridėti prie pasiūlymo, kopijuojami į naujus kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="612de-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="612de-123">Naujų kainoraščių pavadinimai perteikia pasiūlymo pavadinimą ir turi šių kainoraščių sukūrimo datos ir laiko žymą.</span><span class="sxs-lookup"><span data-stu-id="612de-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="612de-124">Galite naudoti visus šiuos kainoraščius ir atnaujinti darbo (vaidmens kaina) ir išlaidų (kategorijos kaina) kainas.</span><span class="sxs-lookup"><span data-stu-id="612de-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="612de-125">Šios kainos bus taikomos tik šiam projekto pasiūlymui.</span><span class="sxs-lookup"><span data-stu-id="612de-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="612de-126">Projekto sutartyje esantys kainoraščiai</span><span class="sxs-lookup"><span data-stu-id="612de-126">Price lists on a project contract</span></span>

<span data-ttu-id="612de-127">Projekto sutartyje numatytoji projekto kainodara visada yra pasirinktinis kainoraštis, kuriame nurodytas sutarties pavadinimas ir prie pavadinimo pridėta sukūrimo datos ir laiko žyma.</span><span class="sxs-lookup"><span data-stu-id="612de-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="612de-128">Tai taikytina ir kai sutartis buvo sukurta laimėjus pasiūlymą, ir kai sutartis buvo sukurta nuo pradžių.</span><span class="sxs-lookup"><span data-stu-id="612de-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="612de-129">Jei reikia, galite pašalinti šį susiejimą su pasirinktiniu kainoraščiu ir vietoj to susieti standartinį kainoraštį su projekto sutartimi.</span><span class="sxs-lookup"><span data-stu-id="612de-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="612de-130">Kai susiejate standartinį kainoraštį su projekto kainoraščiu pasiūlyme ar sutartyje, visi kainoraščio kainų pakeitimai turės įtakos visiems pasiūlymams ir sutartims, kurie naudoja šį kainoraštį.</span><span class="sxs-lookup"><span data-stu-id="612de-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]