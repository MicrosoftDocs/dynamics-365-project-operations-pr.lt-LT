---
title: „Project Operations“ dvigubo rašymo integravimas
description: Šioje temoje apžvelgiamas „Project Operations“ dvigubo rašymo integravimas.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 540b6f74d8e79116e5fdb2ceffaa4bbb487ff08f
ms.sourcegitcommit: 0fafe022731f0e1e8693382ff906e3f8541d34ca
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/07/2021
ms.locfileid: "6368441"
---
# <a name="project-operations-dual-write-integration-overview"></a>„Project Operations“ dvigubo rašymo integravimo apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

„Project Operations“ naudoja [dvigubo rašymo galimybes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) duomenims tarp „Microsoft Dataverse“ ir „Dynamics 365 Finance“ sinchronizuoti.

Toliau pateiktoje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami atliekant šį „Dataverse“ ir „Finance“ integravimą.

![„Project Operations“ duomenų srautų apžvalga](./media/ProjectOperationsFlows.jpg)

„Project Operations“ naudojant „Dataverse“ suteikia modernią vartotojo sąsają (UI) ir lengvo išplėtimo galimybę nenaudojant kodo / naudojant nedaug kodo ir taikant „Power Platform“ galimybes. Pasitelkę „Project Operations“ naudodami „Dataverse“, savo veiklą vykdo projektų vadovai, išteklių vadovai, projekto komandų nariai ir kiti vadovaujantieji asmenys.

„Project Operations“ naudojant „Finance“ palaiko projektų apskaitos ir pajamų pripažinimo galimybę. „Project Operations“ papildo „Finance“ finansinę sistemą, kad būtų galima apskaičiuoti PVM, valiutos kursus, teikti finansinių išlaidų ataskaitas ir kt. Projektų buhalterių funkcijos daugiausia pagrįstos sprendimu „Finance“.

„Project Operations“ integravimą sudaro toliau nurodytų komponentų integravimas.


- [„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas](resource-dual-write-setup-integration.md) 
- [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md)
- [Projektų sąskaitos faktūros](resource-dual-write-project-invoice.md)
- [Išlaidų valdymas](resource-dual-write-expense.md)
- [Tiekėjo sąskaita faktūra](resource-dual-write-vendor-invoice.md)
