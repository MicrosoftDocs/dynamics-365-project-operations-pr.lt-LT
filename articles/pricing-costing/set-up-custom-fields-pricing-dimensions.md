---
title: Pasirinktinių laukų kaip kainodaros dimensijų nustatymas
description: Šioje temoje pateikiama informacija apie tai, kaip nustatyti kainodaros dimensijas naudojant pasirinktinius laukus.
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 41c65d6bf64d8a81759239f2a31f3a68953181c8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599418"
---
# <a name="set-up-custom-fields-as-pricing-dimensions"></a>Pasirinktinių laukų kaip kainodaros dimensijų nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Prieš pradedant, šioje temoje daroma prielaida, kad atlikote temose [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities-pricing-dimensions.md) ir [Būtinų pasirinktinių laukų įtraukimas į kainos sąranką ir operacijų objektus](add-custom-fields-price-setup-transactional-entities.md)  nurodytas procedūras. Jei neatlikote šių procedūrų, grįžkite ir jas atlikite, o tada grįžkite į šią temą. 

Šioje temoje pateikiama informacija apie tai, kaip nustatyti pasirinktines kainodaros dimensijas. Puslapyje **Parametrai**, skirtuke **Suma pagrįstos kainodaros dimensijos** rodomi kainodaros dimensijų objektų įrašai. Pagal numatytuosius nustatymus šiame skirtuke tinklelyje yra dvi eilutės:

- **msdyn_resourcecategory** (vaidmuo)
- **msdyn_OrganizationalUnit** (organizacinis vienetas)

> [!IMPORTANT]
> Nenaikinkite šių eilučių. Tačiau, jei jums jų nereikia, padarykite juos netaikomais konkrečiame kontekste nustatydami **Taikoma savikainai**, **Taikoma pardavimui** ir **Taikoma pirkimui** kaip **Ne**. Nustačius šias atributų reikšmes kaip **Ne**, tai turi tokį patį poveikį kaip kainodaros dimensijos lauko neturėjimas.

Kad laukas taptų kainodaros dimensija, jis turi:

- Būti sukurtas kaip laukas objektuose **Vaidmens kaina** ir **Vaidmens kainos antkainis**. Daugiau informacijos apie tai, kaip tai padaryti, žr. [Pasirinktinių laukų įtraukimas į kainos sąranką ir operacijų objektus](add-custom-fields-price-setup-transactional-entities.md).

- Būti sukurtas kaip eilutė lentelėje **Kainodaros dimensija**. Pavyzdžiui, įtraukite kainodaros dimensijos eilutes kaip parodyta toliau pateiktame paveiksle. 

![Suma pagrįstos kainodaros dimensijos eilutės.](media/Amt-based-PD.png)

Išteklių darbo valandos (**msdyn_resourceworkhours**) įtrauktos kaip antkainiu pagrįsta dimensija ir įtrauktos į tinklelį skirtuke **Antkainiu pagrįsta kainodaros dimensija**.

![Antkainiu pagrįstos kainodaros dimensijos eilutės.](media/Markup-based-PD.png)


> [!IMPORTANT]
> Bet koks esamas arba naujas kainodaros dimensijos duomenų pakeitimas šioje eilutėje yra perkeliamas į kainodaros verslo logiką, tik kai atnaujinama talpykla. Talpyklos atnaujinimo laikas gali užtrukti iki 10 minučių. Leiskite šį laiką, kad matytumėte pakeitimus kainos numatytoje logikoje, kurie turi būti kainodaros dimensijos duomenų pakeitimų rezultatas.


## <a name="attributes-of-the-pricing-dimensions-table"></a>Kainodaros dimensijų lentelės atributai
Tolesniuose skyriuose pateikiama informacija apie skirtingus atributus lentelėje **Kainodaros dimensijos**.

### <a name="pricing-dimension-name"></a>Kainodaros dimensijos pavadinimas
Ši reikšmė turi būti tokia pati kaip ir lauko, kuris įtrauktas į pasirinktinių kainodaros dimensijų lentelę **Vaidmens kaina**, schemos pavadinimas. Daugiau informacijos apie tai, kaip įtraukti laikus į lentelę **Vaidmens kaina**, žr. [Pasirinktinių laukų įtraukimas į kainos sąranką ir operacijų objektus](add-custom-fields-price-setup-transactional-entities.md).

