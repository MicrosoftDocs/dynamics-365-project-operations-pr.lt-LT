---
title: Kas nauja 2021 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. balandžio mėn. „Project Operations“, skirtoje ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams.
author: sigitac
manager: tfehr
ms.date: 04/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 359d39898ed60c7253b122cb884465fbd9605e0c
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868003"
---
# <a name="whats-new-april-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2021 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“, esanti „Dataverse“ aplinkoje, 4.9.0.221 versija
- Projektų valdymas ir apskaita „Dynamics 365 Finance” aplinkoje, 10.0.17 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- Projektams skirtos nelaikomos medžiagos. Toliau pateiktos pagrindinės savybės.
  - Nelaikomų medžiagų įvertinimas ir įkainojimas projekto pardavimo ciklo metu. Norėdami gauti daugiau informacijos, žr. [Katalogo produktų savikainos ir pardavimo kainų sąranka – „Lite“ versija](../pro/pricing-costing/set-up-cost-sales-rates-catalog-products.md).
  - Nelaikomų medžiagų naudojimo sekimas projekto pristatymo metu. Norėdami gauti daugiau informacijos, žr. [Medžiagos naudojimo projektuose ir projekto užduotyse įrašymas](../material/material-usage-log.md).
  - Sąskaitų faktūrų išrašymas už nelaikomų medžiagų savikainas. Norėdami gauti daugiau informacijos, žr. [Atsiskaitymo nebaigtų užduočių tvarkymas](../proforma-invoicing/manage-billing-backlog.md).
