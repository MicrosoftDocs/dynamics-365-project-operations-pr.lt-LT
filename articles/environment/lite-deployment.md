---
title: „Project Operations“ visuotinis diegimas – „Lite“ versija
description: Šiame straipsnyje pateikta informacija apie tai, kaip įdiegti „Project Operations Lite“ visuotinį diegimą – sandoris į išankstinės sąskaitos faktūros formą.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930328"
---
# <a name="deploy-project-operations---lite"></a>„Project Operations“ visuotinis diegimas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_



Programoje „Project Operations“ palaikomi keli visuotinio diegimo modeliai. Norėdami nustatyti geriausią visuotinio diegimo modelį, žr. [Visuotinio diegimo tipus](determine-deployment-type.md).


> [!IMPORTANT]
> Šis visuotinis diegimas, „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą – yra **„Dataverse“ vienintelio „Project Operations“ visuotinio diegimo** rezultatas.

- [„Project Operations“ diegimas į naują „Dataverse“ aplinką](#new)
- [Diegimas į esamą „Dataverse“ aplinką](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a>„Project Operations“ diegimas į nauja Dataverse aplinką

1. Kaip [visuotinis arba Power Platform administratorius](/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, kurkite naują „Dataverse“ aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com). Įsitikinkite, kad įjungta **Kurti duomenų bazę šiai aplinkai** ir **„Dynamics 365“ programos**. Norėdami gauti daugiau informacijos, žr. [Aplinkų kūrimas ir tvarkymas „Power Platform“ administravimo centre](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pasirinkite **Microsoft Dynamics 365 Project Operations** iš „Dynamics 365“ programų visuotinio diegimo sąrašo.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a>„Project Operations“ diegimas į esamą „Dataverse“ aplinką
1. Užtikrinkite, kad aplinka nebūtų konfigūruojama naudojant [dvigubą rašymą](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview), nes tuomet diegiant bus įdiegtos [„Project Operations“, skirtos išteklių / nelaikomų medžiagų scenarijams](project-operations-integrated-deployment-overview.md), galimybės.
2. Kaip [visuotinis arba „Power Platform“ administratorius](/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, raskite aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com), kur norite įdiegti „Project Operations“.
3. Įdiekite **Microsoft Dynamics 365 Project Operations** iš „Dynamics 365“ programų visuotinio diegimo sąrašo. Daugiau informacijos žr. [„Dynamics 365“ programų valdymas](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
