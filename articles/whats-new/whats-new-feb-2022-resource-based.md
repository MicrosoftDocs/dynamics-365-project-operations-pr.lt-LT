---
title: 2022 m. vasario mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie kokybės atnaujinimus, kuriuos galima rasti 2022 m. vasario mėn.
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: b036c0a3c39c52cb15277293679ef88906cae2c4
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8932996"
---
# <a name="whats-new-february-2022---project-operations-for-resourcenon-stocked-based-scenarios"></a>2022 m. vasario mėn. naujienos – „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams

*Taikoma: „Project Operations“, skirta išteklių / nelaikomų medžiagų scenarijams*

Šis straipsnis taikomas šiems "Microsoft" Dynamics 365 Project Operations komponentams ir versijoms:

- Projekto operacijos aplinkos versijoje Dataverse 4.28.0.120
- Projektų valdymas ir apskaita Dynamics 365 Finance aplinkoje 10.0.24 versija

## <a name="features-included-in-this-release"></a>Į šį leidimą įtrauktos funkcijos

- Nuo šio leidimo į vieną projektą galite įtraukti iki 300 komandos narių. Anksčiau komandos narių skaičiaus apribojimas buvo 150. Daugiau informacijos ieškokite [Project limits](../project-management/create-wbs.md#project-limitations).

## <a name="project-operations-dual-write-map-updates"></a>"Project Operations" dvigubo rašymo žemėlapio naujinimai

Toliau pateiktame sąraše rodomi dvigubo rašymo žemėlapiai, kurie buvo modifikuoti arba įtraukti į "Project Operations" 2022 m. vasario mėn.

| Objekto schema | Atnaujinta versija | Komentarai |
| --- | --- | --- |
| Projekto operacijų integravimo projekto išlaidų eksportavimo objektas (msdyn\_ išlaidos) | 1.0.0.3 | Išplėstas projekto veiklos sinchronizavimui iki Dataverse. |

Dabartiniame "Project Operations" dvigubo rašymo žemėlapių sąraše ir versijose ieškokite ["Project Operations" dvigubo rašymo žemėlapio versijose](../environment/resource-dual-write-maps.md).

Visada paleiskite naujausią žemėlapio versiją savo aplinkoje ir įgalinkite visas susijusias lentelių struktūras, kai atnaujinsite "Project Operations Dataverse " sprendimą ir "Finance" sprendimo versiją. Kai kurios funkcijos ir galimybės gali neveikti tinkamai, jei naujausia žemėlapio versija nesuaktyvinta. Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote lentelės struktūrą, iš naujo taikykite pakeitimus. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).

Jei paleidę žemėlapį susiduriate su problema, vadovaukitės instrukcijomis, pateiktomis [dviejų rašymo trikčių šalinimo vadovo skyriuje Trūksta lentelės stulpelių problema žemėlapių](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps) skyriuje.

## <a name="quality-updates"></a>Kokybės naujinimai

### <a name="project-operations-on-dataverse"></a>„Project Operations“ aplinkoje „Dataverse“

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Sąskaitų siuntimas ir kainodara | 2415109 | Numatytoji **vertė lauke Operacijos mokėjimo sąlygos** turi būti projekto sutarties kliento įrašas ir formos SF įrašas. |
| Sąskaitų siuntimas ir kainodara | 2497369 | Medžiagų taisymas turi atitikti datos reikšmę parametruose **Taisymas**. |
| Sąskaitų siuntimas ir kainodara | 2498697 | Patobulinta laiko įrašo atšaukimo **saugos konfigūracija**. |
| Sąskaitų siuntimas ir kainodara | 2513824 | Išteklių scenarijų operacijos kategorijos ID projekto operacijose neturi viršyti 28 simbolių. |
| Sąskaitų siuntimas ir kainodara | 2517455 | Negalima leisti, kad veiksmo **Atnaujinti SF eilutės operacijas** būtų galima suaktyvinti kelis kartus vienu metu toje pačioje SF. |
| Sąskaitų siuntimas ir kainodara | 2517465 | Veiksmas **Išjungti SF eilutės informaciją** užblokuotas, nes jis nepalaikomas. |
| Sąskaitų siuntimas ir kainodara | 2556660 | Fiksuotas datos veiksmingumo patikrinimas, atliekamas kainoraštyje, pridėtame prie projekto parametrų įrašo. |
|  Galimybių valdymas | 2369202 | Pataisė verslo logiką, kuri patikrina, ar kainoraščiai, kurių įgyvendinimo datos sutampa, gali būti pridedami prie tos pačios projekto sutarties. |
|  Galimybių valdymas | 2385965 | Ištaisė elgesį **puslapio Projekto sutartis** skirtuke **Klientai**, kai pasirenkate **Įrašyti ir uždaryti**. |
| Laikas ir išlaidos | 2538503 | Užregistravus išlaidų ataskaitą, **objekte Projekto faktinės** aplinkybės turi būti pasiekiama projekto užduotis. |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Projektų valdymas ir apskaita pagal Dynamics 365 Finance

