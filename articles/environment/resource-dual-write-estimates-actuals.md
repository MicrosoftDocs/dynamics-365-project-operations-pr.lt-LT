---
title: Projektų įvertinimų ir faktinių duomenų integravimas
description: Šioje temoje pateikiama informacijos apie „Project Operations“ projektų įvertinimų ir faktinių duomenų dvigubo rašymo integravimą.
author: sigitac
ms.date: 4/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d8aa1541a3560db175acead1d000895312b299db
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000041"
---
# <a name="project-estimates-and-actuals-integration"></a>Projektų įvertinimų ir faktinių duomenų integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikiama informacijos apie „Project Operations“ projektų įvertinimų ir faktinių duomenų dvigubo rašymo integravimą.

## <a name="project-estimates"></a>Projekto įvertinimai

Projektų darbo, išlaidų ir medžiagų įvertinimai kuriami bei tvarkomi naudojant „Microsoft Dataverse“ ir apskaitos tikslais sinchronizuojami su „Finance and Operations“ programomis. Naudojant „Finance and Operations“ programas, kūrimo, naujinimo ir naikinimo operacijos nepalaikomos.

Norint kurti įvertinimus, reikia tinkamos projekto apskaitos konfigūracijos. Su sutarties eilutėmis susieti projektai turi turėti tinkamą projekto kaštų ir pajamų profilį, apibrėžtą projekto kaštų ir pajamų profilių taisyklėse. Norėdami sužinoti daugiau, žr. [Apmokėtinų projektų apskaitos konfigūravimas](../project-accounting/configure-accounting-billable-projects.md#configure-project-cost-and-revenue-profile-rules).

## <a name="labor-estimates"></a>Darbo įvertinimai

Darbo įvertinimus sukuria projekto vadovas arba išteklių vadovas, kuris taip pat projekto užduočiai priskiria bendrąjį arba įvardytąjį išteklių. Išteklių priskyrimo įrašus galima peržiūrėti „Dataverse“ skirtuko **Išteklių priskyrimai** puslapyje **Išsami projekto informacija**. Naudodami **„Project Operations“ integravimo objektą, skirtą valandų įvertinimams (msdyn\_resourceassignments)**, „Dataverse“ išteklių priskyrimo įrašai „Finance and Operations“ programose sukuria valandų prognozių įrašus.

   ![Darbo įvertinimų integravimas](./Media/DW4LaborEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja išteklių priskyrimo įrašus su eilučių paruošimo lentele (**ProjCDSKurdsKurdIngSImport**), o tada naudoja verslo logiką valandų prognozių įrašams kurti ir naujinti (**ProjForecastEmpl**).

Projektų buhalteris peržiūri „Finance and Operations“ programose sukurtus prognozių valandų įrašus nueidamas į **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Planas** > **Valandų prognozės**.

## <a name="expense-estimates"></a>Išlaidų sąmatos

Išlaidų įvertinimus projekto vadovas sukuria „Dataverse“ puslapio **Išsami projekto informacija** skirtuke **Išlaidų įvertinimai**. Išlaidų įvertinimų įrašai saugomi „Dataverse“ objekte **Įvertinimo eilutė**. Šiems įvertinimų įrašams priskirta operacijų klasė **Išlaidos** ir jie sinchronizuojami su išlaidų prognozių įrašais „Finance and Operations“ programose naudojant **„Project Operations“ integravimo objektą, skirtą išlaidų įvertinimams (msdyn \_estimatelines)**.

   ![Išlaidų įvertinimų integravimas](./Media/DW4ExpenseEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja išlaidų įvertinimų įrašus su eilučių paruošimo lentele (**ProjCDSEstimateExpenseImport**), o tada naudoja verslo logiką išlaidų prognozių įrašams kurti ir naujinti (**ProjForecastCost**). Įvertinimo eilutėse pardavimo įvertinimų ir kaštų įvertinimų įrašai saugomi atskirai. „Finance and Operations“ programų verslo logika automatiškai įveda vieną išlaidų prognozės įrašą naudodama šią išsamią informaciją eilučių paruošimo lentelėje.

Projektų buhalteris gali peržiūrėti išlaidų prognozių įrašus „Finance and Operations“ programose nueidamas į **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Planas** > **Išlaidų prognozės**.

## <a name="material-estimates"></a>Medžiagų įvertinimai

Medžiagų įvertinimus projekto vadovas sukuria „Dataverse“ puslapio **Išsami projekto informacija** skirtuke **Medžiagų įvertinimai**. Medžiagų įvertinimų įrašai saugomi „Dataverse“ objekte **Įvertinimo eilutė**. Šiems įvertinimų įrašams priskirta operacijų klasė **Medžiaga** ir jie sinchronizuojami su prekių prognozių įrašais „Finance and Operations“ programose naudojant **„Project Operations“ integravimo lentelę, skirtą medžiagų įvertinimams (msdyn \_estimatelines)**.

   ![Medžiagų įvertinimų integravimas](./Media/DW4MaterialEstimates.png)

Dvigubo rašymo funkcija sinchronizuoja medžiagų įvertinimų įrašus su eilučių paruošimo lentele (**ProjForecastSalesImpor**), o tada naudoja verslo logiką prekių prognozių įrašams kurti ir naujinti (**ForecastSales**). Įvertinimo eilutėse pardavimo įvertinimų ir kaštų įvertinimų įrašai saugomi atskirai. „Finance and Operations“ programų verslo logika automatiškai įveda vieną prekės prognozės įrašą naudodama šią išsamią informaciją eilučių paruošimo lentelėje.

Projektų buhalteris gali peržiūrėti prekių prognozių įrašus „Finance and Operations“ programose nueidamas į **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Planas** > **Prekių prognozės**.

## <a name="project-actuals"></a>Projekto faktiniai duomenys

Projekto faktiniai duomenys sprendime „Dataverse“ kuriami pagal laiką, išlaidas, medžiagą ir atsiskaitymo veiklą. Šiame „Dataverse“ objekte užfiksuojami visi šių operacijų atributai, įskaitant kiekį, savikainą, pardavimo kainą ir projektą. Norėdami gauti daugiau informacijos, žr. [Faktiniai duomenys](../actuals/actuals-overview.md). Faktiniai įrašai sinchronizuojami su „Finance and Operations“ programomis naudojant dvigubo rašymo lentelės schemą **„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)**, skirtą tolimesnei apskaitai.

   ![Faktinių duomenų integravimas](./Media/DW4Actuals.png)

Lentelės schema **„Project Operations“ integravimo faktiniai duomenys** sinchronizuoja visus „Dataverse“ objekto **Faktiniai duomenys** įrašus, kai atributas **Praleisti sinchronizavimą (naudoti tik viduje)** nustatytas kaip **Klaidinga**. Ši atributo reikšmė sprendime „Dataverse“ nustatoma automatiškai, kuriant įrašą. Toliau pateikti pavyzdžiai, kai šis atributas nustatytas kaip **Teisinga**.

  - Projekto kaštų faktiniai duomenys apie vidinės įmonės operacijas. Norėdami sužinoti daugiau, žr. [Vidinės įmonės operacijų kūrimas](../project-accounting/create-intercompany-transactions.md). Šie įrašai praleidžiami, nes, užregistravus vidinės įmonės tiekėjo sąskaitą faktūrą, „Finance and Operations“ programose sistema iš naujo sukuria projekto kaštų faktinius duomenis.
  - Neigiami pardavimo, už kurį neišrašyta sąskaita, įrašai sukuriami patvirtinus išankstinę sąskaitą faktūrą. Šie įrašai praleidžiami, nes „Finance and Operations“ programų projekto papildoma didžioji knyga neatšaukia pardavimo, už kurį neišrašyta sąskaita, kai išrašoma sąskaita faktūra, bet pakeičia būseną į už visą sumą išrašytos sąskaitos faktūros.

Dvigubo rašymo lentelės schema faktinių duomenų įrašus sinchronizuoja su įrašų paruošimo lentele **ProjCDSActualsImport**. Šiuos įrašus apdoroja periodinis procesas **Importavimas iš įrašų paruošimo lentelės**, kai kuriamos „Project Operations“ integravimo žurnalo eilutės ir projekto sąskaitų faktūrų pasiūlymų eilutės. Norėdami sužinoti daugiau, žr. [„Project Operations“ integravimo žurnalas](../project-accounting/project-operations-integration-journal.md).

„Dataverse“ taip pat užfiksuoja ryšius tarp projekto faktinių operacijų objekte **Operacijos ryšys**. Norėdami sužinoti daugiau, žr. [Faktinių duomenų susiejimas su pradiniais įrašais](../actuals/linkingactuals.md). Saitai tarp faktinių operacijų taip pat sinchronizuojami su „Finance and Operations“ programomis naudojant dvigubo rašymo lentelės schemą **Projekto operacijų ryšių integravimo objektas (msdyn \_transactionconnections)**. Šiuos įrašus naudoja periodinis procesas **Importavimas iš įrašų paruošimo lentelės**, kai kuriamos „Project Operations“ integravimo žurnalo eilutės ir projekto sąskaitų faktūrų pasiūlymų eilutės.

Registruojant „Project Operations“ integravimo žurnalą ir projekto sąskaitos faktūros pasiūlymą, paleidžiamas atitinkamų įrašų, esančių jų paruošimo lentelėje **ProjCDSActualsImport**, naujinimas. Sistema užfiksuoja ir įrašo toliau nurodytus faktinių duomenų operacijų apskaitos atributus.

- Apskaitos suma
- Valiutos kursas
- Kvito numeris
- PVM suma

Naudodama šią informaciją, lentelės schema **„Project Operations“ integravimo faktiniai duomenys** atnaujina atitinkamus faktinių duomenų įrašus sprendime „Dataverse“.
