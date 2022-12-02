---
title: Tiekėjo sąskaitos faktūros etapų eilutės
description: Šiame straipsnyje paaiškinta, kaip sukurti etapams skirtas tiekėjo sąskaitos faktūros eilutes dėl sustabdymo.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f066c2ac7377a989a92a9ae2e9a732d3c979a0db
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261038"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Tiekėjo sąskaitos faktūros etapų eilutės

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Microsoft Dynamics 365 Project Operations " tiekėjo sąskaitoje faktūroje gali būti etapų tiekėjo sąskaitos faktūros eilučių, apibrėžtų išsamūsoje eilutėje. Projektų vadovai gali naudoti etapų tiekėjo sąskaitų faktūrų eilutes, kad įrašydamos aptarnavimo išlaidas, kurios yra įsigytos kaip etapinės išlaidos, susijusios su projektui įsigytais aptarnavimais arba produktais.

Etapų tiekėjo sąskaitos faktūros eilutėse visada turi būti nurodyta sudėtys, kurioms taikomas fiksuotos kainos atsiskaitymo metodas. Kai etapų tiekėjo sąskaitos faktūros eilutė nurodo sudėčių eilutę, projektų vadovai galės greti ir patikrinti pagrindines laiko, išlaidų ar medžiagos išlaidas, kurios nurodo, kad etapą, kuriam tiekėjas išrašo sąskaitą faktūrą, sugretinti.

Toliau pateiktoje lentelėje nurodyta informacija apie laukelius tiekėjo sąskaitos eilutėse pagrindiniams terminams.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Subrangos sąskaitos eiltuės pavadinimas, kuris padeda identifikuoti. | Jis bus rodomas kaip pirmasis visų peržvalgų stulpelis, remiantis subrangos sutarties eilutėmis. |
| Aprašą | Trumpas paslaugų arba produktų, perkamų pagal tiekėjo sąskaitos faktūros eilutes, aprašas. | Joks |
| Subrangos sutartis | Paslaugų papildomo tiekėjo užsakymas. | Kai pasirenkamas tiekėjo sąskaitos faktūros sutemdumas, visos tiekėjo sąskaitos faktūros eilutės paveldės tą pasirinkimą. Tiekėjo sąskaitoje faktūroje negali būti tiekėjo sąskaitos faktūros eilučių, kurios nurodo skirtingus inodus. |
| Subrangos sutarties eilutė | Papildoma sutarties eilutė, pagal kurią paslaugos buvo užsakytos. Galima pasirinkti tik pažymėtų ne darbo laiko tarpo eilučių sąrašą. | Kai tiekėjo sąskaitos faktūros eilutėje, susijusioje su etapais, yra pasirinkta sąrangos **eilutė** vaidmenų **ir operacijų kategorijos** laukai ir su produktu susiję laukai yra netinkami ir jų nėra. Kiekio **vieneto** ir **vienetų** grupės laukai taip **pat** nėra susiję su etapų tiekėjo sąskaitos faktūros eilutėmis. |
| Operacijos data | Data, kai į projektą bus įrašytos tiekėjo sąskaitos faktūros eilutės išlaidos. | Joks |
| Operacijos klasė | Pažymėkite **etapą**, kad būtų galima įrašyti užbaigto etapo, kuris buvo apibrėžtas sudėtame ne išsamūs eilutėje, tiekėjo sąskaitą faktūrą. | Joks |
| Etapas | Pažymėkite etapą, apibrėžtą susijusioje susietus sąrangos eilutėje, pažymėtoje kaip Paruošta **sąskaita faktūra**. | Papildomos sutarties eiltuės pagrindiniai terminai **Paruoštą išrašyti sąskaitą** gali būti pasirinkti tiekėjo sąskaitose eilutėje. |
| Project | Projekto pavadinimas, dėl kurio naudojamos paslaugos buvo įtrauktos į sąskaitą. | Būtinas užpildyti laukas negali būti tuščias. |
| Užduotis | Projekto užduoties pavadinimas, dėl kurio naudojamos paslaugos buvo įtrauktos į sąskaitą. Šis laukas galimas tik jei pažymėtas projektas. Projekto užduoties pasirinkimas yra pasirinktinis. | Jei šis laukas paliekamas tuščias, projekto vadovas gali sugretinti tiekėjo sąskaitos faktūros eilutę su susijusios eilutės, įrašytos bet kurioje projekto užduotyje, operacijų klasėmis. Jei tiekėjo sąskaitos faktūros eilutėje nėra nuorodos į suslėptą eilutę, o šis laukas paliekamas tuščias, faktinės išlaidos, kurias sukūrė tiekėjo sąskaitos faktūros eilutė, nebus susietos su bet kokiais neišrašytus pardavimo faktiniais įrašais. Tokiu atveju, jei nustatomas užduotimis pagrįstas atsiskaitymas, klientui sąskaitos faktūros gali nepavykti išrašyti. |
| Etapo suma | Įveskite vertę etape, apibrėžtą susijusioje susietus sąrangos eilutėje, pažymėtoje kaip Paruošta sąskaita faktūra. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendra subrangos tiekėjo SF eilutės suma įskaitant mokesčius. Tai tik skaityti skirtas laukas *Etapo suma* + *Pardavimo mokesčiai*. | Joks |

> [!NOTE]
> Sukūrus tiekėjo sąskaitos faktūros eilutę, kuri nurodo etapą,, kuriame yra išsąstas etapas, išiemos etapo būsena atnaujinama į sukurtą tiekėjo **sąskaitą faktūrą**. Tada, kai patvirtinama ta tiekėjo sąskaita faktūra, persodinamas eilutės etapas atnaujinamas į tiekėjo **sąskaitą faktūrą**.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
