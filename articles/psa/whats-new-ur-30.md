---
title: Kas nauja arba pakeista „Project Service Automation“ V3 30 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra pasiekiami „Project Service Automation“ V3 30 atnaujintame leidime.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 04/01/2021
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
ms.openlocfilehash: 07ca20425d05d1d638d9b2b8c3425562e39dd6627916794d1ad8441f00658459
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986996"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 30 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution.md).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 30 atnaujintame leidime. Šios versijos komponavimo versijos numeris yra V3.10.51.61 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2021 m. balandžio mėn.

## <a name="update-release-30"></a>30 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

**Laikas ir išlaidos**

Buvo pataisytos šios problemos:

- Kuriant ir įrašant laiko įrašą puslapyje **Spartusis kūrimas** įvyksta klaida, jei pašalintas laukas **Vaidmuo**.
- Laiko įvesties filtre pritaikomas netinkamas filtro operatorius.
- Nukopijuoti grafikai automatiškai nerodomi laiko įrašo valdiklyje pasirinkus **Kopijuoti savaitę**.

**Išteklių valdymas**

Buvo pataisytos šios problemos:

- Pratęsus rezervavimą, rodoma neteisinga galutiniam rezervavimui priskirta rezervavimo būsena. Pratęsus rezervavimą, paisoma rezervavimo būsenos, rezervavimo sąrankos metaduomenyse apibrėžtos kaip **Patvirtinta**.
- Nenurodžius tinkamos rezervavimo būsenos, klaidos pranešimas yra neteisingai lokalizuotas.

**Projektų valdymas**

Buvo pataisytos šios problemos:

- Projektų negalima sukurti viena valiuta ir įtraukti susijusių užduočių kita valiuta.

**Pardavimas**

Buvo pataisytos šios problemos:

- Nukopijavus kainoraštį, neatnaujinamos kainos.
- Kai savikainos informacijos srityje pateikta kilmės reikšmė, nepavyksta uždaryti pasiūlymo kaip laimėto.
- Objekte **Projekto užduotis** dalis **Įvertinta savikaina** pervardyta į **Suplanuotos savikainos (bazinės)**.
- Sukūrus sąskaitų faktūrų arba jas panaikinus, sugeneruojama neapibrėžtos nuorodos išimtis.
