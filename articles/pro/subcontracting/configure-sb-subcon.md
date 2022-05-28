---
title: Sukonfigūruokite grafiko lentą, kad būtų rodomi sutarties darbuotojai ir subrangos pajėgumas
description: Šioje temoje aprašoma, kaip konfigūruoti planavimo lentą programoje "Microsoft" Dynamics 365 Project Operations, kad būtų rodomi subrangovų išteklių pajėgumai, kai įdarbinami projekto išteklių poreikiai.
author: rumant
ms.date: 08/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6e382b33fafe91c8b96a91d033fe12b998114bdc
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8587840"
---
# <a name="configure-schedule-board-to-show-contract-workers-and-subcontracted-capacity"></a>Sukonfigūruokite grafiko lentą, kad būtų rodomi sutarties darbuotojai ir subrangos pajėgumas 

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Planavimo lenta programoje "Microsoft" Dynamics 365 Project Operations gali būti naudojama išteklių paieškai dviem būdais:

- Bendroji išteklių paieška be jokio konkretaus projektinio išteklių poreikio konteksto.
- Konkretaus poreikio išteklių ieška, kurioje projekto reikalavimas pateiks siūlomų išteklių kontekstą.

Norėdami pranešti grafiko lentai apie subrangovų išteklių pajėgumus ir sutartininkus, turite atnaujinti grafiko lentos parametrus. Šie naujinimai apima: 
- Atnaujinti bendrosios išteklių ieškos grafiko lentos parametrus.
- Atnaujinti poreikiu pagrįstos išteklių ieškos grafiko lentos parametrus.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Atnaujinti bendrosios išteklių ieškos grafiko lentos parametrus
### <a name="update-filters-for-general-resource-search"></a>Atnaujinti bendrosios išteklių ieškos filtrus
Kai ieškote ištekliaus, grafiko lentoje esantys filtrai turėtų būti atnaujinti, kad taip pat galėtumėte ieškoti išorinių išteklių, nurodydami bet kurį arba visus šiuos dalykus:
  - Darbuotojo tipas, ar rodomi ištekliai turi būti sutartininkai, ar darbuotojai.
  - Tiekėjo įmonė, kuriai turėtų priklausyti išteklius.
  - Ištekliai, priklausantys konkrečiai subrangos arba subrangos eilutei.
    
### <a name="update-retrieve-resource-query"></a>Atnaujinti išteklių nuskaitymo užklausą
Ieškai naudojama užklausa taip pat turėtų būti atnaujinta, kad būtų galima naudoti šiuos papildomus filtro atributus. Norėdami atnaujinti bendrosios išteklių ieškos grafiko lentos konfigūraciją, atlikite šiuos veiksmus:  
1. Atidarykite **konkrečios grafiko lentos parametrus** konkrečiai grafiko lentai.
2. Atidarykite skirtuką **Bendrieji parametrai** ir slinkite į **Kiti parametrai**.
3. Šio skyriaus parametrų sąraše atnaujinkite **filtro maketą** į **Numatytąjį "Project Operations Lite**" filtro maketą.
4. Atnaujinkite **gauti išteklių užklausą** į numatytąją **"Project Operations Lite" išteklių nuskaitymo užklausą**.

![Atnaujinti bendrosios išteklių ieškos grafiko lentos parametrus](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Atnaujinti poreikiu pagrįstos išteklių ieškos grafiko lentos parametrus
### <a name="update-filters-for-requirement-specific-resource-search"></a>Atnaujinti konkretaus poreikio išteklių ieškos filtrus 
Kai ieškote ištekliaus, grafiko lentoje esantys filtrai turėtų būti atnaujinti, kad taip pat galėtumėte ieškoti išorinių išteklių, nurodydami bet kurį arba visus šiuos dalykus:
 - Darbuotojo tipas, ar rodomi ištekliai turi būti sutartininkai, ar darbuotojai.
 - Tiekėjo įmonė, kuriai turėtų priklausyti išteklius.
 - Ištekliai, priklausantys konkrečiai subrangos arba subrangos eilutei.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Atnaujinti konkretaus poreikio išteklių ieškos nuskaitymo išteklių užklausą 
Ieškai naudojama užklausa taip pat turėtų būti atnaujinta, kad būtų galima naudoti šiuos papildomus filtro atributus. Norėdami atnaujinti planavimo lentos konfigūraciją, atlikite šiuos veiksmus, kad galėtumėte ieškoti poreikiais pagrįstų išteklių:

1. Atidarykite **konkrečios grafiko lentos parametrus**, tada pasirinkite **Atidaryti numatytuosius parametrus**, kad atidarytumėte konkretaus reikalavimo ieškos parametrus.
2. Atidarykite skirtuką **Bendrieji parametrai** ir slinkite į **Kiti parametrai**.
3. Šio skyriaus parametrų sąraše atnaujinkite **filtro maketą** į **Numatytąjį "Project Operations Lite**" filtro maketą.
4. Atnaujinkite **gauti išteklių užklausą** į numatytąją **"Project Operations Lite" išteklių nuskaitymo užklausą**.
5. Atidarykite skirtuką **Grafiko tipai** ir eikite į **"Project"**.
6. Dalyje "Project" parametrai atnaujinkite **planavimo asistento** nuskaitymo išteklių užklausą **į numatytąją**"Project Operations Lite **" išteklių užklausą ir atnaujinkite** planavimo asistento nuskaitymo apribojimų užklausą **į numatytąją**"Project Operations Lite **" nuskaitymo apribojimų užklausą.**

![Atnaujinti poreikiu pagrįstos išteklių ieškos grafiko lentos parametrus](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
