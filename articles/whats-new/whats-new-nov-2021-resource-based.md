---
title: 2021 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės atnaujinimus, kuriuos galima rasti 2021 m. lapkričio mėn.
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

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projekto operacijos aplinkos versijoje Dataverse 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.22 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- Projekto planavimo programų programavimo sąsajos (API) dabar palaiko galimybę kurti ir naikinti "Project" kibirus.

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](/dynamics365/project-operations/environment/resource-dual-write-maps).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei naujausia žemėlapio versija nesuaktyvinta. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote lentelės struktūrą, iš naujo taikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis [dvigubo rašymo trikčių šalinimo vadovo skyriuje Trūksta lentelės stulpelių problema žemėlapių](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-in-dataverse"></a>Projekto operacijos Dataverse

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2240080 | Laukas **Mokėjimo sąlygos** negali būti dubliuojamas išankstinėje SF. |
| Sąskaitų pateikimas ir kainodara | 2358236 | SF taisymas turi leisti pataisymus, kurių eilutės yra nulinės kainos. |
| Išteklių valdymas | 2410072 | Leisti nustatyti išteklių, priskirtų užduočiai kaip projekto vadovui. |
| Sąskaitų pateikimas ir kainodara | 2430234 | Išspręskite išlaidų efektyvumo skaičiavimo problemą. |
| Laikas ir išlaidos | 2436978 | Leisti įvesti laiką hh:mm formatu. |
| Sąskaitų pateikimas ir kainodara | 2448623 | Leisti atnaujinti kainoraščius, susietus su organizaciniu vienetu. |
| Laikas ir išlaidos | 2460396 | Leisti panaikinti laiko įrašą išvalant langelį. |
| Sąskaitų pateikimas ir kainodara | 2467386 | Leisti panaikinti projektą su užduotimi, net jei užduotis susieta su laimėtu pasiūlymu. |
| Laikas ir išlaidos | 2461744 | Rodinyje **Mano nesėkmingas patvirtinimas** yra tik projekto patvirtinimai **etape Pateikta**. |
| Laikas ir išlaidos | 2464082 | Pašalinkite saitą iš projekto patvirtinimų į patvirtinimo rinkinį, kai sutampa paskirties būsena. |
| Laikas ir išlaidos | 2468108 | Užduotis Grafikas neturėtų nustatyti **patvirtinimo rinkinio apdorojimo** būsenos. |
| Laikas ir išlaidos | 2471503 | Panaikinkite septynių dienų senumo patvirtinimo rinkinius. |
| Sąskaitų pateikimas ir kainodara | 2480687 | Sukūrus pasiūlymo eilutės etapą, pasiūlymo eilutės nuorodos pašalinti negalima. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansų srityje

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Nepaskirstytos tiekėjo sumos projekto išlaidų operacijose nerodomos operacijų sąraše. |
| Projektų valdymas ir apskaita | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Įjungus tiekėjo SF, vidinės įmonės tiekėjo SF sulūžta. |
| Projektų valdymas ir apskaita | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Mokėjimo sąlygos projekto SF neveikia taip, kaip tikėtasi. |
| Projektų valdymas ir apskaita | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kai tiekėjo užlaikymas išleidžiamas, kvito registravime yra papildomų neteisingų eilučių. |
| Projektų valdymas ir apskaita | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Užregistravus projekto operacijų integravimo žurnalą, jis nepavyksta dėl trūkstamų sąskaitos, kurioje neregistruojama, dimensijų. |
| Projektų valdymas ir apskaita | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | Skirtuko **Projektas** negalima redaguoti laukiančioje tiekėjo SF, kai prekei priskiriama įsigijimo kategorija. |
| Projektų valdymas ir apskaita | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Trūksta naršymo srities, jei nesate prisijungę prie "Project Operations Dataverse". |
| Projektų valdymas ir apskaita | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kai registruojate pajamas iš projekto SF sugretintu užlaikantuvo atveju, iškyla problema, nes kvito operacijos nesubalansuojamos. |
| Projektų valdymas ir apskaita | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Įvertinimo sukūrimas užregistravus SF pasiūlymą blokuoja taisymo eilutes iš importavimo. |
| Projektų valdymas ir apskaita | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Neturėtų būti įmanoma modifikuoti visos sąskaitos faktūros etapo įrašo. |
| Kelionės ir išlaidos | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visos išlaidų ataskaitos yra matomos, kai ieškote kategorijos mobiliųjų įrenginių programėlėje Išlaidos. |
| Kelionės ir išlaidos | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Neteisingos tiekėjo operacijų ir PVM operacijų sumos registruojamos iš išlaidų, sukurtų iš kredito kortelės operacijos. |
| Kelionės ir išlaidos | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Neatnaujinus puslapį Išlaidų ataskaita **, atsiranda nereikšmingas įspėjimas**. |
| Kelionės ir išlaidos | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Neteisingas laikinasis tvirtintojas naudojamas, kai panaikinate laikinąjį tvirtintoją ir iš naujo pateikiate išlaidų ataskaitą naudodami darbo eigą. |
| Kelionės ir išlaidos | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Įvyksta registravimo klaida, susijusi su ridos nustatymu. |
