---
title: Visuotinis „Project Operations“ „Dataverse“ programos su dvigubo rašymo palaikymu diegimas rankiniu būdu
description: Šioje temoje paaiškinta, kaip rankiniu būdu visuotinai įdiegti „Project Operations“ „Dataverse“ programą, kad ji palaikytų dvigubą rašymą.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 06325a9a9f9084d1f506f2493c32565fe7b7c52ae6fe22c81339b9c1d632e688
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986456"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Visuotinis „Project Operations“ „Dataverse“ programos su dvigubo rašymo palaikymu diegimas rankiniu būdu

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šioje temoje paaiškinta, kaip rankiniu būdu į „Microsoft Dataverse“ visuotinai įdiegti „Microsoft Dynamics 365 Project Operations“, kad ji palaikytų dvigubą rašymą. „Project Operations“ aptinka aplinkos konfigūraciją ir įtraukia papildomą dvigubo rašymo palaikymą, jei tenkinamos būtinosios sąlygos.

Jei, visuotinai diegdami per „Microsoft Dynamics“ „Lifecycle Services“ (LCS), vadovavotės šioje temoje pateiktais nurodymais, galite praleisti visuotinį „Microsoft Power Platform“ integracijos (anksčiau vadintos „Common Data Service“ aplinka) diegimą.

„Project Operations“ visuotinio diegimo į „Dataverse“ procesas, kad ji palaikytų dvigubą rašymą, apima keturis pagrindinius veiksmus, nurodytus toliau.

1. [Naujos „Dataverse“ aplinkos, palaikančios dvigubą rašymą, sukūrimas](#create).
2. [Dvigubo rašymo būtinųjų sąlygų įraukimas į aplinką](#prerequisites).
3. [„Project Operations“ „Dataverse“ programos įtraukimas](#dataverse).
4. [Aplinkų susiejimas](#link).

## <a name="create-a-new-environment-in-dataverse-that-supports-dual-write"></a><a name="create"></a>Naujos „Dataverse“ aplinkos, palaikančios dvigubą rašymą, sukūrimas

Norėdami atlikti šią procedūrą, turite prisijungti kaip administratorius.

1. Atidarykite [„Power Platform“ administravimo centrą](https://admin.powerplatform.com) ir prisijunkite kaip administratorius.
2. Sukurkite naują aplinką ir ją pavadinkite.
3. Pasirinkite aplinkos tipą. Jei užsiregistravote naudoti bandomosios versijos pasiūlymą, pasirinkite **Bandomoji versija (pagrįsta prenumerata)**.
4. Patvirtinkite visuotinio diegimo regioną.
5. Įjunkite parinktį **Kurti duomenų bazę šiai aplinkai**. 
6. Patvirtinkite kalbą, tada patvirtinkite, kad valiuta atitinka jūsų „Finance and Operations“ programų valiutą.
7. Įjunkite parinktį **„Dynamics 365“ programos** ir patvirtinkite, kad laukas **Automatiškai visuotinai diegti šias programas** nustatytas kaip **Nėra**.
8. Jei reikia saugos grupės, ją įtraukite.
9. Norėdami sukurti aplinką, pasirinkite **Įrašyti**.
10. Palaukite, kol visuotinis diegimas bus baigtas, o aplinka pasieks būseną **Paruošta**.

## <a name="add-dual-write-prerequisites-to-the-environment"></a><a name="prerequisites"></a>Dvigubo rašymo būtinųjų sąlygų įraukimas į aplinką

Dvigubo rašymo palaikymas apima papildomus laukus, įtrauktus į pagrindinius objektus, pvz., objektą **Įmonė**. Jei dvigubo rašymo palaikymą įtraukiate į esamą aplinką, gali reikėti atnaujinti duomenis, kad būtų galimas palaikymas. Informacijos apie tai, kaip perkrauti duomenis, ieškokite dalyje [Įmonės duomenų perkrovimas](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/bootstrap-company-data). Daugiau informacijos apie dvigubą rašymą žr. dalyje [Dvigubo rašymo sistemos reikalavimai](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-system-req).

Atlikite šią procedūrą norėdami į savo aplinką įtraukti dvigubo rašymo būtinąsias sąlygas.

1. Atidarykite ką tik sukurtą aplinką, tada eikite į **Išteklius** \> **„Dynamics 365“ programos**.
2. Programų sąraše pasirinkite **Pagrindinis dvigubo rašymo sprendimas** ir jį įdiekite.
3. Palaukite, kol diegimas bus baigtas. Tada programų sąraše pasirinkite **Dvigubo rašymo programos tvarkymo sprendimas** ir jį įdiekite.

## <a name="add-the-project-operations-dataverse-app"></a><a name="dataverse"></a>„Project Operations“ „Dataverse“ programos įtraukimas

Šią procedūrą galite atlikti, tik jei prieš diegdami „Project Operations“ atlikote ankstesnes procedūras. Vykstant diegimui sistema analizuoja aplinkos konfigūraciją ir įtraukia dvigubo rašymo palaikymą, jei to reikia.

1. Atidarykite anksčiau sukurtą aplinką, tada eikite į **Išteklius** \> **„Dynamics 365“ programos**.
2. Programų sąraše pasirinkite **„Microsoft Dynamics 365 Project Operations“** ir ją įdiekite.

## <a name="link-your-environments"></a><a name="link"></a>Aplinkų susiejimas

Įdiegę „Dataverse“ aplinką, galite nustatyti saitą savo „Finance and Operations“ programose. Atlikite veiksmus, nurodytus dalyje [Aplinkų susiejimas naudojant dvigubo rašymo vedlį](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
