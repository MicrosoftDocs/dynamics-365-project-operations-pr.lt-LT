---
title: Tiekėjo sąskaitų faktūrų antraštės informacija
description: Šiame straipsnyje paaiškinamos funkcijos, pateiktos tiekėjo SF antraštėje programoje "Microsoft"Dynamics 365 Project Operations.
author: rumant
ms.date: 03/25/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: d575ebe44e45411e1009c64e9b575777b741322f
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261672"
---
# <a name="header-details-for-vendor-invoices"></a>Tiekėjo sąskaitų faktūrų antraštės informacija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinamos funkcijos, pateiktos tiekėjo SF antraštėje programoje "Microsoft"Dynamics 365 Project Operations.

Kai projektų vadovai planuoja ir vykdo projektus, jie gali samdyti subrangovus ir pirkti produktus bei paslaugas iš tiekėjų. Projekto vykdymo metu išlaidos patiriamos dėl paslaugų, medžiagų ir išlaidų kategorijų, kurios perkamos subrangos sutartimis su tiekėjais. Tiekėjai išrašo sąskaitas faktūras už šias išlaidas projektams kurdami tiekėjo SF.

Šioje lentelėje pateikiama informacija apie "Project Operations" tiekėjo SF antraščių laukus.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo SF pavadinimas. | Visuose išplečiamuosiuose tiekėjo SF sąrašuose tiekėjo SF pavadinimas pateikiamas pirmame stulpelyje, kad būtų lengviau identifikuoti tiekėjo SF. Pagal numatytuosius parametrus, kai tiekėjo SF sukuriama iš subrangos sutarties, **tiekėjo SF laukas Pavadinimas** nustatomas kaip reikšmė, kurią sudaro subrangos pavadinimas ir dabartinė data. |
| Aprašą | Trumpas paslaugų ir produktų, kuriems išrašomos tiekėjo SF, aprašas. | Joks |
| Tiekėjas | Įmonės, kuri išrašo sąskaitas faktūras už produktus ir paslaugas, pavadinimas. Ši įmonė turėtų būti abonemento įrašas, turintis tiekėjo arba tiekėjo santykių **tipą**.**·** | <p>Atsižvelgiant į pasirinktą tiekėją, numatytosios reikšmės automatiškai įvedamos į šiuos laukus:</p><ul><li>Valiuta</li><li>Kainoraščiai</li><li>Mokėjimo sąlygos</li><li>Mokėjimo adresas</li></ul> |
| Subrangos sutartis | Tiekėjo SF nuoroda į subrangos sutartį. | <p>Atsižvelgiant į pasirinktą subrangos sutartį, numatytosios reikšmės automatiškai įvedamos į šiuos laukus:</p><ul><li>Valiuta</li><li>Kainoraščiai</li><li>Mokėjimo sąlygos</li><li>Mokėjimo adresas</li></ul><p>Tiekėjo SF antraštėje pasirinkta subrangos sutartis pagal numatytuosius nustatymus įvedama tiekėjo SF eilutėse ir ten negali būti keičiama.</p> |
| Sąskaitos faktūros data | Faktinių išlaidų, kurios bus sukurtos patvirtinus tiekėjo SF, data. | Sąskaitos faktūros data taip pat naudojama norint pasirinkti tinkamą pirkimo kainoraštį iš kainoraščių, pridėtų prie susijusio tiekėjo, arba iš projekto parametrų. |
| Būsenos tipas | Tiekėjo SF būsena. | <p>Būsena nustato, kur tiekėjo SF yra verslo procese ir ar ją galima redaguoti. Štai keletas galimų reikšmių:</p><ul><li>**Juodraštis** – tiekėjo SF galima redaguoti.</li><li>**Patvirtinta** – tiekėjo SF buvo patikrinta ir patvirtinta. Šios būsenos tiekėjo sf negalima redaguoti ar ištrinti.</li><li>**Proceso metu** – peržiūrima tiekėjo SF. Šios būsenos tiekėjo sf galima redaguoti, bet jų panaikinti negalima.</li><li>**Atšaukta** – tiekėjo SF buvo atšaukta. Šios būsenos tiekėjo sf negalima redaguoti ar ištrinti.</li></ul> |
| Valiuta | Valiuta, kuria tiekėjas išrašo sf už tiekėjo SF nurodytus produktus ir paslaugas. | Tiekėjo SF, kuri nurodo subrangos sutartį, subrangos valiuta pagal numatytuosius nustatymus įvedama kaip tiekėjo SF valiuta. Tiekėjo SF, kuri nenurodo subrangos sutarties, numatytoji reikšmė įvedama iš tiekėjo abonemento įrašo ir gali būti pakeista. Įrašius tiekėjo SF, valiutos redaguoti nebegalima. |
| Sutartį sudarantis vienetas | Įmonės padalinys, atsakingas už paslaugų ir (arba) produktų gavimą iš tiekėjo. | Joks |
| Mokėjimo sąlygos | Išrašomų tiekėjo SF mokėjimo sąlygos. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Mokėjimo sąlygos iš subrangos sutarties nukopijuojamos į visas tiekėjo sf, susijusias su subrangos sutartimi. Mokėjimo sąlygas galima atnaujinti, jei tiekėjo SF būsena yra **Juodraštis**. |
| Mokėjimo adresas | Tiekėjo, kuriam turi būti siunčiami mokėjimai, adresas. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Mokėjimo adresas iš subrangos sutarties nukopijuojamas kaip mokėjimo adresas į visas tiekėjo sf, sukurtas tai subrangos sutarčiai. Mokėjimo adresą galima atnaujinti, jei tiekėjo SF būsena yra **Juodraštis**. |
| Tarpinė suma | Jei tiekėjo SF nėra eilučių, įveskite tarpinę SF sumą prieš mokesčius. Jei tiekėjo SF yra eilučių, šis laukas yra tik skaitomas. Tokiu atveju rodoma suma yra tarpinė suma iš visų tiekėjo SF eilučių. | Joks |
| Iš viso mokesčio | Jei tiekėjo SF eilučių nėra, įveskite visus subrangos sutarties mokesčius. Jei tiekėjo SF yra eilučių, šis laukas yra tik skaitomas. Tokiu atveju rodoma suma yra mokesčių sumų suma iš visų tiekėjo SF eilučių. | Joks |
| Bendra suma | Šiame apskaičiuotajame lauke rodoma bendra tiekėjo SF suma po to, kai įtraukiami mokesčiai. | Joks |

> [!NOTE]
> Įrašius tiekėjo SF, šių tiekėjo SF laukų keisti negalima: **Tiekėjo, Subrangos**, **Valiutos**, **Sutarties** vieneto **ir** Mokėjimo **sąlygų**. Jei reikia keisti šiuos tiekėjo SF laukus, turite panaikinti tiekėjo SF ir sukurti naują tiekėjo SF.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
