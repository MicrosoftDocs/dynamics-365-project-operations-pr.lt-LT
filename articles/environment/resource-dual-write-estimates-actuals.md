---
title: Projektų įvertinimų ir faktinių duomenų integravimas
description: Šioje temoje pateikiama informacijos apie „Project Operations“ projektų įvertinimų ir faktinių duomenų dvigubo rašymo integravimą.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 5aaa59020427438fa6ebab3789fbb70c5b86e272
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8577200"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektų įvertinimų ir faktinių duomenų integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikiama informacijos apie „Project Operations“ projektų įvertinimų ir faktinių duomenų dvigubo rašymo integravimą.

## <a name="project-estimates"></a>Projekto įvertinimai

Projekto darbo, išlaidų ir medžiagų įvertinimai sukuriami ir prižiūrimi Microsoft Dataverse bei sinchronizuojami su "Finance and Operations" programomis apskaitos tikslais. Kurti, naujinti ir naikinti operacijas nepalaikomos naudojant "Finance and Operations" programas.

Norint kurti įvertinimus, reikia tinkamos projekto apskaitos konfigūracijos. Su sutarties eilutėmis susieti projektai turi turėti tinkamą projekto kaštų ir pajamų profilį, apibrėžtą projekto kaštų ir pajamų profilių taisyklėse. Norėdami sužinoti daugiau, žr. [Apmokėtinų projektų apskaitos konfigūravimas](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Darbo įvertinimai

Darbo įvertinimus sukuria projekto vadovas arba išteklių vadovas, kuris taip pat projekto užduočiai priskiria bendrąjį arba įvardytąjį išteklių. Išteklių priskyrimo įrašus galima peržiūrėti „Dataverse“ skirtuko **Išteklių priskyrimai** puslapyje **Išsami projekto informacija**. Išteklių priskyrimo įrašai Dataverse kuriant valandų prognozės įrašus "Finance and Operations" programose, naudojant **"Project Operations" integravimo objektą valandų įvertinimams (msdyn\_ resourceassignments)**.

   ![Darbo įvertinimų integravimas.](./Media/DW4LaborEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja išteklių priskyrimo įrašus su eilučių paruošimo lentele (**ProjCDSKurdsKurdIngSImport**), o tada naudoja verslo logiką valandų prognozių įrašams kurti ir naujinti (**ProjForecastEmpl**).

Projekto apskaitininkas peržiūri prognozės valandų įrašus, sukurtus "Finance and Operations" programose, eidamas į **projektų valdymą ir apskaitą** > **Visi projektai** > **Planuoja** > **valandų prognozes**.

## <a name="expense-estimates"></a>Išlaidų sąmatos

Išlaidų įvertinimus projekto vadovas sukuria „Dataverse“ puslapio **Išsami projekto informacija** skirtuke **Išlaidų įvertinimai**. Išlaidų įvertinimų įrašai saugomi „Dataverse“ objekte **Įvertinimo eilutė**. Šie įvertinimo įrašai turi operacijų klasę, **Išlaidas** ir yra sinchronizuojami su išlaidų prognozės įrašais "Finance and Operations" programose, naudojant **"Project Operations" integravimo objektą išlaidų sąmatoms (msdyn\_ sąmatos eilutės)**.

   ![Išlaidų įvertinimų integravimas.](./Media/DW4ExpenseEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja išlaidų įvertinimų įrašus su eilučių paruošimo lentele (**ProjCDSEstimateExpenseImport**), o tada naudoja verslo logiką išlaidų prognozių įrašams kurti ir naujinti (**ProjForecastCost**). Įvertinimo eilutėse pardavimo įvertinimų ir kaštų įvertinimų įrašai saugomi atskirai. Verslo logika "Finance and Operations" programose užpildo vieną išlaidų prognozės įrašą, naudodama šią išsamią informaciją sustojimo lentelėje.

Projekto buhalteris gali peržiūrėti išlaidų prognozės įrašus "Finance and Operations" programose, eidamas į **projektų valdymą ir apskaitą** > **Visi projektai** > **Planuoti** > **išlaidų prognozes**.

## <a name="material-estimates"></a>Medžiagų įvertinimai

Medžiagų įvertinimus projekto vadovas sukuria „Dataverse“ puslapio **Išsami projekto informacija** skirtuke **Medžiagų įvertinimai**. Medžiagų įvertinimų įrašai saugomi „Dataverse“ objekte **Įvertinimo eilutė**. Šie įvertinimo įrašai turi operacijų klasę, **Medžiagą** ir yra sinchronizuojami su prekių prognozės įrašais "Finance and Operations" programose, naudojant **"Project" integravimo lentelę medžiagų įvertinimams (msdyn\_ estimatelines)**.

   ![Medžiagų įvertinimų integravimas.](./Media/DW4MaterialEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja medžiagų įvertinimų įrašus su eilučių paruošimo lentele (**ProjForecastSalesImpor**), o tada naudoja verslo logiką prekių prognozių įrašams kurti ir naujinti (**ForecastSales**). Įvertinimo eilutėse pardavimo įvertinimų ir kaštų įvertinimų įrašai saugomi atskirai. Verslo logika "Finance and Operations" programose užpildo vieną elemento prognozės įrašą, naudodama šią išsamią informaciją įtraukimo lentelėje.

Projekto apskaitininkas gali peržiūrėti prekių prognozės įrašus "Finance and Operations" programose, eidamas į **Projektų valdymas ir apskaita** > **Visi projektai** > **Planuoti** > **prekių prognozes**.

## <a name="project-actuals"></a>Projekto faktiniai duomenys

Projekto faktiniai duomenys sprendime „Dataverse“ kuriami pagal laiką, išlaidas, medžiagą ir atsiskaitymo veiklą. Šiame „Dataverse“ objekte užfiksuojami visi šių operacijų atributai, įskaitant kiekį, savikainą, pardavimo kainą ir projektą. Norėdami gauti daugiau informacijos, žr. [Faktiniai duomenys](../actuals/actuals-overview.md). Faktiniai įrašai sinchronizuojami su "Finance and Operations" programomis, naudojant dvigubo rašymo lentelės žemėlapį **"Project Operations" integravimo faktiniai duomenys (msdyn\_ faktiniai duomenys)** pasroviui.

   ![Faktinių duomenų integravimas.](./Media/DW4Actuals.png)

Lentelės schema **„Project Operations“ integravimo faktiniai duomenys** sinchronizuoja visus „Dataverse“ objekto **Faktiniai duomenys** įrašus, kai atributas **Praleisti sinchronizavimą (naudoti tik viduje)** nustatytas kaip **Klaidinga**. Ši atributo reikšmė sprendime „Dataverse“ nustatoma automatiškai, kuriant įrašą. Toliau pateikti pavyzdžiai, kai šis atributas nustatytas kaip **Teisinga**.

  - Projekto kaštų faktiniai duomenys apie vidinės įmonės operacijas. Norėdami sužinoti daugiau, žr. [Vidinės įmonės operacijų kūrimas](../project-accounting/create-intercompany-transactions.md). Šie įrašai praleidžiami, nes sistema atkuria projekto savikainą, faktinę finansų ir operacijų programose, kai užregistruojama vidinės įmonės tiekėjo SF.
  - Neigiami pardavimo, už kurį neišrašyta sąskaita, įrašai sukuriami patvirtinus išankstinę sąskaitą faktūrą. Šie įrašai praleidžiami, nes "Finance and Operations" programų projekto subklasteris neatšaukia neaprašyto pardavimo įrašo išrašant SF, bet pakeičia būseną į visiškai išrašytą SF.

Dvigubo rašymo lentelės schema faktinių duomenų įrašus sinchronizuoja su įrašų paruošimo lentele **ProjCDSActualsImport**. Šiuos įrašus apdoroja periodinis procesas **Importavimas iš įrašų paruošimo lentelės**, kai kuriamos „Project Operations“ integravimo žurnalo eilutės ir projekto sąskaitų faktūrų pasiūlymų eilutės. Norėdami sužinoti daugiau, žr. [„Project Operations“ integravimo žurnalas](../project-accounting/project-operations-integration-journal.md).

„Dataverse“ taip pat užfiksuoja ryšius tarp projekto faktinių operacijų objekte **Operacijos ryšys**. Norėdami sužinoti daugiau, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](../actuals/linkingactuals.md). Ryšiai tarp faktinių operacijų taip pat sinchronizuojami su "Finance" ir "Operations" programomis, naudojant dvigubo rašymo lentelės schemą, **projekto operacijų ryšių integravimo objektą (msdyn\_ transactionconnections)**. Šiuos įrašus naudoja periodinis procesas **Importavimas iš įrašų paruošimo lentelės**, kai kuriamos „Project Operations“ integravimo žurnalo eilutės ir projekto sąskaitų faktūrų pasiūlymų eilutės.

Registruojant „Project Operations“ integravimo žurnalą ir projekto sąskaitos faktūros pasiūlymą, paleidžiamas atitinkamų įrašų, esančių jų paruošimo lentelėje **ProjCDSActualsImport**, naujinimas. Sistema užfiksuoja ir įrašo toliau nurodytus faktinių duomenų operacijų apskaitos atributus.

- Apskaitos suma
- Valiutos kursas
- Kvito numeris
- PVM suma

Naudodama šią informaciją, lentelės schema **„Project Operations“ integravimo faktiniai duomenys** atnaujina atitinkamus faktinių duomenų įrašus sprendime „Dataverse“.
