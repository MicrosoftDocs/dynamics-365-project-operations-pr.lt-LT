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
ms.openlocfilehash: ea04178d4327ccd701ab431f172463a13a55154e
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4132388"
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




[!INCLUDE[footer-include](../includes/footer-banner.md)]