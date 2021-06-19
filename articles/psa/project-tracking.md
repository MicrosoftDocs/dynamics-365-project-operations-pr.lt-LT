---
title: Projekto eiga ir savikainos naudojimas
description: Šioje temoje pateikta informacija apie projekto eigos ir sąnaudų sekimą.
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 4fe6adf1a16c1eafc5e37dbd8878dda44cbca230
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6009041"
---
# <a name="project-progress-and-cost-consumption"></a>Projekto eiga ir savikainos naudojimas

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

Poreikis sekti eigą atsižvelgiant į grafiką, priklauso nuo pramonės šakos. Kai kurie pramonės šakų atstovai seka projektą stambiu planu, o kitų pramonės šakų atstovai seka eigą bendru planu. Šioje temoje nurodyta, kaip planuoti norint atitikti jūsų organizacijos reikalavimus.

## <a name="effort-tracking-view"></a>Pastangų sekimo rodinys

Rodinyje **Pastangų sekimas** sekama užduočių eiga grafike. Jame faktinės pastangų valandos, sugaištos atliekant užduotį, lyginamos su suplanuotomis užduoties pastangų valandomis. Siekiant apskaičiuoti sekimo metrikas, „Project Service Automation“ naudoja šias formules:

Iš pradžių užduoties kūrime: suplanuota kaina bus nustatyta į numatomą savikainą. Kai faktiniai duomenys įrašomi į užduotį, sekantis veiksmas bus stebėjimo rodinio apskaičiavimas pastangai

- Progreso procentas = faktinė pastanga iki šios datos ÷ įvertinimas pabaigoje (EAC) 
- Įvertinimas pabaigoje (ETC) = įvertinimas pabaigoje (EAC) – faktinė pastanga iki šios datos 
- EAC = likusi pastanga + faktinė pastanga iki šios datos 
- Numatomos pastangos nuokrypis = planuojamos pastangos – EAC

„Project Service Automation“ rodo pastangos nuokrypio užduotyje projekciją. Jei EAC yra daugiau nei planuojamų pastangų, užduotis prognozuojama užtrukti ilgiau nei buvo planuota iš pradžių. Todėl pagal grafiką ją vėluojama atlikti. Jei EAC yra mažiau nei planuojamų pastangų, užduotis prognozuojama užtrukti trumpiau nei buvo planuota iš pradžių. Todėl ji įgyvendinama greičiau nei nurodyta grafike.

## <a name="reprojecting-effort"></a>Pastangų pakartotinė prognozė

Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas. Projekto pakartotinės prognozės yra projekto vadovo numatyta sąmata, apskaičiuota pagal dabartinę projekto būseną. Tačiau nerekomenduojame projekto vadovams keisti pradinių skaičių, nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.

Projektų vadovas gali iš naujo sukurti užduoties pastangų prognozę dviem būdais:

- Perrašyti numatytuosius ETC nustatymus su nauju užduoties likusių pastangų įvertinimu. 
- Perrašyti numatytuosius eigos procentais nustatymus su nauju užduoties patikslintos eigos įvertinimu.

Dėl kiekvieno iš šių metodų perskaičiuojamos užduoties ETC, EAC bei eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Pakartotinė pastangų suvestinėms užduotims prognozė

Pastangas suvestinėms užduotims ar talpyklės užduotims galima dar kartą prognozuoti. Neatsižvelgiant į tai, ar vartotojas pakartotinai kurs suvestinių užduočių prognozę pagal likusiais pastangas ar eigą procentais, pradedami vykdyti šie skaičiavimo procesai:

- Užduoties EAC, ETC bei eiga procentais apskaičiuojami.
- Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis užduoties EAC.
- Apskaičiuojamas kiekvienos individualios užduoties iki lapo mazgo užduočių naujas EAC. 
- Paveiktų antrinių užduočių iki lapų mazgų ETC ir eiga procentais perskaičiuojami pagal EAC reikšmę. Taip sukuriama nauja pastangų užduočiai nuokrypio prognozė. 
- Suvestinių užduočių iki šaknies mazgo EAC perskaičiuojamas.

### <a name="cost-tracking-view"></a>Savikainos sekimo rodinys 

**Kainos sekimo** rodinys lygina faktinę kainą, kuri buvo išleista užduočiai, su suplanuota kaina. 

> [!NOTE]
> Šiame rodinyje rodomos tik darbo savikainos ir nėra įtraukiamos savikainos iš išlaidų įvertinimų. 

Siekiant apskaičiuoti sekimo metrikas, „Project Service Automation“ naudoja šias formules:

Kai užduotis sukuriama, suplanuota kaina yra lygi numatytai užbaigimo kainai. Kai faktiniai duomenys įrašomi į užduotį, toliau apskaičiuojamas **Sekimo** rodinys kainai:

 - Sąnaudų procentinė dalis = iki šios datos išleista faktinė kaina ÷ numatyta užduoties užbaigimo kaina
 - Kaina užbaigti (CTC) = numatyta užbaigimo kaina – iki šios datos išleista faktinė kaina
 - Numatyta užbaigimo kaina = CTC + iki šios datos išleista faktinė kaina
 - Numatytas kainų nuokrypis = suplanuota kaina – numatyta užbaigimo kaina

Rodoma savikainos nuokrypio užduočiai prognozė. Jei numatyta užbaigimo kaina yra didesnė nei suplanuota kaina, numatoma, kad užduotis kainuos daugiau nei buvo planuota iš pradžių. Todėl biudžetas viršijamas. Jei numatyta užbaigimo kaina yra mažesnė nei suplanuota kaina, numatoma, kad užduotis kainuos mažiau nei buvo planuota iš pradžių ir nesieks biudžeto. 

## <a name="project-managers-reprojection-of-cost"></a>Projekto vadovo nauja išlaidų prognozė

Kai pastanga yra numatoma iš naujo, CTC, numatoma užbaigimo kaina, sąnaudų procentinė dalis ir numatomas kainos nuokrypis yra perskaičiuojami pagal **Kainos sekimo** rodinį.

## <a name="project-status-summary"></a>Projekto būsenos suvestinė

Stebėjimo duomenys rodiniuose **Pastangų sekimas** ir **Savikainos sekimas** nurodo projekto šakninio mazgo, suvestinių užduočių ir lapų mazgo užduočių lygių eigą ir sąnaudas. Skyriuje **Būsena**, esančiame puslapyje **Projekto objektas**, rodoma projekto lygio būsenos suvestinė.

## <a name="status-summary-fields"></a>Būsenos suvestinės laukai

Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną. Lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, kad nurodytų didėjančią riziką. Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną. Lauko **Būsena atnaujinta** negalima redaguoti, o reikšmė turi laiko žyma, kuri nurodo kada paskutinį kartą buvo atnaujinta būsena.

Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo datą. Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite nustatyti šiuos laukus į **Prieš laiką**. Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti juos į **Vėluoja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]