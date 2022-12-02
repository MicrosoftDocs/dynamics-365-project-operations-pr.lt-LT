---
title: Kas nauja 2022 m. gegužės mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2022 m. gegužės mėn. „Microsoft Dynamics 365 Project Operations“ išteklių ir nesaugomais pagrįsti scenarijai.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: beb75fc4b721d52cddbdaf2d20194218cefced5e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921404"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. gegužės mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.42.0.70 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.26 versijoje

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai
### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Išteklių valdymas | 2634019 | Patobulintos klaidų pranešimai verslo tikrinimo metu įtraukiant bendrosios komandos narius kaip išteklius. |
| Projektų planavimas ir sekimas | 2648515 | Riboti savininko **būsenos** ir **būseno** naujinimai **planavimo** objektuose. |
| Sąskaitų siuntimas ir kainodara | 2653167 | Verčių **tinklelio** dešimtainis skyriklis turi atitikti asmeninių parinkčių **formato parametrus**. |
| Sąskaitų siuntimas ir kainodara| 2662251 | Laukų **Vienetų grupė** ir **Pataisytas vienetas** numatytieji laukeliai kuriant įrašus medžiagų įvertinime. |
| Sąskaitų siuntimas ir kainodara| 2571408 | Kuriant sąskaitos faktūros juodraštį, nepažymėtos pardavimo faktinės sumos antspauduojami profesionalo sąskaitos faktūros ID. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita „Dynamics 365 Finance” programos aplinkose

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į šį naujinimą, prisijunkite prie „Microsoft Dynamics Lifecycle Services“ (LCS) ir rrodyti [KB straipsnis](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
