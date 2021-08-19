---
title: „Project Service Automation“ rezervavimo paskirstymo būdai
description: Šioje temoje pateikta informacija apie įvairius paskirstymo būdus.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: a770a51c2bf05e227367efc834dbff2832a316f617ae4fe22a43572940f43cbe
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7000856"
---
# <a name="booking-allocation-methods-in-project-service-automation"></a>„Project Service Automation“ rezervavimo paskirstymo būdai

[!include [banner](../includes/psa-now-project-operations.md)]

Nesvarbu, ar komandos narį į projektą įtraukiate tiesiogiai skirtuke **Komanda**, ar rezervuojate išteklių projekte arba reikalavimą iš grafikos lentos, yra keli skirtingi paskirstymo metodai, kuriuos galite panaudoti. Šioje temoje paaiškinama, kaip veikia kiekvienas metodas ir kurių metodų taikymas gali tapti resursų per didelio kiekio rezervavimo priežastimi.

## <a name="full-capacity"></a>Visas pajėgumas 
Visas pajėgumo metodas – rezervuojamas visas ištekliaus pajėgumas nurodytu pradžios ir pabaigos datų laikotarpiu. Pavyzdžiui, jei nustatyta, kad ištekliaus kalendorius turi veikti 8 valandas per dieną, 5 dienas per savaitę, nustačius pradžios ir pabaigos laikotarpį, apimantį penkias darbo dienas, išteklius bus rezervuotas 40 valandų. Toks rezervavimas atliekamas neatsižvelgiant į išteklių pajėgumo likutį. Jei nurodytu laikotarpiu išteklius jau rezervuotas kitiems projektams, 40 valandų rezervuojamos kaip papildomos, o tai gali tapti per didelio kiekio rezervavimo priežastimi.

## <a name="remaining-capacity"></a>Pajėgumo likučio metodas
Pajėgumo likučio metodą galima naudoti galima tik tada, jei rezervuojama tiesiai projekte, naudojant grafiko lentą. Naudojant šį metodą rezervuojamas išteklių pajėgumas, galimas nurodytu laikotarpiu. Pavyzdžiui, jei ištekliaus pajėgumas yra 40 valandų per savaitę ir jau yra rezervuota 10 valandų, rezervavus tai pačiai savaitei liks 30 pajėgumo tą savaitę valandų.

## <a name="percentage-capacity"></a>Pajėgumo procentinės dalies rezervavimo metodas
Pajėgumo procentinės dalies metodas suteikia galimybę rezervuoti ištekliaus pajėgumą pagal procentinę dalį nurodytu pradžios ir pabaigos datų laikotarpiu. Pavyzdžiui, jei nustatyta, kad ištekliaus kalendorius turi veikti 8 valandas per dieną, 5 dienas per savaitę, nustačius pradžios ir pabaigos laikotarpį, apimantį penkias darbo dienas, 50 % pajėgumu, išteklius bus rezervuotas 20 valandų. Atskiri rezervavimai kiekvienai dienai yra tolygiai paskirstomi visu laikotarpiu, pavyzdžiui, šiuo atveju keturioms valandoms kiekvieną dieną. Toks rezervavimas atliekamas neatsižvelgiant į išteklių pajėgumo likutį. Jei nurodytu laikotarpiu tam tikras išteklius jau rezervuotas kitiems projektams, 20 valandų rezervuojamos kaip papildomos, o tai gali tapti per didelio kiekio rezervavimo priežastimi.

## <a name="evenly-distribute-hours"></a>Tolygiai paskirstomų valandų metodas
Tolygiai paskirstomų valandų metodas suteikia galimybę išteklių rezervuoti nurodytam valandų skaičiui, kiekvienai dienai skirtą laiką tolygiai paskirstant nuo nurodyto laikotarpio pradžios ir pabaigos. Pavyzdžiui, jei išteklių rezervuojate 20 valandų penkių dienų laikotarpiui, taikant šį metodą 20 valandų tolygiai paskirstomos po keturias valandas per dieną. Toks rezervavimas atliekamas neatsižvelgiant į išteklių pajėgumo likutį. Jei nurodytu laikotarpiu tam tikras išteklius jau rezervuotas kitiems projektams, 20 valandų rezervuojamos kaip papildomos, o tai gali tapti per didelio kiekio rezervavimo priežastimi.

