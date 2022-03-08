---
title: Kelių klientų valdymas projekto sutartyse
description: Šioje temoje pateikiama informacijos, kaip tvarkyti kelis klientus projekto sutartyje.
author: rumant
ms.date: 11/18/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 1adb786c36d43a148e8c5a8b25ded5a997557119f7e6e9e2248935ad4ed211d5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992081"
---
# <a name="manage-multiple-customers-on-project-contracts"></a>Kelių klientų valdymas projekto sutartyse

Šioje temoje pateikiama informacijos, kaip tvarkyti kelis klientus projekto sutartyje. Galite naudoti projekto sutartį, kai siekiant finansuoti sandorį reikia sudaryti sutartį su keliais klientais. Puslapio **Projekto sutartis** skirtuke **Suvestinė** pateikiama informacija apie pirminį sandorio klientą. Kitus klientus, dalyvaujančius sandoryje, galima pridėti skirtuke **Klientai**.

Visi sutarties klientai, esantys projekto sutarties skirtuke **Klientai**, nustatomi kaip numatytieji sutarties eilutės klientai visose naujose projektu pagrįstos sutarties eilutėse, skirtose projekto sutarčiai. Jokios esamos projektu pagrįstos sutarties eilutės nebus pakeistos naujais sutarties klientų įrašais, kurie sukuriami vėliau.

Galite bet kada pridėti, atnaujinti arba panaikinti sutarties ir sutarties eilutės klientus prieš laimint sutartį. Projekto sutarties klientą reikia nustatyti kaip klientą puslapio **Klientai** įmonės, kuriai priklauso, arba juridinio subjekto dalyje. Juridiniai subjektai nustatomi „Dynamics 365 Project Operations“ modulyje **Projektų valdymas ir apskaita** ir jie pasiekiami kaip įmonės „Project Operations“ moduliuose **Projekto pardavimas** ir **Pristatymas**.

## <a name="primary-customers"></a>Pirminiai klientai

Potencialus klientas, nurodytas projekto sutarties skirtuke **Suvestinė**, yra pirminis sutarties klientas. Negalima atnaujinti pirminio kliento naudojant sutarties klientų sąrašą. Bandant panaikinti pirminį klientą iš sutarties klientų sąrašo, pateikiamas klaidos pranešimas, kad sutarties pirminio kliento įrašo panaikinti negalima. Vietoj to pakeiskite klientą projekto sutarties skirtuko **Suvestinė** lauką **Potencialus klientas**. Atnaujinus šį lauką, naujai pasirinktas klientas pridedamas kaip naujas sutarties klientas nustatant žymę **Pirminis** kaip **Taip**. Ankstesnis pirminis klientas vis tiek liks sutarties klientu, bet nebebus pirminiu klientu.

## <a name="create-update-or-delete-a-contract-customer-record"></a>Sutarties kliento įrašo kūrimas, naujinimas arba panaikinimas

Galite kurti, atnaujinti arba panaikinti sutarties klientą puslapio **Sutartis** skirtuke **Sutarties klientai**. Toliau nurodyti laukai įtraukiami į projekto sutarties kliento įrašą.

