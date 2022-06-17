---
title: Projekto tiekėjo sąskaitos faktūros atšaukimas
description: Šiame straipsnyje paaiškinama, kaip atšaukti projekto tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations ir projekto tiekėjo SF atšaukimo finansinis poveikis.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7ddaadc0f6e336a8ba67bb4ad8000f7e894f3eb0
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911560"
---
# <a name="cancel-a-project-vendor-invoice"></a>Projekto tiekėjo sąskaitos faktūros atšaukimas

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
