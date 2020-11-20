---
title: Kaip man atlikti preliminarią išteklių rezervaciją programos versijoje 2.x?
description: Šiame straipsnyje aprašoma, kaip „Project Service“ programoje preliminariai rezervuoti komandos narius.
author: JohnPBurrows
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/21/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a35799b422fa338c2666e1b2aa11bc2a54f5cce3
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122263"
---
# <a name="how-do-i-soft-book-resources-in-the-web-app-project-service-app-v2x"></a>Kaip man atlikti preliminarią išteklių rezervaciją žiniatinklio programoje („Project Service“ versija v2.x)?

[!INCLUDE[cc-applies-to-psa-app-1.x-2.x](../includes/cc-applies-to-psa-app-1x-2x.md)]

Galite preliminariai planuoti arba preliminariai rezervuoti išteklius projekto komandai norėdami parodyti, kad planuojate projektui priskirti tuos išteklius. Preliminarūs rezervavimai nesunaudoja galimo išteklių pajėgumo. Preliminariai rezervuoti komandos nariams negali būti priskiriamos projekto užduotys. Tik ištekliams, kurių būsena yra „Galutinai rezervuoti“, o vykdymo tipas – „Patvirtinta“, gali būti priskiriamos užduotys (darant prielaidą, kad ištekliai galutinai rezervuoti pakankamam kiekiui valandų, kad būtų padengtos priskyrimo pastangos).

Preliminariai rezervuoti komandos nariai matomi komandos nario tinklelyje, o jų preliminariai rezervuotos valandos nurodomos stulpelyje „Preliminarus rezervavimas”. Ši informacija taip pat atsiranda grafiko lentoje. Pasikartosime, jais nenurodomas joks pajėgumo sunaudojimas, nes preliminarus rezervavimas nesunaudoja išteklių pajėgumo.

Yra trys būdai, kaip „Project Service“ programos 2.x versijoje galite preliminariai rezervuoti komandos narį projektui. Tą galite padaryti grafiko lentoje, naudodami rezervavimų išlaikymo funkciją arba sukurdami bendruosius išteklius. Šie būdai yra aprašomi žemiau.

## <a name="soft-book-with-the-schedule-board"></a>Preliminarus rezervavimas grafiko lentoje

Norėdami atlikti preliminarų rezervavimą grafiko lentoje, turite: 
1. Atidaryti grafiko lentą.
2. Grafiko lentos apačioje esančiame skyde „Rezervavimo reikalavimai“ pasirinkti skirtuką „Projektas“.
3. Rasti projektą, kuriam norite preliminariai rezervuoti išteklius. Jei turite daug projektų, spustelėkite stulpelio „Projektas“ antraštę ir naudodami filtrą suraskite reikiamą projektą.
4. Spustelėti projektą, tada nuvilkti jį ant išteklių laiko tinklelio.
5. Tą atlikus dešinėje bus atidarytas skydas „Sukurti išteklių rezervavimą“. Nustatyti pradžios ir pabaigos datas, pasirinkti rezervavimo būseną „Preliminari“ ir nustatyti valandas. 
6. Spustelėti „Rezervuoti”.
7. Grįžus į projektą, ištekliai jau bus rodomi kaip komandos narys, kurio preliminariai rezervuotos valandos bus nurodytos stulpelyje „Rezervuoti preliminariai“.

Atkreipkite dėmesį, kad darbo paskirstymo struktūroje (WBS) negalėsite ištekliams paskirti užduočių, nes norint jiems priskirti užduotis, jie turi būti galutinai rezervuoti komandoje.

## <a name="soft-book-using-the-maintain-bookings-feature"></a>Preliminarus rezervavimas naudojant rezervavimo išlaikymo funkciją

