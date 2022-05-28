---
title: Kas nauja 2022 m. gegužės mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, kurie yra prieinami "Microsoft" Dynamics 365 Project Operations 2022 m. gegužės mėn.
author: sigitac
ms.date: 05/02/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d3ac63f0d33d36cc5b6d4cea3ab8167e5974cfe6
ms.sourcegitcommit: 7e419a5f73f80fa887084e3b212c90586fc397dd
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/05/2022
ms.locfileid: "8710144"
---
# <a name="whats-new-may-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. gegužės mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Ši tema taikoma šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projekto operacijos aplinkos versijoje Dataverse 4.42.0.70
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.26 versija

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei naujausia žemėlapio versija nesuaktyvinta. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote lentelės struktūrą, iš naujo taikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis [dvigubo rašymo trikčių šalinimo vadovo skyriuje Trūksta lentelės stulpelių problema žemėlapių](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai
### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Išteklių valdymas | 2634019 | Patobulinomi verslo patvirtinimų klaidų pranešimai, kai į bendruosius komandos narius įtraukiami kaip ištekliai. |
| Projektų planavimas ir sekimas | 2648515 | Apriboti savininko **,** būsenos **ir** būsenos **naujinimai** planavimo objektuose. |
| Sąskaitų siuntimas ir kainodara | 2653167 | Įvertinimų tinklelio **dešimtainis skyriklis turi atitikti formato parametrus asmeninėse parinktyse** **.** |
| Sąskaitų siuntimas ir kainodara| 2662251 | Reikšmės laukuose **Pataisytas vienetas** ir **Vienetų grupė numatytosios** kuriant įrašus medžiagų įvertinimuose. |
| Sąskaitų siuntimas ir kainodara| 2571408 | Kuriant SF juodraštį, neapmokėti pardavimo faktiniai duomenys antspauduojami proforma SF ID. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita Dynamics 365 Finance

Norėdami gauti informacijos apie klaidų taisymus, įtrauktus į šį naujinimą, prisijunkite prie Microsoft Dynamics "Lifecycle Services" (LCS) ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
