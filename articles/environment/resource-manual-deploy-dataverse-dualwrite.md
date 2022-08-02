---
title: Visuotinis „Project Operations“ „Dataverse“ programos su dvigubo rašymo palaikymu diegimas rankiniu būdu
description: Šiame straipsnyje paaiškinama, kaip rankiniu būdu įdiegti programą "Project Operations Dataverse ", kad ji palaikytų dvigubą rašymą.
author: stsporen
ms.date: 06/18/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a25e2a59f1c069057c6689825ce52b13d842af71
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028574"
---
# <a name="manually-deploy-the-project-operations-dataverse-app-with-dual-write-support"></a>Visuotinis „Project Operations“ „Dataverse“ programos su dvigubo rašymo palaikymu diegimas rankiniu būdu

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Šiame straipsnyje paaiškinama, kaip rankiniu būdu įdiegti "Microsoft"Dynamics 365 Project Operations Microsoft Dataverse, kad ji palaikytų dvigubą rašymą. „Project Operations“ aptinka aplinkos konfigūraciją ir įtraukia papildomą dvigubo rašymo palaikymą, jei tenkinamos būtinosios sąlygos.

Diegdami per Microsoft Dynamics "Lifecycle Services" (LCS), jei vykdėte šiame straipsnyje pateiktas instrukcijas, galite praleisti integravimo (anksčiau vadinto aplinka) diegimą Microsoft Power Platform Common Data Service.

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
6. Patvirtinkite kalbą ir patvirtinkite, kad valiuta atitinka jūsų finansų ir operacijų programų valiutą.
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

Dataverse Įdiegę aplinką, galite nustatyti nuorodą savo finansų ir operacijų programose. Atlikite veiksmus, nurodytus dalyje [Aplinkų susiejimas naudojant dvigubo rašymo vedlį](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/link-your-environment).
