---
title: Kas nauja arba pakeista „Project Service Automation“ V3 25 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 25 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 10/26/2020
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
ms.openlocfilehash: a5a81893c4a804deb09cf33e0ac3f1a25b8bca36
ms.sourcegitcommit: a2b810219d381716d3eedb14c4eb6cdefb5b5845
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/02/2020
ms.locfileid: "4183553"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 25 atnaujintame leidime

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos naujos ar pakeistos „Project Service Automation“ V3, atnaujinto 25 leidimo funkcijos ir taisymai. Šios komponavimo versijos numeris yra V 3.10.43.76 ir ji yra visuotinai pasiekiama 2020 m. spalio mėn. savaiminiame naujinime.

## <a name="update-release-25"></a>25 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Toliau nurodyta problema buvo išspręsta.

- Laiko įrašo diagrama, kurioje rodomi papildomi duomenys, pagrįsti per dideliu nuskaitomu intervalu.

**Išteklių valdymas**

Toliau nurodyta problema buvo išspręsta.

- Pridėtas „Package Deployer” kodas, skirtas praleisti „Universal Resource Scheduling” pataisos importavimą, jei jau yra naujesnės versijos pataisa.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Ištaisyti apvalinimo ir valiutos kurso nesutapimai, lemiantys netinkamą planuojamą savikainą projekto sekimo tinklelyje.
- Palaikoma galimybė rodyti du ar daugiau reagavimo tinklelių formoje **Projektas**.
- Teikiamas tikrinimas, skirtas galimybei priskirti užduotį praėjus kalendoriaus pabaigos datai, dėl ko nepavykdavo priskirti išteklių.
- Patobulintas klaidų tvarkymas sprendžiant klaidą „Null Reference Exception” generuojamą iš:

    - **PreValidateProjectTeamMemberCreate** priedo
    - **PreValidateProjectTaskCreate**, kai projekto užduotis sukuriama nenaudojant susijusio projekto
    - **PreProjectTeamMemberCreate** priedo
    - **PostProjectTeamMemberDelete** priedo
    - **PreValidateProjectTaskDelete** priedo

**„Sales“**

Buvo pataisytos šios problemos:

- Patobulintas klaidų tvarkymas, sprendžiant klaidą „Null Reference Exceptions”, generuojamą iš **Projekto kopijavimas: įvertinamas HelperResource valdymas**.
- Laukas **Neparengta išrašyti sąskaitos faktūros** dalyje **Laiko ir medžiagų atsiskaitymo nebaigtos užduotys** neišvalo atsiskaitymo būsenos.
- Ištaisytas netinkamai pažymėtas mygtukas **Kainos** skirtukuose **Vaidmens kaina** ir **Katalogo elementai**.
