---
title: Kelių klientų tvarkymas projekto sutartyse – „Lite“ versija
description: Šioje temoje pateikiama informacija apie kelių klientų tvarkymą projekto sutartyse.
author: rumant
ms.date: 10/27/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 31a12e44353160dde851e2b9b06148a31fbeb167
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6002864"
---
# <a name="manage-multiple-customers-on-project-contracts---lite"></a>Kelių klientų tvarkymas projekto sutartyse – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

„Dynamics 365 Project Operations“ projekto sutartyse palaikomas scenarijus, kai sutartinis susitarimas apima kelis sandorį finansuojančius klientus. Puslapio **Projekto sutartis** skirtuke **Suvestinė** yra laukas **Klientas**. Šiame lauke nurodomas pirminis sandorio klientas. Kitus sandorio klientus galima nustatyti puslapio **Projekto sutartis** skirtuke **Klientai**.

Visi sutarties klientai, nurodyti projekto sutartyje, nustatomi kaip numatytieji sutarties eilutės klientai visose naujose projektu pagrįstose sutarties eilutėse, kurios sukuriamos projekto sutarčiai. Esamos projektu pagrįstos sutarties eilutės nebus pakeistos naujų sutarties klientų įrašais, kai sukuriami nauji įrašai.

Produktu pagrįstos sutarties eilutės automatiškai susiejamos su pirminiu klientu.

Sutarties klientus ir sutarties eilutės klientus galima įtraukti, atnaujinti arba panaikinti bet kuriuo metu prieš laimint sutartį.

## <a name="primary-customer"></a>Pirminis klientas

Klientas, nurodytas projekto sutarties skirtuke **Suvestinė** kaip potencialus klientas, yra pirminis sutarties klientas. Bandant panaikinti pirminį klientą iš sutarties klientų sąrašo, pateikiamas klaidos pranešimas, kad sutarties pirminio kliento įrašo panaikinti negalima.

Pirminio kliento negalima atnaujinti naudojant sutarties klientų sąrašą. Vietoj to, pakeiskite potencialų klientą sutarties skirtuke **Suvestinė**. Atnaujinus šį lauką puslapyje **Sutarties suvestinė** naujas klientas įtraukiamas kaip naujas sutarties klientas, kuriam nustatoma žymė **Pirminis**. Ankstesnis pirminis klientas vis tiek bus sutarties klientas.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Sutarties kliento įrašo kūrimas, naujinimas arba panaikinimas

Sutarties klientą galima sukurti, atnaujinti arba panaikinti puslapio **Projekto sutartis** skirtuke **Klientai**. Toliau esančioje lentelėje pateikti laukai yra projekto sutarties kliento įraše, į kuriuos reikia atsižvelgti dirbant su sutartimi.

| Laukas | Vieta | Aprašo | Tolesnis poveikis |
| --- | --- | --- | --- |
| **Klientas** | Tinklelį galima redaguoti skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Išvardinkite visus aktyvius klientus. Šis laukas užrakinamas sukūrus įrašą. Naudojamas norint atnaujinti klientą, panaikinti įrašą ir sukurti jį iš naujo. Jei įrašėte bet kokius faktinius duomenis arba jei sutarties kliento įrašas yra pirminis klientas, įrašo panaikinti negalima. | Sutarties klientai nukopijuojami kaip sutarties eilutės klientai, kai sukuriama sutarties eilutė. |
| **Atsiskaitymo išskaidymo procentas** | Tinklelį galima redaguoti skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Nurodo kiekvienos pardavimo operacijos, už kurią neišrašyta sąskaita faktūra, procentinę dalį, kuri priskirta šios sutarties klientui. | Nukopijuojama į naujas sutarties eilutes ir į projekto sutarties eilutės klientus naujose projekto sutarties eilutėse. |
| **Sąskaitų gavėjo kontakto vardas ir pavardė** | Tinklelį galima redaguoti skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Tai teksto laukas, kurį reikėtų naudoti kliento, kuriam išrašyta sąskaita faktūra, kontaktams identifikuoti. Šio lauko numatytosios reikšmės pateikiamos iš susijusio kliento įrašo. | Nukopijuojama į šiam klientui sugeneruojamos sąskaitos faktūros lauką **Sąskaitų gavėjo kontakto vardas ir pavardė**. |
| **Sąskaitų gavėjo vardas** | Tinklelį galima redaguoti skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Tai teksto laukas, kurį reikėtų naudoti kliento, kuriam išrašyta sąskaita faktūra, kontaktams identifikuoti. Šio lauko numatytosios reikšmės pateikiamos iš susijusio kliento įrašo. | Nukopijuojama į šiam klientui sugeneruojamos sąskaitos faktūros lauką **Sąskaitų gavėjo kontakto vardas ir pavardė**. |
| **Mokėjimo sąlygos** | Tinklelį galima redaguoti skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Numatytosios reikšmės pateikiamos iš susijusio kliento įrašo. | Nukopijuojama į šiam klientui sugeneruojamos sąskaitos faktūros lauką **Sąskaitų gavėjo kontakto vardas ir pavardė**. |
| **Apvalinamas** | Tinklelį galima redaguoti skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Nurodo, ar šis klientas yra numatytasis šio sandorio apvalinimo klientas. Projekto sutartyje galima nurodyti tik vieną apvalinimo klientą. | Kai padalijus išlaidas ir pardavimo operacijas, už kurias neišrašyta sąskaita faktūra, atsiranda apvalinimo paklaida, paklaida taikoma faktiniams duomenims, susietiems su šiuo klientu. |
| **Limitas, kurio negalima viršyti** | Tinklelį galima redaguoti skirtuke **Sutarties klientai** ir formose **Pagrindinis** ir **Spartusis kūrimas**, skirtose sutarties klientui. | Nurodo, ar yra sutartinis limitas, ar viršutinė riba, taikoma bendrai sumai, kuri bus išrašyta šio sandorio klientui. | **Limitas, kurio negalima viršyti**, nustatytas sutarties kliento lygiu, bus apskaičiuotas dalyje **Pardavimo faktiniai duomenys, už kuriuos neišrašyta sąskaita faktūra**, susietoje su šiuo sutarties klientu. |

## <a name="edit-billing-split-percentages"></a>Atsiskaitymo išskaidytos procentinės dalies redagavimas

Atsiskaitymo išskaidymo procentines vertes galima redaguoti įdėtajame tinklelyje. Jei atsiskaitymo išskaidymo procentinės vertės nesudaro 100 procentų, bus pateikta klaida. Pakoregavę atsiskaitymo išskaidymo procentines vertes, atnaujinkite puslapį, kad pašalintumėte klaidą.

Taip pat galite pažymėti parinktį **Paskirstyti tolygiai** papildomame tinklelyje **Sutarties klientai**, kad tolygiai paskirstytumėte atsiskaitymo išskaidymą visiems sutarties klientams. Jei yra apvalinimo koeficientas, jis bus įtraukta į apvalinimo klientą. Vienas iš sutarties klientų visada turi būti pažymėtas kaip **apvalinimo** klientas; tai reiškia, kad sutarties kliento įrašo apvalinimo žymė nustatyta kaip **Taip**. Paprastai tai yra pirminis sutarties klientas, bet jį taip pat galima keisti.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]