---
title: Projekto komandos kūrimas
description: Šioje temoje pateikta informacija apie tai, kaip sukurti ir valdyti projekto komandas.
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: kdwns
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1ab8ae045852a75a7a39a4eccfa86a114a34273581c98631975bcbfac5a7a343
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7005806"
---
# <a name="create-a-project-team"></a>Kurti projekto komandą

[!include [banner](../includes/banner.md)]

Norėdamas naudoti vaidmenis, kurie buvo anksčiau nustatyti projekte, projekto vadovas turi susieti šiuos vaidmenis su projektu. Projektui galima priskirti kelis vaidmenis. Siekiant išvengti painiavos, šie vaidmenys rezervavimo metu pažymimi automatiškai. Pavyzdžiui, jei projekto vadovui reikia trijų programinės įrangos inžinierių, automatiškai generuojami trys programinės įrangos inžinierių vaidmenys, turintys žymas **1-as programinės įrangos inžinierius**, **2-as programinės įrangos inžinierius** ir **3-ias programinės įrangos inžinierius**. Jei vaidmens charakteristikos anksčiau buvo nustatytos, ieškant išteklių jos taikomos kaip filtras. Jeigu reikia, galima įtraukti papildomų charakteristikų, siekiant dar labiau patikslinti iešką.

Taip pat galima tinkinti rodinio parametrus, siekiant suteikti geresnį išteklių pasiekiamumo rodinį. Galima rodyti pasiekiamumą pagal valandas, dienas, savaites, mėnesius, ketvirčius ir metus. Taip pat galima rodyti pasiekiamą ir likusį išteklių pajėgumą. Ši parinktis naudinga valdant laiką, kai įvertinate galimą veiklos arba išteklių pasiekiamumo laiką.

Projekto vadovas gali puslapyje pasirinkti vaidmenį, tada, jeigu yra pasiekiamas reikalavimus atitinkantis išteklius, pasirinkti rezervuoti išteklių, kad jis atliktų šį vaidmenį. Atkreipkite dėmesį, kad šiame planavimo etape išteklių rezervuoti nereikia. Kai sukursite WBS, galėsite keisti projekto vaidmenis darbuotojams priskirtais ištekliais. Jei vaidmenys keičiami darbuotojams priskirtais ištekliais WBS, išteklių sąranka automatiškai atnaujina projekto komandos sąrašą ir grafiką.

[![Projekto komandos sąrašas, kuriame išvardyti ir vaidmenys, ir faktiniai ištekliai.](./media/projectresourcing03-1024x368.jpg)](./media/projectresourcing03.jpg) 

Projekto vadovas turi įvairių projekto ištekliaus rezervavimo parinkčių, pvz., **Pajėgumo likučio metodas**, **Viso pajėgumo metodas**, **Pajėgumo procentinės dalies rezervavimo metodas** ir **Nurodytos valandos**. Šios rezervavimo parinktys gali būti atšauktos bet kuriuo metu, jei pasikeičia išteklių priskyrimai. Palaikomi du rezervavimo tipai.

- **Rezervuoti galutinai** – rezervuotas išteklius buvo patvirtintas dirbti įtraukime nustatytą laiko tarpą.
- **Preliminarus rezervavimas** – rezervuotas išteklius buvo preliminariai paskirtas dirbti įtraukime nustatytą laiko tarpą.

Tolesne procedūra paaiškinama, kaip sukurti projekto komandą.

## <a name="create-a-project-team"></a>Kurti projekto komandą

1. Sąrašo **Visi projektai** puslapyje pasirinkite projektą, tada pasirinkite **Redaguoti**.
2. Skirtuko **Projekto komanda ir planavimas** lauke **Grafiko pabaigos data** įveskite grafiko pradžios datą plius vieną mėnesį. Pavyzdžiui, jei grafiko pradžios data yra 2017 m. birželio 24 d. (2017-06-24), įveskite **2017-07-24**.
3. Pasirinkite **Įtraukti**.
4. Srityje **Įtraukti vaidmenis į projektą**, lauke **Vaidmuo** pasirinkite **Vyresnysis projektų vadovas**.
5. Pasirinkite **Reikiamos kompetencijos**.
6. Puslapyje **Pasirinkite charakteristikas** charakteristikos, kurias anksčiau nustatėte vyresniojo projektų vadovo vaidmeniui, pasirenkamos pagal numatytuosius nustatymus. Pasirinkite **Gerai**.
7. Puslapyje **Įtraukti vaidmenis į projektą**, lauke **Išteklių skaičius** įveskite **1**.
8. Lauke **Ištekliai**, peržvalgos rodinyje parodomi visi ištekliai, turintys reikiamas kompetencijas. Pasirinkite **Danielis Goldschmidtas**, tada pasirinkite **Kurti**.
9. Puslapyje **Projektas** pasirinkite **Įtraukti**.
10. Srityje **Įtraukti vaidmenis į projektą**, lauke **Vaidmuo** pasirinkite **Komandos narys**. Lauke **Išteklių skaičius** įveskite **5**.
11. Pasirinkite **Kurti**.
12. Puslapyje **Projektai** pasirinkite **Naudoti išteklių**.

## <a name="monitor-project-teams"></a>Stebėkite projektų komandas
1. Puslapyje **Visi projektai** pasirinkite projekto **XYZ Upgrade Phase 2** saitą **Projekto ID**.
2. „FastTab” skirtuke **Projekto komanda ir planavimas** patikrinkite, ar išvardyti projekto ištekliai yra tinkami.


[!INCLUDE[footer-include](../includes/footer-banner.md)]