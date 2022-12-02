---
title: Peržiūrėti siūlomus išteklius
description: Šiame straipsnyje pateikiama informacija apie tai, kaip siūlyti projekto išteklius.
author: ruhercul
ms.date: 08/18/2021
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 2a5b5159ceb8aa5b29dffad59517bc11fbf16871
ms.sourcegitcommit: 66e376675e6df8efc86fa84ec24e9aad6a980304
ms.translationtype: MT
ms.contentlocale: lt-LT
ms.lasthandoff: 07/21/2022
ms.locfileid: "9183985"
---
# <a name="review-proposed-resources"></a>Peržiūrėti siūlomus išteklius

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Išteklių valdytojai projektų vadovui gali pasiūlyti išteklius naudodami išteklių užklausą.

Norėdami peržiūrėti siūlomus išteklius, atlikite toliau nurodytus veiksmus.

1. Tinklelyje **Užklausa** arba pačios užklausos srityje pasirinkite **Rasti išteklius**.
2. Puslapyje **Grafiko planavimo pagalbinė priemonė** pasirinkite išteklių ir patvirtinkite, kad visos siūlomos valandos įtrauktos į siūlomą rezervavimą.
3. Srityje **Kurti išteklių rezervavimą** lauką **Rezervavimo būsena** nustatykite į **Pasiūlyta**, tada pasirinkite **Rezervuoti**.

    > [!NOTE]
    > Nustačius **Rezervavimo būsena** į **Pasiūlyta**, ištekliai nėra galutinai rezervuojami ir bendrieji ištekliai nepakeičiami į pavadintą komandos narį.

    Galimi šie būsenos naujinimai:

    - Puslapyje **Planavimo pagalbinė priemonė** būsenos indikatoriai atnaujinami, kad būtų rodoma, jog rezervacija yra pasiūlyta, o ne galutinai rezervuota.
    - Išteklių užklausoje užklausos užklausėjas turėtų pakeisti būseną į **Reikia peržiūrėti**.
    - Projekto skirtuke **Komanda** bendrosios komandos nario reikšmė **Užklausos būsena** automatiškai pakeičiama į **Reikia peržiūrėti**.

Projekto vadovas šį pasiūlymą gali priimti arba atmesti.

Kai išteklių valdytojas apdoroja išteklių užklausas, jis gali naudoti bet kurį iš toliau nurodytų metodų.

- Pasiūlyti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užpildytų pageidaujamas valandas. Tada pasiūlytos valandos padalinamos keliams ištekliams, kurie gali patenkinti pageidaujamas valandas. Tokiu atveju valandos negali persidengti.
- Pasiūlyti mažiau išteklių, nei pageidaujama. Tokiu atveju pasiūlytas išteklių pajėgumas yra mažesnis nei pageidaujamos valandos, kurias nurodė pageidaujantis asmuo. Kai pageidaujantis asmuo sutinka su pasiūlytais ištekliais, sukuriamas neįvykdytas išteklių reikalavimas, kurį taikant fiksuojama likusi poreikio dalis.
- Rezervuoti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užbaigtų darbą.
- Rezervuoti mažiau išteklių, nei pageidaujama. Tokiu atveju rezervuotų valandų yra mažiau nei pageidautų valandų. Sistema parodys, kaip pasiūlyti išteklius, o ne rezervacijas, kad pageidaujantis asmuo galėtų patikrinti ir stebėti likusią poreikio dalį.

## <a name="resource-availability"></a>Išteklių pasiekiamumą

Išteklių valdytojai tuiri peržiūrėti išteklių pasiekiamumą ir naujinti rezervacijas. Kai kuriais atvejais formalaus poreikio (išteklių užklausos) nėra. Tačiau išteklių valdytojas turi reaguoti į neplanuotą poreikį, gaunamą kitais kanalais, pvz., el. paštu, telefono skambučiais arba tiesioginiais pranešimais. Išteklių valdytojai naudoja **grafiko lentą** ir atnaujina išteklius bei rezervacijas.

Išteklių darbo valandos naudojamos kaip skaičiavimo pagrindas apskaičiuojant išteklių pasiekiamumą. Išteklių rezervacijos naudoja išteklių pajėgumą.

**Grafiko lentoje** naudojamos spalvos ir atspalviai, kuriais nurodomos rezervacijos, pasiekiamumas, per didelis rezervacijų kiekis ir rezervacijų būsena. Naudojant parametrą **Grafiko lenta** suteikiama galimybė pasirinkti legendą.

Jei dalyje **Grafiko lenta** šalia atskirų rezervuojamų išteklių rodoma rodyklė į dešinę, išteklius galima išplėsti, kad būtų rodoma darbo, kuriam rezervuotas išteklius, informacija.

Kadangi Dynamics 365 Project Operations naudoja Universal Resource Scheduling variklį, jei taip pat įdiegėte Dynamics 365 Field Service, galite peržiūrėti projektams, darbo užsakymams ir objektams, kuriuos išplėtėte planavimui, išteklių rezervacijų informaciją.

Norėdami peržiūrėti papildomą informaciją apie atskirus išteklius, spustelėkite dešiniu pelės klavišu, kad atidarytumėte išteklių kortelę.



[!INCLUDE[footer-include](../includes/footer-banner.md)]
