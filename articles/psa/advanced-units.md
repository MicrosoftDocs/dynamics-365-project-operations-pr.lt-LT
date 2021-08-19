---
title: Vienetų grupės ir vienetai
description: Šioje temoje pateikiama informacija apie vienetų grupes ir vienetus.
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 55696b32b7b37048ba4c292b33d93b7b12614f2186fb972a2c3f3732e5512c82
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987581"
---
# <a name="unit-groups-and-units"></a>Vienetų grupės ir vienetai

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Vienetų grupės ir vienetai yra pagrindiniai „Microsoft Dynamics 365“ objektai. Vienetas – tai vienas matavimo vienetas, o kelis vienetus galima sugrupuoti į vienetų grupes. Vienetų grupė kartais „Dynamics 365“ vartotojo sąsajoje (UI) vadinama vienetų grafiku. 

Toliau pateikiami keli vienetų ir vienetų grupių pavyzdžiai.
 
- **Vienetų grupė**: atstumas 
    - **Vienetai**: mylia, kilometras ir pan.
- **Vienetų grupė**: laikas
    - **Vienetai**: valanda, diena, savaitė ir pan. 

Nustatę kelis vienetų grupės vienetus, taip pat turite nustatyti jų konvertavimo koeficientą, nurodydami pirmąjį vienetą, kurį nustatote kaip numatytąjį arba pagrindinį vienetų grupės vienetą. 

Pavyzdžiui, jei vienetų grupėje **Laikas** nustatysite parinktį **Valanda** kaip pirmąjį vienetą, sistema paskirs reikšmę **Valanda** kaip numatytąjį vienetą. Jei kitas nustatytas vienetas yra **Diena**, turite nustatyti vieneto **Diena** konvertavimo koeficientą **Valanda**. Jei tada kaip trečią vienetą įtrauksite **Savaitė**, reikės nustatyti vieneto **Savaitė** konvertavimo koeficientą **Diena** arba **Valanda**. 

Tolesniame paveiksle pateikiamas vieneto **Diena**, kurio lauke **Kiekis** rodomas dienos valandų skaičius, ir vieneto **Savaitė**, kurio lauke **Kiekis** rodomas, savaitės dienų skaičius, sąrankos pavyzdys.

> ![Vienetų grupė: informacijos puslapis.](media/advanced-2.png)

## <a name="using-units-and-unit-groups"></a>Vienetų ir vienetų grupių naudojimas

„Dynamics 365 Project Service Automation“ apdorojant įvertinimus ir įrašus naudoja vienetus ir vienetų grupes. 

Apdorojant išlaidas kiekvienai išlaidų kategorijai nustatoma numatytoji vienetų grupė ir vienetas. Šios reikšmės įvedamos kaip numatytosios reikšmės į išlaidų kategorijų kainoraščio įrašus. 

Pavyzdžiui, turite išlaidų kategoriją pavadinimu **Kilometražas**. Joje yra vienetų grupė pavadinimu **Atstumas** ir numatytasis vienetas pavadinimu **Mylia**. Jei vienetų grupėje **Atstumas** nustatysite du vienetus (**Mylia** ir **Kilometras**), viename kainoraštyje galėsite nustatyti dvi kategorijos **Kilometražas** kainas: kainą už mylią ir kainą už kilometrą.

| Išlaidų kategorija  | Vienetų grupė  | Vienetas      | Kainodaros metodas  | Vieneto kaina  |
|-------------------|---------------|-----------|-------------------|-------------------|
| Kilometražas           | Atstumas      | Mylia      | Vieneto kaina    | 10 USD            |
| Kilometražas           | Atstumas      | Kilometras | Vieneto kaina    |  6 USD            |

Kai įvedate projekto išlaidas, sistema nustato kainą naudodama išlaidų kategorijos ir vieneto derinį. 

| Išlaidų aprašas        | Išlaidų kategorija  | Vienetas  | Kiekis  | Vieneto kaina   |
|----------------------------|---------------------|-------|-----------|----------------|
| Važiavimas į kliento vietą | Kilometražas             | Mylia  | 10        | 10 USD         |

