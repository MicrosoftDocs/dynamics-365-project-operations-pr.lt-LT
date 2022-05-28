---
title: Projekto įvertinimo šalinimas
description: Šioje temoje pateikta informacija apie užbaigto projekto įvertinimo pašalinimą.
author: Yowelle
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 267b5ffab7ef3a6776c31100deea81fb523752b6
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2022
ms.locfileid: "8684100"
---
# <a name="eliminate-a-project-estimate"></a>Projekto įvertinimo šalinimas

[!include [banner](../includes/banner.md)]

Projekto įvertinimai nurodomi finansiniame rodinyje to projekto darbo, kuris įvertintas ir suplanuotas. Norėdami naudoti projekto įvertinimus, turite pridėti projektą prie įvertinimo projekto. Įvertinimo projektas visada paremtas esamu projektu, tačiau keli projektai gali nurodyti vieną įvertinimo projektą. Prie įvertinimo projektų galima pridėti tik fiksuotos kainos ir investicinius projektus, o tie projektai turi priklausyti tai pačiai projektų grupei kaip ir įvertinimo projektas.

Jei norite pašalinti įvertinamo projektą, jis turi būti užbaigtas. Toliau aprašyti veiksmai paaiškina, kaip pašalinti įvertinimą.

1. Pasirinkite **Projektų valdymas ir apskaita** > **Visi projektai** ir atidarykite projektą. 
2. Skirtuke **Tvarkyti** pasirinkite **Įvertinimai** ir puslapyje **Įvertinimas** pasirinkite **Šalinti**.
3. Puslapio **Šalinti įvertinimą** skirtuke **Bendra** nustatykite toliau nurodytas parinktis.

   - **Laikotarpio kodas**: pasirinkite laikotarpio kodą, kad pasirinktumėte tinkamus įvertinimo projektus. 
   - **Įvertinimo data**: pasirinkite tinkamą įvertinimo šalinimo datą.
   - **Šalinti su NG įspėjimais**: įjunkite šią parinktį norėdami pateikti pranešimą, kai pašalinamas įvertinimas, susietas su nebaigta gamyba (NG). Kai ši parinktis neįjungta, pašalinimo tęsti negalima, jei yra neįvertintų operacijų. 
   > [!NOTE]
   > Ši parinktis galima tik tada, kai šalinimas taikomas įvertinimo projektui. Ji nepasiekiama, jei naudojate periodinius registravimus. Šis parametras suderinamas su parametrais, esančiais puslapio **Projekto parametrai** skirtuke **Įvertinimas**, laukų grupėje **Leisti pašalinti, kai yra neįvertintų operacijų**.
   - **Nustatyti etapą kaip baigtą**: įjunkite šią parinktį, kad atlikus šalinimą būtų nustatytas įvertinimo projekto etapas **Baigtas**.
   - **Spausdinti įvertinimo sąrašą**: pasirinkite, kad informacija būtų įtraukta į spausdinamą įvertinimo sąrašą.
   - **Rodyti sistemos pranešimą**: įjunkite šią parinktį, kad būtų rodomas sistemos pranešimas.
   - **Registravimo data**: pasirinkite įvertinimo DK registravimo datą.

4.  Pasirinkite **Gerai**.
5. Baigus šalinimo procesą, pašalintas įvertinimo projektas rodomas su neigiama reikšme. 

Jei neketinote panaikinti įvertinimo, galite pasirinkti pašalintus įvertinimus ir pasirinkti **Anuliuoti**.   


[!INCLUDE[footer-include](../includes/footer-banner.md)]