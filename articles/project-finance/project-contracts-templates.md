---
title: Projekto sutarčių ir projektų sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“
description: Šioje temoje aprašomi šablonas ir pagrindinės užduotys, kurie naudojami norint sinchronizuoti projekto sutartis ir projektus tiesiogiai iš „Microsoft Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.
author: KimANelson
manager: AnnBe
ms.date: 09/09/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 57fe4ae8-6ee9-442d-9933-d525b5415db8
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-12-13
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: b914a56b306639253a8cd3b7caa754da175b6df2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753646"
---
# <a name="synchronize-project-contracts-and-projects-directly-from-project-service-automation-to-finance-and-operations"></a>Projekto sutarčių ir projektų sinchronizavimas tiesiogiai iš „Project Service Automation“ į „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonas ir pagrindinės užduotys, kurie naudojami norint sinchronizuoti projekto sutartis ir projektus tiesiogiai iš „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.

> [!NOTE] 
> Jei naudojate 7.3.0 versijos „Enterprise edition”, turite įdiegti KB 4074835.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Duomenų srautas iš „Project Service Automation“ į „Finance“

> [!NOTE]
> Norėdami naudoti „Project Service Automation“ į „Finance“ integravimo sprendimą, turėtumėte susipažinti su „Dynamics 365” duomenų integravimo funkcija.

Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose. Integravimo šablonas, kurį galima naudoti su duomenų integravimo funkcija, leidžia vykdyti duomenų apie projekto sutartis, projektų, projektų sutarčių eilučių ir projektų sutarčių eilučių etapų srautą iš „Project Service Automation“ į „Finance“.

Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.

[![„Project Service Automation“ ir „Finance“ integravimo duomenų srautas](./media/ProjectsAndContractsFlow_upd.JPG)](./media/ProjectsAndContractsFlow.JPG)

## <a name="templates-and-tasks"></a>Šablonai ir užduotys

Norėdami pasiekti galimus šablonus, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.

Toliau pateikiami šablonai ir pagrindinės užduotys naudojami norint sinchronizuoti projekto sutartis ir projektus iš „Project Service Automation“ į „Finance“.

### <a name="integrating-with-dynamics-365-project-service-automation-v2x"></a>Integravimas su „Dynamics 365 Project Service Automation” v2. x
- **Šablono pavadinimas pasirinkus duomenų integravimą:** projektai ir sutartys (PSA į „Fin and Ops“)
- **Projekto užduočių pavadinimas:**

    - Projekto sutarčių PSA į „Fin and Ops“
    - Projektų PSA į „Fin and Ops“
    - Projekto sutarties eilučių PSA į „Fin and Ops“
    - Projekto sutarties eilučių etapų PSA į „Fin and Ops“
  
### <a name="integrating-with-dynamics-365-project-service-automation-v3x"></a>Integravimas su „Dynamics 365 Project Service Automation” v3. x
Programoje „Project Service Automation” yra atliktas schemų pakeitimas, turintis įtakos projekto sutarties eilutės etapo šablonui, todėl norint integruoti v3.x versijos „Project Service Automation” su „Dynamics 365”, reikia naudoti v2 versijos šabloną.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projektai ir sutartys (PSA 3.x į „Fin and Ops“) – v2
- **Projekto užduočių pavadinimas:**

    - Projekto sutarčių PSA į „Fin and Ops“
    - Projektų PSA į „Fin and Ops“
    - Projekto sutarties eilučių PSA į „Fin and Ops“
    - Projekto sutarties eilučių etapų PSA į „Fin and Ops“

Prieš atliekant projekto sutarčių ir projektų sinchronizavimą, reikia sinchronizuoti klientus.

## <a name="entity-set"></a>Objektų rinkinys 

| Project Service Automation       | Finansai                                                |
|----------------------------------|--------------------------------------------------------|
| Užsakymai                           | Projekto sutarties integravimo objektas                |
| Projektai                         | Projekto integravimo objektas                         |
| Užsakymo eilutės                      | Projekto sutarties eilutės integravimo objektas           |
| Projekto sutarties eilutės etapai | Projekto sutarties eilutės etapo integravimo objektas |

## <a name="entity-flow"></a>Objekto srautas

