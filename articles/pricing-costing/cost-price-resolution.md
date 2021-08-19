---
title: Įvertintų ir faktinių savikainų aprašymas
description: Šioje temoje pateikta informacija apie įvertintų ir faktinių savikainų aprašymą.
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f9a6c3236c1d523a967155d3f1fdbe05aa00001bcc36b38afd86270c4cd1d7cc
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003691"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Įvertintų ir faktinių savikainų aprašymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norėdama nustatyti išlaidų kainas ir įvertintų bei faktinių savikainų kainoraštį, sistema naudoja susijusio projekto laukų **Data**, **Valiuta** ir **Sutarties vienetai** informaciją. Nustačius savikainų kainoraštį, programa nustato savikainos tarifą.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Savikainos tarifų faktinėse ir įvertintose laiko eilutėse nustatymas

Įvertintos laiko eilutės nurodo pasiūlymo ir sutarties eilutės duomenis, skirtus projekto laikui ir ištekliams priskirti.

Kai savikainų kainoraštis aprašomas, sistema naudoja laiko įvertinimo eilutės laukus **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas**, kad sugretintų su vaidmens kainų eilutėmis sudarytame kainoraštyje. Šiame gretinime laikoma, kad naudojamos paruoštos darbo savikainos kainodaros dimensijos. Jei sukonfigūravote, kad sistema atitiktų laukus vietoj arba greta laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas**, tada kitoks derinys bus naudojamas gretinimo vaidmens kainos eilutei gauti. Jei programa suranda vaidmens kainos eilutę, kurios laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas** derinys turi savikainos tarifą, tai yra numatytasis savikainos tarifas. Jei programa negali tiksliai sugretinti sričių **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas** reikšmių, ji gaus vaidmens kainos eilutes su atitinkančia vaidmens reikšme, tačiau **Išteklių paskirstymo vienetas** ir **Išteklių paskirstymo įmonė** reikšmės bus nulinės. Aptikus atitinkantį vaidmens kainos įrašą su atitinkančia vaidmens kainos reikšme, nuo to įrašo taikomi numatytosios savikainos tarifai. 

> [!NOTE]
> Jei sukonfigūravote kitokį **Vaidmens**, **Išteklių paskirstymo įmonės** ir **Išteklių paskirstymo vieneto** pirmumą arba jei turite kitokių didesnio prioriteto dimensijų, toks veikimas atitinkamai pasikeis. Sistema vaidmens kainos įrašus su reikšmėmis, atitinkančiomis kiekvieną kainodaros dimensijos reikšmę, gauna prioriteto tvarka su eilutėmis, kuriose dimensijoms taikomos nulinės reikšmės, o jos pateikiamos paskutinėje prioriteto tvarkos vietoje.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Savikainos tarifų faktinėse ir įvertintose išlaidų eilutėse nustatymas

Išlaidų įvertintos eilutės nurodo pasiūlymo ir sutarties eilutės išlaidų informaciją ir projekto išlaidų įvertintas eilutes.

Kai savikainų kainoraštis aprašomas, sistema naudoja išlaidų įvertintos eilutės laukus **Kategorija** ir **Vienetas**, kad sugretintų su **kategorijos kainos** eilutėmis sudarytame kainoraštyje. Jei sistema suranda kategorijos kainos eilutę, kurios laukų **Kategorija** ir **Vienetas** derinys turi savikainos tarifą, savikainos tarifas bus numatytasis. Jei sistema nesuderina laukų **Kategorija** ir **Vienetas** reikšmių arba jei ji gali rasti gretinimo kategorijos kainos eilutę, bet kainodaros metodas nėra **Vieneto kaina**, numatytasis savikainos tarifas nustatomas į nulį (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Savikainos nustatymas medžiagos faktinių duomenų ir įvertinimo eilutėse

Medžiagos įvertinimo eilutėse nurodoma išsami medžiagos pasiūlymo ir sutarties eilutės informacija ir pateikiamos projekto medžiagos įvertinimo eilutės.

Nustačius savikainos kainoraštį, sistemoje, medžiagos įvertinimo eilutėje, naudojamas laukų **Produktas** ir **Vienetas** derinys, kad **Kainų sąrašo elementai** eilutes būtų galima sugretinti su nustatytu kainoraščiu. Jei sistema aptinka produkto kainos eilutę, kurioje nurodytas laukų **Produktas** ir **Vienetas** derinio savikainos tarifas, šis savikainos tarifas nustatomas kaip numatytasis. Jei sistemoje sugretinti laukų **Produktas** ir **Vienetas** reikšmių nepavyksta, vieneto savikainai nustatoma numatytoji nulinė reikšmė. Šis numatytosios reikšmės priskyrimas taip pat bus atliekamas radus atitinkančią kainoraščio elemento eilutę, tačiau kainodaros būdui esant pagrįstam standartine savikaina arba dabartine kaina, neapibrėžta produkte.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
