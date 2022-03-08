---
title: Kaip tinkinti projekto etapų veiklos procesų sekas?
description: Peržiūra, kaip galima tinkinti projekto etapų veiklos procesų seką.
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 15540f524fb8fca8f69a2249f783289ba683cad7dabbf58ecbf620d147e5d491
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 08/06/2021
ms.locfileid: "7002971"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a>Kaip tinkinti projekto etapų veiklos procesų sekas?

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

Yra žinoma, kad ankstesnėse „Project Service“ programos versijose egzistuoja apribojimas, dėl kurio etapų pavadinimai projekto etapų veiklos procesų sekoje privalo būti lygiai tokie pat kaip ir numatytieji angliški pavadinimai (**Quote**, **Plan**, **Close**). Kitu atveju, verslo logika, kuri yra paremta angliškais etapų pavadinimais, neveiks tinkamai. Būtent dėl to negalite matyti žinomų ir projekto formoje galimų veiksmų, tokių kaip **Perjungti procesą** arba **Redaguoti procesą**, o veiklos procesų sekos tinkinimas nėra skatinamas. 

Šis apribojimas panaikintas 2.4.5.48 ir naujesnėse versijose. Šiame straipsnyje pateikiami siūlomi problemos sprendimai, skirti ankstesnėms versijoms, jei jums reikia tinkinti numatytąją veiklos procesų seką,  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a>Verslo logikai reikalingas tikslus jos ir angliškų etapų pavadinimų atitikimas

Į projekto etapų veiklos procesų seką įtraukta verslo logika, kuri yra šių veiksmų priežastis:
- Kai projektas yra susietas su pasiūlymu, kodu nustatomas veiklos procesų sekos etapas **Quote**.
- Kai projektas yra susietas su sutartimi, kodu nustatomas veiklos procesų sekos etapas **Plan**.
- Kai veiklos procesų seka yra perkeliama į etapą **Close**, projekto įrašas yra išjungiamas. Kai projektas yra išjungiamas, projekto forma ir darbo paskirstymo struktūra (WBS) nustatomi į režimą „tik skaityti“, įvardyti išteklių rezervavimai yra paleidžiami, o visi susieti kainoraščiai išjungiami.

Ši verslo logika yra paremta angliškais projekto etapų pavadinimais. Tokia priklausomybė nuo angliškų etapų vadinimų yra pagrindinė priežastis, kodėl nėra skatinamas projektų etapų veiklos procesų sekos tinkinimas, taip pat, kodėl projekto objekte negalite matyti bendrųjų veiklos procesų sekos veiksmų, pavyzdžiui, **„Perjungti procesą“** arba **„Redaguoti procesą“**.

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a>Kas nutinka, jei etapų pavadinimai neatitinka angliškų pavadinimų?

Jei „Project Service“ programos 1.x versijos 8.2 platformoje etapų pavadinimai veiklos procesų sekoje nėra lygiai tokie pat kaip ir angliški etapų pavadinimai, verslo logika, kuria nustatomi tinkami pasiūlymų ar kontraktų etapai, arba uždaromas projektas, yra praleidžiama. Joks klaidos pranešimas neparodomas. Todėl atrodytų, kad galite tinkinti projekto etapų veiklos procesų seką. Vis dėlto, negalėsite matyti jokių automatinių procesų, susijusių su pasiūlymais, sutartimis ir projekto uždarymu.

„Project Service“ programos 2.4.4.30 arba ankstesnės versijos 9.0 platformoje buvo atliktas esminis veiklos procesų sekos architektūros pakeitimas, kuriam buvo būtinas veiklos procesų sekos verslo logikos perrašymas. To rezultatas – jei proceso etapo pavadinimas ir numatytasis angliškas pavadinimas neatitinka, apie tai informuojama klaidos pranešimu. 

Todėl, norėdami tinkinti projekto objekto projekto etapų veiklos procesų seką, galite nebent prie projekto objekto numatytosios veiklos procesų sekos pridėti naujus etapus, **Quote**, **Plan** ir **Close** palikdami tokius, kokie jie yra. Dėl šio apribojimo būsite tikri, kad jūs negausite klaidų pranešimų dėl verslo logikos, pagal kurią veiklos proceso sekoje turi būti angliški pavadinimai.

Šiame straipsnyje aptariama verslo logika 2.4.5.48 arba naujesnėje versijoje bus pašalinta iš numatytosios projekto objekto veiklos procesų sekos. Atnaujinę savąją programą į šią arba naujesnę versiją galėsite tinkinti arba pakeisti numatytąją veiklos procesų seką savąja. 

## <a name="workarounds-for-earlier-versions"></a>Problemos sprendimai senesnėse versijose

