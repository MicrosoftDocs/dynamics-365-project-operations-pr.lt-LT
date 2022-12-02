---
title: Funkcijų pokyčiai lyginant „Project Service Automation“ ir „Project Operations“
description: Šiame straipsnyje apžvelgiami funkcijos pakeitimai iš „Project Service Automation" į „Dynamics 365 Project Operations“.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: a9c69fc4296d30763f3994a4955e64ab258ceb4f
ms.sourcegitcommit: 675e9f3615e701c5f998de3a5ea3e25df11ae107
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/09/2022
ms.locfileid: "9459937"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funkcijų pokyčiai lyginant „Project Service Automation“ ir „Project Operations“

Naujinimas iš „Dynamics 365 Project Service Automation“ į „Dynamics 365 Project Operations Lite" bus pristatytas trimis etapais. Šiame straipsnyje pateikiama informacija apie didelius pakeitimus, kuriuos galite tikėtis matyti baigę naujinimą.

| Naujinimo pristatymas | 1 etapas <br>(2022 m. sausis) | 2 etapas <br>(2022 m. lapkritis) | 3 etapas  |
|------------------|------------------------|---------------------------|---------------------------|
| Darbo paskirstymo struktūra (WBS) nuo projektų nepriklauso. | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS įtrauktas į šiuo metu palaikomus „Project Operations“ limitus. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS, esantis už šiuo metu palaikomų "Project Operations" limitų, įskaitant "Project Desktop Client" palaikymą. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektų valdymas

