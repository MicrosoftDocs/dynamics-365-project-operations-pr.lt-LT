---
title: Kas nauja arba pakeista „Project Service Automation“ V3 30 atnaujintame leidime
description: Šiame straipsnyje išvardijamos funkcijos ir taisymai, kuriuos galima rasti "Project Service Automation Update Release 30", V3.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ad00b126a13e18a5de47df335aea06b9690efa13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925084"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-30-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 30 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Malonu pranešti apie naujausią „Dynamics 365“ programos „Project Service Automation“ naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ internetinių sprendimų puslapio administravimo centrą, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardijamos funkcijos ir taisymai, kurie yra nauji arba pakeisti "Project Service Automation V3", "Update Release 30". Šios versijos komponavimo versijos numeris yra V3.10.51.61 ir ji paprastai pasiekiama savaiminiu naujinimu, vykdytu 2021 m. balandžio mėn.

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
