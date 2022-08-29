---
title: Tiekėjo sąskaitos faktūros eilutės, skirtos išlaidų kategorijoms
description: Šiame straipsnyje paaiškinama, kaip įrašyti išlaidų kategorijų tiekėjo SF eilutes.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 2c3cd2fab87af1cbfccd81e543f2cea0278978f6
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261693"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Tiekėjo sąskaitos faktūros eilutės, skirtos išlaidų kategorijoms

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations gali būti tiekėjo SF eilutės, skirtos išlaidų kategorijoms. Projektų vadovai gali naudoti tiekėjo SF eilutes išlaidų kategorijoms, kad įrašytų įsigytų paslaugų išlaidas kaip išlaidų kategorijas.

Išlaidų kategorijų tiekėjo SF eilutės gali nurodyti išlaidų kategorijų subrangos eilutę arba ne. Jei išlaidų kategorijų tiekėjo SF eilutė nurodo subrangos sutartį, projektų vadovai galės susieti ir patikrinti išlaidas, kurioms tiekėjo SF eilutė išrašo sf, su išlaidomis, kurios įrašomos į šias išlaidų kategorijas ir kurias patvirtina projekto projektų vadovai.

Šioje lentelėje pateikiama informacija apie išlaidų kategorijų tiekėjo SF eilučių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas paslaugų, kurioms tiekėjas išrašo SF sf eilutę tiekėjo SF eilutėje, aprašas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią paslaugos iš pradžių buvo užsakytos. | Tiekėjo SF pasirinkus subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali būti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos linija | Subrangos linija, pagal kurią buvo užsakytos paslaugos. Subrangos linijų, kurias galima pasirinkti, sąrašas apima tik pasirinktos subrangos linijas. | Kai išlaidų kategorijų tiekėjo SF eilutėje pasirenkama subrangos eilutė, numatytosios laukų **Projektas** **,** Užduotis **ir** Operacija reikšmės įvedamos iš atitinkamų subrangos eilutės laukų. Jei pasirinktoje subrangos eilutėje yra reikšmių laukuose **Projektas**, **Užduotis Projektas** ir **Operacija**, atitinkamų laukų tiekėjo SF eilutėje reikšmės negali skirtis nuo tų reikšmių. |
| Operacijos data | Data, kada tiekėjo SF eilutės faktinės išlaidos bus įrašytos į projektą. |Joks |
| Operacijos klasė | Pasirinkite **Išlaidos**, kad įrašytumėte išlaidų kategorijos tiekėjo SF. | Reikšmė **Išlaidos** nurodo, kad tiekėjo SF eilutė naudojama paslaugų, kurios buvo įsigytos kaip išlaidų kategorijos, SF sumai įrašyti. |
| Project | Projekto, kuriame buvo naudojamos paslaugos, kurioms išrašomos sąskaitos faktūros, pavadinimas. | Šis laukas yra būtinas ir jo negalima palikti tuščio. |
| Užduotis | Projekto užduoties, kuriai buvo naudojamos paslaugos, kurioms išrašomos sąskaitos faktūros, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali susieti tiekėjo SF eilutę su išlaidomis, kurios įrašomos atliekant bet kurią projekto užduotį. Jei tiekėjo SF eilutėje nenurodyta subrangos eilutė, o šis laukas paliekamas tuščias, faktinės išlaidos, kurias sukuria tiekėjo SF eilutė, nebus susietos su jokiais neįrašytais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, gali nepavykti išrašyti išlaidų sąskaitos faktūros galutiniam klientui. |
| Operacijos kategorija | Operacijų kategorija, kuriai išrašomos sąskaitos faktūros. Pasirinktai operacijų kategorijai turi būti sukurta atitinkama išlaidų kategorija. | Operacijos kategorijos ir vieneto **reikšmių** derinys bus naudojamas kaip numatytoji arba apskaičiuota lauko Vieneto **kaina** tiekėjo SF eilutėje reikšmė.**·** |
| Kiekis | Įveskite kiekį, kuriam sf sf išrašo tiekėjas SF sf eilutėje. |Joks|
| Vienetų grupė | Numatytoji reikšmė įvedama pagal pasirinktos operacijos kategorijos vienetų grupę. | Joks |
| Vienetas | Numatytoji reikšmė yra pasirinktos vienetų grupės pagrindinis vienetas. Šią vertę galite pakeisti norėdami įsigyti bet kurį vienetų grupės vienetą. | Operacijos kategorijos ir vieneto **reikšmių** derinys bus naudojamas kaip numatytoji arba apskaičiuota lauko Vieneto **kaina** tiekėjo SF eilutėje reikšmė.**·** |
| Vieneto kaina | Numatytoji vieneto kaina naudoja operacijos kategorijos **ir** vieneto **reikšmių** derinį iš projekto kainoraščio, kuris taikomas tiekėjo SF eilutės operacijos datai. | Jei taikomo projekto kainoraščio kaina nustatoma vienete, kuris skiriasi nuo tiekėjo SF eilutėje nurodyto vieneto, sistema naudoja vieneto konvertavimą, kad apskaičiuotų vieneto kainą už vienetą. |
| Tarpinė suma | Šis tik skaityti skirtas laukas apskaičiuojamas kaip *kiekio*&times;*vieneto kaina*, jei reikšmės įvedamos ir **lauke Kiekis,** ir lauke Vieneto **kaina.** Jei vienas arba abu šie laukai yra tušti, šiame lauke galite įvesti reikšmę.| Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendra tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *tarpinis tarpinis PVM* + *·*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
