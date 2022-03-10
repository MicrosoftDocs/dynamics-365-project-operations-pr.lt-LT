---
title: Produktu pagrįstų sutarties eilučių apžvalga – „Lite“ versija
description: Šioje temoje pateikta informacija apie produktu pagrįstas sutarties eilutes.
author: rumant
ms.date: 10/07/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.custom: intro-internal
ms.openlocfilehash: 79b4f6355afb7472f843eda06bf33a3fe732274d6f2566bd23000aa11cbfdce1
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7007561"
---
# <a name="product-based-contract-lines-overview---lite"></a>Produktu pagrįstų sutarties eilučių apžvalga – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Galite kurti produktu pagrįstas sutarties eilutes programoje „Dynamics 365 Project Operations“. Produktu pagrįstos sutarties eilutės gali būti rankiniu būdu sukuriamos eilutės arba tai gali būti prekės iš produktų katalogo.

## <a name="product-catalog"></a>Produktų katalogas

Produktai, esantys produktų kataloge, turi numatytąjį vienetą ir vienetų grupę. Jei keli produktai turi tą patį atributų rinkinį, galite sukurti produktų šeimą, kuri taip pat turi šiuos atributus. Visi vienos produktų šeimos produktai turi tą patį atributų rinkinį.

Pavyzdžiui, įmonė parduoda prenumeratos licencijas įvairiai programinei įrangai. Visa prenumeratos programinė įranga turi šiuos du atributus:

- Vartotojų skaičius
- Prenumeratos trukmė (mėnesiais)

Norėdami išlaikyti šį katalogo tipą sukurkite produktų šeimą, pavadintą **Prenumeratos programinė įranga**. Įtraukite produktų šeimos atributus **Vartotojų skaičius** ir **Prenumeratos trukmė**. Tada į **Prenumeratos programinės įrangos** produktų šeimą įtraukite konkrečius produktus.

## <a name="add-product-catalog-items-to-a-project-contract"></a>Produktų katalogo prekių įtraukimas į projekto sutartį

Projektų sutartyse yra dviejų tipų eilučių skyriai: pagrįstos projektu ir pagrįstos produktu. Produktu pagrįstos eilutės apima visus sutarties produktų kainoraščio produktus ir vienetus. Galima įtraukti produktus, kurių nėra sutarties produktų kainoraštyje.

Galite pasirinkti produktus iš kitų kainoraščių arba tiesiai iš produktų katalogo. Kai produktus tiesiogiai pasirenkate iš produktų katalogo, produkto pardavimo kainai naudojamas to produkto numatytasis kainoraštis. Jei numatytojo kainoraščio nėra, kaina nurodoma kaip 0 (nulis).

Jei sutarties eilutė pagrįsta produktų katalogu, galite perrašyti pardavimo kainą tiesiogiai eilutėje. Sutarties eilutėje yra laukas **Kainodara** su dviem reikšmėmis:

- **Perrašyti kainodarą**
- **Naudoti numatytąjį**

Jei lauką **Kainodara** nustatysite į **Perrašyti kainodarą**, numatytoji kaina nebus nustatyta. Įveskite produkto kainą sutarties eilutėje. Jei lauką nustatysite į **Naudoti numatytąją**, bus naudojama numatytoji pardavimo kaina ir lauko nebus galima redaguoti.

Įdiegus „Project Operations“ numatytąsias pardavimo kainas galima įvesti produktu pagrįstose sutarties eilutėse. Laukas **Kainodara** nustatomas į **Perrašyti kainodarą**, kad galėtumėte redaguoti numatytąją kainą sutarties eilutėse. Tai yra „Project Operations“ būdingas perrašymas į produktu pagrįstų eilučių veikimą naudojant „Dynamics 365 Sales“.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]