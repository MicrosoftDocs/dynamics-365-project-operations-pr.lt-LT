---
title: „Azure“ prenumeratos įtraukimas į LCS projektą
description: Šioje temoje pateikta informacija apie tai, kaip prijungti „Azure“ prenumeratą prie LCS projekto.
author: sigitac
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: ad1ddd69cbb8db7780b8277a7ed7533d3ea3d053
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5289919"
---
# <a name="add-an-azure-subscription-to-an-lcs-project"></a>„Azure“ prenumeratos įtraukimas į LCS projektą

_**Taikoma:** „Project Operations“, skirta ištekliais / atsargose nelaikomomis prekėmis pagrįstiems scenarijams_

Naudojant esamą „Azure“ prenumeratą būtina įdiegti debesyje esančią aplinką. Šioje temoje paaiškinta, kaip prijungti esamą „Azure“ prenumeratą prie LCS projekto. 

## <a name="grant-admin-consent"></a>Administratoriaus sutikimo davimas

1. Savo LCS projekte, skyriuje **Aplinkos**, pasirinkite **„Microsoft Azure“ parametrai**.

![„Microsoft Azure“, parametrai](./media/1MicrosoftAzureSettings.png)

2. Puslapyje **Projekto parametrai**, skirtuke **„Azure“ jungtys** pažymėkite **Leisti**. Taip leidžiama aplinkas įdiegti į šį projektą.

![„Azure” jungtys](./media/2AzureConnectors.png)

3. Dar kartą pasirinkite **Leisti**, kad būtų duotas administratoriaus sutikimas.

![Administratoriaus sutikimo davimas](./media/3GrantAdminConsent.png)

4. Sutikite su teisių užklausa.

![Sutikite su teisių užklausa](./media/4AcceptPermissionRequest.png)

Dabar autorizavimas baigtas. 

![Sėkmingas leidimas](./media/5AuthorizationComplete.png)

## <a name="provide-dynamics-deployment-services-access-to-your-azure-subscription"></a><a name="provide"></a>„Dynamics Deployment Services“ prieigos prie jūsų „Azure“ prenumeratos suteikimas

1. Eikite į [„Microsoft Azure“ atsiskaitymas](https://portal.azure.com/#blade/Microsoft\_Azure\_Billing/SubscriptionsBlade) ir pasirinkite savo prenumeratą. „Dynamics Deployment Services“ reikia pasiekti šią prenumeratą, kad būtų galima visuotinai diegti aplinkas.

![„Azure“ prenumeratos informacija](./media/6AzureSubscription.png)

2. Naršymo srityje pasirinkite **Prieigos valdymas (IAM)**, tada pažymėkite **Įtraukti vaidmens priskyrimą**.
3. Dešinėje pusėje esančiame slankiklyje pasirinkite **Dalyvio vaidmuo**, pateiktame sąraše raskite ir pažymėkite **Dynamics Deployment Services**. 
4. Pasirinkite **Įrašyti**.

![Prenumeratos prieiga](./media/7SubscriptionAccess.png)

### <a name="add-a-subscription-connector-to-an-lcs-project"></a>Įtraukti prenumeratos jungtį į LCS projektą

1. Savo LCS projekto puslapyje **„Microsoft Azure“ parametrai** pasirinkite **Įtraukti**, kad įtrauktumėte naują jungtį.
2. Įveskite savo „Azure“ prenumeratos ID. Savo „Azure“ prenumeratos ID galite rasti [„Azure“ portale](https://ms.portal.azure.com/) dalyje **Parametrai** apatiniame kairiajame ekrano kampe.
3. Lauke **Konfigūruoti naudoti „Azure Resource Manager“** pasirinkite **Taip**.
4. Įsitikinkite, kad „Azure“ prenumeratos AAD nuomotojo domenas atitinka domeno „Azure“ prenumeratą, kurią naudojate, ir pažymėkite **Kitas**.
5. Ekrane **„Microsoft Azure“ sąranka** pasirinkite **Kitas**, kad patvirtintumėte. Jei šiame ekrane įvyksta klaida, grįžkite į skyrių [„Dynamics Deployment Services“ prieigos prie jūsų „Azure“ prenumeratos suteikimas](#provide)ir įsitikinkite, kad atlikote visus veiksmus.
6. Atsisiųskite „Azure Management Certificate“ į vietinį aplanką savo kompiuteryje, tada įkelkite jį į „Azure Management Portal“ įėję į **Parametrai** > **Valdymo sertifikatai**. Šis sertifikatas leis LCS užmegzti ryšį su „Azure“ jūsų vardu. Šį veiksmą galite praleisti, jei jūsų vartotojas turi prieigą prie prenumeratos.
7. Pasirinkite **Toliau**.
8. Pažymėkite „Azure“ regioną, skirtą visuotinai diegti, ir pasirinkite duomenų centrą, esantį netoli tos sistemos, kurią ketinate naudoti.
9.  Pasirinkite **Prisijungti**.

Sėkmingai prisijungėte prie „Azure“ prenumeratos. Dabar galite įdiegti „Dynamics 365 Finance“ debesyje veikiančias aplinkas.




[!INCLUDE[footer-include](../includes/footer-banner.md)]