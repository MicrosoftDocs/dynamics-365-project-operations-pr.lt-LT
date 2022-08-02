---
title: Projektų įvertinimų ir faktinių duomenų integravimas
description: Šiame straipsnyje pateikiama informacija apie "Project Operations" dvigubo rašymo integravimą, skirtą projekto įverčiams ir faktinėms aplinkybėms.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: dc8f65aec6f2328ccef5f9591a0f4d9c792b0d8f
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029090"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektų įvertinimų ir faktinių duomenų integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šiame straipsnyje pateikiama informacija apie "Project Operations" dvigubo rašymo integravimą, skirtą projekto įverčiams ir faktinėms aplinkybėms.

## <a name="project-estimates"></a>Projekto įvertinimai

Projekto darbo, išlaidų ir medžiagų įvertinimai kuriami, prižiūrimi Microsoft Dataverse ir sinchronizuojami su finansų ir operacijų programomis apskaitos tikslais. Kūrimo, naujinimo ir naikinimo operacijos nepalaikomos naudojant finansų ir operacijų programas.

Norint kurti įvertinimus, reikia tinkamos projekto apskaitos konfigūracijos. Su sutarties eilutėmis susieti projektai turi turėti tinkamą projekto kaštų ir pajamų profilį, apibrėžtą projekto kaštų ir pajamų profilių taisyklėse. Norėdami sužinoti daugiau, žr. [Apmokėtinų projektų apskaitos konfigūravimas](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Darbo įvertinimai

Darbo įvertinimus sukuria projekto vadovas arba išteklių vadovas, kuris taip pat projekto užduočiai priskiria bendrąjį arba įvardytąjį išteklių. Išteklių priskyrimo įrašus galima peržiūrėti „Dataverse“ skirtuko **Išteklių priskyrimai** puslapyje **Išsami projekto informacija**. Išteklių priskyrimo įrašai Dataverse kuriant valandų prognozių įrašus finansų ir operacijų programose naudojant **"Project Operations" integravimo objektą valandų įverčiams (msdyn\_ resourceassignments)**.

   ![Darbo įvertinimų integravimas.](./Media/DW4LaborEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja išteklių priskyrimo įrašus su eilučių paruošimo lentele (**ProjCDSKurdsKurdIngSImport**), o tada naudoja verslo logiką valandų prognozių įrašams kurti ir naujinti (**ProjForecastEmpl**).

"Project" buhalteris peržiūri prognozių valandų įrašus, sukurtus finansų ir operacijų programose, eidamas į **Projektų valdymas ir apskaita** > **Visi projektai** > **Plano** > **valandos prognozės**.

## <a name="expense-estimates"></a>Išlaidų sąmatos

Išlaidų įvertinimus projekto vadovas sukuria „Dataverse“ puslapio **Išsami projekto informacija** skirtuke **Išlaidų įvertinimai**. Išlaidų įvertinimų įrašai saugomi „Dataverse“ objekte **Įvertinimo eilutė**. Šie įvertinimų įrašai turi operacijų klasę, **išlaidas** ir yra sinchronizuojami su išlaidų prognozės įrašais finansų ir operacijų programose, naudojant **"Project Operations" integravimo objektą išlaidų įvertinimui (msdyn\_ įvertinimo eilutės)**.

   ![Išlaidų įvertinimų integravimas.](./Media/DW4ExpenseEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja išlaidų įvertinimų įrašus su eilučių paruošimo lentele (**ProjCDSEstimateExpenseImport**), o tada naudoja verslo logiką išlaidų prognozių įrašams kurti ir naujinti (**ProjForecastCost**). Įvertinimo eilutėse pardavimo įvertinimų ir kaštų įvertinimų įrašai saugomi atskirai. Verslo logika finansų ir operacijų programose užpildo vieną išlaidų prognozės įrašą, naudodama šią išsamią informaciją išdėstymo lentelėje.

Projekto buhalteris gali peržiūrėti išlaidų prognozės įrašus finansų ir operacijų programose nuėjęs į **Projekto valdymas ir apskaita** > **Visi projektai** > **Plano** > **išlaidų prognozės**.

## <a name="material-estimates"></a>Medžiagų įvertinimai

Medžiagų įvertinimus projekto vadovas sukuria „Dataverse“ puslapio **Išsami projekto informacija** skirtuke **Medžiagų įvertinimai**. Medžiagų įvertinimų įrašai saugomi „Dataverse“ objekte **Įvertinimo eilutė**. Šie įvertinimų įrašai turi operacijų klasę, **Medžiagą** ir yra sinchronizuojami su prekių prognozės įrašais finansų ir operacijų programose naudojant **projekto integravimo lentelę, skirtą reikšmingiems įverčiams (msdyn\_ estimatelines)**.

   ![Medžiagų įvertinimų integravimas.](./Media/DW4MaterialEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja medžiagų įvertinimų įrašus su eilučių paruošimo lentele (**ProjForecastSalesImpor**), o tada naudoja verslo logiką prekių prognozių įrašams kurti ir naujinti (**ForecastSales**). Įvertinimo eilutėse pardavimo įvertinimų ir kaštų įvertinimų įrašai saugomi atskirai. "Finance and operations" programų verslo logika užpildo vieną elemento prognozės įrašą naudodama šią išsamią informaciją išdėstymo lentelėje.

Projekto buhalteris gali peržiūrėti elementų prognozės įrašus finansų ir operacijų programose, nuėjęs į **Projekto valdymas ir apskaita** > **Visi projektai** > **Plano** > **elementų prognozės**.

## <a name="project-actuals"></a>Projekto faktiniai duomenys

Projekto faktiniai duomenys sprendime „Dataverse“ kuriami pagal laiką, išlaidas, medžiagą ir atsiskaitymo veiklą. Šiame „Dataverse“ objekte užfiksuojami visi šių operacijų atributai, įskaitant kiekį, savikainą, pardavimo kainą ir projektą. Norėdami gauti daugiau informacijos, žr. [Faktiniai duomenys](../actuals/actuals-overview.md). Faktiniai įrašai sinchronizuojami su finansų ir operacijų programomis naudojant dvigubo rašymo lentelės žemėlapį **"Project Operations" integravimo faktinės sumos (msdyn\_ actuals)** paskesnei apskaitai.

   ![Faktinių duomenų integravimas.](./Media/DW4Actuals.png)

Lentelės schema **„Project Operations“ integravimo faktiniai duomenys** sinchronizuoja visus „Dataverse“ objekto **Faktiniai duomenys** įrašus, kai atributas **Praleisti sinchronizavimą (naudoti tik viduje)** nustatytas kaip **Klaidinga**. Ši atributo reikšmė sprendime „Dataverse“ nustatoma automatiškai, kuriant įrašą. Toliau pateikti pavyzdžiai, kai šis atributas nustatytas kaip **Teisinga**.

  - Projekto kaštų faktiniai duomenys apie vidinės įmonės operacijas. Norėdami sužinoti daugiau, žr. [Vidinės įmonės operacijų kūrimas](../project-accounting/create-intercompany-transactions.md). Šie įrašai praleidžiami, nes sistema iš naujo sukuria faktines projekto išlaidas finansų ir operacijų programose, kai užregistruojama vidinės įmonės tiekėjo SF.
  - Neigiami pardavimo, už kurį neišrašyta sąskaita, įrašai sukuriami patvirtinus išankstinę sąskaitą faktūrą. Šie įrašai praleidžiami, nes projekto antrinė knyga finansų ir operacijų programose nepanaikina neįrašyto pardavimo įrašo sfinge, bet pakeičia būseną į visiškai sąskaitą faktūrą.

Dvigubo rašymo lentelės schema faktinių duomenų įrašus sinchronizuoja su įrašų paruošimo lentele **ProjCDSActualsImport**. Šiuos įrašus apdoroja periodinis procesas **Importavimas iš įrašų paruošimo lentelės**, kai kuriamos „Project Operations“ integravimo žurnalo eilutės ir projekto sąskaitų faktūrų pasiūlymų eilutės. Norėdami sužinoti daugiau, žr. [„Project Operations“ integravimo žurnalas](../project-accounting/project-operations-integration-journal.md).

„Dataverse“ taip pat užfiksuoja ryšius tarp projekto faktinių operacijų objekte **Operacijos ryšys**. Norėdami sužinoti daugiau, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](../actuals/linkingactuals.md). Ryšiai tarp faktinių operacijų taip pat sinchronizuojami su finansų ir operacijų programomis naudojant dvigubo rašymo lentelės žemėlapį, **integravimo objektą projekto operacijų ryšiams (msdyn\_ operacijų jungtys)**. Šiuos įrašus naudoja periodinis procesas **Importavimas iš įrašų paruošimo lentelės**, kai kuriamos „Project Operations“ integravimo žurnalo eilutės ir projekto sąskaitų faktūrų pasiūlymų eilutės.

Registruojant „Project Operations“ integravimo žurnalą ir projekto sąskaitos faktūros pasiūlymą, paleidžiamas atitinkamų įrašų, esančių jų paruošimo lentelėje **ProjCDSActualsImport**, naujinimas. Sistema užfiksuoja ir įrašo toliau nurodytus faktinių duomenų operacijų apskaitos atributus.

- Apskaitos suma
- Valiutos kursas
- Kvito numeris
- PVM suma

Naudodama šią informaciją, lentelės schema **„Project Operations“ integravimo faktiniai duomenys** atnaujina atitinkamus faktinių duomenų įrašus sprendime „Dataverse“.
