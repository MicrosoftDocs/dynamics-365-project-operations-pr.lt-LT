---
title: Dienpinigių išlaidos
description: Šioje temoje pateikiama informacija apie tai, kaip dirbti su dienpinigių išlaidomis.
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
ms.openlocfilehash: fe72f066a6819c3b43e3977d5e7afb01ba95338c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8596060"
---
# <a name="per-diem-expenses"></a>Dienpinigių išlaidos

> [!IMPORTANT] 
> Šioje temoje aprašytos funkcijos yra prieinamos tiksliniams vartotojams kaip peržiūros leidimo dalis.

Dienpinigių mokėjimas yra fiksuotas, iš anksto nustatytas dienpinigis, kurį įmonė moka savo darbuotojams už apgyvendinimą (viešbučius), maitinimą ir atsitiktines išlaidas, kurias šie darbuotojai patiria keliaudami į darbą. Bendrovė moka šią išmoką darbuotojams, o ne moka faktines kelionės išlaidas. Darbuotojai gali naudoti savo **atsitiktinius / kitus** dienpinigius, kad padengtų patarimus, kambarių aptarnavimą, skalbinius ar sauso valymo paslaugas svarbiems verslo susitikimams. Dienpinigių tarifas gali skirtis, priklausomai nuo to, ar darbdavys nusprendžia kompensuoti bendras apgyvendinimo ir maitinimo išlaidas, ar tik už maitinimo ir atsitiktinių incidentų išlaidas.

Dienpinigiai gali būti pagrįsti metų laiku, kelionės vieta arba abiem. Kai sukuriate dienpinigių taisyklę, galite nurodyti, kad dienpinigių normos procentas bus išskaičiuotas, jei darbuotojas gaus nemokamą maitinimą ar paslaugas. Taip pat galite nustatyti minimalų valandų skaičių ir maksimalų valandų skaičių, kurį dienpinigių tarifas gali būti taikomas darbuotojo kelionei.

Dienpinigiai apskaičiuojami kaip bendra pašalpa, siūloma per dieną, atėmus darbuotojui suteiktą maitinimo sumažėjimą (nemokamo maitinimo išlaidas).

## <a name="configure-per-diems"></a>Konfigūruoti pagal dienpinigius

Norėdami konfigūruoti dienpinigių išlaidas, atlikite šiuos veiksmus.

1. Eikite į **Išlaidų valdymo** \> **nustatymo** \> **bendrųjų** \> **išlaidų valdymo parametrai.**
2. Skirtuko **dienpinigiai** lauke Skaičiuoti maisto kiekio mažinimą **pagal dydį** pasirinkite, kaip turėtų būti apskaičiuojamas dienpinigių skaičius:

    - **Maitinimo tipas vienai kelionei** - Apskaičiuokite dienpinigius pagal įvesto valgio tipą (pusryčius, pietus ar vakarienę) ir pagal valgio sumažinimą, kuris nurodomas kiekvienam valgio tipui už dienpinigių pašalpą kelionės metu.
    - **Valgio tipas per dieną** - Apskaičiuokite dienpinigius pagal įvesto valgio tipą ir pagal valgio sumažinimą, kuris nurodomas kiekvienam valgio tipui už dienpinigius per dieną.
    - **Valgių skaičius per dieną** - Apskaičiuokite dienpinigius pagal per dieną įvestų valgių skaičių ir pagal kiekvieną dieną tiekiamų valgių skaičių.

3. Eikite į **Išlaidų valdymo** \> **nustatymo** \> **skaičiavimai ir dienpinigių vietų** kodai.\>**·**
4. Pridėkite vietas, kuriose galima naudoti dienpinigius.
5. Kiekvienoje pridėtoje **vietoje skirtuke Dienpinigiai** pasirinkite dienpinigių kursą ir valiutą, galiojančią tarp konkrečių apgyvendinimo pradžios ir pabaigos datų, maitinimo ir kitų išlaidų. Norėdami konfigūruoti dienpinigių kursus ir valiutas, eikite į **Išlaidų valdymo** \> **nustatymo** \> **skaičiavimai ir kodai** \> **Pagal dienpinigius.**

## <a name="per-diems-in-the-reimagined-expense-interface"></a>Per dienpinigius iš naujo įsivaizduojamoje išlaidų sąsajoje

Dienpinigių funkcija palaikoma atnaujintoje **išlaidų valdymo** darbo srityje 365 Finance 10.0.25 ir vėlesnėje Microsoft Dynamics versijoje.

