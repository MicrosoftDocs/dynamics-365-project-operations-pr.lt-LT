---
title: Operacijos kilmė – faktinių duomenų susiejimas su jų šaltiniu
description: Šiame straipsnyje paaiškinama, kaip operacijų kilmės sąvoka naudojama faktiniams duomenims susieti su pradiniais šaltinio įrašais, pvz., laiko įvedimu, išlaidų įrašu arba medžiagų naudojimo žurnalais.
author: rumant
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f1beff392ddd449a930d38016ca6083fea97953b
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921312"
---
# <a name="transaction-origins---link-actuals-to-their-source"></a>Operacijos kilmė – faktinių duomenų susiejimas su jų šaltiniu

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Operacijos kilmės įrašai sukuriami siekiant susieti faktinius duomenis su jų šaltiniu, tokiais laiko įrašais, išlaidų įrašais, medžiagų naudojimo žurnalais ir projekto SF.

Toliau pateiktame pavyzdyje parodytas tipinis „Project Operations“ projekto ciklo laiko įrašų apdorojimas.

> ![Visas apdorojimo laikas projekto operacijose.](media/basic-guide-17.png)
 
1. Pateikus laiko įrašą, sukuriamos dvi žurnalo eilutės: viena savikainai ir viena neapmokėtiems pardavimams.
2. Patvirtinus laiko įrašą, sukuriami du faktiniai duomenys: vienas savikainai ir vienas neapmokėtiems pardavimams.
3. Vartotojui kuriant projekto sąskaitą faktūrą, sąskaitos faktūros eilutės operacija sukuriama naudojant faktinės pardavimo, už kurį neišrašyta sąskaita, sumos duomenis.
4. Patvirtinus sąskaitą faktūrą, sukuriamos dvi naujos faktinės sumos: pardavimo, už kurį neišrašyta sąskaita, atšaukimo suma ir faktinė pardavimo, už kurį išrašyta sąskaita, suma.

Kiekvienas šios apdorojimo darbo eigos įvykis suaktyvina įrašų kūrimą operacijos kilmės objekte, kad padėtų sukurti ryšius tarp šių įrašų, sukurtų pagal laiko įrašą, žurnalo eilutę, faktinę ir SF eilutės informaciją.

Tolesnėje lentelėje pateikiami ankstesnės darbo eigos objekto Operacijos kilmė įrašai.

