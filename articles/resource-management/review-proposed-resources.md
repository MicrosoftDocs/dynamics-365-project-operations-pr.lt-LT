---
title: Peržiūrėti siūlomus išteklius
description: Šioje temoje pateikiama informacija apie tai, kaip siūlyti projekto išteklius.
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
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
ms.openlocfilehash: ad5cbdeb5fe05e6115eb024833a8d58b626ea4c9
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: lt-LT
ms.lasthandoff: 10/16/2020
ms.locfileid: "4080803"
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

## <a name="billable-utilization"></a>Apmokėtinas naudojimas

Ištekliai gali turėti tikslinį apmokėtiną naudojimą. Šis tikslinis naudojimas apibrėžiamas kaip atributas išteklių numatytame vaidmenyje arba nustatomas atskiro rezervuojamo ištekliaus įraše. Naudojimo skaičiavimai pagrįsti faktinėmis valandomis, apie kurias ištekliai pranešė naudodami patvirtintus laiko įrašus.

Naudojimo skaičiavimui naudojamos toliau nurodytos formulės.

- Apmokėtinas naudojimas = apmokestinamos faktinės valandos ÷ išteklių pajėgumas
- Neapmokėtinas naudojimas = faktinis laikas su apmokėtino tipo ID = neapmokestinamas, papildomas arba negalimas ÷ išteklių pajėgumas
- Vidinis = faktinis laikas be pardavimo sutarties ÷ išteklių pajėgumas
- Išteklių pajėgumas = išteklių darbo valandos – išvykęs – ne darbo dienos

Rodinį **Išteklių naudojimas** galite rasti skyde **Ištekliai**.

Kiekvienas tinklelio langelis nurodo išteklių apmokėtiną naudojimą pagal laiką, pavyzdžiui, dieną, savaitę arba mėnesį. Langeliams naudojamos toliau nurodytos spalvos.

- **Žalia:** apmokėtinas naudojimas \>= išteklių tikslinis naudojimas
- **Geltona:** tikslinis naudojimas – 20 \<= apmokėtinas naudojimas \< tikslinis naudojimas
- **Raudona:** apmokėtinas naudojimas \< tikslinis naudojimas – 20

Kadangi rodinys **Išteklių naudojimas** pagrįstas grafiko lenta, galite naudoti grafiko lentos filtravimo galimybes, kad filtruotumėte rezultatus.

Reikia, kad tinkleliui nustatytumėte tikslinį naudojimą arba pagal vaidmenį, arba individualų išteklių. Norėdami atlikti tokius nustatymus, eikite į **Ištekliai** \> **Išteklių vaidmenys**.

Be to, kiekvienam rezervuojamam ištekliui reikia priskirti numatytąjį vaidmenį. Eikite į **Ištekliai** \> **Ištekliai**. Skirtuke **Project Service** patikrinkite, kad nustatytas išteklių vaidmuo ir kad laukas **Yra numatytasis** nustatytas kaip **Taip**. Galite įtraukti papildomų vaidmenų, kai **Kaip numatytasis = ne**. Vaidmuo, kai **Yra numatytasis = taip** , naudojamas išteklių naudojimui įvertinti pagal to vaidmens tikslą.

Skirtuke **Project Service** taip pat galite ištekliui nustatyti individualų tikslinį naudojimą. Tada naudojimo skaičiavimui naudojamas šis tikslinis naudojamas, kad būtų įvertintas išteklių tikslas, o ne išteklių numatytojo vaidmens tikslas.

Išteklių naudojimas rodomas, tik jei šis išteklius turi patvirtintą ir apmokestinamą laiką periode, kuris rodomas tinklelyje.

## <a name="resource-availability"></a>Išteklių pasiekiamumą

Labai svarbu, kad išteklių valdytojai galėtų peržiūrėti išteklių pasiekiamumą ir naujinti rezervacijas. Kai kuriais atvejais nėra formalaus poreikio (išteklių užklausos), tačiau išteklių valdytojas turi reaguoti į neplanuotą poreikį, kurį gauna per tokius kanalus kaip el. paštas, telefono skambutis ar tiesioginis pranešimas. Išteklių valdytojai naudoja grafiko lentą, kad naujintų išteklius ir rezervacijas.

Išteklių darbo valandos naudojamos kaip išteklių pasiekiamumo skaičiavimo pagrindas. Išteklių rezervacijos naudoja išteklių pajėgumą.

Grafiko lentoje naudojamos spalvos ir atspalviai, kurie rodo rezervacijas, pasiekiamumą ir per daug rezervacijų, taip pat rezervacijų būseną. Grafiko lentos parametrai leidžia rodyti legendą.

Jei grafiko lentoje šalia atskiro rezervuojamo ištekliaus atsiranda į dešinę rodanti rodyklė, išteklių galima išplėsti, kad būtų rodoma darbo, kuriam rezervuotas išteklius, informacija.

Kadangi „Dynamics 365 Project Operations“ naudoja „Universal Resource Scheduling“ modulį, jei jūs taip pat esate įdiegę „Dynamics 365 Field Service“, galėsi peržiūrėti projektams skirtų išteklių rezervavimų, darbo užsakymų ir bet kokių kitų objektų, kuriuos išplėtėte planavimui, išsamią informaciją.

Norėdami peržiūrėti daugiau informacijos apie atskirą išteklių, spustelėkite dešiniu pelės klavišu, kad atidarytumėte išteklių kortelę.

