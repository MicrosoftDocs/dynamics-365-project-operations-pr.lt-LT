---
title: Kelių klientų tvarkymas projektu pagrįsto pasiūlymo eilutėse
description: Šiame straipsnyje pateikiama informacija apie tai, kaip valdyti kelis klientus pagal projektą pagrįstose pasiūlymo eilutėse.
author: rumant
ms.date: 10/06/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 0160a7023ff1d5f806b8c01115a48d0552008d15
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928258"
---
# <a name="manage-multiple-customers-on-project-based-quote-lines"></a>Kelių klientų tvarkymas projektu pagrįsto pasiūlymo eilutėse

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Projektu pagrįsto pasiūlymo eilučių palaikymo scenarijai, kai kiekvienoje pasiūlymo eilutėje yra klientų, mokančių už jį, sąrašas. Projektu pagrįsto pasiūlymo eilutėse esančių klientų sąrašas gali būti toks pat, kaip ir pasiūlyme esančių klientų sąrašas. Taip pat galite pakeisti klientų sąrašą, kad jis būtų skirtingas. Norint kurti galimą projekto sutartį, kai laimėtas projekto pasiūlymas, projekto pasiūlymo eilutės klientų sąrašas bus nukopijuotas į atitinkamą projeku pagrįstą sutarties eilutę. Projektu pagrįstame pasiūlyme esantys klientai kopijuojami į projekto sutartį.

Kai galutinio projekto sutarčiai išrašote sąskaitą faktūrą, klientų sąrašas, esantis projektu pagrįstos sutarties eilutėje, pirmenybę teikia projekto sutarties sąrašui. Klientų sąrašas projekto sutartyje naudojamas tik numatytosioms naujoms projekto sutarties eilutėms.

Visi pasiūlymo Klientai, esantys projekto pasiūlymo skirtuke **Klientai**, nustatomi kaip pasiūlymo eilutės klientai naujo projektu pagrįsto pasiūlymo eilutėse, sukurtose projekto pasiūlymui. Bet kokios esamos projektu pagrįsto pasiūlymo eilutės nepaveldės naujo pasiūlymo klientų įrašų, sukurtų po jų.

## <a name="create-update-or-delete-a-quote-line-customer-record"></a>Pasiūlymo eilutės kliento įrašo kūrimas, naujinimas arba naikinimas

Galite kurti, atnaujinti arba panaikinti pasiūlymo eilutės klientą skirtuke **Pasūlymo eilutės klientai**, esančiame puslapyje **Projektu pagrįsto pasiūlymo eilutė**. Kai į projektu pagrįsto pasiūlymo eilutę įtraukiate naują klientą, klientas taip pat įtraukiamas į bendrąjį pasiūlymą kaip pasiūlymo klientas, o bendra pasiūlymo sumos procentinė dalis yra 0%. Bendro pasiūlymo atsiskaitymo išskaidyta procentinė dalis kopijuojama į naujo pasiūlymo eilutes ir į galimą projekto sutartį. Tačiau, kai išrašote sąskaitą faktūrą iš sutarties, naudojama atsiskaitymo procentinė dalis pasiūlymo eilutės lygyje, o ne bendro sutarties lygio sąskaitų išrašymo procentinė dalis. 

Šioje lentelėje nurodomi projektu laukai, esantys pagrįsto pasiūlymo eilutės pasiūlymo eilutės klientų įraše.

| Laukas | Vieta | Aprašas ir gairės | Tolesnis poveikis |
| --- | --- | --- | --- |
| **Klientas** | Redaguojamas tinklelis skirtuke **Pasiūlymo eilutės klientai**, pagrindinė forma ir sparčiojo kūrimo forma pasiūlymo eilutės klientams. | Išvardinkite visus aktyvius klientus. Šis laukas užrakinamas sukūrus įrašą. Jei reikia atnaujinti lauką, ištrinkite ir iš naujo sukurkite įrašą. Jei įrašėte bet kokius faktinius duomenis, negalėsite panaikinti įrašo. | Kai pasirenkate klientą iš įtraukiamų klientų pagrindinio sąrašo, pasiūlymo eilutės klientas taip pat pridedamas kaip pasiūlymo klientas. Pasiūlymo eilutės klientai kopijuojami į projekto sutarties eilutės klientus laimėjus pasiūlymą. |
| **Atsiskaitymo išskaidymo procentas** | Redaguojamas tinklelis skirtuke **Pasiūlymo eilutės klientai**, pagrindinė forma ir sparčiojo kūrimo forma pasiūlymo eilutės klientams. | Atitinka kiekvieno pardavimo, už kurį neišrašyta SF, operacijos procentinę dalį, kuri bus priskirta šios pasiūlymo eilutės klientui. | Kopijuojama į projekto sutarties eilutės klientus. |
| **Limitas, kurio negalima viršyti** | Redaguojamas tinklelis skirtuke **Pasiūlymo eilutės klientai**, pagrindinė forma ir sparčiojo kūrimo forma pasiūlymo eilutės klientams. | Nurodo, ar yra sutartinis limitas ar viršutinė riba bendrai sumai, pagal kurią bus išrašyta SF šiam klientui už šią pasiūlytą eilutę. | Nukopijuota į projekto sutarties eilutę klientams, kai laimėtas pasiūlymas. |
| **Valdančioji įmonė** | Redaguojamas tinklelis skirtuke **Pasiūlymo eilutės klientai**, pagrindinė forma ir sparčiojo kūrimo forma pasiūlymo eilutės klientams, | Juridinis subjektas, kuriame šis klientas nustatomas **Projekto valdymo ir apskaitos** modulyje. Šis laukas yra tik skaitomas ir nustatytas kaip paties pasiūlymo valdančioji įmonė. Klientų, kuriuos norite įtraukti į lauką **Klientas**, sąrašas jau filtruojamas į sąrašą iš valdančiosios įmonės „Project Operations“ **Projekto valdymo ir apskaitos** modulyje. | Valdančioji įmonė atitinka juridinio subjekto sąvoką. Visos išlaidos ir pajamos, gautos iš šio projekto, įtraukiamos į valdančiosios įmonės DK. |
| **Apvalinamas** | Redaguojamas tinklelis skirtuke **Pasiūlymo eilutės klientai**, pagrindinė forma ir sparčiojo kūrimo forma pasiūlymo eilutės klientams. | Nurodo, ar šis klientas yra šio projektu pagrįsto pasiūlymo eilutės numatytasis apvalinimo klientas. | Nukopijuota į projekto sutarties klientus, kai laimėtas pasiūlymas. |

## <a name="edit-billing-split-percentages"></a>Atsiskaitymo išskaidytos procentinės dalies redagavimas

Galite redaguoti atsiskaitymo išskaidytą procentinę dalį eilutėje. Kai atsiskaitymo išskaudyta procentinė dalis nėra iš viso 100%, įvyksta klaida. Kai redaguojate atsiskaitymo išskaidytą procentinę dalį, atnaujinkite pasiūlymo eilutės puslapį ir pašalinkite klaidą.

Naudokite tolygiai paskirstytą veiksmą pasiūlymo eilutės klientų papildomame tinklelyje, norėdami paskirstyti atsiskaitymo sumą visiems pasiūlymo eilučių klientams. Jei yra apvalinimo koeficientas, jis bus įtrauktas į apvalinimo klientą. Vienas iš pasiūlymo eilučių klientų yra visada žymimas kaip apvalinimo klientas, o tai reiškia, kad pasiūlymo eilutės kliento įraše yra apvalinimo žymė nustatyta į **Taip**. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]