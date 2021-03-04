---
title: Kas nauja arba pakeista „Project Service Automation“ V3 12 atnaujintame leidime
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 12 atnaujintame leidime V3.
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom: dyn365-projectservice
ms.date: 02/04/2020
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
ms.openlocfilehash: daf0e6c7a4b1b953cb808cfefab74475c47d3996
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 02/10/2021
ms.locfileid: "5143838"
---
# <a name="project-service-automation-update-release-12-v3"></a>„Project Service Automation“ V3 12 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](https://docs.microsoft.com/power-platform/admin/install-remove-preferred-solution).

Šioje temoje išvardytos funkcijos ir pataisymai, kurie yra nauji arba pakeisti „Project Service Automation“ V3 12 atnaujintame leidime. Ši versija turi naują komponavimo versijos numerį V3.10.2.34 ir ją galima pasiekti per 2019 m. spalio mėn. automatinį naujinimą.

## <a name="update-release-12"></a>12 atnaujintas leidimas

### <a name="bug-fixes"></a>Ištaisytos klaidos

- Laikas ir išlaidos

    - Sutaisyta: laiko įrašų klaidų pranešimai turi labiau susijusį kontekstą.
    - Sutaisyta: laiko įrašų tinklelyje ir grafike tinkamai rodoma vertikali slinkties juosta, kai reikia.
    - Sutaisyta: pateiktas išlaidas ir laiko įrašus galima patvirtinti.
    - Sutaisyta: sutvarkytas atšaukimo patvirtinimo patvirtinimo dialogo lango pranešimas, kad atspindėtų patvirtinimo būseną, kai pakeičiama iš **Patvirtinta** į **Pateikta**.
    - Sutaisyta: laukai **Kaina**, **Vienetas** ir **Kiekis** dabar užrakinami išlaidų įraše po to, kai patvirtinami.

- Projektų valdymas

    - Sutaisyta: pašalintas **Naujas** veiksmas **Komandos narys** pagrindinėje formoje.
    - Sutaisyta: išteklių priskyrimai atnaujinti, kad reaguotų į netikslaus apvalinimo klaidas, dėl kurių pasikeičia užduoties pabaigos data.
    - Sutaisyta: užduočių tinklelyje su serveriu susijusios klaidos bus rodomos vartotojui.
    - Sutaisyta: komandos nario vardas, o ne pareigų pavadinimas dabar pateikiamas užduoties žmonių parinkiklyje.

- Išteklių valdymas

    - Sutaisyta: išteklių projektams reikalavimų išsami informacija, sukurta pagal šabloną, dabar naujo projekto kalendorių.
    - Sutaisyta: įgūdžiai ir kompetencijos dabar perkeliamos iš vaidmens pagrindinių duomenų į išteklių reikalavimą, sukurtą tam vaidmeniui.

- Sales

    - Sutaisyta: dubliuoti objekto ID, randami **Sutarties pagrindinėje** formoje.
    - Sutaisyta: logika buvo atnaujinta taip, kad skirtuke **Pasiūlymo analizė** būtų rodomi skirtuko sąrankos metaduomenys.
    - Sutaisyta: apskaitos data faktiniame įraše dabar gaunama iš laiko datos / išlaidų įrašo datos, o ne patvirtinimo datos.


[!INCLUDE[footer-include](../includes/footer-banner.md)]