---
title: Projektų planavimo žurnalai
description: Šioje temoje pateikiama informacija ir pavyzdžiai, kurie padės naudoti projektų planavimo žurnalus gedimams, susijusiems su projektų planavimo tarnyba ir projektų planavimo API, sekti.
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 1a58a588d3e2fb92f1b4a4ed0f6f69d0a63908db
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/14/2022
ms.locfileid: "8589528"
---
# <a name="project-scheduling-logs"></a>Projektų planavimo žurnalai

_**Taikoma: "Project Operations",** skirtos išteklių / nekauptų scenarijų scenarijui, "Lite" diegimas - sandoris su "proforma" SF išrašymu_, _"Project for the Web"_

"Microsoft" Dynamics 365 Project Operations naudoja ["Project" žiniatinklyje](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) kaip pagrindinį planavimo variklį. Užuot naudojusi standartines Microsoft Dataverse žiniatinklio programų programavimo sąsajas (API), "Project Operations" naudoja naujas projektų planavimo API, kad sukurtų, atnaujintų ir panaikintų projekto užduotis, išteklių priskyrimus, užduočių priklausomybes, projektų grupes ir projektų komandų narius. Tačiau, kai kūrimo, naujinimo ar naikinimo operacijos programiškai vykdomos darbo paskirstymo struktūros (WBS) objektuose, gali atsirasti klaidų. Šioms klaidoms ir operacijų retrospektyvai sekti buvo įdiegti du nauji administravimo žurnalai: **Operacijų rinkinys** ir **Projektų planavimo tarnyba (PSS)**. Norėdami pasiekti šiuos žurnalus, eikite į **Parametrų** \> **grafiko integravimas.**

Toliau pateiktoje iliustracijoje parodytas projektų planavimo žurnalų duomenų modelis.

