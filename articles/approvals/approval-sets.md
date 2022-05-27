---
title: Patvirtinimo rinkiniai
description: Šioje temoje aiškinama, kaip dirbti su patvirtinimo rinkiniais, užklausomis ir šių operacijų antriniais rinkiniais.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 6809e01d8c3c93841125d0100d898dc208577019
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576234"
---
# <a name="approval-sets"></a>Patvirtinimo rinkiniai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Patvirtinimo grupės patvirtinimo užklausos nustatomos pagal mažesnius operacijų antrinius rinkinius. Naudojant šį grupavimą, patvirtinimus galima apdoroti pagal projektą konkrečia tvarka ir pakartotinai vykdyti bei nustatyti seką. Sugrupavus patvirtinimo užklausas, pagerėja didelio kiekio patvirtinimų patvirtinimo apdorojimo patikimumas ir atsekamumas.

Patvirtinimo rinkiniuose nurodoma bendra su jais susijusių įrašų apdorojimo būsena. Kai patvirtinimo įrašas apdorojamas naudojant patvirtinimo rinkinį, įrašas iš **Pateikta** perkeliamas į **Patvirtinta** ir nebėra susietas su patvirtinimo rinkiniu. Jei pateikti patvirtinti įrašą nepavyksta, įrašo būsena lieka **Pateikta**, o rinkinys pažymimas kaip nepavykęs. Patvirtinimo rinkinys registruoja klaidos pranešimą apie triktį.

## <a name="processing-approvals-and-approval-sets"></a>Patvirtinimų ir patvirtinimo rinkinių apdorojimas
Į eilę įtraukti apdorojimo patvirtinimai matomi rodinyje **Apdorojimo patvirtinimai**. Sistema visus įrašus keletą kartų apdoroja asinchroniškai, taip pat ir patvirtina pakartotinai, jei ankstesni bandymai buvo atlikti nesėkmingai.

Lauke **Patvirtinimo rinkinio galiojimo laikas** įrašomas bandymų apdoroti rinkinį skaičius, tik tada pažymimas kaip nepavykęs.

Patvirtinimo rinkiniai apdorojami periodiškai aktyvuojant pagal debesies srautą **, pavadintą** **"Project Service" – periodiškai planuoti projektų patvirtinimo rinkinius**. Tai yra sprendime **,** pavadintame **"Project Operations"**. 

Įsitikinkite, kad srautas suaktyvintas, atlikdami šiuos veiksmus.

1. Kaip administratorius, prisijunkite prie [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Viršutiniame dešiniajame kampe perjunkite aplinką, kurioje naudojate Dynamics 365 Project Operations.
3. Pasirinkite **Sprendimai**, kad išvardytumėte aplinkoje įdiegtus sprendimus.
4. Sprendimų sąraše pasirinkite **Projekto operacijos**.
5. Pakeiskite filtrą iš **Visi** į **Debesies srautus**.
6. Patikrinkite, **ar projekto tarnyba – periodiškai planuoti projekto patvirtinimo rinkinių** srautą nustatyta kaip **Įjungta**. Jei ne, pasirinkite srautą, tada pasirinkite **Įjungti**.
7. Patikrinkite, ar apdorojimas vyksta kas penkias minutes, peržiūrėdami **sistemos užduočių** sąrašą, esantį **"Project Operations**" aplinkos srityje Parametrai Dataverse.

## <a name="failed-approvals-and-approval-sets"></a>Patvirtinimų ir patvirtinimo rinkinių pažymėjimas kaip nepavykusių
Rodinyje **Nesėkmingai atlikti patvirtinimai** pateikiami visi patvirtinimai, kuriems reikalingas vartotojo įsikišimas. Atidarykite susijusių patvirtinimo rinkinių žurnalus, kad būtų galima nustatyti nesėkmės priežastį.
Jei pažymėsite **Bandyti dar kartą**, bus pridedamas patvirtinimo rinkinio laiko skaičiavimas, patvirtinimo rinkinys vėl nustatomas į būseną **Apdorojama** ir bandoma apdoroti likusius įrašus.

## <a name="configure-approval-sets"></a>Patvirtinimo rinkinių konfigūravimas

### <a name="enable-the-approval-sets-feature"></a>Įjungti patvirtinimo rinkinių funkciją
Prieš įjungdami patvirtinimo rinkinių funkciją patikrinkite, ar šiuo metu nėra apdorojamų patvirtinimų.

- Eikite į puslapį **Projekto parametrai** ir pasirinkite **Funkcijų valdymas** > **Įjungti modernius patvirtinimus**.

### <a name="turn-off-the-approval-sets-feature"></a>Išjungti patvirtinimo rinkinių funkciją
Prieš išjungdami patvirtinimo rinkinių funkciją patikrinkite, ar šiuo metu nėra apdorojamų patvirtinimų.

- Eikite į puslapį **Projekto parametrai** ir pasirinkite **Funkcijų valdymas** > **Išjungti modernius patvirtinimus**.

### <a name="configuring-the-asynchronous-threshold"></a>Asinchroninės ribinės vertės konfigūravimas 
Kai sukuriami patvirtinimo rinkiniai, apdorojimas pereina į foną, kai pažymėtas patvirtinti įrašų skaičius viršija nurodytą ribinę vertę. Naudokite lauką **Asinchroninė ribinė reikšmė** ir konfigūruokite, kada patvirtinimo apdorojimas turėtų būti vykdomas sinchroniškai arba asinchroniškai. Pažymėkite vieną iš šių reikšmių:

  - Nulinė: visos užklausos turi būti apdorojamos asinchroniškai. 
  - Skaičiai, didesni nei nulis: patvirtinimai asinchroniškai apdorojami tik tada, kai pateiktas patvirtinimų skaičius viršija šią reikšmę.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
