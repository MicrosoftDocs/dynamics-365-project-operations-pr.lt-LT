---
title: Konfigūracijos duomenų nustatymas ir taikymas programoje „Common Data Service”
description: Šioje temoje pateikta informacija apie konfigūracijos duomenų nustatymą ir taikymą dalyje „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 11/04/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7de8db5e91265c77c79f34a513bf27d9a55b789a
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401138"
---
# <a name="set-up-and-apply-configuration-data-in-the-common-data-service"></a>Konfigūracijos duomenų nustatymas ir taikymas programoje „Common Data Service” 

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

## <a name="prerequisites"></a>Būtinosios sąlygos

Prieš pradėdami konfigūruoti duomenis programoje „Common Data Service” (CDS), turite atitikti toliau pateikiamas būtinąsias sąlygas.

1.  CDS aplinkos ir „Dynamics 365 Finance” aplinkos parengimas, skirtas „Project Operations”.
2.  Juridinio objekto informacija iš „Dynamics 365 Finance” bendrinama su CDS aplinka. Tai reiškia, kad CDS esančiame objekte **Įmonė** yra toliau pateikiami įmonės įrašai.
  - THPM
  - USPM
  - GBPM

## <a name="install-setup-and-configuration-data"></a>Sąrankos ir konfigūracijos duomenų diegimas

1. Atsisiųskite, atblokuokite ir išskleiskite [sąrankos ir konfigūracijos duomenų paketą](https://download.microsoft.com/download/1/3/4/1349369c-6209-42b7-b3b4-5be0e67cacd8/ProjOpsSampleSetupData-%20Integrated%20UR1.zip).
2. Nueikite į neišskleistą aplanką ir vykdykite vykdomąjį failą *DataMigrationUtility*.
3. „Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.

![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. CMT vedlio 2 puslapyje pažymėkite **Microsoft 365** kaip **Visuotinio diegimo tipą**.
5. Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.
6. Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus ir pasirinkite **Prisijungti**.

![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. 3 puslapyje nuomotojo organizacijų sąraše pasirinkite organizaciją, į kurią norite importuoti demonstracinius duomenis, ir pasirinkite **Prisijungti**.
8. 4 puslapyje pasirinkite suglaudintą failą *SampleSetupAndConfigData* neišskleistame aplanke.

![Suglaudinto failo pasirinkimas](./media/3ZipFile.png)

![Pasirinkite failą](./media/4SelectAFile.png)

9. Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.

![Importuoti duomenis](./media/5ImportData.png)

10. Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių. Baigus importuoti uždarykite CMT vediklį. 
11. Patikrinkite savo organizacijos duomenis šiuose 19 objektų:

  - Valiuta
  - Organizacijos vienetas
  - Susisiekite
  - Mokesčių grupė
  - Klientų grupė
  - Vienetas
  - Vienetų grupė
  - Kainoraštis
  - Projekto parametrų kainoraštis
  - Sąskaitos faktūros dažnumas
  - Rezervuojamų išteklių kategorija
  - Operacijos kategorija
  - Išlaidų kategorija
  - Vaidmens kaina
  - Operacijos kategorijos kaina
  - Charakteristika
  - Rezervuojamas išteklius
  - Rezervuojamų išteklių kategorijos sąsaja
  - Rezervuojamų išteklių charakteristika

![Importavimo užbaigimas](./media/6CompleteImport.png)

## <a name="update-project-operations-configurations"></a>„Project Operations“ konfigūracijų naujinimas

1. Eikite į CE aplinką. Ją rasite atidarę [„Power Platform“ administravimo centrą](https://admin.powerplatform.microsoft.com/environments), pasirinkę aplinką ir pasirinkę **Atidaryti aplinką**. 

![Aplinkos atidarymas](./media/7OpenEnvironment.png)

2. Eikite į **Projektai** > **Ištekliai**, tada pasirinkite **Naujas**, kad vartotojui sukurtumėte išteklių, kurį galima rezervuoti.

![Rezervuojami ištekliai](./media/8BookableResources.png)

3. Skirtuke **Bendra** pasirinkite administratoriaus vartotoją. Patikrinkite, ar laiko juosta atitinka tą, kurioje esate jūs. 

![Naujas rezervuojamas išteklius](./media/9NewBookableResource.png)

4. Skirtuko **Planavimas** lauke **Įmonė** pasirinkite įmonę **USPM** ir pasirinkite **Įrašyti**. 

![Planavimo skirtukas](./media/10SchedulingTab.png)

5. Pasirinkite skirtuką **Darbo valandos**.  

![Darbo valandos](./media/11WorkHours.png)

6. Kalendoriuje dukart spustelėkite bet kokią reikšmę ir pasirinkite **Redaguoti** > **Visi sekos įvykiai**. 

![Darbo kalendorius](./media/12WorkCalendar.png)

7. Pakeiskite darbo valandas į aštuonių (8) valandų darbo dieną, pažymėkite savaitgalius kaip ne darbo dienas ir įsitikinkite, kad laiko juosta atitinka jūsų. 
8. Pasirinkite **Įrašyti ir uždaryti**.

![Kalendoriaus naujinimas](./media/13UpdateCalendar.png)

9. Eikite į **Parametrai** > **Kalendoriaus šablonas** ir pasirinkite **Naujas**.
 
 ![Kalendoriaus šablonai](./media/14CalendarTemplates.png)
 
 10. Įveskite pavadinimą, pasirinkite sukurtą šablono išteklių, tada pasirinkite **Įrašyti**. 
 
 ![Kalendoriaus šablono įrašymas](./media/15SaveCalendarTemplate.png)
 
 11. Eikite į **Parametrai** ir dukart spustelėkite įrašą. 
 
 ![Projekto parametrai](./media/16ProjectParameters.png)
 
12. Atnaujinkite toliau nurodytus laukus:

 - **Numatytoji įmonė**: USPM
 - **Numatytasis organizacinis vienetas**: „Contoso Robotics Global“
 - **Sąskaitų faktūrų dažnumas**: septintoji diena ir paskutinė diena
 - **Darbo valandų šablonas**: pakeiskite į savo sukurtą šabloną.

13. Pasirinkite **Įrašyti**. 

![Projekto parametrai atnaujinti](./media/17UpdatedProjectParameters.png)
