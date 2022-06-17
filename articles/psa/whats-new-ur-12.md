---
title: Kas nauja arba pakeista „Project Service Automation“ V3 12 atnaujintame leidime
description: Šiame straipsnyje pateikiama informacija apie tai, kas naujo "Project Service Automation Update Release 12", V3.
author: ruhercul
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
ms.reviewer: johnmichalak
ms.openlocfilehash: 28539b2e1331c8509e40aaf771f4d88d6f54e022
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8922646"
---
# <a name="project-service-automation-update-release-12-v3"></a>„Project Service Automation“ V3 12 naujinimo leidimas

[!include [banner](../includes/psa-now-project-operations.md)]

Džiaugiamės galėdami pranešti apie naujausią Dynamics 365 Project Service Automation (PSA) programos naujinimą. Šiame leidime yra kai kurių svarbių kokybės, veikimo ir naudojimo patobulinimų. Šis leidimas suderinamas su „Dynamics 365“ 9.x versija. Norėdami naujinti šį leidimą, eikite į „Dynamics 365“ administravimo centrą, tada eikite į sprendimų puslapį, iš kurio galite įdiegti naujinimą. Daugiau informacijos žr. [Pageidaujamo sprendimo diegimas, naujinimas arba šalinimas](/power-platform/admin/install-remove-preferred-solution).

Šiame straipsnyje išvardijamos naujos arba pakeistos "Project Service Automation V3", "Update Release 12" funkcijos ir pataisymai. Ši versija turi naują komponavimo versijos numerį V3.10.2.34 ir ją galima pasiekti per 2019 m. spalio mėn. automatinį naujinimą.

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
