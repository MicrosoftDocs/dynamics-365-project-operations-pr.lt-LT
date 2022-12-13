---
title: Kas nauja 2022 m. spalio mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2022 m. spalio mėnesio "Microsoft" Dynamics 365 Project Operations leidime, skirtame ištekliais / be atsargų pagrįstiems scenarijams.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 392a12d6954c2390e5bad8e8e36cf58b7a1d0749
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806757"
---
# <a name="whats-new-october-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. spalio mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.57.0.176 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.30 versijoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Projektų planavimas ir sekimas | **"Project Operations" išorinis planavimas**<br>Išorinio planavimo režimas leidžia klientams kurti, naujinti ir naikinti objektus, susijusius su darbo paskirstymo struktūromis (WBS), naudojant vietines Dataverse API be dabartinių apribojimų, kuriuos taiko "Project for the Web". | [Išorinis planavimas](/dynamics365/project-operations/project-management/external-scheduling) |
| Visuotinis diegimas ir konfigūravimas | <p>**Leidimas klientams pasirinkti diegimo tipą**<br>Produktu pagrįsti "Project Operations" naujinimai (PDU) naudojami automatiškai įdiegti "Project Operations Dual-write" sprendimą, kai aplinkoje įdiegiami dvigubo rašymo branduolio ir orkestravimo sprendimai.</p><p>Ši funkcija pristato naują **sprendimo naujinimo elgsenos** parametrą projekto parametruose. Kai šis parametras nustatytas kaip **Tik** Lite, PUD nebebus automatiškai įdiegtas "Project Operations Dual-write" sprendimas, net jei aplinkoje įdiegti dvigubo rašymo branduolio ir orkestravimo sprendimai. Toks veikimas bus naudingas klientams, kurie planuoja naudoti dvigubo rašymo sprendimus, kad integruotų pardavimo užsakymus į "finance and operations" programas, bet nori naudoti "Project Operations" supaprastintuoju režimu (t. y. be integravimo į "finance and operations" programas).</p> | |
| Sąskaitų pateikimas ir kainodara | <p>**Valiutos konvertavimas į išlaidas, už kurias neapmokėta sąskaita, pardavimo operacija integruotoje aplinkoje**<br>Klientams, kurie naudoja "Project Operations", integruotą su "finance and operations" programomis (t. y. išteklių / ne atsargų diegimo tipo), valiutų kursai paprastai įvaldomi "finance and operations" programose. Tačiau, jei išlaidų kategorija turėtų būti įkainota naudojant kainos skaičiavimo metodą "savikaina" arba "antkainis virš savikainos", kai klientui išrašoma sąskaita, valiutos kursas, naudojamas pardavimo sumai apskaičiuoti, naudoja valiutų kursus, o Dataverse ne valiutų kursus iš "Finance and Operations" programų.</p><p>Ši funkcija projekto parametruose pristato naują **valiutos konvertavimo elgsenos** parametrą. Kai šis parametras nustatytas kaip **Išplėstas su atsarginiu variantu**, išlaidų operacijų neapmokėtos pardavimo sumos apskaičiuojamos naudojant valiutų kursus iš "Finance and Operations" programų.</p> | |

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2316317 | Sistema leidžia kurti sąskaitas faktūras, kuriose nėra apmokestinamų operacijų. |
| Sąskaitų pateikimas ir kainodara | 2737300 | Patikrinkite **kliento** lauko pasiekiamumą prieš pasiekiant formą. |
| Sąskaitų pateikimas ir kainodara | 2744948 | Pridėkite nulinį atsiskaitymo metodo tikrinimą. |
| Sąskaitų pateikimas ir kainodara | 2763515 | Nulinės nuorodos klaidos tvarkymas, kai trūksta sąskaitos faktūros pardavimo sutarties. |
| Sąskaitų pateikimas ir kainodara | 2844301 | Paketinės sąskaitos faktūros sukurti nepavyksta dėl klaidos. |
| Sąskaitų pateikimas ir kainodara | 2845869 | Neteisingas organizacijos tarnybos saugojimas. |
| Sąskaitų pateikimas ir kainodara | 2853729 | Vaidmens ir kainos informacija atnaujinama, kai modifikuojamas atsiskaitymo tipas. |
| Sąskaitų pateikimas ir kainodara | 2940350 | Kai faktinės kainos nustatomos, automatiškai įvedami tik aktyvūs kainoraščiai. |
| Visuotinis diegimas ir konfigūravimas | 3001206 | Objektas msdyn\_ replaylogheader neleidžia naujinti klientų orgijų. |
| Galimybės valdymas | 2755582 | Neapibrėžtų nuorodų išimčių rankenėlė padalinto atsiskaitymo taisyklės pagalbinėje priemonėje. |
| Galimybės valdymas | 2761477 | Kai naudojamas išskaidytas atsiskaitymas, panaikinus riboženklį (antraštę), paliekami našlaičių riboženkliai. |
| Galimybės valdymas | 2767595 | Kai pagrindinėje formoje atidaromas medžiagos naudojimo įrašas, įrašo rezervuojamas išteklius pakeičiamas į šiuo metu prisijungusį vartotoją. |
| Projektų planavimas ir sekimas | 2790384 | "Pending OperationSet" skirtasis laikas yra per trumpas. |
| Projektų planavimas ir sekimas | 2957840 | Užduočių įrašyti negalima, o stulpelių negalima įtraukti į integruotų **projekto operacijų puslapį Užduotys** . |
| Išteklių valdymas | 2751560 | Nenuoseklus pageidaujamas organizacijos vienetas išteklių poreikio. |
| Subranga | 2853245 | Tiekėjo SF eilutės faktinių duomenų atitikimas neatnaujina patvirtinimo būsenos, jei sutarties eilutė jau susieta su tiekėjo SF eilute. |
| Subranga | 2907231 | Tiekėjo SF proceso etapo negalima paankstinti. |
| Laikas ir išlaidos | 2867363 | Įrašai neiškrenta iš rodinio Nebuvimas / atostogos patvirtinimui, kai jie yra eilėje patvirtinti. |
| Laikas ir išlaidos | 2894405 | TESA: nenaudojamas POC katalogas sukelia atitikties problemų. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita programoje „Finance”

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į šį naujinimą, prisijunkite prie „Microsoft Dynamics Lifecycle Services“ (LCS) ir rrodyti [KB straipsnis](https://fix.lcs.dynamics.com/Issue/Details?bugId=745468).
