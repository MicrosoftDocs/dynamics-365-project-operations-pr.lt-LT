---
title: Projekto tiekėjo sąskaitos faktūros patvirtinimas
description: Šiame straipsnyje paaiškinta, kaip patvirtinti projekto tiekėjo sąskaitą faktūrą programoje „Microsoft Dynamics 365 Project Operations“, ir projekto tiekėjo sąskaitos faktūros patvirtinimo finansinis poveikis.
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

Programoje „Microsoft Dynamics 365 Project Operations“ patikrinę visas tiekėjo sąskaitos faktūros eilutes, galite naudoti veiksmą Patvirtinti, kad patvirtintumėte tiekėjo sąskaitą faktūrą.

Kai tiekėjo sąskaitai faktūrai pasirenkate **Patvirtinti**, įvyksta tokie dalykai:

1. Tiekėjo sąskaitos faktūros būsena atnaujinama į **Patvirtinta**.
2. Patvirtinta tiekėjo sąskaita faktūra ir su ja susiję įrašai tampa tik skaitomi, jų negalima redaguoti ar naikinti.
3. Jei gretinimo proceso metu kokie nors savikainos faktiniai duomenys nurodo tiekėjo sąskaitos faktūros eilutę, visi savikainos faktiniai duomenys, susieti su nurodoma tiekėjo sąskaitos faktūros eilute, atšaukiami.
4. Nauji savikainos faktiniai duomenys sukuriami naudojant informaciją, esančią tiekėjo sąskaitos faktūros eilutėje.
5. Patvirtinę tiekėjo sąskaitą faktūrą, nebegalite kurti koregavimo žurnalų, apdoroti laiko įrašų atšaukimų ar atšaukti pradinio laiko, išlaidų ar medžiagos faktinių duomenų, kurie buvo atšaukti, patvirtinimo.

> [!NOTE]
> Jei kurios nors tiekėjo sąskaitos faktūros eilutės tikrinimo būsena yra ne **Atlikta**, tiekėjo sąskaitos faktūros patvirtinti negalima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
