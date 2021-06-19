---
title: Projekto įvertinimų ir faktinių duomenų savikainų nustatymas
description: Šioje temoje pateikiama informacija apie tai, kaip nustatomos projekto įvertinimų ir faktinių duomenų savikainos.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6b42bc97251aec7259d314fe51b3a012edf597aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004406"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a>Projekto įvertinimų ir faktinių duomenų savikainų nustatymas 

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Norėdama nustatyti išlaidų kainas ir įvertintų bei faktinių savikainų kainoraštį, sistema naudoja susijusio projekto laukų **Data**, **Valiuta** ir **Sutarties vienetai** informaciją. Nustačius savikainų kainoraštį, programa nustato savikainos tarifą.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Savikainos tarifų faktinėse ir įvertintose laiko eilutėse nustatymas

Įvertintos laiko eilutės nurodo pasiūlymo ir sutarties eilutės duomenis, skirtus projekto laikui ir ištekliams priskirti.

Nustačius savikainų kainoraštį, laukai **Vaidmuo** ir **Išteklių paskirstymo vienetas** laiko įvertinimo eilutėje yra gretinami su vaidmens kainos eilutėmis kainoraštyje. Šis atitikmuo reiškia, kad darbo savikainai naudojate standartinės kainodaros dimensijas. Jei sukonfigūravote, kad sistema atitiktų laukus vietoj arba greta laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas**, tada kitoks derinys bus naudojamas gretinimo vaidmens kainos eilutei gauti. Jei programa suranda vaidmens kainos eilutę, kurios laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** derinys turi savikainos tarifą, tai yra numatytasis savikainos tarifas. Jei programa negali sugretinti laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** reikšmių, tada ji nuskaito vaidmens kainų eilutes su atitinkamu vaidmeniu, bet **Išteklių paskirstymo vieneto** reikšmės lieka neapibrėžtos. Kai jis turi atitinkantį vaidmens kainos įrašą, numatytasis savikainos tarifas nustatomas iš to įrašo. 

> [!NOTE]
> Jei sukonfigūravote kitokį **Vaidmens** ir **Išteklių paskirstymo vieneto** pirmumą arba jei turite kitokių didesnio prioriteto dimensijų, toks veikimas atitinkamai pasikeis. Sistema nuskaito vaidmens kainų įrašus su atitinkamomis kiekvienos kainodaros dimensijos vertėmis pirmumo tvarka: eilutės su neapibrėžtomis tų dimensijų vertėmis pateikiamos paskutinės.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Savikainos tarifų faktinėse ir įvertintose išlaidų eilutėse nustatymas

Išlaidų įvertintos eilutės nurodo pasiūlymo ir sutarties eilutės išlaidų informaciją ir projekto išlaidų įvertintas eilutes.

Nustačius savikainų kainoraštį, sistema naudoja laukų **Kategorija** ir **Vienetas** derinį išlaidų įvertinimo eilutėje, kad būtų atitiktos **Kategorijos kaina** eilutės nustatytame kainoraštyje. Jei sistema suranda kategorijos kainos eilutę, kurios laukų **Kategorija** ir **Vienetas** derinys turi savikainos tarifą, savikainos tarifas bus numatytasis. Jei sistema negali atitikti **Kategorija** ir **Vienetas** reikšmių, arba jei sistema randa sutampančios kategorijos kainos eilutę, tačiau kainodaros būdas nėra **Vieneto kaina**, numatytasis savikainos tarifas bus nulis (0).

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a>Savikainos nustatymas Medžiagos faktinių duomenų ir įvertinimo eilutėse

Medžiagos įvertinimo eilutėse nurodoma išsami medžiagos pasiūlymo ir sutarties eilutės informacija ir pateikiamos projekto medžiagos įvertinimo eilutės.

Nustačius savikainos kainoraštį, sistemoje, medžiagos įvertinimo eilutėje, naudojamas laukų **Produktas** ir **Vienetas** derinys, kad **Kainų sąrašo elementai** eilutes būtų galima sugretinti su nustatytu kainoraščiu. Jei sistema aptinka produkto kainos eilutę, kurioje nurodytas laukų **Produktas** ir **Vienetas** derinio savikainos tarifas, šis savikainos tarifas nustatomas kaip numatytasis. Jei sistemoje negalima sugretinti **Produktas** ir **Vienetas** reikšmių arba joje randamas atitinkantis kainų sąrašo elementas, tačiau kainodaros būdas pagrįstas standartine arba dabartine kaina, iš kurių nė viena nėra apibrėžta produkte, vieneto savikainai nustatoma numatytoji nulinė reikšmė.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
