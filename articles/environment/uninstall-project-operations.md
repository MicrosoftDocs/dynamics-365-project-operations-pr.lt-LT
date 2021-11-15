---
title: „Dynamics 365 Project Operations“ šalinimas
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Operations“ pašalinimą.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b87c9324b1c95c10ef1e18b0fbf4572bdbe76827
ms.sourcegitcommit: b8b7a59eee7d93638446e93726d270316e45ab3d
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/10/2021
ms.locfileid: "7783653"
---
# <a name="uninstall-dynamics-365-project-operations"></a>„Dynamics 365 Project Operations“ šalinimas 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Jeigu norite pašalinti „Dynamics 365 Project Operations”, jums turi būti priskirtas administratoriaus vaidmuo.

1. Eikite į **Parametrai** > **Sprendimai**.

    ![Parametrų puslapis.](./media/uninstall-proj-ops-solutions.png)
  
2. Pašalinkite sprendimus tiksliai tokia tvarka, kokia jie išvardyti tolesnėje lentelėje. 

    | Veiksmas | Sprendimo pavadinimas                                    | Pastaba.                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 2 | ProjectOperations_Anchor                           | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 5 | ProjectService                                     | Papildomų pastabų nėra.                                                                         |
    | 6 | ProjectServiceCore_Patch                           | Papildomų pastabų nėra.                                                                         |
    | 7 | ProjectServiceCore                                 | Papildomų pastabų nėra.                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 9 | Field Service Common                                 | Privaloma, norint naudoti dvigubo rašymo funkciją programose „Dynamics 365 Finance” arba „Dynamics 365 Supply Chain Management”.   |
    | 10 | msdyn_AssetCommon                                  | Privaloma, norint naudoti dvigubo rašymo funkciją programose „Dynamics 365 Finance” arba „Dynamics 365 Supply Chain Management”.   |
    | 11 | msdyn_TESA_Anchor                                  | Privaloma „Dynamics 365 Field Service”.                                                     |
    | 12 | msdyn_TESA_Patch                                   | Privaloma „Dynamics 365 Field Service”.                                                     |
    | 13 | msdyn_TESA                                         | Privaloma „Dynamics 365 Field Service”.                                                     |
    | 14 | ResourceSchedulingControls                         | Privaloma „Dynamics 365 Field Service”.                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Privaloma „Dynamics 365 Field Service”.                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Privaloma „Dynamics 365 Field Service”.                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Privaloma „Dynamics 365 Field Service”.                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 19 | Dynamics365Notes                                   | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 21 | DualWriteCore                                      | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 22 | Dynamics365AssetManagementApp                      | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 23 | Dynamics365AssetManagement                         | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 25 | Dynamics365FinanceExtended                         | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 26 | HCMCommon                                          | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 28 | Šalis                                              | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 29 | Dynamics365Company                                 | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 30 | CurrencyExchangeRates                              | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
    | 31 | AssetCommon                                        | Jeigu neradote šio sprendimo, jį praleiskite.                                                            |
