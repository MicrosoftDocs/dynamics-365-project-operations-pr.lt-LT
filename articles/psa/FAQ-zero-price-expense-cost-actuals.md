---
title: Kodėl numatytoji faktinių duomenų išlaidų savikaina nustatoma kaip nulis?
description: Trikčių šalinimas – kodėl numatytoji faktinių duomenų išlaidų savikaina nustatoma kaip 0.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
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
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146358"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="27593-103">Kodėl numatytoji faktinių duomenų išlaidų savikaina nustatoma kaip nulis?</span><span class="sxs-lookup"><span data-stu-id="27593-103">Why is the price defaulting to zero on expense cost actuals</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="27593-104">Šie DUK taikomi faktiniams išlaidų duomenims, kai nustatyta operacijos klasė „Išlaidos“, o operacijos tipas „Savikaina“.</span><span class="sxs-lookup"><span data-stu-id="27593-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="27593-105">Trikčių šalinimas – faktinių duomenų išlaidų savikainos tarifai</span><span class="sxs-lookup"><span data-stu-id="27593-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="27593-106">Eikite į susijusį išlaidų įrašą ir įsitikinkite, kad išlaidų įvesties lauke yra suma.</span><span class="sxs-lookup"><span data-stu-id="27593-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="27593-107">Jei pradinio išlaidų įrašo sumos laukas neužpildytas, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="27593-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="27593-108">Norėdami išspręsti šią problemą, iš naujo sukurkite išlaidų įrašą su tinkama suma ir patvirtinkite jį.</span><span class="sxs-lookup"><span data-stu-id="27593-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
