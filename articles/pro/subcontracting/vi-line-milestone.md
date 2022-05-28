---
title: Tiekėjo SF eilutės, skirtos etapams
description: Šioje temoje paaiškinama, kaip sukurti tiekėjo SF eilutes antrinės sutarties tarpiniams etapams.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 4fa11e2a4f459016b3ce141b03fe97e55c9a2759
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590632"
---
# <a name="vendor-invoice-lines-for-milestones"></a>Tiekėjo SF eilutės, skirtos etapams

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations gali turėti tiekėjo SF eilutes etapams, nurodytiems subrangos eilutėje. Projektų vadovai gali naudoti tiekėjo SF eilutes tarpiniams etapams, kad įrašytų aptarnavimo, kuris yra perkamas kaip etapais pagrįstas išlaidas, patiriamas teikiant paslaugas ar produktus, įsigytus projektui.

Etapų tiekėjo SF eilutėse visada turi būti nurodyta subrangos eilutė, kurioje yra fiksuotos kainos atsiskaitymo metodas. Kai etapų tiekėjo SF eilutė nurodo subrangos eilutę, projektų vadovai galės suderinti ir patikrinti pagrindines laiko, išlaidų ar medžiagų išlaidas, kurios nurodo tą subrangos eilutę su etapu, kuriam tiekėjas išrašo SF.

Šioje lentelėje pateikiama informacija apie etapų tiekėjo SF eilučių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas paslaugų, kurioms tiekėjas tiekėjo SF eilutėje išrašo SF, aprašymas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią paslaugos iš pradžių buvo užsakytos. | Pasirinkus tiekėjo SF subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali turėti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos eilutė | Subrangos eilutė, kurioje buvo užsakytos paslaugos. Subrangos eilučių, kurias galima pasirinkti, sąrašas apsiriboja pasirinkto subrangos sutarties eilutėmis. | Kai tarpinių etapų tiekėjo SF eilutėje pasirenkama antrinės sutarties eilutė, **laukai Vaidmuo** ir **Operacija** bei su produktu susiję laukai yra nesvarbūs ir nepasiekiami. Laukai **Kiekis**, **Vienetas** ir **Vienetų grupė** taip pat nėra svarbūs tarpiniu etapu pagrįstoms tiekėjo SF eilutėms. |
| Operacijos data | Data, kai tiekėjo SF eilutės faktinė savikaina bus įrašyta į projektą. | Joks |
| Operacijos klasė | Pasirinkite **Orientyras**, jei norite įrašyti tiekėjo SF už užbaigtą etapą, kuris buvo apibrėžtas subrangos eilutėje. | Joks |
| Etapas | Pasirinkite etapą, nurodytą susijusioje subrangos eilutėje, pažymėtoje kaip **Paruošta išrašyti SF**. | Subrangos eilutės etapus, kurių būsena **yra Paruošta išrašyti SF**, galima pasirinkti tiekėjo SF eilutėje. |
| Project | Projekto, kuriame buvo naudojamos paslaugos, kurioms išrašyta SF, pavadinimas. | Šis laukas yra būtinas ir negali būti paliktas tuščias. |
| Užduotis | Projekto užduoties, kuriai buvo naudojamos paslaugos, kurioms išrašyta SF, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali suderinti tiekėjo SF eilutę su susijusių subrangos eilutės operacijų klase, įrašyta į bet kurią projekto užduotį. Jei tiekėjo SF eilutė nenurodo subrangos eilutės ir šis laukas paliekamas tuščias, tiekėjo SF eilutėje sukurta faktinė savikaina nebus susieta su jokiais neapmokėtais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, išlaidoms gali nepavykti išrašyti SF galutiniam vartotojui. |
| Etapo suma | Įveskite etapo, nurodyto subrangos eilutėje, kuriai paruošta išrašyti SF, reikšmę. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendroji tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *etapo suma* + *PVM*. | Joks |

> [!NOTE]
> Kai sukuriama tiekėjo SF eilutė, nurodanti subrangos eilutės etapą, subrangos etapo būsena atnaujinama į **sukurtą** Tiekėjo SF. Tada, patvirtinus tą tiekėjo SF, subrangos eilutės etapo būsena atnaujinama į **patvirtinta** tiekėjo SF.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
