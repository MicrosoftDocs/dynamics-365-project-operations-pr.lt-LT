---
title: Dienpinigių išlaidos
description: Šiame straipsnyje pateikiama informacija apie tai, kaip dirbti su dienpinigių išlaidomis.
author: suvaidya
ms.date: 03/18/2022
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: ''
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 0d2f95b677720726049d7d010e9738ad8c513802
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923198"
---
# <a name="per-diem-expenses"></a>Dienpinigių išlaidos

> [!IMPORTANT] 
> Šiame straipsnyje apibūdintos funkcijos tiksliniams vartotojams pasiekiamos kaip peržiūros leidimo dalis.

Dienpinigių mokėjimas yra fiksuota, iš anksto nustatyta kasdienė išmoka, kurią įmonė moka darbuotojams už nakvynę (viešbučius), maistą ir papildomas išlaidas, su kuriomis šie darbuotojai susiduria keliaudami į darbą. Įmonė šią išmoką moka darbuotojams, o ne apmoka faktines kelionės išlaidas. Darbuotojai gali naudoti savo **Nenumatytų/Kitų išlaidų** dienpinigių išmoką arbatpinigiams, kambarių aptarnavimui, skalbimui arba sausojo valymo paslaugoms per svarbius verslo susitikimus. Dienpinigių norma gali skirtis atsižvelgiant į tai, ar darbuotojas pasirenka kompensuoti bendrą nakvynės ir maisto kainą, ar tik maisto ir nenumatytų išlaidų kainą.

Dienpinigiai gali būti pagrįsti metų laiku, kelionės vieta arba abiem. Kai sukuriate dienpinigių taisyklę, galite nurodyti, kad už dienpinigius procentinė dalis bus išskaičiuota, jei darbuotojas gaus papildomą maitinimą ar aptarnavimą. Taip pat galite nustatyti mažiausią ir didžiausią valandų skaičių, už kurias būtų skiriami dienpinigiai darbuotojui keliaujant.

Dienpinigiai apskaičiuojami kaip bendra per dieną siūlomų išlaidų suma atėmus darbuotojui teikiamo maisto sumažinimą (papildomo maitinimo kainą).

## <a name="configure-per-diems"></a>Sukonfigūruokite dienpinigius

Norėdami sukonfigūruoti dienpinigių išlaidas, atlikite toliau nurodytus veiksmus.

1. Eikite **į Išlaidų valdymas** \> **Sąranka** \> **Bendrieji** \> **Išlaidų valdymo parametrai.**
2. Skirtuko **Dienpinigiai**, lauke **Skaičiuoti maisto sumažinimą pagal** pažymėkite, kaip turėtų būti apskaičiuojami dienpinigiai:

    - **Maitinimo tipai kelionėje** apskaičiuokite dienpinigius pagal įvestus maitinimo tipus (pusryčiai, pietūs, vakarienė) ir pagal maisto sumažinimą, kuris yra apibrėžtas kiekvienam maitinimo tipui dienpinigiams kelionės trukmei.
    - **Maitinimo tipai per dieną** apskaičiuokite dienpinigius pagal įvestus maitinimo tipus ir pagal maisto sumažinimą, kuris yra apibrėžtas kiekvienam maitinimo tipui dienpinigiams per dieną.
    - **Maitinimų skaičius per dieną** apskaičiuokite dienpinigius pagal tai, kiek maitinimų buvo per dieną ir pagal maitinimo sumažinimą kasdien teikiamų maitinimų skaičiui.

3. Eikite į **Išlaidų valdymas** \> **Nustatymai** \> **Skaičiavimai ir kodai** \> **Dienpinigių vietos**.
4. Įtraukite vietas, kur galima naudoti dienpinigius.
5. Kiekvienai įtrauktai vietai **Dienpinigių** skirtuke, pasirinkite dienpinigių normą ir valiutą, galiojančią nuo konkrečios pradžios iki pabaigos datos nakvynei, maitinimui ir kitoms išlaidoms. Norėdami sukonfigūruoti dienpinigių normas ir valiutas, eikite į **Išlaidų valdymas** \> **Sąranka** \> **Skaičiavimai ir kodai** \> **Dienpinigiai**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Dienpinigiai pakeistoje išlaidų sąsajoje

