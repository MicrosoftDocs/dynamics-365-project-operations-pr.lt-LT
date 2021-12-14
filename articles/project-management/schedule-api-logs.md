---
title: Projekto planavimo žurnalai
description: Šioje temoje pateikiama informacija ir pavyzdžiai, kurie padės naudoti projekto planavimo žurnalus gedimams, susijusiems su projektų planavimo tarnyba ir projektų planavimo API, sekti.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 1c5632a880fa30d1b863c326b22e3d930c9564dc
ms.sourcegitcommit: 844ec8eacd0fc10d1659b437cc5cbb4480ec9e1e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/01/2021
ms.locfileid: "7877515"
---
# <a name="project-scheduling-logs"></a>Projekto planavimo žurnalai

_**Taikoma:** projekto operacijos išteklių / ne sandėlyje pagrįsti scenarijai, Lite diegimas - spręsti proforma SF išrašymas_, projektas _internete_

"Microsoft Dynamics 365 Project Operations naudoja ["Project" žiniatinklyje](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kaip pagrindinį planavimo modulį. Užuot naudojus standartines Microsoft Dataverse žiniatinklio programų programavimo sąsajas (API), projekto operacijos naudoja naujas projektų planavimo API projekto užduotims, išteklių priskyrimams, užduočių priklausomybėms, projektų grupėms ir projektų komandų nariams kurti, naujinti ir naikinti. Tačiau, kai kurti, atnaujinti arba naikinti operacijas programiškai paleisti darbo paskirstymo struktūros (WBS) objektų, gali atsirasti klaidų. Norint sekti šias klaidas ir operacijų retrospektyvą, įdiegti du nauji administravimo žurnalai: **operacijų rinkinys ir projekto planavimo tarnyba** **(PSS).** Norėdami pasiekti šiuos žurnalus, eikite į **Parametrų** \> **tvarkaraščio integravimas**.

Šioje iliustracijoje parodytas projekto planavimo žurnalų duomenų modelis.

