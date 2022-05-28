---
title: Tiekėjo SF eilutės laikui
description: Šioje temoje paaiškinama, kaip įrašyti tiekėjo SF eilutes laiko išlaidoms, kurias įdėjo subrangovai.
author: rumant
ms.date: 03/15/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ac598dff7b0b4a29ac0397a31130ada3b197fe44
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597210"
---
# <a name="vendor-invoice-lines-for-time"></a>Tiekėjo SF eilutės laikui

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations gali turėti tiekėjo SF eilutes. Projektų vadovai gali naudoti tiekėjo SF eilutes laikui, kad įrašytų subrangovo laiko sąnaudas projektuose.

Tiekėjo SF eilutės laikui gali arba negali nurodyti antrinės sutarties eilutės. Jei tiekėjo SF eilutė laiko nuoroda nurodo subrangos sutartį, projektų vadovai galės suderinti ir patikrinti laiką, kuriam tiekėjo SF eilutė išrašo SF eilutę pagal laiką, kurį įrašo subrangovai ir patvirtina projekto vadovai.

Šioje lentelėje pateikiama informacija apie tiekėjo SF eilučių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas paslaugų, kurioms tiekėjas tiekėjo SF eilutėje išrašo SF, aprašymas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią paslaugos iš pradžių buvo užsakytos. | Pasirinkus tiekėjo SF subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali turėti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos eilutė | Subrangos eilutė, kurioje buvo užsakytos paslaugos. Subrangos eilučių, kurias galima pasirinkti, sąrašas apsiriboja pasirinkto subrangos sutarties eilutėmis. | Kai tiekėjo SF eilutėje pasirenkama subrangos eilutė laikui, iš atitinkamų subrangos eilutės laukų Projektas **,** Vaidmuo **ir** Rezervuojamas išteklius **numatytosios vertės** įvedamos iš atitinkamų subrangos eilutės laukų. Jei pasirinktoje subrangos eilutėje yra vertės laukuose **Projektas**, **Vaidmuo** ir **Rezervuojama**, atitinkamų tiekėjo SF eilutės laukų vertės negali skirtis nuo šių verčių. |
| Operacijos data | Data, kai tiekėjo SF eilutės faktinė savikaina bus įrašyta į projektą. | Joks |
| Operacijos klasė | Numatytoji reikšmė yra **Laikas**. | Vertės **laikas** rodo, kad tiekėjo SF eilutė naudojama subrangovo laiko SF sumai įrašyti. |
| Project | Projekto, kuriame buvo naudojamos paslaugos, kurioms išrašyta SF, pavadinimas. | Šis laukas yra būtinas ir negali būti paliktas tuščias. |
| Užduotis | Projekto užduoties, kuriai buvo naudojamos paslaugos, kurioms išrašyta SF, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali suderinti tiekėjo SF eilutę su laiku, kurį subrangovo ištekliai įrašo į bet kurią projekto užduotį. Jei tiekėjo SF eilutė nenurodo subrangos eilutės ir šis laukas paliekamas tuščias, tiekėjo SF eilutėje sukurta faktinė savikaina nebus susieta su jokiais neapmokėtais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, išlaidoms gali nepavykti išrašyti SF galutiniam vartotojui. |
| Vaidmuo | Subrangos išteklių, kurių laikui išrašyta SF, vaidmuo. | Šiame lauke nurodomas vaidmuo, kurį atlieka subrangos ištekliai, kurių laikas tiekėjo SF išrašytas. |
| Rezervuojami ištekliai | Subrangovo, kurio laikui išrašyta SF, pavadinimas. Rezervuoto ištekliaus pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali suderinti tiekėjo SF eilutę su laiku, kurį įrašo bet kuris tiekėjo SF eilutės tiekėjui priklausantis išteklius. |
| Kiekis | Įveskite laiko valandų skaičių, kuriam SF eilutėje tiekėjas išrašo SF. |Joks |
| Vienetų grupė | Numatytoji reikšmė yra **Laiko vienetų grupė** ir jos keisti negalima. | Joks |
| Vienetas | Numatytoji vertė yra bazinis valandų vienetas iš laiko vienetų grupės. Šią vertę galite keisti, kad pirktumėte bet kuriame laiko vienetų grupės vienete, pvz., dieną ar savaitę. | Vaidmens ir vieneto **verčių** derinys bus naudojamas kaip numatytoji **arba apskaičiuota tiekėjo SF eilutės lauko Vieneto kaina** vertė.**·** |
| Vieneto kaina | Numatytoji vieneto kaina naudoja vaidmens **ir** vieneto **verčių** derinį iš projekto kainoraščio, kuris taikomas tiekėjo SF eilutės operacijos datai. | Jei taikomo projekto kainoraščio kaina nustatoma vienetu, kuris skiriasi nuo vieneto tiekėjo SF eilutėje, sistema naudoja vieneto konvertavimą, kad apskaičiuotų vieneto kainą. |
| Tarpinė suma | Šis tik skaitomas laukas apskaičiuojamas kaip *Kiekio*&times;*vieneto kaina*, jei vertės įvedamos ir **į lauką Kiekis**, ir į lauką Vieneto **kaina.** Jei vienas arba abu šie laukai yra tušti, šiame lauke galite įvesti vertę. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendroji tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *tarpinės sumos* + *PVM*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
