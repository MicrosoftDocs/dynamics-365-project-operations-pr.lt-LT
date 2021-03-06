---
title: Projekto įvertinimų importavimas į projektu pagrįstą pasiūlymo eilutę
description: Šioje temoje pateikta informacija apie projekto įvertinimų importavimą į pasiūlymo eilutę.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75511f0d7ef1d2d1b3bf5cc598a8f51d0c553939
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908381"
---
# <a name="import-estimates-for-a-project-to-a-project-based-quote-line"></a>Projekto įvertinimų importavimas į projektu pagrįstą pasiūlymo eilutę

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


Jei projektas kuriamas prieš pardavimo etapą, galite pažymėti, kad į projektu pagrįstą pasiūlymo eilutę importuotumėte projekto finansinį įvertinimą.

1. Įsitikinkite, kad projektu pagrįstos pasiūlymo eilutė lauke **Projektas** turi projekto informaciją.
2. Skirtuke **Pasiūlymo eilutės išsami informacija** pasirinkite **Importuoti iš projekto įvertinimo**.
3. Dialogo lango puslapyje pažymėkite vieną iš nurodytų santraukos parinkčių.

  - **Operacijos klasė**
  - **Kategorija**
  - **Vaidmuo** 
  - **Projekto užduotis**

Remiantis jūsų pasirinkimu, kopijuojami visų operacijų klasių, įtrauktų į šią pasiūlymo eilutę, projekto įvertinimai. Norėdami patikrinti, kokios operacijų klasės įtrauktos, pasirinkite skirtuką **Bendra**, esantį projektu pagrįstoje pasiūlymo eilutėje, ir patikrinkite reikšmes parinktyse **Įtraukti laiką**, **Įtraukti išlaidas** ir **Įtraukti mokesčius**.

Kai importuojate įvertinimus, sistema pagal numatytuosius nustatymus nustato kainas pagal projekto kainoraščius, pridėtus prie pasiūlymo, ir sąskaitos išrašymo tipą, nustatytą projektu pagrįstoje pasiūlymo eilutėje. Jei vaidmuo arba kategorija nustatomi projektu pagrįstoje pasiūlymo eilutėje kaip neapmokestinama, importuota įvertinimo eilutė bus nustatyta kaip neapmokestinama ir nebus įtraukta į pasiūlymo eilutės pasiūlymo vertę.

Kai pasiūlymo eilutėje yra eilutės išsami informacija, pasiūlymo eilutės laukai **Pasiūlymo reikšmė** ir **Numatomi mokesčiai** yra apibendrinami ir jų redaguoti negalima.

Kai pasirenkamos kelios santraukos parinktys, santraukoje bandoma apibendrinti visas pasirinktas parinktis. Tai reiškia, kad importuojamų pasiūlymo eilučių išvestis bus didesnė nei pažymėjus tik vieną santraukos parinktį.

Pavyzdžiui, jei projekte yra šios išlaidų įvertinimo eilutės.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| Užduotis B | Viešbutis | 2020-01-10 | 4 | Virš 200 | 800 |
| Užduotis C | Viešbutis | 2020-01-11 | 2 | Virš 200 | 400 |

Kai vartotojas pasirenka apibendrinti pagal operacijų klasę, bus importuojama ši informacija.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| | | 2020-01-10 | 3.34 | 840 | 2800 |

Kai vartotojas pasirenka apibendrinti pagal operacijų klasę ir kategoriją, bus importuojama ši informacija.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| | Viešbutis | 2020-01-10 | 6 | Virš 200 | 1200 |

Kai vartotojas pasirenka apibendrinti pagal operacijų klasę, kategoriją ir lapo mazgo užduotį, bus importuojama ši informacija. Atkreipkite dėmesį, kad šis rezultatas tas pats, kaip projekte.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| Užduotis B | Viešbutis | 2020-01-10 | 4 | Virš 200 | 800 |
| Užduotis C | Viešbutis | 2020-01-11 | 2 | Virš 200 | 400 |