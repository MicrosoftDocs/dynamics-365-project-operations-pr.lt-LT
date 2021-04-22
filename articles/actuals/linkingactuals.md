---
title: Faktinių duomenų susiejimas su pradiniais įrašais
description: Šioje temoje aiškinama, kaip susieti faktinius duomenis su originaliais įrašais, pvz., laiko ir išlaidų įrašais arba medžiagos naudojimo žurnalais.
author: rumant
manager: tfehr
ms.date: 03/25/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 545775c4eae6c3dc689f264e7f662471c17b2340
ms.sourcegitcommit: b4a05c7d5512d60abdb0d05bedd390e288e8adc9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/02/2021
ms.locfileid: "5852599"
---
# <a name="link-actuals-to-original-records"></a>Faktinių duomenų susiejimas su pradiniais įrašais

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


Programoje „Dynamics 365 Project Operations“ *verslo operacija* yra abstrakti sąvoka, nereiškianti objekto. Tačiau kai kuriems bendriesiems objektų laukams ir procesams gali būti naudojama verslo operacijų koncepcija. Ši abstrakti sąvoka naudojama toliau nurodytiems objektams.

- Pasiūlymo eilučių informacija
- Sutarties eilučių informacija
- Įvertinimo eilutės
- Žurnalo eilutės
- Faktinės

Iš visų šių objektų, **Pasiūlymo eilučių informacija**, **Sutarties eilučių informacija** ir **Įvertinimo eilutės** siejamos su projekto ciklo įvertinimo etapu. **Žurnalo eilutės** ir **Faktinių duomenų objektai** siejami su projekto ciklo vykdymo etapu.

„Project Operations“ atpažįsta šių penkių objektų įrašus kaip laiko verslo operacijas. Vienintelis skirtumas yra tas, kad objektų, susietų su įvertinimo etapu, įrašai yra laikomi finansinėmis prognozėmis, o objektų, susietų su vykdymo etapu, įrašai – jau įvykusiais finansiniais faktais.

## <a name="concepts-that-are-unique-to-business-transactions"></a>Unikalios verslo operacijų koncepcijos
Toliau nurodytos koncepcijos yra unikalios verslo operacijų koncepcijos:

- Operacijos tipas
- Operacijos klasė
- Operacijos kilmė
- Operacijos ryšys

### <a name="transaction-type"></a>Operacijos tipas

Operacijos tipas reiškia finansinio poveikio projektui laiką ir kontekstą. Tai nurodo parinkčių rinkinys, kuris programoje „Project Operations“ turi toliau nurodytas palaikomas reikšmes.

  - Savikaina
  - Projekto sutartis
  - Neišrašytas pardavimas
  - Išrašytas pardavimas
  - Pardavimas tarp organizacijų
  - Išteklių paskirstymo vieneto savikaina

### <a name="transaction-class"></a>Operacijos klasė

Operacijos klasė nurodo skirtingus projekto išlaidų tipus. Tai nurodo parinkčių rinkinys, kuris programoje „Project Operations“ turi toliau nurodytas palaikomas reikšmes.

  - Laikas
  - Išlaidos
  - Medžiaga
  - Rinkliava
  - Etapas
  - Mokestis

Verslo logikoje reikšmė **Etapas** paprastai naudojama „Project Operations“ fiksuotos kainos atsiskaitymams.

### <a name="transaction-origin"></a>Operacijos kilmė

**Operacijos kilmė** yra objektas, kuris išsaugo kiekvienos verslo operacijos kilmę. Pradėjus vykdyti projektą, sulig kiekviena verslo operacija pradedama kita verslo operacija, o sulig šia, savo ruožtu, dar viena ir t. t. Operacijos kilmės objektas skirtas duomenims apie kiekvienos operacijos kilmę saugoti, kad būtų galima lengviau teikti ataskaitas ir naudotis atsekamumo funkcija. 

### <a name="transaction-connection"></a>Operacijos ryšys

**Operacijos ryšys** – tai objektas, nusakantis ryšį tarp dviejų panašių verslo operacijų, pvz., savikainos ir susijusių pardavimo faktinių duomenų arba operacijų atšaukimų, suaktyvinamų atsiskaitymo veiklomis, pvz., sąskaitos faktūros patvirtinimu arba sąskaitos faktūros koregavimu.

Kartu naudojant **operacijos kilmę** ir **operacijos ryšį**, galima sekti ryšius tarp verslo operacijų ir veiksmų, dėl kurių buvo atlikta konkreti verslo operacija.

### <a name="example-how-transaction-origin-works-with-transaction-connection"></a>Pavyzdys: operacijos kilmės ir operacijos ryšio sąveika

Toliau pateiktame pavyzdyje parodytas tipinis „Project Operations“ projekto ciklo laiko įrašų apdorojimas.

> ![„Project Service“ ciklo laiko įrašų apdorojimas](media/basic-guide-17.png)
 
1. Pateikus laiko įrašą, sukuriamos dvi žurnalo eilutės: viena, skirta išlaidoms, o kita – pardavimui, už kurį neišrašyta sąskaita.
2. Galiausiai patvirtinus laiko įrašą, sukuriamos dvi faktinės sumos: viena faktinė išlaidų suma ir viena faktinė pardavimo, už kurį neišrašyta sąskaita, suma.
3. Sukūrus naują projekto sąskaitą faktūrą, sąskaitos faktūros eilutės operacija sukuriama naudojant faktinės pardavimo, už kurį neišrašyta sąskaita, sumos duomenis. 
4. Patvirtinus sąskaitą faktūrą, sukuriamos dvi naujos faktinės sumos: pardavimo, už kurį neišrašyta sąskaita, faktinio atšaukimo suma ir faktinė pardavimo, už kurį išrašyta sąskaita, suma.

Kiekvienam iš šių įvykių objektuose **Operacijos kilmė** ir **Operacijos ryšys** sukuriamas įrašas. Šie nauji įrašai padeda sukurti ryšių tarp įrašų, sukurtų laiko įrašuose, žurnalo eilutėse, faktiniuose duomenyse ir sąskaitos faktūros eilutės informacijos dalyje, retrospektyvą.

Tolesnėje lentelėje pateikiami darbo eigos objekto **Operacijos kilmė** įrašai.

| Renginys                        | Kilmė                   | Kilmės tipas                       | Operacija                       | Operacijos tipas         |
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

Tolesnėje lentelėje pateikiami darbo eigos objekto **Operacijos ryšys** įrašai.

| Renginys                          | 1 operacija                 | 1 operacijos vaidmuo | 1 operacijos tipas           | 2 operacija                | 2 operacijos vaidmuo | 2 operacijos tipas |
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
