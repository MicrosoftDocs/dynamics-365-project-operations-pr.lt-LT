---
title: Tiekėjo sąskaitos faktūros eilutės, skirtos išlaidų kategorijoms
description: Šiame straipsnyje paaiškinama, kaip įrašyti išlaidų kategorijų tiekėjo SF eilutes.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 3ffad20b53344221ead9b6850ecdc1efd48d5b13
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925896"
---
# <a name="vendor-invoice-lines-for-expense-categories"></a>Tiekėjo sąskaitos faktūros eilutės, skirtos išlaidų kategorijoms

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

"Microsoft" Dynamics 365 Project Operations tiekėjo SF gali turėti išlaidų kategorijų tiekėjo SF eilutes. Projektų vadovai gali naudoti tiekėjo SF eilutes išlaidų kategorijoms, kad įrašytų aptarnavimo, įsigyto kaip išlaidų kategorijos, išlaidas.

Išlaidų kategorijų tiekėjo SF eilutės gali arba negali nurodyti išlaidų kategorijų subrangos eilutės. Jei išlaidų kategorijų tiekėjo SF eilutė nurodo subrangos sutartį, projektų vadovai galės suderinti ir patikrinti išlaidas, kurioms tiekėjo SF eilutė išrašo SF eilutę, ir jas patikrinti su išlaidomis, įrašytomis šiose išlaidų kategorijose ir patvirtintomis projekto vadovų.

Šioje lentelėje pateikiama informacija apie išlaidų kategorijų tiekėjo SF eilučių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas paslaugų, kurioms tiekėjas tiekėjo SF eilutėje išrašo SF, aprašymas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią paslaugos iš pradžių buvo užsakytos. | Pasirinkus tiekėjo SF subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali turėti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos eilutė | Subrangos eilutė, kurioje buvo užsakytos paslaugos. Subrangos eilučių, kurias galima pasirinkti, sąrašas apsiriboja pasirinkto subrangos sutarties eilutėmis. | Kai išlaidų kategorijų tiekėjo SF eilutėje pasirenkama subrangos eilutė, iš atitinkamų subrangos eilutės laukų Projektas **,** Užduotis **ir** Operacija **numatytosios vertės** įvedamos iš atitinkamų subrangos eilutės laukų. Jei pasirinktos subrangos eilutės laukuose **Projektas**, **Projekto užduotis** ir **Operacija** yra reikšmių, atitinkamų tiekėjo SF eilutės laukų vertės negali skirtis nuo šių verčių. |
| Operacijos data | Data, kai tiekėjo SF eilutės faktinė savikaina bus įrašyta į projektą. |Joks |
| Operacijos klasė | Pasirinkite **Išlaidos**, jei norite įrašyti išlaidų kategorijos tiekėjo SF. | Vertė **Išlaidos** nurodo, kad tiekėjo SF eilutė naudojama aptarnavimo, kuris buvo įsigytas kaip išlaidų kategorijos, SF sumai įrašyti. |
| Project | Projekto, kuriame buvo naudojamos paslaugos, kurioms išrašyta SF, pavadinimas. | Šis laukas yra būtinas ir negali būti paliktas tuščias. |
| Užduotis | Projekto užduoties, kuriai buvo naudojamos paslaugos, kurioms išrašyta SF, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali suderinti tiekėjo SF eilutę su išlaidomis, įrašytomis į bet kurią projekto užduotį. Jei tiekėjo SF eilutė nenurodo subrangos eilutės ir šis laukas paliekamas tuščias, tiekėjo SF eilutėje sukurta faktinė savikaina nebus susieta su jokiais neapmokėtais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, išlaidoms gali nepavykti išrašyti SF galutiniam vartotojui. |
| Operacijos kategorija | Operacijos kategorija, kuriai išrašyta SF. Turi būti sukurta atitinkama pasirinktos operacijos kategorijos išlaidų kategorija. | Operacijos kategorijos **ir vieneto** **verčių derinys bus naudojamas kaip numatytoji** arba apskaičiuota tiekėjo SF eilutės lauko Vieneto kaina **vertė**. |
| Kiekis | Įveskite kiekį, kuriam SF eilutėje tiekėjas išrašo SF. |Joks|
| Vienetų grupė | Numatytoji vertė įvedama pagal pasirinktos operacijos kategorijos vienetų grupę. | Joks |
| Vienetas | Numatytoji vertė yra pasirinktos vienetų grupės bazinis vienetas. Šią vertę galite keisti, kad pirktumėte bet kuriame vienetų grupės vienete. | Operacijos kategorijos **ir vieneto** **verčių derinys bus naudojamas kaip numatytoji** arba apskaičiuota tiekėjo SF eilutės lauko Vieneto kaina **vertė**. |
| Vieneto kaina | Numatytoji vieneto kaina naudoja operacijos kategorijos **ir** vieneto **verčių** derinį iš projekto kainoraščio, kuris taikomas tiekėjo SF eilutės operacijos datai. | Jei taikomo projekto kainoraščio kaina nustatoma vienetu, kuris skiriasi nuo vieneto tiekėjo SF eilutėje, sistema naudoja vieneto konvertavimą, kad apskaičiuotų vieneto kainą. |
| Tarpinė suma | Šis tik skaitomas laukas apskaičiuojamas kaip *Kiekio*&times;*vieneto kaina*, jei vertės įvedamos ir **į lauką Kiekis**, ir į lauką Vieneto **kaina.** Jei vienas arba abu šie laukai yra tušti, šiame lauke galite įvesti vertę.| Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendroji tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *tarpinės sumos* + *PVM*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