## <a name="front-load-hours"></a>Priekinės apkrovos valandų metodas
Priekinės apkrovos valandų metodas suteikia galimybę išteklių rezervuoti nurodytam valandų skaičiui, priekinę apkrovą pritaikant pagal kiekvienai dienai skirtų valandų skaičių nuo nurodyto laikotarpio pradžios ir pabaigos. Taikant priekinės apkrovos metodą galimi išteklio pajėgumai naudojami remiantis principu „pirmasis sunaudojamas pirmiausiai“.er Pavyzdžiui, jei ištekliaus darbo grafike numatytos aštuonios valandos per dieną, penkias dienas per savaitę ir tuo metu nėra rezervavimų, rezervuojant išteklių 20 valandų penkių darbo dienų laikotarpiu grafikas atrodytų taip: 

|         Rezervavimai          |    Pirma diena    |    Antra diena    |    Trečia diena    |    Ketvirta diena    |    Penkta diena    |    Iš viso    |
|---------------------------|-------------|-------------|-------------|-------------|-------------|-------------|
|    Atliktos rezervacijos    |    0        |    0        |    0        |    0        |    0        |    0        |
|    Nauja rezervacija          |    8        |    8        |    4        |    0        |    0        |    20       |

Taikant priekinės apkrovos metodą atsižvelgiama į esamus rezervavimus ir galimą naudoti pajėgumą. Pavyzdžiui, jei tie patys ištekliai jau yra rezervuoti dvidešimčiai valandų darbo savaitėje, nauji rezervavimai likusį pajėgumą pajėgumus naudotų taip:

|   Rezervavimai          | Pirma diena | Antra diena | Trečia diena | Ketvirta diena | Penkta diena | Iš viso |
|---------------------|-------|-------|-------|-------|-------|-------|
| Atliktos rezervacijos | 8     | 8     | 4     | 0     | 0     | 20    |
| Nauja rezervacija       | 0     | 0     | 4     | 8     | 8     | 20    |

Kadangi atsižvelgiama į galimą pajėgumą, gali būti, kad jei nebeliks išteklių pajėgumo, kurį gali sunaudoti rezervavimas, gausite klaidos pranešimą. Naudodami šį metodą rezervavimo perviršio nepasieksite.

## <a name="none"></a>Joks
Metodą „Joks“ galėsite naudoti tik tada, jei rezervavimą atliksite projekto skirtuke **Komanda**. Taikant šį metodą ištekliai projekte pridedami kaip komandos narys, tačiau nesukuria rezervavimų, kurie naudotų išteklių pajėgumą. Šis metodas yra naudojamas, kai numatytasis projekto vadovo komandos narys įtraukiamas sukūrus projektą. Projekto vadovo vartotojas, kuris sukūrė projektą, prie projekto pridedamas pagal numatytuosius nustatymus, todėl projekto objekto įrašas turi savininką ir egzistuoja vienas projekto patvirtintojas. Kadangi šis vartotojas neturi rezervavimų, norėdami užsakyti išteklių, galite ištrinti ir iš naujo įtraukti jį naudodami kitą paskirstymo metodą, arba išteklius įtraukti į užduotis, tada panaudoti parinktį **Išplėsti rezervavimus** skirtuke **Derinimas** ir taip priskyrimams sukurti rezervavimus.

## <a name="allocation-methods-that-lead-to-overbooking"></a>Paskirstymo metodai, galintys tapti rezervavimo perviršio priežastimi
Apibendrinant, toliau pateikiami paskirstymo metodai gali tapti rezervavimo perviršio priežastimi, jei rezervuojami ištekliai jau naudojami kitiems projektams (arba kitiems darbo užsakymams ar planuojamiems objektams) atlikti:

- Viso pajėgumo metodas
- Pajėgumo procentinės dalies rezervavimo metodas
- Tolygiai paskirstomų valandų metodas

Naudojant vieną iš šių trijų paskirstymo metodų, jums nebus pranešama, kad pasiektas išteklių rezervavimo perviršis. Tam, kad ištaisytumėte per didelio kiekio rezervavimą, turėsite pasinaudoti grafiko lenta.


[!INCLUDE[footer-include](../includes/footer-banner.md)]