---
title: Įvertintų ir faktinių savikainų aprašymas
description: Šioje temoje pateikta informacija apie įvertintų ir faktinių savikainų aprašymą.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119699"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a>Įvertintų ir faktinių savikainų aprašymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norėdama nustatyti išlaidų kainas ir įvertintų bei faktinių savikainų kainoraštį, sistema naudoja susijusio projekto laukų **Data**, **Valiuta** ir **Sutarties vienetai** informaciją. Nustačius savikainų kainoraštį, programa nustato savikainos tarifą.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a>Savikainos tarifų faktinėse ir įvertintose laiko eilutėse nustatymas

Įvertintos laiko eilutės nurodo pasiūlymo ir sutarties eilutės duomenis, skirtus projekto laikui ir ištekliams priskirti.

Kai savikainų kainoraštis aprašomas, sistema naudoja laiko įvertinimo eilutės laukus **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas**, kad sugretintų su vaidmens kainų eilutėmis sudarytame kainoraštyje. Šiame gretinime laikoma, kad naudojamos paruoštos darbo savikainos kainodaros dimensijos. Jei sukonfigūravote, kad sistema atitiktų laukus vietoj arba greta laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas**, tada kitoks derinys bus naudojamas gretinimo vaidmens kainos eilutei gauti. Jei programa suranda vaidmens kainos eilutę, kurios laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas** derinys turi savikainos tarifą, tai yra numatytasis savikainos tarifas. Jei programa negali sugretinti laukų **Vaidmuo**, **Išteklių paskirstymo įmonė** ir **Išteklių paskirstymo vienetas** reikšmių, tada ji nuskaito vaidmens kainų eilutes su atitinkamu vaidmeniu, bet **Išteklių paskirstymo vieneto** reikšmės lieka neapibrėžtos. Kai jis turi atitinkantį vaidmens kainos įrašą, numatytasis savikainos tarifas nustatomas iš to įrašo. 

> [!NOTE]
> Jei sukonfigūravote kitokį **Vaidmens**, **Išteklių paskirstymo įmonės** ir **Išteklių paskirstymo vieneto** pirmumą arba jei turite kitokių didesnio prioriteto dimensijų, toks veikimas atitinkamai pasikeis. Sistema nuskaito vaidmens kainų įrašus su atitinkamomis kiekvienos kainodaros dimensijos vertėmis pirmumo tvarka: eilutės su neapibrėžtomis tų dimensijų vertėmis pateikiamos paskutinės.

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Savikainos tarifų faktinėse ir įvertintose išlaidų eilutėse nustatymas

Išlaidų įvertintos eilutės nurodo pasiūlymo ir sutarties eilutės išlaidų informaciją ir projekto išlaidų įvertintas eilutes.

Kai savikainų kainoraštis aprašomas, sistema naudoja išlaidų įvertintos eilutės laukus **Kategorija** ir **Vienetas**, kad sugretintų su **kategorijos kainos** eilutėmis sudarytame kainoraštyje. Jei sistema suranda kategorijos kainos eilutę, kurios laukų **Kategorija** ir **Vienetas** derinys turi savikainos tarifą, savikainos tarifas bus numatytasis. Jei sistema nesuderina laukų **Kategorija** ir **Vienetas** reikšmių arba jei ji gali rasti gretinimo kategorijos kainos eilutę, bet kainodaros metodas nėra **Vieneto kaina**, numatytasis savikainos tarifas nustatomas į nulį (0).
