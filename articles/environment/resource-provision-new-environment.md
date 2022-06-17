---
title: Naujos aplinkos parengimas
description: Šiame straipsnyje pateikiama informacija apie tai, kaip pateikti naują projekto operacijų aplinką.
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9cc3dafd6a2b6f92b585643c5d43ab52a3faf59e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8931616"
---
# <a name="provision-a-new-environment"></a>Naujos aplinkos parengimas

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_



Šiame straipsnyje pateikiama informacija apie tai, kaip sukurti naują Dynamics 365 Project Operations išteklių / nekauptų scenarijų aplinką.

## <a name="enable-project-operations-automated-provisioning-in-an-lcs-project"></a>Automatinio „Project Operations“ parengimo įjungimas LCS projekte

Atlikite toliau nurodytus veiksmus, kad įjungtumėte automatinį „Project Operations“ parengimą LCS projekte.

1. Eikite į [LCS](https://lcs.dynamics.com/v2) ir pasirinkite plytelę **Peržiūros versijos funkcijų valdymas**.
2. Sąraše **Peržiūros versijos funkcija** pasirinkite **„Project Operations“ funkcija**, tada pasirinkite **Peržiūros versijos funkcija įjungta**, kad įjungtumėte „Project Operations“.

   > [!NOTE]
   > Šį veiksmą reikia atlikti tik vieną kartą LCS projekte.

## <a name="provision-a-project-operations-environment"></a>„Project Operations“ aplinkos parengimas

1. Atidarykite naują Dynamics 365 Finance [demonstracinę aplinką](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) arba [smėlio dėžės / gamybos aplinkos](/dynamics365/fin-ops-core/dev-itpro/deployment/deployenvironment-newinfrastructure) diegimą. 
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

     ![Visuotinio diegimo parametrai.](./media/1DeploymentSettings.png)

    > [!IMPORTANT]
    > Pasirinkite **Sutinku**, kad sutiktumėte su paslaugos teikimo sąlygomis, tada pasirinkite **Atlikta**, kad grįžtumėte į visuotinio diegimo parametrus.
    >
    >![Visuotinio diegimo sutikimas.](./media/2DeploymentConsent.png)

7. Pasirinktinai – aplinkai taikykite demonstracinius duomenis. Eikite į **Išplėstiniai parametrai**, pasirinkite **Tinkinti SQL duomenų bazės konfigūraciją** ir nustatykite parinktį **Nurodykite programos duomenų bazės duomenų rinkinį** į **Demonstracinis**.
8. Užpildykite likusius būtinus vediklio laukus ir patvirtinkite visuotinį diegimą. Aplinkos rengimo laikas skiriasi atsižvelgiant į aplinkos tipą. Parengimo procesas gali užtrukti iki šešių valandų.

   Sėkmingai užbaigus visuotinį diegimą, bus rodoma aplinkos būsena **Įdiegta**.

9. Jei norite patvirtinti, kad aplinka sėkmingai įdiegta, pasirinkite **Prisijungti** ir prissijungę prie aplinkos patvirtinkite.

    ![Išsami aplinkos informacija.](./media/3EnvironmentDetails.png)

## <a name="apply-updates-to-the-finance-environment"></a>Naujinimų taikymas „Finance“ aplinkai

„Project Operations“ reikalinga „Finance“ aplinka su **10.0.13 (10.0.569.20009)** arba naujesnės versijos programa.

Kad galėtumėte gauti šią versiją, gali reikėti „Finance“ aplinkai taikyti kokybinius naujinimus.

1. LCS puslapio **Išsami aplinkos informacija** skyriuje **Pasiekimai naujiniai** pasirinkite **Peržiūrėti naujinį**.

    ![Peržiūrėti naujinius.](./media/5ViewUpdates.png)

2. Puslapyje **Dvejetainiai naujinimai** pasirinkite **Įrašyti paketą**.

    ![Įrašyti paketą.](./media/6SavePackage.png)

3. Spustelėkite **Pasirinkti viską** ir pasirinkite **Įrašyti paketą**.

    ![Peržiūrėti ir įrašyti naujinius.](./media/7ReviewAndSaveUpdates.png)

4. Įveskite paketo pavadinimą ir aprašą, tada pasirinkite **Įrašyti**. Atsižvelgiant į interneto ryšį, šis procesas gali šiek tiek užtrukti.

    ![Paketo nusiuntimas į išteklių biblioteką.](./media/8UploadPackageToAssetsLibrary.png)

5. Įrašę paketą pasirinkite **Atlikta** ir įrašykite šį paketą LCS projekto išteklių bibliotekoje.

   Paketo įrašymo ir tikrinimo procesas gali užtrukti maždaug 15 minučių.

6. Norėdami taikyti naujinį, eikite į LCS puslapį **Išsami aplinkos informacija** ir pasirinkite **Tvarkyti** > **Taikyti naujinius**.

    ![Aplinkų tvarkymas.](./media/9MaintainEnvironment.png)

7. Naujinių sąraše pasirinkite sukurtą paketą ir pasirinkite **Taikyti**.

    ![Naujinių taikymas.](./media/10ApplyUpdates.png)

   Aplinkos paruošimas gali šiek tiek užtrukti. Baigus vėl bus nustatyta aplinkos būsena Įdiegta.

    ![Aplinka įdiegta.](./media/11EnvironmentDeployed.png)

## <a name="establish-a-dual-write-connection"></a>Dvigubo rašymo ryšio nustatymas 

1. LCS projekte eikite į puslapį **Išsami aplinkos informacija**.
2. Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**.
3. Susiejus dar kartą pasirinkite **Susieti su CDS programoms**. Būsite nukreipti į dvigubo rašymo sistemą modulyje „Finance“.

    ![Susiejimas su CDS.](./media/12LinktoCDS.png)

4. Pasirinkite **Taikyti sprendimą**, kad pasiektumėte objektus, kurie bus susieti atliekant integravimą.

    ![Taikyti sprendimus.](./media/13ApplySolutions.png)

5. Pasirinkite abu sprendimus, **Dynamics 365 Finance and Operations Dvigubo rašymo objekto žemėlapį** ir **Dynamics 365 Project Operations Dvigubo rašymo objektų žemėlapius**, tada pasirinkite **Taikyti**.

    ![Sprendimų patvirtinimas.](./media/14ConfirmSolutions.png)

    Pritaikius sprendimus, į aplinką įtraukiami dvigubo rašymo objektai.

    ![Sprendimų taikymas.](./media/15ApplyingSolutions.png)

    Pritaikius objektus visi galimi susiejimai pateikiami aplinkoje.

    ![Dvigubo rašymo schemos.](./media/15DWMappings.png)

## <a name="refresh-the-data-entities-after-the-update"></a>Duomenų objektų atnaujinimas atlikus naujinimą

1. Modulyje „Finance“ eikite į darbo sritį **Duomenų valdymas**.

    ![Duomenų valdymo darbo sritis.](./media/16DataManagement.png)

2. Pasirinkite plytelę **Sistemos parametrai**.

    ![Sistemos parametrai.](./media/17FrameworkParameters.png)

3. Puslapyje **Objektų parametrai** pasirinkite **Atnaujinti objektų sąrašą**.

    ![Objektų sąrašo atnaujinimas.](./media/18RefreshEntityList.png)

Atnaujinimas truks apie 20 minučių. Kai jis bus baigtas, gausite įspėjimą.

  ![Patvirtinimo atnaujinimas.](./media/19RefreshConfirmation.png)

## <a name="update-security-settings-on-project-operations-on-dataverse"></a>„Project Operations“ saugos parametrų naujinimas „Dataverse“ aplinkoje

1. Eikite į „Project Operations“ „Dataverse“ aplinkoje. 
2. Eikite į **Parametrai** > **Sauga** > **Saugos vaidmenys**. 
3. Puslapio **Saugos vaidmenys** vaidmenų sąraše pasirinkite **dvigubo rašymo programos vartotoją** ir pasirinkite skirtuką **Tinkinti objektai**.  
4. Patikrinkite, ar vaidmuo turi **Skaityti** ir **Pridėti prie** teises šiems objektams:
      
      - **Valiutos kurso tipas**
      - **Sąskaitų diagrama**
      - **Finansinis kalendorius**
      - **Didžioji knyga**
      - **Įmonė**
      - **Išlaidos**

5. Atnaujinus saugos vaidmenį, eikite į **Parametrai** > **Sauga** > **Komandos** ir komandos rodinyje **Vietinės įmonės savininkas** pasirinkite numatytąją komandą.
6. Pasirinkite **Tvarkyti vaidmenis** ir patikrinkite, ar šiai komandai taikoma **dvigubo rašymo programos vartotojo** saugos teisė.

## <a name="run-project-operations-dual-write-maps"></a>„Project Operations“ dvigubo rašymo schemų vykdymas

1. LCS projekte eikite į puslapį **Išsami aplinkos informacija**.
2. Dalyje **„Common Data Service“ aplinkos informacija** pasirinkite **Susieti su CDS programoms**. Pasirinkus saitą būsite nukreipti į susiejimų objektų sąrašą.
3. Paleiskite schemas. Daugiau informacijos žr. [„Project Operations“ dvigubo rašymo schemų versijos](resource-dual-write-maps.md#project-operations-dual-write-maps)
4. Įsitikinkite, kad visos su projektu susijusios schemos yra vykdomos.

    ![Visos schemos yra vykdomos.](./media/22AllMapsRunning.png)


## <a name="apply-configuration-data-in-cds-for-project-operations-optional"></a>Konfigūracijos duomenų taikymas CDS, skirtoje „Project Operations“ (pasirenkama)

Jeigu pritaikėte demonstracinius duomenis „Finance“ aplinkoje, žr. [Konfigūracijos duomenų nustatymas ir taikymas „Project Operations” skirtoje „Common Data Service”](resource-apply-pro-setup-config-data.md), kad pritaikytumėte demonstracinius duomenis CDS aplinkai.


Jūsų „Project Operations“ aplinka dabar parengta ir sukonfigūruota. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
