---
title: Kas nauja arba pakeista „Project Service Automation“ V3 40 atnaujintame leidime
description: Šiame straipsnyje išvardytos funkcijos ir pataisos, įtrauktos į „Microsoft Dynamics 365 Project Service Automation“ V3 40 atnaujintą leidimą.
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

Šiame straipsnyje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 40 atnaujintame leidime. Šios versijos numeris yra V3.10.61.61 ir ji visuotinai pasiekiama įdiegiant savaiminį 2022 m. vasario mėn. naujinimą.

## <a name="update-release-40"></a>40 atnaujintas leidimas

### <a name="features"></a>Funkcijos
Atnaujinimo iš „Project Service Automation" į "Project Operations" 1 etapas – "Lite" bus išleistas visiems klientams 2022 m. vasario mėn. Norėdami patikrinti suderinamumą, žr. [Naujinimas iš „Project Service Automation“ į „Project Operations“ – „Lite“](upgrade-project-operations-non-stocked.md). Jei taikomoji programa administravimo centre nerodoma jūsų Power Platform egzemplioriuje, kreipkitės į klientų aptarnavimo tarnybą ir prašo įgalinti jūsų aplinkose įjungtą skrydžių funkciją. Jūsų užklausoje turi būti aplinkos IDs sąrašas, kuriame reikia įjungti išvykimą.

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Laikas ir išlaidos**
- Atmetus arba atšaukus laiko įrašą, trūksta pastabos įrašo. 

**Pardavimas**

- Kai atnaujinate išlaidas arba pardavimo vertinimus naudodami iš anksto nustatytas papildinys, jums neteisingai leidžiama siųsti JSON payloads, kurie galioja ne vartotojo sąsajoje.
- Kai atnaujinate pasiūlymo eilutes naudodami sparčiąjį rodinį, jums leidžiama aktyvinti pasiūlymus.
