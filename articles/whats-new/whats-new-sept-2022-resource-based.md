---
title: Kas nauja 2022 m. rugsėjo mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kurie pasiekiami 2022 m. rugsėjo mėnesio "Microsoft" Dynamics 365 Project Operations leidime, skirtuose ištekliais / ne atsargomis pagrįstiems scenarijams.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: ef8b4dd98d64dac1e2420f8e6a104258f126f112
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621347"
---
# <a name="whats-new-september-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2022 m. rugsėjo mėn. – „Project Operations“, skirta išteklių / atsargose nelaikomų medžiagų scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project" operacijos Dataverse aplinkos versijos 4.46.0.60
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.29 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Galimybės valdymas | **Citatų peržiūra ir aktyvinimas**<br>"Project Operations" suteikia visišką pardavimo proceso palaikymą. Projekto citatos gali būti suaktyvintos, kad atspindėtų būseną, kurioje citata yra tik skaitoma ir yra peržiūrima. Suaktyvintas kabutes galima peržiūrėti, kad būtų sukurtos naujos kabutės, turinčios padidintą peržiūrų skaičių. Suaktyvintos projekto citatos arba citatos pataisymai gali būti uždaryti kaip laimėti arba pralaimėti. | [Projekto pasiūlymo aktyvinimas ir peržiūra](/dynamics365/project-operations/sales/activation-and-revision) |
| Sąskaitų pateikimas ir kainodara | **Laiko juostos agnostinės kainos įsipareigojimų nevykdymas**<br>"Project Operations" pristatė laiko juostos agnostinės datos koncepciją visose projekto faktinėse bylose. Naujas laukas Operacijos **data** dabar pasiekiamas žurnalo eilutėse ir faktinėse bylose ir bus naudojamas operacijos įvykdymo datai saugoti, bet nekonvertuojant tos datos į suderintąjį visuotinį laiką. Ši data bus naudojama tolesniems procesams, pvz., kainų įsipareigojimų neįvykdymui ir sąskaitų faktūrų kūrimui. | <p>[Projektinių įvertinimų ir faktinių duomenų savikainos tarifų nustatymas](/dynamics365/project-operations/pricing-costing/cost-price-resolution)</p><p>[Projektinių įvertinimų ir faktinių duomenų pardavimo kainų nustatymas](/dynamics365/project-operations/pricing-costing/sales-price-resolution)</p> |
| Sąskaitų pateikimas ir kainodara | **Datos įsigaliojimo kainos nepaisymas "Project Operations"**<br>Datos įsigaliojimo kainų nepaisymas suteikia galimybę nepaisyti arba pakeisti konkrečias kainas kainoraštyje. | [Faktinės datos kaina nepaiso](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Subrangos | **Subrangos sutarčių sudarymas ir tiekėjo SF suderinimas**<br>Ši funkcija leidžia klientams kurti subrangos sutartis, kad įsigytų išteklių laiką, išlaidų kategorijas ir medžiagas, naudojamas projekto darbams. Tai taip pat leidžia klientams finansų ir operacijų programose įrašyti tiekėjo SF, kurios bus pasiekiamos projektų vadovams Dataverse patvirtinti. | <p>[Subrangos valdymas](/dynamics365/project-operations/pro/subcontracting/managing-subcontracts-overview)</p><p>[Tiekėjo sąskaitų faktūrų kūrimas](/dynamics365/project-operations/procurement/vendor-invoicing-concept-and-creation)</p> |
| Laikas ir išlaidos | **Visuotinis tvirtintojas**<br>Ši funkcija įgalina nepriklausomą programinės įrangos tiekėją (ISV) ir centralizuotą patvirtinimą, neatsižvelgiant į projekto ar komandos nario būseną projekte. | [Sauga ir patvirtinimas](/dynamics365/project-operations/approvals/approvals-security) |
| Išlaidų valdymas | **Galimybė registruoti išlaidų įsipareigojimus tiekėjo valiuta**<br>Ši funkcija leidžia registruoti grynųjų pinigų mokėjimo metodo išlaidų ataskaitas tiekėjo valiuta. | [Galimybė registruoti išlaidų įsipareigojimus tiekėjo valiuta](/dynamics365/project-operations/expense/posting-expense-reports#enable-the-ability-to-post-expense-liability-in-vendor-currency-for-cash-payment-method-feature) |
| Projekto viešieji pirkimai | **Mokėjimas, kai mokamas tiekėjo mokėjimas**<br>Ši funkcija leidžia funkciją Mokėti, kai mokama (PWP) naudoti su "Project Operations" ne atsargų aplinkomis. Tai leidžia užblokuoti / išlaikyti tiekėjo mokėjimus pagal saugojimo sąlygas, kol mokėjimas bus gautas iš kliento. | [Mokėjimas, kai mokamas tiekėjo mokėjimas](/dynamics365/project-operations/procurement/pay-when-paid) |
| Projekto viešieji pirkimai | **Projekto pirkimo paraiškos**<br>Ši funkcija leidžia vartotojams kurti su projektu susijusius pirkimo užsakymus juridiniuose subjektuose, kuriuose įgalintos "Project Operations" Dynamics 365 Customer Engagement integravimas. Projekto pirkimo užsakymus galima naudoti norint įrašyti neįrengtą medžiagų pirkimą pagal projektą, kurį vykdo Pirkimų skyriaus persona. Projekto pirkimo užsakymai nebus sinchronizuojami su Dataverse. Tačiau galite naudoti virtualų objektą, kad pateiktumėte projekto pirkimo užsakymo eilutes Dataverse projektų vadovo informacijai gauti. Su projektu susijusios tiekėjo SF išlaidos yra integruotos į objektą Projekto faktinės sumos.Dataverse Projekto išlaidos įrašomos į projekto subledgerį naudojant žurnalą "Project Operations Integration". | |

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šioje lentelėje pateikiami dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į 2022 m. rugsėjo mėnesio "Project Operations" leidimą.

| Objekto schema | Atnaujinta versija | Komentarai |
| -------------- | ------------------- | ------------|
| „Project Operations“ integravimo faktiniai duomenys (msdyn_actuals) | 1.0.0.15 | Šis žemėlapis palaiko subrangos faktinių duomenų apdorojimą naudojant "Project Operations", skirtą ištekliais pagrįstiems scenarijams. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices) | 1.0.0.2 | Šis žemėlapis palaiko subrangos faktinių duomenų apdorojimą naudojant "Project Operations", skirtą ištekliais pagrįstiems scenarijams. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn_projectvendorinvoicelines) | 1.0.0.5 | Šis žemėlapis palaiko subrangos faktinių duomenų apdorojimą naudojant "Project Operations", skirtą ištekliais pagrįstiems scenarijams. |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visus susijusius lentelių žemėlapius, kai atnaujinate "Project Operations" Dataverse sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei nesuaktyvinta naujausia žemėlapio versija. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote paruoštą naudoti lentelės žemėlapį, iš naujo pritaikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis skyriuje Trūksta lentelės stulpelių žemėlapiuose, esančiame [dvigubo](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) rašymo trikčių šalinimo vadovo skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2754422 | Medžiagų ir išlaidų įvertinimai nepatenka į finansus, kai projektai kopijuojami Dataverse. |
| Laikas ir išlaidos | 2787409 | Negaliojantis tvirtintojas gali patvirtinti ne projekto laiko įrašą. |
| Galimybės valdymas | 2788907 | Atnaujintas klaidos pranešimas apie užsakymo eilučių, kuriose yra vėliavėlių, unikalumo tikrinimą. |
| Laikas ir išlaidos | 2842253 | Nulinių išimčių tvarkymas laiko patvirtinimui. |
| Sąskaitų pateikimas ir kainodara | 2844181 | Nepavykus gauti koreliacijos ID blokuojamas sąskaitos faktūros kūrimas. |
| Sąskaitų pateikimas ir kainodara | 2876628 | QLD, CLD – įvertinti kainoraščio skiriamąją gebą turėtų būti naudojami senieji kainoraščio dienų sekos laukai. |
| Subrangos | 2893222 | Jei subrangos linijoje nenurodytas joks vaidmuo, turėtų būti įmanoma pasirinkti tą eilutę iš komandos nario bet kokiam vaidmeniui. |

