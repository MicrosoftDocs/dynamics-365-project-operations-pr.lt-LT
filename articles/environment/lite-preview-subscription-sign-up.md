---
title: Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip užsiprenumeruoti ir įdiegti "Project Operations lite" diegimą – spręsti proforma sąskaitų faktūrų išrašymą.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 29bf31cd1bc9c1c5ac757de989154b4c7acc53fe
ms.sourcegitcommit: 16c9eded66d60d4c654872ff5a0267cccae9ef0e
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/07/2022
ms.locfileid: "9410044"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija 

Šiame straipsnyje paaiškinama, kaip užsiprenumeruoti bandomąjį pasiūlymą ir įdiegti Dynamics 365 Project Operations supaprastintą diegimą - spręsti proforma sąskaitų faktūrų išrašymą.

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
> Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365“ portalo.


1. Eikite į [Microsoft 365 administravimo centrą](https://portal.office.com/) ir priskirkite licencijas savo vartotojams.
2. Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.
3. Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“** licencija. 
4. Pasirinkite **Įrašyti pakeitimus**.

## <a name="create-a-new-dataverse-environment"></a>Naujos „Dataverse” aplinkos kūrimas

1. Konfigūruokite naują "Project Operations" Dataverse diegimo aplinką vykdydami instrukcijas, pateiktas straipsnyje diegimo [Dataverse modelis](lite-deployment.md). Pasirinkę aplinkos tipą įsitikinkite, kad naudojate **bandomąją versiją (prenumeratos pagrindu)**.

  ![Nauja aplinka.](./media/19CreateEnvironment.png)

2. Pasirinkite nustatymą **Įjungti „Dynamics 365“ programėles** ir palikite lauką **Automatiškai diegti šias programėles** tuščią.  
3. Norėdami sukurti aplinką, pasirinkite **Įrašyti**.

  ![Įtraukti duomenų bazę.](./media/20CreateEnvironment1.png)

4. Sukūrę aplinką įdiekite **„Microsoft Dynamics 365 Project Operations“** sprendimą. 

![Sprendimo diegimas.](./media/21InstallSolution.png)

## <a name="set-up-demo-data"></a>Demonstracinių duomenų nustatymas

Nustatykite demonstracinius duomenis vadovaudamiesi straipsnyje ["Taikyti demonstracinius sąrankos ir konfigūravimo duomenis" pateiktomis instrukcijomis](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]
