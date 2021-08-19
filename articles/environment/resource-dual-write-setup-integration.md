---
title: „Project Operations“ sąrankos ir konfigūracijos duomenų integravimas
description: Šioje temoje pateikiama informacijos apie „Project Operations“ dvigubo rašymo schemų nustatymą ir konfigūravimą.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 6d263f7c5ef0d562edde6a603340a3b8746195df190fdb527bfa40297f68eed2
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986546"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikiama informacijos apie „Project Operations“ sąrankos ir konfigūracijos objektų dvigubo rašymo integravimą.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektų sutartys, sutarčių eilutės ir projektai

Projektų sutartys, sutarčių eilutės ir projektai kuriami sprendime „Dataverse“ bei sinchronizuojami su „Finance and Operations“ programomis papildomai apskaitai atlikti. Šių objektų įrašus galima kurti ir naikinti tik naudojant „Dataverse“. Tačiau į šiuos „Finance and Operations“ programų įrašus galima įtraukti apskaitos atributus, pvz., numatytąsias PVM grupių reikšmes ir finansines dimensijas.

  ![Projektų sutarčių integravimo sąvokos.](./media/1ProjectContract.jpg)

Galimi pardavimo veiklos klientai, galimybės ir pasiūlymai sekami sprendime „Dataverse“ ir nesinchronizuojami su „Finance and Operations“ programomis, nes su šia veikla nėra susietos tolimesnės apskaitos.

„Dataverse“ projektų sutarčių funkcija sukuria projekto sutarties įrašą „Finance and Operations“ programose naudodama lentelės schemą **Projektų sutarčių antraštės (salesorders)**. Įrašius projekto sutartį sprendime „Dataverse“, taip pat paleidžiamas projekto sutarties kliento objekto įrašo kūrimas. Šis įrašas sinchronizuojamas su „Finance and Operations“ programomis naudojant lentelės schemą **Projekto finansavimo šaltinis (msdyn\_projectcontractssplitbillingrules)**. Ši schema taip pat sinchronizuoja projekto sutarties klientų įtraukimus, naujinimus ir naikinimus. Išskaidymo atsiskaitymo procentai tarp projekto sutarties klientų valdomi tik sprendime „Dataverse“ ir nėra sinchronizuojami su „Finance and Operations“ programomis.

Kai projekto sutartis sukuriama naudojant „Dataverse“, projekto buhalteris gali atnaujinti šios projekto sutarties apskaitos atributus „Finance and Operations“ programose nuėjęs į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Nustatymas** > **Rodyti numatytąją apskaitą**. Buhalteris gali peržiūrėti projekto sutarties operacijų atributus, pvz., pageidaujamą pristatymo datą ir sutarties sumą, pasirinkdamas projekto sutarties ID „Finance and Operations“ programose, taip atidarydamas susijusį projekto sutarties įrašą sprendime „Dataverse“.

Projekto objektas sinchronizuojamas su „Finance and Operations“ programomis naudojant lentelės schemą **Projektai V2 (msdyn\_projects)**. Projekto buhalteris gali atlikti toliau nurodytas užduotis.

  - Peržiūrėti projektus „Finance and Operations“ programose, nueidamas į **Projektų tvarkymas ir apskaita** > **Visi projektai**. 
  - Atnaujinti projekto apskaitos atributus „Finance and Operations“ programose nueidamas į **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Nustatymas** > **Rodyti numatytąją apskaitą**.  
  - Peržiūrėti projektų operacijų atributus, pvz., numatomas pradžios ir pabaigos datas, pasirinkdamas projekto ID „Finance and Operations“ programose, taip susijusį projekto įrašą atidarydamas sprendime „Dataverse“.

Projektą galima susieti su projekto sutartimi naudojant objektą **Projekto sutarties eilutė**.

„Dataverse“ projektų sutarčių eilutės sukuria projekto sutarties atsiskaitymo taisyklę „Finance and Operations“ programose naudodamos lentelės schemą **Projektų sutarčių eilutės (salesorderdetails)**. Atsiskaitymo metodas apibrėžia projektų sutarčių atsiskaitymo taisyklių tipą „Finance and Operations“ programose, kaip nurodyta toliau.

  - Projektų sutarčių eilutėse, kuriose naudojamas laiko ir medžiagų atsiskaitymo metodas, sukuriama laiko ir medžiagų tipo atsiskaitymo taisyklė.
  - Fiksuotos kainos atsiskaitymo metodo sutarčių eilutėse sukuriama etapų tipo atsiskaitymo taisyklė.

