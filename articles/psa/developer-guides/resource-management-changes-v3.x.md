---
title: Išteklių valdymo pakeitimai (Project Service Automation 3.x)
description: Šioje temoje pateikiama informacija apie pakeitimus išteklių valdymo srityje.
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 03/18/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 94f9adc67163254486387a1ce59d5d3e8e93c335
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5148653"
---
# <a name="resource-management-changes-project-service-automation-3x"></a>Išteklių valdymo pakeitimai (Project Service Automation 3.x)

[!include [banner](../../includes/psa-now-project-operations.md)]

Šios temos skyriuose pateikiama informacija apie pakeitimus, kurie atlikti Dynamics 365 Project Service Automation 3.x versijos išteklių valdymo srityje.

## <a name="project-estimates"></a>Projekto įvertinimai

Projekto įvertinimai pagrįsti ne objektu **msdyn\_projecttask** (**Projekto užduotis**), o objektu **msdyn\_resourceassignment** (**Išteklių priskyrimas**). Išteklių priskyrimai užduočių planavimui ir įkainiams tapo „tiesos šaltiniu“.

## <a name="line-tasks"></a>Eilutės užduotys

PSA 3.x versijoje eilutės užduotys yra pasenusios (nebenaudojamos). Dabar priskyrimai nurodo visą užduotį, o ne eilutės užduotis.

Toliau pateiktame pavyzdyje parodoma, kaip užduotis, pavadinimu „Bandomoji užduotis“, priskiriama komandos nariams A ir B ankstesnė PSA versijose ir PSA 3.x versijoje.

- **Prieš PSA 3.x:**

    - Bandomoji užduotis

        - Bandomoji užduotis – 1 eilutės užduotis

            - Priskyrimas A

        - Bandomoji užduotis – 2 eilutės užduotis

            - Priskyrimas B

- **PSA 3.x:**

    - Bandomoji užduotis

        - Priskyrimas A
        - Priskyrimas B

## <a name="unassigned-assignment"></a>Nepriskirti priskyrimai

PSA 3.x nepriskirtas priskyrimas yra priskyrimas, kuris priskirtas **NULL** komandos nariui ir **NULL** ištekliams. Nepriskirti priskyrimai įvyksta keliais atvejais:

- Jei užduotis sukurta, tačiau dar nepriskirta jokiam komandos nariui, visada sukuriamas nepriskirtas priskyrimas. 
- Jei visi užduočiai priskirtieji asmenys yra pašalinami, šiai užduočiai iš naujo sukuriamas nepriskirtas priskyrimas.

## <a name="scheduling-fields-on-the-project-task-entity"></a>Projekto užduoties objekto planavimo laukai

Laukai objekte **msdyn\_projecttask** nebenaudojami arba perkelti į objektą **msdyn\_resourceassignment**, arba dabar jie yra nurodomi iš objekto **msdyn\_projectteam** (**Projekto komandos narys**).

| Nebenaudojamas laukas, esantis msdyn\_projecttask (Projekto užduotis) | Naujas laukas, esantis msdyn\_resourceassignment (Išteklių priskyrimas) | Komentaras |
|---|---|---|
| msdyn\_assignedresources | Joks | |
| msdyn\_assignedteammembers | Joks | |
| msdyn\_numberofresources | Joks | |
| msdyn\_scheduledhours | Joks | |
| msdyn\_effortcontour | msdyn\_plannedwork | „JavaScript Object Notation“ (JSON) duomenų struktūros saugomos lauke, formatas pakeistas. |

## <a name="schedule-contour"></a>Grafiko kontūras

Grafiko kontūras saugomas kiekvieno objekto **Išteklių priskyrimas** (**msdyn\_resourceassignment**) lauke **Suplanuotas darbas** (**msdyn\_plannedwork**).

### <a name="structure"></a>Struktūra

Naują grafiko kontūro struktūrą sudaro lankstūs laiko segmentai, kurie apibrėžti kiekvienai grafiko dienai. Kiekvienas laiko segmentas turi šias ypatybes:

- **Pradžia** – dienos darbo valandų pradžia pagal projekto kalendorių.
- **Pabaiga** – dienos darbo valandų pabaiga pagal projekto kalendorių.
- **Valandos** – valandų, priskirtų dienai, skaičius.

