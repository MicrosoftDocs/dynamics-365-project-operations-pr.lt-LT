---
title: Kelių valiutų scenarijai (versija 3.x)
description: Šioje temoje pateikta informacija apie kelių valiutų scenarijus.
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/26/2018
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
ms.openlocfilehash: 7be029eeca3129d30f4bec1bf9b180a0a5122a86
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080946"
---
# <a name="multiple-currency-scenarios"></a>Kelių valiutų scenarijai

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Microsoft Dynamics 365 yra dvi valiutų sąvokos:

- **Operacijos valiuta** – valiuta, kuria vykdomas operacija. 
- **Pagrindinė valiuta** – Dynamics 365 egzemplioriaus valiuta. Ši valiuta nustatoma, Dynamics 365 egzemplioriaus aptarnavimo metu. Jos keisti negalima.

Pavyzdžiui, Danys JAV pardavė 100 marškinėlių klientui Jungtinėje Karalystėje po 15 svarų sterlingų (GBP) už vienetą. Sekančioje lentelėje parodoma, kaip ši operacija įrašoma Produkto Užsakymas objekte.

| Produktas | Kiekis | Vieneto kaina | Valiuta | Kiekis | Valiutos kursas | Pradinė vieneto kaina| Suma (pagrindinė)|
|---------|----------|----------------|----------|--------|---------------|----------------------|--------------|
| Marškinėliai | 100      | 15             | GBP      | 1500   | 0.94          | $17,25               | $1,725       |

Stulpelyje **Valiuta** rodoma operacijos valiuta, t.y. valiuta, kuria įvyko pardavimas. **Keitimo kursas** stulpelyje nurodomas operacijos valiutos ir bazinės valiutos keitimo kursas. Bazinė valiuta yra JAV doleris (USD). Ši valiuta buvo nustatyta, kai Dynamics 365 egzempliorius buvo aptarnautas.
Kaip rodo lentelė, kiekviena operacija įrašoma operacijos valiuta ir pagrindine valiuta. Dynamics 365 naudoja valiutos kursą, kad apskaičiuotų bazinę valiutos sumą.

## <a name="project-service-automation-extensions"></a>Project Service Automation plėtiniai

Dynamics 365 Project Service Automation įtakoja operacijos valiutą, nes verslo sandoriai paprastai turi du aspektus: kaštai ir pardavimas.

Toliau nurodyti objektai laikomi verslo sandoriais:

- Pasiūlymo eilutės informacija
- Projekto sutarties eilutės informacija
- Įvertinimo eilutė
- Žurnalo eilutė
- Sąskaitos faktūros eilutės informacija
- Faktinis

Kiekviename iš šių objektų yra įrašas, nurodantis išlaidų sumą arba pardavimo sumą. Bet kurio Dynamics 365 objekto, kuriame yra laukas **Suma** , kiekviename įraše nurodomos sumos operacijos ir bazine valiuta. 

PSA išplečia išlaidų ir pardavimo operacijų valiutos sampratą sekančiais būdais:

- Laiko operacijų išlaidų operacijos valiuta visada gaunama iš organizacijos vieneto, kuriam priklauso arba kuris vadovauja projektui, valiutos. Šis organizacijos vienetas vadinamas sutarties vienetu.
- Laiko ir išlaidų operacijų pardavimo operacijos valiuta visada gaunama iš projekto sutarties valiutos.
- Sąnaudų operacijos valiuta išlaidoms gaunama iš valiutos, kuria buvo sukurtas išlaidų įrašas.

## <a name="multiple-currency-scenario"></a>Kelių valiutų scenarijus

Šiame skyriuje aprašomas projekto, kurį Danys JK pristato klientui, kuris pavadintas Fabrikam, Japonija, pavyzdys. Štai kaip scenarijus buvo sudarytas:

1. GBP ir Japonijos jena (JPY) nustatomos **Parametrai** \> **Verslo Valdymas** \> **Valiutos**. 
2. Kliento sąskaita, pavadinta **Fabrikam-Japonija** , sukuriama, o JPY nustatoma kaip sąskaitos valiuta.
3. Nustatomas organizacijos vienetas, pavadintas **Danys JK** , o GBP nustatoma kaip valiuta.
4. Sukuriama projekto sutartis, kurioje **Danys** yra nurodytas kaip sutarties vienetas, o **Fabrikam – Japonija** nurodytas kaip klientas.
5. Sukuriamos projekto sutarties eilutės, remiantis įvairių projekto operacijų klasių atsiskaitymo tvarka, pvz., atsiskaitymas už laiką lyginant su atsiskaitymu už išlaidas.
6. Projektas sukurtas, kai **Danys** yra nurodytas kaip sutarties vienetas. Šis projektas sukurtas ir susietas su projekto sutarties eilutėmis.


