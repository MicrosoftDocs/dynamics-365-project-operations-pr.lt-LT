---
title: Projekto įvertinimų sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurie naudojami norint sinchronizuoti projekto valandų įvertinimus ir projekto išlaidų įvertinimus tiesiogiai iš „Microsoft Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 6696449d80e0915a0c878dbe75cfdf6e268b98ad9f6453bcfc4b424db68021e4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988211"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a>Projekto įvertinimų sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurie naudojami norint sinchronizuoti projekto valandų įvertinimus ir projekto išlaidų įvertinimus tiesiogiai iš „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, valandų įvertinimas, išlaidų įvertinimas ir funkcijų blokavimas prieinami 8.0 versijoje.
> - Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Duomenų srautas iš „Project Service Automation“ į „Finance“

Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose. Integravimo šablonai, kuriuos galima naudoti su duomenų integravimo funkcija, įjungia duomenų srautą apie projekto valandų įvertinimus ir projekto išlaidų įvertinimus iš „Project Service Automation“ į „Finance“.

Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.

[![„Project Service Automation“ ir „Finance“ integravimo duomenų srautas.](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)

## <a name="project-hour-estimates"></a>Projekto valandų įvertinimai

### <a name="template-and-tasks"></a>Šablonas ir užduotys

Norėdami pasiekti galimus šablonus, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.

Toliau pateikiamas šablonas ir pagrindinės užduotys naudojami norint sinchronizuoti projekto valandų įvertinimus iš „Project Service Automation“ į „Finance“.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projekto valandų įvertinimai (PSA į „Fin and Ops“)
- **Projekto užduočių pavadinimas:**

    - Operacijų ryšiai
    - Išlaidų sąmatos

### <a name="entity-set"></a>Objektų rinkinys

| Project Service Automation | Finansai                                       |
|----------------------------|-----------------------------------------------|
| Projekto užduotys              | Projekto valandų įvertinimų integravimo objektas |

### <a name="entity-flow"></a>Objekto srautas

Projekto valandų įvertinimai valdomi naudojant „Project Service Automation“, o sinchronizuojami su „Finance“ kaip projekto valandų prognozės.

### <a name="prerequisites"></a>Būtinosios sąlygos

Prieš atliekant projekto valandų įvertinimų sinchronizavimą, reikia sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.

### <a name="power-query"></a>„Power Query“

Projekto valandų įvertinimo šablone turite naudoti „Microsoft Power Query for Excel”, kad atliktumėte tolesnes užduotis.

- Nustatykite numatytojo prognozės modelio ID, kuris bus naudojamas, kai integruojant bus kuriamos naujos valandų prognozės.
- Filtruokite visus konkretiems ištekliams būdingus užduoties įrašus, kuriuos nepavyks integruoti į valandų prognozes.
- Filtruokite tuščias operacijų kategorijos eilutes. Jei nepavyks atlikti šios užduoties, valandų prognozės gali būti netikslios.

#### <a name="set-the-default-forecast-model-id"></a>Numatytojo prognozės modelio ID nustatymas

Norėdami šablone atnaujinti numatytojo prognozės modelio ID, spustelėkite **struktūros** rodyklę ir atidarykite susiejimą. Tada pasirinkite saitą **Išplėstinė užklausa ir filtravimas**.

- Jei naudojate numatytąjį projekto valandų įvertinimų šabloną (PSA į „Fin and Ops“), sąraše **Taikomi veiksmai** pažymėkite **Įtraukta sąlyga**. Įraše **Funkcija** pakeiskite **O\_prognozė** prognozės modelio ID pavadinimu, kuris turi būti naudojamas su šiuo integravimu. Numatytajame šablone naudojamas demonstracinių duomenų prognozės modelio ID.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį. „Power Query” pasirinkite **Įtraukti sąlygos stulpelį** ir įveskite naujo stulpelio pavadinimą, pvz., **ModelID**. Įveskite stulpelio sąlygą, kur, jei projekto užduotis apibrėžta, tada \<enter the forecast model ID\>; kitu atveju neapibrėžta reikšmė.

#### <a name="filter-out-resource-specific-records"></a>Filtruokite konkretiems ištekliams būdingus įrašus

Projekto valandų įvertinimų (PSA į „Fin and Ops“) šablonas turi numatytąjį filtrą, kuriuo pašalinami visi konkretiems ištekliams būdingi įrašai. Kurdami savo šabloną, turite įtraukti šį filtrą. Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**, jei norite filtruoti stulpelį **msdyn\_islinetask**, kad būtų įtraukti tik **Klaidingi** įrašai.

#### <a name="filter-out-empty-transaction-category-rows"></a>Filtruokite tuščias operacijų kategorijos eilutes

Reikia įtraukti filtrą, kad būtų pašalintos visos eilutės, kuriose yra tuščių operacijų kategorijų. Ši užduotis yra privaloma, neatsižvelgiant į tai, ar naudojate numatytąjį šabloną, ar kuriate savo. Šiuo filtru iš „Project Service Automation” pašalinamos visos suvestinių eilutes, dėl kurių valandų prognozės programoje „Finance” gali būti netikslios. Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**, kad filtruotumėte neapibrėžtų reikšmių įrašus stulpelyje **msdyn\_transactioncategory\_value**.

### <a name="template-mapping-in-data-integration"></a>Šablonų susiejimas pasirinkus Duomenų integravimas

Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimo pavyzdys. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.

[![Šablono užduoties susiejimas duomenų integravime.](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)

## <a name="project-expense-estimates"></a>Projekto išlaidų įvertinimai

### <a name="template-and-tasks"></a>Šablonas ir užduotys

Toliau pateikiamas šablonas ir pagrindinės užduotys naudojami norint sinchronizuoti projekto išlaidų įvertinimus iš „Project Service Automation“ į „Finance“.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projekto išlaidų įvertinimai (PSA į „Fin and Ops“)
- **Projekto užduočių pavadinimas:**

    - Operacijų ryšiai 
    - Išlaidų sąmatos

### <a name="entity-set"></a>Objektų rinkinys

| Project Service Automation | Finansai                                                  |
|----------------------------|----------------------------------------------------------|
| Operacijos ryšiai    | Projekto operacijų ryšių integravimo objektas |
| Įvertinimo eilutės             | Projekto išlaidų įvertinimų integravimo objektas         |

### <a name="entity-flow"></a>Objekto srautas

Projekto išlaidų įvertinimai valdomi naudojant „Project Service Automation“, o sinchronizuojami su „Finance“ kaip projekto išlaidų prognozės.

### <a name="prerequisites"></a>Būtinosios sąlygos

Prieš atliekant projekto išlaidų įvertinimų sinchronizavimą, reikia sinchronizuoti projektus, projekto užduotis ir projekto išlaidų operacijų kategorijas.

### <a name="power-query"></a>„Power Query“

Projekto išlaidų įvertinimo šablone turite naudoti „Power Query”, kad atliktumėte tolesnes užduotis.

- Filtruokite, kad įtrauktumėte tik išlaidų įvertinimų eilučių įrašus.
- Nustatykite numatytojo prognozės modelio ID, kuris bus naudojamas, kai integruojant bus kuriamos naujos valandų prognozės.
- Atsiskaitymo tipų keitimas.
- Operacijų tipų keitimas.

#### <a name="filter-to-include-only-expense-estimate-lines"></a>Filtruokite, kad įtrauktumėte tik išlaidų įvertinimų eilutes

Projekto išlaidų įvertinimų (PSA į „Fin and Ops“) šablone yra numatytasis filtras, kuriuo į integravimą įtraukiamos tik išlaidų eilutės. Kurdami savo šabloną, turite įtraukti šį filtrą. Pasirinkite užduotį **Operacijų ryšiai**, tada spustelėkite **struktūros** rodyklę, kad atidarytumėte susiejimą. Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**. Filtruokite stulpelį **msdyn\_transactiontype1**, kad jame būtų tik **msdyn\_estimateline**.

#### <a name="set-the-default-forecast-model-id"></a>Numatytojo prognozės modelio ID nustatymas

Norėdami šablone atnaujinti numatytojo prognozės modelio ID, pasirinkite užduotį **Išlaidų įvertinimai**, tada spustelėkite **struktūros** rodyklę ir atidarykite susiejimą. Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**.

- Jei naudojate numatytąjį projekto išlaidų įvertinimų šabloną (PSA į „Fin and Ops“), „Power Query” skyriuje **Taikomi veiksmai** pasirinkite pirmą **įtrauktą sąlygą**. Įraše **Funkcija** pakeiskite **O\_prognozė** prognozės modelio ID pavadinimu, kuris turi būti naudojamas su šiuo integravimu. Numatytajame šablone naudojamas demonstracinių duomenų prognozės modelio ID.
- Jei kuriate naują šabloną, turite įtraukti šį stulpelį. „Power Query” pasirinkite **Įtraukti sąlygos stulpelį** ir įveskite naujo stulpelio pavadinimą, pvz., **ModelID**. Įveskite stulpelio sąlygą, kur, jei įvertinimo eilutės ID apibrėžta, tada \<enter the forecast model ID\>; kitu atveju neapibrėžta reikšmė.

#### <a name="transform-the-billing-types"></a>Atsiskaitymo tipų keitimas

Projekto išlaidų įvertinimų (PSA į „Fin and Ops“) šablone yra sąlygos stulpelis, kuris yra naudojamas atsiskaitymo tipams, gaunamiems iš „Project Service Automation” integravimo metu, keisti. Kurdami savo šabloną, turite įtraukti šį sąlygos stulpelį. Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**, tada pasirinkite **Įtraukti sąlygos stulpelį**. Įveskite naujo stulpelio pavadinimą, pvz., **BillingType**. Tada įveskite tolesnę sąlygą.

Jei **msdyn\_billingtype** lygu 192350000, tada **NonChargeable**  
Taip pat jei **msdyn\_billingtype** lygu 192350001, tada **Chargeable**  
Taip pat jei **msdyn\_billingtype** lygu 192350002, tada **Complimentary**  
kitaip **NotAvailable**

#### <a name="transform-the-transaction-types"></a>Operacijų tipų keitimas

Projekto išlaidų įvertinimų (PSA į „Fin and Ops“) šablone yra sąlygos stulpelis, kuris yra naudojamas operacijų tipams, gaunamiems iš „Project Service Automation” integravimo metu, keisti. Kurdami savo šabloną, turite įtraukti šį sąlygos stulpelį. Pasirinkite saitą **Išplėstinė užklausa ir filtravimas**, tada pasirinkite **Įtraukti sąlygos stulpelį**. Įveskite naujo stulpelio pavadinimą, pvz., **TransactionType**. Tada įveskite tolesnę sąlygą.

Jei **msdyn\_transactiontypecode** lygu 192350000, tada **Cost**  
Taip pat jei **msdyn\_transactiontypecode** lygu 192350005, tada **Sales**  
kitaip **null**

### <a name="template-mapping-in-data-integration"></a>Šablonų susiejimas pasirinkus Duomenų integravimas

Šiose iliustracijose pateikiami duomenų integravimo šablonų užduočių susiejimų pavyzdžiai. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.

[![Išlaidų įvertinimo operacijų šablono susiejimas.](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)

[![Išlaidų įvertinimo šablono susiejimas.](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]