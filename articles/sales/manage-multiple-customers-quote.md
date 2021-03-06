---
title: Kelių klientų tvarkymas projekto pasiūlymuose
description: Šioje temoje pateikta informacija apie darbą su pasiūlymais, apimančiais kelis klientus, kurie finansuos projektą.
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 8b1d9284c063e34e34ec6525072a1f8f860116b6
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/01/2020
ms.locfileid: "3908390"
---
# <a name="manage-multiple-customers-on-project-quotes"></a>Kelių klientų tvarkymas projekto pasiūlymuose

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Projekto pasiūlymai palaiko scenarijų, kai pasiūlymas apima kelis klientus, kurie finansuos sandorį. Pasiūlymo skirtuke **Suvestinė** yra laukas **Potencialus klientas**, kuris nustato pirminį sandorio klientą. Kitus sandėrio klientus galima nustatyti projekto pasiūlymo skirtuke **Klientai**.

Visi pasiūlymo klientai, esantys projekto pasiūlymo skirtuke **Klientai** nustatomi kaip pasiūlymo eilutės klientai bet kuriose **naujo** projektu pagrįsto pasiūlyo eilutėse, sukurtose šiam pasiūlymui. Bet kokios esamos projektu pagrįsto pasiūlymo eilutės nepaveldės naujo pasiūlymo klientų įrašų, sukurtų po jų.

Pasiūlymo klientai ir pasiūlymo eilutės klientai gali būti įtraukti, atnaujinti arba panaikinti bet kuriuo metu, kai pasiūlymas dar nelaimėtas. Galiojantis pasiūlymo klientas turi būti nustatytas kaip valdančiosios įmonės arba juridinio subjekto klientas puslapyje **Klientai**. Juridiniai subjektai yra nustatomi „Dynamics 365 Project Operations“ **Projektų valdymo ir apskaitos** modulyje yra yra pateikiami kaip įmonės „Project Operations“ **Projektų pardavimų ir pristatymo** modulyje.

## <a name="concept-of-a-primary-customer"></a>Pirminio kliento koncepcija

Klientas, projekto pasiūlymo skirtuke **Suvestinė** įrašytas kaip potencialus klientas, yra pirminis pasiūlymo klientas. Jei bandysite panaikinti pirminį klientą pasiūlymo klientų sąraše, atsiras klaidos pranešimas, kad pirminio kliento įrašas pasiūlyme negali būti panaikintas.

Pirminis klientas neturi būti atnaujinamas iš pasiūlyme esančio klientų sąrašo. Tačiau galite daryti įtaką pirminiam klientui keisdami potencialų klientą pasiūlymo skirtuke **Suvestinė**. Kai šis laukas atnaujinamas **Pasiūlymo suvestinėje**, naujai pasirinktas potencialus klientas pridedamas kaip naujas pasiūlymo klientas su vėliavėle **Pirminis**. Ankstesnis potencialus klientas vis dar bus pasiūlymo klientas.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Pasiūlymo kliento įrašo kūrimas, naujinimas arba naikinimas

Pasiūlymo klientą galima sukurti, atnaujinti arba panaikinti skirtuke **Pasiūlymo klientai**, esančiame puslpayje **Pasiūlymas**. Šioje lentelėje nurodomi laukai yra projekto pasiūlymo kliento įraše.

