---
title: Numatytieji kainoraščiai
description: Šiame straipsnyje pateikiama informacija apie numatytuosius pardavimo ir savikainos kainoraščius programoje "Project Operations".
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
1. Jei prie sąskaitos įrašo nepridedama projekto kainoraščių, sistema peržiūri pardavimo kainoraščius, pridėtus prie projekto parametrų, atitinkančių projekto pasiūlymo valiutą.
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

Kainoraščiai nėra numatytieji jokiame „Project Operations“ objekte. Išlaidų kainoraštis, naudojamas projekto išlaidoms, visada nustatomas pagal kiekvieną operaciją. Sistema baigia toliau nurodytą procesą, kad nustatytų, kokį kainoraštį naudoti projekto išlaidose.

1. Sistema žiūri į kainoraščius, kurie pridedami prie projekto rangos organizacijos padalinio.
1. Toliau sistema nagrinėja kainoraščių, atitinkančių gaunamo įvertinimo konteksto datą arba faktinį kontekstą, datos efektingumą.

    - *Įvertinimo kontekstas* nurodo bet kurį iš trijų projekto operacijų įvertinimo kontekstų:

        - Projekto įvertinimo eilutė
        - Pasiūlymo eilutės informacija
        - Sutarties eilutės informacija

    - *Faktinis kontekstas* nurodo bet kurį iš trijų projekto operacijų faktinių duomenų šaltinių:

       - Neautomatiniu būdu sukurtos įrašų žurnalo eilutės arba taisymo žurnalo eilutės, sukurtos taisymo žurnale
       - Žurnalo eilutės, sukurtos pateikiant laiko, išlaidų ar medžiagų naudojimo žurnalus
       - Sąskaitos faktūros eilutės informacija

    Kai "Project Operations" atitinka gaunamo žurnalo eilutės arba sąskaitos faktūros eilutės išsamios informacijos datos efektyvumą realiame *kontekste*, ji naudoja lauką **Operacijos data**.

    - Jei keli kainoraščiai galioja gaunamo įvertinimo konteksto arba faktinio konteksto datai, pasirenkamas vėliausiai sukurtas kainoraštis.
    - Jei prie projekto sutartinio organizacijos vieneto nepridedami kainoraščiai, sistema peržiūri išlaidų kainoraščius, pridėtus prie projekto parametrų, atitinkančių projekto valiutą.

## <a name="enable-multi-currency-cost-price-list"></a>Įgalinti kelių valiutų savikainos kainoraštį

Šį nustatymą galite rasti skiltyje **"Nustatymų** \> **parametrai".** Numatytoji reikšmė yra **Ne**.

Kai šis parametras įjungtas (t. y. reikšmė nustatyta kaip **Taip**), sistema veikia taip:

- Tai leidžia išlaidų kainoraščius bet kuria valiuta susieti su organizaciniu vienetu. Pavyzdžiui, išlaidų kainoraštis EUR valiuta gali būti pridėtas prie organizacinio vieneto USD valiuta. Sistema ir toliau tikrins, ar išlaidų kainoraščiai, pridėti prie organizacinio vieneto, neturi persidengiančio datos veiksmingumo.
- Jis patvirtina, kad išlaidų kainoraščiai, pridėti prie projekto parametrų, neturi sutampančio datos efektingumo, net jei jų valiutos skiriasi. Šis elgesys skiriasi nuo numatytojo elgesio (t. y. elgesio, kai reikšmė nustatyta kaip **Ne**). Atliekant numatytąjį veiksmą, tik išlaidų kainoraščiai, kurių **valiuta yra ta pati**, yra tikrinami dėl nepersidengiančio datos efektingumo.
- Gaunamo sandorio kontekste jis nustato savikainos kainoraštį, remdamasis tik datos veiksmingumu. Šis veikimo būdas skiriasi nuo numatytojo veikimo būdo, kai sistema pasirenka išlaidų kainoraštį, kuris atitinka ir projekto valiutą, ir datos efektyvumą.

Dėl šių elgsenos pokyčių "Project Operations" klientai galės tvarkyti visuotinį išlaidų kainoraštį, kuris bus aktualus visai įmonei. Jiems nereikės turėti kainoraščių kiekvienoje operacijų valiutoje. Pasaulinis kainoraštis turės poveikį datai ir leis nustatyti sąnaudų kursą bet kuria valiuta konkrečiam kainodaros dimensijos verčių deriniui. Savikainos kainoraščio valiuta naudojama tik nustatant numatytąsias reikšmes, kai **sukuriamos vaidmenų kainos**, **Kategorijų kainos** ir **Kainoraštis** prekių įrašai. Jis nebus naudojamas kainoraštiui nustatyti.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
