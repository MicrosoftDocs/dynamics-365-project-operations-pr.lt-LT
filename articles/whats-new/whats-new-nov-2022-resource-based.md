---
title: 2022 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, pasiekiamus "Microsoft" Dynamics 365 Project Operations 2022 m. lapkričio mėnesio leidime, skirtame ištekliais / be atsargų pagrįstiems scenarijams.
author: ryansandness
ms.date: 12/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ryansandness
ms.openlocfilehash: 509e303aeb0567627590fd89c6888b59a414c6f1
ms.sourcegitcommit: 952fcefe33de192ad48f4108c3adbe658fd7b94f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831136"
---
# <a name="whats-new-november-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.58.0.119 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.30 versijoje

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2781818 | Raktas nerastas klaida nustatant numatytąją medžiagos naudojimo žurnalo kainą. |
| Sąskaitų pateikimas ir kainodara | 2922373 | Nepavyksta susieti citatos eilutės su projektu, kuris buvo uždarytas kaip prarasta citata. |
| Sąskaitų pateikimas ir kainodara | 2943206 | **Laukas Sutarties eilutė** projekto objekte turi būti neprivalomas. |
| Sąskaitų pateikimas ir kainodara | 2953182 | Patobulinkite klaidų pranešimą taisydami sąskaitas faktūras.|
| Sąskaitų pateikimas ir kainodara | 2959500 | Nepavyksta susieti pasiūlymo eilutės su projekto užduotimi, kuri jau susieta su prarastu pasiūlymu.|
| Sąskaitų pateikimas ir kainodara | 2959560 | "Šis klientas jau yra projekto sutartyje" pranešimas, gautas uždarant pasiūlymą kaip laimėtą tam tikrose vietovėse. |
| Sąskaitų pateikimas ir kainodara | 3031727 | Išteklių priskyrimai nepavyksta su klaida Būtinas laukas "msdyn_Company". |
| Sąskaitų pateikimas ir kainodara | 3036905 | Nuosavybės įmonė niekada nėra inicijuota "ProjectTeamMember". |
| Galimybės valdymas | 2763519 | Neapibrėžta nuorodos klaida EnsureProjectContractAllowsUpdates. |
| Galimybės valdymas | 2783798 | Importuojant projekto įvertinimus pasiūlymo eilutėje, trūksta išlaidų ir medžiagų įvertinimų užduočių aprašų.|
| Galimybės valdymas | 2988635 | Pagerinkite klaidos msg aprašą ištrindami Klientą citatoje. |
| Galimybės valdymas | 3001191 | Nepavyko sukurti pasiūlymo iš galimybės, kur atsiskaitymo būdas nurodytas kaip neapibrėžtas. |
| Naujinti | 3012324 | Projekto konvertavimas nepavyko projekte, kurio pavadinime buvo valdymo simboliai, pvz., Tab. || Projektų planavimas ir sekimas | 2790384 | "Pending OperationSet" skirtasis laikas yra per trumpas. |
| Projektų planavimas ir sekimas | 3044275 | Trūksta lokalizacijos: missingProjectSchedulerErrorMessage. |
| Projektų planavimas ir sekimas | 3044277 | "Project Recon" tinklelis neįkeliamas, kai planuoklis išjungtas.|
| Išteklių valdymas | 2943153 | Atnaujinkite skirtuką Sekimas, kad būtų rodomos dvi skaitmenys po kablelio dalyje Trukmė.|
| Subranga | 2932774 | Tiekėjo SF eilutė Skaityti tik neteisingai pateikiant klaidą. |
| Subranga | 2939556 | Tiekėjo SF antraštės būsena neturėtų būti nustatyta kaip Juodraštinis naikinimas tinkle, jei ji neaktyvi. |
| Laikas ir išlaidos | 2939998 | Naujos TESA versijos panaudojimas "ProjOps". |


### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita programoje „Finance”

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į šį naujinimą, prisijunkite prie „Microsoft Dynamics Lifecycle Services“ (LCS) ir rrodyti [KB straipsnis](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
