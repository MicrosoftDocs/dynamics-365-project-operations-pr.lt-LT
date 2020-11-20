---
title: Kodėl negalima panaikinti įrašų iš objekto Faktiniai duomenys?
description: Šioje temoje pateikiama informacija apie tai, kodėl negalima panaikinti įrašo iš faktinės reikšmės objekto.
author: JPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: b9b45e3ae0cd9273af4d2a5cd9cce30502c0aa78
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127168"
---
# <a name="why-cant-i-delete-records-from-the-actuals-entity"></a><span data-ttu-id="b3cad-103">Kodėl negalima panaikinti įrašų iš objekto Faktiniai duomenys?</span><span class="sxs-lookup"><span data-stu-id="b3cad-103">Why can’t I delete records from the Actuals entity?</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="b3cad-104">„Project Service Automation“ (PSA) neleidžia naikinti faktinių duomenų, nes jie kaip tiesos šaltiniai naudojami operacijoms, kurios turi finansinių sunkumų, kaip pvz., didžiajai knygai gauti.</span><span class="sxs-lookup"><span data-stu-id="b3cad-104">Project Service Automation (PSA) doesn't allow you to delete actuals because they serve as the source of truth for transactions that have financial implications to downstream systems, such as the general ledger.</span></span> <span data-ttu-id="b3cad-105">Jei faktiniai duomenys gali būti panaikinti, gali būti abejojama finansinių ataskaitų vientisumu.</span><span class="sxs-lookup"><span data-stu-id="b3cad-105">If actuals could be deleted, the integrity of the financial reporting transactions could be questioned.</span></span> <span data-ttu-id="b3cad-106">Norint nustatyti įrašo sekimą, klientai turėtų naudoti žurnalus, kad galėtų sukurti kompensacines operacijas.</span><span class="sxs-lookup"><span data-stu-id="b3cad-106">To establish an audit trail, customers should use journals to create compensating transactions.</span></span>

