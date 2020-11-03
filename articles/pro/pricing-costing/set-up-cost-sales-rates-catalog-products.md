---
title: Katalogo produktų savikainos ir pardavimo tarifų nustatymas
description: Šioje temoje pateikta informacija, kaip nustatyti produktų kataloge esančių prekių savikainą ir pardavimo tarifus.
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080903"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a>Katalogo produktų savikainos ir pardavimo tarifų nustatymas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_


Produktų katalogo prekių kainodaros nustatymas naudojant „Dynamics 365 Project Operations“ yra toks pat, kaip ir naudojant „Dynamics 365 Sales“.

Kadangi produktų negalima įvertinti arba naudoti „Project Operations“ projektuose, produktų katalogo kainų nereikia nustatyti pasiūlymų ir sutarčių projektų kainoraščiuose.

Produktų katalogo kainos turėtų būti nustatomos pasiūlymo, sutarties arba kliento lauke **Produkto kaina**. Šių objektų produktų katalogo kainų nenustatinėkite projektų kainoraščiuose. Projektų kainoraščiai yra nesuderinami su „Project Operations“. Yra programai skirta verslo logika, kuri nukopijuoja kainoraščius iš pasiūlymo į sutartį. Rezultatas – sutarčiai skirtas projekto kainoraštis. Kopijavimo operacija gali atidėti pasiūlymo laimėjimo procesą, jei projekto kainoraštis pasiūlyme bus per didelis. Produktų kainoraščiai nėra kopijuojami siekiant sutartyse sukurti pasirinktinius kainoraščius. Tai reiškia, kad produktų kainoraščiai nedaro poveikio pasiūlymo laimėjimo proceso efektyvumui.