Projektų sutartys valdomos naudojant „Project Service Automation“, o sinchronizuojamos su „Finance“ kaip projektų sutartys. Programoje „Finance“ galite nustatyti projekto sutarties integravimo šaltinį kaip integravimo šablono dalį.

Laiko ir medžiagų projektai bei fiksuotos kainos projektai valdomi naudojant „Project Service Automation“, o sinchronizuojamos su „Finance“ kaip projektai. Programoje „Finance“ galite nustatyti projekto integravimo šaltinį kaip šablono integravimo dalį.

Projektų sutarčių eilutės valdomos naudojant „Project Service Automation“, o sinchronizuojamos su „Finance“ kaip projektų sutarčių atsiskaitymo taisyklės. Jei atsiskaitymo būdas skiriasi nuo numatytojo projekto tipo, sinchronizuojant atnaujinamas sutarties eilutės projekto ir projekto grupės projekto tipas.

Projektų sutarčių eilučių etapai valdomi naudojant „Project Service Automation“, o sinchronizuojami su „Finance“ kaip projektų sutarčių atsiskaitymo taisyklių etapai.

## <a name="project-service-automation-to-finance-integration-solution"></a>„Project Service Automation“ į „Finance“ integravimo sprendimas

Laukas **Projekto sutarties ID** pasiekiamas puslapyje **Projekto sutartys**. Šis laukas sukurtas kaip natūralus ir unikalus integravimo palaikymo raktas.

Jeigu sukuriama nauja projekto sutartis, o reikšmės **Projekto sutarties ID** dar nėra, ji generuojama automatiškai, naudojant numerių seką. Reikšmę sudaro **ORD**, laipsniškai didėjanti numerių seka ir šešių simbolių sufiksas. Štai pavyzdys: **ORD-01022-Z4M9Q0**.

Laukas **Projekto numeris** pasiekiamas puslapyje **Projektai**. Šis laukas sukurtas kaip natūralus ir unikalus integravimo palaikymo raktas.

Jeigu sukuriamas naujas projektas, o reikšmės **Projekto numeris** dar nėra, ji generuojama automatiškai, naudojant numerių seką. Reikšmę sudaro **PRJ**, laipsniškai didėjanti numerių seka ir šešių simbolių sufiksas. Štai pavyzdys: **PRJ-01049-CCNID0**.

Taikant „Project Service Automation” į „Finance” integravimo sprendimą, naujinimo scenarijus nustato esamų projektų sutarčių lauką **Projekto sutarties ID** ir esamų projektų lauką **Projekto numeris** programoje „Project Service Automation”.

## <a name="prerequisites-and-mapping-setup"></a>Būtinosios sąlygos ir susiejimo sąranka

