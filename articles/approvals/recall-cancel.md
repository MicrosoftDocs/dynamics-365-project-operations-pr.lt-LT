---
title: Anksčiau patvirtintų įrašų atšaukimas
description: Šiame straipsnyje paaiškinta, kaip projekto komandos narys gali prašyti anksčiau pateiktų ir patvirtintų laiko, išlaidų ir medžiagų naudojimo įrašų, taip pat kaip projekto vadovas gali patvirtinti arba atmesti atmetimo užklausas.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 54fc7ac2301a4423ebf70b0b67ad489580c347b5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930374"
---
# <a name="recall-previously-approved-entries"></a>Anksčiau patvirtintų įrašų atšaukimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projekto komandos narys, kuris pateikia laiko, išlaidų ar medžiagų naudojimo įrašą, gali atšaukti tą įrašą po to kai jis buvo patvirtintas. Atšaukimo procesą sudaro du pagrindiniai veiksmai:

1. Pateikėjas prašo atšaukti.
2. Tvirtintojas patvirtina atšaukimo prašymą.

## <a name="request-a-recall"></a>Prašymas atšaukti

Norėdami prašyti atšaukti patvirtintą laiko, išlaidų arba medžiagų naudojimo įrašą, atlikite šiuos veiksmus.

1. Atsižvelgdami į norimo atšaukti įrašo tipą, atlikite vieną iš toliau pateiktų veiksmų:

    - Jei naudojate laiko įrašus, eikite į **Projektai** \> **Mano darbas** \>**Laiko įrašas** ir pažymėkite visus laiko įrašus, skirtus konkrečiam projekto ir užduoties deriniui. Arba tinklelyje pažymėkite pavienius laiko langelius, nurodyti tam tikro projekto konkrečiai datai.
    - Jei tai išlaidų įrašai, eikite į **Projektai** \> **Mano darbas** \> **Išlaidos** ir pažymėkite išlaidų įrašo, skirto atšaukti, eilutę.
    - Jei tai materialaus naudojimo įrašai, eikite į **Projektai** \> **Mano darbas** \> **Medžiagų naudojimo žurnalas** ir pažymėkite medžiagų naudojimo įrašo, skirto atšaukti, eilutę.

2. Pažymėkite **Atšaukti**. Rodomos patvirtinimo dialogo langas. Jei pažymėti laiko, išlaidų ar medžiagų naudojimo įrašai jau buvo patvirtinti, būsite paraginti įvesti grąžinimo priežastį.
3. Įveskite atšaukimo priežastį, tada pažymėkite **Gerai**, kad patvirtintumėte operaciją. Sistema siunčia asmeniui, patvirtinusiam įrašus, užklausą patvirtinti atšaukimą.

> [!IMPORTANT]
> Negalite sukurti atšaukimo prašymo anksčiau patvirtintų laiko, išlaidų ar medžiagos naudojimo įrašų, pagal kuriuos klientui jau išrašyta sąskaita faktūra, patvirtinimo. Jei bandysite, gausite pranešimą, kuriame teigiama, kad laiko, išlaidų ar medžiagų naudojimo negalima atšaukti, nes jau buvo išrašyta sąskaita faktūra. Tokiu atveju galite prašyti atšaukti įrašą tik tuomet, jei naudojama koreguojamoji sąskaita faktūra, norint pradinės sąskaitos faktūros klientui išrašyti visą kreditą arba atlikti grąžinimą.

## <a name="approve-or-reject-a-recall-request"></a>Atšaukimo užklausos patvirtinimas arba atmetimas

Norėdami patvirtinti arba atmesti atšaukimo užklausą, atlikite šiuos veiksmus.

1. Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.
2. Sąrašo puslapyje **Patvirtinimai** pakeiskite rodinį į **Atšaukimo užklausos patvirtinti**. Rodomas pateiktų atšaukimo užklausų sąrašas.
3. Pažymėkite vieną arba kelis įrašus, tada pasirinkite **Patvirtinti** arba **Atmesti**.
4. Jei pažymėjote **Patvirtinti**, gausite įspėjimo pranešimą, paaiškinantį patvirtinimo poveikį. Pasirinkite **Gerai** norėdami patvirtinti operaciją. Atšaukimo užklausa patvirtinta.

    -arba-

    Jei pasirinkote **Atmesti**, atšaukimo užklausa atmetama.

> [!IMPORTANT]
> Kai atšaukimas patvirtinamas, kai jis buvo paprašytas, sistema tikrina, ar nėra sąskaitų faktūrų išrašymo veiklos pagal laiko, išlaidų ar medžiagų naudojimo įrašus. Jei įrašui jau buvo išrašyta sąskaita faktūra arba jis yra juodraščio sąskaitoje faktūroje, tvirtintojas gauna klaidos pranešimą, kuriame nurodoma, kad laiko ar išlaidų negalima patvirtinti atšaukti, nes jau buvo išrašyta sąskaita faktūra. Tokiu atveju patvirtintojas galite patvirtinti įrašo atšaukimą tik tuomet, jei naudojama koreguojamoji sąskaita faktūra, norint pradinės sąskaitos faktūros klientui išrašyti visą kreditą arba atlikti grąžinimą.

## <a name="impact-of-a-recall-request"></a>Atšaukimo užklausos poveikis

Kai patvirtinama atšaukti, atsiranda operatyvinis ir finansinis poveikis.

### <a name="operational-impact"></a>Operatyvinis poveikis

Jei atšaukimo užklausa patvirtinama, patvirtinimo įrašas pažymimas kaip **Atmesta**. Įrašo būsena pakeičiama į **Grąžinta** arba **Atmesta**, atsižvelgiant į tai, ar tai yra laiko įrašas, ar išlaidų įrašas, ar medžiagos naudojimo įrašas.

Projekto komandos narys gali peržiūrėti įrašus, redaguoti ir pakartotinai pateikti įrašus arba visiškai panaikinti įrašus.

Jei atšaukimo užklausa atmetama, įrašo būsena lieka **Patvirtinta**, o projekto komandos nariui ar projekto tvirtintojui negalima redaguoti įrašo.

### <a name="financial-impact"></a>Finansinis poveikis

Jei atšaukimo užklausa patvirtinama, atitinkami savikainos ir pardavimo faktiniai duomenys atnaujinami tokiu būdu:

- Laukas **Koregavimo būsena** atnaujinamas į **Pakoreguota**.
- Laukas **SF išrašymo būsena** atnaujinamas į **Pakoreguota**.

Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai. Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes. Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės. Vietoj to, šios reikšmės yra atšaukiamos. Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys. Laukas **Koregavimo būsena**, esantis atvirkštinių faktinių duomenų srityje, nustatomas kaip **Nekoreguojamas**, o laukas **SF išrašymo būsena** nustatomas kaip **Atšaukta**. Dėl šių pakeitimų įrašyto neužbaigto projekto išlaidos ir pajamos nebebus įtraukiamos į sumas, kurias atitinka šie faktiniai duomenys.

Jei atšaukimo užklausa atmetama, ji neturi finansinio poveikio projektui.

## <a name="changes-to-time-entry-records"></a>Laiko įrašų kitimai

Šioje iliustracijoje rodomi kitimai, kurie įvyksta dėl patvirtintų laiko įrašų ir atitinkamčių patvirtinimo įrašų, kai jie atšaukiami.

![Laiko įrašo būsenos perėjimai.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Išlaidų įrašų ir medžiagų naudojimo įrašų kitimai

Šioje iliustracijoje rodomi kitimai, kurie įvyksta dėl patvirtintų išlaidų ir medžiagų naudojimo įrašų ir atitinkamčių patvirtinimo įrašų, kai jie atšaukiami.

![Išlaidų įrašų būsenos perėjimai.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
