---
title: Subrangos sutarties eilutės, skirtos produktams
description: Šioje temoje aiškinama, kaip įrašyti produktų subrangos sutarties eilutes, ir naudotis įvairiais laukais norint įrašyti produktų pirkimus iš tiekėjų.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c0ddc39638ae9830eacc57f3e1def75aa36e6553
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323696"
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

| Laukas | Aprašymas |
| ----- | ----------- |
| Pavadinimas / vardas ir pavardė | Subrangos sutarties eilutės pavadinimas. |
| Aprašymas | Trumpas paslaugų arba produktų, užsakomų pagal subrangos sutarties eilutę, aprašas. |
| Eilutės tipas | Šio lauko vertė pagal numatytuosius parametrus yra **Pagrįsta kiekiu**. |
| Atsiskaitymo metodas |  Subrangos sutarties eilutės atsiskaitymo metodas. Pasirinkus fiksuotos kainos atsiskaitymo metodus, galima naudotis etapais pagrįstą sąskaitos faktūros grafiką. |
| Operacijos klasė | Šio lauko vertė pagal numatytuosius parametrus yra **Laikas**. Norėdami sukurti produktų pirkimo subrangos sutarties eilučių, lauke **Operacijos klasė** pasirinkite **Medžiaga**. Šiuo pasirinkimu nurodoma, kad subrangos sutarties eilutė naudojama projekte naudotinų produktų pirkimo faktui įrašyti. |
| Pasirinkti produktą | Pasirinkite, ar perkamas produktas priklauso produktų katalogui, ar yra įtraukiamasis. |
| Produktas | Pasirinkite aktyvųjį produktą iš katalogo. Šį lauką galima naudoti tik tada, kai **Pasirinkti produktą** nustatyta kaip **Esamas**. |
| Įrašomas produktas | Įveskite įtraukiamojo produkto pavadinimą. Šį lauką galima naudoti tik tada, kai **Pasirinkti produktą** nustatyta kaip **Įtraukiamasis**.  |
| Pageidaujama pristatymo data | Pasirinkite reikiamą produktų pristatymo datą. Data taip pat naudojama norint pasirinkti projekto kainoraštį iš prie subrangos sutarties pridėtų projekto kainoraščių. Tada produkto savikaina subrangos sutarties eilutėje nustatoma pagal numatytuosius atitinkamo kainoraščio parametrus. |
| Sutarties pristatymo data | Pasirinkite datą, kada sutartimi susitariama produktus pristatyti.  |
| Užsakytas kiekis | Įveskite iš tiekėjo perkamo produkto kiekį. Jei projekto vadovas viršys šį kiekį, bus rodomas įspėjimas. |
| Vienetų grupė | Ši reikšmė pagal numatytuosius parametrus taikoma tik katalogo produktams. Kai pasirinkta **Produktas** ir **Pageidaujama pristatymo data**, sistema taikytiną kainoraštį parenka pagal pristatymo datą. Užklausa dėl susijusių kainoraščio elementų pateikiama norint sugretinti produktą. Vieneto ir vienetų grupės vertės pagal numatytuosius parametrus nustatomos remiantis kainoraščio elemento įrašo sąranka. |
| Vienetas | Pagal numatytuosius parametrus nustatoma vertė, esanti atliekant kainoraščio elemento įrašo vienetų sąranką. Jei reikia, galite pakeisti į kitą vienetą. Produkto ir vieneto derinys naudojamas numatytajai vieneto kainai esamtų katalogo produktų subrangos sutarties eilutėje nustatyti. |
| Vieneto kaina | Vieneto kainos vertė pagal numatytuosius parametrus nustatoma atsižvelgiant į kainoraščio elemetų, susijusių su projekto kainoraščiu, taikomu pageidaujamai pristatymo datai subrangos sutarties eilutėje, produkto ir vieneto derinį.  |
| Tarpinė suma | Šis tik skaityti skirtas laukas apskaičiuojamas taip: kiekis x vieneto kaina (jei vertės įvestos į abu laukus). Jei kuris nors iš laukų **Kiekis**, **Vieneto kaina** arba abu yra tušti, vertę galite įvesti rankiniu būdu.  |
| PVM | Įveskite PVM vertę. |
| Bendra suma | Šiame apskaičiuotajame lauke pateikiama bendra subrangos sutarties eilutės suma įtraukus mokesčius. Šio lauko vertė apskaičiuojama taip: tarpinė suma + mokestis. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
