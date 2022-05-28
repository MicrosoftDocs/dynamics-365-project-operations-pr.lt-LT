---
title: Produktų tiekėjo SF eilutės
description: Šioje temoje paaiškinama, kaip įrašyti produktų tiekėjo SF eilutes ir naudoti skirtingus laukus produktų pirkimams iš tiekėjų įrašyti.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: af078cd4392f8353b509db2dc48dc5237b8ee275
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8599188"
---
# <a name="vendor-invoice-lines-for-products"></a>Produktų tiekėjo SF eilutės

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Tiekėjo SF programoje "Microsoft" Dynamics 365 Project Operations gali būti produktų tiekėjo SF eilutės (dar vadinamos medžiagomis). Projektų vadovai gali naudoti produktų tiekėjo SF eilutes, kad įrašytų projektuose įsigytų produktų savikainą.

Produktų tiekėjo SF eilutės gali arba negali nurodyti subrangos eilutės medžiagoms. Jei produktų tiekėjo SF eilutė nurodo subrangos sutartį, projektų vadovai galės suderinti ir patikrinti produktus, kuriems tiekėjo SF eilutėje išrašoma SF eilutė, su įsigytų produktų, kuriuos įrašo ir patvirtina projektų vadovai, naudojimu.

Šioje lentelėje pateikiama informacija apie produktų tiekėjo SF eilučių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF eilutės pavadinimas, padedantis identifikuoti. | Šis pavadinimas bus rodomas kaip pirmasis stulpelis visose peržvalgose, pagrįstose tiekėjo SF eilutėmis. |
| Aprašą | Trumpas produktų, kuriems tiekėjas tiekėjo SF eilutėje išrašo SF, aprašymas. | Joks |
| Subrangos sutartis | Subrangos sutartis, pagal kurią produktai iš pradžių buvo užsakyti. | Pasirinkus tiekėjo SF subrangos sutartį, visos tiekėjo SF eilutės paveldės tą pasirinkimą. Tiekėjo SF negali turėti tiekėjo SF eilučių, nurodančių skirtingas subrangos sutartis. |
| Subrangos eilutė | Subrangos eilutė, pagal kurią produktai buvo užsakyti. Subrangos eilučių, kurias galima pasirinkti, sąrašas apsiriboja pasirinkto subrangos sutarties eilutėmis. | Kai produktų tiekėjo SF eilutėje pasirenkama subrangos eilutė, iš atitinkamų subrangos eilutės laukų **Projektas**, **Užduotis** ir **Produktas** vertės įvedamos iš atitinkamų subrangos eilutės laukų. Jei pasirinktos subrangos eilutės laukuose **Projektas**, **Užduotis** ir **Produktas** yra verčių, atitinkamų tiekėjo SF eilutės laukų vertės negali skirtis nuo šių verčių. |
| Operacijos data | Data, kai tiekėjo SF eilutės faktinė savikaina bus įrašyta į projektą. | Joks|
| Operacijos klasė | Kai produktams išrašoma SF, šis laukas turi būti nustatytas kaip **Medžiaga**. | Vertė **Medžiaga** nurodo, kad tiekėjo SF eilutė naudojama įsigytų medžiagų SF sumai įrašyti. |
| Project | Projekto, kuriame buvo naudojami produktai, kuriems išrašyta SF, pavadinimas. | Šis laukas yra būtinas ir negali būti paliktas tuščias. |
| Užduotis | Projekto užduoties, kuriai buvo naudojami produktai, kuriems išrašyta SF, pavadinimas. Šis laukas galimas tik pasirinkus projektą. Projekto užduoties pasirinkimas yra neprivalomas. | Jei šis laukas paliekamas tuščias, projekto vadovas gali suderinti tiekėjo SF eilutę su įsigytu produktu, kuris naudojamas bet kuriai projekto užduočiai. Jei tiekėjo SF eilutė nenurodo subrangos eilutės ir šis laukas paliekamas tuščias, tiekėjo SF eilutėje sukurta faktinė savikaina nebus susieta su jokiais neapmokėtais pardavimo faktiniais duomenimis. Tokiu atveju, jei nustatytas užduotimis pagrįstas atsiskaitymas, išlaidoms nebus galima išrašyti SF galutiniam vartotojui. |
| Pasirinkti produktą | Pasirinkite, ar produktas, kuriam išrašyta SF, yra esamas katalogo produktas, ar įrašymo produktas. | Numatytoji vertė įvedama iš subrangos eilutės, kai pasirenkama subrangos eilutė. |
| Produktas | Pasirinkite produktą iš katalogo. Jei produktas yra įrašymo produktas, įveskite produkto pavadinimą. | Šis laukas naudojamas esamų produktų numatytosioms pirkimo kainoms įvesti. |
| Kiekis | Įveskite medžiagos kiekį, kuriam tiekėjas išrašo SF šioje SF eilutėje. | Joks |
| Vienetų grupė | Pasirinkite vieneto, kuriame išreiškiamas kiekis, kuriam išrašyta SF, vienetų grupę. | Joks |
| Vienetas | Numatytoji vertė yra pasirinktos vienetų grupės bazinis vienetas. Galite pakeisti šią vertę, kad galėtumėte mokėti bet kuriuo pasirinktos vienetų grupės vienetu. | Produkto **ir vieneto** **verčių derinys bus naudojamas kaip numatytoji** arba apskaičiuota tiekėjo SF eilutės lauko Vieneto kaina **vertė**. |
| Vieneto kaina | Numatytoji vieneto kaina naudoja produkto **ir** vieneto **verčių** derinį iš projekto kainoraščio, kuris taikomas tiekėjo SF eilutės operacijos datai. | Joks |
| Tarpinė suma | Šis tik skaitomas laukas apskaičiuojamas kaip *Kiekio*&times;*vieneto kaina*, jei vertės įvedamos ir **į lauką Kiekis**, ir į lauką Vieneto **kaina.** Jei vienas arba abu šie laukai yra tušti, šiame lauke galite įvesti vertę. | Joks |
| PVM | Įveskite PVM sumą. | Joks |
| Bendra suma | Bendroji tiekėjo SF eilutės suma, įskaitant mokesčius. Šis laukas apskaičiuojamas kaip *tarpinės sumos* + *PVM*. | Joks |

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
