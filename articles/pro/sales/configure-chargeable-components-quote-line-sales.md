---
title: Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie apmokestinamų ir neapmokestinamų komponentų nustatymą projektais pagrįsto pasiūlymo eilutėje.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e0b64d7edb21df127bf7544f044de7f3c496dfe3
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080957"
---
# <a name="configure-the-chargeable-components-of-a-quote-line"></a>Pasiūlymo eilutės apmokestinamų komponentų konfigūravimas

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

Pasiūlymo eilutės apmokestinamumas apibrėžiamas užduotyse ir taikomas visoms į eilutę įtrauktoms operacijų klasėms. Jei laukas **Įtraukti užduotis** yra tuščias arba nustatytas į parinktį **Visas projektas** , skirtukas **Apmokestinamos užduotys** nebus pateiktas.

Pasiūlymo eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei projekto pasiūlymo eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne** , skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Pasiūlymo eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei projekto pasiūlymo eilutės laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne** , skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-project-task-to-be-chargeable-or-non-chargeable"></a>Projekto užduoties atnaujinimas į apmokestinamą arba neapmokestinamą

Projekto užduotis gali būti apmokestinama arba neapmokestinama konkrečios projektais pagrįsto pasiūlymo eilutės kontekste, todėl galima nustatyti toliau nurodytą sąranką.

Jei projekto pasiūlymo eilutėje yra **Laikas** ir užduotis **T1** , užduotis susieta su pasiūlymo eilute kaip apmokestinama. Jei antroje išlaidas eilutėje yra **Išlaidos** , **T1** užduotį galite susieti išlaidas eilutėje kaip neapmokestinamą. Todėl visas laikas, užfiksuotas užduotyje, yra apmokestinamas, o visos užduotyje įrašytos išlaidos – neapmokestinamos.

Užduoties atsiskaitymo tipą galima sukonfigūruoti projektais pagrįsto pasiūlymo eilutės skirtuke **Apmokestinamos užduotys** atnaujinant papildomo tinklelio **Pasiūlymo eilutės užduotys** lauką **Atsiskaitymo tipas**. Taip pat galite atnaujinti projekto užduoties atsiskaitymo tipą projekto, kuriame rodomos su užduotimi susietos pasiūlymo eilutės, užduoties atsiskaitymo sąrankos papildomo tinklelio lauką **Atsiskaitymo tipas**.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečios projektais pagrįsto pasiūlymo eilutės kontekste.

Vaidmens atsiskaitymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinami vaidmenys** atnaujinant papildomo tinklelio **Apmokestinami vaidmenys** lauką **Atsiskaitymo tipas**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje pasiūlymo eilutėje.

Operacijos atsiskaitymo tipą galima sukonfigūruoti pasiūlymo eilutės skirtuke **Apmokestinamos kategorijos** atnaujinant papildomo tinklelio **Apmokestinamos kategorijos** lauką **Atsiskaitymo tipas**.

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
