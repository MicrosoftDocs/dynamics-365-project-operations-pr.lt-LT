---
title: Numatytieji kainoraščiai
description: Šioje temoje pateikta informacija apie numatytuosius pardavimo ir savikainos kainoraščius programoje „Project Operations“.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 275ef9b9706d212a6da0dc7c060081c3226572f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080715"
---
# <a name="default-price-lists"></a>Numatytieji kainoraščiai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

## <a name="sales-price-lists"></a>Pardavimo kainoraščiai

Kiekviename projekto pasiūlyme ir sutartyje programoje „Dynamics 365 Project Operations“ yra numatytasis pardavimo savikainų kainoraštis. 

### <a name="price-list-default-on-project-quotes"></a>Numatytasis projekto pasiūlymų kainoraštis
Sistema baigia toliau nurodytą procesą, kad nustatytų, kokį kainoraštį pasirinkti kaip numatytąjį projekto pasiūlymo kainoraštį.

1. Sistema atsižvelgia į kainoraščius, pridėtus prie kliento projektų kainoraščių. 
2. Jei prie kliento įrašo pridėti projektų kainoraščiai, sistema atsižvelgia į pardavimo kainoraščius, pridėtus prie projekto parametrų, kurie atitinka projekto pasiūlymo valiutą.
3. Tada sistema patikrina kainoraščių, atitinkančių projekto pasiūlymo datų intervalą, įsigaliojimo datą. Konkrečiai – datą, kai pasiūlymas buvo sukurtas.
4. Jei yra keli kainoraščiai, kurie galioja projekto pasiūlymo datą, projekto pasiūlyme nustatomi visi numatytieji kainoraščiai.
5. Jei projekto pasiūlymo datą galiojančių kainoraščių nėra, projekto pasiūlyme nėra numatytojo projekto kainoraščio. Projekto pasiūlyme pasirodys įspėjamasis pranešimas. Pranešime nurodoma, kad faktinės ir įvertintos projektų sumos nebus įkainotos, nes nėra pridėtų projektų kainoraščių.

### <a name="price-list-default-on-project-contracts"></a>Numatytasis projekto sutarčių kainoraštis 
Sistema baigia toliau nurodytą procesą, kad nustatytų, kokį kainoraštį pasirinkti kaip numatytąjį projekto sutarties kainoraštį.

1. Jei sutartis sukuriama iš pasiūlymo, projekto kainoraščiai pasiūlyme yra kopijuojami atskirai ir pridedami prie projekto sutarties.
2. Jei sutartis sukuriama nuo nulio, sistema atsižvelgia į kainoraščius, pridėtus prie kliento projektų kainoraščių. Jei prie kliento įrašo nepridėti projektų kainoraščiai, sistema atsižvelgia į pardavimo kainoraščius, pridėtus prie projekto parametrų, kurie atitinka projekto sutarties valiutą.
4. Tada sistema patikrina kainoraščių, atitinkančių projekto sutarties datų intervalą, įsigaliojimo datą. Konkrečiai – datą, kai sutartis buvo sukurta.
5. Jei yra keli kainoraščiai, kurie galioja sutarties datą, sutartyje nustatomi visi numatytieji kainoraščiai.
6. Jei sutarties datą galiojančių kainoraščių nėra, sutartyje nėra numatytųjų projektų kainoraščių. Projekto sutartyje pasirodys įspėjamasis pranešimas. Pranešime nurodoma, kad faktinės ir įvertintos projektų sumos nebus įkainotos, nes nėra pridėtų projektų kainoraščių.

## <a name="cost-price-lists"></a>Savikainos kainoraščiai

Kainoraščiai nėra numatytieji jokiame „Project Operations“ objekte. Išlaidų kainoraščio, skirto projekto išlaidoms, nustatymas visada atliekamas šiuo metu. Sistema baigia toliau nurodytą procesą, kad nustatytų, kokį kainoraštį naudoti projekto išlaidose.

1. Sistema pirmiausia ieško kainoraščių, pridėtų prie projekto sutartį sudarančio organizacijos vieneto.
2. Tada sistema peržiūri kainoraščių, atitinkančių gaunamo įvertinimo arba faktinės eilutės data, įsigaliojimo datą. Esant tokiai situacijai, *įvertinimo eilutė* apima visus tris „Project Operations“ įvertinimo kontekstus.

    - Projekto įvertinimo eilutė
    - Pasiūlymo eilutės informacija
    - Sutarties eilutės informacija
  
3. Jei yra keli kainoraščiai, kurie galioja gaunamo įvertinimo arba faktinės eilutės datą, pasirenkamas vėliausiai sukurtas kainoraštis.
4. Jei prie projekto sutartį sudarančio organizacijos vieneto kainoraščiai nepridėti, sistema atsižvelgia į savikainos kainoraščius, pridėtus prie projekto parametrų, kurie atitinka projekto valiutą.
5. Tada sistema peržiūri kainoraščių, atitinkančių gaunamo įvertinimo arba faktinės eilutės data, įsigaliojimo datą. 
6. Jei yra keli kainoraščiai, kurie galioja gaunamo įvertinimo arba faktinės eilutės datą, pasirenkamas vėliausiai sukurtas kainoraštis.
7. Jei savikainos kainoraščiai nėra pridėti prie projekto parametrų, atitinkančių valiutą ir įsigaliojimo datą, sistema pagal nustato numatytąjį savikainos tarifą į nulį (0) gaunamo įvertinimo arba faktinėje eilutėje.