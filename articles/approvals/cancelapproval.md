---
title: Atšaukti anksčiau patvirtintų įrašų patvirtinimą
description: Šioje temoje paaiškinama, kaip projekto vadovas gali atšaukti anksčiau patvirtintų laiko, išlaidų ar medžiagų naudojimo įrašų patvirtinimą.
author: rumant
ms.date: 01/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 03d4511e85e9fc8d596b269274c4a7e10016244c
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8584790"
---
# <a name="cancel-the-approval-of-previously-approved-entries"></a>Atšaukti anksčiau patvirtintų įrašų patvirtinimą

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projekto vadovas arba tvirtintojas, anksčiau patvirtinęs laiko, išlaidų ar medžiagų naudojimo įrašus, gali atšaukti šių įrašų patvirtinimą. 

Atlikite šiuos veiksmus, kad atšauktumėte anksčiau patvirtinto laiko, išlaidų ar medžiagų naudojimo įrašo patvirtinimą.

1. Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.
2. Sąrašo **puslapyje Patvirtinimai rodomi visų laikų** įrašai, kurie laukia patvirtinimo. Pakeiskite rodinį į **Mano ankstesni patvirtinimai**.
3. Pasirinkite atšaukimo laiką, išlaidas arba medžiagų patvirtinimus. Tada veiksmų srityje pasirinkite **Atšaukti patvirtinimą**.
4. Pasirodžiusiame patvirtinimo pranešimo lauke pasirinkite **Gerai**, kad patvirtintumėte operaciją.

> [!IMPORTANT]
> Negalite atšaukti anksčiau patvirtinto laiko, išlaidų ir medžiagų naudojimo įrašo, kuriam klientui jau išrašyta SF, patvirtinimo. Jei bandysite, gausite pranešimą, kuriame nurodoma, kad patvirtinimo atšaukti negalima, nes jam jau išrašyta SF. Tokiu atveju patvirtinimą galite atšaukti tik tuo atveju, jei taisomoji sąskaita faktūra naudojama norint išrašyti klientui visą kreditą arba grąžinti pinigus iš pradinės sąskaitos faktūros.

## <a name="impact-of-canceling-the-approval-of-a-previously-approved-entry"></a>Anksčiau patvirtinto įrašo patvirtinimo atšaukimo poveikis

Atšaukus patvirtinimą, patiriamas veiklos ir finansinis poveikis.

### <a name="operational-impact"></a>Operatyvinis poveikis

Jei įrašo patvirtinimas atšaukiamas, patvirtinimo įrašas pažymimas kaip **Pateiktas**. Įrašo būsena pakeičiama į **Pateikta**. Šiame etape projekto komandos narys gali atšaukti įrašą nepateikdamas atšaukimo užklausos.

Tvirtintojas gali pakeisti **atsiskaitymo kiekio** ir **atsiskaitymo tipo** vertes, tada dar kartą patvirtinti įrašą.

### <a name="financial-impact"></a>Finansinis poveikis

Jei įrašo patvirtinimas atšaukiamas, atitinkami faktiniai išlaidų ir pardavimų duomenys atnaujinami taip:

- Laukas **Koregavimo būsena** atnaujinamas į **Pakoreguota**.
- Laukas **SF išrašymo būsena** atnaujinamas į **Pakoreguota**.

Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai. Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes. Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės. Vietoj to, šios reikšmės yra atšaukiamos. Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys. Laukas **Koregavimo būsena**, esantis atvirkštinių faktinių duomenų srityje, nustatomas kaip **Nekoreguojamas**, o laukas **SF išrašymo būsena** nustatomas kaip **Atšaukta**. Dėl šių pakeitimų įrašyto neužbaigto projekto išlaidos ir pajamos nebebus įtraukiamos į sumas, kurias atitinka šie faktiniai duomenys.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
