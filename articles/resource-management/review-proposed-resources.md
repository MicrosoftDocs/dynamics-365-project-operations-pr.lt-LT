---
title: Peržiūrėti siūlomus išteklius
description: Šioje temoje pateikiama informacija apie tai, kaip siūlyti projekto išteklius.
author: ruhercul
manager: AnnBe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 54a0924da17eac86e2fa400540e629f6d803aa35
ms.sourcegitcommit: 14aa380759214713d9bf560f5a7f619b7f4bd5b8
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 11/05/2020
ms.locfileid: "4401183"
---
# <a name="review-proposed-resources"></a>Peržiūrėti siūlomus išteklius

_**Taikoma:** „Project Operations“ išteklių / ne atsargomis pagrįstiems scenarijams, „Lite“ visuotiniui diegimui – „Proforma“ sąskaitų faktūrų išrašymui_

Išteklių valdytojai projektų vadovui gali pasiūlyti išteklius naudodami išteklių užklausą.

1. Išteklių užklausos tinklelyje pažymėkite **Rasti išteklius**.
2. Puslapyje **Planavimo pagalbinė priemonė** pažymėkite išteklius, tada skyde **Kurti išteklių rezervaciją** lauke **Rezervacijos būsena** pažymėkite **Rezervuoti**.

Galimi šie būsenos naujinimai:

- Puslapyje **Planavimo pagalbinė priemonė** būsenos indikatoriai atnaujinami, kad rodytų, kad rezervacija yra pasiūlyta, o ne galutinai rezervuota.
- Išteklių užklausoje būsena pakeičiama į **Reikia peržiūrėti**.
- Projekto skirtuke **Komanda** bendrosios komandos nario reikšmė **Pageidauti būsenos** pakeičiama į **Reikia peržiūrėti**.

Projekto vadovas gali priimti arba atmesti pasiūlymą.

Kai išteklių valdytojas apdoroja išteklių užklausas, jis gali naudoti bet kurį iš toliau nurodytų metodų.

- Pasiūlyti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užpildytų pageidaujamas valandas. Tada pasiūlytos valandos padalinamos keliams ištekliams, kurie gali patenkinti pageidaujamas valandas. Tokiu atveju valandos negali persidengti.
- Pasiūlyti mažiau išteklių, nei pageidaujama. Tokiu atveju pasiūlytas išteklių pajėgumas yra mažesnis nei pageidaujamos valandos, kurias nurodė pageidaujantis asmuo. Todėl, kai pageidaujantis asmuo sutinka su pasiūlytais ištekliais, sukuriamas neįvykdytas išteklių reikalavimas, kuris fiksuoja likusią poreikio dalį.
- Rezervuoti kelis išteklius, kad patenkintų poreikį, jei nėra nei vieno atskiro ištekliaus, kuris užbaigtų darbą.
- Rezervuoti mažiau išteklių, nei pageidaujama. Tokiu atveju rezervuotų valandų yra mažiau nei pageidautų valandų. Sistema parodys, kaip pasiūlyti išteklius, o ne rezervacijas, kad pageidaujantis asmuo galėtų patikrinti ir stebėti likusią poreikio dalį.

## <a name="resource-availability"></a>Išteklių pasiekiamumą

Labai svarbu, kad išteklių valdytojai galėtų peržiūrėti išteklių pasiekiamumą ir naujinti rezervacijas. Kai kuriais atvejais nėra formalaus poreikio (išteklių užklausos), tačiau išteklių valdytojas turi reaguoti į neplanuotą poreikį, kurį gauna per tokius kanalus kaip el. paštas, telefono skambutis ar tiesioginis pranešimas. Išteklių valdytojai naudoja grafiko lentą, kad naujintų išteklius ir rezervacijas.

Išteklių darbo valandos naudojamos kaip išteklių pasiekiamumo skaičiavimo pagrindas. Išteklių rezervacijos naudoja išteklių pajėgumą.

Grafiko lentoje naudojamos spalvos ir atspalviai, kurie rodo rezervacijas, pasiekiamumą ir per daug rezervacijų, taip pat rezervacijų būseną. Grafiko lentos parametrai leidžia rodyti legendą.

Jei grafiko lentoje šalia atskiro rezervuojamo ištekliaus atsiranda į dešinę rodanti rodyklė, išteklių galima išplėsti, kad būtų rodoma darbo, kuriam rezervuotas išteklius, informacija.

Kadangi „Dynamics 365 Project Operations“ naudoja „Universal Resource Scheduling“ modulį, jei jūs taip pat esate įdiegę „Dynamics 365 Field Service“, galėsi peržiūrėti projektams skirtų išteklių rezervavimų, darbo užsakymų ir bet kokių kitų objektų, kuriuos išplėtėte planavimui, išsamią informaciją.

Norėdami peržiūrėti daugiau informacijos apie atskirą išteklių, spustelėkite dešiniu pelės klavišu, kad atidarytumėte išteklių kortelę.



[!INCLUDE[footer-include](../includes/footer-banner.md)]