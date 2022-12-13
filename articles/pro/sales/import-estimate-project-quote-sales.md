---
title: Įvertinimų importavimas iš projekto į projekto pasiūlymo eilutę
description: Šiame straipsnyje pateikiama informacija apie tai, kaip importuoti įvertinimus iš projekto į projekto pasiūlymo eilutę.
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 61c9660f18882d12a7da8965c23b65e408256219
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824497"
---
# <a name="import-estimates-from-a-project-to-a-project-quote-line"></a>Įvertinimų importavimas iš projekto į projekto pasiūlymo eilutę 

_**Taikoma (kam):** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Jei projektas kuriamas prieš pardavimo etapą, galite pažymėti, kad į projektu pagrįstą pasiūlymo eilutę importuotumėte projekto finansinį įvertinimą.

1. Įsitikinkite, kad projektu pagrįstos pasiūlymo eilutė lauke **Projektas** turi projekto informaciją.
2. Skirtuke **Pasiūlymo eilutės išsami informacija** pasirinkite **Importuoti iš projekto įvertinimo**.
3. Dialogo lango puslapyje pažymėkite vieną iš nurodytų santraukos parinkčių.

  - **Operacijos klasė**
  - **Kategorija**
  - **Vaidmuo** 
  - **Projekto užduotis**

Remiantis jūsų pasirinkimu, kopijuojami visų operacijų klasių, įtrauktų į šią pasiūlymo eilutę, projekto įvertinimai. Norėdami patikrinti, kokios operacijos klasės įtrauktos, projektu pagrįsto pasiūlymo eilutėje pasirinkite skirtuką **Bendra** ir patikrinkite **Įtraukti laiką**, **Įtraukti išlaidas**, **Įtraukti medžiagas** ir **Įtraukti mokesčius** reikšmes.  Jei norite patikrinti, kokios užduotys įtrauktos, pasirinkite skirtuką **Apmokestinama užduotis** pasiūlymo eilutėje.

Atsižvelgiant į susietas užduotis ir įtrauktas operacijų klases, tų užduočių ir operacijų klasių derinių įvertinimai importuojami į pasiūlymo eilutę.

Kai importuojate įvertinimus, sistema pagal numatytuosius nustatymus nustato kainas pagal projekto kainoraščius, pridėtus prie pasiūlymo, ir sąskaitos išrašymo tipą, nustatytą projektu pagrįstoje pasiūlymo eilutėje. Jei užduotis, vaidmuo arba kategorija nustatomi projektu pagrįstoje pasiūlymo eilutėje kaip neapmokestinama, importuota įvertinimo eilutė bus nustatyta kaip neapmokestinama ir nebus įtraukta į pasiūlymo eilutės pasiūlymo vertę.

Kai pasiūlymo eilutėje yra eilutės išsami informacija, pasiūlymo eilutės laukai **Pasiūlymo reikšmė** ir **Numatomi mokesčiai** yra apibendrinami ir jų redaguoti negalima.

Kai pasirenkamos kelios santraukos parinktys, sistema bando apibendrinti visas pasirinktas parinktis. Tai reiškia, kad importuojamų pasiūlymo eilučių išvestis bus didesnė nei pažymėjus tik vieną santraukos parinktį.

Pavyzdžiui, jei projekte yra šios išlaidų įvertinimo eilutės.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
| Užduotis A | skrydžių; | 2020-01-10 | 4 | 400 | 1600 |
| Užduotis B | Viešbutis | 2020-01-10 | 4 | Virš 200 | 800 |
| Užduotis C | Viešbutis | 2020-01-11 | 2 | Virš 200 | 400 |

Kai vartotojas pasirenka apibendrinti pagal operacijų klasę, bus importuojama ši informacija.

| Užduotis | Kategorija. | Data | Kiekis | Vieneto kaina | Suma |
| --- | --- | --- | --- | --- | --- |
|||2020-01-10 | 3.34 | 840 | 2800 |

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
