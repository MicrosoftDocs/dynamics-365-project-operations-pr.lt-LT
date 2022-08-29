---
title: Tiekėjo sąskaitos faktūros produktų eilutės
description: Šiame straipsnyje paaiškinama, kaip įrašyti produktų tiekėjo SF eilutes ir naudoti skirtingus laukus produktų pirkimams iš tiekėjų įrašyti.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d38a447c576c095a7bbe2f5ed84342a88bf69a9b
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261569"
---
# <a name="vendor-invoice-lines-for-products"></a>Tiekėjo sąskaitos faktūros produktų eilutės

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations gali būti tiekėjo SF eilutės, skirtos produktams (dar vadinamiems medžiagomis). Projektų vadovai gali naudoti tiekėjo SF eilutes produktams, kad įrašytų produktų, įsigytų projektuose, išlaidas.

Produktų tiekėjo SF eilutės gali nurodyti arba nurodyti subrangos eilutę medžiagoms. Jei produktų tiekėjo SF eilutė nurodo subrangos sutartį, projektų vadovai galės susieti ir patikrinti produktus, kuriems išrašoma SF tiekėjo SF eilutė, su įsigytų produktų, kuriuos įrašė ir patvirtino projektų vadovai, naudojimu.

Šioje lentelėje pateikiama informacija apie produktų tiekėjo SF eilučių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas produktų, kuriems tiekėjo SF išrašomos sąskaitos faktūros tiekėjo SF eilutėje, aprašas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią produktai iš pradžių buvo užsakyti. | Tiekėjo SF pasirinkus subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali būti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos linija | Subrangos linija, pagal kurią produktai buvo užsakyti. Subrangos linijų, kurias galima pasirinkti, sąrašas apima tik pasirinktos subrangos linijas. | Kai produktų tiekėjo SF eilutėje pasirenkama subrangos eilutė, numatytosios laukų **Projektas**, **Užduotis** ir **Produktas** reikšmės įvedamos iš atitinkamų subrangos linijos laukų. Jei pasirinktoje subrangos eilutėje yra reikšmių laukuose **Projektas**, **Užduotis** ir **Produktas**, tiekėjo SF eilutės atitinkamų laukų reikšmės negali skirtis nuo šių reikšmių. |
| Operacijos data | Data, kada tiekėjo SF eilutės faktinės išlaidos bus įrašytos į projektą. | Joks|
| Operacijos klasė | Kai produktams išrašoma sf, šis laukas turi būti nustatytas kaip **Medžiaga**. | Reikšmė **Medžiaga** nurodo, kad tiekėjo SF eilutė naudojama įsigytų medžiagų SF sumai įrašyti. |
| Project | Projekto, kuriame buvo naudojami produktai, kuriems išrašomos sąskaitos faktūros, pavadinimas. | Šis laukas yra būtinas ir jo negalima palikti tuščio. |
| Užduotis | Projekto užduoties, kuriai buvo naudojami produktai, kuriems išrašomos sąskaitos faktūros, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali susieti tiekėjo SF eilutę su įsigytu produktu, kuris naudojamas bet kuriai projekto užduočiai atlikti. Jei tiekėjo SF eilutėje nenurodyta subrangos eilutė, o šis laukas paliekamas tuščias, faktinės išlaidos, kurias sukuria tiekėjo SF eilutė, nebus susietos su jokiais neįrašytais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, išlaidų sąskaitos faktūros galutiniam klientui nebus galima išrašyti. |
| Pasirinkti produktą | Pasirinkite, ar produktas, kuriam išrašomos sąskaitos faktūros, yra esamas produktas iš katalogo, ar įrašymo produktas. | Numatytoji reikšmė įvedama iš subrangos linijos, kai pasirenkama subrangos linija. |
| Produktas | Pasirinkite produktą iš katalogo. Jei produktas yra įrašomas produktas, įveskite produkto pavadinimą. | Šis laukas naudojamas norint įvesti numatytąsias esamų produktų pirkimo kainas. |
| Kiekis | Šioje SF eilutėje įveskite medžiagos kiekį, kuriam tiekėjas išrašo SF. | Joks |
| Vienetų grupė | Pasirinkite vieneto vienetų grupę, kuria išreiškiamas kiekis, kuriam išrašomos sąskaitos faktūros. | Joks |
| Vienetas | Numatytoji reikšmė yra pasirinktos vienetų grupės pagrindinis vienetas. Šią vertę galite pakeisti, kad mokėtumėte bet kuriuo pasirinktos vienetų grupės vienetu. | Produkto ir vieneto **reikšmių** derinys bus naudojamas kaip numatytoji arba apskaičiuota lauko Vieneto **kaina** tiekėjo SF eilutėje reikšmė.**·** |
| Vieneto kaina | Numatytoji vieneto kaina naudoja produkto **ir** vieneto **reikšmių** derinį iš projekto kainoraščio, kuris taikomas tiekėjo SF eilutės operacijos datai. | Joks |
| Tarpinė suma | Šis tik skaityti skirtas laukas apskaičiuojamas kaip *kiekio*&times;*vieneto kaina*, jei reikšmės įvedamos ir **lauke Kiekis,** ir lauke Vieneto **kaina.** Jei vienas arba abu šie laukai yra tušti, šiame lauke galite įvesti reikšmę. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendra tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *tarpinis tarpinis PVM* + *·*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
