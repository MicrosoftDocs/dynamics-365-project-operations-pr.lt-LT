---
title: Išplėstinių atsiskaitymo sutarčių kūrimas atsižvelgiant į eigą
description: Šioje temoje paaiškinama, kaip kurti projektų sutartis, kad galėtumėte generuoti klientų sąskaitas faktūras remdamiesi atlikto darbo procentine dalimi.
author: RadhikaRS
ms.date: 03/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: bdafc2ed2398054d8b0bf42bdd96dfe0eccee93b
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8683173"
---
# <a name="create-advanced-contracts-for-billing-based-on-progress"></a>Išplėstinių atsiskaitymo sutarčių kūrimas atsižvelgiant į eigą
[!include [banner](../includes/banner.md)]

Šioje temoje paaiškinama, kaip kurti projektų sutartis, kad galėtumėte sukurti klientų sąskaitas faktūras remdamiesi atlikto darbo procentine dalimi. Sąskaitos faktūros sumos automatiškai apskaičiuojamos pagal darbo, kurį nustatėte projekte, biudžeto kategorijas. Sąskaitų faktūrų išrašymo laikas nustatomas jums derantis su klientu dėl projekto sutarties.

Naudodami šioje temoje nurodytas procedūras galite nustatyti sutartį, susijusį projektą ir atsiskaitymo taisykles, pagal kurias apskaičiuojamos darbo, nustatyto projekte, biudžeto kategorijų sąskaitų sumos.

Sukūrę sutartį ir projektą, galite nustatyti projekto išsamią informaciją. Pavyzdžiui, galite apibrėžti veiklos rūšis ir priskirti projektui darbuotojus.

## <a name="example"></a>Pavyzdžiui

Jūsų organizacija yra programinės įrangos kūrimo įmonė. Jūs sutinkate sukurti klientui algalapių apskaitos paketą už bendrą 20 000 JAV dolerių (USD) mokestį. Jūsų organizacija sutinka klientui išrašyti sąskaitą faktūrą, kai baigsite tam tikrą projekto procentinę dalį. Galite nustatyti toliau nurodytas darbo projektų kategorijas, kad jas galėtumėte naudoti atsiskaitydami:

- Konsultavimas
- Dizainas
- Diegimas

Be to, nustatote atsiskaitymo taisykles, pagal kurias automatiškai apskaičiuojamos sąskaitos faktūros sumos už atlikto kiekvienos kategorijos projekto darbo procentinę dalį.

Biudžeto tvarkytuvas sukuria projektų kategorijų biudžetą. Atlikto darbo suma automatiškai apskaičiuojama kaip faktinio darbo procentinė dalis, palyginti su sąmatos sumomis.

## <a name="prerequisites"></a>Būtinosios sąlygos

Prieš kurdami projektą, kuris naudoja atsiskaitymo taisykles, turite nustatyti atsiskaitymo taisyklių numeraciją ir mokesčių žurnalą, naudojamą registruoti vykdomus atsiskaitymus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
2. Puslapyje **Projektų valdymo ir apskaitos parametrai**, skirtuke **Numeracijos**, nustatykite numeraciją, kurią norite naudoti, kai kuriamos atsiskaitymo taisyklės.
3. Eikite į **Projektų valdymas ir apskaita** \> **Žurnalai** \> **Mokestis**.
4. Puslapyje **Mokesčių žurnalas** pasirinkite **Naujas** ir įveskite žurnalo pavadinimą.

## <a name="create-a-contract-for-progress-billings"></a>Vykdomų atsiskaitymų sutarties kūrimas

