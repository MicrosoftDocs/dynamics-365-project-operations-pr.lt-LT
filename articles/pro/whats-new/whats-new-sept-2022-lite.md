---
title: Kas nauja 2022 m. rugsėjo mėn. – „Project Operations lite“ visuotinis diegimas
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kuriuos galima rasti 2022 m. rugsėjo mėnesio "Microsoft Dynamics 365 Project Operations lite" diegimo leidime.
author: ramagadu
ms.date: 09/28/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: ramagadu
ms.openlocfilehash: a02ac7a69489bc7974eb0e63c11fa5de74795b78
ms.sourcegitcommit: b3a70bc4f2850cff5c2b7114cff7bd61ec298143
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2022
ms.locfileid: "9634863"
---
# <a name="whats-new-september-2022---project-operations-lite-deployment"></a>Kas nauja 2022 m. rugsėjo mėn. – „Project Operations lite“ visuotinis diegimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- "Project Operations" Dataverse aplinkos versijoje 4.46.0.60

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Galimybės valdymas | **Citatų peržiūra ir aktyvinimas**<br>"Project Operations" visiškai palaiko pardavimo procesą. Projekto citatos gali būti suaktyvintos, kad atspindėtų būseną, kurioje citata yra tik skaitoma ir peržiūrima. Suaktyvintas citatas galima peržiūrėti, kad būtų sukurtos naujos citatos, turinčios padidintą redakcijos numerį. Suaktyvintos projekto citatos arba pasiūlymų pataisymai gali būti uždaryti kaip laimėti arba pralaimėti. | [Projekto pasiūlymo aktyvinimas ir peržiūra](/dynamics365/project-operations/sales/activation-and-revision) |
| Sąskaitų pateikimas ir kainodara | **Numatytoji kaina pagal laiko juostą**<br>"Project Operations" visose projekto faktinėse situacijose įvedė laiko juostos agnostinės datos sąvoką. Naujas laukas Operacijos data **dabar** pasiekiamas žurnalo eilutėse ir faktiniuose duomenyse ir bus naudojamas operacijos įvykdymo datai saugoti, tačiau nekonvertuojant tos datos į suderintąjį visuotinį laiką. Ši data bus naudojama tolesniems procesams, pvz., numatytosioms kainoms ir sąskaitų faktūrų kūrimui. | <p>[Projektu pagrįstų įvertinimų ir faktinių duomenų išlaidų tarifų nustatymas](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Projektinių įvertinimų ir faktinių duomenų pardavimo kainų nustatymas](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Sąskaitų pateikimas ir kainodara | **Datos kainų nepaisymas "Project Operations"**<br>Galiojančios datos kainų nepaisymas suteikia galimybę nepaisyti arba pakeisti konkrečias kainas kainoraštyje. | [Kainų nepaisymas pagal įsigaliojimo datą](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Laikas ir išlaidos | **"Global Approver"**<br>Ši funkcija įgalina nepriklausomą programinės įrangos tiekėją (ISV) ir centralizuotą patvirtinimą, neatsižvelgiant į projekto ar komandos nario būseną projekte. | [Sauga ir patvirtinimas](/dynamics365/project-operations/approvals/approvals-security) |
|Projektų planavimas ir sekimas|**Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti** </br> </br>Išteklių priskyrimo kontūro redagavimo API kūrėjai programiškai nurodo užduoties perėmėjo pastangas bet kurioje palaikomoje dienų sekoje, kad būtų galima detaliau planuoti pastangas etapais.|[Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kokybės naujinimai

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2754422 | Medžiagų ir išlaidų įvertinimai neperkeliami į Dynamics 365 Finance, kai projektai kopijuojami į Dataverse. |
| Laikas ir išlaidos | 2787409 | Negaliojantis tvirtintojas gali patvirtinti ne projekto laiko įrašą. |
| Galimybės valdymas | 2788907 | Atnaujintas klaidos pranešimas apie užsakymo eilučių, kuriose yra vėliavėlių, unikalumo tikrinimą. |
| Laikas ir išlaidos | 2842253 | Nulinis išimčių tvarkymas laiko patvirtinimui. |
| Sąskaitų pateikimas ir kainodara | 2844181 | Nepavykus gauti koreliacijos ID, blokuojamas sąskaitos faktūros kūrimas. |
| Sąskaitų pateikimas ir kainodara | 2876628 | QLD, CLD – įvertinkite kainoraščio skiriamąją gebą, naudokite senstelėjusius kainoraščio dienų sekos laukus. |
| Subrangos | 2893222 | Jei subrangos linijos vaidmuo nenurodytas, turėtų būti įmanoma pasirinkti tą eilutę komandos nariui bet kuriam vaidmeniui. |
