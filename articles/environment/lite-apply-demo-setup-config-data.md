---
title: Demonstracinės sąrankos ir konfigūracijos duomenų taikymas
description: Šioje temoje pateikta informacija apie tai, kaip taikyti demonstracinę sąranką ir konfigūracijos programai „Project Operations“.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 42e02f393e89d20b2a462645f519a3792bee8f2f
ms.sourcegitcommit: b9d8bf00239815f31686e9b28998ac684fd2fca4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/02/2020
ms.locfileid: "3948977"
---
# <a name="apply-demo-setup-and-configuration-data-for-project-operations-lite-deployment---deal-to-proforma-invoicing"></a>Demonstracinės sąrankos ir konfigūracijos duomenų taikymas „Project Operations“ programos „lite“ visuotiniam diegimui – sandoris į išankstinės sąskaitos faktūros formą

_** „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą_

1. Atsisiųskite [pagrindinių duomenų paketą](https://download.microsoft.com/download/3/4/1/341bf279-a64f-4baa-af31-ce624859b518/ProjOpsSampleSetupData%20-%20CE%20only%20CMT.zip). 
2. Eikite į aplanką *ProjOpsDemoDataSetupAndMaster - Integrated CMT* ir vykdykite vykdomą failą *DataMigrationUtility*.
3. „Common Data Service“ konfigūravimo perkėlimo (CMT) vedlio 1 puslapyje pasirinkite **Importuoti duomenis**, o tada pasirinkite **Tęsti**.

![Konfigūravimo perkėlimas](./media/1ConfigurationMigration.png)

4. CMT vedlio 2 puslapyje pažymėkite **„Office 365“** kaip **Visuotinio diegimo tipą**.
5. Pažymėkite žymės langelius **Rodyti galimų organizacijų sąrašą** ir **Rodyti išsamiau**.
6. Pasirinkite savo nuomotojo regioną, įveskite savo kredencialus, o tada pasirinkite **Prisijungti**.

![Prisijungimas prie konfigūracijos](./media/2ConfigurationSignin.png)

7. 3 puslapyje iš nuomotojo organizacijų sąrašo pasirinkite į kurią organizaciją norite importuoti demonstracinius duomenis, o tada pasirinkite **Prisijungti**.
8. 4 puslapyje pasirinkite suglaudintą failą *MasterAndSetupData*, esantį išpakuotame aplanke *ProjOpsDemoDataSetupAndMaster - Integrated CMT*.

![Suglaudintas failas](./media/3ZipFile.png)

![Pasirinkite failą](./media/4SelectAFile.png)

9. Pasirinkę suglaudintą failą, pasirinkite **Importuoti duomenis**.

![Importuoti duomenis](./media/5ImportData.png)

10. Priklausomai nuo jūsų tinklo spartos, importavimas užims apie 2-10 minučių. Baigę importuoti uždarykite CMT vediklį. 
11. Patikrinkite savo organizacijos duomenis šiuose 20 objektų:

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
- Sąskaitos faktūros dažnumo informacija
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
