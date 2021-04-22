---
title: Vidinių projektų apskaitos konfigūravimas
description: Šioje temoje pateikta informacija, kaip nustatyti vidinių projektų apskaitos praktikas naudojant „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 65d05e3a6321dc32aee55c28b3eaa4bd0bae2f86
ms.sourcegitcommit: 5fd529f2308edfe9322082313e6d50146df56aca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/06/2021
ms.locfileid: "5857988"
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
