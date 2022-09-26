---
title: Išlaidų kategorijų subrangos sutarties eilutės
description: Šiame straipsnyje paaiškinama, kaip įrašyti išlaidų subrangos eilutes ir naudoti laukus laiko pirkimui iš tiekėjų įrašyti.
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ba1241ce40b7c5b488e278e8f1b8e9f352f45dc8
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522618"
---
#  <a name="subcontract-lines-for-expense-categories"></a>Išlaidų kategorijų subrangos sutarties eilutės

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

„Dynamics 365 Project Operations“ subrangos sutartyje gali būti išlaidų kategorijoms skirta eilutė. Išlaidų kategorijų subrangos sutarties eilutės suteikia projekto vadovui galimybę iš tiekėjų įsigyti paslaugų arba produktų kategorijas, kurios už naudojimą projekte gali būti apmokestintos.

Norėdami „Project Operations“ sukurti išlaidų kategorijų subrangos sutarties eilutę, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje pasirinkite **Subrangos sutartys** ir atidarykite subrangos sutartį, su kuria norite dirbti.
2. Skirtuke **Subrangos sutarties eilutės** pasirinkite **Nauja** ir sukurkite naują eilutę.
3. Puslapio **Spartusis kūrimas** lauke **Operacijos klasė** pasirinkite **Išlaidos** ir įveskite arba pasirinkite bet kurio kito reikiamo lauko informaciją.

Toliau esančioje lentelėje pateikiama informacija apie laukus, esančius išsamios informacijos puslapyje **Subrangos sutarties eilutė** ir puslapyje **Spartusis kūrimas**.

| **Laukas** | **Aprašas** | **Funkcinis poveikis** |
| --- | --- | --- |
| Pavadinimas / vardas ir pavardė | Subrangos sutarties eilutės pavadinimas, kuris padeda identifikuoti. | Jis bus rodomas kaip pirmasis visų peržvalgų stulpelis, remiantis subrangos sutarties eilutėmis. |
| Aprašymas | Trumpas išlaidų kategorijų, susijusių su subrangos sutarties eilutės pirkimu, apibūdinimas. | Nėra |
|Eilutės tipas | Šio lauko numatytoji vertė yra **Pagrįsta kiekiu**. |Nėra |
| Atsiskaitymo metodas | Tai yra parinkčių rinkinys, atitinkantis du pagrindinius sutarčių modelius, kuriuos palaiko „Project Operations“: **Fiksuota kaina** ir **Laikas ir medžiaga**. | Jei pasirinktas fiksuotos kainos sąskaitų išrašymo metodas, subrangos sutarčių eilutėms galima naudoti etapais pagrįstą sąskaitų faktūrų grafiką. |
| Operacijos klasė | Šio lauko numatytoji vertė yra **Laikas**. Norėdami sukurti produktų pirkimo subrangos sutarties eilučių, lauką **Operacijos klasė** nustatykite į **Išlaidos**.  | Tai reiškia, kad projektų išlaidų kategorijos pirkiniui įrašyti naudojama subrangos sutarties eilutė. |
| Operacijos kategorija | Rodomas sistemoje aktyvių operacijų kategorijų sąrašas. |Nėra |
| Pageidaujama pradžia | Įveskite datą, kada turi būti pasiekiamos tiekėjo pirkimo kategorijos. | Pageidaujama pradžia naudojama norint pasirinkti projekto kainoraštį iš projekto kainoraščių, pridėtų prie subrangos sutarties. Kategorijos savikaina, pateikta subrangos sutarties eilutėje, gaunama iš to kainoraščio. |
| Prašoma pabaiga | Įveskite datą, nuo kurios nebereikės pirkimo kategorijų. | Tai bus naudojama įspėjimams rodyti, kai projekto vadovas šią subrangos sutarties eilutę susies su konkrečiais projekto išlaidų įvertinimais, reikalingais po šios datos. |
| Užsakytas kiekis | Iš tiekėjo įsigytos kategorijos kiekis. | Tai bus naudojama įspėjimams rodyti, kai projekto vadovas šį kiekį viršys.|
| Vienetų grupė | Numatytoji reikšmė yra pagrįsta numatytąja vienetų grupe, nustatyta pažymėtai kategorijai. |Nėra |
| Vienetas | Numatytoji reikšmė yra pagrįsta numatytuoju vienetu, nustatytu pažymėtai kategorijai.  | **Kategorijos** ir **Vieneto** derinys bus naudojamas kaip numatytasis arba apskaičiuotas subrangos sutarties eilutės vieneto kainai.  |
| Vieneto kaina | Numatytoji reikšmė naudoja **Kategoriją** ir **Vienetą** iš kategorijų kainų, susijusių su projekto kainoraščiu, kuris taikomas prašomai subrangos sutarties eilutės pradžiai. |Nėra |
| Tarpinė suma | Tai yra tik skaitomas laukas, apskaičiuojamas kaip X kiekio vieneto kaina, jei įvedamos kiekio ir vieneto kainų reikšmės. Jei kuris nors arba abu laukai yra tušti, šiame lauke galite įvesti reikšmę. |Nėra |
| PVM | Įveskite PVM sumą. |Nėra |
| Bendra suma | Bendra subrangos sutarties eilutės suma įskaitant mokesčius. Šis laukas apskaičiuojamas kaip tarpinė suma + PVM. |Nėra |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
