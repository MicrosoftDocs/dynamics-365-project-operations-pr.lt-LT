---
title: Projekto pardavimo kainų įvertinimų ir faktinių duomenų nustatymas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatomos projektų pardavimų kainos pagal įvertinimus ir faktinius duomenis.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 1288a571d50604ee400db9c16822719d0649628b
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475195"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Projekto pardavimo kainų įvertinimų ir faktinių duomenų nustatymas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Nustatydama pardavimų kainą pagal įvertinimus ir faktinius duomenis programoje „Microsoft Dynamics 365 Project Operations“, sistema iš pradžių naudoja datą ir valiutą, esančias gaunamame įvertinime arba faktinių duomenų kontekste, kad nustatytų pardavimo kainoraštį. Konkrečiai faktinių duomenų kontekste sistema naudoja lauką **Operacijos data**, kad nustatytų, kuris kainoraštis taikomas. Gaunamo įvertinimo arba faktinių duomenų reikšmė **Operacijos data** palyginama su kainoraščio reikšmėmis **Efektyvi pradžios data (nekonvertuoti pagal laiko juostą)** ir **Efektyvi pabaigos data (nekonvertuoti pagal laiko juostą)**. Nustačiusi pardavimų kainoraštį, sistema nustato pardavimo arba sąskaitų tarifą.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Pardavimo tarifų faktinėse ir įvertinimo eilutėse (skirtose laikui) nustatymas

**Laiko** įvertinimo kontekstas nurodo:

- **Laiko** pasiūlymo eilutės išsami informacija
- **Laiko** sutarties eilutės išsami informacija
- Išteklių priskyrimas projektui.

**Laiko** faktinis kontekstas nurodo:

- **Laiko** įrašo ir koregavimo žurnalo eilutės.
- Žurnalo eilutės, sukurtos pateikus laiko įrašą.
- **Laiko** sąskaitos faktūros eilutės išsami informacija 

Kai pardavimo kainoraštis nustatytas, sistema atlieka toliau nurodytus veiksmus, kad įvestų numatytąjį sąskaitų tarifą.

1. Sistema sugretina **Laiko** įvertinimo arba faktinių duomenų konteksto laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** derinį su vaidmens kainų eilutėmis, esančiomis kainoraštyje. Šiame gretinime laikoma, kad jūs naudojate paruoštas sąskaitų tarifų kainodaros dimensijos. Jei kainodarą sukonfigūravote remdamiesi bet kuriais kitais laukais vietoje arba greta laukų **Vaidmuo**, **Išteklių paskirstymo vienetas**, tada toks laukelių derinys bus naudojamas gretinimo vaidmens kainos eilutei gauti.
1. Jei sistema suranda vaidmens kainos eilutę, kurios laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** derinys turi sąskaitos tarifą, tas sąskaitos tarifas bus naudojamas kaip numatytasis.
1. Jei sistema negali sugretinti laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** reikšmių, ji nuskaito vaidmens kainų eilutes su atitinkančia lauko **Vaidmuo** reikšme, bet lauko **Išteklių vienetas** reikšmės lieka nulinės. Kai sistema randa atitinkamą vaidmens kainos įrašą, sąskaitos tarifas iš to įrašo bus naudojamas numatytajam sąskaitos tarifui nustatyti. Šiame gretinime laikoma, kad paruošta santykinio **Vaidmens** lyginant su **Išteklių paskirstymo vieneto** pirmumo konfigūracija, yra pardavimo kainodaros dimensija.

> [!NOTE]
> Jei sukonfigūravote kitokį laukų **Vaidmuo** ir **Išteklių paskirstymo vienetas** prioritetą arba jei turite kitokių didesnio prioriteto dimensijų, ankstesnis veikimo būdas atitinkamai pasikeis. Sistema nuskaito vaidmens kainos įrašus, kurių reikšmės atitinka kiekvieną įkainio dimensijos reikšmę prioriteto tvarka. Eilutės, kurios turi nulines šių dimensijų reikšmes, yra paskutinės.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Pardavimo tarifų faktinėse ir įvertinimo eilutėse (skirtose išlaidoms) nustatymas

