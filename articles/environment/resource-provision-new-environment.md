---
title: Naujos aplinkos parengimas
description: Šioje temoje pateikiama informacija, kaip parengti naują „Project Operations“ aplinką.
author: sigitac
manager: Annbe
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 09af2a7693c45d1d0b9c75420d018cc50d2cc0fa
ms.sourcegitcommit: 04c446746aad97fc3f4c3d441983c586b918a3a6
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/11/2020
ms.locfileid: "4727800"
---
# <a name="provision-a-new-environment"></a>Naujos aplinkos parengimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Šioje temoje pateikiama informacijos, kaip sukonfigūruoti naują „Dynamics 365 Project Operations“ aplinką, skirtą ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Automatinio „Project Operations“ parengimo įjungimas LCS projekte

Atlikite toliau nurodytus veiksmus, kad įjungtumėte automatinį „Project Operations“ parengimą LCS projekte.

1. Eikite į [LCS](https://lcs.dynamics.com/v2) ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.
2. Sąraše **Peržiūros versijos funkcija** pasirinkite **„Project Operations“ funkcija**, tada pasirinkite **Peržiūros versijos funkcija įjungta**, kad įjungtumėte „Project Operations“.

> [!NOTE]
> Šį veiksmą reikia atlikti tik vieną kartą LCS projekte.

## <a name="provision-a-project-operations-environment"></a>„Project Operations“ aplinkos parengimas

1. Atidarykite naują „Dynamics 365 Finance“ [demonstracinės aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) arba [smėlio dėžės / gamybos aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) visuotinio diegimo paketą. 
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

7. Pasirinktinai – aplinkai taikykite demonstracinius duomenis. Eikite į **Išplėstiniai parametrai**, pasirinkite **Tinkinti SQL duomenų bazės konfigūraciją** ir nustatykite parinktį **Nurodykite programos duomenų bazės duomenų rinkinį** į **Demonstracinis**.

8. Užpildykite likusius būtinus vediklio laukus ir patvirtinkite visuotinį diegimą. Aplinkos rengimo laikas skiriasi atsižvelgiant į aplinkos tipą. Parengimo procesas gali užtrukti iki šešių valandų.

  Sėkmingai užbaigus visuotinį diegimą, bus rodoma aplinkos būsena **Įdiegta**.

9. Jei norite patvirtinti, kad aplinka sėkmingai įdiegta, pasirinkite **Prisijungti** ir prissijungę prie aplinkos patvirtinkite.

![Išsami „“ aplinkos informacija](./media/3EnvironmentDetails.png)

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

5. Pasirinkite abu sprendimus **Dynamics 365 Finance and Operations“ dvigubo rašymo objektų schema** ir **„Dynamics 365 Project Operations“ dvigubo rašymo objektų schemos**, tada pasirinkite **Taikyti**.

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

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>„Project Operations“ saugos parametrų naujinimas „Dataverse“ aplinkoje

1. Eikite į „Project Operations“ „Dataverse“ aplinkoje. 
2. Eikite į **Parametrai** > **Sauga** > **Saugos vaidmenys**. 
3. Puslapio **Saugos vaidmenys** vaidmenų sąraše pasirinkite **dvigubo rašymo programos vartotoją** ir pasirinkite skirtuką **Tinkinti objektai**.  
4. Patikrinkite, ar vaidmuo turi **Skaityti** ir **Pridėti prie** teises, skirtas:
      
      - **Valiutos kurso tipas**
      - **Sąskaitų diagrama**
      - **Finansinis kalendorius**
      - **Didžioji knyga**

5. Atnaujinus saugos vaidmenį, eikite į **Parametrai** > **Sauga** > **Komandos** ir komandos rodinyje **Vietinės įmonės savininkas** pasirinkite numatytąją komandą.
6. Pasirinkite **Tvarkyti vaidmenis** ir patikrinkite, ar šiai komandai taikoma **dvigubo rašymo programos vartotojo** saugos teisė.

## <a name="run-project-operations-dual-write-maps"></a>„Project Operations“ dvigubo rašymo schemų vykdymas

1. LCS projekte eikite į puslapį **Išsami aplinkos informacija**.
2. Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**. Pasirinkus saitą būsite nukreipti į susiejimų objektų sąrašą.
3. Paleiskite schemas, kaip aprašyta toliau esančioje lentelėje. Būtinai viską darykite iš eilės, kaip nurodyta.

| **Objekto schema** | **Atnaujinti objektą** | **Pradinis sinchronizavimas** | **Pradinio sinchronizavimo šablonas** | **Vykdymo būtinosios sąlygos** | **Būtinas pradinis sinchronizavimas** |
| --- | --- | --- | --- | --- | --- |
| **Projekto išteklių vaidmenys visoms įmonėms (bookableresourcecategories)** | No | Taip | „Common Data Service“ | No | Nėra |
| **Juridiniai subjektai (cdm\_companies)** | No | Taip | „Finance and Operations“ programos | No | Nėra |
| **Didžioji knyga (msdyn_ledgers)** | No | Taip | „Finance and Operations“ programos | Taip | Taip, „Finance and Operations“ programos |
| **„Project Operations“ integravimo faktiniai duomenys (msdyn\_actuals)** | No | No | Nėra | Taip | No |
| **Projekto sutarties eilutės (salesorderdetails)** | No | No | Nėra | No | No |
| **Projekto operacijų ryšių integravimo objektas (msdyn\_transactionconnections)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo sutarties eilučių etapai (msdyn\_contractlinesscheduleofvalues)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo objektas, skirtas išlaidų įvertinimams (msdyn\_estimateslines)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integracijos projekto išlaidų kategorijų eksportavimo objektas (msdyn\_expensecategories)** | No | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo projekto išlaidų eksportavimo objektas (msdyn\_expenses)** | Taip | No | Nėra | No | Nėra |
| **„Project Operations“ integravimo objektas, skirtas valandų įvertinimams (msdyn\_resourceassignments)** | Taip | No | Nėra | No | Nėra |


4. Norėdami atnaujinti objektą, pasirinkite schemos pavadinimą ir pasirinkite **Atnaujinti objektus**. 


![Schemos atnaujinimas](./media/20RefreshMapping.png)

5. Atnaujinę paleiskite schemą. Prieš įjungdami kitą schemą patikrinkite, ar lentelėje schemos būsena yra **Vykdoma**. Gali šiek tiek užtrukti, kol bus paleistos schemos, turinčios daug būtinųjų sąlygų.

Norėdami paleisti schemą su būtinosiomis sąlygomis, įjunkite perjungiklį **Rodyti susijusias objektų schemas**. Jei lentelėje nurodyta **Būtinas pradinis sinchronizavimas** reikšmė **Ne**, įsitikinkite, kad žymės **Pradinis sinchronizavimas** būklė yra **Išjungta** visose būtinosiose schemose prieš ją vykdydami.

![Schemos vykdymas](./media/21RunMap.png)

6. Įsitikinkite, kad visos su projektu susijusios schemos yra vykdomos.

![Visos schemos yra vykdomos](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Konfigūracijos duomenų taikymas CDS, skirtoje „Project Operations“ (pasirenkama)

Jeigu pritaikėte demonstracinius duomenis „Finance“ aplinkoje, žr. [Konfigūracijos duomenų nustatymas ir taikymas „Project Operations” skirtoje „Common Data Service”](resource-apply-pro-setup-config-data.md), kad pritaikytumėte demonstracinius duomenis CDS aplinkai.


Jūsų „Project Operations“ aplinka dabar parengta ir sukonfigūruota. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]