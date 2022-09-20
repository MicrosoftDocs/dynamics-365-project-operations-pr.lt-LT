---
title: Projekto tiekėjo SF patvirtinimas
description: Šiame straipsnyje paaiškinama, kaip patvirtinti projekto tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations, ir aprašomas projekto tiekėjo SF patvirtinimo finansinis poveikis.
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
# <a name="confirm-project-vendor-invoices"></a>Projekto tiekėjo SF patvirtinimas

_ **Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

Įgalinus parametrą **Rankinis** patvirtinimas pm metodu, tiekėjo sf, kurios sukuriamos naudojant juodraščio Microsoft Dataverse būseną, turi **juodraščio** būseną. Tokiu būdu sukurtos tiekėjo sąskaitos faktūros turi būti peržiūrėtos ir patvirtintos rankiniu būdu. Kai parametras Rankinis **patvirtinimas PM yra išjungtas**, automatiškai patvirtinamos sukurtos Dataverse tiekėjo sąskaitos faktūros. Jokių tolesnių veiksmų nereikia. 

Patikrinę visas tiekėjo SF eilutes Dynamics 365 Project Operations, pasirinkite **Patvirtinti**, kad patvirtintumėte tiekėjo SF.

Kai tiekėjo SF pasirenkate **Patvirtinti**, įvyksta toks veiksmas:

1. Tiekėjo SF būsena atnaujinama į **Patvirtinta**.
1. Patvirtinta tiekėjo SF ir su ja susiję įrašai tampa skirti tik skaityti ir jų negalima redaguoti ar panaikinti.
1. Jei kokios nors savikainos faktinės sumos nurodo tiekėjo SF eilutę kaip susiejimo proceso dalį, visos faktinės savikainos, susietos su nurodyta tiekėjo SF eilute, yra atvirkštinės.
1. Naujos savikainos faktinės sumos sukuriamos naudojant tiekėjo SF eilutėje esančią informaciją.
1. Nebegalite kurti taisymo žurnalų, apdoroti laiko įrašų atšaukimų arba atšaukti pradinio laiko, išlaidų ar esminių faktinių aplinkybių, kurios buvo atšauktos, patvirtinimo.
1. **Dynamics 365 Finance projekto savikainos** reikšmė atnaujinama naudojant žurnalą "Project integration", o įsigijimo integravimo paskyra atšaukiama *po* to, kai paskelbiamas žurnalas "Project" integravimas.

> [!NOTE]
> Jei kurios nors tiekėjo SF eilutės patvirtinimo būsena yra kita nei **Baigta**, tiekėjo SF patvirtinti negalima.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
