---
title: Sukonfigūruokite grafiko lentą, kad būtų rodomi sutarties darbuotojai ir subrangos pajėgumas
description: Šiame straipsnyje aprašoma, kaip konfigūruoti "Microsoft" Dynamics 365 Project Operations grafikų lentą, kad būtų rodomas subrangos būdu susietų išteklių pajėgumas, kai dirbama su projekto išteklių reikalavimais.
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

"Microsoft" Dynamics 365 Project Operations tvarkaraščių lenta gali būti naudojama ieškant išteklių dviem būdais:

- Bendroji išteklių paieška be jokio konkretaus projektu pagrįsto išteklių poreikio konteksto.
- Konkretaus reikalavimo išteklių paieška, kai projekto reikalavimas suteiks siūlomų išteklių kontekstą.

Norėdami pranešti grafiko valdybai apie subrangos būdu sudarytus išteklių pajėgumus ir sutartininkus, turite atnaujinti grafiko lentos parametrus. Šie naujinimai apima: 
- Atnaujinkite bendrosios išteklių paieškos tvarkaraščių lentos parametrus.
- Atnaujinkite tvarkaraščio lentos parametrus, kad galėtumėte atlikti ištekliais pagrįstą išteklių paiešką.

## <a name="update-schedule-board-settings-for-general-resource-search"></a>Atnaujinkite bendrosios išteklių paieškos tvarkaraščio lentos nustatymus
### <a name="update-filters-for-general-resource-search"></a>Bendrosios išteklių paieškos filtrų naujinimas
Kai ieškote išteklių, tvarkaraščio lentoje esantys filtrai turėtų būti atnaujinti, kad galėtumėte ieškoti išorinių išteklių nurodydami bet kurį arba visus šiuos dalykus:
  - Darbuotojo tipas, ar rodomi ištekliai turėtų būti sutartininkai, ar darbuotojai.
  - Tiekėjo įmonė, kuriai turėtų priklausyti išteklius.
  - Ištekliai, priklausantys konkrečiai subrangos arba subrangos linijai.
    
### <a name="update-retrieve-resource-query"></a>Išteklių gavimo užklausos naujinimas
Paieškai naudojama užklausa taip pat turėtų būti atnaujinta, kad būtų galima naudoti šiuos papildomus filtro atributus. Norėdami atnaujinti bendrosios išteklių ieškos planavimo lentos konfigūraciją, atlikite šiuos veiksmus:  
1. Atidarykite **konkrečios tvarkaraščio lentos nustatymus**.
2. Atidarykite skirtuką **Bendrieji nustatymai** ir slinkite iki **Kiti nustatymai**.
3. Šio skyriaus parametrų sąraše atnaujinkite **filtro maketą** į **numatytąjį "Project Operations Lite"** filtro maketą.
4. Atnaujinkite **išteklių gavimo užklausą** į **numatytąją išteklių gavimo užklausą, skirtą "Project Operations Lite"**.

![Atnaujinkite bendrosios išteklių paieškos tvarkaraščio lentos nustatymus](../media/BoardSettings.png)  

## <a name="update-schedule-board-settings-for-requirementbased-resource-search"></a>Tvarkaraščio lentos parametrų naujinimas, kad būtų galima atlikti ištekliais pagrįstą išteklių paiešką
### <a name="update-filters-for-requirement-specific-resource-search"></a>Konkrečių reikalavimų išteklių ieškos filtrų naujinimas 
Kai ieškote išteklių, tvarkaraščio lentoje esantys filtrai turėtų būti atnaujinti, kad galėtumėte ieškoti išorinių išteklių nurodydami bet kurį arba visus šiuos dalykus:
 - Darbuotojo tipas, ar rodomi ištekliai turėtų būti sutartininkai, ar darbuotojai.
 - Tiekėjo įmonė, kuriai turėtų priklausyti išteklius.
 - Ištekliai, priklausantys konkrečiai subrangos arba subrangos linijai.

### <a name="update-retrieve-resource-query-for-requirement-specific-resource-search"></a>Naujinimas gauti išteklių užklausą, kad būtų galima atlikti konkrečių reikalavimų išteklių paiešką 
Paieškai naudojama užklausa taip pat turėtų būti atnaujinta, kad būtų galima naudoti šiuos papildomus filtro atributus. Norėdami atnaujinti tvarkaraščio lentos konfigūraciją, kad atnaujintumėte reikalavimais pagrįstą išteklių paiešką, atlikite šiuos veiksmus:

1. Atidarykite **konkrečios tvarkaraščių lentos parametrus**, tada pasirinkite **Atidaryti numatytuosius parametrus**, kad atidarytumėte konkrečių reikalavimų paieškos parametrus.
2. Atidarykite skirtuką **Bendrieji nustatymai** ir slinkite iki **Kiti nustatymai**.
3. Šio skyriaus parametrų sąraše atnaujinkite **filtro maketą** į **numatytąjį "Project Operations Lite"** filtro maketą.
4. Atnaujinkite **išteklių gavimo užklausą** į **numatytąją išteklių gavimo užklausą, skirtą "Project Operations Lite"**.
5. Atidarykite skirtuką **Tvarkaraščio tipai** ir eikite į **Projektas**.
6. Dalyje "Project" parametrų atnaujinkite **grafiko** asistentą, kad gautumėte išteklių užklausą **į** numatytąją išteklių užklausą, skirtą "Project Operations Lite"**, ir atnaujinkite** grafiko asistentą Gauti apribojimų užklausą **į** numatytąją nuskaitymo apribojimų užklausą, skirtą "Project Operations Lite"**.**

![Tvarkaraščio lentos parametrų naujinimas, kad būtų galima atlikti ištekliais pagrįstą išteklių paiešką](../media/SASettings.png)  

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
