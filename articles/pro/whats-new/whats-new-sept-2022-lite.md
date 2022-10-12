---
title: Kas nauja 2022 m. rugsėjo mėn. – „Project Operations lite“ visuotinis diegimas
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kurie pasiekiami 2022 m. rugsėjo mėnesio "Microsoft lite" Dynamics 365 Project Operations diegimo leidime.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: 2cce7ae25f05258e8bf0bab9430324bc9b30e329
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621354"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Kas nauja 2022 m. rugsėjo mėn. – „Project Operations lite“ visuotinis diegimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project" operacijos Dataverse aplinkos versijos 4.46.0.60

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Galimybės valdymas | **Citatų peržiūra ir aktyvinimas**<br>"Project Operations" suteikia visišką pardavimo proceso palaikymą. Projekto citatos gali būti suaktyvintos, kad atspindėtų būseną, kurioje citata yra tik skaitoma ir yra peržiūrima. Suaktyvintas kabutes galima peržiūrėti, kad būtų sukurtos naujos kabutės, turinčios padidintą peržiūrų skaičių. Suaktyvintos projekto citatos arba citatos pataisymai gali būti uždaryti kaip laimėti arba pralaimėti. | [Projekto pasiūlymo aktyvinimas ir peržiūra](/dynamics365/project-operations/sales/activation-and-revision) |
| Sąskaitų pateikimas ir kainodara | **Laiko juostos agnostinės kainos įsipareigojimų nevykdymas**<br>"Project Operations" pristatė laiko juostos agnostinės datos koncepciją visose projekto faktinėse bylose. Naujas laukas Operacijos **data** dabar pasiekiamas žurnalo eilutėse ir faktinėse bylose ir bus naudojamas operacijos įvykdymo datai saugoti, bet nekonvertuojant tos datos į suderintąjį visuotinį laiką. Ši data bus naudojama tolesniems procesams, pvz., kainų įsipareigojimų neįvykdymui ir sąskaitų faktūrų kūrimui. | <p>[Projektinių įvertinimų ir faktinių duomenų savikainos tarifų nustatymas](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Projektinių įvertinimų ir faktinių duomenų pardavimo kainų nustatymas](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Sąskaitų pateikimas ir kainodara | **Datos įsigaliojimo kainos nepaisymas "Project Operations"**<br>Datos įsigaliojimo kainų nepaisymas suteikia galimybę nepaisyti arba pakeisti konkrečias kainas kainoraštyje. | [Faktinės datos kaina nepaiso](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Laikas ir išlaidos | **Visuotinis tvirtintojas**<br>Ši funkcija įgalina nepriklausomą programinės įrangos tiekėją (ISV) ir centralizuotą patvirtinimą, neatsižvelgiant į projekto ar komandos nario būseną projekte. | [Sauga ir patvirtinimas](/dynamics365/project-operations/approvals/approvals-security) |

## <a name="quality-updates"></a>Kokybės naujinimai

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2754422 | Medžiagų ir išlaidų įvertinimai nepatenka į Dynamics 365 Finance, kai projektai kopijuojami Dataverse. |
| Laikas ir išlaidos | 2787409 | Negaliojantis tvirtintojas gali patvirtinti ne projekto laiko įrašą. |
| Galimybės valdymas | 2788907 | Atnaujintas klaidos pranešimas apie užsakymo eilučių, kuriose yra vėliavėlių, unikalumo tikrinimą. |
| Laikas ir išlaidos | 2842253 | Nulinių išimčių tvarkymas laiko patvirtinimui. |
| Sąskaitų pateikimas ir kainodara | 2844181 | Nepavykus gauti koreliacijos ID blokuojamas sąskaitos faktūros kūrimas. |
| Sąskaitų pateikimas ir kainodara | 2876628 | QLD, CLD – įvertinti kainoraščio skiriamąją gebą turėtų būti naudojami senieji kainoraščio dienų sekos laukai. |
| Subrangos | 2893222 | Jei subrangos linijoje nenurodytas joks vaidmuo, turėtų būti įmanoma pasirinkti tą eilutę iš komandos nario bet kokiam vaidmeniui. |
