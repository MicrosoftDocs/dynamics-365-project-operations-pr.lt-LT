---
title: Šiuolaikinių patvirtinimų atnaujinimo aspektai
description: Straipsnyje aptariami klausimai, į kuriuos administratoriai turėtų atsižvelgti, kai įjungia šiuolaikinių patvirtinimų funkciją.
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
# <a name="upgrade-considerations-for-modern-approvals"></a>Šiuolaikinių patvirtinimų atnaujinimo aspektai 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Kaip dalis 2022 m. balandžio 1 bangos leidimo, šiuolaikinių patvirtinimų funkcija bus įjungta pagal numatytuosius nustatymus. Ši funkcija pagerina patvirtinimo logikos patikimumą ir užtikrina, kad galite nustatyti priežastį, jei patvirtinimo logika nepavyksta.

Atliekant šį pakeitimą, atnaujinami projekto patvirtinimų būsenos pakeitimai. Dabar būsena eina tiesiai iš **Pateikta** į **Patvirtintą**. **Laukiama** nebėra patvirtinimų būsena. Norėdami nustatyti, ar laukiama patvirtinimo, patikrinkite, ar patvirtinimas yra patvirtinimo rinkinio dalis, ir peržiūrėkite pridėto patvirtinimo rinkinio būseną.

## <a name="before-you-upgrade"></a>Prieš atnaujindami versiją

Prieš atnaujindami versiją į "Modern Approvals", įsitikinkite, kad neturite laukiančių patvirtinimų. Šiuolaikiniai patvirtinimai nenaudoja **būsenos Laukiama**. Todėl visi patvirtinimai, kurie po atnaujinimo vis dar pažymėti kaip **Laukiantys**, nebus apdorojami.

## <a name="after-you-upgrade"></a>Atnaujinus versiją

Atnaujinęs versiją į Šiuolaikiniai patvirtinimai, administratorius turi patvirtinti, kad debesies srautas, apdorojantis patvirtinimus, buvo įgalintas.

1. Prisijungti prie [flow.microsoft.com](https://flow.microsoft.com)
2. Puslapio viršutiniame dešiniajame kampe perjunkite aplinką į atnaujintą aplinką.
3. Pasirinkite **Sprendimai**, kad išvardytumėte aplinkoje įdiegtus sprendimus.
4. Sprendimų sąraše pasirinkite **"Project Operations** " arba **"Project Service**".
5. Pakeiskite filtrą iš **Visi** į **Debesies srautus**.
6. Patikrinkite, ar parinktis **Projekto tarnyba – periodiškai planuoti projekto patvirtinimo rinkinius** nustatyta kaip **Įjungta**. Jei ne, pasirinkite srautą, tada pasirinkite **Įjungti**.
7. Patikrinkite, ar apdorojimas vyksta kas penkias minutes, **peržiūrėdami sistemos užduočių** sąrašą **srityje Parametrai**.

## <a name="short-term-rollback"></a>Trumpalaikis grąžinimas

Jei negalite įsisavinti pakeitimų arba susiduriate su rimta šios funkcijos problema, galite laikinai grįžti prie pradinio patvirtinimo srauto atlikdami šiuos veiksmus:
1. Prisijunkite prie savo aplinkos ir patikrinkite, ar nėra laukiančių patvirtinimų.
2. Eikite į **Parametrų** > **projekto parametrai**.
3. Pasirinkite **Funkcijų valdymas**, tada pasirinkite **Modernūs patvirtinimai**, kad išjungtumėte funkciją.

## <a name="removing-the-feature-flag"></a>Funkcijos vėliavėlės šalinimas

2022 m. spalio mėn.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
