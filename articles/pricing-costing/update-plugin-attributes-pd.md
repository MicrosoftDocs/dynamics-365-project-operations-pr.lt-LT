---
title: Priedo atributų atnaujinimas siekiant įtraukti naujas kainodaros dimensijas
description: Šioje temoje pateikta informacijos, kaip atnaujinti priedo atributus, kad būtų galima naudoti kainodaros dimensijas.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d57ec617d2c7b10a01a75e7eaa9ca2d646af3f6ee1d06d4e6fb228fc0533da27
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988346"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a>Priedo atributų atnaujinimas siekiant įtraukti naujas kainodaros dimensijas

Šioje temoje pateikta informacijos, kaip atnaujinti priedo atributus, kad būtų galima naudoti kainodaros dimensijas.

> [!NOTE]
> Ši tema taikoma tik „Dynamics 365 Project Operations“ pasiūlymo ir sutarties funkcijoms.

## <a name="prerequisites"></a>Būtinosios sąlygos
Kad galėtumėte atlikti šioje temoje nurodytus veiksmus, pirmiau turite būti užbaigę toliau nurodytose temose aprašytas procedūras.

  - [Pasirinktinių laukų ir objektų kūrimas](create-custom-fields-entities-pricing-dimensions.md) 
  - [Pasirinktinių laukų įtraukimas į kainų sąranką ir operacijų objektus ](add-custom-fields-price-setup-transactional-entities.md)
  - [Pasirinktinių laukų kaip kainodaros dimensijų nustatymas](set-up-custom-fields-pricing-dimensions.md). 
  
Jei neatlikote šių procedūrų, atlikite jas ir tada grįžkite į šią temą.

## <a name="register-a-plug-in"></a>Priedo užregistravimas
Kai puslapyje **Pasiūlymo eilutė** sukuriama projekto pasiūlymo eilutei skirta pasiūlymo eilutės informacija, sistema sukuria dvi įvertinimo eilutes. Viena įvertinimo eilutė skirta sąnaudoms, o kita eilutė – pardavimui. Tas pats taikoma projekto sutarties eilutėms.

Kai sąnaudų dalyje keičiate kiekį arba lauką, šis pakeitimas taip pat perkeliamas į pardavimo dalį. Tai įmanoma padaryti, nes priedas PreOperation, esantis Quotelinedetail ir Contractlinedetail objektuose, susieja konkrečius operacijos sąnaudų atributus su pardavimo atributais. Jei norite, kad pardavimo dalyje atlikti kainodaros dimensijų verčių pakeitimai būtų atlikti ir sąnaudų dalyje, pakeitus kainodaros dimensiją reikia iš naujo užregistruoti toliau nurodytus priedus.

Toliau pateikiami priedai, kuriuos reikia atnaujinti ir iš naujo užregistruoti.

- PreOperationContractLineDetailUpdate – **msdyn_orderlinetransaction naujinimas**
- PreOperationQuoteLineDetailUpdate – **msdyn_quotelinetransaction naujinimas**

Norėdami atnaujinti ir iš naujo užregistruoti priedus, atlikite toliau nurodytus veiksmus.

1. Atidarykite **PluginRegistrationTool** ir prijunkite prie savo „Project Operations Dataverse“ aplinkos.
2. Pasirinkite **Ieškoti** ir įveskite kelias pirmąsias priedo, kurį reikia atnaujinti, pavadinimo raides.
3. Radę priedą, pasirinkite jį ir spustelėkite **Pasirinkti pagrindinėje formoje**.
4. Pasirinkite veiksmą **msdyn_orderlinetransaction naujinimas**, spustelėkite dešiniuoju pelės mygtuku ir pasirinkite **Atnaujinti**.
5. Dialogo lange **Atnaujinimas** filtravimo atributų dalyje pasirinkite daugtaškį (**...**).
6. Atidaromas filtravimo atributų langas ir pateikiamas visų objekto ir kainodaros dimensijų atributų sąrašas. Pažymėkite kainodaros dimensijų atributų žymės langelius.
7. Pasirinkite **Gerai**, kad uždarytumėte puslapį, tada pasirinkite **Atnaujinti veiksmą**.
8. Pakartokite 2–7 veiksmus ir su antru priedu **PreOperationQuoteLineDetail**. Pasirinkus šį priedą reikia atnaujinti veiksmą **msdyn_quotelinetransaction naujinimas**.
9. Uždarykite **PluginRegistrationTool**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]