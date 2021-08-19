---
title: Juodraštinių projekto sąskaitų faktūrų pasiūlymų apskaitos koregavimas
description: Šioje temoje paaiškinta, kaip koreguoti su apskaita susijusią informaciją juodraštiniame sąskaitos faktūros pasiūlyme.
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 153a239d4b88906909ee0bfae8a18cabebc3766399290d83bb79f5d6375a942c
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6999326"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a>Juodraštinių projekto sąskaitų faktūrų pasiūlymų apskaitos koregavimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projekto sąskaitų faktūrų *operacijų išsamią informaciją* projekto vadovas tvarko pro forma sąskaitoje faktūroje. Ši išsami informacija apima sprendimą dėl valandų, išlaidų, medžiagų ar etapų, kuriuos reikia įtraukti į sąskaitą faktūrą, tarifus ir avanso bei išankstinio apmokėjimo sumų taikymą. Patvirtinę originalią išankstinę sąskaitą faktūrą, galite koreguoti operacijų išsamią informaciją sukurdami ir patvirtindami [koreguojamąją išankstinę sąskaitą faktūrą](../proforma-invoicing/corrective-invoices.md).

Projektų sąskaitų faktūrų *apskaitos informacija* tvarkoma klientui skirtame sąskaitų faktūrų dokumente. Į šią informaciją įtraukiamas PVM skaičiavimas ir sąskaitai faktūrai taikomos finansinės dimensijos. Šioje temoje pateikiama išsami informacija apie tai, kaip šią išsamią apskaitos informaciją galima koreguoti juodraštiniame projekto sąskaitos faktūros pasiūlyme.

## <a name="adjust-sales-tax"></a>PVM koregavimas

Numatytąsias atsiskaitymo PVM grupes ir prekių PVM grupes galima koreguoti tiesiogiai sąskaitos faktūros pasiūlymo dokumente. Norėdami koreguoti šias grupes, pasirinkite **Redaguoti**, tada kiekvienoje projekto sąskaitos faktūros pasiūlymo eilutėje esančiame lauke **PVM grupė** arba **Prekių PVM grupė** įveskite naują reikšmę.

## <a name="adjust-financial-dimensions"></a>Finansinių dimensijų koregavimas

Projekto sąskaitos faktūros pasiūlymo eilutėje finansinių dimensijų tiesiogiai redaguoti negalima. Vietoj to atlikite toliau nurodytus veiksmus, kad pakoreguotumėte finansines dimensijas projekto sąskaitos faktūros pasiūlyme.

1. Projekto sąskaitos faktūros pasiūlyme pasirinkite **Naikinti viską**, kad pašalintumėte projekto sąskaitos faktūros pasiūlymo eilutes.

    > [!NOTE]
    > Mygtukas **Naikinti viską** pasiekiamas tik tada, kai sistemos administratorius darbo srityje **Funkcijų valdymas** įjungia funkciją **Naudojant „Project Operations“, skirtą ištekliais / ne atsargose laikomomis prekėmis pagrįstiems scenarijams, naikinti sąskaitų faktūrų pasiūlymų eilutes**.

2. Finansinių dimensijų koregavimas

    - **Laisvos formos sąskaitų operacijos (atsiskaitymo etapai).** Eikite į **Visi projektai** \> **Tvarkyti** \> **Laisvos formos operacijos** ir pasirinkite etapą, kurį reikia koreguoti. Tada skirtuke **Finansinės dimensijos** atnaujinkite reikšmes taip, kaip reikia.
    - **Laiko, išlaidų ir medžiagų operacijos.** Puslapyje **Užregistruotos projektų operacijos** pasirinkite **Koreguoti apskaitą**, kad atnaujintumėte finansines dimensijas.

3. Kai pakoreguosite finansinių dimensijų reikšmes, eikite į **Projektų valdymas ir apskaita** \> **Periodiniai** \> **„Project Operations“ integravimas** ir pasirinkite **Importuoti iš paruošimo lentelės**, kad būtų vykdomas periodinis procesas. Šiame procese naudojamos atnaujintos finansinių dimensijų reikšmės, kad iš naujo būtų sukuriamos projekto sąskaitos faktūros pasiūlymo eilutės. Tada atnaujintos reikšmės naudojamos projekto papildomoje knygoje ir didžiojoje knygoje, registruojant projekto sąskaitą faktūrą.
