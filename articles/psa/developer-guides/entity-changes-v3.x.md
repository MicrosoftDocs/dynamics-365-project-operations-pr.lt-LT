---
title: Objekto, valdiklio ir vartotojo sąsajos pakeitimai („Project Service Automation 3.x“)
description: Šioje temoje aprašomi „Microsoft Dynamics Project Service Automation 3.x“ skirti sprendimo pakeitimai.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/15/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 2d93e5eaae7cff302be1cb2e96e3f45c24739b0c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4081031"
---
# <a name="entity-control-and-user-interface-changes-project-service-automation-3x"></a>Objekto, valdiklio ir vartotojo sąsajos pakeitimai („Project Service Automation 3.x“)
Išleidus „Microsoft Dynamics Project Service Automation (PSA), 3.x“, buvo pristatyta daug objektų, valdiklių, rodinių ir vartotojo sąsajos pakeitimų. Šioje temoje pateikiama informacija, susijusi su šiais svarbiais pakeitimais.

## <a name="parent-child-relationships-for-sales-document-sales-document-line-sales-document-line-detail-entities"></a>Pardavimo dokumento, pardavimo dokumento eilutės, pardavimo dokumento eilutės informacijos objektų pirminių ir antrinių elementų ryšiai
Naudojant „Dynamics 365 Project Service Automation“ (PSA) versijas, išleistas iki versijos 3.0, kai kurie ryšiai tarp pardavimo dokumentų, pardavimo dokumento eilučių ir pardavimo dokumento eilutės informacijos objektų būdavo įdiegiami naudojant eilutės laukus, kuriuose būdavo susijusio objekto GUID eilutės atvaizdavimas. Taip vykdavo dėl platformos apribojimų, o norint juos pašalinti reikėdavo atlikti nemažai pasirinktinio programavimo darbų serveryje ir iš kliento sprendimo pusės, kad šie ryšiai veiktų panašiai, kaip įprasti „Dynamics CRM“ objekto ryšiai, o eilučių laukai veiktų kaip peržvalgos laukai.

PSA 3.0 buvo atnaujinta, kad tarp pardavimo dokumento ir pardavimo dokumento eilutės objektų būtų galima panaudoti naujus objekto ryšius.

Kadangi peržvalgos laukus dabar galima naudoti nuorodoms į objektus kurti, laukai, kuriuose būdavo susijusio objekto GUID eilutės vertė, ankstesnėse versijose tapo nebereikalingi ir yra nebenaudojami. Taip pat nebenaudojama pasirinktinio redagavimo iš kliento ir serverio pusės funkcija, kurią naudojant tvarkomi ryšiai, apibrėžti senstelėjusių eilučių laukuose.

### <a name="entity-schema-changes"></a>Objekto schemos pakeitimai
Šioje lentelėje pateikiamas „vienas su vienu“ nebenaudojamų eilutės laukų ir naujų objektų peržvalgos laukų sąrašas. 

 Objektas |   Nebenaudojamas laukas (eilutė) | Naujas laukas (peržvalga)
--- | --- | ---
invoicedetail (sąskaitos faktūros eilutė) |  msdyn_contractline |    msdyn_contractlineid
msdyn_actual (faktinis dydis) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_contractlineinvoiceschedule (projekto sutarties eilutės sąskaitos faktūros grafikas) |    msdyn_contractline |    msdyn_contractlineid
msdyn_contractlinescheduleofvalue (projekto sutarties eilutės etapas) |   msdyn_contractline |    msdyn_contractlineid
msdyn_fact (faktinis dydis) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_invoicelinetransaction (sąskaitos faktūros eilutės informacija) | msdyn_invoiceline <br> msdyn_salescontractline | msdyn_invoicelineid <br> msdyn_salescontractlineid
msdyn_journalline (žurnalo eilutė) |  msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlineresourcecategory (projekto sutarties eilutės išteklių kategorija) | msdyn_salescontractline |   msdyn_contractlineid
msdyn_orderlinetransaction (projekto sutarties eilutės informacija) | msdyn_salescontractline |   msdyn_salescontractlineid
msdyn_orderlinetransactioncategory (projekto sutarties eilutės operacijos kategorija) |   msdyn_contractline |    msdyn_contractlineid
msdyn_orderlinetransactionclassification (projekto sutarties eilutės operacijų klasifikacija) |   msdyn_contractline |    msdyn_contractlineid
msdyn_quotelineinvoiceschedule (pasiūlymo eilutės sąskaitos faktūros grafikas) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelineresourcecategory (pasiūlymo eilutės išteklių kategorija) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinescheduleofvalue (pasiūlymo eilutės etapas) | msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransaction (pasiūlymo eilutės informacija) |    msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactioncategory (pasiūlymo eilutės operacijos kategorija) |  msdyn_quoteline |   msdyn_quotelineid
msdyn_quotelinetransactionclassification (pasiūlymo eilutės operacijų klasifikacija) |  msdyn_quoteline |   msdyn_quotelineid
SalesOrderDetail (užsakymo eilutė) | msdyn_quotelineid | msdyn_quoteline 

### <a name="deprecated-custom-views-and-controls"></a>Nebenaudojami pasirinktiniai rodiniai ir valdikliai
Nebenaudojami toliau nurodyti pasirinktiniai rodiniai ir valdikliai bei su jais susiję artefaktai.

- Apmokestinimo rodinys.
- Pasirinktiniai tinklelio valdikliai, skirti pasiūlymo eilutės informacijai puslapio **Projekto informacija** pasiūlymo eilutėje pateikti.
- Pasirinktiniai tinklelio valdikliai, skirti projekto sutarties eilutės informacijai puslapio **Projekto informacija** pardavimo užsakymo eilutėje pateikti.

> [!NOTE]
> Norėdami pamatyti visą nebenaudojamų išteklių sąrašą, žr. [Nebenaudojami „Project Service Automation v3.x“ žiniatinklio ištekliai](../developer-guides/web-resources-deprecated-v3.x.md)

## <a name="unified-client-interface-app-module"></a>Vieningosios kliento sąsajos programėlės modulis
Pristačius vieningosios kliento sąsajos (UCI) programėlės modulį, PSA svetainės struktūros įrašai buvo pašalinti iš sistemos.  
Galimybės, pasiūlymo, užsakymo, sąskaitos faktūros funkcijos, susijusios su formų perjungimu, nebenaudojamos, nes UCI programėlės modulyje teikiamos tik formų PSA versijos.  

Nebenaudojami šie žiniatinklio ištekliai:

- msdyn_\SalesDocument\SalesDocumentFormLoader.js
- msdyn_\SalesDocument\PSSalesDocumentCustomFormIds.js

> [!NOTE]
> Norėdami pamatyti visą nebenaudojamų išteklių sąrašą, žr. [Nebenaudojami „Project Service Automation v3.x“ žiniatinklio ištekliai](../developer-guides/web-resources-deprecated-v3.x.md).


