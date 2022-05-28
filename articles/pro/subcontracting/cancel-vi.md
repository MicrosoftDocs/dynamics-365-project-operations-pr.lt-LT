---
title: Atšaukti projekto tiekėjo SF
description: Šioje temoje paaiškinama, kaip atšaukti projekto tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations ir kokį finansinį poveikį turi projekto tiekėjo SF atšaukimas.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 87f6bdca30c5779e3d70922e75609ff4cdfca167
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580650"
---
# <a name="cancel-a-project-vendor-invoice"></a>Atšaukti projekto tiekėjo SF

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Patvirtinus tiekėjo SF, jos redaguoti ar panaikinti negalima. Jei patvirtinta tiekėjo SF įvyko klaida, galite naudoti veiksmą Atšaukti, kad atšauktumėte tiekėjo SF poveikį ir sukurtumėte naują tiekėjo SF.

Kai tiekėjo SF pasirenkate **Atšaukti**, įvyksta toks veikimas:

1. Tiekėjo SF būsena atnaujinama į **Atšaukta**.
2. Atšaukta tiekėjo SF ir su ja susiję įrašai tampa skirti tik skaityti ir jų negalima redaguoti ar panaikinti.
3. Visos faktinės savikainos, sukurtos pagal tiekėjo SF eilutes kaip tiekėjo SF patvirtinimo dalį, atšaukiamos.
4. Jei bet kokie faktiniai išlaidų duomenys buvo susieti su tiekėjo SF eilutėmis kaip gretinimo proceso dalis, pradinis tiekėjo SF patvirtinimas jas atšaukė. Atšaukiant tiekėjo SF, šios faktinės išlaidos atkuriamos iš naujo. Kilmė nurodo laiko, išlaidų ar medžiagų naudojimo įrašus.
5. Atšaukę tiekėjo SF, galite dar kartą kurti taisymo žurnalus, apdoroti laiko įrašų atšaukimus ir atšaukti pradinio laiko, išlaidų ar medžiagų faktinių duomenų patvirtinimą.

> [!NOTE]
> Atšaukti galima tik patvirtintas projekto tiekėjo SF. Kitų būsenų tiekėjų SF atšaukti negalima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
