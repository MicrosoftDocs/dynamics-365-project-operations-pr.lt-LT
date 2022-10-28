---
title: Sauga ir patvirtinimas
description: Šiame straipsnyje pateikiama informacija apie saugos sąranką dirbant su patvirtinimais "Microsoft"Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709408"
---
# <a name="security-and-approvals"></a>Sauga ir patvirtinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

"Microsoft" Dynamics 365 Project Operations naudoja du saugos vaidmenis, kad leistų patvirtinti laiko, išlaidų ir medžiagų įrašus:

- Projekto tvirtintojas
- "Project Approver" administratorius

## <a name="project-approver"></a>Projekto tvirtintojas

Turite turėti **projekto tvirtintojo** saugos vaidmuo, kad galėtumėte patvirtinti projekto laiką, išlaidas ir medžiagų įrašus. Taip pat turite turėti prieigą prie atitinkamų susijusių objektų, pvz., **"Project"**. Šią prieigą gali priskirti asmuo, **turintis projekto vadovo** vaidmenį. Be to, turite būti projekto komandos narys ir pažymėtas kaip tvirtintojas.

Norėdami patvirtinti ne projekto įrašus, turite būti pateikėjo vadovas.

## <a name="project-approver-admin"></a>"Project Approver" administratorius

> [!NOTE]
> Patvirtinimo [rinkinių](approval-sets.md) funkcija turi būti įjungta, kad galėtumėte naudoti "Project Approver Admin" funkcijas.

"**Project Approver Admin saugos vaidmuo**" leidžia vartotojams apeiti strategijas ir leidžia patvirtinti visų projektų įrašus. Priskyrus šį vaidmenį, bus apeinama tikrinimo logika, reikalaujanti komandos narystės ir pažymėjimo kaip tvirtintojo. Turite turėti prieigą prie atitinkamų susijusių lentelių, pvz., **"Project**", naudodami jums priskirtus saugos vaidmenis.

SYSTEM vartotojo kontekstas apeina patvirtinimus taip pat, kaip saugos vaidmuo Project Approver Admin".
