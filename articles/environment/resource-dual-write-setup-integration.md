---
title: „Project Operations“ sąrankos ir konfigūracijos duomenų integravimas
description: Šioje temoje pateikiama informacijos apie „Project Operations“ dvigubo rašymo schemų nustatymą ir konfigūravimą.
author: sigitac
ms.date: 4/23/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1ffa25ff36c39010d6aee31d928c3eaa0086c3d8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8586906"
---
# <a name="project-operations-setup-and-configuration-data-integration"></a>„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikiama informacijos apie „Project Operations“ sąrankos ir konfigūracijos objektų dvigubo rašymo integravimą.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektų sutartys, sutarčių eilutės ir projektai

Projekto sutartys, sutarčių eilutės ir projektai kuriami Dataverse ir sinchronizuojami su "Finance and Operations" programomis, kad būtų galima atlikti papildomą apskaitą. Šių objektų įrašus galima kurti ir naikinti tik naudojant „Dataverse“. Tačiau apskaitos atributus, pvz., PVM grupės numatytąsias reikšmes ir finansines dimensijas, galima įtraukti į šiuos įrašus programose "Finance and Operations".

  ![Projektų sutarčių integravimo sąvokos.](./media/1ProjectContract.jpg)

Pardavimo veiklos galimi klientai, galimybės ir pasiūlymai yra stebimi ir nesinchronizuojami Dataverse su "Finance and Operations" programomis, nes nėra su šia veikla susijusios tolesnės apskaitos.

Projekto sutarties funkcija Dataverse sukuria projekto sutarties įrašą "Finance and Operations" programose, naudodama **"Project" sutarties antraščių (pardavimo užsakymų)** lentelės struktūrą. Įrašius projekto sutartį sprendime „Dataverse“, taip pat paleidžiamas projekto sutarties kliento objekto įrašo kūrimas. Šis įrašas sinchronizuojamas su "Finance and Operations" programomis naudojant **lentelės "Project" finansavimo šaltinio (msdyn\_ projectcon contracttssplitbillingrules)** žemėlapį. Ši schema taip pat sinchronizuoja projekto sutarties klientų įtraukimus, naujinimus ir naikinimus. Perskirti atsiskaitymo procentus tarp projekto sutarties klientų yra įsisavinami tik Dataverse ir nesinchronizuojami su "Finance and Operations" programomis.

Sukūrus Dataverse projekto sutartį programoje, projekto buhalteris gali atnaujinti šios projekto sutarties apskaitos atributus "Finance and Operations" programose, eidamas į **Projektų valdymo ir apskaitos** > **projektų sutartis** > **Nustatyti** > **numatytąją apskaitą**. Buhalteris gali peržiūrėti veiklos projekto sutarties atributus, pvz., pageidaujamą pristatymo datą ir sutarties sumą, pasirinkdamas projekto sutarties ID programose "Finance and Operations", kuri atidaro susijusį projekto sutarties įrašą programoje Dataverse.

Projekto objektas sinchronizuojamas su "Finance and Operations" programomis naudojant **lentelės "Projektai V2" (msdyn\_ projektai)** struktūrą. Projekto buhalteris gali atlikti toliau nurodytas užduotis.

  - Peržiūrėkite projektus finansų ir operacijų programose, eidami į **projektų valdymą ir apskaitą** > **Visi projektai**. 
  - Atnaujinkite projekto apskaitos atributus "Finance and Operations" programose, eidami į **Projektų valdymas ir apskaita** > **Visi projektai** > **Nustatyti** > **rodyti numatytąją apskaitą**.  
  - Peržiūrėkite veiklos projekto atributus, pvz., numatomas pradžios ir pabaigos datas, pasirinkdami projekto ID programose "Finance and Operations", kuri atidaro susijusį projekto įrašą programoje Dataverse.

Projektą galima susieti su projekto sutartimi naudojant objektą **Projekto sutarties eilutė**.

Projekto sutarties eilutės sukuria Dataverse projekto sutarties atsiskaitymo taisyklę "Finance and Operations" programose, naudojant **lentelių struktūrą Projekto sutarties eilutės (salesorderdetails).** Atsiskaitymo metodas apibrėžia projekto sutarties atsiskaitymo taisyklės tipą "Finance and Operations" programose:

  - Projektų sutarčių eilutėse, kuriose naudojamas laiko ir medžiagų atsiskaitymo metodas, sukuriama laiko ir medžiagų tipo atsiskaitymo taisyklė.
  - Fiksuotos kainos atsiskaitymo metodo sutarčių eilutėse sukuriama etapų tipo atsiskaitymo taisyklė.

