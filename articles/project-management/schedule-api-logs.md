---
title: Projektų planavimo žurnalai
description: Šiame straipsnyje pateikiama informacija ir pavyzdžiai, kurie padės naudoti projektų planavimo žurnalus, kad sektų triktis, susijusias su projektų planavimo paslauga ir projektų planavimo API.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923705"
---
# <a name="project-scheduling-logs"></a>Projektų planavimo žurnalai

_**Taikoma:** „Project Operations“ ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams, „Lite“ visuotinis diegimas – sąskaitų faktūrų išrašymo sandoris_, „_Project for the web_“

„Microsoft Dynamics 365 Project Operations“ naudoja [„Project for the Web“](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5), kaip pirminį planavimo įrankį. „Microsoft Dataverse“ „Project Operations" nenaudoja standartinių žiniatinklio programų programavimo sąsajų (API), o naudoja naujas projektų planavimo API projekto užduotims, išteklių priskyrimams, užduočių priklausomybiams, projektų telkiniams ir projektų komandų nariams kurti, naujinti ir naikinti. Tačiau kuriant, naujinant ar naikinant operacijas programiškai paleidžiant darbo paskirstymo struktūros (WBS) objektus, gali įvykti klaidų. Norint sekti šias klaidas ir operacijų retrospektyvą, įgyvendinti du nauji administravimo žurnalai: **Operacijų rinkinio** ir **Projektų planavimo paslaugos (PSS)**. Norėdami pasiekti šiuos žurnalus, eikite į **Parametrai** \> **Grafiko integravimas.**

Toliau pateiktoje iliustracijoje parodytas projekto planavimo žurnalo duomenų modelis.