![Projekto planavimo žurnalų duomenų modelis.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operacijų rinkinio žurnalas

Operacijų rinkinio žurnalas seka operacijų rinkinio, naudojamo vykdyti vieną ar kelias projektų, projekto užduočių, išteklių priskyrimų, užduočių priklausomybių, projektų grupių arba projekto komandos narių paketo operacijas, vykdymą. **Lauke Operacija būsenoje rodoma bendra operacijų rinkinio** būsena. Operacijos rinkinio naudingosios apkrovos informacija fiksuojama susijusiuose operacijų rinkinio išsamių įrašų duomenyse.

### <a name="operation-set"></a>Operacijų rinkinys

Šioje lentelėje rodomi laukai, susiję su **objektu Operacijų** rinkinys.

| SchemaName            | Aprašą                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Operacijos rinkinio užbaigimo arba nesėkmingo vykdymo data / laikas.                                                | CompletedOn            |
| msdyn_correlationid   | **Užklausos correlationId** reikšmė.                                                                  | CorrelationId          |
| msdyn_description     | Operacijų rinkinio aprašymas.                                                                        | Aprašą            |
| msdyn_executedon      | Įrašo vykdymo data / laikas.                                                                       | Įvykdyta            |
| msdyn_operationsetId  | Objekto egzempliorių unikalusis identifikatorius.                                                                   | OperationSet           |
| msdyn_Project         | Projektas, susijęs su operacijų rinkiniu.                                                            | Project                |
| msdyn_projectid       | **Užklausos projectId** reikšmė.                                                                      | ProjectId (nerekomenduojama) |
| msdyn_projectName     | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_PSSErrorLog     | Projektų planavimo tarnybos klaidų žurnalo, susieto su operacijų rinkiniu, unikalusis identifikatorius. | PSS klaidos žurnalas          |
| msdyn_PSSErrorLogName | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_status          | Operacijų rinkinio būsena.                                                                             | Būsena                 |
| msdyn_statusName      | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_useraadid       | Vartotojo, kuriam priklauso užklausa, Azure Active Directory (Azure AD) objekto ID.                     | UserAADID              |

### <a name="operation-set-detail"></a>Išsami operacijos rinkinio informacija

Šioje lentelėje rodomi laukai, susiję su **objektu Išsami operacijos rinkinio** informacija.

| SchemaName                 | Aprašą                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Užklausos Dataverse laukai eilutėmis.                                            | CdsPayload            |
| msdyn_entityname           | Užklausos objekto pavadinimas.                                                     | EntityName            |
| msdyn_httpverb             | Užklausos metodas.                                                                         | HTTP veiksmažodis (nerekomenduojama) |
| msdyn_httpverbName         | Netaikoma.                                                                             | Netaikoma        |
| msdyn_operationset         | Unikalusis operacijų rinkinio, kuriam priklauso įrašas, identifikatorius.                      | OperationSet          |
| msdyn_operationsetdetailId | Objekto egzempliorių unikalusis identifikatorius.                                                  | Išsami OperationSet informacija   |
| msdyn_operationsetName     | Netaikoma.                                                                             | Netaikoma        |
| msdyn_operationtype        | Operacijos rinkinio išsamumo operacijos tipas.                                             | „OperationType“         |
| msdyn_operationtypeName    | Netaikoma.                                                                             | Netaikoma        |
| msdyn_psspayload           | Užklausos laukai Serijinis projekto planavimo tarnyba.                           | PssPayload            |
| msdyn_recordid             | Užklausos įrašo identifikatorius.                                                       | Įrašo ID             |
| msdyn_requestnumber        | Automatiškai sugeneruotas numeris, identifikuojantis užsakymą, kuriuo buvo gautos užklausos. | Užklausos numeris        |

## <a name="project-scheduling-service-error-logs"></a>Projekto planavimo tarnybos klaidų žurnalai

Projekto planavimo tarnybos klaidų žurnaluose fiksuojamos triktys, kurios įvyksta, kai projekto planavimo tarnyba bando **įrašyti** arba atidaryti **operaciją**. Yra trys palaikomi scenarijai, kai šie žurnalai generuojami:

- Vartotojo inicijuoti veiksmai kritiškai nepavyksta (pvz., priskyrimo sukurti negalima dėl trūkstamų teisių).
- Projekto planavimo tarnyba negali programiškai kurti, naujinti, naikinti ar atlikti jokios kitos pakopinės objekto operacijos.
- Vartotojas patiria klaidų, kai įrašo nepavyksta atidaryti (pvz., kai atidaromas projektas arba atnaujinama komandos nario informacija).

### <a name="project-scheduling-service-log"></a>Projekto planavimo tarnybos žurnalas

Šioje lentelėje rodomi laukai, įtraukti į projekto planavimo tarnybos žurnalą.

| SchemaName          | Aprašą                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Išimties iškvietimų dėklas.                                               | Iškvietimų dėklas     |
| msdyn_correlationid | Klaidos koreliacijos ID.                                               | CorrelationId  |
| msdyn_errorcode     | Laukas, naudojamas Dataverse klaidos kodui arba HTTP klaidos kodui saugoti. | Klaidos kodas     |
| msdyn_HelpLink      | Saitas su vieša žinyno dokumentacija.                                       | Žinyno saitas      |
| msdyn_log           | Žurnalas iš projektų planavimo tarnybos.                                   | Žurnalas            |
| msdyn_project       | Projektas, susietas su klaidų žurnalu.                             | Project        |
| msdyn_projectName   | Projekto pavadinimas, jei bus išlaikyta operacijų rinkinio naudingoji apkrova. | Netaikoma |
| msdyn_psserrorlogId | Objekto egzempliorių unikalusis identifikatorius.                                     | PSS klaidos žurnalas  |
| msdyn_SessionId     | Projekto seanso ID.                                                        | Seanso ID     |

## <a name="error-log-cleanup"></a>Klaidų žurnalo valymas

Pagal numatytuosius nustatymus tiek projekto planavimo tarnybos klaidų žurnalus, tiek operacijų rinkinio žurnalą galima išvalyti kas 90 dienų. Visi senesni nei 90 dienų įrašai bus panaikinti. Tačiau keisdami puslapio **Projekto parametrai lauko msdyn_StateOperationSetAge** **reikšmę**, administratoriai gali koreguoti valymo diapazoną, kad jis būtų nuo 1 iki 120 dienų. Galimi keli šios reikšmės keitimo būdai:

- Tinkinkite **objektą Projekto parametras** sukurdami pasirinktinį puslapį ir įtraukdami **lauką Pasenęs operacijų rinkinio** amžius.
- Naudokite kliento kodą, kuris naudoja [WebApi programinės įrangos kūrimo rinkinys (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Naudokite tarnybos SDK kodą, kuris naudoja Xrm SDK **updateRecord** metodą (kliento API nuoroda) modeliu pagrįstose programose. Power Apps yra naujinimoįrašo metodo aprašas ir palaikomi **parametrai**.

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
