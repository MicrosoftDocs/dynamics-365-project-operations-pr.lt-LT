---
title: Tiekėjo SF su patvirtintais faktiniais duomenimis tikrinimas
description: Šioje temoje paaiškinama, kaip "Microsoft" Dynamics 365 Project Operations leidžia projektų vadovams patikrinti tiekėjo SF su faktiniais duomenimis, kurie buvo patvirtinti kaip rangovai, atliko darbą ir įrašytą laiką, taip pat išlaidas ir medžiagas, kurias naudojo projekto komandos nariai.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3350a51bde2872036b79a789fae23ea6790fb21a
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8585480"
---
# <a name="verification-of-vendor-invoices-with-approved-actuals"></a>Tiekėjo SF su patvirtintais faktiniais duomenimis tikrinimas

[!include [banner](../../includes/dataverse-preview.md)]

_ **Taikoma:** "Lite" diegimas – sandoris su "proforma" SF išrašymu

Microsoft Dynamics 365 Project Operations leidžia projektų vadovams patikrinti tiekėjo SF eilutes šiais būdais:

- **Naudokite tiekėjo SF eilučių lauką Tikrinimo būsena**.
- Jei tiekėjo SF eilutės nurodo subrangos eilutę, susieti subrangovo veiklos savikainos faktines vertes su tomis tiekėjo SF eilutėmis. Saitas sukuriamas sugretinus faktinių išlaidų sumas su tiekėjo SF eilutėmis.

    > [!NOTE]
    > Nors tiekėjo SF eilučių, kurios nenurodo subrangos sutarties, tikrinimo būseną galima sekti, faktinių išlaidų negalima susieti su tomis tiekėjo SF eilutėmis.

## <a name="verification-status"></a>Tikrinimo būsena

Tiekėjo SF eilutės laukas **Tikrinimo būsena** nurodo tą tikrinimo būseną. Palaikomos šios būsenos:

1. Nepradėta
2. Vykdoma
3. Užbaigta

Tiekėjo SF eilutes, kurių tikrinimo būsena **nepradėta**, galima redaguoti.

Nebegalima redaguoti tiekėjo SF eilučių, kurių tikrinimo būsena **vykdoma**. Tiekėjo SF eilutėje, nurodančioje subrangos sutartį, tikrinimo būsena automatiškai nustatoma į **Vykdoma**, kai tik pirmoji faktinė savikaina bus suderinta su tiekėjo SF eilute.

Nebegalima redaguoti tiekėjo SF eilučių, kurių tikrinimo būsena **yra Baigta**. Kai visos tiekėjo SF eilutės turi šią tikrinimo būseną, tiekėjo SF galima patvirtinti.

## <a name="match-cost-actuals-to-vendor-invoice-lines"></a>Suderinti savikainos faktines vertes su tiekėjo SF eilutėmis

Faktinių išlaidų atitikimas padeda atlikti tiekėjo SF eilutės tikrinimo procesą. Norėdami suderinti savikainos faktines vertes su tiekėjo SF eilute, atlikite šiuos veiksmus.

1. Atidarykite tiekėjo SF eilutę ir pasirinkite skirtuką **Nesuderintos savikainos faktinės** sumos. Tinklelyje rodomas faktinių išlaidų sąrašas, nurodantis tą pačią subrangos eilutę kaip ir tiekėjo SF eilutė.
2. Pasirinkite vieną ar daugiau faktinių išlaidų, tada įrankių juostoje virš tinklelio pasirinkite **Gretinti**. Sistema patvirtina, kad pasirinktos faktinės išlaidos gali būti suderintos. Atlikus tikrinimą, faktiniai išlaidų duomenys susiejami su tiekėjo SF eilute.

### <a name="validation-criteria-that-are-used-to-link-cost-actuals-to-vendor-invoice-lines"></a>Tikrinimo kriterijai, naudojami kaštų faktinėms išlaidoms susieti su tiekėjo SF eilutėmis

Derinimo proceso metu ryšį tarp faktinės savikainos ir tiekėjo SF eilutės galima nustatyti tik tuo atveju, jei tenkinamos abi šios sąlygos:

- Kiekvienos **pasirinktos faktinės savikainos laukas Koregavimo būsena** turi būti tuščias. Kitaip tariant, faktinių išlaidų faktinės sumos neturi būti pakeistos kitomis faktinėmis išlaidomis atšaukimo, patvirtinimo atšaukimo ar taisymo žurnalo proceso metu.
- Toliau nurodytų laukų vertės suderinamos tarp tiekėjo SF eilutės ir pasirinktos faktinės savikainos. Jei tiekėjo SF eilutėje nenustatytas kuris nors laukas, jis nelaikomas gretinimu.

    - Projekto sutartis
    - Projekto sutarties eilutė
    - Operacijos klasė
    - Project
    - Užduotis
    - Išteklių kategorija
    - Operacijos kategorija
    - Produktas
    - Subrangos eilutė
    - Rezervuojami ištekliai

## <a name="unmatch-cost-actuals-from-a-vendor-invoice-line"></a>Sugretinti savikainos faktines vertes iš tiekėjo SF eilutės

Faktinių išlaidų neatitikimas taip pat gali padėti atlikti tiekėjo SF tikrinimo procesą, leidžiant pašalinti anksčiau nustatytus saitus. Savikainos faktinius duomenis galima nesuderinti tik iš tiekėjo SF eilučių, kurių tikrinimo būsena **vykdoma**. Norėdami iš tiekėjo SF eilutės suderinti faktinius savikainos duomenis, atlikite šiuos veiksmus.

1. Atidarykite tiekėjo SF eilutę ir pasirinkite skirtuką **Suderintos savikainos faktinės** sumos. Tinklelyje rodomas faktinių išlaidų, nurodančių tiekėjo SF eilutę, sąrašas.
2. Pasirinkite vieną ar daugiau faktinių išlaidų, tada įrankių juostoje virš tinklelio pasirinkite **Nesuderinti**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
