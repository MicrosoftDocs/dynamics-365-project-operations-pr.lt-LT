---
title: Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti
description: Šiame straipsnyje pateikiama informacija apie projekto grafiko API sąsajų naudojimą ir jo pavyzdžiai.
author: sigitac
ms.date: 01/13/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 159d395efff98f2af780e5ed1e5ab3d6483cba89
ms.sourcegitcommit: b1c26ea57be721c5b0b1a33f2de0380ad102648f
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/20/2022
ms.locfileid: "9541135"
---
# <a name="use-project-schedule-apis-to-perform-operations-with-scheduling-entities"></a>Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_


**Grafiko objektai**

Projekto grafiko API sąsajos suteikia galimybę atlikti kūrimo, naujinimo ir naikinimo operacijas su **planavimo objektais**. Šie objektai valdomi naudojant „Project for the Web“ planavimo variklį. Ankstesniuose „Dynamics 365 Project Operations“ leidimuose operacijų kūrimas, naujinimas ir naikinimas naudojant **planavimo objektus** buvo apribotas.

Toliau esančioje lentelėje pateikiamas visas projekto grafiko objektų sąrašas.

| **Objekto pavadinimas**         | **Loginis objekto pavadinimas**     |
|-------------------------|-----------------------------|
| Project                 | msdyn_project               |
| Projekto užduotis            | msdyn_projecttask           |
| Projekto užduoties priklausomybė | msdyn_projecttaskdependency |
| Išteklių priskyrimas     | msdyn_resourceassignment    |
| Projekto talpykla          | msdyn_projectbucket         |
| Projekto komandos narys     | msdyn_projectteam           |
| Projekto kontroliniai sąrašai      | msdyn_projectchecklist      |
| Projekto žyma           | msdyn_projectlabel          |
| Projekto užduotis, skirta žymėti   | msdyn_projecttasktolabel    |
| Projekto sprintas          | msdyn_projectsprint         |

**OperationSet**

OperationSet yra darbo vieneto modelis, kurį galima naudoti, kai operacijoje reikia apdoroti keletą grafikui poveikį darančių užklausų.

**Projekto grafiko API sąsajos**

Toliau pateikiamas dabartinių projekto grafiko API sąrašas.

| **API**                                 | Aprašą                                                                                                                       |
|-----------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------|
| **msdyn_CreateProjectV1**               | Šis API yra naudojamas sukurti projektą. Projektas ir numatytoji projekto talpykla yra sukuriami nedelsiant.                         |
| **msdyn_CreateTeamMemberV1**            | Šis API yra naudojamas sukurti projekto komandos narį. Komandos nario įrašas sukuriamas nedelsiant.                                  |
| **msdyn_CreateOperationSetV1**          | Šį API galima naudoti norint suplanuoti keletą užklausų, kurias reikia atlikti operacijoje.                                        |
| **msdyn_PssCreateV1**                   | Šis API yra naudojamas sukurti objektą. Toks objektas gali būti bet kuris projekto planavimo objektas, kuris palaiko kūrimo operaciją. |
| **msdyn_PssUpdateV1**                   | Šis API yra naudojamas atnaujinti objektą. Toks objektas gali būti bet kuris projekto planavimo objektas, kuris palaiko naujinimo operaciją  |
| **msdyn_PssDeleteV1**                   | Šis API yra naudojamas panaikinti objektą. Toks objektas gali būti bet kuris projekto planavimo objektas, kuris palaiko naikinimo operaciją. |
| **msdyn_ExecuteOperationSetV1**         | Šis API naudojamas norint vykdyti visas nurodyto operacijų rinkinio operacijas.                                                 |
| **msdyn_PssUpdateResourceAssignmentV1** | Šis API naudojamas išteklių priskyrimo suplanuoto darbo susiejinimui naujinti.                                                        |



**Projekto grafiko API sąsajų naudojimas su OperationSet**

