---
title: Numatytieji kainoraščiai
description: Šiame straipsnyje pateikta informacija apie numatytuosius pardavimo ir savikainos kainoraščius programoje „Project Operations“.
author: rumant
ms.date: 09/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 50dbf74e31b9eb8d63c378e5fd718dc17c9691f4
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410273"
---
# <a name="default-price-lists"></a>Numatytieji kainoraščiai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

## <a name="sales-price-lists"></a>Pardavimo kainoraščiai

Kiekviename „Dynamics 365 Project Operations“ projekto pasiūlyme ir sutartyje yra numatytasis pardavimo kainoraštis. 

### <a name="price-list-default-on-project-quotes"></a>Numatytasis projekto pasiūlymų kainoraštis
Sistema baigia toliau nurodytą procesą, kad nustatytų, kokį kainoraštį pasirinkti kaip numatytąjį projekto pasiūlymo kainoraštį.

1. Sistema atsižvelgia į kainoraščius, pridėtus prie kliento projektų kainoraščių. 
1. Jei prie kliento įrašo nepridėta jokių projekto kainoraščių, sistema atsižvelgia į pardavimo kainoraščius, pridėtus prie projekto parametrų, kurie atitinka projekto pasiūlymo valiutą.
1. Tada sistema patikrina kainoraščių, atitinkančių projekto pasiūlymo datų intervalą, įsigaliojimo datą. Konkrečiai – datą, kai pasiūlymas buvo sukurtas.
1. Jei yra keli kainoraščiai, kurie galioja projekto pasiūlymo datą, projekto pasiūlyme nustatomi visi numatytieji kainoraščiai.
1. Jei projekto pasiūlymo datą galiojančių kainoraščių nėra, projekto pasiūlyme nėra numatytojo projekto kainoraščio. Projekto pasiūlyme pasirodys įspėjamasis pranešimas. Pranešime nurodoma, kad faktinės ir įvertintos projektų sumos nebus įkainotos, nes nėra pridėtų projektų kainoraščių.

### <a name="price-list-default-on-project-contracts"></a>Numatytasis projekto sutarčių kainoraštis 
Sistema baigia toliau nurodytą procesą, kad nustatytų, kokį kainoraštį pasirinkti kaip numatytąjį projekto sutarties kainoraštį.

1. Jei sutartis sukuriama iš pasiūlymo, projekto kainoraščiai pasiūlyme yra kopijuojami atskirai ir pridedami prie projekto sutarties.
1. Jei sutartis sukuriama nuo nulio, sistema atsižvelgia į kainoraščius, pridėtus prie kliento projektų kainoraščių. Jei prie kliento įrašo nepridėti projektų kainoraščiai, sistema atsižvelgia į pardavimo kainoraščius, pridėtus prie projekto parametrų, kurie atitinka projekto sutarties valiutą.
1. Tada sistema patikrina kainoraščių, atitinkančių projekto sutarties datų intervalą, įsigaliojimo datą. Konkrečiai – datą, kai sutartis buvo sukurta.
1. Jei yra keli kainoraščiai, kurie galioja sutarties datą, sutartyje nustatomi visi numatytieji kainoraščiai.
1. Jei sutarties datą galiojančių kainoraščių nėra, sutartyje nėra numatytųjų projektų kainoraščių. Projekto sutartyje pasirodys įspėjamasis pranešimas. Pranešime nurodoma, kad faktinės ir įvertintos projektų sumos nebus įkainotos, nes nėra pridėtų projektų kainoraščių.

## <a name="cost-price-lists"></a>Savikainos kainoraščiai

Kainoraščiai nėra numatytieji jokiame „Project Operations“ objekte. Išlaidų kainoraščio, skirto projekto išlaidoms, nustatymas visada atliekamas operacijų pagrindu. Sistema baigia toliau nurodytą procesą, kad nustatytų, kokį kainoraštį naudoti projekto išlaidose.

