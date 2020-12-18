---
title: Projektu pagrįstos sutarties eilutės apmokestinamųjų komponentų konfigūravimas – „Lite“
description: Šioje temoje pateikta informacija apie tai, kaip įtraukti apmokestinamus komponentus į sutarties eilutes naudojant „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b881e03a2bb085c6d7cfccb7eec70442e696e62c
ms.sourcegitcommit: 869bde007805ef255f61b03937e4a44aeef61df9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/12/2020
ms.locfileid: "4513889"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line---lite"></a>Projektu pagrįstos sutarties eilutės apmokestinamųjų komponentų konfigūravimas – „Lite“

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

Projekto sutarties eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms. Jei sutarties eilutės laukas **Įtraukti užduotis** yra tuščias arba nustatytas kaip **Visas projektas**, skirtukas **Apmokestinamos užduotys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei sutarties eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą

Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje, todėl galima nustatyti toliau nurodytą sąranką.

Jei projekto sutarties eilutėje yra nurodyti **Laikas** ir tam tikra užduotis, **T1** su ja susieta kaip apmokestinama. Jei antroje sutarties eilutėje yra **Išlaidos**, T1 užduotį galite susieti sutarties eilutėje kaip neapmokestinamą. Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos išlaidos – neapmokestinamos.

Užduoties sąskaitų išrašymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinamosios užduotys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį sutarties eilutės užduočių papildomame tinklelyje. Arba galite atnaujinti lauką **Atsiskaitymo tipas**, esantį projekto, kuriame sutarties eilutės rodomos kaip susietos su užduotimi, atsiskaitymo už užduotis sąrankos papildomame tinklelyje.

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečioje sutarties eilutėje.

Vaidmens atsiskaitymo tipą galima sukonfigūruoti sutarties eilutės skirtuke **Apmokestinami vaidmenys**. Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamieji vaidmenys**.

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje sutarties eilutėje.

Operacijos atsiskaitymo tipą galima sukonfigūruoti projektais pagrįstos sutarties eilutės skirtuke **Apmokestinamos kategorijos**. Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.

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
