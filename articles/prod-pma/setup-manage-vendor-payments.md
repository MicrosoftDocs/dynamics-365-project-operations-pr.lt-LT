---
title: Tiekėjo mokėjimų „mokėti sumokėjus“ nustatymas ir naudojimas
description: Šioje temoje paaiškinama, kaip sukurti „mokėjimo sumokėjus“ (PWP) sąlygas, kad būtų galima atlikti dalinius tiekėjo mokėjimus remiantis kliento mokėjimais.
author: RadhikaRS
manager: AnnBe
ms.date: 03/30/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: e872c4a2d35cef4cddc6851615c6c4d73b4e9d9a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080815"
---
# <a name="set-up-and-use-pay-when-paid-vendor-payments"></a>Tiekėjo mokėjimų „mokėti sumokėjus“ nustatymas ir naudojimas

[!include [banner](../includes/banner.md)]

Kai patvirtinate, kad tiekėjas dirbs kaip subrangovas, galite norėti sustabdyti mokėjimą tiekėjui, kol jūsų klientas sumokės už projektą. Jei pageidaujate šio scenarijaus, galite nustatyti „mokėti sumokėjus“ (PWP) sąlygas konfigūruodami tiekėjo pirkimo užsakymą.

Pavyzdžiui, kai klientas sumoka pagal projekto sąskaitą faktūrą, galite sumokėti dalį tiekėjo sąskaitos faktūros sumos arba visą sumą. Tiesiog nustatykite PWP sąlygas, nurodančias, kad tiekėjas gaus mokėjimą, kai jūs iš kliento gausite susijusio mokėjimo procentinę dalį. Jei iš kliento gaunate dalinį mokėjimą, galite rankiniu būdu apmokėti dalį susijusio tiekėjo sąskaitų faktūrų.

Šiame pavyzdyje pateikiamas procesas, kai naudojamos PWP sąlygos.

## <a name="example"></a>Pavyzdžiui

Jūsų organizacija sutinka pateikti klientui 100 kompiuterių su įdiegta programine įranga – vieno kompiuterio kaina 150,00 JAV dolerių (USD). Tada pasamdykite tiekėją, kad pristatytų jums kompiuterius su įdiegta programine įranga. Pagal sutartį klientas turi patvirtinti kompiuterių kokybę prieš sumokėdamas jūsų organizacijai. Jūsų organizacijos strategija yra sustabdyti mokėjimą tiekėjams, kol jums sumokės klientas. Todėl galite nustatyti projektą taip, kad jo PWP procentas būtų 100.

Tiekėjas siunčia jums 100 kompiuterių su įdiegta programine įranga ir 10 000,00 USD sąskaita faktūra. Kadangi nustatytos projekto PWP sąlygos, gavę kompiuterius jūs tiekėjui nemokate. Jūs siunčiate kompiuterius klientui kartu su 15 000,00 sąskaita faktūra. Klientas patikrina kompiuterius ir patvirtina visą projekto sąskaitos faktūros sumą.

Gavę iš kliento visą mokėjimą sumokate tiekėjui 10 000,00 – visą tiekėjo sąskaitos faktūros sumą.

## <a name="set-up-pwp-terms-for-a-project"></a>Projekto PWP sąlygų nustatymas

Nustatydami projekto PWP sąlygas turite nurodyti, kaip procentą, mažiausią sumą, kurią klientas turi jums sumokėti už projektą, kad jūsų galėtumėte mokėti tiekėjui. Ribinė suma automatiškai apskaičiuojama pagal projekto kliento sąskaitas faktūras. Norėdami nustatyti PWP sąlygų ribinę procentinę dalį, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.
2. Raskite ir atidarykite projektą, kuriam norite nustatyti PWP sąlygas.
3. „FastTab“ **Tiekėjų sutartys** pasirinkite **Įtraukti eilutę**.
3. Lauke **Kliento kodas** pasirinkite vieną iš pateiktų parinkčių:

    - **Lentelė** – PWP sąlygos taikomos vienam tiekėjui.
    - **Grupė** – PWP sąlygos taikomos visiems tiekėjams, priklausantiems tiekėjų grupei.
    - **Visi** – PWP sąlygos taikomos visiems tiekėjams.

