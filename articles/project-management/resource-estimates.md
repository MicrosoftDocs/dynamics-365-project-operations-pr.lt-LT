---
title: Išteklių įvertinimai
description: Šioje temoje pateikta informacija apie tai, kaip „Project Operations“ nustatomi išteklių įvertinimai.
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2ebde2b3c5bcfb5faa02ee476065ac34b1953432
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080756"
---
# <a name="resource-estimates"></a>Išteklių įvertinimai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Išteklių įvertinimai pateikiami remiantis laikotarpių pastangomis, apibrėžtomis darbo paskirstymo struktūroje, ir atitinkamomis kainų dimensijomis. Paprastai skaičiuojama pagal tokią formulę: **kiekvieno vaidmens valandinis įkainis x val.** Kiekvienos ištekliaus laikotarpio pastangų duomenys įrašomi ištekliaus priskyrimo įraše. Kainų duomenys laikomi iš anksto apibrėžtame kainoraštyje. Vienetų konvertavimas atliekamas pagal taikomą kainoraštį.

![Išteklių įvertinimai](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a>Numatytoji savikainos ir sąnaudų valiuta

Numatytosios savikainos reikšmės pateikiamos remiantis organizaciniu vienetu.

## <a name="default-bill-rate-and-sales-currency"></a>Numatytasis sąskaitų tarifas ir pardavimo valiuta

Pardavimo kainos taikomos vieną kartą sandoriui. Numatytojo pardavimo kainoraščio sąrašo hierarchija:

1. Organizacija
2. Klientas
3. Pasiūlymas / sutartis
