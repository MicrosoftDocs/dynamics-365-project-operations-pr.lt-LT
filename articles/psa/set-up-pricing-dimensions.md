---
title: Pasirinktinių laukų kaip kainodaros dimensijų nustatymas
description: Šiame straipsnyje pateikiama informacija apie pasirinktinių kainodaros dimensijų nustatymą.
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/20/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 14d27b53b42744d47e298bf5a926c1262dbf44d4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922607"
---
# <a name="setting-up-custom-fields-as-pricing-dimensions"></a>Pasirinktinių laukų kaip kainodaros dimensijų nustatymas 

[!include [banner](../includes/psa-now-project-operations.md)]

Prieš pradėdami, šiame straipsnyje daroma prielaida, kad atlikote procedūras straipsniuose, [Kurti pasirinktinius laukus ir objektus](create-custom-fields-entities.md) bei [Įtraukti pasirinktinius laukus į kainų nustatymą ir operacijų objektus](field-references.md). Jei dar neatlikote šių procedūrų, grįžkite ir užpildykite jas, tada grįžkite į šį straipsnį. 

Šiame straipsnyje pateikiama informacija apie pasirinktinių kainodaros dimensijų nustatymą. „Project Service“ žiniatinklio sąsajos puslapio **Parametrai** skirtuke **Kaina pagrįstos kainodaros dimensijos** rodomi įrašai kainodaros dimensijų objektuose. Pagal numatytuosius parametrus „Project Service“ diegimas sukuria 2 eilutes šio skirtuko tinklelyje:

- **msdyn_resourcecategory** (vaidmuo)
- **msdyn_OrganizationalUnit** (organizacinis vienetas)

> [!IMPORTANT]
> Nenaikinkite šių eilučių. Tačiau, jei jums jų nereikia, padarykite juos netaikomais konkrečiame kontekste nustatydami **Taikoma savikainai**, **Taikoma pardavimui** ir **Taikoma pirkimui** kaip **Ne**. Nustačius šias atributų reikšmes kaip **Ne**, tai turi tokį patį poveikį kaip kainodaros dimensijos lauko neturėjimas.

Kad laukas taptų kainodaros dimensija, jis turi:

- Būti sukurtas kaip laukas objektuose **Vaidmens kaina** ir **Vaidmens kainos antkainis**. Daugiau informacijos apie tai, kaip tai padaryti, žr. [Pasirinktinių laukų įtraukimas į kainos sąranką ir operacijų objektus](field-references.md).
- Būti sukurtas kaip eilutė lentelėje **Kainodaros dimensija**. Pavyzdžiui, įtraukite kainodaros dimensijos eilutes kaip parodyta toliau pateiktame paveiksle. 

![Suma pagrįstos kainodaros dimensijos eilutės.](media/Amt-based-PD.png)

Atkreipkite dėmesį, kad išteklių darbo valandos (**msdyn_resourceworkhours**) įtrauktos kaip antkainiu pagrįsta dimensija ir įtrauktos į tinklelį skirtuke **Antkainiu pagrįsta kainodaros dimensija**.

![Antkainiu pagrįstos kainodaros dimensijos eilutės.](media/Markup-based-PD.png)

> [!IMPORTANT]
> Bet koks esamas arba naujas kainodaros dimensijos duomenų pakeitimas šioje eilutėje yra perkeliamas į „Project Service“ kainodaros verslo logiką, tik kai atnaujinama talpykla. Talpyklos atnaujinimo laikas gali užtrukti iki 10 minučių. Leiskite šį laiką, kad matytumėte pakeitimus kainos numatytoje logikoje, kurie turi būti kainodaros dimensijos duomenų pakeitimų rezultatas.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Kainodaros dimensijų lentelės atributai
Tolesniuose skyriuose pateikiama informacija apie skirtingus atributus lentelėje **Kainodaros dimensijos**.

### <a name="pricing-dimension-name"></a>Kainodaros dimensijos pavadinimas
Ši reikšmė turi būti tokia pati kaip ir lauko, kuris įtrauktas į pasirinktinių kainodaros dimensijų lentelę **Vaidmens kaina**, schemos pavadinimas. Daugiau informacijos apie tai, kaip įtraukti laikus į lentelę **Vaidmens kaina**, žr. [Pasirinktinių laukų įtraukimas į kainos sąranką ir operacijų objektus](field-references.md).

