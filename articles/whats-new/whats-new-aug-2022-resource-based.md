---
title: Kas nauja – 2022 m. rugpjūčio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kurie pasiekiami "Microsoft" Dynamics 365 Project Operations 2022 m. rugpjūčio mėnesio leidime, skirtuose išteklių / ne atsargų scenarijams.
author: ramagadu
ms.date: 07/19/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 4042dca72a33f48e04e51af2a3cfd2da83146afd
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9403867"
---
# <a name="whats-new-august-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2022 m. rugpjūčio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project" operacijos Dataverse aplinkos versijos 4.45.0.53
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.28 versija

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visus susijusius lentelių žemėlapius, kai atnaujinate "Project Operations" Dataverse sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei nesuaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote paruoštą naudoti lentelės žemėlapį, iš naujo pritaikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis skyriuje Trūksta lentelės stulpelių žemėlapiuose, esančiame [dvigubo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) rašymo trikčių šalinimo vadovo skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
|  Galimybių valdymas | 2762089 | Klaidų tvarkymas nutraukiant sutartį kaip prarastą, jei automatinis įrašymas organizacijoje yra išjungtas.|
|Projektų planavimas ir sekimas | 2767841 | Telemetrija atnaujina projekto objektą Kurti arba Naujinti scenarijus.|
|Sąskaitų pateikimas ir kainodara | 2771072 | Nulinės nuorodos išimčių tvarkymas laimint pasiūlymą.|
|Sąskaitų pateikimas ir kainodara | 2844181 |Nepavyko gauti koreliacijos ID ir užblokuoti sąskaitos faktūros sukūrimo.|
|Sąskaitų pateikimas ir kainodara | 2852836 | Vidinės įmonės faktinės sumos trūkstamos vidinės įmonės išlaidoms, sukurtoms ir patvirtintoms CE.|


### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansų srityje

Norėdami gauti informacijos apie į šį naujinimą įtrauktus klaidų pataisymus, prisijunkite prie Microsoft Dynamics "Lifecycle Services" (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=694438).
