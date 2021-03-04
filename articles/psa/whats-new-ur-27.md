---
title: Kas nauja arba pakeista „Project Service Automation“ V3 27 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 27 atnaujintame leidime.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 01/12/2021
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
ms.openlocfilehash: 6b9da3ec54ec10408774945d26db9e702c858d05
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146673"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 27 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 27 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V3.10.45.98 ir ją galima pasiekti per 2021 m. sausio mėn. automatinį naujinimą.

## <a name="update-release-27"></a>27 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Bendra**

Buvo pataisytos šios problemos:

- Žurnalai, kuriuos sugeneravo „Project Service Automation“ priedai, nebuvo nustatyti automatiniam panaikinimui.
- Automatinis naujinimas nepavyksta, nes „Project Service Automation“ sprendime yra senstelėjusios įrangos nulinės NavBarArea ir pavadinimo elementas.

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- Tinklelyje **Laiko įrašas** rodomi neteisingi duomenys, skirti **Nepriklauso nuo laiko juostos** datos veikimui.
- Tinklelyje **Laiko įrašas** sukuriamas neteisingas laikas, skirtas **Nepriklauso nuo laiko juostos** datos veikimui.
- Užduočių peržvalga neapsiriboja pasirinktu projektu puslapyje **Redaguoti laiko įrašą**.
- Ne projekto laiko įrašų laiko patvirtinimas užblokuojamas, nes sistema ieško projekto tvirtintojo.
- Teisingi įrašai faktiniuose duomenyse rodo neteisingą klaidos pranešimą.
- Kai užduotyje yra neapibrėžta faktinių išlaidų reikšmė ir atnaujinamos bendrosios projekto sumos, įvyksta ši klaida: „Raktas nėra žodyne“.
- Konkrečiais atvejais **Grupuoti pagal** filtras, esantis skirtuke **Projekto įvertinimas**, nerodo išlaidų įvertinimų.
- **Vasaros laiko** intervalas neteisingas laiko įrašams.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Talpyklų patobulinimai, kurie pagerina našumą, susijusį su puslapio **Projektas** įkėlimu.
- Pasenusi veiklos taisyklė, neleidžianti atlikti projekto užduočių.
- „Microsoft Project“ papildinių kontūrai nepaiso priedo kalendoriaus, todėl išteklių reikalavimai neteisingi.
- Projektų kūrimas iš šablonų neteisingai nustato priskyrimo datas ir neleidžia generuoti išteklių reikalavimų.
- Vartotojas, naudodamasis klaviatūra, negali pasiekti parinkčių **Kategorija**, **Aprašas** ir **Būsena**.
- Į faktines projekto pardavimo vertes neįtraukiamos mokesčių ir medžiagų pardavimo vertės.
- Fiksuotas faktinių pardavimo ir faktinių išlaidų agregavimas įvyksta neteisingai naudojant kitokius valiutos kursus.
- **Numatytojo darbo valandų šablono** aprašas yra klaidinantis.
- Užduoties įtrauka nepašalina kategorijos **Kategorija** vartotojo sąsajoje, kol ji neatsinaujina.
- Trūksta tikrinimo, kad būtų įsitikinta, kad projekto perkėlimas po jo pabaigos datos negalimas.

**„Sales“**

Buvo pataisytos šios problemos:

- Projekto pasiūlymo eilutėje generuojama neapibrėžta nuorodos išimtis, nes **Importuoti iš projekto įvertinimo** matomas nepasirinkus projekto.
- Klaida „Objekto nuoroda nenustatyta į objekto egzempliorių“ įvyksta, kai pasiūlymas uždaromas kaip **Laimėtas**.
- Koregavimo būsena nėra nustatoma atliekant faktinį atšaukimą, atsiejant projektą nuo sutarties eilutės.
- Kai „Dynamics 365 Field Service“ ir „Project Service Automation“ yra įdiegti, parinktys **Užrakinti įkainius** ir **Naudoti dabartinius įkainius** nėra rodomi tuo pačiu metu puslapyje **Sąskaita faktūra**.
- Japonų kalbai yra nesuderinamas vertimas į kitus kalendoriumi pagrįstus puslapius.
- Parinktys **Aktyvuoti** ir **Išjungti** buvo pašalintos iš „Project Service Automation“ objektų **Kainoraščio susiejimas**.