### <a name="project-management-and-accounting-in-finance"></a>Projektų valdymas ir apskaita finansų srityje

Norėdami gauti informacijos apie į šį naujinimą įtrauktus klaidų pataisymus, prisijunkite prie Microsoft Dynamics "Lifecycle Services" ir peržiūrėkite [KB straipsnį](https://fix.lcs.dynamics.com/Issue/Details?bugId=726559).

## <a name="features-turned-on-by-default-in-upcoming-release"></a>Funkcijos, įjungtos pagal numatytuosius nustatymus būsimame leidime

Šioje lentelėje išvardytos funkcijos, kurios pagal numatytuosius nustatymus yra įjungtos 10.0.30 versijoje. Daugumą automatiškai įjungtų funkcijų galima išjungti funkcijų [valdyme](/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview). Ateityje kai kurios automatiškai įjungtos funkcijos gali būti pašalintos iš funkcijų valdymo ir taps privalomos. Šis pakeitimas užtikrina, kad klientai naudotų dabartines funkcijas, kad patobulinimai galėtų būti pagrįsti dabartinėmis funkcijomis, kai jos pridedamos. Funkcijos niekada nebus automatiškai įjungtos per mažiau nei vienerius metus, nebent bus nustatyta, kad jos yra būtinos.

| Funkcijos pavadinimas | Įjungimo data | Funkcija pridėta | Funkcijos būsena | Modulis |
| --- | --- | --- |--- |--- |
| Įgalinkite async veikimą, kai vartotojui reikia perjungti sinchronizavimo ir async operacijas | 2022 m. spalio 21 d. | 2021 m. balandžio 9 mėn. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
| Reikalingų kvitų išlaidų politikos vertinimas | 2022 m. spalio 21 d. | 2021 m. gruodžio 20 d. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
| Išlaidų ataskaitų, sukurtų deleguojant darbuotojus, sąrašo rodinys | 2022 m. spalio 21 d. | 2020 m. vasario 19 d. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
| Ridos sumos skaičiavimas pagal finansiniai metai | 2022 m. spalio 21 d. | 2022 m. gegužės mėn. 10 d. | Įjungta pagal numatytuosius nustatymus | Išlaidų valdymas |
