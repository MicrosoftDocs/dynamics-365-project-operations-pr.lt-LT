---
title: Kas nauja 2022 m. rugsėjo mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2022 m. rugsėjo mėn. „Microsoft Dynamics 365 Project Operations“ išteklių ir nesaugomais pagrįsti scenarijai.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 04b5f2f8223cdc80028860dd880dde314be244eb
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634816"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. rugsėjo mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.46.0.60 versijos „Dataverse“ aplinkoje
- Projektų valdymas ir apskaita „Dynamics 365 Finance“ aplinkos 10.0.29 versijoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Galimybės valdymas | **Pasiūlymų peržiūra ir aktyvavimas**<br>"Project Operations" visiškai palaiko pardavimo procesą. Projekto pasiūlymus galima įjungti, kad būtų galima nurodyti būseną, kai pasiūlymas yra skirtas tik skaityti ir yra peržiūrimas. Suaktyvintus pasiūlymus galima peržiūrėti, kad būtų sukurti nauji pasiūlymai, kurių peržiūros numeris yra didėjantis. Projekto pasiūlymą galima uždaryti kaip laimėtą arba pralaimėtą. | [Projekto pasiūlymo aktyvinimas ir peržiūra](/dynamics365/project-operations/sales/activation-and-revision) |
| Sąskaitų pateikimas ir kainodara | **Numatytoji laiko juostos agnostinė kaina**<br>„Project Operations" pristatė laiko juostos agnostikos datos sąvoką visuose projekto faktiniuose operacijoms. Naujas laukas **Operacijos data**, dabar prieinamas skirtuko eilutėse ir faktiniuose duomenyse, bus naudojamas operacijos datai saugoti, tačiau tos datos neįrašius į "Pristabdęs visuotinį laiką". Ši data bus naudojama tolesniems procesams, pvz., numatytųjų kainų nustatymui ir sąskaitų faktūrų kūrimui. | <p>[Projekto savikainos tarifų nustatymas pagal įvertinimus ir faktinius duomenis](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Projekto pagrindo pardavimo kainų įvertinimų ir faktinių duomenų nustatymas](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Sąskaitų pateikimas ir kainodara | **Datų kainos perrašymai "Project Operations"**<br>Kainos perrašymų įsigaliojimo data suteikia galimybę perrašyti arba pakeisti konkrečias kainoraštyje esančias kainas. | [Kainos perrašymų įsigaliojimo data](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subranga | **Sąskaitų faktūrų ir pardavėjų sąskaitų faktūrų išsąsdinimas**<br>Ši funkcija leidžia klientams kurti indus ir pirkti išteklių laiką, išlaidų kategorijas ir medžiagą, naudojamą projektų darbui. Tai taip pat leidžia klientams finansų ir operacijų programose įrašyti tiekėjo sąskaitas faktūras, kurias projektų vadovai galės patikrinti Dataverse. | <p>[Subrangos sutarties valdymas](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Tiekėjo sąskaitų faktūrų kūrimas](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Laikas ir išlaidos | **Visuotinis tvirtinantis**<br>Ši funkcija leidžia independent software vendor (ISV) ir centralizuotai patvirtinti, neatsižvelgiant į projekto projekto ar komandos nario būseną. | [Sauga ir patvirtinimas](/dynamics365/project-operations/approvals/approvals-security) |
| Išlaidų valdymas | **Galimybė skelbti išlaidų atsakomybę tiekėjo valiuta**<br>Ši funkcija leidžia išlaidų ataskaitas registruoti tiekėjo valiuta mokėjimo grynaisiais pinigais būdu. | [Galimybė skelbti išlaidų atsakomybę tiekėjo valiuta](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektų rezultatai | **Tiekėjo mokėjimai „mokėti sumokėjus“**<br>Ši funkcija įjungia funkciją "Apmokėti, kai apmokėta" (PWP) galima naudoti su "Project Operations" ne akcijų aplinka. Tai leidžia blokuoti / išlaikyti pardavėjo apmokėjimą pagal saugojimo sąlygas tol, kol iš kliento gaunamas apmokėjimas. | [Tiekėjo mokėjimai „mokėti sumokėjus“](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektų rezultatai | **Projekto pirkimo užsakymai**<br>Ši funkcija leidžia vartotojams kurti su projektais susijusius pirkimo užsakymus juridiniuose objektuose, kuriuose įjungta "Project Operations on Dynamics 365 Customer Engagement‟ integracija. Projektų pirkimo užsakymus galima naudoti nepaisomos medžiagos, dėl kurios projektą siųstas negavimo skyrius persona, įrašui įrašyti. Projektų pirkimo užsakymai nebus sinchronizuojami su Dataverse. Tačiau naudodami virtualų objektą projekto vadovo informacijai norite pateikti Dataverse projekto pirkimo užsakymo eilučių paviršiuje. Su projektu susijusios tiekėjo sąskaitos faktūros išlaidos integruojama su projekto faktinių duomenų objektu, esamu Dataverse. Projekto išlaidų apskaita įrašoma į „Project Operations“integravimo žurnalą dalyje „Integrational journal“. | |
|Projektų planavimas ir sekimas|**Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti** </br> </br>Išteklių priskyrimo priemonė, redaguojant API, kūrėjams programiškai nurodo užduočių priskyrimo pastangas bet kuriame palaikomame datų intervale, kad būtų galima planuoti daugiau laiko etapus.|[Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktame sąraše parodytos dvigubo rašymo schemos, modifikuotos arba įtrauktos „Project Operations“ 2022 m. rugsėjo mėn. leidime.

| Objekto schema | Atnaujinta versija | Komentarai |
| -------------- | ------------------- | ------------|
| „Project Operations“ integravimo faktiniai duomenys (msdyn_actuals) | 1.0.0.15 | Ši struktūra palaiko ištekliaus scenarijų naudojant "Project Operations" faktinių duomenų apdorojimą. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices) | 1.0.0.2 | Ši struktūra palaiko ištekliaus scenarijų naudojant "Project Operations" faktinių duomenų apdorojimą. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Ši struktūra palaiko ištekliaus scenarijų naudojant "Project Operations" faktinių duomenų apdorojimą. |

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2754422 | Kopijuojant projektus, į projektus medžiagos ir išlaidų sąmatos neįeina į "Finance" Dataverse. |
| Laikas ir išlaidos | 2787409 | Nepatvirtintojas gali patvirtinti ne projekto laiko į įrašą. |
| Galimybės valdymas | 2788907 | Atnaujintas klaidos pranešimas dėl unikalių užsakymo eilučių, kuriose yra vėliavos, tikrinimo. |
| Laikas ir išlaidos | 2842253 | Nulinių išimtų tvarkymas siekiant patvirtinti laiką. |
| Sąskaitų pateikimas ir kainodara | 2844181 | Nepavyko sukurti sąskaitų faktūrų, o ne gauti išsąsdų ID. |
| Sąskaitų pateikimas ir kainodara | 2876628 | Q TIK, C JID – kai kainų sąrašo sprendimo vertinimas turi naudoti senesnius kai kainų sąrašo datų diapazono laukus. |
| Subranga | 2893222 | Jei nenurodytas nė vienas komandos nario, kuriam nors vaidmeniui, eilutė turi būti išsamus, galima pažymėti. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita programoje „Finance”

Norėdami gauti daugiau informacijos apie klaidų ištaisymus, įtrauktus į šį naujinimą, prisijunkite prie „Microsoft Dynamics Lifecycle Services“ (LCS) ir rrodyti [KB straipsnis](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Būsimame leidime funkcijos bus įjungtos pagal numatytuosius parametrus

Tolesnėje lentelėje pateiktos funkcijos, kurios įjungtos pagal nustatymus 10.0.30 versijoje. Daugelį funkcijų, kurios buvo automatiškai įjungtos, gali būti išjungtos [Funkcijų valdyme](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ateityje kai kurios automatiškai įjungtos funkcijos gali būti pašalintos iš funkcijų valdymo ir tapti privalomos. Šis pakeitimas užtikrina, kad klientai naudoja dabartines funkcijas, kad patobulinimai galėtų būti sukurti pagal dabartinę funkciją, nes jos yra pridėtos. Funkcijos niekada nebus automatiškai įjungiamos trumpiau nei metus, nebent jos bus nustatytos kaip būtinos.

| Funkcijos pavadinimas | Įgalinti datą | Funkcija įtraukta | Funkcijos būsena | Modulis |
| --- | --- | --- |--- |--- |
| Įjunkite "Async" operaciją, kai vartotojui reikia perjungti sinchronizavimo ir "async" operacijas | 2022 m. spalio 21 d. | 2021 m. balandžio 9 mėn. | Įjungta pagal numatytuosius parametrus | Išlaidų valdymas |
| Reikiamo gavimo išlaidų strategijos sutemos | 2022 m. spalio 21 d. | 2021 m. gruodžio 20 d. | Įjungta pagal numatytuosius parametrus | Išlaidų valdymas |
| Išlaidų ataskaitų, sukurtų išrašant darbuotojus, sąrašo rodinys | 2022 m. spalio 21 d. | 2020 m. vasario 19 d. | Įjungta pagal numatytuosius parametrus | Išlaidų valdymas |
| Alitesų sumų skaičiavimas pagal finansiniai metai | 2022 m. spalio 21 d. | 2022 m. gegužės mėn. 10 d. | Įjungta pagal numatytuosius parametrus | Išlaidų valdymas |
