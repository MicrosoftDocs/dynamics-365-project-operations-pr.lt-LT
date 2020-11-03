---
title: Produktu pagrįstos galimybių eilutės
description: Šioje temoje pateikta informacija apie produktu pagrįstų galimybės eilučių elementus „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080762"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="209bb-103">Produktu pagrįstos galimybių eilutės</span><span class="sxs-lookup"><span data-stu-id="209bb-103">Product-based opportunity lines</span></span>

<span data-ttu-id="209bb-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="209bb-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="209bb-105">Produktu pagrįstos galimybės eilutės yra eilutės elementai.</span><span class="sxs-lookup"><span data-stu-id="209bb-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="209bb-106">Šios eilutės pristatomos klientui kaip atskiri eilutės elementai galutinėje sąskaitoje faktūroje be jokių kitų pridėtinės vertės paslaugų.</span><span class="sxs-lookup"><span data-stu-id="209bb-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="209bb-107">Susijusio projekto užduočių susijusios išlaidos ir vartojimas nėra sekamas.</span><span class="sxs-lookup"><span data-stu-id="209bb-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="209bb-108">Produktu pagrįstos eilutės gali būti katalogo elementai arba įtraukiamieji produktai.</span><span class="sxs-lookup"><span data-stu-id="209bb-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="209bb-109">Dauguma galimybės naudojant produktu pagrįstas eilutes funkcijų atitinka funkcijas, esančias „Dynamics 365 Sales“ programoje.</span><span class="sxs-lookup"><span data-stu-id="209bb-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="209bb-110">Daugiau informacijos apie produktu pagrįstos galimybės eilutes žr. [Produktų įtraukimas į galimybę](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span><span class="sxs-lookup"><span data-stu-id="209bb-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="209bb-111">Viena sąvoka apie produktu pagrįstų galimybių eilutes, būdingas projektu pagrįstomis galimybėmis, yra **Kliento biudžetas**.</span><span class="sxs-lookup"><span data-stu-id="209bb-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="209bb-112">Šiame lauke galite sekti sumą, kurią klientas nori mokėti už eilutės elementą.</span><span class="sxs-lookup"><span data-stu-id="209bb-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="209bb-113">Jei galimybės suvestinės pajamų metodas nustatytas kaip **Sistema apskaičiuota** , kliento biudžeto reikšmės visose produktu ir projektu pagrįstose eilutėse yra apibendrintos, kad būtų galima apskaičiuoti numatomas pajamas.</span><span class="sxs-lookup"><span data-stu-id="209bb-113">If the revenue method of the Opportunity summary is set to **System Calculated** , the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
