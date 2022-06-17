---
title: Išlaidų valdymo parametrų konfigūravimas
description: Šiame straipsnyje aprašomi parametrai, kontroliuojantys bendrą išlaidų valdymo elgesį.
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 6432e119f38071b028c013561bab99820778a11d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931478"
---
# <a name="configure-expense-management-parameters"></a>Išlaidų valdymo parametrų konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šiame straipsnyje aprašomi parametrai, kontroliuojantys bendrą išlaidų valdymo elgesį.

## <a name="general"></a>Bendroji informacija

| Laukas                                                    | Aprašo |
|----------------------------------------------------------|-------------|
| Standartinis kilometražo tarifas                                 | Įveskite nuvažiuoto atstumo išlaidų kompensavimo tarifą. Šis tarifas padauginamas iš kilometražo, kuris nustatytas išlaidoms, kad būtų galima apskaičiuoti sumą, kompensuotą kelionės išlaidoms. |
| Išlaidų paskirties tikrinimas                                 | Įjunkite šią parinktį, kad apribotumėte vartotojus iki esamo reikšmių rinkinio, sukonfigūruoto lauke **Išlaidų ataskaitos paskirtis**, kai jie kuria išlaidų ataskaitas. |
| Asmeninės išlaidos, kurias sumoka                                | Pažymėkite, kas atsakingas už bet kokios kreditinės kortelės operacijų sumų, suskirstytų kaip asmeninės, mokėjimą. |
| Visų išlaidų ataskaitų rodymas funkcijoje „drillback“               | Pažymėkite šią parinktį, kad būtų rodomos visos išlaidų ataskaitos išlaidos, kai pirminio dokumento duomenys peržiūrimi pagal tam tikrą kvitą, kuris buvo sugeneruotas publikavus išlaidų ataskaitą. |
| Būtina išankstinė kelionės registracija                 | Pažymėkite šią parinktį, kad reikalautumėte, jog kelionės paraiška būtų pateikta ir patvirtinta prieš darbuotojui pateikiant išlaidų ataskaitą. |
| Leisti redaguoti paskirstymus prieš registruojant            | Pažymėkite, ar išlaidų ataskaitos paskirstymą galima redaguoti prieš užregistruojant. |
| Išlaidų valdymo strategijos vertinimas                     | Pažymėkite, kada išlaidos įvertinamos, kad nustatytumėte, ar buvo pažeista išlaidų strategija. Išlaidas galima įvertinti už pažeidimus, kai įvedami ir įrašomi išlaidų įrašai arba kai išlaidos pateikiamos tvirtinti. Strategijos taisyklės, skirtos kvitams, bus įvertinamos, kai išsaugoma išlaidų eilutė. |
| Leisti vidinės įmonės išlaidų eilutes                         | Pažymėkite, ar kitų juridinių objektų išlaidas galima įvesti išlaidų ataskaitoje. |
| Leisti redaguoti kredito kortelės išlaidų valiutos kursą | Pažymėkite šią parinktį, kad leistumėte vartotojui redaguoti importuotų kredito kortelių išlaidų valiutos kursą. |
| Kelių lygių hierarchijos laukų rodymas                  | Pažymėkite, kurie tvirtintojo laukai rodomi, kai darbo eigos priskyrimo tipas nustatomas į hierarchiją, o pasirinkimas **Hierarchija** nustatytas naudoti patvirtinimo hierarchiją, išlaidų kelių lygių patvirtinimą. Kai darbo eigoje naudojama kelių lygių patvirtinimo hierarchija, pažymėti laukai bus rodomi išlaidų ataskaitoje ir gali būti redaguojami. |
| Įveskite darbuotojo kredito kortelės numerį                        | Pažymėkite, ar galima įvesti 15 simbolių arba 16 simbolių numerį, kuris bus išsaugotas lauke **Kortelės ID**, esančiame darbuotojo puslapyje **Kreditinės kortelės**. |
| Patikrinkite kelionės paraiškos paskirtį                      | Įjunkite šią parinktį, kad apribotumėte vartotojus iki esamo reikšmių rinkinio, sukonfigūruoto lauke **Išlaidų ataskaitos paskirtis**, kai jie kuria kelionės paraiškas. |

## <a name="financial"></a>Finansų

