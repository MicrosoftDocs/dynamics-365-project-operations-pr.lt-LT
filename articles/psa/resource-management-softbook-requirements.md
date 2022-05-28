---
title: Preliminaraus rezervavimo reikalavimai
description: Šioje temoje pateikiama informacija apie preliminaraus rezervavimo reikalavimus.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: ba5e2e01c1280f5c5a1af284f1ca9c49c8b1fe27
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598866"
---
# <a name="soft-book-requirements"></a>Preliminaraus rezervavimo reikalavimai

[!include [banner](../includes/psa-now-project-operations.md)]

Išteklių reikalavimas gali būti galutinė rezervacija. Galutinė rezervacija sukuria pasiūlymą, kuris naudoja išteklių pajėgumą. Tada pasiūlymas siunčiamas prašytojo patvirtinimui. Preliminari rezervacija preliminariai įtraukia išteklius į projekto komandą ir turi skirtingas būsenas grafiko lentoje, tačiau nenaudoja išteklių pajėgumo. Norėdami atlikti preliminarią rezervaciją iš grafiko lentos, nustatykite lauką **Rezervacijos būsena** į **Preliminari**.

![Rezervacijos būsena nustatyta į „Preliminari“.](media/Resource-Management-image77.png)

Kai skirtukas **Komanda** yra rodinyje **Įvardinti komandos nariai**, ten pradedami rodyti ištekliai. Preliminariai rezervuotos valandos rodomos stulpelyje **Preliminariai rezervuotos valandos**.

![Preliminariai rezervuotos valandos rodinyje „Įvardinti komandos nariai“.](media/Resource-Management-image78.png)

Preliminariai rezervuotiems komandos nariams gali būti priskiriamos užduotys.

![Preliminariai rezervuotam komandos nariui priskirta užduotis.](media/Resource-Management-image79.png)

Skirtuke **Derinimas** nerodomos preliminariai rezervuotų išteklių rezervacijos, nes skirtuke **Derinimas** rodomos tik galutinės rezervacijos.

![Preliminariai rezervuoti ištekliai be rezervacijos skirtuke „Derinimas“.](media/Resource-Management-image80.png)

> [!NOTE]
> Negalite preliminariai rezervuoti išteklių iš reikalavimo, kuris buvo sugeneruotas iš bendrosios komandos nario.

Grafiko lentoje preliminarioms išteklių rezervacijoms naudojamos skirtingos spalvos.

![Preliminarios rezervacijos grafiko lentoje.](media/Resource-Management-image81.png)

Jei norite konvertuoti preliminarų rezervavimą į galutinį užsakymą, grafiko lentoje dešiniuoju pelės mygtuku spustelėkite **Keisti būseną** \> **Galutiniai užsakymai** \> **Galutiniai**.

![Rezervavimo būsena pakeista į „Galutinė“.](media/Resource-Management-image82.png)

Rezervacija pakeista, būsena taip pat pakeista grafiko lentoje. Kadangi rezervacijos būsena dabar yra **Galutinė**, ištekliai rodomi kaip rezervuoti, o jų pajėgumas ir pasiekiamumas pakeisti.

Tą patį metodą galite naudoti, kad atšauktumėte galutinę rezervaciją arba preliminarią rezervaciją grafiko lentoje.

Norėdami preliminariai rezervuotus išteklius pakeisti į galutinai rezervuotus projekto skirtuke **Komanda**, pažymėkite išteklius, tada pažymėkite **Patvirtinti**.

![Komanda „Patvirtinti“.](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
