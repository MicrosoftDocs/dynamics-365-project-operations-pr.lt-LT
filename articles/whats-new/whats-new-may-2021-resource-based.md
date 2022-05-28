---
title: Kas nauja 2021 m. gegužės mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacija apie kokybės naujinimus, pasiekiamus 2021 m. gegužės mėn. „Project Operations“, skirtoje ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams.
author: sigitac
ms.date: 05/11/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d0af6d99a24619b3613a3aaa027404556b1b81c4
ms.sourcegitcommit: 577fa51e0892625f98f17ff39874ed1a09444421
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/06/2022
ms.locfileid: "8723778"
---
# <a name="whats-new-may-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>Kas nauja 2021 m. gegužės mėn. – „Project Operations“, skirtai ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Ši tema taikoma toliau nurodytiems „Dynamics 365 Project Operations“ komponentams ir versijoms:

- „Project Operations“ „Dynamics 365 Dataverse“ 4.10.0.186 versijos aplinkoje
- Projektų valdymas ir apskaita "Finance and Operations" programų aplinkose 10.0.18 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Į šį leidimą buvo įtrauktos toliau nurodytos funkcijos.

- [Planavimo režimai](../project-management/scheduling-modes.md): projektų vadovai dabar gali apibrėžti, ar projektą reikia valdyti naudojant fiksuotą trukmę, fiksuotą darbą ar fiksuotą vienetų planavimo režimą.
- [Kilometražo nustatymas naudojant kilometražo tarifo pakopas](../expense/set-up-mileage.md): atnaujinkite darbuotojo išlaidų ataskaitų kilometražo tarifo pakopas.

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktame sąraše parodytos dvigubo rašymo schemos, modifikuotos arba įtrauktos „Project Operations“ 2021 m. gegužės mėn. leidime.

| Objekto schema | Atnaujinta versija | Komentarai |
| --- | --- | --- |
| Projekto finansavimo šaltinis (msdyn\_projectcontractsplitbillingrules) | 1.0.0.2 | Projekto sutarties kliento mokėjimo sąlygų sinchronizavimas. |
| Projekto sąskaitų faktūrų pasiūlymų V2 (SF) | 1.0.0.3 | Proforma sąskaitų faktūrų mokėjimo sąlygų sinchronizavimas. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn\_projectvendorinvoicelines) | 1.0.0.1 | Kokybės naujinimai |
| Projektai V2 (msdyn\_projects) | 1.0.0.2 | Kokybės naujinimai |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance and Operations" programų sprendimo versiją. Jei nesuaktyvinama naujausia schemos versija, kai kurios funkcijos ir galimybės gali veikti netinkamai. Aktyvią schemos versiją galite matyti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus pritaikykite iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidžiant schemą kyla kokia nors problema, vykdykite nurodymus, pateikiamus dvigubo rašymo trikčių šalinimo vadovo skyriuje [Trūkstamų lentelių stulpelių problema schemose](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps).

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| **Funkcijų sritis** | **Nuorodos numeris** | **Kokybės naujinimas** |
| --- | --- | --- |
| Sąskaitų pateikimas ir kainodara | 2227635 | Laukų **Vienetų grupė** ir **Vienetas** reikšmės yra numatytosios iš produkto, kuris yra tinklelyje **Medžiagų įvertinimai**. |
| Sąskaitų pateikimas ir kainodara | 2234127 | Laukas **Užduoties ID** dabar tinkamai integruotas į projekto Dataverse faktinius duomenis, kai užregistruojama tiekėjo sąskaita faktūra. |
| Sąskaitų pateikimas ir kainodara | 2235564 | Įrašant žurnalo eilutę užtikrinama, kad valiuta, rodoma žurnalo eilutės įraše, atitiks eilutės numatytąją valiutą ją įrašius. |
| Sąskaitų pateikimas ir kainodara | 2246671 | Išrašant sąskaitą faktūrą operaciją padarius neapmokestinamą, atšaukiamas neišrašytos sąskaitos pardavimo įrašas ir sukuriamas naujas neišrašytos sąskaitos pardavimo įrašas kaip neapmokestinamas. |
| Sąskaitų pateikimas ir kainodara | 2264042 | Tinkamos sąskaitos faktūros taisymo blokuoti negalima, jei yra sąskaitos faktūros taisymo išsami informacija, kurios negalima naudoti aplinkoje. |
| Sąskaitų pateikimas ir kainodara | 2146367 | Projekto sąskaitos faktūros antraštės dvigubas rašymas praplečiamas, kad būtų įtrauktos mokėjimo sąlygos. |
|  Galimybių valdymas | 2086888 | Prieš kopijuodami pasiūlymą į apmokestinamus naujai nukopijuoto pasiūlymo vaidmenis ir kategorijas, neįtraukite išjungtų vaidmenų ir kategorijų. |
|  Galimybių valdymas | 2234376 | Tik skaitomi laukai tinklelyje **Medžiagų įvertinimai** yra pilki. |
|  Galimybių valdymas | 2238337 | Pasiūlymą, pagrįstą kontaktu, galima įrašyti, net jei jis nėra susietas su projekto kainoraščiu. |
|  Galimybių valdymas | 2239810 | Uždarant prarastą pasiūlymą taip pat uždaromas susietasis projektas ir atšaukiami visi rezervavimai. |
| Projektų planavimas ir sekimas | 2099559 | Prieš atidarant tinklelį **Projekto užduotys** įtraukiami papildomi sistemos sveikatos tikrinimai. |
| Projektų planavimas ir sekimas | 2178987 | Išspręsta laikina klaida, kuri įvykdavo puslapyje **Projektas** pasirinkus **Kitas etapas**. |
| Išteklių valdymas | 2224817 | Funkcija, leidžianti praplėsti numatytąsias rezervavimo reikšmes į teisingą rezervavimo būseną. |
| Laiko įrašas | 2202476 | Puslapyje **Laiko įrašas** dabar naudojamas reaguojantis tinklelio valdiklis ir ištaisomos problemos, pvz., tinklelio nesulygiavimas. |
| Laiko įrašas | 2223377 | Laiko įvestis paslėpta puslapio **Rezervuotini ištekliai** skyriuje **Susiję**, kad nebūtų galima naudoti. |

