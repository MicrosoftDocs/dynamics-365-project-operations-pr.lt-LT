---
title: Kas nauja – 2022 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2022 m. birželio mėn. „Microsoft Dynamics 365 Project Operations“ išteklių ir nesaugomais pagrįsti scenarijai.
author: sigitac
ms.date: 06/03/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32bc7793c5a0ee8c04272d3ffcbd290b39fce4cc
ms.sourcegitcommit: 7772d72a7c96a44ffb23369f8ffb436813449239
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/20/2022
ms.locfileid: "9031341"
---
# <a name="whats-new-june-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2022 m. birželio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.43.0.77 arba 4.43.0.119 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.27 versijoje

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktame sąraše parodytos dvigubo rašymo schemos, modifikuotos arba įtrauktos „Project Operations“ 2022 m. birželio mėn. leidime.

| Objekto schema | Atnaujinta versija | Komentarai |
| --- | --- | --- |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices) | 1.0.0.1 | Nebenaudojamas senesnio lauko ir jis susietas su naujuoju tiekėjo sąskaitos faktūros būsenos sekimo lauku. |

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Subranga | 2708885 | Išspręstas klaidos pranešimas, rodomas, kai vartotojas sukuria rezervuotinos išteklių rezervavimo antraštės įrašą, į kurį neįrašoma rezervuotina išteklių. |
| Projektų planavimas ir sekimas | 2629441 | Taisė darbo eigos paleidimo logiką, kad atnaujinus projekto užduotis būtų užkirstas kelias "susveikti". |
| Laikas ir išlaidos | 2641209 | Laiko įvesties importas iš priskyrimų / rezervavimo turi išlaikyti rezervuotinos išteklių nuorodą. |
| Projektų planavimas ir sekimas | 2651148 | Projekto dokumento antraštė turi būti atsainiai.|
| Projektų planavimas ir sekimas | 2653145 | Įtrauktas patikrinimas, siekiant užtikrinti, kad nebus sukurtas projekto įrašas, kurio pavadinime yra neleistini simboliai. |
| Laikas ir išlaidos | 2654710 | Taisė filtravimą **patvirtinimo** puslapyje. |
| Sąskaitų siuntimas ir kainodara | 2667805 | Įtraukti tikrinimą, padedantys išvengti faktinių sąskaitų faktūrų pardavimo rezultatų, jei nėra atsarginių nepažymėtų pardavimo faktinių duomenų. |
| Sąskaitų siuntimas ir kainodara | 2668378 | Įtraukti tikrinimą, kad būtų užkirstas kelias pasirinktinių kainodaros prisiejimių sąrašo įd ėmei, jei nėra loginio pavadinimo ir lauko pavadinimo. |
| Subranga | 2677485 | Atnaujinta tiekėjo sąskaitos faktūros eilučių "dvigubas" rašymo struktūros tikslinė versija. |
| Laikas ir išlaidos | 2700428 | Patobulintos patvirtinimų logikos siekiant užtikrinti, kad kiti projekto patvirtinimo rinkiniai gali būti apdorojami net jei vienas iš patvirtinimo rinkinių įstringa sistemos užduotyse. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita programoje „Finance”

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į šį naujinimą, prisijunkite prie „Microsoft Dynamics Lifecycle Services“ (LCS) ir rrodyti [KB straipsnis](https://fix.lcs.dynamics.com/Issue/Details?bugId=673271).