| **Laukas** | **Vieta** | **Atitiktis, tikslas ir gairės** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Abonementas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Išvardinkite visus aktyvius klientus. Šis laukas užrakinamas sukūrus įrašą. Jei norite jį atnaujinti, panaikinkite įrašą ir jį sukurkite iš naujo. Jei įrašėte bet kokius faktinius duomenis arba jei pasiūlymo kliento įrašas yra pirminis klientas, galėsite panaikinti įrašą. | Pasiūlymo klientai kopijuojami kaip pasiūlymo eilutės klientai, kai sukuriama pasiūlymo eilutė. Pasiūlymo klientai taip pat kopijuojami į projekto sutarties klientus, kai laimimas pasiūlymas. |
| Atsiskaitymo išskaidymo procentas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Atitinka kiekvieno pardavimo, už kurį neišrašyta SF, operacijos procentinę dalį, kuri bus priskirta šio pasiūlymo klientui. | Nukopijuota į sukurtas naujo pasiūlymo eilutes ir į projekto sutarties klientus. |
| Sąskaitų gavėjo kontakto vardas ir pavardė | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Tai teksto laukas, kurį reikėtų naudoti kliento, kuriam išrašyta sąskaita faktūra, kontaktams identifikuoti. Tai yra nustatyta iš susijusio kliento įrašo | Kopijuojama į projekto sutarties klientus, kai laimimas pasiūlymas, ir savo ruožtu į sąskaitų gavėjo kontaktinių duomenų lauką, esantį sąskaitoje faktūroje, kuri generuojama šiam klientui. |
| Sąskaitų gavėjo vardas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Tai teksto laukas, kurį reikėtų naudoti kliento, kuriam išrašyta sąskaita faktūra, kontaktams identifikuoti. | Kopijuojama į projekto sutarties klientus, kai laimimas pasiūlymas, ir savo ruožtu į **sąskaitų gavėjo kontaktinių duomenų** lauką, esantį sąskaitoje faktūroje, kuri generuojama šiam klientui. |
| Mokėjimo sąlygos | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Tai parinkčių rinkinys su reikšmėmis, kurios nustatomos iš susijusio kliento įrašo. | Kopijuojama į projekto sutarties klientus, kai laimimas pasiūlymas, ir savo ruožtu į **sąskaitų gavėjo kontaktinių duomenų** lauką, esantį sąskaitoje faktūroje, kuri generuojama šiam klientui. |
| Apvalinamas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Nurodo, ar šis klientas yra numatytasis šio sandorio apvalinimo klientas. | Nukopijuota į projekto sutarties klientus, kai laimėtas pasiūlymas. |
| Įmonė, kuriai priklauso | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Juridinis subjektas, su kuriuo šis klientas nustatomas **Projekto valdymo ir apskaitos** modulyje. Šis laukas yra tik skaitomas ir nustatytas kaip paties pasiūlymo valdančioji įmonė. Klientų, kuriuos norite įtraukti į lauką **Klientas**, sąrašas jau filtruojamas į sąrašą iš šios valdančiosios įmonės „Project Operations“ **Projekto valdymo ir apskaitos** modulyje. | Valdančioji įmonė atitinka juridinio subjekto koncepciją „Project Operations“ **Projekto valdymo ir apskaitos** modulyje. Visos išlaidos ir pajamos, gautos iš šio projekto, įtraukiami į valdančiosios įmonės DK. |
| Limitas, kurio negalima viršyti | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Nurodo, ar yra sutartinis limitas ar viršutinė riba bendrai sumai, pagal kurią bus išrašyta SF šiam klientui už šį įtraukimą. | Nukopijuota į projekto sutarties klientus, kai laimėtas pasiūlymas. |

## <a name="editing-billing-split-percentages"></a>Atsiskaitymo išskaidytos procentinės dalies redagavimas

Galite redaguoti atsiskaitymo išskaidytą procentinę dalį naudodami eilutės tinklelio redagavimą. Kai atsiskaitymo išskaidyta procentinė dalis nėra iš viso 100%, įvyksta klaida. Kai atnaujinate atsiskaitymo išskaidytą procentinę dalį, atnaujinkite pasiūlymo eilutės puslapį ir pašalinkite klaidą.

Taip pat galite bandyti pasirinkti parinktį **Paskirstyti tolygiai**, esančią pasiūlymo klientų papildomame tinklelyje. Šis veiksmas išskaido atsiskaitymą visiems pasiūlymo klientams. Jei yra apvalinimo koeficientas, jis bus įtrauktas į apvalinimo klientą. Vienas iš pasiūlymo klientų yra visada žymimas kaip apvalinimo klientas. Tai reiškia, kad pasiūlymo kliento įraše yra **apvalinimo**žymė nustatyta į **Taip**. Paprastai tai yra pirminis pasiūlymo klientas, tačiau jį galima keisti.