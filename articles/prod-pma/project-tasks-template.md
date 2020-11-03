---
title: Projekto užduočių sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“
description: Šioje temoje aprašomi šablonas ir pagrindinė užduotis, kurie naudojami norint sinchronizuoti projekto užduotis tiesiogiai iš „Microsoft Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.
author: Yowelle
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 0383607a07def6c21562bf4b0893fe3ce3db6a04
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080818"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Projekto užduočių sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonas ir pagrindinė užduotis, kurie naudojami norint sinchronizuoti projekto užduotis tiesiogiai iš „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, valandų įvertinimas, išlaidų įvertinimas ir funkcijų blokavimas prieinami 8.0 versijoje.
> - Jei naudojate „Enterprise Edition“ 7.3.0, įdiegę KB 4132657 ir KB 4132660, galėsite naudoti šablonus projektų užduotims, išlaidų operacijų kategorijoms, valandų įvertinimui, išlaidų įvertinimui ir faktiniams duomenims integruoti bei funkcijų blokavimui konfigūruoti. Jei reikia iš naujo nustatyti apskaitos paskirstymą, rekomenduojame įdiegti ir KB 4131710.
> - Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Duomenų srautas iš „Project Service Automation“ į „Finance“

Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose. Integravimo šablonas, kurį galima naudoti su duomenų integravimo funkcija, įjungia duomenų srautą apie projektų užduotis iš „Project Service Automation“ į „Finance“.

Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.

[![„Project Service Automation“ ir „Finance“ integravimo duomenų srautas](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Šablonas ir užduotis

Norėdami pasiekti šabloną, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai** , tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.

Toliau pateikiamas šablonas ir pagrindinė užduotis naudojami norint sinchronizuoti projekto užduotis iš „Project Service Automation“ į „Finance“.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projekto užduotys (PSA į „Fin and Ops“)
- **Projekto užduoties pavadinimas:** projekto užduotys

Prieš atliekant projekto užduočių sinchronizavimą, reikia sinchronizuoti projektų sutartis ir projektus.

## <a name="entity-set"></a>Objektų rinkinys 

| Project Service Automation | „Finance“                             |
|----------------------------|-------------------------------------|
| Projekto užduotys              | Projekto užduoties integravimo objektas |

## <a name="entity-flow"></a>Objekto srautas

Projektų užduotys valdomos naudojant „Project Service Automation“, o sinchronizuojamos su „Finance“ kaip projektų veiklos.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

Prieš atliekant projekto užduočių sinchronizavimą, reikia sinchronizuoti projektų sutartis ir projektus.

## <a name="power-query"></a>„Power Query“

Norėdami filtruoti duomenis, jei patenkinama toliau pateikiama sąlyga, turite naudoti „Microsoft Power Query for Excel“.

- Projekto užduotyje yra ištekliams būdingų įrašų.

Jei reikia naudoti „Power Query“, vadovaukitės toliau pateikiamais nurodymais.

- Projektų užduočių (PSA į „Fin and Ops“) šablone yra numatytasis filtras, neįtraukiantis ištekliams būdingų įrašų į projekto užduotį, nustatydamas filtro **IsLineTask** reikšmę **Klaidinga**. Kurdami savo šabloną, turite įtraukti šį filtrą.

## <a name="template-mapping-in-data-integration"></a>Šablonų susiejimas pasirinkus Duomenų integravimas

Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimų pavyzdys. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.

[![Šablonų susiejimas](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
