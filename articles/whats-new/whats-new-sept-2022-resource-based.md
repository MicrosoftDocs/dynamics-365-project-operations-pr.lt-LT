---
title: Kas nauja 2022 m. rugsėjo mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2022 m. rugsėjo mėnesio "Microsoft" Dynamics 365 Project Operations leidime, skirtame ištekliais / be atsargų pagrįstiems scenarijams.
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

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project Operations" Dataverse aplinkos versijoje 4.46.0.60
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.29 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Galimybės valdymas | **Citatų peržiūra ir aktyvinimas**<br>"Project Operations" visiškai palaiko pardavimo procesą. Projekto citatos gali būti suaktyvintos, kad atspindėtų būseną, kurioje citata yra tik skaitoma ir peržiūrima. Suaktyvintas citatas galima peržiūrėti, kad būtų sukurtos naujos citatos, turinčios padidintą redakcijos numerį. Suaktyvintos projekto citatos arba pasiūlymų pataisymai gali būti uždaryti kaip laimėti arba pralaimėti. | [Projekto pasiūlymo aktyvinimas ir peržiūra](/dynamics365/project-operations/sales/activation-and-revision) |
| Sąskaitų pateikimas ir kainodara | **Numatytoji kaina pagal laiko juostą**<br>"Project Operations" visose projekto faktinėse situacijose įvedė laiko juostos agnostinės datos sąvoką. Naujas laukas Operacijos data **dabar** pasiekiamas žurnalo eilutėse ir faktiniuose duomenyse ir bus naudojamas operacijos įvykdymo datai saugoti, tačiau nekonvertuojant tos datos į suderintąjį visuotinį laiką. Ši data bus naudojama tolesniems procesams, pvz., numatytosioms kainoms ir sąskaitų faktūrų kūrimui. | <p>[Projektu pagrįstų įvertinimų ir faktinių duomenų išlaidų tarifų nustatymas](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Projektinių įvertinimų ir faktinių duomenų pardavimo kainų nustatymas](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Sąskaitų pateikimas ir kainodara | **Datos kainų nepaisymas "Project Operations"**<br>Galiojančios datos kainų nepaisymas suteikia galimybę nepaisyti arba pakeisti konkrečias kainas kainoraštyje. | [Kainų nepaisymas pagal įsigaliojimo datą](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subrangos | **Subrangos ir tiekėjo sąskaitų faktūrų suderinimas**<br>Ši funkcija leidžia klientams kurti subrangos sutartis, kad įsigytų išteklių laiko, išlaidų kategorijų ir medžiagų, naudojamų projekto darbui. Ji taip pat leidžia klientams "finance and operations" programose įrašyti tiekėjo SF, kurios bus pasiekiamos projektų vadovams Dataverse patikrinti. | <p>[Subrangos sutarčių valdymas](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Tiekėjo sąskaitų faktūrų kūrimas](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Laikas ir išlaidos | **"Global Approver"**<br>Ši funkcija įgalina nepriklausomą programinės įrangos tiekėją (ISV) ir centralizuotą patvirtinimą, neatsižvelgiant į projekto ar komandos nario būseną projekte. | [Sauga ir patvirtinimas](/dynamics365/project-operations/approvals/approvals-security) |
| Išlaidų valdymas | **Galimybė registruoti išlaidų įsipareigojimą tiekėjo valiuta**<br>Ši funkcija leidžia registruoti grynųjų pinigų mokėjimo metodo išlaidų ataskaitas tiekėjo valiuta. | [Galimybė registruoti išlaidų įsipareigojimą tiekėjo valiuta](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projektų viešieji pirkimai | **Mokėkite, kai mokami tiekėjo mokėjimai**<br>Ši funkcija įgalina funkciją Mokėti, kai mokama (PWP) galima naudoti su "Project Operations" ne atsargų aplinka. Tai leidžia blokuoti / išlaikyti tiekėjo mokėjimus pagal saugojimo sąlygas, kol mokėjimas bus gautas iš kliento. | [Mokėkite, kai mokami tiekėjo mokėjimai](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projektų viešieji pirkimai | **Projekto pirkimo paraiškos**<br>Ši funkcija leidžia vartotojams kurti su projektu susijusius pirkimo užsakymus juridiniuose subjektuose, kuriuose įgalintos Dynamics 365 Customer Engagement integravimo "Project Operations". Projekto pirkimo užsakymai gali būti naudojami nesaugomų medžiagų įsigijimui pagal projektą, kurį vykdo Pirkimų skyriaus persona, įrašyti. Projektų pirkimo užsakymai nebus sinchronizuojami su Dataverse"". Tačiau galite naudoti virtualų objektą, kad pateiktumėte projekto pirkimo užsakymo eilutes Dataverse projekto vadovo informacijai. Su projektu susijusios tiekėjo SF savikaina yra integruota su objektu "Project Actuals", esančiu Dataverse. Projekto savikaina įrašoma į projekto antrinę knygą naudojant žurnalą "Project Operations Integration". | |
|Projektų planavimas ir sekimas|**Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti** </br> </br>Išteklių priskyrimo kontūro redagavimo API kūrėjai programiškai nurodo užduoties perėmėjo pastangas bet kurioje palaikomoje dienų sekoje, kad būtų galima detaliau planuoti pastangas etapais.|[Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šioje lentelėje pateikiami dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į 2022 m. rugsėjo mėnesio "Project Operations" leidimą.

| Objekto schema | Atnaujinta versija | Komentarai |
| -------------- | ------------------- | ------------|
| „Project Operations“ integravimo faktiniai duomenys (msdyn_actuals) | 1.0.0.15 | Šis žemėlapis palaiko subrangos faktinių sutarčių apdorojimą naudojant "Project Operations", skirtą ištekliais pagrįstiems scenarijams. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices) | 1.0.0.2 | Šis žemėlapis palaiko subrangos faktinių sutarčių apdorojimą naudojant "Project Operations", skirtą ištekliais pagrįstiems scenarijams. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Šis žemėlapis palaiko subrangos faktinių sutarčių apdorojimą naudojant "Project Operations", skirtą ištekliais pagrįstiems scenarijams. |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visus susijusius lentelių žemėlapius, kai naujinate "Project Operations Dataverse " sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei nesuaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės žemėlapį, pakeitimus taikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vykdykite nurodymus, pateiktus [dviejų rašinių trikčių šalinimo vadovo žemėlapių skyriuje](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) Trūkstami lentelės stulpeliai.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2754422 | Medžiagų ir išlaidų įvertinimai neperkeliami į "Finance", kai projektai nukopijuojami į Dataverse"". |
| Laikas ir išlaidos | 2787409 | Negaliojantis tvirtintojas gali patvirtinti ne projekto laiko įrašą. |
| Galimybės valdymas | 2788907 | Atnaujintas klaidos pranešimas apie užsakymo eilučių, kuriose yra vėliavėlių, unikalumo tikrinimą. |
| Laikas ir išlaidos | 2842253 | Nulinis išimčių tvarkymas laiko patvirtinimui. |
| Sąskaitų pateikimas ir kainodara | 2844181 | Nepavykus gauti koreliacijos ID, blokuojamas sąskaitos faktūros kūrimas. |
| Sąskaitų pateikimas ir kainodara | 2876628 | QLD, CLD – įvertinkite kainoraščio skiriamąją gebą, naudokite senstelėjusius kainoraščio dienų sekos laukus. |
| Subrangos | 2893222 | Jei subrangos linijos vaidmuo nenurodytas, turėtų būti įmanoma pasirinkti tą eilutę komandos nariui bet kuriam vaidmeniui. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansų srityje

Norėdami gauti informacijos apie klaidų pataisymus, kurie įtraukti į šį naujinimą, prisijunkite prie Microsoft Dynamics "Lifecycle Services" ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcijos, įjungtos pagal numatytuosius nustatymus būsimame leidime

Šioje lentelėje išvardytos funkcijos, kurios yra įjungtos pagal numatytuosius nustatymus 10.0.30 versijoje. Daugumą automatiškai įjungtų funkcijų galima išjungti dalyje [Funkcijų valdymas](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ateityje kai kurios automatiškai įjungtos funkcijos gali būti pašalintos iš funkcijų valdymo ir tapti privalomos. Šis pakeitimas užtikrina, kad klientai naudoja dabartines funkcijas, kad patobulinimai galėtų būti grindžiami dabartinėmis funkcijomis, kai jie pridedami. Funkcijos niekada nebus automatiškai įjungtos greičiau nei per vienerius metus, nebent bus nustatyta, kad jos yra būtinos.

| Funkcijos pavadinimas | Įjungimo data | Funkcija pridėta | Funkcijos būsena | Modulis |
| --- | --- | --- |--- |--- |
| Įgalinkite "async" veikimą, kai vartotojui reikia perjungti sinchronizavimo ir "async" operacijas | 2022 m. spalio 21 d. | 2021 m. balandžio 9 mėn. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
| Reikalingų kvitų išlaidų politikos vertinimas | 2022 m. spalio 21 d. | 2021 m. gruodžio 20 d. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
| Išlaidų ataskaitų, sukurtų perduodant darbuotojus, sąrašo rodinys | 2022 m. spalio 21 d. | 2020 m. vasario 19 d. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
| Ridos sumų skaičiavimas pagal finansiniai metai | 2022 m. spalio 21 d. | 2022 m. gegužės mėn. 10 d. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
