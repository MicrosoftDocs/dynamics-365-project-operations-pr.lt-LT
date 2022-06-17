---
title: Tiekėjo sąskaitų faktūrų antraštės informacija
description: Šiame straipsnyje paaiškinamos funkcijos, pateiktos "Microsoft" tiekėjo SF antraštėje Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 95f84f2d2a357abbd8d507705412a0434b44f658
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8929868"
---
# <a name="header-details-for-vendor-invoices"></a>Tiekėjo sąskaitų faktūrų antraštės informacija

[!include [banner](../../includes/dataverse-preview.md)]

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinamos funkcijos, pateiktos "Microsoft" tiekėjo SF antraštėje Dynamics 365 Project Operations.

Kadangi projektų vadovai planuoja ir vykdo projektus, jie gali samdyti subrangovus ir pirkti produktus bei paslaugas iš tiekėjų. Projekto vykdymo metu išlaidos patiriamos iš paslaugų, medžiagų ir išlaidų kategorijų, kurios perkamos pagal subrangos sutartis su pardavėjais. Tiekėjai išrašo SF šioms išlaidoms projektams kurdami tiekėjo SF.

Šioje lentelėje pateikiama informacija apie "Project Operations" tiekėjo SF antraščių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF pavadinimas. | Visuose tiekėjo SF išplečiamuosiuose sąrašuose tiekėjo SF pavadinimas pateikiamas pirmame stulpelyje, kad padėtų identifikuoti tiekėjo SF. Pagal numatytuosius nustatymus, kai tiekėjo SF sukuriama iš subrangos sutarties, **tiekėjo SF laukas Pavadinimas** nustatomas kaip vertė, kurią sudaro subrangos sutarties pavadinimas ir dabartinė data. |
| Aprašą | Trumpas paslaugų ir produktų, kuriems tiekėjo SF išrašyta SF, aprašymas. | Joks |
| Tiekėjas | Įmonės, kuri išrašo sąskaitas už produktus ir paslaugas, pavadinimas. Ši įmonė turėtų būti sąskaitos įrašas, kurio ryšio tipas yra **Tiekėjas** arba **Tiekėjas**. | <p>Pagal pasirinktą tiekėją numatytosios vertės automatiškai įvedamos į šiuos laukus:</p><ul><li>Valiuta</li><li>Kainoraščiai</li><li>Mokėjimo sąlygos</li><li>Mokėjimo adresas</li></ul> |
| Subrangos sutartis | Nuoroda į tiekėjo SF subrangos sutartį. | <p>Remiantis pasirinkta subrangos sutartimi, numatytosios vertės automatiškai įvedamos į šiuos laukus:</p><ul><li>Valiuta</li><li>Kainoraščiai</li><li>Mokėjimo sąlygos</li><li>Mokėjimo adresas</li></ul><p>Tiekėjo SF antraštėje pasirinkta subrangos sutartis pagal numatytuosius nustatymus įvedama tiekėjo SF eilutėse ir jos ten keisti negalima.</p> |
| Sąskaitos faktūros data | Faktinių išlaidų, kurios bus sukurtos patvirtinus tiekėjo SF, data. | SF data taip pat naudojama norint pasirinkti tinkamą pirkimo kainoraštį iš kainoraščių, pridėtų prie susijusio tiekėjo, arba iš projekto parametrų. |
| Būsenos tipas | Tiekėjo SF būsena. | <p>Būsena nustato, kur tiekėjo SF yra verslo procese ir ar ją galima redaguoti. Štai keletas galimų reikšmių:</p><ul><li>**Juodraštis** – tiekėjo SF galima redaguoti.</li><li>**Patvirtinta** – tiekėjo SF buvo patikrinta ir patvirtinta. Šios būsenos tiekėjo SF redaguoti ar panaikinti negalima.</li><li>**Vykdoma** – peržiūrima tiekėjo SF. Šios būsenos tiekėjo SF galima redaguoti, tačiau jų panaikinti negalima.</li><li>**Atšaukta** – tiekėjo SF atšaukta. Šios būsenos tiekėjo SF redaguoti ar panaikinti negalima.</li></ul> |
| Valiuta | Valiuta, kuria tiekėjas išrašo TIEKĖJO SF produktams ir paslaugoms tiekėjo SF. | Tiekėjo SF, nurodančioje subrangos sutartį, subrangos sutarties valiuta pagal numatytuosius nustatymus įvedama kaip tiekėjo SF valiuta. Tiekėjo SF, kuri nenurodo subrangos sutarties, numatytoji vertė įvedama iš tiekėjo sąskaitos įrašo ir gali būti pakeista. Įrašius tiekėjo SF, valiutos redaguoti nebegalima. |
| Sutartį sudarantis vienetas | Įmonės padalinys, atsakingas už paslaugų ir (arba) produktų gavimą iš tiekėjo. | Joks |
| Mokėjimo sąlygos | Išrašytų tiekėjo SF mokėjimo sąlygos. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Mokėjimo sąlygos iš subrangos sutarties nukopijuojamos į visas tiekėjo SF, susijusias su subrangos sutartimi. Mokėjimo sąlygas galima atnaujinti, jei tiekėjo SF būsena **yra Juodraštis**. |
| Mokėjimo adresas | Tiekėjo, kuriam turi būti siunčiami mokėjimai, adresas. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Mokėjimo adresas iš subrangos sutarties nukopijuojamas kaip mokėjimo adresas į visas tiekėjo SF, sukurtas tai subrangos sutarčiai. Mokėjimo adresą galima atnaujinti, jei tiekėjo SF būsena **yra Juodraštis**. |
| Tarpinė suma | Jei tiekėjo SF nėra eilučių, įveskite SF tarpinę sumą prieš mokesčius. Jei tiekėjo SF yra eilučių, šis laukas yra tik skaitomas. Tokiu atveju rodoma suma yra tarpinė suma iš visų tiekėjo SF eilučių. | Joks |
| Iš viso mokesčių | Jei tiekėjo SF neturi eilučių, antrinėje sutartyje įveskite bendruosius mokesčius. Jei tiekėjo SF yra eilučių, šis laukas yra tik skaitomas. Tokiu atveju rodoma suma yra mokesčių sumų suma iš visų tiekėjo SF eilučių. | Joks |
| Bendra suma | Šiame apskaičiuotame lauke rodoma bendroji tiekėjo SF suma, įtraukus mokesčius. | Joks |

> [!NOTE]
> Įrašius tiekėjo SF, šių tiekėjo SF laukų keisti negalima: Tiekėjas **, Subrangos sutartis**, **Valiuta**, **Sutarties** vienetas **ir** Mokėjimo sąlygos **.** Jei reikia atlikti kokius nors šių tiekėjo SF laukų pakeitimus, turite panaikinti tiekėjo SF ir sukurti naują tiekėjo SF.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
