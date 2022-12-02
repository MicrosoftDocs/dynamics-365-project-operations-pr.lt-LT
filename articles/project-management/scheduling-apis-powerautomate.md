---
title: Projekto grafiko API naudojimas su „Power Automate“
description: Šiame straipsnyje pateikiamas srauto pavyzdys, naudojantis projektų grafiko programų programavimo sąsajas (API).
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: afec082c680596e8dcb8ec0b350b4bb7853c49ff
ms.sourcegitcommit: 7ed8e77a92917f2d242988ca02bd7de9571cce5e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/02/2022
ms.locfileid: "9404460"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>Projekto grafiko API naudojimas su „Power Automate“

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Šiame straipsnyje aprašomas srauto pavyzdys, rodantis, kaip sukurti visą projekto planą naudojant „Microsoft Power Automate“, kaip sukurti operacijų rinkinį ir kaip atnaujinti objektą. Pavyzdys, kuriame aprašoma, kaip kurti projektą, projekto komandos narį, operacijų rinkinius, projekto užduotis ir išteklių priskyrimus. Šiame straipsnyje taip pat paaiškinta, kaip atnaujinti objektą ir vykdyti operacijų rinkinį.

Toliau pateikiamas visas šio straipsnio srauto pavyzdyje nurodytų žingsnių sąrašas:

