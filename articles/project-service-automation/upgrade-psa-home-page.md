---
title: Pagrindinio puslapio atnaujinimas
description: Šioje temoje nurodoma, kur rasti svarbią informaciją apie naujas ir pakeistas „Dynamics 365 Project Service Automation“ funkcijas bei naujinimo į naujausią versiją procesą.
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 05/30/2019
ms.topic: article
ms.prod: ''
ms.technology: Dynamics 365 for Project Service 3.x
author: rumant
ms.assetid: c92d0849-e40c-4a56-9719-34030fbf5991
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 55f544636f39fc4faae06fdd512f859800bb7b44
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 03/24/2020
ms.locfileid: "3753731"
---
# <a name="upgrade-home-page"></a>Pagrindinio puslapio atnaujinimas

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

## <a name="upgrade-from-psa-version-2x-or-1x-to-version-3x"></a>Atnaujinti iš PSA versijos 2.x arba 1.x į versiją 3.x

### <a name="new-instances"></a>Nauji egzemplioriai

Nuo 2019 m. gegužės 17 d., kai kuriant naują egzempliorių pasirenkama „Project Service Automation“, pagal numatytuosius nustatymus įdiegiama 3.x versija.

### <a name="existing-instances"></a>Esami egzemplioriai

Anksčiau klientai, turintys PSA 2.x versijos egzempliorių ir kuriems reikia atnaujinti į 3.x versiją, kuri yra vieningąją kliento sąsaja (UCI) pagrįsta PSA versija, turėjo kreiptis į „Microsoft“ pagalbos tarnybą ir pateikti išsamią informaciją apie savo egzempliorių, kad pagalbos tarnyba galėtų nustatyti, kad egzempliorių būtų galima atnaujinti į 3.x versiją. Nuo 2020 m. kovo 1 d. klientai, kurie turi PSA 2.x versijos egzempliorių ir kuriems reikia naujinti į 3.x versiją, galės naujinti savo egzempliorius tiesiai iš administravimo portalo nesusisiekdami su „Microsoft“ pagalbos tarnyba.  

> [!NOTE]
> PSA 3.x versijoje yra reikšmingų pakeitimų. Ji sukurta naudojant vieningosios sąsajos sistemą siekiant užtikrinti patobulintą vartotojų patirtį. Pertvarkyta programa užtikrina nuoseklią, vienodą vartotojo sąsają (UI), kurią rengiant pasirinktas poreikius atitinkantis dizainas, kad būtų galima optimaliai peržiūrėti bet kokio dydžio ekrane arba bet kokiame įrenginyje. Programoje atlikta ir kitų pakeitimų. Kai kurios iš pakeistų sričių yra išteklių kainodara, rezervavimas ir priskyrimas, laikas, išlaidos ir patvirtinimai.

Prieš pradedant naujinimo procesą rekomenduojame atlikti šias užduotis:

- Patikrinkite, ar nustatytame egzemplioriuje yra įdiegta ir „Dynamics 365 Field Service“, ir „Project Service Automation“. Jei abu sprendimai įdiegti, prieš tęsdami įprastą egzemplioriaus naudojimą turėtumėte suplanuoti atnaujinti juos abu.
- Atidžiai peržiūrėkite toliau pateiktas temas. Žinodami apie versijų skirtumus ir juos suprasdami galėsite lengviau vykdyti atnaujinimo procesą. Šiose temose pateikta informacija apie svarbiausius PSA pakeitimus kartu su dalykais, į kuriuos reikia atsižvelgti, ir rekomendacijomis planuojant atnaujinimą į 3.x versiją.

    - [Kas nauja arba pakeista programos „Project Service Automation“ 3 versijoje](whats-new-changed-v3.md)
    - [Atnaujinimo aptarimas - iš „Project Service Automation“ 2.x arba 1.x versijos į 3 versiją](upgrade-v3.md)

- Prieš naujindami gamybos egzempliorius, atnaujinkite smėlio dėžės egzempliorius, kad įvertintumėte diegimo keitimus.

Kai peržiūrėsite temas, kurios buvo paminėtos anksčiau, ir būsite pasiruošę atnaujinti į PSA 3.x versiją arba UCI pagrįstą versiją, pateikite „Microsoft“ palaikymo tarnybai užklausą, kad atnaujinimas būtų pasiekiamas iš administravimo centro. Užklausoje nurodykite savo egzemplioriaus išsamią informaciją.

## <a name="older-versions-of-psa-psa-version-2x-in-a-newly-created-instance"></a>Senesnės PSA versijos (PSA 2.x versija) naujai sukurtame egzemplioriuje

Nuo 2019 m. gegužės 17 d. visų naujų egzempliorių numatytasis klientas bus UCI. Norint suderinti su šiuo pakeitimu, PSA 3.x versija ir „Field Service“ 8.x versija bus parengta pagal numatytuosius nustatymus, nes šios versijos skirtos darbui su UCI klientu.

Nuo 2020 m. kovo 1 d. „Dynamics“ PSA klientai nebegalės kurti naujų aplinkų naudodami senas PSA versijas, pavyzdžiui, PSA 2.x ir senesnes versijas. Bet kokią naują aplinką bus galima gauti tik naudojant PSA 3.x versiją.

> [!NOTE]
> Norėdami gauti geriausią patirtį, kai naudojatės senesnėmis „Field Service“ ir PSA programomis, eikite į puslapį **Sistemos parametrai** ir lauke **Naudoti tik naują vieningąją sąsają (rekomenduojama)** pasirinkite **Ne**, nes šios versijos nėra sukurtos taip, kad jas būtų galima tinkamai įkelti į UCI. Išjungę UCI, galite atidaryti ir paleisti šias „Field Service“ ir PSA versijas naudodami senąjį žiniatinklio klientą. Instrukcijų apie tai, kaip išjungti UCI klientą, žr. [Tik vieningosios sąsajos įjungimas](../admin/enable-unified-interface-only.md).
