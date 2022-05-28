---
title: Kas nauja – 2021 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šioje temoje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2021 m. birželio mėn. „Project Operations“, skirtos išteklių / nelaikomų medžiagų scenarijams, leidime.
author: sigitac
ms.date: 06/14/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 21a446fdb9526c1a2b110c5368516dafb64b5e01
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600798"
---
# <a name="whats-new-june-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2021 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.11.0.156 arba 4.11.0.164 versijos „Dynamics 365“ „Dataverse“ aplinkoje.
- Projektų valdymas ir apskaita "Finance and Operations" programų aplinkose 10.0.19 versija.

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- Galimybė panaikinti [projektų SF pasiūlymų eilutes koregavimo scenarijams](../invoicing/correct-project-invoice-proposals.md).
- Detalizuotos išlaidų eilutės atspindi subkategorijų pavadinimus išlaidų ataskaitoje [Pertvarkytos išlaidų ataskaitos – naujos funkcijos](../expense/expense-reports-reimagined.md#new-features).
- Kuriant naujas išlaidas, mokėjimo būdas pasiekiamas naujoje išlaidų srityje.
- Projekto grafiko API bendras pasiekiamumas. Ši nauja funkcija leidžia klientams programiškai atlikti projekto užduočių, išteklių priskyrimų, užduočių priklausomybių ir projekto komandos narių įrašų kūrimo, naujinimo ir naikinimo operacijas. Daugiau informacijos žr. [Projekto grafiko API naudojimas operacijoms su planavimo objektais atlikti](../project-management/schedule-api-preview.md).

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. 

Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance and Operations" programų sprendimo versiją. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite matyti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Naują schemos versiją galite suaktyvinti pasirinkdami **Lentelių schemų versijos**, pasirinkdami naujausią versiją ir įrašydami pasirinktą versiją. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleisdami schemą susiduriate su problema, vykdykite nurodymus, pateikiamus vadovo Dvigubo rašymo trikčių šalinimas skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2281417 | Išspręsta problema, susijusi su automatinio SF kūrimo naudojant SF grafiką triktimi. |
| Sąskaitų pateikimas ir kainodara | 2287835 | Pagerintas SF patvirtinimo našumas. |
| Galimybės valdymas | 2222555 | Naudojant **Importuoti iš projekto sąmatos**, medžiagų sąmatų apmokestinimas turi būti tinkamai nukopijuotas į pasiūlymo eilutės duomenis. |
| Galimybės valdymas | 2223427 | Dabar leidžiami veiksmo **GenerateRetainersFromRetainerScheduleOptions** tinkinimai. |
| Galimybės valdymas | 2277528 | Pataisytas projekto sutarčių eilučių su keliais klientais atsiskaitymo etapų reikšmių skaičiavimas. |
| Projektų planavimas ir sekimas | 2226110 | Išspręsta pasikartojanti problema naudojant tinklelio **Projekto komanda** funkciją **Generuoti reikalavimą**. |
| Projektų planavimas ir sekimas | 2208109 | Vartotojai negali sukurti projekto viena valiuta, kai susijusios užduotys yra kita valiuta. |
| Projektų planavimas ir sekimas | 2258228 | Atnaujintas laukų, kuriuos leidžiama modifikuoti naudojant **planavimo** objektus ir grafiko API, sąrašas. |
| Projektų planavimas ir sekimas | 2293989 | Tinkama kalba ir regiono parametrai turi būti perduoti į tinklelį **Projekto užduotys**. |
| Išteklių valdymas | 2220493 | Pataisytos vartotojo funkcijos tinklelyje **Užduotis**, kai išteklių užklausa greitai pažymima kaip baigta. |
| Išteklių valdymas | 2330496 | Išspręsta **Grafiko lentos** įkėlimo problema. (Kokybinis naujinimas pasiekiamas naudojant 4.11.0.164 versiją) |
| Laikas ir išlaidos | 2194431 | Tinklelis **Laiko įrašas** turi atsižvelgti į savaitės pradžią, kaip nustatyta **sistemos parametruose**. |
| Laikas ir išlaidos | 2277311 | Panaikinus reikšmę tinklelio **Laiko įrašas** langelyje, žymiklis lieka tinklelyje. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektų valdymas ir apskaita pagal Dynamics 365 Finance

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [552976](https://fix.lcs.dynamics.com/Issue/Details/?bugId=552976) | **Formos pastabos** ir **Formos sąranka** nematomi „Finance“ juridinių segmentų, integruotų į „Project Operations“, dalyje **Projektų valdymo sąranka**. |
| Projektų valdymas ir apskaita | [527970](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527970) | Numatytasis PVM aprašas yra tuščias, kai projektų SF kvitų **registravimo tipas** = **PVM**. |
| Projektų valdymas ir apskaita | [565089](https://fix.lcs.dynamics.com/Issue/Details/?bugId=565089) | Kai į „Project Operations“ integruotoje „Dataverse“ naudojamas užduotimis pagrįstas atsiskaitymas, registruojamos dvigubos operacijos. |
| Projektų valdymas ir apskaita | [566869](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566869) | Naudojant „Project Operations“ integravimą, atliekant pajamų pripažinimą užbaigtumo procentas yra neteisingas. |
| Projektų valdymas ir apskaita | [568107](https://fix.lcs.dynamics.com/Issue/Details/?bugId=568107) | „Project Operations“ integruoto scenarijaus atveju laukiančioje tiekėjo SF įplaukų kaupimas yra dvigubas. |
| Projektų valdymas ir apskaita | [572370](https://fix.lcs.dynamics.com/Issue/Details/?bugId=572370) | Nepavyksta užregistruoti integravimo žurnalo, kai įplaukų profilio taisyklė nustatyta kaip sąranka **Grupė**. |
| Projektų valdymas ir apskaita | [573596](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573596) | Negalima registruoti projekto pirkimo užsakymų, kuriuose yra eilučių su keliais matavimo vienetais, pirkimo SF. |
| Projektų valdymas ir apskaita | [573637](https://fix.lcs.dynamics.com/Issue/Details/?bugId=573637) | Numatytosios projekto finansinės dimensijos negalima atnaujinti naudojant projekto duomenų objektą **V2**. |
| Projektų valdymas ir apskaita | [577211](https://fix.lcs.dynamics.com/Issue/Details/?bugId=577211) | Projekto sąmatų kūrimo paketinis procesas trunka per ilgai. |
| Projektų valdymas ir apskaita | [582329](https://fix.lcs.dynamics.com/Issue/Details/?bugId=582329) | Panaikinus sutartį taip pat panaikinamas su klientu susietas adresas. |
| Kelionės ir išlaidos | [514930](https://fix.lcs.dynamics.com/Issue/Details/?bugId=514930) | Išlaidų ataskaitos patvirtinimo darbo eigos sąlyga įvertinta neteisingai. |
| Kelionės ir išlaidos | [519304](https://fix.lcs.dynamics.com/Issue/Details/?bugId=519304) | Išlaidų ataskaitos strategija netinkamai įvertina projekto ID. |
| Kelionės ir išlaidos | [522463](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522463) | Funkcija **Įmonės vidaus išlaidų operacijas skaidyti į asmenines** veikia netinkamai. |
| Kelionės ir išlaidos | [534702](https://fix.lcs.dynamics.com/Issue/Details/?bugId=534702) | Panaikinus tam tikras kelionės paraiškas, išlaidų ataskaitos eilutės pagrindimai netyčia panaikinami. Taip nutinka, kai išlaidų ataskaitos ir kelionės paraiškos recID yra vienodi. |
| Kelionės ir išlaidos | [544368](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544368) | Mobiliojoje programėlėje Išlaidos kyla problema, kai išlaidų ataskaitos strategijose reikalingas laukas **Projekto ID**. |
| Kelionės ir išlaidos | [545331](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545331) | Įmonės vidaus išlaidų, susietų su projektu, redaguoti negalima. Vietoj to rodomas šis klaidos pranešimas „Objekto nuoroda nenustatyta objekto egzemplioriui.“ |
| Kelionės ir išlaidos | [548659](https://fix.lcs.dynamics.com/Issue/Details/?bugId=548659) | Užregistravus išlaidų ataskaitą, banko papildomoje knygoje nurodyta neteisinga valiuta ir suma. |
| Kelionės ir išlaidos | [558336](https://fix.lcs.dynamics.com/Issue/Details/?bugId=558336) | Patobulinta funkcija *Naikinti kredito kortelių operacijas*.  |
| Kelionės ir išlaidos | [525070](https://fix.lcs.dynamics.com/Issue/Details/?bugId=525070) | Į išlaidų ataskaitą įtrauktas PVM nėra vienodai skaičiuojamas, kai juridiniame subjekte nurodoma kita ataskaitų valiuta. |
| Kelionės ir išlaidos | [527779](https://fix.lcs.dynamics.com/Issue/Details/?bugId=527779) | Įtraukus naujas kelionės grynųjų pinigų išlaidas, pakinta našumas. |
| Kelionės ir išlaidos | [537841](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537841) | Išlaidų strategijos taisyklės nesuaktyvinamos išlaidų ataskaitoje. |
| Kelionės ir išlaidos | [566386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=566386) | Kai naudojant duomenų valdymo sistemą nusiunčiama nauja bendrinama kategorija, pašalinamos visos visų bendrinamų kategorijų subkategorijos. |
| Kelionės ir išlaidos | [574131](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574131) | Kai sukuriate išlaidų eilutę ir pasirenkate kokią nors kategoriją, rodomas šis klaidos pranešimas: „PVM grupės DOM ir prekių PVM grupės STD derinys netinkamas." |
| Kelionės ir išlaidos | [574900](https://fix.lcs.dynamics.com/Issue/Details/?bugId=574900) | Yra sinchronizavimo problemų mobiliojoje programoje Išlaidos. |