Kadangi įrašai, naudojant **CreateProjectV1** ir **CreateTeamMemberV1**, sukuriami nedelsiant, šių API negalima naudoti tiesiai **OperationSet**. Tačiau API galite naudoti norėdami sukurti reikiamus įrašus, **OperationSet**, tada šiuos iš anksto sukurtus įrašus panaudoti **OperationSet**.

**Palaikomos operacijos**

| **Grafiko objektas**   | **Kūrimas** | **Atnaujinimas** | **Naikinti** | **Svarbi informacija**                                                                                                                                                                                                                                                                                                                            |
|-------------------------|------------|------------|------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Projekto užduotis            | Taip        | Taip        | Taip        | Laukus **Eiga**, **Pastangos įdėtos** ir **Pastangos** galima redaguoti „Project for the Web", tačiau jų negalima redaguoti „Project Operations“.                                                                                                                                                                                             |
| Projekto užduoties priklausomybė | Taip        | No         | Taip        | Projekto užduoties priklausomybės įrašai neatnaujinami. Vietoj to, seną įrašą galima panaikinti ir sukurti naują.                                                                                                                                                                                                                                 |
| Išteklių priskyrimas     | Taip        | Taip\*      | Taip        | Nepalaikomos operacijos, kurioms naudojami šie laukai: **BookableResourceID**, **Pastangos**, **EffortCompleted**, **EffortRemaining** ir **PlannedWork**. Išteklių priskyrimo įrašai neatnaujinami. Vietoj to, seną įrašą galima panaikinti ir sukurti naują. Siekiant atnaujinti išteklių priskyrimo kontūrus, buvo pateikta atskira API. |
| Projekto talpykla          | Taip        | Taip        | Taip        | Numatytoji talpykla sukuriama naudojant **CreateProjectV1** API. Projektų naikinimo ir kūrimo palaikymas buvo įtrauktas į 16 naujinimo leidimą.                                                                                                                                                                                                   |
| Projekto komandos narys     | Taip        | Taip        | Taip        | Kūrimo operacijai naudokite **CreateTeamMemberV1** API.                                                                                                                                                                                                                                                                                           |
| Project                 | Taip        | Taip        |            | Nepalaikomos operacijos, kurioms naudojami šie laukai: **StateCode**, **BulkGenerationStatus**, **GlobalRevisionToken**, **CalendarID**, **Pastangos**, **EffortCompleted**, **EffortRemaining**, **Eiga**, **Pabaiga**, **TaskEarliestStart** ir **Duration**.                                                                                       |
| Projekto kontroliniai sąrašai      | Taip        | Taip        | Taip        |                                                                                                                                                                                                                                                                                                                                                         |
| Projekto žyma           | No         | Taip        | No         | Žymų pavadinimus galima keisti. Ši funkcija pasiekiama tik „Project for the Web“                                                                                                                                                                                                                                                                      |
| Projekto užduotis, skirta žymėti   | Taip        | No         | Taip        | Ši funkcija pasiekiama tik „Project for the Web“                                                                                                                                                                                                                                                                                                  |
| Projekto sprintas          | Taip        | Taip        | Taip        | Lauko **Pradžia** data turi būti ankstesnė nei **Pabaigos** laukelyje. To paties projekto vykdymas vienas su kitu nepersidengia. Ši funkcija pasiekiama tik „Project for the Web“                                                                                                                                                                    |




ID ypatybė yra pasirinktinė. Jei ji pateikta, sistema bando ypatybę panaudoti ir, jei to padaryti negalima, pateikia išimtį. Jei ypatybė nepateikta, sistema ją sugeneruos.

**Apribojimai ir žinomos problemos**

Toliau pateikiamas apribojimų ir žinomų problemų sąrašas.

