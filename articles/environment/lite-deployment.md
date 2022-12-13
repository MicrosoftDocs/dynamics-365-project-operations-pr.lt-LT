---
title: "\"Project Operations Lite\" diegimas"
description: Šiame straipsnyje pateikta informacija apie tai, kaip įdiegti „Project Operations Lite“ visuotinį diegimą – sandoris į išankstinės sąskaitos faktūros formą.
author: stsporen
ms.date: 11/29/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 2c508f56b3018b6a86fea78bcf9ee4136e90f385
ms.sourcegitcommit: 38cb012502cbd640abbc21a0912b195112b27ccb
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/30/2022
ms.locfileid: "9810989"
---
# <a name="deploy-project-operations-lite"></a>"Project Operations Lite" diegimas

_**Taikoma:** „Lite“ visuotiniam diegimui – nuo sandorio iki išankstinės sąskaitos faktūros kūrimo_



Programoje „Project Operations“ palaikomi keli visuotinio diegimo modeliai. Norėdami nustatyti geriausią visuotinio diegimo modelį, žr. [Visuotinio diegimo tipus](determine-deployment-type.md).


> [!IMPORTANT]
> Šis visuotinis diegimas, „Lite“ visuotinis diegimas – sandoris į išankstinės sąskaitos faktūros formą – yra **„Dataverse“ vienintelio „Project Operations“ visuotinio diegimo** rezultatas.

- [„Project Operations“ diegimas į naują „Dataverse“ aplinką](#new)
- [Diegimas į esamą „Dataverse“ aplinką](#existing)
- [Diegimas esamoje Dataverse aplinkoje, kurioje yra dvigubo rašymo komponentai](#existingdw)



## <a name="install-project-operations-lite-to-a-new-dataverse-environment"></a><a name="new"></a>"Project Operations Lite" diegimas naujoje Dataverse aplinkoje

1. Kaip [visuotinis arba Power Platform administratorius](/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, kurkite naują „Dataverse“ aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com). Įsitikinkite, kad įjungta **Kurti duomenų bazę šiai aplinkai** ir **„Dynamics 365“ programos**. Norėdami gauti daugiau informacijos, žr. [Aplinkų kūrimas ir tvarkymas „Power Platform“ administravimo centre](/power-platform/admin/create-environment#create-an-environment-in-the-power-platform-admin-center).
1. Pasirinkite **Microsoft Dynamics 365 Project Operations** iš „Dynamics 365“ programų visuotinio diegimo sąrašo.


## <a name="install-project-operations-lite-to-an-existing-dataverse-environment"></a><a name="existing"></a>"Project Operations Lite" diegimas esamoje Dataverse aplinkoje 
1. Kaip [visuotinis arba „Power Platform“ administratorius](/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, raskite aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com), kur norite įdiegti „Project Operations“.
1. Įdiekite **Microsoft Dynamics 365 Project Operations** iš „Dynamics 365“ programų visuotinio diegimo sąrašo. Daugiau informacijos žr. [„Dynamics 365“ programų valdymas](/power-platform/admin/manage-apps).

## <a name="install-project-operations-lite-to-an-existing-dataverse-environment-where-dual-write-solutions-are-already-present"></a><a name="existingdw"></a> Įdiekite "Project Operations Lite" esamoje Dataverse aplinkoje, kurioje jau yra dvigubo rašymo sprendimai

Jei norite toliau vykdyti "Project Operations" supaprastintuoju diegimo režimu, turėtumėte atlikti šiuos veiksmus:

1. Kaip [visuotinis arba „Power Platform“ administratorius](/power-platform/admin/global-service-administrators-can-administer-without-license), turintis „Project Operations“ licenciją, raskite aplinką [„PowerPlatform“ administravimo centre](https://admin.powerplatform.com), kur norite įdiegti „Project Operations“.
1. Įdiekite **Microsoft Dynamics 365 Project Operations** iš „Dynamics 365“ programų visuotinio diegimo sąrašo. Daugiau informacijos žr. [„Dynamics 365“ programų valdymas](/power-platform/admin/manage-apps).
1. Kadangi jūsų aplinkoje yra dvigubo rašymo komponentų, kurie padeda integruoti į įdiegtas "Finance and Operations" programas, "Project Operations" diegimas taip pat įdiegs galimybes ir plėtinius, reikalingus su "Project" susijusiems duomenims integruoti į "finance and operations" programas. Kadangi norite vykdyti "Project Operations" naudodami "Lite" diegimą, šie integravimo komponentai turėtų būti pašalinti, nes jie sukurs "Lite" diegimo scenarijų apribojimus ir pridėtines išlaidas. Rankiniu būdu pašalinkite sprendimus **Dynamics 365 Project Operations Dual Write ir** Dual Write **Dynamics 365 Project Operations Entity Maps**, kad pašalintumėte šiuos komponentus.
1. Eikite į **Project Operations -> Settings -> Parameters**.  **Atidarykite puslapį Projekto parametro** informacija ir nustatykite **lauką Sprendimo naujinimo elgsena** į **Tik supaprastintas**. Taip užtikrinama, kad bet kokie vėlesni "Project Operations" naujinimai nesugrąžins integravimo komponentų į "Project Operations".  

[!INCLUDE[footer-include](../includes/footer-banner.md)]
