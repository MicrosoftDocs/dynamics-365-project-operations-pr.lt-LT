---
title: Verslo operacijos
description: Šioje temoje pateikiama informacija apie verslo operacijas.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: 28555f29e65c11255c8966f3d4b900512aa01c30fef0a9cef3a3794edaf92a0b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987536"
---
# <a name="business-transactions"></a>Verslo operacijos

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Programoje „Dynamics 365 Project Service Automation“ *verslo operacija* yra abstrakti koncepcija, nereiškianti jokio objekto. Tačiau kai kuriems bendriesiems objektų laukams ir procesams gali būti naudojama verslo operacijų koncepcija. Ši abstrakti koncepcija naudojama toliau nurodytiems objektams.

- Pasiūlymo eilučių informacija
- Sutarties eilučių informacija
- Įvertinimo eilutės
- Žurnalo eilutės
- Faktinės

Iš visų šių objektų pasiūlymo eilučių informacija, sutarties eilučių informacija ir įvertinimo eilutės siejamos su projekto ciklo įvertinimo etapu. Žurnalo eilučių ir faktinių duomenų objektai siejami su projekto ciklo vykdymo etapu.

PSA šių penkių objektų įrašus laiko verslo operacijomis. Vienintelis skirtumas yra tas, kad objektų, susietų su įvertinimo etapu, įrašai yra laikomi finansinėmis prognozėmis, o objektų, susietų su vykdymo etapu, įrašai – jau įvykusiais finansiniais faktais.

