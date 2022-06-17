---
title: Kas nauja arba pakeista „Project Service Automation“ V3 40 atnaujintame leidime
description: Šiame straipsnyje išvardijamos funkcijos ir taisymai, kuriuos galima rasti 40-ajame naujinimo leidime Microsoft Dynamics 365 Project Service Automation, V3.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 01/31/2022
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
ms.openlocfilehash: dca7f340b8d544b183aa0390ac3c11a38f536ed0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912802"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-40-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 40 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardijamos funkcijos ir taisymai, kurie yra nauji arba pakeisti "Project Service Automation Update Release 40" V3. Šios versijos numeris yra V3.10.61.61 ir ji visuotinai pasiekiama įdiegiant savaiminį 2022 m. vasario mėn. naujinimą.

## <a name="update-release-40"></a>40 atnaujintas leidimas

### <a name="features"></a>Funkcijos
1 etapas atnaujinimo iš projekto paslaugų automatizavimo į projekto operacijas - "Lite" bus išleistas 2022 m. Vasario mėn. Norėdami patikrinti tinkamumą, žr [...](upgrade-project-operations-non-stocked.md). Jei taikomoji programa nerodoma jūsų egzemplioriuje Administravimo centre, susisiekite su palaikymo Power Platform tarnyba ir paprašykite, kad skrydis būtų įgalintas jūsų aplinkoje. Jūsų prašyme turi būti pateiktas aplinkos ID, kuriuose turi būti įjungtas skrydis, sąrašas.

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Laikas ir išlaidos**
- Pastabos įrašo trūksta, kai laiko įrašas atmetamas arba atšaukiamas. 

**Pardavimas**

- Kai atnaujinate išlaidų arba pardavimų įvertinimus naudodami "out-of-the-box" papildinius, jums neteisingai leidžiama siųsti JSON naudingąsias apkrovas, kurios negalioja už vartotojo sąsajos ribų.
- Kai atnaujinate pasiūlymo eilutes naudodami spartųjį rodinį, jums leidžiama aktyvinti pasiūlymus.
