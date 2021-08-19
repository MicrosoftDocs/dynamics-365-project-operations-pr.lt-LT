---
title: Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti
description: Šioje temoje pateikiama informacija apie projekto grafiko API sąsajų naudojimą ir jo pavyzdžiai.
author: sigitac
ms.date: 06/22/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 55bd9020275fbb72761b45ba09294f57266b418c0e5b506ba55a2a498aff24e5
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7008776"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

> [!IMPORTANT] 
> Kai kurios arba visos šioje temoje paminėtos funkcijos pasiekiamos kaip peržiūros versijos leidimo dalis. Turinys ir funkcijos gali keistis. 

## <a name="scheduling-entities"></a>Grafiko objektai

Projekto grafiko API sąsajos suteikia galimybę atlikti kūrimo, naujinimo ir naikinimo operacijas su **planavimo objektais**. Šie objektai valdomi naudojant „Project for the Web“ planavimo variklį. Ankstesniuose „Dynamics 365 Project Operations“ leidimuose operacijų kūrimas, naujinimas ir naikinimas naudojant **planavimo objektus** buvo apribotas.

Toliau esančioje lentelėje pateikiamas visas projekto grafiko objektų sąrašas.

| Objekto pavadinimas  | Loginis objekto pavadinimas |
| --- | --- |
| Project | msdyn_project |
| Projekto užduotis  | msdyn_projecttask  |
| Projekto užduoties priklausomybė  | msdyn_projecttaskdependency  |
| Išteklių priskyrimas | msdyn_resourceassignment |
| Projekto talpykla  | msdyn_projectbucket |
| Projekto komandos narys | msdyn_projectteam |

## <a name="operationset"></a>OperationSet

OperationSet yra darbo vieneto modelis, kurį galima naudoti, kai operacijoje reikia apdoroti keletą grafikui poveikį darančių užklausų.

## <a name="project-schedule-apis"></a>Projekto grafiko API sąsajos

Toliau pateikiamas dabartinių projekto grafiko API sąrašas.

- **msdyn_CreateProjectV1**: šį API galima naudoti norint sukurti projektą. Projektas ir numatytoji projekto talpykla sukuriami nedelsiant.
- **msdyn_CreateTeamMemberV1**:šį API galima naudoti norint sukurti projekto komandos narį. Komandos nario įrašas sukuriamas nedelsiant.
- **msdyn_CreateOperationSetV1**: šį API galima naudoti norint suplanuoti keletą užklausų, kurias reikia atlikti operacijoje.
- **msdyn_PSSCreateV1**: šį API galima naudoti norint sukurti objektą. Toks objektas gali būti bet kuris projekto planavimo objektas, kuris palaiko kūrimo operaciją.
- **msdyn_PSSUpdateV1**: šį API galima naudoti norint atnaujinti objektą. Toks objektas gali būti bet kuris projekto planavimo objektas, kuris palaiko naujinimo operaciją.
- **msdyn_PSSDeleteV1**: šį API galima naudoti norint panaikinti objektą. Toks objektas gali būti bet kuris projekto planavimo objektas, kuris palaiko naikinimo operaciją.
- **msdyn_ExecuteOperationSetV1**: šis API naudojamas norint vykdyti visas nurodyto operacijų rinkinio operacijas.

## <a name="using-project-schedule-apis-with-operationset"></a>Projekto grafiko API sąsajų naudojimas su OperationSet

Kadangi įrašai, naudojant **CreateProjectV1** ir **CreateTeamMemberV1**, sukuriami nedelsiant, šių API negalima naudoti tiesiai **OperationSet**. Tačiau API galite naudoti norėdami sukurti reikiamus įrašus, **OperationSet**, tada šiuos iš anksto sukurtus įrašus panaudoti **OperationSet**.

## <a name="supported-operations"></a>Palaikomos operacijos

