---
title: Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams
description: Šioje temoje pateikiama informacijos, kaip užsiprenumeruoti ir įdiegti „Project Operations“, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.
author: sigitac
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7a03f021b1ae0a87dfc947976b8a16c8246e1684
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080722"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje aiškinama, kaip užsiprenumeruoti peržiūros versijos / partnerio pasiūlymą ir visuotinai įdiegti „Project Operations“ aplinką, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams.

## <a name="prerequisites"></a>Būtinosios sąlygos

- Gausite el. laišką, kviečiantį išbandyti peržiūros versiją. Galite pateikti užklausą dėl peržiūros versijos [„Project Operations“ svetainėje](https://dynamics.microsoft.com/en-us/project-operations/overview/).
- Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises.
- Norint diegti „Finance“ aplinką, reikia tinkamos „Azure“ prenumeratos, pagal kurią mokama už aplinką. Norėdami pradėti, galite naudoti esamą organizacijos prenumeratą arba naudoti [„Azure“ bandomąją versiją](https://azure.microsoft.com/en-us/free/). CDS aplinka bus pasiekiama nemokamai 30 dienų.

## <a name="subscribe"></a>Prenumeruoti

Patvirtinus jūsų [peržiūros versijos užklausą](https://forms.office.com/FormsPro/Pages/ResponsePage.aspx?id=v4j5cvGGr0GRqy180BHbR56j8lZs0FdAvwT75_WNFyxUMkRDV1NYQU5TNjE2VjhKOVBUNVg2R0s1NC4u), el. paštu gausite iš „Microsoft“ tris pasiūlymus. Šie pasiūlymai leidžia visuotinai įdiegti „Project Operations“ peržiūros versiją:

- „Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija
- „Office 365 Project Operations“ – bandomoji peržiūros versija
- „Dynamics 365 Finance“ – bandomoji peržiūros versija

> [!IMPORTANT]
> Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį. Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.

### <a name="dynamics-365-project-operations-crm---preview-trial"></a>„Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija 

Prieš pradėdami įsitikinkite, kad esate prisijungę prie naršyklės naudodami vartotojo darbo klientą nuomotojuje, kuriame norite atlikti „Project Operations“ peržiūrą.

1. Pasinaudokite pirmuoju pasiūlymo kodu **„Dynamics 365 Project Operations“ (CRM) – bandomoji peržiūros versija** , įklijuodami jį į naršyklės URL lauką.

![Pasinaudoti pasiūlymu](./media/16RedeemFirstOfferNew.png)

2. Patvirtinkite užsakymą.

![Patvirtinkite užsakymą](./media/17ConfirmOrderNew.png)

Pamatysite sėkmingai panaudotą patvirtinimo pasiūlymą.

![Patvirtinimas](./media/18OrderConfirmationNew.png)

### <a name="office-365-project-operations---preview-trial"></a>„Office 365 Project Operations“ – bandomoji peržiūros versija

Pakartokite veiksmus, kaip ir taikydami pirmąjį pasiūlymo kodą. Būtinai įtraukite antrą pasiūlymo kodą, naudodami tą patį vartotojo klientą, kuris buvo naudojamas su pirmuoju pasiūlymo kodu.

### <a name="dynamics-365-finance-preview-trial"></a>„Dynamics 365 Finance“ bandomoji peržiūros versija

Pakartokite tuos pačius veiksmus su paskutiniu pasiūlymu, esančiu pasveikinimo el. laiške.

## <a name="assign-licenses"></a>Licencijų priskyrimas

> [!IMPORTANT]
> Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365 Portal“.

1. Eikite į [„Microsoft 365“ administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas vartotojams.

![Administravimo centro pagrindinis puslapis](./media/14AdminPortal.png)

2. Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.

![Licencijų priskyrimas](./media/15AssignLicenses.png)

3. Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“ (CRM) peržiūros versijos** ir **„Office 365 Project Operations“ – peržiūros versijos** licencija, tada pasirinkite **Išsaugoti pakeitimus**.

> [!NOTE]
> „Finance“ bandomosios versijos pasiūlymo nereikia priskirti vartotojui.

## <a name="start-a-new-project-in-lcs"></a>Pradėkite naują LCS projektą

Sukurkite naują LCS projektą, kaip aprašytą temoje [Naujo LCS projekto pradėjimas](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>„Azure“ prenumeratos įtraukimas į LCS projektą

Norėdami atlikti šią užduotį, atlikite veiksmus, nurodytus temoje [„Azure“ prenumeratos įtraukimas į LCS projektą](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>„Finance“ demonstracinės aplinkos ir „Project Operations“, skirtos ištekliais / ne atsargomis pagrįstiems scenarijams, visuotinis diegimas

Vadovaukitės nurodymais, pateiktais temoje [Naujos aplinkos parengimas](resource-provision-new-environment.md), kad užbaigtumėte visuotinį diegimą. Naudokite [demonstracinės aplinkos](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) visuotinio diegimo tipą, skirtą peržiūros versijai. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS sąrankos ir konfigūracijos duomenų diegimas

Įdiekite CDS sąrankos ir konfigūracijos duomenis, kaip aprašyta temoje [Konfigūracijos duomenų nustatymas ir taikymas sistemoje „Common Data Service“](resource-apply-pro-setup-config-data.md).
Atlikite šį veiksmą tik tada, kai įdiegiama „Finance“ demonstracinė aplinka ir demonstraciniai duomenys yra paruošti FO.
