---
title: Išlaidų ataskaitų pertvarkymas
description: Šioje temoje pateikta informacija apie išlaidų ataskaitos įrašo pertvarkytą patirtį.
author: suvaidya
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 18d7407681906361f3f818225efb8510ac981d98
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122804"
---
# <a name="expense-reports-reimagined"></a>Išlaidų ataskaitų pertvarkymas

Išlaidų ataskaitos įrašas buvo perkurtas, kad procesas būtų paprastesnis ir sutrumpėtų laikas, reikalingas ataskaitai užbaigti. Čia yra pagrindiniai naujų išlaidų patirties komponentai:

- Nauja išlaidų valdymo darbo sritis, leidžianti pasiekti atstovo išlaidas.
- Nauja kvitą atitinkanti patirtis, siekiant geriau rodyti antraščių lygio kvitus ir supaprastinti kvitų įtraukimą į išlaidų eilutes procesą.
- Naujas tik skaitomas tinklelis, leidžiantis peržiūrėti daugiau išlaidų eilučių ir papildomų duomenų stulpelių. Dabar galite matyti visas detalizuotas ir išskaidytas eilutes ir jų pirmines išlaidas.
- Supaprastinta išlaidų redagavimo sritis.
- Pertvarkyti klaidų, įspėjimų ir strategijų pranešimai, kad būtų perteiktas teisingas kontekstas ir problemos supratimas ir kaip ją išspręsti. Pašalinome kelis pranešimus, kurie atsirasdavo prieš vartotojams atlikus užduotis ir sprendžiant problemas.
- Naujas puslapis, kuriame galima nurodyti būtinus laukus, pasirinktinius laukus ir laukus, kurie neturėtų būti įtraukiami. Šis puslapis padeda sumažinti laukų, kuriuos reikia nustatyti, skaičių.
- Nauja išlaidų ataskaitų išvaizda, kad ataskaitos nebeatrodytų lyg būtų skirtos tik apskaitą suprantantiems asmenims.

Norėdami įjungti naują naudojimo patirtį, naudokite darbo sritį **Funkcijų valdymas**, kad įjungtumėte funkciją **Išlaidų ataskaitų pertvarkymas**. Įjungus šią funkciją atliekami šie veiksmai:

- Esama išlaidų darbo sritis pakeičiama nauja darbo sritimi.
- Įtraukiamas naujas išlaidų lauko matomumo meniu elementas.
- Nepanaikinti jokie esami išlaidų ataskaitų (esamo puslapio) arba išlaidų ataskaitos laukų meniu elementai.
- Darbo eigos ir bet kokie patvirtinimai vis dar pateksite į esamų išlaidų ataskaitų puslapį.

## <a name="getting-started-video-for-new-users"></a>Darbo pradžios vaizdo įrašai naujiems vartotojams

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

[„Dynamics 365 for Finance and Operations“ išlaidų patirties](https://youtu.be/Ocy-MsTvEE0) vaizdo įrašai (nurodytų aukščiau) įtraukti į [„Finance and Operations“ grojaraštį](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), kurį galite rasti „YouTube“.

## <a name="new-features"></a>Naujos funkcijos

| Nauja funkcija | Aprašo |
|---|----|
| Išlaidų lauko matomumas | Naujame nustatymų puslapyje galite nurodyti, kurie laukai turi būti išjungti organizacijai, kurie laukai turi būti būtini ir kurie yra rekomenduojami. |
| Būtini laukai | Naudojant naują paprastą konfigūraciją galite kelis laukus padaryti būtinais nenaudojant strategijos sistemos. |
| Pasirinktiniai laukai | Pridedamas antras pasirinktinių laukų puslapis. Tokiu būdu darbuotojai nesijaus, lyg turi nustatyti laukus, tačiau laukai vis dar lengvai pasiekiami. |
| Nepridėtų kvitų įtraukimas | Galimybė įtraukti nepridėtus kvitus į išlaidų ataskaitą labiau matoma iš darbo srities ir išlaidų ataskaitos. |
| Patobulinti pranešimai | Yra geresnis matomumas į išlaidų eilutes, kurios turi įspėjimus ir klaidas. |
| Mažiau pranešimų pranešimų juostoje| „Infolog“ pranešimų skaičius sumažėjo ir daugelyje atvejų nebus rodomi pasikartojantys pranešimai. |
| Sugrupuoti bendrieji veiksmai | Sąsaja buvo išvalyta pridedant naują veiksmų mygtuką daugeliui bendrųjų eilutės lygio veiksmų ir pridedant elipsės mygtuką (...), skirtą antraštėms ir kitiems rečiau naudojamiems veiksmams. |
| Nauja darbo sritis siekiant padidinti matomumą | Nauja darbo sritis sujungia funkcijas ir saitus, kurie vartotojams leidžia pereiti į skirtingas sritis. |
| Esamų išlaidų ir kvitų įtraukimas atliekant išlaidų kūrimą | Kurdami išlaidų ataskaitas galite įtraukti visas arba pasirinktas išlaidas ir kvitus. |
| Valiutos kurso skaičiuotuvas | Įtraukiamas valiutos kurso skaičiuotuvas, leidžiantis apskaičiuoti kišenės kelių valiutų operacijų valiutos kursą. |
| Naujų išlaidų eilučių išsaugojimas ir įtraukimas | Įvesdami naujas išlaidas, galite naudoti mygtukus **Įrašyti** ir **Nauja**, kad greitai įvestumėte išlaidų eilutes. |
| Išskaidytų ir detaliai išvardytų eilučių geresnis matomumas | Detaliai išvardytos ir išskaidytos eilutės tiesiogiai įtraukiamos į išlaidų sąrašą, kad būtų padidintas matomumas ir būtų lengviau nustatyti, ar yra klaidų. |
| Kvitų rodymas detalizavimo metu | Galite matyti kvitus detalizavimo metu. |

Pradinis leidimas sutelktas į išlaidų įrašų scenarijus. Bet koks išlaidų ataskaitos peržiūros arba patvirtinimo scenarijus toliau naudos esamą išlaidų įrašo puslapį.

Toliau pateiktos funkcijos yra esamame puslapyje, bet dar nepateiktos naujame puslapyje. Šios funkcijos bus iš naujo įtrauktos į kitus kelis leidimus:

- Patvirtinimai
- Mokėtinų sumų patvirtinimai ir galimybė redaguoti apskaitą
- Keli įvesties taškai
- Kelionės paraiškos integravimas
- Duomenų objektas išlaidų lauko matomumui
- Dienpinigių išlaidų įrašas
- Eilutės lygio darbo eiga
- Tarpinio tvirtintojo palaikymas
- Išplėstinis detalizavimas
