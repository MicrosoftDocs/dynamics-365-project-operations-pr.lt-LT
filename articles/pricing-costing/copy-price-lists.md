---
title: Kainoraščių kopijavimas
description: Šioje temoje pateikta informacija apie kainoraščių kopijavimą programoje „Project operations“.
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 91ee798a206ea5200780c8ebafc8f99cd9a3e219
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080875"
---
# <a name="copy-price-lists"></a>Kainoraščių kopijavimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Galite kurti kainoraščių kopijas programoje "Dynamics 365 Project Operations“. Pavyzdžiui, galite kurti būsimų metų kainoraščius naudodami kainoraštį iš esamų metų.  Arba galite kopijuoti sąskaitų tarifų ir pardavimo kainų kainoraštį iš išlaidų kainoraščių. 

Norėdami nukopijuoti kainoraštį, atlikite toliau nurodytus veiksmus.

1. Atidarykite kainoraštį, kurį norite kopijuoti, ir pasirinkite **Kopijuoti**.
2. Įveskite visą būtiną informaciją, kad nukopijuotumėte kainoraštį. Toliau pateiktoje lentelėje nurodomi svarstymai, į kuriuos reikia atsižvelgti įvedant informaciją.

| Laukas | Atitiktis, tikslas ir gairės | Tolesnis poveikis |
| --- | --- | --- |
| Pavadinimas / vardas, pavardė | Šaltinio kainoraščio pavadinimas kartu su prierašu **kopija**. | Kainoraštis apima šią reikšmę visuose sąrašo puslapiuose ir išplečiamosiose parinktyse. |
| Kontekstas | Įveskite norimą paskirties kainoraščio kontekstą. | Kainoraštis, kurio kontekstas nustatytas į **Savikaina** , naudojamas norint ieškoti numatomos savikainos ir faktinės savikainos. Kainoraštis, kurio kontekstas nustatytas į **Pardavimas** , naudojamas norint ieškoti numatomos pardavimo kainos ir faktinės pardavimo kainos. Prie kliento, pasiūlymų arba sutarties projekto kainoraščių galima pridėti tik kainoraščius, kurių kontekstas nustatytas į **Pardavimas**. |
| Pradžios data | Kainoraščio galiojimo laikotarpio pradžios data. | Kartu su lauku **Pabaigos data** , šis laukas naudojamas norint nustatyti, kuris kainoraštis taikomas tam tikrai numatomai arba faktinei eilutei. |
| Pabaigos data | Kainoraščio galiojimo laikotarpio pabaigos data. | Kartu su lauku **Pradžios data** , šis laukas naudojamas norint nustatyti, kuris kainoraštis taikomas tam tikrai numatomai arba faktinei eilutei. |
| Valiuta | Šaltinio kainoraščio valiuta. To keisti negalima. | Kai tai pakeičiama, visos gautos kainų eilutės už darbą, išlaidas ir produktų katalogų prekes konvertuojamos į paskirties kainoraščio valiutą kopijuojant. |
| Laiko vienetas | Šaltinio kainoraščio valiuta. To keisti negalima. | Kai tai pakeičiama, visos gautos kainų eilutės už darbo prekes konvertuojamos į paskirties kainoraščio vienetą kopijuojant. Naudojamas šaltinio kainoraščio laiko vieneto ir paskirties kainoraščio laiko vieneto konvertavimas iš vienetų sąrankos. |
| Aprašo | Šaltinio kainoraščio aprašas kartu su prierašu **kopija**. Šiame teksto lauke galite nurodyti keleto eilučių kainoraščio aprašą. | Šis laukas rodomas įvairių objektų, kurie turi susietų kainoraščių, kainoraščių **susietuose** rodiniuose. |

3. Įrašykite kainoraštį. 

## <a name="update-a-price-list-by-applying-a-mark-up-to-all-the-prices"></a>Kainoraščio naujinimas taikant antkainį visoms prekėms

1. Kainoraščio skirtukuose **Vaidmuo** , **Kategorija** ir **Kainoraščio elemento prekė** , galite pasirinkti **Atnaujinti kainas** , kad taikytumėte antkainį visos antrinio tinklelio kainoms. 
2. Atidarytame dialogo lango puslapyje įveskite antkainį. Taip pat galite įvesti neigiamą antkainį procentais, kad sumažintumėte kainas tam tikra procentine dalimi. 
3. Dialogo lango puslapyje pasirinkite **Gerai** ir patikrinkite, ar papildomo tinklelio kainos atitinka atliktus pakeitimus.
