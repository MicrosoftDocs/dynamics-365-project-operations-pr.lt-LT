---
title: „Dynamics 365 Project Operations“ šalinimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip pašalinti Dynamics 365 Project Operations.
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911974"
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
    | 9 | Field Service Common                                 | Reikalingas dvigubam rašymui su Dynamics 365 Finance arba Dynamics 365 Supply Chain Management.   |
    | 10 | msdyn_AssetCommon                                  | Reikalingas dvigubam rašymui su Dynamics 365 Finance arba Dynamics 365 Supply Chain Management.   |
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
