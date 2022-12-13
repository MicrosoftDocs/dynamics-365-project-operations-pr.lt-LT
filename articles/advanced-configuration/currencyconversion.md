---
title: Valiutos konvertavimo nustatymas pardavimo kainoms skaičiuoti pagal savikainos tarifus
description: Šiame straipsnyje paaiškinama, kaip sukonfigūruoti valiutos konvertavimo veikimą, kuris bus naudojamas "Microsoft", Dynamics 365 Project Operations kai pardavimo operacijos generuojamos iš išlaidų operacijų.
author: rumant
ms.date: 11/01/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3fa8077deb18f1a54e7f0f5e6dc4491a830df45b
ms.sourcegitcommit: 95e52fcf012a51229f3f6ae7dbf7b0fa56072a85
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/01/2022
ms.locfileid: "9816695"
---
# <a name="set-up-currency-conversion-to-calculate-sales-prices-from-cost-rates"></a>Valiutos konvertavimo nustatymas pardavimo kainoms skaičiuoti pagal savikainos tarifus

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

"Microsoft" Dynamics 365 Project Operations išlaidų kategorijų pardavimo kainas galima nustatyti kaip skaitines reikšmes arba jas galima nustatyti taip, kad jos būtų apskaičiuojamos pagal patirtas išlaidas.

Kai jos nustatytos skaičiuoti pagal patirtas išlaidas, galimos šios parinktys:

- Savikaina
- Žymėjimo procentas virš savikainos

Tais atvejais, kai išlaidų išlaidos patiriamos valiuta, kuri skiriasi nuo projekto sutarties pardavimo valiutos, norint apskaičiuoti pardavimo kainą pagal išlaidas, reikia konvertuoti valiutą.

## <a name="currency-conversion-behavior-that-uses-native-dataverse-exchange-rates"></a>Valiutos konvertavimo elgsena, kai naudojami vietiniai Dataverse valiutų kursai

Pagal numatytuosius nustatymus "Project Operations" naudoja valiutų keitimo kursus, saugomus lentelėje Valiuta Dataverse. Norėdami sukonfigūruoti "Project Operations", kad pardavimo kainoms pagal savikainą skaičiuoti būtų naudojami vietiniai valiutų kursai, atlikite šiuos veiksmus.

1. Eikite į **Projekto operacijų \> parametrų \> parametrai**.
1.  **Atidarykite puslapį Projekto parametro** informacija.
1. Nustatykite **tuščią reikšmę lauke Valiutos konvertavimo logika** .

## <a name="currency-conversion-behavior-that-uses-exchange-rates-from-finance-and-operations-apps"></a>Valiutos konvertavimo elgsena, kai naudojami valiutų kursai iš finansų ir operacijų programų

Valiutų kursai lentelėje Valiuta, kuri yra savaime pasiekiama Dataverse , negalioja pagal datą. Todėl jie ne visada gali būti pritaikyti pagal reikalavimus, kuriuos turite pardavimo kainoms apskaičiuoti pagal savikainą.

Galite naudoti valiutų kursus iš finansų ir operacijų aplinkos, kad apskaičiuotumėte pardavimo kainą pardavimo valiuta pagal išlaidų kursą savikainos valiuta. Norėdami sukonfigūruoti šią valiutos konvertavimo elgseną, atlikite šiuos veiksmus.

1. Puslapyje **Projekto parametrai** įtraukite **lauką Valiutos konvertavimo logika** . Tada išsaugokite ir paskelbkite tinkinimą.
1. Eikite į **Projekto operacijų \> parametrų \> parametrai**.
1.  **Atidarykite puslapį Projekto parametro** informacija. 
1. Nustatykite **lauką Valiutos konvertavimo elgsena** kaip **Išplėstas su atsarginiu variantu į numatytąjį**.
1. Suteikite **"Dual-write App User**  saugos vaidmuo **Global Read"** leidimą šioms lentelėms:

    - msdyn\_ valiutų keitimo kursai
    - msdyn\_ currencyexchangeratepairs
    - msdyn\_ valiutų kursų tipai

1. "Finance and Operations" aplinkoje paleiskite šiuos dvigubo rašymo žemėlapius su pradiniu sinchronizavimu:

    - Valiutos kurso tipas (msdyn\_ valiutų kursų tipai)
    - Valiutų kursų pora (msdyn\_ currencyexchangeratepairs)
    - CDS valiutų kursai (msdyn\_ currencyexchangerates)

Kai šie pakeitimai bus baigti, dvigubas rašymas padarys valiutų kursus iš finansų ir operacijų aplinkos prieinamus Dataverse. Tada "Project Operations" naudos šiuos valiutų kursus savikainos kursams konvertuoti į sutarties pardavimo valiutą.

> [!NOTE]
> Šis valiutos konvertavimo veikimas taikomas tik skaičiuojant pardavimo kainas pagal savikainos kursus. Jis nebus naudojamas bendrai apskaičiuoti bazinės valiutos vertes. Bazinės valiutos vertės visada naudos vietinius Dataverse valiutų kursus, neatsižvelgiant į tai, ar atliksite šią procedūrą.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