Atliekant vertinimą, naudojant pasiūlymo eilutės duomenis, projekto sutarties eilutės duomenis arba tvarkaraščio įvertinimo eilutėje, visada sukuriami du įrašai objekte. Viena eilutė skirta išlaidoms, o kita eilutė skirta pardavimams.

- Pagal numatytuosius parametrus operacijos valiuta, esanti sąnaudų įraše, nustatoma tokia, kaip projekto sutarties vieneto valiuta. Šiame pavyzdyje valiuta yra GBP.
- Pagal numatytuosius parametrus transakcijos valiuta, esanti pardavimų įraše, nustatoma kaip projekto sutarties vieneto valiuta. Šiame pavyzdyje valiuta yra JPY.

Kai faktiniai duomenys sukuriami laikui naudojant laiko įrašą arba žurnalo eilutę, nutinka sekančiai:

- Pagal numatytuosius parametrus operacijos valiuta, esanti sąnaudų įraše, nustatoma kaip projekto sutarties vieneto valiuta.
- Pagal numatytuosius parametrus transakcijos valiuta, esanti pardavimų įraše, nustatoma kaip projekto sutarties vieneto valiuta.

Kai faktiniai duomenys sukuriami išlaidoms naudojant išlaidų įrašą arba žurnalo eilutę, nutinka sekančiai:

- Galite įrašyti išlaidų sumą bet kuria valiuta. Pažymėkite valiutą, naudodami valiutos parinkimo įrankš, esantį **Išlaidų įvedimas** puslapyje arba **Žurnalo eilutė** puslapyje. Pagal numatytuosius nustatymus sąnaudų įraše operacijos valiuta nustatoma tokia, kaip išlaidų įvedimo valiuta. 
- Pagal numatytuosius nustatymus pardavimo įraše operacijos valiuta yra projekto sutarties valiuta. Kad nustatytų šią valiutą, sistema pirma konvertuoja operacijų sumą vartotojo įvesta valiuta į bazinę valiutą. Tada suma konvertuojama į projekto sutarties valiutą. 

### <a name="computing-roll-ups-when-project-actuals-are-recorded-in-multiple-transaction-currencies"></a>Kompiuterio duomenys kaupiami kai projekto faktiniai duomenys įrašomi keliomis operacijų valiutomis

Dynamics 365 automatiškai apdoroja kaupiamas sumas skirtingomis valiutomis. Štai pavyzdys.

| Operacijos klasė | Operacijos tipas| Date   | Ištekliai | Operacijos kategorija | Kiekis | Vieneto kaina | Kiekis      | Valiutos kursas | Suma bazine valiuta |
|-------------------|------------------|--------|----------|----------------------|----------|--------------|-------------|---------------|----------------|
| Time              | Neišrašytas pardavimas   | Birželio 14 d. | Darius  |                      | 8 val.    | 20,000 JPY    | 160,000 JPY | 123           | 1300,81 USD    |
| Time              | Neišrašytas pardavimas   | Birželio 15 d. | Darius  |                      | 8 val.    | 20,000 JPY    | 160,000 JPY | 123           | 1300,81 USD    |
| Išlaidos           | Neišrašytas pardavimas   | Birželio 16 d. | Darius  | viešbučių;                | 1 ea     | 250 EUR      | 250 EUR     | 0.94          | 265,95 USD     |
| Išlaidos           | Neišrašytas pardavimas   | Birželio 17 d. | Darius  | Automobilio nuoma           | 1 ea     | 150 EUR      | 150 EUR     | 0.94          | 159,57 USD     |

Norėdami apskaičiuoti bendrąją neišrašytą projekto vertę, galite sukurti kaupiamą lauką laukui **Suma** visiems susijusiems neišrašytų pardavimų faktiniams duomenims. Kaupiamas laukas yra Dynamics 365 konstruktas, leidžiantis sparčiąsias formules su susijusiais įrašais.
