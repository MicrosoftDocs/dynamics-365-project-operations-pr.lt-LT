---
title: Kas nauja – 2022 m. liepos mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kurie pasiekiami 2022 m. liepos mėnesio "Microsoft" Dynamics 365 Project Operations leidime, skirtuose ištekliais / ne atsargomis pagrįstiems scenarijams.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: e63b29741dbaa400a2176ff8b4c35c6d64dfeab4
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403962"
---
# <a name="whats-new-july-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2022 m. liepos mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project" operacijos Dataverse aplinkos versijos 4.44.0.22
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.28 versija

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visus susijusius lentelių žemėlapius, kai atnaujinate "Project Operations" Dataverse sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei nesuaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote paruoštą naudoti lentelės žemėlapį, iš naujo pritaikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis skyriuje Trūksta lentelės stulpelių žemėlapiuose, esančiame [dvigubo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) rašymo trikčių šalinimo vadovo skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Visuotinis diegimas ir konfigūravimas | 2761472 | Apdorojama "Project Operations" diegimo klaida. |
| Sąskaitų pateikimas ir kainodara | 2746940 | Subrangos linijos pavadinimo ilgis turėtų būti ne didesnis kaip 100 ženklų. |
| Sąskaitų pateikimas ir kainodara | 2739162 | Klientai turi matyti juostelės mygtukus faktinių aplinkybių tinklelio rodinyje. |
| Projektų planavimas ir sekimas | 2730318 | Atnaujintas nepalaikomų projekto temos simbolių tikrinimas. |
| Sąskaitų pateikimas ir kainodara | 2705361 | Tarpinio etapo sąskaitos pardavimo faktinės sumos turi būti įtrauktos į projekto stebėjimo laukus. |
| Sąskaitų pateikimas ir kainodara | 2675880 | Neleiskite, kad projektas būtų susietas su sutarties eilute, kuri nėra pagrįsta darbu. |
| Sąskaitų pateikimas ir kainodara | 2664396 | Jei citatos kainoraštis išsaugomas be citatos, turi būti klaida, nurodanti, kad pasiūlymas negali būti tuščias. |
| Sąskaitų pateikimas ir kainodara | 2184019 | Skirtukas Užduotimi **pagrįstas atsiskaitymas** neturėtų būti rodomas projektams, kurie neturi atsarginės sutarties ar pasiūlymo. |
| Laikas ir išlaidos | 2754459 | Kai pasikartojantis debesų srauto planavimas yra neaktyvus, parodykite reklamjuostę ir apeikite asinchronizatorių apdorojimą. |
| Sąskaitų pateikimas ir kainodara | 2724391 | Neteisinga išimtis atmetama, kai projekto sutarties padalijimo atsiskaitymo taisyklėje trūksta kliento vertės. |
| Sąskaitų pateikimas ir kainodara | 2708638 | Įrašo nerasta ieškant naudojant tinklelio paiešką medžiagos naudojimo ir medžiagų naudojimo patvirtinimuose.|
| Sąskaitų pateikimas ir kainodara | 2686977 | Neleiskite tikrinti sąskaitos faktūros eilutės tikrinimo kuriant sąskaitą faktūrą. |
| Sąskaitų pateikimas ir kainodara | 2683032 | Apmokestinamų vaidmenų ir kategorijų kopijavimas neviršija 5000 įrašų.|
| Sąskaitų pateikimas ir kainodara | 2673363 | Išlaidų sunaudojimas % projekte yra sugadintas, kai projektui yra ir pastangų, ir išlaidų sąmatos, ir faktinės aplinkybės. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansų srityje