- Prieš atliekant projekto sutarčių ir projektų sinchronizavimą, reikia sinchronizuoti klientus.
- Savo ryšių rinkinyje įtraukite integravimo rakto lauko susiejimą **msdyn\_organizationalunits** į **msdyn\_name \[pavadinimas\]**. Galbūt pirma reikės įtraukti projektą į ryšių rinkinį. Norėdami gauti daugiau informacijos žr. [Duomenų integravimas į „Common Data Service”, skirta programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Savo ryšių rinkinyje įtraukite integravimo rakto lauko susiejimą **msdyn\_projects** į **msdynce\_projectnumber \[projekto numeris\]**. Galbūt pirma reikės įtraukti projektą į ryšių rinkinį. Norėdami gauti daugiau informacijos žr. [Duomenų integravimas į „Common Data Service”, skirta programoms](https://docs.microsoft.com/powerapps/administrator/data-integrator).
- Projektų sutarčių ir projektų **SourceDataID** gali būti atnaujintas į kitą reikšmę arba pašalintas iš susiejimo. Numatytoji šablono reikšmė yra **„Project Service Automation”**.
- Susiejimas **PaymentTerms** turi būti atnaujintas, kad atspindėtų galiojančias mokėjimo sąlygas programoje „Finance”. Taip pat galite pašalinti susiejimą iš projekto užduoties. Numatytosios reikšmės struktūroje yra numatytosios demonstracinių duomenų reikšmės. Šioje lentelėje pateikiamos „Project Service Automation” esančios reikšmės.

    | Vertė | Aprašo   |
    |-------|---------------|
    | 1     | Apmokėjimas per 30 dienų        |
    | 2     | Apmok.per 30 d., apmok.per 10 d.taik.2% nuol. |
    | 3     | Apmokėjimas per 45 dienas        |
    | 4     | Apmokėjimas per 60 dienų        |

## <a name="power-query"></a>„Power Query“

Norėdami filtruoti duomenis, jei patenkinamos toliau pateikiamos sąlygos, turite naudoti „Microsoft Power Query for Excel“.

- Programoje „Dynamics 365 Sales” turite pardavimo užsakymų.
- Programoje „Project Service Automation” turite kelis organizacijos vienetus ir šie organizaciniai vienetai bus susiejami su keliais juridiniais subjektais programoje „Finance”.

Jei reikia naudoti „Power Query“, vadovaukitės toliau pateikiamais nurodymais.

- Projektų ir sutarčių (PSA į „Fin and Ops“) šablone yra numatytasis filtras, kuriame yra tik **Darbo elemento (msdyn\_ordertype = 192350001)** tipo pardavimo užsakymai. Šis filtras padeda užtikrinti, kad nebūtų kuriamos projektų sutartys, skirtos pardavimo užsakymams programoje „Finance”. Kurdami savo šabloną, turite įtraukti šį filtrą.
- Turite sukurti „Power Query” filtrą, kuriame būtų tik tos sutarčių organizacijos, kurias reikia sinchronizuoti su integravimo ryšių rinkinio juridiniu subjektu. Pavyzdžiui, projektų sutartys, kurias turite sudarę su sutarčių organizacijos vienetu „Contoso“, JAV, turi būti sinchronizuojamos su USSI juridiniu subjektu, o projektų sutartys, kurias turite sudarę su sutarčių organizacijos vienetu „Contoso Global“, turi būti sinchronizuojamos su USMF juridiniu subjektu. Jei neįtrauksite šio filtro į užduočių susiejimą, visos projektų sutartys bus sinchronizuojamos su juridiniu subjektu, nustatytu ryšio rinkiniui, neatsižvelgiant į sutarties organizacijos vienetą.

## <a name="template-mapping-in-data-integration"></a>Šablonų susiejimas pasirinkus Duomenų integravimas

> [!NOTE] 
> Laukai **CustomerReference**, **AddressCity**, **AddressCountryRegionID**, **AddressDescription**, **AddressLine1**, **AddressLine2**, **AddressState** ir **AddressZipCode** neįtraukti į projektų sutarčių numatytąjį susiejimą. Jei reikia, kad šie duomenys būtų sinchronizuojami su projektų sutartimis, galite įtraukti šiuos susiejimus.
>
> Laukai **Description**, **ParentID**, **ProjectGroup**, **ProjectManagerPersonnelNumber** ir **ProjectType** neįtraukti į projektų numatytąjį susiejimą. Jei reikia, kad šie duomenys būtų sinchronizuojami su projektais, galite įtraukti šiuos susiejimus.

Šiose iliustracijose pateikiami duomenų integravimo šablonų užduočių susiejimų pavyzdžiai. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.

[![Šablonų susiejimas](./media/ProjectContractTemplateMapping.JPG)](./media/ProjectContractTemplateMapping.JPG)

[![Šablonų susiejimas](./media/ProjectTemplateMapping.JPG)](./media/ProjectTemplateMapping.JPG)

[![Šablonų susiejimas](./media/ProjectContractLinesMapping.JPG)](./media/ProjectContractLinesMapping.JPG)

[![Šablonų susiejimas](./media/ProjectContractLineMilestonesMapping.JPG)](./media/ProjectContractLineMilestonesMapping.JPG)

#### <a name="project-contract-line-milestone-mapping-in-the-projects-and-contracts-psa-3x-to-dynamics---v2-template"></a>Projekto sutarties eilutės etapo susiejimas projektų ir sutarčių dalyje (PSA 3.x į „Dynamics”) – v2 šablonas.

[![Šablonų susiejimas](./media/ProjectContractLineMilestoneMapping_v2.jpg)](./media/ProjectContractLineMilestoneMapping_v2.jpg)
