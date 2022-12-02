---
title: Kas nauja 2021 m. liepos mėn. „Project Operations“ „Lite“ visuotinėje įdiegtyje
description: Šiame straipsnyje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2021 m. liepos mėn. „Project Operations“ „Lite“ visuotinėje įdiegtyje.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 7964f38c1bc7a8e0440e2e922ff153fd9bede131
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8913998"
---
# <a name="whats-new-july-2021---project-operations-lite-deployment"></a>Kas nauja 2021 m. liepos mėn. „Project Operations“ „Lite“ visuotinėje įdiegtyje

_Taikoma (kam): „Lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros kūrimą_

Šis straipsnis taikomas toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

  - „Project Operations“ 4.12.0.148 arba 4.12.0.152 versijos „Dataverse“ aplinkoje.

## <a name="quality-updates"></a>Kokybės naujinimai
| **Funkcijų sritis**              | **Nuorodos numeris** | **Kokybės naujinimas**                                                                                                                                                                                             |
|-------------------------------|----------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Sąskaitų pateikimas ir kainodara           | 2224046              | Lauką **Operacijos klasė** galima redaguoti skirtuke **Pasiūlymo eilutės informacija**, tačiau, jei dirbate puslapyje **Pasiūlymo eilutės informacija**, jis yra užrakintas.                                                                     |
| Sąskaitų pateikimas ir kainodara           | 2224400              | Kai pasiūlyme nėra datos etapų, veiksmo **Uždaryti pasiūlymą kaip laimėtą** atlikti nepavyksta.                                                                                                                                    |
| Sąskaitų pateikimas ir kainodara           | 2234089              | Kai rankiniu būdu įvedate produkto aprašą, jis išvalomas įvedus medžiagų sąmatos kiekį.                                                                                                                         |
| Sąskaitų pateikimas ir kainodara           | 2234100              | Projekto skirtuko **Atsiskaitymas už užduotis** tinklelyje **Atsiskaitymo už užduotis sąranka** nėra stulpelio **Medžiaga** ir jo reikšmės.                                                                                                       |
| Sąskaitų pateikimas ir kainodara           | 2277409              | Produkto ID nėra medžiagos tipo sutarties eilutės duomenyse.                                                                                                                                        |
| Sąskaitų pateikimas ir kainodara           | 2281728              | Kuriant sutarties eilutę, be reikalo iš naujo įvertinami faktiniai duomenys, todėl labai padidėja duomenų apimtis, o tai turi įtakos našumui.                                                                                |
| Sąskaitų pateikimas ir kainodara           | 2298668              | Su atšauktomis ir panaikintomis išlaidomis susietos žurnalo eilutės nėra pašalinamos.                                                                                                                                     |
| Sąskaitų pateikimas ir kainodara           | 2300192              | Kai sąskaitą faktūrą redaguoja keli vartotojai, gali būti, kad patvirtintoje SF bus sukurta naujų SF sąskaitos eilutės duomenų.                                                                                   |
| Sąskaitų pateikimas ir kainodara           | 2301569              | Jei buvo pritaikyta \$0 USD apmokėjimo suma, sąskaitų faktūrų negalima koreguoti.                                                                                                                                        |
| Sąskaitų pateikimas ir kainodara           | 2307965              | Jei sukuriama kategorijos kaina su trūkstamomis reikšmėmis, įvyksta klaida.                                                                                                                           |
| Sąskaitų pateikimas ir kainodara           | 2326870              | Jei **producttypecode** yra neapibrėžtas, įvyksta **Microsoft.Dynamics.ProjectService.Plugins.PostInvoiceLineDelete** klaida.                                                                            |
| Sąskaitų pateikimas ir kainodara           | 2332732              | Jei sutarties eilutės etapas sukuriamas be užsakymo eilutės, įvyksta klaida.                                                                                                                |
| Projektų planavimas ir sekimas | 2181094              | Projektų planavimo API dabar palaiko PSS žurnalus ir operacijų rinkinio žurnalus, saugomus 90 dienų.                                                                                                                  |
| Projektų planavimas ir sekimas | 2254201              | Žyma **Grafiko režimas** atnaujinama informacija, apibūdinančia numatytąją logiką.                                                                                                                                      |
| Projektų planavimas ir sekimas | 2300252              | **openProject** atsakymų talpykla atnaujinta – joje yra atpažinimo ženklo savininkas talpyklos rakte **base Url** ir **Segment Url**, kad, pasikeitus **base Url**, **Request Url** visada būtų galima sukurti iš naujo. |
| Projektų planavimas ir sekimas | 2301312              | **msdyn_membershipstatus** pašalintas iš rodinio **Projekto komandos narys**.                                                                                                                                        |
| Projektų planavimas ir sekimas | 2302759              | Produktai be reikalo iškviečiami skirtukuose **Išteklių priskyrimai**, **Sąmatos** ir **Išlaidų sąmatos**.                                                                                                        |
| Projektų planavimas ir sekimas | 2308050              | Įvyksta **CopyProject** triktis ir pateikiama klaida „Nepavyko gauti atpažinimo ženklo, kad būtų galima užmegzti ryšį su nuotoline tarnyba“.                                                                                                                           |
| Projektų planavimas ir sekimas | 2322650              | Rodinys **Projekto užduočių sąrašas** atnaujintas, kad pagal numatytuosius parametrus būtų rodoma užduoties data.                                                                                                            |
| Projektų planavimas ir sekimas | 2327266              | Kai kopijuojamos sąmatos, **CopyProject** generuoja klaidą „Raktas nerastas žodyne“.                                                                                                      |
| Projektų planavimas ir sekimas | 2328123              | **CopyProject** generuoja klaidą „Nepavyko gauti atpažinimo ženklo, kad būtų galima užmegzti ryšį su nuotoline tarnyba“.                                                                                                                          |
| Projektų planavimas ir sekimas | 2336258              | **CopyProject** klaidingai nukopijuoja išteklių padėčių pavadinimus.                                                                                                                                                 |
| Sąskaitų pateikimas ir kainodara           | 2224476              | Laukas **Rezervuojamasis išteklius** pagal numatytuosius parametrus nėra tinkamai nustatomas kaip prisijungęs vartotojas puslapyje **Medžiagų naudojimas**.                                                                                                            |
| Išteklių valdymas           | 2277249              | Kai atnaujinamas ne projektais pagrįsto ištekliaus reikalavimas, įvyksta klaida.                                                                                                            |
| Išteklių valdymas           | 2323869              | Išteklių naudojimas netinkamai atpažįsta filtruotus išteklius.                                                                                                                                             |
| Laikas ir išlaidos              | 2176538              | Valdikliui **Laiko įrašas** taikomi netinkami filtrų operatoriai.                                                                                                                                                   |
| Laikas ir išlaidos              | 2177462              | Panaikinus laiko įrašą tinklelyje, mygtukų **Pateikti**, **Atšaukti**, **Naikinti** ir **Redaguoti įrašą** būsena atnaujinama ne taip, kaip tikimasi.                                                                                        |
| Laikas ir išlaidos              | 2299985              | **TimeEntriesImportFromResourceAssignment** netvarko pradžios / pabaigos laiko pagal priskyrimo kontūrus.                                                                                                  |
| Laikas ir išlaidos              | 2318426              | Kai pateikiamas laiko įrašas, užrakintus laukus vis dar galima redaguoti.                                                                                                                                   |
| Laikas ir išlaidos              | 2323749              | Kai išlaidos sukuriamos rezervuojamojo ištekliaus skirtuke **Susiję**, įvyksta klaida.                                                                                                      |
| Laikas ir išlaidos              | 2327678              | Kai sukuriate laiko įrašą rezervuojamojo ištekliaus skirtuke **Susiję**, pirminis išteklius nėra perduodamas laiko įrašo valdikliui.                                                                            |
| Bendroji informacija                       | 2296857              | Ilgai vykdomų užduočių eigos sekimas.                                                                                                                                                                        |
| Bendroji informacija                       | 2253682              | „Project Operations“ dvigubo rašymo sprendimas neturi būti diegiamas, kai pagrindinis dvigubo rašymo sprendimas įdiegtas aplinkoje be dvigubo rašymo tvarkymo sprendimo.                                                |
| Bendroji informacija                       | 2316420              | Jei programos vartotojo verslo vienetas pakeičiamas, įvyksta projektų vykdymo paslaugų pagrindinio sprendimo parengimo triktis.                                                                                                                     |
| Bendroji informacija                       | 2376405              | Išspręsta leidėjo valdoma naujinimo problema (Kokybiškas naujinys pasiekiamas 4.12.0.152 versijoje)                                                                                                                     |