Jei atnaujinti programos negalite, galimi du projekto objekto projekto etapų veiklos procesų sekos tinkinimo būdai:

1. Galite prie numatytosios konfigūracijos pridėti papildomus etapus, tuo pat metu palikdami angliškus etapų .**Quote**, **Plan** ir **Close** pavadinimus.


![Etapų pridėjimo prie numatytosios konfigūracijos ekrano nuotrauka.](media/FAQ-Customize-BPF-1.png)
 
2. Galite sukurti savąją veiklos procesų seką bei ją paversti pirmine projekto objekto veiklos procesų seka, kas leistų jums etapus vadinti taip, kaip norite. Tačiau jei norite naudoti tuos pačius standartinių projektų etapus **Quote**, **Plan** ir **Close**, turėsite atlikti keletą tinkinimų, po kurių bus pašalinti jūsų pasirinktiniai etapų pavadinimai. Dar sudėtingesnė yra projekto uždarymo logika, kurią vis vien galite sužadinti tiesiog išjungdami projekto įrašą.

![BPF tinkinimas.](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a>Kitos pastabos dėl „Project Service“ programos 2.4.4.30 arba ankstesnės versijos 9.0 platformoje

„Project Service“ 2.4.4.30 arba ankstesnės versijos 9.0 platformoje, naudojant pasirinktinę veiklos procesų seką, projekto objekto laukas **„Etapo pavadinimas“**, kuris yra naudojamas diagramoje **„Projektas pagal etapą“**, ir projekto sąrašo rodiniai neatsinaujins, nes jie yra susieti su numatytąja projekto etapų veiklos procesų seka. Šią problemą galite išspręsti atlikdami šiuos veiksmus:

- Įtraukite pasirinktinį lauką ir galėsite užfiksuoti dabartinį veiklos procesų sekos etapą, kuris yra naujinamas vartotojui žengiant per pasirinktinę veiklos procesų seką.

- Modifikuokite diagramą **Projektas pagal etapą** ir galėsite dirbti su savo pasirinktiniu lauku, o ne numatytąja konfigūracija.

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a>Asmeninės projekto objekto veiklos procesų sekos sukūrimo žingsniai

Norėdami sukurti asmeninę projekto objekto veiklos procesų seką atlikite šiuos veiksmus:

1. Eikite į **„Parametrai“** > **„Procesų centras“**. Nekopijuokite projekto etapų veiklos procesų eilės, nes tuomet bus nukopijuota ir „Project Service“ verslo logika.

  ![Proceso kūrimas.](media/FAQ-Customize-BPF-3.png)

2. Naudodami procesų kūrimo įrankį sukurkite norimus etapų pavadinimus. Jei norite, kad jūsų etapo funkcionalumas būtų toks pat kaip ir numatytųjų etapų **Quote**, **Plan** ir **Close**, kurti etapą turėsite remdamiesi savo pasirinktinės veiklos procesų eilės etapų pavadinimais.

   ![Procesų kūrimo įrankio, naudojamo veiklos procesų sekai tinkinti, ekrano nuotrauka.](media/FAQ-Customize-BPF-4.png) 

3. Įėję į procesų kūrimo įrankį, spustelėkite **„Užsakymo proceso seka“** tam, kad pasirinktinę veiklos procesų seką padarytumėte pirmine projekto objekto veiklos procesų seka, ką atliksite ją perkėlę į sąrašo viršų, virš projekto etapų veiklos procesų sekos.


   [Parinkties Užsakymo proceso seka naudojimo ekrano nuotrauka](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a>Šie veiksmai gali būti taikomi programos „Project Service“ 2.4.4.30 arba ankstesnės versijos 9.0 platformoje

4. Įtraukite naują pasirinktinį lauką į projekto objektą, kad užfiksuotumėte jūsų pasirinktinės veiklos procesų sekos pasirinktinius etapus. Jums reikės pridėti verslo logiką (priedas/darbo eiga) tam, kad šis laukas būtų atnaujinamas, kada atnaujinamas ir pasirinktinės veiklos procesų sekos etapas.

   ![Projekto objekto tinkinimo ekrano nuotrauka.](media/FAQ-Customize-BPF-6-720.png)

5. Modifikuokite diagramą **„Projektas pagal etapą“** ir galėsite naudoti savo naujuosius pasirinktinius laukus etapams.

   ![Diagramos Projektas pagal etapą naudojimo ekrano nuotrauka.](media/FAQ-Customize-BPF-7-720.png)

6. Modifikuokite visus projekto objekto rodinius kad etapams galėtumėte įtraukti savo naujuosius pasirinktinius laukus.

   ![Rodinių modifikavimo projekto objekte ekrano nuotrauka.](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]