| Grafiko objektas | Kūrimas | Atnaujinimas | Delete | Svarbi informacija |
| --- | --- | --- | --- | --- |
Projekto užduotis | Taip | Taip | Taip | Nėra |
| Projekto užduoties priklausomybė | Taip | Taip | | Projekto užduoties priklausomybės įrašai neatnaujinami. Vietoj to, seną įrašą galima panaikinti ir sukurti naują. |
| Išteklių priskyrimas | Taip | Taip | | Nepalaikomos operacijos, kurioms naudojami šie laukai: **BookableResourceID**, **Pastangos**, **EffortCompleted**, **EffortRemaining** ir **PlannedWork**. Išteklių priskyrimo įrašai neatnaujinami. Vietoj to, seną įrašą galima panaikinti ir sukurti naują. |
| Projekto talpykla | Netaikoma | Netaikoma | Netaikoma | Numatytoji talpykla sukuriama naudojant **CreateProjectV1** API. |
| Projekto komandos narys | Taip | Taip | Taip | Kūrimo operacijai naudokite **CreateTeamMemberV1** API. |
| Project | Taip | Taip | Netaikoma | Nepalaikomos operacijos, kurioms naudojami šie laukai: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Pastangos**, **EffortCompleted**, **EffortRemaining**, **Eiga**, **Pabaiga**, **TaskEarliestStart** ir **Duration**. |

Šias API galima iškviesti naudojant objektus, kuriuose įtraukti pasirinktini laukai.

ID ypatybė yra pasirinktinė. Jei ji pateikta, sistema bando ypatybę panaudoti ir, jei to padaryti negalima, pateikia išimtį. Jei ypatybė nepateikta, sistema ją sugeneruos.

## <a name="restricted-fields"></a>Apriboti laukai

Toliau pateikiamose lentelėse apibrėžiami laukai, kurių negalima **Kurti** ir **Redaguoti**.

### <a name="project-task"></a>Projekto užduotis

| **Loginis pavadinimas**                       | **Gali kurti** | **Gali redaguoti**     |
|----------------------------------------|----------------|------------------|
| msdyn_actualcost                       | ne             | ne               |
| msdyn_actualcost_base                  | ne             | ne               |
| msdyn_actualend                        | ne             | ne               |
| msdyn_actualsales                      | ne             | ne               |
| msdyn_actualsales_base                 | ne             | ne               |
| msdyn_actualstart                      | ne             | ne               |
| msdyn_costatcompleteestimate           | ne             | ne               |
| msdyn_costatcompleteestimate_base      | ne             | ne               |
| msdyn_costconsumptionpercentage        | ne             | ne               |
| msdyn_effortcompleted                  | ne             | ne               |
| msdyn_effortestimateatcomplete         | ne             | ne               |
| msdyn_iscritical                       | ne             | ne               |
| msdyn_iscriticalname                   | ne             | ne               |
| msdyn_ismanual                         | ne             | ne               |
| msdyn_ismanualname                     | ne             | ne               |
| msdyn_ismilestone                      | ne             | ne               |
| msdyn_ismilestonename                  | ne             | ne               |
| msdyn_LinkStatus                       | ne             | ne               |
| msdyn_linkstatusname                   | ne             | ne               |
| msdyn_msprojectclientid                | ne             | ne               |
| msdyn_plannedcost                      | ne             | ne               |
| msdyn_plannedcost_base                 | ne             | ne               |
| msdyn_plannedsales                     | ne             | ne               |
| msdyn_plannedsales_base                | ne             | ne               |
| msdyn_pluginprocessingdata             | ne             | ne               |
| msdyn_progress                         | ne             | ne (taip, jei P4W) |
| msdyn_remainingcost                    | ne             | ne               |
| msdyn_remainingcost_base               | ne             | ne               |
| msdyn_remainingsales                   | ne             | ne               |
| msdyn_remainingsales_base              | ne             | ne               |
| msdyn_requestedhours                   | ne             | ne               |
| msdyn_resourcecategory                 | ne             | ne               |
| msdyn_resourcecategoryname             | ne             | ne               |
| msdyn_resourceorganizationalunitid     | ne             | ne               |
| msdyn_resourceorganizationalunitidname | ne             | ne               |
| msdyn_salesconsumptionpercentage       | ne             | ne               |
| msdyn_salesestimateatcomplete          | ne             | ne               |
| msdyn_salesestimateatcomplete_base     | ne             | ne               |
| msdyn_salesvariance                    | ne             | ne               |
| msdyn_salesvariance_base               | ne             | ne               |
| msdyn_scheduleddurationminutes         | ne             | ne               |
| msdyn_scheduledend                     | ne             | ne               |
| msdyn_scheduledstart                   | ne             | ne               |
| msdyn_schedulevariance                 | ne             | ne               |
| msdyn_skipupdateestimateline           | ne             | ne               |
| msdyn_skipupdateestimatelinename       | ne             | ne               |
| msdyn_summary                          | ne             | ne               |
| msdyn_varianceofcost                   | ne             | ne               |
| msdyn_varianceofcost_base              | ne             | ne               |

