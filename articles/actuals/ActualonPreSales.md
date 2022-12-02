---
title: Faktinių duomenų poveikis įtraukimui etape iki pardavimo
description: Šiame straipsnyje pateikiama informacija apie įtaką lentelei Faktiniai duomenys, esant įvairiems įvykiams, kai įtraukimas yra „Microsoft Dynamics 365 Project Operations“ etape prieš pardavimą.
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
ms.openlocfilehash: d03d6ac2154806189d0d9d0b232bb317f51071ba
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922370"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Faktinių duomenų poveikis įtraukimui etape iki pardavimo

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Šioje lentelėje išvardyti skirtingų operacijų tipų faktiniai duomenys, sukurti vykstant įvairiems projekto įtraukimo etapo prieš pardavimą įvykiams.

| Renginys | Faktinės išlaidos | Pavyzdžiui |
|---|---|---|
| Laikas sukurtas. | Netaikoma | <p>Bobas Kozackas iš „Fabrikam“ JAV organizacinio vieneto, kurio savikainos tarifas yra 100 JAV dolerių (100 USD) per valandą, dirba su projektu, pavadintu „ARM diegimas „Adatum“. Šis projektas susietas su fiksuotos kainos atsiskaitymo būdu, esančiu sutarties eilutėje. Čia pateiktas Bobo Kozako laiko įrašo pavyzdys:</p><p>Bobas Kozackas – 8 valandos</p> |
| Laikas pateiktas | Netaikoma | Sukuriama laiko įrašo sąnaudų žurnalo eilutė. Numatytasis savikainos tarifas įvedamas į žurnalo įrašą. |
| Laiko įrašas atšauktas prieš jį patvirtinant. | Netaikoma | |
| Laikas patvirtintas. | Sukuriami savikainos faktiniai duomenys. | <p>Sukurti nauji faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD</li></ul> |
| Laiko patvirtinimas atšauktas. | <p>Pradinės savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p> | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul> |
| Laiko įrašas atšauktas jį patvirtinus. | <p>Pradinės savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p> | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul> |
| Pasiūlymas laimėtas ir sutartis sukurta. | <p>Senų savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p><p>Sukuriami nauji savikainos faktiniai duomenys, iš naujo įvertinus sutarties taisykles.</p> | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul><p>Nauji faktiniai duomenys, sukurti iš naujo įvertintam finansiniam poveikiui, kai pasiūlymas laimėtas ir sukurta sutartis:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD</li><li>**Pardavimo, už kurį neišrašyta sąskaita, faktinė suma:** Bobas Kozackas, 8 val., 1 600 USD</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
