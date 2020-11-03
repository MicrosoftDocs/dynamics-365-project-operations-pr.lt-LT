---
title: Kas nauja arba pakeista „Project Service Automation“ V3 14 atnaujintame leidime
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 14 atnaujintame leidime V3.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom: dyn365-projectservice
ms.date: 01/29/2020
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
ms.openlocfilehash: 00ce5c68b1141c88671f0534f7500bf0d7eebd8e
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080794"
---
# <a name="project-service-automation-update-release-14-v3"></a>„Project Service Automation“ V3 14 naujinimo leidimas
Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 14 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V3.10.4.21 ir ją galima gauti pagal toliau pateiktą grafiką:

- **Bendras prieinamumas (automatinis naujinimas):** 2020 m. sausio mėn.
- **Automatinis naujinimas:** 2020 m. vasario mėn.

## <a name="update-release-14"></a>14 atnaujintas leidimas

### <a name="enhancements"></a>Patobulinimai

- Sales

     - Pasirinktinės lauko reikšmės iš **Pasiūlymo eilutės išsami informacija** kopijuojamos į **Projekto sutarties eilutės išsami informacija** , kai pasiūlymas atnaujinamas į **Uždarytas kaip laimėjęs**.
     - Patvirtinti projektai gali būti **Uždaryti kaip pralaimėję**.

- Išteklių valdymas

     - Išplečiant rezervacijas vartotojai matys patvirtinimo dialogo langelį, kuris paragins apibendrinti rezervavimo rezultatus ir pateikti saitą į Išlaikyti rezervavimus.


### <a name="bug-fixes"></a>Ištaisytos klaidos

- Laikas ir išlaidos

     - Pataisyta: pagerinta vartotojo patirtis, kai jis nepasirinko jokių taisytinų įrašų.

- Išteklių valdymas

     - Sutaisyta: ištekliaus rezervavimas kelis kartus užpildo rezervuojamo ištekliaus pavadinimą.

- Sales

     - Sutaisyta: bendra pardavimo kaina nėra apskaičiuojama, kol vartotojas neįveda išlaidų savikainos, apskaičiuotos projektui.
     - Sutaisyta: uždaryti pasiūlymo kaip **Laimėjęs** nepavyksta, jei susijusio projekto būsena nėra **Juodraštis**.

