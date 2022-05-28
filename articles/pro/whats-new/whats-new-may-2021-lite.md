---
title: Kas nauja – 2021 m. gegužės mėn. „Project Operations Lite“ visuotinis diegimas
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. gegužės mėn. „Project Operations Lite“ visuotinio diegimo versijoje.
author: sigitac
ms.date: 05/17/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 854a8c2290281b4d11a045321a334d8866806041
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8583686"
---
# <a name="whats-new-may-2021---project-operations-lite-deployment"></a>Kas nauja – 2021 m. gegužės mėn. „Project Operations Lite“ visuotinis diegimas

_Taikoma (kam): „Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros kūrimą_

Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

   - „Project Operations“ „Dataverse“ aplinkoje, 4.10.0.186 versija.

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- [Planavimo režimai](../../project-management/scheduling-modes.md): projektų vadovai dabar gali apibrėžti, ar projektą reikia valdyti naudojant fiksuotą trukmę, fiksuotą darbą ar fiksuotą vienetų planavimo režimą.

## <a name="quality-updates"></a>Kokybės naujinimai

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Sąskaitų siuntimas ir kainodara | 2224568 | Įtraukta logika, kad būtų galima įjungti tinkinimus, apimančius sąskaitos faktūros patvirtinimo priedo iškvietimą. |
| Sąskaitų siuntimas ir kainodara | 2101098 | Patobulinta numatytųjų laukų logika į proforma sąskaitą faktūrą. Šie laukai apima **Sąskaitų siuntimo adresas**, **Sąskaitos gavėjo vardas, pavardė** ir **Mokėjimo sąlygos**. Laukai dabar yra numatytieji iš atitinkamo projekto sutarties kliento įrašo. |
| Sąskaitų siuntimas ir kainodara | 2021413 | Atnaujinti laukai **Faktinė savikaina** ir **Pardavimas** objekte **Užduotis**, kad į užduotis būtų įtrauktos išlaidų, už kurias išrašyta ir neišrašyta sąskaita faktūra, pardavimo reikšmės. |
| Sąskaitų siuntimas ir kainodara | 2182110 | Kopijuojant projekto sutartį, sutarties eilutės ID yra iš naujo sugeneruojamas paskirties projekto sutartyje, kad būtų užtikrinta, jog jis bus unikalus. |
| Galimybės valdymas | 2186741 | Įtraukti patvirtinimai, siekiant užtikrinti, kad laukų **Kilmė** ir operacijos tipas nebus galima atnaujinti esamos pasiūlymo eilutės informacijos dalyje. |
| Galimybės valdymas | 2191353 | Etapų nebegalima kurti laiko ir medžiagos sutarties eilutėje. |
| Galimybės valdymas | 2216956 | Išspręstos problemos, susijusios su funkcija **Naujinti kainas**. |
| Planavimas ir stebėjimas | 2182979 | Patobulinta projekto kopijavimo funkcija, siekiant užtikrinti, kad išlaidų įvertinimo eilutės bus kopijuojamos iš pradinio projekto. |
| Planavimas ir stebėjimas | 2184144 | Patobulinta projekto kopijavimo funkcija, siekiant užtikrinti, kad išteklių padėties pavadinimas bus kopijuojamos iš pradinio projekto. |
| Planavimas ir stebėjimas | 2184799 | Sugriežtinta kontrolė, siekiant užtikrinti, kad kopijuojant projektą numatomos pradžios datos nebūtų galima pakeisti vykstant kopijavimui. |
| Planavimas ir stebėjimas | 2185134 | Kopijuojant projektą paskirties projekto numatoma pradžios data nustatoma į šiandienos datą. |
| Planavimas ir stebėjimas | 2196373 | Užtikrinama, kad projekto vadovo ir komandos nario įrašai projekto komandoje nėra dubliuojami kopijuojant projektą. |
| Planavimas ir stebėjimas | 2211833 | Išteklių priskyrimai kopijuojami iš šaltinio projekto užduoties į paskirties projektą. |
| Planavimas ir stebėjimas | 2186541 | Išspręstos problemos tinklelyje **Įvertinimai** grupuojant pagal **Ištekliai**. |
| Planavimas ir stebėjimas | 2166906 | Operacijos kategoriją iš užduoties reikia nukopijuoti į objektą **Išteklių priskyrimas**. |
| Išteklių valdymas | 2125362 | Išspręstos problemos kuriant bendrąjį komandos narį naudojant valandomis pagrįstą paskirstymo būdą. |
| Laikas ir išlaidos | 2113603 | Išspręsta su tinkinimu susijusi problema šalinant atributus puslapio **Laiko įvestis**. Dabar sistema patikrina, ar prieš pasiekiant puslapį naudojant scenarijų jame yra atributas. |
| Laikas ir išlaidos | 2204377 | Nukopijuoti grafikai turi būti rodomi automatiškai, pasirinkus **Kopijuoti savaitę**. |
| Laikas ir išlaidos | 2209059 | Galima redaguoti „Dynamics 365 Field Service“ laiko įrašų lauką **Būsena**. |
