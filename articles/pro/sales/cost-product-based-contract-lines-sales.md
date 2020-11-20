---
title: Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip kurti
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 0e961bcf32a5dd662b7cd27a23eb5f664c45c292
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177251"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_


Produktais pagrįstos sutarties eilutės programoje „Dynamics 365 Project Operations“ apima lauką **Savikaina**, kuriame saugoma produkto savikaina tolesniems pelningumo skaičiavimams.

Kai katalogo produktui sukuriama produktais pagrįsta sutarties eilutė, produktu pagrįsta sutarties eilutė naudojama kaip numatytoji remiantis produkto katalogo lauku **Standartinė savikaina**. Laukas **Standartinė savikaina** produktų kataloge nustatomas organizacijos pagrindine valiuta. Kai sutarties eilutėje nustatoma vieneto savikaina, ji konvertuojama į sutarties pardavimo valiutą.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Vieneto savikaina produktais pagrįstoje sutarties eilutėje

Produktais pagrįstoje sutarties eilutėje esant vieneto savikainai, galima naudoti skirtingas kiekvieno vieneto pardavimo išlaidas. Nors tai ne visada būtina, yra tam tikrų atvejų, kai tiekėjas klientui gali pritaikyti produkto savikainos nuolaidą. Apsvarstykite toliau pateiktą situaciją.

„Fabrikam Robotics“ diegia roboto rankas „Adatum Corporation“ rinkinio eilutėse. „Fabrikam“ teikia diegimo paslaugas, tačiau robotų rankos įsigyjamos iš „Trey Research“. Jei roboto rankų diegimas įmonėje „ADatum Corporation“ atveria naują pramonės segmentą įmonės „Trey Research“; už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“. Šiuo atveju „Fabrikam“ sukuria produktais pagrįstą robotų rankų sutarties eilutę ir nurodo šios sutarties vieneto savikainą, kuri skiriasi nuo standartinės robotų rankų savikainos „Trey Research“.
