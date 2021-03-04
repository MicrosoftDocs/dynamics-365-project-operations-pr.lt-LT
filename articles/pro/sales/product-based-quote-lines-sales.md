---
title: Produktu pagrįstų pasiūlymo eilučių apžvalga – „Lite“ versija
description: Šioje temoje pateikta informacija apie darbą su produktu pagrįstomis pasiūlymo eilutėmis.
author: rumant
manager: Annbe
ms.date: 10/30/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6aa428c486f149308ad078f9d7a80a0be0f0f04
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4178198"
---
# <a name="product-based-quote-lines-overview---lite"></a>Produktu pagrįstų pasiūlymo eilučių apžvalga – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Galite kurti produktu pagrįstas pasiūlymo eilutes programoje „Dynamics 365 Project Operations”. Produktu pagrįstos pasiūlymo eilutės gali būti pridedamos rankiniu būdu arba jos gali būti produktų katalogo elementais.

## <a name="product-catalog"></a>Produktų katalogas

Kiekvienas produktų kataloge esantis produktas turi numatytąjį vienetą ir vieneto grupę. Jei keli produktai turi tą patį atributų rinkinį, galite sukurti produktų šeimą, kuri taip pat turi šiuos atributus. 

Pavyzdžiui, įmonė parduoda prenumeratos licencijas įvairiai programinei įrangai. Visa prenumeratos programinė įranga turi šiuos du atributus:

- Vartotojų skaičius
- Prenumeratos trukmė mėnesiais

Siekdami išlaikyti šio tipo katalogą, sukurkite produktų šeimą, pavadintą **Prenumeratos programinė įranga**, pridėkite vartotojų skaičių ir prenumeratos trukmę kaip atributus. Tada galite įtraukti atskirus produktus į produktų šeimą **Prenumeratos programinė įranga**.

## <a name="add-product-catalog-items-to-a-project-quote"></a>Produktų katalogo elementų įtraukimas į projekto pasiūlymą

Puslapiuose **Projekto pasiūlymas** ir **Projekto sutartis** yra skyriai, skirti projektu pagrįstoms eilutėms ir produktu pagrįstoms eilutėms. Produktu pagrįstoms eilutėms pasiūlymo eilutės arba projekto sutarties eilutės išplečiamajame sąraše yra visi produktai ir vienetai, esantys produkto kainoraštyje. Taip pat galite įtraukti produktų, kurie neįvardyti produktų kainoraštyje.

Be to, galite pažymėti produktus iš kitų kainoraščių arba tiesiogiai iš produktų katalogo. Kai produktus tiesiogiai žymite iš produktų katalogo, produkto numatytasis kainoraštis naudojamas produkto pardavimo kainai gauti. Jei numatytojo kainoraščio nėra, kaina nurodoma kaip nulis (0).

Kai pasiūlymo eilutė pagrįsta produktų katalogu, galite perrašyti pardavimo kainą tiesiogiai pasiūlymo eilutėje. Pasiūlymo eilutė lauke **Kainodara** su dviem galimomis reikšmėmis:

- **Perrašyti kainodarą**
- **Naudoti numatytąjį**

Jei pažymėsite **Perrašyti kainodarą**, numatytoji kaina nenustatoma. Vietoje to pasiūlymo eilutėje turite įvesti produkto kainą. Jei pažymėsite **Naudoti numatytąsias reikšmes**, naudojama numatytoji pardavimo kaina, o laukas užrakinamas ir negali būti redaguojamas.

Numatytąsias pardavimo kainas galima įvesti pasiūlymo produktu pagrįstose eilutėse. Tada laukas **Kainodara** nustatomas į **Perrašyti kainodarą**, kad galėtumėte redaguoti numatytąją kainą pasiūlymo eilutėse. Tai yra konkrečiai „Project Operations” naudojamas perrašymo į produktu pagrįstas eilutes veikimo būdas programoje „Dynamics 365 Sales”.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]