---
title: Tiekėjo sąskaitų faktūrų antraštės informacija
description: Šiame straipsnyje aprašomos funkcijos, nurodytos tiekėjo sąskaitos faktūros antraštėje „Microsoft Dynamics 365 Project Operations“.
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

Šiame straipsnyje aprašomos funkcijos, nurodytos tiekėjo sąskaitos faktūros antraštėje „Microsoft Dynamics 365 Project Operations“.

Kaip projektų vadovo projektų planavimą ir vykdymą, jie gali naudoti subrangovus ir produkus bei paslaugas pirkti iš tiekėjų. Vykdant projektą išlaidos patiriamos dėl paslaugų, med iagų ir išlaidų kategorijų, kurios su pardavėjais susijusios su tomis išlaidų kategorijomis. Tiekėjams išrašo šių išlaidų sąskaitą faktūrą projektams sukurdami tiekėjo sąskaitas faktūras.

Šioje lentelėje pateikiama informacija apie laukus, esančius tiekėjo sąskaitos antraštėje „Project Operations“.

| Laukas | Aprašą | Funkcinis poveikis |
| --- | --- | --- |
| Pavadinimą | Tiekėjo sąskaitos faktūros pavadinimas. | Visuose tiekėjo sąskaitos faktūros išskleidžiamuosiuose sąrašuose sąskaitos faktūros pavadinimas pateikiamas pirmajame stulpelyje, kad būtų lengviau nustatyti sąskaitą faktūrą. Pagal numatytuosius nustatymus, kai tiekėjo sąskaita faktūra sukuriama naudojant susąrangą, **pardavėjo** sąskaitos faktūros pavadinimo laukas nustatomas kaip reikšmė, kurią sudaro išsamūs ir dabartinės datos pavadinimas. |
| Aprašą | Trumpas paslaugų arba produktų, perkamų pagal tiekėjo sąskaitą faktūrą, aprašas. | Joks |
| Tiekėjas | Įmonės, kuri išrašo sąskaitą faktūrą perkamiems produktams ir paslaugoms, pavadinimas. Ši įmonė turi būti ataskaitos įrašas, kuris turi sąntykio tipą tarp **Tiekėjo** ar **Pardavėjo**. | <p>Atsižvelgiant į pasirinktą tiekėją, automatiškai įvedamos numatytosios šių laukų reikšmės:</p><ul><li>Valiuta</li><li>Kainoraščiai</li><li>Mokėjimo sąlygos</li><li>Mokėjimo adresas</li></ul> |
| Subrangos sutartis | Nuoroda į tiekėjo sąskaitos faktūros indą. | <p>Atsižvelgiant į pasirinktą subrangos tiekėją, automatiškai įvedamos numatytosios šių laukų reikšmės:</p><ul><li>Valiuta</li><li>Kainoraščiai</li><li>Mokėjimo sąlygos</li><li>Mokėjimo adresas</li></ul><p>Pagal numatytuosius nustatymus tiekėjo sąskaitos faktūros eilutėse įvedamas ir ten jo keisti negalima.</p> |
| Sąskaitos faktūros data | Faktinių išlaidų data, kuri bus sukurta patvirtinus tiekėjo sąskaitą faktūrą. | Subrangos sutarties data naudojama norint pasirinkti tinkamą pirkimo kainoraštį iš kainoraščių, pridėtų prie susijusio tiekėjo, arba iš projekto parametrų. |
| Būsenos tipas | Tiekėjo sąskaitos būsena. | <p>Būsena nustato, kurioje tiekėjo sąskaitos vietoje subrangos sutartis yra ir ar galima ją redaguoti. Čia pateikiame kelias prieinamas vertes:</p><ul><li>**Juodraštis**: tiekėjo sąskaitą galima redaguoti.</li><li>**Patvirtinta** – tiekėjo sąskaita faktūra buvo patvirtinta ir patvirtinta. Tiekėjo sąskaitos šioje būsenoje redaguojamos ar naikinamos būti negali.</li><li>**Procesas** – peržiūrima tiekėjo sąskaita faktūra. Tiekėjo sąskaitos šioje būsenoje redaguojamos ar naikinamos būti negali.</li><li>**Atšaukta** – tiekėjo sąskaita faktūra buvo atšaukta. Tiekėjo sąskaitos šioje būsenoje redaguojamos ar naikinamos būti negali.</li></ul> |
| Valiuta | Valiuta, kuria išrašomi tiekėjo sąskaitos faktūros produktų ir aptarnavimo sąskaitos faktūros produktai ir aptarnavimas. | Tiekėjo sąskaitoje faktūroje, kuri nurodo persodinę, pagal numatytuosius nustatymus konvertuojama valiuta įvedama kaip tiekėjo sąskaitos faktūros valiuta. Tiekėjo sąskaitoje faktūroje, kuri neturi nuorodos į susegtinį, numatytoji reikšmė įvedama iš tiekėjo kliento įrašo ir gali būti pakeista. Įrašius tiekėjo sąskaitą faktūrą, valiutos redaguoti nebegalima. |
| Sutartį sudarantis vienetas | Įmonės skyrius, atsakingas už paslaugų ir (arba) produktų gavimą iš tiekėjo. | Joks |
| Mokėjimo sąlygos | Mokėjimo sąlygos pagal tiekėjo sąskaitas faktūras, išrašytas dėl šios subrangos sutarties. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Apmokėjimo sąlygos iš subrangos sutarties nukopijuojamos į visas tiekėjo sąskaitas faktūras, susijusias su šia subrangos sutartimi. Mokėjimo sąlygas galima atnaujinti, jeigu tiekėjo SF būsena yra **Juodraštis**. |
| Mokėjimo adresas | Tiekėjo, kuriam turi būti siunčiami mokėjimai, adresas. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Mokėjimo adresas iš subrangos sutarties nukopijuojamas kaip mokėjimo adresas į visas tiekėjo sąskaitas faktūras, sukuriamas šiai subrangos sutarčiai. Mokėjimo adresą galima atnaujinti, jeigu tiekėjo SF būsena yra **Juodraštis**. |
| Tarpinė suma | Jei tiekėjo SF nėra eilučių, įveskite tarpinę SF sumą prieš apskaičiuojant mokesčius. Jei tiekėjo SF eilučių yra, šis laukas yra skirtas tik skaityti. Šiuo atveju, rodoma suma yra tarpinė suma iš visų tiekėjo SF eilučių. | Joks |
| Bendra mokesčių suma | Jei tiekėjo SF nėra eilučių, įveskite tarpinę mokeesčių sumą pagal subrangą. Jei tiekėjo SF eilučių yra, šis laukas yra skirtas tik skaityti. Šiuo atveju, rodoma suma yra tarpinė suma visų mokesčių suma iš visų tiekėjo SF eilučių. | Joks |
| Bendra suma | Šiame apskaičiuotajame lauke pateikiama bendra tiekėjo SF suma įtraukus mokesčius. | Joks |

> [!NOTE]
> Įrašius tiekėjo sąskaitą faktūrą, šių laukų tiekėjo sąskaitoje faktūroje pakeisti negalima: **Tiekėjas**, **Subrangos sutartis**, **Valiuta**, **Sutarties šalis** ir **Mokėjimo sąlygos**. Jei reikia pakeisti šiuos laukus tiekėjo sąskaitoje faktūroje, turite panaikinti tiekėjo sąskaitą faktūrą ir sukurti naują tiekėjo sąskaitą faktūrą.

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