Svarbiausi vartotojo patirties pakeitimai bus projektų planavimo srityje. „Project Operations" priima naują, modernią darbo paskirstymo struktūros (WBS) valdymo patirtį, pasverdama planavimo galimybes, teikiamas [„Project for the Web"](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Planavimo funkcijų skirtumai

Toliau esančioje lentelėje apibendrinti „Project Service Automation" ir „Project Operations" planavimo skirtumai.

|  Planavimas     |   „Project Operations“   |   Psa   |
|-----------------|------------------------|---------|
| Projektų šablonai – galimybė apibrėžti ir taikyti projektų šablonus kuriant projektą  |  &nbsp;    | :heavy_check_mark: |
| Projektų darbo paskirstymo struktūros (WBS) integravimas su darbalaukio klientu   |    &nbsp;  | :heavy_check_mark: |
| Apribojimai – pradėkite ne anksčiau kaip, baikite ne vėliau kaip  | :heavy_check_mark: |   &nbsp;  |
| Etapai – užduotys, kurių trukmė nulinė   | :heavy_check_mark:  |  &nbsp;  |
| Ištekliais pagrįstos užduotys paisys priskirtų išteklių pasiekiamumo   | :heavy_check_mark: |  &nbsp;    |
| Laike suskirstytas redagavimas – redaguokite planus ir dirbkite kiekvieną dieną   |   &nbsp;  | :heavy_check_mark: |
| Automatinis / rankinis planavimas – naudokite projekto planavimo funkciją, kad automatiškai arba rankiniu būdu planuotumėte užduotis |  &nbsp; | :heavy_check_mark:  |
| Tiesiogiai vartotojo sąsajoje redaguokite didelius projektus: nėra jokių redaguojamų planų dydžio apribojimų  | 500 užduočių limitas  | :heavy_check_mark:       |
| Užbaigta procentinė dalis – užduoties eigos žymėjimas   | :heavy_check_mark:  |  &nbsp;  |
| [Projekto grafiko režimai](../project-management/scheduling-modes.md) – projekto apibrėžimas kaip fiksuotų vienetų, fiksuotų pastangų arba fiksuotos trukmės | :heavy_check_mark: | &nbsp; |
| Laiko planavimo juosta – kurkite ir tinkinkite laiko planavimo juostos rodinį, kad vizualizuotumėte išsamią grafiko informaciją ir bendraukite su suinteresuotomis šalimis. | :heavy_check_mark:  | &nbsp; |
| Pastangomis pagrįstos užduotys – planavimo funkcijos palaikymas užduočiai, kaip pastangomis pagrįstai, planuoti  | :heavy_check_mark:  | &nbsp; |
| **Užduoties informacijos** dialogo langas – įrašyti išsamią užduoties informaciją naudojant dialogo langą | :heavy_check_mark:  |  &nbsp;  |
| Nuvilkite – kelių pasirinkių užduotys ir galimybė modifikuoti jų padėtį WBS | :heavy_check_mark: | &nbsp;  |
| Lankstūs, pastovūs rodiniai – apibrėžkite grūdėtesnį užduoties rodinio vaizdą   | :heavy_check_mark:  | &nbsp; |
| Filtruoti ir rikiuoti WBS  | :heavy_check_mark:  | &nbsp; |
| Lentelių rodinys, skirtas ne krioklinio modelio projektų pristatymui  | :heavy_check_mark:   | &nbsp; |
| Laiko planavimo juostos rodinys – interaktyvioji Gantt diagrama, naudojama WBS vizualizuoti ir redaguoti   | :heavy_check_mark:  | &nbsp; |
| Spartieji klavišai – naudokite sparčiuosius klavišus bendroms operacijoms, pvz., įtraukų arba įterpimo  | :heavy_check_mark:  |  &nbsp; |
| Kelių lygių grįžimas atfal – atlikite analizę "kas jei", kad visiškai suprastumėte pakeitimų poveikį atšaukdami ir iš naujo pritaikydami visą operacijų rinkinį | :heavy_check_mark: | &nbsp; |
| Iškirpti / kopijuoti / įklijuoti – bendradarbiaukite planuojant plėtrą kopijuojant ir įklijuojant išsamią grafiko informaciją tarp programų  | :heavy_check_mark: | &nbsp; |
| Užduočių kontroliniai sąrašai – į užduotį įtraukite iki 20 sąrašo elementų   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekto planavimas

„Project Operations“ **Projektai** puslapyje yra daug skirtumų, palyginti su „Project Service Automation“ **Project** puslapiu.

Toliau nurodyti veiksmai iš puslapio **Projektai** pašalinti kaip 1 etapo naujinimo dalis:

  - **Atidaryti programoje „MS Project“**
  - **Kurti šabloną**
  - **Atsieti nuo „MS Project“**

Į „Project Operations“ **Projektų** puslapį įtraukti šie nauji skirtukai.

- **Medžiagų įvertinimai**
- **Užduočių atsiskaitymo sąranka**

Skirtukas **Būsena** pašalintas, o **Būsena** laukas dabar yra skirtuke **Suvestinė** su projekto planavimo režimu.

   ![Projekto puslapio naujiniai](media/projectform.png)

Skirtukas **Grafikas** pervadintas į skirtuką **Užduotis** ir su „Project for the Web“ leidžia naudoti naujas projektų planavimo funkcijas.

   ![Naujas Projekto užduočių skirtukas.](media/tasktab.png)

## <a name="scheduling-modes"></a>Planavimo režimai

„Project Operations“ pristatė naują funkciją [Planavimo režimai](../project-management/scheduling-modes.md). Visi esami „Project Service Automation" projektai „Project Operations“ programoje pagal numatytuosius nustatymus bus nustatyti kaip **Fiksuotos trukmės**. Tačiau numatytąsias naujų projektų reikšmes galima valdyti nuėjus į **Nustatymai** > **Parametrai** > **Parametras** > **Grafiko režimas**.

   ![Grafiko režimo projekto parametrų nustatymai.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekto planavimo limitai

„Project Operations" visose projektų planavimo operacijose remiasi „Project for the Web". „Project for the Web“ valdo darbo paskirstymo struktūrą naudodamas toliau pateiktoje lentelėje nurodytus apribojimus.

| **Laukas**                                          | **Riba**             |
|----------------------------------------------------|-----------------------|
| Maksimalus bendras projekto užduočių skaičius                  | 500                   |
| Maksimali bendra projekto trukmė               | 3650 dienų (10 metų)  |
| Maksimalus bendras projekto išteklių skaičius              | 300                   |
| Maksimalus bendras projekto saitų skaičius (tik vėlesnės veiklos) | 600                   |
| Maksimalus bendras projekto pasirinktinių laukų skaičius          | 10                    |
| Maksimalus hierarchijos lygis                            | 10 lygių             |
| Maksimalus nuorodų skaičius (vėlesnės veiklos ir ankstesnės veiklos)            | 20                    |
| Maksimali lapo užduoties trukmė                      | 1250 d.             |
| Maksimali suvestinės užduoties trukmė                 | 3650 dienų (10 metų)  |
| Maksimalus užduočiai priskirtų išteklių skaičius               | 20 išteklių          |
| Palaikomas užduoties datų diapazonas                    | 2000-01-01–2149-12-31 |
| Kontrolinio sąrašo elementai                                    | 20                    |

## <a name="project-planning-extensibility-and-development"></a>Projektų planavimo tęstinumas ir kūrimas

Atnaujinę į „Project Operations", norėdami vykdyti šių objektų kūrimo, naujinimo ir naikinimo operacijas, turite naudoti „Project Scheduling API“.

|   Objekto pavadinimas           |   Loginis objekto pavadinimas       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekto užduotis            | msdyn_projecttask           |
| Projekto užduoties priklausomybė | msdyn_projecttaskdependency |
| Išteklių priskyrimas     | msdyn_resourceassignment    |
| Projekto talpykla          | msdyn_projectbucket         |
| Projekto komandos narys     | msdyn_projectteam           |

Jei šiuo metu turite tinkinimų, kurie susiję su šiais objektais, [žr. projektų planavimo API naudojimas operacijoms su planavimo objektais atlikti](../project-management/schedule-api-preview.md), kad būtų galima atlikti diegimo nurodymus.

## <a name="data-model-changes"></a>Duomenų modelio pakeitimai

Yra 1 versijos naujinimo etapo duomenų modelio pakeitimai. Šie pakeitimai pirmiausia yra esamų objektų laukų pakeitimai. 1 etape objektai, **msydn_project** ir **msdyn_projectteam** yra tinkinimų pertvarkymai. 

> [!IMPORTANT]
> Šis skyrius bus atnaujintas su papildomais objektais, nes ateityje bus užbaigti būsimi naujinimo etapai.

Šie laukai pakeisti naujais laukais.

|   Entity          |   Senas logiškas pavadinimas   |   Naujas logiškas pavadinimas    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Buvo pridėti tolesnės laukeliai.

|   Entity          |   Loginis pavadinimas                               |   Aprašą |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Rodomas agreguotas projekto faktinio mokesčio pardavimas. Skirta naudoti tik „Project Service Automation“. |
| msdyn_project     | msdyn_actualmaterialcost                     | Rodoma agreguota faktinė materiali projekto savikaina. Skirta naudoti tik „Project Service Automation“. |
| msdyn_project     | msdyn_actualmaterialsales                    | Rodomas agreguotas faktinis projekto medžiagos pardavimas. Skirta naudoti tik „Project Service Automation“. |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Sutarties eilutė, susieta su šiuo projektu. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Tai yra vidinis sistemos laukas, naudojamas funkcijai **Kopijuoti projektą**, susijusiai su sąsajos identifikatoriumi. Skirta naudoti tik „Project Service Automation“. |
| msdyn_project     | msdyn_copyprojectsessionid                   | Tai yra vidinis sistemos laukas, naudojamas funkcijai **Kopijuoti projektą**, susijusiai su sesijos identifikatoriumi. Skirta naudoti tik „Project Service Automation“. |
| msdyn_project     | msdyn_globalrevisiontoken                    | Paskutinio sinchronizavimo xRM visuotinio peržiūros atpažinimo ženklas iš projektų planavimo tarnybos. |
| msdyn_project     | msdyn_msprojectdocument                      | Projektui priklausantis „Microsoft Project“ dokumentas. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Rodoma agreguota planinė materiali projekto savikaina. Skirta naudoti tik „Project Service Automation“. |
| msdyn_project     | msdyn_plannedmaterialsales                   | Rodoma agreguota planinė materiali projekto pardavimų reikšmė. Skirta naudoti tik „Project Service Automation“. |
| msdyn_project     | msdyn_program                                | Programa, su kuriuo susijęs šis projektas. |
| msdyn_project     | msdyn_quotelineproject                       | Pasiūlymo eilutė, susieta su šiuo projektu. |
| msdyn_project     | msdyn_replaylogheader                        | Pakartojimo žurnalų antraštė. |
| msdyn_project     | msdyn_schedulemode                           | Numatytasis planavimo režimas, naudojamas visoms projekto užduotims.  |
| msdyn_project     | msdyn_taskearlieststart                      | Anksčiausia bet kurios projekto užduoties pradžios data.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projekto komandos narys, iš kurio buvo nukopijuotas šis projekto komandos narys. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Nurodo ar naujai sukurtam bendrajam komandos nariui sukurti išteklių reikalavimą.  |
| msdyn_projectteam | msdyn_deletestatus                           | Ištrintas komandos nario statusas, kad būtų galima sekti, ar ištrintas prašymas nusiųstas projekto planavimo tarnybai ir ar jis sėkmingai atsiunčia atsakymą atgal per numatytą laiką. |
| msdyn_projectteam | msdyn_effortcompleted                        | Seka komandos nario pastangas atliekant priskyrimus. |
| msdyn_projectteam | msdyn_effortremaining                        | Seka dar būsimas komandos nario pastangas atliekant priskyrimus. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Laukimo laikotarpis, nuo kurio komandos narys siunčia naikinimo prašymą projekto planavimo paslaugoms iki tol, kol komandos narys yra ištrinamas „Microsoft Dataverse“.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Laiko žymė, skirta įrašyti, kada komandos nario naikinimo užklausa išsiųsta „Project scheduling service“. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Rodomas projekto komandos narys, iš kurio buvo nukopijuotas šis projekto komandos narys.  |

## <a name="project-templates"></a>Projekto šablonai

„Project Operations" nepalaiko projektų šablonų. Tačiau naudodami [projekto kopijavimo](../project-management/dev-copy-project.md) galite daugelį pagrindinių funkcijų pakartoti.

## <a name="desktop-add-in-support"></a>Darbalaukio papildinio palaikymas

„Microsoft Project Desktop" papildinio palaikymas nebus galimas pirmuose 2 naujinimo etapuose. 3 etape klientai, kurių projektai yra didesni nei šiuo metu palaikomi „Project for the Web" apribojimai, galės naudoti darbalaukio papildinį.

## <a name="editing-resource-assignment-contours"></a>Išteklių priskyrimo kontūrų redagavimas

Galimybė redaguoti išteklių priskyrimo etapą bus pasiekiama, kai bus prieinamas naujinimo 2 etapas.

## <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

„Project Operations“ grafike pridėtos šios naujos funkcijos. Šios funkcijos yra pridedamojo pobūdžio ir neturi įtakos „Project Service Automation" duomenų modeliui.

- [Medžiagų naudojimo projektuose ir projekto užduotyse įrašymas](../material/material-usage-log.md)
- [Subrangos sutarties valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Neviršijimo būsenos ir tikrinimų sutartis](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Užduotimis pagrįstas atsiskaitymas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Nerekomenduojami komponentai

Toliau pateikiamose lentelėse pateikiami visi nerekomenduojami laukai, perkelti į nerekomenduojamų komponentų sprendimą po atnaujinimo. Daugiau informacijos ir spendimų nuorodos ieškokite [Dynamics 365 Project Service Automation 3x „Project Operations“ 4x nerekomenduojami komponentai](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>Invoicedetail

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
|invoicedetail.msdyn_contractline    |

### <a name="msdyn_actual"></a>msdyn_actual

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_actual.msdyn_salescontractline                                                          |

### <a name="msdyn_characteristicreqforteammember"></a>msdyn_characteristicreqforteammember

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_characteristicreqforteammember.msdyn_characteristic                                     |
| msdyn_characteristicreqforteammember.msdyn_characteristicreqforteammemberid                   |
| msdyn_characteristicreqforteammember.msdyn_characteristictype                                 |
| msdyn_characteristicreqforteammember.msdyn_name                                               |
| msdyn_characteristicreqforteammember.msdyn_ratingvalue                                        |
| msdyn_characteristicreqforteammember.msdyn_resourcerequirementid                              |

### <a name="msdyn_contractlineinvoiceschedule"></a>msdyn_contractlineinvoiceschedule

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_contractlineinvoiceschedule.msdyn_contractline                                          |
| msdyn_contractlinescheduleofvalue.msdyn_contractline                                          |
 
### <a name="msdyn_dataexport"></a>msdyn_dataexport

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_dataexport.msdyn_dataexportid                                                           |
| msdyn_dataexport.msdyn_datatoken                                                              |
| msdyn_dataexport.msdyn_entityname                                                             |
| msdyn_dataexport.msdyn_exportedrecordcount                                                    |
| msdyn_dataexport.msdyn_exportstatus                                                           |
| msdyn_dataexport.msdyn_linkedentitydata                                                       |
| msdyn_dataexport.msdyn_name                                                                   |
| msdyn_dataexport.msdyn_pagingdata                                                             |

### <a name="msdyn_fact"></a>msdyn_fact

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_fact.msdyn_salescontractline                                                            |

### <a name="msdyn_findworkevent"></a>msdyn_findworkevent

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_findworkevent.msdyn_bookableresource                                                    |
| msdyn_findworkevent.msdyn_findworkeventid                                                     |
| msdyn_findworkevent.msdyn_name                                                                |
| msdyn_findworkevent.msdyn_timestamp                                                           |
| msdyn_findworkevent.msdyn_type                                                                |
| msdyn_findworkevent.msdyn_value                                                               |
| msdyn_findworkevent.msdyn_work                                                                |

### <a name="msdyn_invoicelinetransaction"></a>msdyn_invoicelinetransaction

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_invoicelinetransaction.msdyn_invoiceline                                                |
| msdyn_invoicelinetransaction.msdyn_salescontractline                                          |

### <a name="msdyn_journalline"></a>msdyn_journalline

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_journalline.msdyn_salescontractline                                                     |

### <a name="msdyn_opportunitylineresourcecategory"></a>msdyn_opportunitylineresourcecategory

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylineresourcecategory.msdyn_billingtype                                       |
| msdyn_opportunitylineresourcecategory.msdyn_description                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_amount                                                 |
| msdyn_opportunitylinetransaction.msdyn_amount_base                                            |
| msdyn_opportunitylinetransaction.msdyn_amountmethod                                           |
| msdyn_opportunitylinetransaction.msdyn_basisamount                                            |
| msdyn_opportunitylinetransaction.msdyn_basisamount_base                                       |
| msdyn_opportunitylinetransaction.msdyn_basisprice                                             |
| msdyn_opportunitylinetransaction.msdyn_basisprice_base                                        |
| msdyn_opportunitylinetransaction.msdyn_basisquantity                                          |
| msdyn_opportunitylinetransaction.msdyn_billingtype                                            |
| msdyn_opportunitylinetransaction.msdyn_bookableresource                                       |
| msdyn_opportunitylinetransaction.msdyn_contactcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_contactvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_customertype                                           |
| msdyn_opportunitylinetransaction.msdyn_description                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_percent                                                |
| msdyn_opportunitylinetransaction.msdyn_price                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_pricelist                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_project                                                |
| msdyn_opportunitylinetransaction.msdyn_quantity                                               |
| msdyn_opportunitylinetransaction.msdyn_resourcecategory                                       |
| msdyn_opportunitylinetransaction.msdyn_resourceorganizationalunitid                           |
| msdyn_opportunitylinetransaction.msdyn_startdatetime                                          |
| msdyn_opportunitylinetransaction.msdyn_task                                                   |
| msdyn_opportunitylinetransaction.msdyn_transactioncategory                                    |
| msdyn_opportunitylinetransaction.msdyn_transactionclassification                              |
| msdyn_opportunitylinetransaction.msdyn_transactiontypecode                                    |
| msdyn_opportunitylinetransaction.msdyn_unit                                                   |
| msdyn_opportunitylinetransaction.msdyn_unitschedule                                           |
| msdyn_opportunitylinetransaction.msdyn_vendortype                                             |

### <a name="msdyn_opportunitylinetransactioncategory"></a>msdyn_opportunitylinetransactioncategory

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactioncategory.msdyn_billingtype                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_description                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_description                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_include                                   |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunityline                           |
| msdyn_opportunitylinetransactionclassificatio.msdyn_opportunitylinetransactionclassificatioid |
| msdyn_opportunitylinetransactionclassificatio.msdyn_transactionclassification                 |

### <a name="msdyn_orderlineresourcecategory"></a>msdyn_orderlineresourcecategory

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlineresourcecategory.msdyn_contractline                                            |

### <a name="msdyn_orderlinetransaction"></a>msdyn_orderlinetransaction

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransaction.msdyn_salescontractline                                            |
| msdyn_orderlinetransactioncategory.msdyn_contractline                                         |

### <a name="msdyn_orderlinetransactionclassification"></a>msdyn_orderlinetransactionclassification

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_orderlinetransactionclassification.msdyn_contractline                                   |

### <a name="msdyn_project"></a>msdyn_project

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_project.msdyn_actualdurationminutes                                                     |
| msdyn_project.msdyn_actualhours                                                               |
| msdyn_project.msdyn_istemplate                                                                |
| msdyn_project.msdyn_plannedhours                                                              |
| msdyn_project.msdyn_projecttemplate                                                           |
| msdyn_project.msdyn_remaininghours                                                            |
| msdyn_project.msdyn_scheduleddurationminutes                                                  |
| msdyn_project.msdyn_scheduledend                                                              |
| msdyn_project.msdyn_stagename                                                                 |
| msdyn_project.msdyn_wbsduration                                                               |


### <a name="msdyn_projecttask"></a>msdyn_projecttask

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttask.msdyn_actualdurationminutes                                                 |
| msdyn_projecttask.msdyn_actualeffort                                                          |
| msdyn_projecttask.msdyn_aggregationdirection                                                  |
| msdyn_projecttask.msdyn_assignedresources                                                     |
| msdyn_projecttask.msdyn_assignedteammembers                                                   |
| msdyn_projecttask.msdyn_autoscheduling                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_numberofresources                                                     |
| msdyn_projecttask.msdyn_remaininghours                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_description                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhourstocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_number                                                                |
| msdyn_projectteam.msdyn_to                                                                    |

### <a name="msdyn_projectteammembersignup"></a>msdyn_projectteammembersignup

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteammembersignup.msdyn_bookableresource                                          |
| msdyn_projectteammembersignup.msdyn_membershipstatus                                          |
| msdyn_projectteammembersignup.msdyn_name                                                      |
| msdyn_projectteammembersignup.msdyn_projectteammembersignupid                                 |
| msdyn_projectteammembersignup.msdyn_teammembership                                            |

### <a name="msdyn_projecttransactioncategory"></a>msdyn_projecttransactioncategory

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttransactioncategory.msdyn_billingtype                                            |
| msdyn_projecttransactioncategory.msdyn_name                                                   |
| msdyn_projecttransactioncategory.msdyn_project                                                |
| msdyn_projecttransactioncategory.msdyn_projecttransactioncategoryid                           |
| msdyn_projecttransactioncategory.msdyn_transactioncategory                                    |

### <a name="msdyn_quotelineinvoiceschedule"></a>msdyn_quotelineinvoiceschedule

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_quotelineinvoiceschedule.msdyn_quoteline                                                |
| msdyn_quotelineresourcecategory.msdyn_quoteline                                               |
| msdyn_quotelinescheduleofvalue.msdyn_quoteline                                                |
| msdyn_quotelinetransaction.msdyn_quoteline                                                    |
| msdyn_quotelinetransactioncategory.msdyn_quoteline                                            |
| msdyn_quotelinetransactionclassification.msdyn_quoteline                                      |

### <a name="msdyn_resourceassignment"></a>msdyn_resourceassignment

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_resourceassignment.msdyn_hours                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_duration                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>pardavimųužsakymųišsamiinformacija

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

