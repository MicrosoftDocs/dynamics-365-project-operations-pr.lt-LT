---
title: Sauga ir patvirtinimas
description: Šiame straipsnyje pateikta informacija apie saugos sąranką darbui su patvirtinimais programoje „Microsoft Dynamics 365 Project Operations“.
author: stsporen
ms.date: 08/29/2022
ms.topic: conceptual
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 88186485dff43c3011095b267640151948b4d77c
ms.sourcegitcommit: 0d11377bf3ac74c80afbd2013775fcc9869f926a
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/10/2022
ms.locfileid: "9841934"
---
# <a name="security-and-approvals"></a>Sauga ir patvirtinimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Microsoft Dynamics 365 Project Operations“ naudojami du saugos vaidmenys, kad leistų patvirtinti laiką, išlaidas ir medžiagos įrašus:

- Projekto tvirtintojas
- Projektų tvirtinimo administratorius

## <a name="project-approver"></a>Projekto tvirtintojas

Privalote turėti saugos vaidmenį **Projekto tvirtintojas**, kad galėtumėte tvirtinti projekto laiką, išlaidas ir medžiagos įrašus. Taip pat privalote turėti prieigą prie atitinkamų susijusių objektų, pvz., **Projektas**. Šią prieigą gali priskirti asmuo, kuriam priskirtas vaidmuo **Projektų vadovas**. Be to, turite būti projekto komandos narys ir būti pažymėtas kaip tvirtintojas.

Jei norite patvirtinti ne projekto įrašus, turite būti pateikėjo vadovas.

## <a name="project-approver-admin"></a>Projektų tvirtinimo administratorius

> [!NOTE]
> Kad būtų galima naudoti projektų tvirtinimo administratoriaus funkciją, turi būti įjungta funkcija [Patvirtinimo rinkiniai](approval-sets.md).

Saugos vaidmuo **Projektų tvirtinimo administratorius** leidžia vartotojams apeiti strategijas ir leidžia patvirtinti visų projektų įrašus. Šio vaidmens priskyrimas apeis tikrinimo logiką, pagal kurią būtina turėti komandos narystę ir būti pažymėtam kaip tvirtintojas. Per jums priskirtus saugos vaidmenis privalote turėti prieigą prie atitinkamų susijusių lentelių, pvz., **Projektas**.

SISTEMOS vartotojo kontekstas apeina tikrinimą taip pat, kaip ir saugos vaidmuo Projektų tvirtinimo administratorius.
