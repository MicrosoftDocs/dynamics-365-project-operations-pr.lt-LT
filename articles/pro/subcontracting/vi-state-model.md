---
title: Būsenos perėjimai tiekėjo sąskaitoje faktūroje
description: Šiame straipsnyje paaiškinami tiekėjo SF būsenos perėjimai programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: e25e4d63d4c9098112a7f40abe60c7184018d582
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261027"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Būsenos perėjimai tiekėjo sąskaitoje faktūroje

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinami tiekėjo SF būsenos perėjimai programoje "Microsoft"Dynamics 365 Project Operations. Naudojamos šios būsenos: **Juodraštis**, **Peržiūrima**, **Patvirtinta**, **Sulaikyta** ir **Atšaukta**.

Toliau pateiktose iliustracijose rodomi būsenos perėjimai.

![Subrangos būsenos perėjimo modelis.](../media/VI_State_Model.jpg)

Šioje lentelėje paaiškinama, ką kiekviena būsena reiškia tiekėjo SF palaikymo cikle "Project Operations".

| Rajonas | Aprašą | Leidžiami perėjimai |
| --- | --- | --- |
| Juodraštis | Ši būsena yra pradinė tiekėjo SF būsena. Linijos ir kainodara gali būti keičiamos. Šios būsenos tiekėjo SF galima redaguoti ir panaikinti. | Vyksta procesas |
| Peržiūrima | Ši būsena reiškia tiekėjo SF apdorojimo būseną. Bent vienos tiekėjo SF eilutės patvirtinimo būsena **yra Vykdoma**. | Patvirtinta, sulaikyta |
| Patvirtinta | Ši būsena nurodo tiekėjo SF etapą, kai programa sukūrė kiekvienos tiekėjo SF eilutės faktines išlaidų sumas. Visos susietos savikainos faktinės sumos, kurios buvo suderintos su tiekėjo SF eilutėmis, buvo atšauktos ir pakeistos faktinėmis sąnaudomis iš tų tiekėjo SF eilučių. Šios būsenos tiekėjo SF redaguoti ar naikinti negalima. Galite naudoti mygtuką Atšaukti **,** kad atšauktumėte patvirtintą tiekėjo SF. Veiksmas Atšaukti panaikina veiksmo Patvirtinti poveikį. | Atšauktos |
| Sulaikyta | <p>Ši būsena reiškia tiekėjo SF etapą, kai tiekėjo SF negali būti perkelta dėl sąskaitos faktūros arba tiekėjo būsenos problemos. Šios būsenos tiekėjo SF negalima patvirtinti, atšaukti, redaguoti ar panaikinti.</p><p>Galite naudoti veiksmą Iš naujo atidaryti, kad perkeltumėte tiekėjo SF į juodraščio **arba** **peržiūros** būseną. Jei bent vienos tiekėjo SF eilutės patvirtinimo būsena **yra Vykdoma** arba **Baigta**, tiekėjo SF bus iš naujo atidaryta būsenoje **Peržiūrima**. Jei visų tiekėjo SF eilučių tikrinimo būsena **yra Nepradėta**, tiekėjo SF bus iš naujo atidaryta juodraščio **būsenoje**.</p> | Juodraštis, Peržiūrimas |
| Atšauktos | Ši būsena reiškia subrangos etapą, kai nebereikia faktinio medžiagų pristatymo ir (arba) darbo naudojant subrangos išteklius. Šios būsenos subrangos sutartis negali būti naudojama išteklių ir medžiagų projekto poreikiams įvertinti ir darbuotojų projektų poreikiams įvertinti, taip pat negali būti nurodyta pagal laiką, išlaidas ir medžiagų naudojimą projekte. Šios būsenos subrangos sutarties redaguoti ar ištrinti negalima. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
