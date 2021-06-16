---
title: „Project Operations“ dvigubo rašymo schemos versijos
description: Šioje temoje pateikiamas dvigubo rašymo schemų, reikalingų naudojant „Dynamics 365 Project Operations“, sąrašas.
author: sigitac
manager: Annbe
ms.date: 04/22/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fa0342985f2c860cd3cb3f686f0dcaa59d8cfd41
ms.sourcegitcommit: bc51629df94c164325cf2afee387d0e7cda66da7
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/23/2021
ms.locfileid: "5939016"
---
# <a name="project-operations-dual-write-map-versions"></a>„Project Operations“ dvigubo rašymo schemos versijos

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Norint „Dynamics 365 Project Operations“ naudoti išteklių / atsargose nelaikomų medžiagų scenarijams, aplinkoje turi veikti tam tikros dvigubo rašymo schemos. 

## <a name="prerequisite-maps-dual-write-orchestration-solution"></a>Būtinosios schemos: dvigubo rašymo tvarkymo sprendimas

Toliau nurodytos schemos yra būtinieji sprendimo „Project Operations“ komponentai. Įsitikinkite, kad savo aplinkoje naudojate toliau pateiktoje lentelėje išvardytas ir susijusias lentelių schemas.

| Lentelės schema | Pradinis sinchronizavimas |
| --- | --- |
| Didžioji knyga (msdyn_ledgers) | Reikia iš pradžių sinchronizuoti lentelės schemą ir visus būtinuosius komponentus. Pradinio sinchronizavimo šablonas yra „Finance and Operations“ programos. |
| Juridiniai subjektai (cdm_companies) | Nebūtina. Sistema šį objektą įveda automatiškai, kai aplinkos yra susiejamos naudojant dvigubo rašymo funkciją. |
| Klientai V3 (accounts) | Konfigūruojant naudoti nebūtina. |
| Tiekėjai V2 (msdyn_vendors) | Konfigūruojant naudoti nebūtina. |

1. Schemų sąraše pasirinkite Didžioji knyga **(msdyn\_ledgers)** schemą su visomis būtinosiomis sąlygomis ir pažymėkite žymės langelį **Pradinis sinchronizavimas**. Tiek didžiosios knygos schemos, tiek visų būtinųjų schemų lauke **Pradinio sinchronizavimo šablonas** pasirinkite **„Finance and Operations“ programos**. Pasirinkite **Vykdyti**.

![Didžiosios knygos struktūros sinchronizavimas](media/DW6.png)

1. Tuos pačius veiksmus atlikite su visomis likusiomis lentelių schemomis, išvardytomis pirmiau pateiktoje lentelėje. Paleisdami šias schemas nepažymėkite žymės langelio **Pradinis sinchronizavimas**.

## <a name="project-operations-dual-write-maps"></a>„Project Operations“ dvigubo rašymo schemos

Toliau nurodytos schemos yra reikalingos naudojant sprendimą „Project Operations“.

