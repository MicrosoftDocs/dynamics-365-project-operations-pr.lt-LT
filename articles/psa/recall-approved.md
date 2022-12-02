---
title: Patvirtintas laiko arba išlaidų įrašų atšaukimas
description: Šiame straipsnyje pateikta informacija apie tai, kaip atšaukti anksčiau patvirtintą laiko arba išlaidų operaciją.
author: rumant
ms.custom: ''
ms.author: rumant
ms.date: 03/08/2019
ms.topic: article
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: e106ee8734a7c4986693aa06ce6a3b7349a27ac4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910734"
---
# <a name="recall-approved-time-or-expense-entries"></a>Patvirtintas laiko arba išlaidų įrašų atšaukimas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekto komandos narys arba kitas asmuo, kuris pateikia laiko arba išlaidų įrašą, gali atšaukti tą laiko arba išlaidų įrašą, kai jis buvo patvirtintas. Patvirtinto laiko arba išlaidų įrašo atšaukimo procesą sudaro du veiksmai:

1. Pateikėjas prašo atšaukti.
2. Tvirtintojas patvirtina atšaukimą.

## <a name="request-a-recall"></a>Prašymas atšaukti

Norėdami prašyti atšaukti patvirtintą laiko arba išlaidų įrašą, atlikite šiuos veiksmus.

1. Norėdami gauti laiko įrašus, pereikite į **Projektai** \> **Mano projektai** \> **Laiko įrašas**.

    -arba-

    Norėdami gauti išlaidų įrašus, pereikite į **Projektai** \> **Mano projektai** \> **Išlaidų įrašai**.

2. Jei naudojate laiko įrašus, pažymėkite visus laiko įrašus, skirtus konkrečiam projekto ir užduoties deriniui. Arba tinklelyje pažymėkite pavienius laiko langelius, nurodyti tam tikro projekto konkrečiai datai.

    -arba-

    Jei tai išlaidų įrašai, pažymėkite išlaidų įrašo, skirto atšaukti, eilutę.

3. Pažymėkite **Atšaukti**. Rodomos patvirtinimo dialogo langas. Jei pažymėti laiko ir išlaidų įrašai jau buvo patvirtinti, būsite paraginti įvesti grąžinimo priežastį.
4. Įveskite atšaukimo priežastį, tada pažymėkite **Gerai**, kad patvirtintumėte operaciją. Sistema siunčia asmeniui, patvirtinusiam įrašus, užklausą patvirtinti atšaukimą.

> [!NOTE]
> Nors patvirtinti laiko ir išlaidų įrašai gali būti atšaukti, jei patvirtintas laikas arba išlaidos jau buvo išrašyti klientui sąskaita faktūra, nebus galima sukurti atšaukimo užklausos. Naudotojas, kuris bando sukurti atšaukimo užklausą, gaus pranešimą, kuriame teigiama, kad laiko ar išlaidų negalima atšaukti, nes jau buvo išrašyta sąskaita faktūra.

## <a name="approve-or-reject-a-recall-request"></a>Atšaukimo užklausos patvirtinimas arba atmetimas

Norėdami patvirtinti arba atmesti atšaukimo užklausą, atlikite šiuos veiksmus.

1. Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.
2. Sąrašo puslapyje **Patvirtinimai** pakeiskite rodinį į **Atšaukimo užklausos patvirtinti**. Rodomas pateiktų atšaukimo užklausų sąrašas.
3. Pažymėkite vieną arba kelis įrašus, tada pasirinkite **Patvirtinti** arba **Atmesti**.
4. Jei pažymėjote **Patvirtinti**, gausite įspėjimo pranešimą, paaiškinantį patvirtinimo poveikį. Pasirinkite **Gerai** norėdami patvirtinti operaciją. Atšaukimo užklausa patvirtinta.

    -arba-

    Jei pasirinkote **Atmesti**, atšaukimo užklausa atmetama.

> [!NOTE]
> Kai atšaukimas patvirtinamas, sistema tikrina, ar nėra sąskaitų faktūrų išrašymo veiklos pagal laiko arba išlaidų įrašus. Jei įrašui jau buvo išrašyta sąskaita faktūra arba jis yra juodraščio sąskaitoje faktūroje, tvirtintojas gaus klaidos pranešimą, kuriame nurodoma, kad laiko ar išlaidų negalima patvirtinti atšaukti, nes jau buvo išrašyta sąskaita faktūra.

## <a name="impact-of-a-recall-request"></a>Atšaukimo užklausos poveikis

Kai patvirtinama atšaukti, atsiranda operatyvinis ir finansinis poveikis.

### <a name="operational-impact"></a>Operatyvinis poveikis

Jei atšaukimo užklausa patvirtinama, patvirtinimo įrašas pažymimas kaip **Atmesta**. Įrašo būsena pakeičiama į **Grąžinta** arba **Atmesta**, atsižvelgiant į tai, ar tai yra laiko įrašas, ar išlaidų įrašas.

Projekto komandos narys gali peržiūrėti įrašus, redaguoti ir pakartotinai pateikti įrašus arba visiškai panaikinti įrašus.

Jei atšaukimo užklausa atmetama, įrašo būsena lieka **Patvirtinta**, o projekto komandos nariui ar projekto tvirtintojui negalima redaguoti įrašo.

### <a name="financial-impact"></a>Finansinis poveikis

Jei atšaukimo užklausa patvirtinama, atitinkami savikainos ir pardavimo faktiniai duomenys atnaujinami tokiu būdu:

- Laukas **Koregavimo būsena** atnaujinamas į **Pakoreguota**.
- Laukas **SF išrašymo būsena** atnaujinamas į **Pakoreguota**.

Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai. Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes. Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės. Vietoj to, šios reikšmės yra atšaukiamos. Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys. Laukas **Koregavimo būsena**, esantis atvirkštinių faktinių duomenų srityje, nustatomas kaip **Nekoreguojamas**, o laukas **SF išrašymo būsena** nustatomas kaip **Atšaukta**. Dėl šių pakeitimų įrašyto neužbaigto projekto išlaidos ir pajamos nebebus įtraukiamos į sumas, kurias atitinka šie faktiniai duomenys.

Jei atšaukimo užklausa atmetama, ji neturi finansinio poveikio projektui.

## <a name="changes-to-time-entry-records"></a>Laiko įrašų kitimai

Šioje iliustracijoje rodomi kitimai, kurie įvyksta dėl patvirtintų laiko įrašų, kai jie atšaukiami.

![Laiko įrašo būsenos perėjimai.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-entry-records"></a>Išlaidų įrašų kitimai

Šioje iliustracijoje rodomi kitimai, kurie įvyksta dėl patvirtintų išlaidų įrašų, kai jie atšaukiami.

![Išlaidų įrašų būsenos perėjimai.](media/ExpenseEntryStateTransitions.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
