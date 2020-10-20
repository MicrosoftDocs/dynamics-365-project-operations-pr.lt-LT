---
title: Dienpinigiai
description: Šioje temoje pateikta informacija apie dienpinigių taisykles, kurios naudojamos išlaidų valdyme.
author: suvaidya
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 7d1c4ac7781cb711e2cc0d09606d422b4dd554f3
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908388"
---
# <a name="per-diems"></a>Dienpinigiai

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Dienpinigiai yra pašalpa, mokama darbuotojui, kuris keliauja darbo reikalais. Išlaidų valdyme galite sukurti dienpinigius skirtingoms keliavimo situacijoms. Dienpinigiai gali būti pagrįsti metų laiku, kelionės vieta arba abiem. Kai sukuriate dienpinigius, galite nurodyti, kad už dienpinigius procentinė dalis bus išskaičiuota, jei darbuotojas gaus papildomą maitinimą ar aptarnavimą. Taip pat galite nustatyti mažiausią ir didžiausią valandų skaičių, už kurias būtų skiriami dienpinigiai darbuotojui keliaujant.

## <a name="configuration"></a>Konfigūracija 

1. Norėdami įtraukti dienpinigius, eikite į **Sąranka** > **Skaičiavimai ir kodai** > **Dienpinigių vietos**.
2. Kiekvienai įtrauktai vietai pažymėkite dienpinigius ir valiutą, galiojančią nuo konkrečios pradžios iki pabaigos datos viešbučiui, maitinimuisi ir kitoms išlaidoms. Dienpinigiai ir valiutos sukonfigūruojami **Sąranka** > **Skaičiavimai ir kodai** > **Dienpinigiai**.
3. Puslapyje **Dienpinigių vietos** konfigūruokite dienpinigių normas. Dienpinigių normos leidžia apibrėžti viešbučių, maitinimosi ir kitų išlaidų dienos pašalpos procentinę dalį. 
4. Jei norite nurodyti mažesnę procentinę dalį pusryčiams, pietums arba vakarienei, atnaujinkite laukų, esančių puslapio **Išlaidų valdymo parametrai** skirtuke **Dienpinigiai**, reikšmes. 
    
## <a name="submit-expenses-using-per-diem"></a>Pateikti išlaidas pagal dienpinigius
Norėdami pateikti išlaidas, panaudojant dienpinigius, kurdami išlaidų ataskaitą naudokite išlaidų kategoriją **Dienpinigiai**. Įveskite reikšmes **Dienpinigiai nuo datos**, **Dienpinigiai iki datos** ir **Dienpinigių vietos**. Suma bus apskaičiuota pagal pasirinktos vietos dienpinigius, o mažesnė procentinė dalis už maistą bus apskaičiuota pagal dienpinigių normas.
