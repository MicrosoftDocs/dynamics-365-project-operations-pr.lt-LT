---
title: Išlaidų kategorijų subrangos sutarties eilutės
description: Šioje temoje aiškinama, kaip įrašyti išlaidų subrangos sutarties eilutes, ir šiuos laukus panaudoti norint įrašyti pirkimo iš tiekėjų laiką.
author: rumant
ms.date: 08/06/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9e8e7bb66063dab6db1ac8da1753913aee0ef3fc
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323831"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Išlaidų kategorijų subrangos sutarties eilutės

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ subrangos sutartyje gali būti išlaidų kategorijoms skirta eilutė. Išlaidų kategorijų subrangos sutarties eilutės suteikia projekto vadovui galimybę iš tiekėjų įsigyti paslaugų arba produktų kategorijas, kurios už naudojimą projekte gali būti apmokestintos.

Norėdami „Project Operations“ sukurti išlaidų kategorijų subrangos sutarties eilutę, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje pasirinkite **Subrangos sutartys** ir atidarykite subrangos sutartį, su kuria norite dirbti.
2. Skirtuke **Subrangos sutarties eilutės** pasirinkite **Nauja** ir sukurkite naują eilutę.
3. Puslapio **Spartusis kūrimas** lauke **Operacijos klasė** pasirinkite **Išlaidos** ir įveskite arba pasirinkite bet kurio kito reikiamo lauko informaciją.

Toliau esančioje lentelėje pateikiama informacija apie laukus, esančius išsamios informacijos puslapyje **Subrangos sutarties eilutė** ir puslapyje **Spartusis kūrimas**.

| **Laukas** |  **Aprašas** |
| ----------| ---------------- |
| Pavadinimas / vardas ir pavardė | Subrangos sutarties eilutės pavadinimas. |
| Aprašymas | Trumpas paslaugos arba produkto kategorijų, kurios perkamos subrangos sutarties eilutėje, aprašas. |
| Eilutės tipas | Šio lauko numatytoji vertė yra **Pagrįsta kiekiu**.  |
| Atsiskaitymo metodas | Subrangos sutarties eilutės atsiskaitymo metodas. Priklausomai nuo eilutės atsiskaitymo metodo, fiksuotos kainos atsiskaitymo metodui galima pasirinkti etapu pagrįstos sąskaitos faktūros grafiką.  |
| Operacijos klasė | Šio lauko numatytoji vertė yra **Laikas**. Norėdami sukurti produktų pirkimo subrangos sutarties eilučių, lauką **Operacijos klasė** nustatykite kaip **Išlaidos**. Šio lauko verte nurodoma, kad subrangos sutarties eilutė naudojama projekte naudotinų produktų arba paslaugų kategorijos pirkimo faktui įrašyti. |
| Operacijos kategorija | Pasirinkite operacijos kategoriją. |
| Pageidaujama pradžia | Data, kai iš tiekėjo turi būti galima įsigyti pirkimo kategorijas. Pageidaujama pradžia naudojama norint pasirinkti projekto kainoraštį iš prie subrangos sutarties pridėtų projekto kainoraščių. Kategorijos savikaina subrangos sutarties eilutėje nustatoma pagal numatytuosius atitinkamo kainoraščio parametrus. |
| Prašoma pabaiga | Data, kai pirkimo kategorijų nebereikia. Kai projekto vadovas šią subrangos sutarties eilutę susieja su konkrečiais išlaidų įvertinimais, priklausančiais projektams, vėlesniems nei ši data, šią dieną pateikiamas įspėjimas. |
| Užsakytas kiekis | Iš tiekėjo perkamas kategorijos kiekis. Projekto vadovui viršijus sigytą kiekį, bus rodomas įspėjimas.  |
| Vienetų grupė | Ši lauko vertė nustatoma pagal numatytuosius parametrus remiantis numatytąja vienetų grupe, nustatyta pasirinktai kategorijai. |
| Vienetas | Ši lauko vertė nustatoma pagal numatytuosius parametrus remiantis numatytuoju vienetu, nustatytu pasirinktai kategorijai. Kategorijos ir vieneto derinys naudojamas numatytajai vieneto kainai subrangos sutarties eilutėje nustatyti. |
| Vieneto kaina | Vieneto kainos lauko vertė nustatoma pagal numatytuosius parametrus, atsižvelgiant į kategorijos kainų, susijusių su projekto kainoraščiu, taikomu pageidaujamai pradžiai subrangos sutarties eilutėje, kategorijos ir vieneto derinį.  |
| Tarpinė suma | Šis tik skaityti skirtas laukas kaip kiekio vieneto kaina automatiškai apskaičiuojamas tada, jei įvestos kiekio ir vieneto kainos vertės. Jei kuris nors arba abu laukai yra tušti, šiame lauke vertę galite įvesti rankiniu būdu.  |
| PVM | Įveskite PVM sumą.  |
| Bendra suma | Bendra subrangos sutarties eilutės suma įskaitant mokesčius. Šis laukas apskaičiuojamas taip: tarpinė suma + PVM kodas.  |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
