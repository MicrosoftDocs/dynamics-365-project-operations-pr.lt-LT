---
title: Projekto būsenos sekimas
description: Kaip sekti projekto būseną „Project Service“
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 70d07c98bd9432712e939445dbf867b96642f5ba
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080922"
---
# <a name="track-a-projects-status-project-service"></a>Sekite projekto būseną („Project Service“)

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Naudodami „[!INCLUDE[pn_dyn_365_project_service_auto](../includes/pn-dyn-365-project-service-auto.md)]‟ galite sekti kliento projekto eigą.  

Bendravimui plėtojantis, projekto etapai atnaujinami, siekiant atspindėti bendravimo etapą.  


|              |                                                                                                                                                                                                                                                                                                  |
|--------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
|   **Naujas**    | Kuriant projektą, etapas nustatomas į **Naujas**. Jei projektą sukūrėte iš šablono, šiame etape projektas gali turėti grafiką, sąmatas ir komandos duomenis. Priešingu atveju tai bus projekto schema, ir jums reikės rankiniu būdu įvesti likusius projekto komponentus. |
|  **Pasiūlymas**   |      Kai projektą susiejate su pasiūlymu ar jį sukuriate iš pasiūlymo, projekto etapas nustatomas į **Pasiūlymas**, ir taip pat atnaujinamos numatomos pradžios bei pabaigos datos. Kai projektas yra pasiūlymo etape, pasiūlymo informacija rodoma **Projekto** puslapio skirtuke **Pardavimas**.      |
|   **Planas**   |                                     Kai laimite su projektu susietą pasiūlymą, ir kai bendravimas išsiplėtoja iki sutarties etapo, projekto etapas atnaujinamas į **Planas**. Sutarties informacija rodoma **Projekto** puslapio skirtuke **Pardavimas**.                                      |
| **Atlikti** |                    Kai projekto darbas baigtas, etapą galite nustatyti į **Baigtas**. Kai nustatytas baigtas projekto etapas, suprantama, kad darbas 100 proc. baigtas, bet projektas lieka atidarytas, kad būtų galima įrašyti laukimo laiko ar išlaidų įrašų.                     |
|  **Uždaryti**   |           Kai įrašytos visos projekto operacijos, ir nemanote, kad jų bus daugiau, etapą galite rankiniu būdu nustatyti į **Uždarytas**. Kai projektas nustatytas į **Uždarytas**, jame registruoti operacijų nebegalite, ir projektą bus galima tik skaityti.           |

## <a name="to-track-a-projects-status"></a>Norėdami sekti projekto būseną  

1.  Pasirinkite **Project Service > Projektai**.  

2.  Spustelėkite projektą, su kuriuo norite dirbti.  

3.  Juostoje ekrano viršuje pasirinkite žemyn nukreiptą rodyklę prie projekto pavadinimo, o tada spustelėkite **Projekto sekimas**.  

4.  Išplečiamajame sąraše, esančiame virš užduočių sąrašo, pasirinkite **Pastangų sekimas** arba **Išlaidų sekimas**.  

5.  Norėdami redaguoti bet kurią užduotį, ją dukart spustelėkite. Taip pat galite perkelti Ganto diagramos juostas ar keisti jų dydį, kad pakeistumėte užduoties trukmę ir eigą.  

### <a name="see-also"></a>Taip pat žr.  
 [Projekto vadovo vadovas](../psa/project-manager-guide.md)
