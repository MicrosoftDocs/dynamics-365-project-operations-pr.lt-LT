---
title: Subrangos sutarties eilutės, skirtos produktams
description: Šioje temoje aiškinama, kaip įrašyti produktų subrangos sutarties eilutes, ir naudotis įvairiais laukais norint įrašyti produktų pirkimus iš tiekėjų.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cda2db2b6beafb943738b35857d091f7ad17390d
ms.sourcegitcommit: d507a75a19c992a9421e4f3605162a2faa84a445
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/27/2021
ms.locfileid: "7558557"
---
# <a name="subcontract-lines-for-products"></a>Subrangos sutarties eilutės, skirtos produktams

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ subrangos sutartyje gali būti produktams skirta subrangos sutarties eilutė. Pasinaudodamas šiomis eilutėmis, projekto vadovas gali iš tiekėjų pirkti produktus ir vėliau panaudoti juos projekto užduotims.

Norėdami „Project Operations“ sukurti produktų subrangos sutarties eilutę, atlikite toliau nurodytus veiksmus.

1. Naršymo puslapyje pasirinkite **Subrangos sutartys**, tada atidarykite subrangos sutartį, su kuria norite dirbti. 
2. Skirtuke **Subrangos sutarties eilutės** pasirinkite **+ Nauja** ir sukurkite naują subrangos sutarties eilutę.
3. Puslapio **Spartusis kūrimas** lauke **Operacijos klasė** pasirinkite **Medžiaga** ir įveskite arba pasirinkite reikiamo lauko informaciją. 
4. Pasirinkite **Įrašyti**.

Toliau esančioje lentelėje pateikiama informacija apie laukus, esančius išsamios informacijos puslapyje **Subrangos sutarties eilutė** ir puslapyje **Spartusis kūrimas**, nes jie aktualūs perkant produktus.

| Laukas | Aprašymas | Funkcinis poveikis|
| ----- | ----------- | ----------- |
| Pavadinimas / vardas ir pavardė | Subrangos sutarties eilutės pavadinimas, kuris padeda identifikuoti. |Jis bus rodomas kaip pirmasis visų peržvalgų stulpelis, remiantis subrangos sutarties eilutėmis.
| Aprašymas | Trumpas paslaugų arba produktų, užsakomų pagal subrangos sutarties eilutę, aprašas. | Nėra |
| Eilutės tipas | Šio lauko numatytoji vertė yra **Pagrįsta kiekiu**. |Nėra |
| Atsiskaitymo metodas | Tai yra parinkčių rinkinys, atitinkantis du pagrindinius sutarčių modelius, kuriuos palaiko „Project Operations“: **Fiksuota kaina** ir **Laikas ir medžiaga**. | Remiantis pasirinktu atsiskaitymo metodu, subrangos sutarčių eilutėms su fiksuotos kainos atsiskaitymo metodu galima naudoti etapais pagrįstą sąskaitų faktūrų grafiką. |
| Operacijos klasė |Šio lauko numatytoji vertė yra **Laikas**. Norėdami sukurti produktų pirkimo subrangos sutarties eilučių, lauką **Operacijos klasė** nustatykite į **Medžiaga**.  | Tai reiškia, kad projektų produktų pirkiniui įrašyti naudojama subrangos sutarties eilutė. |
| Pasirinkti produktą | Pasirinkite, ar perkamas produktas priklauso produktų katalogui, ar yra įtraukiamasis. |Nėra |
| Produktas | Pasirinkite aktyvųjį produktą iš katalogo. Šį lauką galima naudoti tik tada, kai **Pasirinkti produktą** nustatyta kaip **Esamas**. |**Produkto** ir **Vieneto** derinys bus naudojamas kaip numatytasis arba apskaičiuotas subrangos sutarties eilutės vieneto kainai.
| Įrašomas produktas | Įveskite įtraukiamojo produkto pavadinimą. Šį lauką galima naudoti tik tada, kai **Pasirinkti produktą** nustatyta kaip **Įtraukiamasis**.  |Pirkinio kaina nebus automatiškai įrašoma įtraukiamiesiems produktams.|
| Pageidaujama pristatymo data | Įveskite reikiamą produktų pristatymo datą.| Data taip pat naudojama norint pasirinkti projekto kainoraštį iš prie subrangos sutarties pridėtų projekto kainoraščių. Tada produkto savikaina subrangos sutarties eilutėje nustatoma pagal numatytuosius atitinkamo kainoraščio parametrus. |
| Sutarties pristatymo data | Įveskite datą, kurią produktai turi būti pristatyti pagal sutartį.  |Nėra|
| Užsakytas kiekis | Įveskite iš tiekėjo perkamo produkto kiekį.| Tai bus naudojama įspėjimams rodyti, kai projekto vadovas šį kiekį viršys.|
| Vienetų grupė | Ši reikšmė pagal numatytuosius parametrus taikoma tik katalogo produktams. |Kai pasirinkta **Produktas** ir **Pageidaujama pristatymo data**, sistema taikytiną kainoraštį parenka pagal pristatymo datą. Užklausa dėl susijusių kainoraščio elementų pateikiama norint sugretinti produktą. Vieneto ir vienetų grupės vertės pagal numatytuosius parametrus nustatomos remiantis kainoraščio elemento įrašo sąranka. |
| Vienetas | Ši reikšmė pagal numatytuosius nustatymus nustatoma pagal vienetą, nustatytą kainoraščio elemento įraše. Jei reikia, galite pakeisti į kitą vienetą.| Produkto ir vieneto derinys naudojamas numatytajai vieneto kainai esamtų katalogo produktų subrangos sutarties eilutėje nustatyti. |
| Vieneto kaina | Vieneto kainos vertė pagal numatytuosius parametrus nustatoma atsižvelgiant į kainoraščio elemetų, susijusių su projekto kainoraščiu, taikomu pageidaujamai pristatymo datai subrangos sutarties eilutėje, produkto ir vieneto derinį.  |Nėra |
| Tarpinė suma | Šis tik skaityti skirtas laukas apskaičiuojamas taip: kiekis x vieneto kaina (jei vertės įvestos į abu laukus). Jei kuris nors iš laukų **Kiekis**, **Vieneto kaina** arba abu yra tušti, vertę galite įvesti rankiniu būdu.  |Nėra |
| PVM | Įveskite PVM vertę. |Nėra |
| Bendra suma | Šiame apskaičiuotajame lauke pateikiama bendra subrangos sutarties eilutės suma įtraukus mokesčius. Šio lauko vertė apskaičiuojama kaip Tarpinė suma + Mokestis. |Nėra |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
