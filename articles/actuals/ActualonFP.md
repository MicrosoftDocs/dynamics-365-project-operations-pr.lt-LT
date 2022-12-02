---
title: Faktinių duomenų poveikis fiksuotos kainos įtraukimui
description: Šiame straipsnyje pateikiama informacija apie įtaką lentelei Faktiniai duomenys, esant įvairiems įvykiams, vykstantiems fiksuotos kainos įtraukimo į „Microsoft Dynamics 365 Project Operations“ ciklo metu.
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
ms.openlocfilehash: 50819d77d56935bfe5438d7d9dae99562bcc0b49
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8918138"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Faktinių duomenų poveikis fiksuotos kainos įtraukimui

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Šioje lentelėje išvardyti skirtingų operacijų tipų faktiniai duomenys, sukurti vykstant įvairiems fiksuotos kainos įtraukimo įvykiams.

| Renginys | Faktinės išlaidos | Pardavimas, už kurį neišrašyta sąskaita | Pardavimo, už kurį išrašyta sąskaita, faktinė suma | Pavyzdžiui |
|---|---|---|---|---|
| Laikas sukurtas. | Netaikoma | Netaikoma | Netaikoma | <p>Bobas Kozackas iš „Fabrikam“ JAV organizacinio vieneto, kurio savikainos tarifas yra 100 JAV dolerių (100 USD) per valandą, dirba su projektu, pavadintu „ARM diegimas „Adatum“. Šis projektas susietas su fiksuotos kainos atsiskaitymo būdu, esančiu sutarties eilutėje. Čia pateiktas Bobo Kozako laiko įrašo pavyzdys:</p><p>Bobas Kozackas – 8 valandos</p> |
| Laikas pateiktas | Netaikoma | Netaikoma | Netaikoma | Sukuriama laiko įrašo sąnaudų žurnalo eilutė. Numatytasis savikainos tarifas įvedamas į žurnalo įrašą. |
| Laiko įrašas atšauktas prieš jį patvirtinant. | Netaikoma | Netaikoma | Netaikoma | |
| Laikas patvirtintas. | Sukuriami savikainos faktiniai duomenys. | Netaikoma | Netaikoma | <p>Sukurti nauji faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD</li></ul> |
| Laiko patvirtinimas atšauktas. | <p>Pradinės savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p> | Netaikoma | Netaikoma | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul> |
| Laiko įrašas atšauktas jį patvirtinus. | <p>Pradinės savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p> | Netaikoma | Netaikoma | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul> |
| Sutartis patvirtinta. | <p>Senų savikainos faktinių duomenų koregavimo būsena atnaujinta į **Pakoreguota**.</p><p>Sukuriami anuliuojami savikainos faktiniai duomenys, kurių būsena yra **Nekoreguojama**.</p><p>Sukuriami nauji savikainos faktiniai duomenys, iš naujo įvertinus sutarties taisykles.</p> | Netaikoma | Netaikoma | <p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD, *Pakoreguota*</li></ul><p>Sukurti nauji faktiniai duomenys, norint panaikinti ankstesnį finansinį poveikį:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, (8 val.), (800 USD), *Nekoreguojama*</li></ul><p>Sukurti nauji iš naujo įvertinto finansinio poveikio faktiniai duomenys:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD</li></ul> |
| Sukurta sąskaita faktūra. | Netaikoma | Netaikoma | Netaikoma | |
| Sąskaita faktūra patvirtinama naudojant etapą. | Netaikoma | Netaikoma | Sukuriami nauji etapais pagrįsti pardavimo faktiniai duomenys. | <p>Esami faktiniai duomenys, kurie lieka nepakeisti:</p><ul><li>**Savikainos faktiniai duomenys:** Bobas Kozackas, 8 val., 800 USD</li></ul><p>Nauji faktiniai duomenys, sukurti pardavimo, už kurį išrašyta sąskaita faktūra, reikšmėms įrašyti:</p><ul><li>**Pardavimo, už kurį išrašyta sąskaita, faktinės suma:** etapas, 5 000 USD</li></ul> |
| Sąskaita faktūra ištaisoma, kad būtų įskaityta į etapą. | Netaikoma | Netaikoma | Sukuriamos anuliuojamos pardavimo, už kurį išrašyta sąskaita, faktinės sumos. | <p>Esami faktiniai duomenys, kurie lieka nepakeisti:</p><ul><li>**Faktinė suma:** Bobas Kozackas, 8 val., 800 USD</li></ul><p>Atnaujinti esami faktiniai duomenys:</p><ul><li>**Pardavimo, už kurį išrašyta sąskaita, faktinės suma**: etapas, 5 000 USD, *pakoreguota*</li></ul><p>Nauji faktiniai duomenys, sukurti pardavimo, už kurį išrašyta sąskaita faktūra, ankstesnėms reikšmėms panaikinti:</p><ul><li>**Pardavimo, už kurį išrašyta sąskaita, faktinės suma**: etapas, (5 000 USD), *nekoreguojama*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
