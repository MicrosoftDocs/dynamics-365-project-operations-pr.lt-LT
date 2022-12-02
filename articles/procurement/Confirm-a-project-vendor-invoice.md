---
title: Projekto tiekėjo sąskaitų faktūrų patvirtinimas
description: Šiame straipsnyje paaiškinta, kaip patvirtinti projekto tiekėjo sąskaitą faktūrą programoje „Microsoft Dynamics 365 Project Operations“, ir aprašomas projekto tiekėjo sąskaitos faktūros patvirtinimo finansinis poveikis.
author: suvaidya
ms.date: 8/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: suvaidya
ms.openlocfilehash: 9739b15753aa34c51a0aa1e6dfeb7f590655ca7a
ms.sourcegitcommit: 60a34a00e2237b377c6f777612cebcd6380b05e1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/13/2022
ms.locfileid: "9475476"
---
# <a name="confirm-project-vendor-invoices"></a>Projekto tiekėjo sąskaitų faktūrų patvirtinimas

_ **Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

Kai įjungtas parametras **Reikalingas PM rankinis patvirtinimas**, programoje „Microsoft Dataverse“ sukurtų tiekėjo sąskaitų faktūrų būsena yra **Juodraštis**. Taip sukurtas tiekėjo sąskaitas faktūras reikia peržiūrėti ir patvirtinti rankiniu būdu. Kai parametras **Reikalingas PM rankinis patvirtinimas,** išjungtas, programoje „Dataverse“ sukurtos tiekėjo sąskaitos faktūros patvirtinamos automatiškai. Nereikia atlikti jokių tolesnių veiksmų. 

Programoje „Dynamics 365 Project Operations“ patikrinę visas tiekėjo sąskaitos faktūros eilutes, pasirinkite **Patvirtinti**, kad patvirtintumėte tiekėjo sąskaitą faktūrą.

Kai tiekėjo sąskaitai faktūrai pasirenkate **Patvirtinti**, įvyksta tokie dalykai:

1. Tiekėjo sąskaitos faktūros būsena atnaujinama į **Patvirtinta**.
1. Patvirtinta tiekėjo sąskaita faktūra ir su ja susiję įrašai tampa tik skaitomi, jų negalima redaguoti ar naikinti.
1. Jei gretinimo proceso metu kokie nors savikainos faktiniai duomenys nurodo tiekėjo sąskaitos faktūros eilutę, visi savikainos faktiniai duomenys, susieti su nurodoma tiekėjo sąskaitos faktūros eilute, atšaukiami.
1. Nauji savikainos faktiniai duomenys sukuriami naudojant informaciją, esančią tiekėjo sąskaitos faktūros eilutėje.
1. Nebegalite kurti koregavimo žurnalų, apdoroti laiko įrašų atšaukimų ar atšaukti pradinio laiko, išlaidų ar medžiagos faktinių duomenų, kurie buvo atšaukti, patvirtinimo.
1. Programoje „Dynamics 365 Finance“ reikšmė **Projekto savikaina**‟ atnaujinama naudojant „Project“ integravimo žurnalą, o jį užregistravus *atšaukiama* įsigijimo integravimo sąskaita.

> [!NOTE]
> Jei kurios nors tiekėjo sąskaitos faktūros eilutės tikrinimo būsena yra ne **Atlikta**, tiekėjo sąskaitos faktūros patvirtinti negalima.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
