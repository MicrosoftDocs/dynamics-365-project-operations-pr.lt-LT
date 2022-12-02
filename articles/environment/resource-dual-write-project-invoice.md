---
title: Projekto sąskaitų faktūrų integravimas
description: Šiame straipsnyje pateikiama informacijos apie „Project Operations“ dvigubo rašymo integravimą klientų sąskaitoms faktūroms teikti.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 61f16ebdbabd6545c09d8d7bd82d99b85dc09975
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029034"
---
# <a name="project-invoice-integration"></a>Projekto sąskaitų faktūrų integravimas

Šiame straipsnyje pateikiama informacijos apie „Project Operations“ dvigubo rašymo integravimą klientų sąskaitoms faktūroms teikti.

Naudodamas „Project Operations“ projektų vadovas tvarko nebaigtas projektų atsiskaitymo užduotis ir sprendime „Microsoft Dataverse“ klientui sukuria išankstinę sąskaitą faktūrą. Pagal šią išankstinę sąskaitą faktūrą gautinų sumų klerkas arba projekto buhalteris sukuria klientui skirtą sąskaitą faktūrą. Dvigubo rašymo integravimo funkcija užtikrina, kad išsami informacija apie išankstinę sąskaitą faktūrą būtų sinchronizuojama su finansų ir operacijų programomis. Kai klientui skirta sąskaita faktūra užregistruojama, sistema atitinkamo projekto faktinius duomenis sprendime „Dataverse“ atnaujina išsamia apskaitos informacija. Toliau pateiktame grafiniame elemente pateikiama aukšto lygio konceptuali šio integravimo apžvalga.

   ![Projekto sąskaitų faktūrų integravimas.](./media/DW5Invoicing.png)

Kai projekto vadovas patvirtina išankstinę sąskaitą faktūrą naudodamas „Dataverse“, išankstinės sąskaitos faktūros antraštės informacija sinchronizuojama su finansų ir operacijų programomis naudojant dvigubo rašymo lentelės schemą **Projekto sąskaitos faktūros pasiūlymas V2 (sąskaitos faktūros)**. Tai – vienkryptis integravimas iš „Dataverse“ į finansų ir operacijų programas. Projektų sąskaitų faktūrų pasiūlymų tiesioginio kūrimo arba naikinimo galimybė naudojant finansų ir operacijų programas nėra palaikoma.

Patvirtinant sąskaitas faktūras sprendime „Dataverse“, taip pat paleidžiama verslo logika, kad objekte **Faktiniai duomenys** būtų kuriami su atsiskaitymu susiję įrašai. Šie įrašai sinchronizuojami su finansais ir operacijomis naudojant dvigubo rašymo lentelės schemą **„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals).** Norėdami sužinoti daugiau, žr. [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md). 

Projekto sąskaitų faktūrų pasiūlymų eilutės kuriamos naudojant periodinį procesą **Importavimas iš eilučių paruošimo lentelės**. Šis procesas pagrįstas pardavimo, už kurį išrašyta sąskaita faktūra, faktinių duomenų informacija, pateikta lentelėje **Faktinių duomenų paruošimas**. Norėdami sužinoti daugiau, žr. [Projektų sąskaitų faktūrų pasiūlymų tvarkymas](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
