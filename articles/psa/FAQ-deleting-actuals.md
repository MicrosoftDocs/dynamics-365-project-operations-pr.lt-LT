---
title: Kodėl negalima panaikinti įrašų iš objekto Faktiniai duomenys?
description: Šioje temoje pateikiama informacija apie tai, kodėl negalima panaikinti įrašo iš faktinės reikšmės objekto.
author: JPBurrows
ms.custom:
- dyn365-projectservice
ms.date: 11/6/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 434be93cedb4772616b1e6d5cbe15fc715eed19a
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993111"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="78150-103">Kodėl negalima panaikinti įrašų iš objekto Faktiniai duomenys?</span><span class="sxs-lookup"><span data-stu-id="78150-103">Why can’t I delete records from the Actuals entity?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="78150-104">„Project Service Automation“ (PSA) neleidžia naikinti faktinių duomenų, nes jie kaip tiesos šaltiniai naudojami operacijoms, kurios turi finansinių sunkumų, kaip pvz., didžiajai knygai gauti.</span><span class="sxs-lookup"><span data-stu-id="78150-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="78150-105">Jei faktiniai duomenys gali būti panaikinti, gali būti abejojama finansinių ataskaitų vientisumu.</span><span class="sxs-lookup"><span data-stu-id="78150-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="78150-106">Norint nustatyti įrašo sekimą, klientai turėtų naudoti žurnalus, kad galėtų sukurti kompensacines operacijas.</span><span class="sxs-lookup"><span data-stu-id="78150-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]