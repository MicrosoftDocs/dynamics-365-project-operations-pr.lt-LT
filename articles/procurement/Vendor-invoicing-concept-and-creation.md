---
title: Tiekėjo sąskaitų faktūrų kūrimas
description: Šiame straipsnyje aprašoma tiekėjo sąskaitų faktūrų sąvoka ir paaiškinta, kaip jas sukurti naudojant „Microsoft Dynamics 365 Project Operations“.
author: suvaidya
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 7f6c1ec46f23b6823734b28755b80ced4e3f9325
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475471"
---
# <a name="create-vendor-invoices"></a>Tiekėjo sąskaitų faktūrų kūrimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norėdami naudoti šiame straipsnyje aprašytas **funkcijas** turite įjungti funkciją Išteklių valdymo darbo srityje naudoti funkciją „Project Operations“ for ištekliams faktinių **duomenų** apdorojimą.

„Microsoft Dynamics 365 Project Operations“ tiekėjo sąskaitų faktūrų išrašymas gali būti naudojamas įrašant išlaidas pagal paslaugų ir (ar) medžiagos pristatymą projektui, kurį užbaigė pardavėjai.

Kai aptarnavimas ir (arba) medžiaga yra prisodintas pardavėjui, šis su šiuo pardavėju susitarimas dėl išsaisvėjo. Kai tiekėjas teikia paslaugas arba kai medžiaga gauta ir naudojama projekto užduotims, išlaidos įrašomas į projektą. Tada tiekėjas periodiškai siunčia sąskaitas faktūras. Šios sąskaitos faktūros tikrinamos ir gretintos su įrašyomis projekto išlaidoms. Baigus tikrinimo procesą tiekėjo sąskaita faktūra patvirtinama ir išleidžiama apmokėti.

## <a name="scenarios-for-use"></a>Naudojimo scenarijai

„Project Operations" tiekėjo sąskaitas faktūras galima naudoti dviem skirtingais scenarijais:

- Klientai naudoja visas susaistymas ir funkcijas.
- Klientai nenaudoja visų papildomai sąsodinimo funkcijų, tačiau nori turėti vieningą projektų išlaidų vaizdą "Project Operations".

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klientai naudoja visas susaistymas ir funkcijas

Naudojant tiekėjo sąskaitų faktūrų funkcijas galima patikrinti laiko įrašus, medžiagos naudojimą ir išlaidų įrašus, kurie nurodo komponentus, kurie yra sugretinti su tiekėjo sąskaitos faktūros eilutėmis. Šį procesą galima naudoti tiekėjo sąskaitos faktūros eilučių tikslumui patikrinti. Baigus tikrinimo procesą ir patvirtinus tiekėjo sąskaitą faktūrą, sistema, naudodama tiekėjo sąskaitos faktūros eilutes, surašo faktinius duomenis, kurie buvo įrašyti patvirtintu laiku, išlaidoms ir medžiagos naudojimo žurnalams, ir sukuria naujus faktinius išlaidų faktinius duomenis.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klientai nenaudoja visų papildomai subrangos sutarties funkcijų, tačiau nori turėti vieningą projektų išlaidų vaizdą „Project Operations“

Jei stebite trečiosios šalies sistemos indų sąsodį, galite įrašyti išlaidas iš tos trečiosios šalies sistemos į „Project Operations", sukurdami tiekėjo sąskaitas faktūras, kurios neturi nuorodos į sugretinimo funkciją. Tokiu būdu jūsų projektų vadovai gali turėti bendrą bendrą visų projekto išlaidų vaizdą.

## <a name="create-vendor-invoices-in-project-operations"></a>Sukurkite tiekėjo sąskaitas„Project Operations“

Tiekėjo sąskaitos faktūros kuriamos naudojant „Dynamics 365 Finance" **modulį Klientai**. Negalite kurti tiekėjo sąskaitų faktūrų tiesiogiai „Dataverse“.

### <a name="set-up-vendor-invoice-verification"></a>Tiekėjo SF sąskaitų patikra

Jei tiekėjo sąskaita faktūra yra skirta tam, kad būtų galimas „Dataverse“ susekusi, **turite įjungti parametrą Rankiniu būdu patikrinti** pagal PM. Parinkties nustatymas nurodo, ar tiekėjo sąskaita faktūra turi būti automatiškai „Dataverse“ patvirtinama, ar ją reikia patvirtinti rankiniu būdu. Kiekvienos projekto tiekėjo sąskaitos faktūros antraštėje yra tokio paties pavadinimo parinktis. Pagal numatytuosius nustatymus visų projekto tiekėjo sąskaitų faktūrų antraštės parinktis nustatoma kaip čia nustatyta reikšmė. Tačiau, kaip nurodyta, atskirų tiekėjo sąskaitų faktūrų antraštėje galite atnaujinti reikšmę.

Jei parinktis nustatyta kaip **Taip**, tiekėjo sąskaita faktūra, sukurta naudojant "Finance" ir sinchronizuota su juodraščio „Dataverse“ **būsena**. Tada projekto vadovas turi patikrinti ir patvirtinti sąskaitą faktūrą, kad ji būtų apdorota ir išsiųsta į konkretų projektą bei "Finance" klientai.

Jei parinktis nustatyta kaip **Ne**, tiekėjo sąskaita faktūra patvirtinama automatiškai. Nereikia atlikti jokių tolesnių veiksmų.

Norėdami nustatyti tiekėjo SF patikrą RCS, atlikite šiuos veiksmus:

