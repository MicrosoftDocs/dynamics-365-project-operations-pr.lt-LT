---
title: Juodraštinių projekto sąskaitų faktūrų pasiūlymų apskaitos koregavimas
description: Šiame straipsnyje paaiškinama, kaip koreguoti su apskaita susijusią informaciją sąskaitos faktūros pasiūlymo projekte.
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

Projektų sąskaitų faktūrų *apskaitos informacija* tvarkoma klientui skirtame sąskaitų faktūrų dokumente. Į šią informaciją įtraukiamas PVM skaičiavimas ir sąskaitai faktūrai taikomos finansinės dimensijos. Šiame straipsnyje pateikiama išsami informacija apie tai, kaip šią apskaitos informaciją galima koreguoti projekto SF pasiūlymo projekte.

## <a name="adjust-sales-tax"></a>PVM koregavimas

Numatytąsias atsiskaitymo PVM grupes ir prekių PVM grupes galima koreguoti tiesiogiai sąskaitos faktūros pasiūlymo dokumente. Norėdami koreguoti šias grupes, pasirinkite **Redaguoti**, tada kiekvienoje projekto sąskaitos faktūros pasiūlymo eilutėje esančiame lauke **PVM grupė** arba **Prekių PVM grupė** įveskite naują reikšmę.

## <a name="adjust-financial-dimensions"></a>Finansinių dimensijų koregavimas

### <a name="header-dimensions"></a>Antraštės dimensijos

Pagal numatytuosius nustatymus SF finansinės dimensijos gaunamos iš neapmokėtų projekto operacijų įrašų, kuriems išrašyta SF. Tačiau sistemos parametrai leidžia naudoti finansines dimensijas projekto SF pasiūlymų antraštėje, kad užregistruotumėte klientų balansus. Norėdami įgalinti šią funkciją, puslapio Projektų valdymas ir apskaitos parametrai skirtuke Finansai pasirinkite **Leisti gautinų sumų** projekto dimensijų **naujinimus.** **·**

Finansines dimensijas SF antraštėse galima redaguoti prieš registruojant SF. **Puslapyje Projekto SF pasiūlymas** perjunkite į **antraštės** rodinį, tada redaguokite vertes skirtuke **Finansinės dimensijos**.

Antraštės rodinys **galimas tik po to, kai sistemos administratorius** įgalina formas Naudoti projekto SF pasiūlymą ir SF žurnalo formas su rodinio **Antrašte** ir Eilutė funkcija darbo srityje Funkcijų valdymas **.** Šiai funkcijai reikia "Finance" naujinimo 10.0.25 arba naujesnės versijos.

### <a name="line-dimensions"></a>Eilutės dimensijos

Projekto sąskaitos faktūros pasiūlymo eilutėje finansinių dimensijų tiesiogiai redaguoti negalima. Vietoj to atlikite toliau nurodytus veiksmus, kad pakoreguotumėte finansines dimensijas projekto sąskaitos faktūros pasiūlyme.

1. Projekto sąskaitos faktūros pasiūlyme pasirinkite **Naikinti viską**, kad pašalintumėte projekto sąskaitos faktūros pasiūlymo eilutes.

    Mygtukas **Naikinti viską** pasiekiamas tik tada, kai sistemos administratorius darbo srityje **Funkcijų valdymas** įjungia funkciją **Naudojant „Project Operations“, skirtą ištekliais / ne atsargose laikomomis prekėmis pagrįstiems scenarijams, naikinti sąskaitų faktūrų pasiūlymų eilutes**.

2. Finansinių dimensijų koregavimas

    - **Laisvos formos sąskaitų operacijos (atsiskaitymo etapai).** Eikite į **Visi projektai** \> **Tvarkyti** \> **Laisvos formos operacijos** ir pasirinkite etapą, kurį reikia koreguoti. Tada skirtuke **Finansinės dimensijos** atnaujinkite reikšmes taip, kaip reikia.
    - **Laiko, išlaidų ir medžiagų operacijos.** Puslapyje **Užregistruotos projektų operacijos** pasirinkite **Koreguoti apskaitą**, kad atnaujintumėte finansines dimensijas.

3. Kai pakoreguosite finansinių dimensijų reikšmes, eikite į **Projektų valdymas ir apskaita** \> **Periodiniai** \> **„Project Operations“ integravimas** ir pasirinkite **Importuoti iš paruošimo lentelės**, kad būtų vykdomas periodinis procesas. Šiame procese naudojamos atnaujintos finansinių dimensijų reikšmės, kad iš naujo būtų sukuriamos projekto sąskaitos faktūros pasiūlymo eilutės. Tada atnaujintos reikšmės naudojamos projekto papildomoje knygoje ir didžiojoje knygoje, registruojant projekto sąskaitą faktūrą.
