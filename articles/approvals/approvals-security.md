---
title: Saugumas ir patvirtinimai
description: Šiame straipsnyje pateikiama informacija apie saugos sąranką, skirtą darbui su patvirtinimais programoje "Microsoft"Dynamics 365 Project Operations.
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: bc33f63f66bdcf1470e5d9386cfc3661774436fd
ms.sourcegitcommit: b2d05f898daa552179d67fdf4c060c93a9c66bd1
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/16/2022
ms.locfileid: "9525409"
---
# <a name="security-and-approvals"></a>Saugumas ir patvirtinimai

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

"Microsoft" Dynamics 365 Project Operations naudoja du saugos vaidmenis, kad galėtų patvirtinti laiko, išlaidų ir medžiagų įrašus:

- Projekto tvirtintojas
- Projekto patvirtinimo administratorius

## <a name="project-approver"></a>Projekto tvirtintojas

Turite turėti **projekto patvirtinimo saugos vaidmuo**, kad galėtumėte patvirtinti projekto laiką, išlaidas ir medžiagų įrašus. Taip pat turite turėti prieigą prie atitinkamų susijusių objektų, pvz. **, "Project"**. Šią prieigą gali priskirti asmuo, turintis **projektų vadovo** vaidmenį. Be to, turite būti projekto komandos narys ir pažymėtas kaip tvirtintojas.

Norėdami patvirtinti ne projekto įrašus, turite būti pateikėjo vadovas.

## <a name="project-approver-admin"></a>Projekto patvirtinimo administratorius

> [!NOTE]
> Patvirtinimo [rinkinių](approval-sets.md) funkcija turi būti įjungta, kad galėtumėte naudoti projekto patvirtinimo administratoriaus funkciją.

Projekto **patvirtinimo administratoriaus** saugos vaidmuo leidžia vartotojams apeiti strategijas ir leidžia patvirtinti įrašus visuose projektuose. Šio vaidmens priskyrimas apeis patvirtinimo logiką, kuriai reikia komandos narystės ir žymėjimo kaip tvirtintojo. Turite turėti prieigą prie atitinkamų susijusių objektų, pvz. **, "Project"**. Šią prieigą gali priskirti asmuo, turintis **projektų vadovo** vaidmenį.

SISTEMOS vartotojo kontekstas apeina tikrinimus taip pat, kaip ir projekto patvirtinimo administratoriaus saugos vaidmuo.
