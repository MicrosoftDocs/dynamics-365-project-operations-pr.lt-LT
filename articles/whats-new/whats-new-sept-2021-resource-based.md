---
title: Kas nauja 2021 m. rugsėjo mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. rugsėjo „Project Operations“ leidime, skirtame išteklių / atsargose nelaikomų medžiagų scenarijams.
author: sigitac
ms.date: 09/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 842ea95892fa4f7a29a778cfd2c33a66e84f676c
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547164"
---
# <a name="whats-new-september-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2021 m. rugsėjo mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

   - „Project Operations“ 4.14.0.99 versijos „Microsoft Dataverse“ aplinkoje.
   - Projektų valdymas ir apskaita 10.0.20 versijos „Dynamics 365 Finance” aplinkoje.

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų. Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite matyti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą iškyla problema, vykdykite instrukcijas, pateikiamas Dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūksta lentelės stulpelių schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Laikas ir išlaidos | 1811407 | Pakoreguotas projekto tvirtintojo saugos vaidmuo, kad būtų galima patvirtinti išlaidų įrašus. |
| Laikas ir išlaidos | 1811438 | Pakoreguotas projekto tvirtintojo saugos vaidmuo, kad būtų galima atšaukti laiko įrašo patvirtinimą. |
| Laikas ir išlaidos | 2370126 | Atnaujintos **Projekto užduoties** ir **Vaidmens** piktogramos **Laiko įrašo** objekte. |
| Laikas ir išlaidos | 2379879 | Pataisyta laiko įrašo funkcija **Kopijuoti savaitę**, kai naudojama „Dynamics 365“, skirta telefonui. |
| Sąskaitų pateikimas ir kainodara | 2371906 | Išankstinės sąskaitos faktūros bendroji suma neturi būti koreguojama „Project Operations“ ištekliais pagrįstuose visuotiniuose diegimuose. |
| Sąskaitų pateikimas ir kainodara | 2385802 | Ištaisyta klaida, įvykstanti atnaujinus projekto bendrąsias sumas su neigiamomis faktinėmis valandomis. |
| Sąskaitų pateikimas ir kainodara | 2389675 | Patobulintas išankstinių sąskaitų faktūrų patvirtinimo veikimas. Ilgai vykdomų užduočių objektas turi atsižvelgti į veiklą, reikalingą norint rašyti apskaitos patvirtinimo rezultatus. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita programoje „Dynamics 365 Finance”

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Kelionės ir išlaidos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Neteisingos sumos, nurodytos tiekėjo ir PVM operacijose, kurios užregistruotos iš išlaidų, sukurtų naudojant kredito kortelės operaciją. |
| Kelionės ir išlaidos | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Generuojant mokėjimų žurnalą sukuriamos neteisingos sudengimo eilutės. |
| Kelionės ir išlaidos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Neteisingos sumos, nurodytos PVM operacijose, kurios užregistruotos iš išlaidų, sukurtų naudojant kredito kortelės operaciją. |
| Kelionės ir išlaidos | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Išlaidų eilutės naikinimas gali ilgai užtrukti. |
| Projekto apskaita | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Kai pritaikote KB 4619395, numeracijos pakeitimas į **Nuolatinė** nepalaikomas ir kai registruojate įvertinimą, įvyksta klaida „Sistema nepalaiko numeracijos Proj_X „nuolatinio“ nustatymo“. |
| Projekto apskaita | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Gali nepavykti užregistruoti tiekėjo sąskaitos faktūros ir bus gautas klaidos pranešimas „2021 17 05 nesubalansuotos kvito operacijos. (apskaitos valiuta: 0,00 – ataskaitų valiuta: 0,01)“. |