---
title: „Modern Approvals“ naujinimo aspektai
description: Straipsnyje minimi taškai, į kuriuos administratoriai turi atsižvelgti įjungę „Modern Approvals“ funkcijas.
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 44a933c92d4ef8dff40f20200d74c4bbdf8caa76
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931754"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>„Modern Approvals“ naujinimo aspektai 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Kaip 2022 m. balandžio mėn. „Modern Approvals" 1 bangos leidimo dalį, pagal numatytuosius nustatymus įjungiamos šiuolaikinės patvirtinimo funkcijos. Ši funkcija pagerina patvirtinimo logikos patikimumą ir užtikrina, kad galėsite nustatyti priežastį, jei patvirtinimo logika nepavyks.

Kaip šio pakeitimo dalį sudaro projekto patvirtinimų būsenos pakeitimai. Dabar būsena tiesiogiai pereina iš **Pateikta** į **Patvirtinta**. **Laukiama** nebėra patvirtinimo būsena. Norėdami nustatyti, ar laukiama patvirtinimo, patikrinkite, ar patvirtinimas yra patvirtinimo rinkinio dalis, ir peržiūrėkite pridėto patvirtinimo rinkinio būseną.

## <a name="before-you-upgrade"></a>Prieš pradėdami naujinti

Prieš naujdami į „Modern Approvals“ įsitikinkite, kad neturite laukiančių patvirtinimų. Naudojant modernius patvirtinimus, būsena **Laukiama** nėra. Todėl visi patvirtinimai, kurie po atnaujinimo vis dar pažymėti kaip **laukiami**, nebus apdorojami.

## <a name="after-you-upgrade"></a>Po Jūsų naujinimo

Kai atnaujinsite į „Modern Approvals“, administratorius turi patikrinti, ar įjungta debesies eiga, apdorojanti patvirtinimus.

1. Prisijunkite prie [flow.microsoft.com](https://flow.microsoft.com)
2. Viršutiniame dešiniajame puslapio kampe įjunkite aplinką, kurią atnaujinote.
3. Pažymėkite **Sprendimus**, kad būtų išvardyti aplinkoje įdiegti sprendimai.
4. Sprendimų sąraše pasirinkite **Project Operations** ar **Project Service**.
5. Pakeiskite filtrą iš **Visi** į **Debesies srautai**.
6. Patikrinkite, ar srautas **„Project Service“ – projekto patvirtinimo rinkinių planavimas pakartotinai** nustatytas kaip **Įjungta**. Jei eiga dar neįjungta, rinkitės eigą ir tada **Įjungti**.
7. Patikrinkite, ar apdorojama kas penkias minutes, parametrų srityje **Sistemos užduotys** sąrašą **Nustatymo** srityje.

## <a name="short-term-rollback"></a>Trumpo laikotarpio atšaukimas

Jei negalite vykdyti pakeitimų arba susidūrėte su su šia funkcija susijusia problema, laikinai galite grįžti prie pradinės patvirtinimo eigos atlikdami šiuos veiksmus:
1. Prisijunkite prie savo aplinkos ir patikrinkite, ar nėra laukiančių patvirtinimų.
2. Eikite į **Nustatymai** > **Projekto parametrai**.
3. Pasirinkite **Funkcijų valdymas** ir, norėdami **išjungti funkciją,** pasirinkite „Modern Approvals“.

## <a name="removing-the-feature-flag"></a>Funkcijos žymos pašalinimas

2022 m. spalio mėn. „Wave 2“ naujinime, galimybė išjungti šią funkciją bus panaikinta.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
