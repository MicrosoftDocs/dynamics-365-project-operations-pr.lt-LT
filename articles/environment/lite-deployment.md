---
title: „Project Operations“ visuotinis diegimas – „Lite“ versija
description: Šiame straipsnyje pateikiama informacija apie tai, kaip įdiegti "Project Operations lite" diegimą - spręsti proforma SF išrašymo problemą.
author: stsporen
ms.date: 02/28/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 86293b725e86db3d4b8bdaf5810b16b7c670e8a3
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8930328"
---
# <a name="deploy-project-operations---lite"></a>„Project Operations“ visuotinis diegimas – „Lite“ versija

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_



Programoje „Project Operations“ palaikomi keli visuotinio diegimo modeliai. Norėdami nustatyti geriausią visuotinio diegimo modelį, žr. [Visuotinio diegimo tipus](determine-deployment-type.md).


> [!IMPORTANT]
> Šis visuotinis diegimas, „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą – yra **„Dataverse“ vienintelio „Project Operations“ visuotinio diegimo** rezultatas.

- [Projekto operacijų diegimas naujoje Dataverse aplinkoje](#new)
- [Diegti esamoje Dataverse aplinkoje](#existing)



## <a name="install-project-operations-to-a-new-dataverse-environment"></a><a name="new"></a> Projekto operacijų diegimas naujoje Dataverse aplinkoje

1. Kaip visuotinis arba administratorius [, turintis "Project Operations" licenciją, sukurkite Power Platform naują](/power-platform/admin/global-service-administrators-can-administer-without-license) aplinką "PowerPlatform" administravimo centre Dataverse.[...](https://admin.powerplatform.com) Įsitikinkite, kad **šios aplinkos** duomenų bazės kūrimas ir **įgalintos "Dynamics 365" programos**. Norėdami gauti daugiau informacijos, žr. [Aplinkų kūrimas ir tvarkymas „Power Platform“ administravimo centre](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
2. Pasirinkite **Microsoft Dynamics 365 Project Operations** iš „Dynamics 365“ programų visuotinio diegimo sąrašo.


## <a name="install-project-operations-to-an-existing-dataverse-environment"></a><a name="existing"></a> Diegti projekto operacijas esamoje Dataverse aplinkoje
1. Įsitikinkite, kad aplinka nesukonfigūruota naudojant dvigubą rašymą [, nes diegimas įdiegs](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-overview) išteklių / nekauptų scenarijų galimybių projekto operacijas [.](project-operations-integrated-deployment-overview.md)
2. Kaip [visuotinis arba „Power Platform“ administratorius](/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, raskite aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com), kur norite įdiegti „Project Operations“.
3. Įdiekite **Microsoft Dynamics 365 Project Operations** iš „Dynamics 365“ programų visuotinio diegimo sąrašo. Daugiau informacijos žr. [„Dynamics 365“ programų valdymas](/power-platform/admin/manage-apps).




[!INCLUDE[footer-include](../includes/footer-banner.md)]
