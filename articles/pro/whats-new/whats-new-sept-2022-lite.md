---
title: Kas nauja 2022 m. rugsėjo mėn. – „Project Operations lite“ visuotinis diegimas
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2022 m. rugsėjo mėn. „Microsoft Dynamics 365 Project Operations“ lite talpinimas.
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

Šis straipsnis taikomas toliau nurodytiems „ Microsoft Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ 4.46.0.60 versijos „Dataverse“ aplinkoje

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

| Funkcijų sritis | Funkcijos pavadinimas | Daugiau informacijos |
| --- | --- | --- |
| Galimybės valdymas | **Pasiūlymų peržiūra ir aktyvavimas**<br>"Project Operations" visiškai palaiko pardavimo procesą. Projekto pasiūlymus galima įjungti, kad būtų galima nurodyti būseną, kai pasiūlymas yra skirtas tik skaityti ir yra peržiūrimas. Suaktyvintus pasiūlymus galima peržiūrėti, kad būtų sukurti nauji pasiūlymai, kurių peržiūros numeris yra didėjantis. Projekto pasiūlymą galima uždaryti kaip laimėtą arba pralaimėtą. | [Projekto pasiūlymo aktyvinimas ir peržiūra](/dynamics365/project-operations/sales/activation-and-revision) |
| Sąskaitų pateikimas ir kainodara | **Numatytoji laiko juostos agnostinė kaina**<br>„Project Operations" pristatė laiko juostos agnostikos datos sąvoką visuose projekto faktiniuose operacijoms. Naujas laukas **Operacijos data**, dabar prieinamas skirtuko eilutėse ir faktiniuose duomenyse, bus naudojamas operacijos datai saugoti, tačiau tos datos neįrašius į "Pristabdęs visuotinį laiką". Ši data bus naudojama tolesniems procesams, pvz., numatytųjų kainų nustatymui ir sąskaitų faktūrų kūrimui. | <p>[Projekto savikainos tarifų nustatymas pagal įvertinimus ir faktinius duomenis](/dynamics365/project-operations/pro/pricing-costing/cost-price-resolution-sales)</p><p>[Projekto pagrindo pardavimo kainų įvertinimų ir faktinių duomenų nustatymas](/dynamics365/project-operations/pro/pricing-costing/sales-price-resolution-sales)</p> |
| Sąskaitų pateikimas ir kainodara | **Datų kainos perrašymai "Project Operations"**<br>Kainos perrašymų įsigaliojimo data suteikia galimybę perrašyti arba pakeisti konkrečias kainoraštyje esančias kainas. | [Kainos perrašymų įsigaliojimo data](/dynamics365/project-operations/pricing-costing/dateffective_price_overrides) |
| Laikas ir išlaidos | **Visuotinis tvirtinantis**<br>Ši funkcija leidžia independent software vendor (ISV) ir centralizuotai patvirtinti, neatsižvelgiant į projekto projekto ar komandos nario būseną. | [Sauga ir patvirtinimas](/dynamics365/project-operations/approvals/approvals-security) |
|Projektų planavimas ir sekimas|**Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti** </br> </br>Išteklių priskyrimo priemonė, redaguojant API, kūrėjams programiškai nurodo užduočių priskyrimo pastangas bet kuriame palaikomame datų intervale, kad būtų galima planuoti daugiau laiko etapus.|[Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti](/dynamics365/project-operations/project-management/schedule-api-preview)|

## <a name="quality-updates"></a>Kokybės naujinimai

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2754422 | Kopijuojant projektus, į projektus medžiagos ir išlaidų sąmatos neįeina į „Dynamics 365 Finance" Dataverse. |
| Laikas ir išlaidos | 2787409 | Nepatvirtintojas gali patvirtinti ne projekto laiko į įrašą. |
| Galimybės valdymas | 2788907 | Atnaujintas klaidos pranešimas dėl unikalių užsakymo eilučių, kuriose yra vėliavos, tikrinimo. |
| Laikas ir išlaidos | 2842253 | Nulinių išimtų tvarkymas siekiant patvirtinti laiką. |
| Sąskaitų pateikimas ir kainodara | 2844181 | Nepavyko sukurti sąskaitų faktūrų, o ne gauti išsąsdų ID. |
| Sąskaitų pateikimas ir kainodara | 2876628 | Q TIK, C JID – kai kainų sąrašo sprendimo vertinimas turi naudoti senesnius kai kainų sąrašo datų diapazono laukus. |
| Subranga | 2893222 | Jei nenurodytas nė vienas komandos nario, kuriam nors vaidmeniui, eilutė turi būti išsamus, galima pažymėti. |
