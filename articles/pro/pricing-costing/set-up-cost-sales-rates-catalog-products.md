---
title: Katalogo produktų savikainos ir pardavimo tarifų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti produktų kataloge esančių prekių savikainą ir pardavimo tarifus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080903"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="2e215-103">Katalogo produktų savikainos ir pardavimo tarifų nustatymas</span><span class="sxs-lookup"><span data-stu-id="2e215-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="2e215-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="2e215-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="2e215-105">Produktų katalogo prekių kainodaros nustatymas naudojant „Dynamics 365 Project Operations“ yra toks pat, kaip ir naudojant „Dynamics 365 Sales“.</span><span class="sxs-lookup"><span data-stu-id="2e215-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="2e215-106">Kadangi produktų negalima įvertinti arba naudoti „Project Operations“ projektuose, produktų katalogo kainų nereikia nustatyti pasiūlymų ir sutarčių projektų kainoraščiuose.</span><span class="sxs-lookup"><span data-stu-id="2e215-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="2e215-107">Produktų katalogo kainos turėtų būti nustatomos pasiūlymo, sutarties arba kliento lauke **Produkto kaina**.</span><span class="sxs-lookup"><span data-stu-id="2e215-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="2e215-108">Šių objektų produktų katalogo kainų nenustatinėkite projektų kainoraščiuose.</span><span class="sxs-lookup"><span data-stu-id="2e215-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="2e215-109">Projektų kainoraščiai yra nesuderinami su „Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="2e215-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="2e215-110">Yra programai skirta verslo logika, kuri nukopijuoja kainoraščius iš pasiūlymo į sutartį.</span><span class="sxs-lookup"><span data-stu-id="2e215-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="2e215-111">Rezultatas – sutarčiai skirtas projekto kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="2e215-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="2e215-112">Kopijavimo operacija gali atidėti pasiūlymo laimėjimo procesą, jei projekto kainoraštis pasiūlyme bus per didelis.</span><span class="sxs-lookup"><span data-stu-id="2e215-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="2e215-113">Produktų kainoraščiai nėra kopijuojami siekiant sutartyse sukurti pasirinktinius kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="2e215-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="2e215-114">Tai reiškia, kad produktų kainoraščiai nedaro poveikio pasiūlymo laimėjimo proceso efektyvumui.</span><span class="sxs-lookup"><span data-stu-id="2e215-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
