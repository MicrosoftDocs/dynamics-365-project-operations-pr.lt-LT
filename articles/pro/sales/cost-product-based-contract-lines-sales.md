---
title: Produktu pagrįstų sutarties eilučių įkainojimas
description: Šioje temoje pateikta informacija apie tai, kaip kurti
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 7dfb9425174dddee52f9ee64f7a963e48a6bca70
ms.sourcegitcommit: 3a0c18823a7ad23df5aa3de272779313abe56c82
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2020
ms.locfileid: "4081067"
---
# <a name="costing-product-based-contract-lines"></a>Produktu pagrįstų sutarties eilučių įkainojimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_


Produktais pagrįstos sutarties eilutės programoje „Dynamics 365 Project Operations“ apima lauką **Savikaina** , kuriame saugoma produkto savikaina tolesniems pelningumo skaičiavimams.

Kai katalogo produktui sukuriama produktais pagrįsta sutarties eilutė, produktu pagrįsta sutarties eilutė naudojama kaip numatytoji remiantis produkto katalogo lauku **Standartinė savikaina**. Laukas **Standartinė savikaina** produktų kataloge nustatomas organizacijos pagrindine valiuta. Kai sutarties eilutėje nustatoma vieneto savikaina, ji konvertuojama į sutarties pardavimo valiutą.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Vieneto savikaina produktais pagrįstoje sutarties eilutėje

Produktais pagrįstoje sutarties eilutėje esant vieneto savikainai, galima naudoti skirtingas kiekvieno vieneto pardavimo išlaidas. Nors tai ne visada būtina, yra tam tikrų atvejų, kai tiekėjas klientui gali pritaikyti produkto savikainos nuolaidą. Apsvarstykite toliau pateiktą situaciją.

„Fabrikam Robotics“ diegia roboto rankas „Adatum Corporation“ rinkinio eilutėse. „Fabrikam“ teikia diegimo paslaugas, tačiau robotų rankos įsigyjamos iš „Trey Research“. Jei roboto rankų diegimas įmonėje „ADatum Corporation“ atveria naują pramonės segmentą įmonės „Trey Research“; už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“. Šiuo atveju „Fabrikam“ sukuria produktais pagrįstą robotų rankų sutarties eilutę ir nurodo šios sutarties vieneto savikainą, kuri skiriasi nuo standartinės robotų rankų savikainos „Trey Research“.
