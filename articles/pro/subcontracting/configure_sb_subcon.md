---
title: Konfigūruoti grafiko lentą, kad būtų rodomi sutartininkai ir subrangos pajėgumai
description: Šioje temoje aprašoma, kaip konfigūruoti "Microsoft" grafiko Dynamics 365 Project Operations lentą, kad dirbant projekto išteklių poreikius būtų rodomi subrangos išteklių pajėgumai.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: tonyafehr
ms.author: rumant
ms.openlocfilehash: d645dee741a45dcb0219e4e4f58a329b7b873e10
ms.sourcegitcommit: 45893132bd8bfaf944ee0ac855484684dd1ee945
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/09/2021
ms.locfileid: "7903060"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Konfigūruoti grafiko lentą, kad būtų rodomi sutartininkai ir subrangos pajėgumai 

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Planuoti lentą "Microsoft" Dynamics 365 Project Operations galima naudoti ieškant išteklių dviem būdais:

- Bendroji išteklių paieška be jokio konkretaus projektu pagrįsto ištekliaus poreikio konteksto.
- Konkrečių reikalavimų išteklių paieška, kai projekto reikalavimas suteiks siūlomų išteklių kontekstą.

Norėdami pranešti subrangos išteklių pajėgumų ir sutartininkų grafiko valdybai, turite atnaujinti grafiko valdybos parametrus. Šie naujinimai apima: 
- Naujinti grafiko lentos parametrus bendrajai išteklių ieškai.
- Naujinti planinės lentos parametrus, kad būtų galima ieškoti reikalavimais pagrįsto ištekliaus.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Naujinti grafiko lentos parametrus bendrajai išteklių ieškai
### <a name="update-filters-for-general-resource-search"></a>Atnaujinti bendrosios išteklių ieškos filtrus
Kai ieškote ištekliaus, grafiko lentoje esantys filtrai turi būti atnaujinti taip, kad taip pat galėtumėte ieškoti išorinių išteklių, nurodydami bet kurį iš šių elementų:
  - Darbuotojo tipas, ar rodomi ištekliai turėtų būti sutartininkai, ar darbuotojai.
  - Tiekėjo įmonė, kuriai turi priklausyti išteklius.
  - Ištekliai, priklausantys konkrečiai subrangos arba subrangos linijai.
    
### <a name="update-retrieve-resource-query"></a>Atnaujinti išteklių gavimo užklausą
Paieškai naudojama užklausa taip pat turėtų būti atnaujinta, kad būtų naudojami šie papildomi filtro atributai. Norėdami atnaujinti suvestinės lentos konfigūraciją bendrajai išteklių ieškai, atlikite šiuos veiksmus:  
1. Atidarykite **grafiko lentos parametrus konkrečiai grafiko** lentai.
2. Atidarykite **skirtuką Bendrieji parametrai** ir slinkite į Kiti **parametrai**.
3. Šio skyriaus parametrų sąraše atnaujinkite **filtro maketą** į **numatytąjį projekto operacijų lite filtro maketą**.
4. Naujinti **išteklių gavimo** užklausą į **numatytąją "Project Operations Lite" išteklių užklausą**.

![Naujinti grafiko lentos parametrus bendrajai išteklių ieškai](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Atnaujinti grafiko lentos parametrus, kad būtų galima ieškoti reikalavimu pagrįstų išteklių
### <a name="update-filters-for-requirement-specific-resource-search"></a>Atnaujinti konkrečių poreikių išteklių ieškos filtrus 
Kai ieškote ištekliaus, grafiko lentoje esantys filtrai turi būti atnaujinti taip, kad taip pat galėtumėte ieškoti išorinių išteklių, nurodydami bet kurį iš šių elementų:
 - Darbuotojo tipas, ar rodomi ištekliai turėtų būti sutartininkai, ar darbuotojai.
 - Tiekėjo įmonė, kuriai turi priklausyti išteklius.
 - Ištekliai, priklausantys konkrečiai subrangos arba subrangos linijai.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Atnaujinti išteklių užklausą, skirtą konkrečiai išteklių ieškai 
Paieškai naudojama užklausa taip pat turėtų būti atnaujinta, kad būtų naudojami šie papildomi filtro atributai. Norėdami atnaujinti reikalavimo pagrindu pagrįstos išteklių ieškos grafiko lentos konfigūraciją, atlikite šiuos veiksmus:

1. Atidarykite **Grafiko lentos parametrus konkrečiai grafiko** lentai, tada pasirinkite **Atidaryti numatytuosius** parametrus, kad atidarytumėte konkrečių reikalavimų ieškos parametrus.
2. Atidarykite **skirtuką Bendrieji parametrai** ir slinkite į Kiti **parametrai**.
3. Šio skyriaus parametrų sąraše atnaujinkite **filtro maketą** į **numatytąjį projekto operacijų lite filtro maketą**.
4. Naujinti **išteklių gavimo** užklausą į **numatytąją "Project Operations Lite" išteklių užklausą**.
5. Atidarykite **skirtuką Grafiko tipai** ir eikite į **Projektas**.
6. Dalyje Projekto parametrai **atnaujinkite** **planavimo pagalbinės informacijos išteklių** užklausą į **numatytąją "Project Operations Lite" išteklių užklausą** ir atnaujinkite **grafiko asistento gavimo apribojimų** užklausą į **numatytąją "Project Operations Lite" gavimo apribojimų užklausą**.

![Atnaujinti grafiko lentos parametrus, kad būtų galima ieškoti reikalavimu pagrįstų išteklių](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
