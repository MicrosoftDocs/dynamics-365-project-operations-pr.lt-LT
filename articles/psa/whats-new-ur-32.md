---
title: Kas nauja arba pakeista „Project Service Automation“ V3 32 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 32 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 06/01/2021
ms.topic: article
ms.author: ruhercul
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
ms.openlocfilehash: 3ad87eceb90a48997aadf00803b8d14c5108eb83
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580098"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-32-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 32 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 32 atnaujintame leidime. Šios versijos komponavimo numeris yra V3.10.53.108; ji visuotinai pasiekiama naudojant 2021 m. birželio mėn. savarankišką naujinimą.

## <a name="update-release-32"></a>32 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

#### <a name="general"></a>Bendroji informacija

- Kai nepavyksta atlikti didelio atnaujinimo, siekiant užtikrinti, kad bendrinami objektai vis dar būtų pasiekiami, turėtų būti užblokuojami tik pagrindiniai programos įvesties taškai.

#### <a name="time-and-expense"></a>Laikas ir išlaidos

Buvo pataisytos šios problemos:

- **TimeEntriesImportFromResourceAssignment** neišlaiko išteklių priskyrimo dalies pradžios ir pabaigos laikų.
- Kai pasirenkate **Atidaryti įrašą** tinklelyje **Laiko įrašas**, gali būti, kad jums nebus galima pasirinkti kitų formų.
- Kai importuojate priskyrimus į laiko įrašus, kliento kodo užklausa gali sugeneruoti ilgą URL, kuris užklausos neįvykdo.
- Tinklelyje **Laiko įrašas** iš langelio panaikinus reikšmę, tinklelyje įvesties vietos neliks.
- Mygtukas **Atmesti** buvo pašalintas iš modernių patvirtinimų rodinio **Patvirtinimų apdorojimas**.
- Laiko įvesties masinio patvirtinimo stabilumą ir efektyvumą paveikė aklavietė ir netinkamai apdorojami tinkinimai, susiję su objektu **Laiko įvedimo**.

#### <a name="project-planning"></a>Projekto planavimas

- Nulinė nuorodos išimtis sugeneruojama atnaujinus projektą, kuris lauke **Sutartį sudarantis vienetas** turi nulinę reikšmę.
- **Atnaujinti projekto sumas** neteisingai skaičiuojamos likusios projekto išlaidos ir likęs pardavimas.
- Dėl nereikalingo kainodaros skaičiavimo paveikiamas našumas, susijęs su išteklių priskyrimo kontūrų naujinimais.

#### <a name="resource-management"></a>Išteklių valdymas

Toliau nurodyta problema buvo išspręsta.

- Kai rezervuotino išteklių kalendoriaus pajėgumas yra didesnis nei 1, „Project Service Automation“ netinkamai atpažįsta pajėgumą kaip 0 (nulinis). Todėl grafiko rodinyje sukeliamas begalinis ciklas.

#### <a name="sales"></a>Pardavimas

Buvo pataisytos šios problemos:

- Kai sukuriama žurnalo eilutė, kurios operacijos tipas yra pasirinktinis, įvyksta tokia nulinės nuorodos išimtis: *Microsoft.Dynamics.ProjectService.Plugins.JournalLinePlugins.ValidateUnitScheduleAndUnitWithTransactionType(TransactionTypetransactionType, TransactionTypeCode transTypeCodeFromPlugin)*.
- Prieš kopijuodami pasiūlymą į apmokestinamus naujai nukopijuoto pasiūlymo vaidmenis ir kategorijas negalima įtraukti išjungtų vaidmenų ir kategorijų.
- Dokumento data ir apskaitos data nesulygiuojamos su pradžios data, pateikiama sąskaitos faktūros eilutės išsamioje informacijoje, kuri sukuriama tiesiogiai juodraščio sąskaitoje faktūroje.
- Nulinės nuorodos išimtys generuojamos scenarijuose, susijusiuose su vaidmenų ir kategorijų išjungimu prieš kopijuojant pasiūlymą.
- Puslapyje **Projektai** veiksmas **Atnaujinti kainas** nenaujina išlaidų įvertinimų ir medžiagų įvertinimų.
