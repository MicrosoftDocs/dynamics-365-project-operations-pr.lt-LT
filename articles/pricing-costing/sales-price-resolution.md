---
title: Įvertintų ir faktinių pardavimo kainų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti įvertintus ir faktinius pardavimo tarifus.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b78d0f970f942513ecb6911d64fcffa629567f93f1a763eef20ca168080e4d02
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986276"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a>Įvertintų ir faktinių pardavimo kainų nustatymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Kai pardavimo kainos pagal vertinimus ir faktinius duomenis išsprendžiamos programoje „Dynamics 365 Project Operations“, sistema iš pradžių naudoja susijusio projekto pasiūlymo ar sutarties datą ir valiutą, kad būtų išspręstas pardavimo kainoraštis. Resolved pardavimo kainoraštį, sistema resolves pardavimo arba sąskaitų tarifą.

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

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-material"></a>Pardavimo kainų nustatymas medžiagos faktinių duomenų ir įvertinimo eilutėse

„Project Operations“ medžiagos įvertinimo eilutės naudojamos norint nurodyti medžiagų pasiūlymo ir sutarties eilutės informaciją bei pateikti medžiagos įvertinimo eilutes projekte.

Kai sudaromas pardavimo kainoraštis, sistema atlieka toliau nurodytus veiksmus, kad nustatytų numatytąją vieneto pardavimo kainą.

1. Sistema medžiagos įvertinimo eilutei naudoja laukų **Produktas** ir **Vienetas** derinį, kad sugretintų kainų sąrašo elemento eilutes nustatytame kainoraštyje.
2. Jei sistema randa kainų sąrašo elemento eilutę, kurioje nurodytos laukų **Produktas** ir **Vienetas** derinio pardavimo kainos, o įkainojimo metodas nustatytas kaip **Valiutos suma**, naudojama kainoraščio eilutėje nurodyta pardavimo kaina.
3. Jei laukų **Produktas** ir **Vienetas** reikšmės nesutampa, pardavimo kainai nustatoma numatytoji nulinė reikšmė.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
