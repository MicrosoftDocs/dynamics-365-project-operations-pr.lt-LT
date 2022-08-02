---
title: „Project Operations“ sąrankos ir konfigūracijos duomenų integravimas
description: Šiame straipsnyje pateikiama informacija apie "Project Operations" dvigubo rašymo žemėlapių nustatymą ir konfigūravimą.
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

Šiame straipsnyje pateikiama informacija apie "Project Operations" dvigubo rašymo integravimą sąrankos ir konfigūravimo objektams.

## <a name="project-contracts-contract-lines-and-projects"></a>Projektų sutartys, sutarčių eilutės ir projektai

Projektų sutartys, sutarčių eilutės ir projektai kuriami Dataverse ir sinchronizuojami su finansų ir operacijų programomis, kad būtų galima atlikti papildomą apskaitą. Šių objektų įrašus galima kurti ir naikinti tik naudojant „Dataverse“. Tačiau apskaitos atributus, pvz., PVM grupės numatytuosius nustatymus ir finansines dimensijas, galima įtraukti į šiuos įrašus finansų ir operacijų programose.

  ![Projektų sutarčių integravimo sąvokos.](./media/1ProjectContract.jpg)

Pardavimo veiklos potencialūs klientai, galimybės ir pasiūlymai yra sekami ir nesinchronizuojami Dataverse su finansų ir operacijų programomis, nes nėra tolesnės apskaitos, susijusios su šia veikla.

Projekto sutarties funkcija Dataverse sukuria projekto sutarties įrašą finansų ir operacijų programose, naudodama lentelės žemėlapį **"Project" sutarčių antraštės (pardavimo užsakymų teikėjai).** Įrašius projekto sutartį sprendime „Dataverse“, taip pat paleidžiamas projekto sutarties kliento objekto įrašo kūrimas. Šis įrašas sinchronizuojamas su finansų ir operacijų programomis naudojant **lentelės žemėlapį Projekto finansavimo šaltinis (msdyn\_ projectcontractssplitbillingrules).** Ši schema taip pat sinchronizuoja projekto sutarties klientų įtraukimus, naujinimus ir naikinimus. Išskaidyti atsiskaitymo procentai tarp projekto sutarties klientų yra valdomi tik Dataverse finansų ir operacijų programose, o ne sinchronizuojami su jomis.

Sukūrus projekto sutartį, projekto buhalteris Dataverse gali atnaujinti šios projekto sutarties apskaitos atributus finansų ir operacijų programose, eidamas į **Projektų valdymas ir apskaita** > **Projekto sutartys** > **Nustatyti rodyti** > **numatytąją apskaitą**. Buhalteris gali peržiūrėti veiklos projekto sutarties atributus, pvz., prašomą pristatymo datą ir sutarties sumą, finansų ir operacijų programose pasirinkdamas projekto sutarties ID, kuris atidaro susijusį projekto sutarties įrašą Dataverse.

Projekto objektas sinchronizuojamas su finansavimo ir operacijų programomis naudojant lentelės žemėlapį **Projektai V2 (msdyn\_ projektai).** Projekto buhalteris gali atlikti toliau nurodytas užduotis.

  - Peržiūrėkite finansų ir operacijų programų projektus eidami į **Projektų valdymas ir apskaita** > **Visi projektai**. 
  - Atnaujinkite projekto apskaitos atributus finansų ir operacijų programose eidami į **Projekto valdymas ir apskaita** > **Visi projektai** > **Nustatyti** > **Rodyti numatytąją apskaitą**.  
  - Peržiūrėkite veiklos projekto atributus, pvz., numatomas pradžios ir pabaigos datas, finansų ir operacijų programose pasirinkdami projekto ID, kuris atidaro susijusį projekto įrašą Dataverse.

Projektą galima susieti su projekto sutartimi naudojant objektą **Projekto sutarties eilutė**.

Projekto sutarčių eilutės sukuria Dataverse projekto sutarties atsiskaitymo taisyklę finansų ir operacijų programose, naudojant lentelės žemėlapį **Projekto sutarties eilutės (salesorderdetails).** Atsiskaitymo metodas apibrėžia projekto sutarties atsiskaitymo taisyklės tipą finansų ir operacijų programose:

  - Projektų sutarčių eilutėse, kuriose naudojamas laiko ir medžiagų atsiskaitymo metodas, sukuriama laiko ir medžiagų tipo atsiskaitymo taisyklė.
  - Fiksuotos kainos atsiskaitymo metodo sutarčių eilutėse sukuriama etapų tipo atsiskaitymo taisyklė.