Projektų sutarčių eilutes projekto buhalteris gali peržiūrėti „Finance and Operations“ programose nueidamas į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Nustatymas** > **Rodyti numatytąją apskaitą** ir peržiūrėdamas išsamią informaciją skirtuke **Sutarčių eilutės**. Šiame skirtuke buhalteris taip pat gali nustatyti numatytąsias fiksuotos kainos atsiskaitymo metodo sutarčių eilučių finansines dimensijas.

## <a name="billing-milestones"></a>Atsiskaitymo etapai

Projektų sutarčių eilutėms, kuriose naudojamas fiksuotos kainos atsiskaitymo metodas, sąskaitos faktūros išrašomos taikant atsiskaitymo etapus. Atsiskaitymo etapai „Finance and Operations“ programose sinchronizuojami su projektų sąskaitų operacijomis naudojant lentelės schemą **„Project Operations“ integravimo sutarčių eilučių etapai (msdyn\_contractlinescheduleofvalues)**.

  ![Atsiskaitymo etapų integravimas.](./media/2Milestones.jpg)

Buhalteris gali peržiūrėti sąskaitų operacijas ir koreguoti šių operacijų apskaitos atributus nueidamas į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Tvarkymas** > **Sąskaitų operacijos** arba **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Tvarkymas** > **Sąskaitų operacijos**.

Jums pirmą kartą sukūrus konkrečios projekto sutarties eilutės atsiskaitymo etapą, sistema automatiškai sukuria su šia sutarties eilute susijusio projekto fiksuotos kainos pajamų įvertinimo projektą. Fiksuotos kainos pajamų įvertinimo projektus galima peržiūrėti nuėjus į **Projektų tvarkymas ir apskaita** > **Fiksuotos kainos pajamų įvertinimo projektai**.

### <a name="project-tasks"></a>Projekto užduotys

Projektų užduotys su „Finance and Operations“ programomis tik informaciniais tikslais sinchronizuojamos naudojant lentelės schemą **Projekto užduotys (msdyn\_projecttasks)**. Naudojant „Finance and Operations“ programas, kūrimo, naujinimo ir naikinimo operacijos nepalaikomos.

  ![Projektų užduočių integravimas.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektų ištekliai

Objektas **Projektų išteklių vaidmenys** tik informaciniais tikslais su „Finance and Operations“ programomis sinchronizuojamas naudojant lentelės schemą **Visų įmonių projektų išteklių vaidmenys (bookableresourcecategories)**. Kadangi „Dataverse“ išteklių vaidmenys nėra skirti konkrečioms įmonėms, sistema „Finance and Operations“ programose automatiškai sukuria atitinkamus konkrečių įmonių išteklių vaidmenų įrašus visiems juridiniams subjektams, įtrauktiems į dvigubo rašymo integravimo aprėptį.

![Išteklių vaidmenų integravimas.](./media/5Resources.jpg)

„Project Operations“ projektų ištekliai tvarkomi sprendime „Dataverse“ ir nesinchronizuojami su „Finance and Operations“ programomis.

### <a name="transaction-categories"></a>Operacijų kategorijos

Operacijų kategorijos tvarkomos sprendime „Dataverse“ ir sinchronizuojamos su „Finance and Operations“ programomis naudojant lentelės schemą **Projektų operacijų kategorijos (msdyn\_transactioncategories)**. Kai sinchronizuojamas operacijų kategorijos įrašas, sistema automatiškai sukuria keturis bendrai naudojamus kategorijos įrašus. Kiekvienas įrašas atitinka „Finance and Operations“ programų operacijų tipą ir jį susieja su operacijų kategorijos įrašu.

![Operacijų kategorijų integravimas.](./media/4TransactionCategories.jpg)

Norėdamas operacijų kategorijas naudoti įvertinimams ir faktiniams duomenims, projekto buhalteris arba sistemos administratorius kiekviename juridiniame subjekte turi sukurti atitinkamas projektų kategorijas. Norėdami sužinoti daugiau, žr. [Projektų kategorijų konfigūravimas](../project-accounting/configure-project-categories.md).
