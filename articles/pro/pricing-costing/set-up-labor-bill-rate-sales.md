---
title: Darbo sąskaitų tarifų sąranka – „Lite“ versija
description: Šiame straipsnyje pateikiama informacija apie darbo atsiskaitymo tarifų nustatymą projekto operacijose.
author: rumant
ms.date: 10/16/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 443132797f20c961b42ed20340e74f420965526f
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8917448"
---
# <a name="set-up-labor-bill-rates---lite"></a>Darbo sąskaitų tarifų sąranka – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Kiekviename kainoraštyje yra galiojančių vaidmenų kainų arba darbo tarifų rinkinys ir galiojimo data, įtraukta į kainoraščio antraštę. Sąskaitų tarifai už laiką programoje „Dynamics 365 Project Operations“ gali būti nustatyti tik viena valiuta, kuri yra nurodyta kainoraščio antraštėje.

1. Jei norite nustatyti pardavimo kainoraščio darbo sąskaitų tarifus, sukurkite kainoraštį pagal kainoraščio antraštę. 
2. Skirtuke **Vaidmenų kainos**, papildomame tinklelyje, pasirinkite **+ Naujo vaidmens kaina**. 
3. **Sparčiojo kūrimo** srityje įveskite vaidmens ir organizacijos vieneto derinį, kuriam norite nustatyti sąskaitos tarifą.

  Toliau esančioje lentelėje yra laukai skirtuke **Bendra** ir vaidmens kainos eilutės **Sparčiojo kūrimo** sritis, kuriuos reikia turėti omenyje kuriant vaidmenų kainas pardavimo kainoraštyje:

  | Laukas | Vieta | Aprašo | Tolesnis poveikis |
  | --- | --- | --- | --- |
  | Vaidmuo | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Pasirinkite vaidmenį, kuriam nustatote sąskaitos tarifą. | Gaunamų įvertinimo arba faktinių reikšmių vaidmuo bus sugretintas su šia eilute, kad būtų nustatytas numatytasis vaidmens sąskaitos tarifas. |
  | Išteklių paskirstymo vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Pasirinkite įmonės organizacijos vienetą arba padalinį, kuriam priklauso šis vaidmuo. Pavyzdžiui, kūrėjas iš „Fabrikam India“ robotų padalinio arba kūrėjas iš „Fabrikam USA“ programinės įrangos padalinio. | Gaunamų įvertinimo arba faktinių reikšmių išteklių paskirstymo vienetas bus sugretintas su šia eilute, kad būtų nustatytas numatytasis vaidmens sąskaitos tarifas. |
  | Kainos | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Nustatykite vaidmens, išteklių paskirstymo įmonės ir išteklių paskirstymo vieneto derinio sąskaitos tarifą. Pavyzdžiui, „Fabrikam India“ kūrėjo sąskaitos tarifas yra 100 USD, o „Fabrikam USA“ kūrėjo sąskaitos tarifas 150 USD. | Ši kaina yra numatytasis sąskaitos tarifas, nustatomas gaunamo įvertinimo arba faktinės laiko operacijos klasės eilutės vieneto kainai. |
  | Valiuta | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis| Pagal numatytuosius nustatymus valiutos reikšmė gaunama naudojant pardavimo kainoraščio antraštės valiutą. Pardavimo kainoraštyje valiutos negalima perrašyti. | Ši valiuta yra numatytoji valiuta, taikoma gaunamos faktinės pardavimo eilutės (laiko operacijos klasė) vieneto kainai. |
  | Vieneto grafikas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Šis numatytasis vieneto grafikas yra laikas ir jo negalima pakeisti vaidmens kainos objekte, nes jis naudoja skubius tarifus pagal laiko vienetus. | Nėra jokio tolesnio šio lauko poveikio. |
  | Vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Vieneto vertė gaunama iš pardavimo kainoraščio antraštės lauko **Laiko vienetas**. Tačiau reikšmės negalima perrašyti. Pavyzdžiui, „Fabrikam India“ kūrėjo sąskaitos tarifas yra 1000 USD už **Indijos dieną**. „Fabrikam USA“ kūrėjo sąskaitos tarifas yra 1500 USD už **JAV dieną**. | Sistema naudoja vienetų sistemą ir konvertavimą pradiniais vienetais, kad apskaičiuotų vieneto kainą ir numatytąją vieneto kainą gaunamo įvertinimo arba faktinėje eilutėje. Pavyzdžiui, skaičiuojamas kūrėjo iš Indijos 10 **Indijos dienų** darbo vertės įvertinimas, o vienetas Indijos diena apibrėžiamas kaip 10 valandų. Įkainojant šią įvertinimo eilutę, programa apskaičiuoja vieneto kainą taip: 1000 USD / 10 valandų = 100 USD už valandą. |


## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Kitų organizacijos vienetų arba padalinių kainodaros perkėlimas arba išteklių sąskaitų tarifų nustatymas 

Projektų įmonės projektams vykdyti gali naudoti darbuotojus iš skirtingų įmonės padalinių. Projektus galima vykdyti iš vieno padalinio, o darbuotojai arba konsultantai gali susirinkti ir iš skirtingų įmonės padalinių. Su projektu taip pat gali dirbti žmonės iš skirtingų padalinių. Naudojant „Project Operations“ projektą pristatanti įmonė vadinama **Sutartį sudarančiu vienetu**. Visi kiti išteklius teikiantys padaliniai vadinami **Išteklių paskirstymo vienetais**. Dėl darbo išlaidų skirtumų įvairiose pasaulio vietovėse ir darbo rinkose darbo sąskaitų tarifai taip pat apskaičiuojami skirtingai.

Pavyzdžiui, kūrėjui iš „Fabrikam India“, dirbančios su JAV projektu, išrašyta sąskaita taikant 100 USD valandinį tarifą. Kūrėjui iš „Fabrikam US“, dirbančiam su JAV projektu, išrašyta sąskaita taikant 150 USD valandinį tarifą.

### <a name="example-set-up-a-bill-rate"></a>Pavyzdys: sąskaitos tarifo nustatymas

1. Sukurkite pardavimo kainoraštį pavadinimu *„Fabrikam US“ sąskaitų tarifai* ir nustatykite galiojimo datą.
2. Pardavimo kainoraštyje įveskite tokią tarifo informaciją:

    | Vaidmuo | Organizacijos vienetas | Sąskaitos tarifas |
    | --- | --- | --- |
    | Programų kūrėjas | „Fabrikam India“ | 100 JAV dol. |
    | Programų kūrėjas | „Fabrikam Philippines“ | 90 USD |
    | Programų kūrėjas | „Fabrikam US“ | 150 USD |

3. Pridėkite pardavimo kainoraštį **„Fabrikam US“ sąskaitų tarifai** prie projekto sutarties kainoraščio arba prie tam tikro kliento.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]