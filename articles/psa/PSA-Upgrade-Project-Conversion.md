---
title: "\"Project Service Automation to Project Operations\" projekto planavimo konvertavimo procesas"
description: Šiame straipsnyje apžvelgiami funkcijų pakeitimai, skirti Microsoft Dynamics 365 Project Service Automation ""Dynamics 365 Project Operations.
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
# <a name="project-service-automation-to-project-operations-project-scheduling-conversion-process"></a>"Project Service Automation to Project Operations" projekto planavimo konvertavimo procesas

Sėkmingai atnaujinus projektą iš Microsoft Dynamics 365 Project Service Automation 3.X į Dynamics 365 Project Operations Lite, projekto užduočių tinklelio darbo paskirstymo struktūroje (WBS) redaguoti projekto užduočių neįmanoma. Klientai galės peržiūrėti WBS sekimo tinklelyje, į kurį buvo įtraukti nauji laukai, kad pateiktų visą su užduotimi susijusią informaciją. Projektams, kuriuos reikia redaguoti WBS, galite pasirinktinai konvertuoti reikalavimus atitinkančius projektus į naują projektą, kad galėtumėte planuoti žiniatinklyje.

## <a name="project-conversion-process"></a>Projekto konvertavimo procesas

Norėdami konvertuoti projektą, atlikite šiuos veiksmus.

1. Atidarykite pagrindinį projekto puslapį ir veiksmų srityje pasirinkite **Konvertuoti**.
1. Patvirtinimo pranešimo laukelyje pasirinkite **Gerai**, kad pradėtumėte projekto konvertavimą. Atliekami šie veiksmai:

    1. Pranešimų juostoje, kuri rodoma pagrindiniame projekto puslapyje, nurodoma: "Projekto grafikas konvertuojamas. Negalite keisti projekto, kol nebus baigta konversija."
    1. Esate nukreipiami į projektų sąrašą.

    Baigus projekto konversiją, atliekami šie veiksmai:

    1. Priskirtas projekto vadovas gauna pranešimą dešinėje paraiškos pusėje.
    1. Pranešimų juosta, nurodanti, kad vyksta konversija, pašalinama.
    1. Skirtuke **Grafikas** rodoma nauja planavimo patirtis naudojant "Project for the Web". Bet kuris vartotojas, turintis atitinkamas licencijas ir saugos vaidmenis, gali redaguoti WBS.
    1. Laukas **Planavimo modulis** atnaujinamas į **"Project", skirtą žiniatinkliui**.
    1. Mygtukas **Konvertuoti** pašalinamas iš veiksmų srities.

> [!IMPORTANT]
> Masinis projektų konvertavimas neleidžiamas. Bet koks bandymas vienu metu atnaujinti didelį projektų kiekį bus sužlugdytas. Šis apribojimas padeda užtikrinti aukštą našumą visiems klientams.

## <a name="manual-tasks-vs-automatic-tasks"></a>Neautomatinės užduotys ir automatinės užduotys

Kai aplinka atnaujinama iš "Project Service Automation" į "Project Operations", visos WBS užduotys laikomos automatiškai suplanuotomis. Neautomatiškai suplanuotų užduočių koncepcija negalima internetinėje "Project". Tačiau kurdami naujus projektus galite nustatyti pageidaujamą projektų planavimo veikimą naudodami planavimo režimo [parametrą](/project-management/scheduling-modes.md).

## <a name="restricted-operations-for-pre-conversion-projects"></a>Apribotos prieš konversiją vykdomų projektų operacijos

Šiame skyriuje aprašomi funkciniai skirtumai, kurių galite tikėtis, kai projektai nebuvo konvertuoti.

### <a name="copy-project"></a>Kopijuoti projektą

Kopijavimo **operacija** palaikoma tik konvertuotuose projektuose. Naujovintų projektų negalima nukopijuoti prieš konversiją.

### <a name="move-project"></a>Perkelti projektą

Pakeitus projekto pradžios datą, užduočių pradžia nebus proporcingai perkelta, nebent projektas bus konvertuotas.

## <a name="frequently-asked-questions"></a>Dažnai užduodami klausimai

### <a name="what-are-the-differences-between-converted-projects-and-new-projects-that-are-created-after-the-upgrade-has-been-completed"></a>Kuo skiriasi konvertuoti projektai ir nauji projektai, sukurti užbaigus naujinimą?

Projektams, kurie konvertuojami atnaujinus aplinkos versiją, bus nustatyta vėliavėlė, nurodanti grafikui laikytis tik projekto kalendoriaus. Šis veikimas atitinka "Project Service Automation" veikimą. Tačiau vėliavėlė nebus nustatyta naujiems projektams, sukurtiems atnaujinus versiją. Todėl grafikas atitiks išteklių darbo valandas, kai jie bus priskirti užduočiai.

### <a name="what-should-i-do-if-my-project-fails-to-be-converted"></a>Ką daryti, jei nepavyksta konvertuoti projekto?

Jei jūsų projekto nepavyksta konvertuoti, pirmiausia reikia peržiūrėti klaidų žurnalus, kad nustatytumėte visas įprastas problemas, susijusias su jūsų WBS. Jei žurnaluose nenurodyta konkreti klaida, dėl kurios galėtumėte imtis veiksmų, kreipkitės į klientų aptarnavimo tarnybą, kad jūsų atvejį būtų galima peržiūrėti toliau.

### <a name="how-are-business-closures-handled-in-project-for-the-web"></a>Kaip verslo uždarymas tvarkomas internetinėje "Project"?

"Project", skirta žiniatinkliui, nepaiso verslo uždarymų, kuriuos įmonė apibrėžia organizacijos lygiu. Tačiau jis gerbs kitų tipų poilsio dienas, apibrėžtas tam tikrame darbo valandos šablone.

### <a name="what-are-the-limitations-of-project-for-the-web"></a>Kokie yra "Project for the Web" apribojimai?

Žiūrėkite [Darbo paskirstymo struktūros kūrimas: Projekto apribojimai](/project-management/create-wbs#project-limitations.md).

### <a name="can-i-expect-changes-to-my-cost-and-sales-estimates"></a>Ar galiu tikėtis savo išlaidų ir pardavimo įvertinimų pokyčių?

Retais atvejais, kai išteklių priskyrimo kontūrai perskaičiuojami arba kai jie patenka į kitą datos ribą nei šaltinio projektas, galite matyti pardavimo ir išlaidų įvertinimų skirtumus. Tikimasi, kad atnaujinimo proceso metu klientai išbandys reprezentatyvų projektų pavyzdžių rinkinį, kad galėtų suprasti bet kokius galimus tvarkaraščio pakeitimus.
