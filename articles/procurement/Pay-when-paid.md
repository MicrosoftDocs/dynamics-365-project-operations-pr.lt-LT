---
title: Tiekėjo mokėjimai „mokėti sumokėjus“
description: Šioje temoje paaiškinta, kaip naudoti scenarijų „mokėti sumokėjus“ (PWP).
author: mukumarm
ms.date: 08/18/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: mukumarm
ms.openlocfilehash: d1fe8d92663b31b22dc405fc1f3e06d976e6c5dc
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525388"
---
# <a name="pay-when-paid-vendor-payments"></a>Tiekėjo mokėjimai „mokėti sumokėjus“

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje paaiškinta, kaip naudoti scenarijų „mokėti sumokėjus“ (PWP).

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Sukurkite pirkimo užsakymą, kuriame būtų PWP sąlygos

Kai registruojate tiekėjo sąskaitą faktūrą, jei tiekėjui taikomos PWP sąlygos, jos rodomos pirkimo užsakymo eilutėse. Norėdami sukurti pirkimo užsakymą su PWP sąlygomis atlikite nurodytus veiksmus.

1. Programoje „Microsoft Dynamics 365 Finance“ atlikite vieną arba kelis iš šių veiksmų.

    - Eikite į **Įsigijimas ir šaltinio pasirinkimas** \> **Pirkimo užsakymai** \> **Visi pirkimo užsakymai**. Veiksmų srityje pasirinkite **Naujas**. Dialogo lange **Pirkimo užsakymo kūrimas** pasirinkite tiekėją, kuriam nustatytos projekto PWP sąlygos, įveskite kitą reikiamą informaciją, tada pasirinkite **Gerai**.
    - Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**. Veiksmų srities skirtuke **Valdyti** pasirinkite **Elementų užduotys**. Pasirinkite pirkimo užsakymą. Pasirinkite tiekėją, kuriam nustatytos projekto PWP sąlygos, tada pasirinkite **Gerai**.

2. Puslapio **Pirkimo užsakymas** skirtuke **Pirkimo užsakymo eilutės** pasirinkite **Įtraukti eilutę**, kad sukurtumėte pirkimo užsakymo eilutę.
3. Pasirinkite prekės numerį arba įsigijimo kategoriją ir įveskite kitą reikiamą informaciją. Peržiūrėkite tiekėjo pirkimo užsakymo eilutės išsamią informaciją.

    Parinktis **Mokėti sumokėjus** pasirenkama automatiškai, o lauko **PWP ribinė procentinė dalis** reikšmė automatiškai nukopijuojama iš lauko **PWP ribinė procentinė dalis** puslapyje **Projektai**.

4. Jei tiekėjui nenorite taikyti PWP sąlygų (pirkimo užsakymo eilutei), išvalykite parinktį **Mokėti sumokėjus**. Tokiu atveju pirkimo užsakymo eilutės laukas **PWP ribinės vertės procentinis dydis** bus iš naujo nustatytas kaip **0** (nulis).
5. Veiksmų srities puslapio **Pirkimo užsakymas** skirtuke **Pirkimas** pasirinkite **Patvirtinti**, kad patvirtintumėte pirkimo užsakymą.
6. Veiksmų srities skirtuke **Sąskaita faktūra** pasirinkite **Sąskaita faktūra**, kad sukurtumėte pirkimo užsakymo sąskaitą faktūrą.

## <a name="create-a-project-invoice-proposal"></a>Projekto sąskaitos faktūros pasiūlymo kūrimas

Projekto sąskaitų faktūrų pasiūlymai naudojami norint klientui sukurti projekto sąskaitas faktūras. PWP scenarijuje tiekėjo mokėjimai priklauso nuo kliento mokėjimų pagal PWP parametrus. Tačiau yra parinkčių, kurios leidžia išleisti mokėjimus be kliento mokėjimų, kai to reikia. Norėdami klientui sukurti projekto sąskaitą faktūrą, atlikite toliau nurodytus veiksmus.

1. „Customer Engagement“ programose eikite į **Projektas** \> **Projektai** ir pasirinkite projektą.
2. Skirtuke **Faktiniai duomenys** pasirinkite faktinių duomenų eilutę, sugeneruotą pirkimo užsakymo, kurioje yra operacijos tipas **Pardavimas, už kurį neišrašyta sąskaita**. Tada pasirinkite **Paruošta sąskaitai faktūrai**.
3. Eikite į **Pardavimas** \> **Pardavimai** \> **Projekto sutartis** ir pasirinkite projekto sutartį.
4. Veiksmų srityje pasirinkite **Sąskaita faktūra**, kad sukurtumėte kliento sąskaitą faktūrą.
5. Naudodami „Finance“ eikite į **Projektų tvarkymas ir apskaita** \> **Periodinis** \> **Importuoti iš eilučių paruošimo lentelės**, tada pasirinkite **Gerai**, kad užpildytumėte „Project Operations“ integravimo žurnalą.
6. Eikite į to **Projektų tvarkymas ir apskaita** \> **Projektų sąskaitos faktūros** \> **Projekto sąskaitos faktūros pasiūlymas** ir pasirinkite **Skelbti**, kad paskelbtumėte sąskaitos faktūros pasiūlymą, kuris buvo sukurtas projektui.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliento mokėjimo atnaujinimas ir mokėjimas tiekėjui

Kai tiekėjas baigia dirbti su projektu ir atsiunčia jums sąskaitą faktūrą, turite peržiūrėti projekto būseną ir kliento sąskaitas faktūras, kad nustatytumėte, ar buvo įvykdytos projekto PWP sąlygos. Jei tiekėjo PWP sąlygos įvykdytos, galite nustatyti, kurias tiekėjo sąskaitos faktūros eilutes apmokėti, remdamiesi kliento mokėjimais. Jei nusprendžiate sumokėti tiekėjui, nors PWP sąlygos nebuvo įvykdytos, galite perrašyti PWP sąlygas puslapyje **Tiekėjo sąskaita faktūra „mokėti sumokėjus“**.

1. Naudodami „Finance“ eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projektą.
2. Veiksmų srityje pasirinkite **Valdymas**, tada pasirinkite **Tiekėjo sąskaitos faktūros**, kad būtų parodytos visos projektui sugeneruotos tiekėjo sąskaitos faktūros.
3. Puslapyje **Tiekėjo sąskaitos faktūros „mokėti sumokėjus“** ieškos lauke įveskite reikšmes, kad rastumėte tiekėjo sąskaitą faktūrą, kurią norite peržiūrėti, tada pasirinkite **Ieškoti**.
4. Pasirinkite parinktį **Mokėti sumokėjusi**, norėdami peržiūrėti tik PWP sąskaitas faktūras.
5. „Fast Tab“ **Tiekėjo sąskaitos faktūros eilutės** pasirinkite eilutes, kurias norite išleisti apmokėjimui.
6. Pasirinkite **Išleisti tiekėjo mokėjimą**. Parinktis **Mokėti sumokėjus** išvaloma, o lauko **Paruošta mokėti** reikšmė pakeičiama į **Taip**.
