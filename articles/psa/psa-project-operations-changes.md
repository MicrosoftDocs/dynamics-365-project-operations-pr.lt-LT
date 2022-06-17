---
title: Funkcijų pokyčiai lyginant „Project Service Automation“ ir „Project Operations“
description: Šiame straipsnyje apžvelgiami funkcijų keitimai iš "Project Service Automation" į Dynamics 365 Project Operations.
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
ms.openlocfilehash: 8a6030faf777051ea1003679589af4bdf97322ab
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8925360"
---
# <a name="feature-changes-from-project-service-automation-to-project-operations"></a>Funkcijų pokyčiai lyginant „Project Service Automation“ ir „Project Operations“

Atnaujinimas iš Dynamics 365 Project Service Automation " Dynamics 365 Project Operations Lite" bus vykdomas trimis etapais. Šiame straipsnyje pateikiama informacija apie pagrindinius pakeitimus, kuriuos galite tikėtis pamatyti, kai naujinimas bus baigtas.

| Atnaujinti pristatymą | 1 etapas <br>(2022 m. Sausio mėn.) | 2 etapas <br>(2022 m. Balandžio banga) | 3 etapas  |
|------------------|------------------------|---------------------------|---------------------------|
| Nėra priklausomybės nuo projektų darbo paskirstymo struktūros (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS yra įtrauktas į šiuo metu palaikomas projekto operacijų ribas. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS nepatenka į šiuo metu palaikomas "Project Operations" ribas, įskaitant "Project" darbalaukio kliento palaikymą. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektų valdymas

Svarbiausi vartotojo patirties pokyčiai bus projektų planavimo srityje. "Project Operations" priima naują modernią patirtį valdant darbo paskirstymo struktūrą (WBS), panaudojant "Project for the Web" teikiamas [planavimo galimybes](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Planavimo patirties skirtumai

Šioje lentelėje apibendrinami planavimo skirtumai tarp "Project Service Automation" ir "Project Operations".

|  Planavimas     |   „Project Operations“   |   PSA   |
|-----------------|------------------------|---------|
| Projekto šablonai – galimybė apibrėžti ir taikyti projekto šablonus kuriant projektą  |  &nbsp;    | :heavy_check_mark: |
| Projekto darbo paskirstymo struktūros (WBS) integravimas su darbalaukio klientu   |    &nbsp;  | :heavy_check_mark: |
| Apribojimai – pradėti ne anksčiau kaip, baigti ne vėliau kaip  | :heavy_check_mark: |   &nbsp;  |
| Etapai – nulinės trukmės užduotys   | :heavy_check_mark:  |  &nbsp;  |
| Ištekliais grindžiamos užduotys atitiks priskirtų išteklių prieinamumą   | :heavy_check_mark: |  &nbsp;    |
| Laiko tarpsnių redagavimas – redaguokite planus ir dirbkite kiekvieną dieną   |   &nbsp;  | :heavy_check_mark: |
| Automatinis / neautomatinis planavimas – naudokite projekto planavimo variklį užduotims automatiškai arba rankiniu būdu planuoti |  &nbsp; | :heavy_check_mark:  |
| Redaguoti didelius projektus tiesiogiai vartotojo sąsajoje: redaguojamų planų dydžiui nėra ribų  | 500 užduočių limitas  | :heavy_check_mark:       |
| Įvykdymo procentas – pažymėti užduoties eigą   | :heavy_check_mark:  |  &nbsp;  |
| [Projekto grafiko režimai](../project-management/scheduling-modes.md) – apibrėžkite projektą kaip fiksuotus vienetus, fiksuotas pastangas arba fiksuotą trukmę | :heavy_check_mark: | &nbsp; |
| Laiko planavimo juosta – kurkite ir tinkinkite laiko planavimo juostos rodinį, kad vizualizuotumėte išsamią tvarkaraščio informaciją ir bendrautumėte su suinteresuotosiomis šalimis. | :heavy_check_mark:  | &nbsp; |
| Į pastangas orientuotos užduotys – variklio palaikymo planavimas, skirtas užduoties planavimui kaip pastangų varomoms pastangoms  | :heavy_check_mark:  | &nbsp; |
| **Dialogo langas Užduoties informacija** – išsamios užduoties informacijos įrašymas naudojant dialogo langą | :heavy_check_mark:  |  &nbsp;  |
| Vilkimas ir numetimas – kelių pasirinkimų užduotys ir jų padėties modifikavimas WBS | :heavy_check_mark: | &nbsp;  |
| Lankstūs nuolatiniai rodiniai – apibrėžkite išsamesnius užduočių atributų rodinius   | :heavy_check_mark:  | &nbsp; |
| WBS rūšiavimas ir filtravimas  | :heavy_check_mark:  | &nbsp; |
| Ne krioklio projekto pristatymo lentų rodinys  | :heavy_check_mark:   | &nbsp; |
| Laiko planavimo juostos rodinys – interaktyvi Ganto diagrama, naudojama WBS vizualizavimui ir redagavimui   | :heavy_check_mark:  | &nbsp; |
| Spartieji klavišai – sparčiųjų klavišų naudojimas bendroms operacijoms, pvz., įtraukai arba įterpimui  | :heavy_check_mark:  |  &nbsp; |
| Kelių lygių anuliavimas – atlikite analizę, kad visiškai suprastumėte pakeitimų poveikį, atšaukdami ir iš naujo taikydami visą operacijų rinkinį | :heavy_check_mark: | &nbsp; |
| Iškirpti / kopijuoti / įklijuoti - bendradarbiaukite kurdami tvarkaraštį kopijuodami ir įklijuodami tvarkaraščio informaciją tarp programų  | :heavy_check_mark: | &nbsp; |
| Užduočių kontroliniai sąrašai – į užduotį įtraukti iki 20 kontrolinio sąrašo elementų   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekto planavimas

" **Project Operations" puslapyje Projektas** yra daug skirtumų, **palyginti su "Project"** puslapiu "Project Service Automation".

Atnaujinant 1 etapą iš **puslapio Projektai** buvo pašalinti šie veiksmai:

  - **Atidaryti programoje „MS Project“**
  - **Kurti šabloną**
  - **Atsieti nuo „MS Project“**

**Projekto** operacijų puslapyje yra šie nauji skirtukai.

- **Medžiagų įvertinimai**
- **Užduočių atsiskaitymo sąranka**

Skirtukas **Būsena** buvo pašalintas, o laukas **Būsena** dabar yra skirtuke **Suvestinė** su projekto planavimo režimu.

   ![Projekto puslapio naujinimai.](media/projectform.png)

Skirtukas Tvarkaraštis **buvo** pervardytas į skirtuką **Užduotis** ir jame yra nauja projekto planavimo patirtis su "Project for the Web".

   ![Skirtukas Naujos projekto užduotys.](media/tasktab.png)

## <a name="scheduling-modes"></a>Planavimo režimai

"Project Operations" pristatė naują funkciją – [planavimo režimus](../project-management/scheduling-modes.md). Visi esami "Project Service Automation" projektai bus numatyti kaip **fiksuota trukmė** projekto operacijose. Tačiau numatytąją naujų projektų reikšmę galima valdyti perėjus į parametrų **parametrų parametrų** > **·** > **grafiko režimą** > **.**

   ![Grafiko režimo projekto parametrų parametrai.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projektų planavimo ribos

Visų projektų planavimo operacijų projekto operacijos remiasi žiniatinklio projektu. Žiniatinklio projektas valdo darbo paskirstymo struktūrą naudodamas šioje lentelėje nurodytas ribas.

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

## <a name="project-planning-extensibility-and-development"></a>Projektų planavimo išplėtimas ir plėtra

Atnaujinę versiją į "Project Operations", turite naudoti projektų planavimo API, kad galėtumėte vykdyti šių objektų kūrimo, atnaujinimo ir naikinimo operacijas:

|   Objekto pavadinimas           |   Loginis objekto pavadinimas       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekto užduotis            | msdyn_projecttask           |
| Projekto užduoties priklausomybė | msdyn_projecttaskdependency |
| Išteklių priskyrimas     | msdyn_resourceassignment    |
| Projekto talpykla          | msdyn_projectbucket         |
| Projekto komandos narys     | msdyn_projectteam           |

Jei šiuo metu turite tinkinimų, susijusių su šiais objektais, žr [...](../project-management/schedule-api-preview.md).

## <a name="data-model-changes"></a>Duomenų modelio pakeitimai

Kaip 1 atnaujinimo etapo dalis, duomenų modelis keičiasi. Šie pakeitimai visų pirma yra esamų objektų lauko pakeitimai. 1 etape objektai, **msydn_project** ir **msdyn_projectteam** yra tinkinimų pertvarkymas. 

> [!IMPORTANT]
> Šis skyrius bus atnaujintas papildomais objektais, kai bus baigti būsimi atnaujinimo etapai.

Šie laukai buvo pakeisti naujais laukais.

|   Entity          |   Senas loginis pavadinimas   |   Naujas loginis pavadinimas    |
|-------------------|----------------------|-----------------------|
| msdyn_project     | msdyn_actualhours    | msdyn_effortcompleted |
| msdyn_project     | msdyn_plannedhours   | msdyn_effort          |
| msdyn_project     | msdyn_remaininghours | msdyn_effortremaining |
| msdyn_project     | msdyn_scheduledend   | msdyn_finish          |
| msdyn_project     | msdyn_wbsduration    | msdyn_duration        |
| msdyn_projectteam | msdyn_assignedhours  | msdyn_effort          |
| msdyn_projectteam | msdyn_from           | msdyn_start           |
| msdyn_projectteam | msdyn_to             | msdyn_finish          |

Įtraukti šie laukai.

|   Entity          |   Loginis pavadinimas                               |   Aprašą |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Rodo faktinių projekto mokesčių pardavimų suvestinę. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_actualmaterialcost                     | Rodo faktinių projekto medžiagų savikainos suvestinę. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_actualmaterialsales                    | Rodo faktinių medžiagų pardavimų projekte suvestinę. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Sutarties eilutė, susieta su šiuo projektu. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Tai vidinės sistemos laukas, naudojamas **kopijuoti projektą**, susijusį su koreliacijos identifikatoriumi. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_copyprojectsessionid                   | Tai vidinės sistemos laukas, naudojamas **kopijuoti projektą**, susijusį su seanso identifikatoriumi. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_globalrevisiontoken                    | Paskutinis sinchronizuojamas xRM visuotinio peržiūros atpažinimo ženklas iš projekto planavimo tarnybos. |
| msdyn_project     | msdyn_msprojectdocument                      | "Microsoft Project" dokumentas, priklausantis projektui. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Planuojamų projekto materialinių išlaidų visuma. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_plannedmaterialsales                   | Planuojamų medžiagų pardavimų sudarymu projekte. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_program                                | Programa, su kuriuo susijęs šis projektas. |
| msdyn_project     | msdyn_quotelineproject                       | Pasiūlymo eilutė, susieta su šiuo projektu. |
| msdyn_project     | msdyn_replaylogheader                        | Pakartojimo žurnalų antraštė. |
| msdyn_project     | msdyn_schedulemode                           | Numatytasis planavimo režimas, naudojamas visoms projekto užduotims.  |
| msdyn_project     | msdyn_taskearlieststart                      | Anksčiausia bet kurios projekto užduoties pradžios data.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projekto komandos narys, iš kurio buvo nukopijuotas šis projekto komandos narys. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Nurodo, ar kurti išteklių poreikį naujai sukurtam bendrosios komandos nariui.  |
| msdyn_projectteam | msdyn_deletestatus                           | Komandos nario naikinimo būsena, kad būtų galima stebėti, ar projekto planavimo tarnybai siunčiama naikinimo užklausa ir ar ji sėkmingai siunčia atsakymą atgal per numatytą laiko langą. |
| msdyn_projectteam | msdyn_effortcompleted                        | Seka komandos nario pastangas atliekant užduotis. |
| msdyn_projectteam | msdyn_effortremaining                        | Seka pastangas, kurias komandos narys dar turi atlikti savo užduotyse. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Laukimo laikotarpis nuo tada, kai komandos narys siunčia naikinimo užklausą projekto planavimo tarnybai, kol komandos narys iš tikrųjų panaikinamas Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Laiko žyma, skirta įrašyti, kai komandos narys naikina užklausą, siunčiama į projekto planavimo tarnybą. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Rodomas projekto komandos narys, iš kurio buvo nukopijuotas šis projekto komandos narys.  |

## <a name="project-templates"></a>Projekto šablonai

Projekto operacijos nepalaiko projektų šablonų. Tačiau galite atkartoti didžiąją dalį pagrindinių funkcijų naudodami ["Project Copy API"](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Darbalaukio priedo palaikymas

"Microsoft Project Desktop" priedo palaikymas nebus pasiekiamas per pirmuosius 2 atnaujinimo etapus. 3 etape klientai, kurių projektai yra didesni už šiuo metu palaikomus "Project for the Web" apribojimus, galės naudoti darbalaukio priedą.

## <a name="editing-resource-assignment-contours"></a>Išteklių priskyrimo kontūrų redagavimas

Galimybė redaguoti išteklių priskyrimo kontūrus bus prieinama, kai bus galima atnaujinti 2 etapą.

## <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

Šios naujos funkcijos buvo įtrauktos į "Project Operations". Šios funkcijos yra papildomo pobūdžio ir neturi įtakos "Project Service Automation" duomenų modeliui.

- [Medžiagos naudojimo registravimas projektuose ir projekto užduotyse](../material/material-usage-log.md)
- [Subrangos sutarčių valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sutarties būsena ir patvirtinimai, kurių būsena neviršijama](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Pagal užduotis pagrįstas atsiskaitymas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Nebenaudojami komponentai

Šiose lentelėse dokumentuojami visi nebenaudojami laukai, perkelti į nebenaudojamų komponentų sprendimą po atnaujinimo. Daugiau informacijos ir saito su sprendimu ieškokite [Dynamics 365 Project Service Automation 3x to Project Operations 4x nebenaudojamų komponentų](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>invoicedetail

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
| msdyn_opportunitylinetransaction.msdyn_kainoraštis                                              |
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
| msdyn_projecttask.msdyn_automatinis planavimas                                                        |
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
| msdyn_projecttaskstatususer.msdyn_expectedhours tocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_iscompleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_percentcomplete                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatuserid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_applicantsavailable                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_description                                                           |
| msdyn_projectteam.msdyn_nuo                                                                  |
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
| msdyn_resourceassignmentdetail.msdyn_nuo                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>salesorderdetail

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

