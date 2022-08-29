---
title: Tiekėjo sąskaitos faktūros laiko eilutės
description: Šiame straipsnyje paaiškinama, kaip įrašyti tiekėjo SF eilutes, skirtas laiko išlaidoms, kurias įdeda subrangovai.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 7f28af3ad76d456dddcfd8e85d968cecb773f8fc
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9262023"
---
# <a name="vendor-invoice-lines-for-time"></a>Tiekėjo sąskaitos faktūros laiko eilutės

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations tam tikrą laiką tiekėjo SF eilutės gali būti nurodytos. Projektų vadovai gali tam tikrą laiką naudoti tiekėjo SF eilutes, kad įrašytų subrangovų laiko sąnaudas projektuose.

Tiekėjo SF eilutės laiko atžvilgiu gali nurodyti subrangos liniją arba jos nenurodyti. Jei tiekėjo SF eilutė, skirta laiko nuorodoms, nurodo subrangos sutartį, projektų vadovai galės sugretinti ir patikrinti laiką, kuriam tiekėjo SF eilutė išrašo sąskaitą faktūrą, su laiku, kurį įrašo subrangovai ir patvirtina projekto vadovai.

Šioje lentelėje pateikiama informacija apie tiekėjo SF eilučių laukus tam tikrą laiką.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas paslaugų, kurioms tiekėjas išrašo SF sf eilutę tiekėjo SF eilutėje, aprašas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią paslaugos iš pradžių buvo užsakytos. | Tiekėjo SF pasirinkus subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali būti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos linija | Subrangos linija, pagal kurią buvo užsakytos paslaugos. Subrangos linijų, kurias galima pasirinkti, sąrašas apima tik pasirinktos subrangos linijas. | Kai tiekėjo SF eilutėje laiko atžvilgiu pasirenkama subrangos eilutė, numatytosios laukų **Projektas**, **Vaidmuo** ir **Rezervuojamas išteklius** reikšmės įvedamos iš atitinkamų subrangos linijos laukų. Jei pasirinktos subrangos eilutės reikšmės yra laukuose **Projektas**, **Vaidmuo** ir **Rezervuojama**, atitinkamų laukų tiekėjo SF eilutėje reikšmės negali skirtis nuo tų reikšmių. |
| Operacijos data | Data, kada tiekėjo SF eilutės faktinės išlaidos bus įrašytos į projektą. | Joks |
| Operacijos klasė | Numatytoji reikšmė yra **Laikas**. | Reikšmė **Laikas** nurodo, kad tiekėjo SF eilutė naudojama subrangovo laiko SF sumai įrašyti. |
| Project | Projekto, kuriame buvo naudojamos paslaugos, kurioms išrašomos sąskaitos faktūros, pavadinimas. | Šis laukas yra būtinas ir jo negalima palikti tuščio. |
| Užduotis | Projekto užduoties, kuriai buvo naudojamos paslaugos, kurioms išrašomos sąskaitos faktūros, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali susieti tiekėjo SF eilutę su laiku, kurį subrangovo ištekliai įrašo atlikdami bet kurią projekto užduotį. Jei tiekėjo SF eilutėje nenurodyta subrangos eilutė, o šis laukas paliekamas tuščias, faktinės išlaidos, kurias sukuria tiekėjo SF eilutė, nebus susietos su jokiais neįrašytais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, gali nepavykti išrašyti išlaidų sąskaitos faktūros galutiniam klientui. |
| Vaidmuo | Subrangos išteklių, kurių laikas išrašomas sąskaitose faktūrose, vaidmuo. | Šiame lauke nurodomas vaidmuo, kurį atlieka subrangos ištekliai, kurių laikas nurodytas tiekėjo SF. |
| Rezervuojami ištekliai | Subrangovo, kurio laikas išrašomas sąskaitose faktūrose, pavadinimas. Rezervuojamo šaltinio pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali susieti tiekėjo SF eilutę su laiku, kurį tiekėjo SF eilutėje įrašo bet kuris tiekėjui priklausantis išteklius. |
| Kiekis | Įveskite laiko, kurį tiekėjas sf išrašo sf sf, skaičių SF eilutėje. |Joks |
| Vienetų grupė | Numatytoji reikšmė yra **laiko vienetų grupė** ir jos keisti negalima. | Joks |
| Vienetas | Numatytoji reikšmė yra pagrindinis valandų vienetas iš laiko vienetų grupės. Šią vertę galite pakeisti, kad įpirktumėte bet kurį laiko vienetų grupės vienetą, pvz., dieną ar savaitę. | Vaidmens ir vieneto **reikšmių** derinys bus naudojamas kaip numatytoji arba apskaičiuota lauko Vieneto **kaina** tiekėjo SF eilutėje reikšmė.**·** |
| Vieneto kaina | Numatytoji vieneto kaina naudoja vaidmens **ir** vieneto **reikšmių** derinį iš projekto kainoraščio, kuris taikomas tiekėjo SF eilutės operacijos datai. | Jei taikomo projekto kainoraščio kaina nustatoma vienete, kuris skiriasi nuo tiekėjo SF eilutėje nurodyto vieneto, sistema naudoja vieneto konvertavimą, kad apskaičiuotų vieneto kainą už vienetą. |
| Tarpinė suma | Šis tik skaityti skirtas laukas apskaičiuojamas kaip *kiekio*&times;*vieneto kaina*, jei reikšmės įvedamos ir **lauke Kiekis,** ir lauke Vieneto **kaina.** Jei vienas arba abu šie laukai yra tušti, šiame lauke galite įvesti reikšmę. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendra tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *tarpinis tarpinis PVM* + *·*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
