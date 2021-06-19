---
title: Tiekėjo sąskaitų faktūrų integravimas
description: Šioje temoje pateikiama informacijos apie tiekėjų sąskaitų faktūrų integravimą naudojant „Project Operations“.
author: sigitac
ms.date: 04/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d4f1b0ad94b71dc4adc5b2b3423340c5fdb171eb
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002285"
---
# <a name="vendor-invoice-integration"></a>Tiekėjo sąskaitų faktūrų integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Su projektais susijusius viešuosius pirkimus sprendime „Dynamics 365 Project Operations“ galima įrašyti nuėjus į **Mokėtinos sumos** > **Sąskaitos faktūros** > **Laukiančios tiekėjų sąskaitos faktūros** ir naudojant laukiančios tiekėjo sąskaitos faktūros dokumentą. Norėdami sužinoti daugiau, žr. [Atsargose nelaikomų medžiagų įsigijimas naudojant laukiančią tiekėjo sąskaitą faktūrą](../procurement/pending-vendor-invoices.md).

> [!IMPORTANT]
> Prieš naudodami šioje temoje aprašytas funkcijas, peržiūrėkite ir pritaikykite reikiamas konfigūracijas. Norėdami sužinoti daugiau, žr. [Galimybės naudoti atsargose nelaikomas medžiagas ir laukiančias tiekėjų sąskaitas faktūras įjungimas](../procurement/configure-materials-nonstocked.md).

Sprendime „Project Operations“ su projektais susijusios tiekėjų sąskaitos faktūros registruojamos naudojant specialias toliau nurodytas registravimo taisykles.

- Su projektais susiję kaštai (įskaitant nesusigrąžinamus mokesčius) nėra iš karto registruojami didžiosios knygos projekto kaštų sąskaitoje. Kaštai registruojami **viešųjų pirkimų integravimo sąskaitoje**. Ši sąskaita konfigūruojama nuėjus į **Projektų tvarkymas ir apskaita** > **Sąranka** > **Projektų tvarkymo ir apskaitos parametrai**, skirtuke **„Project Operations“ naudojant „Dynamics 365 Customer Engagement“**.
- Naudodama toliau nurodytas lentelių schemas, dvigubo rašymo funkcija tiekėjo sąskaitų faktūrų išsamią informaciją sinchronizuoja su „Microsoft Dataverse“.

     - **„Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices)**: ši lentelės schema sinchronizuoja tiekėjų sąskaitų faktūrų antraščių informaciją. Su „Dataverse“ sinchronizuojamos tik tos tiekėjų sąskaitos faktūros, kuriose yra bent viena eilutė su projekto ID.
     - **„Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eilučių eksportavimo objektas (msdyn_projectvendorinvoicelines)**: ši lentelės schema sinchronizuoja tiekėjų sąskaitų faktūrų eilučių informaciją. Su „Dataverse“ sinchronizuojamos tik tos eilutės, kuriose yra projekto ID.

     > [!NOTE]
     > Tiekėjų sąskaitų faktūrų išsamios informacijos sprendime „Dataverse“ redaguoti negalima.

Registruojant tiekėjo sąskaitą faktūrą, sprendime „Dynamics 365 Finance“ pagal poreikį įrašomos papildomos mokesčių knygos, papildomos tiekėjų knygos ir kiti finansiniai registravimai.

![Tiekėjo sąskaitų faktūrų integravimas](media/DW7VendorInvoice.png)

Kai įrašai rašomi „Dataverse“ objekte **Tiekėjo sąskaita faktūra**, pradedamas automatizuotas įrašų patvirtinimo procesas. Jei reikia, automatizuoto patvirtinimo proceso būseną galima peržiūrėti sprendime „Dataverse“ nuėjus į **Išplėstiniai parametrai** > **Sistema** > **Sistemos užduotys**. Baigusi patvirtinimą, sistema objekte **Faktiniai duomenys** sukuria medžiagų operacijų klasės įrašus.

Su medžiagomis susiję faktiniai duomenys tada apdorojami naudojant dvigubo rašymo lentelės schemą **„Project Operations“ integravimo faktiniai duomenys (msdyn_actuals)**. Norėdami sužinoti daugiau, žr. [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md).

Periodinis procesas **Importavimas iš įrašų paruošimo lentelės** sukuria su tiekėjo sąskaita faktūra susijusias „Project Operations“ integravimo žurnalo eilutes. Numatyta, kad korespondentinė sąskaita nustatoma kaip viešųjų pirkimų integravimo sąskaita. Kai užregistruojamas integravimo žurnalas, pašalinamas tiekėjo sąskaitos faktūros sąskaitos balansas ir eilutės suma perkeliama į projekto kaštų sąskaitą. Dėl tolimesnio sąskaitų faktūrų išrašymo ir pajamų pripažinimo tikslais taip pat sukuriama projekto papildomų knygų operacijų.
