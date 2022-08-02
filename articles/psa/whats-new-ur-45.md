---
title: Kas nauja arba pakeista „Project Service Automation“ V3 45 atnaujintame leidime
description: Šiame straipsnyje išvardijamos funkcijos ir pataisymai, pasiekiami 45 naujinimo leidime Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 07/14/2022
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
ms.openlocfilehash: 98f7c973917d7d6334e6e0aeb15214c538b33143
ms.sourcegitcommit: 36fda4f45ddeb0f81d30bd1e22852727df644754
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/16/2022
ms.locfileid: "9169183"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-45-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 45 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardijamos funkcijos ir pataisos, kurios yra naujos arba pakeistos "Project Service Automation Update" 45 versijos V3 leidime. Šios komponavimo versijos numeris yra V3.10.76.168 ir ji visuotinai pasiekiama naudojant savaimini naujinimą 2022 m. liepos mėn.

## <a name="update-release-45"></a>45 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Pardavimas**

- Vartotojai negali sėkmingai kurti sąskaitų faktūrų po to, kai bando sukurti sąskaitą faktūrą be jokio neįrašyto pardavimo, jei jie taip pat peržiūri tą patį puslapio egzempliorių ir jo neatnaujina.

**Laikas ir išlaidos**

- Įgalinus šiuolaikinius patvirtinimus ir patvirtinus atšauktą projekto patvirtinimą, įrašymo etapas neteisingai atnaujinamas į **Atšaukimo užklausa patvirtinta**.
- Įgalinus šiuolaikinius patvirtinimus ir neaktyvius debesies srautus, patvirtinimo procesas nėra sėkmingas, o naudotojams, pateikusiems arba tvirtinantiems, apie tai nepranešama.
