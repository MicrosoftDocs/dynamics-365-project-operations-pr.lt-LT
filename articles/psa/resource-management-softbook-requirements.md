---
title: Preliminaraus rezervavimo reikalavimai
description: Šioje temoje pateikiama informacija apie preliminaraus rezervavimo reikalavimus.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: e753dd2f5635d1e9d0d6a02ea5d1d537879dd3a5
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124108"
---
# <a name="soft-book-requirements"></a>Preliminaraus rezervavimo reikalavimai

Išteklių reikalavimas gali būti galutinė rezervacija. Galutinė rezervacija sukuria pasiūlymą, kuris naudoja išteklių pajėgumą. Tada pasiūlymas siunčiamas prašytojo patvirtinimui. Preliminari rezervacija preliminariai įtraukia išteklius į projekto komandą ir turi skirtingas būsenas grafiko lentoje, tačiau nenaudoja išteklių pajėgumo. Norėdami atlikti preliminarią rezervaciją iš grafiko lentos, nustatykite lauką **Rezervacijos būsena** į **Preliminari**.

![Rezervacijos būsena nustatyta į „Preliminari“](media/Resource-Management-image77.png)

Kai skirtukas **Komanda** yra rodinyje **Įvardinti komandos nariai**, ten pradedami rodyti ištekliai. Preliminariai rezervuotos valandos rodomos stulpelyje **Preliminariai rezervuotos valandos**.

![Preliminariai rezervuotos valandos rodinyje „Įvardinti komandos nariai“](media/Resource-Management-image78.png)

Preliminariai rezervuotiems komandos nariams gali būti priskiriamos užduotys.

![Preliminariai rezervuotam komandos nariui priskirta užduotis](media/Resource-Management-image79.png)

Skirtuke **Derinimas** nerodomos preliminariai rezervuotų išteklių rezervacijos, nes skirtuke **Derinimas** rodomos tik galutinės rezervacijos.

![Preliminariai rezervuoti ištekliai be rezervacijos skirtuke „Derinimas“](media/Resource-Management-image80.png)

> [!NOTE]
> Negalite preliminariai rezervuoti išteklių iš reikalavimo, kuris buvo sugeneruotas iš bendrosios komandos nario.

Grafiko lentoje preliminarioms išteklių rezervacijoms naudojamos skirtingos spalvos.

![Preliminarios rezervacijos grafiko lentoje](media/Resource-Management-image81.png)

Jei norite konvertuoti preliminarų rezervavimą į galutinį užsakymą, grafiko lentoje dešiniuoju pelės mygtuku spustelėkite **Keisti būseną** \> **Galutiniai užsakymai** \> **Galutiniai**.

![Rezervavimo būsena pakeista į „Galutinė“](media/Resource-Management-image82.png)

Rezervacija pakeista, būsena taip pat pakeista grafiko lentoje. Kadangi rezervacijos būsena dabar yra **Galutinė**, ištekliai rodomi kaip rezervuoti, o jų pajėgumas ir pasiekiamumas pakeisti.

Tą patį metodą galite naudoti, kad atšauktumėte galutinę rezervaciją arba preliminarią rezervaciją grafiko lentoje.

Norėdami preliminariai rezervuotus išteklius pakeisti į galutinai rezervuotus projekto skirtuke **Komanda**, pažymėkite išteklius, tada pažymėkite **Patvirtinti**.

![Komanda „Patvirtinti“](media/Resource-Management-image83.png)