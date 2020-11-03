---
title: Vidinių projektų apskaitos konfigūravimas
description: Šioje temoje pateikta informacija, kaip nustatyti vidinių projektų apskaitos praktikas naudojant „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 504e7481cb2aee6310cb4ace2d0791d1c7fe360d
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080770"
---
# <a name="configure-accounting-for-internal-projects"></a>Vidinių projektų apskaitos konfigūravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Vidiniai projektai įmonėms suteikia galimybę sekti išlaidas, susijusias su veiklomis, už kurias klientui negalima išrašyti sąskaitos faktūros. Vidinių projektų pavyzdžiai.

- Produkto kūrimas, pvz., mobiliųjų įrenginių programėlės, ir su kūrimu susijusių išlaidų sekimas.
- Laiko ir išlaidų valdymas iki pardavimo. Šį vidinį projektą iki pardavimo galima konvertuoti vėliau į apmokestinamą projektą, jei pasiūlymas laimėtas.

Bet koks projektas, nesusietas su sutartimi programoje „Dynamics 365 Project Operations“, laikomas vidiniu. Projekto išlaidų ir pajamų profiliai nėra naudojami nustatant projekto apskaitos taisykles. Vidinio projekto savikaina visada registruojama naudojant pelno ir nuostolio principus. Registravimo DK sąskaitos apibrėžtos puslapyje **DK registravimo sąranka**.

- Laiko operacijos registruojamos atskaitant sumas iš **išlaidų** sąskaitos ir įskaitant jas į **algalapio priskyrimo** sąskaitą.
- Išlaidų operacijos registruojamos atskaitant sumas iš **išlaidų** sąskaitos ir įskaitant jas į **korespondentinę sąskaitą už išlaidas**.

Užregistravus operacijas projekte, jei projektas susietas su projekto sutartimi, sistema anuliuoja visas sukauptas operacijas ir sukuria naujas apmokestinamas operacijas. Apmokestinamos operacijos atitinka apskaitos taisykles, apibrėžtas atitinkamame projekto išlaidų ir pajamų profilyje.


