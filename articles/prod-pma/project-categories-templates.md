---
title: Projekto išlaidų kategorijų sinchronizavimas tarp „Finance and Operations“ ir „Project Service Automation“
description: Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurios naudojami norint sinchronizuoti projekto išlaidų kategorijas tarp „Microsoft Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“.
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
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: ed7ca3c85d3f99b7eefe10f4ddec822b9aeb1684
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080975"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Projekto išlaidų kategorijų sinchronizavimas tarp „Finance and Operations“ ir „Project Service Automation“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonai ir pagrindinės užduotys, kurios naudojami norint sinchronizuoti projekto išlaidų kategorijas tarp „Dynamics 365 Finance“ ir „Dynamics 365 Project Service Automation“.

> [!NOTE]
> - Projekto užduočių integravimas, išlaidų operacijų kategorijos, valandų įvertinimas, išlaidų įvertinimas ir funkcijų blokavimas prieinami 8.0 versijoje.
> - Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.
> - Jei naudojate „Enterprise Edition“ 7.3.0, įdiegę KB 4132657 ir KB 4132660, galėsite naudoti šablonus projektų užduotims, išlaidų operacijų kategorijoms, valandų įvertinimui, išlaidų įvertinimui ir faktiniams duomenims integruoti bei funkcijų blokavimui konfigūruoti. Jei reikia iš naujo nustatyti apskaitos paskirstymą, rekomenduojame įdiegti ir KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Duomenų srautas iš „Project Service Automation“ ir „Finance“

Naudojant „Project Service Automation“ ir „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose. Integravimo šablonai, kuriuos galima naudoti su duomenų integravimo funkcija, įjungia duomenų srautą apie projekto išlaidų operacijų kategorijas tarp „Project Service Automation“ ir „Finance“.

Jei projekto išlaidų kategorijos valdomos „Finance“, integravimo srautas pirmiausia vyksta iš „Finance“ į „Project Service Automation“. Projekto išlaidų kategorijų integravimo ID atnaujinami sinchronizuojant iš „Project Service Automation“ į „Finance“.

Jei projekto išlaidų kategorijos valdomos „Project Service Automation“, integravimo srautas pirmiausia vyksta iš „Project Service Automation“ į „Finance“. Prieš sinchronizuojant iš „Project Service Automation“ projektų kategorijos jau turi būti sukonfigūruotos „Finance“. Tada sinchronizuokite iš „Finance“ atgal į „Project Service Automation“, o tada – vėl iš „Project Service Automation“ į „Finance“. Tokiu būdu padėsite užtikrinti, kad kategorijos būtų susietos ir kad nebūtų sukurta jokių dublikatų.

> [!NOTE]
> Paprastai, projekto išlaidų kategorijos valdomos „Finance“. Tačiau, jei jų nėra arba jei išlaidų kategorijos jau buvo sukurtos „Project Service Automation“, pirmiausia turite sinchronizuoti naudodami projekto išlaidų operacijų kategorijų (PSA į „Fin and Ops“) šabloną. Tada sinchronizuokite naudodami projekto išlaidų operacijų kategorijų („Fin and Ops“ į PSA) šabloną. Tada turėtumėte dar kartą sinchronizuoti iš „Project Service Automation“ į „Finance“.
>
> Jei pirmą kartą sinchronizuojate iš „Project Service Automation“, prieš paleisdami sinchronizavimą turite atitikti tolesnius „Finance“ reikalavimus.
>
> - „Project Service Automation“ turi būti bendrai naudojama kategorija, kuri atitinka projekto kategoriją, ir ji turi būti įjungta tiek **Projektas** , tiek **Išlaidos**.
> - Kiekvienas „Finance“ juridinis subjektas, su kuriuo turi būti integruota, turi turėti tolesnes kategorijas.
>
>     - **Projekto kategorija** yra. 
>     - **Naudoti išlaidose** įjungta.
>     - **Aktyvu žurnale** įgalinta.
>     - **Operacijos tipas** nustatytas kaip **Išlaidos**.

Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.