-   Projekto grafiko API sąsajas gali naudoti tik **Vartotojai, turintys „Microsoft Project“ licenciją**. Jų negali toliau nurodyti vartotojai.
    -   Programų vartotojai
    -   Sistemos vartotojai
    -   Integravimo vartotojai
    -   Kiti vartotojai, neturintys reikiamos licencijos
-   Kiekviename **OperationSet** gali būti ne daugiau kaip 100 operacijų.
-   Kiekvienas vartotojas gali turėti ne daugiau kaip 10 atvirų **OperationSet**.
-   „Project Operations“ šiuo metu palaikoma ne daugiau kaip 500 projekto užduočių iš viso.
-   Kiekviena išteklių priskyrimo naujinimo operacija apskaičiuojama kaip viena operacija.
-   Kiekviename atnaujintų kontūrų sąraše gali būti ne daugiau kaip 100 laiko pjūvių.
-   **OperationSet** trikties būsena ir trikties žurnalai šiuo metu negalimi.
-   Vienam projektui įgyvendinti galimi ne daugiau kaip 400 spustelėjimų.
-   [Projektų ir užduočių limitai bei ribos](/project-for-the-web/project-for-the-web-limits-and-boundaries).
-   Žymos kol kas pasiekiamos tik „Project for the Web“.

**Klaidų apdorojimas**

-   Norėdami peržiūrėti iš operacijų rinkinių sugeneruotas klaidas, eikite į **Parametrai** \> **Grafiko integravimas** \> **Operacijų rinkiniai**.
-   Norėdami peržiūrėti klaidas, sugeneruotas projekto grafiko tarnyboje, eikite į **Parametrai** \> **Grafiko integracija** \> **PSS klaidų žurnalai**.

**Išteklių priskyrimo kontūrų redagavimas**

Skirtingai nei visos kitos projekto planavimo API, atnaujinančios objektą, išteklių priskyrimo API yra visiškai atsakinga už vieno lauko msdyn_plannedwork, t. y. vieno objekto, msydn_resourceassignment.

Nurodytas grafiko režimas yra:

-   **fiksuoti vienetai**
-   projekto kalendorius yra 9-5p yra 9-5pst, pirmadienis, antradienis, ketvirtadienis, penktadienis (TREČIADIENIAIS NEDIRBAMA)
-   Ir išteklių kalendorius yra 9-1p PST nuno pirmadienio iki penktadienio

Šis priskyrimas skirtas savaitei, keturioms valandoms per dieną. Taip yra todėl, kad išteklių kalendorius yra iš 9-1 PST arba keturių valandų per dieną.

| &nbsp;     | Užduotis | Pradžios data | Pabaigos data  | Kiekis | 2022-06-13 | 2022-06-14 | 2022-06-15 | 2022-06-16 | 2022-06-17 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9–1 darbuotojai |  T1  | 2022-06-13  | 2022-06-17 | 20       | 4         | 4         | 4         | 4         | 4         |

Pavyzdžiui, jei norite, kad darbuotojas dirbtų tik tris valandas kiekvieną šios savaitės dieną ir leisti vieną valandą atlikti kitas užduotis.

#### <a name="updatedcontours-sample-payload"></a>UpdatedContours apkrovos pavyzdys:

```json
[{

"minutes":900.0,

"start":"2022-06-13T00:00:00-07:00",

"end":"2022-06-18T00:00:00-07:00"

}]
```

Tai yra priskyrimas paleidus grafiko API kontūro naujinimą.

| &nbsp;     | Užduotis | Pradžios data | Pabaigos data  | Kiekis | 2022-06-13 | 2022-06-14 | 2022-06-15 | 2022-06-16 | 2022-06-17 |
|------------|------|------------|-----------|----------|-----------|-----------|-----------|-----------|-----------|
| 9–1 darbuotojai | T1   | 2022-06-13  | 2022-06-17 | 15       | 3         | 3         | 3         | 3         | 3         |


**Scenarijaus pavyzdys**

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

** Papildomi pavyzdžiai

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
