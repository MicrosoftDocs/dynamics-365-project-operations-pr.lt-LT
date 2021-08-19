---
title: Kas nauja arba pakeista „Project Service Automation“ V3 18 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 18 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/27/2020
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
ms.openlocfilehash: 43491a3820d84e9d2a43e678f2604e234e18794d9e28889429debc0b991bbfac
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004366"
---
# <a name="project-service-automation-update-release-18-v3"></a>„Project Service Automation“ V3 18 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 18 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V3.10.8.12 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. balandžio mėn.

## <a name="update-release-18"></a>18 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

- Išspręsta: srautai **Atšaukti**, **Pateikti užklausą** ir **Atšaukti patvirtinimą** pateikia išimtis su neaiškiais klaidos pranešimais.
- Išspręsta: kai išlaidoms nepavyksta **Atšaukti patvirtinimą**, nepateikiama reikiama išimties klaida.
- Išspręsta: tinklelyje Laiko įrašas neteisingai tvarkomos ne darbo dienos Australijoje po vasaros laiko įvedimo (DST) spalio mėn.
- Išspręsta: dėl netinkamos numatytojo vykdymo logikos negalima pateikti išlaidų.
- Išspręsta: kai laiko įrašo patvirtinimas yra nesėkmingas, jis tebėra būsenoje **Laukiama**.
- Išspręsta: SQL masinių patvirtinimų klaidos (aklavietė / pasibaigė skirtasis laikas).
- Išspręsta: patvirtinant laiko įrašus vartotojo patirtyje atsiranda reikšmingų našumo problemų, kai naujinami komandos nariai.

**Projektų valdymas**

- Išspręsta: laiko juostos pranešimas perkeltas iš rodinio **Suderinimas** į pagrindinę formą **Projektas**.
- Išspręsta: kalendoriaus šablonas netinkamai vykdomas, kai atidaroma nauja projekto forma.
- Išspręsta: „Chromium“ pagrindu sukurtose naršyklėse vartotojai negali lengvai pažymėti naikinti ankstesnių užduočių.
- Išspręsta: kuriant arba kopijuojant **projektą iš tuščio šablono** iškviečiami nesusiję priskyrimai.
- Išspręsta: tam tikrais kraštutiniais atvejais sukūrus naują priskyrimą iš užduočių tinklelio, sukuriami įrašų dublikatai.
- Išspręsta: neautomatiniu režimu vartotojai negali atnaujinti užduoties pradžios datos, kad ši būtų vėlesnė nei dabartinė įrašyta data.

**Išteklių valdymas**

- Išspręsta: išplėtus rezervavimus rodinio **Suderinimas** tarpinės sumos eilutėje neteisingai apskaičiuojamas rezervavimų nuokrypis.
- Išspręsta: rodinyje **Suderinimas** netinkamai rodomi išteklių priskyrimai, kai rezervuotinų išteklių kalendorius neatitinka projekto kalendoriaus.

**„Sales“**

- Išspręsta: kai laiko įrašai patvirtinami iš naujo (**Patvirtinti > Atšaukti >** patvirtinti dar kartą), sukuriamas įrašo duplikatas su neapmokestinama faktine reikšme.


[!INCLUDE[footer-include](../includes/footer-banner.md)]