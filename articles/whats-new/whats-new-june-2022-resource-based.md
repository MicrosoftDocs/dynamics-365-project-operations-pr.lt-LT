---
title: Kas nauja – 2022 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kuriuos galima rasti 2022 Dynamics 365 Project Operations m. birželio mėn.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fde1f0be42eecfc5ee809cb9b2191d3aeae57131
ms.sourcegitcommit: 51745acac29dfacba43a4003d86baff4d6ca2fb8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/14/2022
ms.locfileid: "8959681"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2022 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projekto operacijos aplinkos versijoje Dataverse 4.43.0.77
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.27 versija

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktoje lentelėje rodomi dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į "Project Operations" 2022 m. birželio mėn.

| Objekto schema | Atnaujinta versija | Komentarai |
| --- | --- | --- |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices) | 1.0.0.1 | Nebenaudojamas senstelėjęs laukas ir susietas su nauju tiekėjo SF būsenos stebėjimo lauku. |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei naujausia žemėlapio versija nesuaktyvinta. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote lentelės struktūrą, iš naujo taikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis [dvigubo rašymo trikčių šalinimo vadovo skyriuje Trūksta lentelės stulpelių problema žemėlapių](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Subrangos | 2708885 | Ištaisytas klaidos pranešimas, rodomas vartotojui sukūrus užskaitomo išteklių rezervavimo antraštės įrašą, kuriame neužpildoma jokių užskaitomų išteklių. |
| Projektų planavimas ir sekimas | 2629441 | Pataisė darbo eigos suaktyvinimo logiką, kad būtų išvengta begalinio ciklo, kai atnaujinamos projekto užduotys. |
| Laikas ir išlaidos | 2641209 | Laiko įrašo importavimas iš priskyrimų / užsakymų turi išlaikyti rezervuotą išteklių nuorodą. |
| Projektų planavimas ir sekimas | 2651148 | Projekto dokumento antraštė turi būti saugoma.|
| Projektų planavimas ir sekimas | 2653145 | Pridėtas tikrinimas, siekiant užtikrinti, kad negalima sukurti projekto įrašo, kurio pavadinime yra neleistinų simbolių. |
| Laikas ir išlaidos | 2654710 | Pataisė filtravimą **puslapyje Patvirtinimai**. |
| Sąskaitų siuntimas ir kainodara | 2667805 | Pridėti patvirtinimai, padedantys užkirsti kelią pardavimo faktams, už kuriuos išrašyta sąskaita, kurti, jei nėra nepagrindinių pardavimo faktinių įrodymų palaikymo. |
| Sąskaitų siuntimas ir kainodara | 2668378 | Įtraukti patvirtinimai, padedantys išvengti pasirinktinės kainodaros dimensijos įtraukimo, nebent būtų užpildytas loginis pavadinimas ir lauko pavadinimas. |
| Subrangos | 2677485 | Atnaujinta tiekėjo SF eilučių dvigubo rašymo schemos paskirties versija. |
| Laikas ir išlaidos | 2700428 | Patobulinta patvirtinimų logika, siekiant užtikrinti, kad kiti projekto patvirtinimo rinkiniai galėtų būti apdorojami, net jei vienas iš patvirtinimo rinkinių yra įstrigęs sistemos užduotyse. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansų srityje

Norėdami gauti informacijos apie klaidų taisymus, įtrauktus į šį naujinimą, prisijunkite prie Microsoft Dynamics "Lifecycle Services" (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
