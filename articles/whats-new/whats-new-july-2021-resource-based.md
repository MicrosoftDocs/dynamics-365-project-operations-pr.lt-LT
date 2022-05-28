---
title: Kas nauja – 2021 m. liepos mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams
description: Šioje temoje pateikiama informacija apie kokybinius naujinimus, kuriuos galima rasti 2021 m. liepos mėn. „Project Operations“, skirtos išteklių / nelaikomų medžiagų scenarijams, leidime.
author: sigitac
ms.date: 07/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1c88f3b4747005bee0d68d0e8a4314c01ffdaf34
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8600890"
---
# <a name="whats-new-july-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja – 2021 m. liepos mėn. – „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

   - „Project Operations“ 4.12.0.148 arba 4.12.0.152 versijos „Microsoft Dataverse“ aplinkoje.
   - Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.20 versija.

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- Galimybė administratoriams peržiūrėti PSS žurnalus ir operacijų rinkinių žurnalus parametrų meniu. Žurnalai saugomi 90 dienų.

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Šiame leidime nėra „Project Operations“ dvigubo rašymo schemų naujinimų.

Dabartinį „Project Operations“ dvigubo rašymo schemų sąrašą ir versijas rasite straipsnyje [„Project Operations“ dvigubo rašymo schemų versijos](../environment/resource-dual-write-maps.md).

Atnaujindami „Project Operations“ „Dataverse“ sprendimo ir „Finance“ sprendimo versijas, visada naudokite naujausią schemos versiją savo aplinkoje ir įjunkite visas susijusias lentelių schemas. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite matyti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Naują schemos versiją galite suaktyvinti pasirinkdami **Lentelių schemų versijos**, pasirinkdami naujausią versiją ir įrašydami pasirinktą versiją. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleisdami schemą susiduriate su problema, vykdykite nurodymus, pateikiamus vadovo Dvigubo rašymo trikčių šalinimas skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

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
### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektų valdymas ir apskaita pagal Dynamics 365 Finance

| Funkcijų sritis                      | Nuorodos numeris | Kokybės naujinimas                                                                                                                                                                                                                                                                                                                |
|-----------------------------------|------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projektų valdymas ir apskaita | 4620267          | Negalima suasmeninti formų ir įtraukti lauko **Paskirtis** į puslapius **Projekto užregistruota operacija**, **Sąskaitos faktūros pasiūlymo kūrimas** bei **Sąskaitos faktūros pasiūlymas**.                                                                                                                                                                                         |
| Projektų valdymas ir apskaita | 4613449          | Kai programoje „Finance“ pasirenkate projekto sutarties ID, integruota „Project Operations“ aplinka atidaro puslapį, kuriame galima kurti naują įrašą, o ne puslapį, skirtą jau sukurtoms projektų sutartims.                                                                                                                                           |
| Projektų valdymas ir apskaita | 4614445          | „Project Operations“ integruoto scenarijaus visuotinėje įdiegtyje negalite redaguoti lauko **Prekių PVM grupė** sąskaitos faktūros pasiūlyme, kuris yra importuotas iš paruošimo. Prekių PVM grupę turi būti galima redaguoti atidarytame SF pasiūlyme, naudojant visus operacijų tipus, įskaitant laisvos formos, valandų, išlaidų, mokesčių ir prekių. |
| Projektų valdymas ir apskaita |                  | Negalima registruoti sąskaitos faktūros pasiūlymo, gauto dėl neigiamos laiko operacijos korekcijos.                                                                                                                                                                                                                                              |
| Projektų valdymas ir apskaita |                  | Sąskaitų faktūrų pasiūlymų eilutės yra dubliuojamos dėl kelių periodinių procesų **Importavimas iš paruošimo**, vykdomų vienu metu.                                                                                                                                                                                                                |

