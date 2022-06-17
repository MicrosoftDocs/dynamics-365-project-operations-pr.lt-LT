---
title: Kas nauja – 2021 m. rugpjūčio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės atnaujinimus, kuriuos galima rasti 2021 m. rugpjūčio mėn.
author: sigitac
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: bd91f7f6b3a6f78161f8900aa06c810a58609b53
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912296"
---
# <a name="whats-new-august-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2021 m. rugpjūčio mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Šis straipsnis taikomas šiems Dynamics 365 Project Operations komponentams ir versijoms:

   - „Project Operations“ 4.13.0.152 versijos „Microsoft Dataverse“ aplinkoje.
   - Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.20 versija.

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- **Patvirtinimo rinkiniai**. Patvirtinimo rinkiniuose laiko, išlaidų arba medžiagų naudojimo patvirtinimo užklausos sugrupuojamos į mažesnius antrinius operacijų rinkinius. Naudojant šį grupavimą, patvirtinimus galima apdoroti pagal projektą konkrečia tvarka ir pakartotinai vykdyti bei nustatyti seką. Sugrupavus užklausas, pagerėja didelio kiekio patvirtinimų apdorojimo patikimumas ir atsekamumas. Norėdami gauti daugiau informacijos, žr. [Patvirtinimo rinkiniai](../approvals/approval-sets.md).

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų.

Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite matyti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Naują schemos versiją galite suaktyvinti pasirinkdami **Lentelių schemų versijos**, pasirinkdami naujausią versiją ir įrašydami pasirinktą versiją. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleisdami schemą susiduriate su problema, vykdykite nurodymus, pateikiamus vadovo Dvigubo rašymo trikčių šalinimas skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Sąskaitų siuntimas ir kainodara | 2295625 | Etapo pavadinimą reikia nukopijuoti iš sąskaitų faktūrų grafiko į sąskaitos faktūros eilutės išsamios informacijos sritį. |
| Sąskaitų siuntimas ir kainodara | 2316323 | Ištekliais pagrįstų scenarijų atveju nuolaida negali būti redaguojama „Project Operations“ išankstinėje sąskaitoje faktūroje. |
|  Galimybių valdymas | 2338619 | Veiklos taisyklės **Galimybė** ir **Pasiūlymas** gali būti iškviečiamos tik puslapiuose. |
| Išteklių valdymas | 2316523 | Naudojant **siuntimo užklausą** iš ištekliaus reikalavimo, prie kurio pridėtas vaidmuo, neturi būti rodoma klaida. |
| Išteklių valdymas | 2326885 | Kuriant išteklių reikalavimą naudojant projektą, neturi būti rodoma klaida. |
| Laikas ir išlaidos | 2335584 | Nerekomenduojami užduočių srautai laiko įraše. |
| Laikas ir išlaidos | 2336884 | Laiko įrašo mygtukas **Kopijuoti savaitę** turi veikti ne tik dabartiniam vartotojui. |


### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektų valdymas ir apskaita pagal Dynamics 365 Finance

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Kelionės ir išlaidos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kai išlaidos sukuriamos pagal kredito kortelės operaciją, užregistruojamos neteisingos tiekėjo operacijos ir PVM operacijos sumos. |
| Kelionės ir išlaidos | [4620366](https://fix.lcs.dynamics.com/Issue/Details?kb=4620366&amp;bugId=579485&amp;dbType=3&amp;qc=e864789bd95505ea624c537d585bf113c2de60b97c88439d44693dbd85aa8e92) | Generuojant mokėjimo žurnalą sukuriamos neteisingos sudengimo eilutės. |
| Kelionės ir išlaidos | [4618082](https://fix.lcs.dynamics.com/Issue/Details?kb=4618082&amp;bugId=583101&amp;dbType=3&amp;qc=9c85ac8ca1e5e9cd07fac9e9aa2cb0914724e28b86ad3339dacf7741f554c605) | Kai išlaidos sukuriamos pagal kredito kortelės operaciją, užregistruojamos neteisingos PVM operacijos sumos. |
| Kelionės ir išlaidos | [4621765](https://fix.lcs.dynamics.com/Issue/Details?kb=4621765&amp;bugId=587306&amp;dbType=3&amp;qc=6fbfad0123d4e95eaf8d5a5a2f6c354577c991b7905c852ab02d1f94e728a876) | Išlaidų eilutės naikinimas gali ilgai užtrukti. |
| Projekto apskaita | [4623737](https://fix.lcs.dynamics.com/Issue/Details?kb=4623737&amp;bugId=598109&amp;dbType=3&amp;qc=4101fc5865201e21815299f2ff11ae46d5d5370510868df86c25ee09a8ca1a0c) | Sistema nepalaiko galimybės nustatyti nuolatinės skaičių sekos, kai registruojate įvertinimą pritaikę KB 4619395. |
| Projekto apskaita | [4623332](https://fix.lcs.dynamics.com/Issue/Details?kb=4623332&amp;bugId=586034&amp;dbType=3&amp;qc=2f64bb1977c4a9c9dd2ce9de7e72230b86eca14b6295c5bbfb614ea97ad81caf) | Gali nepavykti užregistruoti tiekėjo sąskaitos faktūros ir pateikiamas klaidos pranešimas „2021-05-17 d. kvito operacijos nesubalansuotos. (apskaitos valiuta: 0,00 – ataskaitų valiuta: 0,01)“ |
