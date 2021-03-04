---
title: Katalogo produktų savikainos ir pardavimo kainų sąranka – „Lite“ versija
description: Šioje temoje pateikta informacija, kaip nustatyti produktų kataloge esančių prekių savikainą ir pardavimo tarifus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5e851193df8151821e112e01a9f33df5afee7df7
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764566"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="b05e6-103">Katalogo produktų savikainos ir pardavimo kainų sąranka – „Lite“ versija</span><span class="sxs-lookup"><span data-stu-id="b05e6-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="b05e6-104">_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_</span><span class="sxs-lookup"><span data-stu-id="b05e6-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="b05e6-105">Produktų katalogo prekių kainodaros nustatymas programoje „Dynamics 365 Project Operations“ yra toks pat kaip ir programoje „Dynamics 365 Sales“.</span><span class="sxs-lookup"><span data-stu-id="b05e6-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="b05e6-106">Programoje „Project Operations“ produktų negalima įvertinti arba naudoti projektuose, todėl nereikia nustatyti produktų katalogo kainų pasiūlymų ir sutarčių projektų kainoraščiuose.</span><span class="sxs-lookup"><span data-stu-id="b05e6-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="b05e6-107">Norėdami nustatyti produktų katalogo kainas, naudokite pasiūlymo, sutarties arba sąskaitos lauką **Produkto kaina**.</span><span class="sxs-lookup"><span data-stu-id="b05e6-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="b05e6-108">Projekto kainoraštyje nenustatykite produktų katalogo kainų.</span><span class="sxs-lookup"><span data-stu-id="b05e6-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="b05e6-109">Projektų kainoraščiai yra nesuderinami su „Project Operations“.</span><span class="sxs-lookup"><span data-stu-id="b05e6-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="b05e6-110">Konkrečios programos verslo logika nukopijuoja kainoraščius iš pasiūlymo į sutartį.</span><span class="sxs-lookup"><span data-stu-id="b05e6-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="b05e6-111">Rezultatas – sutarčiai skirtas projekto kainoraštis.</span><span class="sxs-lookup"><span data-stu-id="b05e6-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="b05e6-112">Kopijavimo operacija gali atidėti pasiūlymo laimėjimo procesą, jei projekto kainoraštis pasiūlyme bus per didelis.</span><span class="sxs-lookup"><span data-stu-id="b05e6-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="b05e6-113">Produktų kainoraščiai nėra kopijuojami siekiant sutartyse sukurti pasirinktinius kainoraščius.</span><span class="sxs-lookup"><span data-stu-id="b05e6-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="b05e6-114">Kadangi kopijavimas neįtrauktas, pasiūlymo proceso našumas nepaveikiamas.</span><span class="sxs-lookup"><span data-stu-id="b05e6-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>
