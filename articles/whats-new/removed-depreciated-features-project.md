---
title: Pašalintos arba nebenaudojamos funkcijos Dynamics 365 Project Operations
description: Šiame straipsnyje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš Dynamics 365 Project Operations.
author: sigitac
ms.date: 03/16/2022
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: df9d8a40fa853e72416e64846bf59748815048be
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8921496"
---
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Pašalintos arba nebenaudojamos funkcijos Dynamics 365 Project Operations

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite” versijos visuotinis diegimas – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, ir „Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

Šiame straipsnyje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš Dynamics 365 Project Operations.

- *Pašalinta* funkcija nebepasiekiama naudojantis šiuo produktu.
- *Nerekomenduojama* funkcija nėra aktyviai programuojama ir gali būti pašalinta būsimuose atnaujinimuose.

Šis sąrašas yra skirtas tam, kad planuodami galėtumėte atsižvelgti į šias pašalintas ir nerekomenduojamas funkcijas.

> [!NOTE]
> Išsamią informaciją apie objektus "Finance and Operations" programose galima rasti techninėse informacinėse [**ataskaitose**](/dynamics/s-e/global/axtechrefrep_61). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie pasikeitė arba buvo pašalinti kiekvienoje "Finance and Operations" programų versijoje.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Priemonės, pašalintos arba nebenaudojamos "Project Operations" 2022 m. kovo mėn.

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Parametras Projektų valdymas ir apskaita "Visada kurti koregavimo operaciją"

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Koregavimo operacijos reikalingos audito tikslais. Po nusidėvėjimo šis parametras bus paslėptas. Sistema visada sukurs koregavimo operacijas, kaip ir dabar, kai parametras nustatytas į **Taip**. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Gamybos / sandėliuojamų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: Iki kovo 1 d. mes paslėpsime parametrą ir pakeisime sistemos veikimą, kad visada būtų sukurtos koregavimo operacijos. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Parametras Projektų valdymas ir apskaita "Naudoti koregavimo datą kaip naują projekto datą" parametras

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Šis parametras iš pradžių buvo naudojamas norint atlikti koregavimus uždarius ataskaitinis laikotarpis. Tačiau tai nebereikalinga, nes operacijos apskaitos datą galima pakeisti į pirmąją atviro laikotarpio datą, jei ji sukonfigūruota. Projekto datos keisti negalima, nes ji nurodo operacijos datą. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Gamybos / sandėliuojamų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: Iki kovo 1 d. mes paslėpsime parametrą ir pakeisime sistemos veikimą, kad projekto data niekada nebūtų pakeista koreguojant. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>Išteklių užklausos darbo eiga projekto operacijose, skirtoje sandėliuojamiems / gamybos scenarijams

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nebenaudojama dėl mažo naudojimo ir operacijų apimties apribojimų. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Gamybos / sandėliuojamų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: Iki kovo 1 d. 2023 m. išjungsime galimybę prašyti projekto išteklių naudodami darbo eigą. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projekto SF pasiūlymo puslapis be antraštės ir eilučių rodinių

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nebenaudojamas pagerinus puslapį, kuris buvo įvestas kartu su **formomis Naudoti projekto SF ir SF žurnalą su antraštės ir eilučių rodinio** priemonės raktu. |
| **Pakeičiama kita funkcija?** | Taip |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | Gamybos ir (arba) atsargų scenarijų projekto operacijos; Išteklių / nekauptų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: iki kovo 1 d. išjungsime ankstesnį (senstelėjusį) puslapį ir įjungsime **formas Naudoti projekto SF pasiūlymą ir SF žurnalo formas su antraštės ir eilučių rodinio** funkcijos raktu pagal numatytuosius nustatymus. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Funkcijos pašalintos arba nebenaudojamos "Project Operations" 2021 m. gruodžio mėn.

### <a name="collaboration-workspaces"></a>Bendradarbiavimo darbo sritys

[Bendradarbiavimo darbo srities kūrimas arba susiejimas su ja (projektas)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nebenaudojamas dėl mažo naudojimo. Klientai, naudojantys "Project Operations" išteklių / ne atsargų scenarijams, gali pasinaudoti [bendradarbiavimu su "Office" grupėmis](../project-management/collaboration-groups.md). |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa  |
| **Visuotinio diegimo parinktis** | Gamybos / sandėliuojamų scenarijų projekto operacijos |
| **Būsena** | Nebenaudojama: iki gruodžio 1 d. planuojame nebepalaikyti bendradarbiavimo darbo vietų. |
