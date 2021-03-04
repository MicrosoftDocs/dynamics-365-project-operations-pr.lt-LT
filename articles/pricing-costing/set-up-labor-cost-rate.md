---
title: Darbo sąnaudų tarifų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti darbo savikainos tarifus naudojant „Project Operations“
author: rumant
manager: Annbe
ms.date: 10/12/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 697129b65f53359615ea537fe135d657748dd909
ms.sourcegitcommit: f6f86e80dfef15a7b5f9174b55dddf410522f7c8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/31/2020
ms.locfileid: "4180607"
---
# <a name="set-up-labor-cost-rates"></a>Darbo sąnaudų tarifų nustatymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Kiekviename kainoraštyje yra darbo tarifų (vaidmens kainos) rinkinys, kuris derinamas su kainoraščio turiniu ir galiojimo data.

1. Sukurkite kainoraštį ir skirtuke **Vaidmens kaina** papildomo tinklelio eilutėje pasirinkite **Naujas vaidmuo**.
2. Puslapyje **Spartusis kūrimas** pasirinkite vaidmenį ir organizacijos vienetą.
3. Laukuose įveskite kitą būtiną informaciją.

Šioje lentelėje yra laukų, kurie svarbūs savikainos kainoraštyje kuriant darbo tarifus.

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| Vaidmuo | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pasirinkite vaidmenį, kuriam taikomas savikainos tarifas. | Gaunamų įvertinimo arba faktinių reikšmių vaidmuo bus sugretintas su šia eilute, kad būtų nustatyta numatytoji vaidmens savikaina. |
| Išteklių paskirstymo įmonė | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pasirinkite juridinį subjektą, kuriam priskirtas vaidmuo. Pavyzdžiui, kūrėjas iš „Fabrikam India“arba kūrėjas iš „Fabrikam USA“. | Gaunamų įvertinimo arba faktinių reikšmių išteklių paskirstymo įmonė bus sugretinta su šia eilute, kad būtų nustatytas numatytasis vaidmens savikainos tarifas. |
| Išteklių paskirstymo vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pasirinkite įmonės organizacijos vienetą arba padalinį, kur šis vaidmuo bus naudojamas. Pavyzdžiui, kūrėjas iš „Fabrikam India“ robotų padalinio arba kūrėjas iš „Fabrikam USA“ programinės įrangos padalinio. | Gaunamų įvertinimo arba faktinių reikšmių išteklių paskirstymo vienetas bus sugretintas su šia eilute, kad būtų nustatyta numatytoji vaidmens savikaina. |
| Kainos | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Nustatykite vaidmens, išteklių paskirstymo įmonės ir išteklių paskirstymo vieneto derinio savikainos tarifą. Pavyzdžiui, kūrėjas iš „Fabrikam India“ kainuoja 1000 INR arba kūrėjas iš „Fabrikam USA“ kainuoja 150 USD. | Kaina yra numatytasis savikainos tarifas, nustatomas gaunamo įvertinimo arba faktinės **Laiko** operacijos klasės eilutės vieneto savikainai. |
| Valiuta | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pagal numatytuosius nustatymus valiutos reikšmė gaunama iš savikainos kainoraščio antraštės valiutos, bet ją galima perrašyti. Pavyzdžiui, „Fabrikam India“ kūrėjas kainuoja 1000 INR. „Fabrikam USA“ kūrėjas kainuoja 150 USD. | Ši numatytoji valiuta taikoma gaunamai faktinei **Laiko** operacijos klasės sąnaudų eilutei (vieneto savikainai). Projekto įvertinime valiutos reikšmė konvertuojama į projekto valiutą ir parodoma įvertinimo laipsniškai laike išdėstytame rodinyje. |
| Vieneto grafikas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Numatytasis vieneto grafikas yra laikas ir jo negalima pakeisti vaidmens kainos objekte, nes jis naudoja skubius tarifus pagal laiko vienetus. | Tai neturi poveikio tolesniam procesui. |
| Vienetas | Skirtukas **Bendra** ir **Sparčiojo kūrimo** puslapiai | Pagal numatytuosius nustatymus reikšmė gaunama iš lauko **Laiko vienetas**, esančio savikainos kainoraščio antraštėje. Reikšmės negalima perrašyti. Pavyzdžiui, „Fabrikam India“ kūrėjas kainuoja 1000 INR už **Indijos dieną**. „Fabrikam USA“ kūrėjas kainuoja 150 USD už **JAV dieną**. | Sistema naudoja vienetų sistemą ir konvertavimą pradiniais vienetais, kad apskaičiuotų vieneto savikainą ir numatytąją vieneto kainą gaunamo įvertinimo arba faktinėje eilutėje. Pavyzdžiui, skaičiuojamas kūrėjo iš Indijos 10 **Indijos dienų** darbo vertės įvertinimas, o vienetas **Indijos diena** apibrėžiamas kaip 10 valandų. Įkainojant šią įvertinimo eilutę, programa apskaičiuoja įvertinimo vieneto savikainą: 1000 INR / 10 valandų = 100 INR už valandą, kuri konvertuojama į USD ir rodoma kaip vieneto savikaina puslapyje **Projektų įvertinimai**. |

