---
title: Kas nauja arba pakeista „Project Service Automation“ V3 37 atnaujintame leidime
description: Šioje temoje išvardytos funkcijos ir pataisos, įtrauktos į „Microsoft Dynamics 365 Project Service Automation“ 37 naujinimo leidimo 3 v.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 11/01/2021
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
ms.openlocfilehash: e8696d84aaca019c2e12d852e669df71146484b3
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593484"
---
# <a name="whats-new-or-changed-in-project-service-automation-update-release-37-v3"></a>Kas nauja arba pakeista „Project Service Automation“ V3 37 atnaujintame leidime

[!include [banner](../includes/psa-now-project-operations.md)]

Norime pranešti apie naujausią programos Microsoft Dynamics 365 Project Service Automation naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Ji suderinama su „Dynamics 365 9.x“. Norėdami atnaujinti į šį leidimą, apsilankykite „Dynamics 365 Online“ sprendimų administravimo centro puslapyje ir įdiekite naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos naujos arba pakeistos funkcijos ir pataisos, susijusios su 3 versijos „Project Service Automation“ 37 naujinimo leidimu. Šios versijos komponavimo numeris yra V3.10.58.120 ir ji yra visuotinai pasiekiama naudojant 2021 m. lapkričio mėn. savaiminį atnaujinimą.

## <a name="update-release-37"></a>37 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

Buvo pataisytos tolesnės problemos.

**Laikas ir išlaidos**
- Vartotojai negali panaikinti laiko įrašo išvalydami langelį.
- Rodinyje **Mano nepavykęs patvirtinimas** yra tik tie projekto patvirtinimai, kurių būsena **Pateikta**.

**Projektų valdymas**
- Jei projekto komandos nario pareigų pavadinimo laukas tuščias, vartotojams atidarant projektą „Microsoft” darbalaukio papildinyje pateikiama neapibrėžta nuorodos išimtis.
- Puslapyje **Projekto užduotis** nėra mygtuko **Įrašyti**, todėl vartotojai negali įrašyti užduočių įrašų pakeitimų.
- Vartotojai negali panaikinti projekto, kuriame yra užduotis, susieta su pasiūlymu, kurio būsena yra **Laimėta**.

**Pardavimas**
- Puslapio **Projektas** laukas **Valiuta** yra atnaujintas, kad atitiktų taikomą šablono valiutą.
- Užduočių, turinčių keletą valiutų, savikaina skaičiuojama netinkamai.
