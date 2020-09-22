---
title: Projekto eiga ir sąnaudos
description: Šioje temoje pateikta informacija apie tai, kaip sekti projekto eigą ir sąnaudas.
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 0d742164-5469-421d-8917-63160a81f651
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 8aa5814938129f30885d8161a7c86197ab013364
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753754"
---
# <a name="project-progress-and-cost-consumption"></a>Projekto eiga ir sąnaudos

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Poreikis sekti eigą atsižvelgiant į grafiką, priklauso nuo pramonės šakos. Kai kurie pramonės šakų atstovai seka projektą stambiu planu, o kitų pramonės šakų atstovai seka eigą bendru planu. Šioje temoje nurodyta, kaip planuoti norint atitikti jūsų organizacijos reikalavimus.

## <a name="effort-tracking-view"></a>Pastangų sekimo rodinys

Rodinyje **Pastangų sekimas** sekama užduočių eiga grafike. Jame faktinės pastangų valandos, iki šiol sugaištos atliekant užduotį, lyginamos su suplanuotomis užduoties pastangų valandomis. Norėdami apskaičiuoti sekimo metriką, PSA naudoja šias formules:

- Eiga procentais = iki šios datos naudotos faktinės pastangos ÷ planuojamų užduoties pastangų 
- Įvertinimas užbaigti (ETC) = planuojamos pastangos – iki šios datos naudotos faktinės pastangos 
- Įvertinimas pabaigoje (EAC) = likusios pastangos – iki šios datos naudotos faktinės pastangos 
- Numatomos pastangos nuokrypis = planuojamos pastangos – EAC

PSA rodoma pastangų nuokrypio projekcija užduočiai. Jei EAC yra daugiau nei planuojamų pastangų, užduotis prognozuojama užtrukti ilgiau nei buvo planuota iš pradžių. Todėl pagal grafiką ją vėluojama atlikti. Jei EAC yra mažiau nei planuojamų pastangų, užduotis prognozuojama užtrukti trumpiau nei buvo planuota iš pradžių. Todėl ji įgyvendinama greičiau nei nurodyta grafike.

## <a name="re-projecting-effort"></a>Projekto pakartotinė prognozė

Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas. Projekto pakartotinės prognozės yra projekto vadovo, atsižvelgiant į dabartinę projekto būseną, įvertinimų suvokimas. Tačiau nerekomenduojame projekto vadovams keisti pradinių skaičių, nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.

Yra du būdai, kaip projektų vadovas gali iš naujo sukurti užduotis pastangų prognozę:

- Perrašyti numatytuosius ETC nustatymus su nauju užduoties likusių pastangų įvertinimu. 
- Perrašyti numatytuosius eigos procentais nustatymus su nauju užduoties patikslintos eigos įvertinimu.

Dėl kiekvieno iš šių metodų perskaičiuojamos užduoties ETC, EAC bei eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.

## <a name="re-projection-of-effort-on-summary-tasks"></a>Pakartotinė pastangų suvestinėms užduotims prognozė

Pastangas suvestinėms užduotims ir konteinerio užduotims galima dar kartą prognozuoti. Neatsižvelgiant į tai, ar vartotojas pakartotinai kurs suvestinių užduočių prognozę pagal likusiais pastangas ar eigą procentais, tokie skaičiavimo procesai pradedami vykdyti:

- Užduoties EAC, ETC bei eiga procentais apskaičiuojami.
- Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis užduoties EAC.
- Naujas kiekvienos individualios užduoties iki lapo mazgo užduočių EAC apskaičiuojamas. 
- Paveiktų antrinių užduočių iki lapų mazgų ETC ir eiga procentais perskaičiuojami pagal EAC reikšmę. Taip sukuriama nauja pastangų užduočiai nuokrypio prognozė. 
- Suvestinių užduočių iki šaknies mazgo EAC perskaičiuojamas.

### <a name="cost-tracking-view"></a>Savikainos sekimo rodinys 

Rodinyje **Savikainos sekimas** lyginama faktinė savikaina užduočiai atlikti su planuojama užduoties savikaina. 

> [!NOTE]
> Šiame rodinyje rodomos tik darbo savikainos ir nėra įtraukiamos savikainos iš išlaidų įvertinimų. 

Norėdami apskaičiuoti sekimo metriką, PSA naudoja šias formules:

- Sąnaudų procentinė dalis = iki šios datos naudota faktinė savikaina ÷ planuojama užduoties savikaina
- Savikaina užbaigti (CTC) = planuojama savikaina – iki šios datos naudota savikaina
- EAC = CTC + iki šios datos naudota faktinė savikaina
- Prognozuojamas savikainos nuokrypis = planuojama savikaina – EAC

Rodoma savikainos nuokrypio užduočiai prognozė. Jei EAC yra daugiau nei planuojama savikaina, užduotis prognozuojama kainuosianti daugiau nei buvo planuota iš pradžių. Todėl biudžetas viršijamas. Jei EAC yra mažiau nei planuojama savikaina, užduotis prognozuojama kainuosianti daugiau nei buvo planuota iš pradžių. Todėl biudžetas nėra viršijamas.

## <a name="project-managers-re-projection-of-cost"></a>Projekto vadovo nauja išlaidų prognozė

Kai pastangos yra iš naujo prognozuojamos, CTC, EAC, sąnaudų procentinė dalis ir prognozuojamas savikainos nuokrypis perskaičiuojami pagal rodinį **Savikainos sekimas**.

## <a name="project-status-summary"></a>Projekto būsenos suvestinė

Stebėjimo duomenys rodiniuose **Pastangų sekimas** ir **Savikainos sekimas** nurodo projekto šakninio mazgo, suvestinių užduočių ir lapų mazgo užduočių lygių eigą ir sąnaudas. Skyriuje **Būsena**, esančiame puslapyje **Projekto objektas**, rodoma projekto lygio būsenos suvestinė.

## <a name="status-summary-fields"></a>Būsenos suvestinės laukai

Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną. Lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, kad nurodytų didėjančią riziką. Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną. Lauko **Būsena atnaujinta** negalima redaguoti, o reikšmė turi laiko žyma, kuri nurodo kada paskutinį kartą buvo atnaujinta būsena.

Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo datą. Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite nustatyti šiuos laukus į **Prieš laiką**. Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti juos į **Vėluoja**.
