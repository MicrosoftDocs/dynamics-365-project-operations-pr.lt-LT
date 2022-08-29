---
title: Tiekėjo sąskaitos faktūros etapų eilutės
description: Šiame straipsnyje paaiškinama, kaip sukurti tiekėjo SF eilutes, skirtas svarbiems įvykiams subrangos sutartyje.
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

Tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations tiekėjo SF eilutėse gali būti tiekėjo SF eilutės, skirtos etapams, apibrėžtiems subrangos eilutėje. Projektų vadovai gali naudoti tiekėjo SF eilutes riboženkliams, kad įrašytų paslaugų, kurios perkamos kaip tarpinėmis reikšmėmis pagrįstos išlaidos, patirtas dėl projektui įsigytų paslaugų ar produktų, išlaidas.

Tiekėjo SF eilutėse, skirtose riboženkliams, visada turi būti nurodytas subrangos eilutė, kurioje yra atsiskaitymo už fiksuotą kainą metodas. Kai tiekėjo SF eilutė, skirta riboženkliams, nurodo subrangos liniją, projektų vadovai galės susieti ir patikrinti pagrindines laiko, išlaidų ar medžiagų, nurodančių tą subrangos liniją, išlaidas arba medžiagas, nurodančias tą subrangos liniją, su tarpiniu įvykiu, kuriam tiekėjas išrašo SF.

Šioje lentelėje pateikiama informacija apie tiekėjo SF eilučių laukus, skirtus riboženkliams.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas paslaugų, kurioms tiekėjas išrašo SF sf tiekėjo SF eilutėje, aprašas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią paslaugos iš pradžių buvo užsakytos. | Tiekėjo SF pasirinkus subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali būti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos linija | Subrangos linija, pagal kurią buvo užsakytos paslaugos. Subrangos linijų, kurias galima pasirinkti, sąrašas apima tik pasirinktos subrangos linijas. | Kai tiekėjo SF eilutėje pasirenkama gairių tiekėjo SF eilutė, **laukai Vaidmenų** ir operacijų kategorija **ir** su produktu susiję laukai yra nesvarbūs ir negalimi. Laukai **Kiekis**, **Vienetas** ir **Vienetas grupės** taip pat nėra aktualūs tiekėjo SF eilutėms, pagrįstoms tiekėjo SF eilutėmis. |
| Operacijos data | Data, kada tiekėjo SF eilutės faktinės išlaidos bus įrašytos į projektą. | Joks |
| Operacijos klasė | Pasirinkite **Etapas**, kad įrašytumėte užbaigto etapo tiekėjo SF, kuri buvo apibrėžta subrangos eilutėje, tiekėjo SF. | Joks |
| Etapas | Pasirinkite riboženklį, apibrėžtą susijusioje subrangos eilutėje, kuri pažymėta kaip **Paruošta sf**. | Subrangos eilutės gaires, kurių būsena **paruošta sf**, galima pasirinkti tiekėjo SF eilutėje. |
| Project | Projekto, kuriame buvo naudojamos paslaugos, kurioms išrašomos sąskaitos faktūros, pavadinimas. | Šis laukas yra būtinas ir jo negalima palikti tuščio. |
| Užduotis | Projekto užduoties, kuriai buvo naudojamos paslaugos, kurioms išrašomos sąskaitos faktūros, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali susieti tiekėjo SF eilutę su operacijų klase susijusioje subrangos eilutėje, kuri įrašoma atliekant bet kurią projekto užduotį. Jei tiekėjo SF eilutėje nenurodyta subrangos eilutė, o šis laukas paliekamas tuščias, faktinės išlaidos, kurias sukuria tiekėjo SF eilutė, nebus susietos su jokiais neįrašytais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, gali nepavykti išrašyti išlaidų sąskaitos faktūros galutiniam klientui. |
| Etapo suma | Įveskite riboženklio reikšmę, apibrėžtą subrangos eilutėje, kuri yra parengta apmokėti sąskaitą faktūrą. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendra tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *tarpinė suma* + *PVM*. | Joks |

> [!NOTE]
> Kai sukuriama tiekėjo SF eilutė, nurodanti subrangos eilutės riboženklį, subrangos etapo būsena atnaujinama į **sukurtą** tiekėjo SF. Tada, kai ta tiekėjo SF patvirtinama, subrangos eilutės etapo būsena atnaujinama į **Patvirtinta** tiekėjo SF.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
