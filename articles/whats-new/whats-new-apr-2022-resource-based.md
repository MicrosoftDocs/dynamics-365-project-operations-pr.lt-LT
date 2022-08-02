---
title: Kas nauja 2022 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kurie pasiekiami "Microsoft" Dynamics 365 Project Operations 2022 m. balandžio mėnesio leidime, skirtuose ištekliais / ne atsargomis pagrįstiems scenarijams.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110894"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project" operacijos Dataverse aplinkos versijos 4.41.0.45
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.26 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Įsigijimo kategorijas galima naudoti projekto pirkimo užsakymuose ir laukiančiose tiekėjo SF. Daugiau informacijos ieškokite [Įsigijimo kategorijų naudojimas su projekto pirkimo užsakymais ir laukiančiomis tiekėjo SF](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šioje lentelėje pateikiami dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į 2022 m. kovo mėnesio "Project Operations" leidimą.

| Objekto schema | Atnaujinta versija | Komentarai |
| -------------- | ------------------- | ------------|
| "Project Operations" integravimo projekto tiekėjo SF eilutės eksportavimo objektas msdyn\_ projectvendorinvoicelines | 1.0.0.4 | Šis žemėlapis palaiko įsigijimo kategorijų naudojimą su pirkimo užsakymais ir laukiančiomis tiekėjo sąskaitomis faktūromis. |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visus susijusius lentelių žemėlapius, kai atnaujinate "Project Operations" Dataverse sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei nesuaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote paruoštą naudoti lentelės žemėlapį, iš naujo pritaikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis skyriuje Trūksta lentelės stulpelių žemėlapiuose, esančiame [dvigubo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) rašymo trikčių šalinimo vadovo skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| ------------ | ---------------- | -------------- |
| Laikas ir išlaidos | 2573900 | Šiuolaikinio **patvirtinimo** funkcija turi būti įjungta pagal numatytuosius nustatymus. |
| Sąskaitų siuntimas ir kainodara | 2603313 | Ištaisyta pasikartojančio įrašo klaida, kuri neleido įtraukti citatos ir sutarties eilučių, kuriose yra produktas. |
| Visuotinis diegimas ir konfigūravimas | 2611368 | Klientai turi turėti galimybę prie sprendimo pridėti iki penkių pasirinktinių objektų naudodami šiuolaikinį programų dizaino įrankį. |
| Laikas ir išlaidos | 2628285 | Išspręsta problema, kuri turėjo įtakos galimybei nustatyti tinkamą išteklių kategoriją importuojant laiko įrašą. |
|  Galimybių valdymas| 2628815 | Atnaujinkite citatos eilutės išsamios aprašo simbolių ribą, kad ji atitiktų užduoties temos simbolių ribą, kad būtų galima importuoti užduotis, kurių tema yra ilgesnė nei 100 simbolių. |
| Laikas ir išlaidos| 2629547 | Lauke **Pateikta pagal** projekto patvirtinimus turi būti nurodytas vartotojas, pateikęs įrašą. |
| Laikas ir išlaidos| 2629865 | Laukas **Kopijuoti kategoriją** apie užduotis, kai projektai kopijuojami. |
| Laikas ir išlaidos| 2636463 | Pataisė patvirtinimų filtrus šiuolaikinėse patvirtinimų formose. |
| Projektų planavimas ir sekimas | 2648300 | Išspręsta problema, dėl kurios projekto savininkas negali būti pakeistas. |
| Sąskaitų siuntimas ir kainodara | 2563000 | Žurnalo eilutės, skirtos nepirktiniam pardavimui, kai valiuta skiriasi nuo sutartinės valiutos, neturi būti leidžiamos. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita Dynamics 365 Finance

Norėdami gauti informacijos apie į šį naujinimą įtrauktus klaidų pataisymus, prisijunkite prie Microsoft Dynamics "Lifecycle Services" (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