### <a name="type-of-dimension"></a>Dimensijos tipas
Yra dviejų tipų kainodaros dimensijos:
  
  - **Suma pagrįstos dimensijos**: dimensijų reikšmės iš įvesties konteksto yra sugretinamos su dimensijų reikšmėmis eilutėje **Vaidmens kaina** ir kaina / savikaina pagal numatytuosius parametrus tiesiogiai nustatoma iš lentelės **Vaidmens kaina**.
  - **Antkainiu pagrįstos dimensijos**: tai yra dimensijos, kuriose „Project Service“ pritaikys toliau nurodytą 3 veiksmų procesą, kad gautų kainą / savikainą:
 
    1. „Project Service“ sugretina dimensijų, kurios nėra pagrįstos antkainiu, reikšmes iš įvesties konteksto su vaidmens kainos eilute, kad gautų bazinį tarifą.
    2. „Project Service“ sugretina visas dimensijų reikšmes iš įvesties konteksto su eilute **Vaidmens kainos antkainis**, kad gautų antkainio procentą.
    3. „Project Service“ taiko antkainio procentą iš antrojo veiksmo baziniam tarifui, gautam iš lentelės **Vaidmens kaina** pirmojo veiksmo metu, kad gautų galutinę kainą / savikainą.
   
   Toliau pateiktoje lentelėje parodomas kainos antkainių skaičiavimas.
  
| Vaidmuo        | Org. vienetai    |Darbo vieta      |Standartinis pavadinimas      |Išteklių darbo valandos      |  Antkainis|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Vietoje            |                    |Viršvalandžiai                 |15     |
|             | Contoso India|Vietinis             |                    |Viršvalandžiai                 |10     |
|             | „Danys“, JAV   |Vietinis             |                    |Viršvalandžiai                 |20     |


Jei ištekliai iš „Danys India“, kurių bazinis tarifas yra 100 USD, dirba internetu, ir jie laiko įraše užregistruoja 8 reguliaraus laiko valandas ir 2 valandas viršvalandžių, „Project Service“ kainodaros variklis naudos 100 bazinį tarifą už 8 valandas įrašui 800 USD. Už 2 valandas viršvalandžių 100 baziniam tarifui bus taikomas 15 % antkainis, kad būtų gauta 115 USD vieneto kaina, ir įrašys bendrą savikainą, lygią 230 USD.

### <a name="applicable-to-cost"></a>Taikoma savikainai 
Jei tai nustatyta kaip **Taip**, tai nurodo, kad dimensijos reikšmė iš įvesties konteksto turi būti naudojama, siekiant suderinti **Vaidmens kaina** ir **Vaidmens kainos antkainis**, kai gaunami savikainos ir antkainio tarifai.

### <a name="applicable-to-sales"></a>Taikoma pardavimui
Jei tai nustatyta kaip **Taip**, tai nurodo, kad dimensijos reikšmė iš įvesties konteksto turi būti naudojama, siekiant suderinti **Vaidmens kaina** ir **Vaidmens kainos antkainis**, kai gaunami sąskaitų ir antkainio tarifai.

### <a name="applicable-to-purchase"></a>Taikoma pirkimui
Jei tai nustatyta kaip **Taip**, tai nurodo, kad dimensijos reikšmė iš įvesties konteksto turi būti naudojama, siekiant suderinti **Vaidmens kaina** ir **Vaidmens kainos antkainis**, kai gaunama pirkimo kaina. Šiuo metu „Project Service“ nepalaiko subrangos scenarijų, todėl šis laukas nenaudojamas. 

### <a name="priority"></a>Pirmenybė
Dimensijos prioriteto nustatymas padeda „Project Service“ kainodarai sukurti kainą netgi tada, kai ji negali rasti tikslaus įvesties dimensijos reikšmių ir reikšmių iš lentelių **Vaidmens kaina** arba **Vaidmens kainos antkainis** atitikties. Tokiu atveju „Project Service“ naudos nulines nesutampančių dimensijos reikšmių reikšmes įvertindama dimensijas pagal jų prioritetų tvarką.

- **Savikainos prioritetas**: dimensijos savikainos prioriteto reikšmė nurodys dimensijos įvertinimą lygindama su savikainos sąranka. **Savikainos prioriteto** reikšmė turi būti unikali visose dimensijose, kurios taikomos **Taikoma savikainai**.
- **Pardavimo prioritetas**: dimensijos pardavimo prioriteto reikšmė nurodys dimensijos įvertinimą lygindama su pardavimo kainų arba sąskaitų tarifų sąranka. **Pardavimo prioriteto** reikšmė turi būti unikali visose dimensijose, kurios taikomos **Taikoma pardavimui**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
