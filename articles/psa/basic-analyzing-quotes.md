---
title: Projekto pasiūlymų analizė
description: Šioje temoje pateikiama informacija apie projekto pasiūlymų analizę.
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/05/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: d1b79a61147bfccf13b0a33179464af91b45121e
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291269"
---
# <a name="analysis-of-project-quotes"></a>Projekto pasiūlymų analizė

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

„Dynamics 365 Project Service Automation“ analizuoja projekto pasiūlymus ir įvertina jų pelningumą. Ji taip pat analizuoja, kiek pasiūlymas atitinka kliento lūkesčius dėl pristatymo datos arba įvykdymo datos ir biudžeto.

## <a name="profitability-analysis"></a>Pelningumo analizė

Programos „Project Service Automation“ vykdomai pelningumo analizei naudojama bruto marža ir pakoreguota bruto marža.

- Bruto maržos apskaičiuojamos pagal toliau nurodytą formulę.

  `
    (Sum of estimated chargeable sales value – Sum of estimated chargeable costs) x 100
  `
- Pakoreguota bruto marža apskaičiuojama pagal toliau nurodytą formulę.

  `
    (Sum of estimated chargeable sales value – Sum of all estimated costs) x 100
  `

Jei bruto maržos ir pakoreguotos bruto maržos reikšmės stipriai skiriasi, didelė pasiūlymo darbų dalis klasifikuojama kaip neapmokestinama.

## <a name="analysis-of-customer-expectations"></a>Kliento lūkesčių analizė

Jei įvedate toliau nurodytų laukų reikšmes, galite analizuoti pasiūlymus ir kurti kliento lūkesčių, susijusių su grafiku ir biudžetu, diagramas.

- Laukas **Pageidaujama pristatymo data** pasiūlymo antraštėje.
- Kiekvienos pasiūlymo eilutės (projektu pagrįstų eilučių ir produktu pagrįstų eilučių) laukas **Kliento biudžetas**.

Kliento lūkesčių dėl grafiko analizė atliekama lyginant vėliausią pasiūlymo eilutės informacijos pabaigos datą su pageidaujama visų pasiūlymo eilučių pristatymo data.

Klientų lūkesčių dėl biudžeto analizė atliekama lyginant visą kliento biudžeto sumą su visų pasiūlymo eilučių pasiūlyta suma.


[!INCLUDE[footer-include](../includes/footer-banner.md)]