1. [Kurti „PowerApps“ perjungimą](#1)
2. [Projekto kūrimas](#2)
3. [Komandos nario kintamojo inicijavimas](#3)
4. [Bendrojo komandos nario kūrimas.](#4)
5. [Parinkčių rinkinio kūrimas](#5)
6. [Projekto talpyklos kūrimas](#6)
7. [Saito būsenos kintamojo inicijavimas](#7)
8. [Užduočių skaičiaus kintamojo inicijavimas](#8)
9. [Projekto užduoties ID kintamojo inicijavimas](#9)
10. [Atlikite iki](#10)
11. [Nustatyti projekto užduotį](#11)
12. [Kurti projekto užduotį](#12)
13. [Išteklių priskyrimo kūrimas](#13)
14. [Kintamojo mažėjimas](#14)
15. [Projekto užduoties pervardijimas.](#15)
16. [Parinkčių rinkinio paleidimas](#16)

## <a name="assumptions"></a>Prielaidos

Šiame straipsnyje laikoma, kad turite pagrindinių žinių apie „Dataverse“ platformą, debesies srautus ir projektų planavimo programos programavimo sąsają (API). Daugiau informacijos žr. šio straipsnio skyriuje „[Šaltiniai](#references)“.

## <a name="create-a-flow"></a>Kurti srautą

### <a name="select-an-environment"></a>Pasirinkite aplinką

Galite kurti „Power Automate“ srautą savo aplinkoje.

1. Įeikite <https://flow.microsoft.com> ir prisijunkite naudodami savo administratoriaus kredencialus.
2. Dešiniajame viršutiniame kampe pasirinkite **Aplinkos**.
3. Sąraše pasirinkite aplinką, kurioje įdiegta „Dynamics 365 Project Operations“.

### <a name="create-a-solution"></a>Sprendimo kūrimas

Norėdami sukurti [sprendimų srautą](/power-automate/overview-solution-flows), atlikite šiuos veiksmus. Sukūrę į sprendimų srautą, galite lengviau eksportuoti srautą, kad galėtumėte naudoti vėliau.

1. Naršymo srityje pasirinkite **Sprendimai**.
2. Puslapyje **Sprendimai** pasirinkite **Naujas sprendimas**.
3. Dialogo lange **Naujas sprendimas** nustatykite reikiamus laukus ir pasirinkite **Kurti**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>1 žingsnis: Sukurkite „PowerApps“ perjungimą

1. Puslapyje **Srendimai** pasirinkite sprendimą, kurį sukūrėte ir tada pasirinkite **Naujas**.
2. Kairiojoje srityje pasirinkite **Debesies srautai** \> **Automatizavimas** \> **„Debesies srautas** \> **Tiesioginiai pranešimai**.
3. Lauke **Srauto pavadinimas** įveskite **Grafiko API demonstracinis srautas**.
4. Sąraše **Pasirinkite, kaip paleisti šį srautą**, pažymėkite **Power Apps**. Kai sukuriate paleidiklį „Power Apps“, logiką sudarote jūs, kaip autorius. Šiame straipsnyje įvesties parametrus palikite tuščius bandymams.
5. Pasirinkite **Kurti**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2 veiksmas. Sukurkite projektą

Norėdami sukurti projekto pavyzdį, atlikite šiuos veiksmus.

1. Sukurtame sraute pasirinkite **Naujas žingsnis**.

    ![Naujo veiksmo įtraukimas.](media/newstep.png)

2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusiejamąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.

    ![Pasirinkite operaciją.](media/chooseactiontab.png)

3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.

![Veiksmo pervadijimas.](media/renamestep.png)

4. Pervardykite veiksmą **Kurti projektą**.
5. Lauke **Veiksmo pavadinimas** pasirinkite **msdyn\_CreateProjectV1**.
6. Laukui **msdyn\_subject** pasirinkite **Įtraukti dinaminį turinį**.
7. Skirtuko **Išraiška** funkcijų lauke įveskite **Projekto pavadinimas – utcNow()**.
8. Pasirinkite **Gerai**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>3 veiksmas: Komandos nario kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Init komandos narys**.
5. Lauke **Pavadinimas** įveskite **KomandosNarioVeiksmas**.
6. Lauke **Tipas** pasirinkite **Eilutė**.
7. Lauke **Value** įveskite **msdyn\_CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>4 veiksmas: sukurkite bendrąjį komandos narį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusiejamąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti komandos narį**.
5. Lauke **Veiksmo pavadinimas** pasirinkite **KomandosNarioVeiksmas** **Dinaminio turinio** dialogo lauke.
6. Lauke **Veiksmo parametrai** įveskite toliau nurodytą parametrų informaciją.

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

    Toliau pateiktas parametrų paaiškinimas:

    - **\@\@odata.type** – objekto pavadinimas. Pavyzdžiui, įveskite **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**.
    - **msdyn\_projectteamid** – pirminis projekto komandos nario ID raktas. Reikšmė yra visuotinio unikalaus identifikatoriaus (GUID) išraiška.   ID generuojamas iš išraiškos skirtuko.

    - **msdyn\_project\@odata.bind** – projektui priklausančio projekto ID. Reikšmė bus dinaminis turinys, gaunamas iš veiksmo „Kurti projektą" atsako. Įsitikinkite, kad įvedate visą kelią ir įtraukiate dinaminį turinį tarp skliaustelių. Kabutės yra būtinos. Pavyzdžiui, įveskite " **/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_name** – komandos nario pavadinimas. Pavyzdžiui, įveskite **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>5 veiksmas: sukurkite operacijų rinkinį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusiejamąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti operacijų rinkinį**.
5. Lauke **Veiksmo pavadinimas** pažymėkite pasirinktinį **msdyn\_CreateOperationSetV1** Dataverse veiksmą.
6. Lauke **Aprašas** įveskite **ScheduleAPIDemoOperationSet**.
7. Lauke **Projektas** įveskite **/msdyn\_projects(**.
8. **Dinaminio turinio** dialogo lauke, pasirinkite **msdyn\_CreateProjectV1Response ProjectId**.
9. **Projekto** lauke, įveskite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>6 veiksmas. Sukurkite projekto talpyklą

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lange **Pasirinkti operaciją** ieškos lauke įveskite **pridėti naują eilutę**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti talpyklą**.
5. Lauke **Lentelės pavadinimas** pasirinkite **Projekto talpyklos**.
6. Lauke **Pavadinimas** įveskite **ScheduleAPIDemoBucket1**.
7. Lauke **Projektas** pasirinkite **msdyn\_CreateProjectV1Response ProjectId** **Dinaminio turinio** dialogo lauke.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>7 veiksmas: Saito būsenos kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Init linkstatus**.
5. Lauke **Pavadinimas** įveskite **linkstatus**.
6. Lauke **Tipas** pasirinkite **Integer**.
7. Lauke **Reikšmė** įveskite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>8 veiksmas: Užduočių skaičiaus kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Užduočių skaičiaus init**.
5. In the **Pavadinimas** įveskite **užduočių skaičius**.
6. Lauke **Tipas** pasirinkite **Integer**.
7. Lauke **Reikšmė** įveskite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>9 veiksmas: Projekto užduoties ID kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijuoti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Init ProjectTaskID**.
5. In the **Pavadinimas** įveskite **užduočių skaičius**.
6. Lauke **Tipas** pasirinkite **Eilutė**.
7. Lauke **Reikšmė** įveskite **guid()** „expression builder“ lauke.

## <a name="step-10-do-until"></a><a id="10"></a>10 veiksmas: darykite iki

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lange **Pasirinkti operaciją** ieškos lauke įveskite **daryti iki**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Sąlyginės ataskaitos pirmąją reikšmę nustatykite kaip kintamąjį **užduočių skaičius** iš dialogo **Dinaminis turinys** lauko.
4. Sąlygą nustatykite į **mažesnis arba lygus**.
5. Sąlyginės ataskaitos antrą reikšmę nustatykite kaip **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a>11 veiksmas: nustatyti projekto užduotį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **nustatyti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Naujame veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Nustatyti projekto užduotį**.
5. Lauke **Name** pasirinkite **msdyn\_projecttaskid**.
6. Lauke **Reikšmė** įveskite **guid()** „expression builder“ lauke.

## <a name="step-12-create-a-project-task"></a><a id="12"></a>12 veiksmas. Sukurkite projekto užduotį

Atlikite šiuos veiksmus, kad sukurtumėte projekto užduotį, turinčia unikalų ID, priklausantį dabartiniam projektui ir jūsų sukurtam projekto talpyklai.

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusiejamąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Sukurti projekto užduotį**.
5. Lauke **Veiksmo pavadinimas** pasirinkite **msdyn\_PssCreateV1**.
6.  **Objekto“** lange įveskite toliau pateiktus informacinius parametrus.

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

    Toliau pateiktas parametrų paaiškinimas:

    - **\@\@odata.type** – objekto pavadinimas. Pavyzdžiui, įveskite **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**.
    - **msdyn\_projecttaskid** – Unikalusis užduoties ID. Reikšmė turi būti nustatyta į dinaminį kintamąjį iš **msdyn\_projecttaskid**.
    - **msdyn\_project\@odata.bind** – projektui priklausančio projekto ID. Reikšmė bus dinaminis turinys, gaunamas iš veiksmo „Kurti projektą" atsako. Įsitikinkite, kad įvedate visą kelią ir įtraukiate dinaminį turinį tarp skliaustelių. Kabutės yra būtinos. Pavyzdžiui, įveskite " **/msdyn\_projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_subject** – bet koks užduoties pavadinimas.
    - **msdyn\_projectbucket\@odata.bind** – projekto talpykla, kurioje yra užduotys. Reikšmė bus dinaminis turinys, gaunamas iš veiksmo "Kurti talpyklą" atsako. Įsitikinkite, kad įvedate visą kelią ir įtraukiate dinaminį turinį tarp skliaustelių. Kabutės yra būtinos. Pavyzdžiui, įveskite **/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)**.
    - **msdyn\_start** – dinaminis pradžios datos turinys. Pvz., rytoj bus pateikiamas kaip **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduledstart** – suplanuota operacijos pradžios data. Pvz., rytoj bus pateikiamas kaip **"addDays(utcNow(), 1)"**.
    - **msdyn\_scheduleend** – suplanuota pabaigos data. Ateityje pažymėkite datą. Pavyzdžiui, nurodykite **"addDays(utcNow(), 5)"**.
    - **msdyn\_LinkStatus** – saito būsena. Pavyzdžiui, įveskite **"192350000"**.

7. Lauke **OperationSetId** pasirinkite **msdyn\_CreateOperationSetV1Response** **Dinaminio turinio** dialogo lauke.

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>13 veiksmas: išteklių užduoties kūrimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusiejamąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti užduotį**.
5. Lauke **Veiksmo pavadinimas** pasirinkite **msdyn\_PssCreateV1**.
6.  **Objekto“** lange įveskite toliau pateiktus informacinius parametrus.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. Lauke **OperationSetId** pasirinkite **msdyn\_CreateOperationSetV1Response** **Dinaminio turinio** dialogo lauke.

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>Step 14: Kintamojo mažėjimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **mažinti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Lauke **Pavadinimas** įveskite **užduočių skaičius**.
4. Lauke **Reikšmė** įveskite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>15 veiksmas: pervadyti projekto užduotį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusiejamąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Pervadyti projekto užduotį**.
5. Lauke **Veiksmo pavadinimas** pasirinkite **msdyn\_PssUpdateV1**.
6.  **Objekto“** lange įveskite toliau pateiktus informacinius parametrus.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Lauke **OperationSetId** pasirinkite **msdyn\_CreateOperationSetV1Response** **Dinaminio turinio** dialogo lauke.

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>16 veiksmas: vykdykite operacijų rinkinį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusiejamąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pažymėkite operaciją.
3. Veiksme pažymėkite elipsę (**...**) ir tada pažymėkite **Pervardyti**.
4. Pervardykite veiksmą **Vykdyti operacijų rinkinį**.
5. Lauke **Veiksmo pavadinimas** pasirinkite **msdyn\_ExecuteOperationSetV1**.
6. Lauke **OperationSetId** pasirinkite **msdyn\_CreateOperationSetV1Response OperationSetId** **Dinaminio turinio** dialogo lauke.

## <a name="references"></a>Nuorodos

- [Apžvalga, kaip integruoti srautus į Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti](schedule-api-preview.md)
- [Debesies srautų apžvalga – Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Su sprendimais susijusių srautų apžvalga - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
