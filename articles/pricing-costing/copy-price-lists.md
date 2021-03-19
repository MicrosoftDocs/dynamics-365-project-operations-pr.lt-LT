---
title: Kainoraščių kopijavimas
description: Šioje temoje pateikta informacija apie kainoraščių kopijavimą programoje „Project operations“.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: e49a95a04e9506e983d920c49d4c504d9f944c88
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5275728"
---
# <a name="copy-price-lists"></a>Kainoraščių kopijavimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Programoje „Dynamics 365 Project Operations“ galite kurti kainoraščių kopijas. Pavyzdžiui, galite kurti būsimų metų kainoraščius naudodami kainoraštį iš esamų metų.  Arba galite kopijuoti sąskaitų tarifų ir pardavimo kainų kainoraštį iš išlaidų kainoraščių. 

Norėdami nukopijuoti kainoraštį, atlikite toliau nurodytus veiksmus.

1. Atidarykite kainoraštį, kurį norite kopijuoti, ir pasirinkite **Kopijuoti**.
2. Įveskite visą būtiną informaciją, kad nukopijuotumėte kainoraštį. Toliau pateiktoje lentelėje nurodomi svarstymai, į kuriuos reikia atsižvelgti įvedant informaciją.

| Laukas | Aprašo | Tolesnis poveikis |
| --- | --- | --- |
| Pavadinimas / vardas, pavardė | Šaltinio kainoraščio pavadinimas kartu su prierašu **kopija**. | Kainoraštis apima šią reikšmę visuose sąrašo puslapiuose ir išplečiamosiose parinktyse. |
| Kontekstas | Įveskite norimą paskirties kainoraščio kontekstą. | Kainoraštis, kurio kontekstas nustatytas į **Savikaina**, naudojamas norint ieškoti numatomos savikainos ir faktinės savikainos. Kainoraštis, kurio kontekstas nustatytas į **Pardavimas**, naudojamas norint ieškoti numatomos pardavimo kainos ir faktinės pardavimo kainos. Prie kliento, pasiūlymų arba sutarties projekto kainoraščių galima pridėti tik kainoraščius, kurių kontekstas nustatytas į **Pardavimas**. |
| Pradžios data | Kainoraščio galiojimo laikotarpio pradžios data. | Kartu su lauku **Pabaigos data**, šis laukas naudojamas norint nustatyti, kuris kainoraštis taikomas tam tikrai numatomai arba faktinei eilutei. |
| Pabaigos data | Kainoraščio galiojimo laikotarpio pabaigos data. | Kartu su lauku **Pradžios data**, šis laukas naudojamas norint nustatyti, kuris kainoraštis taikomas tam tikrai numatomai arba faktinei eilutei. |
| Valiuta | Šaltinio kainoraščio valiuta. To keisti negalima. | Kai tai pakeičiama, visos gautos kainų eilutės už darbą, išlaidas ir produktų katalogų prekes konvertuojamos į paskirties kainoraščio valiutą kopijuojant. |
| Laiko vienetas | Šaltinio kainoraščio valiuta. To keisti negalima. | Kai tai pakeičiama, visos gautos kainų eilutės už darbo prekes konvertuojamos į paskirties kainoraščio vienetą kopijuojant. Naudojamas šaltinio kainoraščio laiko vieneto ir paskirties kainoraščio laiko vieneto konvertavimas iš vienetų sąrankos. |
| Aprašo | Šaltinio kainoraščio aprašas kartu su prierašu **kopija**. Šiame teksto lauke galite nurodyti keleto eilučių kainoraščio aprašą. | Šis laukas rodomas įvairių objektų, kurie turi susietų kainoraščių, kainoraščių **susietuose** rodiniuose. |

3. Įrašykite kainoraštį. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Kainoraščio naujinimas taikant antkainį visoms prekėms

1. Kainoraščio skirtukuose **Vaidmuo**, **Kategorija** ir **Kainų sąrašo elementas** galite pasirinkti **Naujinti kainas**, kad visoms papildomo tinklelio kainoms pritaikytumėte antkainį. 
2. Atidarytame dialogo lango puslapyje įveskite antkainį. Taip pat galite įvesti neigiamą antkainį procentais, kad sumažintumėte kainas tam tikra procentine dalimi. 
3. Dialogo lango puslapyje pasirinkite **Gerai** ir patikrinkite, ar papildomo tinklelio kainos atitinka atliktus pakeitimus.


[!INCLUDE[footer-include](../includes/footer-banner.md)]