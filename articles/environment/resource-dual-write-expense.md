---
title: Išlaidų tvarkymo integravimas
description: Šioje temoje pateikiama informacijos apie išlaidų ataskaitos integravimą į „Project Operations“ naudojant dvigubo rašymo funkciją.
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 8c347f14f3a479eb4aec951cfe4094c5581bce32
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955797"
---
# <a name="expense-management-integration"></a>Išlaidų tvarkymo integravimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikiama informacijos apie išlaidų ataskaitų integravimą į „Project Operations“ [visų išlaidų įdiegtį](../expense/expense-overview.md) naudojant dvigubo rašymo funkciją.

## <a name="expense-categories"></a>Išlaidų kategorijos

Visų išlaidų įdiegtyje išlaidų kategorijos kuriamos ir tvarkomos „Finance and Operations“ programose. Norėdami sukurti naują išlaidų kategoriją, atlikite toliau nurodytus veiksmus.

1. Sprendime „Microsoft Dataverse“ sukurkite kategoriją **Operacija**. Dvigubo rašymo integravimo funkcija šią operacijų kategoriją sinchronizuos su „Finance and Operations“ programomis. Norėdami sužinoti daugiau, žr. [Projektų kategorijų konfigūravimas](/dynamics365/project-operations/project-accounting/configure-project-categories) ir [„Project Operations“ sąrankos ir konfigūracijos duomenų integravimas](resource-dual-write-setup-integration.md). Dėl šio integravimo sistema „Finance and Operations“ programose sukuria keturis bendrai naudojamus kategorijų įrašus.
2. Sprendime „Finance“ nueikite į **Išlaidų tvarkymas** > **Sąranka** > **Bendrai naudojamos kategorijos** ir pasirinkite bendrai naudojamą kategoriją, kurios operacijų klasė yra **Išlaidos**. Parametrą **Galima naudoti išlaidose** nustatykite kaip **Teisinga** ir apibrėžkite norimą naudoti išlaidų tipą.
3. Naudodami šį bendrai naudojamos kategorijos įrašą, sukurkite naują išlaidų kategoriją nuėję į **Išlaidų tvarkymas** > **Sąranka** > **Išlaidų kategorijos** ir pasirinkę **Nauja**. Kai įrašas įrašomas, dvigubo rašymo funkcija naudoja lentelės schemą **„Project Operations“ integravimo projekto išlaidų kategorijų eksportavimo objektas (msdyn \_expensecategories)** šiam įrašui su „Dataverse“ sinchronizuoti.

  ![Išlaidų kategorijų integravimas](./media/DW6ExpenseCategories.png)

Išlaidų kategorijos „Finance and Operations“ programose skiriasi atsižvelgiant į konkrečią įmonę ar juridinį subjektą. Sprendime „Dataverse“ naudojami atskiri atitinkami konkretiems juridiniams subjektams skirti įrašai. Kai projekto vadovas įvertina išlaidas, jis negali pasirinkti išlaidų kategorijų, sukurtų projektui, kuris priklauso kitai įmonei nei ta įmonė, kuriai priklauso projektas, su kuriuo projekto vadovas dirba. 

## <a name="expense-reports"></a>Išlaidų ataskaitos

Išlaidų ataskaitos kuriamos ir tvirtinamos „Finance and Operations“ programose. Norėdami sužinoti daugiau, žr. [Išlaidų ataskaitų kūrimas ir apdorojimas sprendime „Dynamics 365 Project Operations“](/learn/modules/create-process-expense-reports/). Kai išlaidų ataskaitą patvirtina projekto vadovas, ji užregistruojama didžiojoje knygoje. Sprendime „Project Operations“ su projektais susijusios išlaidų ataskaitų eilutės registruojamos naudojant specialias toliau nurodytas registravimo taisykles.

  - Su projektais susiję kaštai (įskaitant nesusigrąžinamus mokesčius) nėra iš karto registruojami didžiosios knygos projekto kaštų sąskaitoje – jie registruojami išlaidų integravimo sąskaitoje. Ši sąskaita konfigūruojama nuėjus į **Projektų tvarkymas ir apskaita** > **Sąranka** > **Projektų tvarkymo ir apskaitos parametrai**, skirtuke **„Project Operations“ naudojant „Dynamics 365 Customer Engagement“**.
  - Dvigubo rašymo funkcija su „Dataverse“ sinchronizuoja naudodama lentelės schemą **„Project Operations“ integravimo projekto išlaidų eksportavimo objektas (msdyn \_expenses)**.
  - Papildomos mokesčių knygos, papildomos tiekėjų knygos ir kiti finansiniai registravimai pagal poreikį įrašomi registruojant išlaidų ataskaitas.

  ![Išlaidų ataskaitų integravimas](./media/DW6ExpenseReports.png)

Kai į „Dataverse“ objektą **Išlaidos** įrašomas koks nors įrašas, sistema paleidžia automatizuotą to įrašo patvirtinimo procesą. Jei reikia, automatizuoto patvirtinimo proceso būseną galima peržiūrėti sprendime „Dataverse“ nuėjus į **Išplėstiniai parametrai** > **Sistema** > **Sistemos užduotys**. Patvirtinus įrašą, objekte **Faktiniai duomenys** sukuriami išlaidų operacijų klasės įrašai.

Su išlaidomis susiję faktiniai duomenys tada apdorojami naudojant dvigubo rašymo lentelės schemą **„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)**. Norėdami sužinoti daugiau, žr. [Projektų įvertinimai ir faktiniai duomenys](resource-dual-write-estimates-actuals.md).

Periodinis procesas **Importavimas iš įrašų paruošimo lentelės** „Project Operations“ integravimo žurnale sukuria su išlaidų ataskaita susijusias eilutes. Numatyta, kad korespondentinė sąskaita nustatoma kaip išlaidų integravimo sąskaita. Registravimo integravimo žurnalas pašalina sąskaitos balansą už išlaidų operaciją ir išlaidų sumą perkelia į projekto kaštų sąskaitą. Dėl tolimesnio sąskaitų faktūrų išrašymo ir pajamų pripažinimo tikslais sistema taip pat sukuria papildomų knygų operacijų.