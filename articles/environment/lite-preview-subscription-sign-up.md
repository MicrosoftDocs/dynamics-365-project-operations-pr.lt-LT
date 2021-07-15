---
title: Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip prenumeruoti ir diegti „Project Operations Lite“ visuotinį diegimą – sandoris į išankstinės sąskaitos faktūros formą.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2b5a65f5e29915c349d40400ebbf3e4923b36a67
ms.sourcegitcommit: 52b26950bb3b1596ad81aa4ff91745ee9615d1b0
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/02/2021
ms.locfileid: "6334792"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija 

Šioje temoje paaiškinama, kaip užsiprenumeruoti bandomajam pasiūlymui ir įdiegti „Dynamics 365 Project Operations“ „Lite“ įdiegtį – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo.

> [!NOTE]
> Šis procesas pasikeis būsimuose „Project Operations“ leidimuose.

## <a name="prerequisites"></a>Būtinosios sąlygos
- Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises. Pasinaudodami pirmuoju pasiūlymu, galite sukurti nuomotoją.

> [!IMPORTANT]
> Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį. Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.
> 
> Bandomosios versijos nuomotojuje yra vienkartinės. Bandomąją versiją galite paleisti tik vieną kartą. Bandomajai versijai rekomenduojame sukurti naują nuomotoją.

### <a name="dynamics-365-project-operations-trial"></a>„Dynamics 365 Project Operations“ bandomoji versija 

Prieš pradėdami įsitikinkite, kad esate prisijungę prie naršyklės naudodami vartotojo darbo klientą nuomotojuje, kuriame norite atlikti „Project Operations“ peržiūrą.

1. Eikite į [„Project Operations“ bandomoji versija](https://aka.ms/try-po), kad panaudotumėte pirmąjį pasiūlymo kodą – **„Dynamics 365 Project Operations“**.
2. Patvirtinkite užsakymą.

  Pamatysite, kad patvirtinimo pasiūlymu sėkmingai pasinaudota.

## <a name="assign-licenses"></a>Licencijų priskyrimas

> [!IMPORTANT]
> Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365 Portal“.


1. Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas vartotojams.
2. Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.
3. Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“** licencija. 
4. Pasirinkite **Įrašyti pakeitimus**.

## <a name="create-a-new-dataverse-environment"></a>Naujos „Dataverse” aplinkos kūrimas

1. Parenkite naują „Project Operations“ „Dataverse“ visuotinio diegimo aplinką sekdami šioje temoje pateiktas instrukcijas – [„Dataverse“ visuotinio diegimo modelis](lite-deployment.md). Pasirinkę aplinkos tipą įsitikinkite, kad naudojate **bandomąją versiją (prenumeratos pagrindu)**.

  ![Nauja aplinka](./media/19CreateEnvironment.png)

2. Pasirinkite nustatymą **Įjungti „Dynamics 365“ programėles** ir palikite lauką **Automatiškai diegti šias programėles** tuščią.  
3. Norėdami sukurti aplinką, pasirinkite **Įrašyti**.

  ![Įtraukti duomenų bazę](./media/20CreateEnvironment1.png)

4. Sukūrę aplinką įdiekite **„Microsoft Dynamics 365 Project Operations“** sprendimą. 

![Sprendimo diegimas](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS konfigūracijos ir sąrankos demonstracinių duomenų diegimas

Įdiekite CDS konfigūraciją ir nustatykite demonstracinius duomenis vadovaudamiesi šioje temoje pateikiamomis instrukcijomis – [Demonstracinės sąrankos ir konfigūravimo duomenų taikymas](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
