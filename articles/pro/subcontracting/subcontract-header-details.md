---
title: Subrangos sutarčių antraščių informacija
description: Šiame straipsnyje paaiškinamos funkcijos, pateiktos subrangos antraštėje programoje "Project Operations".
author: rumant
ms.date: 09/14/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: ce16b7a968bc7e6904411ae9e021a5ca1839d02e
ms.sourcegitcommit: b2224d1f3c0bd4925d647e6ca3960db81a209521
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/11/2022
ms.locfileid: "9261428"
---
# <a name="header-details-for-subcontracts"></a>Subrangos sutarčių antraščių informacija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Šiame straipsnyje paaiškinamos funkcijos, pateiktos subrangos sutarties antraštėje Dynamics 365 Project Operations.

Projektų vadovui planuojant ir vykdant projektus, jie gali naudoti subrangovus ir produkus bei paslaugas pirkti iš tiekėjų. Kai projekto vadovas turi įsigyti produktų ar paslaugų, „Project Operations“ galima sukurti subrangos sutartį.

Norėdami sukurti subrangos sutartį, atlikite toliau nurodytus veiksmus.

1. Naršymo srityje pasirinkite **Subrangos sutartys**, o puslapyje **Subrangos sutartis** pasirinkite **Nauja**.
2. Įveskite reikiamą informaciją ir pasirinkite **„Įrašyti“**.

    Toliau esančioje lentelėje pateikiama informacija apie laukus **Subrangos sutarties antraštės** puslapyje.

    | Laukas | Aprašymas |Funkcinis poveikis |
    |---|------|---| 
    | Pavadinimas / vardas ir pavardė | Subrangos sutarties pavadinimas. | Visuose subrangos sutarties išskleidžiamuosiuose sąrašuose subrangos sutarties pavadinimas pateikiamas pirmajame stulpelyje, kad būtų lengviau nustatyti subrangos sutartį. | 
    | Aprašymas | Trumpas paslaugų arba produktų, perkamų pagal subrangos sutartį, aprašas. | Nėra |
    | Tiekėjas | Įmonės, iš kurios perkami produktai ir paslaugos, pavadinimas. Šios paskyros įrašo tipas yra **Tiekėjas** arba **Pristatytojas**. | Atsižvelgiant į pasirinktą tiekėją, automatiškai įvedamos numatytosios šių laukų reikšmės:<br/> **• Valiuta** </br> **• Kainoraščiai** </br> **• Mokėjimo sąlygos**</br> **• Mokėjimo adresas**</br> **• Sąskaitų siuntimo adresas**</br> **• Sąskaitų gavėjo vardas** </br>**• Tiekėjo klientų vadovas**|
    | Subrangos sutarties data | Subrangos sutarties sukūrimo data. | Subrangos sutarties data naudojama norint pasirinkti tinkamą pirkimo kainoraštį iš kainoraščių, pridėtų prie susijusio tiekėjo, arba iš projekto parametrų. |
    | Būsenos tipas | Subrangos sutarties būsena. | Būsena nustato, kurioje veiklos proceso vietoje subrangos sutartis yra ir ar galima ją redaguoti. <br/>Reikšmės apima:<br>• **Juodraštis**: subrangos sutartį galima redaguoti. Galite redaguoti tik subrangos sutartis, kurių būsena yra **Juodraštis**.<br/>• **Patvirtinta**: derybos su tiekėju baigtos ir subrangos sutartis patvirtinta pristatyti. <br/>• **Uždaryta**: subrangos sutarties pristatymas baigtas.<br/>• **Atšaukta**: subrangos sutartis buvo atšaukta ir nesuplanuota jokio pristatymo.  | 
    | Valiuta | Valiuta, kuria sumokama už perkamus produktus ir paslaugas. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos, tačiau ją galima pakeisti. | Subrangos sutarties valiuta naudojama norint pasirinkti pirkimo kainoraštį iš kainoraščių, pridėtų prie susijusio tiekėjo, arba iš projekto parametrų. Kainoraščių kita valiuta negalima susieti su subrangos sutartimi. Laiko sąnaudos, išlaidos ir medžiagos, kurias tiekėjo ištekliai pateikia iš šios subrangos sutarties, projekte įrašomi šia valiuta. Kai įrašomas subrangos sutarties įrašas, negalima pakeisti subrangos sutarties valiutos.|
    | Sutartį sudarantis vienetas | Pirkimo arba subrangos sutartį su tiekėju sudarančios įmonės padalinys. | Nėra |
    | Mokėjimo sąlygos | Mokėjimo sąlygos pagal tiekėjo sąskaitas faktūras, išrašytas dėl šios subrangos sutarties. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Apmokėjimo sąlygos iš subrangos sutarties nukopijuojamos į visas tiekėjo sąskaitas faktūras, susijusias su šia subrangos sutartimi. Mokėjimo sąlygas galima atnaujinti, jeigu subrangos sutarties būsena yra **Juodraštis**. | 
    | Mokėjimo adresas | Tiekėjo, kuriam turi būti siunčiami mokėjimai, adresas. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Mokėjimo adresas iš subrangos sutarties nukopijuojamas kaip mokėjimo adresas į visas tiekėjo sąskaitas faktūras, sukuriamas šiai subrangos sutarčiai. Mokėjimo adresą galima atnaujinti, jeigu subrangos sutarties būsena yra **Juodraštis**.|
    | Sąskaitų gavėjo vardas | Tiekėjo įmonės asmens, kuris išsiųs sąskaitą faktūrą, vardas ir pavardė arba skyrius, išsiųsiantis sąskaitą faktūrą. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | **Sąskaitų gavėjo vardas** reikšmė iš subrangos sutarties nukopijuojama į visas tiekėjo sąskaitas faktūras, susijusias su šia subrangos sutartimi. Šį lauką galima atnaujinti, jeigu subrangos sutarties būsena yra **Juodraštis**.|
    | Sąskaitų siuntimo adresas | Adresas, naudojamas tiekėjo sąskaitose faktūrose. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. | Šis adresas yra „sąskaita faktūra iš“ adresas tiekėjo sąskaitose faktūrose, sukurtose šiai subrangos sutarčiai. |
    | Tarpinė suma | Jei subrangos sutartyje nėra eilučių, įveskite tarpinę užsakymo sumą prieš apskaičiuojant mokesčius. Jei subrangos sutartyje eilučių yra, šis laukas yra skirtas tik skaityti. Rodoma suma yra tarpinė suma iš visų subrangos sutarties eilučių. | Nėra |
    | Bendra mokesčių suma | Jei subrangos sutartyje nėra eilučių, įveskite bendruosius šios subrangos sutarties mokesčius. Jei subrangos sutartyje eilučių yra, šis laukas yra skirtas tik skaityti. Rodoma suma yra mokesčių suma iš visų subrangos sutarties eilučių. | Nėra |
    | Bendra suma | Šiame apskaičiuotajame lauke pateikiama bendra subrangos sutarties suma įtraukus mokesčius. | Nėra |
    | Patvirtinimo data | Subrangos sutarties patvirtinimo data. | Nėra |
    | Užklausą pateikė | Pagal numatytuosius nustatymus šis laukas nustatomas kaip vartotojo, kuris sukuria subrangos sutartį, vardas. Tačiau subrangos sutarties kūrėjas gali pakeisti reikšmę ir nurodyti asmenį, kurio vardu sukuria subrangos sutartį. | Nėra |
    | Tiekėjo klientų vadovas | Tiekėjo kliento pirminio kontakto vardas ir pavardė. Numatytoji reikšmė automatiškai įvedama iš tiekėjo sąskaitos įrašo. Kitą kontaktą galite pažymėti kaip subrangos sutarties tiekėjo klientų vadovą. | Galite nustatyti el. pašto įspėjimus, kurie praneš kontaktui apie subrangos sutarties pokyčius dėl kainų derybų. |
