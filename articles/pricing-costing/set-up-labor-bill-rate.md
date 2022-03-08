---
title: Darbo sąskaitų tarifų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti atsiskaitymo už darbą tarifus naudojant „Project Operations“.
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0fee2c98713f4d1f8da85a0b60fb3fc2a873e5f82a64cf350ebeb68fe65fab35
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7003556"
---
# <a name="set-up-labor-bill-rates"></a>Darbo sąskaitų tarifų sąranka

_ **Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

Kiekviename kainoraštyje yra galiojančių vaidmenų kainų arba darbo tarifų rinkinys ir galiojimo data, įtraukta į kainoraščio antraštę. Sąskaitų tarifai už laiką programoje „Dynamics 365 Project Operations“ gali būti nustatyti tik viena valiuta, kuri yra nurodyta kainoraščio antraštėje.

1. Norėdami nustatyti pardavimo kainoraščio sąskaitų tarifus, eikite į **Pardavimas** > **Klientai** > **Kainoraščiai** ir pasirinkite **Naujas**, kad sukurtumėte naują kainoraštį. 
2. Skirtuke **Vaidmenų kainos**, papildomame tinklelyje, pasirinkite **Naujo vaidmens kaina**. 
3. **Sparčiojo kūrimo** srityje įveskite vaidmens ir organizacijos vieneto derinį, kuriam norite nustatyti sąskaitos tarifą.

   Toliau esančioje lentelėje yra laukai skirtuke **Bendra** ir vaidmens kainos eilutės **Sparčiojo kūrimo** sritis, kuriuos reikia turėti omenyje kuriant vaidmenų kainas pardavimo kainoraštyje:

    | Laukas | Vieta | Aprašo | Tolesnis poveikis |
    | --- | --- | --- | --- |
    | Vaidmuo | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Pasirinkite vaidmenį, kuriam nustatote sąskaitos tarifą. | Gaunamų įvertinimo arba faktinių reikšmių vaidmuo bus sugretintas su šia eilute, kad būtų nustatytas numatytasis vaidmens sąskaitos tarifas. |
    | Išteklių paskirstymo įmonė | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Pasirinkite įmonę arba juridinį subjektą, kuriam priklauso vaidmuo. Pavyzdžiui, kūrėjas iš „Fabrikam India“arba kūrėjas iš „Fabrikam USA“. | Gaunamų įvertinimo arba faktinių reikšmių išteklių paskirstymo įmonė bus sugretinta su šia eilute, kad būtų nustatytas numatytasis vaidmens sąskaitos tarifas. |
    | Išteklių paskirstymo vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Pasirinkite įmonės organizacijos vienetą arba padalinį, kuriam priklauso šis vaidmuo. Pavyzdžiui, kūrėjas iš „Fabrikam India“ robotų padalinio arba kūrėjas iš „Fabrikam USA“ programinės įrangos padalinio. | Gaunamų įvertinimo arba faktinių reikšmių išteklių paskirstymo vienetas bus sugretintas su šia eilute, kad būtų nustatytas numatytasis vaidmens sąskaitos tarifas. |
    | Kainos | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Nustatykite vaidmens, išteklių paskirstymo įmonės ir išteklių paskirstymo vieneto derinio sąskaitos tarifą. Pavyzdžiui, „Fabrikam India“ kūrėjo sąskaitos tarifas yra 100 USD, o „Fabrikam USA“ kūrėjo sąskaitos tarifas 150 USD. | Ši kaina yra numatytasis sąskaitos tarifas, nustatomas gaunamo įvertinimo arba faktinės laiko operacijos klasės eilutės vieneto kainai. |
    | Valiuta | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis| Pagal numatytuosius nustatymus valiutos reikšmė gaunama naudojant pardavimo kainoraščio antraštės valiutą. Pardavimo kainoraštyje valiutos negalima perrašyti. | Ši valiuta yra numatytoji valiuta, taikoma gaunamos faktinės pardavimo eilutės (laiko operacijos klasė) vieneto kainai. |
    | Vieneto grafikas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Šis numatytasis vieneto grafikas yra laikas ir jo negalima pakeisti vaidmens kainos objekte, nes jis naudoja skubius tarifus pagal laiko vienetus. | Nėra jokio tolesnio šio lauko poveikio. |
    | Vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** sritis | Vieneto vertė gaunama iš pardavimo kainoraščio antraštės lauko **Laiko vienetas**. Tačiau reikšmės negalima perrašyti. Pavyzdžiui, „Fabrikam India“ kūrėjo sąskaitos tarifas yra 1000 USD už **Indijos dieną**. „Fabrikam USA“ kūrėjo sąskaitos tarifas yra 1500 USD už **JAV dieną**. | Sistema naudoja vienetų sistemą ir konvertavimą pradiniais vienetais, kad apskaičiuotų vieneto kainą ir numatytąją vieneto kainą gaunamo įvertinimo arba faktinėje eilutėje. Pavyzdžiui, skaičiuojamas kūrėjo iš Indijos 10 **Indijos dienų** darbo vertės įvertinimas, o vienetas Indijos diena apibrėžiamas kaip 10 valandų. Įkainojant šią įvertinimo eilutę, programa apskaičiuoja vieneto kainą taip: 1000 USD / 10 valandų = 100 USD už valandą. |