| Įvykis                        | Kilmė                   | Kilmės tipas                       | Operacija                       | Operacijos tipas         |
|------------------------------|--------------------------|-----------------------------------|-----------------------------------|--------------------------|
| Laiko įrašo pateikimas        | Laiko įrašo GUID   | Laiko įrašas                        | Žurnalo eilutės įrašo GUID (išlaidos)   | Žurnalo eilutė             |
| Laiko įrašo GUID       | Laiko įrašas               | Žurnalo eilutės įrašo GUID (pardavimas)  | Žurnalo eilutė                      |                          |
| Laiko patvirtinimas                | Žurnalo eilutės įrašo GUID | Žurnalo eilutė                      | Pardavimo, už kurį neišrašyta sąskaita, įrašo GUID        | Faktinis                   |
| Laiko įrašo GUID       | Laiko įrašas               | Pardavimo, už kurį neišrašyta sąskaita, įrašo GUID        | Faktinis                            |                          |
| Žurnalo eilutės įrašo GUID     | Žurnalo eilutė             | Faktinės išlaidų sumos įrašo GUID           | Faktinis                            |                          |
| Laiko įrašo GUID       | Laiko įrašas               | Faktinės išlaidų sumos įrašo GUID           | Faktinis                            |                          |
| Sąskaitos faktūros kūrimas             | Laiko įrašo GUID   | Laiko įrašas                        | Sąskaitos faktūros eilutės operacijos GUID     | Sąskaitos faktūros eilutės operacija |
| Žurnalo eilutės įrašo GUID     | Žurnalo eilutė             | Sąskaitos faktūros eilutės operacijos GUID     | Sąskaitos faktūros eilutės operacija          |                          |
| Sąskaitos faktūros patvirtinimas         | Sąskaitos faktūros eilutės GUID        | Sąskaitos faktūros eilutė                      | Pardavimo, už kurį išrašyta sąskaita, įrašo GUID          | Faktinis                   |
| Sąskaitos faktūros GUID                 | Sąskaita faktūra                  | Pardavimo, už kurį išrašyta sąskaita, įrašo GUID          | Faktinis                            |                          |
| Sąskaitos faktūros eilutės informacijos GUID     | Sąskaitos faktūros eilutės informacija      | Pardavimo, už kurį išrašyta sąskaita, įrašo GUID          | Faktinis                            |                          |
| Laiko įrašo GUID       | Laiko įrašas               | Pardavimo, už kurį išrašyta sąskaita, įrašo GUID          | Faktinis                            |                          |
| Žurnalo eilutės įrašo GUID     | Žurnalo eilutė             | Pardavimo, už kurį išrašyta sąskaita, įrašo GUID          | Faktinis                            |                          |
| Laiko įrašo GUID       | Laiko įrašas               | Pardavimo, už kurį neišrašyta sąskaita, atšaukimo GUID      | Faktinis                            |                          |
| Žurnalo eilutės įrašo GUID     | Žurnalo eilutė             | Pardavimo, už kurį neišrašyta sąskaita, atšaukimo GUID      | Faktinis                            |                          |
| Sąskaitos faktūros juodraščio koregavimas     | Senos sąskaitos faktūros eilutės informacijos GUID             | Sąskaitos faktūros eilutės operacija          | Pakoreguotos sąskaitos faktūros eilutės informacijos GUID               | Sąskaitos faktūros eilutės operacija |
| Senos sąskaitos faktūros eilutės GUID                  | Sąskaitos faktūros eilutė             | Pakoreguotos sąskaitos faktūros eilutės informacijos GUID               | Sąskaitos faktūros eilutės operacija          |                          |
| Senos sąskaitos faktūros GUID             | Sąskaita faktūra                  | Pakoreguotos sąskaitos faktūros eilutės informacijos GUID               | Sąskaitos faktūros eilutės operacija          |                          |
| Laiko įrašo GUID       | Laiko įrašas               | Pakoreguotos sąskaitos faktūros eilutės informacijos GUID               | Sąskaitos faktūros eilutės operacija          |                          |
| Žurnalo eilutės įrašo GUID     | Žurnalo eilutė             | Pakoreguotos sąskaitos faktūros eilutės informacijos GUID               | Sąskaitos faktūros eilutės operacija          |                          |
| Patvirtintos sąskaitos faktūros koregavimas | Senos sąskaitos faktūros eilutės informacijos GUID             | Sąskaitos faktūros eilutės operacija          | Atšauktos pardavimo, už kurį išrašyta sąskaita, faktinės sumos GUID | Faktinis                   |
| Senos sąskaitos faktūros eilutės GUID                  | Sąskaitos faktūros eilutė             | Atšauktos pardavimo, už kurį išrašyta sąskaita, faktinės sumos GUID | Faktinis                            |                          |
| Senos sąskaitos faktūros GUID             | Sąskaita faktūra                  | Atšauktos pardavimo, už kurį išrašyta sąskaita, faktinės sumos GUID | Faktinis                            |                          |
| Laiko įrašo GUID       | Laiko įrašas               | Atšauktos pardavimo, už kurį išrašyta sąskaita, faktinės sumos GUID | Faktinis                            |                          |
| Žurnalo eilutės įrašo GUID     | Žurnalo eilutė             | Atšauktos pardavimo, už kurį išrašyta sąskaita, faktinės sumos GUID | Faktinis                            |                          |
| Senos sąskaitos faktūros eilutės informacijos GUID                 | Sąskaitos faktūros eilutės operacija | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |
| Senos sąskaitos faktūros eilutės GUID                  | Sąskaitos faktūros eilutė             | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |
| Senos sąskaitos faktūros GUID             | Sąskaita faktūra                  | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |
| Laiko įrašo GUID       | Laiko įrašas               | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |
| Žurnalo eilutės įrašo GUID     | Žurnalo eilutė             | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |
| Pakoreguotos sąskaitos faktūros eilutės informacijos GUID          | Sąskaitos faktūros eilutės operacija | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |
| Koregavimo sąskaitos faktūros eilutės GUID           | Sąskaitos faktūros eilutė             | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |
| Koregavimo sąskaitos faktūros GUID      | Sąskaita faktūra                  | Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID    | Faktinis                            |                          |


Toliau pateiktoje iliustracijoje rodomi saitai, sukurti tarp faktinių ir jų šaltinių įvairiuose renginiuose, naudojant laiko įrašų pavyzdį projekto operacijose.

> ![Kaip faktiniai duomenys yra susieti su šaltinio įrašais "Project Operations".](media/TransactionOrigins.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
