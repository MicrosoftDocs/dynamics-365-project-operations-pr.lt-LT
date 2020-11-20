---
title: Išlaidų savikainos ir pardavimo tarifų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti operacijų ir išlaidų kategorijų išlaidų bei pardavimo tarifus.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e5a2402a2c1059ff11dbe1a331a028da77958235
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080755"
---
# <a name="set-up-cost-and-sales-rates-for-expenses"></a>Išlaidų savikainos ir pardavimo tarifų nustatymas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Galite nustatyti operacijų kategorijų savikainą ir pardavimo kainas naudodami „Dynamics 365 Project Operations“. Kadangi savikaina ir pardavimo kainos sukurtos išlaidoms, kiekviena jų operacijos kategorija taip pat turi būti nustatyta kaip išlaidų kategorija. Šis nustatymas užtikrina tikslumą naudojant tolesnio proceso funkcijas. Operacijų kategorijų savikainą ir pardavimo kainas galima nurodyti tik viena valiuta, kuri nurodyta kainoraščio antraštėje.

Norėdami nustatyti operacijų kategorijų savikainos ir pardavimo tarifus, atlikite toliau nurodytus veiksmus. 

1. Sukurkite kainoraštį pagrįstą kainoraščio antrašte. 
2. Papildomo tinklelio meniu parinktyje **Kategorijų kainos** pasirinkite **+ Naujos kategorijos kaina**. 
3. Puslapyje **Spartusis kūrimas** įveskite operacijos kategoriją ir vienetą, kuriam kuriate naują kainą.

Toliau esančioje lentelėje išvardijami laukai skirtuke **Bendra** ir kategorijos kainos eilutės puslapyje **Spartusis kūrimas** , kuriuos turite turėti omenyje kurdami kategorijų kainas pardavimo arba savikainos sąraše.

| Laukas | Vieta | Atitiktis, tikslas ir gairės | Tolesnis poveikis |
| --- | --- | --- | --- |
| Operacijos kategorija | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pasirinkite operacijos kategoriją, kuriai kuriate pardavimą arba savikainą. | Gaunamo išlaidų įvertinimo arba faktinių išlaidų operacijos kategorija bus sugretinta su šia eilute, kad būtų nustatytas numatytasis operacijos kategorijos savikainos arba pardavimo tarifas. |
| Vieneto grafikas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Numatytasis vieneto grafikas nustatomas pagal operacijos kategorijos vieneto grafiką. | Nėra jokio tolesnio šio lauko poveikio. |
| Vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pasirinkite vienetą, kuriam nustatomi tarifai. | Gaunamo įvertinimo arba faktinio dydžio vienetas sugretinamas su šios eilutės vienetu, kad būtų nustatytas numatytasis įvertintų arba faktinių išlaidų tarifas. |
| Kainodaros metodas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Galimos lauko **Kainodaros metodas** reikšmės yra **Vieneto kaina** , **Savikaina** ir **Antkainis prie savikainos**. | Nustatant kainą ir pasirinkus **Vieneto kaina** , kategorijos kainos eilutėje užrakinamas laukas **Procentas**. Jei pasirinkta **Savikaina** , laukai **Kaina** ir **Procentas** užrakinami pardavimo kainoraštyje. Pasirinkus **Antkainis prie savikainos** , pardavimo kainoraštyje užrakinamas laukas **Kainas**. Gaunamoje faktinėje išlaidų eilutėje kainodaros metodas **Savikaina** arba **Antkainis prie savikainos** lemia, kad atitinkamoje pardavimo eilutėje (kuriai neišrašyta sąskaita) priskiriama kaina, lygi faktinei savikainai arba apskaičiuota kaip antkainis. |
| Kainos | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Nustatykite operacijos kategorijos ir vieneto derinio tarifą. Pavyzdžiui, kilometražo tarifas yra 10 USD vienai myliai ir 8 USD vienam kilometrui. | Kilometražo tarifas bus numatytasis tarifas, nustatomas gaunamam įvertinimui arba faktinei išlaidų operacijos klasės eilutei pagal vieneto kainą arba savikainą.|
| Procentas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Nustatykite operacijos kategorijos ir vieneto derinio prie savikainos pridedamą procentą. Pavyzdžiui, lėktuvo bilieto pardavimo tarifas turi būti 10 proc. didesnis nei bilieto pardavimo savikaina. | Šis prie savikainos pridedamas procentas taikomas tik pardavimo kainoraštyje, kai pasirinktas kainodaros metodas **Antkainis prie savikainos**. |
| Valiuta | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pagal numatytuosius nustatymus ši reikšmė gaunama naudojant kainoraščio antraštės valiutą. Operacijos kategorijos kainodaroje valiutos negalima perrašyti. | Ši numatytoji valiuta taikoma gaunamai faktinei išlaidų operacijos klasės eilutei (savikaina ir pardavimas). |

## <a name="pricing-methods-for-expenses"></a>Išlaidų kainodaros metodai

Nustatę kategorijų kainas, kurios svarbios tik išlaidų kainodaros kontekste, galite naudoti vieną iš trijų kainodaros metodų:

- **Vieneto kaina**
- **Savikaina**
- **Antkainis prie savikainos**

### <a name="price-per-unit"></a>Vieneto kaina
Kai šis kainodaros metodas pasirenkamas kategorijos kainos eilutėje, susietoje su pardavimo kainoraščiu, nustatoma numatytoji kategorijos ir vieneto derinio kaina (įvertinta ir faktinė). Įvertinimas rodo apytikres išlaidų eilutes, pasiūlymo eilutės išlaidų duomenis ir sutarties eilutės išlaidų duomenis.

### <a name="at-cost"></a>Savikaina
Kai šis kainodaros metodas pasirenkamas kategorijos kainos eilutėje, susietoje su pardavimo kainoraščiu, nustatoma numatytoji kategorijos ir vieneto derinio kaina (tik faktinėms išlaidoms). Pavyzdžiui, išlaidų operacijos klasės faktinis pardavimas, kuriam neišrašyta sąskaita faktūra. Vieneto kaina nustatoma pagal faktinį pardavimą, kuriam neišrašyta sąskaita faktūra, naudojant tų išlaidų faktinės savikainos vieneto kainą. Numatytųjų kainų nustatymas pagal savikainą nevykdomas projekto išlaidų įvertinimui arba išlaidų pasiūlymo eilutei ir sutarties eilutės duomenims.

### <a name="markup-over-cost"></a>Antkainis prie savikainos
Kai šis kainodaros metodas pasirenkamas kategorijos kainos eilutėje, susietoje su pardavimo kainoraščiu, nustatoma numatytoji kategorijos ir vieneto derinio kaina (tik faktinėms išlaidoms). Pavyzdžiui, išlaidų operacijos klasės faktinis pardavimas, kuriam neišrašyta sąskaita faktūra. Ši vieneto kaina nustatoma faktiniam pardavimui, kuriam neišrašyta sąskaita faktūra, naudojant pagal vieneto kainą (faktinė savikaina) apskaičiuotą vertę pritaikius nustatytą antkainį. Numatytųjų kainų nustatymas pagal savikainą nevykdomas projekto išlaidų įvertinimui arba išlaidų pasiūlymo eilutei ir sutarties eilutės duomenims.