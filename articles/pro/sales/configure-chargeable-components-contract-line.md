---
title: Projektais pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie tai, kaip įtraukti apmokestinamus komponentus į sutarties eilutes naudojant „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4d665a6351d2315d185e64e4eb6b0b8859f7bbc4
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080743"
---
# <a name="configuring-chargeable-components-of-a-project-based-contract-line"></a>Projektais pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Į projektais pagrįstą sutarties eilutę *įtraukti* komponentai ir *apmokestinami* komponentai.

Įtrauktiems komponentams taikomos toliau nurodytos sąlygos.

  - Sąskaitų išrašymo būdo ir klientų išskaidymas
  - Limitas, kurio negalima viršyti 
  - Sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįstoje sutarties eilutėje

Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas naudojant lauką **Atsiskaitymo tipas**. Laukas **Atsiskaitymo tipas** yra parinkčių rinkinys, leidžiantis toliau nurodytas reikšmes sutarties eilutės kontekste.

  - Apmokestinama
  - Neapmokestinama

Apmokestinamus komponentus galima apibrėžti užduotyse, vaidmenyse ir operacijų kategorijose.

Projekto sutarties eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms. Jei sutarties eilutės laukas **Įtraukti užduotis** yra tuščias arba nustatytas į parinktį **Visas projektas** , skirtukas **Apmokestinamos užduotys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei sutarties eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne** , skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne** , skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą

Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje, todėl galima nustatyti toliau nurodytą sąranką.

Jei projekto sutarties eilutėje yra nurodyti **Laikas** ir tam tikra užduotis, **T1** su ja susieta kaip apmokestinama. Jei antroje sutarties eilutėje yra **Išlaidos** , T1 užduotį galite susieti sutarties eilutėje kaip neapmokestinamą. Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos išlaidos – neapmokestinamos.

Užduoties atsiskaitymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinamos užduotys** atnaujinant sutarties eilutės užduočių papildomo tinklelio lauką **Atsiskaitymo tipas**. Taip pat galite atnaujinti projekto, kuriame rodomos su užduotimi susietos sutarties eilutės, užduoties Atsiskaitymo sąranka antrinio tinklelio lauką **Atsiskaitymo tipas**.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečioje sutarties eilutėje.

Vaidmens atsiskaitymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinami vaidmenys**. Norėdami tai atlikti, atnaujinkite papildomo tinklelio **Apmokestinami vaidmenys** lauką **Atsiskaitymo tipas**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje.

Operacijos atsiskaitymo tipą galima sukonfigūruoti projektais pagrįstos sutarties eilutės skirtuke **Apmokestinamos kategorijos**. Norėdami tai atlikti, atnaujinkite papildomo tinklelio **Apmokestinamos kategorijos** lauką **Atsiskaitymo tipas**.

### <a name="resolve-chargeability"></a>Apmokestinamumo sprendimas

Sukurtos numatomos arba faktinės laiko reikšmės bus laikomos apmokestinamomis tik jei **Laikas** įtraukiamas į sutarties eilutę ir jei **Užduotis** ir **Vaidmuo** sukonfigūruojami kaip apmokestinami sutarties eilutėje.

Sukurtos numatomos arba faktinės išlaidų reikšmės bus laikomos apmokestinamomis tik jei **Išlaidos** įtraukiamos į sutarties eilutę ir jei kategorijos **Užduotis** ir **Operacija** sukonfigūruojamos kaip apmokestinamos sutarties eilutėje.


| Įtrauktas laikas | Įtrauktos išlaidos | Įtrauktos užduotys | Vaidmuo           | Kategorija.       | Užduotis                                                                                                      |
|---------------|------------------|----------------|----------------|----------------|-----------------------------------------------------------------------------------------------------------|
| Taip           | Taip              | Visas projektas | Apmokestinama     | Apmokestinama     | Atsiskaitymas pagal faktinį laiką: **Apmokestinamas** </br> Atsiskaitymas pagal faktines išlaidas: **Apmokestinamas**           |
| Taip           | Taip              | Pasirinktos užduotys | Apmokestinama     | Apmokestinama     | Atsiskaitymas pagal faktinį laiką: **Apmokestinamas** </br> Atsiskaitymas pagal faktines išlaidas: **Apmokestinamas**           |
| Taip           | Taip              | Pasirinktos užduotys | Neapmokestinama | Apmokestinama     | Atsiskaitymas pagal faktinį laiką: **Neapmokestinamas** </br> Atsiskaitymas pagal faktines išlaidas: **Apmokestinamas**       |
| Taip           | Taip              | Pasirinktos užduotys | Apmokestinama     | Apmokestinama     | Atsiskaitymas pagal faktinį laiką: **Neapmokestinamas** </br> Atsiskaitymas pagal faktines išlaidas: **Neapmokestinamas** |
| Taip           | Taip              | Pasirinktos užduotys | Neapmokestinama | Apmokestinama     | Atsiskaitymas pagal faktinį laiką: **Neapmokestinamas** </br> Atsiskaitymas pagal faktines išlaidas: **Neapmokestinamas** |
| Taip           | Taip              | Pasirinktos užduotys | Neapmokestinama | Neapmokestinama | Atsiskaitymas pagal faktinį laiką: **Neapmokestinamas** </br> Atsiskaitymas pagal faktines išlaidas: **Neapmokestinamas** |
| No            | Taip              | Visas projektas | Negalima nustatyti   | Apmokestinama     | Atsiskaitymas pagal faktinį laiką: **Nėra**</br>Atsiskaitymas pagal faktines išlaidas: **Apmokestinamas**          |
| No            | Taip              | Visas projektas | Negalima nustatyti   | Neapmokestinama | Atsiskaitymas pagal faktinį laiką: **Nėra**</br> Atsiskaitymas pagal faktines išlaidas: **Neapmokestinamas**     |
| Taip           | No               | Visas projektas | Apmokestinama     | Negalima nustatyti   | Atsiskaitymas pagal faktinį laiką: **Apmokestinamas** </br> Atsiskaitymas pagal faktines išlaidas: **Nėra**        |
| Taip           | No               | Visas projektas | Neapmokestinama | Negalima nustatyti   | Atsiskaitymas pagal faktinį laiką: **Neapmokestinamas** </br>Atsiskaitymas pagal faktines išlaidas: **Nėra**   |
