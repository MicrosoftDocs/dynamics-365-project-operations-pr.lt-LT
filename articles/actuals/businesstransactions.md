---
title: Verslo operacijos naudojant „Project Operations“
description: Šiame straipsnyje pateikiama apžvalga apie verslo operacijų koncepciją programoje „Microsoft Dynamics 365 Project Operations“.
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

Programoje „Microsoft Dynamics 365 Project Operations“ *verslo operacija* yra abstrakti koncepcija, nereiškianti jokio objekto. Tačiau kai kuriems bendriesiems objektų laukams ir procesams gali būti naudojama verslo operacijų koncepcija. Ši abstrakti koncepcija naudojama toliau nurodytiems objektams.

- Pasiūlymo eilučių informacija
- Sutarties eilučių informacija
- Įvertinimo eilutės
- Žurnalo eilutės
- Faktinės

Iš visų šių objektų, Pasiūlymo eilučių informacija, Sutarties eilučių informacija ir Įvertinimo eilutės siejamos su projekto ciklo *įvertinimo etapu*. Žurnalo eilutės ir Faktinių duomenų objektai siejami su projekto ciklo *vykdymo etapu*.

„Project Operations“ šiuos visus penkis objektų įrašus traktuoja kaip verslo operacijas. Vienintelis skirtumas yra tas, kad objektų, susietų su įvertinimo etapu, įrašai (Pasiūlymo eilučių informacija, Sutarties eilučių informacija ir Įvertinimo eilutės) yra laikomi *finansinėmis prognozėmis* objektų, susietų su vykdymo etapu, įrašai (Žurnalo eilutės ir Faktiniai duomenys) – jau įvykusiais *finansiniais faktais*.

Norėdami sužinoti daugiau žr. [Įvertinimai](../project-management/estimating-projects-overview.md) ir [Faktiniai duomenys](actuals-overview.md).

## <a name="concepts-that-are-unique-to-business-transactions"></a>Unikalios verslo operacijų koncepcijos

Toliau nurodytos koncepcijos yra unikalios verslo operacijų koncepcijos:

- Operacijos tipas
- Operacijos klasė
- Operacijos kilmė
- Operacijos ryšys

### <a name="transaction-type"></a>Operacijos tipas

Operacijos tipas reiškia finansinio poveikio projektui laiką ir kontekstą. Tai apibrėžia parinkčių rinkinys, kuris programoje „Project Operations“ turi toliau nurodytas palaikomas reikšmes.

- Savikaina
- Projekto sutartis
- Neišrašytas pardavimas
- Išrašytas pardavimas
- Pardavimas tarp organizacijų
- Išteklių paskirstymo vieneto savikaina

### <a name="transaction-class"></a>Operacijos klasė

Operacijos klasė nurodo skirtingus projekto išlaidų tipus. Tai apibrėžia parinkčių rinkinys, kuris programoje „Project Operations“ turi toliau nurodytas palaikomas reikšmes.

- Laikas
- Išlaidos
- Medžiaga
- Rinkliava
- Etapas
- Mokesčiai

> [!NOTE]
> Verslo logikoje reikšmė **Etapas** paprastai naudojama „Project Operations“ fiksuotos kainos atsiskaitymams.

### <a name="transaction-origin"></a>Operacijos kilmė

Operacijos kilmė yra objektas, kuriame saugomi duomenys apie kiekvienos verslo operacijos kilmę, kad būtų galima lengviau teikti ataskaitas ir naudotis atsekamumo funkcija. Pradėjus vykdyti projektą, kiekviena verslo operacija sukuria kitą verslo operaciją, kuri sukurs dar kitą ir t. t.

### <a name="transaction-connection"></a>Operacijos ryšys

Operacijos ryšys – tai objektas, nusakantis ryšį tarp dviejų panašių verslo operacijų, pvz., savikainos ir susijusių pardavimo faktinių duomenų, arba operacijų atšaukimų, suaktyvinamų atsiskaitymo veiklomis, pvz., sąskaitos faktūros patvirtinimu arba sąskaitos faktūros koregavimu.

Kartu naudojami Operacijos kilmės ir Operacijos ryšio objektai padeda sekti ryšius tarp verslo operacijų ir veiksmų, dėl kurių kuriama konkreti verslo operacija.

[!INCLUDE[footer-include](../includes/footer-banner.md)]
