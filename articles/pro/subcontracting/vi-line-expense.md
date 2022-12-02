---
title: Tiekėjo sąskaitos faktūros eilutės, skirtos išlaidų kategorijoms
description: Šiame straipsnyje aiškinama, kaip įrašyti išlaidų kategorijų tiekėjo sąskaitos faktūros eilutes.
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

Tiekėjo sąskaitoje „Microsoft Dynamics 365 Project Operations“ faktūroje gali būti tiekėjo SF išlaidų kategorijos. Projektų vadovai išlaidų kategorijoms gali naudoti tiekėjo sąskaitų faktūrų eilutes paslaugų, kurios perkamos kaip išlaidų kategorijos, išlaidoms įrašyti.

Tiekėjo sąskaitos išlaidų kategorijos gali nurodyti ar ne nurodyti laiko sustabdymo eilutę išlaidų kategorijoms. Kai etapų tiekėjo sąskaitos faktūros eilutė nurodo sudėčių eilutę, projektų vadovai galės greti ir patikrinti pagrindines laiko, išlaidų ar medžiagos išlaidas, kurios nurodo, kad etapą, kuriam papildomi tiekėjai išrašo sąskaitą faktūrą ir kurią patvirtina projekto vadovai pagal projektą, sugretinti.

Toliau pateiktoje lentelėje nurodyta informacija apie laukelius tiekėjo sąskaitos eilutėse išlaidų kategorijoms.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Subrangos sąskaitos eiltuės pavadinimas, kuris padeda identifikuoti. | Jis bus rodomas kaip pirmasis visų peržvalgų stulpelis, remiantis subrangos sutarties eilutėmis. |
| Aprašą | Trumpas paslaugų perkamų pagal tiekėjo sąskaitos faktūros eilutes, aprašas. | Joks |
| Subrangos sutartis | Paslaugų papildomo tiekėjo užsakymas. | Kai pasirenkamas tiekėjo sąskaitos faktūros sutemdumas, visos tiekėjo sąskaitos faktūros eilutės paveldės tą pasirinkimą. Tiekėjo sąskaitoje faktūroje negali būti tiekėjo sąskaitos faktūros eilučių, kurios nurodo skirtingus inodus. |
| Subrangos sutarties eilutė | Papildoma sutarties eilutė, pagal kurią paslaugos buvo užsakytos. Galima pasirinkti tik pažymėtų ne darbo laiko tarpo eilučių sąrašą. | Kai tiekėjo sąskaitos faktūros eilutėje, skirtame išlaidų kategorijoms, yra pasirinkta sąsodinė eilutė, **projekto**, **užduoties** ir **transakcijos kategorijų** laukų numatytosios reikšmės įvedamos iš atitinkamų stulpelių, esančiuose hierarchijos eilutėje. Jei pasirinktoje inakcijos **eilutėje** yra **reikšmių** laukuose Projektu, **Projekto užduotis** ir Operacijų kategorija, atitinkamų laukų reikšmės tiekėjo sąskaitos faktūros eilutėje negali skirtis nuo šių reikšmių. |
| Operacijos data | Data, kai į projektą bus įrašytos tiekėjo sąskaitos faktūros eilutės išlaidos. |Joks |
| Operacijos klasė | Pažymėkite **Išlaidos**, jei norite įrašyti išlaidų kategorijos tiekėjo sąskaitą faktūrą. | Reikšmė Išlaidos **rodo**, kad tiekėjo sąskaitos faktūros eilutė naudojama paslaugų, kurios buvo įsigytos kaip išlaidų kategorijos, sąskaitos faktūros sumai įrašyti. |
| Project | Projekto pavadinimas, dėl kurio naudojamos paslaugos buvo įtrauktos į sąskaitą. | Būtinas užpildyti laukas negali būti tuščias. |
| Užduotis | Projekto užduoties pavadinimas, dėl kurio naudojamos paslaugos buvo įtrauktos į sąskaitą. Šis laukas galimas tik jei pažymėtas projektas. Projekto užduoties pasirinkimas yra pasirinktinis. | Jei šis laukas neužpildytas, projekto vadovas gali sugretinti tiekėjo sąskaitos faktūros eilutę su išlaidoms, įrašytoms bet kurioje projekto užduotyje. Jei tiekėjo sąskaitos faktūros eilutėje nėra nuorodos į suslėptą eilutę, o šis laukas paliekamas tuščias, faktinės išlaidos, kurias sukūrė tiekėjo sąskaitos faktūros eilutė, nebus susietos su bet kokiais neišrašytus pardavimo faktiniais įrašais. Tokiu atveju, jei nustatomas užduotimis pagrįstas atsiskaitymas, klientui sąskaitos faktūros gali nepavykti išrašyti. |
| Operacijos kategorija | Operacijos kategorija, pagal kurią išrašyta sąskaita faktūra. Reikia sukurti atitinkamą pažymėtos transakcijos kategorijos išlaidų kategoriją. | **Transakcijos Kategorijos** ir **Vieneto** vertės bus naudojamos kaip numatytotios ar apskaičiuota **Vieneto kainos vertės** laukelis tiekėjo SF eilutėje. |
| Kiekis | Sąskaitos faktūros eilutėje įveskite kiekį, kuriam tiekėjas išrašo sąskaitą faktūrą. |Joks|
| Vienetų grupė | Numatytoji reikšmė yra pagrįsta numatytąja vienetų grupe, nustatyta pažymėtai transakcijos kategorijai. | Joks |
| Vienetas | Numatytoji vertė yra pagrindinis pasirinktas vieneto grupės vienetas. Šią reikšmę galite pakeisti, jei norite įsigyti bet kurį laiko vienetų grupės vienetą. | **Transakcijos Kategorijos** ir **Vieneto** vertės bus naudojamos kaip numatytotios ar apskaičiuota **Vieneto kainos vertės** laukelis tiekėjo SF eilutėje. |
| Vieneto kaina | Numatytoji vieneto kainos reikšmė pagal numatytąją **Transakcijos kategoriją** ir **Vieneto** vertės iš projekto kainos sąrašo, kuris yra taikomas tiekėjo sąskaitos eilutės transakcijos datai. | Jei kaina taikomame projekto kainoraštyje kaina nustatyta skirtingu vienetu nei tiekėjo SF vienetas, sistema vieneto kainai apskaičiuoti naudoja vienetų konvertavimo funkciją. |
| Tarpinė suma | Šis tik skaityti skirtas laukas kaip *Kiekio* &times; *Vieneto kaina*, jei vertės yra įvestos tiek į **Kiekio** lauką, tiek į **Vieneto kaino** lauką. Jei bet kuris ar arba abu laukai yra tušti, šiame lauke galite įvesti reikšmę.| Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendra subrangos tiekėjo SF eilutės suma įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *Tarpinė suma* + *Pardavimo mokesčiai*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