### <a name="project-management-and-accounting-in-dynamics-365-finance"></a>Projektų valdymas ir apskaita Dynamics 365 Finance

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [545878](https://fix.lcs.dynamics.com/Issue/Details/?bugId=545878) | „Project Operations“ ištekliais pagrįsti scenarijai: negalite konvertuoti pasiūlymo į laimėtą dėl integravimo klaidos. |
| Projektų valdymas ir apskaita | [546604](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546604) | „Project Operations“: įvyksta klaidos pranešimas bandant susieti sutarties eilutę su projekto ID dėl persidengimo patikros sutarčių eilučių ir operacijos tipų. |
| Projektų valdymas ir apskaita | [547440](https://fix.lcs.dynamics.com/Issue/Details/?bugId=547440) | **ProjCDSProjectContractEntity** nustato finansavimo šaltinio sąskaitos faktūros adresą kitam klientui. |
| Kelionės ir išlaidos | [480451](https://fix.lcs.dynamics.com/Issue/Details/?bugId=480451) | Įvyksta registravimo klaida, susijusi su kilometražo sąranka. |
| Kelionės ir išlaidos | [522084](https://fix.lcs.dynamics.com/Issue/Details/?bugId=522084) | Neveikia užsienio valiutos išlaidų operacijų funkcija **Išskaidyti į asmenines**. |
| Kelionės ir išlaidos | [523938](https://fix.lcs.dynamics.com/Issue/Details/?bugId=523938) | Išlaidų kategorijų išplečiamajame meniu rodomos netinkamos atstovų kategorijos, neatsižvelgiant į tai, ar jie nustatyti kaip ištekliai. |
| Kelionės ir išlaidos | [539266](https://fix.lcs.dynamics.com/Issue/Details/?bugId=539266) | Dėl klaidos **Išteklių / kategorijų tikrinimas** negalite įrašyti vidinės įmonės išlaidų ataskaitos. |
| Kelionės ir išlaidos | [532610](https://fix.lcs.dynamics.com/Issue/Details/?bugId=532610) | Dėl netinkamo kilometražo koeficiento skaičiavimo išlaidų ataskaitoje, registruojant išskaidytos eilutės. |
| Kelionės ir išlaidos | [537404](https://fix.lcs.dynamics.com/Issue/Details/?bugId=537404) | Kai įtraukiamas PVM, o mokėjimo būdo korespondentinės sąskaitos tipas yra **Darbuotojas**, negalite registruoti vidinės įmonės išlaidų ataskaitos. |
| Kelionės ir išlaidos | [542927](https://fix.lcs.dynamics.com/Issue/Details/?bugId=542927) | Atšaukti duomenų įrašo **TrvRequisitionLine** keitimai ir unikali rodyklė yra susieti. |
| Kelionės ir išlaidos | [543239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=543239) | Išlaidų ataskaita palaiko šaltinio dokumento eilutės kūrimą ir naujinimą. |
| Kelionės ir išlaidos | [544323](https://fix.lcs.dynamics.com/Issue/Details/?bugId=544323) | Jei pardavimo mokestis paskelbiamas paskirties vietos juridiniame subjekte, vidinės įmonės scenarijuje rodomas neteisingas papildomos DK žurnalas. |
| Kelionės ir išlaidos | [546877](https://fix.lcs.dynamics.com/Issue/Details/?bugId=546877) | „Project Operations“: panaikinus išlaidų įvertinimą iš „Dataverse“, jis nepanaikinamas iš „Finance“. |
| Kelionės ir išlaidos | [550575](https://fix.lcs.dynamics.com/Issue/Details/?bugId=550575) | Kai išlaidų kategorija yra ne projekto kategorija, puslapyje **Išlaidos** pasirinktos finansinės dimensijos nekopijuojamos į išlaidų ataskaitą. |
