---
title: Produktais pagrįstų pasiūlymo eilučių įkainojimas
description: Šiame straipsnyje pateikiama informacija apie savikainos taikymą produkto pasiūlymo eilutei.
author: ruhercul
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 23eb3d29081769347d62098534a9863fd28fa90c
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932582"
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