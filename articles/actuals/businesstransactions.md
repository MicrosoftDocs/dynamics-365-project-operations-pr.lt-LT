---
title: Verslo operacijos naudojant „Project Operations“
description: Šiame straipsnyje pateikiama "Microsoft" verslo operacijų koncepcijos apžvalga Dynamics 365 Project Operations.
author: rumant
ms.date: 01/31/2022
ms.topic: overview
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.assetid: ''
ms.search.region: ''
ms.search.industry: ''
ms.author: rumant
ms.search.validFrom: 2022-01-31
ms.openlocfilehash: fab0061af6e615c25d0fbf79d024370285dc6f86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923290"
---
# <a name="business-transactions-in-project-operations"></a>Verslo operacijos naudojant „Project Operations“

_**Taikoma kam:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniam diegimui – išankstinėms sąskaitoms faktūroms išrašyti_

Programoje "Microsoft" Dynamics 365 Project Operations *verslo operacija* yra abstrakti sąvoka, kurios neatstovauja joks objektas. Tačiau kai kuriems bendriesiems objektų laukams ir procesams gali būti naudojama verslo operacijų koncepcija. Ši abstrakti koncepcija naudojama toliau nurodytiems objektams.

- Pasiūlymo eilučių informacija
- Sutarties eilučių informacija
- Įvertinimo eilutės
- Žurnalo eilutės
- Faktinės

Iš šių objektų pasiūlymo eilutės informacija, sutarties eilutės informacija ir Įvertinimo eilutės susiejamos su *projekto gyvavimo ciklo įvertinimo etapu*. Žurnalo eilutės ir faktiniai objektai susiejami su *projekto gyvavimo ciklo vykdymo etapu*.

"Project Operations" visų penkių šių objektų įrašus laiko verslo sandoriais. Vienintelis skirtumas yra tas, kad objektų įrašai, susieti su įvertinimo etapu (pasiūlymo eilutės informacija, sutarties eilutės informacija ir Įvertinimo eilutės), laikomi *finansinėmis prognozėmis*, o objektų įrašai, susieti su vykdymo etapu (Žurnalo eilutės ir faktiniai duomenys), laikomi *finansiniais faktais*, kurie jau įvyko.

Norėdami sužinoti daugiau žr. [Įvertinimai](../project-management/estimating-projects-overview.md) ir [Faktiniai duomenys](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Unikalios verslo operacijų koncepcijos

Toliau nurodytos koncepcijos yra unikalios verslo operacijų koncepcijos:

- Operacijos tipas
- Operacijos klasė
- Operacijos kilmė
- Operacijos ryšys

### <a name="transaction-type"></a>Operacijos tipas

Operacijos tipas reiškia finansinio poveikio projektui laiką ir kontekstą. Jį apibrėžia parinkčių rinkinys, turintis šias palaikomas reikšmes projekto operacijose:

- Savikaina
- Projekto sutartis
- Neišrašytas pardavimas
- Išrašytas pardavimas
- Pardavimas tarp organizacijų
- Išteklių paskirstymo vieneto savikaina

### <a name="transaction-class"></a>Operacijos klasė

Operacijos klasė nurodo skirtingus projekto išlaidų tipus. Jį apibrėžia parinkčių rinkinys, turintis šias palaikomas reikšmes projekto operacijose:

- Laikas
- Išlaidos
- Medžiaga
- Rinkliava
- Etapas
- Mokesčiai

> [!NOTE]
> **Etapo** reikšmę paprastai naudoja verslo logika fiksuotos kainos atsiskaitymui projekto operacijose.

### <a name="transaction-origin"></a>Operacijos kilmė

Operacijos kilmė yra objektas, kuris saugo kiekvieno verslo sandorio kilmę, kad padėtų teikti ataskaitas ir atsekti. Kai prasideda projekto vykdymas, kiekvienas verslo sandoris sukuria kitą verslo sandorį, kuris savo ruožtu sukurs kitą verslo sandorį ir pan.

### <a name="transaction-connection"></a>Operacijos ryšys

Operacijos ryšys yra objektas, saugantis ryšį tarp dviejų panašių verslo operacijų, pvz., išlaidų ir susijusių pardavimo faktinių aplinkybių arba operacijų atšaukimų, kuriuos suaktyvina atsiskaitymo veikla, pvz., SF patvirtinimas arba SF taisymai.

Kartu operacijos kilmės ir operacijos ryšio objektai padeda sekti ryšius tarp verslo operacijų ir veiksmų, dėl kurių buvo sukurta konkreti verslo operacija.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
