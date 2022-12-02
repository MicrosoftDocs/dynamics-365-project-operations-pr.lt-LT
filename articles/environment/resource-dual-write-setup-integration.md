---
title: „Project Operations“ sąrankos ir konfigūracijos duomenų integravimas
description: Šiame straipsnyje pateikiama informacijos apie „Project Operations“ dvigubo rašymo schemų nustatymą ir konfigūravimą.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: d03393de893c39ceb53c06a3031395f765a26f55
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9029162"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šiame straipsnyje pateikiama informacijos apie „Project Operations“ sąrankos ir konfigūracijos objektų dvigubo rašymo integravimą.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektų sutartys, sutarčių eilutės ir projektai

Projekto sutartys, sutarties eilutės ir projektai yra sukurti „Dataverse“ ir sinchronizuoti finansų ir operacijų programoms, papildomai apskaitai. Šių objektų įrašus galima kurti ir naikinti tik naudojant „Dataverse“. Tačiau į šiuos finansų ir operacijų programų įrašus galima įtraukti apskaitos atributus, pvz., numatytąsias pardavimų mokesčių grupių reikšmes ir finansines dimensijas.

  ![Projektų sutarčių integravimo sąvokos.](./media/1ProjectContract.jpg)

Galimos pardavimo veiklos, galimybės ir pasiūlymai sekami „Dataverse“ ir nesinchronizuojami su finansų ir operacijų programomis, nes su šia veikla nėra susietos tolimesnės apskaitos.

„Dataverse“ projektų sutarčių funkcija sukuria projekto sutarties įrašą finansų ir operacijų programose naudodama lentelės schemą **Projektų sutarčių antraštės (salesorders)**. Įrašius projekto sutartį sprendime „Dataverse“, taip pat paleidžiamas projekto sutarties kliento objekto įrašo kūrimas. Šis įrašas sinchronizuojamas su finansų ir operacijų programomis naudojant lentelės schemą **Projekto finansavimo šaltinis (msdyn\_projectcontractssplitbillingrules)**. Ši schema taip pat sinchronizuoja projekto sutarties klientų įtraukimus, naujinimus ir naikinimus. Išskaidymo atsiskaitymo procentai tarp projekto sutarties klientų valdomi tik „Dataverse“ ir nėra sinchronizuojami su finansų ir operacijų programomis.

Kai projekto sutartis sukuriama naudojant „Dataverse“, projekto buhalteris gali atnaujinti šios projekto sutarties apskaitos atributus finansų ir operacijų programose nuėjęs į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Nustatymas** > **Rodyti numatytąją apskaitą**. Buhalteris gali peržiūrėti projekto sutarties operacijų atributus, pvz., pageidaujamą pristatymo datą ir sutarties sumą, pasirinkdamas projekto sutarties ID finansų ir operacijų programose, taip atidarydamas susijusį projekto sutarties įrašą sprendime „Dataverse“.

Projekto objektas sinchronizuojamas su finansų ir operacijų programomis naudojant lentelės schemą **Projektai V2 (msdyn\_projects)**. Projekto buhalteris gali atlikti toliau nurodytas užduotis.

  - Peržiūrėti projektus finansų ir operacijų programose galima nuėjus į **Projektų tvarkymas ir apskaita**  > **Visi projektai**. 
  - Atnaujinti projekto apskaitos atributus finansų ir operacijų programose galima nuėjus į **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Nustatymai** > **Rodyti numatytąją apskaitą**.  
  - Peržiūrėti projektų operacijų atributus, pvz., numatomas pradžios ir pabaigos datas, galima pasirinkus projekto ID finansų ir operacijų programose, taip susijusį projekto įrašą atidarant „Dataverse“.

Projektą galima susieti su projekto sutartimi naudojant objektą **Projekto sutarties eilutė**.

„Dataverse“ projektų sutarčių eilutės sukuria projekto sutarties atsiskaitymo taisyklę finansų ir operacijų programose naudodamos lentelės schemą **Projektų sutarčių eilutės (salesorderdetails)**. Atsiskaitymo metodas apibrėžia projekto sutarties sąskaitų išrašymo taisyklės tipą finansų ir operacijų programose:

  - Projektų sutarčių eilutėse, kuriose naudojamas laiko ir medžiagų atsiskaitymo metodas, sukuriama laiko ir medžiagų tipo atsiskaitymo taisyklė.
  - Fiksuotos kainos atsiskaitymo metodo sutarčių eilutėse sukuriama etapų tipo atsiskaitymo taisyklė.

