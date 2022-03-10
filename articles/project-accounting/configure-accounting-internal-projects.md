---
title: Vidinių projektų apskaitos konfigūravimas
description: Šioje temoje pateikta informacija, kaip nustatyti vidinių projektų apskaitos praktikas naudojant „Project Operations“.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: be1dcd1b6b18591c99c904e0013d9870c7cafe1077fa6e9634f2e9f495190848
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005536"
---
# <a name="configure-accounting-for-internal-projects"></a>Vidinių projektų apskaitos konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Vidiniai projektai įmonėms suteikia galimybę sekti išlaidas, susijusias su veiklomis, už kurias klientui negalima išrašyti sąskaitos faktūros. Vidinių projektų pavyzdžiai.

- Produkto kūrimas, pvz., mobiliųjų įrenginių programėlės, ir su kūrimu susijusių išlaidų sekimas.
- Laiko ir išlaidų valdymas iki pardavimo. Šį vidinį projektą iki pardavimo galima konvertuoti vėliau į apmokestinamą projektą, jei pasiūlymas laimėtas.

Bet kuris su „Dynamics 365 Project Operations“ sutartimi nesusietas projektas laikomas vidiniu. Projekto išlaidų ir pajamų profiliai nėra naudojami nustatant projekto apskaitos taisykles. Vidinio projekto savikaina visada registruojama naudojant pelno ir nuostolio principus. Registravimo DK sąskaitos apibrėžtos puslapyje **DK registravimo sąranka**.

- Laiko operacijos registruojamos atskaitant sumas iš **išlaidų** sąskaitos ir įskaitant jas į **algalapio priskyrimo** sąskaitą.
- Išlaidų operacijos registruojamos atskaitant sumas iš **išlaidų** sąskaitos ir įskaitant jas į **korespondentinę sąskaitą už išlaidas**.
- Prekės operacijos užregistruojamos nurašius lėšas nuo sąskaitos **Išlaidos** ir įdėjus jas į sąskaitą **Išlaidos – prekės**.

Užregistravus operacijas projekte, jei projektas susietas su projekto sutartimi, sistema anuliuoja visas sukauptas operacijas ir sukuria naujas apmokestinamas operacijas. Apmokestinamos operacijos atitinka apskaitos taisykles, apibrėžtas atitinkamame projekto išlaidų ir pajamų profilyje.




[!INCLUDE[footer-include](../includes/footer-banner.md)]
