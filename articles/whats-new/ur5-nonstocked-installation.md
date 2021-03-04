---
title: „Project Operations“ naujinimas „Finance“ aplinkoje
description: Šioje temoje pateikiama informacija apie tai, kaip atnaujinti „Project Operations” „Dynamics 365 Finance“ aplinkoje.
author: ruhercul
manager: tfehr
ms.date: 12/11/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 249b8dba17165da04596ec46a625131b9b4daeb5
ms.sourcegitcommit: f4fc6e3a81e8551da050e92f8fde85f8d7b52fbd
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 12/29/2020
ms.locfileid: "4816635"
---
# <a name="update-project-operations-in-your-finance-environment"></a>„Project Operations“ naujinimas „Finance“ aplinkoje

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_


Šioje temoje pateikiama informacija apie tai, kaip atnaujinti „Dynamics 365 Project Operations“ „Dynamics 365 Finance“ aplinkoje. Yra trys procedūros, kurių reikia norint atnaujinti „Project Operations“ į 5 naujinimą (UR5):

- [Importuokite paketą į savo peržiūros projektą](#import)
- [Taikykite naujinimą](#apply)
- [Atnaujinkite „Dataverse“ aplinką](#update)

## <a name="import-the-package-into-your-lcs-project"></a><a name="import"></a>Importuokite paketą į savo LCS projektą

1. Prisijunkite prie [„Lifecycle Services“ (LCS)](https://lcs.dynamics.com/) kaip projekto savininkas arba aplinkos vadovas.
2. Projektų sąraše pažymėkite savo LCS projektą.
3. Puslapyje **Projektas**, grupėje **Aplinka** atidarykite norimą naujinti aplinką.
4. Patikrinkite, ar veikia aplinka. Jei ji nevykdoma, paleiskite aplinką.
5. Dalies **Galimi naujinimai** skyriuje **Naujas leidimas** pasirinkite **Peržiūrėti naujinimą**, skirtą 10.0.15.

![Naujinimo peržiūros mygtukas](media/view-update.png)

6. Puslapyje **Dvejetainiai naujinimai** pasirinkite **Įrašyti paketą**.
7. Puslapyje **Peržiūrėti ir įrašyti naujinimus** pasirinkite **Įrašyti paketą**.
8. Atidaromoje srityje **Įrašyti paketą į turto biblioteką** įveskite paketo pavadinimą, o tada pasirinkite **Įrašyti paketą**.
9. Kai LCS baigia įrašyti paketą, įjungiamas mygtukas **Atlikta**. Pasirinkite **Atlikta**. LCS patikrins paketą. Tikrinimas gali užtrukti kelias minutes arba iki vienos valandos.


## <a name="apply-the-package-update"></a><a name="apply"></a>Taikykite paketo naujinimą

1. LCS programos puslapyje **Išsami aplinkos informacija** pasirinkite **Prižiūrėti** > **Taikyti naujinimus**.
2. Sąraše pažymėkite anksčiau įrašytą paketą, o tada pasirinkite **Taikyti**.
3. Pasirinkite **Taip**, kad patvirtintumėte, jog norite visuotinai įdiegti paketą.

![Paketo visuotinio diegimo dialogo lango patvirtinimas](media/confirm-package-deployment.png)

4. Pasirinkite **Taip**, kad patvirtintumėte, jog norite atnaujinti programą.

![Programos naujinimo dialogo lango patvirtinimas](media/confirm-application-update.png)

Bus pradėta diegti ir naujinti programą. 

Puslapyje **Išsami aplinkos informacija**, viršutiniame dešiniajame kampe, aplinkos būsena bus atnaujinta į **Aptarnavimas**. Po maždaug dviejų valandų naujinimas bus baigtas. Programos leidimo informacija bus atnaujinta į **„Microsoft Dynamics 365 for Finance and Operations“ 10.0.15)**, o aplinkos būsena bus atnaujina į **Įdiegta**.


## <a name="update-your-dataverse-environment"></a><a name="update"></a>Atnaujinkite „Dataverse“ aplinką

1. Prisijunkite prie [„Power Platform“ administravimo centro](https://admin.powerplatform.com/).
2. Sąraše raskite ir atidarykite aplinką, kurią naudojote diegdami „Project Operations“.
3. Puslapyje **Aplinkos** pažymėkite **Išteklius** > **„Dynamics 365“ programos**.
4. Sąraše raskite **„Microsoft Dynamics 365 Project Operations“** ir stulpelyje **Būsena** pasirinkite **Galimas naujinimas**.
5. Pažymėkite žymės langelį **Sutinku su aptarnavimo sąlygomis**, o tada pažymėkite **Atnaujinti**. Bus įdiegta naujausia sprendimo versija.

Baigę diegti turėsite įdiegtą 4.5.0.134 versiją.

## <a name="configure-new-features"></a>Naujų funkcijų konfigūravimas

### <a name="enable-dual-write-mapping"></a>Dvigubo rašymo susiejimo įgalinimas

Baigę naujinti „Finance“ ir „Dataverse“ aplinkas, galite įjungti reikiamus dvigubo rašymo susiejimus. Norėdami įgalinti dvigubo rašymo susiejimus, atlikite toliau nurodytas procedūras.

- [„Customer Engagement“ aplinkos saugos parametrų naujinimas](#security)
- [Duomenų objektų atnaujinimas](#refresh)
- [Dvigubo rašymo susiejimų atnaujinimas ir paleidimas](#run)

### <a name="update-security-settings-on-the-dataverse-environment"></a><a name="security"></a>Atnaujinkite „Dataverse“ aplinkos saugos parametrus

Toliau nurodyti objektų saugos teisių naujinimai būtini kaip UR5 naujinimo dalis.

1. Savo „Dataverse“ aplinkoje eikite į **Parametrai**, o grupėje **Sistema** pasirinkite **Sauga**.

![„Dataverse“ aplinkos nustatymai](media/Picture21.png)

2. Pasirinkite **Saugos vaidmenys**.
3. Vaidmenų sąraše pasirinkite **dvigubo rašymo programos vartotoją** ir pasirinkite skirtuką **Tinkinti objektai**. 
4. Patikrinkite, ar vaidmuo turi **Skaityti** ir **Pridėti prie** teises, skirtas:

      - **Valiutos kurso tipas**
      - **Sąskaitų diagrama** 
      - **Finansinis kalendorius** 
      - **Didžioji knyga**

5. Atnaujinus saugos vaidmenį, eikite į **Parametrai** > **Sauga** > **Komandos**. Patikrinkite, ar komandai buvo pritaikytas **dvigubo rašymo programos vartotojo** vaidmuo. 

### <a name="refresh-data-entities-from-the-update"></a><a name="refresh"></a>Atnaujinkite duomenų objektus iš naujinimo

1. Savo „Finance“ aplinkoje atidarykite darbo sritį **Duomenų valdymas**, o tada atidarykite puslapį **Sistemos parametrai**.
2. Skirtuke **Objekto parametrai** pasirinkite **Atnaujinti objektų sąrašą**.
3. Pažymėkite **Uždaryti**, kad patvirtintumėte objekto atnaujinimą.

 > [!NOTE]
 > Tai užtruks maždaug 20 minučių. Jums bus pranešta, kai bus baigtas naujinimas.

### <a name="update-dual-write-mappings"></a><a name="run"></a>Atnaujinkite dvigubo rašymo susiejimus

1. Darbo srityje **Duomenų valdymas** pasirinkite **Dvigubas rašymas**.
2. Pažymėkite **Taikyti sprendimus**, pasirinkite abu sprendimus, o tada pažymėkite **Taikyti**.
3. Puslapyje **Dvigubas rašymas** pažymėkite toliau nurodytas lentelių struktūras, o tada pasirinkite **Sustabdyti**.

    - **„Project Operations“ integravimo faktiniai duomenys (msdyn_actuals)**
    - **„Project Operations“ integravimo projekto išlaidų kategorijos (msdyn_expensecategories)**
    - **„Project Operations“ integravimo faktinių duomenų projekto išlaidų eksportavimo objektas (msdyn_expenses)**

4. Puslapyje **Lentelės struktūros versija** taikykite naują struktūros versiją kiekvienam iš trijų objektų.
5. Puslapyje **Dvigubas rašymas** pasirinkite vykdyti ir iš naujo paleisti struktūras.
6. Struktūrų sąraše pažymėkite **Didžioji knyga (msdyn_ledgers)** struktūrą su visomis būtinosiomis sąlygomis ir pasirinkite žymės langelį **Pradinis sinchronizavimas**. 
7. Lauke **Pradinio sinchronizavimo šablonas** pasirinkite **„Finance and Operations“ programos**, o tada pasirinkite **Vykdyti**.
 
 ![Didžiosios knygos struktūros sinchronizavimas](media/DW6.png)
 


[!INCLUDE[footer-include](../includes/footer-banner.md)]