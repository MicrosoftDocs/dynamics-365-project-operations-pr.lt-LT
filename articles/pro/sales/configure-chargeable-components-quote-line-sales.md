---
title: Pasiūlymo eilutės apmokestinamųjų komponentų konfigūravimas – „Lite“ versija
description: Šioje temoje pateikta informacija apie apmokestinamų ir neapmokestinamų komponentų nustatymą projektais pagrįsto pasiūlymo eilutėje.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b5d751ecd66975135c4afd5f18e896251ff34990
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177116"
---
# <a name="configure-the-chargeable-components-of-a-quote-line---lite"></a>Pasiūlymo eilutės apmokestinamųjų komponentų konfigūravimas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projektais pagrįsto pasiūlymo eilutėje pateikiama *įtrauktų* ir *apmokestinamų* sąvoka.

Įtrauktiems komponentams taikomos toliau nurodytos sąlygos.

  - Sąskaitų išrašymo būdo ir klientų išskaidymas
  - Limitas, kurio negalima viršyti 
  - Sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįsto pasiūlymo eilutėje

Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas naudojant lauką **Atsiskaitymo tipas**. Laukas **Atsiskaitymo tipas** yra parinkčių rinkinys, leidžiantis toliau nurodytas reikšmes pasiūlymo eilutės kontekste.

  - Apmokestinama
  - Neapmokestinama

Apmokestinamus komponentus galima apibrėžti užduotyse, vaidmenyse ir operacijų kategorijose.

Pasiūlymo eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms. Jei laukas **Įtraukti užduotis** yra tuščias arba nustatytas į parinktį **Visas projektas**, skirtukas **Apmokestinamos užduotys** nebus pateiktas.

Pasiūlymo eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei projekto pasiūlymo eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Pasiūlymo eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei projekto pasiūlymo eilutės laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą

Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečios projektais pagrįsto pasiūlymo eilutės kontekste, todėl galima nustatyti toliau nurodytą sąranką.

Jei projekto pasiūlymo eilutėje yra **Laikas** ir užduotis **T1**, užduotis susieta su pasiūlymo eilute kaip apmokestinama. Jei antroje išlaidas eilutėje yra **Išlaidos**, **T1** užduotį galite susieti išlaidas eilutėje kaip neapmokestinamą. Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos užduotyje įrašytos išlaidos – neapmokestinamos.

Užduoties sąskaitų išrašymo tipą galima sukonfigūruoti projektu pagrįstos pasiūlymo eilutės skirtuke **Apmokestinamosios užduotys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Pasiūlymo eilučių užduotys**. Arba galite atnaujinti projekto užduoties atsiskaitymo tipą lauke **Atsiskaitymo tipas**, esantį projekto, kuriame pasiūlymo eilutės rodomos kaip susietos su užduotimi, atsiskaitymo už užduotis sąrankos papildomame tinklelyje.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečios projektais pagrįsto pasiūlymo eilutės kontekste.

Vaidmens sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamieji vaidmenys**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamieji vaidmenys**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje pasiūlymo eilutėje.

Operacijos sąskaitų išrašymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamosios kategorijos**, atnaujinant lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**.

### <a name="resolve-chargeability"></a>Apmokestinamumo sprendimas
Sukurtos numatomos arba faktinės laiko reikšmės bus laikomos apmokestinamomis tik jei **Laikas** įtraukiamas į pasiūlymo eilutę ir jei **Užduotis** ir **Vaidmuo** sukonfigūruojami kaip apmokestinami pasiūlymo eilutėje.

Sukurtos numatomos arba faktinės išlaidų reikšmės bus laikomos apmokestinamomis tik jei **Išlaidos** įtraukiamos į pasiūlymo eilutę ir jei **Užduotis** bei **Operacijos kategorija** sukonfigūruojamos kaip apmokestinamos pasiūlymo eilutėje.

| Įtrauktas laikas | Įtrauktos išlaidos | Įtrauktos užduotys | Vaidmuo | Kategorija. | Užduotis | Sąskaitų siuntimas |
| --- | --- | --- | --- | --- | --- | --- |
| Taip | Taip | Visas projektas | Apmokestinama | Apmokestinama | Negalima nustatyti | Atsiskaitymas pagal faktinį laiką: Apmokestinamas </br>Atsiskaitymas pagal faktines išlaidas: Apmokestinamas |
| Taip | Taip | Tik pasirinktos užduotys | Apmokestinama | Apmokestinama | Apmokestinama | Atsiskaitymas pagal faktinį laiką: Apmokestinamas</br>Atsiskaitymas pagal faktines išlaidas: Apmokestinamas |
| Taip | Taip | Tik pasirinktos užduotys | Neapmokestinama | Apmokestinama | Apmokestinama | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas</br>Atsiskaitymas pagal faktines išlaidas: Apmokestinamas |
| Taip | Taip | Tik pasirinktos užduotys | Apmokestinama | Apmokestinama | Neapmokestinama | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas</br> Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas |
| Taip | Taip | Tik pasirinktos užduotys | Neapmokestinama | Apmokestinama | Neapmokestinama | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas</br> Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas |
| Taip | Taip | Tik pasirinktos užduotys | Neapmokestinama | Neapmokestinama | Apmokestinama | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas</br> Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas |
| No | Taip | Visas projektas | Negalima nustatyti | Apmokestinama | Negalima nustatyti | Atsiskaitymas pagal faktinį laiką: Nėra </br>Atsiskaitymas pagal faktines išlaidas: Apmokestinamas |
| No | Taip | Visas projektas | Negalima nustatyti | Neapmokestinama | Negalima nustatyti | Atsiskaitymas pagal faktinį laiką: Nėra </br>Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas |
| Taip | No | Visas projektas | Apmokestinama | Negalima nustatyti | Negalima nustatyti | Atsiskaitymas pagal faktinį laiką: Apmokestinamas</br>Atsiskaitymas pagal faktines išlaidas: Nėra |
| Taip | No | Visas projektas | Neapmokestinama | Negalima nustatyti | Negalima nustatyti | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas </br>Atsiskaitymas pagal faktines išlaidas: Nėra |
