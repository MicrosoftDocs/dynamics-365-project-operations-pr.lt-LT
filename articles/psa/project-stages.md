---
title: Projektų etapų tipai
description: Šiame straipsnyje pateikiama informacija apie projekto etapus.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 06/19/2020
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
ms.openlocfilehash: 8d772acce152b08c7986739ac557818e6f97d0fe
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919070"
---
# <a name="project-stage-types"></a>Projektų etapų tipai 

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Projekto etapai sukurti atspindėti projekto būseną, kol jis yra vykdomas. Tinkinimą galima naudoti automatiškai atnaujinant etapus su verslo procesų srautais, Power Automate arba priedų plėtiniais.

Toliau nurodyti etapai nustatomi numatytojoje veiklos proceso sekoje:

- Nauja
- Pasiūlymas
- Planas
- Pristatyti
- Užbaigti
- Uždaryti 

## <a name="new"></a>Naujas

Kuriant projektą, projekto etapas nustatomas į **Naujas**. Jei projektas buvo sukurtas pagal šabloną, jis gali turėti grafiką, sąmatą ir komandos duomenis. Kitaip tai tik projekto planas, o likusius komponentus reikia įvesti.

## <a name="quote"></a>Pasiūlymas

Kai projektą susiejate su pasiūlymu ar jį sukuriate iš pasiūlymo, projekto etapas nustatomas į **Pasiūlymas**, taip pat atnaujinamos numatomos pradžios bei pabaigos datos. Kai projektas yra etape **Pasiūlymas**, skirtuke **Pardavimas**, puslapyje **Projekto objektas**, rodoma išsami informacija apie pasiūlymą.

## <a name="plan"></a>Planas

Kai laimite su projektu susietą pasiūlymą ir kai bendravimas išsiplėtoja iki etapo **Sutartis**, projekto etapas atnaujinamas į **Planas**. Kai projektas yra etape **Pasiūlymas**, puslapyje **Projekto objektas** rodoma išsami informacija apie sutartį.

## <a name="deliver"></a>Pristatyti

Kai projekto planas bus baigtas ir esate pasirengę pradėti projektą, projekto vadovas turėtų atnaujinti projekto etapą į **Pristatyti**, kad parodytų, jog projektas pradėtas.

## <a name="complete"></a>Užbaigti 

Kai projekto veikla baigiama, projektų vadovas gali atnaujinti etapą į **Užbaigti**. Atnaujindamas projekto etapą į **Užbaigti**, projekto vadovas nurodo, kad darbai yra visiškai užbaigti, tačiau projektas yra atviras, kad būtų galima įrašyti visus laukiančius laiko arba išlaidų įrašus.

## <a name="close"></a>Uždaryti

Kai visos projekto operacijos įrašytos, projektų vadovas gali atnaujinti etapą **Uždaryti**. Po to, jokių operacijų nebus galima įrašyti, o projektas nustatomas tik skaityti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
