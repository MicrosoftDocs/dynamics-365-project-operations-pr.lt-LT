---
title: Projekto sąskaitų faktūrų integravimas
description: Šiame straipsnyje pateikiama informacija apie "Project Operations" dvigubo rašymo integravimą kliento SF išrašymui.
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5ee2d78f1ca1d78f6909d9995a92ac301f06d6a6
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8912112"
---
# <a name="project-invoice-integration"></a>Projekto sąskaitų faktūrų integravimas

Šiame straipsnyje pateikiama informacija apie "Project Operations" dvigubo rašymo integravimą kliento SF išrašymui.

Naudodamas „Project Operations“ projektų vadovas tvarko nebaigtas projektų atsiskaitymo užduotis ir sprendime „Microsoft Dataverse“ klientui sukuria išankstinę sąskaitą faktūrą. Pagal šią išankstinę sąskaitą faktūrą gautinų sumų klerkas arba projekto buhalteris sukuria klientui skirtą sąskaitą faktūrą. Dvigubo rašymo integravimas užtikrina, kad proforma sąskaitos faktūros informacija būtų sinchronizuojama su "Finance and Operations" programomis. Kai klientui skirta sąskaita faktūra užregistruojama, sistema atitinkamo projekto faktinius duomenis sprendime „Dataverse“ atnaujina išsamia apskaitos informacija. Toliau pateiktame grafiniame elemente pateikiama aukšto lygio konceptuali šio integravimo apžvalga.

   ![Projekto sąskaitų faktūrų integravimas.](./media/DW5Invoicing.png)

Po to, kai projekto vadovas patvirtina proforma SF Dataverse, proforma SF antraštės informacija sinchronizuojama su "Finance and Operations" programomis naudojant dvigubo rašymo lentelės struktūrą, **projekto SF pasiūlymą V2 (SF)**. Tai yra vienpusė integracija iš Dataverse į "Finance and Operations" programas. Projekto SF pasiūlymų kūrimas arba naikinimas tiesiogiai "Finance and Operations" programose nepalaikomas.

Patvirtinant sąskaitas faktūras sprendime „Dataverse“, taip pat paleidžiama verslo logika, kad objekte **Faktiniai duomenys** būtų kuriami su atsiskaitymu susiję įrašai. Šie įrašai sinchronizuojami su "Finance and Operations" naudojant dvigubo rašymo lentelės schemą, **"Project Operations" integravimo faktinius duomenis (msdyn\_ actuals).** Norėdami sužinoti daugiau, žr. [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md). 

Projekto sąskaitų faktūrų pasiūlymų eilutės kuriamos naudojant periodinį procesą **Importavimas iš eilučių paruošimo lentelės**. Šis procesas pagrįstas pardavimo, už kurį išrašyta sąskaita faktūra, faktinių duomenų informacija, pateikta lentelėje **Faktinių duomenų paruošimas**. Norėdami sužinoti daugiau, žr. [Projektų sąskaitų faktūrų pasiūlymų tvarkymas](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals). 
