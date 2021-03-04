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
ms.openlocfilehash: aabee3fe755e33d2c0f01a96b6f53a68957bc041
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143771"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-25-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 25 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]