Dienpinigių funkcija yra palaikoma pakeistoje **Išlaidų valdymo** darbo srityje „Microsoft Dynamics 365 Finance“ 10.0.25 ir vėlesnėse versijose.

Norėdami įjungti dienpinigių funkciją, atlikite toliau nurodytus veiksmus.

1. **Funkcijų valdymo** darbo srityje raskite ir sąraše pasirinkite funkciją **Pakeistų išlaidų ataskaita**, tada pasirinkite **Įgalinti dabar**.
2. Raskite ir sąraše pasirinkite funkciją **Dienpinigiai išlaidų ataskaitai pakeistoje sąsajoje**, tada pasirinkite **Įgalinti dabar**.

## <a name="how-the-feature-works"></a>Kaip veikia ši funkcija

Šiame skyriuje pateikiami trijų konfigūravimo scenarijų pavyzdžiai. Kiekvienam pavyzdžiui laukelis **Apskaičiuotų maitinimo sumažinimą pagal** nustatytas skirtingomis reikšmėms. Visų trijų pavyzdžių bendra suma, kuri yra apmokama, yra ta pati tol, kol taikomas maitinimo sumažinimas. Po to bendra mokama suma skiriasi kiekviename pavyzdyje.

Norėdami sukurti dienpinigių išlaidas, naudojamas visuose trijuose pavyzdžiuose, atlikite šiuos veiksmus.

1. Eikite į **Darbo sritys** \> **Išlaidų valdymas**.
2. Pasirinkite **Nauja išlaidų ataskaita** arba pažymėkite esamą išlaidų ataskaitą.
3. Įtraukti naujas išlaidas. Laukelyje **Kategorija** pasirinkite **Dienpinigiai**. Pažymėkite savo kelionės vietą ir pradžios bei pabaigos datas. Dienpinigiai nakvynei, maitinimui ir nenumatytoms (kitoms) išlaidoms apskaičiuojami pagal kasdienę išmoką, nustatytą pasirinktai vietai.

    Pvz., pasirenkate vietą **Redmondas (JAV)**. Kasdienė tos vietos išmoka yra 150 JAV dolerių (150 USD) nakvynei, 75 USD maitinimui ir 5 USD nenumatytoms išlaidoms. Pradžios data yra Sausio 10 d., o pabaigos data yra Sausio 14 d. Todėl pažymėta trukmė yra penkios dienos, kai pasirinkta konfigūracija yra kalendorinės dienos su laiku, o pažymėtas laikas prasideda ir baigiasi 12:00 val. pradžios ir pabaigos datomis. Štai skaičiavimai:

    - Bendra mokama suma = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
    - Bendros sumos dalis maistui ir nenumatytoms išlaidoms = 5 × (75 + 5) = 400 USD

Jei per kelionę buvo suteikti pusryčiai, pietūs ir vakarienė, maitinimai turi būti apskaityti kaip maitinimo sumažinimas.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1 pavyzdys: dienpinigiai, kai maisto sumažinimai kelionėje grindžiami maitinimo tipais

Šiame pavyzdyje maitinimo sumažinimas yra 30 procentų pusryčiams, 30 procentų pietums ir 40 procentų vakarienei. Puslapyje **Išlaidų valdymo parametrai** laukelis **Apskaičiuoti maitinimo sumažinimą pagal** nustatytas kaip **Kelionės maitinimo tipai**. Štai skaičiavimai, jei darbuotojui buvo pateikti treji pusryčiai, dveji pietūs ir nulis vakarienių:

- Maitinimo sumažinimas = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = 112,50 USD
- Maitinimas ir nenumatytos išlaidos = 400 – 112,50 = 287,50 USD
- Bendra mokėtina suma = Bendra išmoka – Maitinimo sumažinimas = 1 150 – 112,50 = 1037,50 USD

