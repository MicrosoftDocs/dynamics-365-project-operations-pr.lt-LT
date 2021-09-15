---
title: Subrangos sutarties laiko eilutės
description: Šioje temoje paaiškinama, kaip įrašyti subrangos sutarties laiko eilutes ir laiko pirkimą iš tiekėjų.
author: rumant
ms.date: 08/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 10ebe0fcc86b4652ac01e28108361df1f768b61d
ms.sourcegitcommit: 80aa1e8070f0cb4992ac408fc05bdffe47cee931
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/13/2021
ms.locfileid: "7323876"
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

| **Laukas** | **Aprašas** |
| --- | --- |
| Pavadinimas / vardas ir pavardė | Subrangos sutarties eilutės pavadinimas. |
| Aprašymas | Glaustas paslaugų, įsigyjamų pagal subrangos sutarties eilutę, aprašas. | 
| Eilutės tipas | Šis laukas yra numatytoji reikšmė.  |
| Atsiskaitymo metodas | Pasirinkite atsiskaitymo metodą. Atsižvelgiant į nurodytos subrangos sutarties eilutės atsiskaitymo metodą, fiksuotos kainos atsiskaitymo metodui galima pasirinkti etapu pagrįstos sąskaitos faktūros grafiką. |
| Operacijos klasė | Šis laukas yra numatytoji reikšmė, nurodanti, ar subrangos sutarties eilutė naudojama subrangovo laikui įsigyti. |
| Vaidmuo | Subrangos sutarties išteklių, kurių laikas įsigyjamas, vaidmuo. Subrangos sutarties ištekliams priskirtas vaidmuo lemia įsigijimo kainą. |
| Pageidaujama pradžia | Data, kai subrangovo ištekliai turi pradėti dirbti. Pageidaujama pradžia naudojama norint pasirinkti projekto kainoraštį iš prie subrangos sutarties pridėtų projekto kainoraščių. Tada vaidmens savikaina subrangos sutarties eilutėje nustatoma pagal numatytuosius atitinkamo kainoraščio parametrus. |
| Prašoma pabaiga | Data, kai baigiasi subrangos sutarties išteklių priskyrimas. Ši data naudojama įspėjimams rodyti, kai projektų vadovas šį pajėgumą naudoja išteklių reikalavimams po šios datos vykdyti. |
| Užsakytas kiekis | Iš tiekėjo įsigyjamų vaidmens valandų skaičius. Ši reikšmė naudojama įspėjimams rodyti, kai projektų vadovas naudoja per daug šio pajėgumo išteklių reikalavimams vykdyti. |
| Vienetų grupė | Numatyta, kad ši lauko reikšmė nustatoma kaip laiko vienetų grupė, kurios keisti negalima.  |
| Vienetas | Numatyta, kad šis laukas nustatomas kaip pradinis valandų vienetas iš laiko vienetų grupės. Šią reikšmę galite pakeisti, jei norite įsigyti bet kurį laiko vienetų grupės vienetą, pvz., dieną arba savaitę. Vaidmens ir vieneto derinys naudojamas vieneto kainai subrangos sutarties eilutėje apskaičiuoti. |
| Vieneto kaina | Vieneto kainos reikšmė pagal numatytuosius parametrus nustatoma atsižvelgiant į projekto kainoraščio, taikomo pageidaujamai pradžios datai subrangos sutarties eilutėje, vaidmens ir vieneto derinį. Kai taikomame projekto kainoraštyje kaina nustatyta skirtingu vienetu nei subrangos sutarties vienetas, sistema vieneto kainai apskaičiuoti naudoja vienetų konvertavimo funkciją. |
| Tarpinė suma | Šis laukas skirtas tik skaityti ir jis automatiškai apskaičiuojamas kaip **Kiekis x vieneto kaina**, jei įvestos kiekio ir vieneto kainos reikšmės. Jei kiekis, vieneto kaina arba jie abu yra tušti, reikšmę galite įvesti lauke. |
| PVM |  Įveskite PVM sumą. |
| Bendra suma | Bendroji subrangos sutarties eilutės suma įtraukus mokesčius. |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
