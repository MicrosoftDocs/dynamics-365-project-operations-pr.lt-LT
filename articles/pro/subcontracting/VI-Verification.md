---
title: Tiekėjo sąskaitų faktūrų su patvirtintais faktiniais duomenimis tikrinimas
description: Šiame straipsnyje paaiškinama, kaip "Microsoft" Dynamics 365 Project Operations projektų vadovai tikrina tiekėjo SF su faktinėmis sąskaitomis faktūromis, kurios buvo patvirtintos kaip rangovai, atliko darbą ir įrašė laiką, taip pat išlaidomis ir medžiagomis, kurias naudojo projekto komandos nariai.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ab9f69e36aa58bfe3a2f8e3455db66b6bceea968
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261757"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Tiekėjo sąskaitų faktūrų su patvirtintais faktiniais duomenimis tikrinimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

"Microsoft" Dynamics 365 Project Operations leidžia projektų vadovams tikrinti tiekėjo SF eilutes šiais būdais:

- **Naudokite tiekėjo SF eilučių lauką Patvirtinimo būsena**.
- Jei tiekėjo SF eilutėse nurodoma subrangos eilutė, susiekite faktines išlaidas iš subrangovo veiklos su tomis tiekėjo SF eilutėmis. Saitas sukuriamas suderinus išlaidų faktines sumas su tiekėjo SF eilutėmis.

    > [!NOTE]
    > Nors tiekėjo SF eilučių, kurios nenurodo subrangos sutarties, tikrinimo būseną galima sekti, faktinių išlaidų negalima susieti su tomis tiekėjo SF eilutėmis.

## <a name="verification-status"></a>Patvirtinimo būsena

Tiekėjo SF eilutės laukas **Patvirtinimo būsena** nurodo tą patvirtinimo būseną. Palaikomos šios būsenos:

1. Nepradėta
2. Vykdoma
3. Užbaigta

Tiekėjo SF eilutes, kurių patvirtinimo būsena **yra Nepradėta**, galima redaguoti.

Tiekėjo SF eilučių, kurių patvirtinimo būsena **yra Vykdoma**, nebegalima redaguoti. Tiekėjo SF eilutėje, kuri nurodo subrangos sutartį, tikrinimo būsena automatiškai nustatoma kaip **Vykdoma**, kai tik pirmosios faktinės išlaidos suderinamos su tiekėjo SF eilute.

Tiekėjo SF eilučių, kurių patvirtinimo būsena **yra Baigta**, redaguoti nebegalima. Kai visos tiekėjo SF eilutės turi šią patvirtinimo būseną, tiekėjo SF gali būti patvirtinta.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Faktinių išlaidų susiejimas su tiekėjo SF eilutėmis

Faktinių išlaidų atitikimas padeda atlikti patvirtinimo procesą tiekėjo SF eilutėje. Norėdami susieti faktines išlaidų sumas su tiekėjo SF eilute, atlikite šiuos veiksmus.

1. Atidarykite tiekėjo SF eilutę ir pasirinkite skirtuką **Nesuderintos savikainos faktinės** sumos. Tinklelyje rodomas faktinių išlaidų sąrašas, nurodantis tą pačią subrangos eilutę kaip ir tiekėjo SF eilutė.
2. Pasirinkite vieną ar daugiau faktinių išlaidų, tada įrankių juostoje virš tinklelio pasirinkite **Atitiktis**. Sistema patikrina, ar pasirinktos savikainos faktinės sumos gali būti suderintos. Praėjus tikrinimui, faktinės savikainos susiejamos tiekėjo SF eilutėje.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Tikrinimo kriterijai, naudojami susieti faktines išlaidų sumas su tiekėjo SF eilutėmis

Susiejimo proceso metu saitą tarp faktinės savikainos ir tiekėjo SF eilutės galima nustatyti tik tuo atveju, jei įvykdomos abi šios sąlygos:

- Laukas **Koregavimo būsena** kiekvienai pasirinktai faktinei savikainai turi būti tuščias. Kitaip tariant, faktinės išlaidos neturėjo būti pakeistos kitomis faktinėmis išlaidomis atšaukimo, patvirtinimo atšaukimo ar taisymo žurnalo proceso metu.
- Toliau nurodytų laukų reikšmės suderinamos tiekėjo SF eilutėje ir pasirinktoje faktinėje savikainoje. Jei tiekėjo SF eilutėje nenustatytas kuris nors laukas, į jį neatsižvelgiama.

    - Projekto sutartis
    - Projekto sutarties eilutė
    - Operacijos klasė
    - Project
    - Užduotis
    - Išteklių kategorija
    - Operacijos kategorija
    - Produktas
    - Subrangos linija
    - Rezervuojami ištekliai

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Nesuderintų išlaidų faktinių sumų iš tiekėjo SF eilutės

Faktinių išlaidų neatitikimas taip pat gali padėti atlikti tiekėjo SF patvirtinimo procesą, nes bus galima pašalinti anksčiau nustatytus saitus. Faktines išlaidų sumas galima nesuderinti tik iš tiekėjo SF eilučių, kurių patvirtinimo būsena **yra Vykdoma**. Norėdami nesuderinti faktinių išlaidų sumų iš tiekėjo SF eilutės, atlikite šiuos veiksmus.

1. Atidarykite tiekėjo SF eilutę ir pasirinkite skirtuką **Sutapusios savikainos faktinės** sumos. Tinklelyje rodomas faktinių išlaidų sąrašas, nurodantis tiekėjo SF eilutę.
2. Pasirinkite vieną ar daugiau faktinių išlaidų, tada virš tinklelio esančioje įrankių juostoje pasirinkite **Nesuderinti**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
