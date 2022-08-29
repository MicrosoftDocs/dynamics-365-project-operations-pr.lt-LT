---
title: Projekto tiekėjo sąskaitos faktūros patvirtinimas
description: Šiame straipsnyje paaiškinama, kaip patvirtinti projekto tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations ir projekto tiekėjo SF patvirtinimo finansinis poveikis.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4dafbe64e0727957068d68f510202a12871b62aa
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261522"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekto tiekėjo sąskaitos faktūros patvirtinimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Patikrinę visas tiekėjo SF eilutes programoje "Microsoft" Dynamics 365 Project Operations, galite naudoti veiksmą Patvirtinti, kad patvirtintumėte tiekėjo SF.

Kai tiekėjo SF pasirenkate **Patvirtinti**, įvyksta toks veiksmas:

1. Tiekėjo SF būsena atnaujinama į **Patvirtinta**.
2. Patvirtinta tiekėjo SF ir su ja susiję įrašai tampa skirti tik skaityti ir jų negalima redaguoti ar panaikinti.
3. Jei kokios nors savikainos faktinės sumos nurodo tiekėjo SF eilutę kaip susiejimo proceso dalį, visos faktinės savikainos, susietos su nurodyta tiekėjo SF eilute, yra atvirkštinės.
4. Naujos savikainos faktinės sumos sukuriamos naudojant tiekėjo SF eilutėje esančią informaciją.
5. Patvirtinus tiekėjo SF, nebegalite kurti taisymo žurnalų, apdoroti laiko įrašo atšaukimų arba atšaukti pradinio laiko, išlaidų ar esminių faktinių aplinkybių, kurios buvo atšauktos, patvirtinimo.

> [!NOTE]
> Jei kurios nors tiekėjo SF eilutės patvirtinimo būsena yra kita nei **Baigta**, tiekėjo SF patvirtinti negalima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
