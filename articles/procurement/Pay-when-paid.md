---
title: Mokėjimas, kai mokamas tiekėjo mokėjimas
description: Šioje temoje paaiškinama, kaip naudoti mokėjimo, kai mokama (PWP) scenarijų.
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
# <a name="pay-when-paid-vendor-payments"></a>Mokėjimas, kai mokamas tiekėjo mokėjimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje paaiškinama, kaip naudoti mokėjimo, kai mokama (PWP) scenarijų.

## <a name="create-a-purchase-order-that-has-pwp-terms"></a>Pirkimo užsakymo su PWP sąlygomis kūrimas

Kai registruojate tiekėjo SF, jei tiekėjui taikomos PWP sąlygos, tos sąlygos rodomos pirkimo užsakymo (PU) eilutėse. Norėdami sukurti pirkimo užsakymą su PWP sąlygomis atlikite nurodytus veiksmus.

1. Programoje " Microsoft Dynamics 365 Finance" atlikite vieną iš šių veiksmų:

    - Eikite į **Įsigijimas ir šaltinio pasirinkimas** \> **Pirkimo užsakymai** \> **Visi pirkimo užsakymai**. Veiksmų srityje pasirinkite **Naujas**. Dialogo lange **Kurti pirkimo užsakymą** pasirinkite tiekėją, kuriam projekte nustatytos PWP sąlygos, įveskite kitą būtiną informaciją, tada pasirinkite **Gerai**.
    - Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**. Veiksmų srities skirtuke **Tvarkyti** pasirinkite **Elemento užduotis**. Pasirinkite pirkimo užsakymą. Pasirinkite tiekėją, kuriam projekte nustatytos PWP sąlygos, tada pasirinkite **Gerai**.

2. Puslapio Pirkimo užsakymas **sparčiajame** **skirtuke Pirkimo užsakymo eilutėse** pasirinkite **Įtraukti eilutę**, kad sukurtumėte pirkimo užsakymo eilutę.
3. Pasirinkite prekės numerį arba įsigijimo kategoriją ir įveskite kitą reikiamą informaciją. Peržiūrėkite tiekėjo PU eilutės išsamią informaciją.

    Parinktis **Mokėti sumokėjus** pasirenkama automatiškai, o lauko **PWP ribinė procentinė dalis** reikšmė automatiškai nukopijuojama iš lauko **PWP ribinė procentinė dalis** puslapyje **Projektai**.

4. Jei tiekėjui nenorite taikyti PWP sąlygų (pirkimo užsakymo eilutei), išvalykite parinktį **Mokėti sumokėjus**. Tokiu atveju **PU linijos PWP slenksčio procentinis** laukas bus atstatytas į **0** (nulis).
5. **Puslapio Pirkimo užsakymas** veiksmų srities skirtuke **Pirkimas** pasirinkite **Patvirtinti**, kad patvirtintumėte pirkimo užsakymą.
6. Veiksmų srities skirtuke **Sąskaita faktūra** pasirinkite **Sąskaita faktūra**, kad sugeneruotumėte pirkimo užsakymo sąskaitą faktūrą.

## <a name="create-a-project-invoice-proposal"></a>Projekto sąskaitos faktūros pasiūlymo kūrimas

Projekto sąskaitų faktūrų pasiūlymai naudojami kuriant projekto sąskaitas faktūras klientui. PWP scenarijuje tiekėjo mokėjimai priklauso nuo klientų mokėjimų pagal PWP parametrus. Tačiau yra parinkčių, leidžiančių grąžinti mokėjimus be klientų mokėjimų, kaip jums reikia. Norėdami klientui sukurti projekto sąskaitą faktūrą, atlikite šiuos veiksmus.

1. "Customer Engagement" programose eikite į **"Project Projects**"\>**ir** pasirinkite projektą.
2. Skirtuke **Faktinės** aplinkybės pasirinkite faktinę eilutę, kurią generuoja PU, turintis **neįrašytos pardavimo** operacijos tipą. Tada pasirinkite **Paruošta sąskaitai faktūrai**.
3. Eikite į **"Sales** \> **Sales** \> **Project" sutartį** ir pasirinkite projekto sutartį.
4. Veiksmų srityje pasirinkite **Sąskaita faktūra**, kad sugeneruotumėte kliento SF.
5. Dalyje Finansai eikite į **Projekto valdymas ir apskaita** \> **Periodinis importavimas** \> **iš išdėstymo lentelės** ir pasirinkite **Gerai**, kad sugeneruotumėte projekto operacijų integravimo žurnalą.
6. Eikite į **Projekto valdymas ir apskaita** \> **Projekto sąskaitos faktūros** \> **pasiūlymas** ir pasirinkite **Skelbti**, kad užregistruotumėte projektui sugeneruotą sąskaitos faktūros pasiūlymą.

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliento mokėjimo atnaujinimas ir mokėjimas tiekėjui

Kai tiekėjas baigia darbą su projektu ir atsiunčia jums sf, turite peržiūrėti projekto būseną ir kliento SF, kad nustatytumėte, ar buvo įvykdytos projekto PWP sąlygos. Jei tiekėjo PWP sąlygos įvykdytos, galite nustatyti, kurias tiekėjo sąskaitos faktūros eilutes apmokėti, remdamiesi kliento mokėjimais. Jei nusprendžiate sumokėti tiekėjui, nors PWP sąlygos nebuvo įvykdytos, galite perrašyti PWP sąlygas puslapyje **Tiekėjo sąskaita faktūra „mokėti sumokėjus“**.

1. Dalyje Finansai eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai** ir pasirinkite projektą.
2. Veiksmų srityje pasirinkite **Kontrolė**, tada pasirinkite **Tiekėjo SF**, kad būtų rodomos visos tiekėjo SF, kurios buvo sugeneruotos projektui.
3. Puslapyje **Tiekėjo sąskaitos faktūros „mokėti sumokėjus“** ieškos lauke įveskite reikšmes, kad rastumėte tiekėjo sąskaitą faktūrą, kurią norite peržiūrėti, tada pasirinkite **Ieškoti**.
4. **Pasirinkite parinktį Mokėti, kai mokama,** kad peržiūrėtumėte tik PWP sąskaitas faktūras.
5. Sparčiajame skirtuke **Tiekėjo SF eilutės** pasirinkite eilutes, kurias norite išleisti mokėjimui.
6. Pasirinkite **Išleisti tiekėjo mokėjimą**. Parinktis **Mokėti sumokėjus** išvaloma, o lauko **Paruošta mokėti** reikšmė pakeičiama į **Taip**.