Norėdami gauti informacijos apie į šį naujinimą įtrauktus klaidų pataisymus, prisijunkite prie Microsoft Dynamics "Lifecycle Services" (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcijos, įjungtos pagal numatytuosius nustatymus būsimame leidime

Šioje lentelėje išvardytos funkcijos, kurios pagal numatytuosius nustatymus yra įjungtos 10.0.29 versijoje. Daugumą automatiškai įjungtų funkcijų galima išjungti funkcijų [valdyme](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ateityje kai kurios automatiškai įjungtos funkcijos gali būti pašalintos iš funkcijų valdymo ir taps privalomos. Šis pakeitimas užtikrina, kad klientai naudotų dabartines funkcijas, kad patobulinimai galėtų būti pagrįsti dabartinėmis funkcijomis, kai jos pridedamos. Funkcijos niekada nebus automatiškai įjungtos per mažiau nei vienerius metus, nebent bus nustatyta, kad jos yra būtinos.

| Funkcijos pavadinimas | Įjungimo data | Funkcija pridėta | Funkcijos būsena | Modulis |
| --- | --- | --- |--- |--- |
| Įgalinti valandų operacijos koregavimą atsižvelgiant į finansavimo taisyklių paskirstymo pakeitimą | 2022 m. rugsėjo mėn. 16 d. | 2020 m. spalio 7 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Projekto pirkimo užsakymo išankstinio apmokėjimo sąskaitos faktūros atšaukimo funkcija | 2022 m. rugsėjo mėn. 16 d. | 2021 m. spalio 6 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Ištrinkite sąskaitos faktūros pasiūlymo eilutes, kai naudojate "Project Operations" scenarijams, pagrįstiems ištekliais / be atsargų | 2022 m. rugsėjo mėn. 16 d. | 2021 m. spalio 6 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Apskaitos koregavimas pagal užregistruotą projekto operaciją | 2022 m. rugsėjo mėn. 16 d. | 2020 m. gegužės mėn. 10 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Numatytojo projekto apskaitos nustatymo įgalinimas | 2022 m. rugsėjo mėn. 16 d. | 2020 m. vasario 19 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Įjungti keletą projekto sutarties eilučių | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 29 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Padarykite "Project Hour" žurnalus skirtus tik skaityti, jei dabartinė patvirtinimo būsena neleidžia redaguoti | 2022 m. rugsėjo mėn. 16 d. | 2021 m. spalio 6 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Įgalinkite pardavimo eilučių sinchronizavimą iš pirkimo eilučių, kai atnaujinamos pirkimo eilutės ir įjungiamas pirkimo užsakymo keitimo valdymo parametras | 2022 m. rugsėjo mėn. 16 d. | 2020 m. spalio 7 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| "Project" operacijų įgalinimas Dynamics 365 Customer Engagement | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 29 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |
| Projekto operacijų atšaukimo taisymo funkcija | 2022 m. rugsėjo mėn. 16 d. | 2020 m. liepos 13 d. | Įjungta pagal numatytuosius nustatymus | Projektų valdymas ir apskaita |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcijos, kurios taps privalomos būsimame leidime

Toliau pateiktoje lentelėje išvardytos funkcijos, kurios yra privalomos nuo 10.0.29 versijos.

| Funkcijos pavadinimas | Įjungimo data | Funkcija pridėta | Funkcijos būsena | Modulis |
| --- | --- | --- | --- | --- |
| Apskaičiuokite įsipareigotą vertę finansavimo šaltinyje neapvalindami valiutos kurso | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 14 d. | Privaloma | Projektų valdymas ir apskaita |
| Įgalinkite projekto koregavimo registravimą naudodami tą pačią DK sąskaitą kaip ir pradinė operacija | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 14 d. | Privaloma | Projektų valdymas ir apskaita |
| Išsami informacija apie projekto sutartyje numatytą sumą | 2022 m. rugsėjo mėn. 16 d. | 2019 m. rugpjūčio 31 d. | Privaloma | Projektų valdymas ir apskaita |
| Rūšiavimo pagal išteklius įgalinimas kuriant projekto sąskaitos faktūros pasiūlymą | 2022 m. rugsėjo mėn. 16 d. | 2019 m. rugpjūčio 31 d. | Privaloma | Projektų valdymas ir apskaita |
