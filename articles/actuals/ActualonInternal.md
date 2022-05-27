---
title: Faktinis poveikis vidiniam projektui
description: Šioje temoje pateikiama informacija apie poveikį lentelei Aktualijos įvairiuose "Microsoft" vidinio projekto renginiuose Dynamics 365 Project Operations.
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
ms.openlocfilehash: 66a9ac4d2f56ae95313ed6731c3e51926105cff7
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8579776"
---
# <a name="actuals-impact-for-an-internal-project"></a>Faktinis poveikis vidiniam projektui

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Šioje lentelėje išvardijami skirtingų operacijų tipų, sukurtų įvairiuose vidinio projekto įtraukimo renginiuose, faktiniai duomenys.

| Renginys | Faktinės išlaidos | Pavyzdžiui |
|---|---|---|
| Laikas yra sukurtas. | Netaikoma | <p>Bobas Kozackas iš JAV organizacinio padalinio "Fabrikam", kurio išlaidų norma yra 100 JAV dolerių (100 JAV dolerių) per valandą, dirba prie projekto, pavadinto "Rankų montavimas Adatume". Šis projektas susietas su fiksuotos kainos atsiskaitymo metodu sutarties eilutėje. Čia yra bobo Kozako laiko įrašo pavyzdys:</p><p>Bob Kozack - 8 valandos</p> |
| Laikas pateikiamas. | Netaikoma | Sukuriama laiko įrašo išlaidų žurnalo eilutė. Numatytasis savikainos tarifas įvedamas į žurnalo įrašą. |
| Laiko įrašas atšaukiamas prieš jį patvirtinant. | Netaikoma | |
| Laikas patvirtintas. | Sukuriama faktinė savikaina. | <p>Sukurtas naujas faktinis:</p><ul><li>**Faktinė kaina:** Bobas Kozackas, 8 val., USD 800</li></ul> |
| Laiko patvirtinimas atšaukiamas. | <p>Pradinės faktinės savikainos koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriama faktinė atšaukimo savikaina, kurios koregavimo **būsena yra Neapibrėžta**.</p> | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul> |
| Laiko įrašas atšaukiamas po to, kai jis patvirtinamas. | <p>Pradinės faktinės savikainos koregavimo būsena atnaujinama į **Koreguota**.</p><p>Sukuriama faktinė atšaukimo savikaina, kurios koregavimo **būsena yra Neapibrėžta**.</p> | <p>Esamas faktinis, kuris atnaujinamas:</p><ul><li>**Faktinė kaina:** Bob Kozack, 8 val., USD 800, *Pakoreguota*</li></ul><p>Naujas faktinis, sukurtas ankstesniam finansiniam poveikiui pakeisti:</p><ul><li>**Faktinės išlaidos:** Bob Kozack, (8 val.), (800 USD), *Nepataisomas*</li></ul> |

[!INCLUDE[footer-include](../includes/footer-banner.md)]