Projekto sutarties eilutes projekto buhalteris gali peržiūrėti finansų ir operacijų programose, nuėjęs į **Projekto valdymas ir apskaita** > **Projektų sutartys** > **Nustatyti rodyti** > **numatytąją apskaitą** ir peržiūrėjęs išsamią informaciją skirtuke **Sutarties eilutės** . Buhalteris šiame skirtuke taip pat gali nustatyti numatytąsias fiksuotos kainos atsiskaitymo metodo sutarties eilučių finansines dimensijas.

## <a name="billing-milestones"></a>Atsiskaitymo etapai

Projektų sutarčių eilutėms, kuriose naudojamas fiksuotos kainos atsiskaitymo metodas, sąskaitos faktūros išrašomos taikant atsiskaitymo etapus. Atsiskaitymo etapai sinchronizuojami su projekto operacijomis sąskaitoje finansų ir operacijų programose naudojant lentelės žemėlapį **"Project Operations" integravimo sutarties eilutės orientyrai (msdyn\_ contractlinescheduleofvalues).**

  ![Atsiskaitymo etapų integravimas.](./media/2Milestones.jpg)

Buhalteris gali peržiūrėti sąskaitų operacijas ir koreguoti šių operacijų apskaitos atributus nueidamas į **Projektų tvarkymas ir apskaita** > **Projektų sutartys** > **Tvarkymas** > **Sąskaitų operacijos** arba **Projektų tvarkymas ir apskaita** > **Visi projektai** > **Tvarkymas** > **Sąskaitų operacijos**.

Jums pirmą kartą sukūrus konkrečios projekto sutarties eilutės atsiskaitymo etapą, sistema automatiškai sukuria su šia sutarties eilute susijusio projekto fiksuotos kainos pajamų įvertinimo projektą. Fiksuotos kainos pajamų įvertinimo projektus galima peržiūrėti nuėjus į **Projektų tvarkymas ir apskaita** > **Fiksuotos kainos pajamų įvertinimo projektai**.

### <a name="project-tasks"></a>Projekto užduotys

Projekto užduotys sinchronizuojamos su finansų ir operacijų programomis naudojant **lentelės žemėlapį Project tasks (msdyn\_ projecttasks)** tik informaciniais tikslais. Operacijų kūrimas, naujinimas ir naikinimas nepalaikomas naudojant "Finance and Operations" programas.

  ![Projektų užduočių integravimas.](./media/3Tasks.jpg)

## <a name="project-resources"></a>Projektų ištekliai

Objektas **Projekto išteklių vaidmenys** sinchronizuojamas su finansų ir operacijų programomis, naudojant **visų įmonių (rezervuojamų išteklių išteklių vaidmenų)** lentelės žemėlapį tik informaciniais tikslais. Kadangi išteklių vaidmenys Dataverse nėra būdingi konkrečiai įmonei, sistema automatiškai sukuria atitinkamus konkrečios įmonės išteklių vaidmenų įrašus finansų ir operacijų programose visiems juridiniams subjektams, įtrauktiems į dvigubo rašymo integravimo aprėptį.

![Išteklių vaidmenų integravimas.](./media/5Resources.jpg)

"Project Operations" projekto ištekliai yra prižiūrimi Dataverse ir nesinchronizuojami su finansų ir operacijų programomis.

### <a name="transaction-categories"></a>Operacijų kategorijos

Operacijų kategorijos tvarkomos Dataverse ir sinchronizuojamos su finansų ir operacijų programomis naudojant lentelės žemėlapį **"Project" operacijų kategorijos (msdyn\_ operationscategories).** Kai sinchronizuojamas operacijų kategorijos įrašas, sistema automatiškai sukuria keturis bendrai naudojamus kategorijos įrašus. Kiekvienas įrašas atitinka operacijos tipą finansų ir operacijų programose ir susieja jį su operacijos kategorijos įrašu.

![Operacijų kategorijų integravimas.](./media/4TransactionCategories.jpg)

Norėdamas operacijų kategorijas naudoti įvertinimams ir faktiniams duomenims, projekto buhalteris arba sistemos administratorius kiekviename juridiniame subjekte turi sukurti atitinkamas projektų kategorijas. Norėdami sužinoti daugiau, žr. [Projektų kategorijų konfigūravimas](../project-accounting/configure-project-categories.md).
