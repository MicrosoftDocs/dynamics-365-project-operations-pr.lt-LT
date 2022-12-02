---
title: Subrangos būsenos perėjimai
description: Šiame straipsnyje paaiškinta, kaip sukuriami, vykdomi ir uždaromi būsenos perėjimai naudojant „Microsoft Dynamics 365 Project Operations".
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2804fc30f8dade42dc1093e5fc0f01fa1db22ca3
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522941"
---
# <a name="state-transitions-on-a-subcontract"></a>Subrangos būsenos perėjimai 

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šiame straipsnyje paaiškinami subrangovo sutarties faktūros būsenos perėjimai „Microsoft Dynamics 365 Project Operations“. Kiekviena būsena vaizduojama kaip juodraštis, patvirtinta, uždaryta arba atšaukta. Tolesniuose paveikslėliuose pateikti būsenos perėjimai.

![Subrangos būsenos modelis](../media/SubconStates.png)  

Toliau esančioje lentelėje paaiškinta, ką kiekviena būsena atitinka „Project Operations" tiekėjo subrangos gyvavimo cikle.

| Rajonas | Aprašą | Leisti perėjimai |
| --- | --- | --- |
| Juodraštis | Tai atitinka pradinę subrangos būseną. Vyksta derybos su pardavėju. Eilutės ir kainos gali būti modifikuojamos. Šios būsenos subrangos sutartis gali būti naudojama įvertinti darbuotojų projektų reikalavimus ištekliams ir medžiagoms. Jį taip pat galima nurodyti atsižvelgiant į laiką, išlaidas ir medžiagos naudojimą projektui. Šios būsenos subrangos sutartį galima redaguoti ir panaikinti. | Patvirtinta |
| Patvirtinta | Tai yra subrangos sutarties etapo pabaiga, po derybų su pardavėju dėl įsigytų kainų ir eilučių elementų. Tačiau faktinis medžiagų ir (arba) darbo pristatymas naudojant subrangos sutarties išteklius vis dar vykdomas. Šios būsenos subrangos sutartis gali būti naudojama įvertinti darbuotojų projektų reikalavimus ištekliams ir medžiagoms. Jį taip pat galima nurodyti atsižvelgiant į laiką, išlaidas ir medžiagos naudojimą projektui. Šios būsenos subrangos sutarties negalima redaguoti ar panaikinti. Mygtukas **Atšaukti** leidžia atšaukti patvirtintą subrangos sutartį. Mygtukas **Iš naujo atidaryti** leidžia iš naujo atidaryti subrangos sutartį, kad ji grįžtų į **juodraščio** būseną. Naudokite mygtuką **Uždaryti** kad uždarytumėte patvirtintą subrangos sutartį. | Uždaryta <br> Atšauktos <br> Juodraštis |
| Uždaryta | Ši būsena atitinka etapą, kai faktinis subrangos sutarties medžiagų ir (arba) išteklių pristatymas yra baigtas. Šios būsenos subrangos sutartis gali būti naudojama įvertinti darbuotojų projektų reikalavimus ištekliams ir medžiagoms. Jį taip pat jo nebegalima nurodyti atsižvelgiant į laiką, išlaidas ir medžiagos naudojimą projektui. Šios būsenos subrangos sutarties negalima redaguoti ar panaikinti. | Joks |
| Atšauktos | Ši būsena atitinka etapą, kai faktinis subrangos sutarties medžiagų ir (arba) išteklių pristatymas yra nebereikalingas. Šios būsenos nenaudojama, jei norite įvertinti išteklių ir medžiagos personalo projekto reikalavimus, be to, jo negalima nurodyti laiko, išlaidų ir medžiagos naudojimo projektui. Šios būsenos subrangos sutarties negalima redaguoti ar panaikinti. | Joks |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
