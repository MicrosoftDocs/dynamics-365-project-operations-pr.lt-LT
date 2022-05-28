---
title: Vidinių projektų apskaitos konfigūravimas
description: Šioje temoje pateikta informacija, kaip nustatyti vidinių projektų apskaitos praktikas naudojant „Project Operations“.
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597854"
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