![Dienpinigių išlaidos, kai maitinimo sumažinimas kelionėje grindžiamas maitinimo tipais.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2 pavyzdys: dienpinigiai, kai maitinimo sumažinimai grindžiami maitinimo tipais per dieną

Šiame pavyzdyje maitinimo sumažinimas yra 30 procentų pusryčiams, 30 procentų pietums ir 40 procentų vakarienei. Puslapyje **Išlaidų valdymo parametrai** laukelis **Apskaičiuoti maitinimo sumažinimą pagal** nustatytas kaip **Maitinimo tipai per dieną**. Tokiu atveju, tinklelio **Maitinimai** **Redaguoti išlaidas** dialogo lange, išvalykite žymės langelius ir nurodykite, kurie maitinimai jums buvo pateikti kelionės metu.

Pavyzdžiui, čia pateikiami skaičiavimai, jei pusryčiai buvo pateikti du kartus per pirmąsias tris kelionės dienas:

- Kasdieni maitinimo sumažinimas per kiekvieną iš pirmųjų trijų dienų = 75 × 30% = 22,50 USD
- Bendras maitinimo sumažinimas = 3 × 22,50 = 67,50 USD
- Nuo 1 iki 3 dienų maitinimai ir nenumatytos išlaidos = 75 – 22,50 = 57,50 USD
- Iš viso maitinimai ir nenumatytos išlaidos = maitinimų ir nenumatytų išlaidų suma per penkias dienas = 400 – 67,50 = 332,50 USD
- Bendra mokėtina suma = Bendra suma – Maitinimo sumažinimas = 1150 – 67,50 = 1082,50 USD

![Dienpinigių išlaidos, kai maitinimo sumažinimas grindžiamas maitinimo tipais per dieną.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3 pavyzdys: dienpinigiai, kai maitinimo sumažinimai grindžiami maitinimų skaičiumi per dieną

Šiame pavyzdyje, maitinimo sumažinimai apskaičiuojami pagal tai, kiek maitinimų buvo pateikiama per dieną (tai yra, **Apskaičiuoti maitinimo sumažinimą pagal** laukelis **Išlaidų valdymo parametrų** puslapyje nustatytas **Maitinimų skaičius per dieną**). Tinklelio **Maitinimai** **Redaguoti išlaidas** dialogo lange, išvalykite žymės langelius ir nurodykite, kurie maitinimai jums buvo suteikti.
Tokiu atveju, maitinimo sumažinimas dėl yra pagrįstas tik # teikiamais maitinimais, o ne pateikiamo maitinimo tipais (Pusryčiai / pietūs / vakarienė).

Toliau pateikiami dienpinigių skaičiavimai, kai kasdienė išmoka nakvynei yra 150 USD, maitinimui – 75 USD, o nenumatytoms išlaidoms – 5 USD:

- **Bendra mokama suma** = 5 × (150 + 75 + 5) = 5 × 230 = 1150 USD
- **Vienas maitinimas:** Maitinimo sumažinimas = 20 % = 15 USD
- **Du maitinimai:** Maitinimo sumažinimas = 50 % = 37,50 USD
- **Trys maitinimai:** Maitinimo sumažinimas = 100 % = 75 USD

Toliau pateikiami **maitinimo ir nenumatytų išlaidų išmokos** skaičiavimai, apimantys 5 USD nenumatytoms išlaidoms:

- 1 diena – pateikti du maitinimai = ( 75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 2 diena – pateikti du maitinimai = ( 75 – 37,50) + 5 = 37,50 + 5 = 42,50 USD
- 3 diena – pateiktas vienas maitinimas = (75 –15) + 5 = 60 + 5 = USD 65
- 4 diena – pateikta nulis maitinimų = ( 75 – 0) + 5 = 75 + 5 = 80 USD
- 5 diena – pateikti trys maitinimai = ( 75 – 75) + 5 = 0 + 5 = 5 USD

- Bendras maitinimų ir nenumatytų išlaidų skaičius = 1 diena + 2 diena + 3 diena + 4 diena + 5 diena = 235 USD
- Bendras maitinimo umažinimas = Maitinimo sumažinimas 1 dieną + 2 dieną + 3 dieną + 4 dieną + 5 dieną = 37,5 + 37,5 + 15 + 0 + 75 = 165 USD
- Bendra mokėtina suma = Bendra išmoka – Bendras maitinimo sumažinimas = 1 150 USD – 165 USD = 985 USD

![Dienpinigių išlaidos, kai maitinimo sumažinimas grindžiamas maitinimų skaičiumi per dieną.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> 10.0.23 finansų versijos atveju, jei naudojate perkurtą išlaidų sąsają, negalite sukurti dienpinigių išlaidų, kurios turi persidengiančias datas. Jei bandote, gausite klaidos pranešimą.
