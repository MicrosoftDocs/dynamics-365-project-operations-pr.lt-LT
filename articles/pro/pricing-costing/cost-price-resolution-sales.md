---
title: Įvertinimų ir faktinių duomenų savikainos nustatymas – „Lite“ versija
description: Šioje temoje pateikta informacija apie įvertintų ir faktinių savikainų aprašymą.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: bbb79fdc5c68d67530b5aa34fe6105211eff1768
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274559"
---
# <a name="resolve-cost-prices-on-estimates-and-actuals---lite"></a>Įvertinimų ir faktinių duomenų savikainos nustatymas – „Lite“ versija

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]