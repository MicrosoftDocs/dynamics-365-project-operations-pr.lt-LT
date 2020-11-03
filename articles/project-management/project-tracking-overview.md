---
title: Projekto sekimo apžvalga
description: Šioje temoje pateikta informacija apie tai, kaip sekti projekto eigą ir sąnaudas.
author: ruhercul
manager: AnnBe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: c998addbbdbbea8fe69c95f65e58a24146f394c8
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080687"
---
# <a name="project-tracking-overview"></a>Projekto sekimo apžvalga

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Poreikis sekti eigą atsižvelgiant į grafiką, priklauso nuo pramonės šakos. Kai kurie pramonės šakų atstovai seka projektą stambiu planu, o kitų pramonės šakų atstovai seka eigą bendru planu. Šioje temoje nurodyta, kaip planuoti norint atitikti jūsų organizacijos reikalavimus.

## <a name="effort-tracking-view"></a>Pastangų sekimo rodinys

**Pastangos stebėjimas** rodinys seka užduočių eigą grafike, palygindamas faktines pastangų valandas, praleistas užduočiai, su užduoties suplanuotomis pastangų valandomis. „Dynamics 365 Project Operations“ naudoja šias formules sekimo metrikoms apskaičiuoti:

- **Progreso procentas** : faktinė pastanga iki šios datos ÷ įvertinimas pabaigoje (EAC) 
- **Įvertinimas užbaigti (ETC)** : planuojamos pastangos – iki šios datos naudotos faktinės pastangos 
- **EAC** : likusi pastanga + faktinė pastanga iki šios datos 
- **Numatomos pastangos nuokrypis** : planuojamos pastangos – EAC

„Projects Operations“ rodoma pastangų nuokrypio projekcija užduočiai. Jei EAC yra didesnis nei planuojamos pastangos, prognozuojama, kad užduotis užtruks ilgiau, nei buvo planuota iš pradžių, ir atsiliekama nuo grafiko. Jei EAC yra mažesnis nei planuojamos pastangos, prognozuojama, kad užduotis užtruks mažiau laiko, nei buvo planuota iš pradžių, ir kad ji įgyvendinama greičiau, nei nurodyta grafike.

## <a name="reprojecting-effort"></a>Pastangų pakartotinė prognozė

Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas. Projekto pakartotinės prognozės yra projekto vadovo numatyta sąmata, apskaičiuota pagal dabartinę projekto būseną. Tačiau nerekomenduojame, kad projektų vadovai pakeistų pradinius skaičius. Taip yra nes projekto pradinis planas yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.

Projektų vadovas gali iš naujo sukurti užduoties pastangų prognozę dviem būdais:

- Perrašyti numatytuosius ETC nustatymus su nauju užduoties likusių pastangų įvertinimu. 
- Perrašyti numatytuosius eigos procentais nustatymus su nauju užduoties patikslintos eigos įvertinimu.

Dėl kiekvieno iš šių metodų perskaičiuojamos užduoties ETC, EAC, eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Pakartotinė pastangų suvestinėms užduotims prognozė

Pastangas suvestinėms užduotims ar talpyklės užduotims galima dar kartą prognozuoti. Neatsižvelgiant į tai, ar vartotojas pakartotinai kurs suvestinių užduočių prognozę pagal likusiais pastangas ar eigą procentais, pradedami vykdyti šie skaičiavimo procesai:

- Užduoties EAC, ETC bei eiga procentais apskaičiuojami.
- Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis užduoties EAC.
- Apskaičiuojamas kiekvienos individualios užduoties iki lapo mazgo užduočių naujas EAC. 
- Paveiktų antrinių užduočių iki lapų mazgų ETC ir eiga procentais perskaičiuojami pagal EAC reikšmę. Taip sukuriama nauja pastangų užduočiai nuokrypio prognozė. 
- Suvestinių užduočių iki šaknies mazgo EAC perskaičiuojamas.

### <a name="cost-tracking-view"></a>Savikainos sekimo rodinys 

Rodinyje **Savikainos sekimas** lyginama faktinė savikaina užduočiai atlikti su planuojama užduoties savikaina. 

> [!NOTE]
> Šiame rodinyje rodomos tik darbo savikainos ir nėra įtraukiamos savikainos iš išlaidų įvertinimų. „Project Operations“ naudoja šias formules sekimo metrikoms apskaičiuoti:

- **Sąnaudų procentinė dalis** : iki šios datos išleista faktinė kaina ÷ numatyta užbaigimo kaina
- **Savikaina užbaigti (CTC)** : planuojama savikaina – iki šios datos naudota savikaina
- **EAC** : likusi savikaina + iki šios datos naudota faktinė savikaina
- **Prognozuojamas savikainos nuokrypis** : planuojama savikaina – EAC

Rodoma savikainos nuokrypio užduočiai prognozė. Jei EAC yra daugiau nei planuojama savikaina, užduotis prognozuojama kainuosianti daugiau nei buvo planuota iš pradžių. Todėl biudžetas viršijamas. Jei EAC yra mažiau nei planuojama savikaina, užduotis prognozuojama kainuosianti daugiau nei buvo planuota iš pradžių. Todėl biudžetas nėra viršijamas.

## <a name="project-managers-reprojection-of-cost"></a>Projekto vadovo nauja išlaidų prognozė

Kai pastangos yra prognozuojamos iš naujo, CTC, EAC, sąnaudų procentinė dalis ir prognozuojamas savikainos nuokrypis perskaičiuojami pagal rodinį **Savikainos sekimas**.

## <a name="project-status-summary"></a>Projekto būsenos suvestinė

Stebėjimo duomenys rodiniuose **Pastangų sekimas** ir **Savikainos sekimas** nurodo projekto šakninio mazgo, suvestinių užduočių ir lapų mazgo užduočių lygių eigą ir sąnaudas. Skyriuje **Būsena** , esančiame puslapyje **Projekto objektas** , rodoma projekto lygio būsenos suvestinė.

## <a name="status-summary-fields"></a>Būsenos suvestinės laukai

Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną. Lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, kad nurodytų didėjančią riziką. Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną. Lauko **Būsena atnaujinta** negalima redaguoti, o reikšmė turi laiko žyma, kuri nurodo kada paskutinį kartą buvo atnaujinta būsena.

Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo datą. Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite nustatyti šiuos laukus į **Prieš laiką**. Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti juos į **Vėluoja**.
