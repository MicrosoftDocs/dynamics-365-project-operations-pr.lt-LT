---
title: Projekto kalendorių apibrėžimas
description: Šioje temoje pateikiama informacijos apie tai, kaip projektui taikyti kalendoriaus šabloną projekto grafikui sekti.
author: ruhercul
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 9c2ea49e008d6cde40f152320face073c7e5f548
ms.sourcegitcommit: bbe484e58a77efe77d28b34709fb6661d5da00f9
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 09/10/2021
ms.locfileid: "7487650"
---
# <a name="define-project-calendars"></a>Projekto kalendorių apibrėžimas

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

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
3. Pasirinkite ištekliaus skirtuką **Darbo valandos** ir vykdykite nurodymus, pateiktus dalyje [Ištekliaus darbo valandų nustatymas](/dynamics365/field-service/set-work-hours-resource), kad būtų sukonfigūruotos kalendoriaus taisyklės.

**Naujo kalendoriaus šablono sukūrimas**

1. Nueikite į **Parametrai** \> **Kalendoriaus šablonas**.
2. Pasirinkite **Naujas** ir įveskite pavadinimą, aprašą bei šablono išteklių.

> [!NOTE]
> Kai išteklius yra nurodomas kalendoriaus šablone, ištekliaus kalendoriaus kopija susiejama su kalendoriaus šablonu. Jei nukopijuoto šablono darbo valandos pasikeičia, šie pakeitimai neišplatinami į kalendoriaus šabloną.

Dabar galite susieti darbo šabloną su projekto kalendoriaus šablonu.


[!INCLUDE[footer-include](../includes/footer-banner.md)]

