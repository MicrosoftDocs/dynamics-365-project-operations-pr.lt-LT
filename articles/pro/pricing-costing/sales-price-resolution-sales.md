---
title: Projektų įvertinimų ir faktinių aplinkybių pardavimo kainų nustatymas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatomos projekto įvertinimų ir faktinių aplinkybių pardavimo kainos.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 6504302578d1eb3d00c717ea93cd4c4212acb4e7
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410129"
---
# <a name="determine-sales-prices-for-project-estimates-and-actuals"></a>Projektų įvertinimų ir faktinių aplinkybių pardavimo kainų nustatymas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Norėdami nustatyti pardavimo kainas pagal "Microsoft" Dynamics 365 Project Operations įvertinimus ir faktines vertes, sistema pirmiausia naudoja datą ir valiutą gaunamame įvertinime arba faktiniame kontekste, kad nustatytų pardavimo kainoraštį. Konkrečiai faktiniame kontekste sistema naudoja lauką **Operacijos data**, kad nustatytų, kuris kainoraštis yra taikytinas. Nustačius pardavimo kainoraštį, sistema nustato pardavimo arba sąskaitos tarifą.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-time"></a>Pardavimo tarifų nustatymas faktinėse ir įvertintose laiko eilutėse

Laiko **įvertinimo kontekstas** reiškia:

- Citatos **eilutės informacija apie laiką**.
- Sutarties eilutės informacija apie **laiką**.
- Išteklių priskyrimai projektui.

Faktinis **laiko** kontekstas reiškia:

- Laiko **įvedimo ir taisymo žurnalo** eilutės.
- Žurnalo eilutės, sukurtos, kai pateikiamas laiko įrašas.
- "Time"**sąskaitos faktūros eilutės duomenys**. 

Nustačius pardavimo kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąjį sąskaitų tarifą.

1. Sistema suderina laukų Vaidmuo **ir** Išteklių vienetas **derinį** įvertinime arba faktiniame laiko **kontekste** su vaidmenų kainoraščio kainoraščio eilutėmis. Šiame atitikime daroma prielaida, kad sąskaitų tarifams naudojate nekokybiškus kainodaros aspektus. Jei sukonfigūravote kainodarą taip, kad ji pagrįsta kitais laukais nei vaidmenų **ir** išteklių vienetas **arba be jo**, šis laukų derinys naudojamas norint gauti atitinkamą vaidmens kainos eilutę.
1. Jei sistema randa vaidmens kainos eilutę, kurioje yra derinio Vaidmens **ir** išteklių vienetas sąskaitų **tarifas**, tas sąskaitų tarifas naudojamas kaip numatytasis sąskaitos tarifas.
1. Jei sistema negali sutapti su **reikšmėmis Vaidmuo** ir **Išteklių vienetas**, ji nuskaito vaidmens kainos eilutes, kuriose yra atitinkančios lauko Vaidmuo **reikšmės**, bet lauko Išteklių vienetas **neapibrėžtos** reikšmės. Kai sistema ras atitinkamą vaidmens kainos įrašą, to įrašo sąskaitų tarifas bus naudojamas kaip numatytasis sąskaitų tarifas. Šiame atitikime daroma prielaida, kad "Out-of-of-prepared" konfigūracija, skirta santykiniam vaidmens prioritetui **, palyginti su "ResusOurcing** Unit"**kaip pardavimo kainodaros dimensija.**

> [!NOTE]
> Jei sukonfigūruosite skirtingą laukų **Vaidmenų** ir **išteklių ėmimo vienetas** prioritetų nustatymą arba jei turite kitų dimensijų, kurių prioritetas yra didesnis, ankstesnis veikimas atitinkamai pasikeis. Sistema nuskaito vaidmenų kainų įrašus, kurių reikšmės atitinka kiekvieną kainodaros dimensijos reikšmę prioriteto tvarka. Eilutės, kuriose yra neapibrėžtos tų dimensijų reikšmės, yra paskutinės.

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-expense"></a>Pardavimo tarifų nustatymas faktinėse ir išlaidų įvertinimo eilutėse

