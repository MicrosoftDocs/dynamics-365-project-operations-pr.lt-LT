---
title: Kas nauja arba pakeista „Project Service Automation“ V3 16 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 16 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/18/2020
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
ms.openlocfilehash: 2c93d34b61001b7755d426539ac384641a7bc9da
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4121588"
---
# <a name="project-service-automation-update-release-16-v3"></a>„Project Service Automation“ V3 16 naujinimo leidimas

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų.  Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas ir naujinimas](https://docs.microsoft.com/dynamics365/project-service/upgrade-psa-home-page).
Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 16 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V3.10.6.34 ir ją galima pasiekti per 2020 m. sausio mėn. automatinį naujinimą.


## <a name="update-release-16"></a>16 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

-   Laikas ir išlaidos

    -   Ištaisyta: vartotojai, norintys pateikti panaikintus laiko ir išlaidų įrašus patvirtinimui, dabar gaus susijusius klaidų pranešimus.

-   Projektų valdymas

    -   Ištaisyta: į išteklių paskirstymo vienetus, apibrėžtus komandos nariams šablonuose, atsižvelgiama, kai šablonai taikomi naujam projektui.

    -   Ištaisyta: pagerintas įrašo nuosavybės pakartotinio priskyrimo tvarkymas.

    -   Ištaisyta: projektų, kurie yra kopijuojami, nebus galima nukopijuoti, kol nebaigtas kopijavimo procesas.

-   Išteklių valdymas

    -   Ištaisyta: naudojant funkciją „Išplėsti rezervavimus“ dabar trumpi periodai tvarkomi tinkamai ir išplėstiniuose rezervavimuose nebekuriamos nulinės valandos.

    -   Ištaisyta: suderinimo rodinys dabar pateikiamas, kai projekto laiko juosta yra +5:30 GMT, o vartojo laiko juosta yra kita.

-   Sales

    -   Ištaisyta: kai projektas, susietas su sutarties eilute, buvo pašalinamas ir susiejamas naujas projektas, naujo projekto faktiniai įrašai nebuvo iš naujo įvertinti pagal apmokėjimo ir kainodaros taisykles, apibrėžtas sutarties eilutėje. Ši klaida ištaisyta šiame leidime. Kainodaros ir faktiniai įrašai naujai susietame projekte bus anuliuoti ir iš naujo tinkamai sukurti pagal sutarties eilutės kainodaros ir apmokėjimo taisykles. Nesusieto projekto faktiniai įrašai taip pat bus iš naujo įvertinti ir dėl to perkurti.

    -   Ištaisyta: įtrauktas papildomas tikrinimas į sąmatos eilutės lauką **Suma** siekiant užtikrinti, kad neliktų nulinių reikšmių.

    -   Ištaisyta: į projekto pagrindinę formą įtrauktas atnaujinimo mygtukas, kad, kai atnaujinami projekto faktiniai duomenys, vartotojas juos galėtų iš naujo sinchronizuoti.

    -   Ištaisyta: kai vartotojai 2.X versiją atnaujina į 3X versiją, projektai su NULINE reikšme pavadinime bus leidžiami.
