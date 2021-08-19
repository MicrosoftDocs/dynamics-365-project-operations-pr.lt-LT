---
title: Kas naujo arba pakeista programos „Project Service Automation“ 3.x wave 1 2020 versijoje
description: Šioje temoje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 3 wave 1 2020 versijoje.
ms.custom:
- dyn365-projectservice
ms.date: 05/15/2020
ms.topic: article
author: stsporen
ms.author: stsporen
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: a88b777c54ce54935d5483f616f3a24724ee192d40fbfd5d514f990e958dd5ea
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002116"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Kas naujo arba pakeista programos „Project Service Automation“ 3 wave 1 2020 versijoje

[!include [banner](../includes/psa-now-project-operations.md)]

Šioje temoje aprašomi pagrindiniai naujinimai pereinant į naujausią „Project Service Automation“ (PSA) 3.x wave 1 2020 versijos leidimą.

## <a name="time-entry"></a>Laiko įrašas
Laiko įrašo patirtis išplėsta, kad laiko įrašo išplėtimo galimybes būtų galima įtraukti į daugiau kliento scenarijų. Tai apima galimybę įtraukti įrašų tipus, kuri dabar pasižymi nauju specifiniu elgesiu, pagrįstu lauko schemos pavadinimu **Laiko įrašo parametrai**, rodomu kaip **Laiko ištekliai**. Naujas sprendimas, vadinamas Laiku, išlaidomis, būsenų nustatymu ir patvirtinimais (santr. angl. TESA), buvo įtrauktas palaikyti šią funkciją.

### <a name="upgrade-consideration"></a>Pastabos dėl naujinimo
Norint palaikyti šią funkciją, PSA vaidmenys atnaujinti įtraukiant naujas teises. Šios teisės suteikia skaitymo prieigą prie naujo objekto, **Laiko įrašo parametrai**.

Vartotojams, kuriems reikia registruoti laiką, be esamų vaidmenų turi būti suteiktas vartotojo vaidmuo **Laiko įrašo vartotojas**. Šį vaidmenį sudaro naujos funkcijos ir jis užtikrina, kad laiko įrašas toliau veiks.

Be to, jei turite pasirinktinių programų modulių, kuriuose yra visos laiko įrašo objekto formos, turėsite iš modulio pašalinti **TESA laiko įrašo sparčiojo kūrimo forma**.

### <a name="currently-extended-time-entry-changes"></a>Neseniai išplėstų laiko įrašų pakeitimai
Kad būtų sumažintas poveikis esamiems vartotojo laiko įrašams, šis vaidmens pakeitimas yra vienintelis pagrindinis reikalavimas, būtinas norint naudoti laiko įrašą. Jei sukūrėte pasirinktinius rodinius arba atskiras laiko įrašo patirtis, laukus **Laiko įrašo parametras** turite nustatyti į teisingą PSA reikšmę.


[!INCLUDE[footer-include](../includes/footer-banner.md)]