---
title: Funkcijų pokyčiai lyginant „Project Service Automation“ ir „Project Operations“
description: Šiame straipsnyje pateikiama funkcijų pakeitimų iš "Project Service Automation" į Dynamics 365 Project Operations.
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

Atnaujinimas iš Dynamics 365 Project Service Automation į Dynamics 365 Project Operations "Lite" bus pristatytas trimis etapais. Šiame straipsnyje pateikiama informacija apie pagrindinius pakeitimus, kuriuos galite tikėtis pamatyti, kai versijos naujinimas bus baigtas.

| Atnaujinimo pristatymas | 1 fazė <br>(Sausis 2022) | 2 fazė <br>(Lapkritis 2022) | 3 fazė  |
|------------------|------------------------|---------------------------|---------------------------|
| Nėra priklausomybės nuo projektų darbo paskirstymo struktūros (WBS). | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| WBS yra įtrauktas į šiuo metu palaikomus projekto operacijų apribojimus. | &nbsp; | :heavy_check_mark: | :heavy_check_mark: |
| WBS už šiuo metu palaikomų "Project Operations" apribojimų ribų, įskaitant "Project" darbalaukio kliento palaikymą. | &nbsp; | &nbsp; | :heavy_check_mark: |

## <a name="project-management"></a>Projektų valdymas