### <a name="type-of-dimension"></a>Dimensijos tipas
Yra dviejų tipų kainodaros dimensijos:
  
  - **Suma pagrįstos dimensijos**: dimensijų reikšmės iš įvesties konteksto yra sugretinamos su dimensijų reikšmėmis eilutėje **Vaidmens kaina** ir kaina / savikaina pagal numatytuosius parametrus tiesiogiai nustatoma iš lentelės **Vaidmens kaina**.
  - **Antkainiu pagrįstos dimensijos** – tai yra dimensijos, kuriose naudojamas toliau nurodytas 3 veiksmų proceas kainai / savikainai gauti:
 
    1. Dimensijos, kurios nėra pagrįstos antkainiu, reikšmės iš įvesties konteksto sugretinamos su vaidmens kainos eilute, kad būtų gautas bazinis tarifas.
    2. Dimensijų reikšmės iš įvesties konteksto sugretinamos su eilute **Vaidmens kainos antkainis**, kad būtų gautas antkainio procentas.
    3. Antkainio procentas iš antrojo veiksmo taikomas baziniam tarifui, gautam iš lentelės **Vaidmens kaina** pirmojo veiksmo metu, kad būtų gauta galutinė kaina / savikaina.
   
   Toliau pateiktoje lentelėje parodomas kainos antkainių skaičiavimas.
  
| Vaidmuo        | Org. vienetai    |Darbo vieta      |Standartinis pavadinimas      |Išteklių darbo valandos      |  Antkainis|
| ------------|-------------|-------------------|--------------------|-------------------------|--------:|
|             | Contoso India|Vietoje            |                    |Viršvalandžiai                 |15     |
|             | Contoso India|Vietinis             |                    |Viršvalandžiai                 |10     |
|             | „Danys“, JAV   |Vietinis             |                    |Viršvalandžiai                 |20     |


Jei ištekliai iš „Contoso India“, kurių bazinis tarifas yra 100 USD, dirba internetu, ir jie laiko įraše užregistruoja 8 reguliaraus laiko valandas ir 2 valandas viršvalandžių, kainodaros modulis naudos 100 bazinį tarifą už 8 valandas įrašui 800 USD. Už 2 valandas viršvalandžių 100 baziniam tarifui bus taikomas 15 % antkainis, kad būtų gauta 115 USD vieneto kaina, ir įrašys bendrą savikainą, lygią 230 USD.

### <a name="applicable-to-cost"></a>Taikoma savikainai 
Jei tai nustatyta kaip **Taip**, tai nurodo, kad dimensijos reikšmė iš įvesties konteksto turi būti naudojama, siekiant suderinti **Vaidmens kaina** ir **Vaidmens kainos antkainis**, kai gaunami savikainos ir antkainio tarifai.

### <a name="applicable-to-sales"></a>Taikoma pardavimui
Jei tai nustatyta kaip **Taip**, tai nurodo, kad dimensijos reikšmė iš įvesties konteksto turi būti naudojama, siekiant suderinti **Vaidmens kaina** ir **Vaidmens kainos antkainis**, kai gaunami sąskaitų ir antkainio tarifai.

### <a name="applicable-to-purchase"></a>Taikoma pirkimui
Jei tai nustatyta kaip **Taip**, tai nurodo, kad dimensijos reikšmė iš įvesties konteksto turi būti naudojama, siekiant suderinti **Vaidmens kaina** ir **Vaidmens kainos antkainis**, kai gaunama pirkimo kaina. Subrangos scenarijai nepalaikomi, todėl šis laukas nenaudojamas. 

### <a name="priority"></a>Pirmumas
Dimensijos prioriteto nustatymas padeda kainodarai sukurti kainą netgi tada, kai ji negali rasti tikslaus įvesties dimensijos reikšmių ir reikšmių iš lentelių **Vaidmens kaina** arba **Vaidmens kainos antkainis** atitikties. Tokiu atveju naudojamos nulines nesutampančių dimensijos reikšmių reikšmės įvertinant dimensijas pagal jų prioritetų tvarką.

- **Savikainos prioritetas**: dimensijos savikainos prioriteto reikšmė nurodys dimensijos įvertinimą lygindama su savikainos sąranka. **Savikainos prioriteto** reikšmė turi būti unikali visose dimensijose, kurios taikomos **Taikoma savikainai**.
- **Pardavimo prioritetas**: dimensijos pardavimo prioriteto reikšmė nurodys dimensijos įvertinimą lygindama su pardavimo kainų arba sąskaitų tarifų sąranka. **Pardavimo prioriteto** reikšmė turi būti unikali visose dimensijose, kurios taikomos **Taikoma pardavimui**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]