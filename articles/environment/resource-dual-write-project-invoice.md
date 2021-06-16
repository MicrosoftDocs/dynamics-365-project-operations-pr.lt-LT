---
title: Projekto sąskaitų faktūrų integravimas
description: Šioje temoje pateikiama informacijos apie „Project Operations“ dvigubo rašymo integravimą klientų sąskaitoms faktūroms teikti.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 102a7cdba467a2071119c5b32d2e75e48170c783
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955795"
---
# <a name="project-invoice-integration"></a>Projekto sąskaitų faktūrų integravimas

Šioje temoje pateikiama informacijos apie „Project Operations“ dvigubo rašymo integravimą klientų sąskaitoms faktūroms teikti.

Naudodamas „Project Operations“ projektų vadovas tvarko nebaigtas projektų atsiskaitymo užduotis ir sprendime „Microsoft Dataverse“ klientui sukuria išankstinę sąskaitą faktūrą. Pagal šią išankstinę sąskaitą faktūrą gautinų sumų klerkas arba projekto buhalteris sukuria klientui skirtą sąskaitą faktūrą. Dvigubo rašymo integravimo funkcija užtikrina, kad išsami informacija apie išankstinę sąskaitą faktūrą būtų sinchronizuojama su „Finance and Operations“ programomis. Kai klientui skirta sąskaita faktūra užregistruojama, sistema atitinkamo projekto faktinius duomenis sprendime „Dataverse“ atnaujina išsamia apskaitos informacija. Toliau pateiktame grafiniame elemente pateikiama aukšto lygio konceptuali šio integravimo apžvalga.

   ![Projekto sąskaitų faktūrų integravimas](./media/DW5Invoicing.png)

Kai projekto vadovas patvirtina išankstinę sąskaitą faktūrą naudodamas „Dataverse“, išankstinės sąskaitos faktūros antraštės informacija sinchronizuojama su „Finance and Operations“ programomis naudojant dvigubo rašymo lentelės schemą **Projekto sąskaitos faktūros pasiūlymas V2 (sąskaitos faktūros)**. Tai – vienkryptis integravimas iš „Dataverse“ į „Finance and Operations“ programas. Projektų sąskaitų faktūrų pasiūlymų tiesioginio kūrimo arba naikinimo naudojant „Finance and Operations“ programas galimybė nėra palaikoma.

Patvirtinant sąskaitas faktūras sprendime „Dataverse“, taip pat paleidžiama verslo logika, kad objekte **Faktiniai duomenys** būtų kuriami su atsiskaitymu susiję įrašai. Šie įrašai sinchronizuojami su „Finance and Operations“ naudojant dvigubo rašymo lentelės schemą **„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)**. Norėdami sužinoti daugiau, žr. [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md). 

Projekto sąskaitų faktūrų pasiūlymų eilutės kuriamos naudojant periodinį procesą **Importavimas iš eilučių paruošimo lentelės**. Šis procesas pagrįstas pardavimo, už kurį išrašyta sąskaita faktūra, faktinių duomenų informacija, pateikta lentelėje **Faktinių duomenų paruošimas**. Norėdami sužinoti daugiau, žr. [Projektų sąskaitų faktūrų pasiūlymų tvarkymas](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 