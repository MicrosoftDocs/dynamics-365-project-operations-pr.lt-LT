---
title: 2021 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. lapkričio mėn.
author: sigitac
ms.date: 11/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fb9dad5b04ef2933ed8a8d8211f888f13df5ba40
ms.sourcegitcommit: 9d20e7738cce195d344f5925a115741a1ce3ca36
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/21/2021
ms.locfileid: "7942895"
---
# <a name="whats-new-november-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 m. lapkričio mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Ši tema taikoma toliau pateiktiems Microsoft komponentams ir versijoms Dynamics 365 Project Operations:

- Projekto operacijos Dataverse aplinkos versijoje 4.26.0.145, 4.26.0.148, 4.26.0.150, 4.26.0.155
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkos versijoje 10.0.22

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- Projektų planavimo programų programavimo sąsajos (API) dabar palaiko galimybę kurti ir naikinti projekto kibirus.

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](/dynamics365/project-operations/environment/resource-dual-write-maps).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas atnaujindami projekto operacijų Dataverse sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali tinkamai neveikti, jei nebus suaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote lentelės žemėlapį už lauko ribų, iš naujo pritaikykite keitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vykdykite [dviejų rašymo trikčių šalinimo vadovo skyriuje Žemėlapiai pateiktos lentelės stulpelių išdavimo trūkstamos lentelės](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) stulpelių instrukcijas.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-in-dataverse"></a>Projekto operacijos Dataverse

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2240080 | Lauko **Mokėjimo sąlygos negalima** dubliuoti išankstinėje SF. |
| Sąskaitų pateikimas ir kainodara | 2358236 | SF koregavimas turi leisti pataisymus, kurių eilutės yra nulinės kainos. |
| Išteklių valdymas | 2410072 | Leisti nustatyti išteklių, priskirtų užduočiai kaip projektų tvarkytuvas. |
| Sąskaitų pateikimas ir kainodara | 2430234 | Nustatyti išlaidų našumo skaičiavimo problemą. |
| Laikas ir išlaidos | 2436978 | Leisti įvesti laiką hh:mm formatu. |
| Sąskaitų pateikimas ir kainodara | 2448623 | Leisti atnaujinti kainoraščius po to, kai jie susieti su organizaciniu vienetu. |
| Laikas ir išlaidos | 2460396 | Leisti panaikinti laiko įrašą išvalant langelį. |
| Sąskaitų pateikimas ir kainodara | 2467386 | Leisti panaikinti projektą, kurio užduotis yra panaikinta, net jei užduotis susieta su laimėta citata. |
| Laikas ir išlaidos | 2461744 | **Rodinyje Mano nepavyko** patvirtinti, kuriame yra tik projekto patvirtinimai **pateiktame** etape. |
| Laikas ir išlaidos | 2464082 | Pašalinkite saitą iš projekto patvirtinimų į patvirtinimo rinkinį, kai tikslinė būsena yra suderinta. |
| Laikas ir išlaidos | 2468108 | Planavimo užduotis neturėtų nustatyti **patvirtinimo** rinkinio apdorojimo būsenos. |
| Laikas ir išlaidos | 2471503 | Naikinti septynių dienų senumo patvirtinimo rinkinius. |
| Sąskaitų pateikimas ir kainodara | 2480687 | Pasiūlymo eilutės nuorodos negalima pašalinti, kai sukuriama pasiūlymo eilutės etapas. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansuose

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [584732](https://fix.lcs.dynamics.com/Issue/Details/?bugId=584732) | Nepaskirstytos tiekėjo sumos projekto išlaidų operacijose nerodomos operacijų sąraše. |
| Projektų valdymas ir apskaita | [593068](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593068) | Įjungus tiekėjo SF integravimą, vidinės įmonės tiekėjo SF sugedo. |
| Projektų valdymas ir apskaita | [593382](https://fix.lcs.dynamics.com/Issue/Details/?bugId=593382) | Projekto SF mokėjimo sąlygos neveikia taip, kaip tikėtasi. |
| Projektų valdymas ir apskaita | [596263](https://fix.lcs.dynamics.com/Issue/Details/?bugId=596263) | Kai išleidžiamas tiekėjo užlaikymas, kvito registravime yra papildomų neteisingų eilučių. |
| Projektų valdymas ir apskaita | [598758](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598758) | Užregistravus projekto operacijų integravimo žurnalą, jis nepavyksta, nes trūksta sąskaitos, kurioje neregistruojama, dimensijų. |
| Projektų valdymas ir apskaita | [602650](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602650) | **Skirtuko Projektas** negalima redaguoti laukiančio tiekėjo SF, kai įsigijimo kategorija priskiriama prekei. |
| Projektų valdymas ir apskaita | [605121](https://fix.lcs.dynamics.com/Issue/Details/?bugId=605121) | Jei nesate prisijungę prie projekto operacijų, naršymo srities Dataverse trūksta. |
| Projektų valdymas ir apskaita | [602728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=602728) | Kai registruojate pajamas iš projekto SF taikomu išlaikymo atveju, kyla problema, nes kvito operacijos nesubalansuojamos. |
| Projektų valdymas ir apskaita | [603624](https://fix.lcs.dynamics.com/Issue/Details/?bugId=603624) | Įvertinimo sukūrimas užregistravus SF pasiūlymą blokuoja taisymo eilutes nuo importavimo. |
| Projektų valdymas ir apskaita | [606083](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606083) | Visiškai išrašyto orientyro įrašo, kuriam išrašyta SF, keisti neturėtų būti įmanoma. |
| Kelionės ir išlaidos | [575305](https://fix.lcs.dynamics.com/Issue/Details/?bugId=575305) | Visos išlaidų ataskaitos matomos, kai ieškote kategorijos mobiliojoje programėlėje Išlaidos. |
| Kelionės ir išlaidos | [583101](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583101) | Neteisingos tiekėjo operacijų ir PVM operacijų sumos registruojamos iš išlaidų, sukurtų iš kredito kortelės operacijos. |
| Kelionės ir išlaidos | [583760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=583760) | Neaktualus įspėjimas atsiranda atnaujinus **išlaidų ataskaitos** puslapį. |
| Kelionės ir išlaidos | [598656](https://fix.lcs.dynamics.com/Issue/Details/?bugId=598656) | Netinkamas tarpinis tvirtintojas naudojamas panaikinus tarpinį tvirtintoją ir iš naujo pateikiant išlaidų ataskaitą per darbo eigą. |
| Kelionės ir išlaidos | [612742](https://fix.lcs.dynamics.com/Issue/Details/?bugId=612742) | Įvyksta registravimo klaida, susijusi su ridos nustatymu. |
