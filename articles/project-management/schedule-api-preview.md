---
title: Grafiko API naudojimas norint atlikti operacijas su grafiko objektais
description: Šioje temoje pateikiama informacija ir pavyzdžiai, kaip naudoti grafiko API.
author: sigitac
manager: Annbe
ms.date: 04/07/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: a50a2c6220bb49de8146d0758019827e120e0526
ms.sourcegitcommit: 8ff9fe396db6dec581c21cd6bb9acc2691c815b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 04/07/2021
ms.locfileid: "5868139"
---
# <a name="use-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Grafiko API naudojimas norint atlikti operacijas su grafiko objektais

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

> [!IMPORTANT] 
> Kai kurios arba visos šioje temoje paminėtos funkcijos pasiekiamos kaip peržiūros versijos leidimo dalis. Turinys ir funkcijos gali keistis. 

## <a name="scheduling-entities"></a>Grafiko objektai

Grafiko API suteikia galimybę atlikti kūrimo, naujinimo ir naikinimo operacijas naudojant **grafiko objektus**. Šie objektai valdomi naudojant „Project for the Web“ planavimo variklį. Ankstesniuose „Dynamics 365 Project Operations“ leidimuose operacijų kūrimas, naujinimas ir naikinimas naudojant **planavimo objektus** buvo apribotas.

Toliau esančioje lentelėje pateikiamas visas **planavimo objektų** sąrašas.

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

## <a name="schedule-apis"></a>Grafiko API

Toliau pateikiamas dabartinių grafiko API sąrašas.

- **msdyn_CreateProjectV1**: šį API galima naudoti norint sukurti projektą. Projektas ir numatytoji projekto talpykla sukuriami nedelsiant.
- **msdyn_CreateTeamMemberV1**:šį API galima naudoti norint sukurti projekto komandos narį. Komandos nario įrašas sukuriamas nedelsiant.
- **msdyn_CreateOperationSetV1**: šį API galima naudoti norint suplanuoti keletą užklausų, kurias reikia atlikti operacijoje.
- **msdyn_PSSCreateV1**: šį API galima naudoti norint sukurti objektą. Objektu gali būti bet kuris iš planavimo objektų, palaikančių kūrimo operaciją.
- **msdyn_PSSUpdateV1**: šį API galima naudoti norint atnaujinti objektą. Objektu gali būti bet kuris iš planavimo objektų, palaikančių naujinimo operaciją.
- **msdyn_PSSDeleteV1**: šį API galima naudoti norint panaikinti objektą. Objektu gali būti bet kuris iš planavimo objektų, palaikančių naikinimo operaciją.
- **msdyn_ExecuteOperationSetV1**: šis API naudojamas norint vykdyti visas nurodyto operacijų rinkinio operacijas.

## <a name="using-schedule-apis-with-operationset"></a>Grafiko API naudojimas kartu su OperationSet

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

## <a name="limitations-and-known-issues"></a>Apribojimai ir žinomos problemos
Toliau pateikiamas apribojimų ir žinomų problemų sąrašas.

- Grafiko API gali naudoti tik **vartotojai, turintys „Microsoft Project“ licenciją.** Jų negali toliau nurodyti vartotojai.
    - Programų vartotojai
    - Sistemos vartotojai
    - Integravimo vartotojai
    - Kiti vartotojai, neturintys reikiamos licencijos
- Kiekviename **OperationSet** gali būti ne daugiau kaip 100 operacijų.
- Kiekvienas vartotojas gali turėti ne daugiau kaip 10 atvirų **OperationSet**.
- „Project Operations“ šiuo metu palaikoma ne daugiau kaip 500 projekto užduočių iš viso.
- **OperationSet** trikties būsena ir trikties žurnalai šiuo metu negalimi.
- Grafiko API yra viešosios priežiūros versijos. „Microsoft“ nepalaiko šių API naudojimo gamybos aplinkoje.

## <a name="sample-scenario"></a>Scenarijaus pavyzdys

Pagal šį scenarijų sukursite projektą, komandos narį, keturias užduotis ir du išteklių priskyrimus. Tada atnaujinsite vieną užduotį, atnaujinsite projektą, panaikinsite vieną užduotį, panaikinsite vieną išteklių priskyrimą ir sukursite užduoties priklausomybę.