Norėdami įjungti dienpinigius, atlikite šiuos veiksmus.

1. **Darbo srityje Funkcijų valdymas** raskite ir pasirinkite **sąraše esančią funkciją Išlaidų ataskaitos iš naujo suplanuotos**, tada pasirinkite **Įgalinti dabar**.
2. Sąraše raskite ir pasirinkite **išlaidų ataskaitos iš naujo įsivaizduojamos sąsajos** funkciją Per-diem, tada pasirinkite **Įgalinti dabar**.

## <a name="how-the-feature-works"></a>Kaip veikia funkcija

Šiame skyriuje pateikiami trijų konfigūracijos scenarijų pavyzdžiai. Kiekvieno pavyzdžio laukas **Skaičiuoti maisto kiekio sumažinimą pagal** yra nustatytas į kitą reikšmę. Visų trijų pavyzdžių atveju bendra mokėtina suma yra tokia pati, kol bus taikomas valgio sumažinimas. Po šio punkto bendra mokėtina suma kiekvienam pavyzdžiui skiriasi.

Norėdami sukurti dienpinigių išlaidas, naudojamas visiems trims pavyzdžiams, atlikite šiuos veiksmus.

1. Eikite į **Darbo sričių** \> **išlaidų valdymas**.
2. Pasirinkite **Nauja išlaidų ataskaita** arba pasirinkite esamą išlaidų ataskaitą.
3. Pridėkite naujas išlaidas. Lauke **Kategorija pasirinkite** dienpinigiai **·**. Pasirinkite kelionės vietą ir pradžios bei pabaigos datas. Apgyvendinimo, maitinimo ir atsitiktinių išlaidų (kitų išlaidų) dienpinigiai apskaičiuojami pagal pasirinktoje vietoje nustatytus dienpinigius.

    Pavyzdžiui, kaip vietą pasirenkate **Redmond (JAV).** Dienpinigiai už tą vietą yra 150 JAV dolerių (150 USD) už apgyvendinimą, USD 75 maistui ir USD 5 atsitiktiniams atvejams. Pradžios data yra sausio 10 d., O pabaigos data yra sausio 14 d. Todėl pasirinkta trukmė yra penkios dienos, kai pasirinkta konfigūracija yra kalendorinės dienos su laiku, o pasirinktas laikas prasideda ir baigiasi 12:00 pradžios ir pabaigos datomis. Štai skaičiavimai:

    - Bendra mokėtina suma = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
    - Bendros sumos miltai ir atsitiktinė dalis = 5 × (75 + 5) = USD 400

Jei kelionės metu buvo tiekiami pusryčiai, pietūs ir vakarienė, šie patiekalai turi būti apskaitomi kaip valgio sumažinimas.

### <a name="example-1-per-diem-where-meal-reductions-are-based-on-meal-type-per-trip"></a>1 pavyzdys: dienpinigiai, kai maisto sumažinimas grindžiamas valgio tipu vienai kelionei

Šiame pavyzdyje maistas sumažinamas 30 procentų pusryčiams, 30 procentų pietums ir 40 procentų vakarienei. **Puslapyje Išlaidų valdymo parametrai laukas** Skaičiuoti maisto sumažinimą **pagal** yra nustatytas kaip **Maitinimo tipas vienai kelionei**. Čia pateikiami skaičiavimai, jei darbuotojui buvo pateikti trys pusryčiai, du pietūs ir nulinės vakarienės:

- Miltų sumažinimas = (3 × \[75 × 30%\]) + (2 × \[75 × 30%\]) + 0 = (3 × 22,50) + (2 × 22,50) + 0 = 67,50 + 45 + 0 = USD 112.50
- Maitinimas ir atsitiktiniai atvejai = 400 – 112,50 = USD 287.50
- Bendra mokėtina suma = Bendra pašalpa – Maitinimo sumažinimas = 1 150 –112,50 = USD 1,037.50

![Dienpinigių išlaidos, kai valgio sumažinimas grindžiamas valgio tipu vienai kelionei.](media/1-meal-type-per-trip.png)

### <a name="example-2-per-diem-where-meal-reductions-are-based-on-meal-type-per-day"></a>2 pavyzdys: dienpinigiai, kai maisto sumažinimas grindžiamas valgio tipu per dieną

