---
title: Tiekėjo SF kūrimas
description: Šiame straipsnyje aprašoma tiekėjo sąskaitų faktūrų sąvoka ir paaiškinama, kaip jas sukurti "Microsoft"Dynamics 365 Project Operations.
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
# <a name="create-vendor-invoices"></a>Tiekėjo SF kūrimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norėdami naudoti šiame straipsnyje aprašytas funkcijas, funkcijų valdymo **darbo srityje turite įjungti** funkciją Įgalinti faktinių subrangos sutarčių apdorojimą **naudojant "Project Operations", skirtą ištekliais pagrįstiems scenarijams**.

Tiekėjo sąskaitų faktūrų išrašymas programoje "Microsoft" Dynamics 365 Project Operations gali būti naudojamas paslaugų ir (arba) medžiagų pristatymo išlaidoms, susijusioms su tiekėjų užbaigtu projektu, įrašyti.

Kai paslaugos ir (arba) medžiagos subrangos sutartimi pavedamos tiekėjui, subrangos sutartis yra sutartinė sutartis su tuo tiekėju. Kai tiekėjas teikia paslaugas arba kai medžiagos gaunamos ir naudojamos projekto užduotims atlikti, išlaidos įrašomos į projektą. Tada tiekėjas periodiškai siunčia sąskaitas faktūras. Šios sąskaitos faktūros yra patikrintos ir suderinamos su išlaidomis, kurios įrašomos į projektą. Baigus tikrinimo procesą, tiekėjo SF patvirtinama ir išleidžiama mokėjimui.

## <a name="scenarios-for-use"></a>Naudojimo scenarijai

Tiekėjo sf programoje "Project Operations" galima naudoti dviem skirtingiems scenarijams palaikyti:

- Klientai naudojasi visomis subrangos funkcijomis.
- Klientai nenaudoja visų subrangos funkcijų, bet nori turėti vieningą projektų išlaidų rodinį "Project Operations".

### <a name="customers-use-the-full-subcontracting-experiences"></a>Klientai naudojasi visomis subrangos funkcijomis

Tiekėjo SF funkcijos suteikia galimybę patikrinti laiko įrašus, medžiagų naudojimą ir išlaidų įrašus, nurodančius subrangos komponentus, ir suderinti juos su tiekėjo SF eilutėmis. Šis procesas gali būti naudojamas tiekėjo SF eilučių tikslumui patikrinti. Užbaigus tikrinimo procesą ir patvirtinus tiekėjo SF, sistema pakeičia faktines sumas, kurios buvo įrašytos patvirtintais laiko, išlaidų ir medžiagų naudojimo žurnalais, ir sukuria naujas savikainos faktines vertes naudodama tiekėjo SF eilutes.

### <a name="customers-dont-use-the-full-subcontracting-experiences-but-want-to-have-a-unified-view-of-costs-on-projects-in-project-operations"></a>Klientai nenaudoja visų subrangos funkcijų, bet nori turėti vieningą projektų išlaidų rodinį programoje "Project Operations"

Jei stebite subrangos procesą trečiosios šalies sistemoje, galite įrašyti išlaidas iš tos trečiosios šalies sistemos į "Project Operations" sukurdami tiekėjo SF, kuriose nenurodomos subrangos sutartys. Tokiu būdu jūsų projektų vadovai gali turėti vieną vieningą visų konkretaus projekto išlaidų vaizdą.

## <a name="create-vendor-invoices-in-project-operations"></a>Tiekėjo SF kūrimas programoje "Project Operations"

Tiekėjo SF sukuriamos Dynamics 365 Finance, naudojant modulį **Mokėtinos sumos**. Negalite kurti tiekėjo SF tiesiogiai Dataverse.

### <a name="set-up-vendor-invoice-verification"></a>Tiekėjo SF patvirtinimo nustatymas

Jei tiekėjo SF yra skirta subrangos Dataverse sutarčiai, turite įjungti parametrą Rankinis **tikrinimas pm yra būtinas**. Parinkties nustatymas nustato, ar tiekėjo SF turėtų būti automatiškai patvirtinta Dataverse, ar ją reikia patvirtinti rankiniu būdu. Kiekvienos projekto tiekėjo SF antraštėje yra to paties pavadinimo parinktis. Pagal numatytuosius nustatymus visų projekto tiekėjo SF antraštės parinktis nustatoma kaip reikšmė, kurią čia nustatėte. Tačiau galite atnaujinti reikšmę, kaip reikalaujama atskirų tiekėjo sf antraštėje.

Jei parinktis nustatyta kaip **Taip, tiekėjo SF, kuri sukuriama programoje "Finance" ir sinchronizuojama su** Dataverse juodraščio **būsena**. Tada sąskaitą faktūrą turi patvirtinti ir patikrinti projekto vadovas ir ji turi būti patvirtinta prieš ją apdorojant ir registruojant ją konkrečiame projekto ir DK sąskaitose programoje "Finance".

Jei parinktis nustatyta kaip **Ne**, tiekėjo SF bus automatiškai patvirtinta. Jokių tolesnių veiksmų nereikia.

Norėdami nustatyti tiekėjo SF patvirtinimą, atlikite šiuos veiksmus.

