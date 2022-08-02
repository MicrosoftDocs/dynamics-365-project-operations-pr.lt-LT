---
title: Pašalintos arba nebenaudojamos funkcijos Dynamics 365 Project Operations
description: Šiame straipsnyje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: f0fbaed028db11d8fb1551d304a40543faf35b0d
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028339"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Pašalintos arba nebenaudojamos funkcijos Dynamics 365 Project Operations

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite” versijos visuotinis diegimas – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, ir „Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

Šiame straipsnyje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš Dynamics 365 Project Operations.

- *Pašalinta* funkcija nebepasiekiama naudojantis šiuo produktu.
- *Nerekomenduojama* funkcija nėra aktyviai programuojama ir gali būti pašalinta būsimuose atnaujinimuose.

Šis sąrašas yra skirtas tam, kad planuodami galėtumėte atsižvelgti į šias pašalintas ir nerekomenduojamas funkcijas.

> [!NOTE]
> Išsamią informaciją apie objektus finansų ir operacijų programose galima rasti techninėse orientacinėse [**ataskaitose**](/dynamics/s-e/global/axtechrefrep_61). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti arba pašalinti kiekvienoje finansų ir operacijų programų versijoje.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Funkcijos, pašalintos arba nebenaudojamos iš "Project Operations" 2022 m. kovo mėn.

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametras Projektų valdymas ir apskaita "Visada kurti koregavimo operaciją"

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Koregavimo operacijos reikalingos audito tikslais. Po nusidėvėjimo šis parametras bus paslėptas. Sistema visada sukurs koregavimo operacijas, kaip ir šiuo metu, kai parametras nustatytas į **Taip**. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Gamybos / atsargų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: iki 2023 m. kovo 1 d. paslėpsime parametrą ir pakeisime sistemos veikimą, kad visada būtų sukurtos koregavimo operacijos. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametras Projektų valdymas ir apskaita "Koregavimo datos kaip naujos projekto datos naudojimas"

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Šis parametras iš pradžių buvo naudojamas, kad būtų galima atlikti koregavimus, kai ataskaitinis laikotarpis buvo uždarytas. Tačiau jis nebereikalingas, nes operacijos apskaitos datą galima pakeisti į pirmąją atidarymo laikotarpio datą, jei ji sukonfigūruota. Projekto data negali būti keičiama, nes ji nurodo datą, kada įvyko operacija. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Gamybos / atsargų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: iki 2023 m. kovo 1 d. paslėpsime parametrą ir pakeisime sistemos elgseną, kad atliekant koregavimus projekto data niekada nebūtų pakeista. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Išteklių užklausos darbo eiga "Project Operations", skirtoje atsargomis / gamyba pagrįstiems scenarijams

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nebenaudojamas dėl mažo naudojimo ir operacijų apimties apribojimų. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Gamybos / atsargų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: iki 2023 m. kovo 1 d. išjungsime parinktį prašyti projekto išteklių naudojant darbo eigą. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projekto sąskaitos faktūros pasiūlymo puslapis be antraštės ir eilučių rodinių

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nebenaudojama dėl puslapio, kuris buvo pristatytas kartu su **pasiūlymu Naudoti projekto sf ir sąskaitų faktūrų žurnalo formas su antraštės ir linijų rodinio** funkcijų klavišu, patobulinimų. |
| **Pakeičiama kita funkcija?** | Taip |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Projekto operacijos, skirtos gamybos / atsargų scenarijams; Išteklių / ne atsargų scenarijų projektų operacijos |
| **Būsena** | Nebenaudojama: iki 2023 m. kovo 1 d. išjungsime ankstesnį (senstelėjusį) puslapį ir įjungsime **pasiūlymą Naudoti projekto sąskaitos faktūros pasiūlymą ir sąskaitų faktūrų žurnalo formas naudodami antraštės ir linijų rodinio** funkcijos klavišą pagal numatytuosius nustatymus. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcijos pašalintos arba nebenaudojamos iš "Project Operations" 2021 m. gruodžio mėn.

### <a name="collaboration-workspaces"></a>Bendradarbiavimo darbo sritys

[Bendradarbiavimo darbo srities kūrimas arba susiejimas su ja ("Project")](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nebenaudojamas dėl mažo naudojimo. Klientai, naudojantys "Project Operations" išteklių / ne atsargų scenarijams, gali panaudoti [bendradarbiavimą su "Office" grupėmis](../project-management/collaboration-groups.md). |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa  |
| **Visuotinio diegimo parinktis** | Gamybos / atsargų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: iki 2022 m. gruodžio 1 d. planuojame nebepalaikyti bendradarbiavimo darbo sričių. |
