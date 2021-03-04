---
title: Išteklių rezervavimas ir kaip jis susijęs su užduočių priskyrimais
description: Šioje temoje pateikiama informacija, kaip valdyti įvardytus išteklius, išteklių rezervavimus ir užduočių priskyrimus bei paaiškinama, kaip jie susieti.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/27/2019
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
ms.openlocfilehash: 0e4eea87bfb059a3c0be8ccbd2914a4d6c3cf46b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5149958"
---
# <a name="resource-bookings-and-how-they-relate-to-task-assignments"></a>Išteklių rezervavimas ir kaip jis susijęs su užduočių priskyrimais

[!include [banner](../includes/psa-now-project-operations.md)]

Yra du būdai, kuriais projektų komandoms galima rezervuoti įvardytus išteklius ir priskirti projektų užduotis:

- Išteklius galima rezervuoti tiesiogiai projektui, o tada priskirti projekto užduotims.
- Užduotys gali būti priskirtos bendriesiems ištekliams, kurie po to naudojami siekiant rasti ir pakeisti bendruosius išteklius įvardytais ištekliais. 

Tiek vienu, tiek kitu atveju išteklių rezervavimo metu rezervuojamas išteklių pajėgumas.

Projektą planuojančiam projekto vadovui priklauso projekto planas ir grafikas. Projektų vadovas, priskyrimui naudodamas bendruosius išteklius ir iš jų generuodamas išteklių reikalavimą, gali rezervuoti išteklius projektui, kurio kontūrai nurodyti projekto plane. Jis gali rezervuoti išteklius projektui ir tada priskirti juos užduotims, tačiau neįmanoma sulygiuoti rezervavimo kontūrų su užduočių kontūrais. Rezervavimai neturi įtakos projekto grafikui.

Įsivaizduokite sudėtingą projektą su keliomis persidengiančiomis užduotimis, kur keli to paties tipo ištekliai naudojami vienu metu. Jei ištekliams suteikiamas kontūras, kuris skiriasi nuo jų užduočių kontūrų agregatinės reikšmės, tampa sudėtinga modifikuoti užduotis taip, kad jos atitiktų rezervavimų kontūrus jų atskirų užduočių ir originalių kontūrų atžvilgiu.

Pateiktame pavyzdyje bendras tiems patiems ištekliams iš keturių užduočių rinkinio reikalingas pastangų kiekis yra 62 valandos dviejų savaičių laikotarpiui, be to, čia yra konkretus kontūras. Jei ištekliai, vadinami Bobu, tame pačiame dviejų savaičių laikotarpyje yra rezervuoti 62 valandoms, tačiau naudojant kitą kontūrą, reikalavimas ir rezervavimai dera.

| **Užduoties kontūrai**    | **Bendras valandų skaičius** | Pr 6/4 | An 6/5 | Tr 6/6 | Kt 6/7 | Pn 6/8 | Št 6/9 | Sk 6/10 | Pr 6/11 | An 6/12 | Tr 6/13 | Kt 6/14 | Pn 6/15 |
|----------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| 1 užduotis               | 24              | 8      | 8      | 4      |        |        |        |         |         |         | 4       |         |         |
| 2 užduotis               | 16              |        |        | 4      | 4      |        |        |         | 8       |         |         |         |         |
| 3 užduotis               | 10              |        |        |        |        | 4      |        |         |         | 4       |         | 2       |         |
| 4 užduotis               | 12              |        |        |        |        |        |        |         |         |         | 4       |         | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |         |         |
| **Iš viso**           | 62              | 8      | 8      | 8      | 4      | 4      |        |         | 8       | 4       | 8       | 2       | 8       |
|                      |                 |        |        |        |        |        |        |         |         |         |         |

### <a name="bobs-availability"></a>Bobo prieinamumas
| **Išteklių rezervavimas** | **Bendras valandų skaičius** | Pr 6/4 | An 6/5 | Tr 6/6 | Kt 6/7 | Pn 6/8 | Št 6/9 | Sk 6/10 | Pr 6/11 | An 6/12 | Tr 6/13 | Kt 6/14 | Pn 6/15 |
|------------------------|-----------------|--------|--------|--------|--------|--------|--------|---------|---------|---------|---------|---------|---------|
| Bobas                    | 62              | 4      | 4      | 8      | 8      | 8      |        |         | 4       | 4       | 8       | 8       | 6       |

Vis dėlto, nėra jokio sistemingo būdo rezervuotų valandų kontūrą priskirti užduotims kiekvienos dienos pagrindu. Jei projekto vadovas ketina pakeisti projekto grafiką tam, kad būtų pasiekiami ištekliai, priskyrimas turėtų būti pašalintas ir peržiūrėtos visos užduotys, siekiant atitikti rezervavimo kontūrus.

Jeigu organizacija suteikė projekto planavimo užduotį tiek projekto vadovui, tiek resursų vadovui, projekto vadovas nustato grafiką, o į tą yra įtrauktas ir reikiamo darbo kontūrų sudarymas. Išteklių vadovui neturėtų būti suteikiama galimybė keisti grafiką (rezervuojant tikrus išteklius keisti pastangų kontūrus) be projekto vadovo žinios. Jei išteklių vadovas atlieka kažką kitą, o ne tai, ką prašė projektų vadovas, jie turi susitarti, kas turi būti pakeista projekto grafike.

Kadangi rezervavimai ir priskyrimai nėra artimai susieti, galima rezervuoti kontūrus, kurie skiriasi nuo užduoties kontūrų, arba pakeisti priskyrimus taip, kad rezervavimai ir priskyrimai nelygiuotų.

Skirtuke **„Derinimo rodinys“** projektų vadovas gali matyti, kokie yra kiekvieno projekto komandos nario rezervavimai ir priskyrimai. Naudojant spalvas ir paryškinimus rodinyje parodoma, kur neatitinka komandos narių rezervavimai ir priskyrimai. Remdamasis šia informacija, projekto vadovas gali imtis taisomųjų veiksmų ir arba prailginti išteklių rezervavimą, jei egzistuoja tik priskyrimas be rezervavimo, arba atšaukti rezervuotus, tačiau be priskyrimų esančius išteklius.

> [!NOTE]
> Jei perkelsite užduotį, kurios kontūrus sudarėte patys, šie kontūrai nebus išlaikyti. Kontūrai yra generuojami iš naujo pagal projekto kalendorių, siekiant atsižvelgti į darbo valandų ir atostogų pokyčius Toks procesas yra numatytas, nes sistema nežino, koks yra originalaus kontūro tikslas, ir negali nuspręsti ar yra pagrindo jį išlaikyti naujame laikotarpyje. Kadangi rezervavimai ir priskyrimai nėra prijungti, rezervavimuose išlaikomi originalūs rezervavimo kontūrai. Tokiu atveju jums reikia atšaukti ir iš rezervuoti naują priskyrimo kontūrą.

