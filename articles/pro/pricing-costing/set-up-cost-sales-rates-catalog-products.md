---
title: Katalogo produktų savikainos ir pardavimo kainų sąranka – „Lite“ versija
description: Šioje temoje pateikta informacija, kaip nustatyti produktų kataloge esančių prekių savikainą ir pardavimo tarifus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176711"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a>Katalogo produktų savikainos ir pardavimo kainų sąranka – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_


Produktų katalogo prekių kainodaros nustatymas naudojant „Dynamics 365 Project Operations“ yra toks pat, kaip ir naudojant „Dynamics 365 Sales“.

Kadangi produktų negalima įvertinti arba naudoti „Project Operations“ projektuose, produktų katalogo kainų nereikia nustatyti pasiūlymų ir sutarčių projektų kainoraščiuose.

Produktų katalogo kainos turėtų būti nustatomos pasiūlymo, sutarties arba kliento lauke **Produkto kaina**. Šių objektų produktų katalogo kainų nenustatinėkite projektų kainoraščiuose. Projektų kainoraščiai yra nesuderinami su „Project Operations“. Yra programai skirta verslo logika, kuri nukopijuoja kainoraščius iš pasiūlymo į sutartį. Rezultatas – sutarčiai skirtas projekto kainoraštis. Kopijavimo operacija gali atidėti pasiūlymo laimėjimo procesą, jei projekto kainoraštis pasiūlyme bus per didelis. Produktų kainoraščiai nėra kopijuojami siekiant sutartyse sukurti pasirinktinius kainoraščius. Tai reiškia, kad produktų kainoraščiai nedaro poveikio pasiūlymo laimėjimo proceso efektyvumui.