## <a name="transfer-pricing-and-costs-for-resources-outside-of-your-division-or-legal-entity"></a>Išteklių kainodaros ir išlaidų perkėlimas už savo padalinio arba juridinio subjekto ribų

Projektų įmonėse projektams vykdyti įprasta naudoti darbuotojus iš skirtingų juridinių subjektų arba padalinių. Projektą gali vykdyti vienas juridinis asmuo, tačiau su projektu dirbantys darbuotojai arba konsultantai gali būti iš to paties juridinio subjekto arba iš skirtingų – galimas ir abiejų variantų derinys. Naudojant „Dynamics 365 Project Operations“ juridinis subjektas, kuris pristato projektą, yra **Valdančioji įmonė**, o pristatantis padalinys yra **Sutartį sudarantis vienetas**. Kiti juridiniai subjektai, kurie tiekia išteklius, yra **Išteklių paskirstymo įmonės**, o padaliniai, kurie tiekia išteklius, yra **Išteklių paskirstymo vienetai**. Daugelyje šalių įmonės privalo užtikrinti, kad išteklių paskirstymo juridinis subjektas arba padalinys prašytų valdančiosios įmonės ir sutartį sudarančio vieneto sumokėti už išteklių naudojimą.

Pavyzdžiui, „Fabrikam Corporation“ turi užtikrinti, kad „Fabrikam India-Robotics“ susitarė dėl savikainos tarifo kortelės su „Fabrikam US-Robotics“ arba „Fabrikam UK-Robotics“.

Kūrėjas iš „Fabrikam India-Robotic“ kainuoja 100 USD, kai paskolinamas „Fabrikam US-Robotics“, ir 150 USD, kai paskolinamas „Fabrikam U-Robotics“.

### <a name="set-up-costs-for-outside-resources"></a>Išorinių išteklių išlaidų nustatymas

1. Sukurkite savikainos kainoraštį pavadinimu *„Fabrikam US-Robotics“ savikainos tarifai* ir nustatykite galiojimo datų intervalą.
2. Savikainos kainoraštyje nustatykite tarifus naudodami informaciją iš toliau pateiktos lentelės. 

| Vaidmuo | Išteklių paskirstymo įmonė | Išteklių paskirstymo vienetas | Savikainos tarifas |
| --- | --- | --- | --- |
| Programų kūrėjas | „Fabrikam India“ | „Fabrikam India-Robotics“ | 100 JAV dol. |
| Programų kūrėjas | „Fabrikam Philippines“ | „Fabrikam Philippines-Robotics“ | 90 USD |
| Programų kūrėjas | „Fabrikam US“ | „Fabrikam US-Robotics“ | 150 USD |

3. Šį savikainos kainoraštį pridėkite prie „Fabrikam US-Robotics“ organizacijos vieneto.

### <a name="set-up-transfer-pricing-for-a-resource-in-the-appropriate-currency"></a>Ištekliaus perdavimo kainodaros nustatymas atitinkama valiuta 

Naudojant „Project Operations“ išteklių kainodarą galima nustatyti bet kuria valiuta. Numatytoji valiuta sutampa su kainoraščio antraštės valiuta, bet ją galima pakeisti.

Naudojant perdavimo kainos nustatymo pavyzdį informaciją galima pakeisti į:

„Fabrikam Corporation“ turi užtikrinti, kad „Fabrikam India-Robotics“ susitarė dėl savikainos tarifo su „Fabrikam US-Robotics“ arba „Fabrikam UK-Robotics“.

Kūrėjas iš „Fabrikam India-Robotics“ kainuoja 5000 INR, kai paskolinamas „Fabrikam US-Robotics“, ir 5500 INR, kai paskolinamas „Fabrikam UK-Robotics“.

„Fabrikam US-Robotics“ savikainos kainoraštyje savikainos tarifus galima išreikšti taip:

| Vaidmuo | Išteklių paskirstymo įmonė | Savikaina |
| --- | --- | --- |
| Programų kūrėjas | „Fabrikam India“ | 5000 INR |
| Programų kūrėjas | „Fabrikam US“ | 115 USD |

„Fabrikam UK-Robotics“ savikainos kainoraštyje savikainos tarifus galima išreikšti taip:

| Vaidmuo | Išteklių įmonė | Savikaina |
| --- | --- | --- |
| Programų kūrėjas | „Fabrikam India“ | 5500 INR |
| Programų kūrėjas | „Fabrikam UK“ | 115 GBP |

Savikainos kainoraštis gali pateikti darbo tarifus keliomis valiutomis. Generuojant projekto savikainos įvertinimą „Project Operations“ konvertuos šiuos savikainos tarifus į projekto valiutą ir parodys vartotojui. Kai patvirtinamas laiko įrašas ir sukuriama faktinė savikaina, ji išreiškiama valiuta, kuri nurodyta savikainos kainoraščio vaidmens kainos eilutėje. Faktinė vieno projekto laiko savikaina gali būti įrašyta keliomis valiutomis. Tačiau, kai projekto lygyje sumuojamos faktinės darbo išlaidos, „Project Operations“ konvertuos visas darbo savikainos sumas į projekto valiutą, kurią naudotojas gali matyti.


[!INCLUDE[footer-include](../includes/footer-banner.md)]