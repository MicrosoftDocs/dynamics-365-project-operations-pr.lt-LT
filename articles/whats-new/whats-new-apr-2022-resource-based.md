---
title: Kas nauja 2022 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2022 m. balandžio mėn. „Microsoft Dynamics 365 Project Operations“ išteklių ir nesaugomais pagrįsti scenarijai.
author: sigitac
ms.date: 04/08/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 999006b2c2fe2b31d6e47910a3f1a55cab415f0e
ms.sourcegitcommit: 5c971b15295046b3c92ff6638dd1352129f1c390
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/01/2022
ms.locfileid: "9110894"
---
# <a name="whats-new-april-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. balandžio mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.41.0.45 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.26 versijoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Jį galima naudoti projekto pirkimo užsakymuose ir laukiančiose tiekėjo sąskaitose faktūrose. Dėl daugiau informacijos, žr. [Tiekimo kategorijų naudojimas su projekto pirkimo užsakymais ir laukiančiomis sąskaitomis faktūromis](../procurement/configure-procurement-categories.md).

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktame sąraše parodytos dvigubo rašymo schemos, modifikuotos arba įtrauktos „Project Operations“ 2022 m. kovo mėn. leidime.

| Objekto schema | Atnaujinta versija | Komentarai |
| -------------- | ------------------- | ------------|
| „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn\_projectvendorinvoicelines) | 1.0.0.4 | Tiekimo kategorijų naudojimas su projekto pirkimo užsakymais ir laukiančiomis sąskaitomis faktūromis. |

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| ------------ | ---------------- | -------------- |
| Laikas ir išlaidos | 2573900 | Pagal **numatytuosius nustatymus** šiuolaikinę patvirtinimo funkciją reikia įjungti. |
| Sąskaitų siuntimas ir kainodara | 2603313 | Fiksuota įrašo dublikato klaida, dėl kurios nebuvo galima įtraukti pasiūlymo ir sutarties eilučių, į kurias įtrauktas produktas. |
| Visuotinis diegimas ir konfigūravimas | 2611368 | Klientai į sprendimą turi turėti galimybę įtraukti iki penkių pasirinktinių objektų naudodami modernią programų dizaino įrankį. |
| Laikas ir išlaidos | 2628285 | Išspręsta problema, dėl kurios importuojant laiką buvo paveikta galimybė nustatyti teisingą išteklių kategoriją. |
|  Galimybių valdymas| 2628815 | Atnaujinkite pasiūlymo eilutės išsamios informacijos aprašo simbolių limitą, kad jis atitiktų užduoties temos simbolių limitą, kad būtų galima importuoti užduotis, kai tema ilgesnė nei 100 simbolių. |
| Laikas ir išlaidos| 2629547 | Laukelis **Pateikta** pagal projekto patvirtinimų lauką turi nurodyti įrašą pateikęs vartotojas. |
| Laikas ir išlaidos| 2629865 | Kopijuojant **projektus**, užduočių lauke Kopijuoti kategoriją. |
| Laikas ir išlaidos| 2636463 | Šiuolaikinėse patvirtinimo formose fiksuoti patvirtinimų filtrai. |
| Projektų planavimas ir sekimas | 2648300 | Išspręsta problema, dėl kurios projekto savininko keisti negalima. |
| Sąskaitų siuntimas ir kainodara | 2563000 | Negalima naudoti neišrašyto pardavimo, kai valiuta skiriasi nuo sutarties valiutos, eilučių. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita „Dynamics 365 Finance” programos aplinkose

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į šį naujinimą, prisijunkite prie „Microsoft Dynamics Lifecycle Services“ (LCS) ir rrodyti [KB straipsnis](https://fix.lcs.dynamics.com/Issue/Details?bugId=662864).
