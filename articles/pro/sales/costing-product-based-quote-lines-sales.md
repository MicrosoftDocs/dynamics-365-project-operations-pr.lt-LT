---
title: Produktais pagrįstų pasiūlymo eilučių įkainojimas
description: Šioje temoje pateikta informacija apie tai, kaip taikyti savikainą produktu pagrįstai pasiūlymo eilutei.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1fa7896e249abfefd3e93cba4bad789e67e14f31
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003461"
---
# <a name="costing-product-based-quote-lines"></a>Produktais pagrįstų pasiūlymo eilučių įkainojimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


„Dynamics 365 Project Operations“ produktais pagrįstose pasiūlymo eilutėse taip pat yra laukas **Savikaina**. Šis laukas naudojamas, kad būtų sekama pasiūlymo eilutės produkto savikaina ir tolesnio pelningumo skaičiavimai.

Kai katalogo produktui sukuriama produktų pagrįsta pasiūlymo eilutė, produktu pagrįsta pasiūlymo elutė naudojama kaip numatytoji remiantis produkto katalogo lauku **Standartinė savikaina**. Standartinės savikainos laukas produktų kataloge nustatomas organizacijos pagrindine valiuta. Numatytoji vieneto savikaina produktu pagrįstoje pasiūlymo eilutėje konvertuojama į pardavimo valiutą pasiūlyme.

## <a name="unit-cost-on-a-product-based-quote-line"></a>Vieneto savikaina produktu pagrįstoje pasiūlymo eilutėje

Produktu pagrįstoje pasiūlymo eilutėje turi būti vieneto savikaina, kad būtų leidžiama naudoti skirtingas kiekvieno pardavimo produkto išlaidas. Tai nėra įprastas scenarijus, tačiau kartais produkto savikainą gali sumažinti tiekėjas, atsižvelgdamas į galutinio pardavimo klientą.

Pavyzdžiui:

„Fabrikam Robotics“ diegia roboto rankas „Datum Corporation“ rinkinio eilutėse. „Fabrikam“ teikia diegimo paslaugas, tačiau robotų rankos įsigyjamos iš „Trey Robotics“. Jei roboto rankų diegimas įmonėje „Datum Corporation“ atveria naują pramonės segmentą įmonės „Trey“ robotų rankoms, už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“.

Tokiu atveju „Fabrikam“ sukurs produktu pagrįstą pasiūlymo eilutę, skirtą robotų rankoms, ir įves šio pasiūlymo specialią vieneto kainą. Ši kaina skirsis nuo standartinės „Trey“ robotų rankų savikainos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]