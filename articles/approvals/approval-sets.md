---
title: Patvirtinimo rinkiniai
description: Šioje temoje aiškinama, kaip dirbti su patvirtinimo rinkiniais, užklausomis ir šių operacijų antriniais rinkiniais.
author: stsporen
manager: tfehr
ms.date: 08/10/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 1d9333033eb2b03966c6531d0fd6ad5b878acd93
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323246"
---
# <a name="approval-sets"></a>Patvirtinimo rinkiniai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Patvirtinimo grupės patvirtinimo užklausos nustatomos pagal mažesnius operacijų antrinius rinkinius. Naudojant šį grupavimą, patvirtinimus galima apdoroti pagal projektą konkrečia tvarka ir pakartotinai vykdyti bei nustatyti seką. Sugrupavus patvirtinimo užklausas, pagerėja didelio kiekio patvirtinimų patvirtinimo apdorojimo patikimumas ir atsekamumas.

Patvirtinimo rinkiniuose nurodoma bendra su jais susijusių įrašų apdorojimo būsena. Kai patvirtinimo įrašas apdorojamas naudojant patvirtinimo rinkinį, įrašas iš **Pateikta** perkeliamas į **Patvirtinta** ir nebėra susietas su patvirtinimo rinkiniu. Jei pateikti patvirtinti įrašą nepavyksta, įrašo būsena lieka **Pateikta**, o rinkinys pažymimas kaip nepavykęs. Patvirtinimo rinkinys registruoja klaidos pranešimą apie triktį.

## <a name="processing-approvals-and-approval-sets"></a>Patvirtinimų ir patvirtinimo rinkinių apdorojimas
Į eilę įtraukti apdorojimo patvirtinimai matomi rodinyje **Apdorojimo patvirtinimai**. Sistema visus įrašus keletą kartų apdoroja asinchroniškai, taip pat ir patvirtina pakartotinai, jei ankstesni bandymai buvo atlikti nesėkmingai.

Lauke **Patvirtinimo rinkinio galiojimo laikas** įrašomas bandymų apdoroti rinkinį skaičius, tik tada pažymimas kaip nepavykęs.

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
