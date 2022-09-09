---
title: Projekto grafiko API naudojimas su „Power Automate“
description: Šiame straipsnyje pateikiamas pavyzdinis srautas, kuriame naudojamos "Project schedule" programų programavimo sąsajos (API).
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

Šiame straipsnyje aprašomas pavyzdinis srautas, rodantis, kaip sukurti visą projekto planą naudojant Microsoft Power Automate, kaip sukurti operacijų rinkinį ir kaip naujinti objektą. Pavyzdyje parodoma, kaip sukurti projektą, projekto komandos narį, operacijų rinkinius, projekto užduotis ir išteklių užduotis. Šiame straipsnyje taip pat paaiškinama, kaip atnaujinti objektą ir vykdyti operacijų rinkinį.

Toliau pateikiamas išsamus veiksmų, kurie yra dokumentuoti šiame straipsnyje pateiktame pavyzdžių sraute, sąrašas:

1. [PowerApps Sukurkite paleidiklį](#1)
2. [Projekto kūrimas](#2)
3. [Komandos nario kintamojo inicijavimas](#3)
4. [Bendrojo komandos nario kūrimas](#4)
5. [Operacijų rinkinio kūrimas](#5)
6. [Projekto grupės kūrimas](#6)
7. [Saito būsenos kintamojo inicijavimas](#7)
8. [Užduočių skaičiaus kintamojo inicijavimas](#8)
9. [Projekto užduoties ID kintamojo inicijavimas](#9)
10. [Darykite iki](#10)
11. [Projekto užduoties nustatymas](#11)
12. [Projekto užduoties kūrimas](#12)
13. [Išteklių priskyrimo kūrimas](#13)
14. [Kintamojo mažinimas](#14)
15. [Projekto užduoties pervardijimas](#15)
16. [Operacijų rinkinio paleidimas](#16)

## <a name="assumptions"></a>Prielaidos

Šiame straipsnyje daroma prielaida, kad turite pagrindinių žinių apie platformą Dataverse, debesies srautus ir "Project Schedule" taikomųjų programų programavimo sąsają (API). Daugiau informacijos rasite toliau šiame straipsnyje esančiame [skyriuje Nuorodos](#references).

## <a name="create-a-flow"></a>Kurti srautą

### <a name="select-an-environment"></a>Pasirinkite aplinką

Galite sukurti srautą Power Automate savo aplinkoje.

1. Eikite į <https://flow.microsoft.com>, ir prisijunkite naudodami administratoriaus kredencialus.
2. Viršutiniame dešiniajame kampe pasirinkite **Aplinkos**.
3. Sąraše pasirinkite aplinką, kurioje Dynamics 365 Project Operations įdiegta.

### <a name="create-a-solution"></a>Sprendimo kūrimas

Atlikite šiuos veiksmus, kad sukurtumėte sprendimą suprantantį [srautą](/power-automate/overview-solution-flows). Sukūrę sprendimą suvokiantį srautą, galite lengviau eksportuoti srautą, kad galėtumėte jį naudoti vėliau.

1. Naršymo srityje pasirinkite **Sprendimai**.
2. **Puslapyje Sprendimai** pasirinkite **Naujas sprendimas**.
3. Dialogo lange **Naujas sprendimas** nustatykite reikiamus laukus, tada pasirinkite **Kurti**.

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a> 1 veiksmas: sukurkite PowerApps paleidiklį

1. **Puslapyje Sprendimai** pasirinkite sukurtą sprendimą, tada pasirinkite **Naujas**.
2. Kairiojoje srityje pasirinkite **Debesies srautai** \> **Automatizavimo debesies srautas** \> **·** \> **Akimirksniu.**
3. Lauke Srauto **pavadinimas** įveskite **Schedule API Demo Flow**.
4. Sąraše Pasirinkite **, kaip suaktyvinti šį srautą** pasirinkite **Power Apps**. Kai sukuriate paleidiklį Power Apps, logika priklauso nuo jūsų, kaip autoriaus. Šiame straipsnyje palikite įvesties parametrus tuščius bandymo tikslais.
5. Pasirinkite **Kurti**.

## <a name="step-2-create-a-project"></a><a id="2"></a>2 veiksmas. Sukurkite projektą

Atlikite šiuos veiksmus, kad sukurtumėte projekto pavyzdį.

1. Sukurtame sraute pasirinkite **Naujas veiksmas**.

    ![Naujo veiksmo pridėjimas.](media/newstep.png)

2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.

    ![Operacijos pasirinkimas.](media/chooseactiontab.png)

3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.

![Žingsnio pervadinimas.](media/renamestep.png)

4. Pervardykite veiksmą **Kurti projektą**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ CreateProjectV1**.
6. Po lauku **msdyn\_ tema** pasirinkite **Įtraukti dinaminį turinį**.
7. Skirtuko **Išraiška** lauke funkcija įveskite **Projekto pavadinimas - utcNow()**.
8. Pasirinkite **Gerai**.

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a> 3 veiksmas: komandos nario kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijavimo kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **"Init" komandos narys**.
5. **Lauke Pavadinimas** įveskite **TeamMemberAction**.
6. Lauke **Tipas** pasirinkite **Eilutė**.
7. **Lauke Reikšmė** įveskite **msdyn\_ CreateTeamMemberV1**.

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a> 4 veiksmas: sukurkite bendrąjį komandos narį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti komandos narį**.
5. Lauke Veiksmo **pavadinimas** dialogo lange Dinaminis **turinys** pasirinkite **TeamMemberAction**.
6. Lauke Veiksmo **parametrai** įveskite toliau nurodytą parametrų informaciją.

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

    Čia yra parametrų paaiškinimas:

    - **\@\@ odata.type** – objekto pavadinimas. Pavyzdžiui, įveskite **"Microsoft.Dynamics.CRM.msdyn\_ projectteam"**.
    - **msdyn\_ projectteamid** – Pagrindinis projekto komandos ID raktas. Reikšmė yra globaliai unikali identifikatoriaus (GUID) išraiška.   ID sugeneruojamas iš išraiškos skirtuko.

    - **msdyn\_ project\@ odata.bind** – Nuosavo projekto ID. Reikšmė bus dinaminis turinys, gaunamas iš veiksmo "Sukurti projektą" atsakymo. Įsitikinkite, kad įvedėte visą kelią ir skliausteliuose pridėjote dinaminio turinio. Reikalingos kabutės. Pavyzdžiui, įveskite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ vardas** – Komandos nario vardas ir pavardė. Pavyzdžiui, įveskite **"ScheduleAPIDemoTM1"**.

## <a name="step-5-create-an-operation-set"></a><a id="5"></a> 5 veiksmas: sukurkite operacijų rinkinį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Sukurti operacijų rinkinį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite pasirinktinį veiksmą **msdyn\_ CreateOperationSetV1** Dataverse.
6. **Lauke Aprašas** įveskite **ScheduleAPIDemoOperationSet**.
7. **Lauke Projektas** įveskite **/msdyn\_ projects(**.
8. Dialogo lange Dinaminis **turinys** pasirinkite **msdyn\_ CreateProjectV1Response ProjectId**.
9. **Lauke Projektas** įveskite **)**.

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a> 6 veiksmas: sukurkite projekto grupę

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **įtraukti naują eilutę**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti kaušą**.
5. **Lauke Lentelės pavadinimas** pasirinkite **Projekto kaušai**.
6. **Lauke Pavadinimas** įveskite **ScheduleAPIDemoBucket1**.
7. **Lauke Projektas** pasirinkite **msdyn\_ CreateProjectV1Response ProjectId** dialogo lange Dinaminis **turinys**.

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a> 7 veiksmas: nuorodos būsenos kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijavimo kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Init linkstatus**.
5. **Lauke Pavadinimas** įveskite **linkstatus**.
6. **Lauke Tipas** pasirinkite **Sveikasis skaičius**.
7. **Lauke Reikšmė** įveskite **192350000**.

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a> 8 veiksmas: užduočių skaičiaus kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijavimo kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Init užduočių** skaičius.
5. **Lauke Pavadinimas** įveskite **užduočių** skaičių.
6. **Lauke Tipas** pasirinkite **Sveikasis skaičius**.
7. **Lauke Reikšmė** įveskite **5**.

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a> 9 veiksmas: projekto užduoties ID kintamojo inicijavimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **inicijavimo kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **"Init ProjectTaskID**".
5. **Lauke Pavadinimas** įveskite **užduočių** skaičių.
6. Lauke **Tipas** pasirinkite **Eilutė**.
7. Lauke Reikšmė **reiškinio** daryklėje įveskite **guid() (guid().**

## <a name="step-10-do-until"></a><a id="10"></a> 10 veiksmas: darykite iki

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **daryti iki**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Nustatykite pirmąją sąlyginio sakinio reikšmę **į užduočių** skaičiaus kintamąjį iš dialogo lango Dinaminis **turinys**.
4. Nustatykite, kad sąlyga būtų **mažesnė nei lygi**.
5. Nustatykite antrąją sąlyginio teiginio reikšmę į **0**.

## <a name="step-11-set-a-project-task"></a><a id="11"></a> 11 veiksmas: nustatykite projekto užduotį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **nustatyti kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami naują veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Nustatyti projekto užduotį**.
5. **Lauke Pavadinimas** pasirinkite **msdyn\_ projecttaskid**.
6. Lauke Reikšmė **reiškinio** daryklėje įveskite **guid() (guid().**

## <a name="step-12-create-a-project-task"></a><a id="12"></a> 12 veiksmas: sukurkite projekto užduotį

Atlikite šiuos veiksmus, kad sukurtumėte projekto užduotį, turinčią unikalų ID, priklausantį dabartiniam projektui ir jūsų sukurtam projekto kibirui.

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti projekto užduotį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ PssCreateV1**.
6. **Lauke Objektas** įveskite toliau nurodytą parametro informaciją.

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

    Čia yra parametrų paaiškinimas:

    - **\@\@ odata.type** – objekto pavadinimas. Pavyzdžiui, įveskite **"Microsoft.Dynamics.CRM.msdyn\_ projecttask"**.
    - **msdyn\_ projecttaskid** – Unikalus užduoties ID. Vertė turėtų būti nustatyta į dinaminį kintamąjį iš **msdyn\_ projecttaskid**.
    - **msdyn\_ project\@ odata.bind** – Nuosavo projekto ID. Reikšmė bus dinaminis turinys, gaunamas iš veiksmo "Sukurti projektą" atsakymo. Įsitikinkite, kad įvedėte visą kelią ir skliausteliuose pridėjote dinaminio turinio. Reikalingos kabutės. Pavyzdžiui, įveskite **"/msdyn\_ projects(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ tema** – Bet koks užduoties pavadinimas.
    - **msdyn\_ projectbucket\@ odata.bind** - Projekto kibiras, kuriame yra užduotys. Reikšmė bus dinaminis turinys, gaunamas iš žingsnio "Sukurti kibirą" atsakymo. Įsitikinkite, kad įvedėte visą kelią ir skliausteliuose pridėjote dinaminio turinio. Reikalingos kabutės. Pavyzdžiui, įveskite **"/msdyn\_ projectbuckets(ADD DYNAMIC CONTENT)"**.
    - **msdyn\_ start** – dinaminis pradžios datos turinys. Pavyzdžiui, rytojus bus pavaizduotas kaip **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduledstart** – numatyta pradžios data. Pavyzdžiui, rytojus bus pavaizduotas kaip **"addDays(utcNow(), 1)"**.
    - **msdyn\_ scheduleend** – numatyta pabaigos data. Pasirinkite datą ateityje. Pavyzdžiui, nurodykite **"addDays(utcNow(), 5)"**.
    - **msdyn\_ LinkStatus** – nuorodos būsena. Pavyzdžiui, įveskite **"192350000"**.

7. Lauke OperationSetId **dialogo lange Dinaminis turinys** pasirinkite **msdyn\_ CreateOperationSetV1Response** **.**

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a> 13 veiksmas: išteklių priskyrimo kūrimas

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Kurti priskyrimą**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ PssCreateV1**.
6. **Lauke Objektas** įveskite toliau nurodytą parametro informaciją.

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

7. Lauke OperationSetId **dialogo lange Dinaminis turinys** pasirinkite **msdyn\_ CreateOperationSetV1Response** **.**

## <a name="step-14-decrement-a-variable"></a><a id="14"></a> 14 veiksmas: sumažinkite kintamąjį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **sumažinimo kintamąjį**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. **Lauke Pavadinimas** pasirinkite **užduočių** skaičių.
4. **Lauke Reikšmė** įveskite **1**.

## <a name="step-15-rename-a-project-task"></a><a id="15"></a> 15 veiksmas: pervardykite projekto užduotį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Pervardyti projekto užduotį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ PssUpdateV1**.
6. **Lauke Objektas** įveskite toliau nurodytą parametro informaciją.

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. Lauke OperationSetId **dialogo lange Dinaminis turinys** pasirinkite **msdyn\_ CreateOperationSetV1Response** **.**

## <a name="step-16-run-an-operation-set"></a><a id="16"></a> 16 veiksmas: paleiskite operacijų rinkinį

1. Sraute pasirinkite **Naujas veiksmas**.
2. Dialogo lango **Pasirinkti operaciją** ieškos lauke įveskite **atlikti nesusietąjį veiksmą**. Tada skirtuke **Veiksmai** rezultatų sąraše pasirinkite operaciją.
3. Atlikdami veiksmą pasirinkite daugtaškį (**...**), tada pasirinkite **Pervardyti**.
4. Pervardykite veiksmą **Vykdyti operacijų rinkinį**.
5. Lauke Veiksmo **pavadinimas** pasirinkite **msdyn\_ ExecuteOperationSetV1**.
6. **Lauke OperationSetId** pasirinkite **msdyn\_ CreateOperationSetV1Atsakyti operacijąSetId** **dialogo lange Dynamid turinys**.

## <a name="references"></a>Nuorodos

- [Apžvalga, kaip integruoti srautus su Dataverse - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [Projekto grafiko API sąsajų naudojimas operacijoms su planavimo objektais atlikti](schedule-api-preview.md)
- [Debesų srautų apžvalga - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [Sprendimų suvokimo srautų apžvalga - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
