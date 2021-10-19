---
title: Subrangos sutarties laiko eilutės
description: Šioje temoje paaiškinama, kaip įrašyti subrangos sutarties laiko eilutes ir laiko pirkimą iš tiekėjų.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 29b38ec9124502e4283b71d13434b1e0420bc413
ms.sourcegitcommit: 74a7e1c9c338fb8a4b0ad57c5560a88b6e02d0b2
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/23/2021
ms.locfileid: "7547254"
---
# <a name="subcontract-lines-for-time"></a>Subrangos sutarties laiko eilutės

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ subrangos sutartyje gali būti laikui skirta subrangos sutarties eilutė. Naudodamas subrangos sutarties laiko eilutes, projektų vadovas gali įsigyti tiekėjų išteklių laiko projektų užduotims ir išteklių reikalavimams įvykdyti.

Norėdami programoje „Project Operations“ sukurti subrangos sutarties laiko eilutę, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje pasirinkite **Subrangos sutartys** ir atidarykite kokią nors subrangos sutartį.
2. Skirtuke **Subrangos sutarties eilutės** pasirinkite **Nauja** ir sukurkite naują subrangos sutarties eilutę.
3. Puslapio **Spartusis kūrimas** lauke **Operacijos klasė** pasirinkite **Laikas**.
4. Įveskite likusią lauko informaciją ir pasirinkite **Įrašyti**.

  Toliau esančioje lentelėje pateikiama informacija apie laukus, esančius puslapyje **Subrangos sutarties eilutė** ir puslapyje **Spartusis kūrimas**.

| **Laukas** | **Aprašas** | **Funkcinis poveikis** |
| --- | --- | --- |
| Pavadinimas / vardas ir pavardė | Subrangos sutarties eilutės pavadinimas, kuris padeda identifikuoti. | Jis bus rodomas kaip pirmasis visų peržvalgų stulpelis, remiantis subrangos sutarties eilutėmis. |
| Aprašymas | Glaustas paslaugų, įsigyjamų pagal subrangos sutarties eilutę, aprašas. |Nėra |
| Eilutės tipas |   Šio lauko numatytoji vertė yra **Pagrįsta kiekiu**.| Nėra |
| Atsiskaitymo metodas | Tai yra parinkčių rinkinys, atitinkantis du pagrindinius sutarčių modelius, kuriuos palaiko „Project Operations“: **Fiksuota kaina** ir **Laikas ir medžiaga**. | Remiantis pasirinktu atsiskaitymo metodu, subrangos sutarčių eilutėms su fiksuotos kainos atsiskaitymo metodu galima naudoti etapais pagrįstą sąskaitų faktūrų grafiką. |
| Operacijos klasė | Numatytoji reikšmė yra **Laikas**. | Tai reiškia, kad subrangos sutarties eilutė yra naudojama subrangovo laiko pirkimui įrašyti. |
| Vaidmuo | Pažymėkite subrangos sutarties išteklių, kurių laikas perkamas, vaidmenį. | Vaidmuo, kurį atlieka subrangos sutarties ištekliai, lemia pirkimo savikainą. |
| Pageidaujama pradžia | Įveskite datą, kada turi būti pradėti naudoti subrangovo ištekliai. | Tai naudojama norint pasirinkti projekto kainoraštį iš projekto kainoraščių, pridėtų prie subrangos sutarties. Vaidmens savikaina, pateikta subrangos sutarties eilutėje, gaunama iš to kainoraščio. |
| Prašoma pabaiga | Įveskite datą, kada baigiasi subrangovo ištekliaus priskyrimas. | Tai bus naudojama įspėjimams rodyti, kai projekto vadovas siekia naudoti išteklių pajėgumus po šios datos. |
| Užsakytas kiekis | Įveskite vaidmens, kuris perkamas iš tiekėjo, valandų skaičių. | Tai bus naudojama įspėjimams rodyti, kai projekto vadovas viršija šiuos išteklių poreikių pajėgumus. |
| Vienetų grupė | Numatytoji reikšmė yra **Laiko vienetų grupė**, kurios negalima pakeisti. | Nėra|
| Vienetas | Šio lauko numatytoji reikšmė yra pradinis valandų vienetas iš **Laiko vienetų grupės**. Šią reikšmę galite pakeisti, jei norite įsigyti bet kurį **Laiko vienetų grupės** vienetą, pvz., dieną arba savaitę. | **Vaidmens** ir **Vieneto** derinys bus naudojamas kaip numatytasis arba apskaičiuotas subrangos sutarties eilutės vieneto kainai. |
| Vieneto kaina | Numatytoji vieneto kaina naudoja **Vaidmens** ir **Vieneto** derinį iš projekto kainoraščio, taikomo subrangos sutarties eilutės **Pageidaujamai pradžios** datai. | Kai taikomame projekto kainoraštyje kaina nustatyta skirtingu vienetu nei subrangos sutarties vienetas, sistema vieneto kainai apskaičiuoti naudoja vienetų konvertavimo funkciją. |
| Tarpinė suma |    Tai yra tik skaitomas laukas, apskaičiuojamas kaip x kiekio vieneto kaina, jei įvedamos kiekio ir vieneto kainų reikšmės. Jei kiekis, vieneto kaina arba jie abu yra tušti, reikšmę galite įvesti lauke. | Nėra|
| PVM |   Įveskite PVM sumą. |Nėra |
| Bendra suma | Bendra subrangos sutarties eilutės suma įskaitant mokesčius. Šis laukas apskaičiuojamas kaip tarpinė suma + PVM.|Nėra |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
