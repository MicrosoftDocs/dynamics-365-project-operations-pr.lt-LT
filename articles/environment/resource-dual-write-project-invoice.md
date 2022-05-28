---
title: Projekto sąskaitų faktūrų integravimas
description: Šioje temoje pateikiama informacijos apie „Project Operations“ dvigubo rašymo integravimą klientų sąskaitoms faktūroms teikti.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581248"
---
# <a name="project-invoice-integration"></a>Projekto sąskaitų faktūrų integravimas

Šioje temoje pateikiama informacijos apie „Project Operations“ dvigubo rašymo integravimą klientų sąskaitoms faktūroms teikti.

Naudodamas „Project Operations“ projektų vadovas tvarko nebaigtas projektų atsiskaitymo užduotis ir sprendime „Microsoft Dataverse“ klientui sukuria išankstinę sąskaitą faktūrą. Pagal šią išankstinę sąskaitą faktūrą gautinų sumų klerkas arba projekto buhalteris sukuria klientui skirtą sąskaitą faktūrą. Dvigubo rašymo integravimas užtikrina, kad proforma sąskaitos faktūros informacija būtų sinchronizuojama su "Finance and Operations" programomis. Kai klientui skirta sąskaita faktūra užregistruojama, sistema atitinkamo projekto faktinius duomenis sprendime „Dataverse“ atnaujina išsamia apskaitos informacija. Toliau pateiktame grafiniame elemente pateikiama aukšto lygio konceptuali šio integravimo apžvalga.

   ![Projekto sąskaitų faktūrų integravimas.](./media/DW5Invoicing.png)

Po to, kai projekto vadovas patvirtina proforma SF Dataverse, proforma SF antraštės informacija sinchronizuojama su "Finance and Operations" programomis naudojant dvigubo rašymo lentelės struktūrą, **projekto SF pasiūlymą V2 (SF)**. Tai yra vienpusė integracija iš Dataverse į "Finance and Operations" programas. Projekto SF pasiūlymų kūrimas arba naikinimas tiesiogiai "Finance and Operations" programose nepalaikomas.

Patvirtinant sąskaitas faktūras sprendime „Dataverse“, taip pat paleidžiama verslo logika, kad objekte **Faktiniai duomenys** būtų kuriami su atsiskaitymu susiję įrašai. Šie įrašai sinchronizuojami su "Finance and Operations" naudojant dvigubo rašymo lentelės schemą, **"Project Operations" integravimo faktinius duomenis (msdyn\_ actuals).** Norėdami sužinoti daugiau, žr. [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md). 

Projekto sąskaitų faktūrų pasiūlymų eilutės kuriamos naudojant periodinį procesą **Importavimas iš eilučių paruošimo lentelės**. Šis procesas pagrįstas pardavimo, už kurį išrašyta sąskaita faktūra, faktinių duomenų informacija, pateikta lentelėje **Faktinių duomenų paruošimas**. Norėdami sužinoti daugiau, žr. [Projektų sąskaitų faktūrų pasiūlymų tvarkymas](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
