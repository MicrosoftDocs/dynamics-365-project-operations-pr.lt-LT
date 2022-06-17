---
title: Tiekėjo sąskaitų faktūrų išrašymas – sąvoka ir kūrimas
description: Šiame straipsnyje aprašoma tiekėjo SF sąvoka, naudojimo scenarijai ir kaip kurti tiekėjo SF programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 38f0760697522b7a5e561cec7d38dfd5c3eaf9fc
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911468"
---
# <a name="vendor-invoicing---concept-and-creation"></a>Tiekėjo sąskaitų faktūrų išrašymas – sąvoka ir kūrimas

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF išrašymas programoje "Microsoft" Dynamics 365 Project Operations gali būti naudojamas tiekėjų aptarnavimo ir (arba) medžiagų pristatymo į projektą išlaidoms įrašyti.

Kai paslaugos ir (arba) medžiagos yra subrangos sutartys su tiekėju, subrangos sutartis yra sutartinis susitarimas su tuo tiekėju. Kai tiekėjas teikia paslaugas arba medžiagos gaunamos ir naudojamos projekto užduotims, išlaidos įrašomos į projektą. Periodiškai tiekėjas siunčia sf, kurios yra patikrintos ir suderintos su projekte įrašytomis išlaidomis. Baigus tikrinimo procesą, tiekėjo SF patvirtinama ir išleidžiama mokėjimui.

## <a name="scenarios-for-use"></a>Naudojimo scenarijai

Tiekėjo SF projekto operacijose galima naudoti dviem skirtingiems scenarijams palaikyti.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klientai naudojasi visomis subrangos funkcijomis

Tiekėjo SF funkcijos suteikia galimybę patikrinti ir suderinti laiko įrašus, medžiagų sąnaudas ir išlaidų įrašus, kurie nurodo subrangos komponentus su tiekėjo SF eilutėmis. Šis procesas gali būti naudojamas tiekėjo SF eilučių tikslumui patikrinti. Baigus tikrinimo procesą ir patvirtinus tiekėjo SF, gretinimas atšauks faktinius duomenis, įrašytus patvirtintais laiko, išlaidų ir medžiagų naudojimo žurnalais, ir sukurs naujas savikainos faktines vertes naudodamas tiekėjo SF eilutes.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klientai nenaudoja visos subrangos patirties, bet nori turėti vieningą "Project Operations" projektų išlaidų vaizdą

Jei stebite subrangos procesą trečiosios šalies sistemoje, galite įrašyti išlaidas iš tos trečiosios šalies sistemos į "Project Operations" sukurdami tiekėjo SF, kurios nenurodo subrangos sutarčių. Tokiu būdu jūsų projektų vadovai gali turėti vieną, vieningą vaizdą apie visas konkretaus projekto išlaidas.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Tiekėjo SF kūrimas projekto operacijose

Tiekėjo SF galima kurti dviem būdais:

- Iš tiekėjo SF sąrašo puslapio arba vienos tiekėjo SF išsamios informacijos puslapio
- Iš subrangos sutarčių sąrašo puslapio arba išsamios informacijos puslapio, skirto vienai subrangos sutarčiai

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Kūrimas iš tiekėjo SF sąrašo puslapio arba išsamios informacijos puslapio

1. Eikite į **Tiekėjo SF pirkimas** \> **·**.
2. Tiekėjo SF sąrašo puslapyje arba vienos tiekėjo SF išsamios informacijos puslapyje pasirinkite **Naujas**, kad sukurtumėte naują tiekėjo SF.

Tokiu būdu sukurtos tiekėjo SF taip pat gali nurodyti subrangos sutartį.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Kūrimas iš subrangos sąrašo puslapio arba išsamios informacijos puslapio

1. Eikite į **Subrangos** \> **sutarčių pirkimas.**
2. Pasirinkite vieną ar daugiau subrangos sutarčių.
3. Subrangos sutarčių sąrašo puslapyje arba išsamios informacijos puslapyje, skirtame vienai subrangos sutarčiai, pasirinkite **Kurti tiekėjo SF**, kad sukurtumėte naują tiekėjo SF.

Kiekvienai pasirinktai subrangos sutarčiai sukuriama nauja tiekėjo SF **, kurios būsena yra Juodraštis**.

Tokiu būdu sukurtos tiekėjo SF visada nurodo tiekėjo SF porangį tiekėjo SF antraštėje. Dėl kiekvienos subrangos eilutės, kurioje yra laiko ir medžiagų atsiskaitymo metodas, tiekėjo SF bus sukurta eilutė. Dėl kiekvienos subrangos eilutės, kurioje yra fiksuotos kainos atsiskaitymo metodas, tiekėjo SF bus sukurta eilutė kiekvienam subrangos eilutės etapui, kurio būsena **yra Paruošta išrašyti SF**.

Šie laukai ir susiję įrašai bus nukopijuoti iš subrangos sutarties į tiekėjo SF antraštę:

- Tiekėjo.
- Susiję kainoraščiai bus nukopijuoti į tiekėjo SF kaip kainoraščiai.
- Valiuta.
- Sutartininkas.
- Mokėjimo sąlygos.

Laiko ir medžiagų subrangos eilučių laukai ir susiję įrašai bus nukopijuoti iš subrangos eilutės į tiekėjo SF eilutę:

- Subrangos ir subrangos eilučių nuorodos
- Operacijos klasė
- Vaidmuo
- Operacijos kategorija
- Produkto laukai
- Project
- Užduotis
- Rezervuojami ištekliai

Fiksuotos kainos subrangos eilutėse šie laukai bus nukopijuoti iš subrangos eilutės ir subrangos eilutės etapo į tiekėjo SF eilutę:

- Subrangos ir subrangos eilučių nuorodos.
- Operacijų klasė. Pagal numatytuosius nustatymus reikšmė bus **orientyras**.
- Tarpinio etapo pavadinimas ir suma bus nukopijuoti iš susijusio subrangos eilutės etapo.
- Vartotojas galės pasirinkti projektą ir užduotį tiekėjo SF eilutėje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