1. Eikite į Finance **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
1. Skirtuke "Finansai **nustatykite** parinktį Neautomatinis tikrinimas **pagal** yra būtina parinktis Taip, jei įmonės strategija reikalauja patikrinti arba pardavėjo sąskaitas **faktūras**. Jei projekto vadovo tikrinimo nėra būtina, palikite „Dataverse“ žymę parinkčių rinkinys **Ne**. Pagal numatytuosius nustatymus parametras bus naudojamas puslapyje **Laukianti tiekėjo sąskaita faktūra**.

> [!NOTE]
> Tiekėjo sąskaitos faktūros, sukurtos dėl indų su „Dataverse“ gali būti tinkamai apdorojamos tik tada **jei būtina neautomatinio** tikrinimo parinktis yra **Taip**. Projekto vadovas laiko, medžiagos ir išlaidų išlaidų faktines sumas, kurias sukuria instruktoriai, gali rankiniu būdu greti su tiekėjo sąskaitų faktūrų eilutėmis tik jei ši parinktis nustatyta kaip **Taip**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Viešųjų pirkimų integravimo sąskaitos nustatymas tiekėjo sąskaitoms

Kai tiekėjo sąskaita faktūra užregistruojama „Finance“ for „Project Operations“ – Integrated Environment" (ne akcijų), finansai užregistruojami į "Kai išsamūs integravimo abonementai". Sistema generuoja užregistruotos sąskaitos faktūros „Dataverse“ faktinius duomenis. Šie faktiniai rezultatai "Finance" užregistruojami naudojant "Project Integration". Užregistravus šį žurnalą, suma iš viešųjų pirkimų integravimo sąskaitos perkeliama į projekto kaštų sąskaitą.

Norėdami nustatyti Viešojo integravimo paskyrą tiekėjo sąskaitoms, atlikite šiuos veiksmus.

1. Eikite į Finance **Projektų valdymas ir apskaita** \> **Sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
1. Skirtuke **„Project Operations“ naudojant „Dynamics 365 Customer Engagement“** pasirinkite **Medžiagos** \> **Įsigijimo integravimo paskyra**.

### <a name="create-and-post-subcontract-vendor-invoices"></a>Įmonės vidaus kliento ir tiekėjo sąskaitų faktūrų kūrimas

Kai mokėtinos sumos yra išskleistos, gauna sąskaitą faktūrą iš jos, „Finance" sukuriama nauja sąskaita faktūra.

1. „Finance“ eikite į **Mokėtinos sumos** \> **Sąskaitos faktūros** \> **Laukančios tiekėjo sąskaitos**.
1. **Veiksmų juostoje** pasirinkite **Nauja**, kad sukurtumėte tiekėjo sąskaitą faktūrą.
1. Sąskaitos faktūros antraštės lauke Sąskaitos faktūros abonementas **pažymėkite** "Išrašymo ir išrašymo **vieta"**.
1. Pasirinkite sąskaitų faktūrų datą.
1. Skirtuke **Antraštė** nustatykite parinktį Rankiniu **būdu tikrinti pagal PM** kaip **Taip**. Numatytasis šios parinkties parametras nustatomas projektų **valdymo ir apskaitos parametrų** puslapyje. Tačiau jį galima keisti tiekėjo sąskaitos faktūros lygiu.
1. **"FastTab" sąskaitos** faktūros eilutėje pažymėkite **Įtraukti eilutę,** kad sukurtumėte tiekėjo sąskaitos faktūros eilutę.
1. Pažymėkite, kas buvo sukurta, kad būtų išsamūs, ir įveskite vieneto kainą, matavimo vienetą ir kiekį.
1. Pardavėjo sąskaitų faktūrų eilučių skyriaus skirtuke **Projektas pažymėkite** projektą, pagal kurį ne tik nerašomos ir ne.
1. Pažymėkite projekto kategoriją. Tai gali būti bet kokio tipo **elementas**, **išlaidos**, **medžiaga** arba **valandos**.
1. Pažymėkite vaidmenį tik jei pasirinktos projekto kategorijos tipas Yra **Valanda**.
1. Pasirinkite **Registruoti**, kad užregistruotumėte tiekėjo SF.

Arba galite sukurti tiekėjo sąskaitą faktūrą nuėję į **Mokėtinos sumos** \> **Sąskaitos** \> **Atverti tiekėjo sąskaitas** ir rinktis **Naujas**.

Užregistrus tiekėjo sąskaitą faktūrą, ją galima naudoti projektų Dataverse vadovo tikrinimui ir apdorojimui.

## <a name="vendor-invoice-processing-in-dataverse"></a>Tiekėjo sąskaitos apdorojimas Dataverse

Sukurtose tiekėjo sąskaitos faktūrose kai Dataverse, kurios lauko reikšmės yra iš tiekėjo sąskaitos faktūros, įrašytos "Finance". Kitos reikšmės yra numatytosios reikšmės, kurios yra išsiejimos iš persėdus.

Iš tiekėjo sąskaitos faktūros antraštės bus kopijuojami šie laukai ir susiję įrašai:

- Valiuta
- Sutartį sudarantis vienetas
- Mokėjimo sąlygos

Tiekėjo sąskaitos faktūros eilutėse "Project Operations" naudoja šias lauko reikšmes, kad įvesite numatytąją neesmes ir indinės eilutės nuorodą:

- Operacijos klasė
- Vaidmuo
- Operacijos kategorija
- Produkto laukai
- Project
- Užduotis

> [!NOTE]
> „Project Operations" nepalaiko fiksuotų kainų neasodavimo eilučių.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
