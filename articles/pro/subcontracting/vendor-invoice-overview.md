---
title: Tiekėjo sąskaitų faktūrų išrašymas – sąvoka ir kūrimas
description: Šiame straipsnyje aprašoma tiekėjo sąskaitų faktūrų naudojimo secnarijai ir paaiškinta, kaip jas sukurti naudojant „Microsoft Dynamics 365 Project Operations“.
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

„Microsoft Dynamics 365 Project Operations“ tiekėjo sąskaitų faktūrų išrašymas gali būti naudojamas įrašant išlaidas pagal paslaugų ir (ar) medžiagos pristatymą projektui, kurį užbaigė pardavėjai.

Kai aptarnavimas ir (arba) medžiaga yra prisodintas pardavėjui, šis su šiuo pardavėju susitarimas dėl išsaisvėjo. Kai tiekėjas teikia paslaugas arba kai medžiaga gauta ir naudojama projekto užduotims, išlaidos įrašomas į projektą. Periodiškai, tiekėjas siunčia sąskaitas, kurios yra tikrinamos ir gretintos su įrašyomis projekto išlaidoms. Baigus tikrinimo procesą tiekėjo sąskaita faktūra patvirtinama ir išleidžiama apmokėti.

## <a name="scenarios-for-use"></a>Naudojimo scenarijai

„Project Operations“ tiekėjo sąskaitas faktūras galima naudoti dviem skirtingais scenarijais.

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klientai naudoja visas susaistymas ir funkcijas

Naudojant tiekėjo sąskaitų faktūrų funkcijas galima patikrinti laiko įrašus, medžiagos naudojimą ir išlaidų įrašus, kurie nurodo komponentus, kurie yra sugretinti su tiekėjo sąskaitos faktūros eilutėmis. Šį procesą galima naudoti tiekėjo sąskaitos faktūros eilučių tikslumui patikrinti. Baigus tikrinimo procesą ir patvirtinus tiekėjo sąskaitą faktūrą, sistema, naudodama tiekėjo sąskaitos faktūros eilutes, surašo faktinius duomenis, kurie buvo įrašyti patvirtintu laiku, išlaidoms ir medžiagos naudojimo žurnalams, ir sukuria naujus faktinius išlaidų faktinius duomenis.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klientai nenaudoja visų papildomai subrangos sutarties funkcijų, tačiau nori turėti vieningą projektų išlaidų vaizdą „Project Operations“

Jei stebite trečiosios šalies sistemos indų sąsodį, galite įrašyti išlaidas iš tos trečiosios šalies sistemos į „Project Operations", sukurdami tiekėjo sąskaitas faktūras, kurios neturi nuorodos į sugretinimo funkciją. Tokiu būdu jūsų projektų vadovai gali turėti bendrą bendrą visų projekto išlaidų vaizdą.

## <a name="creation-of-vendor-invoices-in-project-operations"></a>Sukurkite tiekėjo sąskaitas„Project Operations“

Tiekėjo sąskaitas galima kurti dviem būdais:

- Tiekėjo sąskaitų faktūrų sąrašo puslapyje arba vienos tiekėjo sąskaitos faktūros išsamios informacijos puslapyje
- Iš nea fortitų sąrašo puslapio arba išsamios informacijos puslapio, kad būtų galima naudoti vieną

### <a name="creation-from-the-vendor-invoice-list-page-or-details-page"></a>Kūrimas iš tiekėjo sąskaitų faktūrų sąrašo puslapio arba išsamios informacijos puslapio

1. Eikite į **Pirkimas** \> **Tiekėjo sąskaitos**.
2. Tiekėjo sąskaitų faktūrų sąrašo puslapyje arba vienos tiekėjo sąskaitos faktūros išsamios informacijos puslapyje pasirinkite **Naujas**, kad sukurtumėte naują tiekėjo sąskaitą faktūrą.

Taip sukurtos tiekėjo sąskaitos faktūros taip pat gali nurodyti susaista.

### <a name="creation-from-the-subcontract-list-page-or-details-page"></a>Kūrimas iš papildomų tiekėjų sąrašo puslapio ar išsamios informacijos puslapio

1. Eikite į **Pirkimas** \> **Papildomi tiekėjai**.
2. Pasirinkite vieną ar daugiau papildomų tiekėjų.
3. Papildomo tiekėjo sąskaitų faktūrų sąrašo puslapyje papildomo tiekėjo puslapyje rinkitės **Kurti tiekėjo sąskaitą**, kad sukurtumėte naują tiekėjo sąskaitą faktūrą.

Sukuriama nauja tiekėjo sąskaita faktūra, **kurios** būsena yra Juodraštis, kiekvienam jūsų pažymėtam tarpui.

Taip sukurtoms tiekėjo sąskaitoms faktūroms visada pateikiama nuoroda į tiekėjo sąskaitos faktūros antraštę. Kiekviena eilutė su laiko ir medžiagos sąskaitų išrašymo būdu, dėl kurios tiekėjo sąskaitoje faktūroje bus sukurta eilutė. Kiekviena eilutė, eilutėje, kuri yra su fiksuotos kainos sąskaitų išrašymo būdu, sukuria eilutę tiekėjo sąskaitoje faktūroje kiekvienam etapui, kurio būsena yra **Paruošta išrašyti sąskaitą faktūrą**.

Iš tiekėjo sąskaitos faktūros antraštės bus kopijuojami šie laukai ir susiję įrašai:

- Tiekėjas.
- Susiję kainorašiai bus kopijuojami į tiekėjo sąskaitą faktūrą kaip kainoraščius.
- Valiuta.
- Sutartį sudarantis vienetas.
- Mokėjimo sąlygos.

Toliau nurodyti laiko ir medžiagos, kuri yra indų, ir susijusių įrašų laukai bus kopijuojami iš tos eilutės į tiekėjo sąskaitos faktūros eilutę:

- Sąrangos ir sąrangos linijos nuorodos
- Operacijos klasė
- Vaidmuo
- Operacijos kategorija
- Produkto laukai
- Project
- Užduotis
- Rezervuojami ištekliai

Dėl fiksuotos kainos papildomo tiekėjo eilutės, tolesni laukai bus nukopijuoti iš papildomo tiekėjo eilutės ir papildomo tiekėjo etapo į tiekėjo sąskaitos eilutę:

- Sąrangos ir sąrangos linijos nuorodos.
- Operacijos klasė. Pagal numatytuosius nustatymus reikšmė bus **etapas**.
- Etapo pavadinimas ir suma bus kopijuojami iš susijusio, su susijusiu, perdėto eilutės etapo.
- Vartotojas galės pasirinkti projektą ir užduotį tiekėjo sąskaitos faktūros eilutėje.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