Projekto sutarčių eilutes projekto buhalteris gali peržiūrėti "Finance and Operations" programose, eidamas į **Projektų valdymo ir apskaitos** > **projekto sutartis** > **Nustatyti** > **numatytąją apskaitą** ir peržiūrėdamas išsamią informaciją skirtuke **Sutarties eilutės** . Buhalteris šiame skirtuke taip pat gali nustatyti numatytąsias fiksuotos kainos atsiskaitymo metodo sutarties eilučių finansines dimensijas.

## <a name="billing-milestones"></a>Atsiskaitymo etapai

Projektų sutarčių eilutėms, kuriose naudojamas fiksuotos kainos atsiskaitymo metodas, sąskaitos faktūros išrašomos taikant atsiskaitymo etapus. Atsiskaitymo etapai sinchronizuojami su projekto laisvos formos sąskaitos operacijomis "Finance and Operations" programose naudojant **lentelių žemėlapį "Project Operations" integravimo sutarties eilutės orientyrai (msdyn\_ contractlineschedule ofvalues).**

  ![Atsiskaitymo etapų integravimas.](./media/2Milestones.jpg)

Buhalteris gali peržiūrėti sąskaitų operacijas ir koreguoti šių operacijų apskaitos atributus nueidamas į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Tvarkymas** > **Sąskaitų operacijos** arba **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Tvarkymas** > **Sąskaitų operacijos**.

Jums pirmą kartą sukūrus konkrečios projekto sutarties eilutės atsiskaitymo etapą, sistema automatiškai sukuria su šia sutarties eilute susijusio projekto fiksuotos kainos pajamų įvertinimo projektą. Fiksuotos kainos pajamų įvertinimo projektus galima peržiūrėti nuėjus į **Projektų tvarkymas ir apskaita** > **Fiksuotos kainos pajamų įvertinimo projektai**.

### <a name="project-tasks"></a>Projekto užduotys

Projekto užduotys sinchronizuojamos su "Finance and Operations" programomis naudojant **lentelę "Project tasks" (msdyn\_ projecttasks)** tik nuorodos tikslais. Operacijų kūrimas, naujinimas ir naikinimas nepalaikomas naudojant "Finance and Operations" programas.

  ![Projektų užduočių integravimas.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektų ištekliai

Projekto **išteklių vaidmenų** objektas sinchronizuojamas su "Finance and Operations" programomis, naudojant **"Project" išteklių vaidmenis visoms įmonėms (bookableresourcecategories)** lentelės struktūrą tik nuorodos tikslais. Kadangi išteklių vaidmenys Dataverse nėra susiję su įmone, sistema automatiškai sukuria atitinkamus konkrečios įmonės išteklių vaidmenų įrašus "Finance and Operations" programose automatiškai visiems juridiniams subjektams, įtrauktiems į dvigubo rašymo integravimo aprėptį.

![Išteklių vaidmenų integravimas.](./media/5Resources.jpg)

Projekto ištekliai "Project Operations" yra prižiūrimi Dataverse ir nesinchronizuojami su "Finance and Operations" programomis.

### <a name="transaction-categories"></a>Operacijų kategorijos

Operacijų kategorijos tvarkomos Dataverse ir sinchronizuojamos su "Finance and Operations" programomis naudojant **"Project" operacijų kategorijų (msdyn\_ transactioncategories)** lentelės struktūrą. Kai sinchronizuojamas operacijų kategorijos įrašas, sistema automatiškai sukuria keturis bendrai naudojamus kategorijos įrašus. Kiekvienas įrašas atitinka operacijos tipą "Finance and Operations" programose ir susieja juos su operacijos kategorijos įrašu.

![Operacijų kategorijų integravimas.](./media/4TransactionCategories.jpg)

Norėdamas operacijų kategorijas naudoti įvertinimams ir faktiniams duomenims, projekto buhalteris arba sistemos administratorius kiekviename juridiniame subjekte turi sukurti atitinkamas projektų kategorijas. Norėdami sužinoti daugiau, žr. [Projektų kategorijų konfigūravimas](../project-accounting/configure-project-categories.md).
