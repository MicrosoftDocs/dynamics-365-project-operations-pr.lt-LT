---
title: 2022 m. kovo mėn. naujienos – „Project Operations“, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės naujinimus, kuriuos galima rasti 2022 m. kovo mėn.
author: sigitac
ms.date: 03/31/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 986d0652ed502873085259fef5ad40aba99c278d
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910916"
---
# <a name="whats-new-march-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 m. kovo mėn. naujienos – „Project Operations“, skirtos ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projekto operacijos aplinkos versijoje Dataverse 4.30.0.99
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.25 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

Per dienpinigius dabar palaikomi naujoje ir pertvarkytoje modernioje išlaidų darbo vietoje. Įmonės, naudojančios dienpinigius, gali leisti šiai funkcijai suteikti vartotojams paprastą būdą pateikti ir gauti kompensaciją už dienpinigius. Daugiau informacijos rasite [Perm išlaidos](../expense/per-diem-expenses.md).

## <a name="project-operations-dual-write-maps-updates"></a>„Project Operations“ dvigubo rašymo schemų naujinimai

Toliau pateiktame sąraše rodomi dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į "Project Operations" 2022 m. kovo mėn.

| **Objekto schema** | **Atnaujinta versija** | **Komentarai** |
| --- | --- | --- |
| Projekto operacijų integravimo projekto tiekėjo SF eilutės eksportavimo objektas msdyn\_ projectvendorinvoicelines | 1.0.0.3 | Susiejimai atnaujinti taip, kad būtų suderinti su tiekėjo SF eilutės objektu, esančiu Dataverse. <br>Nesuaktyvinkite susiejimo versijos 1.0.0.4. Jis bus paruoštas naudoti kartu su "Finance environment" versija 10.0.26 kitame mėnesio atnaujinime. |

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei naujausia žemėlapio versija nesuaktyvinta. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote lentelės struktūrą, iš naujo taikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis [dvigubo rašymo trikčių šalinimo vadovo skyriuje Trūksta lentelės stulpelių problema žemėlapių](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Laikas ir išlaidos | 2388011 | Masinio patvirtinimo metu rodyti atmetimo komentarus laiko įrašų pateikėjams. |
| Projektų planavimas ir sekimas | 2495294 | Išsamios projekto informacijos negalima redaguoti **puslapyje Išsami užduoties informacija**. |
| Sąskaitų siuntimas ir kainodara | 2499605 | Sutarties etapai, sukurti iš pasiūlymo etapų, neteisingai pažymėti kaip skirti tik skaityti. |
| Projektų planavimas ir sekimas | 2506050 | Operacijų rinkinys lieka laukiamas vieną valandą, jei nėra įrašymo pakeitimų. Tada rinkinys klaidingai pažymimas kaip **Nepavyko**, o jį reikia nedelsiant užbaigti. |
| Sąskaitų siuntimas ir kainodara | 2507401 | Numatytieji rangos vienetai neteisingai įvedami į projektus dėl neteisingo talpyklos nustatymo. |
| Sąskaitų siuntimas ir kainodara | 2541660 | **Pardavimo užsakymo kūrimo tikrinimas** dvigubu rašymu turėtų būti taikomas tik projektiniams užsakymams. |
| Sąskaitų siuntimas ir kainodara | 2552745 | Mokestis nėra padalintas tarp klientų, kurie nustatė padalinto atsiskaitymo taisykles. |
| Sąskaitų siuntimas ir kainodara | 2558859 | Patobulino klaidų pranešimus, kai nustatomos kainodaros dimensijos. |
| Sąskaitų siuntimas ir kainodara | 2558933 | **Importuoti iš projekto įvertinimų** nepavyksta, kai **msdyn\_ projektas** įtraukiamas kaip kainodaros dimensija. |
| Sąskaitų siuntimas ir kainodara | 2559101 | Projekto parametrų naikinimas nėra užblokuotas ir sukelia problemų. |
|  Galimybių valdymas | 2570390 | Dvigubo rašymo priedas verčia sąskaitos tipą pasiūlymuose, užsakymuose ir galimybėse būti **klientu**, net jei tas sąskaitos tipas neteisingas. |
| Sąskaitų siuntimas ir kainodara | 2586097 | Išbraukus projektą iš projekto sutarties eilutės, išskaičiuotų išlaidų faktinės sąskaitos neatšaukiamos. |
| Sąskaitų siuntimas ir kainodara | 2589619 | Įrašomosios medžiagos mokestis platinamas į neapmokėtus pardavimo faktus ir SF. |
|  Galimybių valdymas | 2594015 | Pasiūlymo negalima uždaryti kaip laimėto klientams, turintiems **"Net60** " mokėjimo sąlygas. |
| Projektų planavimas ir sekimas | 2595841 | Programoje "Project for the Web" vartotojai gauna klaidos pranešimą apie trūkstamą **msdyn\_ actualstart,** kai sukuria naują išteklių užklausą. |
| Laikas ir išlaidos | 2602511 | Laiko **įrašų lauke Atmesta pagal** rodoma **Sistema**, o ne įvardytas vartotojas kaip atmetimo priemonė. |
| Laikas ir išlaidos | 2602528 | Projekto tvirtintojas gali patvirtinti projektų, kuriuose jie nėra išvardyti kaip tvirtintojai, laiką. |
| Sąskaitų siuntimas ir kainodara | 2608550 | Taisymo SF galima patvirtinti, net jei originalas nekeičiamas. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektų valdymas ir apskaita pagal Dynamics 365 Finance

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [606759](https://fix.lcs.dynamics.com/Issue/Details/?bugId=606759) | Leistiname lauko Kategorijos ID **ilgyje** yra neatitikimas tarp finansų ir projekto operacijų. |
| Projektų valdymas ir apskaita | [617806](https://fix.lcs.dynamics.com/Issue/Details/?bugId=617806) | Fiksuotos kainos projektų negalima pašalinti, kai laukas **Laisvos formos SF** nustatomas kaip **Pelnas ir nuostolis** ir **naudojamas principas Įvykdyta procentinė dalis**. |
| Projektų valdymas ir apskaita | [620979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620979) | Neteisinga numatytoji PVM grupė įvedama iš projekto nustatymo išlaidų eilutėse, esančiose projekto operacijų integravimo žurnale. |
| Projektų valdymas ir apskaita | [623014](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623014) | Negalite redaguoti projekto SF pasiūlymo antraštės dimensijų integruotame diegime su "Project Operations". |
| Projektų valdymas ir apskaita | [624283](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624283) | Vidinės įmonės tiekėjo SF negalima integruoti su Dataverse. |
| Projektų valdymas ir apskaita | [634156](https://fix.lcs.dynamics.com/Issue/Details/?bugId=634156) | Kliento balansų valiuta ir ataskaitų valiuta nesutampa. |
| Projektų valdymas ir apskaita | [641612](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641612) | Galite registruoti projekto SF, net jei pirkėjas yra sulaikytas visoms SF. |
| Projektų valdymas ir apskaita | [642945](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642945) | **Projekto SF pasiūlymuose, kuriuose yra rodiniai** Antraštė **ir** Eilutės **, trūksta mygtuko Naikinti visas eilutes**. |
| Projektų valdymas ir apskaita | [637760](https://fix.lcs.dynamics.com/Issue/Details/?bugId=637760) | Registruojant tiekėjo SF, įvyksta tokia klaida: "SF apskaitos data turi būti tais pačiais ataskaitiniais metais kaip ir susijęs įsigytas užsakymas. Paleiskite pirkimo užsakymo metų pabaigos procesą arba pakeiskite datą į einamuosius ataskaitinius metus." |
| Kelionės ir išlaidos | [604128](https://fix.lcs.dynamics.com/Issue/Details/?bugId=604128) | Įsipareigotos projekto išlaidos nėra išleidžiamos po to, kai bus išleistos kelionės paraiškos įsipareigotos išlaidos. |
| Kelionės ir išlaidos | [620803](https://fix.lcs.dynamics.com/Issue/Details/?bugId=620803) | Pateikiant išlaidų ataskaitą įvyksta ši klaida: "Rietuvės sekimas: įmonės nėra". |
| Kelionės ir išlaidos | [622465](https://fix.lcs.dynamics.com/Issue/Details/?bugId=622465) | Numatytasis **projekto ID** neįvestas į išlaidų ataskaitas, **kai projekte pasirenkamas parametras Reikalauti žurnalo** veiklos. |
| Kelionės ir išlaidos | [626781](https://fix.lcs.dynamics.com/Issue/Details/?bugId=626781) | Mygtukas **Registruoti** išlaidas netinkamai veikia ištekliaus / nekauptų scenarijų projekto operacijose. |
| Kelionės ir išlaidos | [635348](https://fix.lcs.dynamics.com/Issue/Details/?bugId=635348) | Yra problema, susijusi su **tarifu už mylią** ridos išlaidų ataskaitai, į kurią įeina keleiviai. |
| Kelionės ir išlaidos | [638019](https://fix.lcs.dynamics.com/Issue/Details/?bugId=638019) | Darbuotojų išlaidų ridos tarifai nėra teisingai sumuojami, kai ridos tarifų **pakopų** išlaidų kategorijoje naudojami du skirtingi transporto priemonių tipai. |
| Kelionės ir išlaidos | [641272](https://fix.lcs.dynamics.com/Issue/Details/?bugId=641272) | Kelionės paraiškos eilutės lauko Projektas **peržvalga** nepateikia tinkamo projektų sąrašo. |
| Kelionės ir išlaidos | [645905](https://fix.lcs.dynamics.com/Issue/Details/?bugId=645905) | **Peržiūrima** rida rodo įspėjimą apie išlaidų ataskaitas. |
| Kelionės ir išlaidos | [647819](https://fix.lcs.dynamics.com/Issue/Details/?bugId=647819) | Kvito optinio simbolių atpažinimo (OCR) paslauga neveikia dėl išlaidų OCR paslaugos URL problemos. |
| Kelionės ir išlaidos | [648684](https://fix.lcs.dynamics.com/Issue/Details/?bugId=648684) | Įgalinus **funkciją Galimybė greitai** detalizuoti pasikartojančias išlaidas, išlaidų ataskaitų detalizavimo eilučių sumos keičia sumas kiekvieną kartą atidarius **puslapį Itemize**. |
| Kelionės ir išlaidos | [651899](https://fix.lcs.dynamics.com/Issue/Details/?bugId=651899) | Negalite panaikinti išlaidų ataskaitos, kai tarpiniame sąraše yra daugiau nei vienas tvirtintojas. |

## <a name="removed-and-deprecated-features"></a>Pašalintos ir nebenaudojamos funkcijos

Straipsnyje Pašalintos [arba nebenaudojamos "Project Operations](removed-depreciated-features-project.md) " funkcijos aprašomos funkcijos, kurios buvo pašalintos arba nebenaudojamos Dynamics 365 Project Operations.

- Pašalinta funkcija nebepasiekiama naudojantis šiuo produktu.
- Nebenaudojama funkcija nėra aktyviai kuriama ir gali būti pašalinta ateityje atnaujinant.

Pranešimas apie nusidėvėjimą bus rodomas "Project Operations [" straipsnio pašalintose](removed-depreciated-features-project.md) arba nebenaudojamose funkcijose likus 12 mėnesių iki bet kurios funkcijos pašalinimo iš produkto.

Jei norite nutraukti pakeitimus, kurie turi įtakos tik kompiliavimo laikui, bet yra dvejetainiai, suderinami su smėlio dėže ir gamybos aplinkomis, nusidėvėjimo laikas bus trumpesnis nei 12 mėnesių. Paprastai šie pakeitimai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.
