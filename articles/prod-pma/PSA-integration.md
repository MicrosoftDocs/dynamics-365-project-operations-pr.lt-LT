---
title: „Project Service Automation“ apžvalga
description: Šioje temoje pateikiama informacija apie „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“ integravimo sprendimą.
author: ruhercul
manager: AnnBe
ms.date: 07/25/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: ruhercul
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: ruhercul
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d9ccbb29d5035ea061d232011af87cef2c81e76c
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/25/2020
ms.locfileid: "4642463"
---
# <a name="project-service-automation-overview"></a>„Project Service Automation“ apžvalga

[!include[banner](../includes/banner.md)]
[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“ egzemplioriuose per „Common Data Service“. Integravimo šablonai, kuriuos galima naudoti su duomenų integravimo funkcija, leidžia vykdyti projektų, projektų sutarčių, projektų sutarčių eilučių, projektų sutarčių eilučių etapų, projektų užduočių, išlaidų operacijų kategorijų, valandų įvertinimo ir išlaidų įvertinimo srautą iš „Project Service Automation“ į „Finance“.

> [!NOTE]
> - Jei naudojate 7.3.0 versiją, turite įdiegti KB 4074835. Tada galėsite integruoti fiksuotos kainos projektus.
> - Jei naudojate 7.3.0 versiją ir norite įtraukti mokesčių operacijas iš „Project Service Automation“, turite įdiegti KB 4345320, kad įtrauktumėte šiuos mokesčius į projekto sąskaitą faktūrą.
> - Jei naudojate 8.0 versiją, galėsite naudoti projekto užduočių integravimą, išlaidų operacijų kategorijas, valandų įvertinimą, išlaidų įvertinimą ir funkcijų blokavimą.
> - Jei naudojate 8.0.1 arba naujesnę versiją, galėsite sinchronizuoti faktinius duomenis.

Kad galėtumėte integruoti „Project Service Automation“ ir „Finance“, turite sukonfigūruoti „Project Service Automation“ integravimo parametrus. Daugiau informacijos žr. skyriuje [„Project Service Automation“ integravimo parametrai](PSA-parameters.md).

Šis integravimo sprendimas leidžia tiesiogiai sinchronizuoti toliau pateikiamais atvejais.

- Saugokite projektų sutartis „Project Service Automation“ ir sinchronizuokite jas tiesiogiai iš „Project Service Automation“ į „Finance“.
- Kurkite projektus, naudodami „Project Service Automation“, ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.
- Saugokite projektų sutarčių eilutes „Project Service Automation“ ir sinchronizuokite jas tiesiogiai iš „Project Service Automation“ į „Finance“.
- Saugokite projektų sutarčių eilučių etapus „Project Service Automation“ ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.
- Saugokite projektų užduotis „Project Service Automation“ ir sinchronizuokite jas tiesiogiai iš „Project Service Automation“ į „Finance“.
- Saugokite išlaidų operacijų kategorijas „Finance“ ir sinchronizuokite jas tiesiogiai iš „Finance“ į „Project Service Automation“.
- Kurkite projektų valandų įvertinimus, naudodami „Project Service Automation“, ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.
- Kurkite projektų išlaidų įvertinimus, naudodami „Project Service Automation“, ir sinchronizuokite juos tiesiogiai iš „Project Service Automation“ į „Finance“.
- Kurkite projektų laiko, išlaidų ir mokesčių faktinius duomenis, naudodami „Project Service Automation“, ir kurkite projektų operacijas „Project Service Automation“ integravimo žurnale, kad jas būtų galima užregistruoti naudojant „Finance“.

## <a name="data-synchronization"></a>Duomenų sinchronizavimas

Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami vykdant integravimą tarp „Project Service Automation“ ir „Finance“.

> [!NOTE]
> Šiuo metu pasiekiami ne visi šablonai. Šablonai bus išleisti juos užbaigus.

[![„Project Service Automation“ ir „Finance“ integravimas](./media/PSA-integration.png)](./media/PSA-integration.png)

## <a name="system-requirements-for-finance"></a>„Finance“ sistemos reikalavimai

Norėdami naudoti „Project Service Automation“ į „Finance“ integravimo sprendimą, turite įdiegti „Enterprise edition“ 7.3 su 12 arba naujesnės versijos platforma.

## <a name="system-requirements-for-project-service-automation"></a>„Project Service Automation“ sistemos reikalavimai

Norėdami naudoti „Project Service Automation“ į „Finance“ integravimo sprendimą, turite įdiegti toliau pateikiamus komponentus.

- „Dynamics 365 Project Service Automation“ 9.0.0.0 arba naujesnė versija
- „Dynamics 365 Sales“ skirtas galimų klientų pavertimo pinigais sprendimas, 1.14.0.0 (v14) arba naujesnė versija
- „Dynamics 365 Project Service Automation“ skirtas „Project Service Automation“ į „Finance“ sprendimas, 1.0.0.0 arba naujesnė versija

## <a name="install-the-project-service-automation-to-finance-integration-solution-in-your-project-service-automation-instance"></a>„Project Service Automation“ į „Finance“ integravimo sprendimo diegimas „Project Service Automation“ egzemplioriuje

Atsisiųskite „Project Service Automation“ į „Finance“ integravimo sprendimą iš [„Microsoft“ atsisiuntimo centro](https://www.microsoft.com/download/details.aspx?id=57016) ir vykdykite į sprendimą įtrauktas instrukcijas.
