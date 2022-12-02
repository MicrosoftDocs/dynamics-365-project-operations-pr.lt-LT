---
title: Projekto pastangų sekimas
description: Šiame straipsnyje pateikta informacija apie tai, kaip sekti projekto pastangas ir darbo eigą.
author: ruhercul
ms.date: 02/15/2022
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c41dbc138f6fc92a9586de173ba5dfc89c7e44e3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929270"
---
# <a name="project-effort-tracking"></a>Projekto pastangų sekimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Poreikis sekti eigą atsižvelgiant į grafiką, priklauso nuo pramonės šakos. Kai kurie pramonės šakų atstovai seka projektą stambiu planu, o kitų pramonės šakų atstovai seka eigą bendru planu. Šiame straipsnyje nurodyta, kaip planuoti norint atitikti jūsų organizacijos reikalavimus.

## <a name="effort-tracking-view"></a>Pastangų sekimo rodinys

**Pastangos stebėjimas** rodinys seka užduočių eigą grafike, palygindamas faktines pastangų valandas, praleistas užduočiai, su užduoties suplanuotomis pastangų valandomis. Stebėjimo metrikoms apskaičiuoti „Dynamics 365 Project Operations“ naudoja šias formules:

- **Progreso procentas**: faktinė pastanga iki šios datos ÷ įvertinimas pabaigoje (EAC) 
- **Pastangų likutis**: įvertintos pastangos pabaigoje – iki šios datos naudotos faktinės pastangos 
- **EAC**: likusi pastanga + faktinė pastanga iki šios datos 
- **Numatomos pastangos nuokrypis**: planuojamos pastangos – EAC

„Projects Operations“ rodoma pastangų nuokrypio projekcija užduočiai. Jei EAC yra didesnis nei planuojamos pastangos, prognozuojama, kad užduotis užtruks ilgiau, nei buvo planuota iš pradžių, ir atsiliekama nuo grafiko. Jei EAC yra mažesnis nei planuojamos pastangos, prognozuojama, kad užduotis užtruks mažiau laiko, nei buvo planuota iš pradžių, ir kad ji įgyvendinama greičiau, nei nurodyta grafike.

## <a name="reprojecting-effort-on-leaf-node-tasks"></a>Pakartotinė pastangų prognozė lapo mazgo užduotims

Dažnai projektų vadovui reikia peržiūrėti pradines užduoties sąmatas. Projekto pakartotinės prognozės yra projekto vadovo numatyta sąmata, apskaičiuota pagal dabartinę projekto būseną. Tačiau nerekomenduojame projektų vadovams keisti planuojamų pastangų skaičių. Taip yra dėl to, kad planuojamos projekto pastangos yra publikuotas projekto grafiko ir savikainos įvertinimų, su kuriais sutiko visos projekto suinteresuotosios šalys, šaltinis.

Projekto vadovas užduotims pakartotinę prognozę gali atlikti atnaujinęs dalies **Pastangų likutis** reikšmę, įvesdamas naują užduoties įvertinimą. Dėl šio naujinimo perskaičiuojamas užduoties įvertinimas pabaigoje (EAC), eiga procentais ir prognozuojamas pastangų užduočiai nuokrypis. Taip pat perskaičiuojamos suvestinių užduočių EAC, ETC bei eiga procentais ir sukuriama nauja pastangų nuokrypio prognozė.

## <a name="reprojection-of-effort-on-summary-tasks"></a>Pakartotinė pastangų suvestinėms užduotims prognozė

Pastangas suvestinėms užduotims ar talpyklės užduotims galima dar kartą prognozuoti. Projektų vadovai gali atnaujinti suvestinių užduočių pastangų likutį. Atnaujinus pastangų likutį, programoje suaktyvinamas toliau nurodytas skaičiavimų rinkinys.

- Užduoties EAC ir eiga procentais apskaičiuojami.
- Naujas EAC paskiriamas į antrines užduotis pagal tą pačią proporciją kaip ir pradinis užduoties EAC.
- Apskaičiuojamas kiekvienos individualios užduoties iki lapo mazgo užduočių naujas EAC. 
- Paveiktų antrinių užduočių iki lapų mazgų pastangų likutis ir eiga procentais perskaičiuojami pagal EAC reikšmę. Taip sukuriama nauja pastangų užduočiai nuokrypio prognozė. 
- Suvestinių užduočių iki šaknies mazgo EAC perskaičiuojamas.
- Patvirtintos suvestinės užduoties pastangos yra visų antrinių užduočių patvirtintų pastangų ir patvirtintų suvestinės užduoties pastangų suma.
- Likusios suvestinės užduoties pastangos yra visų antrinių užduočių likusių pastangų ir patvirtintų suvestinės užduoties pastangų skirtumas.

## <a name="project-status-summary"></a>Projekto būsenos suvestinė

Stebėjimo duomenys rodiniuose **Pastangų sekimas** ir **Savikainos sekimas** nurodo projekto šakninio mazgo, suvestinių užduočių ir lapų mazgo užduočių lygių eigą ir sąnaudas. Skyriuje **Būsena**, esančiame puslapyje **Projekto objektas**, rodoma projekto lygio būsenos suvestinė.

## <a name="status-summary-fields"></a>Būsenos suvestinės laukai

Laukas **Bendra projekto būsena** yra redaguojamas laukas, rodantis bendrą projekto būseną. Lauke naudojamas spalvinis kodavimas, pvz., žalia, geltona ir raudona, kad nurodytų didėjančią riziką. Lauke **Komentarai** projekto vadovui galima įvesti tam tikrus komentarus apie būseną. Lauko **Būsena atnaujinta** negalima redaguoti, o reikšmė turi laiko žyma, kuri nurodo kada paskutinį kartą buvo atnaujinta būsena.

Laukai **Grafiko našumas** ir **Savikainos našumas** nustatomi pagal sekimo datą. Kai sekimo rodinyje **Pastangų sekimas** šakninio mazgo grafikas ir savikainos nuokrypis yra teigiami, galite nustatyti šiuos laukus į **Prieš laiką**. Kai šakninio mazgo grafikas ir savikainos nuokrypis yra neigiami, galite nustatyti juos į **Vėluoja**.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