| Funkcijų sritis | Nuorodos numeris | Kokybės naujinimas |
| --- | --- | --- |
| Projektų valdymas ir apskaita | [615496](https://fix.lcs.dynamics.com/Issue/Details/?bugId=615496) | Importuojant tiekėjo kredito pažymas įvyksta klaida. Klaidos pranešime teigiama: "Užlaikymo suma negali būti didesnė už likusią grynąją sumą". |
| Projektų valdymas ir apskaita | [619391](https://fix.lcs.dynamics.com/Issue/Details/?bugId=619391) | Jei SF pasiūlyme yra bet kokių nulinės sumos mokesčio operacijų, kurios yra neapmokėtos pardavimo faktinės sumos, SF išrašymo negalima. |
| Projektų valdymas ir apskaita | [624423](https://fix.lcs.dynamics.com/Issue/Details/?bugId=624423) | Atnaujinus pirkimo kainą ir **įgalinus aktyvinti keitimų valdymą**, užregistruotos išlaidos yra neteisingos.|
| Projektų valdymas ir apskaita | [628386](https://fix.lcs.dynamics.com/Issue/Details/?bugId=628386) | Fiksuotos kainos projekto registravimo įvertinimas naudoja neteisingą įvertinimo kvito valiutą ir sumą, net jei **įgalinta įvertinimo skaičiavimo** funkcija Įgalinti projekto sutarties valiutą. |
| Projektų valdymas ir apskaita | [629239](https://fix.lcs.dynamics.com/Issue/Details/?bugId=629239) | **ProjDMFDataPopulation\_ Plėtinys** neturėtų skambinti, kad įgalintų keitimų stebėjimą, neužfiksuodamas išimčių objektams, turintiems konfigūracijos raktus, kurie nėra įgalinti. |
| Projektų valdymas ir apskaita | [623818](https://fix.lcs.dynamics.com/Issue/Details/?bugId=623818) | Paketinė užduotis nustatoma, kai registruojami keli išplėstiniai žurnalai ir įvyksta klaida. |
| Kelionės ir išlaidos | [616805](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616805) | Dėl atsiskaitymo išdavimo, susijusio su grynųjų pinigų avansais išlaidų ataskaitose, mokesčių suma nėra padengiama kaip grynųjų pinigų avanso dalis. |
| Kelionės ir išlaidos | [616959](https://fix.lcs.dynamics.com/Issue/Details/?bugId=616959) | PVM informacija neįtraukta į **ataskaitą Išlaidos - Užregistruotos operacijos**. |
| Kelionės ir išlaidos | [618943](https://fix.lcs.dynamics.com/Issue/Details/?bugId=618943) | Kvitų **reikalaujamas** išlaidų strategijos pažeidimas neteisingai rodo įspėjimą apie išlaidų ataskaitas. |
| Kelionės ir išlaidos | [633470](https://fix.lcs.dynamics.com/Issue/Details/?bugId=633470) | Į projekto operaciją neįtraukiamas negrąžinamas PVM į bendrą pardavimo sumą, kai operacija yra ridos išlaidų rezultatas. |
| Kelionės ir išlaidos | [642979](https://fix.lcs.dynamics.com/Issue/Details/?bugId=642979) | Kai detali eilutė turi mokestį, negalite keisti detalizavimo eilutės datos ir įvyksta šaltinio dokumento būsenos klaida. |

## <a name="removed-and-deprecated-features"></a>Pašalintos ir nebenaudojamos funkcijos

Straipsnyje Pašalintos [arba nebenaudojamos "Project Operations](removed-depreciated-features-project.md) " funkcijos aprašomos funkcijos, kurios buvo pašalintos arba nebenaudojamos Dynamics 365 Project Operations.

- Pašalinta funkcija nebepasiekiama naudojantis šiuo produktu.
- Nebenaudojama funkcija nėra aktyviai kuriama ir gali būti pašalinta ateityje atnaujinant.

Pranešimas apie nusidėvėjimą bus rodomas "Project Operations [" straipsnio pašalintose](removed-depreciated-features-project.md) arba nebenaudojamose funkcijose likus 12 mėnesių iki bet kurios funkcijos pašalinimo iš produkto.

Jei norite nutraukti pakeitimus, kurie turi įtakos tik kompiliavimo laikui, bet yra dvejetainiai, suderinami su smėlio dėže ir gamybos aplinkomis, nusidėvėjimo laikas bus trumpesnis nei 12 mėnesių. Paprastai šie pakeitimai yra funkciniai naujinimai, kuriuos reikia atlikti kompiliatoriui.