Projektų sutarčių eilutes projekto buhalteris gali peržiūrėti finansų ir operacijų programose nueidamas į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Nustatymas** > **Rodyti numatytąją apskaitą** ir peržiūrėdamas išsamią informaciją skirtuke **Sutarčių eilutės**. Šiame skirtuke buhalteris taip pat gali nustatyti numatytąsias fiksuotos kainos atsiskaitymo metodo sutarčių eilučių finansines dimensijas.

## <a name="billing-milestones"></a>Atsiskaitymo etapai

Projektų sutarčių eilutėms, kuriose naudojamas fiksuotos kainos atsiskaitymo metodas, sąskaitos faktūros išrašomos taikant atsiskaitymo etapus. Atsiskaitymo etapai finansų ir operacijų programose sinchronizuojami su projektų sąskaitų operacijomis naudojant lentelės schemą **„Project Operations“ integravimo sutarčių eilučių etapus (msdyn\_contractlinescheduleofvalues)**.

  ![Atsiskaitymo etapų integravimas.](./media/2Milestones.jpg)

Buhalteris gali peržiūrėti sąskaitų operacijas ir koreguoti šių operacijų apskaitos atributus nueidamas į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Tvarkymas** > **Sąskaitų operacijos** arba **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Tvarkymas** > **Sąskaitų operacijos**.

Jums pirmą kartą sukūrus konkrečios projekto sutarties eilutės atsiskaitymo etapą, sistema automatiškai sukuria su šia sutarties eilute susijusio projekto fiksuotos kainos pajamų įvertinimo projektą. Fiksuotos kainos pajamų įvertinimo projektus galima peržiūrėti nuėjus į **Projektų tvarkymas ir apskaita** > **Fiksuotos kainos pajamų įvertinimo projektai**.

### <a name="project-tasks"></a>Projekto užduotys

Projektų užduotys su finansų ir operacijų programomis sinchronizuojamos tik informaciniais tikslais, naudojant lentelės schemą **Projekto užduotys (msdyn\_projecttasks)**. Naudojant finansų ir operacijų programas, kūrimo, naujinimo ir naikinimo operacijos nepalaikomos.

  ![Projektų užduočių integravimas.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektų ištekliai

Objektas **Projektų išteklių vaidmenys** su finansų ir operacijų programomis sinchronizuojamas tik informaciniais tikslais, naudojant lentelės schemą **Visų įmonių projektų išteklių vaidmenys (bookableresourcecategories)**. Kadangi išteklių vaidmenys „Dataverse“ nėra specifiški įmonei, sistema automatiškai sukuria atitinkamus, įmonei specifiškus išteklių vaidmenų įrašus finansų ir operacijų programoje visiems teisiniams subjektams įskaitant dvigubo rašymo integracijos aprėptį.

![Išteklių vaidmenų integravimas.](./media/5Resources.jpg)

„Project Operations“ projektų ištekliai tvarkomi „Dataverse“ ir nesinchronizuojami su finansų ir operacijų programomis.

### <a name="transaction-categories"></a>Operacijų kategorijos

Operacijų kategorijos tvarkomos sprendime „Dataverse“ ir sinchronizuojamos su finansų ir operacijų programomis naudojant lentelės schemą **Projektų operacijų kategorijos (msdyn\_transactioncategories)**. Kai sinchronizuojamas operacijų kategorijos įrašas, sistema automatiškai sukuria keturis bendrai naudojamus kategorijos įrašus. Kiekvienas įrašas atitinka finansų ir operacijų programų operacijų tipą ir jį susieja su operacijų kategorijos įrašu.

![Operacijų kategorijų integravimas.](./media/4TransactionCategories.jpg)

Norėdamas operacijų kategorijas naudoti įvertinimams ir faktiniams duomenims, projekto buhalteris arba sistemos administratorius kiekviename juridiniame subjekte turi sukurti atitinkamas projektų kategorijas. Norėdami sužinoti daugiau, žr. [Projektų kategorijų konfigūravimas](../project-accounting/configure-project-categories.md).