**Išlaidų** įvertinimo kontekstas nurodo:

- **Išlaidų** pasiūlymo eilutės išsami informacija
- **Išlaidų** sutarties eilutės išsami informacija
- Projekto išlaidų eilučių įvertinimas.

**Išlaidų** faktinių duomenų kontekstas nurodo:

- **Išlaidų** įrašo ir koregavimo žurnalo eilutės.
- Žurnalo eilutės, sukurtos pateikus išlaidų įrašą.
- **Išlaidų** sąskaitos faktūros eilutės išsami informacija. 

Kai sudaromas pardavimo kainoraštis, sistema atlieka toliau nurodytus veiksmus, kad įvestų numatytąją vieneto pardavimo kainą.

1. Sistema išlaidų įvertinimo eilutėje priderina laukų **Kategorija** ir **Vienetas** derinį prie **Išlaidų** eilutės, kad sugretintų su kategorijų kainų eilutėmis sudarytame kainoraštyje.
1. Jei sistema suranda kategorijos kainos eilutę, kurios laukų **Kategorija** ir **Vienetas** derinys turi pardavimo tarifą, tas pardavimo tarifas bus naudojamas kaip numatytasis.
1. Jei sistema randa atitinkamos kategorijos kainų eilutę, kainodaros metodą galima naudoti numatytajai pardavimo kainai įvesti. Toliau pateiktoje lentelėje parodytas išlaidų kainos numatytasis veikimas naudojant „Project Operations“.

    | Kontekstas | Kainodaros metodas | Numatytoji kaina |
    | --- | --- | --- |
    | Numatyti | Vieneto kaina | Remiantis kategorijų kainų eilute. |
    |        | Savikaina | 0.00 |
    |        | Antkainis prie savikainos | 0.00 |
    | Faktinis | Vieneto kaina | Remiantis kategorijų kainų eilute. |
    |        | Savikaina | Remiantis susijusia faktine savikaina. |
    |        | Antkainis prie savikainos | Antkainis pritaikytas, kaip apibrėžta susijusios faktinės savikainos vieneto savikainos tarifo kategorijų kainų eilutėje. |

1. Jei sistemai nepavyksta sugretinti laukų **Kategorija** ir **Vienetas** reikšmių, pagal numatytuosius nustatymus pardavimo tarifas nustatomas kaip **0** (nulis).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Pardavimo kainų nustatymas Medžiagos faktinių duomenų ir įvertinimo eilutėse

**Medžiagos** įvertinimo kontekstas nurodo:

- **Medžiagos** pasiūlymo eilutės išsami informacija
- **Medžiagos** sutarties eilutės išsami informacija
- Projekto medžiagų įvertinimo eilutės.

**Medžiagos** faktinių duomenų kontekstas nurodo:

- **Medžiagos** įrašo ir koregavimo žurnalo eilutės.
- Žurnalo eilutės, sukurtos pateikus medžiagų naudojimo žurnalą.
- **Medžiagų** sąskaitos faktūros eilutės išsami informacija. 

Kai sudaromas pardavimo kainoraštis, sistema atlieka toliau nurodytus veiksmus, kad įvestų numatytąją vieneto pardavimo kainą.

1. Sistema **Medžiagos** įvertinimo eilutei priderina laukų **Produktas** ir **Vienetas** derinį, kad sugretintų kainų sąrašo elemento eilutes nustatytame kainoraštyje.
1. Jei sistema randa kainų sąrašo elemento eilutę, kurioje nurodytos laukų **Produktas** ir **Vienetas** derinio pardavimo kainos, o įkainojimo metodas nustatytas kaip **Valiutos suma**, naudojama kainoraščio eilutėje nurodyta pardavimo kaina. 
1. Jei laukelių **Produktas** ir **Vienetas** reikšmės neatitinka arba jei kainodaros metodas yra kitas nei **Valiutos suma** pagal numatytuosius nustatymus pardavimo kursas nustatomas kaip **0** (nulinis). Taip nutinka dėl to, kad „Project Operations“ palaiko tik **Valiutos sumos** įkainių metodą, taikomą projekte naudojamoms medžiagoms.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