- Užduotimi pagrįstas atsiskaitymas: įtraukta galimybė susieti projekto užduotis su projekto sutarties eilutėmis ir taip pritaikyti jas pagal tą patį atsiskaitymo būdą, sąskaitų faktūrų išrašymo dažnumą ir klientus, kurie nurodyti sutarties eilutėje. Šis susiejimas užtikrina tikslų sąskaitų faktūrų išrašymą, apskaitą, pajamų įvertinimą ir pripažinimą dirbti pagal šią projekto užduočių sąranką.
- Naujos API programoje „Dynamics 365 Dataverse“ leidžia kurti, naujinti ir naikinti operacijas naudojant **grafiko objektus**. Norėdami gauti daugiau informacijos, žr. [Grafiko API naudojimas norint atlikti operacijas su grafiko objektais](../project-management/schedule-api-preview.md).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-in-dynamics-365-dataverse"></a>„Dynamics 365 Dataverse“ pateikiama „Project Operations“

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Sąskaitų siuntimas ir kainodara | 2124532 | Mygtukas **Taisyti sąskaitą faktūrą** išankstinėje sąskaitoje faktūroje rodomas, kai išankstinio apmokėjimo suma arba taikoma išankstinio apmokėjimo suma pateikiama pradinėje sąskaitoje faktūroje. Mygtukas rodomas tik tose aplinkose, kurių „Finance“ versija yra 10.0.19 arba naujesnė. |
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

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita programoje „Dynamics 365 Finance”

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [491941](https://fix.lcs.dynamics.com/Issue/Details/?bugId=491941) | Dalyje **Periodinis** neveikia įvertinimo atšaukimo pašalinimas.  |
| Projektų valdymas ir apskaita | [509773](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509773) | Naudojant funkciją **Apskaitos koregavimas** kyla problema dėl didžiosios knygos sąskaitų, kuriose pasirinkta **Neleisti įvesti neautomatiniu būdu**. |
| Projektų valdymas ir apskaita | [510728](https://fix.lcs.dynamics.com/Issue/Details/?bugId=5109728) | Įtraukta verslo logika, kad būtų apdorojamos taisytos sąskaitos faktūros, įskaitant išankstinio apmokėjimo sumą arba pritaikytą išankstinio apmokėjimo sumą. |
| Projektų valdymas ir apskaita | [514364](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514364) | NG pardavimų reikšmę registruojant vidinės įmonės projekto SF, pasirenkamas netikėtas klientas. |
| Projektų valdymas ir apskaita | [521807](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521807) | Dirbant su „Project Operations“ įrašais ir pakeitus numatytąjį projektą sutartyje po to, kai išrašomos sąskaitos faktūros už išankstinius mokėjimus, kyla problemų dėl gaunamų atskaitymų. |
| Projektų valdymas ir apskaita | [527319](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527319) | Jei reikia, „Project Operations“ iš sutarties pašalinus projektą, sutarties numatytasis projektas turėtų būti nustatytas iš naujo. |
| Projektų valdymas ir apskaita | [528212](https://fix.lcs.dynamics.com/Issue/Details/?bugId=528212) | „Project Operations“ vidinės įmonės sąskaitos faktūros sąraše **Įtraukti eilutę** rodomos neteisingos išlaidų eilutės. |
| Projektų valdymas ir apskaita | [543968](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543968) | „Project Operations“ puslapis **Pirkimo sutartis** nerodomas „Finance“ juridinių objektų, integruotų su „Project Operations“, dalyje. |
| Projektų valdymas ir apskaita | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | Dėl „Dataverse“ integravimo klaidos negalite konvertuoti pasiūlymo į laimėtą naudojant „Project Operations“. |
| Projektų valdymas ir apskaita | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | Naudojant **ProjCDSProjectContractEntity** galima nustatyti finansavimo šaltinio sąskaitos faktūros adresą kitam klientui.  |
| Projektų valdymas ir apskaita | [557376](https://fix.lcs.dynamics.com/Issue/Details/?bugId=557376) | Kuriant operacijos paskelbimo sąskaitą faktūrą, „Project Operations“ nepasirenkama jokių dimensijų. |
| Kelionės ir išlaidos | [441256](https://fix.lcs.dynamics.com/Issue/Details/?bugId=441256) | Avansinio mokėjimo likutis neatnaujinamas išlaidų ataskaitoje, jei yra patvirtintas ir paskelbtas kiekvienoje eilutėje. |
| Kelionės ir išlaidos | [482041](https://fix.lcs.dynamics.com/Issue/Details/?bugId=482041) | Netinkamai skaičiuojami mokesčiai, taikomi išvardytų vidinės įmonės išlaidų ataskaitose. |
| Kelionės ir išlaidos | [483469](https://fix.lcs.dynamics.com/Issue/Details/?bugId=483469) | Su projektais susiję papildomi laukai rodomi pertvarkytame puslapyje **Vidinės įmonės išlaidų ataskaitos**. |
| Kelionės ir išlaidos | [486592](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486592) | Išlaidų ataskaitų kvitų antraštėse rodomas neteisingas klaidos pranešimas. |
| Kelionės ir išlaidos | [487971](https://fix.lcs.dynamics.com/Issue/Details/?bugId=487971) | Jei pardavimo mokestis paskelbiamas paskirties vietos juridiniame subjekte, netinkamai paskelbiama išlaidų ataskaita vidinės įmonės scenarijuje. |
| Kelionės ir išlaidos | [505696](https://fix.lcs.dynamics.com/Issue/Details/?bugId=505696) | Patvirtintose išlaidų ataskaitose nespausdinamos ataskaitos pateikimo datos. |
| Kelionės ir išlaidos | [508726](https://fix.lcs.dynamics.com/Issue/Details/?bugId=508726) | Patvirtinus išlaidas, neužpildomi laukai **Patvirtinimo data** ir **Atmetimo data**. |
| Kelionės ir išlaidos | [509913](https://fix.lcs.dynamics.com/Issue/Details/?bugId=509913) | Vienam darbuotojui sukurtą kelionės paraišką galima naudoti kito darbuotojo išlaidų ataskaitai. |
| Kelionės ir išlaidos | [518186](https://fix.lcs.dynamics.com/Issue/Details/?bugId=518186) | Įtraukiant naują išlaidų eilutę, užrakinamos išlaidų kategorijos. |
| Kelionės ir išlaidos | [520914](https://fix.lcs.dynamics.com/Issue/Details/?bugId=520914) | Išvardinant jau padalytas išlaidų ataskaitos eilutes nevisiškai paskelbiamas mokėtinos sumos \ didžiosios knygos kvitas ir nustoja veikti apskaitos šaltinio naršyklė, nes sukuriamas **TRVEXPTRANS.SOURCEDOCUMENTLINE** dublikatas. |
| Kelionės ir išlaidos | [521943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=521943) | Kelionės paraiškos strategija taikoma ne taip, kaip tikėtasi. |
| Kelionės ir išlaidos | [522567](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522567) | Paskelbtose išlaidų ataskaitų projekto operacijose nerodomas tiekėjo sąskaitos pavadinimas. |
| Kelionės ir išlaidos | [525106](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525106) | Naudojantis „Project Operations“ negalima patvirtinti laiko, skirto vidinės įmonės projektui. |
| Kelionės ir išlaidos | [526336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=526336) | Paskelbus avansinio mokėjimo grąžinimo kategorijoje neatnaujinami avansiniai likučiai. |
| Kelionės ir išlaidos | [527218](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527218) | Neteisingai skaičiuojama pardavimo kaina išlaidų ataskaitose, sukurtose užsienio valiuta naudojant importuotas kredito kortelių operacijas, ir susietose su projektu. |
| Kelionės ir išlaidos | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Atšaukti duomenų įrašo **TrvRequisitionLine** keitimai ir susieta unikali rodyklė. |
| Kelionės ir išlaidos | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Į **SOURCESAUMELINE** generavimą įtrauktas naudojimasis prietaisais. |
| Kelionės ir išlaidos | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Jei pardavimo mokestis paskelbiamas paskirties vietos juridiniame subjekte, vidinės įmonės scenarijuje rodomas neteisingas papildomos DK žurnalas. |
| Kelionės ir išlaidos | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | „Project Operations“ panaikinus išlaidų įvertinimus iš „Dataverse“, jie nepanaikinami iš „Finance“. |
| Kelionės ir išlaidos | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kai išlaidų kategorija yra ne projekto kategorija, puslapyje **Išlaidos** pasirinktos finansinės dimensijos nekopijuojamos į išlaidų ataskaitą. |
