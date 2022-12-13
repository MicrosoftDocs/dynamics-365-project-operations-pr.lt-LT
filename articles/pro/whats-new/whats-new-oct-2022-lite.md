---
title: Kas nauja 2022 m. spalio mėn. – „Project Operations lite“ visuotinis diegimas
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2022 m. spalio mėnesio "Microsoft Dynamics 365 Project Operations lite" diegimo leidime.
author: ramagadu
ms.date: 11/17/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: b6975e1f8645721fc03239b355b117eb664785f0
ms.sourcegitcommit: 1f162707ac342343fb5390fb9ae335e4cea4f3f2
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/29/2022
ms.locfileid: "9806762"
---
# <a name="whats-new-october-2022---project-operations-lite-deployment"></a>Kas nauja 2022 m. spalio mėn. – „Project Operations lite“ visuotinis diegimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.57.0.176 versijos „Dataverse“ aplinkoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Projektų planavimas ir sekimas | **"Project Operations" išorinis planavimas**<br>Išorinio planavimo režimas leidžia klientams kurti, naujinti ir naikinti objektus, susijusius su darbo paskirstymo struktūromis (WBS), naudojant vietines Dataverse API be dabartinių apribojimų, kuriuos taiko "Project for the Web". | [Išorinis planavimas](/dynamics365/project-operations/project-management/external-scheduling) |
| Visuotinis diegimas ir konfigūravimas | <p>**Leidimas klientams pasirinkti diegimo tipą**<br>Produktu pagrįsti "Project Operations" naujinimai (PDU) naudojami automatiškai įdiegti "Project Operations Dual-write" sprendimą, kai aplinkoje įdiegiami dvigubo rašymo branduolio ir orkestravimo sprendimai.</p><p>Ši funkcija pristato naują **sprendimo naujinimo elgsenos** parametrą projekto parametruose. Kai šis parametras nustatytas kaip **Tik** Lite, PUD nebebus automatiškai įdiegtas "Project Operations Dual-write" sprendimas, net jei aplinkoje įdiegti dvigubo rašymo branduolio ir orkestravimo sprendimai. Toks veikimas bus naudingas klientams, kurie planuoja naudoti dvigubo rašymo sprendimus, kad integruotų pardavimo užsakymus į "finance and operations" programas, bet nori naudoti "Project Operations" supaprastintuoju režimu (t. y. be integravimo į "finance and operations" programas).</p> | |

## <a name="quality-updates"></a>Kokybės naujinimai

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2316317 | Sistema leidžia kurti sąskaitas faktūras, kuriose nėra apmokestinamų operacijų. |
| Sąskaitų pateikimas ir kainodara | 2737300 | Patikrinkite kliento lauko pasiekiamumą prieš pasiekiant formą. |
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
| Išteklių valdymas | 2751560 | Nenuoseklus pageidaujamas organizacijos vienetas išteklių poreikio. |
| Subranga | 2907231 | Tiekėjo SF proceso etapo negalima paankstinti. |
| Laikas ir išlaidos | 2867363 | Įrašai neiškrenta iš rodinio Nebuvimas / atostogos patvirtinimui, kai jie yra eilėje patvirtinti. |
| Laikas ir išlaidos | 2894405 | TESA: nenaudojamas POC katalogas sukelia atitikties problemų. |
