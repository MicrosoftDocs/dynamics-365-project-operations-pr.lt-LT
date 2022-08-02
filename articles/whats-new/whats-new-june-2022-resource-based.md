---
title: Kas nauja – 2022 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kurie pasiekiami 2022 m. birželio mėnesio "Microsoft" Dynamics 365 Project Operations leidime, skirtuose išteklių / ne atsargų scenarijams.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031341"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2022 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project" operacijos Dataverse aplinkos versijoje 4.43.0.77 arba 4.43.0.119
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.27 versija

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šioje lentelėje pateikiami dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į "Project Operations June 2022" leidimą.

| Objekto schema | Atnaujinta versija | Komentarai |
| --- | --- | --- |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices) | 1.0.0.1 | Nebenaudojamas senstelėjęs laukas ir susietas su nauju tiekėjo SF būsenos sekimo lauku. |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visus susijusius lentelių žemėlapius, kai atnaujinate "Project Operations" Dataverse sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei nesuaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote paruoštą naudoti lentelės žemėlapį, iš naujo pritaikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis skyriuje Trūksta lentelės stulpelių žemėlapiuose, esančiame [dvigubo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) rašymo trikčių šalinimo vadovo skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Subrangos | 2708885 | Ištaisytas klaidos pranešimas, rodomas vartotojui sukūrus rezervuojamą išteklių rezervavimo antraštės įrašą, kuriame neužpildomas joks rezervuojamas išteklius. |
| Projektų planavimas ir sekimas | 2629441 | Ištaisė darbo eigos paleidimo logiką, kad būtų išvengta begalinio ciklo, kai atnaujinamos projekto užduotys. |
| Laikas ir išlaidos | 2641209 | Laiko įvedimo importavimas iš pavedimų / užsakymų turi išlaikyti rezervuojamą išteklių nuorodą. |
| Projektų planavimas ir sekimas | 2651148 | Projekto dokumento antraštė turi būti saugoma.|
| Projektų planavimas ir sekimas | 2653145 | Įtraukti tikrinimai, siekiant užtikrinti, kad nebūtų galima sukurti projekto įrašo, kurio pavadinime yra neleistinų simbolių. |
| Laikas ir išlaidos | 2654710 | Pataisė filtravimą **puslapyje Patvirtinimai**. |
| Sąskaitų siuntimas ir kainodara | 2667805 | Pridėta tikrinimo, kad būtų išvengta sąskaitų apmokėtų pardavimo faktinių duomenų kūrimo, jei nėra neįveiktų pardavimo faktų palaikymo. |
| Sąskaitų siuntimas ir kainodara | 2668378 | Pridėta tikrinimo, kad būtų išvengta tinkintos kainodaros dimensijos įtraukimo, nebent užpildomas loginis pavadinimas ir lauko pavadinimas. |
| Subrangos | 2677485 | Atnaujinta tiekėjo SF eilučių dvigubo rašymo žemėlapio tikslinė versija. |
| Laikas ir išlaidos | 2700428 | Patobulinta patvirtinimo logika, siekiant užtikrinti, kad kiti projekto patvirtinimo rinkiniai galėtų būti apdorojami, net jei vienas iš patvirtinimo rinkinių įstrigo sistemos užduotyse. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansų srityje

Norėdami gauti informacijos apie į šį naujinimą įtrauktus klaidų pataisymus, prisijunkite prie Microsoft Dynamics "Lifecycle Services" (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