Naudodami šią procedūrą sukurkite fiksuotos kainos projekto sutartį. Projekto sąskaitą faktūrą sukuriate, kai atliktas projekto darbas pasiekia nurodytą procentinę dalį.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projektų sutartys**.
2. Puslapyje **Projektų sutartys** pasirinkite **Naujas**.
3. Dialogo lange **Nauja projekto sutartis** nustatykite šiuos laukus:

    - **Pavadinimas**
    - **Finansavimo tipas**
    - **Finansavimo šaltinis**
    - **Pardavimo valiuta** – pagal numatytuosius nustatymus ši valiuta naudojama kliento sąskaitoms faktūroms, susijusioms su projekto sutartimi. Tačiau pardavimo valiutą galite pakeisti konkrečioje kliento sąskaitoje faktūroje.

4. Pasirinkite **Gerai**. Informacija nukopijuojama į puslapio **Projektų sutartys** antraštę.
5. Puslapyje **Projektų sutartys** įrašykite likusią reikiamą projekto informaciją.

## <a name="create-a-project-for-progress-billings"></a>Vykdomų atsiskaitymų projekto kūrimas

Atlikite šiuos veiksmus, kad sukurtumėte projektą ir bet kokius papildomus projektus, susijusius su projekto sutartimi.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.
2. Puslapyje **Visi projektai** pasirinkite **Naujas**.
3. Dialogo lange **Naujas projektas**, lauke **Projekto tipas**, pasirinkite **Laikas ir medžiaga**.
4. Pasirinkite projekto grupę. Projektų grupė apibrėžia grupei priskirtų projektų registravimo informaciją.
5. Pasirinkite **Kurti projektą**.
6. Sukūrę projektą nustatykite projekto etapą į **Vykdoma**.

## <a name="create-a-budget-for-a-project"></a>Projekto biudžeto kūrimas

Biudžeto kategorijos naudojamos norint automatiškai apskaičiuoti sąskaitos faktūros sumas už atlikto kiekvienos kategorijos darbo procentinę dalį. Norėdami sukurti numatytų išlaidų biudžeto kategorijas, atlikite šiuos veiksmus.

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Visi projektai**.
2. Puslapyje **Visi projektai** pasirinkite ir atidarykite norimą projektą.
3. Puslapio **Projektai** veiksmų srityje, skirtuko **Planas** grupėje **Biudžetas** pasirinkite **Projekto biudžetas**.
4. Puslapyje **Projekto biudžetas** įveskite kiekvienos projekto kategorijos numatomą savikainą.

## <a name="create-billing-rules-for-progress-billings"></a>Vykdomų atsiskaitymų taisyklių kūrimas

1. Eikite į **Projektų valdymas ir apskaita** \> **Projektai** \> **Projektų sutartys**.
2. Puslapyje **Projektų sutartys** pasirinkite ir atidarykite projekto sutartį.
3. Projekto sutarties puslapio „FastTab“ **Atsiskaitymo taisyklės** pasirinkite **Įtraukti**.
4. Puslapio **Atsiskaitymo taisyklė** lauke **Eilutės tipas** pasirinkite **Eiga**.
5. „FastTab“ **Atsiskaitymo taisyklės eilutės duomenys** lauke **Sutarties vertė** įveskite bendrą sutarties sumą.
6. Lauke **Kategorija** pasirinkite kategoriją, į kurią norite registruoti mokesčio operaciją.
7. Lauke **Projektas** pasirinkite projektą, kuris naudoja šią atsiskaitymo taisyklę.
8. Pasirinktinai: atsiskaitymo taisyklę priskirkite papildomiems projektams. „FastTab“ **Projektas** skyriuje **Esami projektai** pasirinkite projektą, tada pasirinkite dešiniosios rodyklės mygtuką norėdami įtraukti projektą į skyrių **Pasirinkti projektai**.
9. Pasirinktinai: apskaičiuokite procentinę sumą, kurią klientas atšaukia iš sąskaitos faktūros mokėjimų. „FastTab“ **Mokėjimo sulaikymo sąlygos** pasirinkite finansavimo šaltinį, tada lauke **Sulaikymo procentinė dalis** įveskite sulaikymo procentinę dalį.
10. Norėdami sukurti papildomas projekto sutarties atsiskaitymo taisykles, pakartokite šiuos veiksmus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]