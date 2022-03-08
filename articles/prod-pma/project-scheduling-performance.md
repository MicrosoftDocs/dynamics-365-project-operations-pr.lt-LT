---
title: Projekto išteklių planavimo efektyvumas
description: Šioje temoje pateikta informacija apie tai, kaip padidinti daugelio projektų išteklių planavimo efektyvumą.
author: Yowelle
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 9dc638a7b2d8e0db45b5acfa5cc9512f356f8b2635028748a1e2c3230605c154
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007291"
---
# <a name="project-resource-scheduling-performance"></a>Projekto išteklių planavimo efektyvumas

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Kai projektų skaičius pasiekia tūkstančius, gali atsirasti su išteklių planavimu susijusių efektyvumo problemų. Norint padidinti išteklių planavimo efektyvumą yra funkcija, leidžianti naudotojams sutrumpinti laiką, kurio reikia norint paleisti išteklių pasiekiamumo formą. Tiksliau kalbant, taip pašalinamas išteklių pajėgumo sumavimo sinchronizavimo procesas ir naudojama lentelė **ResProjectResource**, kad paspartėtų išteklių peržvalga. Atkreipkite dėmesį, kad lentelė **ResRollup** nebebus naudojama.

> [!IMPORTANT]
> Jei yra priklausomybė nuo išteklių pajėgumų sumavimo sinchronizavimo proceso arba lentelės **ResProjectResource**, šios funkcijos nenaudokite.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Išteklių planavimo efektyvumo didinimo įjungimas
Norėdami įjungti išteklių planavimo efektyvumo didinimą atlikite toliau nurodytus veiksmus.

1. Eikite į **Funkcijų valdymas** > **Visi** ir funkcijų sąraše raskite **Įjungti projektų išteklių planavimo efektyvumo didinimo funkciją**.
2. Pasirinkite **Įjungti dabar**.

> [!NOTE]
> Jei funkcijos nerandate sąraše, pasirinkite **Tikrinti, ar yra naujinimų** norėdami sąrašą atnaujinti.

3. Atnaujinkite naršyklę, tada eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projektų ištekliai** > **Sinchronizuoti išteklių kalendorių pajėgumą visose įmonėse**.
4. Nustatykite **Pašalinti esamus pajėgumų įrašus** į **Taip** norėdami pašalinti ankstesnius duomenis. Jei norite generuoti papildančiuosius duomenis, nustatykite **Ne**.
5. Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio duomenys turėtų būti generuojami. Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datos nebūtina apibrėžti.
6. Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.
7. Pasirinkite **Gerai**.

 > [!NOTE]
 > Tada bendri duomenys bus paskirstyti lentelėje **ResCalendarCapacity** visoms jūsų aplinkos įmonėms, kad paketinę užduotį pakaktų paleisti tik viename juridiniame subjekte. Šios paketinės užduoties duomenys yra reikalingi norint apskaičiuoti išteklių pajėgumą susietame kalendoriuje.

8. Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Projektų ištekliai** > **Užpildyti projektų išteklius visose įmonėse** ir pasirinkite **Gerai**. Tai bendrų duomenų atnaujinimo scenarijus lentelėse **ResProjectResource**, **ResCalendarDateTimeRange** ir **ResEffectiveDateTimeRange**. Lauko **PSAPRojSchedRole.RootActivity** reikšmės taip pat atnaujinamos. Jei tai nevykdoma, gausite įspėjimą, kai bandysite vykdyti išteklių planavimo operacijas.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Išteklių planavimo efektyvumo didinimo išjungimas

1. Eikite į **Funkcijų valdymas** > **Visi** ir raskite **Įjungti projektų išteklių planavimo efektyvumo didinimo funkciją**.
2. Pasirinkite funkciją ir mygtuką **Išjungti**.
3. Atnaujinkite naršyklę.
4. Eikite į **Projektų valdymas ir apskaita** > **Periodinis** > **Pajėgumų sinchronizavimas** > **Sinchronizuoti išteklių pajėgumų sumavimą**.
5. Puslapyje **Pajėgumų sumavimo sinchronizavimas** nustatykite **Šalinti esamus pajėgumų įrašus** į **Taip** norėdami pašalinti ankstesnius duomenis. Jei norite generuoti papildančiuosius duomenis, nustatykite **Ne**.
6. Lauke **Laikotarpio kodas** pasirinkite laikotarpį, kurio duomenys turėtų būti generuojami. Jei pasirenkate laikotarpio kodą, pradžios ir pabaigos datos nebūtina apibrėžti.
7. Jei lauką **Laikotarpio kodas** paliekate tuščią, duomenims generuoti pasirinkite konkrečias pradžios ir pabaigos datas.
8. Pasirinkite **Gerai**.

> [!NOTE]
> Tada bendri duomenys bus paskirstyti lentelėje **ResRollup** visoms jūsų aplinkos įmonėms, kad paketinę užduotį pakaktų paleisti tik viename juridiniame subjekte. Ši paketinė užduotis reikalinga visiems **Išteklių pasiekiamumo** rodiniams. Jei ši paketinė užduotis nevykdoma, **ResRollup** duomenys nebus sugeneruoti iš karto – tai gali užtrukti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]