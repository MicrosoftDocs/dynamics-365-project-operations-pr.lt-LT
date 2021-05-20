---
title: Kas nauja arba pakeista „Project Service Automation“ V3 19 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 19 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 05/05/2020
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
ms.openlocfilehash: 0137d0241238ff96de406884dd05a5d7f023c318
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949149"
---
# <a name="project-service-automation-update-release-19-v3"></a>„Project Service Automation“ V3 19 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti PSA V3 19 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V3.10.30.41 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2020 m. gegužės mėn.

## <a name="update-release-19"></a>19 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos: 

- Klaidos, gaunamos importuojant laiko įrašus, rodomos netinkamai.
- Laiko įrašo tinklelis nepalaiko lauko veikimo **Tik data**.
- Projekto ištekliai negali sukurti išlaidų su projektu.

**Projektų valdymas**

Buvo pataisytos šios problemos: 

-  Dėl tretinės užduoties pastangų įvertinimo pabaigoje (EAC) skaičiavimai yra klaidingi.

**„Sales“**

Buvo pataisytos šios problemos: 

- Veiksmas **Perskaičiuoti** neveikia su išlaidų sutarties eilutės išsamia informacija arba pasiūlymo eilutės išsamia informacija.
- Išlaidų įvertinimuose trūksta parinkties **Naujinti kainas**.
-  Klientai negali pasirinkti pasirinktinių sutarties būsenos tipų puslapyje **Projekto sutartis**.
- Klientai kurdami pasirinktinį kainoraštį pagal pasiūlymą susiduria su suprastėjusiu veikimu.
- Klientai susiduria su **vienetų** numatytųjų reikšmių nenuoseklumu puslapiuose **Pasiūlymo eilutės išsami informacija** ir **Sutarties eilutės išsami informacija**.
- Į apmokestinamą sutarties eilutę įtraukus neapmokestinamų operacijų kategorijos elementus, nebus paisomas operacijos kategorijos atsiskaitymo tipas **Neapmokestinama**.
- Klientai negali naudoti naujai įtrauktų vaidmenų ir kategorijos anksčiau sudarytoms sutartims.
- Klientai susiduria su suprastėjusiu veikimu, kai šaltinio kode „PreValidateProjectTeamMemberUpdate.cs” vykdomas nereikalingas grąžinimas
- Vaidmenys, nustatyti kaip neapmokestinami sąraše **Išteklių kategorijos**, projekto sutarties eilutėje turėtų būti įtraukti į skirtuką **Apmokestinami vaidmenys** kaip **Neapmokestinami**.
- Kurdami projektą klientai gali susiduria su prastesniu veikimu, nes **GetBookableResourceIdFromUser** grąžina visus rezervuojamų išteklių stulpelius, o ne tik pirminį ID.
- Objektas **TransactionType** neturi išankstinio tikrinimo naujinimo priedo, kad vartotojai negalėtų įvesti **vienetų** ir **UnitGroups**, netinkančių operacijos tipams.
- Veiksmas **Šalinti** neveikia importuojant laiko įrašą.


[!INCLUDE[footer-include](../includes/footer-banner.md)]