1. Sistema ieško kainoraščių, pridėtų prie projekto sutartį sudarančio organizacijos vieneto.
1. Tada sistema peržiūri kainoraščių, atitinkančių gaunamo įvertinimo konteksto arba faktinių duomenų konteksto datą, įsigaliojimo datą.

    - *Įvertinimo kontekstas* nurodo bet kurį iš trijų „Project Operations“ įvertinimo kontekstų:

        - Projekto įvertinimo eilutė
        - Pasiūlymo eilutės informacija
        - Sutarties eilutės informacija

    - *Faktinių duomenų kontekstas* nurodo bet kurį iš trijų „Project Operations“ faktinių duomenų šaltinių:

       - Rankiniu būdu sukurtos įrašų žurnalo eilutės arba rankiniu būdu sukurtos koregavimo žurnalo eilutės, esančios koregavimo žurnale
       - Žurnalo eilutės, sukurtos pateikiant laiko, išlaidų arba medžiagos naudojimo žurnalus
       - Sąskaitos faktūros eilutės informacija

    Kai „Project Operations“ sugretina gaunamos žurnalo eilutės arba sąskaitos faktūros eilutės išsamios informacijos, esančios *faktinių duomenų kontekste*, galiojimo datą, ji naudoja lauką **Operacijos data**.

    - Jei yra keli kainoraščiai, kurie galioja gaunamo įvertinimo konteksto arba faktinių duomenų konteksto dieną, pasirenkamas vėliausiai sukurtas kainoraštis.
    - Jei prie projekto sutartį sudarančio organizacijos vieneto kainoraščiai nepridėti, sistema atsižvelgia į savikainos kainoraščius, pridėtus prie projekto parametrų, kurie atitinka projekto valiutą.

## <a name="enable-multi-currency-cost-price-list"></a>Įgalinti kelių valiutų savikainos kainoraštį

Šį parametrą galima rasti **Parametrai** \> **Parametrai**. Numatytoji reikšmė yra **Ne**.

Kai įjungtas šis parametras (t. y., reikšmė nustatyta kaip **Taip**), sistema veikia taip:

- Ji leidžia su organizacijos vienetu susieti išlaidų kainoraščius bet kuria valiuta. Pavyzdžiui, savikainos kainoraštį EUR valiuta galima pridėti prie organizacijos vieneto USD valiuta. Sistema ir toliau tikrins, ar savikainos kainoraščių, pridėtų prie organizacinio vieneto, galiojimo datos nepersidengia.
- Ji patikrina, ar prie projekto parametrų pridėtų savikainos kainoraščių galiojimo datos nepersidengia, net jei jų valiutos skiriasi. Šis veikimo būdas skiriasi nuo numatytojo (t. y., veikimo būdo, kai reikšmė nustatyta kaip **Ne**). Pagal numatytąjį veikimo būdą tikrinama, ar nepersidengia tik savikainos kainoraščių, kurių valiuta yra **tokia pati** galiojimo datos.
- Esant gaunamos operacijos kontekstui, savikainos kainoraštis nustatomas tik pagal galiojimo datą. Šis veikimo būdas skiriasi nuo numatytojo, kai sistema parenka savikainos kainoraštį, atitinkantį ir projekto valiutą ir galiojimo datą.

Dėl šių veikimo būdo pokyčių „Project Operations“ klientai galės turėti visuotinį savikainos kainoraštį, kuris bus tinkamas visai įmonei. Nereikės turėti kainoraščių kiekviena operacijų valiuta. Visuotiniame kainoraštyje bus galiojimo data ir leis nustatyti savikainos tarifus bet kuria valiuta konkretiems įkainių dimensijos reikšmių deriniams. Savikainos kainoraščio valiuta naudojama tik numatytosioms reikšmėms įvesti, kai kuriami elementų **Vaidmens kainos**, **Kategorijos kainos** ir **Kainoraštis** įrašai. Jis nebus naudojamas kainoraščiui nustatyti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