Šiame pavyzdyje maistas sumažinamas 30 procentų pusryčiams, 30 procentų pietums ir 40 procentų vakarienei. **Puslapyje Išlaidų valdymo parametrai** laukas Skaičiuoti maisto sumažinimą **pagal** yra nustatytas kaip **Valgio tipas per dieną**. Tokiu atveju dialogo lange Koreguoti išlaidas **esančiame tinklelyje Maitinimas išvalykite** **žymės langelius**, nurodančius, kokie patiekalai jums buvo pateikti kelionės metu.

Pavyzdžiui, čia pateikiami skaičiavimai, ar pusryčiai buvo pateikti pirmosioms trims kelionės dienoms:

- Dienos valgio sumažinimas kiekvienai iš pirmųjų trijų dienų = 75 × 30% = USD 22.50
- Bendras valgio sumažinimas = 3 × 22,50 = USD 67.50
- Maitinimas ir atsitiktiniai atsitikimai nuo 1 iki 3 dienų = 75–22,50 = USD 57.50
- Bendras maistas ir atsitiktiniai atvejai = valgio ir atsitiktinių atsitikimų suma per penkias dienas = 400–67,50 = USD 332.50
- Bendra mokėtina suma = Bendra mokėtina suma – Valgio sumažinimas = 1 150 – 67,50 = USD 1,082.50

![Dienpinigių išlaidos, kai valgio sumažinimas grindžiamas valgio tipu per dieną.](media/2-meal-type-per-day.png)

### <a name="example-3-per-diem-where-meal-reductions-are-based-on-number-of-meals-per-day"></a>3 pavyzdys: dienpinigiai, kuriuose maistas sumažinamas atsižvelgiant į valgių skaičių per dieną

Šiame pavyzdyje valgio sumažinimas apskaičiuojamas pagal per dieną suteiktų patiekalų skaičių (ty **puslapio Išlaidų valdymo parametrai laukas** Skaičiuoti maisto sumažinimą **pagal** dydį nustatomas kaip **Valgių skaičius per dieną**). **Dialogo lange Koreguoti išlaidas** esančiame tinklelyje Maitinimas išvalykite **žymės langelius**, nurodančius, kokie patiekalai buvo pateikti.
Tokiu atveju valgio sumažinimas grindžiamas tik suteiktų patiekalų #, o ne tiekiamo valgio tipu (pusryčiai / pietūs / vakarienė).

Čia pateikiami dienpinigių skaičiavimai, kai dienpinigiai yra USD 150 apgyvendinimui, USD 75 maistui ir USD 5 atsitiktiniams atvejams:

- **Bendra mokėtina** suma = 5 × (150 + 75 + 5) = 5 × 230 = USD 1,150
- **Vienas valgis:** valgio sumažinimas = 20% = USD 15
- **Du valgiai:** valgio sumažinimas = 50% = USD 37.50
- **Trys valgiai:** valgio sumažinimas = 100% = USD 75

Čia pateikiami maisto ir atsitiktinių leidimų **apskaičiavimai**, į kuriuos įeina atsitiktinių USD 5:

- 1 diena - Du valgiai = (75–37,50) + 5 = 37,50 + 5 = USD 42.50
- 2 diena - Du valgiai = (75–37,50) + 5 = 37,50 + 5 = USD 42.50
- 3 diena - Vienas valgis = (75–15) + 5 = 60 + 5 = USD 65
- 4 diena - Nulinis maitinimas = (75-0) + 5 = 75 + 5 = USD 80
- 5 diena - Trys valgiai = (75–75) + 5 = 0 + 5 = 0 + 5 = USD 5

- Bendras maistas ir atsitiktiniai atsitikimai = maistas ir atsitiktiniai atsitikimai 1 dieną + 2 dieną + 3 diena + 4 diena + 5 diena = USD 235
- Bendras valgio sumažinimas = valgio sumažinimas 1 dieną + 2 diena +3 diena + 4 diena+ 5 diena = 37,5+ 37,5+ 37,5+ 15 + 0 + 75 = USD 165
- Bendra mokėtina suma = Bendra išmoka – Bendras valgio sumažinimas = USD 1,150 – USD 165 = USD 985

![Dienpinigių išlaidos, kai valgio sumažinimas grindžiamas valgių skaičiumi per dieną.](media/3-number-of-meals-per-day.png)

> [!NOTE]
> Nuo "Finance" versijos 10.0.23, jei naudojate iš naujo įsivaizduojamą išlaidų sąsają, negalite sukurti dienpinigių išlaidų, kurių datos sutampa. Jei bandysite, gausite klaidos pranešimą.