Reikšmingiausi vartotojo patirties pokyčiai bus projekto planavimo srityje. "Project Operations" pritaiko naują modernią darbo paskirstymo struktūros (WBS) valdymo patirtį, panaudojant planavimo galimybes, kurias [teikia "Project for the Web"](https://support.microsoft.com/en-us/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5).

## <a name="differences-in-the-scheduling-experience"></a>Planavimo patirties skirtumai

Šioje lentelėje apibendrinami planavimo skirtumai tarp "Project Service Automation" ir "Project Operations".

|  Planavimas     |   „Project Operations“   |   Psa   |
|-----------------|------------------------|---------|
| Projekto šablonai – galimybė apibrėžti ir taikyti projekto šablonus kuriant projektą  |  &nbsp;    | :heavy_check_mark: |
| Projekto darbo paskirstymo struktūros (WBS) integravimas su darbalaukio klientu   |    &nbsp;  | :heavy_check_mark: |
| Apribojimai - Pradėkite ne anksčiau kaip, užbaikite ne vėliau kaip  | :heavy_check_mark: |   &nbsp;  |
| Orientyrai – užduotys, kurių trukmė nulinė   | :heavy_check_mark:  |  &nbsp;  |
| Ištekliais pagrįstos užduotys atitiks priskirtų išteklių prieinamumą   | :heavy_check_mark: |  &nbsp;    |
| Redagavimas laiko tarpsniu – redaguokite planus ir dirbkite kiekvieną dieną   |   &nbsp;  | :heavy_check_mark: |
| Automatinis / neautomatinis planavimas – naudokite projekto planavimo variklį, kad automatiškai arba rankiniu būdu suplanuotumėte užduotis |  &nbsp; | :heavy_check_mark:  |
| Redaguokite didelius projektus tiesiogiai vartotojo sąsajoje: planų, kuriuos galima redaguoti, dydis neribojamas  | 500 užduočių limitas  | :heavy_check_mark:       |
| Įvykdymo procentas – užduoties eigos žymėjimas   | :heavy_check_mark:  |  &nbsp;  |
| [Projekto tvarkaraščio režimai](../project-management/scheduling-modes.md) – apibrėžkite projektą kaip fiksuotus vienetus, fiksuotas pastangas arba fiksuotą trukmę | :heavy_check_mark: | &nbsp; |
| Laiko planavimo juosta – kurkite ir tinkinkite laiko juostos rodinį, kad vizualizuotumėte išsamią tvarkaraščio informaciją ir bendrautumėte su suinteresuotosiomis šalimis. | :heavy_check_mark:  | &nbsp; |
| Į pastangas orientuotos užduotys – variklio palaikymo planavimas planuojant užduotį kaip varomą pastangų  | :heavy_check_mark:  | &nbsp; |
| **Dialogo langas Užduoties informacija** – užduoties informacijos įrašymas naudojant dialogo langą | :heavy_check_mark:  |  &nbsp;  |
| Vilkite ir numeskite – kelių pasirinkimų užduotys ir pakeiskite jų padėtį WBS | :heavy_check_mark: | &nbsp;  |
| Lankstūs nuolatiniai rodiniai – išsamesnių užduočių atributų rodinių apibrėžimas   | :heavy_check_mark:  | &nbsp; |
| WBS rūšiavimas ir filtravimas  | :heavy_check_mark:  | &nbsp; |
| Lentų požiūris į ne krioklio projekto įgyvendinimą  | :heavy_check_mark:   | &nbsp; |
| Laiko juostos rodinys – interaktyvi Ganto diagrama, naudojama WBS vizualizuoti ir redaguoti   | :heavy_check_mark:  | &nbsp; |
| Spartieji klavišai – sparčiųjų klavišų naudojimas atliekant įprastas operacijas, pvz., įtrauką arba įterpimą  | :heavy_check_mark:  |  &nbsp; |
| Daugiapakopis anuliavimas – atlikite sąlyginę analizę, kad visiškai suprastumėte pakeitimų poveikį, atbuline eiga ir iš naujo pritaikydami visą operacijų rinkinį | :heavy_check_mark: | &nbsp; |
| Iškirpti / kopijuoti / įklijuoti - bendradarbiaukite kurdami tvarkaraštį kopijuodami ir įklijuodami tvarkaraščio informaciją tarp programų  | :heavy_check_mark: | &nbsp; |
| Užduočių kontroliniai sąrašai – prie užduoties pridėkite iki 20 kontrolinio sąrašo elementų   | :heavy_check_mark: | &nbsp; |

## <a name="project-planning"></a>Projekto planavimas

" **Project Operations" puslapyje "Project** " yra daug skirtumų, **palyginti su "Project"** puslapiu, esančiu "Project Service Automation".

Toliau nurodyti veiksmai buvo pašalinti iš **projekto** puslapio kaip 1 etapo atnaujinimo dalis:

  - **Atidaryti programoje „MS Project“**
  - **Kurti šabloną**
  - **Atsieti nuo „MS Project“**

" **Project Operations" puslapyje Projektas** yra šie nauji skirtukai.

- **Medžiagų įvertinimai**
- **Užduočių atsiskaitymo sąranka**

**Būsenos** skirtukas pašalintas, o **laukas Būsena** dabar yra skirtuke **Suvestinė** su projekto planavimo režimu.

   ![Projekto puslapio atnaujinimai.](media/projectform.png)

Skirtukas **Tvarkaraštis** buvo pervardytas į skirtuką **Užduotis** ir jame pateikiama nauja projekto planavimo patirtis naudojant "Project for the Web".

   ![Skirtukas Naujos projekto užduotys.](media/tasktab.png)

## <a name="scheduling-modes"></a>Planavimo režimai

"Project Operations" pristatė naują funkciją [– planavimo režimus](../project-management/scheduling-modes.md). Visi esami "Project Service Automation" projektai pagal numatytuosius nustatymus bus fiksuoti **"Project Operations" trukmės**. Tačiau numatytuosius naujų projektų nustatymus galima valdyti nuėjus į **nustatymų** > **parametrų** > **parametrų grafiko** > **režimą**.

   ![Projekto parametrų parametrai grafiko režimui.](media/projectparameter.png)

## <a name="project-planning-limits"></a>Projekto planavimo apribojimai

"Project Operations" remiasi žiniatinklio projektu visoms projekto planavimo operacijoms. "Project for the Web" valdo darbo paskirstymo struktūrą naudodama šioje lentelėje nurodytus apribojimus.

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

Atnaujinę versiją į "Project Operations", turite naudoti projekto planavimo API, kad galėtumėte vykdyti šių objektų kūrimo, naujinimo ir naikinimo operacijas:

|   Objekto pavadinimas           |   Loginis objekto pavadinimas       |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekto užduotis            | msdyn_projecttask           |
| Projekto užduoties priklausomybė | msdyn_projecttaskdependency |
| Išteklių priskyrimas     | msdyn_resourceassignment    |
| Projekto talpykla          | msdyn_projectbucket         |
| Projekto komandos narys     | msdyn_projectteam           |

Jei šiuo metu turite tinkinimų, susijusių su šiais objektais, diegimo rekomendacijų ieškokite [Projekto grafiko API naudojimas operacijoms su planavimo objektais](../project-management/schedule-api-preview.md) atlikti.

## <a name="data-model-changes"></a>Duomenų modelio pakeitimai

Kaip 1 versijos naujinimo etapo dalis, yra duomenų modelio pakeitimų. Šie pakeitimai visų pirma yra esamų objektų lauko pakeitimai. 1 etape objektai, **msydn_project** ir **msdyn_projectteam** yra tinkinimų pertvarkymas. 

> [!IMPORTANT]
> Šis skyrius bus atnaujintas naudojant papildomus objektus, kai bus baigti būsimi atnaujinimo etapai.

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

Buvo įtraukti šie laukai.

|   Entity          |   Loginis pavadinimas                               |   Aprašą |
|-------------------|----------------------------------------------|---------------|
| msdyn_project     | msdyn_actualfeesales                         | Rodo projekto faktinių mokesčio pardavimų suvestinę. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_actualmaterialcost                     | Rodo projekto faktinių medžiagų sąnaudų suvestinę. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_actualmaterialsales                    | Rodo projekto faktinių medžiagų pardavimų suvestinę. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_businesscase                           |                |
| msdyn_project     | msdyn_contractlineproject                    | Sutarties eilutė, susijusi su šiuo projektu. |
| msdyn_project     | msdyn_copyprojectcorrelationid               | Tai vidinės sistemos laukas, naudojamas kopijavimo **projektui**, susijusiam su koreliacijos identifikatoriumi. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_copyprojectsessionid                   | Tai vidinis sistemos laukas, naudojamas **kopijuoti projektą**, susijusį su seanso identifikatoriumi. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_globalrevisiontoken                    | Paskutinis sinchronizavimas xRM visuotinio modifikavimo atpažinimo ženklas iš projekto planavimo tarnybos. |
| msdyn_project     | msdyn_msprojectdocument                      | Projektui priklausantis "Microsoft Project" dokumentas. |
| msdyn_project     | msdyn_plannedmaterialcost                    | Planuojamų projekto materialinių sąnaudų suma. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_plannedmaterialsales                   | Planuojamų medžiagų pardavimų projekte visuma. Skirta naudoti tik "Project Service Automation". |
| msdyn_project     | msdyn_program                                | Programa, su kuriuo susijęs šis projektas. |
| msdyn_project     | msdyn_quotelineproject                       | Citatos eilutė, susijusi su šiuo projektu. |
| msdyn_project     | msdyn_replaylogheader                        | Pakartojimo žurnalų antraštė. |
| msdyn_project     | msdyn_schedulemode                           | Numatytasis planavimo režimas, naudojamas visoms projekto užduotims atlikti.  |
| msdyn_project     | msdyn_taskearlieststart                      | Anksčiausia bet kurios projekto užduoties pradžios data.  |
| msdyn_project     | msdyn_valuestatement                         |                |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Projekto komandos narys, iš kurio buvo nukopijuotas šis projekto komandos narys. |
| msdyn_projectteam | msdyn_creategenericteammemberwithrequirement | Nurodo, ar sukurti išteklių poreikį naujai sukurtam bendrosios komandos nariui.  |
| msdyn_projectteam | msdyn_deletestatus                           | Komandos nario naikinimo būsena, kad būtų galima stebėti, ar yra naikinimo užklausa, išsiųsta projekto planavimo tarnybai, ir ar ji sėkmingai siunčia atsakymą atgal per numatytą laiko tarpą. |
| msdyn_projectteam | msdyn_effortcompleted                        | Seka komandos nario pastangas, įdėtas atliekant užduotis. |
| msdyn_projectteam | msdyn_effortremaining                        | Seka pastangas, kurias komandos narys dar turi atlikti atlikdamas savo užduotis. |
| msdyn_projectteam | msdyn_markedfordeletiontimer                 | Laukimo laikotarpis nuo tada, kai komandos narys siunčia naikinimo užklausą projekto planavimo tarnybai, kol komandos narys iš tikrųjų panaikinamas Microsoft Dataverse.|
| msdyn_projectteam | msdyn_markedfordeletiontimestamp             | Laiko žyma, skirta įrašyti, kada komandos nario naikinimo užklausa siunčiama į projekto planavimo tarnybą. |
| msdyn_projectteam | msdyn_copiedfromprojectteammember            | Rodomas projekto komandos narys, iš kurio buvo nukopijuotas šis projekto komandos narys.  |

## <a name="project-templates"></a>Projekto šablonai

"Project Operations" nepalaiko projektų šablonų. Tačiau didžiąją dalį pagrindinių funkcijų galite atkartoti naudodami ["Project Copy" API](../project-management/dev-copy-project.md).

## <a name="desktop-add-in-support"></a>Darbalaukio papildinio palaikymas

"Microsoft Project Desktop" papildinio palaikymas nebus pasiekiamas per pirmuosius 2 versijos naujinimo etapus. 3 etape klientai, kurių projektai yra didesni nei šiuo metu palaikomi "Project for the Web" apribojimai, galės naudoti darbalaukio papildinį.

## <a name="editing-resource-assignment-contours"></a>Išteklių priskyrimo kontūrų redagavimas

Galimybė redaguoti išteklių priskyrimo kontūrus bus pasiekiama, kai bus pasiekiamas 2 versijos naujinimo etapas.

## <a name="billing-and-pricing"></a>Sąskaitų siuntimas ir kainodara

Šios naujos funkcijos įtrauktos į "Project Operations". Šios funkcijos yra papildomo pobūdžio ir neturi įtakos "Project Service Automation" duomenų modeliui.

- [Medžiagos naudojimo projektams ir projekto užduotims įrašyti įrašymas](../material/material-usage-log.md)
- [Subrangos valdymas](../pro/subcontracting/managing-subcontracts-overview.md)
- [Išankstinės arba išankstiniais apmokėjimais pagrįstos sutartys](../pro/sales/set-up-advances-retainer-based-contracts-sales.md)
- [Sutarties, kuri neviršija statuso, ir patvirtinimai](../pro/proforma-invoicing/manage-nte-status-validations-sales.md)
- [Užduotimis pagrįstas atsiskaitymas](../pro/sales/mapping-projects-tasks-quote-line-sales.md)

## <a name="deprecated-components"></a>Nebenaudojami komponentai

Toliau pateiktose lentelėse aprašomi visi nebenaudojami laukai, kurie po versijos naujinimo perkeliami į nebenaudojamų komponentų sprendimą. Daugiau informacijos ir nuorodą į sprendimą rasite [Dynamics 365 Project Service Automation 3x į Project Operations 4x nebenaudojami komponentai](https://github.com/microsoft/Dynamics365-Project-Operations-PowerApps/tree/main/3x-4x-deprecated-solution).

### <a name="invoicedetail"></a>Sąskaita faktūradetail

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
| msdyn_characteristicreqforteammember.msdyn_charakteristika                                     |
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
| msdyn_opportunitylineresourcecategory.msdyn_aprašymas                                       |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylineresourcecategoryid                 |
| msdyn_opportunitylineresourcecategory.msdyn_opportunitylinetransactionclassification          |
| msdyn_opportunitylineresourcecategory.msdyn_resourcecategory                                  |

### <a name="msdyn_opportunitylinetransaction"></a>msdyn_opportunitylinetransaction

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransaction.msdyn_accountcustomer                                        |
| msdyn_opportunitylinetransaction.msdyn_accountingdate                                         |
| msdyn_opportunitylinetransaction.msdyn_accountvendor                                          |
| msdyn_opportunitylinetransaction.msdyn_suma                                                 |
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
| msdyn_opportunitylinetransaction.msdyn_aprašymas                                            |
| msdyn_opportunitylinetransaction.msdyn_documentdate                                           |
| msdyn_opportunitylinetransaction.msdyn_enddatetime                                            |
| msdyn_opportunitylinetransaction.msdyn_exchangeeratedate                                       |
| msdyn_opportunitylinetransaction.msdyn_opportunityline                                        |
| msdyn_opportunitylinetransaction.msdyn_opportunitylinetransactionid                           |
| msdyn_opportunitylinetransaction.msdyn_procentų                                                |
| msdyn_opportunitylinetransaction.msdyn_kaina                                                  |
| msdyn_opportunitylinetransaction.msdyn_price_base                                             |
| msdyn_opportunitylinetransaction.msdyn_kainoraštis                                              |
| msdyn_opportunitylinetransaction.msdyn_product                                                |
| msdyn_opportunitylinetransaction.msdyn_projektas                                                |
| msdyn_opportunitylinetransaction.msdyn_kiekis                                               |
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
| msdyn_opportunitylinetransactioncategory.msdyn_aprašymas                                    |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactioncategoryid           |
| msdyn_opportunitylinetransactioncategory.msdyn_opportunitylinetransactionclassification       |
| msdyn_opportunitylinetransactioncategory.msdyn_transactioncategory                            |

### <a name="msdyn_opportunitylinetransactionclassificatio"></a>msdyn_opportunitylinetransactionclassificatio

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_opportunitylinetransactionclassificatio.msdyn_billingtype                               |
| msdyn_opportunitylinetransactionclassificatio.msdyn_aprašymas                               |
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
| msdyn_project.msdyn_likutis                                                            |
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
| msdyn_projecttask.msdyn_auto planavimas                                                        |
| msdyn_projecttask.msdyn_costestimatecontour                                                   |
| msdyn_projecttask.msdyn_effortcontour                                                         |
| msdyn_projecttask.msdyn_islinetask                                                            |
| msdyn_projecttask.msdyn_šaltinių_skaičius                                                     |
| msdyn_projecttask.msdyn_likutis                                                        |
| msdyn_projecttask.msdyn_resourceutilization                                                   |
| msdyn_projecttask.msdyn_salesestimatecontour                                                  |
| msdyn_projecttask.msdyn_scheduledhours                                                        |
| msdyn_projecttask.msdyn_wbsid                                                                 |

### <a name="msdyn_projecttaskstatususer"></a>msdyn_projecttaskstatususer

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projecttaskstatususer.msdyn_bookableresource                                            |
| msdyn_projecttaskstatususer.msdyn_aprašymas                                                 |
| msdyn_projecttaskstatususer.msdyn_expectedcompletiondate                                      |
| msdyn_projecttaskstatususer.msdyn_expectedhours tocomplete                                     |
| msdyn_projecttaskstatususer.msdyn_is completeleted                                                 |
| msdyn_projecttaskstatususer.msdyn_name                                                        |
| msdyn_projecttaskstatususer.msdyn_procentųiškomplektas                                             |
| msdyn_projecttaskstatususer.msdyn_projecttaskid                                               |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatusindicator                                  |
| msdyn_projecttaskstatususer.msdyn_projecttaskstatususerid                                     |

### <a name="msdyn_projectteam"></a>msdyn_projectteam

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| msdyn_projectteam.msdyn_applicantcount                                                        |
| msdyn_projectteam.msdyn_pareiškėjai pasiekiami                                                   |
| msdyn_projectteam.msdyn_assignedhours                                                         |
| msdyn_projectteam.msdyn_aprašymas                                                           |
| msdyn_projectteam.msdyn_from                                                                  |
| msdyn_projectteam.msdyn_hoursrequested                                                        |
| msdyn_projectteam.msdyn_membershipstatus                                                      |
| msdyn_projectteam.msdyn_numeris                                                                |
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
| msdyn_projecttransactioncategory.msdyn_projektas                                                |
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
| msdyn_resourceassignment.msdyn_valandos                                                          |
| msdyn_resourceassignment.msdyn_fromdate                                                       |
| msdyn_resourceassignment.msdyn_msprojectclientid                                              |
| msdyn_resourceassignment.msdyn_todate                                                         |
| msdyn_resourceassignmentdetail.msdyn_trukmė                                                 |
| msdyn_resourceassignmentdetail.msdyn_from                                                     |
| msdyn_resourceassignmentdetail.msdyn_name                                                     |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentdetailid                               |
| msdyn_resourceassignmentdetail.msdyn_resourceassignmentid                                     |

### <a name="salesorderdetail"></a>Pardavimų pavedimas

| Laukai                                                    |
|-----------------------------------------------------------------------------------------------|
| salesorderdetail.msdyn_quoteline                                                              |

