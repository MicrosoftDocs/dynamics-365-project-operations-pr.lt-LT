---
title: Demonstracinės sąrankos ir konfigūracijos duomenų taikymas – „Lite“ versija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip taikyti demonstracinius sąrankos ir konfigūravimo duomenis "Project Operations".
author: sigitac
ms.date: 01/27/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9a3a99c326b7ebbdfa859c3298b35e910af0eb2a
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410033"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations---lite"></a>Demonstracinės sąrankos ir konfigūracijos duomenų taikymas naudojant „Project Operations“ – „Lite“ versija 

_** „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą_



## <a name="prerequisites"></a>Būtinosios sąlygos

Prieš pradėdami konfigūraciją, turite turėti aplinką, Dataverse sukonfigūruotą Dynamics 365 Project Operations.


## <a name="instructions"></a>Instrukcijos

1. Atsisiųskite [pagrindinių duomenų paketą](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData-%20CE%20only.zip). 
2. Eikite į aplanką *ProjOpsSampleSetupData - CE only CMT* ir paleiskite vykdomą failą *DataMigrationUtility*.
3. „Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.

    ![Konfigūravimo perkėlimas.](./media/1ConfigurationMigration.png)

4. CMT vedlio 2 puslapyje pažymėkite **„Microsoft 365“** kaip **Visuotinio diegimo tipą**.
5. Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.
6. Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus, o tada pasirinkite **Prisijungti**.

   ![Prisijungimas prie konfigūracijos.](./media/2ConfigurationSignin.png)

7. 3 puslapyje iš nuomotojo organizacijų sąrašo pasirinkite į kurią organizaciją norite importuoti demonstracinius duomenis, o tada pasirinkite **Prisijungti**.
8. 4 puslapyje pasirinkite zip. failą *SampleSetupAndConfigData* nesupakuotame aplanke *ProjOpsSampleSetupData - CE only CMT*.

   ![Suglaudintas failas.](./media/3ZipFile.png)

   ![Pasirinkti failą.](./media/4SelectAFile.png)

9. Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.

   ![Importuoti duomenis.](./media/5ImportData.png)

10. Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių. Baigę importuoti uždarykite CMT vediklį. 
11. Patikrinkite savo organizacijos duomenis šiuose 18 objektų:

    -   Valiuta
    -   Paskyra
    -   Organizacijos vienetas
    -   Susisiekite
    -   Vienetas
    -   Vienetų grupė
    -   Kainoraštis
    -   Projekto parametrų kainoraštis 
    -   Sąskaitos faktūros dažnumas
    -   Rezervuojamų išteklių kategorija
    -   Operacijos kategorija
    -   Išlaidų kategorija
    -   Vaidmens kaina
    -   Operacijos kategorijos kaina
    -   Charakteristika
    -   Rezervuojamas išteklius
    -   Rezervuojamų išteklių kategorijos sąsaja
    -   Rezervuojamų išteklių charakteristika

    ![Importavimo užbaigimas.](./media/6CompleteImport.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
