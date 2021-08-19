---
title: Projekto faktinių duomenų sinchronizavimas tiesiogiai iš „Project Service Automation“ į projekto integravimo žurnalą norint paskelbti „Finance and Operations“
description: Šioje temoje aprašomi šablonai ir pagrindinė užduotys, kurios naudojamos norint sinchronizuoti projekto faktinius duomenis tiesiogiai iš „Microsoft Dynamics 365 Project Service Automation“ į „Finance and Operations“.
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 85b6c07464e919e363f28d8bc62115e8fb4c72ea6631269b98fd00f324a01cba
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988121"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>Projekto faktinių duomenų sinchronizavimas tiesiogiai iš „Project Service Automation“ į projekto integravimo žurnalą norint paskelbti „Finance and Operations“

[!include[banner](../includes/banner.md)]

Šioje temoje aprašomi šablonai ir pagrindinė užduotys, kurios naudojamos norint sinchronizuoti projekto faktinius duomenis tiesiogiai iš „Dynamics 365 Project Service Automation“ į „Dynamics 365 Finance“.

Šablonas sinchronizuoja operacijas iš „Project Service Automation“ į paruošimo lenteles „Finance“. Baigę sinchronizuoti, **turite** importuoti duomenis iš paruošimo lentelės į integravimo žurnalą.

> [!NOTE]
> - Projekto Faktinių duomenų integravimas galimas 8.0.1 ir naujesnėse versijoje.
> - Jei naudojate „Enterprise Edition“ 7.3.0, įdiegę KB 4132657 ir KB 4132660, galėsite naudoti šablonus projektų užduotims, išlaidų operacijų kategorijoms, valandų įvertinimui, išlaidų įvertinimui ir faktiniams duomenims integruoti bei funkcijų blokavimui konfigūruoti. Jei reikia iš naujo nustatyti apskaitos paskirstymą, rekomenduojame įdiegti ir KB 4131710.
> - Jei naudojate 7.3.0 versiją ir norite įtraukti mokesčių operacijas iš „Project Service Automation“, turite įdiegti KB 4345320, kad įtrauktumėte šiuos mokesčius į projekto sąskaitą faktūrą.
> - Jei pardavimo mokesčių sumas įvedate laiko arba išlaidų operacijose „Project Service Automation“, turite įdiegti „Project Service Automation“ 7 naujinį. Kitaip mokesčių faktiniai duomenys nebus susieti su susijusiais laiko ar išlaidų faktiniais duomenimis ir jų nebus galima sinchronizuoti į „Finance“. Susisiekite su palaikymo komanda, kad gautumėte daugiau informacijos.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Duomenų srautas iš „Project Service Automation“ į „Finance“

Naudojant „Project Service Automation“ į „Finance“ integravimo sprendimą, naudojama duomenų integravimo funkcija, sinchronizuojant duomenis „Project Service Automation“ ir „Finance“ egzemplioriuose. Integravimo šablonai, kuriuos galima naudoti su duomenų integravimo funkcija, įjungia duomenų srautą apie projektų faktinius duomenis iš „Project Service Automation“ į „Finance“.

Šioje iliustracijoje pavaizduota, kaip duomenys sinchronizuojami tarp „Project Service Automation“ ir „Finance“.