| Laukas                                                                                    | Aprašo |
|------------------------------------------------------------------------------------------|-------------|
| DK dienos žurnalo pavadinimas                                                                | Pažymėkite DK žurnalo, su kuriuo registruojamos patvirtintos išlaidų ataskaitos, pavadinimą. |
| Mokesčių atkūrimo iš išlaidų įjungimas                                                        | Pažymėkite šią parinktį, kad būtų įjungtas išlaidų mokesčio atkūrimas, skirtas išlaidoms, už kurias norima susigrąžinti sumokėtą PVM. Šios pasirinkties negalima pažymėti, jei JAV pardavimo mokestis ir naudojimo mokesčių taisyklės yra įjungtos. |
| Iš karto skelbkite avansinius mokėjimus                                                           | Pažymėkite šią parinktį, kad paskelbtumėte patvirtintą avansinį mokėjimą, kai užbaigtas mokėjimo ir pervedimo procesas. Jei ši parinktis nepažymėta, mokėjimo ir pervedimo procesas generuoja neregistruotą bendrąjį žurnalą. |
| Apskaitos datos taisymas publikavimo metu                                                   | Pažymėkite šią parinktį, kad atnaujintumėte apskaitos datą, kai išlaidos registruojamos, jei dabartinis laikotarpis yra sulaikytas arba uždarytas. Apskaitos data nustatoma kitam atviram laikotarpiui. |
| Operacijų grupavimo pagal korespondentinę saskaitą, nurodytą mokėjimo būde, leidimas       | Pažymėkite šią parinktį, jei norite sumuoti išlaidų ataskaitos išlaidų operacijas pagal korespondentinę sąskaitą, nurodytą išlaidų mokėjimo būde. |
| Mokesčiai įtraukti                                                                             | Pažymėkite šią parinktį, jei pagal numatytuosius nustatymus į išlaidų sumą norite įtraukti pardavimų mokestį. |
| Kelionių paraiškų uždarymo apsunkinimų lengvinimas                                      | Pažymėkite šią parinktį, kad palengvintumėte apsunkintas lėšas, kai patvirtintos kelionės paraiška uždaryta. |
| Leisti kelionės paraiškos pateikimą, kai viršytas biudžetas, biudžeto registrui ir projekto biudžetui | Pažymėkite šią parinktį, kad darbuotojai galėtų pateikti kelionės paraiškas patvirtinimui, net jei jie viršija leistiną biudžetą, nustatytą biudžeto registre, arba leistiną projekto biudžetą. |
| Leisti išlaidų ataskaitos pateikimą, kai viršytas biudžetas, biudžeto registrui ir projekto biudžetui     | Pažymėkite šią parinktį, kad darbuotojai galėtų pateikti išlaidų ataskaitas patvirtinimui, net jei jie viršija leistiną biudžetą, nustatytą biudžeto registre, arba leistiną projekto biudžetą. |
| Leisti išlaidų ataskaitos patvirtinimą, kai viršytas biudžetas, tik biudžeto registrui                 | Pažymėkite šią parinktį, jei norite leisti tvirtintojams patvirtinti išlaidų ataskaitas, kurios viršija leistiną biudžetą, nustatytą biudžeto registre. |

## <a name="per-diem"></a>Dienpinigiai

