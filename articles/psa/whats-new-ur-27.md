---
title: Kas nauja arba pakeista „Project Service Automation“ V3 27 atnaujintame leidime
description: Šiame straipsnyje išvardijamos funkcijos ir taisymai, kuriuos galima rasti "Project Service Automation Update Release 27", V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 6c8f4f736f0659f9b6db25f4685ef1278c45d034
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912940"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-27-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 27 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardijamos naujos arba pakeistos "Project Service Automation V3", "Update Release 27" funkcijos ir taisymai. Ši versija turi naują komponavimo versijos numerį V3.10.45.98 ir ją galima pasiekti per 2021 m. sausio mėn. automatinį naujinimą.

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


[!INCLUDE[footer-include](../includes/footer-banner.md)]