| **Laukas** | **Vieta** | **Aprašas** | 
| --- | --- | --- | 
| Paskyra | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti sutarties klientui. | Išvardinkite visus aktyvius klientus. Šis laukas užrakinamas sukūrus įrašą. Norint atnaujinti įrašą, jį reikia panaikinti ir sukurti iš naujo. Jei įrašėte bet kokius faktinius duomenis arba jei sutarties kliento įrašas yra pirminis klientas, įrašo panaikinti negalima. Kai sukuriama sutarties eilutė, sutarties klientai nukopijuojami kaip sutarties eilutės klientai. |
| Atsiskaitymo išskaidymo procentas | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti sutarties klientui. | Nurodo kiekvienos pardavimo operacijos, už kurią neišrašyta sąskaita faktūra, procentinę dalį, kuri priskirta sutarties klientui. Sukūrus naujas projekto sutarties eilutes, atsiskaitymo išskaidymo procentas nukopijuojamas į naujas sukurtas sutarties eilutes ir projekto sutarties eilutės klientus. |
| Sąskaitų gavėjo kontakto vardas ir pavardė | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti sutarties klientui. | Šį teksto lauką reikia naudoti siekiant identifikuoti kliento, kuriam išrašyta sąskaita faktūra, kontaktinį asmenį. Numatytoji reikšmė pateikiama iš susijusio kliento įrašo. Kontakto vardas ir pavardė nukopijuojami į klientui sugeneruotos sąskaitos faktūros lauką **Sąskaitų gavėjo kontakto vardas ir pavardė**. |
| Sąskaitų gavėjo vardas | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti sutarties klientui. | Naudokite šį lauką, kad identifikuotumėte kliento, kuriam išrašyta sąskaita faktūra, kontaktinį asmenį. Numatytoji reikšmė pateikiama iš susijusio kliento įrašo. Vardas ir pavardė nukopijuojami į klientui sugeneruotos sąskaitos faktūros lauką **Sąskaitų gavėjo kontakto vardas ir pavardė**. |
| Mokėjimo sąlygos | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti sutarties klientui. | Numatytoji reikšmė pateikiama iš susijusio kliento įrašo. Sąlygos nukopijuojamos į klientui sugeneruotos sąskaitos faktūros lauką **Sąskaitų gavėjo kontakto vardas ir pavardė**. |
| Įmonė, kuriai priklauso | Redaguojamas tinklelis skirtuke **Projekto sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti projekto sutarties klientui. | Juridinis objektas, kuriame klientas yra nustatytas modulyje **Projektų valdymas ir apskaita**. Šis laukas yra tik skaitomas ir jame nustatoma įmonė, kuriai priklauso projekto sutartis.</br>Klientų, kuriuos norite įtraukti į lauką **Klientas**, sąrašas jau filtruojamas į sąrašą iš valdančiosios įmonės „Project Operations“ **Projekto valdymo ir apskaitos** modulyje. Įmonė, kuriai priklauso, atitinka juridinį subjektą, nustatytą „Project Operations“ modulyje **Projektų valdymas ir apskaita**. Visos išlaidos ir įplaukos, gautos iš projekto, įtraukiamos į įmonės, kuriai priklauso pasiūlymas, didžiąją knygą. |
| Apvalinamas | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti sutarties klientui. | Nurodo, ar klientas yra numatytasis sandorio apvalinimo klientas. Projekto sutartyje galima nurodyti tik vieną apvalinimo klientą. Kai padalijus išlaidas ir pardavimo operacijas, už kurias neišrašyta sąskaita faktūra, atsiranda apvalinimo paklaida, paklaida taikoma faktiniams duomenims, susietiems su klientu. |
| Limitas, kurio negalima viršyti | Redaguojamas tinklelis skirtuke **Sutarties klientai** ir pagrindinis bei sparčiojo kūrimo puslapiai, skirti sutarties klientui. | Nurodo, ar yra sutartinis limitas, ar viršutinė riba, taikoma bendrai sumai, kuri bus išrašyta sandorio klientui. Limitas, kurio negalima viršyti, nustatytas sutarties kliento lygiu, bus įvertintas remiantis pardavimo faktiniais duomenimis, už kuriuos neišrašyta sąskaita faktūra, susijusiais su sutarties klientu. |

## <a name="edit-billing-split-percentages"></a>Atsiskaitymo išskaidytos procentinės dalies redagavimas

Atsiskaitymo išskaidymo procentines vertes galima redaguoti tinklelyje. Jei atsiskaitymo išskaidymo procentinės vertės nesudaro 100 procentų, pateikiama klaida. Pakoregavę atsiskaitymo išskaidymo procentinę vertę, atnaujinkite puslapį **Projekto sutartis**, kad pašalintumėte klaidą.

Taip pat galite pasirinkti parinktį **Paskirstyti tolygiai** projekto sutarties klientų papildomame tinklelyje. Atsiskaitymas išskaidomas tolygiai visiems projekto sutarties klientams. Jei yra koks nors apvalinimo koeficientas, jis bus įtrauktas į apvalinimo klientą. Vienam iš sutarties klientų būtina nustatyti žymę **Apvalinimas** kaip **Taip**. Tas klientas yra apvalinimo klientas. Paprastai apvalinimo klientas taip pat yra pirminis sutarties klientas, bet tai nėra privaloma.


[!INCLUDE[footer-include](../includes/footer-banner.md)]