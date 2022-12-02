---
title: Juodraštinių projekto sąskaitų faktūrų pasiūlymų apskaitos koregavimas
description: Šiame straipsnyje paaiškinta, kaip koreguoti su apskaita susijusią informaciją juodraštiniame sąskaitos faktūros pasiūlyme.
author: sigitac
ms.date: 01/05/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 32f566a798d07b698693392f3aa1823f91fe5408
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921220"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Juodraštinių projekto sąskaitų faktūrų pasiūlymų apskaitos koregavimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projekto sąskaitų faktūrų *operacijų išsamią informaciją* projekto vadovas tvarko pro forma sąskaitoje faktūroje. Ši išsami informacija apima sprendimą dėl valandų, išlaidų, medžiagų ar etapų, kuriuos reikia įtraukti į sąskaitą faktūrą, tarifus ir avanso bei išankstinio apmokėjimo sumų taikymą. Patvirtinę originalią išankstinę sąskaitą faktūrą, galite koreguoti operacijų išsamią informaciją sukurdami ir patvirtindami [koreguojamąją išankstinę sąskaitą faktūrą](../proforma-invoicing/corrective-invoices.md).

Projektų sąskaitų faktūrų *apskaitos informacija* tvarkoma klientui skirtame sąskaitų faktūrų dokumente. Į šią informaciją įtraukiamas PVM skaičiavimas ir sąskaitai faktūrai taikomos finansinės dimensijos. Šiame straipsnyje pateikiama išsami informacija apie tai, kaip šią išsamią apskaitos informaciją galima koreguoti juodraštiniame projekto sąskaitos faktūros pasiūlyme.

## <a name="adjust-sales-tax"></a>PVM koregavimas

Numatytąsias atsiskaitymo PVM grupes ir prekių PVM grupes galima koreguoti tiesiogiai sąskaitos faktūros pasiūlymo dokumente. Norėdami koreguoti šias grupes, pasirinkite **Redaguoti**, tada kiekvienoje projekto sąskaitos faktūros pasiūlymo eilutėje esančiame lauke **PVM grupė** arba **Prekių PVM grupė** įveskite naują reikšmę.

## <a name="adjust-financial-dimensions"></a>Finansinių dimensijų koregavimas

### <a name="header-dimensions"></a>Antraštės matmenys

Pagal numatytuosius nustatymus sąskaitų faktūrų finansinės dimensijos išvedamos iš projekto operacijų įrašų, kuriems neišrašytos sąskaitos faktūros, bet kuriems jos bus išrašytos. Tačiau sistemos parametrai leidžia naudoti finansines dimensijas projekto sąskaitų faktūrų antraštėse, kad būtų galima skelbti klientų balansus. Norėdami įjungti šią funkciją, pasirinkite parinktį **Leisti projekto gautinų sumų dimensijų naujinimus**, esančią skirtuke **Finansai**, kuris yra puslapyje **Projektų valdymo ir apskaitos parametrai**.

Sąskaitų faktūrų antraštėse esančias finansines dimensijas galima redaguoti prieš užregistruojant sąskaitą faktūrą. Puslapyje **Projekto sąskaitos faktūros pasiūlymas** pereikite į rodinį **Antraštė**, tada redaguokite reikšmes skirtuke **Finansinės dimensijos**.

Rodinys **Antraštė** pasiekiamas tik tada, kai sistemos administratorius darbo srityje **Funkcijų valdymas** įjungia funkciją **Naudoti projekto sąskaitų faktūrų pasiūlymus ir sąskaitų faktūrų žurnalų formas su antraščių ir eilučių rodiniais**. Šiai funkcijai reikia „Finance“ 10.0.25 arba naujesnės versijos naujinimo.

### <a name="line-dimensions"></a>Eilučių dimensijos

Projekto sąskaitos faktūros pasiūlymo eilutėje finansinių dimensijų tiesiogiai redaguoti negalima. Vietoj to atlikite toliau nurodytus veiksmus, kad pakoreguotumėte finansines dimensijas projekto sąskaitos faktūros pasiūlyme.

1. Projekto sąskaitos faktūros pasiūlyme pasirinkite **Naikinti viską**, kad pašalintumėte projekto sąskaitos faktūros pasiūlymo eilutes.

    Mygtukas **Naikinti viską** pasiekiamas tik tada, kai sistemos administratorius darbo srityje **Funkcijų valdymas** įjungia funkciją **Naudojant „Project Operations“, skirtą ištekliais / ne atsargose laikomomis prekėmis pagrįstiems scenarijams, naikinti sąskaitų faktūrų pasiūlymų eilutes**.

2. Finansinių dimensijų koregavimas

    - **Laisvos formos sąskaitų operacijos (atsiskaitymo etapai).** Eikite į **Visi projektai** \> **Tvarkyti** \> **Laisvos formos operacijos** ir pasirinkite etapą, kurį reikia koreguoti. Tada skirtuke **Finansinės dimensijos** atnaujinkite reikšmes taip, kaip reikia.
    - **Laiko, išlaidų ir medžiagų operacijos.** Puslapyje **Užregistruotos projektų operacijos** pasirinkite **Koreguoti apskaitą**, kad atnaujintumėte finansines dimensijas.

3. Kai pakoreguosite finansinių dimensijų reikšmes, eikite į **Projektų valdymas ir apskaita** \> **Periodiniai** \> **„Project Operations“ integravimas** ir pasirinkite **Importuoti iš paruošimo lentelės**, kad būtų vykdomas periodinis procesas. Šiame procese naudojamos atnaujintos finansinių dimensijų reikšmės, kad iš naujo būtų sukuriamos projekto sąskaitos faktūros pasiūlymo eilutės. Tada atnaujintos reikšmės naudojamos projekto papildomoje knygoje ir didžiojoje knygoje, registruojant projekto sąskaitą faktūrą.
