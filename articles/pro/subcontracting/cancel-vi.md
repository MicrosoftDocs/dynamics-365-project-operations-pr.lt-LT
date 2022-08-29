---
title: Projekto tiekėjo sąskaitos faktūros atšaukimas
description: Šiame straipsnyje paaiškinama, kaip atšaukti projekto tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations ir projekto tiekėjo SF atšaukimo finansinis poveikis.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 79d00a91f9ab2d66eab2f80349d6f1fba1934f94
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261101"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projekto tiekėjo sąskaitos faktūros atšaukimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Patvirtinus tiekėjo SF, jos redaguoti ar panaikinti negalima. Jei tiekėjo SF, kuri buvo patvirtinta, įvyko klaida, galite naudoti veiksmą Atšaukti, kad pakeistumėte tiekėjo SF poveikį ir sukurtumėte naują tiekėjo SF.

Kai tiekėjo SF pasirenkate **Atšaukti**, įvyksta toks veiksmas:

1. Tiekėjo SF būsena atnaujinta į **Atšaukta**.
2. Atšaukta tiekėjo SF ir su ja susiję įrašai tampa skirti tik skaityti ir jų negalima redaguoti ar panaikinti.
3. Visos savikainos faktinės sumos, sukurtos pagal tiekėjo SF eilutes kaip tiekėjo SF patvirtinimo dalis, yra atšaukiamos.
4. Jei kokios nors savikainos faktinės sumos buvo susietos su tiekėjo SF eilutėmis kaip susiejimo proceso dalis, pradinis tiekėjo SF patvirtinimas jas panaikino. Tiekėjo SF atšaukimo metu šios faktinės savikainos sumos sukuriamos iš naujo. Kilmė nurodo laiko, išlaidų ar medžiagų naudojimo įrašus.
5. Atšaukę tiekėjo SF, galite dar kartą kurti taisymo žurnalus, apdoroti laiko įvedimo atšaukimus ir atšaukti pradinio laiko, išlaidų ar esminių faktinių aplinkybių patvirtinimą.

> [!NOTE]
> Atšaukti galima tik patvirtintas projekto tiekėjo sąskaitas faktūras. Tiekėjo sf kitose valstijose negalima atšaukti.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