![Projekto planavimo žurnalo duomenų modelis.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operacijų rinkinio žurnalas

Operacijų rinkinio žurnalas seka operacijų rinkinio, kuris naudojamas projektų, projektų užduočių, išteklių priskyrimų, užduočių priklausomybių, projekto nenaudoklių arba projekto komandos narių vieno ar kelių kūrimo, naujinimo arba naikinimo operacijų paketui vykdyti, vykdymą. Lauke **Operacijos būsena** rodomas bendras operacijų rinkinio statusas. Operacijos rinkinio apkrovos išsami informacija užfiksuota susijusiuose operacijos rinkinio išsamios informacijos įrašuose.

### <a name="operation-set"></a>Operacijų rinkinys

Toliau pateiktoje lentelėje nurodomi laukai, kurie yra susiję su **Operacijos rinkinio** objektu.

| Schemos pavadinimas            | Aprašą                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Operacijos užbaigimo arba nepavykusios operacijos data ir laikas.                                                | CompletedOn            |
| msdyn_correlationid   | Prašymo **correlationId** reikšmė.                                                                  | CorrelationId          |
| msdyn_description     | Operacijų rinkinio apibrėžtis.                                                                        | Aprašą            |
| msdyn_executedon      | Įrašo paleidimo data ir laikas                                                                       | Įvykdyta            |
| msdyn_operationsetId  | Objekto pavyzdžių unikalusis identifikatorius.                                                                   | OperationSet           |
| msdyn_Project         | Su operacijų rinkiniu susijęs projektas.                                                            | Project                |
| msdyn_projectid       | Prašymo **projectId** reikšmė.                                                                      | ProjectId (nerekomenduojama) |
| msdyn_projectName     | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_PSSErrorLog     | Projektų planavimo tarnybos klaidų žurnalo, susieto su operacijų rinkinio, unikalusis identifikatorius. | PSS klaidos žurnalas          |
| msdyn_PSSErrorLogName | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_status          | Operacijų rinkinio būsena.                                                                             | Būsena                 |
| msdyn_statusName      | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_useraadid       | Vartotojo, kuriam priklauso Azure Active Directory (Azure AD) užklausa, objekto ID.                     | UserAADID              |

### <a name="operation-set-detail"></a>Išsami operacijų rinkinio informacija

Toliau pateiktoje lentelėje nurodomi laukai, kurie yra susiję su **Išsamios operacijų rinkinio informacijos** objektu.

| Schemos pavadinimas                 | Aprašą                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Eilutėmis išdėstyti Dataverse laukai užklausai.                                            | CdsPayload            |
| msdyn_entityname           | Šios užklausos objekto pavadinimas.                                                     | EntityName            |
| msdyn_httpverb             | Užklausos metodas.                                                                         | HTTP veiksmažodis (nerekomenduojama) |
| msdyn_httpverbName         | Netaikoma.                                                                             | Netaikoma        |
| msdyn_operationset         | Operacijų rinkinio, kuriam priklauso šis įrašas, unikalusis identifikatorius.                      | OperationSet          |
| msdyn_operationsetdetailId | Objekto pavyzdžių unikalusis identifikatorius.                                                  | Išsami OperationSet informacija   |
| msdyn_operationsetName     | Netaikoma.                                                                             | Netaikoma        |
| msdyn_operationtype        | Išsamios operacijų rinkinio informacijos operacijų tipas.                                             | „OperationType“         |
| msdyn_operationtypeName    | Netaikoma.                                                                             | Netaikoma        |
| msdyn_psspayload           | Užklausos nuosekliojo projekto planavimo aptarnavimo laukai.                           | PssPayload            |
| msdyn_recordid             | Įrašo užklausos identifikatorius.                                                       | Įrašo ID             |
| msdyn_requestnumber        | Automatiškai sugeneruotas numeris, naudojamas užsakymui, į kurį gaunamos užklausos, identifikuoti. | Užklausos numeris        |

## <a name="project-scheduling-service-error-logs"></a>Projektų planavimo tarnybos klaidų žurnalas

Projektų planavimo tarnybos klaidų žurnale užfiksuojamos klaidos, atsirandančios, kai projektų planavimo tarnyba bando **Įrašyti** arba **Atidaryti** operaciją. Yra trys palaikomi scenarijai, kai generuojami šie žurnalai:

- Labai nepavyksta atlikti vartotojo inicijuotų veiksmų (pvz., negalima sukurti priskyrimo dėl trūkstamų teisių).
- Projektų planavimo tarnyba negali programiškai kurti, naujinti, panaikinti ar atlikti jokios kitos pakopinės objekto operacijos.
- Vartotojui kyla klaidų, kai įrašas neatidaromas (pvz., kai atidaromas projektas arba atnaujinama komandos nario informacija).

### <a name="project-scheduling-service-log"></a>Projektų planavimo tarnybos žurnalas

Toliau pateiktoje lentelėje nurodomi laukai, kurie yra įtraukti į projektų planavimo tarnybos žurnalą.

| Schemos pavadinimas          | Aprašą                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Išimties iškvietimų dėklas.                                               | Iškvietimų dėklas     |
| msdyn_correlationid | Klaidos sąsajos ID.                                               | CorrelationId  |
| msdyn_errorcode     | Laukelis, naudojamas „Dataverse“ klaidos kodui arba HTTP klaidos kodui saugoti. | Klaidos kodas     |
| msdyn_HelpLink      | Viešosios pagalbos dokumentacijos nuoroda.                                       | Žinyno saitas      |
| msdyn_log           | Žurnalą iš projektų planavimo paslaugos.                                   | Žurnalas            |
| msdyn_project       | Projektas, su kuriuo susietas klaidos žurnalas.                             | Project        |
| msdyn_projectName   | Projekto pavadinimas, jei bus išlikęs nustatytų operacijų krūvis. | Netaikoma |
| msdyn_psserrorlogId | Objekto pavyzdžių unikalusis identifikatorius.                                     | PSS klaidos žurnalas  |
| msdyn_SessionId     | Projekto seanso ID.                                                        | Seanso ID     |

## <a name="error-log-cleanup"></a>Klaidų žurnalo išvalymas

Pagal numatytuosius nustatymus projektų planavimo tarnybos klaidų žurnalus ir operacijų rinkinio žurnalą galima išvalyti kas 90 dienų. Visi anksčiau negu prieš 90 dienų pateikti trikčių įrašai bus panaikinti. Tačiau, pakeisdami puslapio **Projekto parametrai** lauko **msdyn_StateOperationSetAge** reikšmę, administratoriai gali koreguoti išvalymą nuo 1 iki 120 dienų. Yra keli šios reikšmės keitimo būdai:

- Tinkinkite **Projekto parametro** objektą sukurdami pasirinktinį puslapį ir įtraukdami lauką **„Stale Operations Set"**.
- Naudokite kliento kodą, kuris naudoja [„WebApi" programinės įrangos kūrimo rinkinį (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Naudokite aptarnavimo SDK kodą, kuris naudoja Xrm SDK **updateRecord** metodą (kliento API nuoroda) modeliu paremtose programose. „Power Apps“ turi aprašą ir palaikomus parametrus **updateRecord** metodui.

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
