---
title: Projekto savikainos tarifų nustatymas pagal faktinius duomenis
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatomi projekto savikainos tarifai pagal įvertinimus ir faktinius duomenis.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c2295174df1ce766c6d1304f4e9c55d32d5c4775
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475242"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Projekto savikainos tarifų nustatymas pagal faktinius duomenis

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Nustatydama savikainos tarifus pagal įvertinimus ir faktinius duomenis programoje „Microsoft Dynamics 365 Project Operations“, sistema iš pradžių naudoja datą ir valiutą, esančias gaunamame įvertinime arba faktinių duomenų kontekste, kad nustatytų savikainos kainoraštį. Konkrečiai faktinių duomenų kontekste sistema naudoja lauką **Operacijos data**, kad nustatytų, kuris kainoraštis taikomas. Gaunamo įvertinimo arba faktinių duomenų reikšmė **Operacijos data** palyginama su kainoraščio reikšmėmis **Efektyvi pradžios data (nekonvertuoti pagal laiko juostą)** ir **Efektyvi pabaigos data (nekonvertuoti pagal laiko juostą)**. Nustačiusi savikainos kainoraštį, sistema nustato savikainos tarifą. 

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Savikainos tarifų nustatymas laiko įvertinimo ir faktinių duomenų kontekstuose

**Laiko** įvertinimo kontekstas nurodo:

- **Laiko** pasiūlymo eilutės išsami informacija
- **Laiko** sutarties eilutės išsami informacija
- Išteklių priskyrimas projektui.

**Laiko** faktinis kontekstas nurodo:

- **Laiko** įrašo ir koregavimo žurnalo eilutės.
- Žurnalo eilutės, sukurtos pateikus laiko įrašą.

Kai savikainos kainoraštis nustatomas, sistema atlieka toliau nurodytus veiksmus, kad įvestų numatytąjį savikainos tarifą.

1. Sistema sugretina **Laiko** įvertinimo arba faktinių duomenų konteksto laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** derinį su vaidmens kainų eilutėmis, esančiomis kainoraštyje. Atliekant šį sugretinimą daroma prielaida, kad darbo savikainai naudojate standartinių įkainių dimensijas. Jei sukonfigūravote, kad sistema sugretintų ne tik laukus **Vaidmuo** ir **Išteklių paskirstymo vienetas**, bet ir kitokius ar papildomus, tada sutampančio vaidmens kainos eilutei gauti bus naudojamas kitoks derinys.
1. Jei sistema randa vaidmens kainos eilutę, kurios laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** derinys turi savikainos tarifą, tuomet jis bus naudojamas kaip numatytasis savikainos tarifas.
1. Jei sistema negali sugretinti laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** reikšmių, ji nuskaito vaidmens kainų eilutes su atitinkančia lauko **Vaidmuo** reikšme, bet lauko **Išteklių paskirstymo vienetas** reikšmės lieka nulinės. Kai sistema ras atitinkamą vaidmens kainos įrašą, savikainos tarifas iš to įrašo bus naudojamas numatytajam savikainos tarifui nustatyti.

> [!NOTE]
> Jei sukonfigūravote kitokį laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** prioritetą arba jei turite kitokių didesnio prioriteto dimensijų, ankstesnis veikimo būdas atitinkamai pasikeis. Sistema nuskaito vaidmens kainos įrašus, kurių reikšmės atitinka kiekvieną įkainio dimensijos reikšmę prioriteto tvarka. Eilutės, kurios turi nulines šių dimensijų reikšmes, yra paskutinės.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Savikainos tarifų nustatymas pagal išlaidų faktinių duomenų ir įvertinimų eilutes

**Išlaidų** įvertinimo kontekstas nurodo:

- **Išlaidų** pasiūlymo eilutės išsami informacija
- **Išlaidų** sutarties eilutės išsami informacija
- Projekto išlaidų įvertinimai.

**Išlaidų** faktinių duomenų kontekstas nurodo:

- **Išlaidų** įrašo ir koregavimo žurnalo eilutės.
- Žurnalo eilutės, sukurtos pateikus išlaidų įrašą.

Kai savikainos kainoraštis nustatomas, sistema atlieka toliau nurodytus veiksmus, kad įvestų numatytąjį savikainos tarifą.

1. Sistema sugretina **Išlaidų** įvertinimo arba faktinių duomenų kontekste esančių laukų **Kategorija** ir **Vienetas** derinį su kategorijos kainos eilutėmis, esančiomis kainoraštyje.
1. Jei sistema randa kategorijos kainos eilutę, kurios laukų **Kategorija** ir **Vienetas** derinys turi savikainos tarifą, jis bus naudojamas numatytasis savikainos tarifas.
1. Jei sistemai nepavyksta sugretinti laukų **Kategorija** ir **Vienetas** reikšmių, pagal numatytuosius nustatymus kaina nustatoma kaip **0** (nulis).
1. Vertinimo kontekste, jei sistema neranda sutampančios kategorijos kainos elemento eilutės, bet įkainių metodas yra kitoks nei **Vieneto kaina**, pagal numatytuosius nustatymus savikainos tarifas nustatomas kaip **0** (nulis).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Savikainos tarifų nustatymas pagal medžiagos faktinių duomenų ir įvertinimo eilutes

**Medžiagos** įvertinimo kontekstas nurodo:

- **Medžiagos** pasiūlymo eilutės išsami informacija
- **Medžiagos** sutarties eilutės išsami informacija
- Projekto medžiagų įvertinimai.

**Medžiagos** faktinių duomenų kontekstas nurodo:

- **Medžiagos** įrašo ir koregavimo žurnalo eilutės.
- Žurnalo eilutės, sukurtos pateikus medžiagų naudojimo žurnalą.

Kai savikainos kainoraštis nustatomas, sistema atlieka toliau nurodytus veiksmus, kad įvestų numatytąjį savikainos tarifą.

1. Sistema naudoja **Medžiagos** įvertinimo arba faktinių duomenų kontekste esančių laukų **Produktas** ir **Vienetas** derinį su kainų sąrašo elementų eilutėmis, esančiomis kainoraštyje.
1. Jei sistema randa kainų sąrašo elemento eilutę, kurios laukų **Produktas** ir **Vienetas** derinys turi savikainos tarifą, jis bus naudojamas numatytasis savikainos tarifas.
1. Jei sistemoje nepavyksta sugretinti laukų **Produktas** ir **Vienetas** reikšmių, pagal numatytuosius nustatymus vieneto savikaina nustatoma kaip **0** (nulis).
1. Vertinimo arba faktinių duomenų kontekste, jei sistema neranda sutampančios kainų sąrašo elemento eilutės, bet įkainių metodas yra kitoks nei **Valiutos suma**, pagal numatytuosius nustatymus vieneto savikaina nustatoma kaip **0**. Taip nutinka dėl to, kad „Project Operations“ palaiko tik **Valiutos sumos** įkainių metodą, taikomą projekte naudojamoms medžiagoms.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
