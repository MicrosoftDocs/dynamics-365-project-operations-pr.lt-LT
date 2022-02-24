---
title: Darbo valandų šablono kūrimas
description: Šioje temoje paaiškinama, kaip sprendime „Project Service“ sukurti darbo valandų šabloną.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981265"
---
# <a name="create-a-work-hours-template-project-service"></a>Darbo valandų šablono kūrimas („Project Service“)

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

Norėdami sukurti ir tvarkyti projektą, projektui turite pritaikyti kalendoriaus šabloną. Kalendoriaus šablonas apibrėžia toliau nurodytus projekto atributus.

- Darbo valandos, įskaitant pradžios ir pabaigos laiką
- Darbo dienos
- Kalendoriaus išimtys, pvz., ne darbo dienos

Projektui taikomas kalendoriaus šablonas yra kalendoriaus šablono, apibrėžto organizacijos parametruose, kopija.

> [!NOTE]
> Jei kalendoriaus šabloną pakeičiate, šie pakeitimai neišplatinami į projekto darbo valandas. Norint pakeisti projekto darbo valandas, reikia pritaikyti naują šabloną.

Norint sukurti savo organizacijos kalendoriaus šabloną, taikomi du pagrindiniai toliau nurodyti reikalavimai.

- Apibrėžkite norimas šablono darbo valandas naudodami naują arba esamą rezervuojamąjį išteklių.
- Sukurkite naują kalendoriaus šabloną ir jį susiekite su rezervuojamuoju ištekliumi.

**Šablono darbo valandų apibrėžimas**

1. Eikite į **Ištekliai** \> **Ištekliai**.
2. Sukurkite naują išteklių, kurį norite nurodyti kalendoriaus šablone, arba pasirinkite esamą išteklių.
3. Pasirinkite ištekliaus skirtuką **Darbo valandos** ir vykdykite nurodymus, pateiktus dalyje [Ištekliaus darbo valandų nustatymas](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource), kad būtų sukonfigūruotos kalendoriaus taisyklės.

**Naujo kalendoriaus šablono sukūrimas**

1. Nueikite į **Parametrai** \> **Kalendoriaus šablonas**.
2. Pasirinkite **Naujas** ir įveskite pavadinimą, aprašą bei šablono išteklių.


> [!NOTE]
> Kai išteklius yra nurodomas kalendoriaus šablone, ištekliaus kalendoriaus kopija susiejama su kalendoriaus šablonu. Jei nukopijuoto šablono darbo valandos pasikeičia, šie pakeitimai neišplatinami į kalendoriaus šabloną.


### <a name="see-also"></a>Taip pat žr.  
 [Išteklių nustatymas](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