1. Dalyje Finansai eikite į **Projektų valdymas ir apskaitos** \> **sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
1. Skirtuke **Finansai** nustatykite parinktį Rankinis **tikrinimas pm yra būtinas** į **Taip,** jei įmonės strategija reikalauja patikrinti subrangovų tiekėjo sąskaitas faktūras. Jei projekto vadovo patvirtinimo nereikia Dataverse, palikite parinkčių rinkinys į **Ne**. Pagal numatytuosius nustatymus parametras bus naudojamas **puslapyje Laukiama tiekėjo SF**.

> [!NOTE]
> Tiekėjo sąskaitos faktūros, sukurtos subrangos sutartims, gali būti tinkamai apdorojamos tik tuo atveju Dataverse, **jei parinktis Rankinis KD patvirtinimas yra nustatyta** kaip **Taip**. Subrangovų kuriamas laiko, medžiagos ir išlaidų išlaidų faktines faktines vertes projekto vadovas gali rankiniu būdu susieti su tiekėjo SF eilutėmis tik tuo atveju, jei ši parinktis nustatyta kaip **Taip**.

### <a name="set-up-a-procurement-integration-account-for-vendor-invoices"></a>Tiekėjo SF įsigijimo integravimo abonemento nustatymas

Kai tiekėjo SF užregistruojama programoje "Finance for Project Operations" – integruotoji aplinka (ne atsargos), finansai registruojami įsigijimo integravimo paskyroje. Sistema sugeneruoja užregistruotos sąskaitos faktūros faktines Dataverse sumas. Šie faktiniai duomenys skelbiami programoje "Finance" naudojant žurnalą "Project" integravimas. Žurnalo "Project integration" registravimas skelbia faktines išlaidas ir pakeičia įsigijimo integravimo paskyrą.

Norėdami nustatyti tiekėjo SF įsigijimo integravimo paskyrą, atlikite šiuos veiksmus.

1. Dalyje Finansai eikite į **Projektų valdymas ir apskaitos** \> **sąranka** \> **Projektų valdymo ir apskaitos parametrai**.
1. Skirtuke **"Project" operacijos, esančios "Dynamics 365 customer engagement"**, pasirinkite **Medžiagų** \> **įsigijimo integravimo paskyra.**

### <a name="create-and-post-subcontract-vendor-invoices"></a>Subrangos tiekėjo SF kūrimas ir registravimas

Kai mokėtinų sumų tarnautojas gauna sąskaitą faktūrą iš subrangovo, programoje "Finance" sukuriama nauja sąskaita faktūra.

1. Dalyje "Finance" eikite į **Mokėtinų** \> **sumų sąskaitos faktūros** \> **Laukiančios tiekėjo SF**.
1. Veiksmų srityje **pasirinkite** **Naujas**, kad sukurtumėte tiekėjo SF.
1. Sąskaitos faktūros antraštės **lauke Sąskaitos faktūros sąskaita** pasirinkite **Subrangovas**.
1. Pasirinkite sąskaitos faktūros datą.
1. Skirtuke **Antraštė** nustatykite parinktį Rankinis **tikrinimas PM yra būtinas** į **Taip**. Numatytasis šios parinkties nustatymas gaunamas iš **puslapio Projekto valdymas ir apskaitos parametrai**. Tačiau jį galima pakeisti tiekėjo SF lygiu.
1. "FastTab" skirtuke **Sf eilutė** pasirinkite **Įtraukti eilutę**, kad sukurtumėte tiekėjo SF eilutę.
1. Pasirinkite įsigijimo kategoriją, kuri buvo sukurta subrangos linijoms, ir įveskite vieneto kainą, matavimo vienetą ir kiekį.
1. Sekcijos tiekėjo SF eilutės skirtuke **Projektas** pasirinkite projektą, pagal kurį subrangovas bendrina subrangos sąskaitą faktūrą.
1. Pasirinkite projekto kategoriją. Tai gali būti bet kokio tipo **prekė**, **išlaidos**, **medžiagos** ar **valandos**.
1. Pasirinkite vaidmenį tik tuo atveju, jei pasirinkta projekto kategorija yra **valandos** tipo.
1. Pasirinkite **Skelbti**, kad užregistruotumėte tiekėjo SF.

Arba galite sukurti tiekėjo SF nuėję į **Mokėtinos** \> **sąskaitos faktūros Sąskaitos faktūros** \> **Atidarykite tiekėjo SF** ir pasirinkdami **Naujas.**

Kai užregistruojama tiekėjo SF, ji tampa pasiekiama Dataverse projektų vadovo patvirtinimui ir apdorojimui.

## <a name="vendor-invoice-processing-in-dataverse"></a>Tiekėjo SF apdorojimas Dataverse

Tiekėjo SF, kuri sukurta programoje Dataverse, kai kurios laukų reikšmės gaunamos iš tiekėjo SF, įrašytos į "Finance". Kitos reikšmės yra numatytosios vertės, gaunamos iš subrangos sutarties.

Šie laukai ir susiję įrašai bus nukopijuoti iš subrangos sutarties į tiekėjo SF antraštę:

- Valiuta
- Sutartį sudarantis vienetas
- Mokėjimo sąlygos

Tiekėjo SF eilutėse "Project Operations" naudoja šias laukų reikšmes, kad įvestų numatytąją subrangos ir subrangos eilutės nuorodą:

- Operacijos klasė
- Vaidmuo
- Operacijos kategorija
- Produktų laukai
- Project
- Užduotis

> [!NOTE]
> Fiksuotos kainos subrangos eilutės nepalaikomos "Project Operations".

[!INCLUDE[footer-include](../includes/footer-banner.md)]
