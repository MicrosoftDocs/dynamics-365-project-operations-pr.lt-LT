---
title: Projekto grafiko API naudojimas su „Power Automate“
description: Šiame straipsnyje pateikiamas pavyzdinis srautas, kuriame naudojamos projekto tvarkaraščio programų programavimo sąsajos (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916344"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projekto grafiko API naudojimas su „Power Automate“

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šiame straipsnyje aprašomas srauto pavyzdys, rodantis, kaip sukurti visą projekto planą naudojant Microsoft Power Automate, kaip sukurti operacijų rinkinį ir kaip atnaujinti objektą. Pavyzdyje parodyta, kaip sukurti projektą, projekto komandos narį, operacijų rinkinius, projekto užduotis ir išteklių priskyrimus. Šiame straipsnyje taip pat paaiškinama, kaip atnaujinti objektą ir vykdyti operacijų rinkinį.

Toliau pateikiamas išsamus veiksmų, kurie yra dokumentuoti šio straipsnio imties sraute, sąrašas:

1. [Trigerio PowerApps kūrimas](#1)
2. [Projekto kūrimas](#2)
3. [Inicijuoti komandos nario kintamąjį](#3)
4. [Bendrojo komandos nario kūrimas](#4)
5. [Operacijų rinkinio kūrimas](#5)
6. [Kurti projekto kibirą](#6)
7. [Inicijuoti saito būsenos kintamąjį](#7)
8. [Inicijuoti užduočių skaičiaus kintamąjį](#8)
9. [Inicijuoti projekto užduoties ID kintamąjį](#9)
10. [Darykite iki](#10)
11. [Projekto užduoties nustatymas](#11)
12. [Kurti projekto užduotį](#12)
13. [Išteklių priskyrimo kūrimas](#13)
14. [Kintamojo dekantavimas](#14)
15. [Projekto užduoties pervardijimas](#15)
16. [Operacijų rinkinio vykdymas](#16)

## <a name="assumptions"></a>Prielaidos

Šiame straipsnyje daroma prielaida, kad turite pagrindinių žinių apie platformą Dataverse, debesies srautus ir projekto tvarkaraščio programų programavimo sąsają (API). Daugiau informacijos rasite [šio straipsnio skyriuje Nuorodos](#references).

## <a name="create-a-flow"></a>Kurti srautą

### <a name="select-an-environment"></a>Pasirinkite aplinką

Galite sukurti srautą Power Automate savo aplinkoje.

1. Eikite į <https://flow.microsoft.com>, ir naudokite administratoriaus kredencialus, kad prisijungtumėte.
2. Viršutiniame dešiniajame kampe pasirinkite **Aplinkos**.
3. Sąraše pasirinkite aplinką, kurioje Dynamics 365 Project Operations įdiegta.

### <a name="create-a-solution"></a>Sprendimo kūrimas

Atlikite šiuos veiksmus, kad sukurtumėte [sprendimą suprantantį srautą](/power-automate/overview-solution-flows). Sukurdami sprendimą suprantantį srautą, galite lengviau eksportuoti srautą, kad galėtumėte jį naudoti vėliau.

1. Naršymo srityje pasirinkite **Sprendimai**.
2. **Puslapyje Sprendimai** pasirinkite **Naujas sprendimas**.
3. Dialogo **lange Naujas sprendimas** nustatykite reikiamus laukus, tada pasirinkite **Kurti**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1 veiksmas: paleidiklio kūrimas PowerApps

1. **Puslapyje Sprendimai** pasirinkite sukurtą sprendimą, tada pasirinkite **Naujas**.
2. Kairiojoje srityje pasirinkite **Debesies srautai** \> **Automation** \> **Cloud flow** \> **Instant.**
3. Lauke **Srauto pavadinimas** įveskite **Planuoti API demonstracinį srautą**.
4. **Dalyje Pasirinkti, kaip suaktyvinti šį srautą**, pasirinkite **Power Apps**. Kai sukuriate trigerį Power Apps, logika priklauso nuo jūsų, kaip autoriaus. Šiame straipsnyje palikite įvesties parametrus tuščius bandymų tikslais.
5. Pasirinkite **Kurti**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2 veiksmas. Sukurkite projektą

Norėdami sukurti pavyzdinį projektą, atlikite šiuos veiksmus.

1. Sukurtame sraute pasirinkite **Naujas veiksmas**.

    ![Pridėkite naują žingsnį.](media/newstep.png)

2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietą veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.

    ![Operacijos pasirinkimas.](media/chooseactiontab.png)

3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.

![Žingsnio pervadinimas.](media/renamestep.png)

4. Pervardykite veiksmą **Kurti projektą**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ CreateProjectV1**.
6. Msdyn **temos\_ lauke pasirinkite** Įtraukti dinaminį **turinį**.
7. Skirtuko **Išraiška** funkcijos lauke įveskite **Projekto pavadinimas - utcNow()**.
8. Pasirinkite **Gerai**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3 veiksmas: inicijuoti komandos nario kintamąjį

1. Sraute pasirinkite **Naujas veiksmas**.
2. **Dialogo lango Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **"Init" komandos narys**.
5. Lauke **Pavadinimas įveskite** TeamMemberAction **·**.
6. Lauke **Tipas** pasirinkite **Eilutė**.
7. Lauke **Vertė įveskite** msdyn **CreateTeamMemberV1\_**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4 veiksmas: bendrinio komandos nario kūrimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietą veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti komandos narį**.
5. Lauke Veiksmo **pavadinimas** dialogo lange Dinaminis turinys **pasirinkite** **TeamMemberAction**.
6. Lauke **Veiksmų parametrai** įveskite šią parametro informaciją.

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    Čia pateikiamas parametrų paaiškinimas:

    - **\@\@ odata.type** – objekto pavadinimas. Pavyzdžiui, įveskite **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – pagrindinis projekto komandos ID raktas. Reikšmė yra visame pasaulyje unikali identifikatoriaus (GUID) išraiška.   ID generuojamas iš išraiškos skirtuko.

    - **msdyn\_ projektas\@ odata.bind** – Projekto ID nuosavo projekto ID. Vertė bus dinamiškas turinys, gaunamas reaguojant į veiksmą "Kurti projektą". Įsitikinkite, kad įvedėte visą kelią ir tarp skliaustų pridėkite dinaminį turinį. Reikalingos kabutės. Pavyzdžiui, įveskite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **Msdyn\_ vardas** – komandos nario vardas ir pavardė. Pavyzdžiui, įveskite **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5 veiksmas: operacijų rinkinio kūrimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietą veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti operacijų rinkinį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite pasirinktinį veiksmą **msdyn\_ CreateOperationSetV1** Dataverse.
6. Lauke **Aprašas** įveskite **ScheduleAPIDemoOperationSet**.
7. Lauke **Projektas įveskite**/msdyn **projektai(\_**.
8. **Dialogo lange Dinaminis turinys** pasirinkite **msdyn\_ CreateProjectV1Response ProjectId**.
9. Lauke **Projektas** įveskite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6 veiksmas: sukurkite projekto kibirą

1. Sraute pasirinkite **Naujas veiksmas**.
2. **Dialogo lango Pasirinkti operaciją** ieškos lauke įveskite **įtraukti naują eilutę**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti kibirą**.
5. Lauke **Lentelės pavadinimas** pasirinkite **Projekto kibirai**.
6. Lauke **Pavadinimas** įveskite **ScheduleAPIDemoBucket1**.
7. **Lauke Projektas** dialogo lange Dinaminis turinys **pasirinkite \_ msdyn** CreateProjectV1Response **ProjectId**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7 veiksmas: inicijuoti saito būsenos kintamąjį

1. Sraute pasirinkite **Naujas veiksmas**.
2. **Dialogo lango Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Init linkstatus**.
5. Lauke **Pavadinimas įveskite** linkstatus **·**.
6. Lauke **Tipas pasirinkite** Sveikasis **skaičius**.
7. Lauke **Vertė** įveskite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8 veiksmas: užduočių skaičiaus kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. **Dialogo lango Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Užduočių skaičius**.
5. Lauke **Pavadinimas** įveskite **užduočių** skaičių.
6. Lauke **Tipas pasirinkite** Sveikasis **skaičius**.
7. Lauke **Vertė** įveskite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9 veiksmas: inicijuoti projekto užduoties ID kintamąjį

1. Sraute pasirinkite **Naujas veiksmas**.
2. **Dialogo lango Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Init ProjectTaskID**.
5. Lauke **Pavadinimas** įveskite **užduočių** skaičių.
6. Lauke **Tipas** pasirinkite **Eilutė**.
7. **Lauke Vertė** išraiškos daryklėje įveskite **guid()**.

## <a name="step-10-do-until"></a><a id="10"></a> 10 žingsnis: darykite iki

1. Sraute pasirinkite **Naujas veiksmas**.
2. **Dialogo lango Pasirinkti operaciją** ieškos lauke įveskite **Daryti iki**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Nustatykite pirmąją sąlyginio išrašo reikšmę į **užduočių** skaičių, kintamą **iš dialogo lango Dinaminis turinys**.
4. Nustatykite sąlygą į **mažesnę nei lygią**.
5. Nustatykite antrąją sąlyginio išrašo reikšmę į **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11 veiksmas: nustatykite projekto užduotį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **nustatytą kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Naujame žingsnyje pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Nustatyti projekto užduotį**.
5. Lauke **Pavadinimas pasirinkite** Msdyn **projecttaskid\_**.
6. **Lauke Vertė** išraiškos daryklėje įveskite **guid()**.

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12 veiksmas: projekto užduoties kūrimas

Atlikite šiuos veiksmus, kad sukurtumėte projekto užduotį, turinčią unikalų ID, priklausantį dabartiniam projektui ir jūsų sukurtam projekto kibirui.

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietą veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti projekto užduotį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ PssCreateV1**.
6. Lauke **Objektas** įveskite šią parametro informaciją.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    Čia pateikiamas parametrų paaiškinimas:

    - **\@\@ odata.type** – objekto pavadinimas. Pavyzdžiui, įveskite **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – unikalus užduoties ID. Reikšmė turėtų būti nustatyta kaip dinaminis kintamasis iš **msdyn\_ projecttaskid**.
    - **msdyn\_ projektas\@ odata.bind** – Projekto ID nuosavo projekto ID. Vertė bus dinamiškas turinys, gaunamas reaguojant į veiksmą "Kurti projektą". Įsitikinkite, kad įvedėte visą kelią ir tarp skliaustų pridėkite dinaminį turinį. Reikalingos kabutės. Pavyzdžiui, įveskite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ tema** – bet koks užduoties pavadinimas.
    - **msdyn\_ projectbucket\@ odata.bind** – projekto kibiras, kuriame yra užduotys. Reikšmė bus dinamiškas turinys, gaunamas iš veiksmo "Sukurti kibirą" atsakymo. Įsitikinkite, kad įvedėte visą kelią ir tarp skliaustų pridėkite dinaminį turinį. Reikalingos kabutės. Pavyzdžiui, įveskite **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ pradžia** – dinaminis pradžios datos turinys. Pavyzdžiui, rytoj bus atstovaujama kaip **"addDays(utcNow(), 1)"**.
    - **msdyn\_ suplanuotas startas** – suplanuota pradžios data. Pavyzdžiui, rytoj bus atstovaujama kaip **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – suplanuota pabaigos data. Pasirinkite datą ateityje. Pavyzdžiui, nurodykite **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – saito būsena. Pavyzdžiui, įveskite **"192350000"**.

7. **Lauke OperationSetId** dialogo lange Dinaminis turinys **pasirinkite \_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13 veiksmas: išteklių priskyrimo kūrimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietą veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti priskyrimą**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ PssCreateV1**.
6. Lauke **Objektas** įveskite šią parametro informaciją.

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. **Lauke OperationSetId** dialogo lange Dinaminis turinys **pasirinkite \_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14 veiksmas: kintamojo dekantavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. **Dialogo lango Pasirinkti operaciją** ieškos lauke įveskite **decrement kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Lauke **Pavadinimas** pasirinkite **užduočių** skaičių.
4. Lauke **Vertė** įveskite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15 veiksmas: projekto užduoties pervardijimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietą veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Pervardyti projekto užduotį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ PssUpdateV1**.
6. Lauke **Objektas** įveskite šią parametro informaciją.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. **Lauke OperationSetId** dialogo lange Dinaminis turinys **pasirinkite \_ msdyn** CreateOperationSetV1Response **·**.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16 veiksmas: paleiskite operacijų rinkinį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo **lango Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietą veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Vykdyti operacijų rinkinį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ ExecuteOperationSetV1**.
6. **Lauke OperationSetId** dialogo lange Dynamid turinys **pasirinkite \_ msdyn** CreateOperationSetV1Response **OperationSetId**.

## <a name="references"></a>Nuorodos

- [Apžvalga, kaip integruoti srautus su Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti](schedule-api-preview.md)
- [Debesų srautų apžvalga - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Sprendimų srautų apžvalga - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
