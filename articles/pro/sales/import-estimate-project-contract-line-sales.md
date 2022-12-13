---
title: Įvertinimų importavimas iš projekto į projekto sutarties eilutę
description: Šiame straipsnyje pateikta informacija apie projekto finansinių įvertinimų importavimą į sutarties eilutę.
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 73ae0ccbb5372c9dfbc28ac154094c89add0913d
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824685"
---
# <a name="import-estimates-from-a-project-to-a-project-contract-line"></a>Įvertinimų importavimas iš projekto į projekto sutarties eilutę

_**Taikoma:**  "Lite" diegimas – sandoris su proforma sąskaitų faktūrų išrašymu, "Project Operations" ištekliams / be atsargų pagrįstiems scenarijams_ _

Programoje „Dynamics 365 Project Operations“ galite importuoti įvertinimus iš projekto į projektu pagrįstą sutarties eilutę.

1. Patikrinkite, ar laukas **Projektas** projektais pagrįstoje sutarties eilutėje yra užpildytas.
2. Skirtuko **Sutarties eilutės informacija** papildomame tinklelyje pasirinkite **Importuoti iš projekto įvertinimo**. Atidaromas dialogo lango puslapis su santraukos parinktimis. Galimos santraukos parinktys yra **Operacijos klasė**, **Kategorija**, **Vaidmuo** ir **Projekto užduotis**.
3. Remiantis santraukos pasirinkimais, kopijuojami visų operacijų klasių ir užduočių, įtrauktų į šią sutarties eilutę, projekto įvertinimai. Norėdami patikrinti, kokios operacijų klasės įtrauktos, projektais pagrįstos sutarties eilutės skirtuke **Bendra** patikrinkite reikšmes laukuose **Įtraukti laiką**, **Įtraukti išlaidas** ir **Įtraukti mokesčius**. 
4. Jei norite patikrinti, kokios užduotys įtrauktos, pasirinkite skirtuką **Apmokestinama užduotis** sutarties eilutėje. Atsižvelgiant į susietas užduotis, kurių laukas **Įtrauktos operacijų klasės** nustatytas į parinktį **Taip**, visi tų užduočių ir operacijų klasių derinių įvertinimai importuojami į sutarties eilutę.

Kai importuojate įvertinimus, sistema pagal numatytuosius nustatymus nustato kainas pagal projekto kainoraščius, pridėtus prie sutarties, ir sąskaitos išrašymo tipą, nustatytą projektais pagrįstoje sutarties eilutėje. Jei vaidmuo arba kategorija nustatoma projektais pagrįstoje sutarties eilutėje kaip neapmokestinama, to importuota įvertinimo eilutė yra neapmokestinama ir nebus įtraukta į sutarties eilutės sutarties vertę.

Kai sutarties eilutėje yra eilutės išsami informacija, sutarties eilutės laukai **Sutarties reikšmė** ir **Numatomi mokesčiai** yra apibendrinami ir jų redaguoti negalima.

Kai pasirenkamos kelios santraukos parinktys, sistema bando apibendrinti visas pasirinktas parinktis. Suvestinės rezultatuose yra daugiau importuotų sutarties eilučių, nei pasirinkus tik vieną santraukos parinktį.

Pavyzdžiui, jei projekte yra šios išlaidų įvertinimo eilutės.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| Užduotis B | Viešbutis | 2020-01-10 | 4 | Virš 200 | 800 |
| Užduotis C | Viešbutis | 2020-01-11 | 2 | Virš 200 | 400 |

Kai vartotojas pasirenka apibendrinti pagal **operacijų klasę**, bus importuojama ši informacija.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| &nbsp; | &nbsp; | 2020-01-10 | 3.34 | 840 | 2800 |

Kai vartotojas pasirenka apibendrinti pagal **operacijų klasę** ir **kategoriją**, bus importuojama ši informacija.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| &nbsp;| Viešbutis | 2020-01-10 | 6 | Virš 200 | 1200 |

Kai vartotojas pasirenka apibendrinti pagal **operacijų klasę**, **kategoriją** ir **lapo mazgo užduotį**, bus importuojama ši informacija. Atkreipkite dėmesį, kad šis rezultatas tas pats, kaip projekte.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| Užduotis B | Viešbutis | 2020-01-10 | 4 | Virš 200 | 800 |
| Užduotis C | Viešbutis | 2020-01-11 | 2 | Virš 200 | 400 |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
