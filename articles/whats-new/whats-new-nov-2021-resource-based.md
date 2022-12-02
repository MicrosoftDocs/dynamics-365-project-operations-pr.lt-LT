---
title: 2021 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. lapkričio mėn. „Project Operations Lite”, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d5b58965f728321cc30d4e476b0dacf621fdec71
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932904"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ „Dataverse“ aplinkos versija 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.22 versijoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- Projektų planavimo programų programavimo sąsajos (API) dabar palaiko galimybę kurti ir naikinti projektų programavimo sąsajas.

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](/dynamics365/project-operations/environment/resource-dual-write-maps).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-in-dataverse"></a>„Project Operations“ „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2240080 | Mokėjimo **terminų lauko** negalima dubliuoti pro forma sąskaitoje faktūroje. |
| Sąskaitų pateikimas ir kainodara | 2358236 | Sąskaitos faktūros taisyme turi būti leidžiama atlikti pataisymus, kurių eilutės nulinės kainos. |
| Išteklių valdymas | 2410072 | Rodomi projekto užduočiai priskirto ištekliaus naudojimo vienetai |
| Sąskaitų pateikimas ir kainodara | 2430234 | Išlaidų efektyvumo skaičiavimo problemos sprendimas. |
| Laikas ir išlaidos | 2436978 | Leisti laiką įvesti hh:mm formatu. |
| Sąskaitų pateikimas ir kainodara | 2448623 | Leisti kainoraščius atnaujinti juos susietus su organizacijos vienetu. |
| Laikas ir išlaidos | 2460396 | Vartotojai negali panaikinti laiko įrašo išvalydami langelį. |
| Sąskaitų pateikimas ir kainodara | 2467386 | Leisti naikinti projektą, kuriame yra užduotis, net kai užduotis yra susieta su laimėta užklausa. |
| Laikas ir išlaidos | 2461744 | Rodinyje **Mano nepavykęs patvirtinimas** yra tik tie projekto patvirtinimai, kurių būsena **Pateikta**. |
| Laikas ir išlaidos | 2464082 | Pašalinsite saitą iš projekto patvirtinimų į patvirtinimo rinkinį, kai bus gretinta paskirties būsena. |
| Laikas ir išlaidos | 2468108 | Planavimo užduotis neturėtų nustatyti patvirtinimo **rinkinio** apdorojimo būsenos. |
| Laikas ir išlaidos | 2471503 | Panaikinkite patvirtinimo rinkinius, kurie yra septynių dienų senumo. |
| Sąskaitų pateikimas ir kainodara | 2480687 | Pasiūlymo eilutės nuorodos negalima pašalinti sukūrus pasiūlymo eilutės etapą. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita programoje „Finance”

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Projektų išlaidų operacijose išsaugotos tiekėjo sumos transakcijose nerodomas. |
| Projektų valdymas ir apskaita | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Įjungtą tiekėjo sąskaitų faktūrų integravimą, tarpusavio tiekėjo sąskaita faktūra bus sugadinta. |
| Projektų valdymas ir apskaita | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projekto sąskaitų faktūrų apmokėjimo sąlygos neveikia taip, kaip tikėjotės. |
| Projektų valdymas ir apskaita | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kai tiekėjo saugojimas išleidžiamas, perstabdymas turi neteisingų papildomų eilučių. |
| Projektų valdymas ir apskaita | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Kai "Project Operations" integravimo žurnalas užregistruojamas, jis nevykdomas, nes nėra kliento, kuriame neįregistruotas, suseka. |
| Projektų valdymas ir apskaita | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Projekto** skirtukas yra neredaguojamas laukiamoje tiekėjo sąskaitoje, kai tiekimo kategorija yra priskirta elementui. |
| Projektų valdymas ir apskaita | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Jei nesate prisijungę prie „Project Operations", naršymo srities nėra Dataverse. |
| Projektų valdymas ir apskaita | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kai publikuojate apyvartą iš projekto sąskaitos taikomu valdymo atveju, nutinka problema, nes perlaidos kvite nesutampa. |
| Projektų valdymas ir apskaita | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Sukūrus sąmatą, kai užregistruojate sąskaitos faktūros siūlymą, blokuojamos pataisų eilutės nuo importavimo. |
| Projektų valdymas ir apskaita | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Negalima modifikuoti visiškai išrašytos sf etapo įrašo. |
| Kelionės ir išlaidos | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visos išlaidų ataskaitos matomos, kai ieškote kategorijos mobiliųjų išlaidų programoje. |
| Kelionės ir išlaidos | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Neteisingos sumos, nurodytos tiekėjo ir PVM operacijose, kurios užregistruotos iš išlaidų, sukurtų naudojant kredito kortelės operaciją. |
| Kelionės ir išlaidos | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Įspėjimas dėl išlaidų ataskaitos atnaujinimo **įvyksta**. |
| Kelionės ir išlaidos | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Netinkamas tarpinis tvirtinantysis naudojamas, kai panaikinate tarpinį tvirtintinį ir iš naujo pateikiate išlaidų ataskaitą naudodami darbo eigą. |
| Kelionės ir išlaidos | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Yra registravimo klaida, susijusi su kilometražo sąranka. |
