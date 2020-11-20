---
title: Įvertinimo importavimas į projektais pagrįstą sutarties eilutę
description: Šioje temoje pateikta informacija apie projekto įvertinimų importavimą į sutarties eilutę.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f2b9cbb4cce1691f262c85d95849e01f1a812d51
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081071"
---
# <a name="import-an-estimate-to-a-project-based-contract-line"></a>Įvertinimo importavimas į projektais pagrįstą sutarties eilutę

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Programoje „Dynamics 365 Project Operations“ galite importuoti įvertinimus iš projekto į projektais pagrįstą sutarties eilutę.

1. Patikrinkite, ar laukas **Projektas** projektais pagrįstoje sutarties eilutėje yra užpildytas.
2. Skirtuko **Sutarties eilutės informacija** papildomame tinklelyje pasirinkite **Importuoti iš projekto įvertinimo**. Atidaromas dialogo lango puslapis su santraukos parinktimis. Galimos santraukos parinktys yra **Operacijos klasė** , **Kategorija** , **Vaidmuo** ir **Projekto užduotis**. Remiantis santraukos pasirinkimais, kopijuojami visų operacijų klasių, įtrauktų į šią sutarties eilutę, projekto įvertinimai. 
3. Norėdami patikrinti, kokios operacijų klasės įtrauktos, sutarties eilutės skirtuke **Bendra** patikrinkite reikšmes laukuose **Įtraukti laiką** , **Įtraukti išlaidas** ir **Įtraukti mokesčius**.

Kai importuojate įvertinimus, programa pagal numatytuosius nustatymus nustato kainas pagal projekto kainoraščius, pridėtus prie sutarties, ir sąskaitos išrašymo tipą, nustatytą projektais pagrįstoje sutarties eilutėje. Jei vaidmuo arba kategorija nustatoma projektais pagrįstoje sutarties eilutėje kaip neapmokestinama, to vaidmens arba kategorijos importuota įvertinimo eilutė yra neapmokestinama ir nebus įtraukta į sutarties eilutės sutarties vertę.

Kai sutarties eilutėje yra eilutės išsami informacija, sutarties eilutės laukai **Sutarties reikšmė** ir **Numatomi mokesčiai** yra apibendrinami ir jų redaguoti negalima.

Kai pasirenkamos kelios santraukos parinktys, sistema bando apibendrinti visas pasirinktas parinktis. Suvestinės rezultatuose yra daugiau importuotų sutarties eilučių, nei pasirinkus tik vieną santraukos parinktį.

Pavyzdžiui, jei projekte yra šios išlaidų įvertinimo eilutės.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| Užduotis B | Viešbutis | 2020-01-10 | 4 | Virš 200 | 800 |
| Užduotis C | Viešbutis | 2020-01-11 | 2 | Virš 200 | 400 |

Kai vartotojas pasirenka apibendrinti pagal **operacijų klasę** , bus importuojama ši informacija.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| &nbsp;  | &nbsp;  | 2020-01-10 | 3.34 | 840 | 2800 |

Kai vartotojas pasirenka apibendrinti pagal **operacijų klasę** ir **kategoriją** , bus importuojama ši informacija.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| &nbsp;  | Viešbutis | 2020-01-10 | 6 | Virš 200 | 1200 |

Kai vartotojas pasirenka apibendrinti pagal **operacijų klasę** , **kategoriją** ir **lapo mazgo užduotį** , bus importuojama ši informacija. Atkreipkite dėmesį, kad šis rezultatas tas pats, kaip projekte.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| Užduotis B | Viešbutis | 2020-01-10 | 4 | Virš 200 | 800 |
| Užduotis C | Viešbutis | 2020-01-11 | 2 | Virš 200 | 400 |