---
title: „Project Operations“ dvigubo rašymo integravimas
description: Šiame straipsnyje pateikiama "Project Operations" dvigubo rašymo integravimo apžvalga.
author: sigitac
ms.date: 04/28/2021
ms.topic: overview
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d365a036f96ff4f7b14107b43e8c6b70df0b5362
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8927982"
---
# <a name="project-operations-dual-write-integration-overview"></a>„Project Operations“ dvigubo rašymo integravimo apžvalga

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

"Project Operations" naudoja [dvigubo rašymo galimybes](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page), kad sinchronizuotų duomenis visoje Microsoft Dataverse ir Dynamics 365 Finance.

Toliau pateiktoje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami atliekant šį „Dataverse“ ir „Finance“ integravimą.

![„Project Operations“ duomenų srautų apžvalga.](./media/ProjectOperationsFlows.jpg)

„Project Operations“ naudojant „Dataverse“ suteikia modernią vartotojo sąsają (UI) ir lengvo išplėtimo galimybę nenaudojant kodo / naudojant nedaug kodo ir taikant „Power Platform“ galimybes. Pasitelkę „Project Operations“ naudodami „Dataverse“, savo veiklą vykdo projektų vadovai, išteklių vadovai, projekto komandų nariai ir kiti vadovaujantieji asmenys.

„Project Operations“ naudojant „Finance“ palaiko projektų apskaitos ir pajamų pripažinimo galimybę. „Project Operations“ papildo „Finance“ finansinę sistemą, kad būtų galima apskaičiuoti PVM, valiutos kursus, teikti finansinių išlaidų ataskaitas ir kt. Projektų buhalterių funkcijos daugiausia pagrįstos sprendimu „Finance“.

„Project Operations“ integravimą sudaro toliau nurodytų komponentų integravimas.


- [„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas](resource-dual-write-setup-integration.md) 
- [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md)
- [Projektų sąskaitos faktūros](resource-dual-write-project-invoice.md)
- [Išlaidų valdymas](resource-dual-write-expense.md)
- [Tiekėjo sąskaita faktūra](resource-dual-write-vendor-invoice.md)
