---
title: Projekto rezervavimo kūrimas i iš Grafiko lentos
description: Šioje temoje pateikiama informacija apie tai, kaip kurti projekto rezervavimą iš grafiko lentos.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
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
ms.openlocfilehash: ccbfedec82b2d9035b51cf1b283ae5c441f1cbcc
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4122308"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>Projekto rezervavimo kūrimas i iš Grafiko lentos

Išteklius projektui galite rezervuoti projekto skirtuke **„Komanda“** iš karto arba iš bendrojo komandos nario priskyrimo sugeneruodami išteklių reikalavimą ir tada jį įvykdydami su projekto komandos nariu.

Taip pat išteklius projektui galite rezervuoti tiesiai iš Grafiko lentos. Yra trys būdai tai padaryti:

- **„Rezervavimas iš sugeneruoto ištekliaus reikalavimo“:** sukūrę bendrąjį išteklių ir priskyrę užduotis projekte galite sugeneruoti išteklių reikalavimą.

- **„Rezervavimas iš pagrindinio reikalavimo“:** pagrindiniai reikalavimai rodomi Grafiko lentoje, skirtuke **„Projektas“**. 

- **„Rezervavimas iš naujo ištekliaus reikalavimo“:** galite iš naujo sukurti išteklių reikalavimą ir susieti jį su projektu. Grafiko lentoje išteklių reikalavimai rodomi skirtuke **„Atidaryti reikalavimus“**.

## <a name="book-from-a-generated-resource-requirement"></a>Rezervavimas iš sugeneruoto išteklių reikalavimo

Galite sukurti bendrąjį išteklių ir projekte jam priskirti vieną ar kelias užduotis. Tada galite generuoti išteklių reikalavimą iš bendrojo komandos nario. 

1.  Grafiko lentoje šie ištekliai bus matomi skirtuke **„Atidaryti reikalavimus“**. Jei turite daug atidarytų reikalavimų, jums gali tekti panaudoti stulpelio filtrus, esančius tinklelyje. 

    ![Reikalavimų skirtuko atidarymas grafiko lentoje](media/FAQ-Project-Booking-Schedule-Board-1.png "Rezervavimo ir užduočių lentelės ekrano nuotrauka")

2. Pasirinkite reikalavimą. Skirtukas **„Rasti pasiekiamumą“** matomas pasirinktos eilutės viršuje.
 
3. Pasirinkus skirtuką paleidžiamas Grafiko lentos pagalbinės planavimo priemonės režimas ir atrenkami galimi ištekliai, atitinkantys ištekliaus reikalavimą. Tada jau galite rezervuoti išteklius.

4. Taip pat galite nuvilkti pasirinktą eilutę iš Grafiko lentos apačios į išteklių langelį, esantį tinklelio viršuje. Jį paleidus dešinėje atidaromas skydas **„Kurti išteklių rezervavimą“**.

    Pasirinkus **„Rezervuoti“** rezervuojami ištekliai projekto komandai.

![Kurti išteklių rezervavimo sritį](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>Rezervavimas iš pirminio reikalavimo

Sukūrus projektą „Project Service“ programoje, automatiškai sukuriamas išteklių reikalavimas, vadinamas pirminiu reikalavimu. Šis reikalavimas yra tuščias ir naudojamas norint greitai rezervuoti išteklius Grafiko lentoje, išvengiant reikalavimo generavimo arba jo kūrimo iš naujo. Kadangi reikalavimas yra tuščias, turėsite nurodyti datas, paskirstymo metodą ir valandas, jei tai yra taikoma. 

1. Norėdami rezervuoti išteklius iš pagrindinio reikalavimo Grafiko lentoje, pasirinkite skirtuką **„Projektas“**. Jei turite daug projektų, gali tekti stulpelyje **„Projektas“** panaudoti stulpelio filtrą.

   ![Stulpelio filtrai grafiko lentoje](media/FAQ-Project-Booking-Schedule-Board-2.png "Rezervavimo ir užduočių lentelės ekrano nuotrauka")

2. Pasirinkite reikalavimą, kurio pavadinimo laukelyje įrašytas projekto pavadinimas, o trukmė – 0.

3. Pasirinkite skirtuką **„Rasti pasiekiamumą“**, atsirandantį eilutėje. Atlikus šį veiksmą Grafiko lentoje įjungiamas pagalbinės planavimo priemonės režimas ir parodomi galimi ištekliai, kuriuos galima rezervuoti projektui.

4. Kadangi **„Pagrindinis reikalavimas“** yra tuščias reikalavimas, o jo trukmė – 0, rinkdamiesi ir rezervuodami išteklius srityje **„Kurti išteklių rezervavimą”** turėsite nustatyti trukmę.

5. Taip pat Grafiko lentos apačioje galite pasirinkti **„Pagrindinis projekto reikalavimas“** bei jį nuvilkti ant išteklių, kad juos rezervuotumėte.
 
    Kadangi **„Pagrindinis reikalavimas“** yra tuščias reikalavimas, o jo trukmė – 0, rinkdamiesi ir rezervuodami išteklius srityje **„Kurti išteklių rezervavimą”** turėsite nustatyti trukmę.
 
    Rezervuodami išteklius Grafiko lentoje per **„Pagrindinis reikalavimas“**, išteklius prie projekto komandos pridedate be jokių užduočių.
 
## <a name="book-from-a-new-resource-requirement"></a>Rezervavimas iš naujo išteklių reikalavimo
Atlikite šiuos veiksmus norėdami rezervuoti iš naujo išteklių reikalavimo. 

1. Norėdami sukurti naują išteklių reikalavimą, eikite į **„Išteklių reikalavimai”** ir pasirinkite **„Naujas”**.

2. Skirtuke **„Projektas“** pažymėkite projektą, kurį reikia susieti su reikalavimu.
 
    Šis naujai sukurtas reikalavimas Grafiko lentoje rodomas kaip **„Atidaryti reikalavimą“**, kurį galite įvykdyti.

3. Rezervuokite išteklius, kad jie būtų įtraukti į projekto komandą.

4. Kai ištekliai jau rezervuoti, reikia rankiniu būdu priskirti užduotis.

