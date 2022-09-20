---
title: Projektinių įvertinimų ir faktinių duomenų savikainos tarifų nustatymas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip nustatomi projektais pagrįstų įvertinimų ir faktinių aplinkybių išlaidų tarifai.
author: rumant
ms.date: 9/12/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 822a7bd8ae87d4fd4044d8b46347bfe1b4ca13ca
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475289"
---
# <a name="determine-cost-rates-for-project-based-estimates-and-actuals"></a>Projektinių įvertinimų ir faktinių duomenų savikainos tarifų nustatymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norėdami nustatyti savikainos kainas pagal "Microsoft" Dynamics 365 Project Operations įvertinimus ir faktines vertes, sistema pirmiausia naudoja datą ir valiutą gaunamame įvertinime arba faktiniame kontekste, kad nustatytų pardavimo kainoraštį. Konkrečiai faktiniame kontekste sistema naudoja lauką **Operacijos data**, kad nustatytų, kuris kainoraštis yra taikytinas. Gaunamo **įvertinimo arba faktinio sandorio datos** vertė lyginama su **kainoraštyje esančiomis reikšmė Efektyvios pradžios (nepriklausoma nuo laiko juostos)** ir **Efektyvios pabaigos (laiko juostos nepriklausoma)** reikšmė. Nustačius išlaidų kainoraštį, sistema nustato išlaidų normą.

## <a name="determining-cost-rates-in-estimate-and-actual-contexts-for-time"></a>Išlaidų tarifų nustatymas įvertinime ir faktiniuose laiko kontekstuose

Laiko **įvertinimo kontekstas** reiškia:

- Citatos **eilutės informacija apie laiką**.
- Sutarties eilutės informacija apie **laiką**.
- Išteklių priskyrimai projektui.

Faktinis **laiko** kontekstas reiškia:

- Laiko **įvedimo ir taisymo žurnalo** eilutės.
- Žurnalo eilutės, sukurtos, kai pateikiamas laiko įrašas.

Nustačius išlaidų kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąjį išlaidų tarifą.

1. Sistema suderina laukų **Vaidmuo**, **Išteklių gavimo įmonė** ir **Išteklių ėmimo vienetas** derinį laiko **įvertinime arba faktiniame kontekste** pagal vaidmenų kainoraščio kainoraščio eilutes. Šiame atitikime daroma prielaida, kad naudojate standartines darbo sąnaudų kainodaros dimensijas. Jei sukonfigūravote sistemą taip, kad ji atitiktų kitus laukus nei vaidmuo **,** išteklių gavimo įmonė **ir** išteklių vienetas **arba be jų**, norint gauti atitinkamą vaidmens kainos eilutę, naudojamas kitas derinys.
1. Jei sistema randa vaidmens kainos eilutę, kurioje yra vaidmenų **,** išteklių gavimo įmonės **ir** išteklių vieneto derinių išlaidų tarifas **, tas išlaidų tarifas** naudojamas kaip numatytasis išlaidų tarifas.
1. Jei sistema negali sutapti su **vaidmenų**, **išteklių gavimo įmonės** ir **išteklių ėmimo vieneto** reikšmėmis, ji sumažina dimensiją, turinčią mažiausią prioritetą, ieško vaidmenų kainų eilučių, atitinkančių kitas dvi dimensijų reikšmes, ir toliau palaipsniui mažina dimensijas, kol randama atitinkanti vaidmens kainos eilutė. Išlaidų tarifas iš to įrašo bus naudojamas kaip numatytasis išlaidų tarifas. Jei sistema neranda atitinkančios vaidmens kainos eilutės, pagal numatytuosius nustatymus kaina bus nustatyta į **0** (nulis).

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

Nustačius išlaidų kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąjį išlaidų tarifą.

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

- Medžiagos įrašo ir taisymo žurnalo **eilutės**.
- Žurnalo eilutės, sukurtos pateikus medžiagos naudojimo žurnalą.

Nustačius išlaidų kainoraštį, sistema atlieka šiuos veiksmus, kad įvestų numatytąjį išlaidų tarifą.

1. Sistema naudoja laukų **Produktas** ir **Vienetas** derinį medžiagos įvertinime arba faktiniame **kontekste** pagal kainoraščio prekių eilutes kainoraštyje.
1. Jei sistema randa kainoraščio prekės eilutę, kurioje yra produkto **ir** vieneto derinio **išlaidų tarifas**, tas išlaidų tarifas naudojamas kaip numatytasis išlaidų tarifas.
1. Jei sistema negali sutapti su produkto ir **vieneto** **reikšmėmis**, vieneto savikaina pagal numatytuosius nustatymus nustatoma kaip **0** (nulis).
1. Įvertinime arba faktiniame kontekste, jei sistema gali rasti atitinkančią kainoraščio prekės eilutę, bet kainodaros metodas yra kažkas kita, o ne **valiutos suma**, vieneto savikaina pagal numatytuosius nustatymus nustatoma į **0**. Taip nutinka todėl, kad "Project Operations" palaiko tik **projekte naudojamų medžiagų valiutos sumos** kainodaros metodą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
