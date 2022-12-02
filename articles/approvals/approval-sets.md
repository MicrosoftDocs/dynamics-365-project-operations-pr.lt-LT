---
title: Patvirtinimo rinkiniai
description: Šiame straipsnyje aiškinama, kaip dirbti su patvirtinimo rinkiniais, užklausomis ir šių operacijų antriniais rinkiniais.
author: stsporen
ms.date: 02/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: ca205073edbce2b399aab3ae273d635c8af96765
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9524927"
---
# <a name="approval-sets"></a>Patvirtinimo rinkiniai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Patvirtinimo grupės patvirtinimo užklausos nustatomos pagal mažesnius operacijų antrinius rinkinius. Naudojant šį grupavimą, patvirtinimus galima apdoroti pagal projektą konkrečia tvarka ir pakartotinai vykdyti bei nustatyti seką. Sugrupavus patvirtinimo užklausas, pagerėja didelio kiekio patvirtinimų patvirtinimo apdorojimo patikimumas ir atsekamumas.

Patvirtinimo rinkiniuose nurodoma bendra su jais susijusių įrašų apdorojimo būsena. Kai patvirtinimo įrašas apdorojamas naudojant patvirtinimo rinkinį, įrašas iš **Pateikta** perkeliamas į **Patvirtinta** ir nebėra susietas su patvirtinimo rinkiniu. Jei pateikti patvirtinti įrašą nepavyksta, įrašo būsena lieka **Pateikta**, o rinkinys pažymimas kaip nepavykęs. Patvirtinimo rinkinys registruoja klaidos pranešimą apie triktį.

## <a name="processing-approvals-and-approval-sets"></a>Patvirtinimų ir patvirtinimo rinkinių apdorojimas
Į eilę įtraukti apdorojimo patvirtinimai matomi rodinyje **Apdorojimo patvirtinimai**. Sistema visus įrašus keletą kartų apdoroja asinchroniškai, taip pat ir patvirtina pakartotinai, jei ankstesni bandymai buvo atlikti nesėkmingai.

Lauke **Patvirtinimo rinkinio galiojimo laikas** įrašomas bandymų apdoroti rinkinį skaičius, tik tada pažymimas kaip nepavykęs.

Patvirtinimo rinkiniai apdorojami naudojant periodinį aktyvinimą, pagrįstą **debesies srautu**, pavadintu **„Project Service“ – projekto patvirtinimo rinkinių planavimas pakartotinai**. Tai galima rasti **sprendime**, pavadintame **Project Operations**. 

Įsitikinkite, kad srautas suaktyvintas, atlikdami toliau nurodytus veiksmus.

1. Administratoriaus teisėmis prisijunkite prie [flow.microsoft.com](https://powerautomate.microsoft.com).
2. Viršutiniame dešiniajame kampe įjunkite aplinką, kurią naudojate dėl „Dynamics 365 Project Operations“.
3. Pažymėkite **Sprendimus**, kad būtų išvardyti aplinkoje įdiegti sprendimai.
4. Sprendimų sąraše pasirinkite **Project Operations**.
5. Pakeiskite filtrą iš **Visi** į **Debesies srautai**.
6. Patikrinkite, ar srautas **„Project Service“ – projekto patvirtinimo rinkinių planavimas pakartotinai** nustatytas kaip **Įjungta**. Jei eiga dar neįjungta, rinkitės eigą ir tada **Įjungti**.
7. Patikrinkite, ar apdorojama kas penkias minutes, peržiūrėdami **sistemos užduočių** sąrašą srityje **Parametrai**, esančioje „Project Operations“ „Dataverse“ aplinkoje.

## <a name="failed-approvals-and-approval-sets"></a>Patvirtinimų ir patvirtinimo rinkinių pažymėjimas kaip nepavykusių
Rodinyje **Nesėkmingai atlikti patvirtinimai** pateikiami visi patvirtinimai, kuriems reikalingas vartotojo įsikišimas. Atidarykite susijusių patvirtinimo rinkinių žurnalus, kad būtų galima nustatyti nesėkmės priežastį.
Jei pažymėsite **Bandyti dar kartą**, bus pridedamas patvirtinimo rinkinio laiko skaičiavimas, patvirtinimo rinkinys vėl nustatomas į būseną **Apdorojama** ir bandoma apdoroti likusius įrašus.

## <a name="configure-approval-sets"></a>Patvirtinimo rinkinių konfigūravimas

### <a name="enable-the-approval-sets-feature"></a>Įjungti patvirtinimo rinkinių funkciją
Prieš įjungdami patvirtinimo rinkinių funkciją patikrinkite, ar šiuo metu nėra apdorojamų patvirtinimų. Įjungus šią funkciją, jos išjungti negalima.

- Eikite į puslapį **Projekto parametrai** ir pasirinkite **Funkcijų valdymas** > **Įjungti modernius patvirtinimus**.

### <a name="configuring-the-asynchronous-threshold"></a>Asinchroninės ribinės vertės konfigūravimas 
Kai sukuriami patvirtinimo rinkiniai, apdorojimas pereina į foną, kai pažymėtas patvirtinti įrašų skaičius viršija nurodytą ribinę vertę. Naudokite lauką **Asinchroninė ribinė reikšmė** ir konfigūruokite, kada patvirtinimo apdorojimas turėtų būti vykdomas sinchroniškai arba asinchroniškai. Pažymėkite vieną iš šių reikšmių:

  - Nulinė: visos užklausos turi būti apdorojamos asinchroniškai. 
  - Skaičiai, didesni nei nulis: patvirtinimai asinchroniškai apdorojami tik tada, kai pateiktas patvirtinimų skaičius viršija šią reikšmę.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
