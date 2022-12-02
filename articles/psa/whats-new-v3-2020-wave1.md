---
title: Kas naujo arba pakeista programos „Project Service Automation“ 3.x wave 1 2020 versijoje
description: Šiame straipsnyje pateikiama informacijos apie tai, kas nauja ir pakeista „Project Service Automation“ 3 wave 1 2020 versijoje.
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
ms.reviewer: johnmichalak
ms.openlocfilehash: c762f2e7931046d32464cfa8486ef8405aa7d836
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 06/03/2022
ms.locfileid: "8928626"
---
# <a name="whats-new-or-changed-in-project-service-automation-version-3-wave-1-2020"></a>Kas naujo arba pakeista programos „Project Service Automation“ 3 wave 1 2020 versijoje

[!include [banner](../includes/psa-now-project-operations.md)]

Šiame straipsnyje aprašomi pagrindiniai naujinimai pereinant į naujausią „Project Service Automation“ (PSA) 3.x wave 1 2020 versijos leidimą.

## <a name="time-entry"></a>Laiko įrašas
Laiko įrašo patirtis išplėsta, kad laiko įrašo išplėtimo galimybes būtų galima įtraukti į daugiau kliento scenarijų. Tai apima galimybę įtraukti įrašų tipus, kuri dabar pasižymi nauju specifiniu elgesiu, pagrįstu lauko schemos pavadinimu **Laiko įrašo parametrai**, rodomu kaip **Laiko ištekliai**. Naujas sprendimas, vadinamas Laiku, išlaidomis, būsenų nustatymu ir patvirtinimais (santr. angl. TESA), buvo įtrauktas palaikyti šią funkciją.

### <a name="upgrade-consideration"></a>Pastabos dėl naujinimo
Norint palaikyti šią funkciją, PSA vaidmenys atnaujinti įtraukiant naujas teises. Šios teisės suteikia skaitymo prieigą prie naujo objekto, **Laiko įrašo parametrai**.

Vartotojams, kuriems reikia registruoti laiką, be esamų vaidmenų turi būti suteiktas vartotojo vaidmuo **Laiko įrašo vartotojas**. Šį vaidmenį sudaro naujos funkcijos ir jis užtikrina, kad laiko įrašas toliau veiks.

Be to, jei turite pasirinktinių programų modulių, kuriuose yra visos laiko įrašo objekto formos, turėsite iš modulio pašalinti **TESA laiko įrašo sparčiojo kūrimo forma**.

### <a name="currently-extended-time-entry-changes"></a>Neseniai išplėstų laiko įrašų pakeitimai
Kad būtų sumažintas poveikis esamiems vartotojo laiko įrašams, šis vaidmens pakeitimas yra vienintelis pagrindinis reikalavimas, būtinas norint naudoti laiko įrašą. Jei sukūrėte pasirinktinius rodinius arba atskiras laiko įrašo patirtis, laukus **Laiko įrašo parametras** turite nustatyti į teisingą PSA reikšmę.


[!INCLUDE[footer-include](../includes/footer-banner.md)]
