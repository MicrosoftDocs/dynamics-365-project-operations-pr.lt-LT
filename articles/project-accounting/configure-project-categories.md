---
title: Projekto kategorijų nustatymas
description: Šioje temoje pateikta informacija apie projektų kategorijų nustatymą.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b7adf61a82714a0148d9c8b1d2b2b37fd611c1cf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287518"
---
# <a name="configure-project-categories"></a>Projekto kategorijų nustatymas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

„Project Operations“ teikia patikimas galimybes skirstyti projektų pajamas ir išlaidas į kategorijas. Kategorijos leidžia teikti ataskaitas apie projekto operacijas ir jas analizuoti bei vykdyti registravimą DK.

Šioje diagramoje vaizduojama sąsaja tarp operacijų kategorijų, bendrai naudojamų kategorijų ir projektų kategorijų. 

Operacijų kategorijos yra pagrindinis projektų operacijų grupavimas. Šiame grupavime yra bendrai naudojamų kategorijų, kurias galima bendrai naudoti programose ir moduliuose, rinkinys. Norint dar labiau atsižvelgti į specifiką, projektų kategorijos yra detaliausias kategorijų lygis. Projektų kategorijos yra būdingos juridiniam subjektui, moduliui ir programai.

![Sąsaja tarp operacijų kategorijų, bendrai naudojamų kategorijų ir projektų kategorijų](media/project-categories.png)

## <a name="transaction-categories"></a>Operacijų kategorijos

Operacijų kategorijos atitinka pagrindinį projektų operacijų grupavimą ir jos nėra specifinis įmonės ar operacijos tipas. Pavyzdžiui, „Contoso Robotics“ naudoja dizaino, kelionių, diegimo ir aptarnavimo operacijų kategorijas projektų operacijoms grupuoti.

Operacijų kategorijos apibrėžiamos „Project Operations“ modulyje. 
1. Eikite į **Nustatymai**\>**Operacijų kategorijos**, kad atidarytumėte formą. 
2. Sukurkite naują operacijos kategoriją pasirinkdami **Nauja** arba pažymėdami **Importuoti iš „Excel“**.

## <a name="shared-categories"></a>Bendrai naudojamos kategorijos

„Dynamics 365“ bendro naudojimo kategorijų sąvoka naudojama išlaidoms suskirstyti skirtingose programose, pvz., „Dynamics 365 Finance“ „Dynamics 365 Supply Chain“ ir „Dynamics 365 Project Operations“. Kiekvienai sukurtai operacijos kategorijai „Project Operations“ automatiškai sukuria keturias susijusias bendrai naudojamas kategorijas: valandos, išlaidos, mokesčiai ir elementas. Bendrai naudojamas kategorijas galite peržiūrėti ir koreguoti nuėję į **Projektų valdymas ir apskaita**\>**Nustatymas**\>**Kategorijas**\>**Bendrai naudojamos kategorijos**.

## <a name="project-categories"></a>Projekto kategorijos

Projekto kategorijos atitinka detaliausią kategorijos konfigūravimo lygį ir jas turi atskirai kiekvienai įmonei konfigūruoti projekto apskaitininkas.

1. Eikite į **Projektų valdymas ir apskaita**\>**Nustatymas**\>**Kategorijos**\>**Projekto kategorijos**.
2. Pasirinkite **Naujas**.
3. Pasirinkite bendrai naudojamos kategorijos, kurią sukūrėte ankstesniame skyriuje, **Kategorijos ID**. „Project Operations“ leidžia naudoti tik tas bendrai naudojamas kategorijas, kurios susietos su operacijų kategorijomis.
4. Kategorijos grupės pasirinkimas.

## <a name="category-groups"></a>Kategorijos grupės

Kategorijų grupės naudojamos norint dalytis ypatybėms, visų pirma registravimo profiliais, tarp susijusių projektų kategorijų. Kiekvienam operacijos tipui turi būti bent viena kategorijos grupė, o kiekvienai projekto kategorijai priskiriama grupė.

„Project Operations“ registravimo specifikacijas apibrėžia projekto išlaidų ir pajamų profilio taisyklės, projektų kategorijos ir kategorijų grupės. Galite nustatyti kategorijų grupes nuėję į **Projektų valdymas ir apskaita**\>**Nustatymai**\>**Kategorijos**\>**Kategorijų grupės**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]