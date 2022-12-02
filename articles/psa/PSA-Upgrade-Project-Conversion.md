---
title: Iš „Project Service Automation“ į „Project Operations“ projektų planavimo konvertavimo procesas
description: Šiame straipsnyje apžvelgiami funkcijos pakeitimai iš „Microsoft Dynamics 365 Project Service Automation“ į „Dynamics 365 Project Operations“.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 10/07/2022
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
ms.openlocfilehash: 84a40fcc9a8561c4ade0be175b08f701f3196508
ms.sourcegitcommit: 28004d38800782540fa5642d41f8fe0f6e2d9fa5
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/08/2022
ms.locfileid: "9642579"
---
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>Iš „Project Service Automation“ į „Project Operations“ projektų planavimo konvertavimo procesas

Sėkmingai atnaujinus projektą „Microsoft Dynamics 365 Project Service Automation“ iš 3.X į „Dynamics 365 Project Operations Lite“, redaguoti projekto užduočių darbo paskirstymo struktūros (WBS) tinklelyje neįmanoma. Klientai galės peržiūrėti WBS sekimo tinklelyje, kur įtraukti nauji laukai, kad pateiktų visą su užduotimi susijusią informaciją. Jei reikia projektų, kuriuose reikia redaguoti WBS, galite pasirinktinai konvertuoti tinkamus projektus į naują „Project for the web“, kad būtų galima planuoti.

## <a name="project-conversion-process"></a>Projektų konvertavimo procesas

Norėdami konvertuoti projektą, atlikite toliau pateikiamus veiksmus.

1. Atidarykite pagrindinį projekto puslapį ir veiksmų srityje pasirinkite **Konvertuoti**.
1. Rodomame patvirtinimo pranešime pasirinkite **Gerai**, kad pradėtumėte projekto konvertavimą. Atsitinka toliau nurodyti veiksmai:

    1. Pranešimų juosta, rodoma projekto pagrindiniame puslapyje: „Projekto grafikas konvertuojamas. Negalima atlikti pakeitimų, kol konvertavimas nebus baigtas.“
    1. Būsite nukreipti į projektų sąrašą.

    Atlikus projekto konvertavimą, gali būti atlikti šie veiksmai:

    1. Paskirtasis projekto vadovas gauna pranešimą dešinėje programos pusėje.
    1. Pranešimų juosta, kuri rodo, kad vyksta konvertavimas, pašalinama.
    1. Skirtuke **Grafikas** rodoma nauja „Project for the web" planavimo patirtis. WBS gali redaguoti bet kuris vartotojas, kuris turi atitinkamas licencijas ir saugos vaidmenis.
    1. Laukas **Planavimo modulis** atnaujintas į " **Project for the web"**.
    1. Mygtukas **Konvertuoti** pašalinamas iš veiksmų srities.

> [!IMPORTANT]
> Projektų masinis konvertavimas neleidžiamas. Bet koks bandymas tuo pat metu atnaujinti didelį projektų kiekį bus užblokuotas. Šis apribojimas padeda užtikrinti aukštą efektyvumą visiems klientams.

## <a name="manual-tasks-vs-automatic-tasks"></a>Rankinės užduotys ir automatinės užduotys

Kai aplinka atnaujinama iš „Project Service Automation" į “Project Operations", visos WBS užduotys laikomos suplanuotomis automatiškai. Rankiniu būdu suplanuotų užduočių sąvokos „Project for the web“ nėra. Tačiau kurdami naujus projektus galite apibrėžti pageidaujamą savo projektų planavimo veikimą naudodami [planavimo režimą](/project-management/scheduling-modes.md).

## <a name="restricted-operations-for-pre-conversion-projects"></a>Ribotos operacijos, taikomos išankstinio konvertavimo projektams

Šiame skyriuje aprašomi veikimo skirtumai, kurių galite tikėtis, kai projektai nebuvo konvertuoti.

### <a name="copy-project"></a>Kopijuoti projektą

Operacija **kopijuoti** palaikoma tik konvertuotų projektų atveju. Atnaujintų projektų negalima kopijuoti prieš konvertavimą.

### <a name="move-project"></a>Perkelti projektą

Jei projektas nėra konvertuotas, projekto pradžios datos pakeitimas proporcingai nepaveiks užduočių pradžios.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kokie yra skirtumai tarp konvertuotų projektų ir naujų projektų, sukurtų atlikus atnaujinimą?

Jei projektai konvertuojami atnaujinus aplinką, bus nustatyta žyma, nurodanti grafikui atsižvelgti tik į projekto kalendorių. Šis veikimas atitinka "Project Service Automation" veikimą. Tačiau nebus nustatyta naujų projektų, sukurtų po atnaujinimo, žyma. Todėl grafike bus paisomos išteklių darbo valandos, kai jie yra priskirti užduočiai.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Ką daryti, jei mano projekto konvertuoti nepavyksta?

Jei projekto konvertuoti nepavyksta, pirmasis veiksmas yra peržiūrėti klaidų žurnalus ir nustatyti bet kokias įprastas problemas, susijusias su jūsų WBS. Jei žurnalai nerodo konkrečios klaidos, dėl kurios galite imtis veiksmų, kreipkitės į klientų aptarnavimo tarnybą, kad atvejį būtų galima peržiūrėti toliau.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kaip įmonės ne darbo laiko išlaidos tvarkomos žiniatinklyje naudojant „Project for the web"?

„Project for the web“ neatsižvelgia į įmonės ne darbo laikotarpius, kuriuos įmonė apibrėžia organizacijos lygiu. Tačiau jis paisys kitų ne darbo valandų šablone apibrėžtų dienų tipų.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kokie yra „Project for the web“ funkcijos apribojimai?

Žr. [Sukurkite darbo paskirstymo struktūrą: Projekto apribojimai](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Ar galiu tikėtis išlaidų ir pardavimo verčių pakeitimų?

Kartais, kai perskaičiuojami išteklių kontūrai, arba kai jie patenka į kitą datos apribojimą nei šaltinio projektas, galite matyti pardavimo ir išlaidų verčių skirtumus. Plėtotės proceso metu klientai turėtų išbandyti tipinį projektų pavyzdžių rinkinį, kad jie galėtų suprasti visus galimus grafiko pakeitimus.
