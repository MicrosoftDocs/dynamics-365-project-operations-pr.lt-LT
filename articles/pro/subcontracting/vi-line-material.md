---
title: Tiekėjo sąskaitos faktūros produktų eilutės
description: Šiame straipsnyje aiškinama, kaip įrašyti produktų tiekėjo SF eilutes, ir naudotis skirtingais laukais norint įrašyti produktų pirkimus iš tiekėjų.
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

Tiekėjo sąskaitoje „Microsoft Dynamics 365 Project Operations“ faktūroje gali būti produktų (dar vadinamų medžiaga) tiekėjo sąskaitų faktūrų eilučių. Projektų vadovai gali naudoti tiekėjo sąskaitų faktūrų eilutes laikui įrašyti produktams, kurie buvo publikuoti projektuose.

Tiekėjo sąskaitos faktūros produktai laikui gali nurodyti arba ne nurodyti medžiagos sustabdymo eilutę. Kai etapų tiekėjo sąskaitos faktūros eilutė nurodo sudėčių eilutę, projektų vadovai galės greti ir patikrinti pagrindines laiko, išlaidų ar medžiagos išlaidas, kurios nurodo, kad etapą, kuriam papildomi tiekėjai išrašo sąskaitą faktūrą ir kurią patvirtina projekto vadovai pagal projektą, sugretinti.

Toliau pateiktoje lentelėje nurodyta informacija apie laukelius tiekėjo sąskaitos eilutėse produktams.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Subrangos sąskaitos eiltuės pavadinimas, kuris padeda identifikuoti. | Jis bus rodomas kaip pirmasis visų peržvalgų stulpelis, remiantis subrangos sutarties eilutėmis. |
| Aprašą | Trumpas produktų, perkamų pagal tiekėjo sąskaitos faktūros eilutes, aprašas. | Joks |
| Subrangos sutartis | Produktų iš pradžių užsakymas. | Kai pasirenkamas tiekėjo sąskaitos faktūros sutemdumas, visos tiekėjo sąskaitos faktūros eilutės paveldės tą pasirinkimą. Tiekėjo sąskaitoje faktūroje negali būti tiekėjo sąskaitos faktūros eilučių, kurios nurodo skirtingus inodus. |
| Subrangos sutarties eilutė | Papildoma sutarties eilutė, pagal kurią produktai buvo užsakyti. Galima pasirinkti tik pažymėtų ne darbo laiko tarpo eilučių sąrašą. | Kai tiekėjo sąskaitos faktūros eilutėje, skirtame produktams, yra pasirinkta sąsodinė eilutė, **projekto**, **užduoties** ir **Produktas** laukų numatytosios reikšmės įvedamos iš atitinkamų stulpelių, esančiuose hierarchijos eilutėje. Jei pasirinktoje inakcijos **eilutėje** yra **Užduoties** laukuose Projekto, **Produktas** ir Operacijų kategorija, atitinkamų laukų reikšmės tiekėjo sąskaitos faktūros eilutėje negali skirtis nuo šių reikšmių. |
| Operacijos data | Data, kai į projektą bus įrašytos tiekėjo sąskaitos faktūros eilutės išlaidos. | Joks|
| Operacijos klasė | Kai išrašote produktų sąskaitą faktūrą, šis laukas turi būti nustatytas kaip **Medžiaga**. | Reikšmė Išlaidos **Medžiaga**, kad tiekėjo sąskaitos faktūros eilutė naudojama paslaugų, kurios buvo įsigytos kaip medžiagoms, SF. |
| Project | Projekto pavadinimas, dėl kurio naudojamos išrašytos sąskaitos. | Būtinas užpildyti laukas negali būti tuščias. |
| Užduotis | Projekto užduoties pavadinimas, dėl kurio naudojamos išrašytos sąskaitos. Šis laukas galimas tik jei pažymėtas projektas. Projekto užduoties pasirinkimas yra pasirinktinis. | Jei šis laukas neužpildytas, projekto vadovas gali sugretinti tiekėjo sąskaitos faktūros eilutę su įsigytais produktais, kurie yra naudojami bet kuriai projekto užduočiai. Jei tiekėjo sąskaitos faktūros eilutėje nėra nuorodos į suslėptą eilutę, o šis laukas paliekamas tuščias, faktinės išlaidos, kurias sukūrė tiekėjo sąskaitos faktūros eilutė, nebus susietos su bet kokiais neišrašytus pardavimo faktiniais įrašais. Tokiu atveju, jei nustatomas užduotimis pagrįstas atsiskaitymas, klientui sąskaitos faktūros išrašyti nepavyks. |
| Pasirinkti produktą | Pasirinkite, ar produktas yra įtrauktas į sąskaitą yra egzistuojantis produktas iš katalogo ar įtraukiamasis produktas. | Numatytoji reikšmė įvedama iš indingos eilutės, kai yra pažymėta neesminė eilutė. |
| Produktas | Pasirinkite produktą iš katalogo. Jei produktas yra įtrauukiamasis produktas, įveskite jo vardą. | Šis laukas naudojamas esamų produktų numatytosios pirkimo kainoms įvesti. |
| Kiekis | Sąskaitos faktūros eilutėje įveskite medžiagos kiekį, kuriam tiekėjas išrašo sąskaitą faktūrą. | Joks |
| Vienetų grupė | Pažymėkite vienetų grupę, pagal kurią nurodomas kiekis, kuriam išrašyta sąskaita faktūra. | Joks |
| Vienetas | Numatytoji vertė yra pagrindinis pasirinktas vieneto grupės vienetas. Šią reikšmę galite pakeisti, jei norite apmokėti bet kurį laiko pasirinktą vienetų grupės vienetą. | **Produkto** ir **Vieneto** vertės bus naudojamos kaip numatytotios ar apskaičiuota **Vieneto kainos vertės** laukelis tiekėjo SF eilutėje. |
| Vieneto kaina | Numatytoji vieneto kainos reikšmė pagal numatytąją **Produkto** ir **Vieneto** vertės iš projekto kainos sąrašo, kuris yra taikomas tiekėjo sąskaitos eilutės transakcijos datai. | Joks |
| Tarpinė suma | Šis tik skaityti skirtas laukas kaip *Kiekio* &times; *Vieneto kaina*, jei vertės yra įvestos tiek į **Kiekio** lauką, tiek į **Vieneto kaino** lauką. Jei bet kuris ar arba abu laukai yra tušti, šiame lauke galite įvesti reikšmę. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendra subrangos tiekėjo SF eilutės suma įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *Tarpinė suma* + *Pardavimo mokesčiai*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
