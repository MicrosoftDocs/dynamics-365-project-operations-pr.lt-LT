---
title: Sukonfigūruokite grafiko lentą, kad būtų rodomi sutarties darbuotojai ir subrangos pajėgumas
description: Šiame straipsnyje aprašoma, kaip programoje „Microsoft Dynamics 365 Project Operations“ konfigūruoti grafiko lentą, kad būtų rodomas subrangos išteklių pajėgumas sudarant projekto išteklių reikalavimus.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 355691b63f437de789afab499369afcdf87e6d3d
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262227"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Sukonfigūruokite grafiko lentą, kad būtų rodomi sutarties darbuotojai ir subrangos pajėgumas 

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Grafiko lentą programoje „Microsoft Dynamics 365 Project Operations“ galima naudoti ištekliams ieškoti dviem būdais:

- Bendroji ieška, nenaudojant jokių konkrečių projektu pagrįstų išteklių reikalavimų konteksto.
- Išteklių ieška pagal konkretų reikalavimą, kai projekto reikalavimas suteiks siūlomų išteklių kontekstą.

Norėdami, kad grafiko lentai būtų pranešama apie subrangos išteklių pajėgumą ir pagal sutartis dirbančius darbuotojus, turite atnaujinti grafiko lentos parametrus. Atlikite šiuos atnaujinimus: 
- Atnaujinkite bendrosios išteklių ieškos grafiko lentos parametrus.
- Atnaujinkite išteklių ieškos pagal konkretų reikalavimą grafiko lentos parametrus.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Bendrosios išteklių ieškos grafiko lentos parametrų naujinimas
### <a name="update-filters-for-general-resource-search"></a>Bendrųjų išteklių ieškos filtrų naujinimas
Kai ieškote išteklių, grafiko lentoje esami filtrai turi būti atnaujinti taip, kad galėtumėte ieškoti ir išorinių išteklių, nurodant bet kurį arba visus šiuos dalykus:
  - Darbuotojo tipas, ar rodomi ištekliai turi būti pagal sutartį dirbantys darbuotojai, ar darbuotojai.
  - Tiekėjo įmonė, kuriai turėtų priklausyti ištekliai.
  - Ištekliai, kurie priklauso konkrečiai subrangos sutarčiai arba subrangos sutarties eilutei.
    
### <a name="update-retrieve-resource-query"></a>Išteklių gavimo užklausos naujinimas
Užklausą, naudojamą ieškai, taip pat reikia atnaujinti, kad būtų naudojami šie papildomi filtrų atributai. Norėdami atnaujinti bendrosios išteklių ieškos grafiko lentos konfigūraciją, atlikite šiuos veiksmus:  
1. Atidarykite **Grafiko lentos parametrus**, skirtus konkrečiai grafiko lentai.
2. Atidarykite skirtuką **Bendrieji parametrai** ir slinkite į **Kiti parametrai**.
3. Šio skyriaus parametrų sąraše atnaujinkite parinkties **Filtro maketas** reikšmę į **Numatytasis „Project Operations Lite" filtro maketas**.
4. Atnaujinkite parinkties **Išteklių gavimo užklausa** reikšmę į **Numatytoji „Project Operations Lite“ išteklių gavimo užklausa**.

![Bendrosios išteklių ieškos grafiko lentos parametrų naujinimas](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Išteklių ieškos pagal konkretų reikalavimą grafiko lentos parametrus naujinimas
### <a name="update-filters-for-requirement-specific-resource-search"></a>Išteklių ieškos pagal konkretų reikalavimą filtrų naujinimas 
Kai ieškote išteklių, grafiko lentoje esami filtrai turi būti atnaujinti taip, kad galėtumėte ieškoti ir išorinių išteklių, nurodant bet kurį arba visus šiuos dalykus:
 - Darbuotojo tipas, ar rodomi ištekliai turi būti pagal sutartį dirbantys darbuotojai, ar darbuotojai.
 - Tiekėjo įmonė, kuriai turėtų priklausyti ištekliai.
 - Ištekliai, kurie priklauso konkrečiai subrangos sutarčiai arba subrangos sutarties eilutei.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Išteklių ieškos pagal konkretų reikalavimą išteklių gavimo užklausos naujinimas 
Užklausą, naudojamą ieškai, taip pat reikia atnaujinti, kad būtų naudojami šie papildomi filtrų atributai. Norėdami atnaujinti išteklių ieškos pagal konkretų reikalavimą grafiko lentos konfigūraciją, atlikite šiuos veiksmus:

1. Atidarykite **Grafiko lentos parametrus**, skirtus konkrečiai grafiko lentai, tada pasirinkite **Atidaryti numatytuosius parametrus**, kad atidarytumėte ieškos pagal konkretų reikalavimą parametrus.
2. Atidarykite skirtuką **Bendrieji parametrai** ir slinkite į **Kiti parametrai**.
3. Šio skyriaus parametrų sąraše atnaujinkite parinkties **Filtro maketas** reikšmę į **Numatytasis „Project Operations Lite" filtro maketas**.
4. Atnaujinkite parinkties **Išteklių gavimo užklausa** reikšmę į **Numatytoji „Project Operations Lite“ išteklių gavimo užklausa**.
5. Atidarykite skirtuką **Grafiko tipai** ir eikite į **Projektas**.
6. **Projekto** parametrų dalyje atnaujinkite parinkties **Planavimo pagalbinės priemonės išteklių gavimo užklausa** reikšmę į **Numatytoji „Project Operations Lite“ išteklių gavimo užklausa**, o reikšmę **Planavimo pagalbinės priemonės apribojimų gavimo užklausa** į **Numatytoji „Project Operations Lite“ apribojimų gavimo užklausa**.

![Išteklių ieškos pagal konkretų reikalavimą grafiko lentos parametrus naujinimas](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