### <a name="project-task-dependency"></a>Projekto užduoties priklausomybė

| **Loginis pavadinimas**              | **Gali kurti** | **Gali redaguoti** |
|-------------------------------|----------------|--------------|
| msdyn_linktype                | ne             | ne           |
| msdyn_linktypename            | ne             | ne           |
| msdyn_predecessortask         | taip            | ne           |
| msdyn_predecessortaskname     | taip            | ne           |
| msdyn_project                 | taip            | ne           |
| msdyn_projectname             | taip            | ne           |
| msdyn_projecttaskdependencyid | taip            | ne           |
| msdyn_successortask           | taip            | ne           |
| msdyn_successortaskname       | taip            | ne           |

### <a name="resource-assignment"></a>Išteklių priskyrimas

| **Loginis pavadinimas**             | **Gali kurti** | **Gali redaguoti** |
|------------------------------|----------------|--------------|
| msdyn_bookableresourceid     | taip            | ne           |
| msdyn_bookableresourceidname | taip            | ne           |
| msdyn_bookingstatusid        | ne             | ne           |
| msdyn_bookingstatusidname    | ne             | ne           |
| msdyn_committype             | ne             | ne           |
| msdyn_committypename         | ne             | ne           |
| msdyn_effort                 | ne             | ne           |
| msdyn_effortcompleted        | ne             | ne           |
| msdyn_effortremaining        | ne             | ne           |
| msdyn_finish                 | ne             | ne           |
| msdyn_plannedcost            | ne             | ne           |
| msdyn_plannedcost_base       | ne             | ne           |
| msdyn_plannedcostcontour     | ne             | ne           |
| msdyn_plannedsales           | ne             | ne           |
| msdyn_plannedsales_base      | ne             | ne           |
| msdyn_plannedsalescontour    | ne             | ne           |
| msdyn_plannedwork            | ne             | ne           |
| msdyn_projectid              | taip            | ne           |
| msdyn_projectidname          | ne             | ne           |
| msdyn_projectteamid          | ne             | ne           |
| msdyn_projectteamidname      | ne             | ne           |
| msdyn_start                  | ne             | ne           |
| msdyn_taskid                 | ne             | ne           |
| msdyn_taskidname             | ne             | ne           |
| msdyn_userresourceid         | ne             | ne           |

### <a name="project-team-member"></a>Projekto komandos narys

| **Loginis pavadinimas**                                 | **Gali kurti** | **Gali redaguoti** |
|--------------------------------------------------|----------------|--------------|
| msdyn_calendarid                                 | ne             | ne           |
| msdyn_creategenericteammemberwithrequirementname | ne             | ne           |
| msdyn_deletestatus                               | ne             | ne           |
| msdyn_deletestatusname                           | ne             | ne           |
| msdyn_effort                                     | ne             | ne           |
| msdyn_effortcompleted                            | ne             | ne           |
| msdyn_effortremaining                            | ne             | ne           |
| msdyn_finish                                     | ne             | ne           |
| msdyn_hardbookedhours                            | ne             | ne           |
| msdyn_hours                                      | ne             | ne           |
| msdyn_markedfordeletiontimer                     | ne             | ne           |
| msdyn_markedfordeletiontimestamp                 | ne             | ne           |
| msdyn_msprojectclientid                          | ne             | ne           |
| msdyn_percentage                                 | ne             | ne           |
| msdyn_requiredhours                              | ne             | ne           |
| msdyn_softbookedhours                            | ne             | ne           |
| msdyn_start                                      | ne             | ne           |

