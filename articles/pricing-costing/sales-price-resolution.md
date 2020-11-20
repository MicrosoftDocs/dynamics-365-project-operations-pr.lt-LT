---
title: Įvertintų ir faktinių pardavimo kainų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti įvertintus ir faktinius pardavimo tarifus.
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8c18dd734312b2dd147381169f5c3dc38a68a601
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119563"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Įvertintų ir faktinių pardavimo kainų nustatymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai įvertintos ir faktinės pardavimo kainos resolved „Dynamics 365 Project Operations“, sistema pirmiausia naudoja susijusio projekto pasiūlymo arba sutarties datą ir valiutą, kad būtų resolve pardavimo kainoraštis. Resolved pardavimo kainoraštį, sistema resolves pardavimo arba sąskaitų tarifą.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a>Pardavimo tarifų faktinėse ir įvertinimo eilutėse (skirta laikui) resolve

Naudojant „Project Operations“ laiko įvertinimo eilutės naudojamos norint nurodyti pasiūlymo eilutės ir sutarties eilutės laiko duomenis bei projekto išteklių priskyrimą.

Kai pardavimo kainoraštis resolved, sistema atlieka toliau nurodytus veiksmus, kad nustatytų numatytąjį sąskaitų tarifą.

1. Sistema naudoja laiko įvertinimo eilutės laukus **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas**, kad sugretintų su vaidmens kainų eilutėmis sudarytame kainoraštyje. Šiame gretinime laikoma, kad naudojamos paruoštos sąskaitų tarifų kainodaros dimensijos. Jei kainodarą sukonfigūravote remdamiesi bet kuriais kitais laukais vietoj arba greta laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas**, tada toks derinys bus naudojamas gretinimo vaidmens kainos eilutei gauti.
2. Jei sistema suranda vaidmens kainos eilutę, kurios laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas** derinys turi sąskaitos tarifą, tas sąskaitos tarifas bus numatytasis.
3. Jei sistema negali sugretinti laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas**, tada ji nuskaito vaidmens kainų eilutes su atitinkamu vaidmeniu, bet **Išteklių paskirstymo vieneto** reikšmės lieka neapibrėžtos. Kai sistema ras atitinkamą vaidmens kainos įrašą, ji remdamasi įrašu nustatys numatytąjį sąskaitos tarifą. Šiame gretinime laikoma, kad paruošta santykinio **Vaidmens** ir **Išteklių paskirstymo vieneto** pirmumo konfigūracija, yra pardavimo kainodaros dimensija.

> [!NOTE]
> Jei sukonfigūravote kitokį **Vaidmens**, **Išteklių paskirstymo įmonės** ir **Išteklių paskirstymo vieneto** pirmumą arba jei turite kitokių didesnio prioriteto dimensijų, toks veikimas atitinkamai pasikeis. Sistema nuskaito vaidmens kainų įrašus su atitinkamomis kiekvienos kainodaros dimensijos vertėmis pirmumo tvarka: eilutės su neapibrėžtomis tų dimensijų vertėmis pateikiamos paskutinės.

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Pardavimo tarifų faktinėse ir įvertinimo eilutėse (skirta išlaidoms) sudarymas

Naudojant „Project Operations“ išlaidų įvertinimo eilutės naudojamos norint nurodyti pasiūlymo eilutės ir sutarties eilutės išlaidų duomenis bei projekto išlaidų įvertinimo eilutes.

Kai sudaromas pardavimo kainoraštis, sistema atlieka toliau nurodytus veiksmus, kad nustatytų numatytąją vieneto pardavimo kainą.

1. Sistema išlaidų įvertinimo eilutėje naudoja laukų **Kategorija** ir **Vienetas** derinį, kad sugretintų su kategorijų kainų eilutėmis sudarytame kainoraštyje.
2. Jei sistema suranda kategorijos kainos eilutę, kurios laukų **Kategorija** ir **Vienetas** derinys turi pardavimo tarifą, tas pardavimo tarifas bus numatytasis.
3. Jei sistema randa atitinkamos kategorijos kainų eilutę, kainodaros metodą galima naudoti numatytajai pardavimo kainai nustatyti. Toliau pateiktoje lentelėje parodytas išlaidų kainos numatytasis veikimas naudojant „Project Operations“.

    | Kontekstas | Kainodaros metodas | Numatytoji kaina |
    | --- | --- | --- |
    | Numatoma | Vieneto kaina | Remiantis kategorijų kainų eilute |
    | &nbsp; | Savikaina | 0.00 |
    | &nbsp; | Antkainis prie savikainos | 0.00 |
    | Faktinis | Vieneto kaina | Remiantis kategorijų kainų eilute |
    | &nbsp; | Savikaina | Remiantis susijusia faktine savikaina |
    | &nbsp; | Antkainis prie savikainos | Pritaikydami antkainį, kaip apibrėžta susijusios faktinės savikainos vieneto savikainos tarifo kategorijų kainų eilutėje |

4. Jei sistema negali sugretinti laukų **Kategorija** ir **Vienetas** reikšmių, nustatomas numatytasis nulinis (0) pardavimo tarifas.