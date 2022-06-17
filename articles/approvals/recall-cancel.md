---
title: Anksčiau patvirtintų įrašų atšaukimas
description: Šiame straipsnyje paaiškinama, kaip projekto komandos narys gali prašyti atšaukti anksčiau pateiktus ir patvirtintus laiko, išlaidų ir medžiagų naudojimo įrašus ir kaip projekto vadovas gali patvirtinti arba atmesti atšaukimo užklausas.
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

Projekto komandos narys, pateikęs laiko, išlaidų ar medžiagų naudojimo įrašą, gali prisiminti tą įrašą po to, kai jis buvo patvirtintas. Atšaukimo procesas turi du pagrindinius etapus:

1. Pateikėjas prašo atšaukti.
2. Tvirtintojas patvirtina atšaukimo užklausą.

## <a name="request-a-recall"></a>Prašymas atšaukti

Atlikite šiuos veiksmus, kad paprašytumėte atšaukti patvirtintus laiko, išlaidų ar medžiagų naudojimo įrašus.

1. Atlikite vieną iš šių veiksmų, atsižvelgdami į įrašo, kurį norite atšaukti, tipą:

    - Norėdami gauti laiko įrašus, eikite į **Projektai** \> **Mano darbo** \> **laiko įrašas** ir pasirinkite visus konkretaus projekto ir užduoties derinio laiko įrašus. Arba tinklelyje pažymėkite pavienius laiko langelius, nurodyti tam tikro projekto konkrečiai datai.
    - Išlaidų įrašų **ieškokite Projects** \> **My Work** \> **Expenses** ir pasirinkite eilutę, kurią norite atšaukti išlaidų įrašui.
    - Medžiagų naudojimo įrašų atveju eikite į **Projektai** \> **Mano darbo** \> **medžiagos naudojimo žurnalas** ir pasirinkite medžiagos naudojimo įrašo, kurį norite atšaukti, eilutę.

2. Pažymėkite **Atšaukti**. Rodomos patvirtinimo dialogo langas. Jei pasirinkti laiko, išlaidų ar medžiagų naudojimo įrašai jau buvo patvirtinti, būsite paraginti įvesti atšaukimo priežastį.
3. Įveskite atšaukimo priežastį, tada pažymėkite **Gerai**, kad patvirtintumėte operaciją. Sistema siunčia asmeniui, patvirtinusiam įrašus, užklausą patvirtinti atšaukimą.

> [!IMPORTANT]
> Negalite sukurti patvirtinto laiko, išlaidų ar medžiagų naudojimo įrašo, kuriam klientui jau išrašyta SF, atšaukimo užklausos. Jei bandysite, gausite pranešimą, kuriame nurodoma, kad laiko, išlaidų ar medžiagų naudojimo įrašo atšaukti negalima, nes jam jau išrašyta SF. Tokiu atveju galite prašyti atšaukti įrašą tik tuo atveju, jei taisomoji sąskaita faktūra naudojama klientui išrašyti visą kreditą arba grąžinti pinigus iš pradinės SĄSKAITOS faktūros.

## <a name="approve-or-reject-a-recall-request"></a>Atšaukimo užklausos patvirtinimas arba atmetimas

Norėdami patvirtinti arba atmesti atšaukimo užklausą, atlikite šiuos veiksmus.

1. Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.
2. Sąrašo puslapyje **Patvirtinimai** pakeiskite rodinį į **Atšaukimo užklausos patvirtinti**. Rodomas pateiktų atšaukimo užklausų sąrašas.
3. Pažymėkite vieną arba kelis įrašus, tada pasirinkite **Patvirtinti** arba **Atmesti**.
4. Jei pažymėjote **Patvirtinti**, gausite įspėjimo pranešimą, paaiškinantį patvirtinimo poveikį. Pasirinkite **Gerai** norėdami patvirtinti operaciją. Atšaukimo užklausa patvirtinta.

    -arba-

    Jei pasirinkote **Atmesti**, atšaukimo užklausa atmetama.

> [!IMPORTANT]
> Kai atšaukimas patvirtinamas, kaip ir tada, kai to prašoma, sistema tikrina, ar nėra sf išrašymo veiklos laiko, išlaidų ar medžiagų naudojimo įrašuose. Jei įrašui jau išrašyta SF arba jei jis yra SF projekte, tvirtintojas gauna klaidos pranešimą, kuriame nurodoma, kad atšaukimo laiko ar išlaidų patvirtinti negalima, nes jam jau išrašyta SF. Tokiu atveju tvirtintojas gali patvirtinti atšaukimą tik tuo atveju, jei taisomoji sąskaita faktūra naudojama išrašant klientui visą kreditą arba grąžinimą originalioje SF.

## <a name="impact-of-a-recall-request"></a>Atšaukimo užklausos poveikis

Kai patvirtinama atšaukti, atsiranda operatyvinis ir finansinis poveikis.

### <a name="operational-impact"></a>Operatyvinis poveikis

Jei atšaukimo užklausa patvirtinama, patvirtinimo įrašas pažymimas kaip **Atmesta**. Įrašo būsena keičiama į Grąžinta **arba** **Atmesta**, atsižvelgiant į tai, ar tai laiko įrašas, ar išlaidų ar medžiagų naudojimo įrašas.

Projekto komandos narys gali peržiūrėti įrašus, redaguoti ir iš naujo pateikti įrašus arba visiškai panaikinti įrašus.

Jei atšaukimo užklausa atmetama, įrašo būsena lieka **Patvirtinta**, o projekto komandos nariui ar projekto tvirtintojui negalima redaguoti įrašo.

### <a name="financial-impact"></a>Finansinis poveikis

Jei atšaukimo užklausa patvirtinama, atitinkami savikainos ir pardavimo faktiniai duomenys atnaujinami tokiu būdu:

- Laukas **Koregavimo būsena** atnaujinamas į **Pakoreguota**.
- Laukas **SF išrašymo būsena** atnaujinamas į **Pakoreguota**.

Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai. Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes. Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės. Vietoj to, šios reikšmės yra atšaukiamos. Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys. Laukas **Koregavimo būsena**, esantis atvirkštinių faktinių duomenų srityje, nustatomas kaip **Nekoreguojamas**, o laukas **SF išrašymo būsena** nustatomas kaip **Atšaukta**. Dėl šių pakeitimų įrašyto neužbaigto projekto išlaidos ir pajamos nebebus įtraukiamos į sumas, kurias atitinka šie faktiniai duomenys.

Jei atšaukimo užklausa atmetama, ji neturi finansinio poveikio projektui.

## <a name="changes-to-time-entry-records"></a>Laiko įrašų kitimai

Toliau pateiktoje iliustracijoje rodomi pakeitimai, atsirandantys patvirtintiems laiko įrašams ir atitinkamiems patvirtinimo įrašams, kai jie atšaukiami.

![Laiko įvedimo būsenos perėjimai.](media/TimeEntryStateTransitions.png)

## <a name="changes-to-expense-and-material-usage-entry-records"></a>Išlaidų ir medžiagų naudojimo įrašų įrašų pakeitimai

Toliau pateiktoje iliustracijoje rodomi pakeitimai, atsirandantys patvirtintiems išlaidų ir medžiagų naudojimo įrašams bei atitinkami patvirtinimo įrašai, kai jie atšaukiami.

![Išlaidų įvedimo būsenos perėjimai.](media/ExpenseEntryStateTransitions.png)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