```C#
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
var task4 = GetTask("4ZZ";, projectReference);

var assignment1 = GetResourceAssignment("R1", teamMember, task2, project);
var assignment2 = GetResourceAssignment"R2", teamMember, task3, project);

var task1Response = CallPssCreateAction(task1, operationSetId);
var task2Response = CallPssCreateAction(task2, operationSetId);
var task3Response = CallPssCreateAction(task3, operationSetId);
var task4Response = CallPssCreateAction(task4, operationSetId);

varassignment1Response = CallPssCreateAction(assignment1, operationSetId);
varassignment2Response = CallPssCreateAction(assignment2, operationSetId);

task2["msdyn_subject"] = "Updated Task";
var task2UpdateResponse = CallPssUpdateAction(task2, operationSetId);

project["msdyn_subject"] = $"Proj update {DateTime.Now.ToShortTimeString()}";
var projectUpdateResponse = CallPssUpdateAction(project, operationSetId);

var task4DeleteResponse = CallPssDeleteAction(task4.Id.ToString(), task4.LogicalName, operationSetId);

varassignment2DeleteResponse = CallPssDeleteAction(assignment2.Id.ToString(), assignment2.LogicalName, operationSetId);

var dependency1 = GetTaskDependency(project, task2, task3);
var dependency1Response = CallPssCreateAction(dependency1, operationSetId);

CallExecuteOperationSetAction(operationSetId);
Console.WriteLine("Done....");
```

## <a name="additional-samples"></a>Papildomi pavyzdžiai

```C#
#region Call actions 

///<summary>
/// Calls the action to create an operationSet
/// </summary>
/// <paramname="projectId">project id for the operations to be included in this operationSet>/param>
/// <paramname="description">description of this operationSet</param>
/// <returns>operationSet id</returns>
privatestring CallCreateOperationSetAction(Guid projectId, string description)
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
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet id</param>
/// <returns>OperationSetResponse</returns>
private OperationSetResponse CallPssCreateAction(Entity entity, string operationSetId)
{
    OrganizationRequest operationSetRequest = new OrganizationRequest("msdyn_PssCreateV1");
    operationSetRequest["Entity"] = entity;
    operationSetRequest["OperationSetId"] = operationSetId;
    return GetOperationSetResponseFromOrgResponse(organizationService.Execute(operationSetRequest));
}

/// <summary<
/// Calls the action to update an entity, only Task for now
/// </summary>
/// <paramname="entity">Task or Resource Assignment</param>
/// <paramname="operationSetId">operationSet Id</param>
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
/// <summary>
/// <paramname="recordId">Id of the record to be deleted</param>
/// <paramname="entityLogicalName">Entity logical name of the record</param>
/// <paramname="operationSetId">OperationSet Id</param>
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
/// <summary>
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="operationSetId">operationSet id</param>
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
/// <paramname="project">Project</param>
/// <returns>project Id</returns>
private Guid CallCreateProjectAction(Entity project)
{
    OrganizationRequest createProjectRequest = new OrganizationRequest("msdyn_CreateProjectV1";
    createProjectRequest["Project"] = project;
    OrganizationResponse response = organizationService.Execute(createProjectRequest);
    var projectId = Guid.Parse((string)response["ProjectId"]);

    return projectId;
}

/// <summary>
/// Calls the action to create a new project team member
/// </summary>
/// <paramname="teamMember">Project team member</param>
/// <returns>project team member Id</returns>
privatestring CallCreateTeamMemberAction(Entity teamMember)
{
    OrganizationRequest request = new OrganizationRequest("msdyn_CreateTeamMemberV1");
    request["TeamMember"] = teamMember;
    OrganizationResponse response = organizationService.Execute(request);
    return (string)response["TeamMemberId"];
}

private OperationSetResponse GetOperationSetResponseFromOrgResponse(OrganizationResponse orgResponse)
{
    return JsonConvert.DeserializeObject><OperationSetResponse>
    ((string)orgResponse.Results["OperationSetResponse";]);
}

private EntityCollection GetDefaultBucket(EntityReference projectReference)
{
    var columnsToFetch = new ColumnSet(";msdyn_project", "msdyn_name");
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
    task["msdyn_effort";] = 4d;
    task["msdyn_scheduledstart"] = DateTime.Today;
    task["msdyn_scheduledend"] = DateTime.Today.AddDays(5);
    task["msdyn_progress"] = 0.34m;
    task["msdyn_start"] = DateTime.Now.AddDays(1);
    task["msdyn_projectbucket"] = GetBucket(projectReference).ToEntityReference();
    task["msdyn_LinkStatus"] = new OptionSetValue(192350000);

    //Custom field handling
    /*
        task["new_custom1"] = "Just my test";
        task[";new_age"] = 98;
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
publicclassOperationSetResponse
{
    [DataMember(Name = "operationSetId")]
    public Guid OperationSetId { get; set; }

    [DataMember(Name = "operationSetDetailId")]
    public Guid OperationSetDetailId { get; set; }

    [DataMember(Name = "operationType")]
    publicstring OperationType { get; set; }

    [DataMember(Name = "recordId")]
    publicstring RecordId { get; set; }

    [DataMember(Name = "correlationId")]
    publicstring CorrelationId { get; set; }
}

#endregion
```