![Projekto planavimo žurnalų duomenų modelis.](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>Operacijų rinkinio žurnalas

Operacijų rinkinio žurnalas seka operacijų rinkinio, naudojamo vienai ar kelioms projektų, projekto užduočių, išteklių priskyrimų, užduočių priklausomybių, projektų kibirų ar projekto komandos narių paketo operacijoms kurti, naujinti arba naikinti, vykdymą. Lauke **Operacija būsenoje** rodoma bendra operacijų rinkinio būsena. Išsami informacija apie operacijos nustatytą naudingąją apkrovą užfiksuojama susijusiuose operacijos išsamios informacijos nustatymo įrašuose.

### <a name="operation-set"></a>Operacijų rinkinys

Šioje lentelėje rodomi laukai, susiję **su objektu Operacijų rinkinys**.

| SchemaName            | Aprašą                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | Operacijos rinkinio užbaigimo arba nesėkmės data / laikas.                                                | CompletedOn            |
| msdyn_correlationid   | Užklausos **correlationId** vertė.                                                                  | CorrelationId          |
| msdyn_description     | Operacijų rinkinio aprašymas.                                                                        | Aprašą            |
| msdyn_executedon      | Įrašo vykdymo data / laikas.                                                                       | Įvykdyta            |
| msdyn_operationsetId  | Unikalusis objekto egzempliorių identifikatorius.                                                                   | OperationSet           |
| msdyn_Project         | Projektas, susijęs su operacijų rinkiniu.                                                            | Project                |
| msdyn_projectid       | Užklausos **projectId** vertė.                                                                      | ProjectId (nerekomenduojama) |
| msdyn_projectName     | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_PSSErrorLog     | Unikalusis projekto planavimo tarnybos klaidų žurnalo, susieto su operacijų rinkiniu, identifikatorius. | PSS klaidos žurnalas          |
| msdyn_PSSErrorLogName | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_status          | Operacijų rinkinio būsena.                                                                             | Būsena                 |
| msdyn_statusName      | Netaikoma.                                                                                              | Netaikoma         |
| msdyn_useraadid       | Vartotojo Azure Active Directory, kuriam priklauso užklausa, (Azure AD) objekto ID.                     | UserAADID              |

### <a name="operation-set-detail"></a>Operacijos rinkinio išsami informacija

Šioje lentelėje rodomi laukai, susiję su veiksmo **informacijos** rinkinio objektu.

| SchemaName                 | Aprašą                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | Nuoseklūs Dataverse užklausos laukai.                                            | CdsPayload            |
| msdyn_entityname           | Užklausos objekto pavadinimas.                                                     | EntityName            |
| msdyn_httpverb             | Prašymo metodas.                                                                         | HTTP veiksmažodis (nerekomenduojama) |
| msdyn_httpverbName         | Netaikoma.                                                                             | Netaikoma        |
| msdyn_operationset         | Unikalusis operacijos rinkinio, kuriam priklauso įrašas, identifikatorius.                      | OperationSet          |
| msdyn_operationsetdetailId | Unikalusis objekto egzempliorių identifikatorius.                                                  | Išsami OperationSet informacija   |
| msdyn_operationsetName     | Netaikoma.                                                                             | Netaikoma        |
| msdyn_operationtype        | Operacijos tipas, kuriame pateikiama išsami informacija apie operacijos informaciją.                                             | „OperationType“         |
| msdyn_operationtypeName    | Netaikoma.                                                                             | Netaikoma        |
| msdyn_psspayload           | Nuoseklūs užklausos projektų planavimo tarnybos laukai.                           | PssPayload            |
| msdyn_recordid             | Užklausos įrašo identifikatorius.                                                       | Įrašo ID             |
| msdyn_requestnumber        | Automatiškai sugeneruotas numeris, identifikuojantis užsakymą, kuriame buvo gautos užklausos. | Užklausos numeris        |

## <a name="project-scheduling-service-error-logs"></a>Projekto planavimo tarnybos klaidų žurnalai

Projekto planavimo tarnybos klaidų žurnalai užfiksuoja klaidas, atsirandančias projektų planavimo tarnybai bandant įrašyti **arba** atidaryti **operaciją**. Yra trys palaikomi scenarijai, kuriuose generuojami šie žurnalai:

- Vartotojo inicijuoti veiksmai kritiškai nepavyksta (pvz., priskyrimo sukurti negalima dėl trūkstamų teisių).
- Projektų planavimo tarnyba negali programiškai kurti, naujinti, naikinti ar atlikti jokios kitos pakopinės objekto operacijos.
- Vartotojas patiria klaidų, kai įrašas neatidaromas (pvz., kai atidaromas projektas arba atnaujinama komandos nario informacija).

### <a name="project-scheduling-service-log"></a>Projekto planavimo tarnybos žurnalas

Šioje lentelėje rodomi laukai, įtraukti į Projektų planavimo tarnybos žurnalą.

| SchemaName          | Aprašą                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | Išimties iškvietimų dėklas.                                               | Iškvietimų dėklas     |
| msdyn_correlationid | Klaidos koreliacijos ID.                                               | CorrelationId  |
| msdyn_errorcode     | Laukas, naudojamas klaidos kodui arba HTTP klaidos kodui saugoti Dataverse. | Klaidos kodas     |
| msdyn_HelpLink      | Nuoroda į viešąjį žinyno dokumentaciją.                                       | Žinyno saitas      |
| msdyn_log           | Žurnalas iš Projektų planavimo tarnybos.                                   | Žurnalas            |
| msdyn_project       | Projektas, susietas su klaidų žurnalu.                             | Project        |
| msdyn_projectName   | Projekto pavadinimas, jei operacijų rinkinio naudingoji apkrova bus išlaikyta. | Netaikoma |
| msdyn_psserrorlogId | Unikalusis objekto egzempliorių identifikatorius.                                     | PSS klaidos žurnalas  |
| msdyn_SessionId     | Projekto seanso ID.                                                        | Seanso ID     |

## <a name="error-log-cleanup"></a>Klaidų žurnalo valymas

Pagal numatytuosius nustatymus tiek "Project Scheduling Service" klaidų žurnalus, tiek operacijų rinkinio žurnalą galima išvalyti kas 90 dienų. Visi senesni nei 90 dienų įrašai bus ištrinti. Tačiau puslapyje Projekto parametrai **pakeisdami lauko** msdyn_StateOperationSetAge **reikšmę**, administratoriai gali koreguoti valymo diapazoną taip, kad jis būtų nuo 1 iki 120 dienų. Galimi keli šios vertės keitimo būdai:

- Tinkinkite objektą **Projekto parametras** sukurdami pasirinktinį puslapį ir įtraukdami **lauką Pasenusių operacijų nustatymo amžius**.
- Naudokite kliento kodą, kuris naudoja ["WebApi" programinės įrangos kūrimo rinkinį (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord).
- Naudokite tarnybos SDK kodą, kuris modelių valdomose programose naudoja Xrm SDK **updateRecord** metodą (kliento API nuoroda). Power Apps apima updateRecord **metodo aprašą ir palaikomus parametrus**.

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
