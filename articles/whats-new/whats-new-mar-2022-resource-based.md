---
title: 2022 m. kovo mėn. naujienos – „Project Operations“, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacijos apie kokybinius naujinimus, pasiekiamus 2022 m. kovo mėn. „Project Operations”, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, leidime.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910916"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 m. kovo mėn. naujienos – „Project Operations“, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.30.0.99 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.25 versijoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Kiekvienam ciema dabar palaikoma naujoje ir naujai atvaizduojame modernioje išlaidų darbo srityje. Įmonės, kurios naudoja per diems, gali įjungti šią funkciją, kad vartotojai galėtų lengvai pateikti ir sustingti pagal savo išlaidas. Daugiau informacijos ieškokite [Per diem išlaidos](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktame sąraše parodytos dvigubo rašymo schemos, modifikuotos arba įtrauktos „Project Operations“ 2022 m. kovo mėn. leidime.

| **Objekto schema** | **Atnaujinta versija** | **Komentarai** |
| --- | --- | --- |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn\_projectvendorinvoicelines) | 1.0.0.3 | Susiejimai atnaujinti, kad atitiktų tiekėjo sąskaitos faktūros eilutės objektą Dataverse. <br>Neaktyvinti susiejimo versijos 1.0.0.4. Ją bus galima naudoti kartu su "Finance Environment" 10.0.26 versija kito mėnesio naujinime. |

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Laikas ir išlaidos | 2388011 | Masinio patvirtinimo metu rodyti komentarus apie laiko įvedimo komentarus. |
| Projektų planavimas ir sekimas | 2495294 | Projekto išsamios informacijos puslapyje Užduoties išsamių duomenų **negalima redaguoti**. |
| Sąskaitų siuntimas ir kainodara | 2499605 | Sutarties etapai, sukurti naudojant pasiūlymo etapus, neteisingai pažymimi kaip tik skaitomi. |
| Projektų planavimas ir sekimas | 2506050 | Jei jokių pakeitimų įrašyti, operacijos rinkinys lieka laukiamas vieną valandą. Tada rinkinys klaidingai pažymimas kaip **nepavykęs**, o jį reikia užpildyti nedelsiant. |
| Sąskaitų siuntimas ir kainodara | 2507401 | Dėl netinkamos talpyklos projektai neteisingai įvedami numatytieji perkantieji vienetai. |
| Sąskaitų siuntimas ir kainodara | 2541660 | **Pardavimo užsakymo kūrimo tikrinimas** naudojant indų rašymo procesą turėtų būti skirtas tik projektais pagrįsties užsakymams. |
| Sąskaitų siuntimas ir kainodara | 2552745 | Mokesčius neskaidyti klientai, kurie nustatė split atsiskaitymo taisykles. |
| Sąskaitų siuntimas ir kainodara | 2558859 | Patobulinti klaidų pranešimai, kai nustatomi kainodaros aspektai. |
| Sąskaitų siuntimas ir kainodara | 2558933 | **Importuoti iš projektų sąmatų** nepavyksta, kai **msdyn\_projektas įtraukiamas** kaip kainodaros susiejimumas. |
| Sąskaitų siuntimas ir kainodara | 2559101 | Projekto parametrų naikinimas neužblokuojamas ir kyla problemų. |
|  Galimybių valdymas | 2570390 | "Dvigubas" rašymo priedas prijungė kliento tipą pasiūlymuose, **užsakymuose** ir galimybėse būti klientu net jei to tipo klientas yra neteisingas. |
| Sąskaitų siuntimas ir kainodara | 2586097 | Iš projekto sutarties eilutės paėmus projektą, sąskaitose išrašytų išlaidų faktiniai rezultatai nepavirinami. |
| Sąskaitų siuntimas ir kainodara | 2589619 | Įrašomosios medžiagos mokestis platinamas iki nepažymėtų pardavimo faktinių duomenų ir sąskaitos faktūros. |
|  Galimybių valdymas | 2594015 | Klientams, kurie turi Net60 mokėjimo terminus, pasiūlymo **uždaryti** negalima. |
| Projektų planavimas ir sekimas | 2595841 | "Project for the Web" vartotojai **kurdami naują išteklių užklausą, gauna klaidos pranešimą apie trūkstamą msdyn\_actualstart**. |
| Laikas ir išlaidos | 2602511 | Laiko **įrašų lauke Atmesti** įrašai rodo **sistemą**, o ne pavadintą vartotoją kaip atmetėją. |
| Laikas ir išlaidos | 2602528 | Projekto patvirtinimas gali patvirtinti laiką tuose projektus, kuriuose jie nėra patvirtinti. |
| Sąskaitų siuntimas ir kainodara | 2608550 | Taisymo sąskaitą faktūrą galima patvirtinti net jei originalo pakeitimų nėra. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektų valdymas ir apskaita „Dynamics 365 Finance” programos aplinkose

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Galimame "Finance and Project Operations" lauke Kategorijos **ID** esantis neatitikimas. |
| Projektų valdymas ir apskaita | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Fiksuotos kainos projektai negali būti sustabdomi **kai laukas Kliento** faktūrų išrašymas nustatomas kaip **Išsamūs ir prarasti** duomenys ir naudojamas principu **Baigta procentinė dalis**. |
| Projektų valdymas ir apskaita | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Iš projekto nustatymo išlaidų eilutėse, kurios yra „Project Operations" integravimo procese, įvedama netinkama numatytoji PARDAVIMO mokesčių grupė. |
| Projektų valdymas ir apskaita | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Naudodami integruotą visuotinį diegimą su „Project Operations", negalite redaguoti projekto sąskaitos faktūros nesąrangos antraštės. |
| Projektų valdymas ir apskaita | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Tarpusavyje susieuotų tiekėjo sąskaitų faktūrų negalima integruoti su „Dataverse“. |
| Projektų valdymas ir apskaita | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Kliento balanso valiuta ir ataskaitų valiuta nesutampa. |
| Projektų valdymas ir apskaita | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Projekto sąskaitą faktūrą galite užregistruoti net jei klientas yra sulaikytas visose sąskaitose faktūrose. |
| Projektų valdymas ir apskaita | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | Projekto sąskaitos **faktūros, kurios** turi rodinius Antraštė ir **Eilutės** **nėra mygtuko Naikinti** visas eilutes. |
| Projektų valdymas ir apskaita | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Kai užregistruojate tiekėjo sąskaitą faktūrą, įvyksta tokia klaida: "Sąskaitos faktūros apskaitos data turi būti tais pačiais ataskaitiniais metais, kaip ir susijęs įsigytas užsakymas. Vykdykite pirkimo užsakymo metų pabaigos procesą arba pakeiskite datą į dabartinius ataskaitinius metus." |
| Kelionės ir išlaidos | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Uždarius kelionės paraišką su priskirtais kaštais, projekto priskirti kaštai išleidžiami. |
| Kelionės ir išlaidos | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Kai pateikiate išlaidų ataskaitos dėtuvės sekimo ataskaitą, įvyksta ši klaida: „Atsargų sekimas. Įmonė neegzistuoja.“ |
| Kelionės ir išlaidos | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Kai projektui **pažymėtas** parametro "Reikalavimo naudoti su "indais" parametras, **išlaidų ataskaitose neį įvestas numatytasis projekto ID**. |
| Kelionės ir išlaidos | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Mygtukas **Skelbti išlaidas** tinkamai neveikia „Project Operations for resource" / "Non-stocked" scenarijuose. |
| Kelionės ir išlaidos | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Kyla problema dėl išlaidų ataskaitos **išlaidų koeficiento pagal ašį**, į kurią įtraukta ir suslėgėtų išlaidų. |
| Kelionės ir išlaidos | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Darbuotojų išlaidų hierarchijos koeficientų **suma nėra tinkamai sumuota, kai "Du skirtingi" tipai naudojami "Du skirtingi" "Tiers** ", kurios išlaidų ataskaitoje naudojamos "Du skirtingi" tipo "Kait." |
| Kelionės ir išlaidos | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Projekto lauko, esančio kelioninių **susegimo** eilutėje, peržvalga negrąžina tinkamo projektų sąrašo. |
| Kelionės ir išlaidos | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Peržiūrint mokesčių sąskaitą**, išlaidų ataskaitose pateikiamas įspėjimas. |
| Kelionės ir išlaidos | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Gavimo nerašo simbolių atpažinimo (OCR) tarnyba neveikia dėl išlaidų OCR tarnybos URL problemos. |
| Kelionės ir išlaidos | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Įjungus **galimybę greitai pateikti** pasikartojančias išlaidas, išlaidų ataskaitų elemento **eilučių** sumos keisis sumas kiekvieną kartą atidarius puslapį Elemento keitimas. |
| Kelionės ir išlaidos | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Išlaidų ataskaitos panaikinti negalima, kai tarpiniame sąraše yra daugiau nei vienas patvirtinimas. |

## <a name="removed-and-deprecated-features"></a>Pašalintos ir nerekomenduojamos funkcijos

Straipsnyje ["Project Operations" pašalintos arba nebenaudojamos](removed-depreciated-features-project.md) funkcijos aprašomos funkcijos, kurios buvo pašalintos arba nebenaudojamos Dynamics 365 Project Operations.

- Pašalinta funkcija nebepasiekiama naudojantis šiuo produktu.
- Nerekomenduojama funkcija nėra aktyviai programuojama ir gali būti pašalinta būsimuose atnaujinimuose.

Nebenaudojamas skelbimas bus rodomas ["Project Operations](removed-depreciated-features-project.md) " straipsnyje, po 12 mėnesių iki funkcijos išėmimo iš produkto, iš jo bus rodomas nebenaudojamas arba nebenaudojamas funkcijas.

Atlikus keitimus, kurie paveikia tik kompiliavimo laiką, bet yra dvejetainiškai suderinami su smėlio dėžės ir gamybos aplinka, nebenaudojimo laikas bus trumpesnis nei 12 mėnesių. Paprastai, šie pakeitimai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.