**Pavyzdys**

Šiame pavyzdyje pateikiamas projekto kalendorius, kuriame darbo diena tęsiasi nuo 9 val. iki 17 val. pagal UTC-8 laiko juostą.

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

### <a name="auto-scheduling-and-manual-scheduling"></a>Automatinis planavimas ir rankinis planavimas

Jei užduotis yra suplanuota automatiškai, valandos yra iš anksto įkeltos, o užduoties trukmę galima sutrumpinti.

**Pavyzdys**

Ši užduotis automatiškai suplanuota 18 valandų trims dienoms (2018 m. gruodžio 3 d.–2018 m. gruodžio 5 d.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
```

Jei užduotis suplanuota rankiniu būdu, valandos vienodai paskirstomos visoms datoms.

**Pavyzdys**

Ši užduotis rankiniu būdu suplanuota 18 valandų trims dienoms (2018 m. gruodžio 3 d.–2018 m. gruodžio 5 d.).

```json
[{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":6},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":6},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":6}]
```

### <a name="assignment-unit"></a>Priskyrimo vienetas

Priskyrimo vienetas nebenaudojamas PSA 3.x versijoje. Užduoties vienos dienos pastangų valandos vienodai padalintos visiems priskirtiems ištekliams.

**Pavyzdys**

Šiame pavyzdyje užduotis priskirta dviem ištekliams ir automatiškai suplanuota 36 valandoms trims dienoms (2018 m. gruodžio 3 d.–2018 m. gruodžio 5 d.).

- 1 priskyrimas:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

- 2 priskyrimas:

    ```json
    [{"End":"\/Date(1543885200000)\/","Start":"\/Date(1543856400000)\/","Hours":8},{"End":"\/Date(1543971600000)\/","Start":"\/Date(1543942800000)\/","Hours":8},{"End":"\/Date(1544058000000)\/","Start":"\/Date(1544029200000)\/","Hours":2}]
    ```

## <a name="pricing-dimensions"></a>Kainodaros dimensijos

PSA 3.x versijoje konkrečių išteklių kainodaros dimensijos laukai (pavyzdžiui, **Vaidmuo** ir **Organizacinis vienetas**) pašalinti iš objekto **msdyn\_projecttask**. Šiuos laukus dabar galima gauti iš išteklių priskyrimo (**msdyn\_resourceassignment**) atitinkamo projekto komandos nario (**msdyn\_projectteam**), kai sugeneruojami projekto įvertinimai. Naujas laukas **msdyn\_organizationalunit** įtrauktas į objektą **msdyn\_projectteam**.

| Nebenaudojamas laukas, esantis msdyn\_projecttask (Projekto užduotis) | Laukas iš msdyn\_projectteam (Projekto komandos narys), kuris naudojamas vietoje |
|---|---|
| msdyn\_resourcecategory | msdyn\_resourcecategory |
| msdyn\_organizationalunit | msdyn\_organizationalunit |

## <a name="contours"></a>Kontūrai

Kainodaros ir įvertinimo kontūro laukai, kurie nebenaudojami **msdyn\_projecttask** objekte. Jie buvo perkelti į objektą **msdyn\_resourceassignment**.

| Nebenaudojamas laukas, esantis msdyn\_projecttask (Projekto užduotis) | Naujas laukas, esantis msdyn\_resourceassignment (Išteklių priskyrimas) |
|---|---|
| msdyn\_costestimatecontour | msdyn\_plannedcostcontour |
| msdyn\_salesestimatecontour | msdyn\_plannedsalescontour |

Toliau nurodyti laukai buvo įtraukti į objektą **msdyn\_resourceassignment**:

* msdyn\_plannedcost
* msdyn\_plannedsales

Toliau nurodyti suplanuotos, faktinės ir likusios savikainos ir pardavimo laukai objekte **msdyn\_projecttask** yra nepakitę:

* msdyn\_plannedcost
* msdyn\_plannedsales
* msdyn\_actualcost
* msdyn\_actualsales
* msdyn\_remainingcost
* msdyn\_remainingsales


[!INCLUDE[footer-include](../../includes/footer-banner.md)]