[![„Project Service Automation“ ir „Finance“ integravimo duomenų srautas](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Projekto išlaidų kategorijos sinchronizavimas iš „Finance“ į „Project Service Automation“

### <a name="template-and-task"></a>Šablonas ir užduotis

Norėdami pasiekti šabloną, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai** , tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.

Toliau pateikiamas šablonas ir pagrindinė užduotis naudojami norint sinchronizuoti projekto išlaidų kategorijas iš „Finance“ į „Project Service Automation“.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projekto išlaidų operacijų kategorijos („Fin and Ops“ į PSA)
- **Užduoties pavadinimas projekte:** kategorijų sinchronizavimas į PSA

### <a name="entity-set"></a>Objektų rinkinys

| Finansai                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Kategorijų integravimo objektas | Operacijų kategorijos     |

### <a name="entity-flow"></a>Objekto srautas

Projekto išlaidų kategorijos valdomos naudojant „Finance, o sinchronizuojamos su „Project Service Automation“ kaip operacijų kategorijos.

### <a name="power-query"></a>„Power Query“

Kai sinchronizuojate į „Project Service Automation“, turite naudoti „ Microsoft Power Query for Excel“, kad nustatytumėte atsiskaitymo tipą transakcijos kategorijoje. Projekto išlaidų operacijų kategorijų („Fin and Ops“ į PSA) šablonas pateikia numatytąjį stulpelį ir susiejimą. Kurdami savo šabloną, turite įtraukti sąlygos stulpelį į „Power Query“. Atlikite šiuos veiksmus.

1. Spustelėkite rodyklę, kad atidarytumėte projekto išlaidų kategorijų užduoties susiejimą projekto išlaidų operacijų kategorijų („Fin and Ops“ į PSA) šablone.
2. Spustelėkite saitą **Išankstinės užklausos ir filtravimas** , kad atidarytumėte „Power Query“.
2. Pažymėkite **Įtraukti sąlyginį stulpelį**.
3. Įveskite naujo stulpelio pavadinimą, pvz., **BillingType**.
4. Įveskite šią sąlygą: **Jei CATEGORYID nėra lygi nuliui, tada 19235001, kitaip nulis**.
5. Stulpelyje spustelėkite **Gerai**.
6. Įsitikinkite, kad susiejote šį naują stulpelį susiejimo puslapyje.

Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimo pavyzdys. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Finance“ į „Project Service Automation“.

[![Projekto išlaidų kategorijos ir „Project Service Automation“ šablonų susiejimas](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Projekto išlaidų kategorijos sinchronizavimas iš „Project Service Automation“ į „Finance“.

### <a name="template-and-task"></a>Šablonas ir užduotis

Toliau pateikiamas šablonas ir pagrindinė užduotis naudojami norint sinchronizuoti projekto išlaidų kategorijas iš „Project Service Automation“ į „Finance“.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projekto išlaidų operacijų kategorijos (PSA į „Fin and Ops“)
- **Užduoties pavadinimas projekte:** kategorijų sinchronizavimas į „Fin Ops“

### <a name="entity-set"></a>Objektų rinkinys

| Project Service Automation | Finansai                           |
|----------------------------|-----------------------------------|
| Operacijų kategorijos     | Kategorijų integravimo objektas |

### <a name="entity-flow"></a>Objekto srautas

Projekto išlaidų kategorijos valdomos naudojant „Finance, o sinchronizuojamos su „Project Service Automation“ kaip operacijų kategorijos. Sinchronizavimas atgal į „Finance“ atnaujina projekto kategoriją „Finance“ suteikdamas integravimo ID iš „Project Service Automation“.

### <a name="template-mapping-in-data-integration"></a>Šablonų susiejimas pasirinkus Duomenų integravimas

Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimo pavyzdys.

> [!NOTE]
> Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.

[![„Project Service Automation“ ir „Finance“ šablonų susiejimas](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]