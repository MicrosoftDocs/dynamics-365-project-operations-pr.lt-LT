---
title: "\"Project Service Automation\" funkcijų pakeitimai į \"Project Operations\""
description: Šiame straipsnyje pateikiama funkcijų pakeitimų, skirtų Microsoft Dynamics 365 Project Service Automation į Dynamics 365 Project Operations.
author: ruhercul
ms.custom: dyn365-projectservice
ms.date: 02/03/2022
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
ms.openlocfilehash: 9869b3ad0fb6429484a26f367e06a0996f110ed8
ms.sourcegitcommit: a2d720ac6d7ddb20a0967fe87992a376b2478208
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/04/2022
ms.locfileid: "9621338"
---
# <a name="feature-changes-for-project-service-automation-to-project-operations"></a>"Project Service Automation" funkcijų pakeitimai į "Project Operations"

Sėkmingai atnaujinus projektą iš Microsoft Dynamics 365 Project Service Automation 3.X į Dynamics 365 Project Operations "Lite", projekto užduočių redaguoti užduočių tinklelio darbo paskirstymo struktūroje (WBS) neįmanoma. Klientai galės peržiūrėti PBS stebėjimo tinklelyje, į kurį įtraukti nauji laukai, kad pateiktų visą su užduotimi susijusią informaciją. Projektuose, kuriuose reikia redaguoti WBS, galite pasirinktinai konvertuoti reikalavimus atitinkančius projektus į naują projektą, kad galėtumėte planuoti žiniatinklį.

## <a name="project-conversion-process"></a>Projekto konvertavimo procesas

Norėdami konvertuoti projektą, atlikite šiuos veiksmus.

1. Atidarykite pagrindinį projekto puslapį ir veiksmų srityje pasirinkite **Konvertuoti**.
1. Patvirtinimo pranešimo laukelyje pasirinkite **Gerai**, kad pradėtumėte projekto konvertavimą. Atliekami šie veiksmai:

    1. Pranešimo juostoje, kuri rodoma pagrindiniame projekto puslapyje, nurodoma: "Projekto grafikas konvertuojamas. Negalite keisti projekto, kol konversija nebus baigta."
    1. Būsite nukreipti į projektų sąrašą.

    Užbaigus projekto konvertavimą, atliekami šie veiksmai:

    1. Paskirtas projekto vadovas gauna pranešimą dešinėje paraiškos pusėje.
    1. Pranešimų juosta, nurodanti, kad vyksta konversija, pašalinama.
    1. Skirtuke **Tvarkaraštis** rodoma nauja planavimo patirtis naudojant "Project", skirtą žiniatinkliui. Bet kuris vartotojas, turintis atitinkamas licencijas ir saugos vaidmenis, gali redaguoti WBS.
    1. Laukas **Planavimo modulis** atnaujinamas į **"Project", skirtą žiniatinkliui**.
    1. Mygtukas **Konvertuoti** pašalinamas iš veiksmų srities.

> [!IMPORTANT]
> Masinis projektų konvertavimas neleidžiamas. Bet koks bandymas atnaujinti didelį projektų kiekį tuo pačiu metu bus sužlugdytas. Šis apribojimas padeda užtikrinti aukštą našumą visiems klientams.

## <a name="manual-tasks-vs-automatic-tasks"></a>Neautomatinės užduotys ir automatinės užduotys

Kai aplinka atnaujinama iš "Project Service Automation" į "Project Operations", visos WBS užduotys laikomos automatiškai suplanuotomis. Rankiniu būdu suplanuotų užduočių koncepcija nepasiekiama "Project", skirtoje žiniatinkliui. Tačiau galite apibrėžti pageidaujamą projektų planavimo elgseną naudodami planavimo režimo [parametrą](/project-management/scheduling-modes.md), kai kuriate naujus projektus.

## <a name="restricted-operations-for-pre-conversion-projects"></a>Apribotos operacijos prieš konversiją vykdomiems projektams

Šiame skyriuje aprašomi funkciniai skirtumai, kurių galite tikėtis, kai projektai nebuvo konvertuoti.

### <a name="copy-project"></a>Kopijuoti projektą

Kopijavimo **operacija** palaikoma tik konvertuotuose projektuose. Naujovintų projektų negalima nukopijuoti prieš konversiją.

### <a name="move-project"></a>Perkelti projektą

Pakeitus projekto pradžios datą, užduočių pradžia nebus proporcingai perkelta, nebent projektas bus konvertuotas.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kuo skiriasi konvertuoti projektai ir nauji projektai, sukurti baigus naujinti versiją?

Projektams, kurie konvertuojami atnaujinus aplinkos versiją, bus nustatyta vėliavėlė, nurodanti grafikui laikytis tik projekto kalendoriaus. Šis elgesys atitinka "Project Service Automation" elgseną. Tačiau vėliavėlė nebus nustatyta naujiems projektams, kurie sukuriami atnaujinus versiją. Todėl tvarkaraštyje bus laikomasi išteklių darbo valandų, kai jie bus priskirti užduočiai.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Ką daryti, jei nepavyksta konvertuoti projekto?

Jei nepavyksta konvertuoti projekto, pirmiausia reikia peržiūrėti klaidų žurnalus, kad būtų galima nustatyti visas įprastas problemas, susijusias su jūsų WBS. Jei žurnaluose nenurodyta konkreti klaida, dėl kurios galite imtis veiksmų, susisiekite su klientų aptarnavimo tarnyba, kad jūsų atvejį būtų galima peržiūrėti toliau.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kaip įmonės uždarymas tvarkomas naudojant "Project for the Web"?

Žiniatinklio projektas neatsižvelgia į verslo uždarymus, kuriuos įmonė apibrėžia organizacijos lygiu. Tačiau jis gerbs kitų tipų poilsio dienas, apibrėžtas tam tikrame darbo valandos šablone.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kokie yra žiniatinklio projekto apribojimai?

Žiūrėkite [Darbo paskirstymo struktūros kūrimas: Projekto apribojimai](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Ar galiu tikėtis išlaidų ir pardavimo įvertinimų pakeitimų?

Retais atvejais, kai išteklių priskyrimo kontūrai perskaičiuojami arba kai jie patenka į kitą datos ribą nei šaltinio projektas, galite matyti pardavimo ir išlaidų įvertinimų skirtumus. Tikimasi, kad naujindami versiją klientai išbandys reprezentatyvų projektų imties rinkinį, kad galėtų suprasti visus galimus tvarkaraščio pakeitimus.
