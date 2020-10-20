---
title: Kelių klientų tvarkymas pasiūlymo eilutėse
description: Šioje temoje pateikta informacija apie darbą su pasiūlymais, apimančiais kelis klientus, kurie finansuos projektą. („Sales“)
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 656418ab99db46455195f70c38b6f5fa13c30755
ms.sourcegitcommit: f6509f7d50de4d4ebb92c1bf2cfcdf09f17458eb
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/06/2020
ms.locfileid: "3966826"
---
# <a name="managing-multiple-customers-on-project-quotes-sales"></a>Kelių klientų tvarkymas projekto pasiūlymuose (pardavimai)

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_

Projekto pasiūlymai palaiko scenarijų, kai pasiūlymas apima kelis klientus, kurie finansuos sandorį. Pasiūlymo skirtuke **Suvestinė** yra laukas **Potencialus klientas**, kuris nustato pirminį sandorio klientą. Kitus sandėrio klientus galima nustatyti projekto pasiūlymo skirtuke **Klientai**.

Visi pasiūlymo klientai, esantys projekto pasiūlymo skirtuke **Klientai** nustatomi kaip pasiūlymo eilutės klientai bet kuriose **naujo** projektu pagrįsto pasiūlyo eilutėse, sukurtose šiam pasiūlymui. Bet kokios esamos projektu pagrįsto pasiūlymo eilutės nepaveldės naujo pasiūlymo klientų įrašų, sukurtų po jų.

Produktu pagrįsto pasiūlymo eilutės automatiškai susiejamos su pirminiu klientu, kuris taip pat yra lauko **Potencialus klientas**, esančio pasiūlymo skirtuke **Suvestinė**, klientas.

Pasiūlymo klientai ir pasiūlymo eilutės klientai gali būti įtraukti, atnaujinti arba panaikinti bet kuriuo metu, kai pasiūlymas dar nelaimėtas.

## <a name="concept-of-a-primary-customer"></a>Pirminio kliento koncepcija

Klientas, esantis projekto pasiūlymo suvestinės skirtuke kaip potencialus klientas, yra pirminis pasiūlymo klientas. Bandydami panaikinti pirminį klientą pasiūlymo klientų sąraše, matysite klaidos pranešimą, kad pirminio kliento įrašas pasiūlyme negali būti panaikintas.

Pirminis klientas neturi būti atnaujinamas iš pasiūlyme esančio klientų sąrašo. Tačiau galite daryti įtaką pirminiam klientui keisdami potencialų klientą pasiūlymo skirtuke **Suvestinė**. Kai šis laukas atnaujinamas **Pasiūlymo suvestinėje**, naujai pasirinktas potencialus klientas pridedamas kaip naujas pasiūlymo klientas su vėliavėle **Pirminis**. Ankstesnis potencialus klientas vis dar bus pasiūlymo klientas.

## <a name="create-update-or-delete-a-quote-customer-record"></a>Pasiūlymo kliento įrašo kūrimas, naujinimas arba naikinimas

Pasiūlymo klientą galima sukurti, atnaujinti arba panaikinti skirtuke **Pasiūlymo klientai**, esančiame puslpayje **Pasiūlymas**. Šioje lentelėje nurodomi laukai yra projekto pasiūlymo kliento įraše.

| **Laukas** | **Vieta** | **Atitiktis, tikslas ir gairės** | **Tolesnis poveikis** |
| --- | --- | --- | --- |
| Abonementas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Išvardinkite visus aktyvius klientus. Šis laukas užrakinamas sukūrus įrašą. Jei norite jį atnaujinti, panaikinkite įrašą ir jį sukurkite iš naujo. Jei įrašėte bet kokius faktinius duomenis arba jei pasiūlymo kliento įrašas yra pirminis klientas, galėsite panaikinti įrašą. | Pasiūlymo klientai kopijuojami kaip pasiūlymo eilutės klientai, kai sukuriama pasiūlymo eilutė. Pasiūlymo klientai taip pat kopijuojami į projekto sutarties klientus, kai laimimas pasiūlymas. |
| Atsiskaitymo išskaidymo procentas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Atitinka kiekvieno pardavimo, už kurį neišrašyta SF, operacijos procentinę dalį, kuri bus priskirta šio pasiūlymo klientui. | Nukopijuota į naujo pasiūlymo eilutes ir į projekto sutarties klientus. |
| Sąskaitų gavėjo kontakto vardas ir pavardė | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Tai teksto laukas, kurį reikėtų naudoti kliento, kuriam išrašyta sąskaita faktūra, kontaktams identifikuoti. Tai yra nustatyta iš susijusio kliento įrašo | Kopijuojama į projekto sutarties klientus, kai laimimas pasiūlymas, ir savo ruožtu į sąskaitų gavėjo kontaktinių duomenų lauką, esantį sąskaitoje faktūroje, kuri generuojama šiam klientui. |
| Sąskaitų gavėjo vardas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Tai teksto laukas, kurį reikėtų naudoti kliento, kuriam išrašyta sąskaita faktūra, kontaktams identifikuoti. | Kopijuojama į projekto sutarties klientus, kai laimimas pasiūlymas, ir savo ruožtu į **sąskaitų gavėjo kontaktinių duomenų** lauką, esantį sąskaitoje faktūroje, kuri generuojama šiam klientui. |
| Mokėjimo sąlygos | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Tai parinkčių rinkinys su reikšmėmis, kurios nustatomos iš susijusio kliento įrašo. | Kopijuojama į projekto sutarties klientus, kai laimimas pasiūlymas, ir savo ruožtu į **sąskaitų gavėjo kontaktinių duomenų** lauką, esantį sąskaitoje faktūroje, kuri generuojama šiam klientui. |
| Apvalinamas | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Nurodo, ar šis klientas yra numatytasis šio sandorio apvalinimo klientas. | Nukopijuota į projekto sutarties klientus, kai laimėtas pasiūlymas. |
| Limitas, kurio negalima viršyti | Redaguojamas tinklelis skirtuke **Pasiūlymo klientai** ir pasiūlymo klientui skirtos formos **Pagrindinis** ir **Spartusis kūrimas**. | Nurodo, ar yra sutartinis limitas ar viršutinė riba bendrai sumai, pagal kurią bus išrašyta SF šiam klientui už šį įtraukimą. | Nukopijuota į projekto sutarties klientus, kai laimėtas pasiūlymas. |

## <a name="editing-billing-split-percentages"></a>Atsiskaitymo išskaidytos procentinės dalies redagavimas

Galite redaguoti atsiskaitymo išskaidytą procentinę dalį naudodami eilutės tinklelio redagavimą. Kai atsiskaitymo išskaidyta procentinė dalis nėra iš viso 100%, įvyksta klaida. Kai atnaujinate atsiskaitymo išskaidytą procentinę dalį, atnaujinkite pasiūlymo eilutės puslapį ir pašalinkite klaidą.

Taip pat galite bandyti pasirinkti parinktį **Paskirstyti tolygiai**, esančią pasiūlymo klientų papildomame tinklelyje. Šis veiksmas išskaido atsiskaitymą visiems pasiūlymo klientams. Jei yra apvalinimo koeficientas, jis bus įtrauktas į apvalinimo klientą. Vienas iš pasiūlymo klientų yra visada žymimas kaip apvalinimo klientas. Tai reiškia, kad pasiūlymo kliento įraše yra **apvalinimo**žymė nustatyta į **Taip**. Paprastai tai yra pirminis pasiūlymo klientas, tačiau jį galima keisti.
