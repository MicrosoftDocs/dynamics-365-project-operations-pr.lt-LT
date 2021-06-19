---
title: Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip kurti
author: rumant
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9458a57863244a68359f57185325c03a46bd6569
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003551"
---
# <a name="cost-product-based-contract-lines---lite"></a>Kaštų produktu pagrįstos sutarties eilutės – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_


Į produktu pagrįstas „Dynamics 365 Project Operations“ sutarties eilutes įtraukiamas laukas **Savikaina**, kuriame saugoma produkto savikaina siekiant apskaičiuoti proceso pabaigos pelningumą.

Kai produktu pagrįsta sutarties eilutė sukūriama katalogo produktui, eilutės numatytoji savikaina nustatoma iš produktų katalogo lauko **Standartinė savikaina**. Laukas **Standartinė savikaina** produktų kataloge nustatomas organizacijos pagrindine valiuta. Kai sutarties eilutėje nustatoma vieneto savikaina, ji konvertuojama į sutarties pardavimo valiutą.

## <a name="unit-cost-on-a-product-based-contract-line"></a>Vieneto savikaina produktais pagrįstoje sutarties eilutėje

Produktais pagrįstoje sutarties eilutėje esant vieneto savikainai, galima naudoti skirtingas kiekvieno vieneto pardavimo išlaidas. Nors tai ne visada būtina, yra tam tikrų atvejų, kai tiekėjas klientui gali pritaikyti produkto savikainos nuolaidą. Apsvarstykite toliau pateiktą situaciją.

„Fabrikam Robotics“ diegia roboto rankas „Adatum Corporation“ rinkinio eilutėse. „Fabrikam“ teikia diegimo paslaugas, tačiau roboto rankos yra iš „Trey Research“. Jei roboto rankų diegimas įmonėje „ADatum Corporation“ atveria naują pramonės segmentą įmonės „Trey Research“; už šį sandorį „Trey“ gali taikyti specialią nuolaidą įmonei „Fabrikam“. Tokiu atveju „Fabrikam“ sukuria produktu pagrįstą sutarties eilutę, skirtą roboto rankoms. Įvedama šios sutarties vieneto kaina. Savikaina skiriasi nuo roboto rankų iš „Trey Research“ savikainos.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]