---
title: Būsenos perėjimai tiekėjo sąskaitoje faktūroje
description: Šiame straipsnyje paaiškinami tiekėjo sąskaitos faktūros būsenos perėjimai „Microsoft Dynamics 365 Project Operations“.
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

Šiame straipsnyje paaiškinami tiekėjo sąskaitos faktūros būsenos perėjimai „Microsoft Dynamics 365 Project Operations“. Naudojamos šios būsenos: **Juodraštis**, **Peržiūrima**, **Patvirtinta**, **Sulaikyta** ir **Atšaukta**.

Tolesniuose paveikslėliuose pateikti būsenos perėjimai.

![Papildomos rangos būsenos perleidimo modelis.](../media/VI_State_Model.jpg)

Toliau esančioje lentelėje paaiškinta, ką kiekviena būsena atitinka „Project Operations" tiekėjo sąskaitos faktūros gyvavimo cikle.

| Rajonas | Aprašą | Leisti perėjimai |
| --- | --- | --- |
| Juodraštis | Ši būsena yra pradinė tiekėjo sąskaitos faktūros būsena. Eilutės ir kainos gali būti modifikacijos. Šios būsenos tiekėjo sąskaitą faktūrą galima redaguoti ir panaikinti. | Apdorajama |
| Peržiūrima | Ši būsena yra pradinė tiekėjo sąskaitos faktūros būsena. Bent vienos tiekėjo sąskaitos faktūros eilutės tikrinimo būsena yra **Vykdoma**. | Patvirtinta, Laukiama |
| Patvirtinta | Ši būsena atitinka tiekėjo sąskaitos faktūros etapą, kai programa sukūrė kiekvienos tiekėjo sąskaitos faktūros eilutės išlaidų faktinius rezultatus. Visos susietos išlaidų faktinės sumos, kurios buvo gretintos su tiekėjo sąskaitos faktūros eilutėmis, buvo atšauktos ir pakeistos išlaidų faktinėmis sąrangomis iš tų tiekėjo sąskaitos faktūros eilučių. Šios būsenos tiekėjo sąskaitą faktūrą galima redaguoti ar panaikinti. Norėdami atšaukti patvirtintą tiekėjo **sąskaitą faktūrą**, galite naudoti mygtuką Atšaukti. Veiksmas Atšaukti panaikina veiksmo Patvirtinti poveikį. | Atšauktos |
| Sulaikyta | <p>Ši būsena atitinka tiekėjo sąskaitos faktūros etapą, kuriame tiekėjo sąskaitos faktūros perkelti negalima dėl sąskaitos faktūros arba tiekėjo būsenos problemos. Šios būsenos tiekėjo sąskaitą faktūrą galima patvirtinti, atšaukti, redaguoti ar panaikinti.</p><p>Norėdami perkelti tiekėjo sąskaitą faktūrą į juodraščio arba **peržiūros būseną, galite naudoti** veiksmą Atidaryti **iš** naujo. Jei bent vienos tiekėjo sąskaitos faktūros eilutės **tikrinimo** būsena yra **Vykdoma** ar Baigta, tiekėjo sąskaita faktūra bus atidaryta iš **naujo peržiūros būsenoje**. Jei visų tiekėjo sąskaitos faktūros eilučių tikrinimo būsena **yra Nepradėta** tiekėjo sąskaita faktūra bus atidaryta iš naujo būsenos **Juodraštis**.</p> | Šablonas, Peržiūrimas |
| Atšauktos | Ši būsena atitinka etapą, kai nebereikalingas faktinis med iagų ir (arba) išteklių prisiejimas naudojant išteklius. Šios būsenos nenaudokite, jei norite įvertinti išteklių ir medžiagos personalo projekto reikalavimus, be to, jo negalima nurodyti laiku, išlaidoms ir medžiagos naudojimui projektui. Šios būsenos papildomo tiekėjo sąskaitą faktūrą galima redaguoti ar panaikinti. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
