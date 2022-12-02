---
title: Anksčiau patvirtintų įrašų patvirtinimo atšaukimas
description: Šiame straipsnyje paaiškinta, kaip projekto vadovas gali atšaukti anksčiau patvirtintų laiko, išlaidų arba medžiagos naudojimo įrašų patvirtinimą.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 08c2248a5fcfc9b7569871a76bc09234ffd172c7
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930466"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Anksčiau patvirtintų įrašų patvirtinimo atšaukimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projekto vadovas arba tvirtintojas, kuris anksčiau patvirtino laiko, išlaidų arba medžiagos naudojimo įrašus, gali atšaukti jų patvirtinimą. 

Norėdami atšaukti anksčiau patvirtintą laiko, išlaidų ar medžiagos naudojimo įrašą, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.
2. Sąrašo puslapyje **Patvirtinimai** rodomi visi laiko įrašai, laukiantys patvirtinimo. Rodinį pakeiskite į **Mano ankstesni patvirtinimai**.
3. Pasirinkite norimus atšaukti laiko, išlaidų arba medžiagos patvirtinimus. Tada veiksmų srityje pasirinkite **Atšaukti patvirtinimą**.
4. Rodomame patvirtinimo pranešime pasirinkite **Gerai**, kad patvirtintumėte operaciją.

> [!IMPORTANT]
> Negalite atšaukti anksčiau patvirtintų laiko, išlaidų ir medžiagos naudojimo įrašų, pagal kuriuos klientui jau išrašyta sąskaita faktūra, patvirtinimo. Jei bandysite, gausite pranešimą, kuriame teigiama, kad patvirtinimo atšaukti negalima, nes jau buvo išrašyta sąskaita faktūra. Tokiu atveju patvirtinimą galite atšaukti tik tuomet, jei naudojama koreguojamoji sąskaita faktūra, norint pradinės sąskaitos faktūros klientui išrašyti visą kreditą arba atlikti grąžinimą.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Anksčiau patvirtintų įrašų patvirtinimo atšaukimo poveikis

Atšaukus patvirtinimą, patiriamas veiklos ir finansinis poveikis.

### <a name="operational-impact"></a>Operatyvinis poveikis

Jei įrašo patvirtinimas atšaukiamas, patvirtinimo įrašas pažymimas kaip **Pateiktas**. Įrašo būsena pakeičiama į **Pateikta**. Šiame etape projekto komandos narys gali atšaukti nepateikdamas atšaukimo užklausos.

Tvirtintojas gali pakeisti laukų **Apmokėtinas kiekis** ir **Atsiskaitymo tipas** reikšmes, tada dar kartą patvirtinti šį įrašą.

### <a name="financial-impact"></a>Finansinis poveikis

Jei įrašo patvirtinimas atšaukiamas, atitinkami savikainos ir pardavimo faktiniai duomenys atnaujinami tokiu būdu:

- Laukas **Koregavimo būsena** atnaujinamas į **Pakoreguota**.
- Laukas **SF išrašymo būsena** atnaujinamas į **Pakoreguota**.

Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai. Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes. Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės. Vietoj to, šios reikšmės yra atšaukiamos. Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys. Laukas **Koregavimo būsena**, esantis atvirkštinių faktinių duomenų srityje, nustatomas kaip **Nekoreguojamas**, o laukas **SF išrašymo būsena** nustatomas kaip **Atšaukta**. Dėl šių pakeitimų įrašyto neužbaigto projekto išlaidos ir pajamos nebebus įtraukiamos į sumas, kurias atitinka šie faktiniai duomenys.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
