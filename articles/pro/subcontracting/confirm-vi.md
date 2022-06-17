---
title: Projekto tiekėjo sąskaitos faktūros patvirtinimas
description: Šiame straipsnyje paaiškinama, kaip patvirtinti projekto tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations ir projekto tiekėjo SF patvirtinimo finansinį poveikį.
author: rumant
ms.date: 03/30/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 092b3cd5981f7d9bb8767c7a2acb2f4952801d06
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932444"
---
# <a name="confirm-a-project-vendor-invoice"></a>Projekto tiekėjo sąskaitos faktūros patvirtinimas

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Patikrinę visas "Microsoft" Dynamics 365 Project Operations tiekėjo SF eilutes, galite naudoti veiksmą Patvirtinti, kad patvirtintumėte tiekėjo SF.

Kai tiekėjo SF pasirenkate **Patvirtinti**, įvyksta toks veikimas:

1. Tiekėjo SF būsena atnaujinama į **Patvirtinta**.
2. Patvirtinta tiekėjo SF ir su ja susiję įrašai tampa skirti tik skaityti ir jų negalima redaguoti ar panaikinti.
3. Jei kokie nors faktiniai išlaidų rodikliai nurodo tiekėjo SF eilutę kaip gretinimo proceso dalį, visi išlaidų faktiniai duomenys, susieti su nurodyta tiekėjo SF eilute, atšaukiami.
4. Naujos savikainos faktinės sumos sukuriamos naudojant tiekėjo SF eilutės informaciją.
5. Patvirtinus tiekėjo SF, nebegalite kurti taisymo žurnalų, apdoroti laiko įrašų atšaukimų arba atšaukti atšauktų pradinio laiko, išlaidų ar medžiagų faktinių duomenų patvirtinimo.

> [!NOTE]
> Jei kurios nors tiekėjo SF eilutės tikrinimo būsena yra kita nei **Baigta**, tiekėjo SF patvirtinti negalima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