[![„Project Service Automation“ integravimas su „Finance and Operations“.](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Projekto faktiniai duomenys iš „Project Service Automation“

### <a name="template-and-tasks"></a>Šablonas ir užduotys

Norėdami pasiekti galimus šablonus, „Microsoft Power Apps“ administravimo centre pasirinkite **Projektai**, tada viršutiniame dešiniajame kampe pasirinkite **Naujas projektas** ir viešuosius šablonus.

Toliau pateikiamas šablonas ir pagrindinės užduotys naudojamos norint sinchronizuoti projekto faktinius duomenis iš „Project Service Automation“ į „Finance“.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projekto faktiniai duomenys (PSA į „Fin and Ops“)
- **Projekto užduočių pavadinimas:**

    - Faktiniai duomenys
    - TransactionConnections

### <a name="entity-set"></a>Objektų rinkinys

| Project Service Automation | Finansai                                   |
|----------------------------|----------------------------------------------------------|
| Faktiniai duomenys                    | Projekto faktinių duomenų integravimo objektas                   |
| Operacijos ryšiai    | Projekto operacijų ryšių integravimo objektas |

### <a name="entity-flow"></a>Objekto srautas

Projekto faktiniai duomenys valdomi „Project Service Automation“, o sinchronizuojami į projekto integravimo žurnalą, esantį „Finance“. Apskaita bus taikoma remiantis numatytosiomis finansinėmis dimensijomis ir registravimo sąranka.

### <a name="prerequisites"></a>Būtinosios sąlygos

Prieš sinchronizuodami faktinius duomenis, turite sukonfigūruoti „Project Service Automation“ integravimo parametrus ir sinchronizuoti projektus, projektų užduotis ir projekto išlaidų operacijų kategorijas.

### <a name="power-query"></a>„Power Query“

Projekto faktinių duomenų šablone turite naudoti „Microsoft Power Query for Excel”, kad atliktumėte tolesnes užduotis.

- Pakeisti operacijos tipą „Project Service Automation“ į tinkamą operacijos tipą „Finance“. Šis pakeitimas jau apibrėžtas projekto faktinių duomenų (PSA į „Fin and Ops“) žurnale.
- Pakeisti atsiskaitymo tipą „Project Service Automation“ į tinkamą atsiskaitymo tipą „Finance“. Šis pakeitimas jau apibrėžtas projekto faktinių duomenų (PSA į „Fin and Ops“) žurnale. Tada atsiskaitymo tipas susiejamas su eilutės ypatybe pagal konfigūraciją puslapyje **„Project Service Automation“ integravimo parametrai**.
- Filtruokite konkrečius išteklių organizacinius vienetus, kuriuos reikia sinchronizuoti su šiuo šablonu.
- Jei vidinės įmonės laiko arba vidinės įmonės išlaidų faktiniai duomenys bus sinchronizuojami su „Finance“, sutarties organizacinį vienetą turite pakeisti į tinkamą juridinį subjektą „Finance“. Projekto faktinių duomenų (PSA į „Fin ir Ops“) šablone sąlyginis stulpelis apibrėžiamas pagal parodomuosius duomenis. Turite atnaujinti paskutinį įterptą sąlyginį stulpelį, kad jame būtų tinkami juridiniai subjektai. Priešingu atveju gali įvykti integravimo klaida arba į „Finance“ gali būti importuotos netinkamos faktinių duomenų operacijos.
- Jei vidinės įmonės laiko arba vidinės įmonės išlaidų faktinės sumos nebus sinchronizuojamos į „Finance“, turite panaikinti paskutinį iš savo šablono įterptą sąlyginį stulpelį. Priešingu atveju gali įvykti integravimo klaida arba į „Finance“ gali būti importuotos netinkamos faktinių duomenų operacijos.

#### <a name="contract-organizational-unit"></a>Sutarties organizacinis vienetas
Norėdami atnaujinti į šabloną įterptą sąlyginį stulpelį, spustelėkite **Struktūros** rodyklę ir atidarykite susiejimą. Spustelėkite saitą **Išankstinės užklausos ir filtravimas**, kad atidarytumėte „Power Query“.

- Jei naudojate numatytąjį projekto faktinių duomenų šabloną (PSA į „Fin and Ops“), „Power Query” skyriuje **Taikomi veiksmai** pasirinkite naujausią **įtrauktą sąlygą**. Įraše **Funkcija** pakeiskite **USSI** juridinio subjekto pavadinimu, kuris turi būti naudojamas su šiuo integravimu. Jei reikia, įtraukite papildomų sąlygų į **Funkcija** įrašą ir atnaujinkite būsena **kitas** iš **USMF** į teisingą juridinį subjektą.
- Jei kuriate naują šabloną, turite įtraukti stulpelį, kuriame palaikomas vidinės įmonės laikas ir išlaidos. Pasirinkite **Įtraukti sąlygos stulpelį** ir įveskite naujo stulpelio pavadinimą, pvz., **LegalEntity**. Įveskite stulpelio sąlygą, kur jei **msdyn\_contractorganizationalunitid.msdyn\_pavadinimas** yra \<organizational unit\>, tada \<enter the legal entity\>; kitu atveju neapibrėžta reikšmė.

### <a name="template-mapping-in-data-integration"></a>Šablonų susiejimas pasirinkus Duomenų integravimas

Šioje iliustracijoje pateikiamas duomenų integravimo šablonų užduočių susiejimo pavyzdys. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Project Service Automation“ į „Finance“.

[![Šablonų susiejimas – faktiniai duomenys.](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![Šablonų susiejimas – operacijų ryšiai.](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>Importavimas iš paruošimo lentelės po integravimo iš „Project Service Automation“

Importavimo iš paruošimo lentelės periodinis procesas turi būti vykdomas sinchronizavus faktinius duomenis iš „Project Service Automation“ į „Finance“. Šis procesas importuos projekto operacijas iš paruošimo lentelės į „Project Service Automation“ integravimo žurnalą, kuriame taikoma apskaita ir gali būti registruojamos importuotos operacijos. Rekomenduojame paleisti šį procesą paketais; galima pasirinktinai nustatyti, kad ji būtų vykdoma kaip pasikartojantis paketas.

## <a name="update-actuals-from-finance"></a>„Finance“ faktinių duomenų naujinimas

### <a name="template-and-tasks"></a>Šablonas ir užduotys

Šis šablonas ir pagrindinės užduotys naudojamos norint sinchronizuoti kvitų numerius ir pardavimo mokesčius, taikomus užregistruotoms projektų operacijoms, iš „Finance“ į „Project Service Automation“.

- **Šablono pavadinimas pasirinkus duomenų integravimą:** projekto faktinių duomenų naujinimas („Fin and Ops“ į PSA)
- **Projekto užduočių pavadinimas:**

    - Faktiniai duomenys 
    - TransactionConnections

### <a name="entity-set"></a>Objektų rinkinys

| Finansai                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| Projekto faktinių duomenų integravimo objektas                   | Faktiniai duomenys                    |
| Projekto operacijų ryšių integravimo objektas | Operacijos ryšiai    |

### <a name="entity-flow"></a>Objekto srautas

Projekto faktiniai duomenys valdomi „Project Service Automation“, o sinchronizuojami į projekto integravimo žurnalą, esantį „Finance“. Užregistravus faktinius duomenis „Finance“, jie atnaujinami „Project Service Automation“ suteikiant kvito numerį iš „Finance“. Jei pardavimo mokesčiai įtraukti į „Finance“, „Project Service Automation“ sukuriami nauji mokesčio faktiniai duomenys.

### <a name="power-query"></a>„Power Query“

Projekto faktinių duomenų naujinimo šablone turite naudoti „Power Query”, kad atliktumėte tolesnes užduotis.

- Pakeisti operacijos tipą „Finance“ į tinkamą operacijos tipą „Project Service Automation“. Šis pakeitimas jau apibrėžtas projekto faktinių duomenų naujinimo („Fin and Ops“ į PSA) šablone.
- Pakeisti atsiskaitymo tipą Finance“ į tinkamą atsiskaitymo tipą „Project Service Automation“. Šis pakeitimas jau apibrėžtas projekto faktinių duomenų naujinimo („Fin and Ops“ į PSA) šablone.

### <a name="template-mapping-in-data-integration"></a>Šablonų susiejimas pasirinkus Duomenų integravimas

Šiose iliustracijose pateikiami duomenų integravimo šablonų užduočių susiejimų pavyzdžiai. Susiejime rodoma lauko informacija, kuri bus sinchronizuojama iš „Finance“ į „Project Service Automation“.

[![Šablonų susiejimas – faktinių duomenų atnaujinimas.](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![Šablonų susiejimas – operacijos atnaujinimas.](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]