---
title: Produktu pagrįstos pasiūlymo eilutės
description: Šioje temoje pateikta informacija apie produktu pagrįstas pasiūlymo eilutes.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/06/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a5b52e74994a40b20353d85d1d9bcd59d435cd0b
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151263"
---
# <a name="product-based-quote-lines"></a>Produktu pagrįstos pasiūlymo eilutės

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]


Galite kurti produktu pagrįstas pasiūlymo eilutes programoje Dynamics 365 Project Service Automation. Produktu pagrįstos pasiūlymo eilutės gali būti „įrašomos“ eilutės arba produktų katalogo elementai.

## <a name="product-catalog"></a>Produktų katalogas

Produktai, esantys „Dynamics 365“ produktų kataloge, turi numatytąjį vienetą ir vieneto grupę. Jei keli produktai turi tą patį atributų rinkinį, galite sukurti produktų šeimą, kuri taip pat turi šiuos atributus. Visi vienos produktų šeimos produktai turi tą patį atributų rinkinį.

Pavyzdžiui, įmonė parduoda prenumeratos licencijas įvairioms programinėms įrangoms. Visa prenumeratos programinė įranga turi šiuos du atributus:

- Vartotojų skaičius 
- Prenumeratos trukmė (mėnesiais)

Geras būdas išlaikyti šio tipo katalogą yra sukurti produktų šeimą, pavadintą **Prenumeratos programinė įranga**, ir kuri turi atributus **Vartotojų skaičius** bei **Prenumeratos trukmė**. Tada galite įtraukti individualius produktus, pavyzdžiui, **Dynamics 365 Sales** arba **Dynamics 365 Field Service**, į produktų šeimą **Prenumeratos programinė įranga**.

## <a name="adding-product-catalog-items-to-a-project-quote"></a>Produktų katalogo elementų įtraukimas į projekto pasiūlymą

Projekto pasiūlymo ir projekto sutarties puslapiuose yra dviejų tipų eilučių skyriai: projektu pagrįstos eilutės ir produktu pagrįstos eilutės. Produktu pagrįstoms eilutėms naudojama „Dynamics 365“, kad įtrauktų elementus iš produktų katalogo į pasiūlymą. Pasiūlymo eilutės arba projekto sutarties eilutės išplečiamajame sąraše yra visi produktai ir vienetai, esantys produktų kainoraštyje, kuris pridėtas prie pasiūlymo arba projekto sutarties. Taip pat galite įtraukti produktų, kurie neįvardyti pasiūlymo produktų kainoraštyje.

Be to, galite pažymėti produktus iš kitų kainoraščių arba galite pažymėti produktus tiesiogiai iš produktų katalogo. Kai produktus tiesiogiai žymite iš produktų katalogo, produkto numatytasis kainoraštis naudojamas produkto pardavimo kainai gauti. Jei numatytojo kainoraščio nėra, kaina nurodoma kaip 0 (nulis).

Jei pasiūlymo eilutė pagrįsta produktų katalogu, galite perrašyti pardavimo kainą tiesiogiai pasiūlymo eilutėje. Atminkite, kad pasiūlymo eilutė, esanti „Dynamics 365“ turi lauką **Kainodara**. Galimos dvi reikšmės:

- Perrašyti kainodarą  
- Naudoti numatytąją

Jei šį lauką nustatysite į **Perrašyti kainodarą**, „Dynamics 365“ nenustato numatytosios kainos. Pasiūlymo eilutėje turite įvesti produkto kainą. Jei šį lauką nustatysite į **Naudoti numatytąją**, „Dynamics 365“ naudoja numatytąją pardavimo kainą ir užrakina lauką, kad jo nebūtų galima redaguoti.

Įdiegus PSA numatytąsias pardavimo kainas galima įvesti pasiūlymo produktu pagrįstose eilutėse. Tada laukas **Kainodara** nustatomas į **Perrašyti kainodarą**, kad galėtumėte redaguoti numatytąją kainą pasiūlymo eilutėse.

> ![Kainodaros perrašymo nustatymas](media/basic-guide-10.png)
 
## <a name="quantity-factors-for-products"></a>Produktų kiekio koeficientai

Programoje PSA naudojami kiekio koeficientai, kad būtų palaikomas prenumerata pagrįstų produktų pardavimas. Prenumerata pagrįstiems produktams pasiūlymo arba projekto sutarties eilutėje kiekis išreiškiamas kaip vartotojo mėnesių skaičius.

Paprastai prenumeratos programinės įrangos kaina kataloge yra kaina vienam vartotojui per mėnesį. Tačiau vietoje to galite naudoti kitus laiko aprašus. Per pardavimo procesą pasiūlymo eilutėje nurodyta kaina paprastai yra vienam vartotojui per mėnesį, dėl kurios susitarė ir nuolaidą pritaikė IT pardavimo agentas. Kiekvienas sandoris turi skirtingą vartotojų skaičių ir skirtingą prenumeratos mėnesių skaičių. Kiekis, naudojamas pasiūlymo eilutės sumai apskaičiuoti, yra vartotojų skaičiaus ir prenumeratos mėnesių skaičiaus produktas.

Norėdami paremti šį pardavimo tipą, PSA pristatė kiekio koeficientų koncepciją. Kiekio koeficientai priklauso nuo „Dynamics 365“ produkto atributų. Konfigūruojant konkrečias produkto ypatybes, PSA leidžia žymėti tų ypatybių pogrupį arba visas ypatybes kaip kiekio koeficientus.

PSA tikrina, kad tik skaitinės ypatybės arba produkto, turinčio skaitinių duomenų tipą, ypatybės būtų žymimos kaip kiekio koeficientai. Kai produktas, kuriam sukonfigūruoti kiekio koeficientai, yra įtraukiamas į pasiūlymo eilutę, pasiūlymo eilutėje esantis laukas **Kiekis** tampa tik skaitomu lauku. Įvedus produktų ypatybių reikšmes, kurios yra kiekio koeficientai, PSA apskaičiuoja pasiūlymo eilutės kiekį.

Pavyzdžiui, „Dynamics 365“ gali turėti šias ypatybes: 

- **Vartotojų skaičius** – vartotojų skaičius 
- **Mėnesių skaičius** – prenumeratos mėnesių skaičius
- **Produkto SKU** 

Ypatybės **Vartotojų skaičius** ir **Mėnesių skaičius** gali būti pažymėtos kaip kiekio koeficientai redaguojant produkto eilutės ypatybes. 

> ![Vartotojų ir mėnesių skaičių žymėjimas kaip kiekio koeficientai](media/basic-guide-11.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]