---
title: Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija
description: Šioje temoje pateikta informacija apie tai, kaip prenumeruoti ir diegti „Project Operations Lite“ visuotinį diegimą – sandoris į išankstinės sąskaitos faktūros formą.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 44edf2613ea4b26dadbd9edc47c784c488c577de
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290054"
---
# <a name="sign-up-for-a-preview-subscription---lite"></a>Registracija norint gauti peržiūros versijos prenumeratą – „Lite“ versija 

Šioje temoje paaiškinamaa, kaip užsiprenumeruoti peržiūros versijos partnerio pasiūlymą ir įdiegti „Dynamics 365 Project Operations Lite“ visuotinį diegimą – sandoris į išankstinės sąskaitos faktūros formą.

> [!NOTE]
> Šis procesas pasikeis būsimuose „Project Operations“ leidimuose.

## <a name="prerequisites"></a>Būtinosios sąlygos

- Gausite el. laišką, kviečiantį išbandyti peržiūros versiją. Galite pateikti užklausą dėl peržiūros versijos [„Project Operations“ svetainėje](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises.
- Peržiūrėkite visus terminus ir sąlygas.

## <a name="subscribe"></a>Prenumeruoti

Gavę [peržiūros versijos užklausos](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u) patvirtinimą, el. paštu iš „Microsoft“ gausite du pasiūlymus. Šie pasiūlymai leidžia visuotinai įdiegti „Project Operations“ peržiūros versiją:

- „Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija
- „Office 365 Project Operations“ – bandomoji peržiūros versija

> [!IMPORTANT]
> Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį. Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>„Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija 

Prieš pradėdami įsitikinkite, kad esate prisijungę prie naršyklės naudodami vartotojo darbo klientą nuomotojuje, kuriame norite atlikti „Project Operations“ peržiūrą.

1. Panaudokite pirmąjį pasiūlymo kodą, skirtą **„Dynamics 365 Project Operations“ (CRM) – bandomajai peržiūros versijai**, įklijuodami jį į naršyklės URL.

![Pasinaudoti pasiūlymu](./media/16RedeemFirstOfferNew.png)

2. Patvirtinkite užsakymą.
![Patvirtinkite užsakymą](./media/17ConfirmOrderNew.png)

Pamatysite sėkmingai panaudotą patvirtinimo pasiūlymą.

![Patvirtinimas](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>„Office 365 Project Operations“ – bandomoji peržiūros versija

Pakartokite veiksmus, kaip ir taikydami pirmąjį pasiūlymo kodą. Būtinai įtraukite antrą pasiūlymo kodą, naudodami tą patį vartotojo klientą, kuris buvo naudojamas su pirmuoju pasiūlymo kodu.

## <a name="assign-licenses"></a>Licencijų priskyrimas

> [!IMPORTANT]
> Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365 Portal“.


1. Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas vartotojams.

![Administravimo centro pagrindinis puslapis](./media/14AdminPortal.png)

2. Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.

![Licencijų priskyrimas](./media/15AssignLicenses.png)

3. Patikrinkite, ar pažymėtos **„Dynamics 365 Project Operations“ (CRM) peržiūros versija** ir **„Office 365 Project Operations“ – peržiūros versija** licencijos. 
4. Pasirinkite **Įrašyti pakeitimus**.

## <a name="create-a-new-cds-environment"></a>Naujos CDS aplinkos kūrimas

1. Parenkite naują „Project Operations“ CDS visuotinio diegimo aplinką sekdami šioje temoje pateiktas instrukcijas – [CDS visuotinio diegimo modelis](lite-deployment.md). Pasirinkę aplinkos tipą įsitikinkite, kad naudojate **bandomąją versiją (prenumeratos pagrindu)**.
![Nauja aplinka](./media/19CreateEnvironment.png)

2. Pasirinkite nustatymą **Įjungti „Dynamics 365“ programėles** ir palikite lauką **Automatiškai diegti šias programėles** tuščią.  
3. Norėdami sukurti aplinką, pasirinkite **Įrašyti**.

![Įtraukti duomenų bazę](./media/20CreateEnvironment1.png)

4. Sukūrę aplinką įdiekite **„Microsoft Dynamics 365 Project Operations“** sprendimą. 

![Sprendimo diegimas](./media/21InstallSolution.png)

## <a name="install-a-cds-configuration-and-setup-demo-data"></a>CDS konfigūracijos ir sąrankos demonstracinių duomenų diegimas

Įdiekite CDS konfigūraciją ir nustatykite demonstracinius duomenis vadovaudamiesi šioje temoje pateikiamomis instrukcijomis – [Demonstracinės sąrankos ir konfigūravimo duomenų taikymas](lite-apply-demo-setup-config-data.md).


[!INCLUDE[footer-include](../includes/footer-banner.md)]