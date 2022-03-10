---
title: Projekto sutarties eilutės apmokestinamų komponentų konfigūravimas
description: Šioje temoje pateikta informacija apie įtrauktus, apmokestinamus ir neapmokestinamus komponentus sutarties eilutėse.
author: rumant
ms.date: 10/12/2020
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 51151089df67e2d164fc6315c1291f880917f43f1fba189304cb305ea973cecb
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7004051"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>Projekto sutarties eilutės apmokestinamų komponentų konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektais pagrįstos sutarties eilutėje pateikiama įtrauktų, apmokestinamų ir neapmokestinamų komponentų sąvoka.

Įtrauktiems komponentams taikomas atsiskaitymo būdas, klientų išskaidymas, neviršytini apribojimai ir sąskaitos faktūros dažnio parametrai, apibrėžti projektais pagrįstoje sutarties eilutėje.

Įtrauktų komponentų pogrupis gali būti pažymėtas kaip apmokestinamas atnaujinant lauką **Atsiskaitymo tipas**.

Apmokestinamus komponentus galima apibrėžti vaidmenyse ir operacijų kategorijose.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas vaidmenyse, taikomas tik tipo **Laikas** operacijų klasei. Jei projekto sutarties eilutės laukas **Įtraukti laiką** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Projekto sutarties eilutės apmokestinamumas, apibrėžtas operacijų kategorijose, taikomas tik tipo **Išlaidos** operacijų klasei. Jei projekto sutarties eilutės laukas **Įtraukti išlaidas** yra nustatytas į parinktį **Ne**, skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

### <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą

Vaidmuo gali būti apmokestinamas arba neapmokestinamas konkrečioje projektais pagrįstojesutarties eilutėje.

Projektu pagrįstos sutarties eilutės skirtuke **Apmokestinamieji vaidmenys**, papildomo tinklelio **Apmokestinamosios kategorijos** lauke **Atsiskaitymo tipas** atnaujinkite vaidmens atsiskaitymo tipą.

### <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą

Operacijos kategorija gali būti apmokestinama arba neapmokestinama konkrečioje projektais pagrįstoje sutarties eilutėje.

Projektu pagrįstos sutarties eilutės skirtuke **Apmokestinamosios kategorijos**, papildomo tinklelio **Apmokestinamosios kategorijos** lauke **Atsiskaitymo tipas** atnaujinkite operacijos atsiskaitymo tipą.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
