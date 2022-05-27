---
title: Faktinis poveikis įsipareigojimo prieš pardavimą etape
description: Šioje temoje pateikiama informacija apie poveikį lentelei Aktualijos įvairiuose renginiuose, kai "Microsoft" pasirengimo pardavimui etape yra engagment Dynamics 365 Project Operations.
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
ms.openlocfilehash: ad62639b345d5519b103d4bde3fbb033b9a7a519
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577246"
---
# <a name="actuals-impact-during-the-pre-sales-stage-of-an-engagement"></a>Faktinis poveikis įsipareigojimo prieš pardavimą etape

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Šioje lentelėje išvardyti skirtingų operacijų tipų, sukurtų įvairiuose renginiuose projekto įtraukimo prieš pardavimą etape, faktiniai duomenys.

| Renginys | Faktinės išlaidos | Pavyzdžiui |
|---|---|---|
| Laikas yra sukurtas. | Netaikoma | <p>Bobas Kozackas iš JAV organizacinio padalinio "Fabrikam", kurio išlaidų norma yra 100 JAV dolerių (100 JAV dolerių) per valandą, dirba prie projekto, pavadinto "Rankų montavimas Adatume". Šis projektas susietas su fiksuotos kainos atsiskaitymo metodu sutarties eilutėje. Čia yra bobo Kozako laiko įrašo pavyzdys:</p><p>Bob Kozack - 8 valandos</p> |
| Laikas pateikiamas. | Netaikoma | Sukuriama laiko įrašo išlaidų žurnalo eilutė. Numatytasis savikainos tarifas įvedamas į žurnalo įrašą. |
| Laiko įrašas atšaukiamas prieš jį patvirtinant. | Netaikoma | |
| Laikas patvirtintas. | Sukuriama faktinė savikaina. | <p>Sukurtas naujas faktinis:</p><ul><li>**Faktinė kaina:** Bobas Kozackas, 8 val., USD 800</li></ul> |
| Laiko patvirtinimas atšaukiamas. | <p>Pradinės faktinės savikainos koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriama faktinė atšaukimo savikaina, kurios koregavimo **būsena yra Neapibrėžta**.</p> | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul> |
| Laiko įrašas atšaukiamas po to, kai jis patvirtinamas. | <p>Pradinės faktinės savikainos koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriama faktinė atšaukimo savikaina, kurios koregavimo **būsena yra Neapibrėžta**.</p> | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul> |
| Pasiūlymas laimėtas ir sukuriama sutartis. | <p>Senųjų faktinių išlaidų koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriami atšaukimo savikainos faktiniai duomenys, kurių koregavimo **būsena yra Neapibrėžta**.</p><p>Naujos faktinės išlaidos sukuriamos iš naujo įvertinus sutarties taisykles.</p> | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul><p>Nauji faktiniai duomenys, sukurti iš naujo įvertintam finansiniam poveikiui, kai pasiūlymas laimimas ir sukuriama sutartis:</p><ul><li>**Faktinė kaina:** Bobas Kozackas, 8 val., USD 800</li><li>**Faktiniai pardavimai:** Bobas Kozackas, 8 val., USD 1,600</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