### <a name="project"></a>Project

| **Loginis pavadinimas**                       | **Gali kurti** | **Gali redaguoti** |
|----------------------------------------|----------------|--------------|
| msdyn_actualexpensecost                | ne             | ne           |
| msdyn_actualexpensecost_base           | ne             | ne           |
| msdyn_actuallaborcost                  | ne             | ne           |
| msdyn_actuallaborcost_base             | ne             | ne           |
| msdyn_actualsales                      | ne             | ne           |
| msdyn_actualsales_base                 | ne             | ne           |
| msdyn_contractlineproject              | taip            | ne           |
| msdyn_contractorganizationalunitid     | taip            | ne           |
| msdyn_contractorganizationalunitidname | taip            | ne           |
| msdyn_costconsumption                  | ne             | ne           |
| msdyn_costestimateatcomplete           | ne             | ne           |
| msdyn_costestimateatcomplete_base      | ne             | ne           |
| msdyn_costvariance                     | ne             | ne           |
| msdyn_costvariance_base                | ne             | ne           |
| msdyn_duration                         | ne             | ne           |
| msdyn_effort                           | ne             | ne           |
| msdyn_effortcompleted                  | ne             | ne           |
| msdyn_effortestimateatcompleteeac      | ne             | ne           |
| msdyn_effortremaining                  | ne             | ne           |
| msdyn_finish                           | taip            | taip          |
| msdyn_globalrevisiontoken              | ne             | ne           |
| msdyn_islinkedtomsprojectclient        | ne             | ne           |
| msdyn_islinkedtomsprojectclientname    | ne             | ne           |
| msdyn_linkeddocumenturl                | ne             | ne           |
| msdyn_msprojectdocument                | ne             | ne           |
| msdyn_msprojectdocumentname            | ne             | ne           |
| msdyn_plannedexpensecost               | ne             | ne           |
| msdyn_plannedexpensecost_base          | ne             | ne           |
| msdyn_plannedlaborcost                 | ne             | ne           |
| msdyn_plannedlaborcost_base            | ne             | ne           |
| msdyn_plannedsales                     | ne             | ne           |
| msdyn_plannedsales_base                | ne             | ne           |
| msdyn_progress                         | ne             | ne           |
| msdyn_remainingcost                    | ne             | ne           |
| msdyn_remainingcost_base               | ne             | ne           |
| msdyn_remainingsales                   | ne             | ne           |
| msdyn_remainingsales_base              | ne             | ne           |
| msdyn_replaylogheader                  | ne             | ne           |
| msdyn_salesconsumption                 | ne             | ne           |
| msdyn_salesestimateatcompleteeac       | ne             | ne           |
| msdyn_salesestimateatcompleteeac_base  | ne             | ne           |
| msdyn_salesvariance                    | ne             | ne           |
| msdyn_salesvariance_base               | ne             | ne           |
| msdyn_scheduleperformance              | ne             | ne           |
| msdyn_scheduleperformancename          | ne             | ne           |
| msdyn_schedulevariance                 | ne             | ne           |
| msdyn_taskearlieststart                | ne             | ne           |
| msdyn_teamsize                         | ne             | ne           |
| msdyn_teamsize_date                    | ne             | ne           |
| msdyn_teamsize_state                   | ne             | ne           |
| msdyn_totalactualcost                  | ne             | ne           |
| msdyn_totalactualcost_base             | ne             | ne           |
| msdyn_totalplannedcost                 | ne             | ne           |
| msdyn_totalplannedcost_base            | ne             | ne           |


