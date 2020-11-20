---
title: Projekto parametrai
description: Šioje temoje pateikta informacija apie projektų valdymo parametrus.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123118"
---
# <a name="project-settings"></a>Projekto parametrai

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Norėdami pasiekti projekto planavimo funkcijas, naudokite šiuos parametrus.

## <a name="work-template"></a>Darbo šablonas

Norėdami sukurti projekto grafiką, sukuriate projekto kalendoriaus šabloną, nurodydami dienos darbo valandų skaičių ir kada įmonės nedirba. Norėdami sukurti projekto kalendoriaus šabloną, susiejate darbo šabloną su projekto **Kalendoriaus šablonas** lauku. Norėdami sukurti darbo šabloną, atlikite šiuos veiksmus.

1. Naudodamiesi PSA, kairiojoje naršymo srityje spustelėkite **Ištekliai**. 
2. Sąrašo puslapyje **Ištekliai** atidarykite vartotojo įrašą, tada pažymėkite **Rodyti darbo valandas**.

  > [!NOTE]
  > Įsitikinkite, kad naršyklėje leidžiami iššokantieji langai. Taip galėsite matyti ištekliui nustatytas darbo valandas.
  
3. Skirtuke **Mėnesio rodinys** spustelėkite **Nustatyti**. Bus rodomas trijų parinkčių sąrašas: 

  - Naujas savaitės grafikas
  - Vienos dienos darbo grafikas
  - Laisvas laikas

> ![Nustatymų parinktys](media/project-13.png)

4. Pažymėkite **Naujas savaitės grafikas** ir nustatykite šio išteklių grafiko parinktis. Galite nustatyti pasikartojantį savaitinį grafiką, dienos darbo valandų parametrus, įmonės ne darbo laiką ir kt.
5. Nustatykite datų intervalą pasirinkdami **Įrašyti**, tada spustelėkite **Uždaryti**. 
6. Grįžkite į sąrašo puslapį **Ištekliai** ir pažymėkite išteklių, kuriam nustatėte darbo valandas. 
7. Pažymėkite **Nustatyti kalendorių kaip** nustatyti darbo šabloną. 
8. Dialogo lange **Darbo šablonas** įveskite darbo šablono pavadinimą, tada pasirinkite **Taikyti**. 

Dabar galite susieti darbo šabloną su projekto kalendoriaus šablonu.

## <a name="resource-roles"></a>Išteklių vaidmenys

Terminas „*išteklių vaidmuo*“ nurodo įgūdžių, kompetencijų ir sertifikavimo rinkinį, kurį asmuo turi turėti, kad atliktų tam tikrą projekto užduočių rinkinį. PSA leidžia nustatyti savikainą ir išrašyti sąskaitą pagal ištekliaus laiką, pagrįstą ištekliaus vaidmeniu, su kuriuo jis susietas. Visos organizacijos turi nustatyti šiuos vaidmenis naudodami kairiąją naršymo juostą meniu **Project Service**.

Kiekviena organizacija turi nustatyti šiuos vaidmenis puslapyje **Aktyvių išteklių kategorijos**. Norėdami atidaryti šį puslapį, kairiojoje naršymo srityje pažymėkite **Išteklių vaidmenys**.

## <a name="price-lists"></a>Kainoraščiai

Kainoraščiais galima nustatyti išteklių vaidmenų, išlaidų kategorijų, produktų ir kitų organizacijos elementų savikainą ir pardavimo kainas. Norėdami sukurti finansines sąmatas už darbą, kuris bus atliekamas vykdant projektą, įsitikinkite, kad yra sudarytas atsarginis savikainos ir pardavimo kainoraštis. Parametrų skyriuje taip pat turite nustatyti numatytąją savikainos ir pardavimo kainoraštį, taikomą visiems organizacijoje sukurtiems projektams. Puslapyje **Aktyvieji projekto parametrai** įsitikinkite, kad nustatėte numatytąjį savikainos ir pardavimo kainoraštį.