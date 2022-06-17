---
title: Būsenos perėjimai tiekėjo sąskaitoje faktūroje
description: Šiame straipsnyje paaiškinami "Microsoft" tiekėjo SF būsenos perėjimai Dynamics 365 Project Operations.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 58b07322fb6480fdeb07eb867a7aabc0eff7b955
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8934330"
---
# <a name="state-transitions-on-a-vendor-invoice"></a>Būsenos perėjimai tiekėjo sąskaitoje faktūroje

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinami "Microsoft" tiekėjo SF būsenos perėjimai Dynamics 365 Project Operations. Naudojamos šios būsenos: **Juodraštis**, **Peržiūrima**, **Patvirtinta**, **Sulaikyta** ir **Atšaukta**.

Toliau pateiktose iliustracijose parodytas valstybės perėjimas.

![Subrangos būsenos perėjimo modelis.](../media/VI_State_Model.jpg)

Šioje lentelėje paaiškinama, ką kiekviena būsena reiškia tiekėjo SF gyvavimo cikle projekto operacijose.

| Rajonas | Aprašą | Leidžiami perėjimai |
| --- | --- | --- |
| Juodraštis | Ši būsena yra pradinė tiekėjo SF būsena. Eilutės ir kainodara gali būti keičiamos. Šios būsenos tiekėjo SF galima redaguoti ir panaikinti. | Vykdomas |
| Peržiūrima | Ši būsena nurodo tiekėjo SF apdorojimo būseną. Bent vienos tiekėjo SF eilutės tikrinimo būsena **vykdoma**. | Patvirtinta, sulaikyta |
| Patvirtinta | Ši būsena nurodo tiekėjo SF etapą, kai programa sukūrė kiekvienos tiekėjo SF eilutės savikainos faktinius duomenis. Visi susieti išlaidų faktiniai duomenys, kurie buvo suderinti su tiekėjo SF eilutėmis, buvo atšaukti ir pakeisti tų tiekėjo SF eilučių savikainos faktinėmis aplinkybėmis. Šios būsenos tiekėjo SF redaguoti ar panaikinti negalima. Norėdami atšaukti patvirtintą tiekėjo SF, galite naudoti **mygtuką Atšaukti**. Veiksmas Atšaukti atšaukia veiksmo Patvirtinti poveikį. | Atšauktos |
| Sulaikyta | <p>Ši būsena nurodo tiekėjo SF etapą, kai tiekėjo SF negali judėti dėl sf arba tiekėjo būsenos išdavimo. Šios būsenos tiekėjo SF negalima patvirtinti, atšaukti, redaguoti ar panaikinti.</p><p>Galite naudoti veiksmą Iš naujo atidaryti, jei norite perkelti tiekėjo SF į **būseną Juodraštis** arba **Peržiūra**. Jei bent vienos tiekėjo SF eilutės tikrinimo būsena **yra Vykdoma** arba **Baigta**, tiekėjo SF bus atidaryta peržiūros **būsenoje**. Jei visų tiekėjo SF eilučių tikrinimo būsena **yra Nepradėta**, tiekėjo SF bus atidaryta juodraščio **būsenoje**.</p> | Juodraštis, peržiūrimas |
| Atšauktos | Ši būsena yra subrangos sutarties etapas, kai faktinis medžiagų pristatymas ir (arba) darbas subrangos ištekliais nebereikalingas. Šios būsenos subrangos sutartis negali būti naudojama ištekliams ir medžiagoms įvertinti ir personalo projekto reikalavimams įvertinti, taip pat negali būti nurodyta apie projekto laiką, išlaidas ir medžiagų naudojimą. Subrangos sutarties šioje būsenoje redaguoti ar panaikinti negalima. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