Norėdami sužinoti daugiau žr. [Įvertinimai](estimates.md) ir [Faktiniai duomenys](actuals.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Unikalios verslo operacijų koncepcijos
Toliau nurodytos koncepcijos yra unikalios verslo operacijų koncepcijos:

- Operacijos tipas
- Operacijos klasė
- Operacijos kilmė
- Operacijos ryšys

### <a name="transaction-type"></a>Operacijos tipas

Operacijos tipas reiškia finansinio poveikio projektui laiką ir kontekstą. Jį nurodo parinkčių rinkinys, kuris programoje PSA turi toliau nurodytas palaikomas reikšmes.
- Išlaidos
- Projekto sutartis
- Pardavimas, už kurį neišrašyta sąskaita
- Pardavimas, už kurį išrašyta sąskaita
- Pardavimas tarp organizacijų
- Išteklių paskirstymo vieneto savikaina

### <a name="transaction-class"></a>Operacijos klasė

Operacijos klasė nurodo skirtingus projekto išlaidų tipus. Jį nurodo parinkčių rinkinys, kuris programoje PSA turi toliau nurodytas palaikomas reikšmes.

- Time
- Išlaidos
- Medžiagos
- Mokestis
- Etapas
- Mokestis

Verslo logikoje reikšmė **Etapas** paprastai naudojama PSA fiksuotos kainos atsiskaitymams.

### <a name="transaction-origin"></a>Operacijos kilmė

Operacijos kilmė yra objektas, kuris išsaugo kiekvienos verslo operacijos kilmę. Vykdant projektą, kiekviena verslo operacija sukurs kitą verslo operaciją, kuri sukurs dar kitą ir t. t. Operacijos kilmės objektas buvo sukurtas norint saugoti duomenis apie kiekvienos operacijos kilmę, kad būtų lengviau parengti ataskaitą ir atsekti. 

### <a name="transaction-connection"></a>Operacijos ryšys

Operacijos ryšys – tai objektas, nusakantis ryšį tarp dviejų panašių verslo operacijų, pvz., savikainos ir susijusių pardavimo faktinių duomenų, arba operacijų atšaukimų, suaktyvinamų atsiskaitymo veiklomis, pvz., sąskaitos faktūros patvirtinimu arba sąskaitos faktūros koregavimu.

Kartu naudodami operacijos kilmę ir operacijos ryšį galite sekti ryšius tarp verslo operacijų ir veiksmų, dėl kurių buvo sukurta konkreti verslo operacija.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Pavyzdys: operacijos kilmės ir operacijos ryšio sąveika

Toliau pateiktame pavyzdyje parodytas tipinis PSA projekto ciklo laiko įrašų apdorojimas.

> ![„Project Service“ ciklo laiko įrašų apdorojimas.](media/basic-guide-17.png)
 
1. Pateikus laiko įrašą, sukuriamos dvi žurnalo eilutės: viena išlaidų eilutė ir viena pardavimo, už kurį neišrašyta sąskaita, eilutė.
2. Galiausiai patvirtinus laiko įrašą, sukuriamos dvi faktinės sumos: viena išlaidų suma ir viena pardavimo, už kurį neišrašyta sąskaita, suma.
3. Vartotojui kuriant projekto sąskaitą faktūrą, sąskaitos faktūros eilutės operacija sukuriama naudojant faktinės pardavimo, už kurį neišrašyta sąskaita, sumos duomenis. 
4. Patvirtinus sąskaitą faktūrą, sukuriamos dvi naujos faktinės sumos: pardavimo, už kurį neišrašyta sąskaita, atšaukimo suma ir faktinė pardavimo, už kurį išrašyta sąskaita, suma.

Kiekvieno iš šių įvykių atveju sukuriami objektų Operacijos kilmė ir Operacijos ryšys įrašai, padedantys sekti ryšį tarp šių įrašų, sukurtų laiko įrašų, žurnalo eilučių, faktinių sumų ir sąskaitos faktūros eilučių informacijoje.

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

Tolesnėje lentelėje pateikiami ankstesnės darbo eigos objekto Operacijos ryšys įrašai.

| Įvykis                          | 1 operacija                 | 1 operacijos vaidmuo | 1 operacijos tipas           | 2 operacija                | 2 operacijos vaidmuo | 2 operacijos tipas |
|--------------------------------|-------------------------------|--------------------|------------------------------|------------------------------|--------------------|--------------------|
| Laiko įrašo pateikimas          | Žurnalo eilutės (pardavimo) GUID     | Pardavimas, už kurį neišrašyta sąskaita     | msdyn_journalline            | Žurnalo eilutės (išlaidų) GUID     | Išlaidos               | msdyn_journalline  |
| Laiko patvirtinimas                  | Faktinės sumos, už kurią neišrašyta sąskaita, GUID (pardavimas)  | Pardavimas, už kurį neišrašyta sąskaita     | msdyn_actual                 | Faktinių išlaidų GUID (išlaidos)       | Išlaidos               | msdyn_actual       |
| Sąskaitos faktūros kūrimas               | Sąskaitos faktūros eilutės informacijos GUID      | Pardavimas, už kurį išrašyta sąskaita       | msdyn_invoicelinetransaction | Pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID   | Pardavimas, už kurį neišrašyta sąskaita     | msdyn_actual       |
| Sąskaitos faktūros patvirtinimas           | Faktinės sumos atšaukimo GUID         | Atšaukimas          | msdyn_actual                 | Pradinio pardavimo, už kurį neišrašyta sąskaita, GUID | Pradinis           | msdyn_actual       |
| Pardavimo, už kurį išrašyta sąskaita, GUID              | Pardavimas, už kurį išrašyta sąskaita                  | msdyn_actual       | Pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID   | Pardavimas, už kurį neišrašyta sąskaita               | msdyn_actual       |                    |
| Sąskaitos faktūros juodraščio koregavimas       | Sąskaitos faktūros eilutės operacijos GUID | Pakeitimas          | msdyn_invoicelinetransaction | Pardavimo, už kurį išrašyta sąskaita, GUID            | Pradinis           | msdyn_actual       |
| Sąskaitos faktūros koregavimo patvirtinimas     | Pardavimo, už kurį išrašyta sąskaita, atšaukimo GUID    | Atšaukimas          | msdyn_actual                 | Pardavimo, už kurį išrašyta sąskaita, GUID            | Pradinis           | msdyn_actual       |
| Naujos pardavimo, už kurį neišrašyta sąskaita, faktinės sumos GUID | Pakeitimas                     | msdyn_actual       | Pardavimo, už kurį išrašyta sąskaita, GUID            | Pradinis                     | msdyn_actual       |                    |


[!INCLUDE[footer-include](../includes/footer-banner.md)]