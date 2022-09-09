---
title: Projektų įvertinimų ir faktinių duomenų savikainos tarifų nustatymas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatomi projekto įvertinimų ir faktinių aplinkybių išlaidų tarifai.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: c7dd264ebbd1da9b2f42d2284fb38988a09aa03f
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410160"
---
# <a name="determine-cost-rates-for-project-estimates-and-actuals"></a>Projektų įvertinimų ir faktinių duomenų savikainos tarifų nustatymas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Norėdami nustatyti išlaidų kainoraštį ir išlaidų tarifus įvertinime ir faktiniuose kontekstuose, sistema naudoja informaciją susijusio projekto laukuose **Data**, **Valiuta** ir **Sutartinis vienetas**.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Išlaidų tarifų nustatymas įvertinime ir faktiniuose laiko kontekstuose

Laiko **įvertinimo kontekstas** reiškia:

- Citatos **eilutės informacija apie laiką**.
- Sutarties eilutės informacija apie **laiką**.
- Išteklių priskyrimai projektui.

Faktinis **laiko** kontekstas reiškia:

- Laiko **įvedimo ir taisymo žurnalo** eilutės.
- Žurnalo eilutės, sukurtos, kai pateikiamas laiko įrašas.

Nustačius savikainos kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąjį išlaidų tarifą.

1. Sistema suderina laukų Vaidmuo **ir** Išteklių vienetas **derinį** įvertinime arba faktiniame laiko **kontekste** su vaidmenų kainoraščio kainoraščio eilutėmis. Šiame atitikime daroma prielaida, kad naudojate standartines darbo sąnaudų kainodaros dimensijas. Jei sukonfigūravote sistemą taip, kad ji atitiktų kitus laukus nei vaidmenų **ir** išteklių gavimo vienetas **arba be jų**, norint gauti atitinkamą vaidmens kainos eilutę, naudojamas kitas derinys.
1. Jei sistema randa vaidmens kainos eilutę, kurioje yra kombinacijos Vaidmens **ir** išteklių vienetas **savikainos koeficientas**, tas išlaidų tarifas naudojamas kaip numatytasis išlaidų tarifas.
1. Jei sistema negali atitikti **reikšmių Vaidmuo** ir **Išteklių vienetas**, ji nuskaito vaidmens kainos eilutes, kuriose yra atitinkančios lauko Vaidmuo **reikšmės**, bet nulinės lauko Išteklių gavimo vienetas **reikšmės**. Kai sistemoje yra atitinkamas vaidmens kainos įrašas, to įrašo išlaidų tarifas bus naudojamas kaip numatytasis išlaidų lygis.

> [!NOTE]
> Jei sukonfigūruosite skirtingą laukų **Vaidmenų** ir **išteklių ėmimo vienetas** prioritetų nustatymą arba jei turite kitų dimensijų, kurių prioritetas yra didesnis, ankstesnis veikimas atitinkamai pasikeis. Sistema nuskaito vaidmenų kainų įrašus, kurių reikšmės atitinka kiekvieną kainodaros dimensijos reikšmę prioriteto tvarka. Eilutės, kuriose yra neapibrėžtos tų dimensijų reikšmės, yra paskutinės.

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-expense"></a>Išlaidų tarifų nustatymas faktinėse ir išlaidų įvertinimo eilutėse

Išlaidų **įvertinimo kontekstas** reiškia:

- Išlaidų citatos **eilutės** informacija.
- Sutarties eilutės informacija apie **išlaidas**.
- Projekto išlaidų sąmatos.

Faktinis **išlaidų** kontekstas reiškia:

- Įrašo ir taisymo žurnalo eilutės, skirtos **išlaidoms**.
- Žurnalo eilutės, sukurtos pateikus išlaidų įrašą.

Nustačius savikainos kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąjį išlaidų tarifą.

1. Sistema suderina laukų **Kategorija** ir **Vienetas** derinį įvertinime arba faktiniame išlaidų **kontekste** su kainoraštyje esančiomis kategorijų kainoraščio kaino eilutėmis.
1. Jei sistema randa kategorijos kainos eilutę, kurioje yra kategorijų **ir** vienetų derinio **išlaidų tarifas, tas išlaidų tarifas** naudojamas kaip numatytasis išlaidų tarifas.
1. Jei sistema negali atitikti **verčių Kategorija** ir **Vienetas**, pagal numatytuosius nustatymus kaina nustatoma kaip **0** (nulis).
1. Įvertinimo kontekste, jei sistema gali rasti atitinkančią kategorijos kainų eilutę, bet kainodaros metodas yra ne **vieneto** kaina, pagal numatytuosius nustatymus savikaina nustatoma kaip **0** (nulis).

## <a name="determining-cost-rates-on-actual-and-estimate-lines-for-material"></a>Savikainos tarifų nustatymas faktinėse ir sąmatos eilutėse, skirtose medžiagai

Medžiagos **įvertinimo kontekstas** reiškia:

- Medžiagos **citatos** eilutės informacija.
- Medžiagos **sutarties eilutės informacija**.
- Reikšmingos projekto sąmatos.

Faktinis **medžiagos kontekstas** reiškia:

- Medžiagos **įrašo ir taisymo žurnalo** eilutės.
- Žurnalo eilutės, sukurtos pateikus medžiagos naudojimo žurnalą.

Nustačius savikainos kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąjį išlaidų tarifą.

1. Sistema naudoja laukų **Produktas** ir **Vienetas** derinį medžiagos įvertinime arba faktiniame **kontekste** pagal kainoraščio prekių eilutes kainoraštyje.
1. Jei sistema randa kainoraščio prekės eilutę, kurioje yra produkto **ir** vieneto derinio **išlaidų tarifas**, tas išlaidų tarifas naudojamas kaip numatytasis išlaidų tarifas.
1. Jei sistema negali sutapti su produkto ir **vieneto** **reikšmėmis**, vieneto savikaina pagal numatytuosius nustatymus nustatoma kaip **0** (nulis).
1. Įvertinime arba faktiniame kontekste, jei sistema gali rasti atitinkančią kainoraščio prekės eilutę, bet kainodaros metodas yra kažkas kita, o ne **valiutos suma**, vieneto savikaina pagal numatytuosius nustatymus nustatoma į **0**. Taip nutinka todėl, kad "Project Operations" palaiko tik **projekte naudojamų medžiagų valiutos sumos** kainodaros metodą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
