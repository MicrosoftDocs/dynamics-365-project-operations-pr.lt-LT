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
ms.openlocfilehash: 306f169ee25d42ac3c9e63fa70956b9c50315829
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122128"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a><span data-ttu-id="b18f2-103">Kodėl numatytoji faktinių duomenų išlaidų savikaina nustatoma kaip nulis?</span><span class="sxs-lookup"><span data-stu-id="b18f2-103">Why is the price defaulting to zero on expense cost actuals?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b18f2-104">Šie DUK taikomi faktiniams išlaidų duomenims, kai nustatyta operacijos klasė „Išlaidos“, o operacijos tipas „Savikaina“.</span><span class="sxs-lookup"><span data-stu-id="b18f2-104">This FAQ applies to expense actuals where the transaction class is set to Expense and transaction type is Cost.</span></span>

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a><span data-ttu-id="b18f2-105">Trikčių šalinimas – faktinių duomenų išlaidų savikainos tarifai</span><span class="sxs-lookup"><span data-stu-id="b18f2-105">Troubleshooting cost rates on expense cost actuals</span></span>

<span data-ttu-id="b18f2-106">Eikite į susijusį išlaidų įrašą ir įsitikinkite, kad išlaidų įvesties lauke yra suma.</span><span class="sxs-lookup"><span data-stu-id="b18f2-106">Go to the related expense entry and make sure that there’s an amount in the expense entry field.</span></span> <span data-ttu-id="b18f2-107">Jei pradinio išlaidų įrašo sumos laukas neužpildytas, nustatėte problemą.</span><span class="sxs-lookup"><span data-stu-id="b18f2-107">If the originating expense entry didn’t have the amount field filled, then you have isolated the problem.</span></span>
 
<span data-ttu-id="b18f2-108">Norėdami išspręsti šią problemą, iš naujo sukurkite išlaidų įrašą su tinkama suma ir patvirtinkite jį.</span><span class="sxs-lookup"><span data-stu-id="b18f2-108">To solve this problem, recreate the expense entry with a valid amount and approve it.</span></span>