## <a name="transfer-pricing-or-set-up-bill-rates-for-resources-from-other-organizational-units-or-divisions"></a>Kitų organizacijos vienetų arba padalinių kainodaros perkėlimas arba išteklių sąskaitų tarifų nustatymas 

Projektų įmonės dažnai juridiniame subjekte vykdant projektą naudoja darbuotojus iš kitų juridinių subjektų ir padalinių. Projektus gali vykdyti tam tikras juridinis subjektas ir padalinys, tačiau su projektais dirbantys darbuotojai arba konsultantai gali būti iš to paties juridinio subjekto ir padalinio arba iš skirtingų. Su projektu taip pat gali dirbti žmonės iš skirtingų juridinių subjektų ir padalinių. Naudojant „Project Operations“ juridinis subjektas, kuris pristato projektą, vadinamas **Valdančiąja įmone**, o pristatantis padalinys vadinamas **Sutartį sudarančiu vienetu**. Visi kiti juridiniai subjektai, kurie tiekia išteklius, yra vadinami **Išteklių paskirstymo įmonėmis**, o padaliniai, kurie tiekia išteklius, yra vadinami **Išteklių paskirstymo vienetais**. Dėl darbo išlaidų skirtumų įvairiose pasaulio vietovėse ir darbo rinkose darbo sąskaitų tarifai taip pat apskaičiuojami skirtingai.

Pavyzdžiui, kūrėjui iš „Fabrikam India“ robotų technikos padalinio, dirbančio su JAV projektu, išrašyta sąskaita taikant 100 USD valandinį tarifą. Kūrėjui iš „Fabrikam US“ robotų technikos padalinio, dirbančio su JAV projektu, išrašyta sąskaita taikant 150 USD valandinį tarifą. 

### <a name="example-set-up-a-bill-rate"></a>Pavyzdys: sąskaitos tarifo nustatymas 

1. Sukurkite pardavimo kainoraštį pavadinimu *„Fabrikam US“ sąskaitų tarifai* ir nustatykite galiojimo datą.
2. Pardavimo kainoraštyje įveskite tokią tarifo informaciją:

    | Vaidmuo | Išteklių įmonė | Išteklių paskirstymo vienetas | Sąskaitos tarifas |
    | --- | --- | --- | --- |
    | Programų kūrėjas | „Fabrikam India“ | „Fabrikam India - Robotics“ | 100 JAV dol. |
    | Programų kūrėjas | „Fabrikam Philippines“ | „Fabrikam Philippines - Robotics“ | 90 USD |
    | Programų kūrėjas | „Fabrikam US“ | „Fabrikam US - Robotics“ | 150 USD |

3. Pridėkite pardavimo kainoraštį **„Fabrikam US“ sąskaitų tarifai** prie projekto sutarties kainoraščio arba prie tam tikro kliento.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