## <a name="limitations-and-known-issues"></a>Apribojimai ir žinomos problemos
Toliau pateikiamas apribojimų ir žinomų problemų sąrašas.

- Projekto grafiko API sąsajas gali naudoti tik **vartotojai, turintys „Microsoft Project“ licenciją**. Jų negali toliau nurodyti vartotojai.
    - Programų vartotojai
    - Sistemos vartotojai
    - Integravimo vartotojai
    - Kiti vartotojai, neturintys reikiamos licencijos
- Kiekviename **OperationSet** gali būti ne daugiau kaip 100 operacijų.
- Kiekvienas vartotojas gali turėti ne daugiau kaip 10 atvirų **OperationSet**.
- „Project Operations“ šiuo metu palaikoma ne daugiau kaip 500 projekto užduočių iš viso.
- **OperationSet** trikties būsena ir trikties žurnalai šiuo metu negalimi.
- [Projektų ir užduočių limitai bei ribos](/project-for-the-web/project-for-the-web-limits-and-boundaries)

## <a name="error-handling"></a>Klaidų apdorojimas

   - Norėdami peržiūrėti iš operacijų rinkinių sugeneruotas klaidas, eikite į **Parametrai** \> **Grafiko integravimas** \> **Operacijų rinkiniai**.
   - Norėdami peržiūrėti klaidas, sugeneruotas projekto grafiko tarnyboje, eikite į **Parametrai** \> **Grafiko integracija** \> **PSS klaidų žurnalai**.

## <a name="sample-scenario"></a>Scenarijaus pavyzdys

Pagal šį scenarijų sukursite projektą, komandos narį, keturias užduotis ir du išteklių priskyrimus. Tada atnaujinsite vieną užduotį, atnaujinsite projektą, panaikinsite vieną užduotį, panaikinsite vieną išteklių priskyrimą ir sukursite užduoties priklausomybę.

```csharp
Entity project = CreateProject();
project.Id = CallCreateProjectAction(project);
var projectReference = project.ToEntityReference();

var teamMember = new Entity("msdyn_projectteam", Guid.NewGuid());
teamMember["msdyn_name"] = $"TM {DateTime.Now.ToShortTimeString()}";
teamMember["msdyn_project"] = projectReference;
var createTeamMemberResponse = CallCreateTeamMemberAction(teamMember);

var description = $"My demo {DateTime.Now.ToShortTimeString()}";
var operationSetId = CallCreateOperationSetAction(project.Id, description);

var task1 = GetTask("1WW", projectReference);
var task2 = GetTask("2XX", projectReference, task1.ToEntityReference());
var task3 = GetTask("3YY", projectReference);
var task4 = GetTask("4ZZ", projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment("R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

var assignment1Response = CallPssCreateAction(assignment1, operationSetId);
var assignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

var assignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Papildomi pavyzdžiai

```csharp
#region Call actions --- Sample code ----

/// <summary>
/// Calls the action to create an operationSet
/// </summary>
/// <param name="projectId">project id for the operations to be included in this operationSet</param>
/// <param name="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
private string CallCreateOperationSetAction(Guid projectId, string description)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_CreateOperationSetV1");
    operationSetRequest["ProjectId"] = projectId.ToString();
    operationSetRequest["Description"] = description;
    OrganizationResponse response = organizationService.Execute(operationSetRequest);
    return response["OperationSetId"].ToString();
}

/// <summary>
/// Calls the action to create an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>

private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <param name="entity">Task or Resource Assignment</param>
/// <param name="operationSetId">operationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssUpdateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssUpdateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to update an entity, only Task and Resource Assignment for now
/// </summary>
/// <param name="recordId">Id of the record to be deleted</param>
/// <param name="entityLogicalName">Entity logical name of the record</param>
/// <param name="operationSetId">OperationSet Id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssDeleteAction(string recordId, string entityLogicalName, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssDeleteV1");
    operationSetRequest["RecordId"] = recordId;
    operationSetRequest["EntityLogicalName"] = entityLogicalName;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// Calls the action to execute requests in an operationSet
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallExecuteOperationSetAction(string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_ExecuteOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary>
/// This can be used to abandon an operationSet that is no longer needed
/// </summary>
/// <param name="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
protected OperationSetResponse CallAbandonOperationSetAction(Guid operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_AbandonOperationSetV1");
    operationSetRequest["OperationSetId"] = operationSetId.ToString();
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}


/// <summary>
/// Calls the action to create a new project
/// </summary>
/// <param name="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1");
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);
    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <param name="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