Norėdami atlikti preliminarų rezervavimą naudodami rezervavimo išlaikymo funkciją, turite:
1. Komandos nario tinklelyje spustelėti „Naujas”.
2. Pasirinkti rezervuotinų išteklių vaidmenį bei pradžios ir pabaigos datas.
3. Pasirinkti vieną iš paskirstymo metodų, išskyrus „Joks”.
- Viso pajėgumo metodas
- Pajėgumo procentinės dalies rezervavimo metodas
- Tolygiai paskirstomų valandų metodas
- Priekinės apkrovos metodas
4. Spustelėkite Įrašyti. Išteklius matysite komandos tinklelyje, o jų valandos bus nurodytos kaip galutinai rezervuotos.
5. Išlaikyti išteklių rezervavimus, spustelint Išlaikyti rezervavimus.
6. Atsidarius grafiko lentai, išplėsti išteklius, kad būtų matomi jų rezervavimai. Išteklių būsena, kurią pamatysite, bus „Galutinė”
7. Dešiniuoju pelės mygtuku spustelėti rezervavimą, po pasirinkimu „Keisti būseną” pasirinkti „Rezervuoti preliminariai” ir tuomet „Preliminariai”. Rezervavimo būsena yra „Preliminariai”
8. Uždarę grafiko lentą pamatysite, kad komandos nario tinklelyje išteklių naudojimo valandų būsena pasikeitė iš „Galutinė“ į „Preliminari“
Atkreipkite dėmesį, kad galutinai rezervavus išteklius komandai ir tada darbo paskirstymo struktūroje jiems priskyrus užduotis, kai naudojate rezervavimų išlaikymą būsenos pakeitimui iš „Galutinė“ į „Preliminari“, bus pašalintos tų išteklių užduočių priskyrimai bus pašalinti, nes tik galutinai rezervuotiems ištekliams gali būti priskirtos užduotys.

## <a name="soft-book-by-creating-a-generic-resource"></a>Preliminarus rezervavimas naudojant bendruosius išteklius

Preliminarų rezervavimą galite atlikti sugeneruodami bendrąjį išteklių komandos narį, įvykdydami naudojant grafiko lentą arba išteklių užklausą ir rezervavimo metu pakeisdami tipą.
Tam atlikti turite:

1. Projekto darbo paskirstymo struktūroje užduotims, kurioms norite generuoti bendruosius komandos narius, priskirti vaidmenis.
2. Spustelėti „Generuoti projekto komandą”.
3. Projekto komandos nario tinklelyje pasirinkti bendruosius išteklius ir spustelėti „Rezervuoti”.
4. Grafiko lentoje pasirinkti norimus rezervuoti išteklius.
5. Grafiko lentos skyde „Kurti išteklių rezervavimą“ pakeisti rezervavimo būseną į „Preliminari“.
6. Spustelėti „Rezervuoti” arba „Rezervuoti ir išeiti”.

Uždarę grafiko lentą pamatysite, kad pasirinkti ištekliai yra pridėti prie komandos, taip pat matysite jų preliminariai rezervuotas bei priskirtas valandas. Taip pat matysite, kad komandoje lieka bendrieji ištekliai, kurie nurodo, kad užduotys yra priskirtos preliminariai rezervuotam komandos nariui.

Kai būsite pasiruošę pakeisti preliminariai rezervuotus komandos nario išteklius į galutinai rezervuotą komandos narį kad galėtumėte jam priskirti užduotis, atlikite šiuos veiksmus:

1. Pasirinkite tuos išteklius ir spustelėkite „Išlaikyti rezervavimus”.
2. Atsidarius grafiko lentai, išplėsti išteklius, kad būtų matomi jų rezervavimai. Išteklių būsena, kuria pamatysite bus „Preliminari“.
3. Dešiniuoju pelės mygtuku spustelėkite rezervavimą, po pasirinkimu „Keisti būseną” pasirinkite „Rezervuoti galutinai” ir tuomet „Galutinai”. Rezervavimo būsena yra „Galutinė”
4. Uždarę grafiko lentą pamatysite, kad komandos nario tinklelyje išteklių naudojimo valandų būsena pasikeitė iš „Preliminari“ į „Galutinė“. Dabar galite ištekliams priskirti užduotis (darant prielaidą, kad galutinai rezervuotos ir priskiriamos užduoties pastangų valandos yra suderintos). Atkreipkite dėmesį, kad jei sekėte elemento nr.3 bendrųjų išteklių įvykdymo veiksmus, esančius aukščiau, jums pakeitus preliminariai rezervuotų rezervuotinų išteklių būseną į galutinę, bendrasis komandos narys pašalinamas iš komandos.
