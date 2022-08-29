---
title: Tiekėjo sąskaitų faktūrų išrašymas – sąvoka ir kūrimas
description: Šiame straipsnyje aprašoma tiekėjo SF sąvoka, naudojimo scenarijai ir kaip kurti tiekėjo SF programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b57ec8cdb6097e6f2207056667aadfb43ee8acfc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261954"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Tiekėjo sąskaitų faktūrų išrašymas – sąvoka ir kūrimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF išrašymas programoje "Microsoft" Dynamics 365 Project Operations gali būti naudojamas išlaidoms, susijusioms su tiekėjų vykdomu paslaugų ir (arba) medžiagos pristatymu į projektą, įrašyti.

Kai paslaugos ir (arba) medžiagos subrangos sutartimi pavedamos tiekėjui, subrangos sutartis yra sutartinė sutartis su tuo tiekėju. Kai tiekėjas teikia paslaugas arba medžiagos gaunamos ir naudojamos projekto užduotims atlikti, išlaidos įrašomos į projektą. Periodiškai tiekėjas siunčia patvirtintas sąskaitas faktūras, kurios yra patikrintos ir suderintos su projekte įrašytomis išlaidomis. Baigus tikrinimo procesą, tiekėjo SF patvirtinama ir išleidžiama mokėjimui.

## <a name="scenarios-for-use"></a>Naudojimo scenarijai

Tiekėjo SF programoje "Project Operations" galima naudoti dviem skirtingiems scenarijams palaikyti.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klientai naudojasi visomis subrangos funkcijomis

Tiekėjo SF funkcijos suteikia galimybę patikrinti ir suderinti laiko įrašus, medžiagų naudojimą ir išlaidų įrašus, nurodančius subrangos komponentus su tiekėjo SF eilutėmis. Šis procesas gali būti naudojamas tiekėjo SF eilučių tikslumui patikrinti. Kai patvirtinimo procesas bus baigtas ir tiekėjo SF bus patvirtinta, programa pakeis faktines sumas, kurios buvo įrašytos patvirtintais laiko, išlaidų ir medžiagų naudojimo žurnalais, ir sukurs naujas faktines išlaidų faktines vertes naudodama tiekėjo SF eilutes.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klientai nenaudoja visų subrangos funkcijų, bet nori turėti vieningą projektų išlaidų rodinį programoje "Project Operations"

Jei stebite subrangos procesą trečiosios šalies sistemoje, galite įrašyti išlaidas iš tos trečiosios šalies sistemos į "Project Operations" sukurdami tiekėjo SF, kuriose nenurodomos subrangos sutartys. Tokiu būdu jūsų projektų vadovai gali turėti vieną, vieningą visų konkretaus projekto išlaidų vaizdą.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Tiekėjo SF kūrimas programoje "Project Operations"

Tiekėjo sąskaitas faktūras galima kurti dviem būdais:

- Iš tiekėjo SF sąrašo puslapio arba išsamios informacijos puslapio, skirto vienai tiekėjo SF
- Subrangos sąrašo puslapyje arba išsamios informacijos puslapyje, skirtame vienai subrangos sutarčiai

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Kūrimas tiekėjo SF sąrašo puslapyje arba išsamios informacijos puslapyje

1. Eikite į **Pirkimo** \> **tiekėjo SF**.
2. Tiekėjo SF sąrašo puslapyje arba išsamios informacijos puslapyje, skirtame vienai tiekėjo SF, pasirinkite **Nauja**, kad sukurtumėte naują tiekėjo SF.

Tokiu būdu sukurtos tiekėjo sąskaitos faktūros taip pat gali nurodyti subrangos sutartį.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Kūrimas iš subrangos sąrašo puslapio arba išsamios informacijos puslapio

1. Eikite į **Pirkimo** \> **subrangos sutartys.**
2. Pasirinkite vieną ar daugiau subrangos sutarčių.
3. Subrangos sąrašo puslapyje arba vienos subrangos sutarties išsamios informacijos puslapyje pasirinkite **Kurti tiekėjo SF**, kad sukurtumėte naują tiekėjo SF.

Nauja tiekėjo SF juodraščio **būsenoje** sukuriama kiekvienai pasirinktai subrangos sutarčiai.

Tokiu būdu sukurtos tiekėjo SF visada nurodo subrangos sutartį tiekėjo SF antraštėje. Kiekvienoje subrangos sutarties eilutėje, kurioje yra laiko ir medžiagų atsiskaitymo metodas, tiekėjo SF bus sukurta eilutė. Kiekvienoje subrangos sutarties eilutėje, kurioje yra fiksuotos kainos atsiskaitymo metodas, tiekėjo SF bus sukurta eilutė kiekvienam subrangos eilutės įvykiui, kurio būsena **paruošta sf**.

Šie laukai ir susiję įrašai bus nukopijuoti iš subrangos sutarties į tiekėjo SF antraštę:

- Tiekėjo.
- Susiję kainoraščiai bus nukopijuoti į tiekėjo SF kaip kainoraščiai.
- Valiuta.
- Sutarčių sudarymo vienetas.
- Mokėjimo sąlygos.

Laiko ir medžiagų subrangos eilutėse šie laukai ir susiję įrašai bus nukopijuoti iš subrangos eilutės į tiekėjo SF eilutę:

- Subrangos ir subrangos linijų nuorodos
- Operacijos klasė
- Vaidmuo
- Operacijos kategorija
- Produktų laukai
- Project
- Užduotis
- Rezervuojami ištekliai

Fiksuotos kainos subrangos eilutėse šie laukai bus nukopijuoti iš subrangos linijos ir subrangos linijos tarpinio įvykio vietos į tiekėjo SF eilutę:

- Subrangos ir subrangos linijų nuorodos.
- Sandorio klasė. Pagal numatytuosius nustatymus reikšmė bus **Milestone**.
- Tarpinio etapo pavadinimas ir suma bus nukopijuoti iš susijusios subrangos linijos etapo.
- Vartotojas galės pasirinkti projektą ir užduotį tiekėjo SF eilutėje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
