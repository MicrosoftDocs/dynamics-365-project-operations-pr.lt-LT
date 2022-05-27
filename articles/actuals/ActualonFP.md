---
title: Faktinis poveikis fiksuotos kainos įtraukimui
description: Šioje temoje pateikiama informacija apie poveikį lentelei Aktualijos įvairiuose įvykiuose per fiksuotos kainos įtraukimo į "Microsoft" gyvavimo ciklą Dynamics 365 Project Operations.
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
ms.openlocfilehash: 222e7c5eefd7c619e4d7389cdaff2f96176ff275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579238"
---
# <a name="actuals-impact-in-a-fixed-price-engagement"></a>Faktinis poveikis fiksuotos kainos įtraukimui

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Šioje lentelėje išvardyti skirtingų operacijų tipų, sukurtų įvairiuose įvykiuose pagal fiksuotos kainos įtraukimą, faktiniai duomenys.

| Renginys | Faktinės išlaidos | Pardavimas, už kurį neišrašyta sąskaita | Faktiniai pardavimai, už kuriuos išrašyta sf | Pavyzdžiui |
|---|---|---|---|---|
| Laikas yra sukurtas. | Netaikoma | Netaikoma | Netaikoma | <p>Bobas Kozackas iš JAV organizacinio padalinio "Fabrikam", kurio išlaidų norma yra 100 JAV dolerių (100 JAV dolerių) per valandą, dirba prie projekto, pavadinto "Rankų montavimas Adatume". Šis projektas susietas su fiksuotos kainos atsiskaitymo metodu sutarties eilutėje. Čia yra bobo Kozako laiko įrašo pavyzdys:</p><p>Bob Kozack - 8 valandos</p> |
| Laikas pateikiamas. | Netaikoma | Netaikoma | Netaikoma | Sukuriama laiko įrašo išlaidų žurnalo eilutė. Numatytasis savikainos tarifas įvedamas į žurnalo įrašą. |
| Laiko įrašas atšaukiamas prieš jį patvirtinant. | Netaikoma | Netaikoma | Netaikoma | |
| Laikas patvirtintas. | Sukuriama faktinė savikaina. | Netaikoma | Netaikoma | <p>Sukurtas naujas faktinis:</p><ul><li>**Faktinė kaina:** Bobas Kozackas, 8 val., USD 800</li></ul> |
| Laiko patvirtinimas atšaukiamas. | <p>Pradinės faktinės savikainos koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriama faktinė atšaukimo savikaina, kurios koregavimo **būsena yra Neapibrėžta**.</p> | Netaikoma | Netaikoma | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul> |
| Laiko įrašas atšaukiamas po to, kai jis patvirtinamas. | <p>Pradinės faktinės savikainos koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriama faktinė atšaukimo savikaina, kurios koregavimo **būsena yra Neapibrėžta**.</p> | Netaikoma | Netaikoma | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul> |
| Sutartis patvirtinta. | <p>Senųjų faktinių išlaidų koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriami atšaukimo savikainos faktiniai duomenys, kurių koregavimo **būsena yra Neapibrėžta**.</p><p>Naujos faktinės išlaidos sukuriamos iš naujo įvertinus sutarties taisykles.</p> | Netaikoma | Netaikoma | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul><p>Naujas faktinis, sukurtas iš naujo įvertintam finansiniam poveikiui:</p><ul><li>**Faktinė kaina:** Bobas Kozackas, 8 val., USD 800</li></ul> |
| Sukuriama SF. | Netaikoma | Netaikoma | Netaikoma | |
| Sąskaita faktūra patvirtinama orientyru. | Netaikoma | Netaikoma | Sukuriami nauji etapais pagrįsti pardavimo faktai, kuriems išrašytos sąskaitos. | <p>Esamas faktinis, kuris lieka nepakitęs:</p><ul><li>**Faktinė kaina:** Bobas Kozackas, 8 val., USD 800</li></ul><p>Naujas faktinis, sukurtas pardavimo vertėms, už kurias išrašyta sf, įrašyti:</p><ul><li>**Faktiniai pardavimai, už kuriuos išrašyta sąskaita:** orientyras, USD 5,000</li></ul> |
| Sf pataisoma, kad būtų galima įskaityti tarpinį etapą. | Netaikoma | Netaikoma | Sukuriami atšaukimo pardavimo, už kurį išrašyta sf, faktinės sumos. | <p>Esamas faktinis, kuris lieka nepakitęs:</p><ul><li>**Faktinė kaina:** Bob kozack, 8 val., 800 USD</li></ul><p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktiniai pardavimai, už kuriuos išrašyta sąskaita:** orientyras, USD 5,000, *koreguotas*</li></ul><p>Naujas faktinis, sukurtas pakeisti ankstesnes pardavimo vertes, už kurias išrašyta sf:</p><ul><li>**Faktiniai pardavimai, už kuriuos išrašyta sąskaita:** orientyras (5 000 JAV dolerių), *Nepataisomas*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
