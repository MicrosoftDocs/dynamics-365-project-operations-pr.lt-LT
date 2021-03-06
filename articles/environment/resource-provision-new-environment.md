---
title: Naujos aplinkos parengimas
description: Šioje temoje pateikiama informacija, kaip parengti naują „Project Operations“ aplinką.
author: sigitac
manager: Annbe
ms.date: 10/02/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 45700371c50e3b5a840df45fc24fa8a5b4584b61
ms.sourcegitcommit: 87b7a8d793c19c50f3765b8d788cde24a6a0ca24
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3949372"
---
# <a name="provision-a-new-environment"></a>Naujos aplinkos parengimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje pateikiama informacija, kaip parengti naują „Dynamics 365 Project Operations“ aplinką, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Automatinio „Project Operations“ parengimo įjungimas LCS projekte

Atlikite toliau nurodytus veiksmus, kad įjungtumėte automatinį „Project Operations“ parengimą LCS projekte.

1. Eikite į [LCS](https://lcs.dynamics.com/v2) ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.
2. Sąraše **Peržiūros versijos funkcija** pasirinkite **Project Operations** ir pasirinkite **Peržiūros versijos funkcija įjungta**, kad įjungtumėte „Project Operations“.

> [!NOTE]
> Šį veiksmą reikia atlikti tik vieną kartą LCS projekte.

## <a name="provision-a-project-operations-environment"></a>„Project Operations“ aplinkos parengimas

1. Atidarykite naują „Dynamics 365 Finance“ [demonstracinės aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) arba [smėlio dėžės / gamybos aplinkos](https://docs.microsoft.com/edynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) visuotinio diegimo paketą. 
2. Atlikite vediklio **Aplinkos parengimas** veiksmus. 

> [!IMPORTANT]
> Įsitikinkite, kad naudojama 10.0.13 arba naujesnė programos versija.

3. Norėdami parengti „Project Operations“, dalyje **Išplėstiniai parametrai** pasirinkite **Common Data Service**. 
4. Įjunkite parametrą **„Common Data Service“ parametras** pasirinkdami **Taip** ir įveskite informaciją privalomuose laukuose:

  - Pavadinimas / vardas, pavardė
  - Regiono ID
  - Kalba
  - Valiuta
 
5. Lauke **„Common Data Service“ šablonas** pasirinkite **Project Operations** 

6. Pasirinkite visuotinio diegimo aplinkos tipą. Jei naudojate prenumeruojamą bandomąją versiją, CDS aplinka galės būti įdiegta 30 dienų. 

![Visuotinio diegimo parametrai](./media/1DeploymentSettings.png)

> [!IMPORTANT]
> Pasirinkite **Sutinku**, kad sutiktumėte su paslaugos teikimo sąlygomis, tada pasirinkite **Atlikta**, kad grįžtumėte į visuotinio diegimo parametrus.

![Visuotinio diegimo sutikimas](./media/2DeploymentConsent.png)

7. Užpildykite likusius būtinus vediklio laukus ir patvirtinkite visuotinį diegimą. Aplinkos parengimo laikas priklauso nuo aplinkos tipo. Parengimo procesas gali užtrukti iki šešių valandų.

  Sėkmingai užbaigus visuotinį diegimą, bus rodoma aplinkos būsena **Įdiegta**.

8. Norėdami įsitikinti, kad aplinka sėkmingai įdiegta, pasirinkite **Prisijungti** ir prisijunkite prie aplinkos, kad patvirtintumėte.

![Išsami „“ aplinkos informacija](./media/3EnvironmentDetails.png)

## <a name="apply-project-operations-finance-demo-data-optional-step"></a>„Project Operations Finance“ demonstracinių duomenų taikymas (pasirinktinis veiksmas)

Taikykite „Project Operations Finance“ demonstracinius duomenis 10.0.13 paslaugų leidimo debesyje esančiai aplinkai, kaip aprašyta [šiame straipsnyje](resource-apply-finance-demo-data.md).

## <a name="apply-updates-to-the-finance-environment"></a>Naujinimų taikymas „Finance“ aplinkai

„Project Operations“ reikalinga „Finance“ aplinka su **10.0.13 (10.0.569.20009)** arba naujesnės versijos programa.

Kad galėtumėte gauti šią versiją, gali reikėti „Finance“ aplinkai taikyti kokybinius naujinimus.

1. LCS puslapio **Išsami aplinkos informacija** skyriuje **Pasiekimai naujiniai** pasirinkite **Peržiūrėti naujinį**.

![Peržiūrėti naujinius](./media/5ViewUpdates.png)

2. Puslapyje **Dvejetainiai naujinimai** pasirinkite **Įrašyti paketą**.

![Įrašyti paketą](./media/6SavePackage.png)

3. Spustelėkite **Pasirinkti viską** ir pasirinkite **Įrašyti paketą**.

![Peržiūrėti ir įrašyti naujinius](./media/7ReviewAndSaveUpdates.png)

4. Įveskite paketo pavadinimą ir aprašą, tada pasirinkite **Įrašyti**. Atsižvelgiant į interneto ryšį, šis procesas gali šiek tiek užtrukti.

![Paketo nusiuntimas į išteklių biblioteką](./media/8UploadPackageToAssetsLibrary.png)

5. Įrašę paketą pasirinkite **Atlikta** ir įrašykite šį paketą LCS projekto išteklių bibliotekoje.

Paketo įrašymo ir tikrinimo procesas gali užtrukti maždaug 15 minučių.

6. Norėdami taikyti naujinį, eikite į LCS puslapį **Išsami aplinkos informacija** ir pasirinkite **Tvarkyti** > **Taikyti naujinius**.

![Aplinkų tvarkymas](./media/9MaintainEnvironment.png)

7. Naujinių sąraše pasirinkite sukurtą paketą ir pasirinkite **Taikyti**.

![Naujinių taikymas](./media/10ApplyUpdates.png)

Aplinkos paruošimas gali šiek tiek užtrukti. Baigus vėl bus nustatyta aplinkos būsena Įdiegta.

![Aplinka įdiegta](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Dvigubo rašymo ryšio nustatymas 

1. LCS projekte eikite į puslapį **Išsami aplinkos informacija**.
2. Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**.
3. Susiejus dar kartą pasirinkite **Susieti su CDS programoms**. Būsite nukreipti į dvigubo rašymo sistemą modulyje „Finance“.

![Susiejimas su CDS](./media/12LinktoCDS.png)

4. Pasirinkite **Taikyti sprendimą**, kad pasiektumėte objektus, kurie bus susieti atliekant integravimą.

![Taikyti sprendimus](./media/13ApplySolutions.png)

5. Pasirinkite abu sprendimus: **„Dynamics 365 Finance and Operations“ dvigubo rašymo objektų schema** ir **„Dynamics 365 Project Operations“ dvigubo rašymo objektų schemos**, tada pasirinkite **Taikyti**.

![Sprendimų patvirtinimas](./media/14ConfirmSolutions.png)

Pritaikius sprendimus, į aplinką įtraukiami dvigubo rašymo objektai.

![Sprendimų taikymas](./media/15ApplyingSolutions.png)

Pritaikius objektus visi galimi susiejimai pateikiami aplinkoje.

![Dvigubo rašymo schemos](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Duomenų objektų atnaujinimas atlikus naujinimą

1. Modulyje „Finance“ eikite į darbo sritį **Duomenų valdymas**.

![Duomenų valdymo darbo sritis](./media/16DataManagement.png)

2. Pasirinkite plytelę **Sistemos parametrai**.

![Sistemos parametrai](./media/17FrameworkParameters.png)

3. Puslapyje **Objektų parametrai** pasirinkite **Atnaujinti objektų sąrašą**.

![Objektų sąrašo atnaujinimas](./media/18RefreshEntityList.png)

Atnaujinimas truks apie 20 minučių. Kai jis bus baigtas, gausite įspėjimą.

![Patvirtinimo atnaujinimas](./media/19RefreshConfirmation.png)

## <a name="run-project-operations-dual-write-maps"></a>„Project Operations“ dvigubo rašymo schemų vykdymas

1. LCS projekte eikite į puslapį **Išsami aplinkos informacija**.
2. Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**. Pasirinkus saitą būsite nukreipti į susiejimų objektų sąrašą.
3. Paleiskite schemas, kaip aprašyta toliau esančioje lentelėje. Būtinai viską darykite iš eilės, kaip nurodyta.

| **Objekto schema** | **Atnaujinti objektą** | **Pradinis sinchronizavimas** | **Pradinio sinchronizavimo šablonas** | **Vykdymo būtinosios sąlygos** | **Būtinas pradinis sinchronizavimas** |
| --- | --- | --- | --- | --- | --- |
| **Projekto išteklių vaidmenys visoms įmonėms (bookableresourcecategories)** | No | Taip | „Common Data Service“ | No | Nėra |
| **Juridiniai subjektai (cdm\_companies)** | No | Taip | „Finance and Operations“ programos | No | Nėra |
| **„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)** | No | No | Nėra | Taip | No |
| **Projekto sutarties eilutės (salesorderdetails)** | No | No | Nėra | No | No |
| **Projekto operacijų ryšių integravimo objektas (msdyn\_transactionconnections)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo sutarties eilučių etapai (msdyn\_contractlinesscheduleofvalues)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo objektas, skirtas išlaidų įvertinimams (msdyn\_estimateslines)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo objektas, skirtas valandų įvertinimams (msdyn\_resourceassignments)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo projekto išlaidų eksportavimo objektas (msdyn\_expenses)** | Taip | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo objektas, skirtas valandų įvertinimams (msdyn\_resourceassignments)** | Taip | No | Nėra | No | Nėra |

4. Norėdami atnaujinti objektą, pasirinkite schemos pavadinimą ir pasirinkite **Atnaujinti objektus**. 
5. Atnaujinus paleiskite schemą.

![Schemos atnaujinimas](./media/20RefreshMapping.png)

Prieš įjungdami kitą schemą patikrinkite, ar lentelėje schemos būsena yra **Vykdoma**. Gali šiek tiek užtrukti, kol bus paleistos schemos, turinčios daug būtinųjų sąlygų.

Norėdami paleisti schemą su būtinosiomis sąlygomis, įjunkite perjungiklį **Rodyti susijusias objektų schemas**. Jei lentelėje nurodyta **Būtinas pradinis sinchronizavimas** reikšmė **Ne**, įsitikinkite, kad žymės **Pradinis sinchronizavimas** būklė yra **Išjungta** visose būtinosiose schemose prieš ją vykdydami.

![Schemos vykdymas](./media/21RunMap.png)

6. Įsitikinkite, kad visos su projektu susijusios schemos yra vykdomos.

![Visos schemos yra vykdomos](./media/22AllMapsRunning.png)

Jūsų „Project Operations“ aplinka dabar parengta ir sukonfigūruota.
