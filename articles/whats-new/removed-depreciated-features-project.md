---
title: Pašalintos arba nerekomenduojamos „Dynamics 365 Project Operations“ funkcijos
description: Šiame straipsnyje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Project Operations“.
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
# <a name="removed-or-deprecated-features-in-dynamics-365-project-operations"></a>Pašalintos arba nerekomenduojamos „Dynamics 365 Project Operations“ funkcijos

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite” versijos visuotinis diegimas – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo, ir „Project Operations“, skirta laikomų medžiagų / gamyba pagrįstiems scenarijams_

Šiame straipsnyje aprašomos funkcijos, kurios buvo pašalintos arba kurias planuojama pašalinti iš „Dynamics 365 Project Operations“.

- *Pašalinta* funkcija nebepasiekiama naudojantis šiuo produktu.
- *Nerekomenduojama* funkcija nėra aktyviai programuojama ir gali būti pašalinta būsimuose atnaujinimuose.

Šis sąrašas yra skirtas tam, kad planuodami galėtumėte atsižvelgti į šias pašalintas ir nerekomenduojamas funkcijas.

> [!NOTE]
> Detalios informacijos apie finansų ir operacijų programų objektus galite rasti [**techninės informacijos ataskaitose**](/dynamics/s-e/global/axtechrefrep_61). Galite palyginti skirtingas šių ataskaitų versijas, kad sužinotumėte apie objektus, kurie buvo pakeisti ar pašalinti kiekvienoje iš finansų ir operacijų programų versijų.

## <a name="features-removed-or-deprecated-in-the-project-operations-march-2022-release"></a>Pašalintos arba nerekomenduojamos „Project Operations“ 2022 m. kovo leidimo funkcijos

### <a name="project-management-and-accounting-always-create-adjustment-transaction-parameter"></a>Projektų valdymo ir apskaitos parametras "Visada kurti koregavimo operaciją"

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Koregavimo operacijos, kurias reikia apdoroti, yra būtinos auditui. Nebenaudojamas šis parametras bus paslėptas. Sistema visada kurs koregavimo operacijas taip pat, kaip šiuo metu, kai parametras bus nustatytas kaip **Taip**. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | „Project Operations“, skirta laikomų medžiagų / gamybos scenarijams |
| **Būsena** | Nebenaudojama: iki 2023 m. kovo 1 d. paslėpsime parametrą ir pakeisime sistemos veikimą, kad būtų visada kuriamos koregavimo operacijos. |

### <a name="project-management-and-accounting-use-adjustment-date-as-new-project-date-parameter"></a>Projekto valdymo ir apskaitos parametras „Naudoti koregavimo datą kaip naują projekto datą"

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Šis parametras iš pradžių buvo naudojamas tam, kad būtų galima koreguoti, kai ataskaitinis laikotarpis buvo uždarytas. Tačiau tai nebereikalinga, nes jei operacijos apskaitos data sukonfigūruota, ją galima pakeisti į pirmąją atviro laikotarpio datą. Projekto datos keisti negalima, nes ji atitinka operacijos datą. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | „Project Operations“, skirta laikomų medžiagų / gamybos scenarijams |
| **Būsena** | Nebenaudojama: iki 2023 m. kovo 1 d. paslėpsime parametrą ir pakeisime sistemos veikimą, kad projekto data nesikeistų pagal koregavimus. |

### <a name="resource-request-workflow-in-project-operations-for-stockedproduction-based-scenarios"></a>„Project Operations“, skirtos laikomų medžiagų / gamyba pagrįstiems scenarijams, išteklių prašymo darbo eiga

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nerekomenduojama dėl žemo naudojimo ir transakcijos apimties apribojimų. |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | „Project Operations“, skirta laikomų medžiagų / gamybos scenarijams |
| **Būsena** | Nerekomenduojama: iki 2023 m. kovo 1 d. išjungsime parinktį reikalauti projekto išteklių naudodami darbo eigą. |

### <a name="project-invoice-proposal-page-without-header-and-lines-views"></a>Projekto sąskaitų faktūrų sąrašymo puslapis be antraščių ir eilučių rodinių

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nerekomenduojama dėl puslapio, kuris buvo pristatytas kartu su **Projekto sąskaitų faktūrų pasiūlymu ir sąskaitų faktūrų žurnalo formomis su rodinio antraštės ir eilutės** funkcijų raktu, patobulinimų. |
| **Pakeičiama kita funkcija?** | Taip |
| **Paveiktos produkto sritys** | Programa |
| **Visuotinio diegimo parinktis** | "Project Operations", skirta gamybos / atsargų scenarijams; „Project Operations for resource" / ne atsargų scenarijai |
| **Būsena** | Nerekomenduojama: iki 2023 m. kovo 1 d. išjungsime ankstesnę (senesnę) puslapio versiją ir įjungsime funkcijos **Naudoti projekto sąskaitų faktūrų pasiūlymą ir sąskaitų faktūrų žurnalo formas su rodiniu Antraštės ir Eilutės** raktą pagal numatytuosius nustatymus. |

## <a name="features-removed-or-deprecated-in-the-project-operations-december-2021-release"></a>Pašalintos arba nerekomenduojamos „Project Operations“ 2021 m. gruodžio mėn. leidimo funkcijos

### <a name="collaboration-workspaces"></a>Bendradarbiavimas darbo srityse

[Bendradarbiavimo darbo srities kūrimas arba siejimas (projektas)](/dynamicsax-2012/appuser-itpro/create-or-link-to-a-collaboration-workspace-project)

| &nbsp; | &nbsp; |
|--------|--------|
| **Priežastys, dėl kurių funkcijos yra nerekomenduojamos / pašalinamos** | Nerekomenduojama dėl to, kad mažai naudojama. Klientai, naudojantys „Project Operations" ištekliams / ne atsargų scenarijams, gali naudoti [Bendradarbiavimą su „Office Groups"](../project-management/collaboration-groups.md). |
| **Pakeičiama kita funkcija?** | No |
| **Paveiktos produkto sritys** | Programa  |
| **Visuotinio diegimo parinktis** | „Project Operations“, skirta laikomų medžiagų / gamybos scenarijams |
| **Būsena** | Nerekomenduojaama: iki 2022 m. gruodžio 1 d. planuojame nebepalaikyti bendradarbiavimo darbo sričių. |