Laiko kategorijoje kiekvieno kainoraščio antraštėje yra laukas **Numatytasis laiko vienetas**. Reikšmė nustatoma kuriant kainoraščio antraštę. Tada šis vienetas naudojamas nustatant visas vaidmenimis pagrįstas kainas šiame kainoraštyje.

Lauko **Pasiūlyme nurodytas laikas** įvertinimų eilutes galima išreikšti bet kuriuo laiko vienetu. Tačiau projektų įvertinimo eilutėse ir projektų laiko įrašuose galima naudoti tik vienetą **Valanda**. Jei laiko įrašo arba įvertinimo eilutės vienetas neatitinka to vaidmens kainoraščio eilutės vieneto, sistema konvertuoja kainą į vienetus, nustatytus projekto įvertinime arba faktinėje projekto operacijoje.

Tolesniame pavyzdyje parodyta, kaip PSA naudoja vienetų grupę, vienetus ir konvertavimo koeficientus.
- Vienetai

   - **Vienetų grupė**: laikas 
   - **Vienetai**: valanda 
    
    - **Diena** – konvertavimo koeficientas: 8 valandos       
    - **Savaitė** – konvertavimo koeficientas: 40 valandos  
        
- A projekto kainoraščio sąranka

    - **Pavadinimas**: 2016 m. pardavimo JK kainos 
    - **Numatytasis laiko vienetas**: diena 
    - **Valiuta**: GBP

| Vaidmuo      | Vienetų grupė | Vienetas | Organizacinis vienetas | Kainos   |
|-----------|------------|------|---------------------|---------|
| Developer | Laikas       | Diena  | Contoso JK          | 800 GBP |

### <a name="time-entry"></a>Laiko įrašas

Tolesnėje lentelėje parodyta PSA sukurta trijų valandų projekto pardavimo operacija.


| Projektas   | Užduotis    | Vaidmuo      | Kiekis | Vienetas  | Vieneto kaina | Pardavimo suma, kuriai neišrašyta sąskaita |
|-----------|---------|-----------|----------|-------|------------|-----------------------|
| A projektas | Dizainas  | Kūrėjas | 3        | Hour  | 100 GBP    | 300 GBP               |

## <a name="time-unit-faq"></a>DUK apie laiko vienetus

### <a name="does-psa-convert-to-different-units-in-the-case-of-expenses"></a>Ar PSA konvertuoja išlaidas į kitus vienetus?
Ne. Galimas tik laiko vienetų konvertavimas. Išlaidų atveju, jei sistemai nepavyksta rasti išlaidų kategorijos ir vieneto derinio kainos, pagal numatytuosius parametrus nustatoma 0,00 dydžio kaina.

### <a name="why-does-psa-convert-time-units"></a>Kodėl PSA konvertuoja laiko vienetus?
Kai kuriose šalyse arba regionuose įtaikomas teisinis reikalavimas sąskaitų tarifus nustatyti dienomis. Pasiūlymo ciklo metu derybos dėl kainų ir nuolaidų vyksta naudojant kiekvieno apmokėtino vaidmens dienos tarifus. Grafikas įvertinamas ir laikas įvedamas valandomis. Siekiant palaikyti šį laiko vienetų skirtumą, PSA konvertuoja laiko vienetus.

### <a name="can-time-units-be-changed-on-project-estimates"></a>Ar galima pakeisti laiko vienetus projektų įvertinimuose?
Ne. Grafiko įvertinimas šiuo metu apribotas naudoti tik valandas ir jo keisti negalima.

### <a name="can-units-and-unit-groups-be-edited-deleted-and-added"></a>Ar galima redaguoti, naikinti ir įtraukti vienetus bei vienetų grupes?
Taip. Išskyrus vienetų grupę **Laikas** ir vienetą **Valanda**, visus vienetus galima panaikinti arba redaguoti bei įtraukti naujų vienetų. PSA negalima panaikinti vienetų grupės **Laikas** ir vieneto **Valanda**. Tačiau juos galima atnaujinti įvedant vertimo tekstą lauke **Pavadinimas**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]