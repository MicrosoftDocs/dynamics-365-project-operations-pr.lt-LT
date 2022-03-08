---
title: Projektais pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie įtrauktus, apmokestinamus ir neapmokestinamus komponentus sutarties eilutėse.
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: af97904b0171618cb15d060da9bc87fcf6bbabeb
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080773"
---
# <a name="configure-chargeable-components-of-a-project-based-contract-line"></a>Projektais pagrįstos sutarties eilutės apmokestinamų komponentų konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektais pagrįstos sutarties eilutėje pateikiama įtrauktų, apmokestinamų ir neapmokestinamų komponentų sąvoka.

Įtrauktiems komponentams taikomas atsiskaitymo būdas, klientų išskaidymas, neviršytini apribojimai ir sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįstoje sutarties eilutėje.

Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas atnaujinant lauką **Atsiskaitymo tipas**.

Apmokestinamus komponentus galima apibrėžti vaidmenyse ir operacijų kategorijose.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei projekto sutarties eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei projekto sutarties eilutės laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečioje projektais pagrįstojesutarties eilutėje.

Projektais pagrįstos sutarties eilutės skirtuke **Apmokestinami vaidmenys**, papildomame tinklelyje **Apmokestinamos kategorijos**, lauke atnaujinkite vaidmens **atsiskaitymo tipą**.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje projektais pagrįstoje sutarties eilutėje.

Projektais pagrįstos sutarties eilutės skirtuke **Apmokestinami kategorijos**, papildomame tinklelyje **Apmokestinamos kategorijos**, lauke atnaujinkite operacijos **atsiskaitymo tipą**.

### <a name="resolve-chargeability"></a>Apmokestinamumo sprendimas

Sukurtos numatomos arba faktinės laiko reikšmės bus laikomos apmokestinamomis tik jei Laikas įtraukiamas į sutarties eilutę ir jei vaidmuo sukonfigūruotas kaip apmokestinamas sutarties eilutėje.

Sukurtos numatomos arba faktinės išlaidų reikšmės bus laikomos apmokestinamomis tik jei Išlaidos įtraukiamos į sutarties eilutę ir jei kategorijos operacijos kategorija sukonfigūruojama kaip apmokestinamos sutarties eilutėje.

| Įtrauktas laikas | Įtrauktos išlaidos | Vaidmuo | Kategorija. | Užduotis |
| --- | --- | --- | --- | --- |
| Taip | Taip | Apmokestinama | Apmokestinama | Atsiskaitymas pagal faktinį laiką: Apmokestinamas </br>Atsiskaitymas pagal faktines išlaidas: Apmokestinamas |
| Taip | Taip | Neapmokestinama | Apmokestinama | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas </br>Atsiskaitymas pagal faktines išlaidas: Apmokestinamas |
| Taip | Taip | Neapmokestinama | Neapmokestinama | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas </br>Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas |
| No | Taip | Negalima nustatyti | Apmokestinama | Atsiskaitymas pagal faktinį laiką: Nėra </br>Atsiskaitymas pagal faktines išlaidas: Apmokestinamas |
| No | Taip | Negalima nustatyti | Neapmokestinama | Atsiskaitymas pagal faktinį laiką: Nėra </br>Atsiskaitymas pagal faktines išlaidas: Neapmokestinamas |
| Taip | No | Apmokestinama | Negalima nustatyti | Atsiskaitymas pagal faktinį laiką: Apmokestinamas </br>Atsiskaitymas pagal faktines išlaidas: Nėra |
| Taip | No | Neapmokestinama | Negalima nustatyti | Atsiskaitymas pagal faktinį laiką: Neapmokestinamas </br> Atsiskaitymas pagal faktines išlaidas: Nėra |
