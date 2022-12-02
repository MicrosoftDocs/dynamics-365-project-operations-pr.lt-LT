---
title: Projekto tiekėjo sąskaitos faktūros atšaukimas
description: Šiame straipsnyje paaiškinta, kaip atšaukti projekto tiekėjo sąskaitą faktūrą programoje „Microsoft Dynamics 365 Project Operations“, ir projekto tiekėjo sąskaitos faktūros atšaukimo finansinis poveikis.
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

Patvirtinus tiekėjo sąskaitą faktūrą, jos negalima redaguoti ar panaikinti. Jei patvirtintoje tiekėjo sąskaitoje faktūroje yra klaida, naudodami veiksmą Atšaukti galite anuliuoti tiekėjo sąskaitos faktūros poveikį ir sukurti naują tiekėjo sąskaitą faktūrą.

Kai tiekėjo sąskaitai faktūrai pasirenkate **Atšaukti**, įvyksta tokie dalykai:

1. Tiekėjo sąskaitos faktūros būsena atnaujinama į **Atšaukta**.
2. Atšaukta tiekėjo sąskaita faktūra ir su ja susiję įrašai tampa tik skaitomi, jų negalima redaguoti ar naikinti.
3. Visi savikainos faktiniai duomenys, kurie buvo sukurti pagal tiekėjo sąskaitos faktūros eilutes kaip tiekėjo sąskaitos faktūros patvirtinimo dalis, yra atšaukiami.
4. Jei gretinimo proceso metu kokie nors savikainos faktiniai duomenys buvo susieti su tiekėjo sąskaitos faktūros eilutėmis, pradinės tiekėjo sąskaitos faktūros patvirtinimas juos atšaukė. Atšaukiant tiekėjo sąskaitą faktūrą šie savikainos faktiniai duomenys sukuriami iš naujo. Kilmė nurodo laiko, išlaidų arba medžiagos naudojimo įrašus.
5. Atšaukę tiekėjo sąskaitą faktūrą, galite dar kartą sukurti koregavimo žurnalus, apdoroti laiko įrašų atšaukimus ir atšaukti pradinio laiko, išlaidų ar medžiagos faktinių duomenų patvirtinimą.

> [!NOTE]
> Galima atšaukti tik patvirtintas projekto tiekėjo sąskaitas faktūras. Kitų būsenų tiekėjo sąskaitų faktūrų atšaukti negalima.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