4. Jei ankstesniame veiksme pasirinkote **Lentelė** arba **Grupė**, lauke **Tiekėjas / tiekėjų grupė**, pasirinkite tiekėją arba tiekėjų grupę, kuriai taikomos PWP sąlygos. Jei ankstesniame veiksme pasirinkote **Visi**, lauko **Tiekėjas / tiekėjų grupė** negalima redaguoti.
5. Jei projekto tiekėjui nustatomos tiekėjo sulaikymo sąlygos, lauke **Tiekėjo sulaikymo sąlygos**, pasirinkite sulaikymo sąlygų taisyklės ID.
6. Lauke **PWP ribinė procentinė dalis** įveskite projekto ribinę procentinę dalį. Projekte įvestas procentas apibrėžia minimalią sumą, kurią klientas turi sumokėti prieš jums mokant tiekėjui.

## <a name="create-a-po-that-has-pwp-terms"></a>Pirkimo užsakymo su PWP sąlygomis kūrimas

Kai registruojate tiekėjo sąskaitą faktūrą, jei tiekėjui taikomos PWP sąlygos, jos rodomos pirkimo užsakymo eilutėse. Norėdami sukurti pirkimo užsakymą su PWP sąlygomis atlikite nurodytus veiksmus.

1. Eikite į **Įsigijimas ir šaltinio pasirinkimas** \> **Pirkimo užsakymai** \> **Visi pirkimo užsakymai**.
2. Veiksmų srityje pasirinkite **Naujas**. Tada dialogo lange **Kurti pirkimo užsakymą** įveskite reikiamą informaciją ir pasirinkite **Gerai**.

    Arba atidarykite esamą pirkimo užsakymą, esantį sąrašo puslapyje **Visi pirkimo užsakymai**.

4. Puslapyje **Pirkimo užsakymas**, „FastTab“ **Pirkimo užsakymo eilutės**, peržiūrėkite tiekėjo pirkimo užsakymo eilutės duomenis. Parinktis **Mokėti sumokėjus** pasirenkama automatiškai, o lauko **PWP ribinė procentinė dalis** reikšmė automatiškai nukopijuojama iš lauko **PWP ribinė procentinė dalis** puslapyje **Projektai**.
6. Jei tiekėjui nenorite taikyti PWP sąlygų (pirkimo užsakymo eilutei), išvalykite parinktį **Mokėti sumokėjus**. Tokiu atveju pirkimo užsakymo eilutės laukas **PWP ribinė procentinė dalis** bus iš naujo nustatytas į 0 (nulis).

## <a name="update-a-customer-payment-and-pay-the-vendor"></a>Kliento mokėjimo atnaujinimas ir mokėjimas tiekėjui

Kai tiekėjas baigia dirbti su projektu ir atsiunčia jums sąskaitą faktūrą, turite peržiūrėti projekto būseną ir kliento sąskaitas faktūras, kad nustatytumėte, ar įvykdytos projekto PWP sąlygos. Jei tiekėjo PWP sąlygos įvykdytos, galite nustatyti, kurias tiekėjo sąskaitos faktūros eilutes apmokėti, remdamiesi kliento mokėjimais. Jei nusprendžiate sumokėti tiekėjui, nors PWP sąlygos nebuvo įvykdytos, galite perrašyti PWP sąlygas puslapyje **Tiekėjo sąskaita faktūra „mokėti sumokėjus“**.

1. Eikite į **Projektų valdymas ir apskaita** \> **Užklausos ir ataskaitos** \> **Sulaikymo užklausos** \> **Tiekėjo sąskaita faktūra „mokėti sumokėjus“**.
2. Puslapyje **Tiekėjo sąskaitos faktūros „mokėti sumokėjus“** ieškos lauke įveskite reikšmes, kad rastumėte tiekėjo sąskaitą faktūrą, kurią norite peržiūrėti, tada pasirinkite **Ieškoti**.
3. „FastTab“ **Tiekėjo sąskaitos faktūros eilutės** pasirinkite eilutes, kurias norite pakeisti.
4. Jei sąskaitos faktūros eilutės **Mokėti sumokėjus** sąlygos neįvykdytos, pasirinkite **Išleisti tiekėjo mokėjimą**. Parinktis **Mokėti sumokėjus** išvaloma, o lauko **Paruošta mokėti** reikšmė pakeičiama į **Taip**.
