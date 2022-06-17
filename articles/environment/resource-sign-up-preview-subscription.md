---
title: Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams
description: Šiame straipsnyje pateikiama informacija apie tai, kaip užsiprenumeruoti ir įdiegti "Project Operations", kad būtų galima iš naujo įdiegti / nekaupti pagrįstus scenarijus.
author: sigitac
ms.date: 07/02/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: fb196a50b4cb9e8533db52414e8536d77a30e425
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920116"
---
# <a name="sign-up-for-project-operations-preview-subscriptions-for-resource-non-stocked-scenarios"></a>Prisiregistravimas norint gauti „Project Operations“ peržiūros versijos prenumeratą, skirtą ištekliais / ne atsargomis pagrįstiems scenarijams

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_



Šiame straipsnyje paaiškinama, kaip užsiprenumeruoti bandomąjį pasiūlymą ir įdiegti "Project Operations" aplinką, skirtą ištekliui / nekauptiems scenarijams.

## <a name="prerequisites"></a>Būtinosios sąlygos
- Vartotojas, kuris įdiegia peržiūros versiją, turi turėti „Azure“ kliento visuotinio administratoriaus teises. Pasinaudodami pirmuoju pasiūlymu, galite sukurti nuomotoją. 
- Norint diegti „Finance“ aplinką, reikia tinkamos „Azure“ prenumeratos, pagal kurią mokama už aplinką. Norėdami pradėti, galite naudoti esamą organizacijos prenumeratą arba naudoti [„Azure“ bandomąją versiją](https://azure.microsoft.com/free/). CDS aplinka bus pasiekiama nemokamai 30 dienų.

> [!IMPORTANT]
> Tik vienas asmuo, nuomotojo administratorius, organizacijoje turi atlikti šią užduotį. Jei nesate šio leidimo prenumeratorius, palaukite, kol jūsų organizacija bus užregistruota ir gausite vartotojo kredencialus.
> 
> Bandomosios versijos nuomotojuje yra vienkartinės. Bandomąją versiją galite paleisti tik vieną kartą. Bandomajai versijai rekomenduojame sukurti naują nuomotoją.


### <a name="dynamics-365-project-operations-ce---preview-trial"></a>„Dynamics 365 Project Operations“ (CE) – peržiūros bandomoji versija 

Prieš pradėdami įsitikinkite, kad esate prisijungę prie naršyklės naudodami vartotojo darbo klientą nuomotojuje, kuriame norite atlikti „Project Operations“ peržiūrą.

1. Pirmąjį pasiūlymo kodą – **„Dynamics 365 Project Operations“** – panaudokite čia: [„Project Operations“ bandomoji versija](https://aka.ms/try-po).
2. Patvirtinkite užsakymą.

  Pamatysite sėkmingai panaudotą patvirtinimo pasiūlymą.

### <a name="dynamics-365-finance-preview-trial"></a>Dynamics 365 Finance peržiūros bandomoji versija

Eikite į [„Dynamics 365 for Finance“ peržiūros bandomoji versija](https://aka.ms/trypoche) ir pakartokite ankstesnio skyriaus veiksmus su pasiūlymu Registracija norint naudoti debesyje esančią aplinką.  

## <a name="assign-licenses"></a>Licencijų priskyrimas

> [!IMPORTANT]
> Norint atlikti toliau nurodytus veiksmus jums reikės administratoriaus prieigos prie organizacijos „Microsoft 365“ portalo.

1. Eikite į [Microsoft 365 administravimo centrą](https://portal.office.com/), kad priskirtumėte licencijas savo vartotojams.

2. Puslapyje **Aktyvūs vartotojai** pasirinkite vartotojus, kuriems norite priskirti licenciją.

3. Patikrinkite, ar pasirinkta **„Dynamics 365 Project Operations“** licencija, ir pasirinkite **Įrašyti keitimus**.

> [!NOTE]
> „Finance“ bandomosios versijos pasiūlymo nereikia priskirti vartotojui.

## <a name="start-a-new-project-in-lcs"></a>Pradėkite naują LCS projektą

Sukurkite naują LCS projektą, kaip aprašyta straipsnyje, [Pradėkite naują projektą LCS](create-lcs-project.md)

## <a name="add-an-azure-subscription-to-an-lcs-project"></a>„Azure“ prenumeratos įtraukimas į LCS projektą

Norėdami atlikti šią užduotį, atlikite straipsnyje ["Įtraukti "Azure" prenumeratą į LCS projektą](resource-add-azure-subscription-lcs-project.md).

## <a name="deploy-finance-demo-environment-with-project-operations-for-resourcenon-stocked-scenarios"></a>„Finance“ demonstracinės aplinkos ir „Project Operations“, skirtos ištekliais / ne atsargomis pagrįstiems scenarijams, visuotinis diegimas

Vadovaukitės straipsnio "Naujos aplinkos [parengimas, kad būtų užbaigtas diegimas"](resource-provision-new-environment.md) pateiktomis gairėmis. Naudokite [demonstracinės aplinkos](/dynamics365/fin-ops-core/dev-itpro/deployment/deploy-demo-environment) visuotinio diegimo tipą, skirtą peržiūros versijai. 

## <a name="install-cds-setup-and-configuration-data"></a>CDS sąrankos ir konfigūracijos duomenų diegimas

Įdiekite CDS sąrankos ir konfigūravimo duomenis, [kaip aprašyta straipsnyje Nustatyti ir taikyti konfigūracijos duomenis Common Data Service](resource-apply-pro-setup-config-data.md).
Šį veiksmą atlikite tik įdiegę „Finance“ demonstracinę aplinką ir parengę demonstracinius duomenis.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
