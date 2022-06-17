---
title: Kas nauja 2022 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kuriuos galima rasti "Microsoft" Dynamics 365 Project Operations 2022 m. balandžio mėn.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ea1c96d64309990962f431b1c72ae47bf445bfa
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912388"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projekto operacijos aplinkos versijoje Dataverse 4.41.0.45
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.26 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Įsigijimo kategorijas galima naudoti projekto pirkimo užsakymuose ir laukiančiose tiekėjo SF. Daugiau informacijos ieškokite [Use procurement categories with project purchase orders and waiting vendor invoices](configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šioje lentelėje rodomi dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į 2022 m. kovo mėn.

| Objekto schema | Atnaujinta versija | Komentarai |
| -------------- | ------------------- | ------------|
| Projekto operacijų integravimo projekto tiekėjo SF eilutės eksportavimo objektas msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Šis žemėlapis palaiko įsigijimo kategorijų naudojimą su pirkimo užsakymais ir laukiančiomis tiekėjo SF. |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei naujausia žemėlapio versija nesuaktyvinta. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote lentelės struktūrą, iš naujo taikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis [dvigubo rašymo trikčių šalinimo vadovo skyriuje Trūksta lentelės stulpelių problema žemėlapių](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| ------------ | ---------------- | -------------- |
| Laikas ir išlaidos | 2573900 | Šiuolaikinio **patvirtinimo** funkcija turi būti įjungta pagal numatytuosius nustatymus. |
| Sąskaitų siuntimas ir kainodara | 2603313 | Ištaisyta įrašo dublikato klaida, dėl kurios nebuvo galima įtraukti pasiūlymo ir sutarties eilučių, kuriose yra produktas. |
| Diegimas ir konfigūravimas | 2611368 | Klientai turi turėti galimybę įtraukti iki penkių pasirinktinių objektų į sprendimą naudodami šiuolaikinį programų dizaino įrankį. |
| Laikas ir išlaidos | 2628285 | Išspręsta problema, kuri turėjo įtakos galimybei nustatyti tinkamą išteklių kategoriją importuojant laiko įrašą. |
|  Galimybių valdymas| 2628815 | Atnaujinkite pasiūlymo eilutės išsamios informacijos aprašo simbolių limitą, kad jis atitiktų užduoties temos simbolių ribą, kad būtų galima importuoti užduotis, kurių tema ilgesnė nei 100 simbolių. |
| Laikas ir išlaidos| 2629547 | Projekto **patvirtinimų laukas Pateikta pagal** turi nurodyti įrašą pateikusį vartotoją. |
| Laikas ir išlaidos| 2629865 | Kopijuojant **projektus, užduočių laukas Kopijuoti kategoriją**. |
| Laikas ir išlaidos| 2636463 | Pritvirtino patvirtinimų filtrus šiuolaikinėse patvirtinimo formose. |
| Projektų planavimas ir sekimas | 2648300 | Išspręsta problema, neleidžianti keisti projekto savininko. |
| Sąskaitų siuntimas ir kainodara | 2563000 | Negalima leisti leistino neapmokėto pardavimo žurnalo eilučių, kai valiuta skiriasi nuo sutarties valiutos. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita Dynamics 365 Finance

Norėdami gauti informacijos apie klaidų taisymus, įtrauktus į šį naujinimą, prisijunkite prie Microsoft Dynamics "Lifecycle Services" (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
