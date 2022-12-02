---
title: Kas nauja – 2021 m. balandžio mėn. „Project Operations Lite“ visuotinis diegimas
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. balandžio mėn. „Project Operations Lite“ visuotinio diegimo versijoje.
author: sigitac
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 987eeaf2e57659a6facae6b0a3688f15992e8bb9
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931249"
---
# <a name="whats-new-april-2021---project-operations-lite-deployment"></a>Kas nauja – 2021 m. balandžio mėn. „Project Operations Lite“ visuotinis diegimas

_Taikoma (kam): „Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros kūrimą_

Šis straipsnis taikomas toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

  - „Project Operations“, esanti „Dataverse“ aplinkoje, 4.9.0.221 versija 

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- Projektams skirtos nelaikomos medžiagos. Toliau pateiktos pagrindinės savybės.
  - Nelaikomų medžiagų įvertinimas ir įkainojimas projekto pardavimo ciklo metu. Norėdami gauti daugiau informacijos, žr. [Katalogo produktų savikainos ir pardavimo kainų sąranka – „Lite“ versija](../pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Nelaikomų medžiagų naudojimo sekimas projekto pristatymo metu. Norėdami gauti daugiau informacijos, žr. [Medžiagos naudojimo projektuose ir projekto užduotyse įrašymas](../../material/material-usage-log.md).
  - Sąskaitų faktūrų išrašymas už nelaikomų medžiagų savikainas. Norėdami gauti daugiau informacijos, žr. [Atsiskaitymo nebaigtų užduočių tvarkymas – „Lite“](../proforma-invoicing/manage-billing-backlog-sales.md#product-billing-backlog).
  - Naujos API programoje „Dynamics 365 Dataverse“ leidžia kurti, naujinti ir naikinti operacijas naudojant **grafiko objektus**. Norėdami gauti daugiau informacijos, žr. [Grafiko API naudojimas norint atlikti operacijas su grafiko objektais](../../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kokybės naujinimai

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Sąskaitų siuntimas ir kainodara | 2224568 | Įtraukta logika, kad būtų galima įjungti tinkinimus, apimančius sąskaitos faktūros patvirtinimo priedo iškvietimą. |
| Sąskaitų siuntimas ir kainodara | 2101098 | Patobulinta numatytųjų išankstinės sąskaitos faktūros laukų logika: **Sąskaitų siuntimo adresas**, **Sąskaitų gavėjo vardas** ir **Mokėjimo sąlygos** dabar nustatomos pagal numatytuosius atitinkamo projekto sutarties kliento įrašo parametrus. |
| Sąskaitų siuntimas ir kainodara | 2021413 | Atnaujinti laukai **Faktinė savikaina** ir **Pardavimas** objekte **Užduotis**, kad į užduotis būtų įtrauktos išlaidų, už kurias išrašyta ir neišrašyta sąskaita faktūra, pardavimo reikšmės. |
| Sąskaitų siuntimas ir kainodara | 2182110 | Kopijuojant projekto sutartį, sutarties eilutės ID yra iš naujo sugeneruojamas paskirties projekto sutartyje, kad būtų užtikrinta, jog jis bus unikalus. |
| Galimybės valdymas | 2186741 | Įtraukti patvirtinimai, siekiant užtikrinti, kad laukų **Kilmė** ir **Operacijos tipas** nebus galima atnaujinti esamos pasiūlymo eilutės informacijos dalyje. |
| Galimybės valdymas | 2191353 | Etapų nebegalima kurti laiko ir medžiagos sutarties eilutėje. |
| Galimybės valdymas | 2216956 | Išspręstos problemos, susijusios su funkcija **Naujinti kainas**. |
| Planavimas ir stebėjimas | 2182979 | Patobulinta projekto kopijavimo funkcija, siekiant užtikrinti, kad išlaidų įvertinimo eilutės bus kopijuojamos iš pradinio projekto. |
| Planavimas ir stebėjimas | 2184144 | Patobulinta projekto kopijavimo funkcija, siekiant užtikrinti, kad išteklių padėties pavadinimas bus kopijuojamos iš pradinio projekto. |
| Planavimas ir stebėjimas | 2184799 | Projekto kopija: sugriežtinta kontrolė, siekiant užtikrinti, kad numatomos pradžios datos nebūtų galima pakeisti vykstant kopijavimui. |
| Planavimas ir stebėjimas | 2185134 | Projekto kopija: paskirties projekto numatoma pradžios data nustatoma į šiandienos datą. |
| Planavimas ir stebėjimas | 2196373 | Projekto kopija: užtikrinama, kad projekto vadovo ir komandos nario įrašai projekto komandoje nėra dubliuojami. |
| Planavimas ir stebėjimas | 2211833 | Projekto kopija: išteklių priskyrimai kopijuojami iš šaltinio projekto užduoties į paskirties projektą. |
| Planavimas ir stebėjimas | 2186541 | Išspręstos problemos tinklelyje **Įvertinimai** grupuojant išteklius. |
| Planavimas ir stebėjimas | 2166906 | Operacijos kategoriją iš užduoties reikia nukopijuoti į objektą **Išteklių priskyrimas**. |
| Išteklių valdymas | 2125362 | Išspręstos problemos kuriant bendrąjį komandos narį naudojant valandomis pagrįstą paskirstymo būdą. |
| Laikas ir išlaidos | 2113603 | Išspręsta su tinkinimu susijusi problema šalinant atributus puslapio **Laiko įvestis**. Dabar sistema patikrina, ar prieš pasiekiant puslapį naudojant scenarijų jame yra atributas. |
| Laikas ir išlaidos | 2204377 | Nukopijuoti grafikai turi būti rodomi automatiškai, laiko įrašo metu pasirinkus **Kopijuoti savaitę**. |
| Laikas ir išlaidos | 2209059 | Galima redaguoti „Dynamics 365 Field Service“ laiko įrašų lauką **Būsena**. |
