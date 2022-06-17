---
title: Projektu pagrįsto pasiūlymo eilutės apmokestinamų komponentų konfigūravimas
description: Šiame straipsnyje pateikiama informacija apie įtrauktus, apmokestinamus ir neapmokestinamus komponentus, esančius projekto pasiūlymo eilutėse.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ff409132ef9103641578f9c94f8ea1ff56738a71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8915562"
---
# <a name="configure-the-chargeable-components-of-a-project-based-quote-line"></a>Projektu pagrįsto pasiūlymo eilutės apmokestinamų komponentų konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektu pagrįsto pasiūlymo eilutėje gali būti įtrauktų komponentų ir apmokestinamų komponentų.

Įtrauktiems komponentams taikomas atsiskaitymo metodas, išskaidymai klientams, limitai, kurių negalima viršyti, ir sąskaitų faktūrų dažnio parametrai, apibrėžti projektu pagrįsto pasiūlymo eilutėje.
Antrinis įtrauktų komponentų rinkinys gali būti pažymėtas kaip apmokestinamas, naudojant lauką **Atsiskaitymo tipas**. Pasiūlymo eilutės kontekste, lauke **Atsiskaitymo tipas**, galite pasirinkti vieną iš toliau nurodytų parinkčių:

   - Apmokestinama
   - Neapmokestinama

Apmokestinamus komponentus galima apibrėžti naudojant vaidmenis ir operacijų kategorijas.

Apmokestinimas, apibrėžtas naudojant projekto pasiūlymo eilutės vaidmenis, taikomas tik operacijos klasei **Laikas**. Jei projekto pasiūlymo eilutėje **Įtraukti laiką** = **Ne**, tai skirtukas **Apmokestinami vaidmenys** nebus pateiktas.

Apmokestinimas, apibrėžtas naudojant projekto pasiūlymo eilutės operacijų kategorijas, taikomas tik operacijos klasei **Išlaidos**. Jei projekto pasiūlymo eilutėje **Įtraukti išlaidas** = **Ne**, tai skirtukas **Apmokestinamos kategorijos** nebus pateiktas.

## <a name="update-a-role-to-be-chargeable-or-non-chargeable"></a>Vaidmens atnaujinimas į apmokestinamą arba neapmokestinamą
Projekto pasiūlymo eilutėje vaidmuo gali būti apmokestinamas arba neapmokestinamas. Atsiskaitymo tipą pagal vaidmenį galima sukonfigūruoti projektu pagrįsto pasiūlymo eilutės skirtuke **Apmokestinami vaidmenys**. Norėdami tai atlikti, atnaujinkite **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinami vaidmenys**. 

## <a name="update-a-transaction-category-to-be-chargeable-or-non-chargeable"></a>Operacijos kategorijos atnaujinimas į apmokestinamą arba neapmokestinamą
Projekto pasiūlymo eilutėje operacijos kategorija gali būti apmokestinama arba neapmokestinama. Atsiskaitymo tipą pagal operaciją galima sukonfigūruoti projektu pagrįsto pasiūlymo eilutės skirtuke **Apmokestinamos kategorijos**. Norėdami tai atlikti, atnaujinkite lauką **Atsiskaitymo tipas**, esantį papildomame tinklelyje **Apmokestinamosios kategorijos**. 

## <a name="resolve-chargeability"></a>Apmokestinamumo sprendimas

Numatomi arba faktiniai duomenys, sukurti pagal laiką, yra apmokestinami tik tuo atveju, jei laikas įtrauktas į pasiūlymo eilutę ir jei vaidmuo sukonfigūruotas kaip apmokestinamas.
Numatomi arba faktiniai duomenys, sukurti pagal išlaidas, yra apmokestinami tik tuo atveju, jei išlaidos įtrauktos į pasiūlymo eilutę ir jei operacijos kategorija pasiūlymo eilutėje sukonfigūruota kaip apmokestinama. Toliau esančioje lentelėje parodytos numatytosios apmokestinimo reikšmės pagal faktinius duomenis. Numatytosios reikšmės pagrįstos įtrauktais komponentais ir atsiskaitymo tipu, nustatytu pasiūlymo eilutėje.

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