private string CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject<OperationSetResponse>((string)orgResponse.Results["OperationSetResponse"]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet("msdyn_project", "msdyn_name");
    var getDefaultBucket = new QueryExpression("msdyn_projectbucket")
    {
        ColumnSet = columnsToFetch,
        Criteria =
        {
            Conditions =
            {
                new ConditionExpression("msdyn_project", ConditionOperator.Equal, projectReference.Id),
                new ConditionExpression("msdyn_name", ConditionOperator.Equal, "Bucket 1")
            }
        }
    };

    return organizationService.RetrieveMultiple(getDefaultBucket);
}

private Entity GetBucket(EntityReference projectReference)
{
    var bucketCollection = GetDefaultBucket(projectReference);
    if (bucketCollection.Entities.Count > 0)
    {
        return bucketCollection[0].ToEntity<Entity>();
    }

    throw new Exception($"Please open project with id {projectReference.Id} in the Dynamics UI and navigate to the Tasks tab");
}

private Entity CreateProject()
{
    var project = new Entity("msdyn_project", Guid.NewGuid());
    project["msdyn_subject"] = $"Proj {DateTime.Now.ToShortTimeString()}";

    return project;
}



private Entity GetTask(string name, EntityReference projectReference, EntityReference parentReference = null)
{
    var task = new Entity("msdyn_projecttask", Guid.NewGuid());
    task["msdyn_project"] = projectReference;
    task["msdyn_subject"] = name;
    task["msdyn_effort"] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
    task["new_custom1"] = "Just my test";
    task["new_age"] = 98;
    task["new_amount"] = 591.34m;
    task["new_isready"] = new OptionSetValue(100000000);
    */

    if (parentReference == null)
    {
        task["msdyn_outlinelevel"] = 1;
    }
    else
    {
        task["msdyn_parenttask"] = parentReference;
    }

    return task;
}

private Entity GetResourceAssignment(string name, Entity teamMember, Entity task, Entity project)
{
    var assignment = new Entity("msdyn_resourceassignment", Guid.NewGuid());
    assignment["msdyn_projectteamid"] = teamMember.ToEntityReference();
    assignment["msdyn_taskid"] = task.ToEntityReference();
    assignment["msdyn_projectid"] = project.ToEntityReference();
    assignment["msdyn_name"] = name;
    assignment["msdyn_start"] = DateTime.Now;
    assignment["msdyn_finish"] = DateTime.Now;

    return assignment;
}

protected Entity GetTaskDependency(Entity project, Entity predecessor, Entity successor)
{
    var taskDependency = new Entity("msdyn_projecttaskdependency", Guid.NewGuid());
    taskDependency["msdyn_project"] = project.ToEntityReference();
    taskDependency["msdyn_predecessortask"] = predecessor.ToEntityReference();
    taskDependency["msdyn_successortask"] = successor.ToEntityReference();
    taskDependency["msdyn_linktype"] = new OptionSetValue(192350000);

    return taskDependency;
}

#endregion


#region OperationSetResponse DataContract --- Sample code ----

[DataContract]
public class OperationSetResponse
{
[DataMember(Name = "operationSetId")]
public Guid OperationSetId { get; set; }

[DataMember(Name = "operationSetDetailId")]
public Guid OperationSetDetailId { get; set; }

[DataMember(Name = "operationType")]
public string OperationType { get; set; }

[DataMember(Name = "recordId")]
public string RecordId { get; set; }

[DataMember(Name = "correlationId")]
public string CorrelationId { get; set; }
}

#endregion
```
