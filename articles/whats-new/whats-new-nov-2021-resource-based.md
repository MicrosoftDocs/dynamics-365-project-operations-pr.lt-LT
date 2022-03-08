---
title: 2021 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. lapkričio mėn.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 20f277bc9b6f571c0144eaaa867bb97c0cf30ddb
ms.sourcegitcommit: 04ebe764afa22742b3fbf8f12af31e8eea93682e
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/23/2021
ms.locfileid: "7827336"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Ši tema taikoma šių komponentų ir versijų Microsoft Dynamics 365 Project Operations:

- Projekto operacijos Dataverse aplinkos versijoje 4.26.0.145, 4.26.0.148, arba 4.26.0.150
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkos versija 10.0.22

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- "Project Scheduling" taikomųjų programų programavimo sąsajos (API) dabar palaiko galimybę kurti ir naikinti projektų rinkinius.

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](/dynamics365/project-operations/environment/resource-dual-write-maps).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinate projekto operacijų Dataverse sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali veikti netinkamai, jei nesuaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote neįrašytą lentelės struktūrą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis [dvigubo rašymo trikčių diagnostikos vadovo skyriuje Trūkstami lentelės](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) stulpeliai žemėlapiuose.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-in-dataverse"></a>Projekto operacijos Dataverse

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2240080 | **Mokėjimo sąlygų lauko negalima** dubliuoti išankstinėje SF. |
| Sąskaitų pateikimas ir kainodara | 2358236 | SF taisymas turi leisti taisymus, kuriuose yra nulinės kainos eilutės. |
| Išteklių valdymas | 2410072 | Leisti nustatyti išteklių, priskirtą užduočiai kaip projekto vadovui. |
| Sąskaitų pateikimas ir kainodara | 2430234 | Išspręskite išlaidų efektyvumo skaičiavimo problemą. |
| Laikas ir išlaidos | 2436978 | Leiskite įvesti laiką hh:mm formatu. |
| Sąskaitų pateikimas ir kainodara | 2448623 | Leisti atnaujinti kainoraščius po to, kai jie susieti su organizacijos vienetu. |
| Laikas ir išlaidos | 2460396 | Leisti panaikinti laiko įrašą išvalant langelį. |
| Sąskaitų pateikimas ir kainodara | 2467386 | Leisti panaikinti projektą, kuriame yra užduotis, net jei užduotis susieta su laimėtu pasiūlymu. |
| Laikas ir išlaidos | 2461744 | **Mano nepavykusio patvirtinimo** rodinyje yra tik projekto patvirtinimai **pateiktame** etape. |
| Laikas ir išlaidos | 2464082 | Pašalinkite saitą iš projekto patvirtinimų į patvirtinimo rinkinį, kai paskirties būsena yra suderinta. |
| Laikas ir išlaidos | 2468108 | Planavimo užduotis neturėtų nustatyti **patvirtinimo rinkinio apdorojimo** būsenos. |
| Laikas ir išlaidos | 2471503 | Panaikinkite septynių dienų senumo patvirtinimo rinkinius. |
| Sąskaitų pateikimas ir kainodara | 2480687 | Pasiūlymo eilutės nuorodos negalima pašalinti, kai sukuriamas pasiūlymo eilutės etapas. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansuose

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Išsaugotos tiekėjo sumos projekto išlaidų operacijose nerodomos operacijų sąraše. |
| Projektų valdymas ir apskaita | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Vidinės įmonės tiekėjo SF sugedus tiekėjo SF integravimui. |
| Projektų valdymas ir apskaita | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projekto SF mokėjimo sąlygos neveikia taip, kaip tikėtasi. |
| Projektų valdymas ir apskaita | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kai tiekėjo užlaikymas pateikiamas, kvito registravime yra papildomų neteisingų eilučių. |
| Projektų valdymas ir apskaita | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Užregistravus projekto operacijų integravimo žurnalą, jis nepavyksta dėl trūkstamų sąskaitos, kurioje neregistruojama, dimensijų. |
| Projektų valdymas ir apskaita | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Skirtuko Projektas** negalima redaguoti laukiančioje tiekėjo SF, kai prekei priskiriama įsigijimo kategorija. |
| Projektų valdymas ir apskaita | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Naršymo srities nėra, jei nesate prisijungę prie projekto operacijų Dataverse. |
| Projektų valdymas ir apskaita | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kai registruojate įplaukas iš projekto SF sugretintu laikiklio atveju, problema kyla dėl to, kad kvito operacijos nesubalansuotos. |
| Projektų valdymas ir apskaita | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Įvertinimo kūrimas po to, kai užregistruosite SF pasiūlymą, blokuoja importavimo taisymo eilutes. |
| Projektų valdymas ir apskaita | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Visiškai išrašyto tarpinio įrašo modifikavimas neturėtų būti įmanomas. |
| Kelionės ir išlaidos | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visos išlaidų ataskaitos matomos, kai ieškote kategorijos programėlėje Išlaidos mobiliesiems. |
| Kelionės ir išlaidos | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Neteisingos tiekėjo operacijų ir PVM operacijų sumos registruojamos iš išlaidų, sukurtų iš kredito kortelės operacijos. |
| Kelionės ir išlaidos | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Neaktualus įspėjimas atsiranda, kai atnaujinate **puslapį Išlaidų** ataskaita. |
| Kelionės ir išlaidos | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Neteisingas tarpinis tvirtintojas naudojamas, kai panaikinate laikinąjį tvirtintojų ir iš naujo pateikiate išlaidų ataskaitą per darbo eigą. |
| Kelionės ir išlaidos | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Įvyksta registravimo klaida, susijusi su kilometražo nustatymu. |
