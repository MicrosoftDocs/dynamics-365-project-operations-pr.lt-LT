---
title: Anksčiau patvirtintų laiko ir išlaidų įrašų atšaukimas
description: Šioje temoje pateikta informacija apie tai, kaip atšaukti anksčiau patvirtintą projekto laiko ir išlaidų operaciją.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/07/2019
ms.topic: article
ms.author: rumant
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
ms.openlocfilehash: 9e3bc94b626b88a2167e3a61472b768e2fb5c731
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590770"
---
# <a name="cancel-previously-approved-time-or-expense-entries"></a>Anksčiau patvirtintų laiko ar išlaidų įrašų atšaukimas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Naudodami naujausią Dynamics 365 Project Service Automation versiją tvirtintojai gali atšaukti laiko arba išlaidų įrašus, kuriuos anksčiau patvirtino.

## <a name="cancel-a-previously-approved-time-or-expense-entry"></a>Anksčiau patvirtinto laiko ar išlaidų įrašų atšaukimas

Norėdami atšaukti laiko ar išlaidų įrašą, kurį anksčiau patvirtinote, atlikite toliau nurodytus veiksmus.

1. Nueikite į **Projektai** \> **Mano darbai** \> **Patvirtinimai**.
2. **Patvirtinimų** sąrašo puslapyje pakeiskite rodinį į **Mano ankstesni patvirtinimai**. Rodomas jūsų anksčiau patvirtintų laiko ir išlaidų įrašų sąrašas.
3. Pasirinkite vieną arba kelis įrašus, tada pasirinkite **Atšaukti patvirtinimą**. Bus pateiktas įspėjimo pranešimas.
4. Norėdami atšaukti patvirtinimą, pasirinkite **Gerai**.

## <a name="understand-the-impact-of-canceling-a-time-or-expense-entry-approval"></a>Poveikio atšaukus laiko arba išlaidų įrašo patvirtinimą išsiaiškinimas

Atšaukus patvirtinimą, patiriamas veiklos ir finansinis poveikis.

### <a name="operational-impact"></a>Veiklos poveikis

Kai patvirtinimas atšaukiamas, veiklos požiūriu įrašo būsena iš naujo nustatoma į **juodraštį**, o patvirtinimas neberodomas rodinyje **Mano ankstesni patvirtinimai**. Vietoj to, atšauktas patvirtinimas rodomas rodinyje **Laiko įrašai, skirti patvirtinti** arba rodinyje **Išlaidų įrašai, skirti patvirtinti**, priklausomai nuo to, ar įrašas buvo laiko, ar išlaidų įrašas. Be to, susijusio laiko arba išlaidų įrašo būsena pakeičiama į **Pateikta**, kad susijęs įrašas atitiktų patvirtinimus, kurių būsena – **Juodraštis**.

Būdami tvirtintoju galite redaguoti kai kuriuos patvirtinimo laukus, kurių būsena – **Juodraštis**. Šie laukai – tai **Atsiskaitymo tipas** ir **Apmokėtinos valandos pagal laiko įrašus**. Atlikę keitimų galite patvirtinti įrašą dar kartą. Taip pat galite atmesti įrašą. Atmetus laiko įrašo patvirtinimą, įrašo būsena pakeičiama į **Grąžinta**. Atmetus išlaidų įrašo patvirtinimą, būsena pakeičiama į **Atmesta**. Funkciniu požiūriu grąžinti ir atmesti įrašai veikia taip pat kaip ir įrašas, kurio būsena – **Juodraštis**. Projekto komandos narys gali atlikti reikiamus įrašo keitimus, tada iš naujo pateikti įrašą patvirtinti arba visiškai jį panaikinti.

### <a name="financial-impact"></a>Finansinis poveikis

Atšaukus patvirtinimą, projektas taip pat paveikiamas finansiškai. Pirmiausia, atitinkami savikainos ir pardavimo faktiniai duomenys atnaujinami taip, kaip nurodyta toliau.

- Koregavimo būsena nustatoma į **Koreguota**.
- Atsiskaitymo būsena nustatoma į **Atšaukta**.

Toliau faktinių duomenų lentelėje sukuriami atšaukimo įrašai. Tam, kad būtų sukurti atšaukimo įrašai, sistema iš pirminių faktinių duomenų nukopijuoja lauko vertes. Vienintelės vertės, kurios nenukopijuojamos, yra kiekio vertės. Vietoj to, šios reikšmės yra atšaukiamos. Sukuriami atšaukti **savikainos** ir **pardavimo, už kurį neišrašyta sąskaita** faktiniai duomenys. Laukui **Koregavimo būsena**, esančiam atvirkštinių faktinių duomenų srityje, nustatoma būsena **Nekoreguojama**, o atsiskaitymo būsenai nustatoma būsena **Atšaukta**.

Atlikus šiuos pakeitimus, suma, kuri įrašoma kaip išleista vykdant projektą, ir nepanaudotos projekto pajamos nebelems sumų, kurias šie faktiniai duomenys iš tikrųjų reiškia.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
