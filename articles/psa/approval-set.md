---
title: „Project Service Automation“ patvirtinimo rinkiniai
description: Šiame straipsnyje pateikiama informacija apie patvirtinimo rinkinį, užklausas ir šių operacijų antrinius rinkinius.
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 568815967b909d2a5ee9bf40b4fee97e0ad4d295
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927062"
---
# <a name="approval-sets-in-project-service-automation"></a>„Project Service Automation“ patvirtinimo rinkiniai

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Patvirtinimo grupės patvirtinimo užklausos nustatomos pagal mažesnius operacijų antrinius rinkinius. Šis grupavimas leidžia apdoroti patvirtinimus pagal projektą ir leidžia pakartotinai bandyti bei nustatyti eiliškumą. Grupavimas pagerina didžiulių patvirtinimo kiekių patvirtinimo proceso patikimumą ir atsekamumą.

Patvirtinimo rinkiniuose nurodoma bendra su jais susijusių įrašų apdorojimo būsena. Kai patvirtinimo įrašas apdorojamas naudojant patvirtinimo rinkinį, įrašas perkeliamas iš **Pateikta** į **Patvirtinta** ir atsiejamas nuo patvirtinimo rinkinio. Jei pateikti patvirtinti įrašą nepavyksta, įrašo būsena lieka **Pateikta**, o rinkinys pažymimas kaip nepavykęs. Patvirtinimo rinkinys registruoja klaidos pranešimą apie triktį.

## <a name="processing-approvals-and-approval-sets"></a>Patvirtinimų ir patvirtinimo rinkinių apdorojimas
Į eilę įtraukti apdorojimo patvirtinimai matomi rodinyje **Apdorojimo patvirtinimai**. Sistema bando apdoroti visus įrašus kelis kartus asinchroniškai, įskaitant pakartotinius bandymus patvirtinti, jei ankstesni bandymų nepavyko.

Lauke **Patvirtinimo rinkinio galiojimo laikas** įrašomas bandymų apdoroti rinkinį skaičius, tik tada pažymimas kaip nepavykęs.

## <a name="failed-approvals-and-approval-sets"></a>Patvirtinimų ir patvirtinimo rinkinių pažymėjimas kaip nepavykusių
Rodinyje **Nepavykę patvirtinimai** išvardyti visi patvirtinimai, kuriems reikia vartotojo įsikišimo. Atidarykite susijusių patvirtinimo rinkinių žurnalus, kad būtų galima nustatyti nesėkmės priežastį.
Jei pažymėsite **Bandyti dar kartą**, bus pridedamas patvirtinimo rinkinio laiko skaičiavimas, patvirtinimo rinkinys vėl nustatomas į būseną **Apdorojama** ir bandoma apdoroti likusius įrašus.

## <a name="configure-approval-sets"></a>Patvirtinimo rinkinių konfigūravimas

###  <a name="enable-the-approval-sets-feature"></a>Įjungti patvirtinimo rinkinių funkciją
Prieš įjungdami patvirtinimo rinkinių funkciją patikrinkite, ar šiuo metu nėra apdorojamų patvirtinimų.

- Eikite į puslapį **Projekto parametrai** ir pasirinkite **Funkcijų valdymas** > **Įjungti modernius patvirtinimus**.

### <a name="turn-off-the-approval-sets-feature"></a>Išjungti patvirtinimo rinkinių funkciją
Prieš išjungdami patvirtinimo rinkinių funkciją patikrinkite, ar šiuo metu nėra apdorojamų patvirtinimų.

- Eikite į puslapį **Projekto parametrai** ir pasirinkite **Funkcijų valdymas** > **Išjungti modernius patvirtinimus**.

### <a name="configuring-the-asynchronous-threshold"></a>Asinchroninės ribinės vertės konfigūravimas 
Kai sukuriami patvirtinimo rinkiniai, apdorojimas pereina į foną, kai pažymėtas patvirtinti įrašų skaičius viršija nurodytą ribinę vertę. Naudokite lauką **Asinchroninė ribinė reikšmė** ir konfigūruokite, kada patvirtinimo apdorojimas turėtų būti vykdomas sinchroniškai arba asinchroniškai.
Tinkamos vertės:

  - Nulinė: visos užklausos turi būti apdorojamos asinchroniškai. 
  - Skaičiai, didesni nei nulis: patvirtinimai asinchroniškai apdorojami tik tada, kai pateiktas patvirtinimų skaičius viršija šią reikšmę.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