| Laukas                                 | Aprašo |
|---------------------------------------|-------------|
| Minimalios valandos dienpinigiams            | Įveskite numatytąjį minimalų valandų skaičių, kurį darbuotojas turi atlikti, kad gautų dienpinigius už su kelionėmis susijusias išlaidas. Ši reikšmė naudojama kaip numatytoji reikšmė tik lauko **Minimalios valandos** dienpinigių pakopoms. |
| Maisto procentas                          | Įveskite numatytąją dienpinigių, skirtų maistui, procentinę dalį, kuri naudojama pirmą ir paskutinę su kelione susijusių išlaidų dieną, kai laukas **Skaičiuoti nuolaidą maistui pagal** nustatytas į **Maisto tipas per dieną** arba **Maisto kiekis per dieną**. Pirmos ir paskutinės dienos darbo diena gali būti trumpesnė nei standartinė darbo diena. Todėl šių dienų dienpinigių suma gali skirtis nuo standartinės sumos. Jei procentinė dalis nustatyta į **0** (nulis), pirmosios ir paskutinės dienos atskaitymai bus 0,00. |
| Viešbučio procentas                         | Įveskite numatytąją dienpinigių, skirtų viešbučiams, procentinę dalį, kuri naudojama pirmą ir paskutinę su kelione susijusių išlaidų dieną. Pirmos ir paskutinės dienos darbo diena gali būti trumpesnė nei standartinė darbo diena. Todėl šių dienų dienpinigių suma gali skirtis nuo standartinės sumos. Jei procentinė dalis nustatyta į **0** (nulis), pirmosios ir paskutinės dienos atskaitymai bus 0,00. |
| Kiti procentai                         | Įveskite numatytąją dienpinigių, skirtų kitoms išlaidoms, procentinę dalį, kuri naudojama pirmą ir paskutinę su kelione susijusių išlaidų dieną. Pirmos ir paskutinės dienos darbo diena gali būti trumpesnė nei standartinė darbo diena. Todėl šių dienų dienpinigių suma gali skirtis nuo standartinės sumos. Jei procentinė dalis nustatyta į **0** (nulis), pirmosios ir paskutinės dienos atskaitymai bus 0,00. |
| Pusryčių procentinės dalies sumažinimas | Įveskite sumą, kuria sumažinami pusryčiams skirti dienpinigiai. Pavyzdžiui, jei darbuotojas gauna nemokamus pusryčius, galite sumažinti dienpinigių sumą iki 10 procentų. |
| Pietų procentinės dalies sumažinimas     | Įveskite sumą, kuria sumažinami pietums skirti dienpinigiai. Pavyzdžiui, jei darbuotojas gauna nemokamus pietus, galite sumažinti dienpinigių sumą iki 15 procentų. |
| Vakarienės procentinės dalies sumažinimas    | Įveskite sumą, kuria sumažinami vakarienei skirti dienpinigiai. Pavyzdžiui, jei darbuotojas gauna nemokamą vakarienę, galite sumažinti dienpinigių sumą iki 25 procentų. |
| Apskaičiuokite maisto nuolaidą pagal           | Nurodykite, kaip sistema turėtų apskaičiuoti maistui skirtų dienpinigių mažinimą, pažymėdami, ar sumažinimas pagrįstas maitinimo tipu kelionėje ar per dieną, ar jis pagrįstas per dieną leidžiamų patiekalų skaičiumi. |
| Dienpinigių apvalinimas                     | Pažymėkite apvalinimo tipą, naudojamą dienpinigiams. Jei pažymėsite įprastą apvalinimą, bet kokios dienpinigių išlaidos, kurių suma 0,50, yra suapvalinamos iki 1,00, o visos dienpinigių išlaidos, kurių suma mažesnė už 0,50, yra suapvalinamos iki 0,00. |
| Dienpinigių skaičiavimas          | Pažymėkite, ar dienpinigių suma priklauso nuo kalendorinės dienos, ar nuo 24 valandų laikotarpio. |

## <a name="fax-cover-pages"></a>Faksogramos tituliniai puslapiai

| Laukas                          | Aprašo |
|--------------------------------|-------------|
| Instrukcijos                   | Įveskite instrukcijas, kurių darbuotojai turi laikytis kurdami faksogramos, kuri naudojama su išlaidų ataskaita susijusiems kvitams siųsti, titulinį puslapį. Norėdami įvesti kalbai būdingą tekstą, kuris bus rodomas, pagal vartotojo kalbą pasirinkite **Vertimai**. |
| Vartotojo ID (brūkšninio kodo informacija) | Pažymėkite šią parinktį, jei norite išsaugoti unikalų darbuotojo identifikatorių brūkšniniame kode, naudojamą faksogramos tituliniame puslapyje. |
| Brūkšninis kodas                       | Pažymėkite brūkšninį kodą, naudojamą faksogramos tituliniame puslapyje. Išlaidų valdyme palaikomi brūkšniniai kodai 39 ir 128. |

## <a name="anti-corruption"></a>Antikorupcija

| Laukas                                 | Aprašo |
|---------------------------------------|-------------|
| Rodyti antikorupcijos atestaciją   | Pažymėkite šią parinktį, jei norite, kad sukūrus išlaidų ataskaitą, būtų rodomas antikorupcinis tekstas. Tada galima įjungti tam tikras išlaidų kategorijas, kurioms esant išlaidų ataskaitoje reikės pažymėti antikorupcijos atestaciją. Pavyzdžiui, dovanų kategorijai, susijusiai su vyriausybinėmis valdžios lėšomis, gali reikėti, kad darbuotojas patvirtintų, jog išlaidos atitinka įmonės politiką, susijusią su vyriausybės pareigūnais. |
| Antikorupcinis pranešimas peteikėjui | Įveskite tekstą, kuris turėtų būti rodomas darbuotojui, kuriančiam išlaidų ataskaitą. Norėdami įvesti kalbai būdingą tekstą, kuris bus rodomas, pagal vartotojo kalbą pasirinkite **Vertimai**. |
| Antikorupcinis pranešimas tvirtintojui  | Įveskite tekstą, kuris turėtų būti rodomas tvirtintojui, kai sukuriama išlaidų ataskaita. Norėdami įvesti kalbai būdingą tekstą, kuris bus rodomas, pagal vartotojo kalbą pasirinkite **Vertimai**. |


[!INCLUDE[footer-include](../includes/footer-banner.md)]