---
title: Kas nauja – 2022 m. liepos mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2022 m. liepos mėn. „Microsoft Dynamics 365 Project Operations“ išteklių ir nesaugomais pagrįsti scenarijai.
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

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.44.0.22 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.28 versijoje

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Visuotinis diegimas ir konfigūravimas | 2761472 | Tvarkoma „Project Operations“ diegimo klaida. |
| Sąskaitų pateikimas ir kainodara | 2746940 | Ne ilgesnis kaip 100 simbolių, todėl ne daugiau kaip 100 eilučių pavadinimo. |
| Sąskaitų pateikimas ir kainodara | 2739162 | Klientai turi matyti juostelės mygtukus faktinių duomenų tinklelio rodinyje. |
| Projektų planavimas ir sekimas | 2730318 | Atnaujintas nepalaikomų projekto temos simbolių tikrinimas. |
| Sąskaitų pateikimas ir kainodara | 2705361 | Į projektų sekimo laukus reikia įtraukti etapų, už kuriuos išrašytos sąskaitos, pardavimo faktinius duomenis. |
| Sąskaitų pateikimas ir kainodara | 2675880 | Projekto negalima susieti su ne darbo sutarties eilute. |
| Sąskaitų pateikimas ir kainodara | 2664396 | Jei pasiūlymo kainrašas įrašomas be pasiūlymo, turi būti klaida, reiškianti, kad pasiūlymo negalima tušti. |
| Sąskaitų pateikimas ir kainodara | 2184019 | Projektų, **kurie neturi atsarginių** sutarčių arba pasiūlymų, užduočių sąskaitų išrašymo skirtukas nerodomas. |
| Laikas ir išlaidos | 2754459 | Kai planavimo debesies eiga yra neaktyvi, rodyti reklaminę juostą ir apeiti "Async" apdorojimą. |
| Sąskaitų pateikimas ir kainodara | 2724391 | Kai projekto sutarties skaidymo atsiskaitymo taisyklėje trūksta kliento reikšmės, įvyksta netinkama išimtis. |
| Sąskaitų pateikimas ir kainodara | 2708638 | Įrašas nerastas, kai naudojant tinklelio iešką ieškoma materialių duomenų naudojimo ir patvirtinimų dalyje Medžiagos naudojimas.|
| Sąskaitų pateikimas ir kainodara | 2686977 | Sąskaitos faktūros eilutės tikrinimo apsauga kuriant sąskaitą faktūrą. |
| Sąskaitų pateikimas ir kainodara | 2683032 | Apmokestinamųjų vaidmenų ir kategorijų kopijavimas neturi masto daugiau nei 5000 įrašų.|
| Sąskaitų pateikimas ir kainodara | 2673363 | Projekto išlaidų sutemos % yra iškraipytos, kai yra ir pastangų, ir išlaidų sąmatų, ir faktinių projekto duomenų. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita programoje „Finance”

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į šį naujinimą, prisijunkite prie „Microsoft Dynamics Lifecycle Services“ (LCS) ir rrodyti [KB straipsnis](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Būsimame leidime funkcijos bus įjungtos pagal numatytuosius parametrus

Tolesnėje lentelėje pateiktos funkcijos, kurios įjungtos pagal nustatymus 10.0.29 versijoje. Daugelį funkcijų, kurios buvo automatiškai įjungtos, gali būti išjungtos [Funkcijų valdyme](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ateityje kai kurios automatiškai įjungtos funkcijos gali būti pašalintos iš funkcijų valdymo ir tapti privalomos. Šis pakeitimas užtikrina, kad klientai naudoja dabartines funkcijas, kad patobulinimai galėtų būti sukurti pagal dabartinę funkciją, nes jos yra pridėtos. Funkcijos niekada nebus automatiškai įjungiamos trumpiau nei metus, nebent jos bus nustatytos kaip būtinos.

| Funkcijos pavadinimas | Įgalinti datą | Funkcija įtraukta | Funkcijos būsena | Modulis |
| --- | --- | --- |--- |--- |
| Įjungti valandinės transakcijos sudė pakeitimą, pagal priskyrimo taisyklę | 2022 m. rugsėjo mėn. 16 d. | 2020 m. spalio 7 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Projekto pirkimo užsakymo išsamūs sąskaitų faktūrų atšaukimo funkcija | 2022 m. rugsėjo mėn. 16 d. | 2021 m. spalio 6 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Naikinti SF pasiūlymų eilutes naudojant, „Project Operations“, skirta ištekliais pagal ar nelaikomomis prekėmis pagrįstiems scenarijams | 2022 m. rugsėjo mėn. 16 d. | 2021 m. spalio 6 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Koreguokite užregistruotos projekto transakcijos sąskaitą | 2022 m. rugsėjo mėn. 16 d. | 2020 m. gegužės mėn. 10 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Įjungti projekto numatytąją apskaitos sąranką | 2022 m. rugsėjo mėn. 16 d. | 2020 m. vasario 19 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Įjungti keletą projekto sutarties eilučių | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 29 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Nustatyti, kad projekto valandų valdymo įrankiai būtų tik skaitomi, jei dabartinio patvirtinimo būsena neleidžia redaguoti | 2022 m. rugsėjo mėn. 16 d. | 2021 m. spalio 6 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Kai pirkimo eilutės atnaujinamos ir įjungiamas pirkimo užsakymo pakeitimų valdymo parametras, įjungti pardavimo eilučių sinchronizavimą iš pirkimo eilučių | 2022 m. rugsėjo mėn. 16 d. | 2020 m. spalio 7 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| "Project Operations‟ įjungimas "Dynamics 365 Customer Engagement‟ | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 29 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |
| Projekto transakcijos atšaukimo taisymo funkcija | 2022 m. rugsėjo mėn. 16 d. | 2020 m. liepos 13 d. | Įjungta pagal numatytuosius parametrus | Projektų valdymas ir apskaita |

## <a name="features-that-become-mandatory-in-the-upcoming-release"></a>Funkcijos, kurios būsimame leidime tampa privalomos

Tolesnėje lentelėje pateiktos būtinosios funkcijos, kurios įjungtos pagal nustatymus 10.0.29. versijoje ir vėlesnėse.

| Funkcijos pavadinimas | Įgalinti datą | Funkcija įtraukta | Funkcijos būsena | Modulis |
| --- | --- | --- | --- | --- |
| Apskaičiuokite fiksuotą vertę pagal indavimo šaltinį ne apvalinimo valiutos kursą | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 14 d. | Privaloma | Projektų valdymas ir apskaita |
| Įjungti projekto išsakcijos registravimą naudojant tą pačią, kaip ir originalią operaciją, paskyrą | 2022 m. rugsėjo mėn. 16 d. | 2020 m. birželio 14 d. | Privaloma | Projektų valdymas ir apskaita |
| Projekto sutarties fiksuotos sumos išsami informacija | 2022 m. rugsėjo mėn. 16 d. | 2019 m. rugpjūčio 31 d. | Privaloma | Projektų valdymas ir apskaita |
| Įjungti rūšiavimą pagal išteklius projekto sąskaitų faktūrų kūrimo metu | 2022 m. rugsėjo mėn. 16 d. | 2019 m. rugpjūčio 31 d. | Privaloma | Projektų valdymas ir apskaita |
