---
title: Faktinių duomenų poveikis vidiniam projektui
description: Šiame straipsnyje pateikiama informacija apie įtaką lentelei Faktiniai duomenys, esant įvairiems „Microsoft Dynamics 365 Project Operations“ vidinio projekto įvykiams.
author: rumant
ms.date: 02/22/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: de05714c079fe121ef68e28b1acb82c24bce095e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921358"
---
# <a name="actuals-impact-for-an-internal-project"></a>Faktinių duomenų poveikis vidiniam projektui

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Šioje lentelėje išvardyti skirtingų operacijų tipų faktiniai duomenys, sukurti vykstant įvairiems vidinio projekto įtraukimo įvykiams.

| Renginys | Faktinės išlaidos | Pavyzdžiui |
|---|---|---|
| Laikas sukurtas. | Netaikoma | <p>Bobas Kozackas iš „Fabrikam“ JAV organizacinio vieneto, kurio savikainos tarifas yra 100 JAV dolerių (100 USD) per valandą, dirba su projektu, pavadintu „ARM diegimas „Adatum“. Šis projektas susietas su fiksuotos kainos atsiskaitymo būdu, esančiu sutarties eilutėje. Čia pateiktas Bobo Kozako laiko įrašo pavyzdys:</p><p>Bobas Kozackas – 8 valandos</p> |
| Laikas pateiktas | Netaikoma | Sukuriama laiko įrašo sąnaudų žurnalo eilutė. Numatytasis savikainos tarifas įvedamas į žurnalo įrašą. |
| Laiko įrašas atšauktas prieš jį patvirtinant. | Netaikoma | |
| Laikas patvirtintas. | Sukuriami savikainos faktiniai duomenys. | <p>Sukurti nauji faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD</li></ul> |
| Laiko patvirtinimas atšauktas. | <p>Pradinės savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p> | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul> |
| Laiko įrašas atšauktas jį patvirtinus. | <p>Pradinės savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p> | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