| **Objekto schema** | **Naujausia versija** | **Pradinis sinchronizavimas** |
| --- | --- | --- |
| Projekto operacijų ryšių integravimo objektas (msdyn\_transactionconnections) | 1.0.0.0 | Konfigūruojant naudoti nebūtina. |
| Projekto sutarčių antraštės (pardavimo užsakymai) | 1.0.0.1 | Konfigūruojant naudoti nebūtina. |
| Projekto sutarties eilutės (salesorderdetails) | 1.0.0.0 | Konfigūruojant naudoti nebūtina. |
| Projekto finansavimo šaltinis (msdyn_projectcontractsplitbillingrules) | 1.0.0.1 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo lentelė, skirta medžiagų įvertinimams (msdyn\_estimatelines) | 1.0.0.0 | Konfigūruojant naudoti nebūtina. |
| Projekto sąskaitų faktūrų pasiūlymai V2 (sąskaitos faktūros) | 1.0.0.2 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo faktiniai duomenys (msdyn_actuals) | 1.0.0.14 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo sutarties eilučių etapai (msdyn_contractlinesscheduleofvalues) | 1.0.0.4 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo objektas, skirtas išlaidų įvertinimams (msdyn_estimateslines) | 1.0.0.2 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo objektas, skirtas valandų įvertinimams (msdyn_resourceassignments) | 1.0.0.5 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integracijos projekto išlaidų kategorijų eksportavimo objektas (msdyn_expensecategories) | 1.0.0.2 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo projekto išlaidų eksportavimo objektas (msdyn_expenses) | 1.0.0.2 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų faktūrų eksportavimo objektas (msdyn_projectvendorinvoices) | 1.0.0.0 | Konfigūruojant naudoti nebūtina. |
| „Project Operations“ integravimo projekto tiekėjų sąskaitų eilučių eksportavimo objektas (msdyn_projectvendorinvoicelines) | 1.0.0.0 | Konfigūruojant naudoti nebūtina. |
| Projekto išteklių vaidmenys visoms įmonėms (bookableresourcecategories) | 1.0.0.1 | Norint, kad lentelės schema sinchronizuotų projektų vadovo ir komandos nario išteklių vaidmenis, kurie konfigūruojant įvedami „Dynamics 365“ „Dataverse“ aplinkoje, reikia atlikti pradinį sinchronizavimą. „Dataverse“ yra pagrindinis pradinio sinchronizavimo šaltinis. |
| Projektų užduotys (msdyn_projecttasks) | 1.0.0.4 | Konfigūruojant naudoti nebūtina. |
| Projektų operacijų kategorijos (msdyn_transactioncategories) | 1.0.0.0 | Konfigūruojant naudoti nebūtina. |
| Projektai V2 (msdyn_projects) | 1.0.0.1 | Konfigūruojant naudoti nebūtina. |

Norėdami paleisti išvardytas schemas, atlikite toliau nurodytus veiksmus.

1. Įjunkite **visų įmonių (bookableresourcecategories)** lentelės schemos projekto išteklių vaidmenis, nes šią schemą reikia iš pradžių sinchronizuoti. Lauke **Pradinio sinchronizavimo šablonas** pasirinkite **„Common Data Service“**. 

 ![Išteklių vaidmenų lentelės schemos sinchronizavimas](media/6ResourceInitialSync.jpg)

 Prieš pereidami prie kito veiksmo palaukite, kol schemos būsena bus **Vykdoma**.

2. Pasirinkite visas likusias reikiamas schemas. Jas galite filtruoti dvigubo rašymo schemų sąraše naudodami raktažodį **Projektas** ieškodami viršutiniame dešiniajame kampe. Galite pasirinkti kelias schemas, o tada jas paleisti. Norėdami sužinoti daugiau, žr. [Kelių lentelių schemų tvarkymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/multiple-entity-maps). Būtinai taip pat įjunkite ir vykdykite susijusias objektų schemas.

### <a name="project-operations-dual-write-map-versions"></a>„Project Operations“ dvigubo rašymo schemos versijos

Savo aplinkoje visada vykdykite naujausią schemos versiją. Esant bet kuriai iš toliau nurodytų sąlygų, tam tikros funkcijos ir galimybės gali veikti netinkamai.

- Schema nesuaktyvinta.
- Nesuaktyvinta naujausia schemos versija. 
- Nesuaktyvintos susijusios lentelių schemos.

Aktyvią schemos versiją galite peržiūrėti puslapio **Dvigubas rašymas** stulpelyje **Versija**. Suaktyvinti naują schemos versiją galite pasirinkdami **Lentelės schemos versijos**, tada – naujausią versiją, tada pasirinktą versiją įrašydami. Jei tinkinote parengtą naudoti lentelės schemą, pakeitimus turėsite pritaikyti iš naujo. Norėdami sužinoti daugiau, žr. [Programų ciklo valdymas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management).