Išlaidų **įvertinimo kontekstas** reiškia:

- Išlaidų citatos **eilutės** informacija.
- Sutarties eilutės informacija apie **išlaidas**.
- Projekto išlaidų įvertinimo eilutės.

Faktinis **išlaidų** kontekstas reiškia:

- Įrašo ir taisymo žurnalo eilutės, skirtos **išlaidoms**.
- Žurnalo eilutės, sukurtos pateikus išlaidų įrašą.
- Sąskaitos faktūros eilutės informacija apie **išlaidas**. 

Nustačius pardavimo kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąją vieneto pardavimo kainą.

1. Sistema suderina laukų **Kategorija** ir **Vienetas** derinį išlaidų **įvertinimo eilutėje su** kainoraštyje esančiomis kategorijų kainoraščio kainoraščio eilutėmis.
1. Jei sistema randa kategorijos kainos eilutę, kurioje yra kategorijų ir **vienetų** derinio **pardavimo** rodiklis, tas pardavimo rodiklis naudojamas kaip numatytasis pardavimo rodiklis.
1. Jei sistema randa atitinkančią kategorijos kainos eilutę, kainodaros metodas gali būti naudojamas norint įvesti numatytąją pardavimo kainą. Šioje lentelėje parodytas numatytasis išlaidų kainų veikimas programoje "Project Operations".

    | Kontekstas | Kainodaros metodas | Numatytoji kaina |
    | --- | --- | --- |
    | Numatyti | Vieneto kaina | Pagal kategorijos kainos eilutę. |
    |        | Savikaina | 0.00 |
    |        | Antkainis prie savikainos | 0.00 |
    | Faktinis | Vieneto kaina | Pagal kategorijos kainos eilutę. |
    |        | Savikaina | Remiantis faktinėmis susijusiomis išlaidomis. |
    |        | Antkainis prie savikainos | Antkainis, kaip apibrėžta kategorijos kainos eilutėje, taikomas faktinių susijusių išlaidų vieneto savikainos tarifui. |

1. Jei sistema negali atitikti **verčių Kategorija** ir **Vienetas**, pardavimo rodiklis pagal numatytuosius nustatymus nustatytas kaip **0** (nulis).

## <a name="determining-sales-rates-on-actual-and-estimate-lines-for-material"></a>Pardavimo tarifų nustatymas faktinėse ir įvertintose medžiagos eilutėse

Medžiagos **įvertinimo kontekstas** reiškia:

- Medžiagos **citatos** eilutės informacija.
- Medžiagos **sutarties eilutės informacija**.
- Projekto medžiagų įvertinimo eilutės.

Faktinis **medžiagos kontekstas** reiškia:

- Medžiagos **įrašo ir taisymo žurnalo** eilutės.
- Žurnalo eilutės, sukurtos pateikus medžiagos naudojimo žurnalą.
- Medžiagos sąskaitos faktūros eilutės **duomenys**. 

Nustačius pardavimo kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąją vieneto pardavimo kainą.

1. Sistema suderina laukų Produktas ir Vienetas **derinį** medžiagos **įvertinimo eilutėje su** kainoraščio prekių eilutėmis kainoraštyje.**·**
1. Jei sistema randa kainoraščio prekės eilutę, kurioje yra produkto ir vieneto **derinio** pardavimo kursas, ir jei kainodaros metodas yra **Suma Valiuta**, naudojama kainoraščio eilutėje nurodyta pardavimo kaina.**·** 
1. **Jei lauko Produkto** ir **vieneto** reikšmės nesutampa arba jei kainodaros metodas yra kažkas kita, o ne **valiutos suma**, pardavimo kursas pagal numatytuosius nustatymus nustatomas kaip **0** (nulis). Taip nutinka todėl, kad "Project Operations" palaiko tik **projekte naudojamų medžiagų valiutos sumos** kainodaros metodą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
